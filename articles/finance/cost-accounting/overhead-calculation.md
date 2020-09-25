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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759462"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6f3f1-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f3f1-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6f3f1-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="6f3f1-105">Term definition</span></span>
---------------

<span data-ttu-id="6f3f1-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6f3f1-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6f3f1-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="6f3f1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6f3f1-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-109">Rent</span></span>
-   <span data-ttu-id="6f3f1-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-110">Electricity</span></span>
-   <span data-ttu-id="6f3f1-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6f3f1-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-112">Overhead calculation overview</span></span>
<span data-ttu-id="6f3f1-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6f3f1-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6f3f1-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6f3f1-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6f3f1-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6f3f1-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="6f3f1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6f3f1-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-119">Version type</span></span>
-   <span data-ttu-id="6f3f1-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="6f3f1-120">Date and time</span></span>
-   <span data-ttu-id="6f3f1-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="6f3f1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6f3f1-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-122">Fiscal year</span></span>
-   <span data-ttu-id="6f3f1-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-123">Fiscal period</span></span>

<span data-ttu-id="6f3f1-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6f3f1-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6f3f1-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6f3f1-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6f3f1-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6f3f1-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6f3f1-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6f3f1-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6f3f1-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="6f3f1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6f3f1-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6f3f1-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6f3f1-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6f3f1-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6f3f1-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-140">Main account</span></span></th>
<th><span data-ttu-id="6f3f1-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-143">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-144">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-145">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-145">10001</span></span></td>
<td><span data-ttu-id="6f3f1-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-146">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6f3f1-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6f3f1-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6f3f1-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6f3f1-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6f3f1-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6f3f1-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6f3f1-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6f3f1-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="6f3f1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6f3f1-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6f3f1-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="6f3f1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6f3f1-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="6f3f1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6f3f1-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-160">Journal</span></span></th>
<th><span data-ttu-id="6f3f1-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6f3f1-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6f3f1-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-164">00001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-164">00001</span></span></td>
<td><span data-ttu-id="6f3f1-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6f3f1-166">مالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-166">Fiscal</span></span></td>
<td><span data-ttu-id="6f3f1-167">2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-167">2017</span></span></td>
<td><span data-ttu-id="6f3f1-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-168">Period 1</span></span></td>
<td><span data-ttu-id="6f3f1-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6f3f1-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-173">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-177">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-178">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-179">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-179">10001</span></span></td>
<td><span data-ttu-id="6f3f1-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-180">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="6f3f1-181">Unclassified</span></span></td>
<td><span data-ttu-id="6f3f1-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6f3f1-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-185">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-187">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-189">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-190">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-191">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-191">10001</span></span></td>
<td><span data-ttu-id="6f3f1-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-192">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="6f3f1-193">Unclassified</span></span></td>
<td><span data-ttu-id="6f3f1-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-194">10,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-196">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-197">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-198">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-198">10001</span></span></td>
<td><span data-ttu-id="6f3f1-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-199">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="6f3f1-200">Unclassified</span></span></td>
<td><span data-ttu-id="6f3f1-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-203">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-204">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-205">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-205">10001</span></span></td>
<td><span data-ttu-id="6f3f1-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-206">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-208">1,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-210">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-211">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-212">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-212">10001</span></span></td>
<td><span data-ttu-id="6f3f1-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-213">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-214">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-215">9,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6f3f1-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6f3f1-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6f3f1-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6f3f1-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6f3f1-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6f3f1-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6f3f1-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6f3f1-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6f3f1-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6f3f1-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-228">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-230">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-231">HR</span></span></td>
<td><span data-ttu-id="6f3f1-232">1,000</span><span class="sxs-lookup"><span data-stu-id="6f3f1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-233">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-234">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-234">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6f3f1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-236">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-237">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-238">0</span><span class="sxs-lookup"><span data-stu-id="6f3f1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-240">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-241">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-244">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-245">HR</span></span></td>
<td><span data-ttu-id="6f3f1-246">1,000</span><span class="sxs-lookup"><span data-stu-id="6f3f1-246">1,000</span></span></td>
<td><span data-ttu-id="6f3f1-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-249">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-250">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-250">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6f3f1-251">6,000</span></span></td>
<td><span data-ttu-id="6f3f1-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6f3f1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-254">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-255">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-256">0</span><span class="sxs-lookup"><span data-stu-id="6f3f1-256">0</span></span></td>
<td><span data-ttu-id="6f3f1-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-258">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6f3f1-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-261">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-262">Formula</span></span></th>
<th><span data-ttu-id="6f3f1-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-263">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-266">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-267">HR</span></span></td>
<td><span data-ttu-id="6f3f1-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6f3f1-269">1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-269">1</span></span></td>
<td><span data-ttu-id="6f3f1-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-271">500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-272">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-273">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-273">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6f3f1-275">1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-275">1</span></span></td>
<td><span data-ttu-id="6f3f1-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-277">500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-278">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-279">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6f3f1-281">0</span><span class="sxs-lookup"><span data-stu-id="6f3f1-281">0</span></span></td>
<td><span data-ttu-id="6f3f1-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-283">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6f3f1-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-285">Journal</span></span></th>
<th><span data-ttu-id="6f3f1-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6f3f1-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6f3f1-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-289">00002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-289">00002</span></span></td>
<td><span data-ttu-id="6f3f1-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6f3f1-291">مالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-291">Fiscal</span></span></td>
<td><span data-ttu-id="6f3f1-292">2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-292">2017</span></span></td>
<td><span data-ttu-id="6f3f1-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-293">Period 1</span></span></td>
<td><span data-ttu-id="6f3f1-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6f3f1-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-298">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-302">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-303">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-304">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-304">10001</span></span></td>
<td><span data-ttu-id="6f3f1-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-305">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-309">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-310">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-311">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-311">10001</span></span></td>
<td><span data-ttu-id="6f3f1-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-312">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-313">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6f3f1-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-317">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-319">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-321">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-322">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-323">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-323">10001</span></span></td>
<td><span data-ttu-id="6f3f1-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-324">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-328">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-329">HR</span></span></td>
<td><span data-ttu-id="6f3f1-330">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-330">10001</span></span></td>
<td><span data-ttu-id="6f3f1-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-331">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-333">500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-333">500.00</span></span></td>
<td><span data-ttu-id="6f3f1-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-335">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-336">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-336">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-337">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-337">10001</span></span></td>
<td><span data-ttu-id="6f3f1-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-338">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-340">500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-340">500.00</span></span></td>
<td><span data-ttu-id="6f3f1-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-342">CC099</span></span></td>
<td><span data-ttu-id="6f3f1-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-343">Default cost center</span></span></td>
<td><span data-ttu-id="6f3f1-344">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-344">10001</span></span></td>
<td><span data-ttu-id="6f3f1-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-345">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-346">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6f3f1-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-349">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-350">HR</span></span></td>
<td><span data-ttu-id="6f3f1-351">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-351">10001</span></span></td>
<td><span data-ttu-id="6f3f1-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-352">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-353">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-354">1,285.71</span></span></td>
<td><span data-ttu-id="6f3f1-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-356">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-357">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-357">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-358">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-358">10001</span></span></td>
<td><span data-ttu-id="6f3f1-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-359">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-360">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6f3f1-361">7,714.29</span></span></td>
<td><span data-ttu-id="6f3f1-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6f3f1-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6f3f1-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6f3f1-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6f3f1-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-367">Define the overhead rate</span></span>

