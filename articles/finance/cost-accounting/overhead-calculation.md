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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822893"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7cb8f-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cb8f-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7cb8f-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="7cb8f-105">Term definition</span></span>
---------------

<span data-ttu-id="7cb8f-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7cb8f-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7cb8f-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="7cb8f-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7cb8f-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-109">Rent</span></span>
-   <span data-ttu-id="7cb8f-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-110">Electricity</span></span>
-   <span data-ttu-id="7cb8f-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7cb8f-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-112">Overhead calculation overview</span></span>
<span data-ttu-id="7cb8f-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7cb8f-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7cb8f-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7cb8f-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7cb8f-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7cb8f-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="7cb8f-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7cb8f-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-119">Version type</span></span>
-   <span data-ttu-id="7cb8f-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="7cb8f-120">Date and time</span></span>
-   <span data-ttu-id="7cb8f-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="7cb8f-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7cb8f-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-122">Fiscal year</span></span>
-   <span data-ttu-id="7cb8f-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-123">Fiscal period</span></span>

<span data-ttu-id="7cb8f-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7cb8f-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7cb8f-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7cb8f-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7cb8f-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7cb8f-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7cb8f-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7cb8f-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7cb8f-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="7cb8f-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7cb8f-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7cb8f-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7cb8f-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7cb8f-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7cb8f-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-140">Main account</span></span></th>
<th><span data-ttu-id="7cb8f-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-143">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-144">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-145">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-145">10001</span></span></td>
<td><span data-ttu-id="7cb8f-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-146">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7cb8f-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7cb8f-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7cb8f-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7cb8f-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7cb8f-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7cb8f-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7cb8f-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7cb8f-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="7cb8f-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7cb8f-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7cb8f-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="7cb8f-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7cb8f-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="7cb8f-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7cb8f-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-160">Journal</span></span></th>
<th><span data-ttu-id="7cb8f-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7cb8f-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7cb8f-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-164">00001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-164">00001</span></span></td>
<td><span data-ttu-id="7cb8f-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7cb8f-166">مالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-166">Fiscal</span></span></td>
<td><span data-ttu-id="7cb8f-167">2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-167">2017</span></span></td>
<td><span data-ttu-id="7cb8f-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-168">Period 1</span></span></td>
<td><span data-ttu-id="7cb8f-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7cb8f-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-173">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-177">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-178">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-179">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-179">10001</span></span></td>
<td><span data-ttu-id="7cb8f-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-180">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="7cb8f-181">Unclassified</span></span></td>
<td><span data-ttu-id="7cb8f-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7cb8f-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-185">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-187">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-189">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-190">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-191">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-191">10001</span></span></td>
<td><span data-ttu-id="7cb8f-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-192">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="7cb8f-193">Unclassified</span></span></td>
<td><span data-ttu-id="7cb8f-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-194">10,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-196">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-197">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-198">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-198">10001</span></span></td>
<td><span data-ttu-id="7cb8f-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-199">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="7cb8f-200">Unclassified</span></span></td>
<td><span data-ttu-id="7cb8f-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-203">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-204">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-205">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-205">10001</span></span></td>
<td><span data-ttu-id="7cb8f-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-206">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-208">1,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-210">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-211">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-212">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-212">10001</span></span></td>
<td><span data-ttu-id="7cb8f-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-213">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-214">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-215">9,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7cb8f-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7cb8f-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7cb8f-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7cb8f-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7cb8f-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7cb8f-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7cb8f-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7cb8f-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7cb8f-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7cb8f-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-228">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-230">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-231">HR</span></span></td>
<td><span data-ttu-id="7cb8f-232">1,000</span><span class="sxs-lookup"><span data-stu-id="7cb8f-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-233">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-234">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-234">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7cb8f-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-236">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-237">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-238">0</span><span class="sxs-lookup"><span data-stu-id="7cb8f-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-240">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-241">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-244">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-245">HR</span></span></td>
<td><span data-ttu-id="7cb8f-246">1,000</span><span class="sxs-lookup"><span data-stu-id="7cb8f-246">1,000</span></span></td>
<td><span data-ttu-id="7cb8f-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-249">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-250">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-250">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7cb8f-251">6,000</span></span></td>
<td><span data-ttu-id="7cb8f-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7cb8f-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-254">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-255">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-256">0</span><span class="sxs-lookup"><span data-stu-id="7cb8f-256">0</span></span></td>
<td><span data-ttu-id="7cb8f-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-258">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7cb8f-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-261">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-262">Formula</span></span></th>
<th><span data-ttu-id="7cb8f-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-263">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-266">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-267">HR</span></span></td>
<td><span data-ttu-id="7cb8f-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7cb8f-269">1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-269">1</span></span></td>
<td><span data-ttu-id="7cb8f-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-271">500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-272">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-273">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-273">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7cb8f-275">1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-275">1</span></span></td>
<td><span data-ttu-id="7cb8f-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-277">500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-278">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-279">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7cb8f-281">0</span><span class="sxs-lookup"><span data-stu-id="7cb8f-281">0</span></span></td>
<td><span data-ttu-id="7cb8f-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-283">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7cb8f-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-285">Journal</span></span></th>
<th><span data-ttu-id="7cb8f-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7cb8f-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7cb8f-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-289">00002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-289">00002</span></span></td>
<td><span data-ttu-id="7cb8f-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7cb8f-291">مالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-291">Fiscal</span></span></td>
<td><span data-ttu-id="7cb8f-292">2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-292">2017</span></span></td>
<td><span data-ttu-id="7cb8f-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-293">Period 1</span></span></td>
<td><span data-ttu-id="7cb8f-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7cb8f-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-298">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-302">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-303">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-304">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-304">10001</span></span></td>
<td><span data-ttu-id="7cb8f-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-305">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-309">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-310">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-311">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-311">10001</span></span></td>
<td><span data-ttu-id="7cb8f-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-312">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-313">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7cb8f-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-317">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-319">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-321">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-322">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-323">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-323">10001</span></span></td>
<td><span data-ttu-id="7cb8f-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-324">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-328">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-329">HR</span></span></td>
<td><span data-ttu-id="7cb8f-330">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-330">10001</span></span></td>
<td><span data-ttu-id="7cb8f-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-331">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-333">500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-333">500.00</span></span></td>
<td><span data-ttu-id="7cb8f-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-335">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-336">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-336">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-337">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-337">10001</span></span></td>
<td><span data-ttu-id="7cb8f-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-338">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-340">500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-340">500.00</span></span></td>
<td><span data-ttu-id="7cb8f-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-342">CC099</span></span></td>
<td><span data-ttu-id="7cb8f-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-343">Default cost center</span></span></td>
<td><span data-ttu-id="7cb8f-344">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-344">10001</span></span></td>
<td><span data-ttu-id="7cb8f-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-345">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-346">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7cb8f-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-349">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-350">HR</span></span></td>
<td><span data-ttu-id="7cb8f-351">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-351">10001</span></span></td>
<td><span data-ttu-id="7cb8f-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-352">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-353">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-354">1,285.71</span></span></td>
<td><span data-ttu-id="7cb8f-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-356">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-357">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-357">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-358">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-358">10001</span></span></td>
<td><span data-ttu-id="7cb8f-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-359">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-360">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7cb8f-361">7,714.29</span></span></td>
<td><span data-ttu-id="7cb8f-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7cb8f-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7cb8f-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7cb8f-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7cb8f-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-367">Define the overhead rate</span></span>

