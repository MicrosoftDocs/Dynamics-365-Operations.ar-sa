---
title: عملية حساب المصروفات الزائدة
description: يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187987"
---
# <a name="overhead-calculation"></a><span data-ttu-id="3c862-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="3c862-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c862-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="3c862-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="3c862-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="3c862-105">Term definition</span></span>

<span data-ttu-id="3c862-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="3c862-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="3c862-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="3c862-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="3c862-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="3c862-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="3c862-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="3c862-109">Rent</span></span>
-   <span data-ttu-id="3c862-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-110">Electricity</span></span>
-   <span data-ttu-id="3c862-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="3c862-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="3c862-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="3c862-112">Overhead calculation overview</span></span>
<span data-ttu-id="3c862-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="3c862-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="3c862-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="3c862-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="3c862-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="3c862-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="3c862-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="3c862-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="3c862-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="3c862-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="3c862-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="3c862-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="3c862-119">Version type</span></span>
-   <span data-ttu-id="3c862-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="3c862-120">Date and time</span></span>
-   <span data-ttu-id="3c862-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="3c862-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="3c862-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-122">Fiscal year</span></span>
-   <span data-ttu-id="3c862-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-123">Fiscal period</span></span>

<span data-ttu-id="3c862-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="3c862-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="3c862-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="3c862-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="3c862-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="3c862-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="3c862-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="3c862-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="3c862-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="3c862-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="3c862-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="3c862-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="3c862-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="3c862-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="3c862-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="3c862-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="3c862-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="3c862-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="3c862-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="3c862-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="3c862-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c862-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="3c862-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="3c862-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="3c862-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="3c862-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="3c862-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="3c862-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="3c862-140">Main account</span></span></th>
<th><span data-ttu-id="3c862-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="3c862-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="3c862-143">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-143">CC099</span></span></td>
<td><span data-ttu-id="3c862-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-144">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-145">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-145">10001</span></span></td>
<td><span data-ttu-id="3c862-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-146">Electricity</span></span></td>
<td><span data-ttu-id="3c862-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="3c862-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="3c862-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c862-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="3c862-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="3c862-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="3c862-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-151">Define the cost behavior rule</span></span>

<span data-ttu-id="3c862-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="3c862-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="3c862-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="3c862-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="3c862-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="3c862-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="3c862-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="3c862-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="3c862-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="3c862-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="3c862-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="3c862-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="3c862-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="3c862-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-160">Journal</span></span></th>
<th><span data-ttu-id="3c862-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="3c862-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3c862-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="3c862-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3c862-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="3c862-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-164">00001</span><span class="sxs-lookup"><span data-stu-id="3c862-164">00001</span></span></td>
<td><span data-ttu-id="3c862-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="3c862-166">مالي</span><span class="sxs-lookup"><span data-stu-id="3c862-166">Fiscal</span></span></td>
<td><span data-ttu-id="3c862-167">2017</span><span class="sxs-lookup"><span data-stu-id="3c862-167">2017</span></span></td>
<td><span data-ttu-id="3c862-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-168">Period 1</span></span></td>
<td><span data-ttu-id="3c862-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3c862-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="3c862-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-173">Cost element</span></span></th>
<th><span data-ttu-id="3c862-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-174">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="3c862-177">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-177">CC099</span></span></td>
<td><span data-ttu-id="3c862-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-178">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-179">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-179">10001</span></span></td>
<td><span data-ttu-id="3c862-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-180">Electricity</span></span></td>
<td><span data-ttu-id="3c862-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="3c862-181">Unclassified</span></span></td>
<td><span data-ttu-id="3c862-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3c862-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-185">Cost element</span></span></th>
<th><span data-ttu-id="3c862-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-186">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-187">Amount</span></span></th>
<th><span data-ttu-id="3c862-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-189">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-189">CC099</span></span></td>
<td><span data-ttu-id="3c862-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-190">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-191">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-191">10001</span></span></td>
<td><span data-ttu-id="3c862-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-192">Electricity</span></span></td>
<td><span data-ttu-id="3c862-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="3c862-193">Unclassified</span></span></td>
<td><span data-ttu-id="3c862-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-194">10,000.00</span></span></td>
<td><span data-ttu-id="3c862-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-196">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-196">CC099</span></span></td>
<td><span data-ttu-id="3c862-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-197">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-198">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-198">10001</span></span></td>
<td><span data-ttu-id="3c862-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-199">Electricity</span></span></td>
<td><span data-ttu-id="3c862-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="3c862-200">Unclassified</span></span></td>
<td><span data-ttu-id="3c862-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-201">-10,000.00</span></span></td>
<td><span data-ttu-id="3c862-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-203">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-203">CC099</span></span></td>
<td><span data-ttu-id="3c862-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-204">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-205">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-205">10001</span></span></td>
<td><span data-ttu-id="3c862-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-206">Electricity</span></span></td>
<td><span data-ttu-id="3c862-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-207">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-208">1,000.00</span></span></td>
<td><span data-ttu-id="3c862-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-210">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-210">CC099</span></span></td>
<td><span data-ttu-id="3c862-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-211">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-212">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-212">10001</span></span></td>
<td><span data-ttu-id="3c862-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-213">Electricity</span></span></td>
<td><span data-ttu-id="3c862-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-214">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-215">9,000.00</span></span></td>
<td><span data-ttu-id="3c862-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="3c862-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="3c862-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="3c862-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="3c862-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="3c862-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="3c862-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="3c862-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-221">Define the cost distribution rule</span></span>

