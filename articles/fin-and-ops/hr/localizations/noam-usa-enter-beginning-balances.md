---
title: إدخال أرصدة البداية لكشف الرواتب
description: يصف الموضوع الخطوات الخاصة بإدخال أرصدة البداية لأكواد الأرباح‬ والخصومات والمزايا والضرائب. تعتبر هذه المعلومات قيّمة بالنسبة إلى الشركاء الذين يريدون ترحيل البيانات الخاصة بتطبيق كشف رواتب‬ جديد أو نقلها من نظام آخر.
author: kherr75
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4bb8f565f5bf5630a7c5f8602b96e569692bc7c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507974"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="bdf73-104">إدخال أرصدة البداية لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="bdf73-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdf73-105">يصف الموضوع الخطوات الخاصة بإدخال أرصدة البداية لأكواد الأرباح‬ والخصومات والمزايا والضرائب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="bdf73-106">تعتبر هذه المعلومات قيمة بالنسبة إلى الشركاء الذين ينقلون البيانات الخاصة بتطبيق كشف رواتب‬ جديد من نظام آخر.</span><span class="sxs-lookup"><span data-stu-id="bdf73-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="bdf73-107">استعدادًا لإدخال أرصدة البداية لكشف الرواتب، نتحقق من صحة المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="bdf73-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="bdf73-108">تم إدخال سجلات الموظفين وهي متاحة في النظام</span><span class="sxs-lookup"><span data-stu-id="bdf73-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="bdf73-109">تم إعداد البيانات التالية وتعيينها للموظفين:</span><span class="sxs-lookup"><span data-stu-id="bdf73-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="bdf73-110">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="bdf73-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="bdf73-111">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="bdf73-111">Earning codes</span></span>
    - <span data-ttu-id="bdf73-112">الضرائب</span><span class="sxs-lookup"><span data-stu-id="bdf73-112">Taxes</span></span>
    - <span data-ttu-id="bdf73-113">الميزات والخصومات</span><span class="sxs-lookup"><span data-stu-id="bdf73-113">Benefits and deductions</span></span>

