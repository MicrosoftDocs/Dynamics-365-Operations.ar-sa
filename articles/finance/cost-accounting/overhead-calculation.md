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
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208837"
---
# <a name="overhead-calculation"></a><span data-ttu-id="f1cec-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="f1cec-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1cec-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="f1cec-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="f1cec-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="f1cec-105">Term definition</span></span>
---------------

<span data-ttu-id="f1cec-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="f1cec-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="f1cec-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="f1cec-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="f1cec-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="f1cec-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="f1cec-109">Rent</span></span>
-   <span data-ttu-id="f1cec-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-110">Electricity</span></span>
-   <span data-ttu-id="f1cec-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="f1cec-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="f1cec-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="f1cec-112">Overhead calculation overview</span></span>
<span data-ttu-id="f1cec-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="f1cec-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="f1cec-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="f1cec-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="f1cec-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="f1cec-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="f1cec-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="f1cec-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="f1cec-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="f1cec-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="f1cec-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-119">Version type</span></span>
-   <span data-ttu-id="f1cec-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="f1cec-120">Date and time</span></span>
-   <span data-ttu-id="f1cec-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="f1cec-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="f1cec-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-122">Fiscal year</span></span>
-   <span data-ttu-id="f1cec-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-123">Fiscal period</span></span>

<span data-ttu-id="f1cec-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="f1cec-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="f1cec-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="f1cec-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="f1cec-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f1cec-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="f1cec-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="f1cec-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="f1cec-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="f1cec-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="f1cec-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="f1cec-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="f1cec-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="f1cec-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="f1cec-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="f1cec-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="f1cec-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="f1cec-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="f1cec-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="f1cec-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="f1cec-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="f1cec-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="f1cec-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="f1cec-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="f1cec-140">Main account</span></span></th>
<th><span data-ttu-id="f1cec-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="f1cec-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="f1cec-143">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-143">CC099</span></span></td>
<td><span data-ttu-id="f1cec-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-144">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-145">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-145">10001</span></span></td>
<td><span data-ttu-id="f1cec-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-146">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="f1cec-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="f1cec-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="f1cec-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="f1cec-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="f1cec-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="f1cec-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-151">Define the cost behavior rule</span></span>

<span data-ttu-id="f1cec-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="f1cec-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="f1cec-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="f1cec-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="f1cec-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="f1cec-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="f1cec-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="f1cec-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="f1cec-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="f1cec-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="f1cec-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="f1cec-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="f1cec-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="f1cec-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-160">Journal</span></span></th>
<th><span data-ttu-id="f1cec-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f1cec-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f1cec-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-164">00001</span><span class="sxs-lookup"><span data-stu-id="f1cec-164">00001</span></span></td>
<td><span data-ttu-id="f1cec-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="f1cec-166">مالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-166">Fiscal</span></span></td>
<td><span data-ttu-id="f1cec-167">2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-167">2017</span></span></td>
<td><span data-ttu-id="f1cec-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-168">Period 1</span></span></td>
<td><span data-ttu-id="f1cec-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f1cec-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="f1cec-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-173">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-174">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="f1cec-177">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-177">CC099</span></span></td>
<td><span data-ttu-id="f1cec-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-178">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-179">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-179">10001</span></span></td>
<td><span data-ttu-id="f1cec-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-180">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="f1cec-181">Unclassified</span></span></td>
<td><span data-ttu-id="f1cec-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f1cec-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-185">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-186">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-187">Amount</span></span></th>
<th><span data-ttu-id="f1cec-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-189">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-189">CC099</span></span></td>
<td><span data-ttu-id="f1cec-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-190">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-191">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-191">10001</span></span></td>
<td><span data-ttu-id="f1cec-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-192">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="f1cec-193">Unclassified</span></span></td>
<td><span data-ttu-id="f1cec-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-194">10,000.00</span></span></td>
<td><span data-ttu-id="f1cec-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-196">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-196">CC099</span></span></td>
<td><span data-ttu-id="f1cec-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-197">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-198">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-198">10001</span></span></td>
<td><span data-ttu-id="f1cec-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-199">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="f1cec-200">Unclassified</span></span></td>
<td><span data-ttu-id="f1cec-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-201">-10,000.00</span></span></td>
<td><span data-ttu-id="f1cec-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-203">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-203">CC099</span></span></td>
<td><span data-ttu-id="f1cec-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-204">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-205">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-205">10001</span></span></td>
<td><span data-ttu-id="f1cec-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-206">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-207">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-208">1,000.00</span></span></td>
<td><span data-ttu-id="f1cec-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-210">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-210">CC099</span></span></td>
<td><span data-ttu-id="f1cec-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-211">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-212">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-212">10001</span></span></td>
<td><span data-ttu-id="f1cec-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-213">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-214">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-215">9,000.00</span></span></td>
<td><span data-ttu-id="f1cec-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="f1cec-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="f1cec-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="f1cec-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="f1cec-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="f1cec-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="f1cec-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-221">Define the cost distribution rule</span></span>

