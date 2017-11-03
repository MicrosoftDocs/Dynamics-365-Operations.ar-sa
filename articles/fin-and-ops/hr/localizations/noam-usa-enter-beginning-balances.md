---
title: "إدخال أرصدة البداية لكشف الرواتب"
description: "يصف الموضوع الخطوات الخاصة بإدخال أرصدة البداية لأكواد الأرباح‬ والخصومات والمزايا والضرائب. تعتبر هذه المعلومات قيّمة بالنسبة إلى الشركاء الذين يريدون ترحيل البيانات الخاصة بتطبيق كشف رواتب‬ جديد أو نقلها من نظام آخر."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceaf56573c99bb257aed127af5e15ee2a7a961a5
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="03da5-104">إدخال أرصدة البداية لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="03da5-104">Enter payroll beginning balances</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="03da5-105">يصف الموضوع الخطوات الخاصة بإدخال أرصدة البداية لأكواد الأرباح‬ والخصومات والمزايا والضرائب.</span><span class="sxs-lookup"><span data-stu-id="03da5-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="03da5-106">تعتبر هذه المعلومات قيمة بالنسبة إلى الشركاء الذين ينقلون البيانات الخاصة بتطبيق كشف رواتب‬ جديد من نظام آخر.</span><span class="sxs-lookup"><span data-stu-id="03da5-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="03da5-107">استعدادًا لإدخال أرصدة البداية لكشف الرواتب، نتحقق من صحة المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="03da5-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="03da5-108">تم إدخال سجلات الموظفين وهي متاحة في النظام</span><span class="sxs-lookup"><span data-stu-id="03da5-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="03da5-109">تم إعداد البيانات التالية وتعيينها للموظفين:</span><span class="sxs-lookup"><span data-stu-id="03da5-109">The following data is set up and assigned to employees:</span></span>

> > * <span data-ttu-id="03da5-110">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="03da5-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="03da5-111">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="03da5-111">Earning codes</span></span>
> > * <span data-ttu-id="03da5-112">الضرائب</span><span class="sxs-lookup"><span data-stu-id="03da5-112">Taxes</span></span>
> > * <span data-ttu-id="03da5-113">الميزات والخصومات</span><span class="sxs-lookup"><span data-stu-id="03da5-113">Benefits and deductions</span></span>

> * <span data-ttu-id="03da5-114">يجب على الشركة اختيار تاريخ حيث يمكن تعيين أرصدة البداية لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="03da5-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>