- <span data-ttu-id="bdf73-114">يجب على الشركة اختيار تاريخ حيث يمكن تعيين أرصدة البداية لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="bdf73-115">تم تجميع معلومات حول كافة الأرباح والميزات/الخصومات، ومساهمات الميزات، وضرائب الموظفين وضرائب أصحاب العمل والمبالغ حتى تاريخه من النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="bdf73-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="bdf73-116">بينما تخطط لإدخال أرصدة البداية، يجب أن تأخذ في الاعتبار إلى أي مدى يجب أن تكون البيانات مفصلة.</span><span class="sxs-lookup"><span data-stu-id="bdf73-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="bdf73-117">يقوم معظم الشركات بإدخال مبلغ واحد مدمج للسنة حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="bdf73-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="bdf73-118">ومع ذلك، إذا كانت هناك حاجة إلى مزيد من المعلومات التفصيلية، فيمكن إدخال الأرصدة بتزايدات ربع سنوية.</span><span class="sxs-lookup"><span data-stu-id="bdf73-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="bdf73-119">من خلال تقرير مستوى التفصيل المطلوب يتحدد عدد قوائم الأجور‬ اليدوية التي يجب إنشاؤها لكل العامل.</span><span class="sxs-lookup"><span data-stu-id="bdf73-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="bdf73-120">لمدة سنة واحدة حتى تاريخه، هناك حاجة إلى كشف حساب يدوي واحد فقط لكل موظف.</span><span class="sxs-lookup"><span data-stu-id="bdf73-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="bdf73-121">للقيام بذلك، استخدم مبالغ السنة حتى تاريخه من قوائم الأجور النهائية من النظام السابق كالمبلغ الذي تم إدخاله في نظام كشف الرواتب الجديد.</span><span class="sxs-lookup"><span data-stu-id="bdf73-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="bdf73-122">يوضح المثال التالي كيفية إدخال أرصدة البداية لكشف رواتب الموظف، بما في ذلك أكواد الأرباح‬ والميزات/الخصومات والضرائب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="bdf73-123">في مثال واقعي، سيتوفر لديك بند لكل كود ربح وخصم الميزة ومساهمة الميزة وضريبة الموظف وضريبة رب العمل مع المبلغ الذي تم إدخاله للسنة حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="bdf73-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="bdf73-124">باستخدام قائمة الأكواد والمبالغ هذه، اتبع الخطوات لإنشاء كشف يدوي للأرباح وقوائم الأجور مع تعطيل المحاسبة لنقل الأرصدة الافتتاحية لأغراض تتعلق بالرواتب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="bdf73-125">ستقوم بتعطيل المحاسبة لأنك لا ترغب في ترحيل قوائم الأجور لرصيد البداية إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="bdf73-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="bdf73-126">كان ذلك يتم في النظام القديم وسينتقل إلى النظام الجديد عند تعيين أرصدة البداية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="bdf73-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="bdf73-127">أ.</span><span class="sxs-lookup"><span data-stu-id="bdf73-127">A.</span></span> <span data-ttu-id="bdf73-128">كيفية إعداد أكواد الإيرادات لاستخدامه على أرصدة البداية لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="bdf73-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="bdf73-129">عندما تقوم بإدخال أرصدة البداية لكشف الرواتب، تأكد من تكوين أكواد الأرباح التي ستستخدمها مع تمكين خيار "السماح بتحرير أسعار كشف الأرباح‬".</span><span class="sxs-lookup"><span data-stu-id="bdf73-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="bdf73-130">سيسمح لك ذلك بإدخال المبلغ من النظام القديم يدويًا.</span><span class="sxs-lookup"><span data-stu-id="bdf73-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="bdf73-131">ب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-131">B.</span></span> <span data-ttu-id="bdf73-132">إنشاء كشف أرباح لأحد الموظفين للحصول على رصيد البداية</span><span class="sxs-lookup"><span data-stu-id="bdf73-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="bdf73-133">تنشئ هذه الخطوة يدويًا كشف أرباح لكل عامل لفترة الدفع‬ الأخيرة من النظام القديم، مما يؤدي إلى إنشاء بنود كشف الأرباح‬ في نظام كشف الرواتب الجديد.</span><span class="sxs-lookup"><span data-stu-id="bdf73-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="bdf73-134">أدخل بندًا واحدًا لكل كود أرباح‬ ومبلغ السنة والساعات حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="bdf73-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="bdf73-135">الخطوات النموذجية هي على الشكل التالي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="bdf73-136">افتح صفحة **جميع كشوف الأرباح‬**، ثم انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="bdf73-137">إدخل التالي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-137">Enter the following:</span></span> 

    | <span data-ttu-id="bdf73-138">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-138">Field</span></span>      | <span data-ttu-id="bdf73-139">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="bdf73-140">العامل</span><span class="sxs-lookup"><span data-stu-id="bdf73-140">Worker</span></span>     | <span data-ttu-id="bdf73-141">مايكل ريدموند</span><span class="sxs-lookup"><span data-stu-id="bdf73-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="bdf73-142">دورة الدفع</span><span class="sxs-lookup"><span data-stu-id="bdf73-142">Pay cycle</span></span>  | <span data-ttu-id="bdf73-143">sm</span><span class="sxs-lookup"><span data-stu-id="bdf73-143">sm</span></span>                    |
    | <span data-ttu-id="bdf73-144">فترة الدفع</span><span class="sxs-lookup"><span data-stu-id="bdf73-144">Pay period</span></span> | <span data-ttu-id="bdf73-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="bdf73-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="bdf73-146">على علامة التبويب **بند كشف الأرباح**، أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="bdf73-147">البند 1: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="bdf73-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="bdf73-148">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-148">Field</span></span>            | <span data-ttu-id="bdf73-149">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="bdf73-150">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="bdf73-150">Earnings code</span></span>    | <span data-ttu-id="bdf73-151">الدفع المنتظم</span><span class="sxs-lookup"><span data-stu-id="bdf73-151">Regular pay</span></span> |
    | <span data-ttu-id="bdf73-152">الكمية</span><span class="sxs-lookup"><span data-stu-id="bdf73-152">Quantity</span></span>         | <span data-ttu-id="bdf73-153">1.00</span><span class="sxs-lookup"><span data-stu-id="bdf73-153">1.00</span></span>        |
    | <span data-ttu-id="bdf73-154">المعدل</span><span class="sxs-lookup"><span data-stu-id="bdf73-154">Rate</span></span>             | <span data-ttu-id="bdf73-155">30,000</span><span class="sxs-lookup"><span data-stu-id="bdf73-155">30,000</span></span>      |
    | <span data-ttu-id="bdf73-156">علامة تبويب تفاصيل البنود‬</span><span class="sxs-lookup"><span data-stu-id="bdf73-156">Line details tab</span></span> |             |
    | <span data-ttu-id="bdf73-157">يدوي</span><span class="sxs-lookup"><span data-stu-id="bdf73-157">Manual</span></span>           | <span data-ttu-id="bdf73-158">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="bdf73-158">(marked)</span></span>    |

    <span data-ttu-id="bdf73-159">البند 2: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="bdf73-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="bdf73-160">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-160">Field</span></span>            | <span data-ttu-id="bdf73-161">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="bdf73-162">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="bdf73-162">Earnings code</span></span>    | <span data-ttu-id="bdf73-163">مكافأة</span><span class="sxs-lookup"><span data-stu-id="bdf73-163">Bonus</span></span>    |
    | <span data-ttu-id="bdf73-164">الكمية</span><span class="sxs-lookup"><span data-stu-id="bdf73-164">Quantity</span></span>         | <span data-ttu-id="bdf73-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="bdf73-165">1.0000</span></span>   |
    | <span data-ttu-id="bdf73-166">المعدل</span><span class="sxs-lookup"><span data-stu-id="bdf73-166">Rate</span></span>             | <span data-ttu-id="bdf73-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="bdf73-167">4250.00</span></span>  |
    | <span data-ttu-id="bdf73-168">علامة تبويب تفاصيل البنود‬</span><span class="sxs-lookup"><span data-stu-id="bdf73-168">Line details tab</span></span> |          |
    | <span data-ttu-id="bdf73-169">يدوي</span><span class="sxs-lookup"><span data-stu-id="bdf73-169">Manual</span></span>           | <span data-ttu-id="bdf73-170">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="bdf73-170">(marked)</span></span> |

    <span data-ttu-id="bdf73-171">البند 3: علامة التبويب **بند كشف الأرباح**</span><span class="sxs-lookup"><span data-stu-id="bdf73-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="bdf73-172">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-172">Field</span></span>           | <span data-ttu-id="bdf73-173">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="bdf73-174">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="bdf73-174">Earnings code</span></span>   | <span data-ttu-id="bdf73-175">العمولة</span><span class="sxs-lookup"><span data-stu-id="bdf73-175">Commission</span></span> |
    | <span data-ttu-id="bdf73-176">الكمية</span><span class="sxs-lookup"><span data-stu-id="bdf73-176">Quantity</span></span>        | <span data-ttu-id="bdf73-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="bdf73-177">1.0000</span></span>     |
    | <span data-ttu-id="bdf73-178">المعدل</span><span class="sxs-lookup"><span data-stu-id="bdf73-178">Rate</span></span>            | <span data-ttu-id="bdf73-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="bdf73-179">!,299.00</span></span>   |
    | <span data-ttu-id="bdf73-180">المعدل</span><span class="sxs-lookup"><span data-stu-id="bdf73-180">Rate</span></span>            | <span data-ttu-id="bdf73-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="bdf73-181">1,299.00</span></span>   |
    | <span data-ttu-id="bdf73-182">علامة تبويب تفاصيل السطر</span><span class="sxs-lookup"><span data-stu-id="bdf73-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="bdf73-183">يدوي</span><span class="sxs-lookup"><span data-stu-id="bdf73-183">Manual</span></span>          | <span data-ttu-id="bdf73-184">(تم تعليمه)</span><span class="sxs-lookup"><span data-stu-id="bdf73-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="bdf73-185">يعتبر تعيين شريط التمرير إلى **يدوي** إلى **نعم** في علامة تبويب **تفاصيل السطر** لكل بند في كشف الأرباح عنصرًا أساسيًا لإدخال أرصدة بداية كشف الرواتب لكل عامل.</span><span class="sxs-lookup"><span data-stu-id="bdf73-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="bdf73-186">في جزء **الإجراء**، انقر فوق **إصدار كشف الأرباح‬** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="bdf73-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="bdf73-187">في جزء **الإجراء**، فوق جزء **كشف الدفع** لفتح صفحة **إنشاء قوائم الأجور** وتعيين ما يلي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="bdf73-188">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-188">Field</span></span>              | <span data-ttu-id="bdf73-189">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="bdf73-190">تاريخ الدفع</span><span class="sxs-lookup"><span data-stu-id="bdf73-190">Payment date</span></span>       | <span data-ttu-id="bdf73-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="bdf73-191">6/30/2017</span></span> |
    | <span data-ttu-id="bdf73-192">نوع تشغيل الدفع</span><span class="sxs-lookup"><span data-stu-id="bdf73-192">Payment run type</span></span>   | <span data-ttu-id="bdf73-193">يدوي</span><span class="sxs-lookup"><span data-stu-id="bdf73-193">Manual</span></span>    |
    | <span data-ttu-id="bdf73-194">تعطيل المحاسبة</span><span class="sxs-lookup"><span data-stu-id="bdf73-194">Disable accounting</span></span> |   <span data-ttu-id="bdf73-195">نعم</span><span class="sxs-lookup"><span data-stu-id="bdf73-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="bdf73-196">يتوفر هذا فقط عندما يتم تشغيل نوع الدفع بشكل يدوي وحيث يريد المستخدم تعطيل المحاسبة في دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="bdf73-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="bdf73-197">انقر فوق **موافق** وأغلق **سجل المعلومات‬**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="bdf73-198">لماذا يجب تعيين شريط تمرير "تعطيل المحاسبة" إلى "نعم" عند إنشاء قوائم الأجور؟</span><span class="sxs-lookup"><span data-stu-id="bdf73-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="bdf73-199">يؤدي تعيين شريط التمرير إلى **نعم** إلى منع توزيع البنود في قائمة الأجور إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="bdf73-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="bdf73-200">تم تحديث مبالغ دفتر الأستاذ العام في وقت سابق عندما تم إدخال أرصدة الحسابات من النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="bdf73-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="bdf73-201">يسمح لك إدخال أرصدة البداية لكشف الرواتب بإنشاء تقارير تتضمن معلومات من السنوات السابقة، بالإضافة إلى تعريف الحدود لأغراض الفوائد والضرائب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="bdf73-202">ج.</span><span class="sxs-lookup"><span data-stu-id="bdf73-202">C.</span></span> <span data-ttu-id="bdf73-203">إنشاء قوائم الأجور‬ للموظفين</span><span class="sxs-lookup"><span data-stu-id="bdf73-203">Create pay statements for employees</span></span>

