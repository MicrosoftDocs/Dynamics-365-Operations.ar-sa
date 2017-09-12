---
title: "عملية حساب المصروفات الزائدة"
description: "يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="42894-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="42894-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="42894-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="42894-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="42894-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="42894-105">Term definition</span></span>
---------------

<span data-ttu-id="42894-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="42894-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="42894-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="42894-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="42894-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="42894-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="42894-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="42894-109">Rent</span></span>
-   <span data-ttu-id="42894-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-110">Electricity</span></span>
-   <span data-ttu-id="42894-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="42894-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="42894-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="42894-112">Overhead calculation overview</span></span>
<span data-ttu-id="42894-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="42894-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="42894-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="42894-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="42894-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="42894-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="42894-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="42894-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="42894-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="42894-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="42894-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="42894-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="42894-119">Version type</span></span>
-   <span data-ttu-id="42894-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="42894-120">Date and time</span></span>
-   <span data-ttu-id="42894-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="42894-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="42894-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="42894-122">Fiscal year</span></span>
-   <span data-ttu-id="42894-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="42894-123">Fiscal period</span></span>

<span data-ttu-id="42894-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="42894-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="42894-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="42894-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="42894-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="42894-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="42894-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="42894-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="42894-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="42894-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="42894-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="42894-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="42894-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="42894-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="42894-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="42894-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="42894-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="42894-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="42894-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="42894-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="42894-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="42894-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="42894-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="42894-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="42894-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="42894-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="42894-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="42894-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="42894-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="42894-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="42894-140">Main account</span></span></th>
<th><span data-ttu-id="42894-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="42894-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="42894-143">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-143">CC099</span></span></td>
<td><span data-ttu-id="42894-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-144">Default cost center</span></span></td>
<td><span data-ttu-id="42894-145">10001</span><span class="sxs-lookup"><span data-stu-id="42894-145">10001</span></span></td>
<td><span data-ttu-id="42894-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-146">Electricity</span></span></td>
<td><span data-ttu-id="42894-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="42894-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="42894-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="42894-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="42894-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="42894-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="42894-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-151">Define the cost behavior rule</span></span>

<span data-ttu-id="42894-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="42894-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="42894-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="42894-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="42894-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="42894-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="42894-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="42894-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="42894-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="42894-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="42894-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="42894-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="42894-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="42894-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-160">Journal</span></span></th>
<th><span data-ttu-id="42894-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="42894-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="42894-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="42894-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="42894-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="42894-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-164">00001</span><span class="sxs-lookup"><span data-stu-id="42894-164">00001</span></span></td>
<td><span data-ttu-id="42894-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="42894-166">مالي</span><span class="sxs-lookup"><span data-stu-id="42894-166">Fiscal</span></span></td>
<td><span data-ttu-id="42894-167">2017</span><span class="sxs-lookup"><span data-stu-id="42894-167">2017</span></span></td>
<td><span data-ttu-id="42894-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-168">Period 1</span></span></td>
<td><span data-ttu-id="42894-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="42894-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="42894-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="42894-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-173">Cost element</span></span></th>
<th><span data-ttu-id="42894-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-174">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="42894-177">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-177">CC099</span></span></td>
<td><span data-ttu-id="42894-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-178">Default cost center</span></span></td>
<td><span data-ttu-id="42894-179">10001</span><span class="sxs-lookup"><span data-stu-id="42894-179">10001</span></span></td>
<td><span data-ttu-id="42894-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-180">Electricity</span></span></td>
<td><span data-ttu-id="42894-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="42894-181">Unclassified</span></span></td>
<td><span data-ttu-id="42894-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="42894-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-185">Cost element</span></span></th>
<th><span data-ttu-id="42894-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-186">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-187">Amount</span></span></th>
<th><span data-ttu-id="42894-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-189">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-189">CC099</span></span></td>
<td><span data-ttu-id="42894-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-190">Default cost center</span></span></td>
<td><span data-ttu-id="42894-191">10001</span><span class="sxs-lookup"><span data-stu-id="42894-191">10001</span></span></td>
<td><span data-ttu-id="42894-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-192">Electricity</span></span></td>
<td><span data-ttu-id="42894-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="42894-193">Unclassified</span></span></td>
<td><span data-ttu-id="42894-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-194">10,000.00</span></span></td>
<td><span data-ttu-id="42894-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-196">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-196">CC099</span></span></td>
<td><span data-ttu-id="42894-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-197">Default cost center</span></span></td>
<td><span data-ttu-id="42894-198">10001</span><span class="sxs-lookup"><span data-stu-id="42894-198">10001</span></span></td>
<td><span data-ttu-id="42894-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-199">Electricity</span></span></td>
<td><span data-ttu-id="42894-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="42894-200">Unclassified</span></span></td>
<td><span data-ttu-id="42894-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-201">-10,000.00</span></span></td>
<td><span data-ttu-id="42894-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-203">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-203">CC099</span></span></td>
<td><span data-ttu-id="42894-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-204">Default cost center</span></span></td>
<td><span data-ttu-id="42894-205">10001</span><span class="sxs-lookup"><span data-stu-id="42894-205">10001</span></span></td>
<td><span data-ttu-id="42894-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-206">Electricity</span></span></td>
<td><span data-ttu-id="42894-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-207">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="42894-208">1,000.00</span></span></td>
<td><span data-ttu-id="42894-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-210">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-210">CC099</span></span></td>
<td><span data-ttu-id="42894-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-211">Default cost center</span></span></td>
<td><span data-ttu-id="42894-212">10001</span><span class="sxs-lookup"><span data-stu-id="42894-212">10001</span></span></td>
<td><span data-ttu-id="42894-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-213">Electricity</span></span></td>
<td><span data-ttu-id="42894-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-214">Variable cost</span></span></td>
<td><span data-ttu-id="42894-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-215">9,000.00</span></span></td>
<td><span data-ttu-id="42894-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-217">للحصول على معلومات تفصيلية حول سلوك التكلفة، راجع سياسة سلوك التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="42894-218">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="42894-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="42894-219">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="42894-220">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="42894-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="42894-221">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="42894-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="42894-222">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-222">Define the cost distribution rule</span></span>