> * <span data-ttu-id="03da5-115">تم تجميع معلومات حول كافة الأرباح والميزات/الخصومات، ومساهمات الميزات، وضرائب الموظفين وضرائب أصحاب العمل والمبالغ حتى تاريخه من النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="03da5-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="03da5-116">بينما تخطط لإدخال أرصدة البداية، يجب أن تأخذ في الاعتبار إلى أي مدى يجب أن تكون البيانات مفصلة.</span><span class="sxs-lookup"><span data-stu-id="03da5-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="03da5-117">يقوم معظم الشركات بإدخال مبلغ واحد مدمج للسنة حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="03da5-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="03da5-118">ومع ذلك، إذا كانت هناك حاجة إلى مزيد من المعلومات التفصيلية، فيمكن إدخال الأرصدة بتزايدات ربع سنوية.</span><span class="sxs-lookup"><span data-stu-id="03da5-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="03da5-119">من خلال تقرير مستوى التفصيل المطلوب يتحدد عدد قوائم الأجور‬ اليدوية التي يجب إنشاؤها لكل العامل.</span><span class="sxs-lookup"><span data-stu-id="03da5-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="03da5-120">لمدة سنة واحدة حتى تاريخه، هناك حاجة إلى كشف حساب يدوي واحد فقط لكل موظف.</span><span class="sxs-lookup"><span data-stu-id="03da5-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="03da5-121">للقيام بذلك، استخدم مبالغ السنة حتى تاريخه من قوائم الأجور النهائية من النظام السابق كالمبلغ الذي تم إدخاله في نظام كشف الرواتب الجديد.</span><span class="sxs-lookup"><span data-stu-id="03da5-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="03da5-122">يوضح المثال التالي كيفية إدخال أرصدة البداية لكشف رواتب الموظف، بما في ذلك أكواد الأرباح‬ والميزات/الخصومات والضرائب.</span><span class="sxs-lookup"><span data-stu-id="03da5-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="03da5-123">في مثال واقعي، سيتوفر لديك بند لكل كود ربح وخصم الميزة ومساهمة الميزة وضريبة الموظف وضريبة رب العمل مع المبلغ الذي تم إدخاله للسنة حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="03da5-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="03da5-124">باستخدام قائمة الأكواد والمبالغ هذه، اتبع الخطوات لإنشاء كشف يدوي للأرباح وقوائم الأجور مع تعطيل المحاسبة لنقل الأرصدة الافتتاحية لأغراض تتعلق بالرواتب.</span><span class="sxs-lookup"><span data-stu-id="03da5-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="03da5-125">ستقوم بتعطيل المحاسبة لأنك لا ترغب في ترحيل قوائم الأجور لرصيد البداية إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="03da5-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="03da5-126">كان ذلك يتم في النظام القديم وسينتقل إلى النظام الجديد عند تعيين أرصدة البداية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="03da5-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="03da5-127">أ.</span><span class="sxs-lookup"><span data-stu-id="03da5-127">A.</span></span> <span data-ttu-id="03da5-128">كيفية إعداد أكواد الإيرادات لاستخدامه على أرصدة البداية لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="03da5-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="03da5-129">عندما تقوم بإدخال أرصدة البداية لكشف الرواتب، تأكد من تكوين أكواد الأرباح التي ستستخدمها مع تمكين خيار "السماح بتحرير أسعار كشف الأرباح‬".</span><span class="sxs-lookup"><span data-stu-id="03da5-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="03da5-130">سيسمح لك ذلك بإدخال المبلغ من النظام القديم يدويًا.</span><span class="sxs-lookup"><span data-stu-id="03da5-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="03da5-131">ب.</span><span class="sxs-lookup"><span data-stu-id="03da5-131">B.</span></span> <span data-ttu-id="03da5-132">إنشاء كشف أرباح لأحد الموظفين للحصول على رصيد البداية</span><span class="sxs-lookup"><span data-stu-id="03da5-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="03da5-133">تنشئ هذه الخطوة يدويًا كشف أرباح لكل عامل لفترة الدفع‬ الأخيرة من النظام القديم، مما يؤدي إلى إنشاء بنود كشف الأرباح‬ في نظام كشف الرواتب الجديد.</span><span class="sxs-lookup"><span data-stu-id="03da5-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="03da5-134">أدخل بندًا واحدًا لكل كود أرباح‬ ومبلغ السنة والساعات حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="03da5-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="03da5-135">الخطوات النموذجية هي على الشكل التالي:</span><span class="sxs-lookup"><span data-stu-id="03da5-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="03da5-136">افتح صفحة **جميع كشوف الأرباح‬**، ثم انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="03da5-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="03da5-137">إدخل التالي:</span><span class="sxs-lookup"><span data-stu-id="03da5-137">Enter the following:</span></span> 

| <span data-ttu-id="03da5-138">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-138">Field</span></span>      | <span data-ttu-id="03da5-139">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="03da5-140">العامل</span><span class="sxs-lookup"><span data-stu-id="03da5-140">Worker</span></span>     | <span data-ttu-id="03da5-141">مايكل ريدموند</span><span class="sxs-lookup"><span data-stu-id="03da5-141">Michael Redmond</span></span>       |
| <span data-ttu-id="03da5-142">دورة الدفع</span><span class="sxs-lookup"><span data-stu-id="03da5-142">Pay cycle</span></span>  | <span data-ttu-id="03da5-143">sm</span><span class="sxs-lookup"><span data-stu-id="03da5-143">sm</span></span>                    |
| <span data-ttu-id="03da5-144">فترة الدفع</span><span class="sxs-lookup"><span data-stu-id="03da5-144">Pay period</span></span> | <span data-ttu-id="03da5-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="03da5-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="03da5-146">على علامة التبويب **بند كشف الأرباح**، أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03da5-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="03da5-147">البند 1: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="03da5-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="03da5-148">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-148">Field</span></span>            | <span data-ttu-id="03da5-149">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="03da5-150">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="03da5-150">Earnings code</span></span>    | <span data-ttu-id="03da5-151">الدفع المنتظم</span><span class="sxs-lookup"><span data-stu-id="03da5-151">Regular pay</span></span> |
| <span data-ttu-id="03da5-152">الكمية</span><span class="sxs-lookup"><span data-stu-id="03da5-152">Quantity</span></span>         | <span data-ttu-id="03da5-153">1.00</span><span class="sxs-lookup"><span data-stu-id="03da5-153">1.00</span></span>        |
| <span data-ttu-id="03da5-154">راج</span><span class="sxs-lookup"><span data-stu-id="03da5-154">Rage</span></span>             | <span data-ttu-id="03da5-155">30.000</span><span class="sxs-lookup"><span data-stu-id="03da5-155">30,000</span></span>      |
| <span data-ttu-id="03da5-156">علامة تبويب تفاصيل البنود‬</span><span class="sxs-lookup"><span data-stu-id="03da5-156">Line details tab</span></span> |             |
| <span data-ttu-id="03da5-157">يدوي</span><span class="sxs-lookup"><span data-stu-id="03da5-157">Manual</span></span>           | <span data-ttu-id="03da5-158">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="03da5-158">(marked)</span></span>    |

