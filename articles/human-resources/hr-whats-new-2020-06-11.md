---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (11 يونيو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cba6e48899ec39fc4de6656f8151a42b8aa43261
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555185"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="d2e86-103">ما الجديد والمتغير في Dynamics 365 Human Resources (11 يونيو 2020)</span><span class="sxs-lookup"><span data-stu-id="d2e86-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="d2e86-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d2e86-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d2e86-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="d2e86-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="d2e86-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="d2e86-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="d2e86-107">يعمل نموذج الموظف المبسط على إيقاف أزرار الإغلاق (X) للنموذج التابع (442369)</span><span class="sxs-lookup"><span data-stu-id="d2e86-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="d2e86-108">عند تمكين نموذج **العامل** الجديد، لا يعمل زر الإغلاق (**X**) أحيانا على النماذج التابعة.</span><span class="sxs-lookup"><span data-stu-id="d2e86-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="d2e86-109">هذه المشكلة متقطعه.</span><span class="sxs-lookup"><span data-stu-id="d2e86-109">This problem was intermittent.</span></span> <span data-ttu-id="d2e86-110">يمكنك إغلاق النموذج بعد تركه والعودة اليه.</span><span class="sxs-lookup"><span data-stu-id="d2e86-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="d2e86-111">علي سبيل المثال، يمكنك تحديد عنصر قائمة على اليسار، والتنقل للخلف إلى نموذج **العامل** ، ثم إغلاقه.</span><span class="sxs-lookup"><span data-stu-id="d2e86-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="d2e86-112">يعمل إصدار هذا الأسبوع على إصلاح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="d2e86-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="d2e86-113">كيان شخص جهة الاتصال الشخصية للعامل لا يقوم بتصدير جهات الاتصال الشخصية بنوع علاقة رئيسي</span><span class="sxs-lookup"><span data-stu-id="d2e86-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="d2e86-114">ومع هذا الإصدار، يقوم كيان **شخص جهة الاتصال الشخصية للعامل** بتصدير كافة أنواع العلاقات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="d2e86-115">يجب أن يكون HcmPositionWorkerAssignmentV2Entity جزءًا من حزمة ‏‫تكامل كشف المرتبات Ceridian‬ بشكل افتراضي (448506)</span><span class="sxs-lookup"><span data-stu-id="d2e86-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="d2e86-116">وبهذا التغيير، يتم تضمين **HcmPositionWorkerAssignmentV2Entity** في حزمة ‏‫تكامل كشف المرتبات Ceridian‬.</span><span class="sxs-lookup"><span data-stu-id="d2e86-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d2e86-117">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="d2e86-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="d2e86-118">تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="d2e86-118">Database logging</span></span>

<span data-ttu-id="d2e86-119">تسمح ميزة تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها.</span><span class="sxs-lookup"><span data-stu-id="d2e86-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="d2e86-120">كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="d2e86-121">يمكنك استخدام إمكانيات تسجيل قاعده البيانات لرؤية هذه التغييرات بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="d2e86-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="d2e86-122">لمزيد من المعلومات، راجع [‏‫تكوين وإدارة تسجيل قاعده البيانات‬](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="d2e86-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="d2e86-123">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="d2e86-123">Human Resources application in Teams</span></span>

<span data-ttu-id="d2e86-124">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d2e86-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d2e86-125">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d2e86-126">لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="d2e86-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="d2e86-127">كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="d2e86-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="d2e86-128">يتم إصدار كيانات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="d2e86-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="d2e86-129">تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة.</span><span class="sxs-lookup"><span data-stu-id="d2e86-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="d2e86-130">كما سيتوفر قالب إدارة المزايا لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="d2e86-131">يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="d2e86-132">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="d2e86-132">Buy and sell leave</span></span> 

<span data-ttu-id="d2e86-133">توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها.</span><span class="sxs-lookup"><span data-stu-id="d2e86-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="d2e86-134">غالبا ما تُدار هذه العملية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="d2e86-134">This process is often managed manually.</span></span> <span data-ttu-id="d2e86-135">تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="d2e86-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="d2e86-136">إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="d2e86-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="d2e86-137">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="d2e86-137">For more information, see:</span></span>

- [<span data-ttu-id="d2e86-138">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="d2e86-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="d2e86-139">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="d2e86-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="d2e86-140">استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية</span><span class="sxs-lookup"><span data-stu-id="d2e86-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="d2e86-141">يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب.</span><span class="sxs-lookup"><span data-stu-id="d2e86-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="d2e86-142">وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="d2e86-143">لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="d2e86-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="d2e86-144">إضافة مرفقات إلى طلبات زمن التوقف‬</span><span class="sxs-lookup"><span data-stu-id="d2e86-144">Add attachments to time off requests</span></span>

<span data-ttu-id="d2e86-145">تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي.</span><span class="sxs-lookup"><span data-stu-id="d2e86-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="d2e86-146">يمكن للموظفين الآن إضافه هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-146">Employees can now add these attachments.</span></span> <span data-ttu-id="d2e86-147">كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="d2e86-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="d2e86-148">لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="d2e86-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="d2e86-149">إضافة كود السبب إلى تعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="d2e86-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="d2e86-150">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="d2e86-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d2e86-151">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="d2e86-151">Carry forward rules</span></span> 

<span data-ttu-id="d2e86-152">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="d2e86-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d2e86-153">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="d2e86-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d2e86-154">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="d2e86-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="d2e86-155">تعليق استحقاق الإجازه لأنواع الإجازات المحددة</span><span class="sxs-lookup"><span data-stu-id="d2e86-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="d2e86-156">يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="d2e86-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d2e86-157">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="d2e86-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d2e86-158">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="d2e86-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d2e86-159">يتوفر كيان DMF لتعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="d2e86-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="d2e86-160">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="d2e86-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d2e86-161">قريبًا</span><span class="sxs-lookup"><span data-stu-id="d2e86-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="d2e86-162">إمكانات النظام الأساسي الجديدة</span><span class="sxs-lookup"><span data-stu-id="d2e86-162">New platform capabilities</span></span> 

<span data-ttu-id="d2e86-163">ستتمكن من جعل الحقول إلزاميه باستخدام التخصيص.</span><span class="sxs-lookup"><span data-stu-id="d2e86-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="d2e86-164">ستلزمك هذه الميزة بتمكين **طرق العرض المحفوظة**.</span><span class="sxs-lookup"><span data-stu-id="d2e86-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="d2e86-165">تكوين اسم خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="d2e86-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="d2e86-166">سيتوفر خيار جديد في محددات الموارد البشرية لتحديث اسم مساحة عمل خدمة الموظف الذاتية إلى الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="d2e86-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="d2e86-167">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d2e86-167">See also</span></span>

[<span data-ttu-id="d2e86-168">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="d2e86-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d2e86-169">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="d2e86-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d2e86-170">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="d2e86-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d2e86-171">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="d2e86-171">Manage features</span></span>](hr-admin-manage-features.md)