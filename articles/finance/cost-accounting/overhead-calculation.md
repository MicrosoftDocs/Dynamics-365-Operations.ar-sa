---
title: عملية حساب المصروفات الزائدة
description: يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440058"
---
# <a name="overhead-calculation"></a><span data-ttu-id="b661c-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="b661c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b661c-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="b661c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b661c-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="b661c-105">Term definition</span></span>
---------------

<span data-ttu-id="b661c-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="b661c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b661c-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="b661c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b661c-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="b661c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b661c-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="b661c-109">Rent</span></span>
-   <span data-ttu-id="b661c-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-110">Electricity</span></span>
-   <span data-ttu-id="b661c-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="b661c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b661c-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="b661c-112">Overhead calculation overview</span></span>
<span data-ttu-id="b661c-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="b661c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b661c-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="b661c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b661c-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b661c-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="b661c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b661c-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="b661c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b661c-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="b661c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b661c-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="b661c-119">Version type</span></span>
-   <span data-ttu-id="b661c-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="b661c-120">Date and time</span></span>
-   <span data-ttu-id="b661c-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="b661c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b661c-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-122">Fiscal year</span></span>
-   <span data-ttu-id="b661c-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-123">Fiscal period</span></span>

<span data-ttu-id="b661c-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="b661c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b661c-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="b661c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b661c-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="b661c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b661c-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="b661c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b661c-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="b661c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b661c-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="b661c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b661c-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="b661c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b661c-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b661c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b661c-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="b661c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b661c-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="b661c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b661c-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b661c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b661c-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="b661c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b661c-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="b661c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b661c-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b661c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="b661c-140">Main account</span></span></th>
<th><span data-ttu-id="b661c-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="b661c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b661c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-143">CC099</span></span></td>
<td><span data-ttu-id="b661c-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-144">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-145">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-145">10001</span></span></td>
<td><span data-ttu-id="b661c-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-146">Electricity</span></span></td>
<td><span data-ttu-id="b661c-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b661c-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b661c-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b661c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b661c-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="b661c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b661c-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b661c-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="b661c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b661c-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="b661c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b661c-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="b661c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b661c-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="b661c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b661c-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b661c-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="b661c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b661c-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="b661c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b661c-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-160">Journal</span></span></th>
<th><span data-ttu-id="b661c-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="b661c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b661c-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="b661c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b661c-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="b661c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-164">00001</span><span class="sxs-lookup"><span data-stu-id="b661c-164">00001</span></span></td>
<td><span data-ttu-id="b661c-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b661c-166">مالي</span><span class="sxs-lookup"><span data-stu-id="b661c-166">Fiscal</span></span></td>
<td><span data-ttu-id="b661c-167">2017</span><span class="sxs-lookup"><span data-stu-id="b661c-167">2017</span></span></td>
<td><span data-ttu-id="b661c-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-168">Period 1</span></span></td>
<td><span data-ttu-id="b661c-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b661c-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="b661c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-173">Cost element</span></span></th>
<th><span data-ttu-id="b661c-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b661c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-177">CC099</span></span></td>
<td><span data-ttu-id="b661c-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-178">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-179">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-179">10001</span></span></td>
<td><span data-ttu-id="b661c-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-180">Electricity</span></span></td>
<td><span data-ttu-id="b661c-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="b661c-181">Unclassified</span></span></td>
<td><span data-ttu-id="b661c-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b661c-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-185">Cost element</span></span></th>
<th><span data-ttu-id="b661c-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-187">Amount</span></span></th>
<th><span data-ttu-id="b661c-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-189">CC099</span></span></td>
<td><span data-ttu-id="b661c-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-190">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-191">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-191">10001</span></span></td>
<td><span data-ttu-id="b661c-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-192">Electricity</span></span></td>
<td><span data-ttu-id="b661c-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="b661c-193">Unclassified</span></span></td>
<td><span data-ttu-id="b661c-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-194">10,000.00</span></span></td>
<td><span data-ttu-id="b661c-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-196">CC099</span></span></td>
<td><span data-ttu-id="b661c-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-197">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-198">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-198">10001</span></span></td>
<td><span data-ttu-id="b661c-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-199">Electricity</span></span></td>
<td><span data-ttu-id="b661c-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="b661c-200">Unclassified</span></span></td>
<td><span data-ttu-id="b661c-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b661c-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-203">CC099</span></span></td>
<td><span data-ttu-id="b661c-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-204">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-205">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-205">10001</span></span></td>
<td><span data-ttu-id="b661c-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-206">Electricity</span></span></td>
<td><span data-ttu-id="b661c-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-208">1,000.00</span></span></td>
<td><span data-ttu-id="b661c-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-210">CC099</span></span></td>
<td><span data-ttu-id="b661c-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-211">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-212">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-212">10001</span></span></td>
<td><span data-ttu-id="b661c-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-213">Electricity</span></span></td>
<td><span data-ttu-id="b661c-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-214">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-215">9,000.00</span></span></td>
<td><span data-ttu-id="b661c-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="b661c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b661c-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b661c-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="b661c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b661c-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="b661c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b661c-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="b661c-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="b661c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b661c-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="b661c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b661c-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="b661c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b661c-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="b661c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b661c-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="b661c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b661c-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="b661c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-228">Cost object</span></span></th>
<th><span data-ttu-id="b661c-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="b661c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-230">CC001</span></span></td>
<td><span data-ttu-id="b661c-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-231">HR</span></span></td>
<td><span data-ttu-id="b661c-232">1,000</span><span class="sxs-lookup"><span data-stu-id="b661c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-233">CC002</span></span></td>
<td><span data-ttu-id="b661c-234">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-234">Finance</span></span></td>
<td><span data-ttu-id="b661c-235">6,000</span><span class="sxs-lookup"><span data-stu-id="b661c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-236">CC003</span></span></td>
<td><span data-ttu-id="b661c-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-237">Assembly</span></span></td>
<td><span data-ttu-id="b661c-238">0</span><span class="sxs-lookup"><span data-stu-id="b661c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="b661c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-240">Cost object</span></span></th>
<th><span data-ttu-id="b661c-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-241">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-244">CC001</span></span></td>
<td><span data-ttu-id="b661c-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-245">HR</span></span></td>
<td><span data-ttu-id="b661c-246">1,000</span><span class="sxs-lookup"><span data-stu-id="b661c-246">1,000</span></span></td>
<td><span data-ttu-id="b661c-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b661c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b661c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-249">CC002</span></span></td>
<td><span data-ttu-id="b661c-250">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-250">Finance</span></span></td>
<td><span data-ttu-id="b661c-251">6,000</span><span class="sxs-lookup"><span data-stu-id="b661c-251">6,000</span></span></td>
<td><span data-ttu-id="b661c-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b661c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b661c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-254">CC003</span></span></td>
<td><span data-ttu-id="b661c-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-255">Assembly</span></span></td>
<td><span data-ttu-id="b661c-256">0</span><span class="sxs-lookup"><span data-stu-id="b661c-256">0</span></span></td>
<td><span data-ttu-id="b661c-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b661c-258">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="b661c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b661c-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="b661c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-261">Cost object</span></span></th>
<th><span data-ttu-id="b661c-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="b661c-262">Formula</span></span></th>
<th><span data-ttu-id="b661c-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-263">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-266">CC001</span></span></td>
<td><span data-ttu-id="b661c-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-267">HR</span></span></td>
<td><span data-ttu-id="b661c-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b661c-269">1</span><span class="sxs-lookup"><span data-stu-id="b661c-269">1</span></span></td>
<td><span data-ttu-id="b661c-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b661c-271">500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-272">CC002</span></span></td>
<td><span data-ttu-id="b661c-273">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-273">Finance</span></span></td>
<td><span data-ttu-id="b661c-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b661c-275">1</span><span class="sxs-lookup"><span data-stu-id="b661c-275">1</span></span></td>
<td><span data-ttu-id="b661c-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b661c-277">500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-278">CC003</span></span></td>
<td><span data-ttu-id="b661c-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-279">Assembly</span></span></td>
<td><span data-ttu-id="b661c-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b661c-281">0</span><span class="sxs-lookup"><span data-stu-id="b661c-281">0</span></span></td>
<td><span data-ttu-id="b661c-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b661c-283">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b661c-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-285">Journal</span></span></th>
<th><span data-ttu-id="b661c-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="b661c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b661c-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="b661c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b661c-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="b661c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-289">00002</span><span class="sxs-lookup"><span data-stu-id="b661c-289">00002</span></span></td>
<td><span data-ttu-id="b661c-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b661c-291">مالي</span><span class="sxs-lookup"><span data-stu-id="b661c-291">Fiscal</span></span></td>
<td><span data-ttu-id="b661c-292">2017</span><span class="sxs-lookup"><span data-stu-id="b661c-292">2017</span></span></td>
<td><span data-ttu-id="b661c-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-293">Period 1</span></span></td>
<td><span data-ttu-id="b661c-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b661c-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="b661c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-298">Cost element</span></span></th>
<th><span data-ttu-id="b661c-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-302">CC099</span></span></td>
<td><span data-ttu-id="b661c-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-303">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-304">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-304">10001</span></span></td>
<td><span data-ttu-id="b661c-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-305">Electricity</span></span></td>
<td><span data-ttu-id="b661c-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-309">CC099</span></span></td>
<td><span data-ttu-id="b661c-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-310">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-311">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-311">10001</span></span></td>
<td><span data-ttu-id="b661c-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-312">Electricity</span></span></td>
<td><span data-ttu-id="b661c-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-313">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b661c-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-317">Cost element</span></span></th>
<th><span data-ttu-id="b661c-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-319">Amount</span></span></th>
<th><span data-ttu-id="b661c-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-321">CC099</span></span></td>
<td><span data-ttu-id="b661c-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-322">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-323">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-323">10001</span></span></td>
<td><span data-ttu-id="b661c-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-324">Electricity</span></span></td>
<td><span data-ttu-id="b661c-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="b661c-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-328">CC001</span></span></td>
<td><span data-ttu-id="b661c-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-329">HR</span></span></td>
<td><span data-ttu-id="b661c-330">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-330">10001</span></span></td>
<td><span data-ttu-id="b661c-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-331">Electricity</span></span></td>
<td><span data-ttu-id="b661c-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-333">500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-333">500.00</span></span></td>
<td><span data-ttu-id="b661c-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-335">CC002</span></span></td>
<td><span data-ttu-id="b661c-336">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-336">Finance</span></span></td>
<td><span data-ttu-id="b661c-337">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-337">10001</span></span></td>
<td><span data-ttu-id="b661c-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-338">Electricity</span></span></td>
<td><span data-ttu-id="b661c-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-340">500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-340">500.00</span></span></td>
<td><span data-ttu-id="b661c-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-342">CC099</span></span></td>
<td><span data-ttu-id="b661c-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b661c-343">Default cost center</span></span></td>
<td><span data-ttu-id="b661c-344">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-344">10001</span></span></td>
<td><span data-ttu-id="b661c-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-345">Electricity</span></span></td>
<td><span data-ttu-id="b661c-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-346">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="b661c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="b661c-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-349">CC001</span></span></td>
<td><span data-ttu-id="b661c-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-350">HR</span></span></td>
<td><span data-ttu-id="b661c-351">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-351">10001</span></span></td>
<td><span data-ttu-id="b661c-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-352">Electricity</span></span></td>
<td><span data-ttu-id="b661c-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-353">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b661c-354">1,285.71</span></span></td>
<td><span data-ttu-id="b661c-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-356">CC002</span></span></td>
<td><span data-ttu-id="b661c-357">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-357">Finance</span></span></td>
<td><span data-ttu-id="b661c-358">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-358">10001</span></span></td>
<td><span data-ttu-id="b661c-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-359">Electricity</span></span></td>
<td><span data-ttu-id="b661c-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-360">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b661c-361">7,714.29</span></span></td>
<td><span data-ttu-id="b661c-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="b661c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b661c-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="b661c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b661c-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="b661c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b661c-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="b661c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b661c-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="b661c-367">Define the overhead rate</span></span>