<span data-ttu-id="7cb8f-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7cb8f-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-370">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="7cb8f-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-372">Proj 1</span></span></td>
<td><span data-ttu-id="7cb8f-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-373">Project 1</span></span></td>
<td><span data-ttu-id="7cb8f-374">3</span><span class="sxs-lookup"><span data-stu-id="7cb8f-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-375">Proj 2</span></span></td>
<td><span data-ttu-id="7cb8f-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-376">Project 2</span></span></td>
<td><span data-ttu-id="7cb8f-377">1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-379">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-380">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="7cb8f-382">Units</span></span></th>
<th><span data-ttu-id="7cb8f-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="7cb8f-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-384">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-385">HR</span></span></td>
<td><span data-ttu-id="7cb8f-386">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-386">10001</span></span></td>
<td><span data-ttu-id="7cb8f-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-387">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-388">1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-388">1</span></span></td>
<td><span data-ttu-id="7cb8f-389">10</span><span class="sxs-lookup"><span data-stu-id="7cb8f-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-391">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-392">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-393">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-396">Proj 1</span></span></td>
<td><span data-ttu-id="7cb8f-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-397">Project 1</span></span></td>
<td><span data-ttu-id="7cb8f-398">3</span><span class="sxs-lookup"><span data-stu-id="7cb8f-398">3</span></span></td>
<td><span data-ttu-id="7cb8f-399">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-399">10001</span></span></td>
<td><span data-ttu-id="7cb8f-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7cb8f-401">30.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-402">Proj 2</span></span></td>
<td><span data-ttu-id="7cb8f-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-403">Project 2</span></span></td>
<td><span data-ttu-id="7cb8f-404">1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-404">1</span></span></td>
<td><span data-ttu-id="7cb8f-405">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-405">10001</span></span></td>
<td><span data-ttu-id="7cb8f-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7cb8f-407">10.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7cb8f-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-409">Journal</span></span></th>
<th><span data-ttu-id="7cb8f-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7cb8f-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7cb8f-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-413">00003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-413">00003</span></span></td>
<td><span data-ttu-id="7cb8f-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7cb8f-415">مالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-415">Fiscal</span></span></td>
<td><span data-ttu-id="7cb8f-416">2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-416">2017</span></span></td>
<td><span data-ttu-id="7cb8f-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-417">Period 1</span></span></td>
<td><span data-ttu-id="7cb8f-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7cb8f-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-421">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-424">Proj 1</span></span></td>
<td><span data-ttu-id="7cb8f-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7cb8f-426">3.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-428">Proj 2</span></span></td>
<td><span data-ttu-id="7cb8f-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7cb8f-430">1.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7cb8f-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-433">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-435">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-437">CC0001</span></span></td>
<td><span data-ttu-id="7cb8f-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-438">HR</span></span></td>
<td><span data-ttu-id="7cb8f-439">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-439">10001</span></span></td>
<td><span data-ttu-id="7cb8f-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-440">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-441">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-442">-30.00</span></span></td>
<td><span data-ttu-id="7cb8f-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-444">Proj 1</span></span></td>
<td><span data-ttu-id="7cb8f-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7cb8f-446">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-446">10001</span></span></td>
<td><span data-ttu-id="7cb8f-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-447">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-448">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-449">30.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-449">30.00</span></span></td>
<td><span data-ttu-id="7cb8f-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-451">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-452">HR</span></span></td>
<td><span data-ttu-id="7cb8f-453">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-453">10001</span></span></td>
<td><span data-ttu-id="7cb8f-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-454">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-455">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-456">-10.00</span></span></td>
<td><span data-ttu-id="7cb8f-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-458">Proj 2</span></span></td>
<td><span data-ttu-id="7cb8f-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7cb8f-460">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-460">10001</span></span></td>
<td><span data-ttu-id="7cb8f-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-461">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-462">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-463">10.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-463">10.00</span></span></td>
<td><span data-ttu-id="7cb8f-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7cb8f-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7cb8f-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7cb8f-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7cb8f-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7cb8f-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7cb8f-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7cb8f-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7cb8f-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7cb8f-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7cb8f-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-475">Define the cost allocation</span></span>

