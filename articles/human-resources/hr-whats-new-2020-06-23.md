---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (25 يونيو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 6/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8d83268292ac65d62cbe8fa9a4c146bf4af36b50
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555017"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>ما الجديد والمتغير في Dynamics 365 Human Resources (23 يونيو 2020)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3347. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>عند انتهاء صلاحية التسجيل لموظف تم إنهاؤه، يتم مسح نوع الإجازة والرصيد والمبلغ في نموذج ترك التسجيل (444867)

يتم الآن الاحتفاظ بالقيم الموجودة في **نوع الإجازة** و**الرصيد** و**المبلغ** بدلا من المسح عند القيام بهذا التحديد.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>الرصيد المتوقع غير صحيح عند تمكين ميزة جديدة (استحقاق المغادرة لشركة فردية أو خطة واحدة) (456553)

يتم عرض الرصيد المتوقع الصحيح الآن عند تمكين استحقاق المغادرة لشركة فردية أو خطة واحدة

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>الكيانات ذات العلاقات ينتج عنها خصائص تنقل مكررة (456486)

يعمل هذا الإصدار على تصحيح مشكلة في خصائص التنقل (العلاقة) لكيانات متعددة. تم الكشف عن العلاقات المكررة. تم تصحيح كافة هذه السيناريوهات.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>التعليقات عبر الشركات في مراجعة الأداء (455536)

التعليق عبر الشركات مرئية الآن في مراجعات الأداء مع هذا الإصلاح. يعمل هذا التغيير على تصحيح طريقة عرض تعليقات المراجع التي تم إدخالها في شركات مختلفة لنفس مراجعة الأداء.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>وجود عدم اتساق في إظهار بيانات إدارة التعويض (432562)

يتم الآن الاحتفاظ بعرض متسق لبيانات التعويض في الخدمة الذاتية للمدير. وفقا للطريقة التي تنتقل بها إلى **تفاصيل التعويض** الخاصة بالعامل، يتم الآن عرض بيانات التعويض بشكل متسق للمديرين.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>يتم تعيين تاريخ سريان خطة التعويض الثابتة على تاريخ اليوم بشكل افتراضي (411994)

يعتمد تاريخ بدء التعويض الآن على تاريخ بداية المنصب الذي يتم تعيينه للموظف.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>تعطيل تعريف نصف اليوم في نموذج الإجازة والغياب عند فتح النموذج (452607)

وبهذا التغيير، سيتم تمكين تعريف **تمكين نصف اليوم** حتى توجد حركات إجازة جديدة. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>يتعذر النشر إلى HcmDiscussionEntity عن طريق Excel؛ خطأ في حقل TotalRatingScore (453899)

يمكنك الآن تحديث حقل **TotalRatingScore** باستخدام **HCMDiscussionEntity** في مصمم مصنف Excel.

## <a name="in-preview"></a>قيد المعاينة

## <a name="database-logging"></a>تسجيل قاعدة البيانات

يسمح تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها. كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات. يمكنك استخدام إمكانيات تسجيل قاعده البيانات لرؤية هذه التغييرات بمرور الوقت. لمزيد من المعلومات، راجع [‏‫تكوين وإدارة تسجيل قاعده البيانات‬](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>حقول إلزامية 

يمكنك الآن جعل الحقول إلزامية باستخدام إمكانيات إضفاء طابع شخصي للموارد البشرية. تتطلب هذه الميزة **طرق عرض محفوظة**.

## <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا
 
يتم إصدار كيانات إدارة المزايا. تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة. كما سيتوفر قالب إدارة المزايا لنقل البيانات. يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.

## <a name="buy-and-sell-leave"></a>شراء الإجازة وبيعها 

توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها. غالبا ما تُدار هذه العملية يدويًا. تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية. إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء. لمزيد من المعلومات، راجع:

- [إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية

يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب. وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات. لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>إضافة مرفقات إلى طلبات زمن التوقف‬

تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي. يمكن للموظفين الآن إضافه هذه المرفقات. كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات. لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>إضافة كود السبب إلى تعليقات الاستحقاق 

تمت إضافه أكواد السبب إلى تعليق الاستحقاق.

## <a name="carry-forward-rules"></a>قواعد نقل الإجازة 

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>تعليق استحقاق الإجازه لأنواع الإجازات المحددة

يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة. يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك. يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>يتوفر كيان DMF لتعليقات الاستحقاق 

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="coming-soon"></a>قريبًا

## <a name="configure-the-name-of-employee-self-service"></a>تكوين اسم خدمة الموظف الذاتية

سيتوفر خيار جديد في **معلمات الموارد البشرية** لتحديث اسم مساحة عمل خدمة الموظف الذاتية إلى الخدمة الذاتية.

## <a name="checklist-entities-included-in-common-data-service"></a>تضمين كيانات قائمة الاختيار في Common Data Service

ستتوفر كيانات قائمة الاختيار الخاصة بعمليات إلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبا في Common Data Service.

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)