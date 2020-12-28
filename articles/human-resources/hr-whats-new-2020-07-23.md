---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (23 يوليو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 23 يوليو 2020.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0672e3039f54a4591db49eee00d69bf5e4278fd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528439"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="64368-103">ما الجديد والمتغير في Dynamics 365 Human Resources (23 يوليو 2020)</span><span class="sxs-lookup"><span data-stu-id="64368-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="64368-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="64368-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="64368-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="64368-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="64368-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="64368-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="64368-107">لا يعمل حذف الأبعاد المالية في أحد المناصب كما هو متوقع (445476)</span><span class="sxs-lookup"><span data-stu-id="64368-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="64368-108">تؤدي الآن إزالة الأبعاد من منصب إلى إزالة هذه المناصب نفسها من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="64368-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="64368-109">المناصب غير الموجودة في التدرج الهرمي تظهر كمناصب غير نشطة (397257)</span><span class="sxs-lookup"><span data-stu-id="64368-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="64368-110">المناصب غير النشطة (التي انتهت مدة صلاحيتها)، لم تعد تظهر في التدرج الهرمي للمناصب على أنها **مناصب غير موجودة في التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="64368-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="64368-111">يتسبب التحقق من الصحة الذي يحدث بين LeaveEnrollmentEntity وHcmWorkerEntity على إطار عمل إدارة البيانات (DMF) في حدوث تحميلات بيانات بطيئة (442324)</span><span class="sxs-lookup"><span data-stu-id="64368-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="64368-112">تؤدي التغييرات في هذا الإصدار إلى زيادة أداء **LeaveEnrollmentEntity**.</span><span class="sxs-lookup"><span data-stu-id="64368-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="64368-113">يتعذر التخصيص في إدارة المؤسسة (447490)</span><span class="sxs-lookup"><span data-stu-id="64368-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="64368-114">وبهذا التغيير، يمكنك الآن تخصيص الارتباطات في **إدارة المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="64368-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="64368-115">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="64368-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="64368-116">حقول إلزامية</span><span class="sxs-lookup"><span data-stu-id="64368-116">Mandatory fields</span></span> 

<span data-ttu-id="64368-117">يمكنك الآن جعل الحقول إلزامية باستخدام إمكانيات إضفاء طابع شخصي للموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="64368-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="64368-118">تتطلب هذه الميزة **طرق عرض محفوظة**.</span><span class="sxs-lookup"><span data-stu-id="64368-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="64368-119">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="64368-119">Human Resources application in Teams</span></span>

<span data-ttu-id="64368-120">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="64368-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="64368-121">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="64368-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="64368-122">لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="64368-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="64368-123">كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="64368-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="64368-124">يتم إصدار كيانات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="64368-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="64368-125">تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة.</span><span class="sxs-lookup"><span data-stu-id="64368-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="64368-126">كما سيتوفر قالب إدارة المزايا لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="64368-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="64368-127">يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="64368-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="64368-128">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="64368-128">Buy and sell leave</span></span> 

<span data-ttu-id="64368-129">توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها.</span><span class="sxs-lookup"><span data-stu-id="64368-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="64368-130">غالبا ما تُدار هذه العملية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="64368-130">This process is often managed manually.</span></span> <span data-ttu-id="64368-131">تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="64368-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="64368-132">إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="64368-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="64368-133">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="64368-133">For more information, see:</span></span>

- [<span data-ttu-id="64368-134">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="64368-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="64368-135">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="64368-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="64368-136">استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية</span><span class="sxs-lookup"><span data-stu-id="64368-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="64368-137">يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب.</span><span class="sxs-lookup"><span data-stu-id="64368-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="64368-138">وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="64368-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="64368-139">لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="64368-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="64368-140">إضافة مرفقات إلى طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="64368-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="64368-141">تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي.</span><span class="sxs-lookup"><span data-stu-id="64368-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="64368-142">يمكن للموظفين الآن إضافه هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="64368-142">Employees can now add these attachments.</span></span> <span data-ttu-id="64368-143">كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="64368-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="64368-144">لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="64368-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="64368-145">إضافة كود السبب إلى تعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="64368-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="64368-146">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="64368-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="64368-147">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="64368-147">Carry forward rules</span></span> 

<span data-ttu-id="64368-148">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="64368-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="64368-149">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="64368-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="64368-150">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="64368-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="64368-151">تعليق استحقاق الإجازه لأنواع الإجازات المحددة</span><span class="sxs-lookup"><span data-stu-id="64368-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="64368-152">يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="64368-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="64368-153">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="64368-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="64368-154">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="64368-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="64368-155">يتوفر كيان DMF لتعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="64368-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="64368-156">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="64368-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="64368-157">قريبًا</span><span class="sxs-lookup"><span data-stu-id="64368-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="64368-158">تضمين كيانات قائمة الاختيار في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="64368-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="64368-159">ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="64368-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="64368-160">تغييرات النظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="64368-160">Platform changes</span></span>

<span data-ttu-id="64368-161">Platform update 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="64368-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="64368-162">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="64368-162">See also</span></span>

[<span data-ttu-id="64368-163">الجديد أو المتغير في Human Resources</span><span class="sxs-lookup"><span data-stu-id="64368-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="64368-164">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="64368-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="64368-165">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="64368-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="64368-166">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="64368-166">Manage features</span></span>](hr-admin-manage-features.md)
