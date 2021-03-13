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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009508"
---
# <a name="overhead-calculation"></a><span data-ttu-id="19b11-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="19b11-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19b11-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="19b11-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="19b11-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="19b11-105">Term definition</span></span>
---------------

<span data-ttu-id="19b11-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="19b11-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="19b11-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="19b11-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="19b11-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="19b11-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="19b11-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="19b11-109">Rent</span></span>
-   <span data-ttu-id="19b11-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-110">Electricity</span></span>
-   <span data-ttu-id="19b11-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="19b11-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="19b11-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="19b11-112">Overhead calculation overview</span></span>
<span data-ttu-id="19b11-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="19b11-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="19b11-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="19b11-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="19b11-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="19b11-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="19b11-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="19b11-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="19b11-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="19b11-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="19b11-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="19b11-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="19b11-119">Version type</span></span>
-   <span data-ttu-id="19b11-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="19b11-120">Date and time</span></span>
-   <span data-ttu-id="19b11-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="19b11-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="19b11-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-122">Fiscal year</span></span>
-   <span data-ttu-id="19b11-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-123">Fiscal period</span></span>

<span data-ttu-id="19b11-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="19b11-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="19b11-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="19b11-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="19b11-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="19b11-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="19b11-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="19b11-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="19b11-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="19b11-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="19b11-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="19b11-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="19b11-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="19b11-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="19b11-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="19b11-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="19b11-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="19b11-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="19b11-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="19b11-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="19b11-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="19b11-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="19b11-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="19b11-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="19b11-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="19b11-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="19b11-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="19b11-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="19b11-140">Main account</span></span></th>
<th><span data-ttu-id="19b11-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="19b11-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="19b11-143">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-143">CC099</span></span></td>
<td><span data-ttu-id="19b11-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-144">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-145">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-145">10001</span></span></td>
<td><span data-ttu-id="19b11-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-146">Electricity</span></span></td>
<td><span data-ttu-id="19b11-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="19b11-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="19b11-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="19b11-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="19b11-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="19b11-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="19b11-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-151">Define the cost behavior rule</span></span>

<span data-ttu-id="19b11-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="19b11-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="19b11-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="19b11-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="19b11-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="19b11-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="19b11-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="19b11-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="19b11-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="19b11-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="19b11-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="19b11-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="19b11-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="19b11-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-160">Journal</span></span></th>
<th><span data-ttu-id="19b11-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="19b11-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="19b11-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="19b11-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="19b11-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="19b11-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-164">00001</span><span class="sxs-lookup"><span data-stu-id="19b11-164">00001</span></span></td>
<td><span data-ttu-id="19b11-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="19b11-166">مالي</span><span class="sxs-lookup"><span data-stu-id="19b11-166">Fiscal</span></span></td>
<td><span data-ttu-id="19b11-167">2017</span><span class="sxs-lookup"><span data-stu-id="19b11-167">2017</span></span></td>
<td><span data-ttu-id="19b11-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-168">Period 1</span></span></td>
<td><span data-ttu-id="19b11-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="19b11-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="19b11-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-173">Cost element</span></span></th>
<th><span data-ttu-id="19b11-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-174">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="19b11-177">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-177">CC099</span></span></td>
<td><span data-ttu-id="19b11-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-178">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-179">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-179">10001</span></span></td>
<td><span data-ttu-id="19b11-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-180">Electricity</span></span></td>
<td><span data-ttu-id="19b11-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="19b11-181">Unclassified</span></span></td>
<td><span data-ttu-id="19b11-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="19b11-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-185">Cost element</span></span></th>
<th><span data-ttu-id="19b11-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-186">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-187">Amount</span></span></th>
<th><span data-ttu-id="19b11-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-189">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-189">CC099</span></span></td>
<td><span data-ttu-id="19b11-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-190">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-191">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-191">10001</span></span></td>
<td><span data-ttu-id="19b11-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-192">Electricity</span></span></td>
<td><span data-ttu-id="19b11-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="19b11-193">Unclassified</span></span></td>
<td><span data-ttu-id="19b11-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-194">10,000.00</span></span></td>
<td><span data-ttu-id="19b11-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-196">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-196">CC099</span></span></td>
<td><span data-ttu-id="19b11-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-197">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-198">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-198">10001</span></span></td>
<td><span data-ttu-id="19b11-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-199">Electricity</span></span></td>
<td><span data-ttu-id="19b11-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="19b11-200">Unclassified</span></span></td>
<td><span data-ttu-id="19b11-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-201">-10,000.00</span></span></td>
<td><span data-ttu-id="19b11-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-203">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-203">CC099</span></span></td>
<td><span data-ttu-id="19b11-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-204">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-205">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-205">10001</span></span></td>
<td><span data-ttu-id="19b11-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-206">Electricity</span></span></td>
<td><span data-ttu-id="19b11-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-207">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-208">1,000.00</span></span></td>
<td><span data-ttu-id="19b11-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-210">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-210">CC099</span></span></td>
<td><span data-ttu-id="19b11-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-211">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-212">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-212">10001</span></span></td>
<td><span data-ttu-id="19b11-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-213">Electricity</span></span></td>
<td><span data-ttu-id="19b11-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-214">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-215">9,000.00</span></span></td>
<td><span data-ttu-id="19b11-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="19b11-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="19b11-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="19b11-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="19b11-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="19b11-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="19b11-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="19b11-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-221">Define the cost distribution rule</span></span>