<span data-ttu-id="6f3f1-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6f3f1-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-370">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="6f3f1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-372">Proj 1</span></span></td>
<td><span data-ttu-id="6f3f1-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-373">Project 1</span></span></td>
<td><span data-ttu-id="6f3f1-374">3</span><span class="sxs-lookup"><span data-stu-id="6f3f1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-375">Proj 2</span></span></td>
<td><span data-ttu-id="6f3f1-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-376">Project 2</span></span></td>
<td><span data-ttu-id="6f3f1-377">1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-379">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-380">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="6f3f1-382">Units</span></span></th>
<th><span data-ttu-id="6f3f1-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="6f3f1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-384">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-385">HR</span></span></td>
<td><span data-ttu-id="6f3f1-386">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-386">10001</span></span></td>
<td><span data-ttu-id="6f3f1-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-387">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-388">1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-388">1</span></span></td>
<td><span data-ttu-id="6f3f1-389">10</span><span class="sxs-lookup"><span data-stu-id="6f3f1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-391">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-392">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-393">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-396">Proj 1</span></span></td>
<td><span data-ttu-id="6f3f1-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-397">Project 1</span></span></td>
<td><span data-ttu-id="6f3f1-398">3</span><span class="sxs-lookup"><span data-stu-id="6f3f1-398">3</span></span></td>
<td><span data-ttu-id="6f3f1-399">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-399">10001</span></span></td>
<td><span data-ttu-id="6f3f1-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6f3f1-401">30.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-402">Proj 2</span></span></td>
<td><span data-ttu-id="6f3f1-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-403">Project 2</span></span></td>
<td><span data-ttu-id="6f3f1-404">1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-404">1</span></span></td>
<td><span data-ttu-id="6f3f1-405">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-405">10001</span></span></td>
<td><span data-ttu-id="6f3f1-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6f3f1-407">10.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6f3f1-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-409">Journal</span></span></th>
<th><span data-ttu-id="6f3f1-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6f3f1-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6f3f1-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-413">00003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-413">00003</span></span></td>
<td><span data-ttu-id="6f3f1-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6f3f1-415">مالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-415">Fiscal</span></span></td>
<td><span data-ttu-id="6f3f1-416">2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-416">2017</span></span></td>
<td><span data-ttu-id="6f3f1-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-417">Period 1</span></span></td>
<td><span data-ttu-id="6f3f1-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6f3f1-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-421">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-424">Proj 1</span></span></td>
<td><span data-ttu-id="6f3f1-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6f3f1-426">3.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-428">Proj 2</span></span></td>
<td><span data-ttu-id="6f3f1-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6f3f1-430">1.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6f3f1-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-433">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-435">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-437">CC0001</span></span></td>
<td><span data-ttu-id="6f3f1-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-438">HR</span></span></td>
<td><span data-ttu-id="6f3f1-439">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-439">10001</span></span></td>
<td><span data-ttu-id="6f3f1-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-440">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-441">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-442">-30.00</span></span></td>
<td><span data-ttu-id="6f3f1-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-444">Proj 1</span></span></td>
<td><span data-ttu-id="6f3f1-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6f3f1-446">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-446">10001</span></span></td>
<td><span data-ttu-id="6f3f1-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-447">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-448">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-449">30.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-449">30.00</span></span></td>
<td><span data-ttu-id="6f3f1-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-451">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-452">HR</span></span></td>
<td><span data-ttu-id="6f3f1-453">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-453">10001</span></span></td>
<td><span data-ttu-id="6f3f1-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-454">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-455">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-456">-10.00</span></span></td>
<td><span data-ttu-id="6f3f1-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-458">Proj 2</span></span></td>
<td><span data-ttu-id="6f3f1-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6f3f1-460">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-460">10001</span></span></td>
<td><span data-ttu-id="6f3f1-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-461">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-462">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-463">10.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-463">10.00</span></span></td>
<td><span data-ttu-id="6f3f1-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6f3f1-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6f3f1-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6f3f1-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="6f3f1-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6f3f1-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6f3f1-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6f3f1-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6f3f1-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6f3f1-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6f3f1-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-475">Define the cost allocation</span></span>

