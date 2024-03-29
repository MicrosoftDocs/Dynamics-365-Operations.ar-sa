---
title: تحديد الفرضية وتحديد المقاييس الخاصة بتجربة
description: يوضح هذا المقال كيفيه تحديد مقاييس الفرضية والنجاح لتجربه تقوم بتشغيلها علي موقع ويب خاص بالتجارة الكترونيه في Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0b6bdf160522fc93e841ec2f8a4542ff80d8f67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852776"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>تحديد الفرضية وتحديد المقاييس الخاصة بتجربة
تتضمن المرحلة الاولي في دوره حياه التجربة تعريف الفرضية للتجربة وتحديد القياسات التي ستتعقبها لتقييم النجاح. يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في [اعداد وتشغيل تجربه](experimentation-overview.md)  علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce. وتتم تغطيه الخطوات الاضافيه في مقالات منفصلة. 

[ ![رحلة مستخدم التجربة - التحديد.](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

الفرضية هو البيان الذي يمكنك التنبؤ بنتيجة التجربة فيه. تنتقل العديد من العوامل إلى تعريف الفرضية، علي سبيل المثال، البحث عن سلوك المستخدم وبيانات موقع الويب التي قمت بتجميعها. باستخدام الفرضية، ستقوم بتعريف الافتراضات أو النظرية التي ترغب في التحقق من صحتها بتجربتك. قد يكون الهدف من المفترض هو ان تكون "*صوره لقميص أبيض علي الصفحة الرئيسية تؤدي إلى تحريك معدل تتبع الاستخدام أكثر من السترات الزرقاء اثناء شهور الصيف نظرا لان الأشخاص يرغبون في وجود شيء خفيف ولون خفيف في الصيف.*" في هذه الحالة، ستقوم بإنشاء التنوعات التي تتضمن القميص الأبيض والسترة الزرقاء، ونشر كل منهما في نفس الوقت.

للتحقق من صحة الفرضية، يجب أن يتم ربط نجاح أو فشل التجربة مباشرة بإجراءات المستخدم؛ على سبيل المثال، إذا قام مستخدم موقع ويب بالنقر فوق ارتباط أو زر. يجب ان تتوافق هذه الإجراءات مع الاحداث التي سيتم الاعلام عنها لتعقب خدمه الجهة الأخرى الخاصة بالتجربة. بمرور الوقت، سيتم تدوين النسبة المئوية للمستخدمين الذين ياخذون الاجراء كقياس يمكنك استخدامه لإنشاء تقارير واجراء تحليلات. لمراجعة جميع الأحداث والسمات المتوفرة، راجع [حداث مكونات Commerce للتشخيصات واستكشاف الأخطاء وإصلاحها‬](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>الخطوة السابقة
[الاختبار في Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>الخطوة التالية
[إعداد تجربة](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]