<span data-ttu-id="3c862-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="3c862-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="3c862-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="3c862-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="3c862-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="3c862-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="3c862-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="3c862-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="3c862-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="3c862-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="3c862-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="3c862-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-228">Cost object</span></span></th>
<th><span data-ttu-id="3c862-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="3c862-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-230">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-230">CC001</span></span></td>
<td><span data-ttu-id="3c862-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-231">HR</span></span></td>
<td><span data-ttu-id="3c862-232">1,000</span><span class="sxs-lookup"><span data-stu-id="3c862-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-233">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-233">CC002</span></span></td>
<td><span data-ttu-id="3c862-234">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-234">Finance</span></span></td>
<td><span data-ttu-id="3c862-235">6,000</span><span class="sxs-lookup"><span data-stu-id="3c862-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-236">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-236">CC003</span></span></td>
<td><span data-ttu-id="3c862-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-237">Assembly</span></span></td>
<td><span data-ttu-id="3c862-238">0</span><span class="sxs-lookup"><span data-stu-id="3c862-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="3c862-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-240">Cost object</span></span></th>
<th><span data-ttu-id="3c862-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-241">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-242">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-244">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-244">CC001</span></span></td>
<td><span data-ttu-id="3c862-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-245">HR</span></span></td>
<td><span data-ttu-id="3c862-246">1,000</span><span class="sxs-lookup"><span data-stu-id="3c862-246">1,000</span></span></td>
<td><span data-ttu-id="3c862-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3c862-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3c862-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-249">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-249">CC002</span></span></td>
<td><span data-ttu-id="3c862-250">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-250">Finance</span></span></td>
<td><span data-ttu-id="3c862-251">6,000</span><span class="sxs-lookup"><span data-stu-id="3c862-251">6,000</span></span></td>
<td><span data-ttu-id="3c862-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3c862-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3c862-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-254">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-254">CC003</span></span></td>
<td><span data-ttu-id="3c862-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-255">Assembly</span></span></td>
<td><span data-ttu-id="3c862-256">0</span><span class="sxs-lookup"><span data-stu-id="3c862-256">0</span></span></td>
<td><span data-ttu-id="3c862-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3c862-258">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="3c862-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="3c862-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="3c862-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-261">Cost object</span></span></th>
<th><span data-ttu-id="3c862-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="3c862-262">Formula</span></span></th>
<th><span data-ttu-id="3c862-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-263">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-264">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-266">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-266">CC001</span></span></td>
<td><span data-ttu-id="3c862-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-267">HR</span></span></td>
<td><span data-ttu-id="3c862-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3c862-269">1</span><span class="sxs-lookup"><span data-stu-id="3c862-269">1</span></span></td>
<td><span data-ttu-id="3c862-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3c862-271">500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-272">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-272">CC002</span></span></td>
<td><span data-ttu-id="3c862-273">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-273">Finance</span></span></td>
<td><span data-ttu-id="3c862-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3c862-275">1</span><span class="sxs-lookup"><span data-stu-id="3c862-275">1</span></span></td>
<td><span data-ttu-id="3c862-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3c862-277">500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-278">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-278">CC003</span></span></td>
<td><span data-ttu-id="3c862-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-279">Assembly</span></span></td>
<td><span data-ttu-id="3c862-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3c862-281">0</span><span class="sxs-lookup"><span data-stu-id="3c862-281">0</span></span></td>
<td><span data-ttu-id="3c862-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3c862-283">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3c862-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-285">Journal</span></span></th>
<th><span data-ttu-id="3c862-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="3c862-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3c862-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="3c862-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3c862-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="3c862-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-289">00002</span><span class="sxs-lookup"><span data-stu-id="3c862-289">00002</span></span></td>
<td><span data-ttu-id="3c862-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="3c862-291">مالي</span><span class="sxs-lookup"><span data-stu-id="3c862-291">Fiscal</span></span></td>
<td><span data-ttu-id="3c862-292">2017</span><span class="sxs-lookup"><span data-stu-id="3c862-292">2017</span></span></td>
<td><span data-ttu-id="3c862-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-293">Period 1</span></span></td>
<td><span data-ttu-id="3c862-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3c862-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="3c862-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-298">Cost element</span></span></th>
<th><span data-ttu-id="3c862-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-299">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-302">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-302">CC099</span></span></td>
<td><span data-ttu-id="3c862-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-303">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-304">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-304">10001</span></span></td>
<td><span data-ttu-id="3c862-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-305">Electricity</span></span></td>
<td><span data-ttu-id="3c862-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-306">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-309">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-309">CC099</span></span></td>
<td><span data-ttu-id="3c862-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-310">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-311">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-311">10001</span></span></td>
<td><span data-ttu-id="3c862-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-312">Electricity</span></span></td>
<td><span data-ttu-id="3c862-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-313">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3c862-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-317">Cost element</span></span></th>
<th><span data-ttu-id="3c862-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-318">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-319">Amount</span></span></th>
<th><span data-ttu-id="3c862-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-321">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-321">CC099</span></span></td>
<td><span data-ttu-id="3c862-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-322">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-323">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-323">10001</span></span></td>
<td><span data-ttu-id="3c862-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-324">Electricity</span></span></td>
<td><span data-ttu-id="3c862-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-325">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-326">-1,000.00</span></span></td>
<td><span data-ttu-id="3c862-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-328">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-328">CC001</span></span></td>
<td><span data-ttu-id="3c862-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-329">HR</span></span></td>
<td><span data-ttu-id="3c862-330">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-330">10001</span></span></td>
<td><span data-ttu-id="3c862-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-331">Electricity</span></span></td>
<td><span data-ttu-id="3c862-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-332">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-333">500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-333">500.00</span></span></td>
<td><span data-ttu-id="3c862-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-335">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-335">CC002</span></span></td>
<td><span data-ttu-id="3c862-336">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-336">Finance</span></span></td>
<td><span data-ttu-id="3c862-337">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-337">10001</span></span></td>
<td><span data-ttu-id="3c862-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-338">Electricity</span></span></td>
<td><span data-ttu-id="3c862-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-339">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-340">500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-340">500.00</span></span></td>
<td><span data-ttu-id="3c862-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-342">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-342">CC099</span></span></td>
<td><span data-ttu-id="3c862-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="3c862-343">Default cost center</span></span></td>
<td><span data-ttu-id="3c862-344">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-344">10001</span></span></td>
<td><span data-ttu-id="3c862-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-345">Electricity</span></span></td>
<td><span data-ttu-id="3c862-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-346">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="3c862-347">-9,000.00</span></span></td>
<td><span data-ttu-id="3c862-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-349">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-349">CC001</span></span></td>
<td><span data-ttu-id="3c862-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-350">HR</span></span></td>
<td><span data-ttu-id="3c862-351">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-351">10001</span></span></td>
<td><span data-ttu-id="3c862-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-352">Electricity</span></span></td>
<td><span data-ttu-id="3c862-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-353">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3c862-354">1,285.71</span></span></td>
<td><span data-ttu-id="3c862-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-356">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-356">CC002</span></span></td>
<td><span data-ttu-id="3c862-357">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-357">Finance</span></span></td>
<td><span data-ttu-id="3c862-358">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-358">10001</span></span></td>
<td><span data-ttu-id="3c862-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-359">Electricity</span></span></td>
<td><span data-ttu-id="3c862-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-360">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3c862-361">7,714.29</span></span></td>
<td><span data-ttu-id="3c862-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="3c862-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="3c862-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="3c862-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="3c862-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="3c862-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="3c862-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="3c862-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="3c862-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="3c862-367">Define the overhead rate</span></span>