<span data-ttu-id="f1cec-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="f1cec-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="f1cec-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="f1cec-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="f1cec-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="f1cec-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="f1cec-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="f1cec-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="f1cec-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="f1cec-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="f1cec-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-228">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="f1cec-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-230">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-230">CC001</span></span></td>
<td><span data-ttu-id="f1cec-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-231">HR</span></span></td>
<td><span data-ttu-id="f1cec-232">1,000</span><span class="sxs-lookup"><span data-stu-id="f1cec-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-233">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-233">CC002</span></span></td>
<td><span data-ttu-id="f1cec-234">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-234">Finance</span></span></td>
<td><span data-ttu-id="f1cec-235">6,000</span><span class="sxs-lookup"><span data-stu-id="f1cec-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-236">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-236">CC003</span></span></td>
<td><span data-ttu-id="f1cec-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-237">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-238">0</span><span class="sxs-lookup"><span data-stu-id="f1cec-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-240">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-241">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-242">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-244">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-244">CC001</span></span></td>
<td><span data-ttu-id="f1cec-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-245">HR</span></span></td>
<td><span data-ttu-id="f1cec-246">1,000</span><span class="sxs-lookup"><span data-stu-id="f1cec-246">1,000</span></span></td>
<td><span data-ttu-id="f1cec-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f1cec-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-249">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-249">CC002</span></span></td>
<td><span data-ttu-id="f1cec-250">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-250">Finance</span></span></td>
<td><span data-ttu-id="f1cec-251">6,000</span><span class="sxs-lookup"><span data-stu-id="f1cec-251">6,000</span></span></td>
<td><span data-ttu-id="f1cec-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f1cec-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f1cec-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-254">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-254">CC003</span></span></td>
<td><span data-ttu-id="f1cec-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-255">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-256">0</span><span class="sxs-lookup"><span data-stu-id="f1cec-256">0</span></span></td>
<td><span data-ttu-id="f1cec-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f1cec-258">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="f1cec-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="f1cec-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-261">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="f1cec-262">Formula</span></span></th>
<th><span data-ttu-id="f1cec-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-263">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-264">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-266">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-266">CC001</span></span></td>
<td><span data-ttu-id="f1cec-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-267">HR</span></span></td>
<td><span data-ttu-id="f1cec-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f1cec-269">1</span><span class="sxs-lookup"><span data-stu-id="f1cec-269">1</span></span></td>
<td><span data-ttu-id="f1cec-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f1cec-271">500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-272">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-272">CC002</span></span></td>
<td><span data-ttu-id="f1cec-273">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-273">Finance</span></span></td>
<td><span data-ttu-id="f1cec-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f1cec-275">1</span><span class="sxs-lookup"><span data-stu-id="f1cec-275">1</span></span></td>
<td><span data-ttu-id="f1cec-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f1cec-277">500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-278">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-278">CC003</span></span></td>
<td><span data-ttu-id="f1cec-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-279">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f1cec-281">0</span><span class="sxs-lookup"><span data-stu-id="f1cec-281">0</span></span></td>
<td><span data-ttu-id="f1cec-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f1cec-283">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f1cec-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-285">Journal</span></span></th>
<th><span data-ttu-id="f1cec-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f1cec-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f1cec-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-289">00002</span><span class="sxs-lookup"><span data-stu-id="f1cec-289">00002</span></span></td>
<td><span data-ttu-id="f1cec-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="f1cec-291">مالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-291">Fiscal</span></span></td>
<td><span data-ttu-id="f1cec-292">2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-292">2017</span></span></td>
<td><span data-ttu-id="f1cec-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-293">Period 1</span></span></td>
<td><span data-ttu-id="f1cec-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f1cec-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="f1cec-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-298">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-299">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-302">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-302">CC099</span></span></td>
<td><span data-ttu-id="f1cec-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-303">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-304">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-304">10001</span></span></td>
<td><span data-ttu-id="f1cec-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-305">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-306">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-309">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-309">CC099</span></span></td>
<td><span data-ttu-id="f1cec-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-310">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-311">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-311">10001</span></span></td>
<td><span data-ttu-id="f1cec-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-312">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-313">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f1cec-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-317">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-318">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-319">Amount</span></span></th>
<th><span data-ttu-id="f1cec-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-321">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-321">CC099</span></span></td>
<td><span data-ttu-id="f1cec-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-322">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-323">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-323">10001</span></span></td>
<td><span data-ttu-id="f1cec-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-324">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-325">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-326">-1,000.00</span></span></td>
<td><span data-ttu-id="f1cec-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-328">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-328">CC001</span></span></td>
<td><span data-ttu-id="f1cec-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-329">HR</span></span></td>
<td><span data-ttu-id="f1cec-330">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-330">10001</span></span></td>
<td><span data-ttu-id="f1cec-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-331">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-332">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-333">500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-333">500.00</span></span></td>
<td><span data-ttu-id="f1cec-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-335">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-335">CC002</span></span></td>
<td><span data-ttu-id="f1cec-336">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-336">Finance</span></span></td>
<td><span data-ttu-id="f1cec-337">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-337">10001</span></span></td>
<td><span data-ttu-id="f1cec-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-338">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-339">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-340">500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-340">500.00</span></span></td>
<td><span data-ttu-id="f1cec-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-342">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-342">CC099</span></span></td>
<td><span data-ttu-id="f1cec-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="f1cec-343">Default cost center</span></span></td>
<td><span data-ttu-id="f1cec-344">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-344">10001</span></span></td>
<td><span data-ttu-id="f1cec-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-345">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-346">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-347">-9,000.00</span></span></td>
<td><span data-ttu-id="f1cec-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-349">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-349">CC001</span></span></td>
<td><span data-ttu-id="f1cec-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-350">HR</span></span></td>
<td><span data-ttu-id="f1cec-351">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-351">10001</span></span></td>
<td><span data-ttu-id="f1cec-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-352">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-353">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-354">1,285.71</span></span></td>
<td><span data-ttu-id="f1cec-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-356">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-356">CC002</span></span></td>
<td><span data-ttu-id="f1cec-357">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-357">Finance</span></span></td>
<td><span data-ttu-id="f1cec-358">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-358">10001</span></span></td>
<td><span data-ttu-id="f1cec-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-359">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-360">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f1cec-361">7,714.29</span></span></td>
<td><span data-ttu-id="f1cec-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="f1cec-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="f1cec-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="f1cec-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="f1cec-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="f1cec-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="f1cec-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="f1cec-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="f1cec-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="f1cec-367">Define the overhead rate</span></span>

