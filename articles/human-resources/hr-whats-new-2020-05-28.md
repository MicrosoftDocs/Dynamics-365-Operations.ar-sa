---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (28‏ مايو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 28 مايو 2020.
author: andreabichsel
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79026c6047f3a10366ef3b22d74caee13b371b66
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891951"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="4cb1c-103">ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (28‏ مايو 2020)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4cb1c-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4cb1c-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="4cb1c-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="4cb1c-107">لا يعمل كيان LeaveRequest عند تمكين أنواع متعددة لكل خطة إجازة (447498)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="4cb1c-108">مع هذا التغيير، يتوفر **LeaveEnrollmentV2Entity** الآن لتصحيح الخطأ الذي يحدث عند تمكين أنواع إجازات متعددة.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="4cb1c-109">ميزة تقليل تعارضات الدُفعات (معاينة) (446619)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="4cb1c-110">عند تمكين هذه الميزة، يمكنك توقع انخفاض الحظر على جداول إطار عمل الدُفعة مع تحديد المهام وإنجازها.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="4cb1c-111">UpdateConflict أثناء حفظ سجل عامل يمنع تحرير سجل في "الأشخاص" (427915)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="4cb1c-112">يعمل هذا التغيير على تصحيح خطأ عند إضافة عامل جديد وتحديث معلومات العنوان وتغيير تفضيل اللغة.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="4cb1c-113">في هذا السيناريو الفريد، يظهر خطأ يشير إلى تعذر تحديث السجل.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="4cb1c-114">تعذر إضافة مرفق بطلب إجازة موافق عليه لإعادة إرساله (425407)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="4cb1c-115">يسمح هذا التغيير الآن للمرفقات بالموافقة على طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="4cb1c-116">بإمكان المستخدم إدخال تعويض لأحد الموظفين في نموذج كيان قانوني مختلف (409529)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="4cb1c-117">يؤدي هذا التغيير إلى تعطيل خيارات التعويض لمنع الإدخال غير المقصود لسجلات التعويض للكيان القانوني غير الصحيح.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="4cb1c-118">خطأ عندما تقوم بتحويل الموظف وتاريخ تعيين منصب العامل يقع قبل مدة المنصب (429402)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="4cb1c-119">تم تحديث رسائل الخطأ عند تحويل أحد الموظفين في هذا السيناريو كي يتم وصف التغييرات المطلوبة لتصحيح المشكلة بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="4cb1c-120">قدرات المرفقات في تسجيل مزايا الخدمة الذاتية للموظفين</span><span class="sxs-lookup"><span data-stu-id="4cb1c-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="4cb1c-121">يمكنك الآن إضافة مرفقات أثناء عملية تسجيل المزايا لكل خطة قام الموظف بالتسجيل فيها.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="4cb1c-122">يمكنك بعد ذلك عرض المرفقات داخل نموذج **ميزات العامل المسجل**.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="4cb1c-123">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="4cb1c-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="4cb1c-124">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="4cb1c-124">Human Resources application in Teams</span></span>

<span data-ttu-id="4cb1c-125">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4cb1c-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="4cb1c-126">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="4cb1c-127">لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="4cb1c-127">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="4cb1c-128">تعليق الإجازة</span><span class="sxs-lookup"><span data-stu-id="4cb1c-128">Leave suspension</span></span>

<span data-ttu-id="4cb1c-129">يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="4cb1c-130">يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="4cb1c-131">إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="4cb1c-132">لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="4cb1c-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="4cb1c-133">تحديث تجربة المستخدم للاشاره إلى ان الاستحقاق معلق (429550)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="4cb1c-134">وتشير تجربة المستخدم الآن إلى انه تم تعليق الاستحقاق لإحدى الخطط.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="4cb1c-135">قريبًا</span><span class="sxs-lookup"><span data-stu-id="4cb1c-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="4cb1c-136">تسجيل قاعدة البيانات (في المعاينة في يونيو)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="4cb1c-137">تسمح ميزة تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="4cb1c-138">كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="4cb1c-139">تتوفر إمكانيات الاستعلام لرؤية هذه التغييرات مع مرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="4cb1c-140">شراء الإجازات وبيعها (في المعاينة 1 يونيو)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="4cb1c-141">توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="4cb1c-142">غالبا ما تُدار هذه العملية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-142">This process is often managed manually.</span></span> <span data-ttu-id="4cb1c-143">توفر هذه الميزة طريقة تلقائية لإدارة السياسات والطلبات الخاصة بقسم الموارد البشرية، وتساعد على إزالة الأخطاء مع تنظيم عملية إدارة الإجازات.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="4cb1c-144">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="4cb1c-144">For more information, see:</span></span>

- [<span data-ttu-id="4cb1c-145">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="4cb1c-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="4cb1c-146">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="4cb1c-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="4cb1c-147">كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="4cb1c-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="4cb1c-148">يتم إصدار كيانات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="4cb1c-149">تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="4cb1c-150">كما سيتوفر قالب إدارة المزايا لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="4cb1c-151">يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="4cb1c-152">إضافة كود السبب إلى تعليقات الاستحقاق (1 يونيو)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="4cb1c-153">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="4cb1c-154">قواعد نقل الإجازة (1 يونيو)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="4cb1c-155">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="4cb1c-156">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="4cb1c-157">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="4cb1c-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="4cb1c-158">تعليق استحقاق الإجازة لأنواع الإجازات المحددة (1 يونيو)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="4cb1c-159">في هذا الإصدار، يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="4cb1c-160">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="4cb1c-161">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="4cb1c-162">يتوفر كيان DMF لتعليقات الاستحقاق (1 يونيو)</span><span class="sxs-lookup"><span data-stu-id="4cb1c-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="4cb1c-163">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="4cb1c-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cb1c-164">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="4cb1c-164">See also</span></span>

[<span data-ttu-id="4cb1c-165">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="4cb1c-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="4cb1c-166">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="4cb1c-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="4cb1c-167">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="4cb1c-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="4cb1c-168">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="4cb1c-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]