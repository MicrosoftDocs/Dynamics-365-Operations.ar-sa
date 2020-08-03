---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (1‏ مايو 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e4da626ce3412fba6f90dd7f953c1cbc79ab60c3
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555113"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="27df4-103">ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (1‏ مايو 2020)</span><span class="sxs-lookup"><span data-stu-id="27df4-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

<span data-ttu-id="27df4-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27df4-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="27df4-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3196.</span><span class="sxs-lookup"><span data-stu-id="27df4-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="27df4-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="27df4-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="27df4-107">كيانات إدارة الأداء الجديدة متوفرة في إطار عمل إدارة البيانات (DMF)</span><span class="sxs-lookup"><span data-stu-id="27df4-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="27df4-108">تتوفر الآن الكيانات التالية.</span><span class="sxs-lookup"><span data-stu-id="27df4-108">The following entities are now available.</span></span> <span data-ttu-id="27df4-109">إذا لم تتمكن من رؤية هذه الكيانات في قائمة الكيانات، فاستخدم الخيار **تحديث الكيانات** في **معلمات إطار العمل > إعدادات الكيان > تحديث قائمة الكيانات**.</span><span class="sxs-lookup"><span data-stu-id="27df4-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="27df4-110">**اختصاص المناقشة**</span><span class="sxs-lookup"><span data-stu-id="27df4-110">**Discussion Competency**</span></span>
- <span data-ttu-id="27df4-111">**أهداف المناقشة**</span><span class="sxs-lookup"><span data-stu-id="27df4-111">**Discussion Goals**</span></span>
- <span data-ttu-id="27df4-112">**قياس المناقشة**</span><span class="sxs-lookup"><span data-stu-id="27df4-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="27df4-113">**موضع المناقشة**</span><span class="sxs-lookup"><span data-stu-id="27df4-113">**Discussion Topic**</span></span>
- <span data-ttu-id="27df4-114">**دفتر يومية الأداء**</span><span class="sxs-lookup"><span data-stu-id="27df4-114">**Performance Journal**</span></span>
- <span data-ttu-id="27df4-115">**القياس**</span><span class="sxs-lookup"><span data-stu-id="27df4-115">**Measurement**</span></span>
- <span data-ttu-id="27df4-116">**قياس الهدف**</span><span class="sxs-lookup"><span data-stu-id="27df4-116">**Goal Measurement**</span></span>

<span data-ttu-id="27df4-117">بالإضافة إلى ذلك، تمت إضافة **النتيجة الإجمالية** و **متوسط النتيجة** إلى كيان **المناقشة**.</span><span class="sxs-lookup"><span data-stu-id="27df4-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="27df4-118">زيادة طول تعليقات طلب الاجازه (275641)</span><span class="sxs-lookup"><span data-stu-id="27df4-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="27df4-119">تسمح الآن التعليقات على طلبات الإجازات بأكثر من 100 حرفًا.</span><span class="sxs-lookup"><span data-stu-id="27df4-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="27df4-120">لا تظهر التعليقات النهائية على المراجعات عند تسجيل المدير أو الموظف في شركه مختلفة (431688)</span><span class="sxs-lookup"><span data-stu-id="27df4-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="27df4-121">ستظهر الآن كافة التعليقات عند عرض المراجعات.</span><span class="sxs-lookup"><span data-stu-id="27df4-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="27df4-122">الارتباطات المعرفة من قبل المستخدم غير مدعومة على نموذج العامل الجديد (390374)</span><span class="sxs-lookup"><span data-stu-id="27df4-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="27df4-123">تم الآن تمكين الارتباطات المعرفة من قبل المستخدم في نموذج **العامل** المبسط.</span><span class="sxs-lookup"><span data-stu-id="27df4-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="27df4-124">HcmRatingLevelEntity يسبب في حدوث عطل في OData API (439476)</span><span class="sxs-lookup"><span data-stu-id="27df4-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="27df4-125">يعمل هذا التغيير على تصحيح تعطل API.</span><span class="sxs-lookup"><span data-stu-id="27df4-125">This change corrects the API crash.</span></span> <span data-ttu-id="27df4-126">حدث هذا الخطأ بسبب وجود اسم مكرر.</span><span class="sxs-lookup"><span data-stu-id="27df4-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="27df4-127">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="27df4-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="27df4-128">تعليق الإجازة</span><span class="sxs-lookup"><span data-stu-id="27df4-128">Leave suspension</span></span>

<span data-ttu-id="27df4-129">يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="27df4-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="27df4-130">يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة.</span><span class="sxs-lookup"><span data-stu-id="27df4-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="27df4-131">إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف.</span><span class="sxs-lookup"><span data-stu-id="27df4-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="27df4-132">لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="27df4-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="27df4-133">تحديث تجربة المستخدم للاشاره إلى ان الاستحقاق معلق (429550)</span><span class="sxs-lookup"><span data-stu-id="27df4-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="27df4-134">وتشير تجربة المستخدم الآن إلى انه تم تعليق الاستحقاق لإحدى الخطط.</span><span class="sxs-lookup"><span data-stu-id="27df4-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="27df4-135">تعليق استحقاق الإجازه لأنواع الإجازات المحددة (272447)</span><span class="sxs-lookup"><span data-stu-id="27df4-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="27df4-136">في هذا الإصدار، يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="27df4-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="27df4-137">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="27df4-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="27df4-138">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="27df4-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="27df4-139">يتوفر كيان DMF لتعليقات الاستحقاق (429549)</span><span class="sxs-lookup"><span data-stu-id="27df4-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="27df4-140">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="27df4-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="27df4-141">إضافة كود السبب إلى تعليقات الاستحقاق (429547)</span><span class="sxs-lookup"><span data-stu-id="27df4-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="27df4-142">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="27df4-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="27df4-143">بدء النقل من معلمات الموارد البشرية إلى معلمات الإجازة والغياب‬</span><span class="sxs-lookup"><span data-stu-id="27df4-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="27df4-144">يبدأ هذا الإصدار في دمج معلمات الموارد البشرية بمعلمات الإجازة والغياب‬.</span><span class="sxs-lookup"><span data-stu-id="27df4-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="27df4-145">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="27df4-145">Carry forward rules</span></span>

<span data-ttu-id="27df4-146">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="27df4-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="27df4-147">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="27df4-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="27df4-148">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="27df4-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="27df4-149">مشكلات معروفة</span><span class="sxs-lookup"><span data-stu-id="27df4-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="27df4-150">معاينة SharePoint لا تعمل في بعض البيئات</span><span class="sxs-lookup"><span data-stu-id="27df4-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="27df4-151">إذا كانت معاينة المستندات للمستندات المخزنة في SharePoint لا تعمل، جرب الإجراء التالي:</span><span class="sxs-lookup"><span data-stu-id="27df4-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="27df4-152">تحقق من وجود بريد إلكتروني مقترن بحساب المستخدم المسؤول.</span><span class="sxs-lookup"><span data-stu-id="27df4-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="27df4-153">يمكنك عرض هذه المعلومات في صفحة **المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="27df4-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="27df4-154">إذا لم يتم إعداد البريد الإلكتروني، فأنت بحاجة إلى إضافة البريد الإلكتروني والموفر مع وظيفة Excel في OData.</span><span class="sxs-lookup"><span data-stu-id="27df4-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="27df4-155">افتراضيًا، لا يكون عنوان البريد الإلكتروني موجودًا في تصميم Excel.</span><span class="sxs-lookup"><span data-stu-id="27df4-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="27df4-156">ستحتاج إلى تحرير تصميم Excel، وإضافة جميع الحقول والتطبيق والتحديث.</span><span class="sxs-lookup"><span data-stu-id="27df4-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="27df4-157">بمجرد إكمال هذه الخطوات، يمكنك تحديث حساب المسؤول.</span><span class="sxs-lookup"><span data-stu-id="27df4-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="27df4-158">بعد أن يحتوي حساب المسؤول على حساب بريد إلكتروني مقترن، قم بتسجيل الدخول إلى Human Resources باستخدام بيانات اعتماد المسؤول.</span><span class="sxs-lookup"><span data-stu-id="27df4-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="27df4-159">يمكنك الوصول إلى مرفق في SharePoint لبدء معاينة المستند.</span><span class="sxs-lookup"><span data-stu-id="27df4-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="27df4-160">قم بتسجيل الدخول باستخدام حساب مستخدم آخر له حق الوصول إلى المرفقات وتحقق من أن المعاينة تعمل كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="27df4-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="27df4-161">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="27df4-161">See also</span></span>

[<span data-ttu-id="27df4-162">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="27df4-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="27df4-163">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="27df4-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="27df4-164">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="27df4-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="27df4-165">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="27df4-165">Manage features</span></span>](hr-admin-manage-features.md)