<span data-ttu-id="bdf73-204">بعد إنشاء قوائم الأجور ذات أرصدة بداية, يجب عليك التحقق من أن قوائم الأجور تعكس بدقة بيانات كشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="bdf73-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="bdf73-205">يجب عليك تحديث معلومات الميزات والضرائب يدويًا لكي تتطابق مع القيم الموجودة في نظام كشف الرواتب السابق أيضًا.</span><span class="sxs-lookup"><span data-stu-id="bdf73-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="bdf73-206">بعد أن تتأكد من أن المبالغ من نظام كشف الرواتب السابق تتطابق مع المبالغ الموجودة في قوائم الأجور الحالية، يجب عليك إنجاز قوائم الأجور.</span><span class="sxs-lookup"><span data-stu-id="bdf73-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="bdf73-207">افتح صفحة **كل قوائم الأجور‬**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="bdf73-208">تمييز قوائم الأجور الأخيرة التم تم إنشاؤها لمايكل ريدموند</span><span class="sxs-lookup"><span data-stu-id="bdf73-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="bdf73-209">انقر فوق **تحرير** لفتح صفحة **قوائم الأجور**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="bdf73-210">افتح علامة تبويب **خصومات الميزة‬** وأدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="bdf73-211">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-211">Field</span></span>             | <span data-ttu-id="bdf73-212">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="bdf73-213">الميزة</span><span class="sxs-lookup"><span data-stu-id="bdf73-213">Benefit</span></span>           | <span data-ttu-id="bdf73-214">مبلغ الخصم</span><span class="sxs-lookup"><span data-stu-id="bdf73-214">Deduction amount</span></span> |
    | <span data-ttu-id="bdf73-215">401 ألف</span><span class="sxs-lookup"><span data-stu-id="bdf73-215">401K</span></span>              | <span data-ttu-id="bdf73-216">المشاركة</span><span class="sxs-lookup"><span data-stu-id="bdf73-216">Participate</span></span>      |
    | <span data-ttu-id="bdf73-217">الأسنان</span><span class="sxs-lookup"><span data-stu-id="bdf73-217">Dental</span></span>            | <span data-ttu-id="bdf73-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="bdf73-218">SubSp</span></span>            |
    | <span data-ttu-id="bdf73-219">إنفاق رعاية المعالين</span><span class="sxs-lookup"><span data-stu-id="bdf73-219">Dep care spending</span></span> | <span data-ttu-id="bdf73-220">المشاركة</span><span class="sxs-lookup"><span data-stu-id="bdf73-220">Participate</span></span>      |
    | <span data-ttu-id="bdf73-221">الرؤية</span><span class="sxs-lookup"><span data-stu-id="bdf73-221">Vision</span></span>            | <span data-ttu-id="bdf73-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="bdf73-222">SupSp</span></span>            |

