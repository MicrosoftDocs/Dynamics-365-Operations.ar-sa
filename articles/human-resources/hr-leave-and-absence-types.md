---
title: تكوين أنواع الإجازة والغياب
description: إعداد أنواع الإجازات التي يمكن للموظفين القيام بها في Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271117"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="33ea3-103">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="33ea3-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="33ea3-104">تحدد أنواع الإجازات في Dynamics 365 Human Resources أنواعًا مختلفة من حالات الغياب التي يمكن للموظفين الإبلاغ عنها.</span><span class="sxs-lookup"><span data-stu-id="33ea3-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="33ea3-105">يمكنك تكييف أنواع الإجازات وفقًا لاحتياجات مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="33ea3-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="33ea3-106">تشتمل أمثلة أنواع الإجازات على ما يلي:</span><span class="sxs-lookup"><span data-stu-id="33ea3-106">Examples of leave types include:</span></span>

- <span data-ttu-id="33ea3-107">زمن التوقف المدفوع (PTO)</span><span class="sxs-lookup"><span data-stu-id="33ea3-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="33ea3-108">إجازة دون راتب</span><span class="sxs-lookup"><span data-stu-id="33ea3-108">Unpaid leave</span></span>
- <span data-ttu-id="33ea3-109">إجازة مدفوعة الأجر</span><span class="sxs-lookup"><span data-stu-id="33ea3-109">Paid vacation</span></span>
- <span data-ttu-id="33ea3-110">إجازة مرضية</span><span class="sxs-lookup"><span data-stu-id="33ea3-110">Sick leave</span></span>
- <span data-ttu-id="33ea3-111">إجازة طبية</span><span class="sxs-lookup"><span data-stu-id="33ea3-111">Medical leave</span></span>
- <span data-ttu-id="33ea3-112">إجازة العائلية</span><span class="sxs-lookup"><span data-stu-id="33ea3-112">Family leave</span></span>
- <span data-ttu-id="33ea3-113">الإعاقة قصيرة الأجل</span><span class="sxs-lookup"><span data-stu-id="33ea3-113">Short-term disability</span></span>
- <span data-ttu-id="33ea3-114">إجازة Bereavement</span><span class="sxs-lookup"><span data-stu-id="33ea3-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="33ea3-115">إضافة نوع إجازة</span><span class="sxs-lookup"><span data-stu-id="33ea3-115">Add a leave type</span></span>

1. <span data-ttu-id="33ea3-116">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="33ea3-117">ضمن **الإعداد**، حدد **أنواع الإجازات والغياب**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="33ea3-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-118">Select **New**.</span></span>

4. <span data-ttu-id="33ea3-119">ادخل اسما لنوع الإجازة ضمن **النوع**، وحدد سير عمل من **معرف سير العمل**، وادخل وصفا ضمن **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="33ea3-120">في **عام**، حدد **بلا** أو **مجدول** أو **غير مجدول** من القائمة المنسدلة **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="33ea3-121">حدد كود دخل من القائمة المنسدلة **رمز الدخل**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="33ea3-122">ضمن **كود السبب المطلوب**، حدد ما إذا كنت ترغب في طلب كود سبب ام لا.</span><span class="sxs-lookup"><span data-stu-id="33ea3-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="33ea3-123">إذا كنت ترغب في طلب أكواد سبب، فقد تحتاج إلى اضافتها.</span><span class="sxs-lookup"><span data-stu-id="33ea3-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="33ea3-124">ضمن **أكواد السبب**، حدد **إضافة**، وحدد كود السبب، ثم حدد خانة الاختيار **ممكن** بجوارها.</span><span class="sxs-lookup"><span data-stu-id="33ea3-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="33ea3-125">ضمن **تقييد الوصول إلى الأدوار المحددة**، اختر ما إذا كنت ترغب في تقييد الوصول ام لا.</span><span class="sxs-lookup"><span data-stu-id="33ea3-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="33ea3-126">ثم حدد ادوار الأمان ضمن **ادوار الأمان لنوع الإجازة هذا**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="33ea3-127">يتم تحديد ادوار الأمان في سير العمل الذي حددته ضمن **معرف سير العمل** في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="33ea3-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="33ea3-128">ضمن **لون التقويم**، اختر اللون الذي سيتم عرضه في تقويمات المغادرة والغياب لهذا النوع من الغياب.</span><span class="sxs-lookup"><span data-stu-id="33ea3-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="33ea3-129">ضمن **علاقات التعليق‬**، اختر إن كنت تريد أن يقوم نوع الإجازة هذا بتعليق نوع إجازة آخر أو أن يتم تعليقه بواسطة نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="33ea3-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="33ea3-130">عند تقديم طلب إذن غياب لنوع الإجازة المعلق، سيتم إنشاء تعليق الإجازة بشكل تلقائي لنوع الإجازة المعلق.</span><span class="sxs-lookup"><span data-stu-id="33ea3-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="33ea3-131">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="33ea3-132">تكوين قواعد أنواع الإجازة</span><span class="sxs-lookup"><span data-stu-id="33ea3-132">Configure leave type rules</span></span>