<span data-ttu-id="03da5-159">البند 2: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="03da5-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="03da5-160">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-160">Field</span></span>            | <span data-ttu-id="03da5-161">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="03da5-162">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="03da5-162">Earnings code</span></span>    | <span data-ttu-id="03da5-163">مكافأة</span><span class="sxs-lookup"><span data-stu-id="03da5-163">Bonus</span></span>    |
| <span data-ttu-id="03da5-164">الكمية</span><span class="sxs-lookup"><span data-stu-id="03da5-164">Quantity</span></span>         | <span data-ttu-id="03da5-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="03da5-165">1.0000</span></span>   |
| <span data-ttu-id="03da5-166">المعدل</span><span class="sxs-lookup"><span data-stu-id="03da5-166">Rate</span></span>             | <span data-ttu-id="03da5-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="03da5-167">4250.00</span></span>  |
| <span data-ttu-id="03da5-168">علامة تبويب تفاصيل البنود‬</span><span class="sxs-lookup"><span data-stu-id="03da5-168">Line details tab</span></span> |          |
| <span data-ttu-id="03da5-169">يدوي</span><span class="sxs-lookup"><span data-stu-id="03da5-169">Manual</span></span>           | <span data-ttu-id="03da5-170">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="03da5-170">(marked)</span></span> |