<span data-ttu-id="19b11-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="19b11-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="19b11-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="19b11-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="19b11-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="19b11-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="19b11-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="19b11-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="19b11-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="19b11-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="19b11-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="19b11-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-228">Cost object</span></span></th>
<th><span data-ttu-id="19b11-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="19b11-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-230">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-230">CC001</span></span></td>
<td><span data-ttu-id="19b11-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-231">HR</span></span></td>
<td><span data-ttu-id="19b11-232">1,000</span><span class="sxs-lookup"><span data-stu-id="19b11-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-233">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-233">CC002</span></span></td>
<td><span data-ttu-id="19b11-234">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-234">Finance</span></span></td>
<td><span data-ttu-id="19b11-235">6,000</span><span class="sxs-lookup"><span data-stu-id="19b11-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-236">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-236">CC003</span></span></td>
<td><span data-ttu-id="19b11-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-237">Assembly</span></span></td>
<td><span data-ttu-id="19b11-238">0</span><span class="sxs-lookup"><span data-stu-id="19b11-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="19b11-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-240">Cost object</span></span></th>
<th><span data-ttu-id="19b11-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-241">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-242">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-244">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-244">CC001</span></span></td>
<td><span data-ttu-id="19b11-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-245">HR</span></span></td>
<td><span data-ttu-id="19b11-246">1,000</span><span class="sxs-lookup"><span data-stu-id="19b11-246">1,000</span></span></td>
<td><span data-ttu-id="19b11-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="19b11-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="19b11-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-249">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-249">CC002</span></span></td>
<td><span data-ttu-id="19b11-250">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-250">Finance</span></span></td>
<td><span data-ttu-id="19b11-251">6,000</span><span class="sxs-lookup"><span data-stu-id="19b11-251">6,000</span></span></td>
<td><span data-ttu-id="19b11-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="19b11-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="19b11-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-254">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-254">CC003</span></span></td>
<td><span data-ttu-id="19b11-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-255">Assembly</span></span></td>
<td><span data-ttu-id="19b11-256">0</span><span class="sxs-lookup"><span data-stu-id="19b11-256">0</span></span></td>
<td><span data-ttu-id="19b11-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="19b11-258">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="19b11-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="19b11-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="19b11-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-261">Cost object</span></span></th>
<th><span data-ttu-id="19b11-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="19b11-262">Formula</span></span></th>
<th><span data-ttu-id="19b11-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-263">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-264">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-266">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-266">CC001</span></span></td>
<td><span data-ttu-id="19b11-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-267">HR</span></span></td>
<td><span data-ttu-id="19b11-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="19b11-269">1</span><span class="sxs-lookup"><span data-stu-id="19b11-269">1</span></span></td>
<td><span data-ttu-id="19b11-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="19b11-271">500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-272">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-272">CC002</span></span></td>
<td><span data-ttu-id="19b11-273">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-273">Finance</span></span></td>
<td><span data-ttu-id="19b11-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="19b11-275">1</span><span class="sxs-lookup"><span data-stu-id="19b11-275">1</span></span></td>
<td><span data-ttu-id="19b11-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="19b11-277">500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-278">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-278">CC003</span></span></td>
<td><span data-ttu-id="19b11-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-279">Assembly</span></span></td>
<td><span data-ttu-id="19b11-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="19b11-281">0</span><span class="sxs-lookup"><span data-stu-id="19b11-281">0</span></span></td>
<td><span data-ttu-id="19b11-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="19b11-283">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="19b11-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-285">Journal</span></span></th>
<th><span data-ttu-id="19b11-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="19b11-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="19b11-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="19b11-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="19b11-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="19b11-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-289">00002</span><span class="sxs-lookup"><span data-stu-id="19b11-289">00002</span></span></td>
<td><span data-ttu-id="19b11-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="19b11-291">مالي</span><span class="sxs-lookup"><span data-stu-id="19b11-291">Fiscal</span></span></td>
<td><span data-ttu-id="19b11-292">2017</span><span class="sxs-lookup"><span data-stu-id="19b11-292">2017</span></span></td>
<td><span data-ttu-id="19b11-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-293">Period 1</span></span></td>
<td><span data-ttu-id="19b11-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="19b11-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="19b11-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-298">Cost element</span></span></th>
<th><span data-ttu-id="19b11-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-299">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-302">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-302">CC099</span></span></td>
<td><span data-ttu-id="19b11-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-303">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-304">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-304">10001</span></span></td>
<td><span data-ttu-id="19b11-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-305">Electricity</span></span></td>
<td><span data-ttu-id="19b11-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-306">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-309">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-309">CC099</span></span></td>
<td><span data-ttu-id="19b11-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-310">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-311">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-311">10001</span></span></td>
<td><span data-ttu-id="19b11-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-312">Electricity</span></span></td>
<td><span data-ttu-id="19b11-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-313">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="19b11-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-317">Cost element</span></span></th>
<th><span data-ttu-id="19b11-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-318">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-319">Amount</span></span></th>
<th><span data-ttu-id="19b11-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-321">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-321">CC099</span></span></td>
<td><span data-ttu-id="19b11-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-322">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-323">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-323">10001</span></span></td>
<td><span data-ttu-id="19b11-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-324">Electricity</span></span></td>
<td><span data-ttu-id="19b11-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-325">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-326">-1,000.00</span></span></td>
<td><span data-ttu-id="19b11-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-328">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-328">CC001</span></span></td>
<td><span data-ttu-id="19b11-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-329">HR</span></span></td>
<td><span data-ttu-id="19b11-330">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-330">10001</span></span></td>
<td><span data-ttu-id="19b11-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-331">Electricity</span></span></td>
<td><span data-ttu-id="19b11-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-332">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-333">500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-333">500.00</span></span></td>
<td><span data-ttu-id="19b11-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-335">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-335">CC002</span></span></td>
<td><span data-ttu-id="19b11-336">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-336">Finance</span></span></td>
<td><span data-ttu-id="19b11-337">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-337">10001</span></span></td>
<td><span data-ttu-id="19b11-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-338">Electricity</span></span></td>
<td><span data-ttu-id="19b11-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-339">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-340">500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-340">500.00</span></span></td>
<td><span data-ttu-id="19b11-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-342">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-342">CC099</span></span></td>
<td><span data-ttu-id="19b11-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="19b11-343">Default cost center</span></span></td>
<td><span data-ttu-id="19b11-344">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-344">10001</span></span></td>
<td><span data-ttu-id="19b11-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-345">Electricity</span></span></td>
<td><span data-ttu-id="19b11-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-346">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="19b11-347">-9,000.00</span></span></td>
<td><span data-ttu-id="19b11-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-349">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-349">CC001</span></span></td>
<td><span data-ttu-id="19b11-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-350">HR</span></span></td>
<td><span data-ttu-id="19b11-351">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-351">10001</span></span></td>
<td><span data-ttu-id="19b11-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-352">Electricity</span></span></td>
<td><span data-ttu-id="19b11-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-353">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="19b11-354">1,285.71</span></span></td>
<td><span data-ttu-id="19b11-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-356">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-356">CC002</span></span></td>
<td><span data-ttu-id="19b11-357">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-357">Finance</span></span></td>
<td><span data-ttu-id="19b11-358">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-358">10001</span></span></td>
<td><span data-ttu-id="19b11-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-359">Electricity</span></span></td>
<td><span data-ttu-id="19b11-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-360">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="19b11-361">7,714.29</span></span></td>
<td><span data-ttu-id="19b11-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="19b11-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="19b11-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="19b11-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="19b11-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="19b11-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="19b11-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="19b11-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="19b11-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="19b11-367">Define the overhead rate</span></span>