1. <span data-ttu-id="33ea3-133">تعيين خيارات التقريب لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="33ea3-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="33ea3-134">تتضمن الخيارات **بلا**، و **لأعلى** و **لأسفل** و **الأقرب**.</span><span class="sxs-lookup"><span data-stu-id="33ea3-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="33ea3-135">يمكنك أيضا تعيين دقه التقريب لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="33ea3-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="33ea3-136">قم بتعيين **تصحيح الإجازة** لنوع العطلة.</span><span class="sxs-lookup"><span data-stu-id="33ea3-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="33ea3-137">عند تحديد هذا الخيار، تستخدم Human Resources عدد العطلات التي تقع في يوم العمل لتحديد كيفيه استحقاق الوقت لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="33ea3-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="33ea3-138">على سبيل المثال، إذا كان يوم عيد الميلاد يوم الاثنين، فإن Human Resources سيطرح يومًا واحدًا من نوع الإجازة عند معالجه الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="33ea3-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="33ea3-139">يمكنك تعيين العطلات في تقويم وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="33ea3-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="33ea3-140">لمزيد من المعلومات، راجع [إنشاء تقويم وقت العمل](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="33ea3-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="33ea3-141">عيّن **نوع الإجازة المنقولة** لنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="33ea3-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="33ea3-142">عند تحديد هذا الخيار، سيتم تحويل الأرصدة المنقولة إلى نوع الإجازة المحدد.</span><span class="sxs-lookup"><span data-stu-id="33ea3-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="33ea3-143">كما يجب تضمين نوع الإجازة المنقولة في خطة الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="33ea3-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
4. <span data-ttu-id="33ea3-144">حدد **قواعد انتهاء الصلاحية** لنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="33ea3-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="33ea3-145">عند تكوين هذا الخيار، يمكنك اختيار وحدة الأيام أو الأشهر وتعيين مدة انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="33ea3-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiration.</span></span> <span data-ttu-id="33ea3-146">يتم استخدام تاريخ السريان لقاعدة انتهاء الصلاحية لتحديد وقت بدء تشغيل وظيفة الدفعة التي تقوم بمعالجة انتهاء صلاحية الإجازة، أو تاريخ سريان مفعول القاعدة.</span><span class="sxs-lookup"><span data-stu-id="33ea3-146">The effective date of the expiration rule is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="33ea3-147">سيتم دائمًا إجراء انتهاء الصلاحية نفسه في تاريخ بدء فترة الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="33ea3-147">The expiration itself will always occur on the accrual period start date.</span></span> <span data-ttu-id="33ea3-148">على سبيل المثال، إذا كان تاريخ بدء فترة الاستحقاق هو 3 أغسطس، 2021، وتم تعيين قاعدة انتهاء الصلاحية إلى 6 أشهر، ستتم معالجة القاعدة استنادًا إلى مقابل انتهاء الصلاحية من تاريخ بدء فترة الاستحقاق، ولذلك سيتم تنفيذها في 3 فبراير، 2022.</span><span class="sxs-lookup"><span data-stu-id="33ea3-148">For example, if the accrual period start date is August 3, 2021, and the expiration rule was set at 6 months, the rule will be processed based on the expiration offset from the accrual period start date, so it would be executed on February 3, 2022.</span></span> <span data-ttu-id="33ea3-149">سيتم طرح أي أرصدة إجازات موجودة عند انتهاء الصلاحية من نوع الإجازة وستظهر في رصيد الإجازة.</span><span class="sxs-lookup"><span data-stu-id="33ea3-149">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span>
 
## <a name="see-also"></a><span data-ttu-id="33ea3-150">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="33ea3-150">See also</span></span>

- [<span data-ttu-id="33ea3-151">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="33ea3-151">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="33ea3-152">إنشاء خطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="33ea3-152">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="33ea3-153">إنشاء تقويم مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="33ea3-153">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="33ea3-154">تعليق الإجازة</span><span class="sxs-lookup"><span data-stu-id="33ea3-154">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)
- [<span data-ttu-id="33ea3-155">إنشاء سير عمل طلب شراء إجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="33ea3-155">Create a buy and sell leave request workflow</span></span>](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
