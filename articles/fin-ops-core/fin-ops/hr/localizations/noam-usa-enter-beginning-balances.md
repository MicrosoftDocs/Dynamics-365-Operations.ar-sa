---
title: إدخال أرصدة البداية لكشف الرواتب
description: يصف الموضوع الخطوات الخاصة بإدخال أرصدة البداية لأكواد الأرباح‬ والخصومات والمزايا والضرائب.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752140"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="05246-103">إدخال أرصدة البداية لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="05246-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05246-104">يصف الموضوع الخطوات الخاصة بإدخال أرصدة البداية لأكواد الأرباح‬ والخصومات والمزايا والضرائب.</span><span class="sxs-lookup"><span data-stu-id="05246-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="05246-105">تعتبر هذه المعلومات قيمة بالنسبة إلى الشركاء الذين ينقلون البيانات الخاصة بتطبيق كشف رواتب‬ جديد من نظام آخر.</span><span class="sxs-lookup"><span data-stu-id="05246-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="05246-106">استعدادًا لإدخال أرصدة البداية لكشف الرواتب، نتحقق من صحة المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="05246-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="05246-107">تم إدخال سجلات الموظفين وهي متاحة في النظام</span><span class="sxs-lookup"><span data-stu-id="05246-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="05246-108">تم إعداد البيانات التالية وتعيينها للموظفين:</span><span class="sxs-lookup"><span data-stu-id="05246-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="05246-109">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="05246-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="05246-110">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="05246-110">Earning codes</span></span>
    - <span data-ttu-id="05246-111">الضرائب</span><span class="sxs-lookup"><span data-stu-id="05246-111">Taxes</span></span>
    - <span data-ttu-id="05246-112">الميزات والخصومات</span><span class="sxs-lookup"><span data-stu-id="05246-112">Benefits and deductions</span></span>