<span data-ttu-id="19b11-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="19b11-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="19b11-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="19b11-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-370">Cost object</span></span></th>
<th><span data-ttu-id="19b11-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="19b11-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-372">Proj 1</span></span></td>
<td><span data-ttu-id="19b11-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-373">Project 1</span></span></td>
<td><span data-ttu-id="19b11-374">3</span><span class="sxs-lookup"><span data-stu-id="19b11-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-375">Proj 2</span></span></td>
<td><span data-ttu-id="19b11-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-376">Project 2</span></span></td>
<td><span data-ttu-id="19b11-377">1</span><span class="sxs-lookup"><span data-stu-id="19b11-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-379">Cost object</span></span></th>
<th><span data-ttu-id="19b11-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-380">Cost element</span></span></th>
<th><span data-ttu-id="19b11-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-381">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="19b11-382">Units</span></span></th>
<th><span data-ttu-id="19b11-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="19b11-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-384">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-384">CC001</span></span></td>
<td><span data-ttu-id="19b11-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-385">HR</span></span></td>
<td><span data-ttu-id="19b11-386">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-386">10001</span></span></td>
<td><span data-ttu-id="19b11-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-387">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-388">1</span><span class="sxs-lookup"><span data-stu-id="19b11-388">1</span></span></td>
<td><span data-ttu-id="19b11-389">10</span><span class="sxs-lookup"><span data-stu-id="19b11-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="19b11-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-391">Cost object</span></span></th>
<th><span data-ttu-id="19b11-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-392">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-393">Cost element</span></span></th>
<th><span data-ttu-id="19b11-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-394">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-396">Proj 1</span></span></td>
<td><span data-ttu-id="19b11-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-397">Project 1</span></span></td>
<td><span data-ttu-id="19b11-398">3</span><span class="sxs-lookup"><span data-stu-id="19b11-398">3</span></span></td>
<td><span data-ttu-id="19b11-399">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-399">10001</span></span></td>
<td><span data-ttu-id="19b11-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="19b11-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="19b11-401">30.00</span><span class="sxs-lookup"><span data-stu-id="19b11-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-402">Proj 2</span></span></td>
<td><span data-ttu-id="19b11-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-403">Project 2</span></span></td>
<td><span data-ttu-id="19b11-404">1</span><span class="sxs-lookup"><span data-stu-id="19b11-404">1</span></span></td>
<td><span data-ttu-id="19b11-405">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-405">10001</span></span></td>
<td><span data-ttu-id="19b11-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="19b11-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="19b11-407">10.00</span><span class="sxs-lookup"><span data-stu-id="19b11-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="19b11-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-409">Journal</span></span></th>
<th><span data-ttu-id="19b11-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="19b11-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="19b11-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="19b11-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="19b11-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="19b11-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-413">00003</span><span class="sxs-lookup"><span data-stu-id="19b11-413">00003</span></span></td>
<td><span data-ttu-id="19b11-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="19b11-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="19b11-415">مالي</span><span class="sxs-lookup"><span data-stu-id="19b11-415">Fiscal</span></span></td>
<td><span data-ttu-id="19b11-416">2017</span><span class="sxs-lookup"><span data-stu-id="19b11-416">2017</span></span></td>
<td><span data-ttu-id="19b11-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-417">Period 1</span></span></td>
<td><span data-ttu-id="19b11-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="19b11-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="19b11-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-421">Cost object</span></span></th>
<th><span data-ttu-id="19b11-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-424">Proj 1</span></span></td>
<td><span data-ttu-id="19b11-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="19b11-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="19b11-426">3.00</span><span class="sxs-lookup"><span data-stu-id="19b11-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-428">Proj 2</span></span></td>
<td><span data-ttu-id="19b11-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="19b11-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="19b11-430">1.00</span><span class="sxs-lookup"><span data-stu-id="19b11-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="19b11-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-433">Cost element</span></span></th>
<th><span data-ttu-id="19b11-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-434">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-435">Amount</span></span></th>
<th><span data-ttu-id="19b11-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="19b11-437">CC0001</span></span></td>
<td><span data-ttu-id="19b11-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-438">HR</span></span></td>
<td><span data-ttu-id="19b11-439">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-439">10001</span></span></td>
<td><span data-ttu-id="19b11-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-440">Electricity</span></span></td>
<td><span data-ttu-id="19b11-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-441">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="19b11-442">-30.00</span></span></td>
<td><span data-ttu-id="19b11-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-444">Proj 1</span></span></td>
<td><span data-ttu-id="19b11-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="19b11-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="19b11-446">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-446">10001</span></span></td>
<td><span data-ttu-id="19b11-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-447">Electricity</span></span></td>
<td><span data-ttu-id="19b11-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-448">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-449">30.00</span><span class="sxs-lookup"><span data-stu-id="19b11-449">30.00</span></span></td>
<td><span data-ttu-id="19b11-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-451">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-451">CC001</span></span></td>
<td><span data-ttu-id="19b11-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-452">HR</span></span></td>
<td><span data-ttu-id="19b11-453">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-453">10001</span></span></td>
<td><span data-ttu-id="19b11-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-454">Electricity</span></span></td>
<td><span data-ttu-id="19b11-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-455">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="19b11-456">-10.00</span></span></td>
<td><span data-ttu-id="19b11-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-458">Proj 2</span></span></td>
<td><span data-ttu-id="19b11-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="19b11-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="19b11-460">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-460">10001</span></span></td>
<td><span data-ttu-id="19b11-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-461">Electricity</span></span></td>
<td><span data-ttu-id="19b11-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-462">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-463">10.00</span><span class="sxs-lookup"><span data-stu-id="19b11-463">10.00</span></span></td>
<td><span data-ttu-id="19b11-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="19b11-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="19b11-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="19b11-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="19b11-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="19b11-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="19b11-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="19b11-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="19b11-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="19b11-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="19b11-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="19b11-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="19b11-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="19b11-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="19b11-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="19b11-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="19b11-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="19b11-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="19b11-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-475">Define the cost allocation</span></span>