5. <span data-ttu-id="bdf73-223">في علامة تبويب **مساهمات الميزة‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="bdf73-224">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-224">Field</span></span>   | <span data-ttu-id="bdf73-225">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="bdf73-226">الميزة</span><span class="sxs-lookup"><span data-stu-id="bdf73-226">Benefit</span></span> | <span data-ttu-id="bdf73-227">مبلغ المساهمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-227">Contribution amount</span></span> |
    | <span data-ttu-id="bdf73-228">401 ألف</span><span class="sxs-lookup"><span data-stu-id="bdf73-228">401K</span></span>    | <span data-ttu-id="bdf73-229">المشاركة</span><span class="sxs-lookup"><span data-stu-id="bdf73-229">Participate</span></span>         |
    | <span data-ttu-id="bdf73-230">الأسنان</span><span class="sxs-lookup"><span data-stu-id="bdf73-230">Dental</span></span>  | <span data-ttu-id="bdf73-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="bdf73-231">SubSp</span></span>               |
    | <span data-ttu-id="bdf73-232">الرؤية</span><span class="sxs-lookup"><span data-stu-id="bdf73-232">Vision</span></span>  | <span data-ttu-id="bdf73-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="bdf73-233">SubSp</span></span>               |

6. <span data-ttu-id="bdf73-234">في علامة تبويب **خصومات الضريبة‬‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="bdf73-235">الحقل</span><span class="sxs-lookup"><span data-stu-id="bdf73-235">Field</span></span>           | <span data-ttu-id="bdf73-236">القيمة</span><span class="sxs-lookup"><span data-stu-id="bdf73-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="bdf73-237">‏‫الكود الضريبي‬</span><span class="sxs-lookup"><span data-stu-id="bdf73-237">Tax code</span></span>        | <span data-ttu-id="bdf73-238">مبلغ الخصم</span><span class="sxs-lookup"><span data-stu-id="bdf73-238">Deduction amount</span></span> |
    | <span data-ttu-id="bdf73-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="bdf73-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="bdf73-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="bdf73-240">1600.00</span></span>          |
    | <span data-ttu-id="bdf73-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="bdf73-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="bdf73-242">825.75</span><span class="sxs-lookup"><span data-stu-id="bdf73-242">825.75</span></span>           |

