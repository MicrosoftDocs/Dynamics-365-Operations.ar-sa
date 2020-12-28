---
title: ‏‫تسجيل الغياب في الوقت والحضور
description: يشرح هذا الموضوع كيفية معالجة تسجيلات الغياب في الوقت والحضور.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16b338010662f8c2115fcc38f6830b58c49259e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421107"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="aa47f-103">‏‫تسجيل الغياب في الوقت والحضور</span><span class="sxs-lookup"><span data-stu-id="aa47f-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa47f-104">يوضح هذا الموضوع مفاهيم الغياب ويشرح كيفية معالجة الغياب في الوقت والحضور.</span><span class="sxs-lookup"><span data-stu-id="aa47f-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="aa47f-105">الغياب الذي يستند إلى ساعات عمل عادية</span><span class="sxs-lookup"><span data-stu-id="aa47f-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="aa47f-106">يتم اعتبار العاملين كغائبين لأي ساعات لا يعملونها أثناء ساعات عملهم العادية.</span><span class="sxs-lookup"><span data-stu-id="aa47f-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="aa47f-107">ويتم تحديد ساعات العمل العادية في ملف تعريف الوقت القياسي للعامل.</span><span class="sxs-lookup"><span data-stu-id="aa47f-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="aa47f-108">على سبيل المثال، عامل يعمل وفقًا لملف تعريف نهاري يبدأ عمله عند 7:00 صباحًا وينتهي عند 3:00 مساء.</span><span class="sxs-lookup"><span data-stu-id="aa47f-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="aa47f-109">إذا بدأ العامل عمله من الساعة 9:00 صباحًا، يعتبر غائبًا في الفترة من 7:00 صباحًا إلى 9:00 صباحًا في ذلك اليوم.</span><span class="sxs-lookup"><span data-stu-id="aa47f-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="aa47f-110">وفي هذه الحالة، تتم مطالبة العاملين بإدخال سبب للغياب.</span><span class="sxs-lookup"><span data-stu-id="aa47f-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="aa47f-111">ويمكنهم تحديد السبب عن طريق تحديد كود الغياب.</span><span class="sxs-lookup"><span data-stu-id="aa47f-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="aa47f-112">أكواد الغياب</span><span class="sxs-lookup"><span data-stu-id="aa47f-112">Absence codes</span></span>

<span data-ttu-id="aa47f-113">تحدد أكواد الغياب الأنواع المختلفة له.</span><span class="sxs-lookup"><span data-stu-id="aa47f-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="aa47f-114">ويتم تحديد أكواد الغياب بواسطة الشركة.</span><span class="sxs-lookup"><span data-stu-id="aa47f-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="aa47f-115">ويمكن تطبيق قواعد مختلفة على أكواد الغياب.</span><span class="sxs-lookup"><span data-stu-id="aa47f-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="aa47f-116">على سبيل المثال، يمكن تكوين كود غياب للخصم أو لمنح أجر.</span><span class="sxs-lookup"><span data-stu-id="aa47f-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="aa47f-117">على سبيل المثال، تحدد شركة ما كود غياب **متأخر** يستخدمه العاملون إذا أتوا متأخرين وليس لديهم أسباب وجيهة لذلك.</span><span class="sxs-lookup"><span data-stu-id="aa47f-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="aa47f-118">تحدد الشركة أيضًا كود غياب **دورة تدريبية داخلية** يستخدمه العاملون للوقت الذي يقضونه في حضور دورات تدريبية داخلية.</span><span class="sxs-lookup"><span data-stu-id="aa47f-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="aa47f-119">يمكن إعداد أكواد الغياب هذه بحيث يخصم الكود **متأخر** من أجر العامل، لكن لا يخصم الكود **دورة تدريبية داخلية** من أجره.</span><span class="sxs-lookup"><span data-stu-id="aa47f-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="aa47f-120">ويمكنك إعداد أكود غياب تلقائية.</span><span class="sxs-lookup"><span data-stu-id="aa47f-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="aa47f-121">يمكن استخدام أكواد الغياب هذه لحساب وقت العامل عند عدم تسجيل غياب.</span><span class="sxs-lookup"><span data-stu-id="aa47f-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="aa47f-122">يحدد ملف تعريف وقت العامل ما إذا كان يتم استخدام كود الغياب للوقت القياسي أو الوقت المرن.</span><span class="sxs-lookup"><span data-stu-id="aa47f-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="aa47f-123">إعداد الوقت القياسي والوقت المرن</span><span class="sxs-lookup"><span data-stu-id="aa47f-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="aa47f-124">يمكنك تكوين المعلمات للوقت القياسي والوقت المرن باستخدام الخيارات **‏‫إدخال الغياب تلقائيًا‬** و **‏‫إدخال الرصيد المرن تلقائيًا‬** الموجودة بصفحة **معلمات الوقت والحضور**.</span><span class="sxs-lookup"><span data-stu-id="aa47f-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="aa47f-125">مجموعات الغياب</span><span class="sxs-lookup"><span data-stu-id="aa47f-125">Absence groups</span></span>