<span data-ttu-id="7cb8f-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7cb8f-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7cb8f-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-479">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-481">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-482">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-482">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-483">35</span><span class="sxs-lookup"><span data-stu-id="7cb8f-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-484">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-485">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-486">55</span><span class="sxs-lookup"><span data-stu-id="7cb8f-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-487">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-488">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-489">10</span><span class="sxs-lookup"><span data-stu-id="7cb8f-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7cb8f-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-492">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-494">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-495">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-496">65</span><span class="sxs-lookup"><span data-stu-id="7cb8f-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-497">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-498">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-499">35</span><span class="sxs-lookup"><span data-stu-id="7cb8f-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7cb8f-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-502">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-504">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-505">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-506">60</span><span class="sxs-lookup"><span data-stu-id="7cb8f-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-507">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-508">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-509">20</span><span class="sxs-lookup"><span data-stu-id="7cb8f-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7cb8f-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-512">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-514">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-515">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-516">80</span><span class="sxs-lookup"><span data-stu-id="7cb8f-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-517">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-518">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-519">15</span><span class="sxs-lookup"><span data-stu-id="7cb8f-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7cb8f-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7cb8f-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7cb8f-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-523">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-524">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-526">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-528">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-529">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-529">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-530">35</span><span class="sxs-lookup"><span data-stu-id="7cb8f-530">35</span></span></td>
<td><span data-ttu-id="7cb8f-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7cb8f-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-532">175.00</span></span></td>
<td><span data-ttu-id="7cb8f-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-534">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-535">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-536">55</span><span class="sxs-lookup"><span data-stu-id="7cb8f-536">55</span></span></td>
<td><span data-ttu-id="7cb8f-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7cb8f-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-538">275.00</span></span></td>
<td><span data-ttu-id="7cb8f-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-540">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-541">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-542">10</span><span class="sxs-lookup"><span data-stu-id="7cb8f-542">10</span></span></td>
<td><span data-ttu-id="7cb8f-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7cb8f-544">50.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-544">50.00</span></span></td>
<td><span data-ttu-id="7cb8f-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-546">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-547">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-547">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-548">35</span><span class="sxs-lookup"><span data-stu-id="7cb8f-548">35</span></span></td>
<td><span data-ttu-id="7cb8f-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7cb8f-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-550">436.00</span></span></td>
<td><span data-ttu-id="7cb8f-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-552">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-553">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-554">55</span><span class="sxs-lookup"><span data-stu-id="7cb8f-554">55</span></span></td>
<td><span data-ttu-id="7cb8f-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7cb8f-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7cb8f-556">685.14</span></span></td>
<td><span data-ttu-id="7cb8f-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-558">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-559">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-560">10</span><span class="sxs-lookup"><span data-stu-id="7cb8f-560">10</span></span></td>
<td><span data-ttu-id="7cb8f-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7cb8f-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7cb8f-562">124.57</span></span></td>
<td><span data-ttu-id="7cb8f-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-565">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-566">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-568">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-570">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-571">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-572">65</span><span class="sxs-lookup"><span data-stu-id="7cb8f-572">65</span></span></td>
<td><span data-ttu-id="7cb8f-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7cb8f-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7cb8f-574">438.75</span></span></td>
<td><span data-ttu-id="7cb8f-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-576">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-577">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-578">35</span><span class="sxs-lookup"><span data-stu-id="7cb8f-578">35</span></span></td>
<td><span data-ttu-id="7cb8f-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7cb8f-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7cb8f-580">236.25</span></span></td>
<td><span data-ttu-id="7cb8f-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-582">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-583">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-584">65</span><span class="sxs-lookup"><span data-stu-id="7cb8f-584">65</span></span></td>
<td><span data-ttu-id="7cb8f-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7cb8f-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7cb8f-586">5,297.69</span></span></td>
<td><span data-ttu-id="7cb8f-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-588">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-589">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-590">35</span><span class="sxs-lookup"><span data-stu-id="7cb8f-590">35</span></span></td>
<td><span data-ttu-id="7cb8f-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7cb8f-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7cb8f-592">2,852.60</span></span></td>
<td><span data-ttu-id="7cb8f-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-595">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-596">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-598">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-600">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-601">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-602">60</span><span class="sxs-lookup"><span data-stu-id="7cb8f-602">60</span></span></td>
<td><span data-ttu-id="7cb8f-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7cb8f-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7cb8f-604">535.31</span></span></td>
<td><span data-ttu-id="7cb8f-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-606">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-607">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-608">20</span><span class="sxs-lookup"><span data-stu-id="7cb8f-608">20</span></span></td>
<td><span data-ttu-id="7cb8f-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7cb8f-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7cb8f-610">178.44</span></span></td>
<td><span data-ttu-id="7cb8f-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-612">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-613">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-614">60</span><span class="sxs-lookup"><span data-stu-id="7cb8f-614">60</span></span></td>
<td><span data-ttu-id="7cb8f-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7cb8f-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7cb8f-616">4,487.12</span></span></td>
<td><span data-ttu-id="7cb8f-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-618">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-619">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-620">20</span><span class="sxs-lookup"><span data-stu-id="7cb8f-620">20</span></span></td>
<td><span data-ttu-id="7cb8f-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7cb8f-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-622">1,495.71</span></span></td>
<td><span data-ttu-id="7cb8f-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7cb8f-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-625">Cost object</span></span></th>
<th><span data-ttu-id="7cb8f-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-626">Magnitude</span></span></th>
<th><span data-ttu-id="7cb8f-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7cb8f-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-628">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-630">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-631">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-632">80</span><span class="sxs-lookup"><span data-stu-id="7cb8f-632">80</span></span></td>
<td><span data-ttu-id="7cb8f-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7cb8f-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7cb8f-634">241.05</span></span></td>
<td><span data-ttu-id="7cb8f-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-636">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-637">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-638">15</span><span class="sxs-lookup"><span data-stu-id="7cb8f-638">15</span></span></td>
<td><span data-ttu-id="7cb8f-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7cb8f-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7cb8f-640">45.20</span></span></td>
<td><span data-ttu-id="7cb8f-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-642">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-643">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-644">80</span><span class="sxs-lookup"><span data-stu-id="7cb8f-644">80</span></span></td>
<td><span data-ttu-id="7cb8f-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7cb8f-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7cb8f-646">2,507.09</span></span></td>
<td><span data-ttu-id="7cb8f-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-648">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-649">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-650">15</span><span class="sxs-lookup"><span data-stu-id="7cb8f-650">15</span></span></td>
<td><span data-ttu-id="7cb8f-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7cb8f-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7cb8f-652">470.08</span></span></td>
<td><span data-ttu-id="7cb8f-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7cb8f-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="7cb8f-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-655">Journal</span></span></th>
<th><span data-ttu-id="7cb8f-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7cb8f-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7cb8f-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="7cb8f-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-659">00004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-659">00004</span></span></td>
<td><span data-ttu-id="7cb8f-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7cb8f-661">مالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-661">Fiscal</span></span></td>
<td><span data-ttu-id="7cb8f-662">2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-662">2017</span></span></td>
<td><span data-ttu-id="7cb8f-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-663">Period 1</span></span></td>
<td><span data-ttu-id="7cb8f-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7cb8f-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7cb8f-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-668">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-672">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-673">HR</span></span></td>
<td><span data-ttu-id="7cb8f-674">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-674">10001</span></span></td>
<td><span data-ttu-id="7cb8f-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-675">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-677">500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-679">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-680">HR</span></span></td>
<td><span data-ttu-id="7cb8f-681">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-681">10001</span></span></td>
<td><span data-ttu-id="7cb8f-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-682">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-683">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-686">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-687">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-687">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-688">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-688">10001</span></span></td>
<td><span data-ttu-id="7cb8f-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-689">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-693">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-694">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-694">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-695">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-695">10001</span></span></td>
<td><span data-ttu-id="7cb8f-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-696">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-697">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7cb8f-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-700">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-701">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-702">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-702">10001</span></span></td>
<td><span data-ttu-id="7cb8f-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-703">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7cb8f-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-707">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-708">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-709">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-709">10001</span></span></td>
<td><span data-ttu-id="7cb8f-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-710">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-711">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7cb8f-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-714">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-715">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-716">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-716">10001</span></span></td>
<td><span data-ttu-id="7cb8f-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-717">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7cb8f-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-721">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-722">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-723">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-723">10001</span></span></td>
<td><span data-ttu-id="7cb8f-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-724">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-725">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7cb8f-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-728">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-729">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-730">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-730">10001</span></span></td>
<td><span data-ttu-id="7cb8f-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-731">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7cb8f-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-735">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-736">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-737">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-737">10001</span></span></td>
<td><span data-ttu-id="7cb8f-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-738">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-739">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7cb8f-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-742">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-743">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-744">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-744">10001</span></span></td>
<td><span data-ttu-id="7cb8f-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-745">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7cb8f-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7cb8f-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-749">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-750">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-751">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-751">10001</span></span></td>
<td><span data-ttu-id="7cb8f-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-752">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-753">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7cb8f-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7cb8f-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7cb8f-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7cb8f-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-757">Cost element</span></span></th>
<th><span data-ttu-id="7cb8f-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7cb8f-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cb8f-759">Amount</span></span></th>
<th><span data-ttu-id="7cb8f-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7cb8f-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-761">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-762">HR</span></span></td>
<td><span data-ttu-id="7cb8f-763">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-763">10001</span></span></td>
<td><span data-ttu-id="7cb8f-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-764">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-766">-500.00</span></span></td>
<td><span data-ttu-id="7cb8f-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-768">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-769">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-769">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-770">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-770">10001</span></span></td>
<td><span data-ttu-id="7cb8f-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-771">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-773">175.00</span></span></td>
<td><span data-ttu-id="7cb8f-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-775">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-776">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-777">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-777">10001</span></span></td>
<td><span data-ttu-id="7cb8f-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-778">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-780">275.00</span></span></td>
<td><span data-ttu-id="7cb8f-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-782">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-783">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-784">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-784">10001</span></span></td>
<td><span data-ttu-id="7cb8f-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-785">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-787">50,00</span></span></td>
<td><span data-ttu-id="7cb8f-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-789">CC001</span></span></td>
<td><span data-ttu-id="7cb8f-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-790">HR</span></span></td>
<td><span data-ttu-id="7cb8f-791">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-791">10001</span></span></td>
<td><span data-ttu-id="7cb8f-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-792">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-793">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7cb8f-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-796">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-797">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-797">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-798">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-798">10001</span></span></td>
<td><span data-ttu-id="7cb8f-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-799">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-800">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-801">436.00</span></span></td>
<td><span data-ttu-id="7cb8f-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-803">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-804">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-805">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-805">10001</span></span></td>
<td><span data-ttu-id="7cb8f-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-806">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-807">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7cb8f-808">685.14</span></span></td>
<td><span data-ttu-id="7cb8f-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-810">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-811">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-812">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-812">10001</span></span></td>
<td><span data-ttu-id="7cb8f-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-813">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-814">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7cb8f-815">124.57</span></span></td>
<td><span data-ttu-id="7cb8f-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-817">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-818">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-818">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-819">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-819">10001</span></span></td>
<td><span data-ttu-id="7cb8f-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-820">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-822">-675.00</span></span></td>
<td><span data-ttu-id="7cb8f-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-824">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-825">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-826">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-826">10001</span></span></td>
<td><span data-ttu-id="7cb8f-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-827">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7cb8f-829">438.75</span></span></td>
<td><span data-ttu-id="7cb8f-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-831">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-832">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-833">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-833">10001</span></span></td>
<td><span data-ttu-id="7cb8f-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-834">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7cb8f-836">236.25</span></span></td>
<td><span data-ttu-id="7cb8f-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-838">CC002</span></span></td>
<td><span data-ttu-id="7cb8f-839">المالية</span><span class="sxs-lookup"><span data-stu-id="7cb8f-839">Finance</span></span></td>
<td><span data-ttu-id="7cb8f-840">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-840">10001</span></span></td>
<td><span data-ttu-id="7cb8f-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-841">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-842">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="7cb8f-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7cb8f-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-845">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-846">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-847">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-847">10001</span></span></td>
<td><span data-ttu-id="7cb8f-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-848">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-849">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7cb8f-850">5,297.69</span></span></td>
<td><span data-ttu-id="7cb8f-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-852">CC004</span></span></td>
<td><span data-ttu-id="7cb8f-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-853">Packaging</span></span></td>
<td><span data-ttu-id="7cb8f-854">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-854">10001</span></span></td>
<td><span data-ttu-id="7cb8f-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-855">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-856">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7cb8f-857">2,852.60</span></span></td>
<td><span data-ttu-id="7cb8f-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-859">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-860">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-861">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-861">10001</span></span></td>
<td><span data-ttu-id="7cb8f-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-862">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="7cb8f-864">-713.75</span></span></td>
<td><span data-ttu-id="7cb8f-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-866">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-867">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-868">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-868">10001</span></span></td>
<td><span data-ttu-id="7cb8f-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-869">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7cb8f-871">535.31</span></span></td>
<td><span data-ttu-id="7cb8f-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-873">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-874">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-875">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-875">10001</span></span></td>
<td><span data-ttu-id="7cb8f-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-876">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7cb8f-878">178.44</span></span></td>
<td><span data-ttu-id="7cb8f-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-880">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-881">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-882">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-882">10001</span></span></td>
<td><span data-ttu-id="7cb8f-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-883">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-884">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="7cb8f-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7cb8f-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-887">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-888">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-889">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-889">10001</span></span></td>
<td><span data-ttu-id="7cb8f-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-890">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-891">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7cb8f-892">4,487.12</span></span></td>
<td><span data-ttu-id="7cb8f-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-894">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-895">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-896">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-896">10001</span></span></td>
<td><span data-ttu-id="7cb8f-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-897">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-898">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7cb8f-899">1,495.71</span></span></td>
<td><span data-ttu-id="7cb8f-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-901">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-902">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-903">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-903">10001</span></span></td>
<td><span data-ttu-id="7cb8f-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-904">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="7cb8f-906">-286.25</span></span></td>
<td><span data-ttu-id="7cb8f-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-908">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-909">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-910">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-910">10001</span></span></td>
<td><span data-ttu-id="7cb8f-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-911">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7cb8f-913">241.05</span></span></td>
<td><span data-ttu-id="7cb8f-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-915">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-916">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-917">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-917">10001</span></span></td>
<td><span data-ttu-id="7cb8f-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-918">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7cb8f-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7cb8f-920">45.20</span></span></td>
<td><span data-ttu-id="7cb8f-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-922">CC003</span></span></td>
<td><span data-ttu-id="7cb8f-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="7cb8f-923">Assembly</span></span></td>
<td><span data-ttu-id="7cb8f-924">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-924">10001</span></span></td>
<td><span data-ttu-id="7cb8f-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-925">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-926">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="7cb8f-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7cb8f-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-929">Prod 1</span></span></td>
<td><span data-ttu-id="7cb8f-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-930">Product 1</span></span></td>
<td><span data-ttu-id="7cb8f-931">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-931">10001</span></span></td>
<td><span data-ttu-id="7cb8f-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-932">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-933">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7cb8f-934">2,507.09</span></span></td>
<td><span data-ttu-id="7cb8f-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7cb8f-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-936">Prod 2</span></span></td>
<td><span data-ttu-id="7cb8f-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-937">Product 2</span></span></td>
<td><span data-ttu-id="7cb8f-938">10001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-938">10001</span></span></td>
<td><span data-ttu-id="7cb8f-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-939">Electricity</span></span></td>
<td><span data-ttu-id="7cb8f-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-940">Variable cost</span></span></td>
<td><span data-ttu-id="7cb8f-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7cb8f-941">470.08</span></span></td>
<td><span data-ttu-id="7cb8f-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="7cb8f-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7cb8f-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-943">Conclusion</span></span>
<span data-ttu-id="7cb8f-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7cb8f-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7cb8f-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7cb8f-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7cb8f-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7cb8f-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7cb8f-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="7cb8f-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7cb8f-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7cb8f-951">CC099</span></span></th>
<th><span data-ttu-id="7cb8f-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7cb8f-952">CC001</span></span></th>
<th><span data-ttu-id="7cb8f-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7cb8f-953">CC002</span></span></th>
<th><span data-ttu-id="7cb8f-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7cb8f-954">CC003</span></span></th>
<th><span data-ttu-id="7cb8f-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7cb8f-955">CC004</span></span></th>
<th><span data-ttu-id="7cb8f-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-956">Proj 1</span></span></th>
<th><span data-ttu-id="7cb8f-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-957">Proj 2</span></span></th>
<th><span data-ttu-id="7cb8f-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="7cb8f-958">Prod 1</span></span></th>
<th><span data-ttu-id="7cb8f-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="7cb8f-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7cb8f-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="7cb8f-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7cb8f-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="7cb8f-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-971">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7cb8f-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-973">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-974">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-975">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-976">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-977">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7cb8f-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7cb8f-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7cb8f-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="7cb8f-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-982">000</span><span class="sxs-lookup"><span data-stu-id="7cb8f-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-983">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-984">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-985">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-986">0.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-987">30.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-988">10.00</span><span class="sxs-lookup"><span data-stu-id="7cb8f-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7cb8f-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7cb8f-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7cb8f-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7cb8f-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7cb8f-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7cb8f-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7cb8f-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7cb8f-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7cb8f-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7cb8f-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="7cb8f-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]