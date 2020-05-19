---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (13 أبريل 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 711cc4491024e647429b108438ce1d88483ea63c
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259807"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="040cf-103">ما الجديد أو المتغير في Dynamics 365 Human Resources (13 أبريل 2020)</span><span class="sxs-lookup"><span data-stu-id="040cf-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="040cf-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="040cf-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="040cf-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="040cf-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="040cf-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="040cf-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="040cf-107">وتيرة إصدار الإنتاج الجديدة</span><span class="sxs-lookup"><span data-stu-id="040cf-107">New production release cadence</span></span>

<span data-ttu-id="040cf-108">مع إصدار هذا الأسبوع، ينتقل إيقاع تحديث Human Resources من تحديث أسبوعي إلى تحديث كل أسبوعين.</span><span class="sxs-lookup"><span data-stu-id="040cf-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="040cf-109">لضمان التوافق مع ممارسات النشر الآمنة، والمحافظة على أعلى معايير الاستقرار والموثوقية في الخدمة، أصبحت الآن عملية نشر تحديثات الخدمة في كل المناطق تتم كل أسبوعين.</span><span class="sxs-lookup"><span data-stu-id="040cf-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="040cf-110">وقد تم وضع عمليات اختبار ومراقبة إضافية للتحقق من نجاح عملية النشر في كل مرحلة من مراحل العملية.</span><span class="sxs-lookup"><span data-stu-id="040cf-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="040cf-111">لمزيد من المعلومات حول وتيرة الإصدار، راجع [عملية التحديث](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="040cf-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="040cf-112">حقل "دقة التقريب" غير قابل للتحرير بعد تحديد نوع التقريب (435616)</span><span class="sxs-lookup"><span data-stu-id="040cf-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="040cf-113">مع هذا التغيير ، أصبح الآن حقل **دقة التقريب** متوفرًا بعد تحديث حقل **نوع التقريب**.</span><span class="sxs-lookup"><span data-stu-id="040cf-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="040cf-114">يتعذر تحرير تاريخ انتهاء تسجيل الإجازة عندما لا تتضمن خطة الإجازة فترات استحقاق (413628)</span><span class="sxs-lookup"><span data-stu-id="040cf-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="040cf-115">يمكنك الآن تحرير تاريخ انتهاء التسجيل دون الحصول على رسالة الخطأ "يجب ملء حقل أساس تاريخ الاستحقاق‬".</span><span class="sxs-lookup"><span data-stu-id="040cf-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="040cf-116">لا يتزامن كيان التوظيف مع Common Data Service (430834)</span><span class="sxs-lookup"><span data-stu-id="040cf-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="040cf-117">يعمل هذا التغيير على تصحيح مشكلة عدم مزامنة بيانات التوظيف مع Common Data Service بعد إضافة الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="040cf-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="040cf-118">إزالة تعدد الأصول لكيان الفاصل الزمني لتقويم العمل‬ (431775)</span><span class="sxs-lookup"><span data-stu-id="040cf-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="040cf-119">يؤدي هذا التغيير إلى إزالة تعدد الأصول لكيان **الفاصل الزمني لتقويم العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="040cf-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="040cf-120">لا تعمل التصفية بواسطة الدالة CAST ضمن استدعاء OData على كيان تعيين العامل بالمنصب‬‏ (431699)</span><span class="sxs-lookup"><span data-stu-id="040cf-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="040cf-121">يتضمن هذا التحديث تغييرًا للسماح بالتصفية بواسطة الدالة CAST ضمن OData للكيان **تعيين العامل بالمنصب‬**.</span><span class="sxs-lookup"><span data-stu-id="040cf-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="040cf-122">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="040cf-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="040cf-123">تعليق الإجازة</span><span class="sxs-lookup"><span data-stu-id="040cf-123">Leave suspension</span></span>

<span data-ttu-id="040cf-124">يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="040cf-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="040cf-125">يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة.</span><span class="sxs-lookup"><span data-stu-id="040cf-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="040cf-126">إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف.</span><span class="sxs-lookup"><span data-stu-id="040cf-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="040cf-127">لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="040cf-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="040cf-128">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="040cf-128">Carry forward rules</span></span>

<span data-ttu-id="040cf-129">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="040cf-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="040cf-130">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="040cf-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="040cf-131">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="040cf-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="040cf-132">مشكلات معروفة</span><span class="sxs-lookup"><span data-stu-id="040cf-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="040cf-133">كيان تفاصيل التوظيف</span><span class="sxs-lookup"><span data-stu-id="040cf-133">Employment Details entity</span></span>

<span data-ttu-id="040cf-134">تم تحديث كيان **تفاصيل التوظيف** بواسطة الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="040cf-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="040cf-135">**تكرار الدفع**</span><span class="sxs-lookup"><span data-stu-id="040cf-135">**PayFrequency**</span></span>
- <span data-ttu-id="040cf-136">**معرف فئة التوظيف**</span><span class="sxs-lookup"><span data-stu-id="040cf-136">**Employment Category ID**</span></span>
- <span data-ttu-id="040cf-137">**نوع التوظيف**</span><span class="sxs-lookup"><span data-stu-id="040cf-137">**Employment Type**</span></span>
- <span data-ttu-id="040cf-138">**معرف نوع التوظيف**</span><span class="sxs-lookup"><span data-stu-id="040cf-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="040cf-139">**حالة ميزة التوظيف**</span><span class="sxs-lookup"><span data-stu-id="040cf-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="040cf-140">يعتمد إعداد بيانات لهذه الحقول على إدارة المزايا التي يتم تمكينها في مساحة العمل **إدارة المزايا**.</span><span class="sxs-lookup"><span data-stu-id="040cf-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="040cf-141">لا تقم بملء هذه الحقول أو تحديثها في كيان **تفاصيل التوظيف**، لأن ذلك سيؤدي إلى حدوث أخطاء أثناء الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="040cf-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="040cf-142">معاينة SharePoint لا تعمل في بعض البيئات</span><span class="sxs-lookup"><span data-stu-id="040cf-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="040cf-143">إذا كانت معاينة المستندات للمستندات المخزنة في SharePoint لا تعمل، جرب الإجراء التالي:</span><span class="sxs-lookup"><span data-stu-id="040cf-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="040cf-144">تحقق من وجود بريد إلكتروني مقترن بحساب المستخدم المسؤول.</span><span class="sxs-lookup"><span data-stu-id="040cf-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="040cf-145">يمكنك عرض هذه المعلومات في صفحة **المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="040cf-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="040cf-146">إذا لم يتم إعداد البريد الإلكتروني، فأنت بحاجة إلى إضافة البريد الإلكتروني والموفر مع وظيفة Excel في OData.</span><span class="sxs-lookup"><span data-stu-id="040cf-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="040cf-147">افتراضيًا، لا يكون عنوان البريد الإلكتروني موجودًا في تصميم Excel.</span><span class="sxs-lookup"><span data-stu-id="040cf-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="040cf-148">ستحتاج إلى تحرير تصميم Excel، وإضافة جميع الحقول والتطبيق والتحديث.</span><span class="sxs-lookup"><span data-stu-id="040cf-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="040cf-149">بمجرد إكمال هذه الخطوات، يمكنك تحديث حساب المسؤول.</span><span class="sxs-lookup"><span data-stu-id="040cf-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="040cf-150">بعد أن يحتوي حساب المسؤول على حساب بريد إلكتروني مقترن، قم بتسجيل الدخول إلى Human Resources باستخدام بيانات اعتماد المسؤول.</span><span class="sxs-lookup"><span data-stu-id="040cf-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="040cf-151">يمكنك الوصول إلى مرفق في SharePoint لبدء معاينة المستند.</span><span class="sxs-lookup"><span data-stu-id="040cf-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="040cf-152">قم بتسجيل الدخول باستخدام حساب مستخدم آخر له حق الوصول إلى المرفقات وتحقق من أن المعاينة تعمل كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="040cf-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>