<span data-ttu-id="3c862-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="3c862-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="3c862-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="3c862-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-370">Cost object</span></span></th>
<th><span data-ttu-id="3c862-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="3c862-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-372">Proj 1</span></span></td>
<td><span data-ttu-id="3c862-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-373">Project 1</span></span></td>
<td><span data-ttu-id="3c862-374">3</span><span class="sxs-lookup"><span data-stu-id="3c862-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-375">Proj 2</span></span></td>
<td><span data-ttu-id="3c862-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-376">Project 2</span></span></td>
<td><span data-ttu-id="3c862-377">1</span><span class="sxs-lookup"><span data-stu-id="3c862-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-379">Cost object</span></span></th>
<th><span data-ttu-id="3c862-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-380">Cost element</span></span></th>
<th><span data-ttu-id="3c862-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-381">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="3c862-382">Units</span></span></th>
<th><span data-ttu-id="3c862-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="3c862-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-384">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-384">CC001</span></span></td>
<td><span data-ttu-id="3c862-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-385">HR</span></span></td>
<td><span data-ttu-id="3c862-386">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-386">10001</span></span></td>
<td><span data-ttu-id="3c862-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-387">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-388">1</span><span class="sxs-lookup"><span data-stu-id="3c862-388">1</span></span></td>
<td><span data-ttu-id="3c862-389">10</span><span class="sxs-lookup"><span data-stu-id="3c862-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="3c862-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-391">Cost object</span></span></th>
<th><span data-ttu-id="3c862-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-392">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-393">Cost element</span></span></th>
<th><span data-ttu-id="3c862-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-394">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-396">Proj 1</span></span></td>
<td><span data-ttu-id="3c862-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-397">Project 1</span></span></td>
<td><span data-ttu-id="3c862-398">3</span><span class="sxs-lookup"><span data-stu-id="3c862-398">3</span></span></td>
<td><span data-ttu-id="3c862-399">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-399">10001</span></span></td>
<td><span data-ttu-id="3c862-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="3c862-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3c862-401">30.00</span><span class="sxs-lookup"><span data-stu-id="3c862-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-402">Proj 2</span></span></td>
<td><span data-ttu-id="3c862-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-403">Project 2</span></span></td>
<td><span data-ttu-id="3c862-404">1</span><span class="sxs-lookup"><span data-stu-id="3c862-404">1</span></span></td>
<td><span data-ttu-id="3c862-405">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-405">10001</span></span></td>
<td><span data-ttu-id="3c862-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="3c862-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3c862-407">10.00</span><span class="sxs-lookup"><span data-stu-id="3c862-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3c862-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-409">Journal</span></span></th>
<th><span data-ttu-id="3c862-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="3c862-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3c862-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="3c862-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3c862-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="3c862-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-413">00003</span><span class="sxs-lookup"><span data-stu-id="3c862-413">00003</span></span></td>
<td><span data-ttu-id="3c862-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="3c862-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="3c862-415">مالي</span><span class="sxs-lookup"><span data-stu-id="3c862-415">Fiscal</span></span></td>
<td><span data-ttu-id="3c862-416">2017</span><span class="sxs-lookup"><span data-stu-id="3c862-416">2017</span></span></td>
<td><span data-ttu-id="3c862-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-417">Period 1</span></span></td>
<td><span data-ttu-id="3c862-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="3c862-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="3c862-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-421">Cost object</span></span></th>
<th><span data-ttu-id="3c862-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-424">Proj 1</span></span></td>
<td><span data-ttu-id="3c862-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="3c862-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3c862-426">3.00</span><span class="sxs-lookup"><span data-stu-id="3c862-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-428">Proj 2</span></span></td>
<td><span data-ttu-id="3c862-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="3c862-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3c862-430">1.00</span><span class="sxs-lookup"><span data-stu-id="3c862-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3c862-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-433">Cost element</span></span></th>
<th><span data-ttu-id="3c862-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-434">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-435">Amount</span></span></th>
<th><span data-ttu-id="3c862-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="3c862-437">CC0001</span></span></td>
<td><span data-ttu-id="3c862-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-438">HR</span></span></td>
<td><span data-ttu-id="3c862-439">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-439">10001</span></span></td>
<td><span data-ttu-id="3c862-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-440">Electricity</span></span></td>
<td><span data-ttu-id="3c862-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-441">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="3c862-442">-30.00</span></span></td>
<td><span data-ttu-id="3c862-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-444">Proj 1</span></span></td>
<td><span data-ttu-id="3c862-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="3c862-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3c862-446">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-446">10001</span></span></td>
<td><span data-ttu-id="3c862-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-447">Electricity</span></span></td>
<td><span data-ttu-id="3c862-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-448">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-449">30.00</span><span class="sxs-lookup"><span data-stu-id="3c862-449">30.00</span></span></td>
<td><span data-ttu-id="3c862-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-451">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-451">CC001</span></span></td>
<td><span data-ttu-id="3c862-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-452">HR</span></span></td>
<td><span data-ttu-id="3c862-453">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-453">10001</span></span></td>
<td><span data-ttu-id="3c862-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-454">Electricity</span></span></td>
<td><span data-ttu-id="3c862-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-455">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="3c862-456">-10.00</span></span></td>
<td><span data-ttu-id="3c862-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-458">Proj 2</span></span></td>
<td><span data-ttu-id="3c862-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="3c862-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3c862-460">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-460">10001</span></span></td>
<td><span data-ttu-id="3c862-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-461">Electricity</span></span></td>
<td><span data-ttu-id="3c862-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-462">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-463">10.00</span><span class="sxs-lookup"><span data-stu-id="3c862-463">10.00</span></span></td>
<td><span data-ttu-id="3c862-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="3c862-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="3c862-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="3c862-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="3c862-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="3c862-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="3c862-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="3c862-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="3c862-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="3c862-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="3c862-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="3c862-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="3c862-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="3c862-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="3c862-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="3c862-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="3c862-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="3c862-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="3c862-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-475">Define the cost allocation</span></span>

