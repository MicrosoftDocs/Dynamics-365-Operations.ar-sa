---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (03 سبتمبر 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 3 سبتمبر 2020.
author: andreabichsel
manager: tfehr
ms.date: 09/03/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1cf348425cba71024ee0d158d42bb1071260d09
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467689"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (3 سبتمبر 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3504. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم المرجع في  Lifecycle Services (LCS).

لمزيد من المعلومات حول الميزات القادمة في Human Resources، راجع [نظرة عامة حول الموجة 2 من إصدار 2019 لتطبيق Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). لمزيد من المعلومات حول عملية تحديث Human Resources، راجع [عملية التحديث](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>في هذا الإصدار

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>نمط جديد للأبعاد المالية الافتراضية ومربعات الحوار في Human Resources (469495)

يتوفر الآن النمط الجديد للأبعاد المالية في النواحي التالية:

- إجراءات المنصب (النموذج: **HcmPositionActionDetail**)
- أكواد أرباح كشف الرواتب (النموذج: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>لا تظهر الإدخالات في تقويم الإجازات في الشركة في حالة عدم تمكين تحسينات تقويم الإجازة والغياب (484406)

يعمل هذا الإصدار على تصحيح مشكلة حيث لا تظهر إدخالات الإجازات في تقوم الإجازات في الشركة. تحدث هذه المشكلة فقط في حال عدم تمكين خيار إدارة الميزات **تحسينات تقويم الإجازة والغياب**.

### <a name="benefitplanemployeeentity-issue-467597"></a>مشكلة BenefitPlanEmployeeEntity (467597)

يعمل هذا الإصدار على تصحيح مشكلة في الكيان **BenefitsPlanEmployee**. عند استيراد تسجيلات العاملين، يتم الآن تعيين **كود التغطية** و **كود نوع الخطة** بشكل صحيح. تؤدي هذه المشكلة إلى عرض خطط مزايا الموظف بشكل غير صحيح في نموذج **خطة ميزات العامل** وفي نموذج **تسجيل مفتوح** في الخدمة الذاتية للموظف.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>إخراج 1094-C للملف الإلكتروني يفتقد حرفًا بتنسيق XML (435190)

يعمل هذا التغيير على تصحيح مشكلة في افتقاد ملف الإخراج إلى حرف مطلوب عند الإرسال إلى IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>جدول التعويض المتغير للموظف معيّن إلى نموذج التعويض الثابت (476117)

يؤدي هذا التغيير إلى مواءمة حقول التعويض الثابت مع نموذج التعويض الثابت. تتوفر الآن حقول التعويض المتغير فقط مع نموذج التعويض المتغير.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>طلبات الإجازة مسموح بها قبل التسجيل إذا كان لنوع الإجازة الحد الأدنى من الرصيد السالب (469917)

يمنع هذا التغيير إدخال طلبات الإجازة قبل التسجيل في الخطة، حتى عند وجود الحد الأدنى من الرصيد السالب في التسجيل. يمكنك إدخال الطلبات أو تقديمها فقط عندما تكون الخطة نشطة.

### <a name="document-templates-dont-download-457279"></a>يتعذر تنزيل قوالب المستندات (457279)

مع هذا التغيير، يمكنك الآن تنزيل كافة قوالب المستندات. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>تظهر البيانات كرؤوس أعمدة بدلاً من صفوف لحقل معدل الدفع في تقرير خطة التعويض (476077)

يعرض تقرير التحليلات الآن معلومات **معدل الدفع** الصحيحة.

## <a name="in-preview"></a>قيد المعاينة

### <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع:

- [تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬
- [تطبيق Human Resources في Teams](https://go.microsoft.com/fwlink/?linkid=2127841) في وثائق Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>تطبيق Human Resources في ميزات المعاينة لـ Teams
 
-  **الإخطارات**: سوف يتم إعلام المُرسلين والمعتمدين لطلبات الإجازات في تطبيق Human Resources في Teams. سيتمكن الموافقون من الموافقة على طلبات الإجازة أو رفضها. سيتم اعلام مقدمي الطلبات ما إذا تمت الموافقة على طلبهم أم رفضه. لمزيد من المعلومات، راجع:
   - [تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬
   - [تمكين الإعلامات لتطبيق Human Resources في Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) في وثائق Human Resources
   - [تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) في وثائق Human Resources
   - [إعلامات Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) في وثائق Human Resources
   - [عرض تقويم إجازة الفريق](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) في وثائق Human Resources
 
- **تقويم إجازة المُدير**: سوف يتمكن المديرون من رؤية الإجازات المعتمدة والمعلقة لتقاريرهم المباشرة في طريقة عرض التقويم. توفر طريقة العرض هذه طريقة سهلة في الفهم عند انقطاع أعضاء فريقهم عن العمل. لمزيد من المعلومات، راجع:
   - [تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬
   - [عرض تقويم إجازة الفريق](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) في وثائق Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>خيار التكوين لوضع عناصر العمل المعينة لي في قائمة (477004)

يتوفر الآن خيار جديد الآن لوضع قائمة **عناصر العمل التي تم تعيينها لي** في العمود الأيسر في لوحه المعلومات. مع هذا التغيير، تظهر كافة عناصر العمل وقوائم المهام في نفس الناحية. يمكنك تمكين هذه الوظيفة عن طريق تشغيل **المعاينة - تحسينات تجربة سير العمل** في إدارة الميزات. للحصول على مزيد من المعلومات حول تشغيل ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).

تقوم هذه الميزة أيضًا بترقية خيارات سير العمل التي تظهر في نماذج إجراءات العاملين. تظهر خيارات سير العمل أيضًا أعلى علامة التبويب السريعة للإجراءات لتمكين الوصول السريع إليها. لمزيد من المعلومات، راجع: 

- [تحسينات في تجربة سير عمل إدارة المؤسسة والموظفين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬

![عناصر عمل تم تعيينها إلي](./media/hr-workflow-work-items-assigned-to-me.png)

![الوصول السريع إلى عناصر سير العمل](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>قريبًا

### <a name="checklist-entities-included-in-dataverse"></a>تضمين كيانات قائمة الاختيار في Dataverse

ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.

### <a name="benefits-management-reason-codes"></a>أكواد سبب إدارة الميزات

سيتم دمج أكواد سبب إدارة الميزات في وقت قريب مع أكواد السبب الموجودة في Human Resources. إذا قمت بإنشاء أكواد أسباب في إدارة الميزات تزيد عن 15 حرفًا، فيجب تغيير اسم كود السبب في نموذج **أكواد السبب** في إدارة الميزات بحيث تتكون من 15 حرفًا أو أقل. بعد تحديث الاسم، سيظهر كود السبب ضمن نموذج كود السبب في إدارة العاملين. سيتوفر هذا التغيير في المستقبل ولن يؤثر علي الوظيفة الموجودة.

## <a name="see-also"></a>راجع أيضًا

[الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]