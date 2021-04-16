---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (03 سبتمبر 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 3 سبتمبر 2020.
author: andreabichsel
ms.date: 09/03/2020
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
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 965f3ca859c601d26470038a889b0f21d2bdff5f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800107"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="b61b1-103">ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (3 سبتمبر 2020)</span><span class="sxs-lookup"><span data-stu-id="b61b1-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b61b1-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b61b1-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b61b1-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3504.</span><span class="sxs-lookup"><span data-stu-id="b61b1-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="b61b1-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم المرجع في  Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b61b1-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="b61b1-107">لمزيد من المعلومات حول الميزات القادمة في Human Resources، راجع [نظرة عامة حول الموجة 2 من إصدار 2019 لتطبيق Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span><span class="sxs-lookup"><span data-stu-id="b61b1-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="b61b1-108">لمزيد من المعلومات حول عملية تحديث Human Resources، راجع [عملية التحديث](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="b61b1-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="b61b1-109">في هذا الإصدار</span><span class="sxs-lookup"><span data-stu-id="b61b1-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="b61b1-110">نمط جديد للأبعاد المالية الافتراضية ومربعات الحوار في Human Resources (469495)</span><span class="sxs-lookup"><span data-stu-id="b61b1-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="b61b1-111">يتوفر الآن النمط الجديد للأبعاد المالية في النواحي التالية:</span><span class="sxs-lookup"><span data-stu-id="b61b1-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="b61b1-112">إجراءات المنصب (النموذج: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="b61b1-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="b61b1-113">أكواد أرباح كشف الرواتب (النموذج: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="b61b1-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="b61b1-114">لا تظهر الإدخالات في تقويم الإجازات في الشركة في حالة عدم تمكين تحسينات تقويم الإجازة والغياب (484406)</span><span class="sxs-lookup"><span data-stu-id="b61b1-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="b61b1-115">يعمل هذا الإصدار على تصحيح مشكلة حيث لا تظهر إدخالات الإجازات في تقوم الإجازات في الشركة.</span><span class="sxs-lookup"><span data-stu-id="b61b1-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="b61b1-116">تحدث هذه المشكلة فقط في حال عدم تمكين خيار إدارة الميزات **تحسينات تقويم الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="b61b1-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="b61b1-117">مشكلة BenefitPlanEmployeeEntity (467597)</span><span class="sxs-lookup"><span data-stu-id="b61b1-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="b61b1-118">يعمل هذا الإصدار على تصحيح مشكلة في الكيان **BenefitsPlanEmployee**.</span><span class="sxs-lookup"><span data-stu-id="b61b1-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="b61b1-119">عند استيراد تسجيلات العاملين، يتم الآن تعيين **كود التغطية** و **كود نوع الخطة** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="b61b1-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="b61b1-120">تؤدي هذه المشكلة إلى عرض خطط مزايا الموظف بشكل غير صحيح في نموذج **خطة ميزات العامل** وفي نموذج **تسجيل مفتوح** في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="b61b1-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="b61b1-121">إخراج 1094-C للملف الإلكتروني يفتقد حرفًا بتنسيق XML (435190)</span><span class="sxs-lookup"><span data-stu-id="b61b1-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="b61b1-122">يعمل هذا التغيير على تصحيح مشكلة في افتقاد ملف الإخراج إلى حرف مطلوب عند الإرسال إلى IRS.</span><span class="sxs-lookup"><span data-stu-id="b61b1-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="b61b1-123">جدول التعويض المتغير للموظف معيّن إلى نموذج التعويض الثابت (476117)</span><span class="sxs-lookup"><span data-stu-id="b61b1-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="b61b1-124">يؤدي هذا التغيير إلى مواءمة حقول التعويض الثابت مع نموذج التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="b61b1-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="b61b1-125">تتوفر الآن حقول التعويض المتغير فقط مع نموذج التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="b61b1-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="b61b1-126">طلبات الإجازة مسموح بها قبل التسجيل إذا كان لنوع الإجازة الحد الأدنى من الرصيد السالب (469917)</span><span class="sxs-lookup"><span data-stu-id="b61b1-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="b61b1-127">يمنع هذا التغيير إدخال طلبات الإجازة قبل التسجيل في الخطة، حتى عند وجود الحد الأدنى من الرصيد السالب في التسجيل.</span><span class="sxs-lookup"><span data-stu-id="b61b1-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="b61b1-128">يمكنك إدخال الطلبات أو تقديمها فقط عندما تكون الخطة نشطة.</span><span class="sxs-lookup"><span data-stu-id="b61b1-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="b61b1-129">يتعذر تنزيل قوالب المستندات (457279)</span><span class="sxs-lookup"><span data-stu-id="b61b1-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="b61b1-130">مع هذا التغيير، يمكنك الآن تنزيل كافة قوالب المستندات.</span><span class="sxs-lookup"><span data-stu-id="b61b1-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="b61b1-131">تظهر البيانات كرؤوس أعمدة بدلاً من صفوف لحقل معدل الدفع في تقرير خطة التعويض (476077)</span><span class="sxs-lookup"><span data-stu-id="b61b1-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="b61b1-132">يعرض تقرير التحليلات الآن معلومات **معدل الدفع** الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="b61b1-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b61b1-133">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="b61b1-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="b61b1-134">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="b61b1-134">Human Resources application in Teams</span></span>

<span data-ttu-id="b61b1-135">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b61b1-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b61b1-136">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="b61b1-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b61b1-137">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="b61b1-137">For more information, see:</span></span>

- <span data-ttu-id="b61b1-138">[تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬</span><span class="sxs-lookup"><span data-stu-id="b61b1-138">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="b61b1-139">[تطبيق Human Resources في Teams](https://go.microsoft.com/fwlink/?linkid=2127841) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-139">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="b61b1-140">تطبيق Human Resources في ميزات المعاينة لـ Teams</span><span class="sxs-lookup"><span data-stu-id="b61b1-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="b61b1-141">**الإخطارات**: سوف يتم إعلام المُرسلين والمعتمدين لطلبات الإجازات في تطبيق Human Resources في Teams.</span><span class="sxs-lookup"><span data-stu-id="b61b1-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="b61b1-142">سيتمكن الموافقون من الموافقة على طلبات الإجازة أو رفضها.</span><span class="sxs-lookup"><span data-stu-id="b61b1-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="b61b1-143">سيتم اعلام مقدمي الطلبات ما إذا تمت الموافقة على طلبهم أم رفضه.</span><span class="sxs-lookup"><span data-stu-id="b61b1-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="b61b1-144">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="b61b1-144">For more information, see:</span></span>
   - <span data-ttu-id="b61b1-145">[تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬</span><span class="sxs-lookup"><span data-stu-id="b61b1-145">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="b61b1-146">[تمكين الإعلامات لتطبيق Human Resources في Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-146">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="b61b1-147">[تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-147">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="b61b1-148">[إعلامات Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-148">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="b61b1-149">[عرض تقويم إجازة الفريق](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-149">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="b61b1-150">**تقويم إجازة المُدير**: سوف يتمكن المديرون من رؤية الإجازات المعتمدة والمعلقة لتقاريرهم المباشرة في طريقة عرض التقويم.</span><span class="sxs-lookup"><span data-stu-id="b61b1-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="b61b1-151">توفر طريقة العرض هذه طريقة سهلة في الفهم عند انقطاع أعضاء فريقهم عن العمل.</span><span class="sxs-lookup"><span data-stu-id="b61b1-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="b61b1-152">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="b61b1-152">For more information, see:</span></span>
   - <span data-ttu-id="b61b1-153">[تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬</span><span class="sxs-lookup"><span data-stu-id="b61b1-153">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="b61b1-154">[عرض تقويم إجازة الفريق](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-154">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="b61b1-155">خيار التكوين لوضع عناصر العمل المعينة لي في قائمة (477004)</span><span class="sxs-lookup"><span data-stu-id="b61b1-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="b61b1-156">يتوفر الآن خيار جديد الآن لوضع قائمة **عناصر العمل التي تم تعيينها لي** في العمود الأيسر في لوحه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="b61b1-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="b61b1-157">مع هذا التغيير، تظهر كافة عناصر العمل وقوائم المهام في نفس الناحية.</span><span class="sxs-lookup"><span data-stu-id="b61b1-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="b61b1-158">يمكنك تمكين هذه الوظيفة عن طريق تشغيل **المعاينة - تحسينات تجربة سير العمل** في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="b61b1-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="b61b1-159">للحصول على مزيد من المعلومات حول تشغيل ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="b61b1-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="b61b1-160">تقوم هذه الميزة أيضًا بترقية خيارات سير العمل التي تظهر في نماذج إجراءات العاملين.</span><span class="sxs-lookup"><span data-stu-id="b61b1-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="b61b1-161">تظهر خيارات سير العمل أيضًا أعلى علامة التبويب السريعة للإجراءات لتمكين الوصول السريع إليها.</span><span class="sxs-lookup"><span data-stu-id="b61b1-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="b61b1-162">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="b61b1-162">For more information, see:</span></span> 

- <span data-ttu-id="b61b1-163">[تحسينات في تجربة سير عمل إدارة المؤسسة والموظفين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬</span><span class="sxs-lookup"><span data-stu-id="b61b1-163">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![عناصر عمل تم تعيينها إلي](./media/hr-workflow-work-items-assigned-to-me.png)

![الوصول السريع إلى عناصر سير العمل](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="b61b1-166">قريبًا</span><span class="sxs-lookup"><span data-stu-id="b61b1-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="b61b1-167">تضمين كيانات قائمة الاختيار في Dataverse</span><span class="sxs-lookup"><span data-stu-id="b61b1-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="b61b1-168">ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b61b1-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="b61b1-169">أكواد سبب إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="b61b1-169">Benefits management reason codes</span></span>

<span data-ttu-id="b61b1-170">سيتم دمج أكواد سبب إدارة الميزات في وقت قريب مع أكواد السبب الموجودة في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b61b1-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="b61b1-171">إذا قمت بإنشاء أكواد أسباب في إدارة الميزات تزيد عن 15 حرفًا، فيجب تغيير اسم كود السبب في نموذج **أكواد السبب** في إدارة الميزات بحيث تتكون من 15 حرفًا أو أقل.</span><span class="sxs-lookup"><span data-stu-id="b61b1-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="b61b1-172">بعد تحديث الاسم، سيظهر كود السبب ضمن نموذج كود السبب في إدارة العاملين.</span><span class="sxs-lookup"><span data-stu-id="b61b1-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="b61b1-173">سيتوفر هذا التغيير في المستقبل ولن يؤثر علي الوظيفة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="b61b1-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="b61b1-174">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b61b1-174">See also</span></span>

[<span data-ttu-id="b61b1-175">الجديد أو المتغير في Human Resources</span><span class="sxs-lookup"><span data-stu-id="b61b1-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b61b1-176">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="b61b1-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b61b1-177">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="b61b1-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b61b1-178">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="b61b1-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]