<span data-ttu-id="3c862-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="3c862-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="3c862-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="3c862-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-479">Cost object</span></span></th>
<th><span data-ttu-id="3c862-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-481">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-481">CC002</span></span></td>
<td><span data-ttu-id="3c862-482">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-482">Finance</span></span></td>
<td><span data-ttu-id="3c862-483">35</span><span class="sxs-lookup"><span data-stu-id="3c862-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-484">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-484">CC003</span></span></td>
<td><span data-ttu-id="3c862-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-485">Assembly</span></span></td>
<td><span data-ttu-id="3c862-486">55</span><span class="sxs-lookup"><span data-stu-id="3c862-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-487">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-487">CC004</span></span></td>
<td><span data-ttu-id="3c862-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-488">Packaging</span></span></td>
<td><span data-ttu-id="3c862-489">10</span><span class="sxs-lookup"><span data-stu-id="3c862-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="3c862-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="3c862-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-492">Cost object</span></span></th>
<th><span data-ttu-id="3c862-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-494">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-494">CC003</span></span></td>
<td><span data-ttu-id="3c862-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-495">Assembly</span></span></td>
<td><span data-ttu-id="3c862-496">65</span><span class="sxs-lookup"><span data-stu-id="3c862-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-497">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-497">CC004</span></span></td>
<td><span data-ttu-id="3c862-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-498">Packaging</span></span></td>
<td><span data-ttu-id="3c862-499">35</span><span class="sxs-lookup"><span data-stu-id="3c862-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="3c862-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="3c862-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-502">Cost object</span></span></th>
<th><span data-ttu-id="3c862-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="3c862-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-504">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-505">Product 1</span></span></td>
<td><span data-ttu-id="3c862-506">60</span><span class="sxs-lookup"><span data-stu-id="3c862-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-507">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-508">Product 2</span></span></td>
<td><span data-ttu-id="3c862-509">20</span><span class="sxs-lookup"><span data-stu-id="3c862-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="3c862-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="3c862-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-512">Cost object</span></span></th>
<th><span data-ttu-id="3c862-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="3c862-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-514">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-515">Product 1</span></span></td>
<td><span data-ttu-id="3c862-516">80</span><span class="sxs-lookup"><span data-stu-id="3c862-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-517">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-518">Product 2</span></span></td>
<td><span data-ttu-id="3c862-519">15</span><span class="sxs-lookup"><span data-stu-id="3c862-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3c862-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="3c862-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="3c862-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="3c862-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="3c862-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="3c862-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-523">Cost object</span></span></th>
<th><span data-ttu-id="3c862-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-524">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-525">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-526">Amount</span></span></th>
<th><span data-ttu-id="3c862-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-528">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-528">CC002</span></span></td>
<td><span data-ttu-id="3c862-529">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-529">Finance</span></span></td>
<td><span data-ttu-id="3c862-530">35</span><span class="sxs-lookup"><span data-stu-id="3c862-530">35</span></span></td>
<td><span data-ttu-id="3c862-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3c862-532">175.00</span><span class="sxs-lookup"><span data-stu-id="3c862-532">175.00</span></span></td>
<td><span data-ttu-id="3c862-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-534">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-534">CC003</span></span></td>
<td><span data-ttu-id="3c862-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-535">Assembly</span></span></td>
<td><span data-ttu-id="3c862-536">55</span><span class="sxs-lookup"><span data-stu-id="3c862-536">55</span></span></td>
<td><span data-ttu-id="3c862-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3c862-538">275.00</span><span class="sxs-lookup"><span data-stu-id="3c862-538">275.00</span></span></td>
<td><span data-ttu-id="3c862-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-540">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-540">CC004</span></span></td>
<td><span data-ttu-id="3c862-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-541">Packaging</span></span></td>
<td><span data-ttu-id="3c862-542">10</span><span class="sxs-lookup"><span data-stu-id="3c862-542">10</span></span></td>
<td><span data-ttu-id="3c862-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3c862-544">50.00</span><span class="sxs-lookup"><span data-stu-id="3c862-544">50.00</span></span></td>
<td><span data-ttu-id="3c862-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-546">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-546">CC002</span></span></td>
<td><span data-ttu-id="3c862-547">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-547">Finance</span></span></td>
<td><span data-ttu-id="3c862-548">35</span><span class="sxs-lookup"><span data-stu-id="3c862-548">35</span></span></td>
<td><span data-ttu-id="3c862-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="3c862-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3c862-550">436.00</span><span class="sxs-lookup"><span data-stu-id="3c862-550">436.00</span></span></td>
<td><span data-ttu-id="3c862-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-552">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-552">CC003</span></span></td>
<td><span data-ttu-id="3c862-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-553">Assembly</span></span></td>
<td><span data-ttu-id="3c862-554">55</span><span class="sxs-lookup"><span data-stu-id="3c862-554">55</span></span></td>
<td><span data-ttu-id="3c862-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="3c862-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3c862-556">685.14</span><span class="sxs-lookup"><span data-stu-id="3c862-556">685.14</span></span></td>
<td><span data-ttu-id="3c862-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-558">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-558">CC004</span></span></td>
<td><span data-ttu-id="3c862-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-559">Packaging</span></span></td>
<td><span data-ttu-id="3c862-560">10</span><span class="sxs-lookup"><span data-stu-id="3c862-560">10</span></span></td>
<td><span data-ttu-id="3c862-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="3c862-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3c862-562">124.57</span><span class="sxs-lookup"><span data-stu-id="3c862-562">124.57</span></span></td>
<td><span data-ttu-id="3c862-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="3c862-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-565">Cost object</span></span></th>
<th><span data-ttu-id="3c862-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-566">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-567">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-568">Amount</span></span></th>
<th><span data-ttu-id="3c862-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-570">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-570">CC003</span></span></td>
<td><span data-ttu-id="3c862-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-571">Assembly</span></span></td>
<td><span data-ttu-id="3c862-572">65</span><span class="sxs-lookup"><span data-stu-id="3c862-572">65</span></span></td>
<td><span data-ttu-id="3c862-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3c862-574">438.75</span><span class="sxs-lookup"><span data-stu-id="3c862-574">438.75</span></span></td>
<td><span data-ttu-id="3c862-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-576">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-576">CC004</span></span></td>
<td><span data-ttu-id="3c862-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-577">Packaging</span></span></td>
<td><span data-ttu-id="3c862-578">35</span><span class="sxs-lookup"><span data-stu-id="3c862-578">35</span></span></td>
<td><span data-ttu-id="3c862-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3c862-580">236.25</span><span class="sxs-lookup"><span data-stu-id="3c862-580">236.25</span></span></td>
<td><span data-ttu-id="3c862-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-582">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-582">CC003</span></span></td>
<td><span data-ttu-id="3c862-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-583">Assembly</span></span></td>
<td><span data-ttu-id="3c862-584">65</span><span class="sxs-lookup"><span data-stu-id="3c862-584">65</span></span></td>
<td><span data-ttu-id="3c862-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3c862-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3c862-586">5,297.69</span></span></td>
<td><span data-ttu-id="3c862-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-588">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-588">CC004</span></span></td>
<td><span data-ttu-id="3c862-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-589">Packaging</span></span></td>
<td><span data-ttu-id="3c862-590">35</span><span class="sxs-lookup"><span data-stu-id="3c862-590">35</span></span></td>
<td><span data-ttu-id="3c862-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="3c862-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3c862-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3c862-592">2,852.60</span></span></td>
<td><span data-ttu-id="3c862-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="3c862-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-595">Cost object</span></span></th>
<th><span data-ttu-id="3c862-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-596">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-597">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-598">Amount</span></span></th>
<th><span data-ttu-id="3c862-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-600">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-601">Product 1</span></span></td>
<td><span data-ttu-id="3c862-602">60</span><span class="sxs-lookup"><span data-stu-id="3c862-602">60</span></span></td>
<td><span data-ttu-id="3c862-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="3c862-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3c862-604">535.31</span><span class="sxs-lookup"><span data-stu-id="3c862-604">535.31</span></span></td>
<td><span data-ttu-id="3c862-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-606">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-607">Product 2</span></span></td>
<td><span data-ttu-id="3c862-608">20</span><span class="sxs-lookup"><span data-stu-id="3c862-608">20</span></span></td>
<td><span data-ttu-id="3c862-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="3c862-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3c862-610">178.44</span><span class="sxs-lookup"><span data-stu-id="3c862-610">178.44</span></span></td>
<td><span data-ttu-id="3c862-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-612">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-613">Product 1</span></span></td>
<td><span data-ttu-id="3c862-614">60</span><span class="sxs-lookup"><span data-stu-id="3c862-614">60</span></span></td>
<td><span data-ttu-id="3c862-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="3c862-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3c862-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3c862-616">4,487.12</span></span></td>
<td><span data-ttu-id="3c862-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-618">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-619">Product 2</span></span></td>
<td><span data-ttu-id="3c862-620">20</span><span class="sxs-lookup"><span data-stu-id="3c862-620">20</span></span></td>
<td><span data-ttu-id="3c862-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="3c862-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3c862-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3c862-622">1,495.71</span></span></td>
<td><span data-ttu-id="3c862-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c862-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="3c862-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-625">Cost object</span></span></th>
<th><span data-ttu-id="3c862-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="3c862-626">Magnitude</span></span></th>
<th><span data-ttu-id="3c862-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="3c862-627">Allocation factor</span></span></th>
<th><span data-ttu-id="3c862-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-628">Amount</span></span></th>
<th><span data-ttu-id="3c862-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-630">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-631">Product 1</span></span></td>
<td><span data-ttu-id="3c862-632">80</span><span class="sxs-lookup"><span data-stu-id="3c862-632">80</span></span></td>
<td><span data-ttu-id="3c862-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="3c862-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3c862-634">241.05</span><span class="sxs-lookup"><span data-stu-id="3c862-634">241.05</span></span></td>
<td><span data-ttu-id="3c862-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-636">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-637">Product 2</span></span></td>
<td><span data-ttu-id="3c862-638">15</span><span class="sxs-lookup"><span data-stu-id="3c862-638">15</span></span></td>
<td><span data-ttu-id="3c862-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="3c862-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3c862-640">45.20</span><span class="sxs-lookup"><span data-stu-id="3c862-640">45.20</span></span></td>
<td><span data-ttu-id="3c862-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-642">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-643">Product 1</span></span></td>
<td><span data-ttu-id="3c862-644">80</span><span class="sxs-lookup"><span data-stu-id="3c862-644">80</span></span></td>
<td><span data-ttu-id="3c862-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="3c862-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3c862-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3c862-646">2,507.09</span></span></td>
<td><span data-ttu-id="3c862-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-648">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-649">Product 2</span></span></td>
<td><span data-ttu-id="3c862-650">15</span><span class="sxs-lookup"><span data-stu-id="3c862-650">15</span></span></td>
<td><span data-ttu-id="3c862-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="3c862-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3c862-652">470.08</span><span class="sxs-lookup"><span data-stu-id="3c862-652">470.08</span></span></td>
<td><span data-ttu-id="3c862-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3c862-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="3c862-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="3c862-655">Journal</span></span></th>
<th><span data-ttu-id="3c862-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="3c862-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3c862-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="3c862-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3c862-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="3c862-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-659">00004</span><span class="sxs-lookup"><span data-stu-id="3c862-659">00004</span></span></td>
<td><span data-ttu-id="3c862-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="3c862-661">مالي</span><span class="sxs-lookup"><span data-stu-id="3c862-661">Fiscal</span></span></td>
<td><span data-ttu-id="3c862-662">2017</span><span class="sxs-lookup"><span data-stu-id="3c862-662">2017</span></span></td>
<td><span data-ttu-id="3c862-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-663">Period 1</span></span></td>
<td><span data-ttu-id="3c862-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="3c862-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="3c862-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="3c862-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3c862-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-668">Cost element</span></span></th>
<th><span data-ttu-id="3c862-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-669">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-672">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-672">CC001</span></span></td>
<td><span data-ttu-id="3c862-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-673">HR</span></span></td>
<td><span data-ttu-id="3c862-674">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-674">10001</span></span></td>
<td><span data-ttu-id="3c862-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-675">Electricity</span></span></td>
<td><span data-ttu-id="3c862-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-676">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-677">500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-679">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-679">CC001</span></span></td>
<td><span data-ttu-id="3c862-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-680">HR</span></span></td>
<td><span data-ttu-id="3c862-681">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-681">10001</span></span></td>
<td><span data-ttu-id="3c862-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-682">Electricity</span></span></td>
<td><span data-ttu-id="3c862-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-683">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="3c862-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-686">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-686">CC002</span></span></td>
<td><span data-ttu-id="3c862-687">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-687">Finance</span></span></td>
<td><span data-ttu-id="3c862-688">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-688">10001</span></span></td>
<td><span data-ttu-id="3c862-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-689">Electricity</span></span></td>
<td><span data-ttu-id="3c862-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-690">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-691">675.00</span><span class="sxs-lookup"><span data-stu-id="3c862-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-693">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-693">CC002</span></span></td>
<td><span data-ttu-id="3c862-694">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-694">Finance</span></span></td>
<td><span data-ttu-id="3c862-695">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-695">10001</span></span></td>
<td><span data-ttu-id="3c862-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-696">Electricity</span></span></td>
<td><span data-ttu-id="3c862-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-697">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="3c862-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-700">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-700">CC003</span></span></td>
<td><span data-ttu-id="3c862-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-701">Assembly</span></span></td>
<td><span data-ttu-id="3c862-702">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-702">10001</span></span></td>
<td><span data-ttu-id="3c862-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-703">Electricity</span></span></td>
<td><span data-ttu-id="3c862-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-704">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-705">713.75</span><span class="sxs-lookup"><span data-stu-id="3c862-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-707">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-707">CC003</span></span></td>
<td><span data-ttu-id="3c862-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-708">Assembly</span></span></td>
<td><span data-ttu-id="3c862-709">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-709">10001</span></span></td>
<td><span data-ttu-id="3c862-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-710">Electricity</span></span></td>
<td><span data-ttu-id="3c862-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-711">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="3c862-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-714">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-714">CC003</span></span></td>
<td><span data-ttu-id="3c862-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-715">Packaging</span></span></td>
<td><span data-ttu-id="3c862-716">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-716">10001</span></span></td>
<td><span data-ttu-id="3c862-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-717">Electricity</span></span></td>
<td><span data-ttu-id="3c862-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-718">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-719">286.25</span><span class="sxs-lookup"><span data-stu-id="3c862-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-721">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-721">CC003</span></span></td>
<td><span data-ttu-id="3c862-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-722">Packaging</span></span></td>
<td><span data-ttu-id="3c862-723">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-723">10001</span></span></td>
<td><span data-ttu-id="3c862-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-724">Electricity</span></span></td>
<td><span data-ttu-id="3c862-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-725">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="3c862-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-728">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-729">Product 1</span></span></td>
<td><span data-ttu-id="3c862-730">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-730">10001</span></span></td>
<td><span data-ttu-id="3c862-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-731">Electricity</span></span></td>
<td><span data-ttu-id="3c862-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-732">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-733">776.36</span><span class="sxs-lookup"><span data-stu-id="3c862-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-735">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-736">Product 1</span></span></td>
<td><span data-ttu-id="3c862-737">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-737">10001</span></span></td>
<td><span data-ttu-id="3c862-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-738">Electricity</span></span></td>
<td><span data-ttu-id="3c862-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-739">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3c862-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-742">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-743">Product 1</span></span></td>
<td><span data-ttu-id="3c862-744">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-744">10001</span></span></td>
<td><span data-ttu-id="3c862-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-745">Electricity</span></span></td>
<td><span data-ttu-id="3c862-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-746">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-747">223.64</span><span class="sxs-lookup"><span data-stu-id="3c862-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="3c862-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-749">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-750">Product 1</span></span></td>
<td><span data-ttu-id="3c862-751">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-751">10001</span></span></td>
<td><span data-ttu-id="3c862-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-752">Electricity</span></span></td>
<td><span data-ttu-id="3c862-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-753">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3c862-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3c862-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3c862-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3c862-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-757">Cost element</span></span></th>
<th><span data-ttu-id="3c862-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-758">Cost behavior</span></span></th>
<th><span data-ttu-id="3c862-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3c862-759">Amount</span></span></th>
<th><span data-ttu-id="3c862-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="3c862-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c862-761">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-761">CC001</span></span></td>
<td><span data-ttu-id="3c862-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-762">HR</span></span></td>
<td><span data-ttu-id="3c862-763">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-763">10001</span></span></td>
<td><span data-ttu-id="3c862-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-764">Electricity</span></span></td>
<td><span data-ttu-id="3c862-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-765">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="3c862-766">-500.00</span></span></td>
<td><span data-ttu-id="3c862-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-768">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-768">CC002</span></span></td>
<td><span data-ttu-id="3c862-769">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-769">Finance</span></span></td>
<td><span data-ttu-id="3c862-770">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-770">10001</span></span></td>
<td><span data-ttu-id="3c862-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-771">Electricity</span></span></td>
<td><span data-ttu-id="3c862-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-772">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-773">175.00</span><span class="sxs-lookup"><span data-stu-id="3c862-773">175.00</span></span></td>
<td><span data-ttu-id="3c862-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-775">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-775">CC003</span></span></td>
<td><span data-ttu-id="3c862-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-776">Assembly</span></span></td>
<td><span data-ttu-id="3c862-777">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-777">10001</span></span></td>
<td><span data-ttu-id="3c862-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-778">Electricity</span></span></td>
<td><span data-ttu-id="3c862-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-779">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-780">275.00</span><span class="sxs-lookup"><span data-stu-id="3c862-780">275.00</span></span></td>
<td><span data-ttu-id="3c862-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-782">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-782">CC004</span></span></td>
<td><span data-ttu-id="3c862-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-783">Packaging</span></span></td>
<td><span data-ttu-id="3c862-784">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-784">10001</span></span></td>
<td><span data-ttu-id="3c862-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-785">Electricity</span></span></td>
<td><span data-ttu-id="3c862-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-786">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-787">50,00</span><span class="sxs-lookup"><span data-stu-id="3c862-787">50,00</span></span></td>
<td><span data-ttu-id="3c862-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-789">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-789">CC001</span></span></td>
<td><span data-ttu-id="3c862-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3c862-790">HR</span></span></td>
<td><span data-ttu-id="3c862-791">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-791">10001</span></span></td>
<td><span data-ttu-id="3c862-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-792">Electricity</span></span></td>
<td><span data-ttu-id="3c862-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-793">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="3c862-794">-1,245.71</span></span></td>
<td><span data-ttu-id="3c862-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-796">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-796">CC002</span></span></td>
<td><span data-ttu-id="3c862-797">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-797">Finance</span></span></td>
<td><span data-ttu-id="3c862-798">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-798">10001</span></span></td>
<td><span data-ttu-id="3c862-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-799">Electricity</span></span></td>
<td><span data-ttu-id="3c862-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-800">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-801">436.00</span><span class="sxs-lookup"><span data-stu-id="3c862-801">436.00</span></span></td>
<td><span data-ttu-id="3c862-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-803">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-803">CC003</span></span></td>
<td><span data-ttu-id="3c862-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-804">Assembly</span></span></td>
<td><span data-ttu-id="3c862-805">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-805">10001</span></span></td>
<td><span data-ttu-id="3c862-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-806">Electricity</span></span></td>
<td><span data-ttu-id="3c862-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-807">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-808">685.14</span><span class="sxs-lookup"><span data-stu-id="3c862-808">685.14</span></span></td>
<td><span data-ttu-id="3c862-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-810">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-810">CC004</span></span></td>
<td><span data-ttu-id="3c862-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-811">Packaging</span></span></td>
<td><span data-ttu-id="3c862-812">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-812">10001</span></span></td>
<td><span data-ttu-id="3c862-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-813">Electricity</span></span></td>
<td><span data-ttu-id="3c862-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-814">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-815">124.57</span><span class="sxs-lookup"><span data-stu-id="3c862-815">124.57</span></span></td>
<td><span data-ttu-id="3c862-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-817">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-817">CC002</span></span></td>
<td><span data-ttu-id="3c862-818">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-818">Finance</span></span></td>
<td><span data-ttu-id="3c862-819">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-819">10001</span></span></td>
<td><span data-ttu-id="3c862-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-820">Electricity</span></span></td>
<td><span data-ttu-id="3c862-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-821">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="3c862-822">-675.00</span></span></td>
<td><span data-ttu-id="3c862-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-824">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-824">CC003</span></span></td>
<td><span data-ttu-id="3c862-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-825">Assembly</span></span></td>
<td><span data-ttu-id="3c862-826">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-826">10001</span></span></td>
<td><span data-ttu-id="3c862-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-827">Electricity</span></span></td>
<td><span data-ttu-id="3c862-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-828">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-829">438.75</span><span class="sxs-lookup"><span data-stu-id="3c862-829">438.75</span></span></td>
<td><span data-ttu-id="3c862-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-831">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-831">CC004</span></span></td>
<td><span data-ttu-id="3c862-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-832">Packaging</span></span></td>
<td><span data-ttu-id="3c862-833">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-833">10001</span></span></td>
<td><span data-ttu-id="3c862-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-834">Electricity</span></span></td>
<td><span data-ttu-id="3c862-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-835">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-836">236.25</span><span class="sxs-lookup"><span data-stu-id="3c862-836">236.25</span></span></td>
<td><span data-ttu-id="3c862-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-838">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-838">CC002</span></span></td>
<td><span data-ttu-id="3c862-839">المالية</span><span class="sxs-lookup"><span data-stu-id="3c862-839">Finance</span></span></td>
<td><span data-ttu-id="3c862-840">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-840">10001</span></span></td>
<td><span data-ttu-id="3c862-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-841">Electricity</span></span></td>
<td><span data-ttu-id="3c862-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-842">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="3c862-843">-8,150.29</span></span></td>
<td><span data-ttu-id="3c862-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-845">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-845">CC003</span></span></td>
<td><span data-ttu-id="3c862-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-846">Assembly</span></span></td>
<td><span data-ttu-id="3c862-847">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-847">10001</span></span></td>
<td><span data-ttu-id="3c862-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-848">Electricity</span></span></td>
<td><span data-ttu-id="3c862-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-849">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3c862-850">5,297.69</span></span></td>
<td><span data-ttu-id="3c862-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-852">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-852">CC004</span></span></td>
<td><span data-ttu-id="3c862-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="3c862-853">Packaging</span></span></td>
<td><span data-ttu-id="3c862-854">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-854">10001</span></span></td>
<td><span data-ttu-id="3c862-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-855">Electricity</span></span></td>
<td><span data-ttu-id="3c862-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-856">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3c862-857">2,852.60</span></span></td>
<td><span data-ttu-id="3c862-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-859">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-859">CC003</span></span></td>
<td><span data-ttu-id="3c862-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-860">Assembly</span></span></td>
<td><span data-ttu-id="3c862-861">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-861">10001</span></span></td>
<td><span data-ttu-id="3c862-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-862">Electricity</span></span></td>
<td><span data-ttu-id="3c862-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-863">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="3c862-864">-713.75</span></span></td>
<td><span data-ttu-id="3c862-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-866">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-867">Product 1</span></span></td>
<td><span data-ttu-id="3c862-868">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-868">10001</span></span></td>
<td><span data-ttu-id="3c862-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-869">Electricity</span></span></td>
<td><span data-ttu-id="3c862-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-870">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-871">535.31</span><span class="sxs-lookup"><span data-stu-id="3c862-871">535.31</span></span></td>
<td><span data-ttu-id="3c862-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-873">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-874">Product 2</span></span></td>
<td><span data-ttu-id="3c862-875">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-875">10001</span></span></td>
<td><span data-ttu-id="3c862-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-876">Electricity</span></span></td>
<td><span data-ttu-id="3c862-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-877">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-878">178.44</span><span class="sxs-lookup"><span data-stu-id="3c862-878">178.44</span></span></td>
<td><span data-ttu-id="3c862-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-880">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-880">CC003</span></span></td>
<td><span data-ttu-id="3c862-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-881">Assembly</span></span></td>
<td><span data-ttu-id="3c862-882">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-882">10001</span></span></td>
<td><span data-ttu-id="3c862-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-883">Electricity</span></span></td>
<td><span data-ttu-id="3c862-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-884">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="3c862-885">-5,982.83</span></span></td>
<td><span data-ttu-id="3c862-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-887">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-888">Product 1</span></span></td>
<td><span data-ttu-id="3c862-889">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-889">10001</span></span></td>
<td><span data-ttu-id="3c862-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-890">Electricity</span></span></td>
<td><span data-ttu-id="3c862-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-891">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3c862-892">4,487.12</span></span></td>
<td><span data-ttu-id="3c862-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-894">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-895">Product 2</span></span></td>
<td><span data-ttu-id="3c862-896">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-896">10001</span></span></td>
<td><span data-ttu-id="3c862-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-897">Electricity</span></span></td>
<td><span data-ttu-id="3c862-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-898">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3c862-899">1,495.71</span></span></td>
<td><span data-ttu-id="3c862-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-901">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-901">CC003</span></span></td>
<td><span data-ttu-id="3c862-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-902">Assembly</span></span></td>
<td><span data-ttu-id="3c862-903">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-903">10001</span></span></td>
<td><span data-ttu-id="3c862-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-904">Electricity</span></span></td>
<td><span data-ttu-id="3c862-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-905">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="3c862-906">-286.25</span></span></td>
<td><span data-ttu-id="3c862-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-908">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-909">Product 1</span></span></td>
<td><span data-ttu-id="3c862-910">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-910">10001</span></span></td>
<td><span data-ttu-id="3c862-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-911">Electricity</span></span></td>
<td><span data-ttu-id="3c862-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-912">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-913">241.05</span><span class="sxs-lookup"><span data-stu-id="3c862-913">241.05</span></span></td>
<td><span data-ttu-id="3c862-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-915">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-916">Product 2</span></span></td>
<td><span data-ttu-id="3c862-917">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-917">10001</span></span></td>
<td><span data-ttu-id="3c862-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-918">Electricity</span></span></td>
<td><span data-ttu-id="3c862-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-919">Fixed cost</span></span></td>
<td><span data-ttu-id="3c862-920">45.20</span><span class="sxs-lookup"><span data-stu-id="3c862-920">45.20</span></span></td>
<td><span data-ttu-id="3c862-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-922">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-922">CC003</span></span></td>
<td><span data-ttu-id="3c862-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="3c862-923">Assembly</span></span></td>
<td><span data-ttu-id="3c862-924">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-924">10001</span></span></td>
<td><span data-ttu-id="3c862-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-925">Electricity</span></span></td>
<td><span data-ttu-id="3c862-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-926">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="3c862-927">-2,977.17</span></span></td>
<td><span data-ttu-id="3c862-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-929">Prod 1</span></span></td>
<td><span data-ttu-id="3c862-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-930">Product 1</span></span></td>
<td><span data-ttu-id="3c862-931">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-931">10001</span></span></td>
<td><span data-ttu-id="3c862-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-932">Electricity</span></span></td>
<td><span data-ttu-id="3c862-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-933">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3c862-934">2,507.09</span></span></td>
<td><span data-ttu-id="3c862-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c862-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-936">Prod 2</span></span></td>
<td><span data-ttu-id="3c862-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-937">Product 2</span></span></td>
<td><span data-ttu-id="3c862-938">10001</span><span class="sxs-lookup"><span data-stu-id="3c862-938">10001</span></span></td>
<td><span data-ttu-id="3c862-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-939">Electricity</span></span></td>
<td><span data-ttu-id="3c862-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-940">Variable cost</span></span></td>
<td><span data-ttu-id="3c862-941">470.08</span><span class="sxs-lookup"><span data-stu-id="3c862-941">470.08</span></span></td>
<td><span data-ttu-id="3c862-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="3c862-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="3c862-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="3c862-943">Conclusion</span></span>
<span data-ttu-id="3c862-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="3c862-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="3c862-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="3c862-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="3c862-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="3c862-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c862-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="3c862-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="3c862-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3c862-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="3c862-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="3c862-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3c862-951">CC099</span><span class="sxs-lookup"><span data-stu-id="3c862-951">CC099</span></span></th>
<th><span data-ttu-id="3c862-952">CC001</span><span class="sxs-lookup"><span data-stu-id="3c862-952">CC001</span></span></th>
<th><span data-ttu-id="3c862-953">CC002</span><span class="sxs-lookup"><span data-stu-id="3c862-953">CC002</span></span></th>
<th><span data-ttu-id="3c862-954">CC003</span><span class="sxs-lookup"><span data-stu-id="3c862-954">CC003</span></span></th>
<th><span data-ttu-id="3c862-955">CC004</span><span class="sxs-lookup"><span data-stu-id="3c862-955">CC004</span></span></th>
<th><span data-ttu-id="3c862-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="3c862-956">Proj 1</span></span></th>
<th><span data-ttu-id="3c862-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="3c862-957">Proj 2</span></span></th>
<th><span data-ttu-id="3c862-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="3c862-958">Prod 1</span></span></th>
<th><span data-ttu-id="3c862-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="3c862-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="3c862-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="3c862-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3c862-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="3c862-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="3c862-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-971">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="3c862-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3c862-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-973">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-974">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-975">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-976">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-977">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3c862-978">776.36</span><span class="sxs-lookup"><span data-stu-id="3c862-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-979">223.64</span><span class="sxs-lookup"><span data-stu-id="3c862-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="3c862-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="3c862-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-982">000</span><span class="sxs-lookup"><span data-stu-id="3c862-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-983">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-984">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-985">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-986">0.00</span><span class="sxs-lookup"><span data-stu-id="3c862-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-987">30.00</span><span class="sxs-lookup"><span data-stu-id="3c862-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-988">10.00</span><span class="sxs-lookup"><span data-stu-id="3c862-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3c862-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3c862-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3c862-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c862-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3c862-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="3c862-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="3c862-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="3c862-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="3c862-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3c862-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="3c862-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="3c862-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]