<span data-ttu-id="f1cec-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="f1cec-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="f1cec-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="f1cec-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-370">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="f1cec-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-372">Proj 1</span></span></td>
<td><span data-ttu-id="f1cec-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-373">Project 1</span></span></td>
<td><span data-ttu-id="f1cec-374">3</span><span class="sxs-lookup"><span data-stu-id="f1cec-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-375">Proj 2</span></span></td>
<td><span data-ttu-id="f1cec-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-376">Project 2</span></span></td>
<td><span data-ttu-id="f1cec-377">1</span><span class="sxs-lookup"><span data-stu-id="f1cec-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-379">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-380">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-381">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="f1cec-382">Units</span></span></th>
<th><span data-ttu-id="f1cec-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="f1cec-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-384">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-384">CC001</span></span></td>
<td><span data-ttu-id="f1cec-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-385">HR</span></span></td>
<td><span data-ttu-id="f1cec-386">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-386">10001</span></span></td>
<td><span data-ttu-id="f1cec-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-387">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-388">1</span><span class="sxs-lookup"><span data-stu-id="f1cec-388">1</span></span></td>
<td><span data-ttu-id="f1cec-389">10</span><span class="sxs-lookup"><span data-stu-id="f1cec-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="f1cec-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-391">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-392">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-393">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-394">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-396">Proj 1</span></span></td>
<td><span data-ttu-id="f1cec-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-397">Project 1</span></span></td>
<td><span data-ttu-id="f1cec-398">3</span><span class="sxs-lookup"><span data-stu-id="f1cec-398">3</span></span></td>
<td><span data-ttu-id="f1cec-399">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-399">10001</span></span></td>
<td><span data-ttu-id="f1cec-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f1cec-401">30.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-402">Proj 2</span></span></td>
<td><span data-ttu-id="f1cec-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-403">Project 2</span></span></td>
<td><span data-ttu-id="f1cec-404">1</span><span class="sxs-lookup"><span data-stu-id="f1cec-404">1</span></span></td>
<td><span data-ttu-id="f1cec-405">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-405">10001</span></span></td>
<td><span data-ttu-id="f1cec-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f1cec-407">10.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f1cec-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-409">Journal</span></span></th>
<th><span data-ttu-id="f1cec-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f1cec-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f1cec-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-413">00003</span><span class="sxs-lookup"><span data-stu-id="f1cec-413">00003</span></span></td>
<td><span data-ttu-id="f1cec-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="f1cec-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="f1cec-415">مالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-415">Fiscal</span></span></td>
<td><span data-ttu-id="f1cec-416">2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-416">2017</span></span></td>
<td><span data-ttu-id="f1cec-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-417">Period 1</span></span></td>
<td><span data-ttu-id="f1cec-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="f1cec-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="f1cec-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-421">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-424">Proj 1</span></span></td>
<td><span data-ttu-id="f1cec-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f1cec-426">3.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-428">Proj 2</span></span></td>
<td><span data-ttu-id="f1cec-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f1cec-430">1.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f1cec-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-433">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-434">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-435">Amount</span></span></th>
<th><span data-ttu-id="f1cec-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="f1cec-437">CC0001</span></span></td>
<td><span data-ttu-id="f1cec-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-438">HR</span></span></td>
<td><span data-ttu-id="f1cec-439">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-439">10001</span></span></td>
<td><span data-ttu-id="f1cec-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-440">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-441">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-442">-30.00</span></span></td>
<td><span data-ttu-id="f1cec-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-444">Proj 1</span></span></td>
<td><span data-ttu-id="f1cec-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f1cec-446">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-446">10001</span></span></td>
<td><span data-ttu-id="f1cec-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-447">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-448">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-449">30.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-449">30.00</span></span></td>
<td><span data-ttu-id="f1cec-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-451">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-451">CC001</span></span></td>
<td><span data-ttu-id="f1cec-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-452">HR</span></span></td>
<td><span data-ttu-id="f1cec-453">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-453">10001</span></span></td>
<td><span data-ttu-id="f1cec-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-454">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-455">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-456">-10.00</span></span></td>
<td><span data-ttu-id="f1cec-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-458">Proj 2</span></span></td>
<td><span data-ttu-id="f1cec-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f1cec-460">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-460">10001</span></span></td>
<td><span data-ttu-id="f1cec-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-461">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-462">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-463">10.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-463">10.00</span></span></td>
<td><span data-ttu-id="f1cec-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="f1cec-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="f1cec-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="f1cec-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="f1cec-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="f1cec-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="f1cec-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="f1cec-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="f1cec-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="f1cec-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="f1cec-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="f1cec-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="f1cec-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="f1cec-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="f1cec-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="f1cec-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="f1cec-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-475">Define the cost allocation</span></span>