<span data-ttu-id="03da5-171">البند 3: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="03da5-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="03da5-172">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-172">Field</span></span>           | <span data-ttu-id="03da5-173">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="03da5-174">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="03da5-174">Earnings code</span></span>   | <span data-ttu-id="03da5-175">العمولة</span><span class="sxs-lookup"><span data-stu-id="03da5-175">Commission</span></span> |
| <span data-ttu-id="03da5-176">الكمية</span><span class="sxs-lookup"><span data-stu-id="03da5-176">Quantity</span></span>        | <span data-ttu-id="03da5-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="03da5-177">1.0000</span></span>     |
| <span data-ttu-id="03da5-178">المعدل</span><span class="sxs-lookup"><span data-stu-id="03da5-178">Rate</span></span>            | <span data-ttu-id="03da5-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="03da5-179">!,299.00</span></span>   |
| <span data-ttu-id="03da5-180">المعدل</span><span class="sxs-lookup"><span data-stu-id="03da5-180">Rate</span></span>            | <span data-ttu-id="03da5-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="03da5-181">1,299.00</span></span>   |
| <span data-ttu-id="03da5-182">علامة تبويب تفاصيل السطر</span><span class="sxs-lookup"><span data-stu-id="03da5-182">Line detail tab</span></span> |            |
| <span data-ttu-id="03da5-183">يدوي</span><span class="sxs-lookup"><span data-stu-id="03da5-183">Manual</span></span>          | <span data-ttu-id="03da5-184">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="03da5-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="03da5-185">يعتبر تعيين شريط التمرير إلى **يدوي** إلى **نعم** في علامة تبويب **تفاصيل السطر** لكل بند في كشف الأرباح عنصرًا أساسيًا لإدخال أرصدة بداية كشف الرواتب لكل عامل.</span><span class="sxs-lookup"><span data-stu-id="03da5-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="03da5-186">في جزء **الإجراء**، انقر فوق **إصدار كشف الأرباح‬** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="03da5-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="03da5-187">في جزء **الإجراء**، فوق جزء **كشف الدفع** لفتح صفحة **إنشاء قوائم الأجور** وتعيين ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03da5-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="03da5-188">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-188">Field</span></span>              | <span data-ttu-id="03da5-189">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="03da5-190">تاريخ الدفع</span><span class="sxs-lookup"><span data-stu-id="03da5-190">Payment date</span></span>       | <span data-ttu-id="03da5-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="03da5-191">6/30/2017</span></span> |
| <span data-ttu-id="03da5-192">نوع تشغيل الدفع</span><span class="sxs-lookup"><span data-stu-id="03da5-192">Payment run type</span></span>   | <span data-ttu-id="03da5-193">يدوي</span><span class="sxs-lookup"><span data-stu-id="03da5-193">Manual</span></span>    |
| <span data-ttu-id="03da5-194">تعطيل المحاسبة</span><span class="sxs-lookup"><span data-stu-id="03da5-194">Disable accounting</span></span> |   <span data-ttu-id="03da5-195">نعم</span><span class="sxs-lookup"><span data-stu-id="03da5-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="03da5-196">يتوفر هذا فقط عندما يتم تشغيل نوع الدفع بشكل يدوي وحيث يريد المستخدم تعطيل المحاسبة في دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="03da5-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="03da5-197">انقر فوق **موافق** وأغلق **سجل المعلومات‬**.</span><span class="sxs-lookup"><span data-stu-id="03da5-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="03da5-198">لماذا يجب تعيين شريط تمرير "تعطيل المحاسبة" إلى "نعم" عند إنشاء قوائم الأجور؟</span><span class="sxs-lookup"><span data-stu-id="03da5-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="03da5-199">يؤدي تعيين شريط التمرير إلى **نعم** إلى منع توزيع البنود في قائمة الأجور إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="03da5-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="03da5-200">تم تحديث مبالغ دفتر الأستاذ العام في وقت سابق عندما تم إدخال أرصدة الحسابات من النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="03da5-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="03da5-201">يسمح لك إدخال أرصدة البداية لكشف الرواتب بإنشاء تقارير تتضمن معلومات من السنوات السابقة، بالإضافة إلى تعريف الحدود لأغراض الفوائد والضرائب.</span><span class="sxs-lookup"><span data-stu-id="03da5-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="03da5-202">ج.</span><span class="sxs-lookup"><span data-stu-id="03da5-202">C.</span></span> <span data-ttu-id="03da5-203">إنشاء قوائم الأجور‬ للموظفين</span><span class="sxs-lookup"><span data-stu-id="03da5-203">Create pay statements for employees</span></span>
<span data-ttu-id="03da5-204">بعد إنشاء قوائم الأجور ذات أرصدة بداية, يجب عليك التحقق من أن قوائم الأجور تعكس بدقة بيانات كشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="03da5-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="03da5-205">يجب عليك تحديث معلومات الميزات والضرائب يدويًا لكي تتطابق مع القيم الموجودة في نظام كشف الرواتب السابق أيضًا.</span><span class="sxs-lookup"><span data-stu-id="03da5-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="03da5-206">بعد أن تتأكد من أن المبالغ من نظام كشف الرواتب السابق تتطابق مع المبالغ الموجودة في قوائم الأجور الحالية، يجب عليك إنجاز قوائم الأجور.</span><span class="sxs-lookup"><span data-stu-id="03da5-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="03da5-207">افتح صفحة **كل قوائم الأجور‬**.</span><span class="sxs-lookup"><span data-stu-id="03da5-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="03da5-208">تمييز قوائم الأجور الأخيرة التم تم إنشاؤها لمايكل ريدموند</span><span class="sxs-lookup"><span data-stu-id="03da5-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="03da5-209">انقر فوق **تحرير** لفتح صفحة **قوائم الأجور**.</span><span class="sxs-lookup"><span data-stu-id="03da5-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="03da5-210">افتح علامة تبويب **خصومات الميزة‬** وأدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03da5-210">Open the **Benefit deductions** tab and enter the following:</span></span>

