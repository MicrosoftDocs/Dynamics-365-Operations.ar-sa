---
title: تكوين أنواع الإجازة والغياب
description: إعداد أنواع الإجازات التي يمكن للموظفين القيام بها في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 6a89816f94c8cdcae6e56fa89843eb99c28b21fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/07/2020
ms.locfileid: "3969012"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="e36fb-103">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="e36fb-103">Configure leave and absence types</span></span>

<span data-ttu-id="e36fb-104">تحدد أنواع الإجازات في Dynamics 365 Human Resources أنواعًا مختلفة من حالات الغياب التي يمكن للموظفين الإبلاغ عنها.</span><span class="sxs-lookup"><span data-stu-id="e36fb-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="e36fb-105">يمكنك تكييف أنواع الإجازات وفقًا لاحتياجات مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="e36fb-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="e36fb-106">تشتمل أمثلة أنواع الإجازات على ما يلي:</span><span class="sxs-lookup"><span data-stu-id="e36fb-106">Examples of leave types include:</span></span>

- <span data-ttu-id="e36fb-107">زمن التوقف المدفوع (PTO)</span><span class="sxs-lookup"><span data-stu-id="e36fb-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="e36fb-108">إجازة دون راتب</span><span class="sxs-lookup"><span data-stu-id="e36fb-108">Unpaid leave</span></span>
- <span data-ttu-id="e36fb-109">إجازة مدفوعة الأجر</span><span class="sxs-lookup"><span data-stu-id="e36fb-109">Paid vacation</span></span>
- <span data-ttu-id="e36fb-110">إجازة مرضية</span><span class="sxs-lookup"><span data-stu-id="e36fb-110">Sick leave</span></span>
- <span data-ttu-id="e36fb-111">إجازة طبية</span><span class="sxs-lookup"><span data-stu-id="e36fb-111">Medical leave</span></span>
- <span data-ttu-id="e36fb-112">إجازة العائلية</span><span class="sxs-lookup"><span data-stu-id="e36fb-112">Family leave</span></span>
- <span data-ttu-id="e36fb-113">الإعاقة قصيرة الأجل</span><span class="sxs-lookup"><span data-stu-id="e36fb-113">Short-term disability</span></span>
- <span data-ttu-id="e36fb-114">إجازة Bereavement</span><span class="sxs-lookup"><span data-stu-id="e36fb-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="e36fb-115">إضافة نوع إجازة</span><span class="sxs-lookup"><span data-stu-id="e36fb-115">Add a leave type</span></span>

1. <span data-ttu-id="e36fb-116">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e36fb-117">ضمن **الإعداد** ، حدد **أنواع الإجازات والغياب** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-117">Under **Setup** , select **Leave and absence types** .</span></span>

3. <span data-ttu-id="e36fb-118">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-118">Select **New** .</span></span>

4. <span data-ttu-id="e36fb-119">ادخل اسما لنوع الإجازة ضمن **النوع** ، وحدد سير عمل من **معرف سير العمل** ، وادخل وصفا ضمن **الوصف** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-119">Enter a name for the leave type under **Type** , select a workflow from **Workflow ID** , and enter a description under **Description** .</span></span>