7. <span data-ttu-id="bdf73-243">في علامة تبويب **خصومات الضريبة‬‬** أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="bdf73-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="bdf73-244">انقر فوق **حساب**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="bdf73-245">تحقق من صحة إجماليات قوائم الأجور التي تتطابق مع النظام القديم للعامل لهذه السنة حتى تاريخه.</span><span class="sxs-lookup"><span data-stu-id="bdf73-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="bdf73-246">قد ترغب في تعليق عملية الإنجاز في الخطوة التالية للقيام ببعض عمليات التحقق الشاملة لكل قوائم الأجور في التجميع.</span><span class="sxs-lookup"><span data-stu-id="bdf73-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="bdf73-247">بعد الانتهاء من عملية التحقق، استعرض كافة قوائم الأجور وعمل على إنجازها.</span><span class="sxs-lookup"><span data-stu-id="bdf73-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="bdf73-248">يمكن تنفيذ العملية نفسها بتزايدات ربع سنوية، إذا لزم الأمر، لجميع أرباع السنة السابقة في كل سنة.</span><span class="sxs-lookup"><span data-stu-id="bdf73-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="bdf73-249">يُعد هذا الأمر مطلوبًا فقط إذا كان العميل بحاجة إلى رؤية البيانات حسب ربع السنة من دون العودة إلى النظام القديم.</span><span class="sxs-lookup"><span data-stu-id="bdf73-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="bdf73-250">عند حدوث خطأ أثناء إدخال أرصدة البداية لموظف</span><span class="sxs-lookup"><span data-stu-id="bdf73-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="bdf73-251">من الممكن عكس الحركات وإعادة إدخالها.</span><span class="sxs-lookup"><span data-stu-id="bdf73-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="bdf73-252">لعكس الحركة، ما عليك سوى إكمال الخطوات التالية في صفحة **كل قوائم الأجور‬**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="bdf73-253">انقر فوق **عكس**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="bdf73-254">انقر فوق **نعم** عند ظهور الرسالة "عندما تقوم بعكس قائمة الأجور هذه، سيتم إنشاء قائمة أجور معكوسة لمقاصة قائمة الأجور هذه.</span><span class="sxs-lookup"><span data-stu-id="bdf73-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="bdf73-255">لا يمكن تحرير أي قائمة أجور منهما.</span><span class="sxs-lookup"><span data-stu-id="bdf73-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="bdf73-256">هل تريد عكس قائمة الأجور هذه؟"</span><span class="sxs-lookup"><span data-stu-id="bdf73-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="bdf73-257">.</span><span class="sxs-lookup"><span data-stu-id="bdf73-257">displays.</span></span> 

<span data-ttu-id="bdf73-258">بعد قيامك بعكس قائمة الأجور، يمكنك إنشاء كشف حساب دفع جديد للعامل من كشف الأرباح الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="bdf73-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="bdf73-259">يجب عليك إصلاح أية بنود غير صحيحة في كشف الأرباح قبل إنشاء قائمة أجور جديدة، ثم إنشاء قوائم أجور جديدة بالمبالغ الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="bdf73-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