| <span data-ttu-id="03da5-211">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-211">Field</span></span>                           | <span data-ttu-id="03da5-212">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-212">Value</span></span>            |
|---------------------------------|------------------|
| <span data-ttu-id="03da5-213">الميزة</span><span class="sxs-lookup"><span data-stu-id="03da5-213">Benefit</span></span>                         | <span data-ttu-id="03da5-214">مبلغ الخصم</span><span class="sxs-lookup"><span data-stu-id="03da5-214">Deduction amount</span></span> |
| <span data-ttu-id="03da5-215">401 ألف</span><span class="sxs-lookup"><span data-stu-id="03da5-215">401K</span></span> | <span data-ttu-id="03da5-216">المشاركة</span><span class="sxs-lookup"><span data-stu-id="03da5-216">Participate</span></span>              | <span data-ttu-id="03da5-217">3000.00</span><span class="sxs-lookup"><span data-stu-id="03da5-217">3000.00</span></span>          |
| <span data-ttu-id="03da5-218">الأسنان</span><span class="sxs-lookup"><span data-stu-id="03da5-218">Dental</span></span> | <span data-ttu-id="03da5-219">SubSp</span><span class="sxs-lookup"><span data-stu-id="03da5-219">SubSp</span></span>                  | <span data-ttu-id="03da5-220">495.00</span><span class="sxs-lookup"><span data-stu-id="03da5-220">495.00</span></span>           |
| <span data-ttu-id="03da5-221">إنفاق رعاية المعالين</span><span class="sxs-lookup"><span data-stu-id="03da5-221">Dep care spending</span></span> | <span data-ttu-id="03da5-222">المشاركة</span><span class="sxs-lookup"><span data-stu-id="03da5-222">Participate</span></span> | <span data-ttu-id="03da5-223">2500.00</span><span class="sxs-lookup"><span data-stu-id="03da5-223">2500.00</span></span>          |
| <span data-ttu-id="03da5-224">الرؤية</span><span class="sxs-lookup"><span data-stu-id="03da5-224">Vision</span></span> | <span data-ttu-id="03da5-225">SupSp</span><span class="sxs-lookup"><span data-stu-id="03da5-225">SupSp</span></span>                  | <span data-ttu-id="03da5-226">500.00</span><span class="sxs-lookup"><span data-stu-id="03da5-226">500.00</span></span>           |

5. <span data-ttu-id="03da5-227">في علامة تبويب **مساهمات الميزة‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03da5-227">In the **Benefit contributions** tab and enter the following:</span></span>

| <span data-ttu-id="03da5-228">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-228">Field</span></span>              | <span data-ttu-id="03da5-229">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-229">Value</span></span>               |
|--------------------|---------------------|
| <span data-ttu-id="03da5-230">الميزة</span><span class="sxs-lookup"><span data-stu-id="03da5-230">Benefit</span></span>            | <span data-ttu-id="03da5-231">مبلغ المساهمة</span><span class="sxs-lookup"><span data-stu-id="03da5-231">Contribution amount</span></span> |
| <span data-ttu-id="03da5-232">401 ألف</span><span class="sxs-lookup"><span data-stu-id="03da5-232">401K</span></span> | <span data-ttu-id="03da5-233">المشاركة</span><span class="sxs-lookup"><span data-stu-id="03da5-233">Participate</span></span> | <span data-ttu-id="03da5-234">3000,00</span><span class="sxs-lookup"><span data-stu-id="03da5-234">3000,00</span></span>             |
| <span data-ttu-id="03da5-235">الأسنان</span><span class="sxs-lookup"><span data-stu-id="03da5-235">Dental</span></span> | <span data-ttu-id="03da5-236">SubSp</span><span class="sxs-lookup"><span data-stu-id="03da5-236">SubSp</span></span>     | <span data-ttu-id="03da5-237">495.00</span><span class="sxs-lookup"><span data-stu-id="03da5-237">495.00</span></span>              |
| <span data-ttu-id="03da5-238">الرؤية</span><span class="sxs-lookup"><span data-stu-id="03da5-238">Vision</span></span> | <span data-ttu-id="03da5-239">SubSp</span><span class="sxs-lookup"><span data-stu-id="03da5-239">SubSp</span></span>     | <span data-ttu-id="03da5-240">500.00</span><span class="sxs-lookup"><span data-stu-id="03da5-240">500.00</span></span>              |

