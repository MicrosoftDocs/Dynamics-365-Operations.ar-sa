---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (14 ديسمبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 36eb5722a7bd98c404fb6c8f5bde407ab38ec28d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024012"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-december-14-2018"></a><span data-ttu-id="c17ee-103">ما الجديد أو المتغير في Dynamics 365 Talent: Core HR‏ (14 ديسمبر 2018)</span><span class="sxs-lookup"><span data-stu-id="c17ee-103">What's new or changed in Dynamics 365 Talent: Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c17ee-104">**الإصدار 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="c17ee-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="c17ee-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="c17ee-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="c17ee-106">التغييرات</span><span class="sxs-lookup"><span data-stu-id="c17ee-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="c17ee-107">دعم قانون الرعاية ميسورة التكلفة‬ (ACA) في الولايات المتحدة للنموذجين 1095-B و1095-C للسنة الضريبية 2018</span><span class="sxs-lookup"><span data-stu-id="c17ee-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="c17ee-108">في كل عام، يتوجب على كبار أصحاب العمل المعنيين (ALE) تزويد جميع الموظفين العاملين بدوام كامل بنماذج 1095-C.</span><span class="sxs-lookup"><span data-stu-id="c17ee-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="c17ee-109">بالإضافة إلى ذلك، إذا قدم صاحب العمل تغطية ذاتية التأمين، فيجب عليه تزويد الموظف العامل بدوام كامل أو جزئي، والمشمول بتغطية إحدى الخطط الصحية التي يقدمها له، بالنموذج 1095-C (إذا كان ينتمي إلى ALE) والنموذج 1095-B (إذا كان من صغار أصحاب العمل).</span><span class="sxs-lookup"><span data-stu-id="c17ee-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="c17ee-110">توفر هذه الميزة نماذج القابلة للطباعة للنموذجين 1095-C و1095-B.</span><span class="sxs-lookup"><span data-stu-id="c17ee-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="c17ee-111">أثناء الاستيراد، يتم تجاهل الحقل SubmittedByPersonId field على HcmPerfJournalEntity</span><span class="sxs-lookup"><span data-stu-id="c17ee-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="c17ee-112">عند استيراد/تصدير إدخالات دفتر يومية الأداء، يتم تجاهل الحقل **تم الإرسال بواسطة‬**.</span><span class="sxs-lookup"><span data-stu-id="c17ee-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="c17ee-113">مع هذا التغيير، ستعكس القيمة **تم الاستيراد/التصدير** القيمة الموجودة في الجدول أثناء التصدير، عند الاستيراد، سيتم تحديث النظام بالقيمة التي تم توفيرها في ملف الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="c17ee-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="c17ee-114">تعرض علامة تبويب التبويب "التحليلات" في مساحة العمل "الإجازة والغياب‬" الخطأ OpenConnectionError لغير أدوار مسؤولي النظام.</span><span class="sxs-lookup"><span data-stu-id="c17ee-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="c17ee-115">مع هذا التحديث، لن تظهر أي أخطاء عند فتح علامة التبويب **التحليلات** في مساحة عمل **الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="c17ee-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="c17ee-116">فشل خدمة الموظف الذاتية، التدرج الهرمي للمناصب في التنقل وصولاً إلى العقدة الأصلية</span><span class="sxs-lookup"><span data-stu-id="c17ee-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="c17ee-117">تم إجراء تغيير لتصحيح الخطأ "فشل الحصول على العقدة الأصلية" عندما تم تخصيص التدرج الهرمي للمناصب للظهور في مساحة عمل موجودة وتحديد منصب في التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="c17ee-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="c17ee-118">بإمكان "مسؤول النظام" رؤية علامة التبويب "كشف الرواتب" في صفحة "المناصب"</span><span class="sxs-lookup"><span data-stu-id="c17ee-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="c17ee-119">تم إجراء تغيير لتضمين العناصر الأمان الصحيحة في الامتياز الحالي: "الاحتفاظ بكشف رواتب العامل وتفاصيل المنصب‬–".</span><span class="sxs-lookup"><span data-stu-id="c17ee-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="c17ee-120">مع هذا التغيير، سيتوفر لمسؤول المرتبات‬، بشكل افتراضي، حق الوصول إلى حقول "كشف الرواتب‬" في صفحة المناصب.</span><span class="sxs-lookup"><span data-stu-id="c17ee-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="c17ee-121">خطأ أثناء إرسال مراجعة الأداء للمدير واستخدام العنصر النائب %Reviews.PerfPeriod% في إرشادات الإرسال</span><span class="sxs-lookup"><span data-stu-id="c17ee-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="c17ee-122">تم إجراء تغيير لتصحيح الخطأ "مرجع فارغ" عند استخدام العنصر النائب %Reviews.PerfPeriod% في إرشادات الإرسال.</span><span class="sxs-lookup"><span data-stu-id="c17ee-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="c17ee-123">يعرض تقرير Power BI للقوى العاملة خطأ عندما يكون تاريخ الأقدمية للعامل يومًا في سنة كبيسة</span><span class="sxs-lookup"><span data-stu-id="c17ee-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="c17ee-124">مع هذا التغيير، أصبحت الآن أيام السنة الكبيسة مدعومة في Power BI.</span><span class="sxs-lookup"><span data-stu-id="c17ee-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="c17ee-125">التكامل بين Core HR وAttract</span><span class="sxs-lookup"><span data-stu-id="c17ee-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="c17ee-126">تم إجراء تغيير لتحديث التكامل بين Core HR وAttract المتعلق بالمرشحين المراد توظيفهم.</span><span class="sxs-lookup"><span data-stu-id="c17ee-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="c17ee-127">لظهور المرشحين المراد توظيفهم في مساحة عمل **إدارة الموظفين**، يتم استخدام كيانات Common Data Service التالية:</span><span class="sxs-lookup"><span data-stu-id="c17ee-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="c17ee-128">استمارة التقديم للوظيفة</span><span class="sxs-lookup"><span data-stu-id="c17ee-128">Job Application</span></span>
- <span data-ttu-id="c17ee-129">يجب تعيين سبب الحالة إلى "قبول العرض"</span><span class="sxs-lookup"><span data-stu-id="c17ee-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="c17ee-130">توفير المرشحين وفرص التوظيف</span><span class="sxs-lookup"><span data-stu-id="c17ee-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="c17ee-131">المرشح</span><span class="sxs-lookup"><span data-stu-id="c17ee-131">Candidate</span></span>
-   <span data-ttu-id="c17ee-132">توفير معلومات عن المرشح</span><span class="sxs-lookup"><span data-stu-id="c17ee-132">Provides Candidate information</span></span>

<span data-ttu-id="c17ee-133">فرص التوظيف</span><span class="sxs-lookup"><span data-stu-id="c17ee-133">Job Opening</span></span>
-   <span data-ttu-id="c17ee-134">توفير معرف فرص التوظيف والمشاركين في فرص التوظيف</span><span class="sxs-lookup"><span data-stu-id="c17ee-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="c17ee-135">المشاركون في فرص التوظيف</span><span class="sxs-lookup"><span data-stu-id="c17ee-135">Job Opening Participants</span></span>
-   <span data-ttu-id="c17ee-136">توفير مدير التوظيف</span><span class="sxs-lookup"><span data-stu-id="c17ee-136">Provides Hiring Manager</span></span>

<span data-ttu-id="c17ee-137">عند إضافة مرشح إلى "إدارة الموظفين"، يمكن الآن استبعاد المرشح أيضًا باستخدام خيار جديد متوفرة على بطاقة المرشح.</span><span class="sxs-lookup"><span data-stu-id="c17ee-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c17ee-138">قريبًا</span><span class="sxs-lookup"><span data-stu-id="c17ee-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="c17ee-139">الإجازة والغياب: الإجازة المستقبلية وتوقع أرصدة الإجازة</span><span class="sxs-lookup"><span data-stu-id="c17ee-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="c17ee-140">مع التغييرات التي تم إدخالها للسماح للموظفين بتوقع زمن التوقف وتقديم طلبات زمن توقف في المستقبل من دون التأثير على أرصدة زمن التوقف الحالية لديهم، طرأ أيضًا تغيير على طريقة عرض أرصدة زمن التوقف.</span><span class="sxs-lookup"><span data-stu-id="c17ee-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="c17ee-141">يمثل الرصيد المتوفر المعروض حاليًا مقدار زمن التوقف المتوفر للطلبات بما في ذلك الاستحقاقات عبر اليوم الحالي وكافة طلبات الإجازات الموافق عليها حتى نهاية الوقت.</span><span class="sxs-lookup"><span data-stu-id="c17ee-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="c17ee-142">عند إصدار القدرة على التوقع، يعرض الرصيد التغييرات بحيث تكون الرصيد الحالي لزمن التوقف بما في ذلك الاستحقاقات عبر اليوم الحالي والطلبات عبر اليوم الحالي.</span><span class="sxs-lookup"><span data-stu-id="c17ee-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="c17ee-143">سوف يرى الموظفون والمدراء هذه الأرصدة المحدثة في الخدمة الذاتية للموظف والمدير على بطاقة **زمن التوقف** وفي نافذة **أرصدة زمن التوقف**.</span><span class="sxs-lookup"><span data-stu-id="c17ee-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="c17ee-144">سيرى مدراء الموارد البشرية هذه الأرصدة المحدّثة في مساحة عمل **الأشخاص** وفي نافذة **خطط الإجازات المعينة للموظف**.</span><span class="sxs-lookup"><span data-stu-id="c17ee-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="c17ee-145">مشكلات معروفة​</span><span class="sxs-lookup"><span data-stu-id="c17ee-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance"></a><span data-ttu-id="c17ee-146">تعيين الأخطاء في التكامل مع Finance</span><span class="sxs-lookup"><span data-stu-id="c17ee-146">Mapping errors in the integration with Finance</span></span>

<span data-ttu-id="c17ee-147">تم التعرف على المشكلات التالية في القالب الحالي لتمكين تكامل Talent مع Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c17ee-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 Finance.</span></span> <span data-ttu-id="c17ee-148">سيتم نشر قالب جديد في وقت قريب وسيتم تطبيقه على جميع مشاريع التكامل التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c17ee-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="c17ee-149">بالنسبة إلى مشاريع التكامل الموجودة، يمكن تحديث تعيينات المهام.</span><span class="sxs-lookup"><span data-stu-id="c17ee-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="c17ee-150">راجع الجدول التالي للاطلاع على التعيينات المحدّثة.</span><span class="sxs-lookup"><span data-stu-id="c17ee-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="c17ee-151">المهمة "تعيين مناصب الوظيفة إلى تعيين الوظيفة الرئيسية للمناصب" لا تدمج البيانات.</span><span class="sxs-lookup"><span data-stu-id="c17ee-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="c17ee-152">هذه مشكلة تجري دراستها حاليًا.</span><span class="sxs-lookup"><span data-stu-id="c17ee-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="c17ee-153">لا يوجد أي حل بديل في التعيين الحالي.</span><span class="sxs-lookup"><span data-stu-id="c17ee-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="c17ee-154">تحتاج مهمة "الأقسام إلى وحدة التشغيل" إلى تحديث التعيينات التالية.</span><span class="sxs-lookup"><span data-stu-id="c17ee-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="c17ee-155">حقل المصدر الموجود</span><span class="sxs-lookup"><span data-stu-id="c17ee-155">Existing source field</span></span>          | <span data-ttu-id="c17ee-156">حقل مصدر جديد</span><span class="sxs-lookup"><span data-stu-id="c17ee-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="c17ee-157">cdm_description (الوصف)</span><span class="sxs-lookup"><span data-stu-id="c17ee-157">cdm_description (Description)</span></span>  | <span data-ttu-id="c17ee-158">cdm_name (الاسم)</span><span class="sxs-lookup"><span data-stu-id="c17ee-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="c17ee-159">يجب أيضًا إضافة تعيين إضافي.</span><span class="sxs-lookup"><span data-stu-id="c17ee-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="c17ee-160">حدد آخر حقل **بلا** لإضافة التعيين التالي.</span><span class="sxs-lookup"><span data-stu-id="c17ee-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="c17ee-161">حقل المصدر</span><span class="sxs-lookup"><span data-stu-id="c17ee-161">Source field</span></span>                   | <span data-ttu-id="c17ee-162">حقل الوجهة</span><span class="sxs-lookup"><span data-stu-id="c17ee-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="c17ee-163">cdm_description (الوصف)</span><span class="sxs-lookup"><span data-stu-id="c17ee-163">cdm_description (Description)</span></span>  | <span data-ttu-id="c17ee-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="c17ee-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="c17ee-165">يجب أن تبدو التعيينات المحدّثة مماثلة للصورة التالية.</span><span class="sxs-lookup"><span data-stu-id="c17ee-165">The updated mappings should look like the following image.</span></span>

![مهمة الأقسام إلى وحدة التشغيل](./media/DepartmentMapping.png)


<span data-ttu-id="c17ee-167">تحتاج مهمة "الوظائف إلى تفاصيل الوظيفة" إلى تحديث التعيينات التالية.</span><span class="sxs-lookup"><span data-stu-id="c17ee-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="c17ee-168">حقل المصدر الموجود</span><span class="sxs-lookup"><span data-stu-id="c17ee-168">Existing source field</span></span>          | <span data-ttu-id="c17ee-169">حقل مصدر جديد</span><span class="sxs-lookup"><span data-stu-id="c17ee-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="c17ee-170">cdm_name (الاسم)</span><span class="sxs-lookup"><span data-stu-id="c17ee-170">cdm_name (Name)</span></span>                | <span data-ttu-id="c17ee-171">cdm_description (الوصف)</span><span class="sxs-lookup"><span data-stu-id="c17ee-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="c17ee-172">cdm_name (الوصف)</span><span class="sxs-lookup"><span data-stu-id="c17ee-172">cdm_name (Description)</span></span>         | <span data-ttu-id="c17ee-173">cdm_jobdescription(وصف الوظيفة)</span><span class="sxs-lookup"><span data-stu-id="c17ee-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="c17ee-174">يجب أن تبدو التعيينات المحدّثة مماثلة للصورة أدناه.</span><span class="sxs-lookup"><span data-stu-id="c17ee-174">The updated mappings should look like the image below.</span></span>

![مهمة "الوظائف إلى تفاصيل الوظيفة"](./media/JobMapping.png)

<span data-ttu-id="c17ee-176">تحتاج مهمة "العاملون إلى العمل" إلى تحديث التعيينات التالية.</span><span class="sxs-lookup"><span data-stu-id="c17ee-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="c17ee-177">حقل المصدر الموجود</span><span class="sxs-lookup"><span data-stu-id="c17ee-177">Existing source field</span></span>                 | <span data-ttu-id="c17ee-178">حقل مصدر جديد</span><span class="sxs-lookup"><span data-stu-id="c17ee-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="c17ee-179">cdm_emailaddress1 (عنوان البريد الإلكتروني 1)</span><span class="sxs-lookup"><span data-stu-id="c17ee-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="c17ee-180">cdm_primaryemailaddress (عنوان البريد الإلكتروني الرئيسي)</span><span class="sxs-lookup"><span data-stu-id="c17ee-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="c17ee-181">cdm_telephone1 (الهاتف 1)</span><span class="sxs-lookup"><span data-stu-id="c17ee-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="c17ee-182">cdm_primarytelephone (الهاتف الرئيسي)</span><span class="sxs-lookup"><span data-stu-id="c17ee-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="c17ee-183">يجب أيضًا تحديث حقل النوع.</span><span class="sxs-lookup"><span data-stu-id="c17ee-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="c17ee-184">حدد نوع التعيين **fn** (وظيفة) للنوع وحدّث تعيينات القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="c17ee-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="c17ee-185">قيمة Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c17ee-185">Common Data Service value</span></span>                   | <span data-ttu-id="c17ee-186">قيمة Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c17ee-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="c17ee-187">75440000</span><span class="sxs-lookup"><span data-stu-id="c17ee-187">75440000</span></span>                    | <span data-ttu-id="c17ee-188">ذكر</span><span class="sxs-lookup"><span data-stu-id="c17ee-188">Male</span></span>                                             |
| <span data-ttu-id="c17ee-189">75440001</span><span class="sxs-lookup"><span data-stu-id="c17ee-189">75440001</span></span>                    | <span data-ttu-id="c17ee-190">أنثى</span><span class="sxs-lookup"><span data-stu-id="c17ee-190">Female</span></span>                                           |
| <span data-ttu-id="c17ee-191">75440002</span><span class="sxs-lookup"><span data-stu-id="c17ee-191">75440002</span></span>                    | <span data-ttu-id="c17ee-192">بلا</span><span class="sxs-lookup"><span data-stu-id="c17ee-192">None</span></span>                                             | 
| <span data-ttu-id="c17ee-193">75440003</span><span class="sxs-lookup"><span data-stu-id="c17ee-193">75440003</span></span>                    | <span data-ttu-id="c17ee-194">غير محدد</span><span class="sxs-lookup"><span data-stu-id="c17ee-194">NonSpecific</span></span>                                      |

<span data-ttu-id="c17ee-195">يجب أن تبدو التعيينات المحدّثة مماثلة للصور التالية.</span><span class="sxs-lookup"><span data-stu-id="c17ee-195">The updated mappings should look like the following images.</span></span>

![مهمة "العاملون إلى العامل"](./media/WorkerMapping.png)

![تحويل حقل النوع](./media/WorkerTransform.png)
