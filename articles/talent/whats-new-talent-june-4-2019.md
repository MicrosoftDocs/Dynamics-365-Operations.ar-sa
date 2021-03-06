---
title: ما الجديد والمتغير في Dynamics 365 Talent (4 يونيو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4a42a3b817024447e2ff26cfcb3cdd0df1351158
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528018"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>ما الجديد والمتغير في Dynamics 365 Talent (4 يونيو 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>قريبًا في Attract

### <a name="job-approvals-on-the-home-page"></a>الموافقات على الوظائف في الصفحة الرئيسية

تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات. يمكن للمعتمدين مراجعة اعتماداتهم تحت **المعينة لك**. يعرض هذا القسم معرف الوظيفة والمسمي الوظيفي والمعتمدين الآخرين وتاريخ تعيين الوظيفة. يمكن للمستخدمين الذين يقومون بتقديم وظيفة للاعتماد مراجعة الوظائف الخاصة بهم تحت **طلبتها**. يعرض هذا القسم المعتمدين الذين يجب عليهم الموافقة علي الوظيفة المرسلة.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>صفحة جديدة للتحقق من صحة بيانات التدرج الهرمي للمناصب

بإمكان موظفي قسم الموارد البشرية (HR) والمسؤولين التحقق من صحة التدرج الهرمي الإداري لأي مراجع دائرية تم استيرادها بشكل غير مقصود. يمكنك الوصول إلى هذه الصفحة الجديدة من **الإدارة التنظيمية \> الارتباطات \> المناصب \> التحقق من صحة بيانات التدرج الهرمي للمناصب‬**.

### <a name="specify-reason-codes-on-leave-types"></a>تحديد أكواد الأسباب في أنواع الإجازات

قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة

قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلبات إجازة. قد يكون هذا الشرط موجودًا بسبب سياسة الشركة أو المتطلبات التنظيمية. يمكنك تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية

لا تؤدي القدرة على تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين فقط ولكنها تساعد أيضًا على ضمان منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) لتمكين موظفي الموارد البشرية من الاطلاع على الأسباب التي تكمن خلف أرصدة أيام الإجازات.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>لا يؤدي حذف سجل من Talent إلى إزالة السجل من Common Data Service

تتم الآن إزالة السجلات التي تمت إزالتها من Talent: Core HR من Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>خطة التعويض المتغير صالحة من/إلى التواريخ غير المسددة

في هذا الإصدار، لا يمكنك تسجيل موظف في خطة تعويض متغيرة إذا كان تاريخ البدء قبل تاريخ بدء الخطة أو تاريخ الانتهاء بعد تاريخ انتهاء الخطة. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>تتم إزالة تعليقات مراجعة الأداء عند تحديد المستخدمين "إلغاء"

يعمل هذا الإصدار علي تصحيح مشكلة إزالة تعليقات المراجعة في حالة بدء مستخدم في تغيير تعليق ثم تحديد **إلغاء**. 

## <a name="in-preview"></a>قيد المعاينة

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>لا يتم تمكين ميزات المعاينة إلا في مثيلات بيئة الاختبار المعزول

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو **إنتاج** أو **بيئة اختبار معزولة**. تسمح أنواع مثيلات **بيئة اختبار معزولة** بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختبار المعزولة**، اتصل بـ [الدعم](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>تقييد أنواع الإجازات في طلب أيام الإجازات

يمكن للمؤسسات تقديم العديد من الأنواع المختلفة من الإجازات إلى الموظفين. ولكن، قد لا يكون مناسبًا للموظفين تقديم طلبات الإجازات لبعض أنواع الإجازات. قد تتم إدارة أنواع الإجازات هذه بواسطة الموارد البشرية بدلاً من ذلك. يمكنك في هذا الإصدار تكوين أنواع الإجازات التي يمكن للموظفين تقديم طلبات أيام الإجازة لها. 

## <a name="coming-soon-in-core-hr"></a>قريبًا من Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>عرض معلومات موسعة حول الأداء في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار المراجعات الجديدة التي يشارك موظفيهم في إدارتها. وبالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة. 

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

سيتمكن الموظفون والمديرون وموظفي الموارد البشرية من طباعة مراجعة أداء الموظف.


[!INCLUDE[footer-include](../includes/footer-banner.md)]