<span data-ttu-id="42894-223">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="42894-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="42894-224">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="42894-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="42894-225">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="42894-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="42894-226">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="42894-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="42894-227">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="42894-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="42894-228">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="42894-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-229">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-229">Cost object</span></span></th>
<th><span data-ttu-id="42894-230">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="42894-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-231">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-231">CC001</span></span></td>
<td><span data-ttu-id="42894-232">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-232">HR</span></span></td>
<td><span data-ttu-id="42894-233">1,000</span><span class="sxs-lookup"><span data-stu-id="42894-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-234">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-234">CC002</span></span></td>
<td><span data-ttu-id="42894-235">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-235">Finance</span></span></td>
<td><span data-ttu-id="42894-236">6,000</span><span class="sxs-lookup"><span data-stu-id="42894-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-237">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-237">CC003</span></span></td>
<td><span data-ttu-id="42894-238">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-238">Assembly</span></span></td>
<td><span data-ttu-id="42894-239">0</span><span class="sxs-lookup"><span data-stu-id="42894-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-240">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="42894-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-241">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-241">Cost object</span></span></th>
<th><span data-ttu-id="42894-242">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-242">Magnitude</span></span></th>
<th><span data-ttu-id="42894-243">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-243">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-244">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-245">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-245">CC001</span></span></td>
<td><span data-ttu-id="42894-246">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-246">HR</span></span></td>
<td><span data-ttu-id="42894-247">1,000</span><span class="sxs-lookup"><span data-stu-id="42894-247">1,000</span></span></td>
<td><span data-ttu-id="42894-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="42894-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="42894-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-250">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-250">CC002</span></span></td>
<td><span data-ttu-id="42894-251">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-251">Finance</span></span></td>
<td><span data-ttu-id="42894-252">6,000</span><span class="sxs-lookup"><span data-stu-id="42894-252">6,000</span></span></td>
<td><span data-ttu-id="42894-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="42894-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="42894-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-255">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-255">CC003</span></span></td>
<td><span data-ttu-id="42894-256">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-256">Assembly</span></span></td>
<td><span data-ttu-id="42894-257">0</span><span class="sxs-lookup"><span data-stu-id="42894-257">0</span></span></td>
<td><span data-ttu-id="42894-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="42894-259">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-260">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="42894-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="42894-261">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="42894-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-262">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-262">Cost object</span></span></th>
<th><span data-ttu-id="42894-263">المعادلة</span><span class="sxs-lookup"><span data-stu-id="42894-263">Formula</span></span></th>
<th><span data-ttu-id="42894-264">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-264">Magnitude</span></span></th>
<th><span data-ttu-id="42894-265">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-265">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-266">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-267">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-267">CC001</span></span></td>
<td><span data-ttu-id="42894-268">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-268">HR</span></span></td>
<td><span data-ttu-id="42894-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="42894-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="42894-270">1</span><span class="sxs-lookup"><span data-stu-id="42894-270">1</span></span></td>
<td><span data-ttu-id="42894-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="42894-272">500.00</span><span class="sxs-lookup"><span data-stu-id="42894-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-273">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-273">CC002</span></span></td>
<td><span data-ttu-id="42894-274">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-274">Finance</span></span></td>
<td><span data-ttu-id="42894-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="42894-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="42894-276">1</span><span class="sxs-lookup"><span data-stu-id="42894-276">1</span></span></td>
<td><span data-ttu-id="42894-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="42894-278">500.00</span><span class="sxs-lookup"><span data-stu-id="42894-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-279">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-279">CC003</span></span></td>
<td><span data-ttu-id="42894-280">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-280">Assembly</span></span></td>
<td><span data-ttu-id="42894-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="42894-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="42894-282">0</span><span class="sxs-lookup"><span data-stu-id="42894-282">0</span></span></td>
<td><span data-ttu-id="42894-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="42894-284">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="42894-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-286">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-286">Journal</span></span></th>
<th><span data-ttu-id="42894-287">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="42894-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="42894-288">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="42894-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="42894-289">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="42894-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-290">00002</span><span class="sxs-lookup"><span data-stu-id="42894-290">00002</span></span></td>
<td><span data-ttu-id="42894-291">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="42894-292">مالي</span><span class="sxs-lookup"><span data-stu-id="42894-292">Fiscal</span></span></td>
<td><span data-ttu-id="42894-293">2017</span><span class="sxs-lookup"><span data-stu-id="42894-293">2017</span></span></td>
<td><span data-ttu-id="42894-294">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-294">Period 1</span></span></td>
<td><span data-ttu-id="42894-295">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="42894-296">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="42894-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-297">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="42894-298">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-299">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-299">Cost element</span></span></th>
<th><span data-ttu-id="42894-300">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-300">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-301">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-302">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-303">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-303">CC099</span></span></td>
<td><span data-ttu-id="42894-304">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-304">Default cost center</span></span></td>
<td><span data-ttu-id="42894-305">10001</span><span class="sxs-lookup"><span data-stu-id="42894-305">10001</span></span></td>
<td><span data-ttu-id="42894-306">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-306">Electricity</span></span></td>
<td><span data-ttu-id="42894-307">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-307">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-308">1000.00</span><span class="sxs-lookup"><span data-stu-id="42894-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-309">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-310">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-310">CC099</span></span></td>
<td><span data-ttu-id="42894-311">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-311">Default cost center</span></span></td>
<td><span data-ttu-id="42894-312">10001</span><span class="sxs-lookup"><span data-stu-id="42894-312">10001</span></span></td>
<td><span data-ttu-id="42894-313">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-313">Electricity</span></span></td>
<td><span data-ttu-id="42894-314">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-314">Variable cost</span></span></td>
<td><span data-ttu-id="42894-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="42894-316">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-317">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-318">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-318">Cost element</span></span></th>
<th><span data-ttu-id="42894-319">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-319">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-320">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-320">Amount</span></span></th>
<th><span data-ttu-id="42894-321">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-322">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-322">CC099</span></span></td>
<td><span data-ttu-id="42894-323">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-323">Default cost center</span></span></td>
<td><span data-ttu-id="42894-324">10001</span><span class="sxs-lookup"><span data-stu-id="42894-324">10001</span></span></td>
<td><span data-ttu-id="42894-325">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-325">Electricity</span></span></td>
<td><span data-ttu-id="42894-326">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-326">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-327">-1000.00</span><span class="sxs-lookup"><span data-stu-id="42894-327">-1,000.00</span></span></td>
<td><span data-ttu-id="42894-328">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-329">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-329">CC001</span></span></td>
<td><span data-ttu-id="42894-330">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-330">HR</span></span></td>
<td><span data-ttu-id="42894-331">10001</span><span class="sxs-lookup"><span data-stu-id="42894-331">10001</span></span></td>
<td><span data-ttu-id="42894-332">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-332">Electricity</span></span></td>
<td><span data-ttu-id="42894-333">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-333">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-334">500.00</span><span class="sxs-lookup"><span data-stu-id="42894-334">500.00</span></span></td>
<td><span data-ttu-id="42894-335">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-336">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-336">CC002</span></span></td>
<td><span data-ttu-id="42894-337">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-337">Finance</span></span></td>
<td><span data-ttu-id="42894-338">10001</span><span class="sxs-lookup"><span data-stu-id="42894-338">10001</span></span></td>
<td><span data-ttu-id="42894-339">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-339">Electricity</span></span></td>
<td><span data-ttu-id="42894-340">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-340">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-341">500.00</span><span class="sxs-lookup"><span data-stu-id="42894-341">500.00</span></span></td>
<td><span data-ttu-id="42894-342">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-343">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-343">CC099</span></span></td>
<td><span data-ttu-id="42894-344">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="42894-344">Default cost center</span></span></td>
<td><span data-ttu-id="42894-345">10001</span><span class="sxs-lookup"><span data-stu-id="42894-345">10001</span></span></td>
<td><span data-ttu-id="42894-346">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-346">Electricity</span></span></td>
<td><span data-ttu-id="42894-347">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-347">Variable cost</span></span></td>
<td><span data-ttu-id="42894-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="42894-348">-9,000.00</span></span></td>
<td><span data-ttu-id="42894-349">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-350">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-350">CC001</span></span></td>
<td><span data-ttu-id="42894-351">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-351">HR</span></span></td>
<td><span data-ttu-id="42894-352">10001</span><span class="sxs-lookup"><span data-stu-id="42894-352">10001</span></span></td>
<td><span data-ttu-id="42894-353">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-353">Electricity</span></span></td>
<td><span data-ttu-id="42894-354">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-354">Variable cost</span></span></td>
<td><span data-ttu-id="42894-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="42894-355">1,285.71</span></span></td>
<td><span data-ttu-id="42894-356">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-357">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-357">CC002</span></span></td>
<td><span data-ttu-id="42894-358">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-358">Finance</span></span></td>
<td><span data-ttu-id="42894-359">10001</span><span class="sxs-lookup"><span data-stu-id="42894-359">10001</span></span></td>
<td><span data-ttu-id="42894-360">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-360">Electricity</span></span></td>
<td><span data-ttu-id="42894-361">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-361">Variable cost</span></span></td>
<td><span data-ttu-id="42894-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="42894-362">7,714.29</span></span></td>
<td><span data-ttu-id="42894-363">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-364">للحصول على معلومات تفصيلية حول توزيع التكلفة وأسس التوزيع، راجع سياسة توزيع التكلفة وأسس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="42894-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="42894-365">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="42894-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="42894-366">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="42894-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="42894-367">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="42894-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="42894-368">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="42894-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="42894-369">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="42894-369">Define the overhead rate</span></span>

