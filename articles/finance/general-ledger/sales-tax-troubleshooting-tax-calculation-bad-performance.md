---
title: يؤثر أداء حساب الضريبة على المعاملات
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها المرتبطة بأداء حساب الضريبة وتاثيرها علي الحركات.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 2bb1f22c33de52f9a7bc00b450ce131d4d58d200
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352824"
---
# <a name="tax-calculation-performance-affects-transactions"></a>يؤثر أداء حساب الضريبة على المعاملات

[!include [banner](../includes/banner.md)]

في بعض الأحيان تتاثر الحركة بمشكلات الأداء التي يواجهها حساب الضريبة. لاستكشاف هذه المشكلة وإصلاحها، اتبع الخطوات الواردة في الأقسام التالية عند الضرورة.

## <a name="review-the-transaction-line-count"></a>راجع عدد بنود الحركة

حدد ما إذا كانت الحركة تحتوي علي عدد كبير من البنود (علي سبيل المثال، أكثر من مئات). وإذا لم يكن موجودا، فقم بالانتقال إلى القسم التالي. إذا كان للحركة عده بنود مئات، قم بتاخير حساب الضريبة. لمزيد من المعلومات، راجع [تمكين حساب الضريبة المؤجلة على دفاتر اليومية](enable-delayed-tax-calculation.md). 

بعد ذلك، يمكنك تحديد ما إذا كان سيتم استيفاء اي من الشروط التالية:

- هناك حركات مستورده من ملفات كبيره.
- وتعالج جلسات العمل المتعددة نفس حساب ضريبة الحركة في نفس الوقت.
- تحتوي الحركة علي عده بنود، ويتم تحديث طرق العرض في الوقت الحقيقي. على سبيل المثال، يتم تحديث حقل **مبلغ ضريبة المبيعات المحسوب** في صفحة **دفتر اليومية العام** في الوقت الفعلي عند تغيير حقول البند.

   [![حساب حقل مبلغ ضريبة المبيعات في صفحة إيصال دفتر اليومية.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

في حاله استيفاء اي من هذه الشروط، قم بتاخير حساب الضريبة.

## <a name="review-the-call-stack"></a>مراجعه مكدس الاستدعاءات

قم بمراجعه مكدس الاستدعاءات لتحديد ما إذا كان سيتم استدعاء حساب الضريبة عده مرات. وإذا لم يكن موجودا، فقم بالانتقال إلى القسم التالي. إذا تم استدعاء مكدس الاستدعاءات عده مرات، اتبع هذه الخطوات للمساعدة في تقليل أوقات حساب الضريبة.

1. إذا كان دفتر اليومية يعتبر الحركة، فقم بتاخير حساب الضريبة. لمزيد من المعلومات، راجع [تمكين حساب الضريبة المؤجلة على دفاتر اليومية](enable-delayed-tax-calculation.md).
2. إذا كانت المعاملة عبارة عن أمر شراء، وكان إصدار التطبيق أحدث من 10.0.15، فيمكنك تأخير حساب الضريبة حتى الحساب النهائي عن طريق تمكين الطيران لـ **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>مراجعه جدول زمني مكدس الاستدعاءات

قم بمراجعه المخطط الزمني لمكدس الاستدعاءات لتحديد ما إذا كانت المشاكل التالية موجودة ام لا. إذا فعلوا ذلك، قم بتمكين الطيران لـ **TaxUncommittedDoIsolateScopeFlighting** لحل المشكلة.

- تؤدي الحركة إلى توقف النظام عن الاستجابة حتى تنتهي الجلسة. التالي، لا يمكن للحركة ان تحسب نتيجة الضريبة. يبين الرسم التوضيحي التالي مربع الرسالة "تم إنهاء الجلسة" والذي تتلقاه.

    [![رسالة انتهاء جلسة العمل.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- تستغرق أساليب **TaxUncommitted** وقت أطول من الطرق الأخرى. على سبيل المثال، في الرسم التوضيحي التالي، فإن أسلوب **TaxUncommitted::updateTaxUncommitted()** تستغرق 43347.42 ثانية، لكن الطرق الأخرى تستغرق 0.09 ثانية.

    [![مدد الأساليب.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>تخصيص واستدعاء حساب الضريبة

عند التخصيص، لا تستدعي حساب الضرائب في أسلوب **insert()** أو **update()** لكل بند. يجب استدعاء حساب الضريبة على مستوى الحركة.

## <a name="determine-whether-customization-exists"></a>حدد ما إذا كان التخصيص موجودًا

إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا. في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