<span data-ttu-id="aa47f-126">يتم تجميع أكواد الغياب في مجموعات الغياب.</span><span class="sxs-lookup"><span data-stu-id="aa47f-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="aa47f-127">يمكنك استخدام مجموعات الغياب لتجميع أكواد الغياب التي لها خصائص مشتركة.</span><span class="sxs-lookup"><span data-stu-id="aa47f-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="aa47f-128">تتضمن الأمثلة أكواد الغياب لسبب قانوني أو الغياب بسبب موعد مع طبيب أو للإدلاء بشهادة أو لرعاية طفل مريض.</span><span class="sxs-lookup"><span data-stu-id="aa47f-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="aa47f-129">الغياب المخطط</span><span class="sxs-lookup"><span data-stu-id="aa47f-129">Planned absence</span></span>

<span data-ttu-id="aa47f-130">إذا كنت تعرف أن أحد العمال سيتغيب لفترة ما، كالغياب في عطلة مقبلة، فيمكنك استخدام الغياب المخطط.</span><span class="sxs-lookup"><span data-stu-id="aa47f-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="aa47f-131">يمكنك إعداد الغياب المخطط عن طريق تكوين كود الغياب بحيث يأخذ الغياب المخطط في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="aa47f-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="aa47f-132">عند إعداد غياب مخطط، لا تتم مطالبتك بكود غياب أثناء فترة الغياب عند حساب التسجيلات الزمنية للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="aa47f-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="aa47f-133">يمكن تحديد الغياب المخطط لعامل واحد، أو يمكنك تحديد وظيفة دفعية للتحديث المجمع للغياب المخطط للعاملين.</span><span class="sxs-lookup"><span data-stu-id="aa47f-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="aa47f-134">إعداد الغياب المخطط</span><span class="sxs-lookup"><span data-stu-id="aa47f-134">Set up planned absence</span></span>

1. <span data-ttu-id="aa47f-135">حدد **الموارد البشرية** &gt; **العاملون** &gt; **الموظفون**، ثم حدد أحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="aa47f-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="aa47f-136">حدد **الوقت** &gt; **تعيينات الوقت** &gt; **تسجيل غياب الوقت**، وقم بإعداد الغياب المخطط.</span><span class="sxs-lookup"><span data-stu-id="aa47f-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="aa47f-137">الغياب المخطط المتقطع</span><span class="sxs-lookup"><span data-stu-id="aa47f-137">Interrupted planned absence</span></span>

<span data-ttu-id="aa47f-138">إذا قمت بتطبيق خيار **المقاطعة** عند إعداد غياب مخطط، فستتم مقاطعة الغياب المخطط إذا قام العامل بتسجيل الدخول أثناء فترة الغياب المخطط.</span><span class="sxs-lookup"><span data-stu-id="aa47f-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="aa47f-139">سيتم وضع علامة **تمت مقاطعته** على الغياب المخطط ولن يكون هناك أي تأثير على الحسابات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="aa47f-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="aa47f-140">إعداد غياب مخطط للمقاطعة</span><span class="sxs-lookup"><span data-stu-id="aa47f-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="aa47f-141">افتح الصفحة **تسجيل غياب الوقت** كما هو موضح في الإجراء لإعداد الغياب المخطط.</span><span class="sxs-lookup"><span data-stu-id="aa47f-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="aa47f-142">حدد **مقاطعة**.</span><span class="sxs-lookup"><span data-stu-id="aa47f-142">Select **Interrupt**.</span></span>