<span data-ttu-id="19b11-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="19b11-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="19b11-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="19b11-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-479">Cost object</span></span></th>
<th><span data-ttu-id="19b11-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-481">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-481">CC002</span></span></td>
<td><span data-ttu-id="19b11-482">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-482">Finance</span></span></td>
<td><span data-ttu-id="19b11-483">35</span><span class="sxs-lookup"><span data-stu-id="19b11-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-484">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-484">CC003</span></span></td>
<td><span data-ttu-id="19b11-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-485">Assembly</span></span></td>
<td><span data-ttu-id="19b11-486">55</span><span class="sxs-lookup"><span data-stu-id="19b11-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-487">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-487">CC004</span></span></td>
<td><span data-ttu-id="19b11-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-488">Packaging</span></span></td>
<td><span data-ttu-id="19b11-489">10</span><span class="sxs-lookup"><span data-stu-id="19b11-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="19b11-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="19b11-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-492">Cost object</span></span></th>
<th><span data-ttu-id="19b11-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-494">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-494">CC003</span></span></td>
<td><span data-ttu-id="19b11-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-495">Assembly</span></span></td>
<td><span data-ttu-id="19b11-496">65</span><span class="sxs-lookup"><span data-stu-id="19b11-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-497">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-497">CC004</span></span></td>
<td><span data-ttu-id="19b11-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-498">Packaging</span></span></td>
<td><span data-ttu-id="19b11-499">35</span><span class="sxs-lookup"><span data-stu-id="19b11-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="19b11-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="19b11-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-502">Cost object</span></span></th>
<th><span data-ttu-id="19b11-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="19b11-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-504">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-505">Product 1</span></span></td>
<td><span data-ttu-id="19b11-506">60</span><span class="sxs-lookup"><span data-stu-id="19b11-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-507">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-508">Product 2</span></span></td>
<td><span data-ttu-id="19b11-509">20</span><span class="sxs-lookup"><span data-stu-id="19b11-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="19b11-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="19b11-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-512">Cost object</span></span></th>
<th><span data-ttu-id="19b11-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="19b11-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-514">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-515">Product 1</span></span></td>
<td><span data-ttu-id="19b11-516">80</span><span class="sxs-lookup"><span data-stu-id="19b11-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-517">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-518">Product 2</span></span></td>
<td><span data-ttu-id="19b11-519">15</span><span class="sxs-lookup"><span data-stu-id="19b11-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="19b11-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="19b11-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="19b11-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="19b11-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="19b11-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="19b11-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-523">Cost object</span></span></th>
<th><span data-ttu-id="19b11-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-524">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-525">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-526">Amount</span></span></th>
<th><span data-ttu-id="19b11-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-528">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-528">CC002</span></span></td>
<td><span data-ttu-id="19b11-529">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-529">Finance</span></span></td>
<td><span data-ttu-id="19b11-530">35</span><span class="sxs-lookup"><span data-stu-id="19b11-530">35</span></span></td>
<td><span data-ttu-id="19b11-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="19b11-532">175.00</span><span class="sxs-lookup"><span data-stu-id="19b11-532">175.00</span></span></td>
<td><span data-ttu-id="19b11-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-534">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-534">CC003</span></span></td>
<td><span data-ttu-id="19b11-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-535">Assembly</span></span></td>
<td><span data-ttu-id="19b11-536">55</span><span class="sxs-lookup"><span data-stu-id="19b11-536">55</span></span></td>
<td><span data-ttu-id="19b11-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="19b11-538">275.00</span><span class="sxs-lookup"><span data-stu-id="19b11-538">275.00</span></span></td>
<td><span data-ttu-id="19b11-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-540">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-540">CC004</span></span></td>
<td><span data-ttu-id="19b11-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-541">Packaging</span></span></td>
<td><span data-ttu-id="19b11-542">10</span><span class="sxs-lookup"><span data-stu-id="19b11-542">10</span></span></td>
<td><span data-ttu-id="19b11-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="19b11-544">50.00</span><span class="sxs-lookup"><span data-stu-id="19b11-544">50.00</span></span></td>
<td><span data-ttu-id="19b11-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-546">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-546">CC002</span></span></td>
<td><span data-ttu-id="19b11-547">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-547">Finance</span></span></td>
<td><span data-ttu-id="19b11-548">35</span><span class="sxs-lookup"><span data-stu-id="19b11-548">35</span></span></td>
<td><span data-ttu-id="19b11-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="19b11-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="19b11-550">436.00</span><span class="sxs-lookup"><span data-stu-id="19b11-550">436.00</span></span></td>
<td><span data-ttu-id="19b11-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-552">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-552">CC003</span></span></td>
<td><span data-ttu-id="19b11-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-553">Assembly</span></span></td>
<td><span data-ttu-id="19b11-554">55</span><span class="sxs-lookup"><span data-stu-id="19b11-554">55</span></span></td>
<td><span data-ttu-id="19b11-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="19b11-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="19b11-556">685.14</span><span class="sxs-lookup"><span data-stu-id="19b11-556">685.14</span></span></td>
<td><span data-ttu-id="19b11-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-558">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-558">CC004</span></span></td>
<td><span data-ttu-id="19b11-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-559">Packaging</span></span></td>
<td><span data-ttu-id="19b11-560">10</span><span class="sxs-lookup"><span data-stu-id="19b11-560">10</span></span></td>
<td><span data-ttu-id="19b11-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="19b11-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="19b11-562">124.57</span><span class="sxs-lookup"><span data-stu-id="19b11-562">124.57</span></span></td>
<td><span data-ttu-id="19b11-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="19b11-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-565">Cost object</span></span></th>
<th><span data-ttu-id="19b11-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-566">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-567">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-568">Amount</span></span></th>
<th><span data-ttu-id="19b11-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-570">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-570">CC003</span></span></td>
<td><span data-ttu-id="19b11-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-571">Assembly</span></span></td>
<td><span data-ttu-id="19b11-572">65</span><span class="sxs-lookup"><span data-stu-id="19b11-572">65</span></span></td>
<td><span data-ttu-id="19b11-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="19b11-574">438.75</span><span class="sxs-lookup"><span data-stu-id="19b11-574">438.75</span></span></td>
<td><span data-ttu-id="19b11-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-576">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-576">CC004</span></span></td>
<td><span data-ttu-id="19b11-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-577">Packaging</span></span></td>
<td><span data-ttu-id="19b11-578">35</span><span class="sxs-lookup"><span data-stu-id="19b11-578">35</span></span></td>
<td><span data-ttu-id="19b11-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="19b11-580">236.25</span><span class="sxs-lookup"><span data-stu-id="19b11-580">236.25</span></span></td>
<td><span data-ttu-id="19b11-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-582">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-582">CC003</span></span></td>
<td><span data-ttu-id="19b11-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-583">Assembly</span></span></td>
<td><span data-ttu-id="19b11-584">65</span><span class="sxs-lookup"><span data-stu-id="19b11-584">65</span></span></td>
<td><span data-ttu-id="19b11-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="19b11-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="19b11-586">5,297.69</span></span></td>
<td><span data-ttu-id="19b11-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-588">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-588">CC004</span></span></td>
<td><span data-ttu-id="19b11-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-589">Packaging</span></span></td>
<td><span data-ttu-id="19b11-590">35</span><span class="sxs-lookup"><span data-stu-id="19b11-590">35</span></span></td>
<td><span data-ttu-id="19b11-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="19b11-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="19b11-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="19b11-592">2,852.60</span></span></td>
<td><span data-ttu-id="19b11-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="19b11-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-595">Cost object</span></span></th>
<th><span data-ttu-id="19b11-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-596">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-597">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-598">Amount</span></span></th>
<th><span data-ttu-id="19b11-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-600">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-601">Product 1</span></span></td>
<td><span data-ttu-id="19b11-602">60</span><span class="sxs-lookup"><span data-stu-id="19b11-602">60</span></span></td>
<td><span data-ttu-id="19b11-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="19b11-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="19b11-604">535.31</span><span class="sxs-lookup"><span data-stu-id="19b11-604">535.31</span></span></td>
<td><span data-ttu-id="19b11-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-606">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-607">Product 2</span></span></td>
<td><span data-ttu-id="19b11-608">20</span><span class="sxs-lookup"><span data-stu-id="19b11-608">20</span></span></td>
<td><span data-ttu-id="19b11-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="19b11-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="19b11-610">178.44</span><span class="sxs-lookup"><span data-stu-id="19b11-610">178.44</span></span></td>
<td><span data-ttu-id="19b11-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-612">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-613">Product 1</span></span></td>
<td><span data-ttu-id="19b11-614">60</span><span class="sxs-lookup"><span data-stu-id="19b11-614">60</span></span></td>
<td><span data-ttu-id="19b11-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="19b11-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="19b11-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="19b11-616">4,487.12</span></span></td>
<td><span data-ttu-id="19b11-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-618">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-619">Product 2</span></span></td>
<td><span data-ttu-id="19b11-620">20</span><span class="sxs-lookup"><span data-stu-id="19b11-620">20</span></span></td>
<td><span data-ttu-id="19b11-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="19b11-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="19b11-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="19b11-622">1,495.71</span></span></td>
<td><span data-ttu-id="19b11-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="19b11-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="19b11-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-625">Cost object</span></span></th>
<th><span data-ttu-id="19b11-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="19b11-626">Magnitude</span></span></th>
<th><span data-ttu-id="19b11-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="19b11-627">Allocation factor</span></span></th>
<th><span data-ttu-id="19b11-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-628">Amount</span></span></th>
<th><span data-ttu-id="19b11-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-630">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-631">Product 1</span></span></td>
<td><span data-ttu-id="19b11-632">80</span><span class="sxs-lookup"><span data-stu-id="19b11-632">80</span></span></td>
<td><span data-ttu-id="19b11-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="19b11-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="19b11-634">241.05</span><span class="sxs-lookup"><span data-stu-id="19b11-634">241.05</span></span></td>
<td><span data-ttu-id="19b11-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-636">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-637">Product 2</span></span></td>
<td><span data-ttu-id="19b11-638">15</span><span class="sxs-lookup"><span data-stu-id="19b11-638">15</span></span></td>
<td><span data-ttu-id="19b11-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="19b11-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="19b11-640">45.20</span><span class="sxs-lookup"><span data-stu-id="19b11-640">45.20</span></span></td>
<td><span data-ttu-id="19b11-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-642">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-643">Product 1</span></span></td>
<td><span data-ttu-id="19b11-644">80</span><span class="sxs-lookup"><span data-stu-id="19b11-644">80</span></span></td>
<td><span data-ttu-id="19b11-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="19b11-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="19b11-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="19b11-646">2,507.09</span></span></td>
<td><span data-ttu-id="19b11-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-648">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-649">Product 2</span></span></td>
<td><span data-ttu-id="19b11-650">15</span><span class="sxs-lookup"><span data-stu-id="19b11-650">15</span></span></td>
<td><span data-ttu-id="19b11-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="19b11-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="19b11-652">470.08</span><span class="sxs-lookup"><span data-stu-id="19b11-652">470.08</span></span></td>
<td><span data-ttu-id="19b11-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="19b11-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="19b11-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="19b11-655">Journal</span></span></th>
<th><span data-ttu-id="19b11-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="19b11-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="19b11-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="19b11-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="19b11-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="19b11-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-659">00004</span><span class="sxs-lookup"><span data-stu-id="19b11-659">00004</span></span></td>
<td><span data-ttu-id="19b11-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="19b11-661">مالي</span><span class="sxs-lookup"><span data-stu-id="19b11-661">Fiscal</span></span></td>
<td><span data-ttu-id="19b11-662">2017</span><span class="sxs-lookup"><span data-stu-id="19b11-662">2017</span></span></td>
<td><span data-ttu-id="19b11-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-663">Period 1</span></span></td>
<td><span data-ttu-id="19b11-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="19b11-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="19b11-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="19b11-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19b11-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-668">Cost element</span></span></th>
<th><span data-ttu-id="19b11-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-669">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-672">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-672">CC001</span></span></td>
<td><span data-ttu-id="19b11-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-673">HR</span></span></td>
<td><span data-ttu-id="19b11-674">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-674">10001</span></span></td>
<td><span data-ttu-id="19b11-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-675">Electricity</span></span></td>
<td><span data-ttu-id="19b11-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-676">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-677">500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-679">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-679">CC001</span></span></td>
<td><span data-ttu-id="19b11-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-680">HR</span></span></td>
<td><span data-ttu-id="19b11-681">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-681">10001</span></span></td>
<td><span data-ttu-id="19b11-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-682">Electricity</span></span></td>
<td><span data-ttu-id="19b11-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-683">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="19b11-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-686">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-686">CC002</span></span></td>
<td><span data-ttu-id="19b11-687">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-687">Finance</span></span></td>
<td><span data-ttu-id="19b11-688">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-688">10001</span></span></td>
<td><span data-ttu-id="19b11-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-689">Electricity</span></span></td>
<td><span data-ttu-id="19b11-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-690">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-691">675.00</span><span class="sxs-lookup"><span data-stu-id="19b11-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-693">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-693">CC002</span></span></td>
<td><span data-ttu-id="19b11-694">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-694">Finance</span></span></td>
<td><span data-ttu-id="19b11-695">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-695">10001</span></span></td>
<td><span data-ttu-id="19b11-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-696">Electricity</span></span></td>
<td><span data-ttu-id="19b11-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-697">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="19b11-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-700">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-700">CC003</span></span></td>
<td><span data-ttu-id="19b11-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-701">Assembly</span></span></td>
<td><span data-ttu-id="19b11-702">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-702">10001</span></span></td>
<td><span data-ttu-id="19b11-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-703">Electricity</span></span></td>
<td><span data-ttu-id="19b11-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-704">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-705">713.75</span><span class="sxs-lookup"><span data-stu-id="19b11-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-707">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-707">CC003</span></span></td>
<td><span data-ttu-id="19b11-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-708">Assembly</span></span></td>
<td><span data-ttu-id="19b11-709">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-709">10001</span></span></td>
<td><span data-ttu-id="19b11-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-710">Electricity</span></span></td>
<td><span data-ttu-id="19b11-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-711">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="19b11-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-714">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-714">CC003</span></span></td>
<td><span data-ttu-id="19b11-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-715">Packaging</span></span></td>
<td><span data-ttu-id="19b11-716">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-716">10001</span></span></td>
<td><span data-ttu-id="19b11-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-717">Electricity</span></span></td>
<td><span data-ttu-id="19b11-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-718">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-719">286.25</span><span class="sxs-lookup"><span data-stu-id="19b11-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-721">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-721">CC003</span></span></td>
<td><span data-ttu-id="19b11-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-722">Packaging</span></span></td>
<td><span data-ttu-id="19b11-723">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-723">10001</span></span></td>
<td><span data-ttu-id="19b11-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-724">Electricity</span></span></td>
<td><span data-ttu-id="19b11-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-725">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="19b11-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-728">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-729">Product 1</span></span></td>
<td><span data-ttu-id="19b11-730">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-730">10001</span></span></td>
<td><span data-ttu-id="19b11-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-731">Electricity</span></span></td>
<td><span data-ttu-id="19b11-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-732">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-733">776.36</span><span class="sxs-lookup"><span data-stu-id="19b11-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-735">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-736">Product 1</span></span></td>
<td><span data-ttu-id="19b11-737">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-737">10001</span></span></td>
<td><span data-ttu-id="19b11-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-738">Electricity</span></span></td>
<td><span data-ttu-id="19b11-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-739">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="19b11-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-742">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-743">Product 1</span></span></td>
<td><span data-ttu-id="19b11-744">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-744">10001</span></span></td>
<td><span data-ttu-id="19b11-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-745">Electricity</span></span></td>
<td><span data-ttu-id="19b11-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-746">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-747">223.64</span><span class="sxs-lookup"><span data-stu-id="19b11-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="19b11-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-749">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-750">Product 1</span></span></td>
<td><span data-ttu-id="19b11-751">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-751">10001</span></span></td>
<td><span data-ttu-id="19b11-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-752">Electricity</span></span></td>
<td><span data-ttu-id="19b11-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-753">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="19b11-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="19b11-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="19b11-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="19b11-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-757">Cost element</span></span></th>
<th><span data-ttu-id="19b11-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-758">Cost behavior</span></span></th>
<th><span data-ttu-id="19b11-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="19b11-759">Amount</span></span></th>
<th><span data-ttu-id="19b11-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="19b11-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19b11-761">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-761">CC001</span></span></td>
<td><span data-ttu-id="19b11-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-762">HR</span></span></td>
<td><span data-ttu-id="19b11-763">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-763">10001</span></span></td>
<td><span data-ttu-id="19b11-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-764">Electricity</span></span></td>
<td><span data-ttu-id="19b11-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-765">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="19b11-766">-500.00</span></span></td>
<td><span data-ttu-id="19b11-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-768">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-768">CC002</span></span></td>
<td><span data-ttu-id="19b11-769">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-769">Finance</span></span></td>
<td><span data-ttu-id="19b11-770">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-770">10001</span></span></td>
<td><span data-ttu-id="19b11-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-771">Electricity</span></span></td>
<td><span data-ttu-id="19b11-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-772">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-773">175.00</span><span class="sxs-lookup"><span data-stu-id="19b11-773">175.00</span></span></td>
<td><span data-ttu-id="19b11-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-775">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-775">CC003</span></span></td>
<td><span data-ttu-id="19b11-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-776">Assembly</span></span></td>
<td><span data-ttu-id="19b11-777">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-777">10001</span></span></td>
<td><span data-ttu-id="19b11-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-778">Electricity</span></span></td>
<td><span data-ttu-id="19b11-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-779">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-780">275.00</span><span class="sxs-lookup"><span data-stu-id="19b11-780">275.00</span></span></td>
<td><span data-ttu-id="19b11-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-782">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-782">CC004</span></span></td>
<td><span data-ttu-id="19b11-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-783">Packaging</span></span></td>
<td><span data-ttu-id="19b11-784">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-784">10001</span></span></td>
<td><span data-ttu-id="19b11-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-785">Electricity</span></span></td>
<td><span data-ttu-id="19b11-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-786">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-787">50,00</span><span class="sxs-lookup"><span data-stu-id="19b11-787">50,00</span></span></td>
<td><span data-ttu-id="19b11-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-789">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-789">CC001</span></span></td>
<td><span data-ttu-id="19b11-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="19b11-790">HR</span></span></td>
<td><span data-ttu-id="19b11-791">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-791">10001</span></span></td>
<td><span data-ttu-id="19b11-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-792">Electricity</span></span></td>
<td><span data-ttu-id="19b11-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-793">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="19b11-794">-1,245.71</span></span></td>
<td><span data-ttu-id="19b11-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-796">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-796">CC002</span></span></td>
<td><span data-ttu-id="19b11-797">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-797">Finance</span></span></td>
<td><span data-ttu-id="19b11-798">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-798">10001</span></span></td>
<td><span data-ttu-id="19b11-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-799">Electricity</span></span></td>
<td><span data-ttu-id="19b11-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-800">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-801">436.00</span><span class="sxs-lookup"><span data-stu-id="19b11-801">436.00</span></span></td>
<td><span data-ttu-id="19b11-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-803">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-803">CC003</span></span></td>
<td><span data-ttu-id="19b11-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-804">Assembly</span></span></td>
<td><span data-ttu-id="19b11-805">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-805">10001</span></span></td>
<td><span data-ttu-id="19b11-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-806">Electricity</span></span></td>
<td><span data-ttu-id="19b11-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-807">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-808">685.14</span><span class="sxs-lookup"><span data-stu-id="19b11-808">685.14</span></span></td>
<td><span data-ttu-id="19b11-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-810">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-810">CC004</span></span></td>
<td><span data-ttu-id="19b11-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-811">Packaging</span></span></td>
<td><span data-ttu-id="19b11-812">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-812">10001</span></span></td>
<td><span data-ttu-id="19b11-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-813">Electricity</span></span></td>
<td><span data-ttu-id="19b11-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-814">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-815">124.57</span><span class="sxs-lookup"><span data-stu-id="19b11-815">124.57</span></span></td>
<td><span data-ttu-id="19b11-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-817">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-817">CC002</span></span></td>
<td><span data-ttu-id="19b11-818">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-818">Finance</span></span></td>
<td><span data-ttu-id="19b11-819">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-819">10001</span></span></td>
<td><span data-ttu-id="19b11-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-820">Electricity</span></span></td>
<td><span data-ttu-id="19b11-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-821">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="19b11-822">-675.00</span></span></td>
<td><span data-ttu-id="19b11-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-824">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-824">CC003</span></span></td>
<td><span data-ttu-id="19b11-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-825">Assembly</span></span></td>
<td><span data-ttu-id="19b11-826">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-826">10001</span></span></td>
<td><span data-ttu-id="19b11-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-827">Electricity</span></span></td>
<td><span data-ttu-id="19b11-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-828">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-829">438.75</span><span class="sxs-lookup"><span data-stu-id="19b11-829">438.75</span></span></td>
<td><span data-ttu-id="19b11-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-831">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-831">CC004</span></span></td>
<td><span data-ttu-id="19b11-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-832">Packaging</span></span></td>
<td><span data-ttu-id="19b11-833">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-833">10001</span></span></td>
<td><span data-ttu-id="19b11-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-834">Electricity</span></span></td>
<td><span data-ttu-id="19b11-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-835">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-836">236.25</span><span class="sxs-lookup"><span data-stu-id="19b11-836">236.25</span></span></td>
<td><span data-ttu-id="19b11-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-838">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-838">CC002</span></span></td>
<td><span data-ttu-id="19b11-839">المالية</span><span class="sxs-lookup"><span data-stu-id="19b11-839">Finance</span></span></td>
<td><span data-ttu-id="19b11-840">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-840">10001</span></span></td>
<td><span data-ttu-id="19b11-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-841">Electricity</span></span></td>
<td><span data-ttu-id="19b11-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-842">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="19b11-843">-8,150.29</span></span></td>
<td><span data-ttu-id="19b11-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-845">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-845">CC003</span></span></td>
<td><span data-ttu-id="19b11-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-846">Assembly</span></span></td>
<td><span data-ttu-id="19b11-847">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-847">10001</span></span></td>
<td><span data-ttu-id="19b11-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-848">Electricity</span></span></td>
<td><span data-ttu-id="19b11-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-849">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="19b11-850">5,297.69</span></span></td>
<td><span data-ttu-id="19b11-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-852">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-852">CC004</span></span></td>
<td><span data-ttu-id="19b11-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="19b11-853">Packaging</span></span></td>
<td><span data-ttu-id="19b11-854">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-854">10001</span></span></td>
<td><span data-ttu-id="19b11-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-855">Electricity</span></span></td>
<td><span data-ttu-id="19b11-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-856">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="19b11-857">2,852.60</span></span></td>
<td><span data-ttu-id="19b11-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-859">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-859">CC003</span></span></td>
<td><span data-ttu-id="19b11-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-860">Assembly</span></span></td>
<td><span data-ttu-id="19b11-861">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-861">10001</span></span></td>
<td><span data-ttu-id="19b11-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-862">Electricity</span></span></td>
<td><span data-ttu-id="19b11-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-863">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="19b11-864">-713.75</span></span></td>
<td><span data-ttu-id="19b11-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-866">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-867">Product 1</span></span></td>
<td><span data-ttu-id="19b11-868">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-868">10001</span></span></td>
<td><span data-ttu-id="19b11-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-869">Electricity</span></span></td>
<td><span data-ttu-id="19b11-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-870">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-871">535.31</span><span class="sxs-lookup"><span data-stu-id="19b11-871">535.31</span></span></td>
<td><span data-ttu-id="19b11-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-873">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-874">Product 2</span></span></td>
<td><span data-ttu-id="19b11-875">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-875">10001</span></span></td>
<td><span data-ttu-id="19b11-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-876">Electricity</span></span></td>
<td><span data-ttu-id="19b11-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-877">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-878">178.44</span><span class="sxs-lookup"><span data-stu-id="19b11-878">178.44</span></span></td>
<td><span data-ttu-id="19b11-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-880">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-880">CC003</span></span></td>
<td><span data-ttu-id="19b11-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-881">Assembly</span></span></td>
<td><span data-ttu-id="19b11-882">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-882">10001</span></span></td>
<td><span data-ttu-id="19b11-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-883">Electricity</span></span></td>
<td><span data-ttu-id="19b11-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-884">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="19b11-885">-5,982.83</span></span></td>
<td><span data-ttu-id="19b11-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-887">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-888">Product 1</span></span></td>
<td><span data-ttu-id="19b11-889">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-889">10001</span></span></td>
<td><span data-ttu-id="19b11-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-890">Electricity</span></span></td>
<td><span data-ttu-id="19b11-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-891">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="19b11-892">4,487.12</span></span></td>
<td><span data-ttu-id="19b11-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-894">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-895">Product 2</span></span></td>
<td><span data-ttu-id="19b11-896">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-896">10001</span></span></td>
<td><span data-ttu-id="19b11-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-897">Electricity</span></span></td>
<td><span data-ttu-id="19b11-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-898">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="19b11-899">1,495.71</span></span></td>
<td><span data-ttu-id="19b11-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-901">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-901">CC003</span></span></td>
<td><span data-ttu-id="19b11-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-902">Assembly</span></span></td>
<td><span data-ttu-id="19b11-903">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-903">10001</span></span></td>
<td><span data-ttu-id="19b11-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-904">Electricity</span></span></td>
<td><span data-ttu-id="19b11-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-905">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="19b11-906">-286.25</span></span></td>
<td><span data-ttu-id="19b11-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-908">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-909">Product 1</span></span></td>
<td><span data-ttu-id="19b11-910">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-910">10001</span></span></td>
<td><span data-ttu-id="19b11-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-911">Electricity</span></span></td>
<td><span data-ttu-id="19b11-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-912">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-913">241.05</span><span class="sxs-lookup"><span data-stu-id="19b11-913">241.05</span></span></td>
<td><span data-ttu-id="19b11-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-915">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-916">Product 2</span></span></td>
<td><span data-ttu-id="19b11-917">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-917">10001</span></span></td>
<td><span data-ttu-id="19b11-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-918">Electricity</span></span></td>
<td><span data-ttu-id="19b11-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-919">Fixed cost</span></span></td>
<td><span data-ttu-id="19b11-920">45.20</span><span class="sxs-lookup"><span data-stu-id="19b11-920">45.20</span></span></td>
<td><span data-ttu-id="19b11-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-922">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-922">CC003</span></span></td>
<td><span data-ttu-id="19b11-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="19b11-923">Assembly</span></span></td>
<td><span data-ttu-id="19b11-924">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-924">10001</span></span></td>
<td><span data-ttu-id="19b11-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-925">Electricity</span></span></td>
<td><span data-ttu-id="19b11-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-926">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="19b11-927">-2,977.17</span></span></td>
<td><span data-ttu-id="19b11-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-929">Prod 1</span></span></td>
<td><span data-ttu-id="19b11-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-930">Product 1</span></span></td>
<td><span data-ttu-id="19b11-931">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-931">10001</span></span></td>
<td><span data-ttu-id="19b11-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-932">Electricity</span></span></td>
<td><span data-ttu-id="19b11-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-933">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="19b11-934">2,507.09</span></span></td>
<td><span data-ttu-id="19b11-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19b11-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-936">Prod 2</span></span></td>
<td><span data-ttu-id="19b11-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-937">Product 2</span></span></td>
<td><span data-ttu-id="19b11-938">10001</span><span class="sxs-lookup"><span data-stu-id="19b11-938">10001</span></span></td>
<td><span data-ttu-id="19b11-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-939">Electricity</span></span></td>
<td><span data-ttu-id="19b11-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-940">Variable cost</span></span></td>
<td><span data-ttu-id="19b11-941">470.08</span><span class="sxs-lookup"><span data-stu-id="19b11-941">470.08</span></span></td>
<td><span data-ttu-id="19b11-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="19b11-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="19b11-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="19b11-943">Conclusion</span></span>
<span data-ttu-id="19b11-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="19b11-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="19b11-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="19b11-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="19b11-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="19b11-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="19b11-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="19b11-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="19b11-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="19b11-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="19b11-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="19b11-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="19b11-951">CC099</span><span class="sxs-lookup"><span data-stu-id="19b11-951">CC099</span></span></th>
<th><span data-ttu-id="19b11-952">CC001</span><span class="sxs-lookup"><span data-stu-id="19b11-952">CC001</span></span></th>
<th><span data-ttu-id="19b11-953">CC002</span><span class="sxs-lookup"><span data-stu-id="19b11-953">CC002</span></span></th>
<th><span data-ttu-id="19b11-954">CC003</span><span class="sxs-lookup"><span data-stu-id="19b11-954">CC003</span></span></th>
<th><span data-ttu-id="19b11-955">CC004</span><span class="sxs-lookup"><span data-stu-id="19b11-955">CC004</span></span></th>
<th><span data-ttu-id="19b11-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="19b11-956">Proj 1</span></span></th>
<th><span data-ttu-id="19b11-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="19b11-957">Proj 2</span></span></th>
<th><span data-ttu-id="19b11-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="19b11-958">Prod 1</span></span></th>
<th><span data-ttu-id="19b11-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="19b11-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="19b11-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="19b11-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="19b11-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="19b11-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="19b11-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-971">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="19b11-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="19b11-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-973">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-974">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-975">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-976">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-977">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="19b11-978">776.36</span><span class="sxs-lookup"><span data-stu-id="19b11-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-979">223.64</span><span class="sxs-lookup"><span data-stu-id="19b11-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="19b11-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="19b11-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-982">000</span><span class="sxs-lookup"><span data-stu-id="19b11-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-983">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-984">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-985">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-986">0.00</span><span class="sxs-lookup"><span data-stu-id="19b11-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-987">30.00</span><span class="sxs-lookup"><span data-stu-id="19b11-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-988">10.00</span><span class="sxs-lookup"><span data-stu-id="19b11-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="19b11-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="19b11-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="19b11-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="19b11-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="19b11-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="19b11-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="19b11-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="19b11-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="19b11-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="19b11-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="19b11-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="19b11-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