<span data-ttu-id="b661c-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="b661c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b661c-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="b661c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-370">Cost object</span></span></th>
<th><span data-ttu-id="b661c-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="b661c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-372">Proj 1</span></span></td>
<td><span data-ttu-id="b661c-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-373">Project 1</span></span></td>
<td><span data-ttu-id="b661c-374">3</span><span class="sxs-lookup"><span data-stu-id="b661c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-375">Proj 2</span></span></td>
<td><span data-ttu-id="b661c-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-376">Project 2</span></span></td>
<td><span data-ttu-id="b661c-377">1</span><span class="sxs-lookup"><span data-stu-id="b661c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-379">Cost object</span></span></th>
<th><span data-ttu-id="b661c-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-380">Cost element</span></span></th>
<th><span data-ttu-id="b661c-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="b661c-382">Units</span></span></th>
<th><span data-ttu-id="b661c-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="b661c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-384">CC001</span></span></td>
<td><span data-ttu-id="b661c-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-385">HR</span></span></td>
<td><span data-ttu-id="b661c-386">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-386">10001</span></span></td>
<td><span data-ttu-id="b661c-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-387">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-388">1</span><span class="sxs-lookup"><span data-stu-id="b661c-388">1</span></span></td>
<td><span data-ttu-id="b661c-389">10</span><span class="sxs-lookup"><span data-stu-id="b661c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="b661c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-391">Cost object</span></span></th>
<th><span data-ttu-id="b661c-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-392">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-393">Cost element</span></span></th>
<th><span data-ttu-id="b661c-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-396">Proj 1</span></span></td>
<td><span data-ttu-id="b661c-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-397">Project 1</span></span></td>
<td><span data-ttu-id="b661c-398">3</span><span class="sxs-lookup"><span data-stu-id="b661c-398">3</span></span></td>
<td><span data-ttu-id="b661c-399">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-399">10001</span></span></td>
<td><span data-ttu-id="b661c-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="b661c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b661c-401">30.00</span><span class="sxs-lookup"><span data-stu-id="b661c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-402">Proj 2</span></span></td>
<td><span data-ttu-id="b661c-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-403">Project 2</span></span></td>
<td><span data-ttu-id="b661c-404">1</span><span class="sxs-lookup"><span data-stu-id="b661c-404">1</span></span></td>
<td><span data-ttu-id="b661c-405">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-405">10001</span></span></td>
<td><span data-ttu-id="b661c-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="b661c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b661c-407">10.00</span><span class="sxs-lookup"><span data-stu-id="b661c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b661c-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-409">Journal</span></span></th>
<th><span data-ttu-id="b661c-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="b661c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b661c-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="b661c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b661c-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="b661c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-413">00003</span><span class="sxs-lookup"><span data-stu-id="b661c-413">00003</span></span></td>
<td><span data-ttu-id="b661c-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="b661c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b661c-415">مالي</span><span class="sxs-lookup"><span data-stu-id="b661c-415">Fiscal</span></span></td>
<td><span data-ttu-id="b661c-416">2017</span><span class="sxs-lookup"><span data-stu-id="b661c-416">2017</span></span></td>
<td><span data-ttu-id="b661c-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-417">Period 1</span></span></td>
<td><span data-ttu-id="b661c-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b661c-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="b661c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-421">Cost object</span></span></th>
<th><span data-ttu-id="b661c-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-424">Proj 1</span></span></td>
<td><span data-ttu-id="b661c-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="b661c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b661c-426">3.00</span><span class="sxs-lookup"><span data-stu-id="b661c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-428">Proj 2</span></span></td>
<td><span data-ttu-id="b661c-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="b661c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b661c-430">1.00</span><span class="sxs-lookup"><span data-stu-id="b661c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b661c-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-433">Cost element</span></span></th>
<th><span data-ttu-id="b661c-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-435">Amount</span></span></th>
<th><span data-ttu-id="b661c-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="b661c-437">CC0001</span></span></td>
<td><span data-ttu-id="b661c-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-438">HR</span></span></td>
<td><span data-ttu-id="b661c-439">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-439">10001</span></span></td>
<td><span data-ttu-id="b661c-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-440">Electricity</span></span></td>
<td><span data-ttu-id="b661c-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-441">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="b661c-442">-30.00</span></span></td>
<td><span data-ttu-id="b661c-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-444">Proj 1</span></span></td>
<td><span data-ttu-id="b661c-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="b661c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b661c-446">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-446">10001</span></span></td>
<td><span data-ttu-id="b661c-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-447">Electricity</span></span></td>
<td><span data-ttu-id="b661c-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-448">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-449">30.00</span><span class="sxs-lookup"><span data-stu-id="b661c-449">30.00</span></span></td>
<td><span data-ttu-id="b661c-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-451">CC001</span></span></td>
<td><span data-ttu-id="b661c-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-452">HR</span></span></td>
<td><span data-ttu-id="b661c-453">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-453">10001</span></span></td>
<td><span data-ttu-id="b661c-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-454">Electricity</span></span></td>
<td><span data-ttu-id="b661c-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-455">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="b661c-456">-10.00</span></span></td>
<td><span data-ttu-id="b661c-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-458">Proj 2</span></span></td>
<td><span data-ttu-id="b661c-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="b661c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b661c-460">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-460">10001</span></span></td>
<td><span data-ttu-id="b661c-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-461">Electricity</span></span></td>
<td><span data-ttu-id="b661c-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-462">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-463">10.00</span><span class="sxs-lookup"><span data-stu-id="b661c-463">10.00</span></span></td>
<td><span data-ttu-id="b661c-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="b661c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b661c-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b661c-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="b661c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b661c-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="b661c-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="b661c-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="b661c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b661c-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="b661c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b661c-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="b661c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b661c-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="b661c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b661c-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b661c-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b661c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b661c-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-475">Define the cost allocation</span></span>