<span data-ttu-id="42894-370">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="42894-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="42894-371">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="42894-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-372">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-372">Cost object</span></span></th>
<th><span data-ttu-id="42894-373">الساعات</span><span class="sxs-lookup"><span data-stu-id="42894-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-374">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-374">Proj 1</span></span></td>
<td><span data-ttu-id="42894-375">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-375">Project 1</span></span></td>
<td><span data-ttu-id="42894-376">3</span><span class="sxs-lookup"><span data-stu-id="42894-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-377">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-377">Proj 2</span></span></td>
<td><span data-ttu-id="42894-378">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-378">Project 2</span></span></td>
<td><span data-ttu-id="42894-379">1</span><span class="sxs-lookup"><span data-stu-id="42894-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-380">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-381">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-381">Cost object</span></span></th>
<th><span data-ttu-id="42894-382">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-382">Cost element</span></span></th>
<th><span data-ttu-id="42894-383">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-383">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-384">الوحدات</span><span class="sxs-lookup"><span data-stu-id="42894-384">Units</span></span></th>
<th><span data-ttu-id="42894-385">المعدل</span><span class="sxs-lookup"><span data-stu-id="42894-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-386">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-386">CC001</span></span></td>
<td><span data-ttu-id="42894-387">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-387">HR</span></span></td>
<td><span data-ttu-id="42894-388">10001</span><span class="sxs-lookup"><span data-stu-id="42894-388">10001</span></span></td>
<td><span data-ttu-id="42894-389">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-389">Variable cost</span></span></td>
<td><span data-ttu-id="42894-390">1</span><span class="sxs-lookup"><span data-stu-id="42894-390">1</span></span></td>
<td><span data-ttu-id="42894-391">10</span><span class="sxs-lookup"><span data-stu-id="42894-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-392">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="42894-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-393">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-393">Cost object</span></span></th>
<th><span data-ttu-id="42894-394">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-394">Magnitude</span></span></th>
<th><span data-ttu-id="42894-395">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-395">Cost element</span></span></th>
<th><span data-ttu-id="42894-396">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-396">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-397">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-398">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-398">Proj 1</span></span></td>
<td><span data-ttu-id="42894-399">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-399">Project 1</span></span></td>
<td><span data-ttu-id="42894-400">3</span><span class="sxs-lookup"><span data-stu-id="42894-400">3</span></span></td>
<td><span data-ttu-id="42894-401">10001</span><span class="sxs-lookup"><span data-stu-id="42894-401">10001</span></span></td>
<td><span data-ttu-id="42894-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="42894-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="42894-403">30.00</span><span class="sxs-lookup"><span data-stu-id="42894-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-404">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-404">Proj 2</span></span></td>
<td><span data-ttu-id="42894-405">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-405">Project 2</span></span></td>
<td><span data-ttu-id="42894-406">1</span><span class="sxs-lookup"><span data-stu-id="42894-406">1</span></span></td>
<td><span data-ttu-id="42894-407">10001</span><span class="sxs-lookup"><span data-stu-id="42894-407">10001</span></span></td>
<td><span data-ttu-id="42894-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="42894-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="42894-409">10.00</span><span class="sxs-lookup"><span data-stu-id="42894-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="42894-410">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-411">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-411">Journal</span></span></th>
<th><span data-ttu-id="42894-412">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="42894-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="42894-413">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="42894-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="42894-414">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="42894-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-415">00003</span><span class="sxs-lookup"><span data-stu-id="42894-415">00003</span></span></td>
<td><span data-ttu-id="42894-416">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="42894-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="42894-417">مالي</span><span class="sxs-lookup"><span data-stu-id="42894-417">Fiscal</span></span></td>
<td><span data-ttu-id="42894-418">2017</span><span class="sxs-lookup"><span data-stu-id="42894-418">2017</span></span></td>
<td><span data-ttu-id="42894-419">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-419">Period 1</span></span></td>
<td><span data-ttu-id="42894-420">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="42894-421">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="42894-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-422">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="42894-423">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-423">Cost object</span></span></th>
<th><span data-ttu-id="42894-424">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-425">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-426">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-426">Proj 1</span></span></td>
<td><span data-ttu-id="42894-427">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="42894-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="42894-428">3.00</span><span class="sxs-lookup"><span data-stu-id="42894-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-429">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-430">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-430">Proj 2</span></span></td>
<td><span data-ttu-id="42894-431">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="42894-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="42894-432">1.00</span><span class="sxs-lookup"><span data-stu-id="42894-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="42894-433">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-434">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-435">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-435">Cost element</span></span></th>
<th><span data-ttu-id="42894-436">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-436">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-437">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-437">Amount</span></span></th>
<th><span data-ttu-id="42894-438">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="42894-439">CC0001</span></span></td>
<td><span data-ttu-id="42894-440">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-440">HR</span></span></td>
<td><span data-ttu-id="42894-441">10001</span><span class="sxs-lookup"><span data-stu-id="42894-441">10001</span></span></td>
<td><span data-ttu-id="42894-442">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-442">Electricity</span></span></td>
<td><span data-ttu-id="42894-443">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-443">Variable cost</span></span></td>
<td><span data-ttu-id="42894-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="42894-444">-30.00</span></span></td>
<td><span data-ttu-id="42894-445">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-446">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-446">Proj 1</span></span></td>
<td><span data-ttu-id="42894-447">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="42894-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="42894-448">10001</span><span class="sxs-lookup"><span data-stu-id="42894-448">10001</span></span></td>
<td><span data-ttu-id="42894-449">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-449">Electricity</span></span></td>
<td><span data-ttu-id="42894-450">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-450">Variable cost</span></span></td>
<td><span data-ttu-id="42894-451">30.00</span><span class="sxs-lookup"><span data-stu-id="42894-451">30.00</span></span></td>
<td><span data-ttu-id="42894-452">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-453">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-453">CC001</span></span></td>
<td><span data-ttu-id="42894-454">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-454">HR</span></span></td>
<td><span data-ttu-id="42894-455">10001</span><span class="sxs-lookup"><span data-stu-id="42894-455">10001</span></span></td>
<td><span data-ttu-id="42894-456">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-456">Electricity</span></span></td>
<td><span data-ttu-id="42894-457">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-457">Variable cost</span></span></td>
<td><span data-ttu-id="42894-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="42894-458">-10.00</span></span></td>
<td><span data-ttu-id="42894-459">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-460">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-460">Proj 2</span></span></td>
<td><span data-ttu-id="42894-461">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="42894-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="42894-462">10001</span><span class="sxs-lookup"><span data-stu-id="42894-462">10001</span></span></td>
<td><span data-ttu-id="42894-463">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-463">Electricity</span></span></td>
<td><span data-ttu-id="42894-464">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-464">Variable cost</span></span></td>
<td><span data-ttu-id="42894-465">10.00</span><span class="sxs-lookup"><span data-stu-id="42894-465">10.00</span></span></td>
<td><span data-ttu-id="42894-466">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-467">للحصول على معلومات تفصيلية حول سياسة معدل المصروفات الزائدة، راجع سياسة معدل المصروفات الزائدة وأسس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="42894-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="42894-468">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="42894-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="42894-469">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="42894-470">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="42894-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="42894-471">يدعم تطبيق Finance and Operations طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="42894-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="42894-472">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="42894-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="42894-473">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="42894-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="42894-474">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="42894-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="42894-475">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="42894-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="42894-476">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="42894-477">[![الأسلوب المتبادل](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="42894-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="42894-478">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-478">Define the cost allocation</span></span>

