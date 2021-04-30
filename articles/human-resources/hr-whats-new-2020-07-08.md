---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (08 يوليو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 8 يوليو 2020.
author: andreabichsel
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b277333ea37c2b6157ae9befc9d94f0e35ff97be
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891879"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>ما الجديد والمتغير في Dynamics 365 Human Resources (8 يوليو 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3382. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="database-logging"></a>تسجيل قاعدة البيانات

يسمح تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها. كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات. يمكنك استخدام إمكانيات تسجيل قاعده البيانات لرؤية هذه التغييرات بمرور الوقت. لمزيد من المعلومات، راجع [‏‫تكوين وإدارة تسجيل قاعده البيانات‬](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>تكوين اسم الخدمة الذاتية للموظف

في **معلمات الموارد البشرية**، يمكنك الآن تغيير اسم مساحة عمل **الخدمة الذاتية للموظف** ليصبح **الخدمة الذاتية**. لمزيد من المعلومات، راجع [تغيير اسم مساحة عمل الخدمة الذاتية للموظف](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>الوصول إلى التسجيل المفتوح لإدارة الميزات خارج الفترة

يعمل هذا الإصدار على إصلاح خطأ حيث يمكن للموظفين الوصول إلى التسجيل المفتوح للميزات خارج فترة التسجيل أو من دون حدث حياة. ونتيجة لذلك، إذا كنت بحاجة إلى عرض التسجيل المفتوح في الخدمة الذاتية للموظف، يجب تعديل تواريخ التسجيل المفتوح إلى اليوم (أو قبل ذلك) لتمكين الوصول إليه. يمكنك تغيير هذا الإعداد ضمن **إدارة الميزات > فترات القواعد والخيارات**.

## <a name="email-employee-enrollment-confirmation"></a>إرسال بريد إلكتروني لتأكيد تسجيل الموظف

يمكنك الآن إرسال رسائل بريد إلكتروني إلى الموظفين بعد إكمال تحديد ميزاتهم. يمكنك إرسال رسالة افتراضية أو استخدام قالب بريد إلكتروني للمؤسسة. توجد هذه الإعدادات ضمن **معلمات الموارد البشرية > إدارة الميزات**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>لا تزال الإجازة الملغية تظهر في الإجازة القادمة في مساحة عمل الأشخاص (441358)

لم تعد الإجازات الملغية تظهر كإجازات قادمة في بطاقات الإجازات في مساحة عمل **الأشخاص**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>غير قادر على استخدام خاصية كيان القسم في الكيان PositionV2 (456486)

يمكنك الآن إضافة قسم دون إنشاء علاقة مكررة.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>لا ينبغي لـ PayrollWorkerEnrolledBenefitDetailEntity إلا استخدام الحقل المحسوب لخطط التقاعد (459779)

عند تصدير الكيان **PayrollWorkerEnrolledBenefitDetailEntity**، يحدد التصدير ما إذا كان ينبغي استخدام حقل محسوب يستند إلى جدول أسعار أم استخدام الحقل **ContributionAmountCur** في الجدول المساعد. يستخدم المنطق الذي يستخدمه كيان البيانات جدول الأسعار في المواقف التي لا يتم فيها التطبيق بصورة طبيعية. يؤدي هذا المنطق إلى إرجاع صادرات الكيان إلى القيمة صفر لهذا العمود، وذلك نظرًا لعدم وجود جدول أسعار حساب وعدم إتاحة المنتج للعميل بتحديد واحد.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>الترجمات المحيرة في اللغة التشيكية لإدارة العاملين والخدمة الذاتية للموظف (400276)

يصحح هذا الإصدار الترجمات **لدليل الشركة** و **الدورة التدريبية المسجلة التالية** و **الوظيفة** و **المنصب**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>لا يحتوي الجدول WorkCalendarEmployment على حقول النظام المُمكَّنة التي تم إنشاؤها وتعديلها (460171)

حقول النظام التي تم إنشاؤها وتعديلها في الجدول **WorkCalendarEmployment** في الموارد البشرية قيد التمكين الآن.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>استثناء مرجع فارغ للتعيين وإضافة تفاصيل للموظف المستقبلي (455475)

يعمل هذا الإصدار على تصحيح خطأ (مرجع فارغ) في إدخال الموظف بشكل مبسط عند تعيين موظف باستخدام الخيار **للتعيين وإضافة تفاصيل**.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>لا يتم عرض التغييرات التي يتم إجراؤها على كيان عامل Dataverse في الموارد البشرية (455652)

ستظهر الآن التغييرات التي تم إجراؤها على الحقول التالية في كيان **العامل** في Dataverse في الموارد البشرية:

- **العمل من المنزل**
- **تاريخ الأقدمية**
- **تاريخ الذكرى السنوية**
- **تاريخ التوظيف الأصلي**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>لا يعتمد مستوى التعويض الصحيح افتراضيًا على الوظيفة المعينة للمنصب (394136)

وبهذا التغيير، تعتمد القيم الافتراضية لمستويات التعويضات الصحيحة على سجلات **تاريخ السريان** **لتفاصيل المنصب** و **تاريخ بدء** **تعيين خطة التعويض**.

## <a name="in-preview"></a>قيد المعاينة

## <a name="mandatory-fields"></a>حقول إلزامية 

يمكنك الآن جعل الحقول إلزامية باستخدام إمكانيات إضفاء طابع شخصي للموارد البشرية. تتطلب هذه الميزة **طرق عرض محفوظة**.

## <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا
 
يتم إصدار كيانات إدارة المزايا. تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة. كما سيتوفر قالب إدارة المزايا لنقل البيانات. يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.

## <a name="buy-and-sell-leave"></a>شراء الإجازة وبيعها 

توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها. غالبا ما تُدار هذه العملية يدويًا. تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية. إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء. لمزيد من المعلومات، راجع:

- [إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية

يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب. وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات. لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>إضافة مرفقات إلى طلبات الإجازة

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

## <a name="checklist-entities-included-in-dataverse"></a>تضمين كيانات قائمة الاختيار في Dataverse

ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]