- <span data-ttu-id="05246-113">يجب على الشركة اختيار تاريخ حيث يمكن تعيين أرصدة البداية لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="05246-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="05246-114">تم تجميع معلومات حول كافة الأرباح والميزات/الخصومات، ومساهمات الميزات، وضرائب الموظفين وضرائب أصحاب العمل والمبالغ حتى تاريخه من النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="05246-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="05246-115">بينما تخطط لإدخال أرصدة البداية، يجب أن تأخذ في الاعتبار إلى أي مدى يجب أن تكون البيانات مفصلة.</span><span class="sxs-lookup"><span data-stu-id="05246-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="05246-116">يقوم معظم الشركات بإدخال مبلغ واحد مدمج للسنة حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="05246-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="05246-117">ومع ذلك، إذا كانت هناك حاجة إلى مزيد من المعلومات التفصيلية، فيمكن إدخال الأرصدة بتزايدات ربع سنوية.</span><span class="sxs-lookup"><span data-stu-id="05246-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="05246-118">من خلال تقرير مستوى التفصيل المطلوب يتحدد عدد قوائم الأجور‬ اليدوية التي يجب إنشاؤها لكل العامل.</span><span class="sxs-lookup"><span data-stu-id="05246-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="05246-119">لمدة سنة واحدة حتى تاريخه، هناك حاجة إلى كشف حساب يدوي واحد فقط لكل موظف.</span><span class="sxs-lookup"><span data-stu-id="05246-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="05246-120">للقيام بذلك، استخدم مبالغ السنة حتى تاريخه من قوائم الأجور النهائية من النظام السابق كالمبلغ الذي تم إدخاله في نظام كشف الرواتب الجديد.</span><span class="sxs-lookup"><span data-stu-id="05246-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="05246-121">يوضح المثال التالي كيفية إدخال أرصدة البداية لكشف رواتب الموظف، بما في ذلك أكواد الأرباح‬ والميزات/الخصومات والضرائب.</span><span class="sxs-lookup"><span data-stu-id="05246-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="05246-122">في مثال واقعي، سيتوفر لديك بند لكل كود ربح وخصم الميزة ومساهمة الميزة وضريبة الموظف وضريبة رب العمل مع المبلغ الذي تم إدخاله للسنة حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="05246-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="05246-123">باستخدام قائمة الأكواد والمبالغ هذه، اتبع الخطوات لإنشاء كشف يدوي للأرباح وقوائم الأجور مع تعطيل المحاسبة لنقل الأرصدة الافتتاحية لأغراض تتعلق بالرواتب.</span><span class="sxs-lookup"><span data-stu-id="05246-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="05246-124">ستقوم بتعطيل المحاسبة لأنك لا ترغب في ترحيل قوائم الأجور لرصيد البداية إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="05246-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="05246-125">كان ذلك يتم في النظام القديم وسينتقل إلى النظام الجديد عند تعيين أرصدة البداية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="05246-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="05246-126">أ.</span><span class="sxs-lookup"><span data-stu-id="05246-126">A.</span></span> <span data-ttu-id="05246-127">كيفية إعداد أكواد الإيرادات لاستخدامه على أرصدة البداية لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="05246-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="05246-128">عندما تقوم بإدخال أرصدة البداية لكشف الرواتب، تأكد من تكوين أكواد الأرباح التي ستستخدمها مع تمكين خيار "السماح بتحرير أسعار كشف الأرباح‬".</span><span class="sxs-lookup"><span data-stu-id="05246-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="05246-129">سيسمح لك ذلك بإدخال المبلغ من النظام القديم يدويًا.</span><span class="sxs-lookup"><span data-stu-id="05246-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="05246-130">ب.</span><span class="sxs-lookup"><span data-stu-id="05246-130">B.</span></span> <span data-ttu-id="05246-131">إنشاء كشف أرباح لأحد الموظفين للحصول على رصيد البداية</span><span class="sxs-lookup"><span data-stu-id="05246-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="05246-132">تنشئ هذه الخطوة يدويًا كشف أرباح لكل عامل لفترة الدفع‬ الأخيرة من النظام القديم، مما يؤدي إلى إنشاء بنود كشف الأرباح‬ في نظام كشف الرواتب الجديد.</span><span class="sxs-lookup"><span data-stu-id="05246-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="05246-133">أدخل بندًا واحدًا لكل كود أرباح‬ ومبلغ السنة والساعات حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="05246-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="05246-134">الخطوات النموذجية هي على الشكل التالي:</span><span class="sxs-lookup"><span data-stu-id="05246-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="05246-135">افتح صفحة **جميع كشوف الأرباح‬**، ثم انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="05246-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="05246-136">إدخل التالي:</span><span class="sxs-lookup"><span data-stu-id="05246-136">Enter the following:</span></span> 

    | <span data-ttu-id="05246-137">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-137">Field</span></span>      | <span data-ttu-id="05246-138">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="05246-139">العامل</span><span class="sxs-lookup"><span data-stu-id="05246-139">Worker</span></span>     | <span data-ttu-id="05246-140">مايكل ريدموند</span><span class="sxs-lookup"><span data-stu-id="05246-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="05246-141">دورة الدفع</span><span class="sxs-lookup"><span data-stu-id="05246-141">Pay cycle</span></span>  | <span data-ttu-id="05246-142">sm</span><span class="sxs-lookup"><span data-stu-id="05246-142">sm</span></span>                    |
    | <span data-ttu-id="05246-143">فترة الدفع</span><span class="sxs-lookup"><span data-stu-id="05246-143">Pay period</span></span> | <span data-ttu-id="05246-144">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="05246-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="05246-145">على علامة التبويب **بند كشف الأرباح**، أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="05246-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="05246-146">البند 1: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="05246-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="05246-147">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-147">Field</span></span>            | <span data-ttu-id="05246-148">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="05246-149">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="05246-149">Earnings code</span></span>    | <span data-ttu-id="05246-150">الدفع المنتظم</span><span class="sxs-lookup"><span data-stu-id="05246-150">Regular pay</span></span> |
    | <span data-ttu-id="05246-151">الكمية</span><span class="sxs-lookup"><span data-stu-id="05246-151">Quantity</span></span>         | <span data-ttu-id="05246-152">1.00</span><span class="sxs-lookup"><span data-stu-id="05246-152">1.00</span></span>        |
    | <span data-ttu-id="05246-153">المعدل</span><span class="sxs-lookup"><span data-stu-id="05246-153">Rate</span></span>             | <span data-ttu-id="05246-154">30,000</span><span class="sxs-lookup"><span data-stu-id="05246-154">30,000</span></span>      |
    | <span data-ttu-id="05246-155">علامة تبويب تفاصيل البنود‬</span><span class="sxs-lookup"><span data-stu-id="05246-155">Line details tab</span></span> |             |
    | <span data-ttu-id="05246-156">يدوي</span><span class="sxs-lookup"><span data-stu-id="05246-156">Manual</span></span>           | <span data-ttu-id="05246-157">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="05246-157">(marked)</span></span>    |

    <span data-ttu-id="05246-158">البند 2: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="05246-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="05246-159">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-159">Field</span></span>            | <span data-ttu-id="05246-160">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="05246-161">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="05246-161">Earnings code</span></span>    | <span data-ttu-id="05246-162">مكافأة</span><span class="sxs-lookup"><span data-stu-id="05246-162">Bonus</span></span>    |
    | <span data-ttu-id="05246-163">الكمية</span><span class="sxs-lookup"><span data-stu-id="05246-163">Quantity</span></span>         | <span data-ttu-id="05246-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="05246-164">1.0000</span></span>   |
    | <span data-ttu-id="05246-165">المعدل</span><span class="sxs-lookup"><span data-stu-id="05246-165">Rate</span></span>             | <span data-ttu-id="05246-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="05246-166">4250.00</span></span>  |
    | <span data-ttu-id="05246-167">علامة تبويب تفاصيل البنود‬</span><span class="sxs-lookup"><span data-stu-id="05246-167">Line details tab</span></span> |          |
    | <span data-ttu-id="05246-168">يدوي</span><span class="sxs-lookup"><span data-stu-id="05246-168">Manual</span></span>           | <span data-ttu-id="05246-169">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="05246-169">(marked)</span></span> |

    <span data-ttu-id="05246-170">البند 3: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="05246-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="05246-171">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-171">Field</span></span>           | <span data-ttu-id="05246-172">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="05246-173">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="05246-173">Earnings code</span></span>   | <span data-ttu-id="05246-174">العمولة</span><span class="sxs-lookup"><span data-stu-id="05246-174">Commission</span></span> |
    | <span data-ttu-id="05246-175">الكمية</span><span class="sxs-lookup"><span data-stu-id="05246-175">Quantity</span></span>        | <span data-ttu-id="05246-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="05246-176">1.0000</span></span>     |
    | <span data-ttu-id="05246-177">المعدل</span><span class="sxs-lookup"><span data-stu-id="05246-177">Rate</span></span>            | <span data-ttu-id="05246-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="05246-178">!,299.00</span></span>   |
    | <span data-ttu-id="05246-179">المعدل</span><span class="sxs-lookup"><span data-stu-id="05246-179">Rate</span></span>            | <span data-ttu-id="05246-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="05246-180">1,299.00</span></span>   |
    | <span data-ttu-id="05246-181">علامة تبويب تفاصيل السطر</span><span class="sxs-lookup"><span data-stu-id="05246-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="05246-182">يدوي</span><span class="sxs-lookup"><span data-stu-id="05246-182">Manual</span></span>          | <span data-ttu-id="05246-183">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="05246-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="05246-184">يعتبر تعيين شريط التمرير إلى **يدوي** إلى **نعم** في علامة تبويب **تفاصيل السطر** لكل بند في كشف الأرباح عنصرًا أساسيًا لإدخال أرصدة بداية كشف الرواتب لكل عامل.</span><span class="sxs-lookup"><span data-stu-id="05246-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="05246-185">في جزء **الإجراء**، انقر فوق **إصدار كشف الأرباح‬** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="05246-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="05246-186">في جزء **الإجراء**، فوق جزء **كشف الدفع** لفتح صفحة **إنشاء قوائم الأجور** وتعيين ما يلي:</span><span class="sxs-lookup"><span data-stu-id="05246-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="05246-187">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-187">Field</span></span>              | <span data-ttu-id="05246-188">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="05246-189">تاريخ الدفع</span><span class="sxs-lookup"><span data-stu-id="05246-189">Payment date</span></span>       | <span data-ttu-id="05246-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="05246-190">6/30/2017</span></span> |
    | <span data-ttu-id="05246-191">نوع تشغيل الدفع</span><span class="sxs-lookup"><span data-stu-id="05246-191">Payment run type</span></span>   | <span data-ttu-id="05246-192">يدوي</span><span class="sxs-lookup"><span data-stu-id="05246-192">Manual</span></span>    |
    | <span data-ttu-id="05246-193">تعطيل المحاسبة</span><span class="sxs-lookup"><span data-stu-id="05246-193">Disable accounting</span></span> |   <span data-ttu-id="05246-194">نعم</span><span class="sxs-lookup"><span data-stu-id="05246-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="05246-195">يتوفر هذا فقط عندما يتم تشغيل نوع الدفع بشكل يدوي وحيث يريد المستخدم تعطيل المحاسبة في دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="05246-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="05246-196">انقر فوق **موافق** وأغلق **سجل المعلومات‬**.</span><span class="sxs-lookup"><span data-stu-id="05246-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="05246-197">لماذا يجب تعيين شريط تمرير "تعطيل المحاسبة" إلى "نعم" عند إنشاء قوائم الأجور؟</span><span class="sxs-lookup"><span data-stu-id="05246-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="05246-198">يؤدي تعيين شريط التمرير إلى **نعم** إلى منع توزيع البنود في قائمة الأجور إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="05246-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="05246-199">تم تحديث مبالغ دفتر الأستاذ العام في وقت سابق عندما تم إدخال أرصدة الحسابات من النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="05246-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="05246-200">يسمح لك إدخال أرصدة البداية لكشف الرواتب بإنشاء تقارير تتضمن معلومات من السنوات السابقة، بالإضافة إلى تعريف الحدود لأغراض الفوائد والضرائب.</span><span class="sxs-lookup"><span data-stu-id="05246-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="05246-201">ج.</span><span class="sxs-lookup"><span data-stu-id="05246-201">C.</span></span> <span data-ttu-id="05246-202">إنشاء قوائم الأجور‬ للموظفين</span><span class="sxs-lookup"><span data-stu-id="05246-202">Create pay statements for employees</span></span>