<span data-ttu-id="f1cec-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="f1cec-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="f1cec-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="f1cec-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-479">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-481">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-481">CC002</span></span></td>
<td><span data-ttu-id="f1cec-482">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-482">Finance</span></span></td>
<td><span data-ttu-id="f1cec-483">35</span><span class="sxs-lookup"><span data-stu-id="f1cec-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-484">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-484">CC003</span></span></td>
<td><span data-ttu-id="f1cec-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-485">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-486">55</span><span class="sxs-lookup"><span data-stu-id="f1cec-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-487">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-487">CC004</span></span></td>
<td><span data-ttu-id="f1cec-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-488">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-489">10</span><span class="sxs-lookup"><span data-stu-id="f1cec-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="f1cec-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="f1cec-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-492">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-494">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-494">CC003</span></span></td>
<td><span data-ttu-id="f1cec-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-495">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-496">65</span><span class="sxs-lookup"><span data-stu-id="f1cec-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-497">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-497">CC004</span></span></td>
<td><span data-ttu-id="f1cec-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-498">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-499">35</span><span class="sxs-lookup"><span data-stu-id="f1cec-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="f1cec-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="f1cec-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-502">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="f1cec-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-504">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-505">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-506">60</span><span class="sxs-lookup"><span data-stu-id="f1cec-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-507">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-508">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-509">20</span><span class="sxs-lookup"><span data-stu-id="f1cec-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="f1cec-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="f1cec-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-512">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="f1cec-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-514">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-515">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-516">80</span><span class="sxs-lookup"><span data-stu-id="f1cec-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-517">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-518">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-519">15</span><span class="sxs-lookup"><span data-stu-id="f1cec-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f1cec-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="f1cec-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="f1cec-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="f1cec-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="f1cec-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="f1cec-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-523">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-524">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-525">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-526">Amount</span></span></th>
<th><span data-ttu-id="f1cec-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-528">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-528">CC002</span></span></td>
<td><span data-ttu-id="f1cec-529">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-529">Finance</span></span></td>
<td><span data-ttu-id="f1cec-530">35</span><span class="sxs-lookup"><span data-stu-id="f1cec-530">35</span></span></td>
<td><span data-ttu-id="f1cec-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f1cec-532">175.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-532">175.00</span></span></td>
<td><span data-ttu-id="f1cec-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-534">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-534">CC003</span></span></td>
<td><span data-ttu-id="f1cec-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-535">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-536">55</span><span class="sxs-lookup"><span data-stu-id="f1cec-536">55</span></span></td>
<td><span data-ttu-id="f1cec-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f1cec-538">275.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-538">275.00</span></span></td>
<td><span data-ttu-id="f1cec-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-540">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-540">CC004</span></span></td>
<td><span data-ttu-id="f1cec-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-541">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-542">10</span><span class="sxs-lookup"><span data-stu-id="f1cec-542">10</span></span></td>
<td><span data-ttu-id="f1cec-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f1cec-544">50.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-544">50.00</span></span></td>
<td><span data-ttu-id="f1cec-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-546">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-546">CC002</span></span></td>
<td><span data-ttu-id="f1cec-547">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-547">Finance</span></span></td>
<td><span data-ttu-id="f1cec-548">35</span><span class="sxs-lookup"><span data-stu-id="f1cec-548">35</span></span></td>
<td><span data-ttu-id="f1cec-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f1cec-550">436.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-550">436.00</span></span></td>
<td><span data-ttu-id="f1cec-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-552">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-552">CC003</span></span></td>
<td><span data-ttu-id="f1cec-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-553">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-554">55</span><span class="sxs-lookup"><span data-stu-id="f1cec-554">55</span></span></td>
<td><span data-ttu-id="f1cec-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f1cec-556">685.14</span><span class="sxs-lookup"><span data-stu-id="f1cec-556">685.14</span></span></td>
<td><span data-ttu-id="f1cec-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-558">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-558">CC004</span></span></td>
<td><span data-ttu-id="f1cec-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-559">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-560">10</span><span class="sxs-lookup"><span data-stu-id="f1cec-560">10</span></span></td>
<td><span data-ttu-id="f1cec-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f1cec-562">124.57</span><span class="sxs-lookup"><span data-stu-id="f1cec-562">124.57</span></span></td>
<td><span data-ttu-id="f1cec-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="f1cec-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-565">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-566">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-567">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-568">Amount</span></span></th>
<th><span data-ttu-id="f1cec-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-570">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-570">CC003</span></span></td>
<td><span data-ttu-id="f1cec-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-571">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-572">65</span><span class="sxs-lookup"><span data-stu-id="f1cec-572">65</span></span></td>
<td><span data-ttu-id="f1cec-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f1cec-574">438.75</span><span class="sxs-lookup"><span data-stu-id="f1cec-574">438.75</span></span></td>
<td><span data-ttu-id="f1cec-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-576">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-576">CC004</span></span></td>
<td><span data-ttu-id="f1cec-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-577">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-578">35</span><span class="sxs-lookup"><span data-stu-id="f1cec-578">35</span></span></td>
<td><span data-ttu-id="f1cec-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f1cec-580">236.25</span><span class="sxs-lookup"><span data-stu-id="f1cec-580">236.25</span></span></td>
<td><span data-ttu-id="f1cec-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-582">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-582">CC003</span></span></td>
<td><span data-ttu-id="f1cec-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-583">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-584">65</span><span class="sxs-lookup"><span data-stu-id="f1cec-584">65</span></span></td>
<td><span data-ttu-id="f1cec-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f1cec-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f1cec-586">5,297.69</span></span></td>
<td><span data-ttu-id="f1cec-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-588">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-588">CC004</span></span></td>
<td><span data-ttu-id="f1cec-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-589">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-590">35</span><span class="sxs-lookup"><span data-stu-id="f1cec-590">35</span></span></td>
<td><span data-ttu-id="f1cec-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="f1cec-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f1cec-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f1cec-592">2,852.60</span></span></td>
<td><span data-ttu-id="f1cec-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="f1cec-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-595">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-596">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-597">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-598">Amount</span></span></th>
<th><span data-ttu-id="f1cec-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-600">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-601">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-602">60</span><span class="sxs-lookup"><span data-stu-id="f1cec-602">60</span></span></td>
<td><span data-ttu-id="f1cec-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="f1cec-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f1cec-604">535.31</span><span class="sxs-lookup"><span data-stu-id="f1cec-604">535.31</span></span></td>
<td><span data-ttu-id="f1cec-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-606">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-607">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-608">20</span><span class="sxs-lookup"><span data-stu-id="f1cec-608">20</span></span></td>
<td><span data-ttu-id="f1cec-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="f1cec-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f1cec-610">178.44</span><span class="sxs-lookup"><span data-stu-id="f1cec-610">178.44</span></span></td>
<td><span data-ttu-id="f1cec-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-612">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-613">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-614">60</span><span class="sxs-lookup"><span data-stu-id="f1cec-614">60</span></span></td>
<td><span data-ttu-id="f1cec-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="f1cec-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f1cec-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f1cec-616">4,487.12</span></span></td>
<td><span data-ttu-id="f1cec-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-618">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-619">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-620">20</span><span class="sxs-lookup"><span data-stu-id="f1cec-620">20</span></span></td>
<td><span data-ttu-id="f1cec-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="f1cec-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f1cec-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-622">1,495.71</span></span></td>
<td><span data-ttu-id="f1cec-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1cec-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="f1cec-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-625">Cost object</span></span></th>
<th><span data-ttu-id="f1cec-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-626">Magnitude</span></span></th>
<th><span data-ttu-id="f1cec-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="f1cec-627">Allocation factor</span></span></th>
<th><span data-ttu-id="f1cec-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-628">Amount</span></span></th>
<th><span data-ttu-id="f1cec-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-630">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-631">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-632">80</span><span class="sxs-lookup"><span data-stu-id="f1cec-632">80</span></span></td>
<td><span data-ttu-id="f1cec-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="f1cec-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f1cec-634">241.05</span><span class="sxs-lookup"><span data-stu-id="f1cec-634">241.05</span></span></td>
<td><span data-ttu-id="f1cec-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-636">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-637">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-638">15</span><span class="sxs-lookup"><span data-stu-id="f1cec-638">15</span></span></td>
<td><span data-ttu-id="f1cec-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="f1cec-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f1cec-640">45.20</span><span class="sxs-lookup"><span data-stu-id="f1cec-640">45.20</span></span></td>
<td><span data-ttu-id="f1cec-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-642">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-643">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-644">80</span><span class="sxs-lookup"><span data-stu-id="f1cec-644">80</span></span></td>
<td><span data-ttu-id="f1cec-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="f1cec-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f1cec-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f1cec-646">2,507.09</span></span></td>
<td><span data-ttu-id="f1cec-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-648">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-649">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-650">15</span><span class="sxs-lookup"><span data-stu-id="f1cec-650">15</span></span></td>
<td><span data-ttu-id="f1cec-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="f1cec-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f1cec-652">470.08</span><span class="sxs-lookup"><span data-stu-id="f1cec-652">470.08</span></span></td>
<td><span data-ttu-id="f1cec-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f1cec-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="f1cec-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-655">Journal</span></span></th>
<th><span data-ttu-id="f1cec-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f1cec-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f1cec-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="f1cec-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-659">00004</span><span class="sxs-lookup"><span data-stu-id="f1cec-659">00004</span></span></td>
<td><span data-ttu-id="f1cec-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="f1cec-661">مالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-661">Fiscal</span></span></td>
<td><span data-ttu-id="f1cec-662">2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-662">2017</span></span></td>
<td><span data-ttu-id="f1cec-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-663">Period 1</span></span></td>
<td><span data-ttu-id="f1cec-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="f1cec-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f1cec-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f1cec-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-668">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-669">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-672">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-672">CC001</span></span></td>
<td><span data-ttu-id="f1cec-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-673">HR</span></span></td>
<td><span data-ttu-id="f1cec-674">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-674">10001</span></span></td>
<td><span data-ttu-id="f1cec-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-675">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-676">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-677">500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-679">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-679">CC001</span></span></td>
<td><span data-ttu-id="f1cec-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-680">HR</span></span></td>
<td><span data-ttu-id="f1cec-681">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-681">10001</span></span></td>
<td><span data-ttu-id="f1cec-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-682">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-683">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-686">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-686">CC002</span></span></td>
<td><span data-ttu-id="f1cec-687">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-687">Finance</span></span></td>
<td><span data-ttu-id="f1cec-688">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-688">10001</span></span></td>
<td><span data-ttu-id="f1cec-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-689">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-690">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-691">675.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-693">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-693">CC002</span></span></td>
<td><span data-ttu-id="f1cec-694">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-694">Finance</span></span></td>
<td><span data-ttu-id="f1cec-695">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-695">10001</span></span></td>
<td><span data-ttu-id="f1cec-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-696">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-697">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="f1cec-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-700">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-700">CC003</span></span></td>
<td><span data-ttu-id="f1cec-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-701">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-702">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-702">10001</span></span></td>
<td><span data-ttu-id="f1cec-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-703">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-704">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-705">713.75</span><span class="sxs-lookup"><span data-stu-id="f1cec-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-707">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-707">CC003</span></span></td>
<td><span data-ttu-id="f1cec-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-708">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-709">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-709">10001</span></span></td>
<td><span data-ttu-id="f1cec-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-710">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-711">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="f1cec-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-714">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-714">CC003</span></span></td>
<td><span data-ttu-id="f1cec-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-715">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-716">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-716">10001</span></span></td>
<td><span data-ttu-id="f1cec-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-717">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-718">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-719">286.25</span><span class="sxs-lookup"><span data-stu-id="f1cec-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-721">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-721">CC003</span></span></td>
<td><span data-ttu-id="f1cec-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-722">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-723">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-723">10001</span></span></td>
<td><span data-ttu-id="f1cec-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-724">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-725">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="f1cec-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-728">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-729">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-730">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-730">10001</span></span></td>
<td><span data-ttu-id="f1cec-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-731">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-732">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-733">776.36</span><span class="sxs-lookup"><span data-stu-id="f1cec-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-735">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-736">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-737">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-737">10001</span></span></td>
<td><span data-ttu-id="f1cec-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-738">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-739">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f1cec-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-742">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-743">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-744">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-744">10001</span></span></td>
<td><span data-ttu-id="f1cec-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-745">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-746">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-747">223.64</span><span class="sxs-lookup"><span data-stu-id="f1cec-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="f1cec-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-749">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-750">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-751">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-751">10001</span></span></td>
<td><span data-ttu-id="f1cec-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-752">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-753">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f1cec-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f1cec-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f1cec-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f1cec-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-757">Cost element</span></span></th>
<th><span data-ttu-id="f1cec-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-758">Cost behavior</span></span></th>
<th><span data-ttu-id="f1cec-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="f1cec-759">Amount</span></span></th>
<th><span data-ttu-id="f1cec-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="f1cec-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1cec-761">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-761">CC001</span></span></td>
<td><span data-ttu-id="f1cec-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-762">HR</span></span></td>
<td><span data-ttu-id="f1cec-763">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-763">10001</span></span></td>
<td><span data-ttu-id="f1cec-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-764">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-765">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-766">-500.00</span></span></td>
<td><span data-ttu-id="f1cec-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-768">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-768">CC002</span></span></td>
<td><span data-ttu-id="f1cec-769">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-769">Finance</span></span></td>
<td><span data-ttu-id="f1cec-770">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-770">10001</span></span></td>
<td><span data-ttu-id="f1cec-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-771">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-772">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-773">175.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-773">175.00</span></span></td>
<td><span data-ttu-id="f1cec-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-775">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-775">CC003</span></span></td>
<td><span data-ttu-id="f1cec-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-776">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-777">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-777">10001</span></span></td>
<td><span data-ttu-id="f1cec-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-778">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-779">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-780">275.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-780">275.00</span></span></td>
<td><span data-ttu-id="f1cec-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-782">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-782">CC004</span></span></td>
<td><span data-ttu-id="f1cec-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-783">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-784">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-784">10001</span></span></td>
<td><span data-ttu-id="f1cec-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-785">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-786">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-787">50,00</span><span class="sxs-lookup"><span data-stu-id="f1cec-787">50,00</span></span></td>
<td><span data-ttu-id="f1cec-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-789">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-789">CC001</span></span></td>
<td><span data-ttu-id="f1cec-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="f1cec-790">HR</span></span></td>
<td><span data-ttu-id="f1cec-791">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-791">10001</span></span></td>
<td><span data-ttu-id="f1cec-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-792">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-793">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-794">-1,245.71</span></span></td>
<td><span data-ttu-id="f1cec-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-796">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-796">CC002</span></span></td>
<td><span data-ttu-id="f1cec-797">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-797">Finance</span></span></td>
<td><span data-ttu-id="f1cec-798">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-798">10001</span></span></td>
<td><span data-ttu-id="f1cec-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-799">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-800">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-801">436.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-801">436.00</span></span></td>
<td><span data-ttu-id="f1cec-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-803">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-803">CC003</span></span></td>
<td><span data-ttu-id="f1cec-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-804">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-805">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-805">10001</span></span></td>
<td><span data-ttu-id="f1cec-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-806">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-807">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-808">685.14</span><span class="sxs-lookup"><span data-stu-id="f1cec-808">685.14</span></span></td>
<td><span data-ttu-id="f1cec-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-810">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-810">CC004</span></span></td>
<td><span data-ttu-id="f1cec-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-811">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-812">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-812">10001</span></span></td>
<td><span data-ttu-id="f1cec-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-813">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-814">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-815">124.57</span><span class="sxs-lookup"><span data-stu-id="f1cec-815">124.57</span></span></td>
<td><span data-ttu-id="f1cec-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-817">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-817">CC002</span></span></td>
<td><span data-ttu-id="f1cec-818">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-818">Finance</span></span></td>
<td><span data-ttu-id="f1cec-819">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-819">10001</span></span></td>
<td><span data-ttu-id="f1cec-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-820">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-821">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-822">-675.00</span></span></td>
<td><span data-ttu-id="f1cec-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-824">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-824">CC003</span></span></td>
<td><span data-ttu-id="f1cec-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-825">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-826">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-826">10001</span></span></td>
<td><span data-ttu-id="f1cec-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-827">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-828">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-829">438.75</span><span class="sxs-lookup"><span data-stu-id="f1cec-829">438.75</span></span></td>
<td><span data-ttu-id="f1cec-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-831">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-831">CC004</span></span></td>
<td><span data-ttu-id="f1cec-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-832">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-833">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-833">10001</span></span></td>
<td><span data-ttu-id="f1cec-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-834">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-835">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-836">236.25</span><span class="sxs-lookup"><span data-stu-id="f1cec-836">236.25</span></span></td>
<td><span data-ttu-id="f1cec-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-838">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-838">CC002</span></span></td>
<td><span data-ttu-id="f1cec-839">المالية</span><span class="sxs-lookup"><span data-stu-id="f1cec-839">Finance</span></span></td>
<td><span data-ttu-id="f1cec-840">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-840">10001</span></span></td>
<td><span data-ttu-id="f1cec-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-841">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-842">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="f1cec-843">-8,150.29</span></span></td>
<td><span data-ttu-id="f1cec-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-845">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-845">CC003</span></span></td>
<td><span data-ttu-id="f1cec-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-846">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-847">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-847">10001</span></span></td>
<td><span data-ttu-id="f1cec-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-848">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-849">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f1cec-850">5,297.69</span></span></td>
<td><span data-ttu-id="f1cec-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-852">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-852">CC004</span></span></td>
<td><span data-ttu-id="f1cec-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="f1cec-853">Packaging</span></span></td>
<td><span data-ttu-id="f1cec-854">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-854">10001</span></span></td>
<td><span data-ttu-id="f1cec-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-855">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-856">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f1cec-857">2,852.60</span></span></td>
<td><span data-ttu-id="f1cec-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-859">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-859">CC003</span></span></td>
<td><span data-ttu-id="f1cec-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-860">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-861">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-861">10001</span></span></td>
<td><span data-ttu-id="f1cec-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-862">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-863">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="f1cec-864">-713.75</span></span></td>
<td><span data-ttu-id="f1cec-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-866">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-867">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-868">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-868">10001</span></span></td>
<td><span data-ttu-id="f1cec-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-869">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-870">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-871">535.31</span><span class="sxs-lookup"><span data-stu-id="f1cec-871">535.31</span></span></td>
<td><span data-ttu-id="f1cec-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-873">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-874">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-875">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-875">10001</span></span></td>
<td><span data-ttu-id="f1cec-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-876">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-877">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-878">178.44</span><span class="sxs-lookup"><span data-stu-id="f1cec-878">178.44</span></span></td>
<td><span data-ttu-id="f1cec-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-880">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-880">CC003</span></span></td>
<td><span data-ttu-id="f1cec-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-881">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-882">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-882">10001</span></span></td>
<td><span data-ttu-id="f1cec-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-883">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-884">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="f1cec-885">-5,982.83</span></span></td>
<td><span data-ttu-id="f1cec-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-887">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-888">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-889">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-889">10001</span></span></td>
<td><span data-ttu-id="f1cec-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-890">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-891">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f1cec-892">4,487.12</span></span></td>
<td><span data-ttu-id="f1cec-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-894">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-895">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-896">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-896">10001</span></span></td>
<td><span data-ttu-id="f1cec-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-897">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-898">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f1cec-899">1,495.71</span></span></td>
<td><span data-ttu-id="f1cec-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-901">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-901">CC003</span></span></td>
<td><span data-ttu-id="f1cec-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-902">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-903">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-903">10001</span></span></td>
<td><span data-ttu-id="f1cec-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-904">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-905">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="f1cec-906">-286.25</span></span></td>
<td><span data-ttu-id="f1cec-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-908">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-909">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-910">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-910">10001</span></span></td>
<td><span data-ttu-id="f1cec-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-911">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-912">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-913">241.05</span><span class="sxs-lookup"><span data-stu-id="f1cec-913">241.05</span></span></td>
<td><span data-ttu-id="f1cec-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-915">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-916">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-917">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-917">10001</span></span></td>
<td><span data-ttu-id="f1cec-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-918">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-919">Fixed cost</span></span></td>
<td><span data-ttu-id="f1cec-920">45.20</span><span class="sxs-lookup"><span data-stu-id="f1cec-920">45.20</span></span></td>
<td><span data-ttu-id="f1cec-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-922">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-922">CC003</span></span></td>
<td><span data-ttu-id="f1cec-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="f1cec-923">Assembly</span></span></td>
<td><span data-ttu-id="f1cec-924">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-924">10001</span></span></td>
<td><span data-ttu-id="f1cec-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-925">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-926">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="f1cec-927">-2,977.17</span></span></td>
<td><span data-ttu-id="f1cec-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-929">Prod 1</span></span></td>
<td><span data-ttu-id="f1cec-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-930">Product 1</span></span></td>
<td><span data-ttu-id="f1cec-931">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-931">10001</span></span></td>
<td><span data-ttu-id="f1cec-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-932">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-933">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f1cec-934">2,507.09</span></span></td>
<td><span data-ttu-id="f1cec-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1cec-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-936">Prod 2</span></span></td>
<td><span data-ttu-id="f1cec-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-937">Product 2</span></span></td>
<td><span data-ttu-id="f1cec-938">10001</span><span class="sxs-lookup"><span data-stu-id="f1cec-938">10001</span></span></td>
<td><span data-ttu-id="f1cec-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-939">Electricity</span></span></td>
<td><span data-ttu-id="f1cec-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-940">Variable cost</span></span></td>
<td><span data-ttu-id="f1cec-941">470.08</span><span class="sxs-lookup"><span data-stu-id="f1cec-941">470.08</span></span></td>
<td><span data-ttu-id="f1cec-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="f1cec-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="f1cec-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="f1cec-943">Conclusion</span></span>
<span data-ttu-id="f1cec-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="f1cec-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="f1cec-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="f1cec-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="f1cec-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="f1cec-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="f1cec-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="f1cec-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="f1cec-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="f1cec-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="f1cec-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f1cec-951">CC099</span><span class="sxs-lookup"><span data-stu-id="f1cec-951">CC099</span></span></th>
<th><span data-ttu-id="f1cec-952">CC001</span><span class="sxs-lookup"><span data-stu-id="f1cec-952">CC001</span></span></th>
<th><span data-ttu-id="f1cec-953">CC002</span><span class="sxs-lookup"><span data-stu-id="f1cec-953">CC002</span></span></th>
<th><span data-ttu-id="f1cec-954">CC003</span><span class="sxs-lookup"><span data-stu-id="f1cec-954">CC003</span></span></th>
<th><span data-ttu-id="f1cec-955">CC004</span><span class="sxs-lookup"><span data-stu-id="f1cec-955">CC004</span></span></th>
<th><span data-ttu-id="f1cec-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-956">Proj 1</span></span></th>
<th><span data-ttu-id="f1cec-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-957">Proj 2</span></span></th>
<th><span data-ttu-id="f1cec-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="f1cec-958">Prod 1</span></span></th>
<th><span data-ttu-id="f1cec-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="f1cec-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="f1cec-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="f1cec-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="f1cec-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="f1cec-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-971">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="f1cec-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="f1cec-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-973">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-974">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-975">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-976">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-977">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-978">776.36</span><span class="sxs-lookup"><span data-stu-id="f1cec-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-979">223.64</span><span class="sxs-lookup"><span data-stu-id="f1cec-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="f1cec-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="f1cec-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-982">000</span><span class="sxs-lookup"><span data-stu-id="f1cec-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-983">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-984">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-985">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-986">0.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-987">30.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-988">10.00</span><span class="sxs-lookup"><span data-stu-id="f1cec-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f1cec-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f1cec-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f1cec-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f1cec-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f1cec-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="f1cec-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="f1cec-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="f1cec-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f1cec-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="f1cec-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="f1cec-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]