<span data-ttu-id="b661c-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b661c-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b661c-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="b661c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-479">Cost object</span></span></th>
<th><span data-ttu-id="b661c-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-481">CC002</span></span></td>
<td><span data-ttu-id="b661c-482">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-482">Finance</span></span></td>
<td><span data-ttu-id="b661c-483">35</span><span class="sxs-lookup"><span data-stu-id="b661c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-484">CC003</span></span></td>
<td><span data-ttu-id="b661c-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-485">Assembly</span></span></td>
<td><span data-ttu-id="b661c-486">55</span><span class="sxs-lookup"><span data-stu-id="b661c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-487">CC004</span></span></td>
<td><span data-ttu-id="b661c-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-488">Packaging</span></span></td>
<td><span data-ttu-id="b661c-489">10</span><span class="sxs-lookup"><span data-stu-id="b661c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b661c-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="b661c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-492">Cost object</span></span></th>
<th><span data-ttu-id="b661c-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-494">CC003</span></span></td>
<td><span data-ttu-id="b661c-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-495">Assembly</span></span></td>
<td><span data-ttu-id="b661c-496">65</span><span class="sxs-lookup"><span data-stu-id="b661c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-497">CC004</span></span></td>
<td><span data-ttu-id="b661c-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-498">Packaging</span></span></td>
<td><span data-ttu-id="b661c-499">35</span><span class="sxs-lookup"><span data-stu-id="b661c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b661c-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="b661c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-502">Cost object</span></span></th>
<th><span data-ttu-id="b661c-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="b661c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-504">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-505">Product 1</span></span></td>
<td><span data-ttu-id="b661c-506">60</span><span class="sxs-lookup"><span data-stu-id="b661c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-507">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-508">Product 2</span></span></td>
<td><span data-ttu-id="b661c-509">20</span><span class="sxs-lookup"><span data-stu-id="b661c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b661c-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="b661c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-512">Cost object</span></span></th>
<th><span data-ttu-id="b661c-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="b661c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-514">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-515">Product 1</span></span></td>
<td><span data-ttu-id="b661c-516">80</span><span class="sxs-lookup"><span data-stu-id="b661c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-517">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-518">Product 2</span></span></td>
<td><span data-ttu-id="b661c-519">15</span><span class="sxs-lookup"><span data-stu-id="b661c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b661c-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="b661c-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b661c-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="b661c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="b661c-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="b661c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-523">Cost object</span></span></th>
<th><span data-ttu-id="b661c-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-524">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-526">Amount</span></span></th>
<th><span data-ttu-id="b661c-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-528">CC002</span></span></td>
<td><span data-ttu-id="b661c-529">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-529">Finance</span></span></td>
<td><span data-ttu-id="b661c-530">35</span><span class="sxs-lookup"><span data-stu-id="b661c-530">35</span></span></td>
<td><span data-ttu-id="b661c-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b661c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="b661c-532">175.00</span></span></td>
<td><span data-ttu-id="b661c-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-534">CC003</span></span></td>
<td><span data-ttu-id="b661c-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-535">Assembly</span></span></td>
<td><span data-ttu-id="b661c-536">55</span><span class="sxs-lookup"><span data-stu-id="b661c-536">55</span></span></td>
<td><span data-ttu-id="b661c-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b661c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="b661c-538">275.00</span></span></td>
<td><span data-ttu-id="b661c-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-540">CC004</span></span></td>
<td><span data-ttu-id="b661c-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-541">Packaging</span></span></td>
<td><span data-ttu-id="b661c-542">10</span><span class="sxs-lookup"><span data-stu-id="b661c-542">10</span></span></td>
<td><span data-ttu-id="b661c-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b661c-544">50.00</span><span class="sxs-lookup"><span data-stu-id="b661c-544">50.00</span></span></td>
<td><span data-ttu-id="b661c-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-546">CC002</span></span></td>
<td><span data-ttu-id="b661c-547">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-547">Finance</span></span></td>
<td><span data-ttu-id="b661c-548">35</span><span class="sxs-lookup"><span data-stu-id="b661c-548">35</span></span></td>
<td><span data-ttu-id="b661c-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="b661c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b661c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="b661c-550">436.00</span></span></td>
<td><span data-ttu-id="b661c-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-552">CC003</span></span></td>
<td><span data-ttu-id="b661c-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-553">Assembly</span></span></td>
<td><span data-ttu-id="b661c-554">55</span><span class="sxs-lookup"><span data-stu-id="b661c-554">55</span></span></td>
<td><span data-ttu-id="b661c-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="b661c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b661c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="b661c-556">685.14</span></span></td>
<td><span data-ttu-id="b661c-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-558">CC004</span></span></td>
<td><span data-ttu-id="b661c-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-559">Packaging</span></span></td>
<td><span data-ttu-id="b661c-560">10</span><span class="sxs-lookup"><span data-stu-id="b661c-560">10</span></span></td>
<td><span data-ttu-id="b661c-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="b661c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b661c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="b661c-562">124.57</span></span></td>
<td><span data-ttu-id="b661c-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="b661c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-565">Cost object</span></span></th>
<th><span data-ttu-id="b661c-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-566">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-568">Amount</span></span></th>
<th><span data-ttu-id="b661c-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-570">CC003</span></span></td>
<td><span data-ttu-id="b661c-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-571">Assembly</span></span></td>
<td><span data-ttu-id="b661c-572">65</span><span class="sxs-lookup"><span data-stu-id="b661c-572">65</span></span></td>
<td><span data-ttu-id="b661c-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b661c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="b661c-574">438.75</span></span></td>
<td><span data-ttu-id="b661c-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-576">CC004</span></span></td>
<td><span data-ttu-id="b661c-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-577">Packaging</span></span></td>
<td><span data-ttu-id="b661c-578">35</span><span class="sxs-lookup"><span data-stu-id="b661c-578">35</span></span></td>
<td><span data-ttu-id="b661c-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b661c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="b661c-580">236.25</span></span></td>
<td><span data-ttu-id="b661c-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-582">CC003</span></span></td>
<td><span data-ttu-id="b661c-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-583">Assembly</span></span></td>
<td><span data-ttu-id="b661c-584">65</span><span class="sxs-lookup"><span data-stu-id="b661c-584">65</span></span></td>
<td><span data-ttu-id="b661c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b661c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b661c-586">5,297.69</span></span></td>
<td><span data-ttu-id="b661c-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-588">CC004</span></span></td>
<td><span data-ttu-id="b661c-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-589">Packaging</span></span></td>
<td><span data-ttu-id="b661c-590">35</span><span class="sxs-lookup"><span data-stu-id="b661c-590">35</span></span></td>
<td><span data-ttu-id="b661c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="b661c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b661c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b661c-592">2,852.60</span></span></td>
<td><span data-ttu-id="b661c-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="b661c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-595">Cost object</span></span></th>
<th><span data-ttu-id="b661c-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-596">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-598">Amount</span></span></th>
<th><span data-ttu-id="b661c-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-600">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-601">Product 1</span></span></td>
<td><span data-ttu-id="b661c-602">60</span><span class="sxs-lookup"><span data-stu-id="b661c-602">60</span></span></td>
<td><span data-ttu-id="b661c-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="b661c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b661c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="b661c-604">535.31</span></span></td>
<td><span data-ttu-id="b661c-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-606">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-607">Product 2</span></span></td>
<td><span data-ttu-id="b661c-608">20</span><span class="sxs-lookup"><span data-stu-id="b661c-608">20</span></span></td>
<td><span data-ttu-id="b661c-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="b661c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b661c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="b661c-610">178.44</span></span></td>
<td><span data-ttu-id="b661c-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-612">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-613">Product 1</span></span></td>
<td><span data-ttu-id="b661c-614">60</span><span class="sxs-lookup"><span data-stu-id="b661c-614">60</span></span></td>
<td><span data-ttu-id="b661c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="b661c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b661c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b661c-616">4,487.12</span></span></td>
<td><span data-ttu-id="b661c-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-618">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-619">Product 2</span></span></td>
<td><span data-ttu-id="b661c-620">20</span><span class="sxs-lookup"><span data-stu-id="b661c-620">20</span></span></td>
<td><span data-ttu-id="b661c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="b661c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b661c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b661c-622">1,495.71</span></span></td>
<td><span data-ttu-id="b661c-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b661c-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="b661c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-625">Cost object</span></span></th>
<th><span data-ttu-id="b661c-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="b661c-626">Magnitude</span></span></th>
<th><span data-ttu-id="b661c-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="b661c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="b661c-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-628">Amount</span></span></th>
<th><span data-ttu-id="b661c-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-630">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-631">Product 1</span></span></td>
<td><span data-ttu-id="b661c-632">80</span><span class="sxs-lookup"><span data-stu-id="b661c-632">80</span></span></td>
<td><span data-ttu-id="b661c-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="b661c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b661c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="b661c-634">241.05</span></span></td>
<td><span data-ttu-id="b661c-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-636">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-637">Product 2</span></span></td>
<td><span data-ttu-id="b661c-638">15</span><span class="sxs-lookup"><span data-stu-id="b661c-638">15</span></span></td>
<td><span data-ttu-id="b661c-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="b661c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b661c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="b661c-640">45.20</span></span></td>
<td><span data-ttu-id="b661c-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-642">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-643">Product 1</span></span></td>
<td><span data-ttu-id="b661c-644">80</span><span class="sxs-lookup"><span data-stu-id="b661c-644">80</span></span></td>
<td><span data-ttu-id="b661c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="b661c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b661c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b661c-646">2,507.09</span></span></td>
<td><span data-ttu-id="b661c-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-648">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-649">Product 2</span></span></td>
<td><span data-ttu-id="b661c-650">15</span><span class="sxs-lookup"><span data-stu-id="b661c-650">15</span></span></td>
<td><span data-ttu-id="b661c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="b661c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b661c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="b661c-652">470.08</span></span></td>
<td><span data-ttu-id="b661c-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b661c-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="b661c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="b661c-655">Journal</span></span></th>
<th><span data-ttu-id="b661c-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="b661c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b661c-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="b661c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b661c-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="b661c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-659">00004</span><span class="sxs-lookup"><span data-stu-id="b661c-659">00004</span></span></td>
<td><span data-ttu-id="b661c-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b661c-661">مالي</span><span class="sxs-lookup"><span data-stu-id="b661c-661">Fiscal</span></span></td>
<td><span data-ttu-id="b661c-662">2017</span><span class="sxs-lookup"><span data-stu-id="b661c-662">2017</span></span></td>
<td><span data-ttu-id="b661c-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-663">Period 1</span></span></td>
<td><span data-ttu-id="b661c-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="b661c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b661c-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="b661c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b661c-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-668">Cost element</span></span></th>
<th><span data-ttu-id="b661c-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-672">CC001</span></span></td>
<td><span data-ttu-id="b661c-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-673">HR</span></span></td>
<td><span data-ttu-id="b661c-674">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-674">10001</span></span></td>
<td><span data-ttu-id="b661c-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-675">Electricity</span></span></td>
<td><span data-ttu-id="b661c-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-677">500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-679">CC001</span></span></td>
<td><span data-ttu-id="b661c-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-680">HR</span></span></td>
<td><span data-ttu-id="b661c-681">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-681">10001</span></span></td>
<td><span data-ttu-id="b661c-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-682">Electricity</span></span></td>
<td><span data-ttu-id="b661c-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-683">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b661c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-686">CC002</span></span></td>
<td><span data-ttu-id="b661c-687">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-687">Finance</span></span></td>
<td><span data-ttu-id="b661c-688">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-688">10001</span></span></td>
<td><span data-ttu-id="b661c-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-689">Electricity</span></span></td>
<td><span data-ttu-id="b661c-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="b661c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-693">CC002</span></span></td>
<td><span data-ttu-id="b661c-694">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-694">Finance</span></span></td>
<td><span data-ttu-id="b661c-695">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-695">10001</span></span></td>
<td><span data-ttu-id="b661c-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-696">Electricity</span></span></td>
<td><span data-ttu-id="b661c-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-697">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b661c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-700">CC003</span></span></td>
<td><span data-ttu-id="b661c-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-701">Assembly</span></span></td>
<td><span data-ttu-id="b661c-702">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-702">10001</span></span></td>
<td><span data-ttu-id="b661c-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-703">Electricity</span></span></td>
<td><span data-ttu-id="b661c-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="b661c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-707">CC003</span></span></td>
<td><span data-ttu-id="b661c-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-708">Assembly</span></span></td>
<td><span data-ttu-id="b661c-709">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-709">10001</span></span></td>
<td><span data-ttu-id="b661c-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-710">Electricity</span></span></td>
<td><span data-ttu-id="b661c-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-711">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b661c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-714">CC003</span></span></td>
<td><span data-ttu-id="b661c-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-715">Packaging</span></span></td>
<td><span data-ttu-id="b661c-716">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-716">10001</span></span></td>
<td><span data-ttu-id="b661c-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-717">Electricity</span></span></td>
<td><span data-ttu-id="b661c-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="b661c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-721">CC003</span></span></td>
<td><span data-ttu-id="b661c-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-722">Packaging</span></span></td>
<td><span data-ttu-id="b661c-723">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-723">10001</span></span></td>
<td><span data-ttu-id="b661c-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-724">Electricity</span></span></td>
<td><span data-ttu-id="b661c-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-725">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b661c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-728">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-729">Product 1</span></span></td>
<td><span data-ttu-id="b661c-730">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-730">10001</span></span></td>
<td><span data-ttu-id="b661c-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-731">Electricity</span></span></td>
<td><span data-ttu-id="b661c-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="b661c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-735">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-736">Product 1</span></span></td>
<td><span data-ttu-id="b661c-737">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-737">10001</span></span></td>
<td><span data-ttu-id="b661c-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-738">Electricity</span></span></td>
<td><span data-ttu-id="b661c-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-739">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b661c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-742">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-743">Product 1</span></span></td>
<td><span data-ttu-id="b661c-744">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-744">10001</span></span></td>
<td><span data-ttu-id="b661c-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-745">Electricity</span></span></td>
<td><span data-ttu-id="b661c-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="b661c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="b661c-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-749">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-750">Product 1</span></span></td>
<td><span data-ttu-id="b661c-751">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-751">10001</span></span></td>
<td><span data-ttu-id="b661c-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-752">Electricity</span></span></td>
<td><span data-ttu-id="b661c-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-753">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b661c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b661c-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b661c-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b661c-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-757">Cost element</span></span></th>
<th><span data-ttu-id="b661c-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="b661c-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b661c-759">Amount</span></span></th>
<th><span data-ttu-id="b661c-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="b661c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b661c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-761">CC001</span></span></td>
<td><span data-ttu-id="b661c-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-762">HR</span></span></td>
<td><span data-ttu-id="b661c-763">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-763">10001</span></span></td>
<td><span data-ttu-id="b661c-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-764">Electricity</span></span></td>
<td><span data-ttu-id="b661c-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="b661c-766">-500.00</span></span></td>
<td><span data-ttu-id="b661c-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-768">CC002</span></span></td>
<td><span data-ttu-id="b661c-769">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-769">Finance</span></span></td>
<td><span data-ttu-id="b661c-770">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-770">10001</span></span></td>
<td><span data-ttu-id="b661c-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-771">Electricity</span></span></td>
<td><span data-ttu-id="b661c-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="b661c-773">175.00</span></span></td>
<td><span data-ttu-id="b661c-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-775">CC003</span></span></td>
<td><span data-ttu-id="b661c-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-776">Assembly</span></span></td>
<td><span data-ttu-id="b661c-777">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-777">10001</span></span></td>
<td><span data-ttu-id="b661c-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-778">Electricity</span></span></td>
<td><span data-ttu-id="b661c-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="b661c-780">275.00</span></span></td>
<td><span data-ttu-id="b661c-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-782">CC004</span></span></td>
<td><span data-ttu-id="b661c-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-783">Packaging</span></span></td>
<td><span data-ttu-id="b661c-784">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-784">10001</span></span></td>
<td><span data-ttu-id="b661c-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-785">Electricity</span></span></td>
<td><span data-ttu-id="b661c-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="b661c-787">50,00</span></span></td>
<td><span data-ttu-id="b661c-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-789">CC001</span></span></td>
<td><span data-ttu-id="b661c-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b661c-790">HR</span></span></td>
<td><span data-ttu-id="b661c-791">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-791">10001</span></span></td>
<td><span data-ttu-id="b661c-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-792">Electricity</span></span></td>
<td><span data-ttu-id="b661c-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-793">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="b661c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="b661c-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-796">CC002</span></span></td>
<td><span data-ttu-id="b661c-797">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-797">Finance</span></span></td>
<td><span data-ttu-id="b661c-798">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-798">10001</span></span></td>
<td><span data-ttu-id="b661c-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-799">Electricity</span></span></td>
<td><span data-ttu-id="b661c-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-800">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="b661c-801">436.00</span></span></td>
<td><span data-ttu-id="b661c-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-803">CC003</span></span></td>
<td><span data-ttu-id="b661c-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-804">Assembly</span></span></td>
<td><span data-ttu-id="b661c-805">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-805">10001</span></span></td>
<td><span data-ttu-id="b661c-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-806">Electricity</span></span></td>
<td><span data-ttu-id="b661c-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-807">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="b661c-808">685.14</span></span></td>
<td><span data-ttu-id="b661c-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-810">CC004</span></span></td>
<td><span data-ttu-id="b661c-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-811">Packaging</span></span></td>
<td><span data-ttu-id="b661c-812">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-812">10001</span></span></td>
<td><span data-ttu-id="b661c-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-813">Electricity</span></span></td>
<td><span data-ttu-id="b661c-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-814">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="b661c-815">124.57</span></span></td>
<td><span data-ttu-id="b661c-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-817">CC002</span></span></td>
<td><span data-ttu-id="b661c-818">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-818">Finance</span></span></td>
<td><span data-ttu-id="b661c-819">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-819">10001</span></span></td>
<td><span data-ttu-id="b661c-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-820">Electricity</span></span></td>
<td><span data-ttu-id="b661c-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="b661c-822">-675.00</span></span></td>
<td><span data-ttu-id="b661c-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-824">CC003</span></span></td>
<td><span data-ttu-id="b661c-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-825">Assembly</span></span></td>
<td><span data-ttu-id="b661c-826">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-826">10001</span></span></td>
<td><span data-ttu-id="b661c-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-827">Electricity</span></span></td>
<td><span data-ttu-id="b661c-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="b661c-829">438.75</span></span></td>
<td><span data-ttu-id="b661c-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-831">CC004</span></span></td>
<td><span data-ttu-id="b661c-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-832">Packaging</span></span></td>
<td><span data-ttu-id="b661c-833">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-833">10001</span></span></td>
<td><span data-ttu-id="b661c-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-834">Electricity</span></span></td>
<td><span data-ttu-id="b661c-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="b661c-836">236.25</span></span></td>
<td><span data-ttu-id="b661c-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-838">CC002</span></span></td>
<td><span data-ttu-id="b661c-839">المالية</span><span class="sxs-lookup"><span data-stu-id="b661c-839">Finance</span></span></td>
<td><span data-ttu-id="b661c-840">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-840">10001</span></span></td>
<td><span data-ttu-id="b661c-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-841">Electricity</span></span></td>
<td><span data-ttu-id="b661c-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-842">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="b661c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="b661c-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-845">CC003</span></span></td>
<td><span data-ttu-id="b661c-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-846">Assembly</span></span></td>
<td><span data-ttu-id="b661c-847">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-847">10001</span></span></td>
<td><span data-ttu-id="b661c-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-848">Electricity</span></span></td>
<td><span data-ttu-id="b661c-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-849">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b661c-850">5,297.69</span></span></td>
<td><span data-ttu-id="b661c-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-852">CC004</span></span></td>
<td><span data-ttu-id="b661c-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="b661c-853">Packaging</span></span></td>
<td><span data-ttu-id="b661c-854">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-854">10001</span></span></td>
<td><span data-ttu-id="b661c-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-855">Electricity</span></span></td>
<td><span data-ttu-id="b661c-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-856">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b661c-857">2,852.60</span></span></td>
<td><span data-ttu-id="b661c-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-859">CC003</span></span></td>
<td><span data-ttu-id="b661c-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-860">Assembly</span></span></td>
<td><span data-ttu-id="b661c-861">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-861">10001</span></span></td>
<td><span data-ttu-id="b661c-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-862">Electricity</span></span></td>
<td><span data-ttu-id="b661c-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="b661c-864">-713.75</span></span></td>
<td><span data-ttu-id="b661c-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-866">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-867">Product 1</span></span></td>
<td><span data-ttu-id="b661c-868">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-868">10001</span></span></td>
<td><span data-ttu-id="b661c-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-869">Electricity</span></span></td>
<td><span data-ttu-id="b661c-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="b661c-871">535.31</span></span></td>
<td><span data-ttu-id="b661c-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-873">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-874">Product 2</span></span></td>
<td><span data-ttu-id="b661c-875">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-875">10001</span></span></td>
<td><span data-ttu-id="b661c-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-876">Electricity</span></span></td>
<td><span data-ttu-id="b661c-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="b661c-878">178.44</span></span></td>
<td><span data-ttu-id="b661c-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-880">CC003</span></span></td>
<td><span data-ttu-id="b661c-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-881">Assembly</span></span></td>
<td><span data-ttu-id="b661c-882">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-882">10001</span></span></td>
<td><span data-ttu-id="b661c-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-883">Electricity</span></span></td>
<td><span data-ttu-id="b661c-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-884">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="b661c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="b661c-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-887">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-888">Product 1</span></span></td>
<td><span data-ttu-id="b661c-889">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-889">10001</span></span></td>
<td><span data-ttu-id="b661c-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-890">Electricity</span></span></td>
<td><span data-ttu-id="b661c-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-891">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b661c-892">4,487.12</span></span></td>
<td><span data-ttu-id="b661c-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-894">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-895">Product 2</span></span></td>
<td><span data-ttu-id="b661c-896">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-896">10001</span></span></td>
<td><span data-ttu-id="b661c-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-897">Electricity</span></span></td>
<td><span data-ttu-id="b661c-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-898">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b661c-899">1,495.71</span></span></td>
<td><span data-ttu-id="b661c-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-901">CC003</span></span></td>
<td><span data-ttu-id="b661c-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-902">Assembly</span></span></td>
<td><span data-ttu-id="b661c-903">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-903">10001</span></span></td>
<td><span data-ttu-id="b661c-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-904">Electricity</span></span></td>
<td><span data-ttu-id="b661c-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="b661c-906">-286.25</span></span></td>
<td><span data-ttu-id="b661c-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-908">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-909">Product 1</span></span></td>
<td><span data-ttu-id="b661c-910">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-910">10001</span></span></td>
<td><span data-ttu-id="b661c-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-911">Electricity</span></span></td>
<td><span data-ttu-id="b661c-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="b661c-913">241.05</span></span></td>
<td><span data-ttu-id="b661c-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-915">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-916">Product 2</span></span></td>
<td><span data-ttu-id="b661c-917">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-917">10001</span></span></td>
<td><span data-ttu-id="b661c-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-918">Electricity</span></span></td>
<td><span data-ttu-id="b661c-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="b661c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="b661c-920">45.20</span></span></td>
<td><span data-ttu-id="b661c-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-922">CC003</span></span></td>
<td><span data-ttu-id="b661c-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="b661c-923">Assembly</span></span></td>
<td><span data-ttu-id="b661c-924">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-924">10001</span></span></td>
<td><span data-ttu-id="b661c-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-925">Electricity</span></span></td>
<td><span data-ttu-id="b661c-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-926">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="b661c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="b661c-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-929">Prod 1</span></span></td>
<td><span data-ttu-id="b661c-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-930">Product 1</span></span></td>
<td><span data-ttu-id="b661c-931">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-931">10001</span></span></td>
<td><span data-ttu-id="b661c-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-932">Electricity</span></span></td>
<td><span data-ttu-id="b661c-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-933">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b661c-934">2,507.09</span></span></td>
<td><span data-ttu-id="b661c-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b661c-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-936">Prod 2</span></span></td>
<td><span data-ttu-id="b661c-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-937">Product 2</span></span></td>
<td><span data-ttu-id="b661c-938">10001</span><span class="sxs-lookup"><span data-stu-id="b661c-938">10001</span></span></td>
<td><span data-ttu-id="b661c-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-939">Electricity</span></span></td>
<td><span data-ttu-id="b661c-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-940">Variable cost</span></span></td>
<td><span data-ttu-id="b661c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="b661c-941">470.08</span></span></td>
<td><span data-ttu-id="b661c-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="b661c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b661c-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="b661c-943">Conclusion</span></span>
<span data-ttu-id="b661c-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="b661c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b661c-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b661c-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="b661c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b661c-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b661c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b661c-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b661c-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="b661c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b661c-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="b661c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b661c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="b661c-951">CC099</span></span></th>
<th><span data-ttu-id="b661c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="b661c-952">CC001</span></span></th>
<th><span data-ttu-id="b661c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="b661c-953">CC002</span></span></th>
<th><span data-ttu-id="b661c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="b661c-954">CC003</span></span></th>
<th><span data-ttu-id="b661c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="b661c-955">CC004</span></span></th>
<th><span data-ttu-id="b661c-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="b661c-956">Proj 1</span></span></th>
<th><span data-ttu-id="b661c-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="b661c-957">Proj 2</span></span></th>
<th><span data-ttu-id="b661c-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="b661c-958">Prod 1</span></span></th>
<th><span data-ttu-id="b661c-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="b661c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b661c-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="b661c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b661c-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b661c-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="b661c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-971">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b661c-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="b661c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-973">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-974">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-975">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-976">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-977">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b661c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="b661c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="b661c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b661c-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="b661c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-982">000</span><span class="sxs-lookup"><span data-stu-id="b661c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-983">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-984">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-985">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-986">0.00</span><span class="sxs-lookup"><span data-stu-id="b661c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-987">30.00</span><span class="sxs-lookup"><span data-stu-id="b661c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-988">10.00</span><span class="sxs-lookup"><span data-stu-id="b661c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b661c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b661c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b661c-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b661c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b661c-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b661c-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="b661c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b661c-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b661c-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b661c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b661c-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="b661c-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