<span data-ttu-id="aa47f-143">يتم تطبيق الخيار **مقاطعة** عندما يتم تسجيل الوقت من خلال الوحدة الطرفية لحالة العمل أو جهاز مراقبة حالة العمل.</span><span class="sxs-lookup"><span data-stu-id="aa47f-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="aa47f-144">لا يتم تطبيق الخيار إذا تم إدخال التسجيلات في صفحات الحساب والموافقة أو في صفحة **بطاقة الوقت الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="aa47f-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="aa47f-145">أمثلة لاستخدام الغياب في ملف تعريف مرن</span><span class="sxs-lookup"><span data-stu-id="aa47f-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="aa47f-146">تبين الأمثلة الثلاثة التالية كيفية حساب الغياب في ملف تعريف به فترات مرنة.</span><span class="sxs-lookup"><span data-stu-id="aa47f-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="aa47f-147">تستخدم الأمثلة ملف التعريف التالي.</span><span class="sxs-lookup"><span data-stu-id="aa47f-147">The examples use the following profile.</span></span>

| <span data-ttu-id="aa47f-148">بدء العمل</span><span class="sxs-lookup"><span data-stu-id="aa47f-148">Clock-in</span></span> | <span data-ttu-id="aa47f-149">وقت قياسي</span><span class="sxs-lookup"><span data-stu-id="aa47f-149">Standard time</span></span>    | <span data-ttu-id="aa47f-150">مقاطعة</span><span class="sxs-lookup"><span data-stu-id="aa47f-150">Break</span></span>             | <span data-ttu-id="aa47f-151">وقت قياسي</span><span class="sxs-lookup"><span data-stu-id="aa47f-151">Standard time</span></span> | <span data-ttu-id="aa47f-152">مرن-</span><span class="sxs-lookup"><span data-stu-id="aa47f-152">Flex-</span></span>        | <span data-ttu-id="aa47f-153">إنهاء العمل</span><span class="sxs-lookup"><span data-stu-id="aa47f-153">Clock-out</span></span> | <span data-ttu-id="aa47f-154">مرن+</span><span class="sxs-lookup"><span data-stu-id="aa47f-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="aa47f-155">8 صباحًا</span><span class="sxs-lookup"><span data-stu-id="aa47f-155">8 AM</span></span>     | <span data-ttu-id="aa47f-156">9 صباحًا إلى 11:30 صباحًا</span><span class="sxs-lookup"><span data-stu-id="aa47f-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="aa47f-157">11:30 صباحًا إلى 12 مساءً</span><span class="sxs-lookup"><span data-stu-id="aa47f-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="aa47f-158">12 مساءً إلى 3 مساءً</span><span class="sxs-lookup"><span data-stu-id="aa47f-158">12 PM to 3 PM</span></span> | <span data-ttu-id="aa47f-159">3 مساءً إلى 4 مساءً</span><span class="sxs-lookup"><span data-stu-id="aa47f-159">3 PM to 4 PM</span></span> | <span data-ttu-id="aa47f-160">4 مساءً</span><span class="sxs-lookup"><span data-stu-id="aa47f-160">4 PM</span></span>      | <span data-ttu-id="aa47f-161">4 مساءً إلى 6 مساءً</span><span class="sxs-lookup"><span data-stu-id="aa47f-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="aa47f-162">مثال 1: تسجيل الخروج خلال فترة مرنة-</span><span class="sxs-lookup"><span data-stu-id="aa47f-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="aa47f-163">يبدأ العامل عمله عند الساعة 8:00 صباحًا وينتهي منه عند الساعة 3:30 مساءً.</span><span class="sxs-lookup"><span data-stu-id="aa47f-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="aa47f-164">في هذه الحالة، نظرًا لأن العامل ينتهي من العمل أثناء فترة مرنة-، لا يتم حساب أي غياب، ويتم اقتطاع نصف ساعة من الرصيد المرن للعامل.</span><span class="sxs-lookup"><span data-stu-id="aa47f-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="aa47f-165">مثال 2: تسجيل الخروج خلال فترة وقت قياسي</span><span class="sxs-lookup"><span data-stu-id="aa47f-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="aa47f-166">يبدأ العامل عمله عند الساعة 8:00 صباحًا وينتهي منه عند الساعة 2:30 مساءً.</span><span class="sxs-lookup"><span data-stu-id="aa47f-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="aa47f-167">في هذه الحالة، نظرًا لأن العامل ينتهي من العمل أثناء فترة وقت قياسي، يتم حساب الغياب من الساعة 2:30 مساءً إلى 4 مساءً، ويتم تسجيل فترة غياب مدتها ساعة ونصف.</span><span class="sxs-lookup"><span data-stu-id="aa47f-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="aa47f-168">وتتطلب هذه الفترة كود غياب.</span><span class="sxs-lookup"><span data-stu-id="aa47f-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="aa47f-169">مثال 3: تسجيل الخروج خلال فترة مرنة+</span><span class="sxs-lookup"><span data-stu-id="aa47f-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="aa47f-170">يبدأ العامل عمله عند الساعة 8:00 صباحًا وينتهي منه عند الساعة 4:30 مساءً.</span><span class="sxs-lookup"><span data-stu-id="aa47f-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="aa47f-171">في هذه الحالة، نظرًا لأن العامل ينتهي من العمل أثناء فترة مرنة+، لا يتم حساب أي غياب، وتتم إضافة نصف ساعة إلى الرصيد المرن للعامل.</span><span class="sxs-lookup"><span data-stu-id="aa47f-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="aa47f-172">الغياب في عملية الحساب والموافقة</span><span class="sxs-lookup"><span data-stu-id="aa47f-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="aa47f-173">يجب حساب تسجيلات وقت العامل والموافقة عليها قبل تحويلها إلى نظام الرواتب كأصناف للدفع.</span><span class="sxs-lookup"><span data-stu-id="aa47f-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="aa47f-174">ويمكن للموافق تغيير تسجيلات وقت العامل.</span><span class="sxs-lookup"><span data-stu-id="aa47f-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="aa47f-175">يمكن للموافق كذلك تغيير أي غياب قد سجله العامل.</span><span class="sxs-lookup"><span data-stu-id="aa47f-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="aa47f-176">إذا قام الموافق بإدخال فترة زمنية تحتوي على كود غياب يدويًا، لا يتم تجاوز كود الغياب لتلك الفترة بواسطة كود الغياب الافتراضي من معلمات الوقت والحضور.</span><span class="sxs-lookup"><span data-stu-id="aa47f-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="aa47f-177">على سبيل المثال، تبدأ عاملة عملها عند الساعة 10 صباحًا وتقوم بتحديد كود غياب يشير إلى أنها متأخرة.</span><span class="sxs-lookup"><span data-stu-id="aa47f-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="aa47f-178">بعد ذلك، تخبر العاملة مشرفها بأنه كان لديها موعد لدى طبيب من الساعة 8 صباحًا إلى 10 صباحًا.</span><span class="sxs-lookup"><span data-stu-id="aa47f-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="aa47f-179">يجب ألا يتسبب موعد الطبيب في خصم من أجر العاملة.</span><span class="sxs-lookup"><span data-stu-id="aa47f-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="aa47f-180">لذلك، في هذه الحالة، يمكن للمشرف تعديل ساعتي الغياب من 8 صباحًا إلى 10 صباحًا بإدخال كود غياب يدويًا يشير إلى سبب مرضي لهاتين الساعتين.</span><span class="sxs-lookup"><span data-stu-id="aa47f-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="aa47f-181">حساب الغياب والموافقة عليه</span><span class="sxs-lookup"><span data-stu-id="aa47f-181">Calculate and approve absence</span></span>

- <span data-ttu-id="aa47f-182">حدد **الحضور الزمني** &gt; **المراجعة والموافقة** &gt; **الموافقة أو الحساب**.</span><span class="sxs-lookup"><span data-stu-id="aa47f-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>
