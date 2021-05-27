---
title: لم يتم إنشاء سجل TaxTrans
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد عندما لا يتم إنشاء سجل TaxTrans.
author: qire
ms.date: 04/13/2021
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
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018771"
---
# <a name="taxtrans-record-isnt-generated"></a>لم يتم إنشاء سجل TaxTrans

[!include [banner](../includes/banner.md)]

إذا قمت بتحديد **ضريبة المبيعات المرحلة** لأحدي الحركات، ولكن كانت  **صفحه ضريبة المبيعات المرحلة** Yما لا تظهر إيه بنود ضريبة أو إذا كانت العلامة تفتقد لبند ضريبة، فربما لم يتم إنشاء سجل **TaxTrans**.

[![صفحه ضريبة المبيعات المرحلة التي لا تحتوي علي أصناف بند](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

لاستكشاف هذه المشكلة وإصلاحها، اتبع الخطوات الواردة في الأقسام التالية عند الضرورة.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>التحقق من ضريبة المبيعات قبل ترحيل الحركة

1. قبل ترحيل الحركة، في صفحة **ترحيل الفاتورة**، حدد **ضريبة المبيعات** للتحقق من الحساب.

    [![زر ضريبة المبيعات علي صفحه ترحيل الفاتورة](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. في صفحة **حركات ضريبة المبيعات المؤقتة**، راجع نتيجة الحساب. في حاله عدم حساب أي ضريبة، راجع [الضريبة التي لم يتم حسابها أو يكون مبلغ الضريبة صفرًا](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>البحث عن سجل TaxTrans في كافة ضرائب المبيعات المرحلة

1. انتقل إلى **الضريبة** \> **الاستعلامات والتقارير** \> **استعلامات ضريبة المبيعات** > **ضريبة المبيعات المرحلة**.
2. في عنوان عمود **الإيصال**، حدد رمز عامل التصفية للعثور على سجل **TaxTrans**.
3. إذا وجدت سجلات ضريبة المبيعات التي تبحث عنها، فتحقق من التاريخ. إذا كان التاريخ مختلفا عن تاريخ راس دفتر اليومية، قم بإنشاء طلب خدمه Microsoft للحصول علي دعم إضافي.

    [![صفحة ضريبة المبيعات المرحّلة](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>تدقيق التصحيح لمراجعه التفاصيل

1. للحصول على معلومات حول كيفية التصحيح وتحديد ما إذا كان قد تم إنشاء **TmpTaxWorkTrans** و **TaxUncommitted** بشكل صحيح، راجع [قيمة الحقل في TaxTrans غير صحيحة](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. في حالة إنشاء **TaxTmpWorkTrans** أو **TaxUncommitted** بشكل صحيح، أضف نقطة توقف **TaxPost::SaveAndPost()** و **Tax::SaveAndPost** لتصحيح سبب عدم إدراج **TaxTrans**.

    [![نقاط التوقف المضافة في التعليمات البرمجية](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![نتائج نقاط التوقف المضافة](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>حدد ما إذا كان التخصيص موجودًا

إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا. في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