<span data-ttu-id="05246-203">بعد إنشاء قوائم الأجور ذات أرصدة بداية, يجب عليك التحقق من أن قوائم الأجور تعكس بدقة بيانات كشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="05246-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="05246-204">يجب عليك تحديث معلومات الميزات والضرائب يدويًا لكي تتطابق مع القيم الموجودة في نظام كشف الرواتب السابق أيضًا.</span><span class="sxs-lookup"><span data-stu-id="05246-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="05246-205">بعد أن تتأكد من أن المبالغ من نظام كشف الرواتب السابق تتطابق مع المبالغ الموجودة في قوائم الأجور الحالية، يجب عليك إنجاز قوائم الأجور.</span><span class="sxs-lookup"><span data-stu-id="05246-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="05246-206">افتح صفحة **كل قوائم الأجور‬**.</span><span class="sxs-lookup"><span data-stu-id="05246-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="05246-207">تمييز قوائم الأجور الأخيرة التم تم إنشاؤها لمايكل ريدموند</span><span class="sxs-lookup"><span data-stu-id="05246-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="05246-208">انقر فوق **تحرير** لفتح صفحة **قوائم الأجور**.</span><span class="sxs-lookup"><span data-stu-id="05246-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="05246-209">افتح علامة تبويب **خصومات الميزة‬** وأدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="05246-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="05246-210">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-210">Field</span></span>             | <span data-ttu-id="05246-211">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="05246-212">الميزة</span><span class="sxs-lookup"><span data-stu-id="05246-212">Benefit</span></span>           | <span data-ttu-id="05246-213">مبلغ الخصم</span><span class="sxs-lookup"><span data-stu-id="05246-213">Deduction amount</span></span> |
    | <span data-ttu-id="05246-214">401 ألف</span><span class="sxs-lookup"><span data-stu-id="05246-214">401K</span></span>              | <span data-ttu-id="05246-215">المشاركة</span><span class="sxs-lookup"><span data-stu-id="05246-215">Participate</span></span>      |
    | <span data-ttu-id="05246-216">الأسنان</span><span class="sxs-lookup"><span data-stu-id="05246-216">Dental</span></span>            | <span data-ttu-id="05246-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="05246-217">SubSp</span></span>            |
    | <span data-ttu-id="05246-218">إنفاق رعاية المعالين</span><span class="sxs-lookup"><span data-stu-id="05246-218">Dep care spending</span></span> | <span data-ttu-id="05246-219">المشاركة</span><span class="sxs-lookup"><span data-stu-id="05246-219">Participate</span></span>      |
    | <span data-ttu-id="05246-220">الرؤية</span><span class="sxs-lookup"><span data-stu-id="05246-220">Vision</span></span>            | <span data-ttu-id="05246-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="05246-221">SupSp</span></span>            |

