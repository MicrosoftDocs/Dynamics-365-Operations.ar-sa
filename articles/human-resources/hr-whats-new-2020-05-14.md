---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (14‏ مايو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
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
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d46671f73a75a9ed3a652d76153c923a3542b5f6
ms.sourcegitcommit: 7c750711e9fe1d3726c6ee650669529684933001
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386097"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="d383d-103">ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (14‏ مايو 2020)</span><span class="sxs-lookup"><span data-stu-id="d383d-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

<span data-ttu-id="d383d-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d383d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d383d-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="d383d-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="d383d-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم المرجع في  Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d383d-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="d383d-107">تغييرات النظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="d383d-107">Platform changes</span></span>

<span data-ttu-id="d383d-108">يتم تضمين تغييرات النظام الأساسي في إصدار هذا الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="d383d-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="d383d-109">لمزيد من المعلومات، راجع [تحديثات النظام الأساسي للإصدار 10.0.10 من تطبيقات Finance and Operations (مايو 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span><span class="sxs-lookup"><span data-stu-id="d383d-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="d383d-110">يتضمن هذا الإصدار إصلاحات الأخطاء والتغييرات التي تمت على طرق العرض المحفوظة.</span><span class="sxs-lookup"><span data-stu-id="d383d-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="d383d-111">تأكد من أن قوائم اختيار Common Data Service متسقة مع تعدادات الإجازات (436343)</span><span class="sxs-lookup"><span data-stu-id="d383d-111">Ensure Common Data Service picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="d383d-112">قوائم اختيار Common Data Service متسقة الآن مع تعدادات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="d383d-112">Common Data Service picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="d383d-113">السماح للمستخدمين بتكوين سير عمل طلب الإجازة استنادا إلى مقدار الطلب (300044)</span><span class="sxs-lookup"><span data-stu-id="d383d-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="d383d-114">يمكن للمستخدمين تكوين سير عمل طلبات الإجازة استنادا إلى مقادير الطلبات.</span><span class="sxs-lookup"><span data-stu-id="d383d-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="d383d-115">نموذج العامل الجديد يعرض البيانات عبر قائمة طرق العرض عند تمكين الأمان المتقدم (403185)</span><span class="sxs-lookup"><span data-stu-id="d383d-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="d383d-116">يصحح هذا الإصدار كيفية عمل عرض العاملين عبر الكيانات القانونية عند تمكين الوصول المتقدم ويمكن الوصول إلى العاملين في شركات أخرى.</span><span class="sxs-lookup"><span data-stu-id="d383d-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="d383d-117">السماح بتشغيل استحقاقات الإجازة لخطة فردية أو شركة فردية (318844)</span><span class="sxs-lookup"><span data-stu-id="d383d-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="d383d-118">مع هذا التغيير، يمكنك تشغيل استحقاقات لإحدى الشركات أو إحدى الخطط.</span><span class="sxs-lookup"><span data-stu-id="d383d-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="d383d-119">إظهار مكافئ الدوام الكامل (FTE) للمنصب في نموذج العمال المسجلين (414658)</span><span class="sxs-lookup"><span data-stu-id="d383d-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="d383d-120">وتحدد قيمة FTE من منصب العامل معدل استحقاق العامل عند تمكين الخيار FTE في نوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="d383d-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="d383d-121">يتم الآن تضمين هذا الحقل في نموذج **العاملين المسجلين** ومربع حوار **التسجيل الجماعي**.</span><span class="sxs-lookup"><span data-stu-id="d383d-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="d383d-122">إضافة وظيفة دفعية لانتهاء صلاحيه رصيد الإجازة (431266)</span><span class="sxs-lookup"><span data-stu-id="d383d-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="d383d-123">تتوفر الآن وظيفة دفعية جديدة يتم تشغيلها يوميًا.</span><span class="sxs-lookup"><span data-stu-id="d383d-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="d383d-124">وهي تقلل رصيد الإجازة المتبقي عندما تصبح تواريخ انتهاء الصلاحية حديثة.</span><span class="sxs-lookup"><span data-stu-id="d383d-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="d383d-125">تصدير جهات الاتصال الشخصية لأحد الموظفين باستخدام كيان شخص جهة الاتصال الشخصية للعامل لا يصدر جهات الاتصال الشخصية بنوع العلاقة الرئيسية (345893)</span><span class="sxs-lookup"><span data-stu-id="d383d-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="d383d-126">يتعذر على كيان بيانات **شخص جهة الاتصال الشخصية للعام** (**HcmPersonalContactPersonEntity** في DMF و **PersonalContactPerson** في OData) تصدير جهات الاتصال الشخصية التي تتضمن نوع العلاقة **رئيسي**.</span><span class="sxs-lookup"><span data-stu-id="d383d-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="d383d-127">تم إصلاح هذه المشكلة لجهات الاتصال الشخصية التي يتم إنشاؤها بعد هذا التغيير.</span><span class="sxs-lookup"><span data-stu-id="d383d-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="d383d-128">سيتم حل جهات الاتصال الشخصية الموجودة من النوع **رئيسي** في إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="d383d-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="d383d-129">تمكين عرض أكواد السبب عبر سيناريوهات مختلفة عند تعليمها على أنها إجازة وغياب وتمكين نموذج الموظف انسيابي (434163)</span><span class="sxs-lookup"><span data-stu-id="d383d-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="d383d-130">يقيد هذا التغيير أكواد السبب على رموز الإجازة والغياب فقط عند تمكين إدخال الموظف الانسيابي.</span><span class="sxs-lookup"><span data-stu-id="d383d-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="d383d-131">ميزة المعاينة التي تعيين خطة إجازة للموظفين في المستقبل تعرض خطأ (433555)</span><span class="sxs-lookup"><span data-stu-id="d383d-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="d383d-132">يعمل هذا التغيير على تصحيح الخطأ عندما تتضمن خطة الإجازة نوعي إجازة معينين وأنت تحاول تعيين موظف.</span><span class="sxs-lookup"><span data-stu-id="d383d-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="d383d-133">ظهور شعار الشروع في العمل لكافة المستخدمين (441731)</span><span class="sxs-lookup"><span data-stu-id="d383d-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="d383d-134">بهذا التغيير، يتم إخفاء شعار الشروع في العمل للمستخدمين الذين لا يكونون من مسؤولي النظام أو مسؤولي إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d383d-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="d383d-135">يعمل كيان عنوان العامل في Common Data Service بشكل مختلف من حيث تواريخ وقت سريان في Human Resources (425071)</span><span class="sxs-lookup"><span data-stu-id="d383d-135">The Common Data Service Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="d383d-136">يؤدي هذا التغيير إلى الاحتفاظ بمعلومات العنوان التي تمت محاذاتها في سيناريوهات معينة، استنادا إلى تواريخ العنوان.</span><span class="sxs-lookup"><span data-stu-id="d383d-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="d383d-137">تعذر إضافة مرفق لطلب إجازة معتمد (425407)</span><span class="sxs-lookup"><span data-stu-id="d383d-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="d383d-138">باستخدام إصدار هذا الأسبوع ، يمكنك إضافة مرفقات إلى طلبات الإجازة المعتمدة دون تغيير طلب الإجازة.</span><span class="sxs-lookup"><span data-stu-id="d383d-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d383d-139">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="d383d-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="d383d-140">تعليق الإجازة</span><span class="sxs-lookup"><span data-stu-id="d383d-140">Leave suspension</span></span>

<span data-ttu-id="d383d-141">يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="d383d-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="d383d-142">يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة.</span><span class="sxs-lookup"><span data-stu-id="d383d-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="d383d-143">إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف.</span><span class="sxs-lookup"><span data-stu-id="d383d-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="d383d-144">لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="d383d-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="d383d-145">تحديث تجربة المستخدم للاشاره إلى ان الاستحقاق معلق (429550)</span><span class="sxs-lookup"><span data-stu-id="d383d-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="d383d-146">وتشير تجربة المستخدم الآن إلى انه تم تعليق الاستحقاق لإحدى الخطط.</span><span class="sxs-lookup"><span data-stu-id="d383d-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="d383d-147">تعليق استحقاق الإجازه لأنواع الإجازات المحددة (272447)</span><span class="sxs-lookup"><span data-stu-id="d383d-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="d383d-148">في هذا الإصدار، يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="d383d-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d383d-149">يمكن أن تكون الإجازه غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="d383d-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d383d-150">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="d383d-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="d383d-151">يتوفر كيان DMF لتعليقات الاستحقاق (429549)</span><span class="sxs-lookup"><span data-stu-id="d383d-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="d383d-152">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="d383d-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="d383d-153">إضافة كود السبب إلى تعليقات الاستحقاق (429547)</span><span class="sxs-lookup"><span data-stu-id="d383d-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="d383d-154">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="d383d-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="d383d-155">بدء النقل من معلمات الموارد البشرية إلى معلمات الإجازة والغياب‬</span><span class="sxs-lookup"><span data-stu-id="d383d-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="d383d-156">يبدأ هذا الإصدار في دمج معلمات الموارد البشرية بمعلمات الإجازة والغياب‬.</span><span class="sxs-lookup"><span data-stu-id="d383d-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d383d-157">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="d383d-157">Carry forward rules</span></span>

<span data-ttu-id="d383d-158">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="d383d-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d383d-159">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="d383d-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d383d-160">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="d383d-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>
