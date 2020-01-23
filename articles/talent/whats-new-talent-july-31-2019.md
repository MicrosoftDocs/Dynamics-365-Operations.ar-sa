---
title: ما الجديد والمتغير في Dynamics 365 Talent (30 يوليو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96937d48e0d1003adbc5f7fedc89b2686ace01cd
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899008"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a>ما الجديد والمتغير في Dynamics 365 Talent (30 يوليو 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2409.


### <a name="region-support-for-canada-and-southeast-asia"></a>دعم المنطقة لكندا وجنوب شرق آسيا

يسرنا الإعلان عن توفر كندا ومناطق جنوب شرق آسيا لتطبيق Talent في الأول من أغسطس 2019. مع هذا التغيير، يمكنك إنشاء بيئات في المناطق الكندية والآسيوية، وستتم المحافظة على بيانات Talent كلها داخل تلك المواقع فقط. يمكنك إنشاء بيئة في هذه المناطق الجديدة عن طريق تحديد الموقع في مربع حوار "بيئة جديدة" واستخدام هذه البيئة لتزويد Talent في LCS كما هو موضح في [تزويد Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

ترحيل البيانات الخاصة بالمشاريع الموجودة من مناطق أخرى إلى المناطق الكندية والآسيوية غير مدعوم. يمكن تزويد المشاريع الجديدة فقط لهذه المناطق المدعومة الجديدة.

### <a name="new-active-positions-list-page"></a>صفحة قائمة المناصب النشطة الجديدة

تتضمن الآن الخيارات الخاصة بالقوائم المستندة إلى المناصب: **جميع المناصب** و**المناصب النشطة** و**المناصب الشاغرة** و**المناصب غير النشطة**. تعرض صفحة قائمة **المناصب النشطة** الجديدة فقط تلك المناصب، الشاغرة أو المشغولة، التي تكون نشطة اعتبارًا من التاريخ الحالي. 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a>السماح بإضافة المشاركين في الدورة التدريبية إلى دورات تدريبية مفتوحة

تعمل تغييرات هذا الأسبوع على مشكلة حيث كان باستطاعة بالمرؤوسين المباشرين فقط التسجيل لحضور دورات تدريبية مفتوحة.

### <a name="fte-analysis-displaying-incorrect-fte-number"></a>يعرض تحليل FTE رقم FTE غير صحيح

تم تصحيح **تحليل FTE** في علامة تبويب **التحليلات** في **إدارة العاملين‏‎**.

### <a name="final-comments-label-translation"></a>ترجمة تسمية التعليقات النهائية

تسمية **التعليقات النهائية** أصبحت الآن مترجمة في نموذج المراجعة.

## <a name="in-preview"></a>قيد المعاينة

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>لا يتم تمكين ميزات المعاينة إلا في مثيلات بيئة الاختبار المعزول

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو **إنتاج** أو **بيئة اختبار معزولة**. تسمح أنواع مثيلات **بيئة اختبار معزولة** بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختبار المعزولة**، اتصل بـ [الدعم](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>عرض معلومات موسعة حول الأداء في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار مراجعات جديدة. بالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة.