5. <span data-ttu-id="05246-222">في علامة تبويب **مساهمات الميزة‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="05246-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="05246-223">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-223">Field</span></span>   | <span data-ttu-id="05246-224">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="05246-225">الميزة</span><span class="sxs-lookup"><span data-stu-id="05246-225">Benefit</span></span> | <span data-ttu-id="05246-226">مبلغ المساهمة</span><span class="sxs-lookup"><span data-stu-id="05246-226">Contribution amount</span></span> |
    | <span data-ttu-id="05246-227">401 ألف</span><span class="sxs-lookup"><span data-stu-id="05246-227">401K</span></span>    | <span data-ttu-id="05246-228">المشاركة</span><span class="sxs-lookup"><span data-stu-id="05246-228">Participate</span></span>         |
    | <span data-ttu-id="05246-229">الأسنان</span><span class="sxs-lookup"><span data-stu-id="05246-229">Dental</span></span>  | <span data-ttu-id="05246-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="05246-230">SubSp</span></span>               |
    | <span data-ttu-id="05246-231">الرؤية</span><span class="sxs-lookup"><span data-stu-id="05246-231">Vision</span></span>  | <span data-ttu-id="05246-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="05246-232">SubSp</span></span>               |

6. <span data-ttu-id="05246-233">في علامة تبويب **خصومات الضريبة‬‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="05246-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="05246-234">الحقل</span><span class="sxs-lookup"><span data-stu-id="05246-234">Field</span></span>           | <span data-ttu-id="05246-235">القيمة</span><span class="sxs-lookup"><span data-stu-id="05246-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="05246-236">‏‫الكود الضريبي‬</span><span class="sxs-lookup"><span data-stu-id="05246-236">Tax code</span></span>        | <span data-ttu-id="05246-237">مبلغ الخصم</span><span class="sxs-lookup"><span data-stu-id="05246-237">Deduction amount</span></span> |
    | <span data-ttu-id="05246-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="05246-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="05246-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="05246-239">1600.00</span></span>          |
    | <span data-ttu-id="05246-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="05246-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="05246-241">825.75</span><span class="sxs-lookup"><span data-stu-id="05246-241">825.75</span></span>           |