6. <span data-ttu-id="03da5-241">في علامة تبويب **خصومات الضريبة‬‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03da5-241">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="03da5-242">الحقل</span><span class="sxs-lookup"><span data-stu-id="03da5-242">Field</span></span>           | <span data-ttu-id="03da5-243">القيمة</span><span class="sxs-lookup"><span data-stu-id="03da5-243">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="03da5-244">‏‫الكود الضريبي‬</span><span class="sxs-lookup"><span data-stu-id="03da5-244">Tax code</span></span>        | <span data-ttu-id="03da5-245">مبلغ الخصم</span><span class="sxs-lookup"><span data-stu-id="03da5-245">Deduction amount</span></span> |
| <span data-ttu-id="03da5-246">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="03da5-246">USA-FED-ER-FICA</span></span> | <span data-ttu-id="03da5-247">1600.00</span><span class="sxs-lookup"><span data-stu-id="03da5-247">1600.00</span></span>          |
| <span data-ttu-id="03da5-248">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="03da5-248">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="03da5-249">825.75</span><span class="sxs-lookup"><span data-stu-id="03da5-249">825.75</span></span>           |

7. <span data-ttu-id="03da5-250">في علامة تبويب **خصومات الضريبة‬‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="03da5-250">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="03da5-251">انقر فوق **حساب**.</span><span class="sxs-lookup"><span data-stu-id="03da5-251">Click **Calculate**.</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="03da5-252">تحقق من صحة إجماليات قوائم الأجور التي تتطابق مع النظام القديم للعامل لهذه السنة حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="03da5-252">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="03da5-253">قد ترغب في تعليق عملية الإنجاز في الخطوة التالية للقيام ببعض عمليات التحقق الشاملة لكل قوائم الأجور في التجميع.</span><span class="sxs-lookup"><span data-stu-id="03da5-253">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="03da5-254">بعد الانتهاء من عملية التحقق، استعرض كافة قوائم الأجور وعمل على إنجازها.</span><span class="sxs-lookup"><span data-stu-id="03da5-254">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="03da5-255">يمكن تنفيذ العملية نفسها بتزايدات ربع سنوية، إذا لزم الأمر، لجميع أرباع السنة السابقة في كل سنة.</span><span class="sxs-lookup"><span data-stu-id="03da5-255">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="03da5-256">يُعد هذا الأمر مطلوبًا فقط إذا كان العميل بحاجة إلى رؤية البيانات حسب ربع السنة من دون العودة إلى النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="03da5-256">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="03da5-257">عند حدوث خطأ أثناء إدخال أرصدة البداية لموظف</span><span class="sxs-lookup"><span data-stu-id="03da5-257">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="03da5-258">من الممكن عكس الحركات وإعادة إدخالها.</span><span class="sxs-lookup"><span data-stu-id="03da5-258">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="03da5-259">لعكس الحركة، ما عليك سوى إكمال الخطوات التالية في صفحة **كل قوائم الأجور‬**.</span><span class="sxs-lookup"><span data-stu-id="03da5-259">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="03da5-260">انقر فوق **عكس**.</span><span class="sxs-lookup"><span data-stu-id="03da5-260">Click **Reverse**.</span></span>

2. <span data-ttu-id="03da5-261">انقر فوق **نعم** عند ظهور الرسالة "عندما تقوم بعكس قائمة الأجور هذه، سيتم إنشاء قائمة أجور معكوسة لمقاصة قائمة الأجور هذه.</span><span class="sxs-lookup"><span data-stu-id="03da5-261">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="03da5-262">لا يمكن تحرير أي قائمة أجور منهما.</span><span class="sxs-lookup"><span data-stu-id="03da5-262">Neither pay statement can be edited.</span></span> <span data-ttu-id="03da5-263">هل تريد عكس قائمة الأجور هذه؟"</span><span class="sxs-lookup"><span data-stu-id="03da5-263">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="03da5-264">.</span><span class="sxs-lookup"><span data-stu-id="03da5-264">displays.</span></span> 

<span data-ttu-id="03da5-265">بعد قيامك بعكس قائمة الأجور، يمكنك إنشاء كشف حساب دفع جديد للعامل من كشف الأرباح الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="03da5-265">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="03da5-266">يجب عليك إصلاح أية بنود غير صحيحة في كشف الأرباح قبل إنشاء قائمة أجور جديدة، ثم إنشاء قوائم أجور جديدة بالمبالغ الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="03da5-266">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