<span data-ttu-id="42894-479">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="42894-480">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="42894-481">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="42894-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-482">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-482">Cost object</span></span></th>
<th><span data-ttu-id="42894-483">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-484">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-484">CC002</span></span></td>
<td><span data-ttu-id="42894-485">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-485">Finance</span></span></td>
<td><span data-ttu-id="42894-486">35</span><span class="sxs-lookup"><span data-stu-id="42894-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-487">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-487">CC003</span></span></td>
<td><span data-ttu-id="42894-488">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-488">Assembly</span></span></td>
<td><span data-ttu-id="42894-489">55</span><span class="sxs-lookup"><span data-stu-id="42894-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-490">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-490">CC004</span></span></td>
<td><span data-ttu-id="42894-491">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-491">Packaging</span></span></td>
<td><span data-ttu-id="42894-492">10</span><span class="sxs-lookup"><span data-stu-id="42894-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-493">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="42894-494">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="42894-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-495">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-495">Cost object</span></span></th>
<th><span data-ttu-id="42894-496">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="42894-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-497">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-497">CC003</span></span></td>
<td><span data-ttu-id="42894-498">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-498">Assembly</span></span></td>
<td><span data-ttu-id="42894-499">65</span><span class="sxs-lookup"><span data-stu-id="42894-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-500">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-500">CC004</span></span></td>
<td><span data-ttu-id="42894-501">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-501">Packaging</span></span></td>
<td><span data-ttu-id="42894-502">35</span><span class="sxs-lookup"><span data-stu-id="42894-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-503">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="42894-504">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="42894-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-505">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-505">Cost object</span></span></th>
<th><span data-ttu-id="42894-506">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="42894-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-507">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-507">Prod 1</span></span></td>
<td><span data-ttu-id="42894-508">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-508">Product 1</span></span></td>
<td><span data-ttu-id="42894-509">60</span><span class="sxs-lookup"><span data-stu-id="42894-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-510">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-510">Prod 2</span></span></td>
<td><span data-ttu-id="42894-511">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-511">Product 2</span></span></td>
<td><span data-ttu-id="42894-512">20</span><span class="sxs-lookup"><span data-stu-id="42894-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-513">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="42894-514">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="42894-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-515">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-515">Cost object</span></span></th>
<th><span data-ttu-id="42894-516">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="42894-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-517">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-517">Prod 1</span></span></td>
<td><span data-ttu-id="42894-518">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-518">Product 1</span></span></td>
<td><span data-ttu-id="42894-519">80</span><span class="sxs-lookup"><span data-stu-id="42894-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-520">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-520">Prod 2</span></span></td>
<td><span data-ttu-id="42894-521">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-521">Product 2</span></span></td>
<td><span data-ttu-id="42894-522">15</span><span class="sxs-lookup"><span data-stu-id="42894-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-523">**ملاحظة:** في Finance and Operations، بإمكان القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج أن تشتق من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="42894-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="42894-524">للحصول على معلومات أكثر تفصيلاً حول موفري القياسات الإحصائية، راجع قالب موفر القياسات الإحصائية.</span><span class="sxs-lookup"><span data-stu-id="42894-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="42894-525">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)‬ يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="42894-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-526">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-526">Cost object</span></span></th>
<th><span data-ttu-id="42894-527">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-527">Magnitude</span></span></th>
<th><span data-ttu-id="42894-528">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-528">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-529">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-529">Amount</span></span></th>
<th><span data-ttu-id="42894-530">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-531">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-531">CC002</span></span></td>
<td><span data-ttu-id="42894-532">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-532">Finance</span></span></td>
<td><span data-ttu-id="42894-533">35</span><span class="sxs-lookup"><span data-stu-id="42894-533">35</span></span></td>
<td><span data-ttu-id="42894-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="42894-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="42894-535">175.00</span><span class="sxs-lookup"><span data-stu-id="42894-535">175.00</span></span></td>
<td><span data-ttu-id="42894-536">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-537">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-537">CC003</span></span></td>
<td><span data-ttu-id="42894-538">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-538">Assembly</span></span></td>
<td><span data-ttu-id="42894-539">55</span><span class="sxs-lookup"><span data-stu-id="42894-539">55</span></span></td>
<td><span data-ttu-id="42894-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="42894-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="42894-541">275.00</span><span class="sxs-lookup"><span data-stu-id="42894-541">275.00</span></span></td>
<td><span data-ttu-id="42894-542">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-543">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-543">CC004</span></span></td>
<td><span data-ttu-id="42894-544">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-544">Packaging</span></span></td>
<td><span data-ttu-id="42894-545">10</span><span class="sxs-lookup"><span data-stu-id="42894-545">10</span></span></td>
<td><span data-ttu-id="42894-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="42894-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="42894-547">50.00</span><span class="sxs-lookup"><span data-stu-id="42894-547">50.00</span></span></td>
<td><span data-ttu-id="42894-548">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-549">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-549">CC002</span></span></td>
<td><span data-ttu-id="42894-550">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-550">Finance</span></span></td>
<td><span data-ttu-id="42894-551">35</span><span class="sxs-lookup"><span data-stu-id="42894-551">35</span></span></td>
<td><span data-ttu-id="42894-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="42894-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="42894-553">436.00</span><span class="sxs-lookup"><span data-stu-id="42894-553">436.00</span></span></td>
<td><span data-ttu-id="42894-554">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-555">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-555">CC003</span></span></td>
<td><span data-ttu-id="42894-556">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-556">Assembly</span></span></td>
<td><span data-ttu-id="42894-557">55</span><span class="sxs-lookup"><span data-stu-id="42894-557">55</span></span></td>
<td><span data-ttu-id="42894-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="42894-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="42894-559">685.14</span><span class="sxs-lookup"><span data-stu-id="42894-559">685.14</span></span></td>
<td><span data-ttu-id="42894-560">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-561">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-561">CC004</span></span></td>
<td><span data-ttu-id="42894-562">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-562">Packaging</span></span></td>
<td><span data-ttu-id="42894-563">10</span><span class="sxs-lookup"><span data-stu-id="42894-563">10</span></span></td>
<td><span data-ttu-id="42894-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="42894-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="42894-565">124.57</span><span class="sxs-lookup"><span data-stu-id="42894-565">124.57</span></span></td>
<td><span data-ttu-id="42894-566">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-567">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="42894-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-568">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-568">Cost object</span></span></th>
<th><span data-ttu-id="42894-569">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-569">Magnitude</span></span></th>
<th><span data-ttu-id="42894-570">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-570">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-571">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-571">Amount</span></span></th>
<th><span data-ttu-id="42894-572">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-573">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-573">CC003</span></span></td>
<td><span data-ttu-id="42894-574">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-574">Assembly</span></span></td>
<td><span data-ttu-id="42894-575">65</span><span class="sxs-lookup"><span data-stu-id="42894-575">65</span></span></td>
<td><span data-ttu-id="42894-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="42894-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="42894-577">438.75</span><span class="sxs-lookup"><span data-stu-id="42894-577">438.75</span></span></td>
<td><span data-ttu-id="42894-578">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-579">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-579">CC004</span></span></td>
<td><span data-ttu-id="42894-580">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-580">Packaging</span></span></td>
<td><span data-ttu-id="42894-581">35</span><span class="sxs-lookup"><span data-stu-id="42894-581">35</span></span></td>
<td><span data-ttu-id="42894-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="42894-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="42894-583">236.25</span><span class="sxs-lookup"><span data-stu-id="42894-583">236.25</span></span></td>
<td><span data-ttu-id="42894-584">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-585">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-585">CC003</span></span></td>
<td><span data-ttu-id="42894-586">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-586">Assembly</span></span></td>
<td><span data-ttu-id="42894-587">65</span><span class="sxs-lookup"><span data-stu-id="42894-587">65</span></span></td>
<td><span data-ttu-id="42894-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="42894-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="42894-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="42894-589">5,297.69</span></span></td>
<td><span data-ttu-id="42894-590">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-591">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-591">CC004</span></span></td>
<td><span data-ttu-id="42894-592">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-592">Packaging</span></span></td>
<td><span data-ttu-id="42894-593">35</span><span class="sxs-lookup"><span data-stu-id="42894-593">35</span></span></td>
<td><span data-ttu-id="42894-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="42894-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="42894-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="42894-595">2,852.60</span></span></td>
<td><span data-ttu-id="42894-596">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-597">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="42894-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-598">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-598">Cost object</span></span></th>
<th><span data-ttu-id="42894-599">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-599">Magnitude</span></span></th>
<th><span data-ttu-id="42894-600">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-600">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-601">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-601">Amount</span></span></th>
<th><span data-ttu-id="42894-602">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-603">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-603">Prod 1</span></span></td>
<td><span data-ttu-id="42894-604">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-604">Product 1</span></span></td>
<td><span data-ttu-id="42894-605">60</span><span class="sxs-lookup"><span data-stu-id="42894-605">60</span></span></td>
<td><span data-ttu-id="42894-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="42894-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="42894-607">535.31</span><span class="sxs-lookup"><span data-stu-id="42894-607">535.31</span></span></td>
<td><span data-ttu-id="42894-608">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-609">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-609">Prod 2</span></span></td>
<td><span data-ttu-id="42894-610">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-610">Product 2</span></span></td>
<td><span data-ttu-id="42894-611">20</span><span class="sxs-lookup"><span data-stu-id="42894-611">20</span></span></td>
<td><span data-ttu-id="42894-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="42894-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="42894-613">178.44</span><span class="sxs-lookup"><span data-stu-id="42894-613">178.44</span></span></td>
<td><span data-ttu-id="42894-614">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-615">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-615">Prod 1</span></span></td>
<td><span data-ttu-id="42894-616">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-616">Product 1</span></span></td>
<td><span data-ttu-id="42894-617">60</span><span class="sxs-lookup"><span data-stu-id="42894-617">60</span></span></td>
<td><span data-ttu-id="42894-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="42894-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="42894-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="42894-619">4,487.12</span></span></td>
<td><span data-ttu-id="42894-620">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-621">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-621">Prod 2</span></span></td>
<td><span data-ttu-id="42894-622">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-622">Product 2</span></span></td>
<td><span data-ttu-id="42894-623">20</span><span class="sxs-lookup"><span data-stu-id="42894-623">20</span></span></td>
<td><span data-ttu-id="42894-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="42894-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="42894-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="42894-625">1,495.71</span></span></td>
<td><span data-ttu-id="42894-626">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42894-627">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="42894-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-628">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-628">Cost object</span></span></th>
<th><span data-ttu-id="42894-629">المقدار</span><span class="sxs-lookup"><span data-stu-id="42894-629">Magnitude</span></span></th>
<th><span data-ttu-id="42894-630">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="42894-630">Allocation factor</span></span></th>
<th><span data-ttu-id="42894-631">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-631">Amount</span></span></th>
<th><span data-ttu-id="42894-632">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-633">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-633">Prod 1</span></span></td>
<td><span data-ttu-id="42894-634">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-634">Product 1</span></span></td>
<td><span data-ttu-id="42894-635">80</span><span class="sxs-lookup"><span data-stu-id="42894-635">80</span></span></td>
<td><span data-ttu-id="42894-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="42894-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="42894-637">241.05</span><span class="sxs-lookup"><span data-stu-id="42894-637">241.05</span></span></td>
<td><span data-ttu-id="42894-638">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-639">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-639">Prod 2</span></span></td>
<td><span data-ttu-id="42894-640">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-640">Product 2</span></span></td>
<td><span data-ttu-id="42894-641">15</span><span class="sxs-lookup"><span data-stu-id="42894-641">15</span></span></td>
<td><span data-ttu-id="42894-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="42894-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="42894-643">45.20</span><span class="sxs-lookup"><span data-stu-id="42894-643">45.20</span></span></td>
<td><span data-ttu-id="42894-644">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-645">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-645">Prod 1</span></span></td>
<td><span data-ttu-id="42894-646">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-646">Product 1</span></span></td>
<td><span data-ttu-id="42894-647">80</span><span class="sxs-lookup"><span data-stu-id="42894-647">80</span></span></td>
<td><span data-ttu-id="42894-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="42894-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="42894-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="42894-649">2,507.09</span></span></td>
<td><span data-ttu-id="42894-650">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-651">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-651">Prod 2</span></span></td>
<td><span data-ttu-id="42894-652">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-652">Product 2</span></span></td>
<td><span data-ttu-id="42894-653">15</span><span class="sxs-lookup"><span data-stu-id="42894-653">15</span></span></td>
<td><span data-ttu-id="42894-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="42894-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="42894-655">470.08</span><span class="sxs-lookup"><span data-stu-id="42894-655">470.08</span></span></td>
<td><span data-ttu-id="42894-656">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="42894-657">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="42894-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-658">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="42894-658">Journal</span></span></th>
<th><span data-ttu-id="42894-659">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="42894-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="42894-660">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="42894-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="42894-661">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="42894-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-662">00004</span><span class="sxs-lookup"><span data-stu-id="42894-662">00004</span></span></td>
<td><span data-ttu-id="42894-663">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="42894-664">مالي</span><span class="sxs-lookup"><span data-stu-id="42894-664">Fiscal</span></span></td>
<td><span data-ttu-id="42894-665">2017</span><span class="sxs-lookup"><span data-stu-id="42894-665">2017</span></span></td>
<td><span data-ttu-id="42894-666">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-666">Period 1</span></span></td>
<td><span data-ttu-id="42894-667">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="42894-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="42894-668">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="42894-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="42894-669">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="42894-670">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-671">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-671">Cost element</span></span></th>
<th><span data-ttu-id="42894-672">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-672">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-673">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-674">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-675">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-675">CC001</span></span></td>
<td><span data-ttu-id="42894-676">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-676">HR</span></span></td>
<td><span data-ttu-id="42894-677">10001</span><span class="sxs-lookup"><span data-stu-id="42894-677">10001</span></span></td>
<td><span data-ttu-id="42894-678">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-678">Electricity</span></span></td>
<td><span data-ttu-id="42894-679">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-679">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-680">500.00</span><span class="sxs-lookup"><span data-stu-id="42894-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-681">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-682">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-682">CC001</span></span></td>
<td><span data-ttu-id="42894-683">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-683">HR</span></span></td>
<td><span data-ttu-id="42894-684">10001</span><span class="sxs-lookup"><span data-stu-id="42894-684">10001</span></span></td>
<td><span data-ttu-id="42894-685">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-685">Electricity</span></span></td>
<td><span data-ttu-id="42894-686">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-686">Variable cost</span></span></td>
<td><span data-ttu-id="42894-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="42894-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-688">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-689">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-689">CC002</span></span></td>
<td><span data-ttu-id="42894-690">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-690">Finance</span></span></td>
<td><span data-ttu-id="42894-691">10001</span><span class="sxs-lookup"><span data-stu-id="42894-691">10001</span></span></td>
<td><span data-ttu-id="42894-692">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-692">Electricity</span></span></td>
<td><span data-ttu-id="42894-693">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-693">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-694">675.00</span><span class="sxs-lookup"><span data-stu-id="42894-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-695">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-696">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-696">CC002</span></span></td>
<td><span data-ttu-id="42894-697">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-697">Finance</span></span></td>
<td><span data-ttu-id="42894-698">10001</span><span class="sxs-lookup"><span data-stu-id="42894-698">10001</span></span></td>
<td><span data-ttu-id="42894-699">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-699">Electricity</span></span></td>
<td><span data-ttu-id="42894-700">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-700">Variable cost</span></span></td>
<td><span data-ttu-id="42894-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="42894-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-702">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-703">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-703">CC003</span></span></td>
<td><span data-ttu-id="42894-704">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-704">Assembly</span></span></td>
<td><span data-ttu-id="42894-705">10001</span><span class="sxs-lookup"><span data-stu-id="42894-705">10001</span></span></td>
<td><span data-ttu-id="42894-706">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-706">Electricity</span></span></td>
<td><span data-ttu-id="42894-707">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-707">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-708">713.75</span><span class="sxs-lookup"><span data-stu-id="42894-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-709">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-710">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-710">CC003</span></span></td>
<td><span data-ttu-id="42894-711">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-711">Assembly</span></span></td>
<td><span data-ttu-id="42894-712">10001</span><span class="sxs-lookup"><span data-stu-id="42894-712">10001</span></span></td>
<td><span data-ttu-id="42894-713">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-713">Electricity</span></span></td>
<td><span data-ttu-id="42894-714">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-714">Variable cost</span></span></td>
<td><span data-ttu-id="42894-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="42894-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-716">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-717">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-717">CC003</span></span></td>
<td><span data-ttu-id="42894-718">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-718">Packaging</span></span></td>
<td><span data-ttu-id="42894-719">10001</span><span class="sxs-lookup"><span data-stu-id="42894-719">10001</span></span></td>
<td><span data-ttu-id="42894-720">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-720">Electricity</span></span></td>
<td><span data-ttu-id="42894-721">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-721">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-722">286.25</span><span class="sxs-lookup"><span data-stu-id="42894-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-723">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-724">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-724">CC003</span></span></td>
<td><span data-ttu-id="42894-725">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-725">Packaging</span></span></td>
<td><span data-ttu-id="42894-726">10001</span><span class="sxs-lookup"><span data-stu-id="42894-726">10001</span></span></td>
<td><span data-ttu-id="42894-727">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-727">Electricity</span></span></td>
<td><span data-ttu-id="42894-728">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-728">Variable cost</span></span></td>
<td><span data-ttu-id="42894-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="42894-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-730">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-731">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-731">Prod 1</span></span></td>
<td><span data-ttu-id="42894-732">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-732">Product 1</span></span></td>
<td><span data-ttu-id="42894-733">10001</span><span class="sxs-lookup"><span data-stu-id="42894-733">10001</span></span></td>
<td><span data-ttu-id="42894-734">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-734">Electricity</span></span></td>
<td><span data-ttu-id="42894-735">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-735">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-736">776.36</span><span class="sxs-lookup"><span data-stu-id="42894-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-737">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-738">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-738">Prod 1</span></span></td>
<td><span data-ttu-id="42894-739">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-739">Product 1</span></span></td>
<td><span data-ttu-id="42894-740">10001</span><span class="sxs-lookup"><span data-stu-id="42894-740">10001</span></span></td>
<td><span data-ttu-id="42894-741">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-741">Electricity</span></span></td>
<td><span data-ttu-id="42894-742">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-742">Variable cost</span></span></td>
<td><span data-ttu-id="42894-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="42894-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-744">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-745">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-745">Prod 2</span></span></td>
<td><span data-ttu-id="42894-746">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-746">Product 1</span></span></td>
<td><span data-ttu-id="42894-747">10001</span><span class="sxs-lookup"><span data-stu-id="42894-747">10001</span></span></td>
<td><span data-ttu-id="42894-748">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-748">Electricity</span></span></td>
<td><span data-ttu-id="42894-749">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-749">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-750">223.64</span><span class="sxs-lookup"><span data-stu-id="42894-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-751">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="42894-752">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-752">Prod 2</span></span></td>
<td><span data-ttu-id="42894-753">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-753">Product 1</span></span></td>
<td><span data-ttu-id="42894-754">10001</span><span class="sxs-lookup"><span data-stu-id="42894-754">10001</span></span></td>
<td><span data-ttu-id="42894-755">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-755">Electricity</span></span></td>
<td><span data-ttu-id="42894-756">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-756">Variable cost</span></span></td>
<td><span data-ttu-id="42894-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="42894-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="42894-758">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="42894-759">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="42894-760">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-760">Cost element</span></span></th>
<th><span data-ttu-id="42894-761">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-761">Cost behavior</span></span></th>
<th><span data-ttu-id="42894-762">المبلغ</span><span class="sxs-lookup"><span data-stu-id="42894-762">Amount</span></span></th>
<th><span data-ttu-id="42894-763">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="42894-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42894-764">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-764">CC001</span></span></td>
<td><span data-ttu-id="42894-765">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-765">HR</span></span></td>
<td><span data-ttu-id="42894-766">10001</span><span class="sxs-lookup"><span data-stu-id="42894-766">10001</span></span></td>
<td><span data-ttu-id="42894-767">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-767">Electricity</span></span></td>
<td><span data-ttu-id="42894-768">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-768">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="42894-769">-500.00</span></span></td>
<td><span data-ttu-id="42894-770">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-771">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-771">CC002</span></span></td>
<td><span data-ttu-id="42894-772">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-772">Finance</span></span></td>
<td><span data-ttu-id="42894-773">10001</span><span class="sxs-lookup"><span data-stu-id="42894-773">10001</span></span></td>
<td><span data-ttu-id="42894-774">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-774">Electricity</span></span></td>
<td><span data-ttu-id="42894-775">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-775">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-776">175.00</span><span class="sxs-lookup"><span data-stu-id="42894-776">175.00</span></span></td>
<td><span data-ttu-id="42894-777">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-778">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-778">CC003</span></span></td>
<td><span data-ttu-id="42894-779">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-779">Assembly</span></span></td>
<td><span data-ttu-id="42894-780">10001</span><span class="sxs-lookup"><span data-stu-id="42894-780">10001</span></span></td>
<td><span data-ttu-id="42894-781">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-781">Electricity</span></span></td>
<td><span data-ttu-id="42894-782">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-782">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-783">275.00</span><span class="sxs-lookup"><span data-stu-id="42894-783">275.00</span></span></td>
<td><span data-ttu-id="42894-784">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-785">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-785">CC004</span></span></td>
<td><span data-ttu-id="42894-786">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-786">Packaging</span></span></td>
<td><span data-ttu-id="42894-787">10001</span><span class="sxs-lookup"><span data-stu-id="42894-787">10001</span></span></td>
<td><span data-ttu-id="42894-788">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-788">Electricity</span></span></td>
<td><span data-ttu-id="42894-789">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-789">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-790">50,00</span><span class="sxs-lookup"><span data-stu-id="42894-790">50,00</span></span></td>
<td><span data-ttu-id="42894-791">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-792">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-792">CC001</span></span></td>
<td><span data-ttu-id="42894-793">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="42894-793">HR</span></span></td>
<td><span data-ttu-id="42894-794">10001</span><span class="sxs-lookup"><span data-stu-id="42894-794">10001</span></span></td>
<td><span data-ttu-id="42894-795">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-795">Electricity</span></span></td>
<td><span data-ttu-id="42894-796">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-796">Variable cost</span></span></td>
<td><span data-ttu-id="42894-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="42894-797">-1,245.71</span></span></td>
<td><span data-ttu-id="42894-798">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-799">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-799">CC002</span></span></td>
<td><span data-ttu-id="42894-800">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-800">Finance</span></span></td>
<td><span data-ttu-id="42894-801">10001</span><span class="sxs-lookup"><span data-stu-id="42894-801">10001</span></span></td>
<td><span data-ttu-id="42894-802">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-802">Electricity</span></span></td>
<td><span data-ttu-id="42894-803">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-803">Variable cost</span></span></td>
<td><span data-ttu-id="42894-804">436.00</span><span class="sxs-lookup"><span data-stu-id="42894-804">436.00</span></span></td>
<td><span data-ttu-id="42894-805">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-806">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-806">CC003</span></span></td>
<td><span data-ttu-id="42894-807">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-807">Assembly</span></span></td>
<td><span data-ttu-id="42894-808">10001</span><span class="sxs-lookup"><span data-stu-id="42894-808">10001</span></span></td>
<td><span data-ttu-id="42894-809">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-809">Electricity</span></span></td>
<td><span data-ttu-id="42894-810">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-810">Variable cost</span></span></td>
<td><span data-ttu-id="42894-811">685.14</span><span class="sxs-lookup"><span data-stu-id="42894-811">685.14</span></span></td>
<td><span data-ttu-id="42894-812">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-813">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-813">CC004</span></span></td>
<td><span data-ttu-id="42894-814">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-814">Packaging</span></span></td>
<td><span data-ttu-id="42894-815">10001</span><span class="sxs-lookup"><span data-stu-id="42894-815">10001</span></span></td>
<td><span data-ttu-id="42894-816">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-816">Electricity</span></span></td>
<td><span data-ttu-id="42894-817">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-817">Variable cost</span></span></td>
<td><span data-ttu-id="42894-818">124.57</span><span class="sxs-lookup"><span data-stu-id="42894-818">124.57</span></span></td>
<td><span data-ttu-id="42894-819">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-820">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-820">CC002</span></span></td>
<td><span data-ttu-id="42894-821">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-821">Finance</span></span></td>
<td><span data-ttu-id="42894-822">10001</span><span class="sxs-lookup"><span data-stu-id="42894-822">10001</span></span></td>
<td><span data-ttu-id="42894-823">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-823">Electricity</span></span></td>
<td><span data-ttu-id="42894-824">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-824">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="42894-825">-675.00</span></span></td>
<td><span data-ttu-id="42894-826">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-827">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-827">CC003</span></span></td>
<td><span data-ttu-id="42894-828">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-828">Assembly</span></span></td>
<td><span data-ttu-id="42894-829">10001</span><span class="sxs-lookup"><span data-stu-id="42894-829">10001</span></span></td>
<td><span data-ttu-id="42894-830">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-830">Electricity</span></span></td>
<td><span data-ttu-id="42894-831">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-831">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-832">438.75</span><span class="sxs-lookup"><span data-stu-id="42894-832">438.75</span></span></td>
<td><span data-ttu-id="42894-833">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-834">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-834">CC004</span></span></td>
<td><span data-ttu-id="42894-835">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-835">Packaging</span></span></td>
<td><span data-ttu-id="42894-836">10001</span><span class="sxs-lookup"><span data-stu-id="42894-836">10001</span></span></td>
<td><span data-ttu-id="42894-837">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-837">Electricity</span></span></td>
<td><span data-ttu-id="42894-838">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-838">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-839">236.25</span><span class="sxs-lookup"><span data-stu-id="42894-839">236.25</span></span></td>
<td><span data-ttu-id="42894-840">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-841">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-841">CC002</span></span></td>
<td><span data-ttu-id="42894-842">المالية</span><span class="sxs-lookup"><span data-stu-id="42894-842">Finance</span></span></td>
<td><span data-ttu-id="42894-843">10001</span><span class="sxs-lookup"><span data-stu-id="42894-843">10001</span></span></td>
<td><span data-ttu-id="42894-844">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-844">Electricity</span></span></td>
<td><span data-ttu-id="42894-845">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-845">Variable cost</span></span></td>
<td><span data-ttu-id="42894-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="42894-846">-8,150.29</span></span></td>
<td><span data-ttu-id="42894-847">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-848">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-848">CC003</span></span></td>
<td><span data-ttu-id="42894-849">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-849">Assembly</span></span></td>
<td><span data-ttu-id="42894-850">10001</span><span class="sxs-lookup"><span data-stu-id="42894-850">10001</span></span></td>
<td><span data-ttu-id="42894-851">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-851">Electricity</span></span></td>
<td><span data-ttu-id="42894-852">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-852">Variable cost</span></span></td>
<td><span data-ttu-id="42894-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="42894-853">5,297.69</span></span></td>
<td><span data-ttu-id="42894-854">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-855">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-855">CC004</span></span></td>
<td><span data-ttu-id="42894-856">التعبئة</span><span class="sxs-lookup"><span data-stu-id="42894-856">Packaging</span></span></td>
<td><span data-ttu-id="42894-857">10001</span><span class="sxs-lookup"><span data-stu-id="42894-857">10001</span></span></td>
<td><span data-ttu-id="42894-858">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-858">Electricity</span></span></td>
<td><span data-ttu-id="42894-859">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-859">Variable cost</span></span></td>
<td><span data-ttu-id="42894-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="42894-860">2,852.60</span></span></td>
<td><span data-ttu-id="42894-861">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-862">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-862">CC003</span></span></td>
<td><span data-ttu-id="42894-863">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-863">Assembly</span></span></td>
<td><span data-ttu-id="42894-864">10001</span><span class="sxs-lookup"><span data-stu-id="42894-864">10001</span></span></td>
<td><span data-ttu-id="42894-865">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-865">Electricity</span></span></td>
<td><span data-ttu-id="42894-866">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-866">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="42894-867">-713.75</span></span></td>
<td><span data-ttu-id="42894-868">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-869">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-869">Prod 1</span></span></td>
<td><span data-ttu-id="42894-870">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-870">Product 1</span></span></td>
<td><span data-ttu-id="42894-871">10001</span><span class="sxs-lookup"><span data-stu-id="42894-871">10001</span></span></td>
<td><span data-ttu-id="42894-872">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-872">Electricity</span></span></td>
<td><span data-ttu-id="42894-873">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-873">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-874">535.31</span><span class="sxs-lookup"><span data-stu-id="42894-874">535.31</span></span></td>
<td><span data-ttu-id="42894-875">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-876">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-876">Prod 2</span></span></td>
<td><span data-ttu-id="42894-877">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-877">Product 2</span></span></td>
<td><span data-ttu-id="42894-878">10001</span><span class="sxs-lookup"><span data-stu-id="42894-878">10001</span></span></td>
<td><span data-ttu-id="42894-879">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-879">Electricity</span></span></td>
<td><span data-ttu-id="42894-880">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-880">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-881">178.44</span><span class="sxs-lookup"><span data-stu-id="42894-881">178.44</span></span></td>
<td><span data-ttu-id="42894-882">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-883">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-883">CC003</span></span></td>
<td><span data-ttu-id="42894-884">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-884">Assembly</span></span></td>
<td><span data-ttu-id="42894-885">10001</span><span class="sxs-lookup"><span data-stu-id="42894-885">10001</span></span></td>
<td><span data-ttu-id="42894-886">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-886">Electricity</span></span></td>
<td><span data-ttu-id="42894-887">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-887">Variable cost</span></span></td>
<td><span data-ttu-id="42894-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="42894-888">-5,982.83</span></span></td>
<td><span data-ttu-id="42894-889">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-890">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-890">Prod 1</span></span></td>
<td><span data-ttu-id="42894-891">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-891">Product 1</span></span></td>
<td><span data-ttu-id="42894-892">10001</span><span class="sxs-lookup"><span data-stu-id="42894-892">10001</span></span></td>
<td><span data-ttu-id="42894-893">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-893">Electricity</span></span></td>
<td><span data-ttu-id="42894-894">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-894">Variable cost</span></span></td>
<td><span data-ttu-id="42894-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="42894-895">4,487.12</span></span></td>
<td><span data-ttu-id="42894-896">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-897">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-897">Prod 2</span></span></td>
<td><span data-ttu-id="42894-898">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-898">Product 2</span></span></td>
<td><span data-ttu-id="42894-899">10001</span><span class="sxs-lookup"><span data-stu-id="42894-899">10001</span></span></td>
<td><span data-ttu-id="42894-900">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-900">Electricity</span></span></td>
<td><span data-ttu-id="42894-901">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-901">Variable cost</span></span></td>
<td><span data-ttu-id="42894-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="42894-902">1,495.71</span></span></td>
<td><span data-ttu-id="42894-903">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-904">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-904">CC003</span></span></td>
<td><span data-ttu-id="42894-905">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-905">Assembly</span></span></td>
<td><span data-ttu-id="42894-906">10001</span><span class="sxs-lookup"><span data-stu-id="42894-906">10001</span></span></td>
<td><span data-ttu-id="42894-907">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-907">Electricity</span></span></td>
<td><span data-ttu-id="42894-908">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-908">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="42894-909">-286.25</span></span></td>
<td><span data-ttu-id="42894-910">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-911">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-911">Prod 1</span></span></td>
<td><span data-ttu-id="42894-912">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-912">Product 1</span></span></td>
<td><span data-ttu-id="42894-913">10001</span><span class="sxs-lookup"><span data-stu-id="42894-913">10001</span></span></td>
<td><span data-ttu-id="42894-914">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-914">Electricity</span></span></td>
<td><span data-ttu-id="42894-915">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-915">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-916">241.05</span><span class="sxs-lookup"><span data-stu-id="42894-916">241.05</span></span></td>
<td><span data-ttu-id="42894-917">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-918">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-918">Prod 2</span></span></td>
<td><span data-ttu-id="42894-919">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-919">Product 2</span></span></td>
<td><span data-ttu-id="42894-920">10001</span><span class="sxs-lookup"><span data-stu-id="42894-920">10001</span></span></td>
<td><span data-ttu-id="42894-921">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-921">Electricity</span></span></td>
<td><span data-ttu-id="42894-922">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-922">Fixed cost</span></span></td>
<td><span data-ttu-id="42894-923">45.20</span><span class="sxs-lookup"><span data-stu-id="42894-923">45.20</span></span></td>
<td><span data-ttu-id="42894-924">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-925">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-925">CC003</span></span></td>
<td><span data-ttu-id="42894-926">التجميع</span><span class="sxs-lookup"><span data-stu-id="42894-926">Assembly</span></span></td>
<td><span data-ttu-id="42894-927">10001</span><span class="sxs-lookup"><span data-stu-id="42894-927">10001</span></span></td>
<td><span data-ttu-id="42894-928">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-928">Electricity</span></span></td>
<td><span data-ttu-id="42894-929">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-929">Variable cost</span></span></td>
<td><span data-ttu-id="42894-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="42894-930">-2,977.17</span></span></td>
<td><span data-ttu-id="42894-931">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-932">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-932">Prod 1</span></span></td>
<td><span data-ttu-id="42894-933">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-933">Product 1</span></span></td>
<td><span data-ttu-id="42894-934">10001</span><span class="sxs-lookup"><span data-stu-id="42894-934">10001</span></span></td>
<td><span data-ttu-id="42894-935">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-935">Electricity</span></span></td>
<td><span data-ttu-id="42894-936">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-936">Variable cost</span></span></td>
<td><span data-ttu-id="42894-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="42894-937">2,507.09</span></span></td>
<td><span data-ttu-id="42894-938">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42894-939">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-939">Prod 2</span></span></td>
<td><span data-ttu-id="42894-940">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-940">Product 2</span></span></td>
<td><span data-ttu-id="42894-941">10001</span><span class="sxs-lookup"><span data-stu-id="42894-941">10001</span></span></td>
<td><span data-ttu-id="42894-942">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-942">Electricity</span></span></td>
<td><span data-ttu-id="42894-943">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-943">Variable cost</span></span></td>
<td><span data-ttu-id="42894-944">470.08</span><span class="sxs-lookup"><span data-stu-id="42894-944">470.08</span></span></td>
<td><span data-ttu-id="42894-945">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="42894-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="42894-946">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="42894-946">Conclusion</span></span>
<span data-ttu-id="42894-947">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="42894-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="42894-948">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="42894-949">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="42894-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="42894-950">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="42894-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="42894-951">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="42894-952">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="42894-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="42894-953">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="42894-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="42894-954">CC099</span><span class="sxs-lookup"><span data-stu-id="42894-954">CC099</span></span></th>
<th><span data-ttu-id="42894-955">CC001</span><span class="sxs-lookup"><span data-stu-id="42894-955">CC001</span></span></th>
<th><span data-ttu-id="42894-956">CC002</span><span class="sxs-lookup"><span data-stu-id="42894-956">CC002</span></span></th>
<th><span data-ttu-id="42894-957">CC003</span><span class="sxs-lookup"><span data-stu-id="42894-957">CC003</span></span></th>
<th><span data-ttu-id="42894-958">CC004</span><span class="sxs-lookup"><span data-stu-id="42894-958">CC004</span></span></th>
<th><span data-ttu-id="42894-959">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="42894-959">Proj 1</span></span></th>
<th><span data-ttu-id="42894-960">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="42894-960">Proj 2</span></span></th>
<th><span data-ttu-id="42894-961">منتج 1</span><span class="sxs-lookup"><span data-stu-id="42894-961">Prod 1</span></span></th>
<th><span data-ttu-id="42894-962">منتج 2</span><span class="sxs-lookup"><span data-stu-id="42894-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="42894-963">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="42894-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="42894-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="42894-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="42894-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="42894-973">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="42894-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-974">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-974">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="42894-975">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="42894-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-976">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-977">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-978">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-979">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-980">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="42894-981">776.36</span><span class="sxs-lookup"><span data-stu-id="42894-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-982">223.64</span><span class="sxs-lookup"><span data-stu-id="42894-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="42894-984">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="42894-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-985">000</span><span class="sxs-lookup"><span data-stu-id="42894-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-986">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-987">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-988">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-989">0.00</span><span class="sxs-lookup"><span data-stu-id="42894-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-990">30.00</span><span class="sxs-lookup"><span data-stu-id="42894-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-991">10.00</span><span class="sxs-lookup"><span data-stu-id="42894-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="42894-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="42894-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="42894-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="42894-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="42894-995">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="42894-996">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="42894-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="42894-997">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="42894-998">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42894-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="42894-999">لمزيد من المعلومات المفصلة، انظر سياسة زيادة التكاليف‬.</span><span class="sxs-lookup"><span data-stu-id="42894-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="42894-1000">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="42894-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