7. <span data-ttu-id="05246-242">في علامة تبويب **خصومات الضريبة‬‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="05246-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="05246-243">انقر فوق **حساب**.</span><span class="sxs-lookup"><span data-stu-id="05246-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="05246-244">تحقق من صحة إجماليات قوائم الأجور التي تتطابق مع النظام القديم للعامل لهذه السنة حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="05246-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="05246-245">قد ترغب في تعليق عملية الإنجاز في الخطوة التالية للقيام ببعض عمليات التحقق الشاملة لكل قوائم الأجور في التجميع.</span><span class="sxs-lookup"><span data-stu-id="05246-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="05246-246">بعد الانتهاء من عملية التحقق، استعرض كافة قوائم الأجور وعمل على إنجازها.</span><span class="sxs-lookup"><span data-stu-id="05246-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="05246-247">يمكن تنفيذ العملية نفسها بتزايدات ربع سنوية، إذا لزم الأمر، لجميع أرباع السنة السابقة في كل سنة.</span><span class="sxs-lookup"><span data-stu-id="05246-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="05246-248">يُعد هذا الأمر مطلوبًا فقط إذا كان العميل بحاجة إلى رؤية البيانات حسب ربع السنة من دون العودة إلى النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="05246-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="05246-249">عند حدوث خطأ أثناء إدخال أرصدة البداية لموظف</span><span class="sxs-lookup"><span data-stu-id="05246-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="05246-250">من الممكن عكس الحركات وإعادة إدخالها.</span><span class="sxs-lookup"><span data-stu-id="05246-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="05246-251">لعكس الحركة، ما عليك سوى إكمال الخطوات التالية في صفحة **كل قوائم الأجور‬**.</span><span class="sxs-lookup"><span data-stu-id="05246-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="05246-252">انقر فوق **عكس**.</span><span class="sxs-lookup"><span data-stu-id="05246-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="05246-253">انقر فوق **نعم** عند ظهور الرسالة "عندما تقوم بعكس قائمة الأجور هذه، سيتم إنشاء قائمة أجور معكوسة لمقاصة قائمة الأجور هذه.</span><span class="sxs-lookup"><span data-stu-id="05246-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="05246-254">لا يمكن تحرير أي قائمة أجور منهما.</span><span class="sxs-lookup"><span data-stu-id="05246-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="05246-255">هل تريد عكس قائمة الأجور هذه؟"</span><span class="sxs-lookup"><span data-stu-id="05246-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="05246-256">.</span><span class="sxs-lookup"><span data-stu-id="05246-256">displays.</span></span> 

<span data-ttu-id="05246-257">بعد قيامك بعكس قائمة الأجور، يمكنك إنشاء كشف حساب دفع جديد للعامل من كشف الأرباح الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="05246-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="05246-258">يجب عليك إصلاح أية بنود غير صحيحة في كشف الأرباح قبل إنشاء قائمة أجور جديدة، ثم إنشاء قوائم أجور جديدة بالمبالغ الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="05246-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]