5. <span data-ttu-id="e36fb-120">في **عام** ، حدد **بلا** أو **مجدول** أو **غير مجدول** من القائمة المنسدلة **الفئة** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-120">In **General** , select **None** , **Scheduled** , or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="e36fb-121">حدد كود دخل من القائمة المنسدلة **رمز الدخل** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="e36fb-122">ضمن **كود السبب المطلوب** ، حدد ما إذا كنت ترغب في طلب كود سبب ام لا.</span><span class="sxs-lookup"><span data-stu-id="e36fb-122">Under **Reason code required** , choose whether you want to require a reason code.</span></span> <span data-ttu-id="e36fb-123">إذا كنت ترغب في طلب أكواد سبب، فقد تحتاج إلى اضافتها.</span><span class="sxs-lookup"><span data-stu-id="e36fb-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="e36fb-124">ضمن **أكواد السبب** ، حدد **إضافة** ، وحدد كود السبب، ثم حدد خانة الاختيار **ممكن** بجوارها.</span><span class="sxs-lookup"><span data-stu-id="e36fb-124">Under **Reason codes** , select **Add** , select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="e36fb-125">ضمن **تقييد الوصول إلى الأدوار المحددة** ، اختر ما إذا كنت ترغب في تقييد الوصول ام لا.</span><span class="sxs-lookup"><span data-stu-id="e36fb-125">Under **Restrict access to selected roles** , choose whether you want to restrict access.</span></span> <span data-ttu-id="e36fb-126">ثم حدد ادوار الأمان ضمن **ادوار الأمان لنوع الإجازة هذا** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-126">Then select the security roles under **Security roles for this leave type** .</span></span> <span data-ttu-id="e36fb-127">يتم تحديد ادوار الأمان في سير العمل الذي حددته ضمن **معرف سير العمل** في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e36fb-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="e36fb-128">ضمن **لون التقويم** ، اختر اللون الذي سيتم عرضه في تقويمات المغادرة والغياب لهذا النوع من الغياب.</span><span class="sxs-lookup"><span data-stu-id="e36fb-128">Under **Calendar color** , choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="e36fb-129">ضمن **علاقات التعليق‬** ، اختر إن كنت تريد أن يقوم نوع الإجازة هذا بتعليق نوع إجازة آخر أو أن يتم تعليقه بواسطة نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="e36fb-129">Under **Suspension relations** , choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="e36fb-130">عند تقديم طلب إذن غياب لنوع الإجازة المعلق، سيتم إنشاء تعليق الإجازة بشكل تلقائي لنوع الإجازة المعلق.</span><span class="sxs-lookup"><span data-stu-id="e36fb-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="e36fb-131">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-131">Select **Save** .</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="e36fb-132">تكوين قواعد أنواع الإجازة</span><span class="sxs-lookup"><span data-stu-id="e36fb-132">Configure leave type rules</span></span>

1. <span data-ttu-id="e36fb-133">تعيين خيارات التقريب لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="e36fb-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="e36fb-134">تتضمن الخيارات **بلا** ، و **لأعلى** و **لأسفل** و **الأقرب** .</span><span class="sxs-lookup"><span data-stu-id="e36fb-134">Options include **None** , **Up** , **Down** , and **Nearest** .</span></span> <span data-ttu-id="e36fb-135">يمكنك أيضا تعيين دقه التقريب لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="e36fb-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="e36fb-136">قم بتعيين **تصحيح الإجازة** لنوع العطلة.</span><span class="sxs-lookup"><span data-stu-id="e36fb-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="e36fb-137">عند تحديد هذا الخيار، تستخدم Human Resources عدد العطلات التي تقع في يوم العمل لتحديد كيفيه استحقاق الوقت لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="e36fb-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="e36fb-138">على سبيل المثال، إذا كان يوم عيد الميلاد يوم الاثنين، فإن Human Resources سيطرح يومًا واحدًا من نوع الإجازة عند معالجه الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="e36fb-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="e36fb-139">يمكنك تعيين العطلات في تقويم وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="e36fb-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="e36fb-140">لمزيد من المعلومات، راجع [إنشاء تقويم وقت العمل](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="e36fb-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="e36fb-141">عيّن **نوع الإجازة المنقولة** لنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="e36fb-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="e36fb-142">عند تحديد هذا الخيار، سيتم تحويل الأرصدة المنقولة إلى نوع الإجازة المحدد.</span><span class="sxs-lookup"><span data-stu-id="e36fb-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="e36fb-143">كما يجب تضمين نوع الإجازة المنقولة في خطة الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="e36fb-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="e36fb-144">حدد **قواعد انتهاء الصلاحية** لنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="e36fb-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="e36fb-145">عند تكوين هذا الخيار، يمكنك اختيار وحدة الأيام أو الأشهر وتعيين مدة انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="e36fb-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="e36fb-146">يمكنك أيضًا تعيين تاريخ السريان لقاعدة انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="e36fb-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="e36fb-147">سيتم طرح أي أرصدة إجازات موجودة عند انتهاء الصلاحية من نوع الإجازة وستظهر في رصيد الإجازة.</span><span class="sxs-lookup"><span data-stu-id="e36fb-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="e36fb-148">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e36fb-148">See also</span></span>

- [<span data-ttu-id="e36fb-149">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="e36fb-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="e36fb-150">إنشاء خطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="e36fb-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="e36fb-151">إنشاء تقويم مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="e36fb-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="e36fb-152">تعليق الإجازة</span><span class="sxs-lookup"><span data-stu-id="e36fb-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