<span data-ttu-id="6f3f1-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6f3f1-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6f3f1-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-479">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-481">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-482">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-482">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-483">35</span><span class="sxs-lookup"><span data-stu-id="6f3f1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-484">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-485">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-486">55</span><span class="sxs-lookup"><span data-stu-id="6f3f1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-487">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-488">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-489">10</span><span class="sxs-lookup"><span data-stu-id="6f3f1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6f3f1-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-492">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-494">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-495">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-496">65</span><span class="sxs-lookup"><span data-stu-id="6f3f1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-497">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-498">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-499">35</span><span class="sxs-lookup"><span data-stu-id="6f3f1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6f3f1-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-502">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-504">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-505">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-506">60</span><span class="sxs-lookup"><span data-stu-id="6f3f1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-507">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-508">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-509">20</span><span class="sxs-lookup"><span data-stu-id="6f3f1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6f3f1-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-512">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-514">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-515">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-516">80</span><span class="sxs-lookup"><span data-stu-id="6f3f1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-517">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-518">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-519">15</span><span class="sxs-lookup"><span data-stu-id="6f3f1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6f3f1-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6f3f1-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6f3f1-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-523">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-524">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-526">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-528">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-529">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-529">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-530">35</span><span class="sxs-lookup"><span data-stu-id="6f3f1-530">35</span></span></td>
<td><span data-ttu-id="6f3f1-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6f3f1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-532">175.00</span></span></td>
<td><span data-ttu-id="6f3f1-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-534">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-535">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-536">55</span><span class="sxs-lookup"><span data-stu-id="6f3f1-536">55</span></span></td>
<td><span data-ttu-id="6f3f1-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6f3f1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-538">275.00</span></span></td>
<td><span data-ttu-id="6f3f1-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-540">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-541">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-542">10</span><span class="sxs-lookup"><span data-stu-id="6f3f1-542">10</span></span></td>
<td><span data-ttu-id="6f3f1-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6f3f1-544">50.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-544">50.00</span></span></td>
<td><span data-ttu-id="6f3f1-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-546">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-547">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-547">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-548">35</span><span class="sxs-lookup"><span data-stu-id="6f3f1-548">35</span></span></td>
<td><span data-ttu-id="6f3f1-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6f3f1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-550">436.00</span></span></td>
<td><span data-ttu-id="6f3f1-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-552">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-553">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-554">55</span><span class="sxs-lookup"><span data-stu-id="6f3f1-554">55</span></span></td>
<td><span data-ttu-id="6f3f1-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6f3f1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6f3f1-556">685.14</span></span></td>
<td><span data-ttu-id="6f3f1-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-558">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-559">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-560">10</span><span class="sxs-lookup"><span data-stu-id="6f3f1-560">10</span></span></td>
<td><span data-ttu-id="6f3f1-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6f3f1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6f3f1-562">124.57</span></span></td>
<td><span data-ttu-id="6f3f1-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-565">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-566">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-568">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-570">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-571">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-572">65</span><span class="sxs-lookup"><span data-stu-id="6f3f1-572">65</span></span></td>
<td><span data-ttu-id="6f3f1-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6f3f1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6f3f1-574">438.75</span></span></td>
<td><span data-ttu-id="6f3f1-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-576">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-577">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-578">35</span><span class="sxs-lookup"><span data-stu-id="6f3f1-578">35</span></span></td>
<td><span data-ttu-id="6f3f1-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6f3f1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6f3f1-580">236.25</span></span></td>
<td><span data-ttu-id="6f3f1-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-582">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-583">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-584">65</span><span class="sxs-lookup"><span data-stu-id="6f3f1-584">65</span></span></td>
<td><span data-ttu-id="6f3f1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6f3f1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6f3f1-586">5,297.69</span></span></td>
<td><span data-ttu-id="6f3f1-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-588">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-589">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-590">35</span><span class="sxs-lookup"><span data-stu-id="6f3f1-590">35</span></span></td>
<td><span data-ttu-id="6f3f1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6f3f1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6f3f1-592">2,852.60</span></span></td>
<td><span data-ttu-id="6f3f1-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-595">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-596">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-598">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-600">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-601">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-602">60</span><span class="sxs-lookup"><span data-stu-id="6f3f1-602">60</span></span></td>
<td><span data-ttu-id="6f3f1-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6f3f1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6f3f1-604">535.31</span></span></td>
<td><span data-ttu-id="6f3f1-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-606">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-607">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-608">20</span><span class="sxs-lookup"><span data-stu-id="6f3f1-608">20</span></span></td>
<td><span data-ttu-id="6f3f1-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6f3f1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6f3f1-610">178.44</span></span></td>
<td><span data-ttu-id="6f3f1-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-612">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-613">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-614">60</span><span class="sxs-lookup"><span data-stu-id="6f3f1-614">60</span></span></td>
<td><span data-ttu-id="6f3f1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6f3f1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6f3f1-616">4,487.12</span></span></td>
<td><span data-ttu-id="6f3f1-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-618">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-619">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-620">20</span><span class="sxs-lookup"><span data-stu-id="6f3f1-620">20</span></span></td>
<td><span data-ttu-id="6f3f1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6f3f1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-622">1,495.71</span></span></td>
<td><span data-ttu-id="6f3f1-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6f3f1-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-625">Cost object</span></span></th>
<th><span data-ttu-id="6f3f1-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-626">Magnitude</span></span></th>
<th><span data-ttu-id="6f3f1-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6f3f1-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-628">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-630">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-631">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-632">80</span><span class="sxs-lookup"><span data-stu-id="6f3f1-632">80</span></span></td>
<td><span data-ttu-id="6f3f1-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6f3f1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6f3f1-634">241.05</span></span></td>
<td><span data-ttu-id="6f3f1-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-636">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-637">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-638">15</span><span class="sxs-lookup"><span data-stu-id="6f3f1-638">15</span></span></td>
<td><span data-ttu-id="6f3f1-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6f3f1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6f3f1-640">45.20</span></span></td>
<td><span data-ttu-id="6f3f1-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-642">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-643">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-644">80</span><span class="sxs-lookup"><span data-stu-id="6f3f1-644">80</span></span></td>
<td><span data-ttu-id="6f3f1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6f3f1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6f3f1-646">2,507.09</span></span></td>
<td><span data-ttu-id="6f3f1-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-648">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-649">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-650">15</span><span class="sxs-lookup"><span data-stu-id="6f3f1-650">15</span></span></td>
<td><span data-ttu-id="6f3f1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6f3f1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6f3f1-652">470.08</span></span></td>
<td><span data-ttu-id="6f3f1-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6f3f1-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="6f3f1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-655">Journal</span></span></th>
<th><span data-ttu-id="6f3f1-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6f3f1-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6f3f1-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="6f3f1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-659">00004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-659">00004</span></span></td>
<td><span data-ttu-id="6f3f1-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6f3f1-661">مالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-661">Fiscal</span></span></td>
<td><span data-ttu-id="6f3f1-662">2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-662">2017</span></span></td>
<td><span data-ttu-id="6f3f1-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-663">Period 1</span></span></td>
<td><span data-ttu-id="6f3f1-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6f3f1-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f3f1-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-668">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-672">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-673">HR</span></span></td>
<td><span data-ttu-id="6f3f1-674">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-674">10001</span></span></td>
<td><span data-ttu-id="6f3f1-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-675">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-677">500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-679">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-680">HR</span></span></td>
<td><span data-ttu-id="6f3f1-681">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-681">10001</span></span></td>
<td><span data-ttu-id="6f3f1-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-682">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-683">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-686">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-687">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-687">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-688">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-688">10001</span></span></td>
<td><span data-ttu-id="6f3f1-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-689">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-693">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-694">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-694">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-695">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-695">10001</span></span></td>
<td><span data-ttu-id="6f3f1-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-696">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-697">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6f3f1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-700">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-701">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-702">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-702">10001</span></span></td>
<td><span data-ttu-id="6f3f1-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-703">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6f3f1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-707">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-708">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-709">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-709">10001</span></span></td>
<td><span data-ttu-id="6f3f1-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-710">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-711">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6f3f1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-714">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-715">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-716">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-716">10001</span></span></td>
<td><span data-ttu-id="6f3f1-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-717">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6f3f1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-721">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-722">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-723">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-723">10001</span></span></td>
<td><span data-ttu-id="6f3f1-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-724">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-725">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6f3f1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-728">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-729">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-730">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-730">10001</span></span></td>
<td><span data-ttu-id="6f3f1-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-731">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6f3f1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-735">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-736">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-737">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-737">10001</span></span></td>
<td><span data-ttu-id="6f3f1-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-738">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-739">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6f3f1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-742">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-743">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-744">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-744">10001</span></span></td>
<td><span data-ttu-id="6f3f1-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-745">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6f3f1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6f3f1-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-749">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-750">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-751">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-751">10001</span></span></td>
<td><span data-ttu-id="6f3f1-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-752">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-753">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6f3f1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6f3f1-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6f3f1-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6f3f1-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-757">Cost element</span></span></th>
<th><span data-ttu-id="6f3f1-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6f3f1-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6f3f1-759">Amount</span></span></th>
<th><span data-ttu-id="6f3f1-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f3f1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-761">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-762">HR</span></span></td>
<td><span data-ttu-id="6f3f1-763">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-763">10001</span></span></td>
<td><span data-ttu-id="6f3f1-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-764">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-766">-500.00</span></span></td>
<td><span data-ttu-id="6f3f1-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-768">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-769">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-769">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-770">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-770">10001</span></span></td>
<td><span data-ttu-id="6f3f1-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-771">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-773">175.00</span></span></td>
<td><span data-ttu-id="6f3f1-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-775">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-776">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-777">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-777">10001</span></span></td>
<td><span data-ttu-id="6f3f1-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-778">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-780">275.00</span></span></td>
<td><span data-ttu-id="6f3f1-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-782">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-783">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-784">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-784">10001</span></span></td>
<td><span data-ttu-id="6f3f1-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-785">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-787">50,00</span></span></td>
<td><span data-ttu-id="6f3f1-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-789">CC001</span></span></td>
<td><span data-ttu-id="6f3f1-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-790">HR</span></span></td>
<td><span data-ttu-id="6f3f1-791">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-791">10001</span></span></td>
<td><span data-ttu-id="6f3f1-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-792">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-793">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6f3f1-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-796">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-797">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-797">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-798">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-798">10001</span></span></td>
<td><span data-ttu-id="6f3f1-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-799">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-800">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-801">436.00</span></span></td>
<td><span data-ttu-id="6f3f1-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-803">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-804">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-805">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-805">10001</span></span></td>
<td><span data-ttu-id="6f3f1-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-806">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-807">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6f3f1-808">685.14</span></span></td>
<td><span data-ttu-id="6f3f1-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-810">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-811">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-812">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-812">10001</span></span></td>
<td><span data-ttu-id="6f3f1-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-813">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-814">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6f3f1-815">124.57</span></span></td>
<td><span data-ttu-id="6f3f1-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-817">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-818">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-818">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-819">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-819">10001</span></span></td>
<td><span data-ttu-id="6f3f1-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-820">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-822">-675.00</span></span></td>
<td><span data-ttu-id="6f3f1-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-824">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-825">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-826">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-826">10001</span></span></td>
<td><span data-ttu-id="6f3f1-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-827">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6f3f1-829">438.75</span></span></td>
<td><span data-ttu-id="6f3f1-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-831">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-832">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-833">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-833">10001</span></span></td>
<td><span data-ttu-id="6f3f1-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-834">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6f3f1-836">236.25</span></span></td>
<td><span data-ttu-id="6f3f1-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-838">CC002</span></span></td>
<td><span data-ttu-id="6f3f1-839">المالية</span><span class="sxs-lookup"><span data-stu-id="6f3f1-839">Finance</span></span></td>
<td><span data-ttu-id="6f3f1-840">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-840">10001</span></span></td>
<td><span data-ttu-id="6f3f1-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-841">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-842">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="6f3f1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6f3f1-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-845">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-846">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-847">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-847">10001</span></span></td>
<td><span data-ttu-id="6f3f1-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-848">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-849">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6f3f1-850">5,297.69</span></span></td>
<td><span data-ttu-id="6f3f1-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-852">CC004</span></span></td>
<td><span data-ttu-id="6f3f1-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-853">Packaging</span></span></td>
<td><span data-ttu-id="6f3f1-854">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-854">10001</span></span></td>
<td><span data-ttu-id="6f3f1-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-855">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-856">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6f3f1-857">2,852.60</span></span></td>
<td><span data-ttu-id="6f3f1-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-859">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-860">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-861">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-861">10001</span></span></td>
<td><span data-ttu-id="6f3f1-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-862">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="6f3f1-864">-713.75</span></span></td>
<td><span data-ttu-id="6f3f1-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-866">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-867">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-868">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-868">10001</span></span></td>
<td><span data-ttu-id="6f3f1-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-869">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6f3f1-871">535.31</span></span></td>
<td><span data-ttu-id="6f3f1-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-873">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-874">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-875">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-875">10001</span></span></td>
<td><span data-ttu-id="6f3f1-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-876">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6f3f1-878">178.44</span></span></td>
<td><span data-ttu-id="6f3f1-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-880">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-881">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-882">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-882">10001</span></span></td>
<td><span data-ttu-id="6f3f1-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-883">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-884">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="6f3f1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6f3f1-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-887">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-888">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-889">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-889">10001</span></span></td>
<td><span data-ttu-id="6f3f1-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-890">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-891">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6f3f1-892">4,487.12</span></span></td>
<td><span data-ttu-id="6f3f1-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-894">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-895">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-896">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-896">10001</span></span></td>
<td><span data-ttu-id="6f3f1-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-897">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-898">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6f3f1-899">1,495.71</span></span></td>
<td><span data-ttu-id="6f3f1-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-901">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-902">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-903">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-903">10001</span></span></td>
<td><span data-ttu-id="6f3f1-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-904">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="6f3f1-906">-286.25</span></span></td>
<td><span data-ttu-id="6f3f1-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-908">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-909">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-910">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-910">10001</span></span></td>
<td><span data-ttu-id="6f3f1-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-911">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6f3f1-913">241.05</span></span></td>
<td><span data-ttu-id="6f3f1-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-915">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-916">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-917">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-917">10001</span></span></td>
<td><span data-ttu-id="6f3f1-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-918">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6f3f1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6f3f1-920">45.20</span></span></td>
<td><span data-ttu-id="6f3f1-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-922">CC003</span></span></td>
<td><span data-ttu-id="6f3f1-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="6f3f1-923">Assembly</span></span></td>
<td><span data-ttu-id="6f3f1-924">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-924">10001</span></span></td>
<td><span data-ttu-id="6f3f1-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-925">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-926">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="6f3f1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6f3f1-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-929">Prod 1</span></span></td>
<td><span data-ttu-id="6f3f1-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-930">Product 1</span></span></td>
<td><span data-ttu-id="6f3f1-931">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-931">10001</span></span></td>
<td><span data-ttu-id="6f3f1-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-932">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-933">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6f3f1-934">2,507.09</span></span></td>
<td><span data-ttu-id="6f3f1-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f3f1-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-936">Prod 2</span></span></td>
<td><span data-ttu-id="6f3f1-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-937">Product 2</span></span></td>
<td><span data-ttu-id="6f3f1-938">10001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-938">10001</span></span></td>
<td><span data-ttu-id="6f3f1-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-939">Electricity</span></span></td>
<td><span data-ttu-id="6f3f1-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-940">Variable cost</span></span></td>
<td><span data-ttu-id="6f3f1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6f3f1-941">470.08</span></span></td>
<td><span data-ttu-id="6f3f1-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="6f3f1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6f3f1-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-943">Conclusion</span></span>
<span data-ttu-id="6f3f1-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6f3f1-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6f3f1-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6f3f1-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6f3f1-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6f3f1-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6f3f1-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="6f3f1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6f3f1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6f3f1-951">CC099</span></span></th>
<th><span data-ttu-id="6f3f1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6f3f1-952">CC001</span></span></th>
<th><span data-ttu-id="6f3f1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6f3f1-953">CC002</span></span></th>
<th><span data-ttu-id="6f3f1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6f3f1-954">CC003</span></span></th>
<th><span data-ttu-id="6f3f1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6f3f1-955">CC004</span></span></th>
<th><span data-ttu-id="6f3f1-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-956">Proj 1</span></span></th>
<th><span data-ttu-id="6f3f1-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-957">Proj 2</span></span></th>
<th><span data-ttu-id="6f3f1-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="6f3f1-958">Prod 1</span></span></th>
<th><span data-ttu-id="6f3f1-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="6f3f1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6f3f1-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="6f3f1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6f3f1-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="6f3f1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-971">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6f3f1-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-973">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-974">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-975">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-976">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-977">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6f3f1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6f3f1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6f3f1-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="6f3f1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-982">000</span><span class="sxs-lookup"><span data-stu-id="6f3f1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-983">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-984">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-985">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-986">0.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-987">30.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-988">10.00</span><span class="sxs-lookup"><span data-stu-id="6f3f1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6f3f1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6f3f1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6f3f1-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6f3f1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6f3f1-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6f3f1-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6f3f1-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6f3f1-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="6f3f1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6f3f1-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="6f3f1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



