---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (25 يونيو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 23 يونيو 2020.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f767ad634a37b7231a7998184ef130668c8a8dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463612"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="6e139-103">ما الجديد والمتغير في Dynamics 365 Human Resources (23 يونيو 2020)</span><span class="sxs-lookup"><span data-stu-id="6e139-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6e139-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e139-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6e139-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="6e139-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="6e139-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="6e139-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="6e139-107">عند انتهاء صلاحية التسجيل لموظف تم إنهاؤه، يتم مسح نوع الإجازة والرصيد والمبلغ في نموذج ترك التسجيل (444867)</span><span class="sxs-lookup"><span data-stu-id="6e139-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="6e139-108">يتم الآن الاحتفاظ بالقيم الموجودة في **نوع الإجازة** و **الرصيد** و **المبلغ** بدلا من المسح عند القيام بهذا التحديد.</span><span class="sxs-lookup"><span data-stu-id="6e139-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="6e139-109">الرصيد المتوقع غير صحيح عند تمكين ميزة جديدة (استحقاق المغادرة لشركة فردية أو خطة واحدة) (456553)</span><span class="sxs-lookup"><span data-stu-id="6e139-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="6e139-110">يتم عرض الرصيد المتوقع الصحيح الآن عند تمكين استحقاق المغادرة لشركة فردية أو خطة واحدة</span><span class="sxs-lookup"><span data-stu-id="6e139-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="6e139-111">الكيانات ذات العلاقات ينتج عنها خصائص تنقل مكررة (456486)</span><span class="sxs-lookup"><span data-stu-id="6e139-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="6e139-112">يعمل هذا الإصدار على تصحيح مشكلة في خصائص التنقل (العلاقة) لكيانات متعددة.</span><span class="sxs-lookup"><span data-stu-id="6e139-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="6e139-113">تم الكشف عن العلاقات المكررة.</span><span class="sxs-lookup"><span data-stu-id="6e139-113">Duplicate relations are detected.</span></span> <span data-ttu-id="6e139-114">تم تصحيح كافة هذه السيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="6e139-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="6e139-115">التعليقات عبر الشركات في مراجعة الأداء (455536)</span><span class="sxs-lookup"><span data-stu-id="6e139-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="6e139-116">التعليق عبر الشركات مرئية الآن في مراجعات الأداء مع هذا الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="6e139-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="6e139-117">يعمل هذا التغيير على تصحيح طريقة عرض تعليقات المراجع التي تم إدخالها في شركات مختلفة لنفس مراجعة الأداء.</span><span class="sxs-lookup"><span data-stu-id="6e139-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="6e139-118">وجود عدم اتساق في إظهار بيانات إدارة التعويض (432562)</span><span class="sxs-lookup"><span data-stu-id="6e139-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="6e139-119">يتم الآن الاحتفاظ بعرض متسق لبيانات التعويض في الخدمة الذاتية للمدير.</span><span class="sxs-lookup"><span data-stu-id="6e139-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="6e139-120">وفقا للطريقة التي تنتقل بها إلى **تفاصيل التعويض** الخاصة بالعامل، يتم الآن عرض بيانات التعويض بشكل متسق للمديرين.</span><span class="sxs-lookup"><span data-stu-id="6e139-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="6e139-121">يتم تعيين تاريخ سريان خطة التعويض الثابتة على تاريخ اليوم بشكل افتراضي (411994)</span><span class="sxs-lookup"><span data-stu-id="6e139-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="6e139-122">يعتمد تاريخ بدء التعويض الآن على تاريخ بداية المنصب الذي يتم تعيينه للموظف.</span><span class="sxs-lookup"><span data-stu-id="6e139-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="6e139-123">تعطيل تعريف نصف اليوم في نموذج الإجازة والغياب عند فتح النموذج (452607)</span><span class="sxs-lookup"><span data-stu-id="6e139-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="6e139-124">وبهذا التغيير، سيتم تمكين تعريف **تمكين نصف اليوم** حتى توجد حركات إجازة جديدة.</span><span class="sxs-lookup"><span data-stu-id="6e139-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="6e139-125">يتعذر النشر إلى HcmDiscussionEntity عن طريق Excel؛ خطأ في حقل TotalRatingScore (453899)</span><span class="sxs-lookup"><span data-stu-id="6e139-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="6e139-126">يمكنك الآن تحديث حقل **TotalRatingScore** باستخدام **HCMDiscussionEntity** في مصمم مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="6e139-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="6e139-127">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="6e139-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="6e139-128">تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="6e139-128">Database logging</span></span>

<span data-ttu-id="6e139-129">يسمح تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها.</span><span class="sxs-lookup"><span data-stu-id="6e139-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="6e139-130">كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="6e139-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="6e139-131">يمكنك استخدام إمكانيات تسجيل قاعده البيانات لرؤية هذه التغييرات بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="6e139-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="6e139-132">لمزيد من المعلومات، راجع [‏‫تكوين وإدارة تسجيل قاعده البيانات‬](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="6e139-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="6e139-133">حقول إلزامية</span><span class="sxs-lookup"><span data-stu-id="6e139-133">Mandatory fields</span></span> 

<span data-ttu-id="6e139-134">يمكنك الآن جعل الحقول إلزامية باستخدام إمكانيات إضفاء طابع شخصي للموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="6e139-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="6e139-135">تتطلب هذه الميزة **طرق عرض محفوظة**.</span><span class="sxs-lookup"><span data-stu-id="6e139-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="6e139-136">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="6e139-136">Human Resources application in Teams</span></span>

<span data-ttu-id="6e139-137">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6e139-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="6e139-138">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="6e139-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="6e139-139">لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="6e139-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="6e139-140">كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="6e139-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="6e139-141">يتم إصدار كيانات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="6e139-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="6e139-142">تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة.</span><span class="sxs-lookup"><span data-stu-id="6e139-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="6e139-143">كما سيتوفر قالب إدارة المزايا لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="6e139-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="6e139-144">يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="6e139-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="6e139-145">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6e139-145">Buy and sell leave</span></span> 

<span data-ttu-id="6e139-146">توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها.</span><span class="sxs-lookup"><span data-stu-id="6e139-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="6e139-147">غالبا ما تُدار هذه العملية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="6e139-147">This process is often managed manually.</span></span> <span data-ttu-id="6e139-148">تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="6e139-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="6e139-149">إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="6e139-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="6e139-150">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="6e139-150">For more information, see:</span></span>

- [<span data-ttu-id="6e139-151">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6e139-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="6e139-152">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6e139-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="6e139-153">استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية</span><span class="sxs-lookup"><span data-stu-id="6e139-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="6e139-154">يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب.</span><span class="sxs-lookup"><span data-stu-id="6e139-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="6e139-155">وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="6e139-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="6e139-156">لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="6e139-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="6e139-157">إضافة مرفقات إلى طلبات زمن التوقف‬</span><span class="sxs-lookup"><span data-stu-id="6e139-157">Add attachments to time off requests</span></span>

<span data-ttu-id="6e139-158">تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي.</span><span class="sxs-lookup"><span data-stu-id="6e139-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="6e139-159">يمكن للموظفين الآن إضافه هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="6e139-159">Employees can now add these attachments.</span></span> <span data-ttu-id="6e139-160">كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="6e139-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="6e139-161">لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="6e139-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="6e139-162">إضافة كود السبب إلى تعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="6e139-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="6e139-163">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="6e139-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="6e139-164">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="6e139-164">Carry forward rules</span></span> 

<span data-ttu-id="6e139-165">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="6e139-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="6e139-166">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="6e139-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="6e139-167">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="6e139-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="6e139-168">تعليق استحقاق الإجازه لأنواع الإجازات المحددة</span><span class="sxs-lookup"><span data-stu-id="6e139-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="6e139-169">يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="6e139-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="6e139-170">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="6e139-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="6e139-171">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="6e139-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="6e139-172">يتوفر كيان DMF لتعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="6e139-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="6e139-173">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="6e139-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6e139-174">قريبًا</span><span class="sxs-lookup"><span data-stu-id="6e139-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="6e139-175">تكوين اسم خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="6e139-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="6e139-176">سيتوفر خيار جديد في **معلمات الموارد البشرية** لتحديث اسم مساحة عمل خدمة الموظف الذاتية إلى الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="6e139-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="6e139-177">تضمين كيانات قائمة الاختيار في Dataverse</span><span class="sxs-lookup"><span data-stu-id="6e139-177">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="6e139-178">ستتوفر كيانات قائمة الاختيار الخاصة بعمليات إلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبا في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6e139-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e139-179">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="6e139-179">See also</span></span>

[<span data-ttu-id="6e139-180">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="6e139-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="6e139-181">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="6e139-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="6e139-182">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="6e139-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="6e139-183">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="6e139-183">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]