---
title: مفاهيم الإجازة والغياب
description: يصف هذا الموضوع مفاهيم الإجازة والغياب، وكيفية تحديد أرصدة زمن التوقف.
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303171"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="7e73f-103">مفاهيم الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="7e73f-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7e73f-104">بإمكان المفاهيم والمصطلحات التي تم وصفها في هذا الموضوع أن تساعدك في تحديد كيفية منح زمن توقف لأحد الموظفين وكيفية احتساب أرصدة الوقت لهذا الموظف.</span><span class="sxs-lookup"><span data-stu-id="7e73f-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="7e73f-105">للحصول على مزيد من المعلومات حول إدارة الغياب والإجازات، راجع [إدارة الغياب والإجازات](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="7e73f-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="7e73f-106">تفاصيل خطة الإجازة</span><span class="sxs-lookup"><span data-stu-id="7e73f-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="7e73f-107">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="7e73f-107">Start date</span></span>

<span data-ttu-id="7e73f-108">تاريخ البدء هو التاريخ الذي تبدأ فيه معالجة الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="7e73f-109">ويعمل تاريخ البدء أيضًا كتاريخ الذكرى السنوية التي يتم استخدامها لحساب المقادير المنقولة.</span><span class="sxs-lookup"><span data-stu-id="7e73f-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="7e73f-110">استحقاقات</span><span class="sxs-lookup"><span data-stu-id="7e73f-110">Accruals</span></span>

<span data-ttu-id="7e73f-111">تحدد الاستحقاقات متى يتم منح زمن توقف للموظف ومدى تكرار ذلك.</span><span class="sxs-lookup"><span data-stu-id="7e73f-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="7e73f-112">تم تعريف السياسات المتعلقة بتوقيت منح الاستحقاقات والسياسات المتعلقة بالتناسب في قسم **الاستحقاقات** عند إعداد خطة الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="7e73f-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="7e73f-113">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-113">Accrual frequency</span></span>

<span data-ttu-id="7e73f-114">يحدد معدل تكرار الاستحقاق عدد مرات استحقاق أو منح إجازة.</span><span class="sxs-lookup"><span data-stu-id="7e73f-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="7e73f-115">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="7e73f-115">The following options are available:</span></span>

- <span data-ttu-id="7e73f-116">يوميًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-116">Daily</span></span>
- <span data-ttu-id="7e73f-117">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-117">Weekly</span></span>
- <span data-ttu-id="7e73f-118">نصف أسبوعي</span><span class="sxs-lookup"><span data-stu-id="7e73f-118">Biweekly</span></span>
- <span data-ttu-id="7e73f-119">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="7e73f-119">Semimonthly</span></span>
- <span data-ttu-id="7e73f-120">شهريًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-120">Monthly</span></span>
- <span data-ttu-id="7e73f-121">ربع سنوي</span><span class="sxs-lookup"><span data-stu-id="7e73f-121">Quarterly</span></span>
- <span data-ttu-id="7e73f-122">نصف سنوي</span><span class="sxs-lookup"><span data-stu-id="7e73f-122">Semiannually</span></span>
- <span data-ttu-id="7e73f-123">سنويًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-123">Annually</span></span>
- <span data-ttu-id="7e73f-124">بلا</span><span class="sxs-lookup"><span data-stu-id="7e73f-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="7e73f-125">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-125">Accrual period basis</span></span>

<span data-ttu-id="7e73f-126">يحدد أساس فترة الاستحقاق التاريخ المستخدم لحساب فترات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="7e73f-127">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="7e73f-127">The following options are available:</span></span>

- <span data-ttu-id="7e73f-128">**تاريخ بدء الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-128">**Plan start date**</span></span>
- <span data-ttu-id="7e73f-129">**تاريخ خاص بالموظف** – عند تحديد هذا الخيار، تحدد القيمة مصدر قيمة التاريخ الأولية التي يتم استخدامها لحساب فترات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="7e73f-130">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="7e73f-130">The following options are available:</span></span>

    - <span data-ttu-id="7e73f-131">مخصص</span><span class="sxs-lookup"><span data-stu-id="7e73f-131">Custom</span></span>
    - <span data-ttu-id="7e73f-132">تاريخ التفعيل السنوي</span><span class="sxs-lookup"><span data-stu-id="7e73f-132">Anniversary date</span></span>
    - <span data-ttu-id="7e73f-133">تاريخ التوظيف الأصلي</span><span class="sxs-lookup"><span data-stu-id="7e73f-133">Original hire date</span></span>
    - <span data-ttu-id="7e73f-134">تاريخ الأقدمية</span><span class="sxs-lookup"><span data-stu-id="7e73f-134">Seniority date</span></span>
    - <span data-ttu-id="7e73f-135">تاريخ البدء المعدل للعامل</span><span class="sxs-lookup"><span data-stu-id="7e73f-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="7e73f-136">تاريخ البدء للعامل</span><span class="sxs-lookup"><span data-stu-id="7e73f-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="7e73f-137">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-137">Accrual award date</span></span>

<span data-ttu-id="7e73f-138">يحدد تاريخ منح الاستحقاقات متى يتم منح زمن توقف للموظف.</span><span class="sxs-lookup"><span data-stu-id="7e73f-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="7e73f-139">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="7e73f-139">The following options are available:</span></span>

- <span data-ttu-id="7e73f-140">**تاريخ انتهاء فترة الاستحقاق** – سيُمنح الموظف زمن توقف في اليوم الأخير من فترة المنحة.</span><span class="sxs-lookup"><span data-stu-id="7e73f-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="7e73f-141">لتمكين استحقاق القيمة الصحيحة، يجب أن تتضمن عملية الاستحقاق الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="7e73f-142">على سبيل المثال، فترة الاستحقاق هي 1 يناير 2018 حتى 31 يناير 2018.</span><span class="sxs-lookup"><span data-stu-id="7e73f-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="7e73f-143">وفي هذه الحالة، لكي يتم تضمين شهر يناير، يجب تشغيل الاستحقاق لتاريخ 1 فبراير 2018.</span><span class="sxs-lookup"><span data-stu-id="7e73f-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="7e73f-144">**تاريخ بدء فترة الاستحقاق** – سيُمنح الموظف زمن توقف في اليوم الأول من فترة المنحة.</span><span class="sxs-lookup"><span data-stu-id="7e73f-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="7e73f-145">سياسة الاستحقاقات عند التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="7e73f-146">تحدد سياسة الاستحقاقات عند التسجيل كيفية حساب الاستحقاق عندما يتم تسجيل موظف في منتصف فترة استحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="7e73f-147">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="7e73f-147">The following options are available:</span></span>

- <span data-ttu-id="7e73f-148">**مقسم بالتناسب** – يتم استخدام نطاق التاريخ بين تاريخ التسجيل وتاريخ البدء لتحديد الفرق في الأيام.</span><span class="sxs-lookup"><span data-stu-id="7e73f-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="7e73f-149">يتم تطبيق هذا الفرق عند معالجة الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="7e73f-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="7e73f-150">**الاستحقاق الكامل** - يُمنح مقدار الاستحقاق الكامل استنادًا إلى الطبقة، خلال معالجة الاستحقاق الأولى.</span><span class="sxs-lookup"><span data-stu-id="7e73f-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="7e73f-151">**لا يوجد استحقاق** -لا يتم منح أي استحقاق حتى فترة الاستحقاق التالية.</span><span class="sxs-lookup"><span data-stu-id="7e73f-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="7e73f-152">سياسة الاستحقاقات عند إلغاء التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="7e73f-153">تحدد سياسة الاستحقاقات عند إلغاء التسجيل كيفية حساب الاستحقاق عندما يتم إلغاء تسجيل موظف في منتصف فترة استحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="7e73f-154">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="7e73f-154">The following options are available:</span></span>

- <span data-ttu-id="7e73f-155">**مقسم بالتناسب** – يتم استخدام نطاق التاريخ بين تاريخ التسجيل وتاريخ البدء لتحديد الفرق في الأيام.</span><span class="sxs-lookup"><span data-stu-id="7e73f-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="7e73f-156">يتم تطبيق هذا الفرق عند معالجة الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="7e73f-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="7e73f-157">**الاستحقاق الكامل** - يُمنح مقدار الاستحقاق الكامل استنادًا إلى الطبقة، خلال معالجة الاستحقاق الأولى.</span><span class="sxs-lookup"><span data-stu-id="7e73f-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="7e73f-158">**لا يوجد استحقاق** -لا يتم منح أي استحقاق حتى فترة الاستحقاق التالية.</span><span class="sxs-lookup"><span data-stu-id="7e73f-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="7e73f-159">جدول الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-159">Accrual schedule</span></span>

<span data-ttu-id="7e73f-160">يحدد جدول الاستحقاق كيف سيقوم الموظف بتجميع زمن التوقف، والمقادير التي سيقوم الموظف بتجميعها ونقلها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="7e73f-161">يمكنك إنشاء طبقات حيث يتم منح زمن التوقف على مستويات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="7e73f-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="7e73f-162">أشهر الخدمة</span><span class="sxs-lookup"><span data-stu-id="7e73f-162">Months of service</span></span>

<span data-ttu-id="7e73f-163">تحدد قيمة **أشهر الخدمة** الحد الأدنى لعدد الأشهر التي يجب أن يعمل خلالها الموظفون لكي يتأهلوا للحصول على الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="7e73f-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="7e73f-164">في حال عدم وجود أي حد أدنى مطلوب للموظفين، فعيّن القيمة إلى **0**.</span><span class="sxs-lookup"><span data-stu-id="7e73f-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="7e73f-165">ساعات العمل</span><span class="sxs-lookup"><span data-stu-id="7e73f-165">Hours worked</span></span>

<span data-ttu-id="7e73f-166">تحدد قيمة **ساعات العمل** الحد الأدنى لعدد الساعات التي يجب أن يعمل خلالها الموظفون لكل فترة استحقاق لكي يتأهلوا للحصول على الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="7e73f-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="7e73f-167">في حال عدم وجود أي حد أدنى مطلوب للموظفين، فعيّن القيمة إلى **0**.</span><span class="sxs-lookup"><span data-stu-id="7e73f-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="7e73f-168">مقدار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-168">Accrual amount</span></span>

<span data-ttu-id="7e73f-169">مقدار الاستحقاق هو عدد الساعات أو الأيام التي سيستحق خلالها زمن التوقف للموظفين لكل فترة.</span><span class="sxs-lookup"><span data-stu-id="7e73f-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="7e73f-170">تستند الفترة إلى معدل تكرار الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="7e73f-171">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-171">Minimum balance</span></span>

<span data-ttu-id="7e73f-172">يمكن استخدام قيمة سالبة للحد الأدنى من الرصيد إذا كان باستطاعة الموظفين طلب إجازة تتجاوز الفترة المتوفرة لهم.</span><span class="sxs-lookup"><span data-stu-id="7e73f-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="7e73f-173">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-173">Maximum carry-forward</span></span>

<span data-ttu-id="7e73f-174">ستقوم عملية الاستحقاق بضبط أرصدة الإجازات التي تتجاوز الحد الأقصى للرصيد المنقول في الذكرى السنوية لتاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="7e73f-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="7e73f-175">المقدار الممنوح</span><span class="sxs-lookup"><span data-stu-id="7e73f-175">Grant amount</span></span>

<span data-ttu-id="7e73f-176">المقدار الممنوح هو الرقم الأولي لعدد الساعات أو الأيام التي يتم منحها للموظفين عند تسجيلهم في خطة الإجازة في بادئ الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e73f-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="7e73f-177">لا يستحق المقدار لكل فترة استحقاق.</span><span class="sxs-lookup"><span data-stu-id="7e73f-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="7e73f-178">التسجيلات والأرصدة</span><span class="sxs-lookup"><span data-stu-id="7e73f-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="7e73f-179">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-179">Enrollment date</span></span>

<span data-ttu-id="7e73f-180">يحدد تاريخ التسجيل الوقت الذي يبدأ فيه الموظف تجميع زمن التوقف.</span><span class="sxs-lookup"><span data-stu-id="7e73f-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="7e73f-181">على سبيل المثال، في حالة تسجيل موظف في خطة الإجازة في 15 يونيو 2018، فسيتعذر عليه تجميع أي زمن توقف قبل 15 يونيو 2018.</span><span class="sxs-lookup"><span data-stu-id="7e73f-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="7e73f-182">الرصيد الحالي</span><span class="sxs-lookup"><span data-stu-id="7e73f-182">Current balance</span></span>

<span data-ttu-id="7e73f-183">الرصيد الحالي هو مقدار الإجازة المتوفر لطلبات زمن التوقف.</span><span class="sxs-lookup"><span data-stu-id="7e73f-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="7e73f-184">ويشتمل هذا المقدار على الاستحقاقات والطلبات الموافق عليها والتسويات عبر التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="7e73f-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="7e73f-185">أمثلة عن الرصيد الحالي</span><span class="sxs-lookup"><span data-stu-id="7e73f-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="7e73f-186">الخطة السنوية</span><span class="sxs-lookup"><span data-stu-id="7e73f-186">Annual plan</span></span>

<span data-ttu-id="7e73f-187">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-187">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-188">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-188">Plan start date</span></span> | <span data-ttu-id="7e73f-189">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-189">Enrollment date</span></span> | <span data-ttu-id="7e73f-190">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-190">Accrual frequency</span></span> | <span data-ttu-id="7e73f-191">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-191">Accrual period basis</span></span> | <span data-ttu-id="7e73f-192">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="7e73f-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-193">1/1/2018</span></span>        | <span data-ttu-id="7e73f-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-194">1/1/2018</span></span>        | <span data-ttu-id="7e73f-195">سنوي</span><span class="sxs-lookup"><span data-stu-id="7e73f-195">Annual</span></span>            | <span data-ttu-id="7e73f-196">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-196">Plan start date</span></span>      | <span data-ttu-id="7e73f-197">انتهاء فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-197">End of accrual period</span></span> |

<span data-ttu-id="7e73f-198">تتم معالجة الاستحقاقات في 1 يناير 2019 (1/1/2019)، بحيث يتم تضمين تلك الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="7e73f-199">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-199">**Results**</span></span>

| <span data-ttu-id="7e73f-200">مقدار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-200">Accrual amount</span></span> | <span data-ttu-id="7e73f-201">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-201">Minimum balance</span></span> | <span data-ttu-id="7e73f-202">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-202">Maximum carry-forward</span></span> | <span data-ttu-id="7e73f-203">المقدار المطلوب</span><span class="sxs-lookup"><span data-stu-id="7e73f-203">Request amount</span></span> | <span data-ttu-id="7e73f-204">الرصيد الحالي (اعتبارًا من 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="7e73f-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="7e73f-205">200</span><span class="sxs-lookup"><span data-stu-id="7e73f-205">200</span></span>            | <span data-ttu-id="7e73f-206">0</span><span class="sxs-lookup"><span data-stu-id="7e73f-206">0</span></span>               | <span data-ttu-id="7e73f-207">120</span><span class="sxs-lookup"><span data-stu-id="7e73f-207">120</span></span>                   | <span data-ttu-id="7e73f-208">40</span><span class="sxs-lookup"><span data-stu-id="7e73f-208">40</span></span>             | <span data-ttu-id="7e73f-209">160</span><span class="sxs-lookup"><span data-stu-id="7e73f-209">160</span></span>                              |

<span data-ttu-id="7e73f-210">الرصيد الحالي (160) = مقدار الاستحقاق (200)-المقدار المطلوب (40)</span><span class="sxs-lookup"><span data-stu-id="7e73f-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="7e73f-211">الخطة النصف الشهرية</span><span class="sxs-lookup"><span data-stu-id="7e73f-211">Semimonthly plan</span></span>

<span data-ttu-id="7e73f-212">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-212">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-213">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-213">Plan start date</span></span> | <span data-ttu-id="7e73f-214">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-214">Enrollment date</span></span> | <span data-ttu-id="7e73f-215">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-215">Accrual frequency</span></span> | <span data-ttu-id="7e73f-216">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-216">Accrual period basis</span></span> | <span data-ttu-id="7e73f-217">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="7e73f-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-218">1/1/2018</span></span>        | <span data-ttu-id="7e73f-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-219">2/1/2018</span></span>        | <span data-ttu-id="7e73f-220">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="7e73f-220">Semimonthly</span></span>       | <span data-ttu-id="7e73f-221">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-221">Plan start date</span></span>      | <span data-ttu-id="7e73f-222">انتهاء فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-222">End of accrual period</span></span> |

<span data-ttu-id="7e73f-223">تتم معالجة الاستحقاقات في 1 مايو 2018 (5/1/2018)، بحيث يتم تضمين تلك الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="7e73f-224">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-224">**Results**</span></span>

| <span data-ttu-id="7e73f-225">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-225">Accrual amount</span></span> | <span data-ttu-id="7e73f-226">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-226">Minimum balance</span></span> | <span data-ttu-id="7e73f-227">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-227">Maximum carry-forward</span></span> | <span data-ttu-id="7e73f-228">المقدار المطلوب</span><span class="sxs-lookup"><span data-stu-id="7e73f-228">Request amount</span></span> | <span data-ttu-id="7e73f-229">الرصيد الحالي (اعتبارًا من 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="7e73f-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="7e73f-230">5</span><span class="sxs-lookup"><span data-stu-id="7e73f-230">5</span></span>              | <span data-ttu-id="7e73f-231">0</span><span class="sxs-lookup"><span data-stu-id="7e73f-231">0</span></span>               | <span data-ttu-id="7e73f-232">120</span><span class="sxs-lookup"><span data-stu-id="7e73f-232">120</span></span>                   | <span data-ttu-id="7e73f-233">8</span><span class="sxs-lookup"><span data-stu-id="7e73f-233">8</span></span>              | <span data-ttu-id="7e73f-234">22</span><span class="sxs-lookup"><span data-stu-id="7e73f-234">22</span></span>                               |

<span data-ttu-id="7e73f-235">الرصيد الحالي (22) = مقدار الاستحقاق (5 × 6)-المقدار المطلوب (8)</span><span class="sxs-lookup"><span data-stu-id="7e73f-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="7e73f-236">الخطة الشهرية</span><span class="sxs-lookup"><span data-stu-id="7e73f-236">Monthly plan</span></span>

<span data-ttu-id="7e73f-237">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-237">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-238">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-238">Plan start date</span></span> | <span data-ttu-id="7e73f-239">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-239">Enrollment date</span></span> | <span data-ttu-id="7e73f-240">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-240">Accrual frequency</span></span> | <span data-ttu-id="7e73f-241">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-241">Accrual period basis</span></span> | <span data-ttu-id="7e73f-242">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="7e73f-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-243">1/1/2018</span></span>        | <span data-ttu-id="7e73f-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-244">2/1/2018</span></span>        | <span data-ttu-id="7e73f-245">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="7e73f-245">Semimonthly</span></span>       | <span data-ttu-id="7e73f-246">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-246">Plan start date</span></span>      | <span data-ttu-id="7e73f-247">انتهاء فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-247">End of accrual period</span></span> |

<span data-ttu-id="7e73f-248">تتم معالجة الاستحقاقات في 1 مايو 2018 (5/1/2018)، بحيث يتم تضمين تلك الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="7e73f-249">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-249">**Results**</span></span>

| <span data-ttu-id="7e73f-250">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-250">Accrual amount</span></span> | <span data-ttu-id="7e73f-251">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-251">Minimum balance</span></span> | <span data-ttu-id="7e73f-252">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-252">Maximum carry-forward</span></span> | <span data-ttu-id="7e73f-253">المقدار المطلوب</span><span class="sxs-lookup"><span data-stu-id="7e73f-253">Request amount</span></span> | <span data-ttu-id="7e73f-254">الرصيد الحالي (اعتبارًا من 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="7e73f-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="7e73f-255">5</span><span class="sxs-lookup"><span data-stu-id="7e73f-255">5</span></span>              | <span data-ttu-id="7e73f-256">0</span><span class="sxs-lookup"><span data-stu-id="7e73f-256">0</span></span>               | <span data-ttu-id="7e73f-257">120</span><span class="sxs-lookup"><span data-stu-id="7e73f-257">120</span></span>                   | <span data-ttu-id="7e73f-258">8</span><span class="sxs-lookup"><span data-stu-id="7e73f-258">8</span></span>              | <span data-ttu-id="7e73f-259">7</span><span class="sxs-lookup"><span data-stu-id="7e73f-259">7</span></span>                                |

<span data-ttu-id="7e73f-260">الرصيد الحالي (7) = مقدار الاستحقاق (5 × 3)-المقدار المطلوب (8)</span><span class="sxs-lookup"><span data-stu-id="7e73f-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="7e73f-261">الرصيد المتوقع</span><span class="sxs-lookup"><span data-stu-id="7e73f-261">Forecasted balance</span></span>

<span data-ttu-id="7e73f-262">يعتبر *الرصيد المتوقع* مقدار الإجازة المتوفرة في تاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="7e73f-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="7e73f-263">يتم توقع تسويات الاستحقاقات والأرصدة المنقولة حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="7e73f-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="7e73f-264">يتم استخدام المعادلة التالية:</span><span class="sxs-lookup"><span data-stu-id="7e73f-264">The following formula is used:</span></span>

<span data-ttu-id="7e73f-265">الرصيد المتوقع يوم الإثنين = الرصيد الحالي – الطلبات + الاستحقاق – التسوية المنقولة</span><span class="sxs-lookup"><span data-stu-id="7e73f-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="7e73f-266">أمثلة عن الرصيد المتوقع</span><span class="sxs-lookup"><span data-stu-id="7e73f-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="7e73f-267">الخطة السنوية</span><span class="sxs-lookup"><span data-stu-id="7e73f-267">Annual plan</span></span>

<span data-ttu-id="7e73f-268">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-268">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-269">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-269">Plan start date</span></span> | <span data-ttu-id="7e73f-270">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-270">Enrollment date</span></span> | <span data-ttu-id="7e73f-271">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-271">Accrual frequency</span></span> | <span data-ttu-id="7e73f-272">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-272">Accrual period basis</span></span> | <span data-ttu-id="7e73f-273">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="7e73f-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-274">1/1/2018</span></span>        | <span data-ttu-id="7e73f-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-275">1/1/2018</span></span>        | <span data-ttu-id="7e73f-276">سنوي</span><span class="sxs-lookup"><span data-stu-id="7e73f-276">Annual</span></span>            | <span data-ttu-id="7e73f-277">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-277">Plan start date</span></span>      | <span data-ttu-id="7e73f-278">انتهاء فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-278">End of accrual period</span></span> |

<span data-ttu-id="7e73f-279">تتم معالجة الاستحقاقات في 15 فبراير 2019 (2/15/2019)، بحيث يتم تضمين تلك الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="7e73f-280">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-280">**Results**</span></span>

| <span data-ttu-id="7e73f-281">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-281">Accrual amount</span></span> | <span data-ttu-id="7e73f-282">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-282">Minimum balance</span></span> | <span data-ttu-id="7e73f-283">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-283">Maximum carry-forward</span></span> | <span data-ttu-id="7e73f-284">الرصيد الحالي</span><span class="sxs-lookup"><span data-stu-id="7e73f-284">Current balance</span></span> | <span data-ttu-id="7e73f-285">الرصيد المتوقع (اعتبارًا من 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="7e73f-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="7e73f-286">20</span><span class="sxs-lookup"><span data-stu-id="7e73f-286">20</span></span>             | <span data-ttu-id="7e73f-287">0</span><span class="sxs-lookup"><span data-stu-id="7e73f-287">0</span></span>               | <span data-ttu-id="7e73f-288">20</span><span class="sxs-lookup"><span data-stu-id="7e73f-288">20</span></span>                    | <span data-ttu-id="7e73f-289">40</span><span class="sxs-lookup"><span data-stu-id="7e73f-289">40</span></span>              | <span data-ttu-id="7e73f-290">40</span><span class="sxs-lookup"><span data-stu-id="7e73f-290">40</span></span>                                   |

<span data-ttu-id="7e73f-291">الرصيد المتوقع (40) = مقدار الاستحقاق (20) + الرصيد الحالي (40) – التسوية المنقولة (20)</span><span class="sxs-lookup"><span data-stu-id="7e73f-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="7e73f-292">الخطة النصف الشهرية</span><span class="sxs-lookup"><span data-stu-id="7e73f-292">Semimonthly plan</span></span>

<span data-ttu-id="7e73f-293">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-293">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-294">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-294">Plan start date</span></span> | <span data-ttu-id="7e73f-295">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-295">Enrollment date</span></span> | <span data-ttu-id="7e73f-296">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-296">Accrual frequency</span></span> | <span data-ttu-id="7e73f-297">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-297">Accrual period basis</span></span> | <span data-ttu-id="7e73f-298">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="7e73f-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-299">1/1/2018</span></span>        | <span data-ttu-id="7e73f-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-300">2/1/2018</span></span>        | <span data-ttu-id="7e73f-301">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="7e73f-301">Semimonthly</span></span>       | <span data-ttu-id="7e73f-302">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-302">Plan start date</span></span>      | <span data-ttu-id="7e73f-303">انتهاء فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-303">End of accrual period</span></span> |

<span data-ttu-id="7e73f-304">تتم معالجة الاستحقاقات في 15 فبراير 2019 (2/15/2019)، بحيث يتم تضمين تلك الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="7e73f-305">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-305">**Results**</span></span>

| <span data-ttu-id="7e73f-306">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-306">Accrual amount</span></span> | <span data-ttu-id="7e73f-307">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-307">Minimum balance</span></span> | <span data-ttu-id="7e73f-308">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-308">Maximum carry-forward</span></span> | <span data-ttu-id="7e73f-309">الرصيد الحالي</span><span class="sxs-lookup"><span data-stu-id="7e73f-309">Current balance</span></span> | <span data-ttu-id="7e73f-310">الرصيد المتوقع (اعتبارًا من 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="7e73f-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="7e73f-311">5</span><span class="sxs-lookup"><span data-stu-id="7e73f-311">5</span></span>              | <span data-ttu-id="7e73f-312">0</span><span class="sxs-lookup"><span data-stu-id="7e73f-312">0</span></span>               | <span data-ttu-id="7e73f-313">20</span><span class="sxs-lookup"><span data-stu-id="7e73f-313">20</span></span>                    | <span data-ttu-id="7e73f-314">40</span><span class="sxs-lookup"><span data-stu-id="7e73f-314">40</span></span>              | <span data-ttu-id="7e73f-315">35</span><span class="sxs-lookup"><span data-stu-id="7e73f-315">35</span></span>                                   |

<span data-ttu-id="7e73f-316">الرصيد المتوقع (35) = مقدار الاستحقاق (5 × 3) + الرصيد الحالي (40) – التسوية المنقولة (20)</span><span class="sxs-lookup"><span data-stu-id="7e73f-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="7e73f-317">الخطة الشهرية</span><span class="sxs-lookup"><span data-stu-id="7e73f-317">Monthly plan</span></span>

<span data-ttu-id="7e73f-318">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-318">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-319">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-319">Plan start date</span></span> | <span data-ttu-id="7e73f-320">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-320">Enrollment date</span></span> | <span data-ttu-id="7e73f-321">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-321">Accrual frequency</span></span> | <span data-ttu-id="7e73f-322">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-322">Accrual period basis</span></span> | <span data-ttu-id="7e73f-323">تاريخ المكافأة المستحقة</span><span class="sxs-lookup"><span data-stu-id="7e73f-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="7e73f-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-324">1/1/2018</span></span>        | <span data-ttu-id="7e73f-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-325">2/1/2018</span></span>        | <span data-ttu-id="7e73f-326">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="7e73f-326">Semimonthly</span></span>       | <span data-ttu-id="7e73f-327">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-327">Plan start date</span></span>      | <span data-ttu-id="7e73f-328">انتهاء فترة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-328">End of accrual period</span></span> |

<span data-ttu-id="7e73f-329">تتم معالجة الاستحقاقات في 15 فبراير 2019 (2/15/2019)، بحيث يتم تضمين تلك الفترة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="7e73f-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="7e73f-330">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-330">**Results**</span></span>

| <span data-ttu-id="7e73f-331">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-331">Accrual amount</span></span> | <span data-ttu-id="7e73f-332">الحد الأدنى للرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-332">Minimum balance</span></span> | <span data-ttu-id="7e73f-333">الحد الأقصى للرصيد المنقول</span><span class="sxs-lookup"><span data-stu-id="7e73f-333">Maximum carry-forward</span></span> | <span data-ttu-id="7e73f-334">الرصيد الحالي</span><span class="sxs-lookup"><span data-stu-id="7e73f-334">Current balance</span></span> | <span data-ttu-id="7e73f-335">الرصيد المتوقع (اعتبارًا من 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="7e73f-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="7e73f-336">10</span><span class="sxs-lookup"><span data-stu-id="7e73f-336">10</span></span>             | <span data-ttu-id="7e73f-337">0</span><span class="sxs-lookup"><span data-stu-id="7e73f-337">0</span></span>               | <span data-ttu-id="7e73f-338">20</span><span class="sxs-lookup"><span data-stu-id="7e73f-338">20</span></span>                    | <span data-ttu-id="7e73f-339">40</span><span class="sxs-lookup"><span data-stu-id="7e73f-339">40</span></span>              | <span data-ttu-id="7e73f-340">30</span><span class="sxs-lookup"><span data-stu-id="7e73f-340">30</span></span>                                   |

<span data-ttu-id="7e73f-341">الرصيد المتوقع (30) = مقدار الاستحقاق (10 × 1) + الرصيد الحالي (40) – التسوية المنقولة (20)</span><span class="sxs-lookup"><span data-stu-id="7e73f-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="7e73f-342">أمثلة عن رصيد التناسب</span><span class="sxs-lookup"><span data-stu-id="7e73f-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="7e73f-343">الخطة الشهرية بالتناسب</span><span class="sxs-lookup"><span data-stu-id="7e73f-343">Prorated monthly plan</span></span>

<span data-ttu-id="7e73f-344">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-344">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-345">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-345">Plan start date</span></span> | <span data-ttu-id="7e73f-346">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-346">Accrual frequency</span></span> | <span data-ttu-id="7e73f-347">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="7e73f-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-348">1/1/2018</span></span>        | <span data-ttu-id="7e73f-349">شهريًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-349">Monthly</span></span>           | <span data-ttu-id="7e73f-350">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-350">Plan start date</span></span>      |

<span data-ttu-id="7e73f-351">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-351">**Results**</span></span>

| <span data-ttu-id="7e73f-352">الموظف</span><span class="sxs-lookup"><span data-stu-id="7e73f-352">Employee</span></span>            | <span data-ttu-id="7e73f-353">أشهر الخدمة</span><span class="sxs-lookup"><span data-stu-id="7e73f-353">Months of service</span></span> | <span data-ttu-id="7e73f-354">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-354">Enrollment date</span></span> | <span data-ttu-id="7e73f-355">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="7e73f-355">Start date</span></span> | <span data-ttu-id="7e73f-356">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-356">Accrual amount</span></span> | <span data-ttu-id="7e73f-357">معالجة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-357">Process accrual</span></span> | <span data-ttu-id="7e73f-358">الرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="7e73f-359">جانيت نيكولسون</span><span class="sxs-lookup"><span data-stu-id="7e73f-359">Jeannette Nicholson</span></span> | <span data-ttu-id="7e73f-360">0.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-360">0.00</span></span>              | <span data-ttu-id="7e73f-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-361">6/1/2018</span></span>        | <span data-ttu-id="7e73f-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-362">6/1/2018</span></span>   | <span data-ttu-id="7e73f-363">1.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-363">1.00</span></span>           | <span data-ttu-id="7e73f-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-364">9/1/2018</span></span>        | <span data-ttu-id="7e73f-365">3.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-365">3.00</span></span>    |
| <span data-ttu-id="7e73f-366">جاي نورمان</span><span class="sxs-lookup"><span data-stu-id="7e73f-366">Jay Norman</span></span>          | <span data-ttu-id="7e73f-367">0.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-367">0.00</span></span>              | <span data-ttu-id="7e73f-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-368">6/15/2018</span></span>       | <span data-ttu-id="7e73f-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-369">6/15/2018</span></span>  | <span data-ttu-id="7e73f-370">1.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-370">1.00</span></span>           | <span data-ttu-id="7e73f-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-371">9/1/2018</span></span>        | <span data-ttu-id="7e73f-372">2.53</span><span class="sxs-lookup"><span data-stu-id="7e73f-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="7e73f-373">الخطة الشهرية للاستحقاق الكامل</span><span class="sxs-lookup"><span data-stu-id="7e73f-373">Full accrual monthly plan</span></span>

<span data-ttu-id="7e73f-374">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-374">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-375">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-375">Plan start date</span></span> | <span data-ttu-id="7e73f-376">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-376">Accrual frequency</span></span> | <span data-ttu-id="7e73f-377">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="7e73f-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-378">1/1/2018</span></span>        | <span data-ttu-id="7e73f-379">شهريًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-379">Monthly</span></span>           | <span data-ttu-id="7e73f-380">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-380">Plan start date</span></span>      |

<span data-ttu-id="7e73f-381">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-381">**Results**</span></span>

| <span data-ttu-id="7e73f-382">الموظف</span><span class="sxs-lookup"><span data-stu-id="7e73f-382">Employee</span></span>            | <span data-ttu-id="7e73f-383">أشهر الخدمة</span><span class="sxs-lookup"><span data-stu-id="7e73f-383">Months of service</span></span> | <span data-ttu-id="7e73f-384">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-384">Enrollment date</span></span> | <span data-ttu-id="7e73f-385">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="7e73f-385">Start date</span></span> | <span data-ttu-id="7e73f-386">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-386">Accrual amount</span></span> | <span data-ttu-id="7e73f-387">معالجة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-387">Process accrual</span></span> | <span data-ttu-id="7e73f-388">الرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="7e73f-389">جانيت نيكولسون</span><span class="sxs-lookup"><span data-stu-id="7e73f-389">Jeannette Nicholson</span></span> | <span data-ttu-id="7e73f-390">0.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-390">0.00</span></span>              | <span data-ttu-id="7e73f-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-391">6/1/2018</span></span>        | <span data-ttu-id="7e73f-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-392">6/1/2018</span></span>   | <span data-ttu-id="7e73f-393">1.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-393">1.00</span></span>           | <span data-ttu-id="7e73f-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-394">9/1/2018</span></span>        | <span data-ttu-id="7e73f-395">3.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-395">3.00</span></span>    |
| <span data-ttu-id="7e73f-396">جاي نورمان</span><span class="sxs-lookup"><span data-stu-id="7e73f-396">Jay Norman</span></span>          | <span data-ttu-id="7e73f-397">0.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-397">0.00</span></span>              | <span data-ttu-id="7e73f-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-398">6/15/2018</span></span>       | <span data-ttu-id="7e73f-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-399">6/15/2018</span></span>  | <span data-ttu-id="7e73f-400">1.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-400">1.00</span></span>           | <span data-ttu-id="7e73f-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-401">9/1/2018</span></span>        | <span data-ttu-id="7e73f-402">3.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="7e73f-403">الخطة الشهرية بدون استحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-403">No accrual monthly plan</span></span>

<span data-ttu-id="7e73f-404">**إعداد الخطة**</span><span class="sxs-lookup"><span data-stu-id="7e73f-404">**Plan setup**</span></span>

| <span data-ttu-id="7e73f-405">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-405">Plan start date</span></span> | <span data-ttu-id="7e73f-406">معدل تكرار الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-406">Accrual frequency</span></span> | <span data-ttu-id="7e73f-407">أساس فترة الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="7e73f-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="7e73f-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-408">1/1/2018</span></span>        | <span data-ttu-id="7e73f-409">شهريًا</span><span class="sxs-lookup"><span data-stu-id="7e73f-409">Monthly</span></span>           | <span data-ttu-id="7e73f-410">تاريخ بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="7e73f-410">Plan start date</span></span>      |

<span data-ttu-id="7e73f-411">**النتائج**</span><span class="sxs-lookup"><span data-stu-id="7e73f-411">**Results**</span></span>

| <span data-ttu-id="7e73f-412">الموظف</span><span class="sxs-lookup"><span data-stu-id="7e73f-412">Employee</span></span>            | <span data-ttu-id="7e73f-413">أشهر الخدمة</span><span class="sxs-lookup"><span data-stu-id="7e73f-413">Months of service</span></span> | <span data-ttu-id="7e73f-414">تاريخ التسجيل</span><span class="sxs-lookup"><span data-stu-id="7e73f-414">Enrollment date</span></span> | <span data-ttu-id="7e73f-415">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="7e73f-415">Start date</span></span> | <span data-ttu-id="7e73f-416">مبلغ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-416">Accrual amount</span></span> | <span data-ttu-id="7e73f-417">معالجة الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="7e73f-417">Process accrual</span></span> | <span data-ttu-id="7e73f-418">الرصيد</span><span class="sxs-lookup"><span data-stu-id="7e73f-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="7e73f-419">جانيت نيكولسون</span><span class="sxs-lookup"><span data-stu-id="7e73f-419">Jeannette Nicholson</span></span> | <span data-ttu-id="7e73f-420">0.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-420">0.00</span></span>              | <span data-ttu-id="7e73f-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-421">6/1/2018</span></span>        | <span data-ttu-id="7e73f-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-422">6/1/2018</span></span>   | <span data-ttu-id="7e73f-423">1.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-423">1.00</span></span>           | <span data-ttu-id="7e73f-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-424">9/1/2018</span></span>        | <span data-ttu-id="7e73f-425">3.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-425">3.00</span></span>    |
| <span data-ttu-id="7e73f-426">جاي نورمان</span><span class="sxs-lookup"><span data-stu-id="7e73f-426">Jay Norman</span></span>          | <span data-ttu-id="7e73f-427">0.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-427">0.00</span></span>              | <span data-ttu-id="7e73f-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-428">6/15/2018</span></span>       | <span data-ttu-id="7e73f-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-429">6/15/2018</span></span>  | <span data-ttu-id="7e73f-430">1.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-430">1.00</span></span>           | <span data-ttu-id="7e73f-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="7e73f-431">9/1/2018</span></span>        | <span data-ttu-id="7e73f-432">2.00</span><span class="sxs-lookup"><span data-stu-id="7e73f-432">2.00</span></span>    |
