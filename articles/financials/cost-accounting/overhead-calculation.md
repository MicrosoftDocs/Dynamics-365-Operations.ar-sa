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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544045"
---
# <a name="overhead-calculation"></a><span data-ttu-id="79088-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="79088-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79088-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="79088-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="79088-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="79088-105">Term definition</span></span>
---------------

<span data-ttu-id="79088-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="79088-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="79088-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="79088-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="79088-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="79088-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="79088-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="79088-109">Rent</span></span>
-   <span data-ttu-id="79088-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-110">Electricity</span></span>
-   <span data-ttu-id="79088-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="79088-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="79088-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="79088-112">Overhead calculation overview</span></span>
<span data-ttu-id="79088-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="79088-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="79088-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="79088-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="79088-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="79088-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="79088-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="79088-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="79088-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="79088-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="79088-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="79088-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="79088-119">Version type</span></span>
-   <span data-ttu-id="79088-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="79088-120">Date and time</span></span>
-   <span data-ttu-id="79088-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="79088-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="79088-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="79088-122">Fiscal year</span></span>
-   <span data-ttu-id="79088-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="79088-123">Fiscal period</span></span>

<span data-ttu-id="79088-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="79088-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="79088-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="79088-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="79088-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="79088-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="79088-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="79088-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="79088-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="79088-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="79088-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="79088-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="79088-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="79088-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="79088-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="79088-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="79088-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="79088-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="79088-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="79088-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="79088-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="79088-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="79088-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="79088-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="79088-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="79088-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="79088-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="79088-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79088-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="79088-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="79088-140">Main account</span></span></th>
<th><span data-ttu-id="79088-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="79088-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="79088-143">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-143">CC099</span></span></td>
<td><span data-ttu-id="79088-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-144">Default cost center</span></span></td>
<td><span data-ttu-id="79088-145">10001</span><span class="sxs-lookup"><span data-stu-id="79088-145">10001</span></span></td>
<td><span data-ttu-id="79088-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-146">Electricity</span></span></td>
<td><span data-ttu-id="79088-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="79088-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="79088-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="79088-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="79088-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="79088-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="79088-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-151">Define the cost behavior rule</span></span>

<span data-ttu-id="79088-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="79088-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="79088-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="79088-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="79088-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="79088-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="79088-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="79088-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="79088-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="79088-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="79088-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="79088-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="79088-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="79088-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-160">Journal</span></span></th>
<th><span data-ttu-id="79088-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="79088-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79088-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="79088-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79088-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="79088-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-164">00001</span><span class="sxs-lookup"><span data-stu-id="79088-164">00001</span></span></td>
<td><span data-ttu-id="79088-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="79088-166">مالي</span><span class="sxs-lookup"><span data-stu-id="79088-166">Fiscal</span></span></td>
<td><span data-ttu-id="79088-167">2017</span><span class="sxs-lookup"><span data-stu-id="79088-167">2017</span></span></td>
<td><span data-ttu-id="79088-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-168">Period 1</span></span></td>
<td><span data-ttu-id="79088-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="79088-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="79088-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79088-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-173">Cost element</span></span></th>
<th><span data-ttu-id="79088-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-174">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="79088-177">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-177">CC099</span></span></td>
<td><span data-ttu-id="79088-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-178">Default cost center</span></span></td>
<td><span data-ttu-id="79088-179">10001</span><span class="sxs-lookup"><span data-stu-id="79088-179">10001</span></span></td>
<td><span data-ttu-id="79088-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-180">Electricity</span></span></td>
<td><span data-ttu-id="79088-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="79088-181">Unclassified</span></span></td>
<td><span data-ttu-id="79088-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79088-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-185">Cost element</span></span></th>
<th><span data-ttu-id="79088-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-186">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-187">Amount</span></span></th>
<th><span data-ttu-id="79088-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-189">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-189">CC099</span></span></td>
<td><span data-ttu-id="79088-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-190">Default cost center</span></span></td>
<td><span data-ttu-id="79088-191">10001</span><span class="sxs-lookup"><span data-stu-id="79088-191">10001</span></span></td>
<td><span data-ttu-id="79088-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-192">Electricity</span></span></td>
<td><span data-ttu-id="79088-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="79088-193">Unclassified</span></span></td>
<td><span data-ttu-id="79088-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-194">10,000.00</span></span></td>
<td><span data-ttu-id="79088-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-196">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-196">CC099</span></span></td>
<td><span data-ttu-id="79088-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-197">Default cost center</span></span></td>
<td><span data-ttu-id="79088-198">10001</span><span class="sxs-lookup"><span data-stu-id="79088-198">10001</span></span></td>
<td><span data-ttu-id="79088-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-199">Electricity</span></span></td>
<td><span data-ttu-id="79088-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="79088-200">Unclassified</span></span></td>
<td><span data-ttu-id="79088-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-201">-10,000.00</span></span></td>
<td><span data-ttu-id="79088-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-203">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-203">CC099</span></span></td>
<td><span data-ttu-id="79088-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-204">Default cost center</span></span></td>
<td><span data-ttu-id="79088-205">10001</span><span class="sxs-lookup"><span data-stu-id="79088-205">10001</span></span></td>
<td><span data-ttu-id="79088-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-206">Electricity</span></span></td>
<td><span data-ttu-id="79088-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-207">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="79088-208">1,000.00</span></span></td>
<td><span data-ttu-id="79088-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-210">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-210">CC099</span></span></td>
<td><span data-ttu-id="79088-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-211">Default cost center</span></span></td>
<td><span data-ttu-id="79088-212">10001</span><span class="sxs-lookup"><span data-stu-id="79088-212">10001</span></span></td>
<td><span data-ttu-id="79088-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-213">Electricity</span></span></td>
<td><span data-ttu-id="79088-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-214">Variable cost</span></span></td>
<td><span data-ttu-id="79088-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-215">9,000.00</span></span></td>
<td><span data-ttu-id="79088-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="79088-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="79088-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="79088-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="79088-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="79088-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="79088-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="79088-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-221">Define the cost distribution rule</span></span>

<span data-ttu-id="79088-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="79088-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="79088-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="79088-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="79088-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="79088-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="79088-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="79088-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="79088-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="79088-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="79088-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="79088-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-228">Cost object</span></span></th>
<th><span data-ttu-id="79088-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="79088-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-230">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-230">CC001</span></span></td>
<td><span data-ttu-id="79088-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-231">HR</span></span></td>
<td><span data-ttu-id="79088-232">1,000</span><span class="sxs-lookup"><span data-stu-id="79088-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-233">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-233">CC002</span></span></td>
<td><span data-ttu-id="79088-234">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-234">Finance</span></span></td>
<td><span data-ttu-id="79088-235">6,000</span><span class="sxs-lookup"><span data-stu-id="79088-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-236">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-236">CC003</span></span></td>
<td><span data-ttu-id="79088-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-237">Assembly</span></span></td>
<td><span data-ttu-id="79088-238">0</span><span class="sxs-lookup"><span data-stu-id="79088-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="79088-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-240">Cost object</span></span></th>
<th><span data-ttu-id="79088-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-241">Magnitude</span></span></th>
<th><span data-ttu-id="79088-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-242">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-244">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-244">CC001</span></span></td>
<td><span data-ttu-id="79088-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-245">HR</span></span></td>
<td><span data-ttu-id="79088-246">1,000</span><span class="sxs-lookup"><span data-stu-id="79088-246">1,000</span></span></td>
<td><span data-ttu-id="79088-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="79088-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="79088-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-249">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-249">CC002</span></span></td>
<td><span data-ttu-id="79088-250">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-250">Finance</span></span></td>
<td><span data-ttu-id="79088-251">6,000</span><span class="sxs-lookup"><span data-stu-id="79088-251">6,000</span></span></td>
<td><span data-ttu-id="79088-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="79088-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="79088-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-254">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-254">CC003</span></span></td>
<td><span data-ttu-id="79088-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-255">Assembly</span></span></td>
<td><span data-ttu-id="79088-256">0</span><span class="sxs-lookup"><span data-stu-id="79088-256">0</span></span></td>
<td><span data-ttu-id="79088-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="79088-258">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="79088-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="79088-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="79088-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-261">Cost object</span></span></th>
<th><span data-ttu-id="79088-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="79088-262">Formula</span></span></th>
<th><span data-ttu-id="79088-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-263">Magnitude</span></span></th>
<th><span data-ttu-id="79088-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-264">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-266">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-266">CC001</span></span></td>
<td><span data-ttu-id="79088-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-267">HR</span></span></td>
<td><span data-ttu-id="79088-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="79088-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="79088-269">1</span><span class="sxs-lookup"><span data-stu-id="79088-269">1</span></span></td>
<td><span data-ttu-id="79088-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="79088-271">500.00</span><span class="sxs-lookup"><span data-stu-id="79088-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-272">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-272">CC002</span></span></td>
<td><span data-ttu-id="79088-273">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-273">Finance</span></span></td>
<td><span data-ttu-id="79088-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="79088-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="79088-275">1</span><span class="sxs-lookup"><span data-stu-id="79088-275">1</span></span></td>
<td><span data-ttu-id="79088-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="79088-277">500.00</span><span class="sxs-lookup"><span data-stu-id="79088-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-278">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-278">CC003</span></span></td>
<td><span data-ttu-id="79088-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-279">Assembly</span></span></td>
<td><span data-ttu-id="79088-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="79088-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="79088-281">0</span><span class="sxs-lookup"><span data-stu-id="79088-281">0</span></span></td>
<td><span data-ttu-id="79088-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="79088-283">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="79088-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-285">Journal</span></span></th>
<th><span data-ttu-id="79088-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="79088-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79088-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="79088-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79088-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="79088-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-289">00002</span><span class="sxs-lookup"><span data-stu-id="79088-289">00002</span></span></td>
<td><span data-ttu-id="79088-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="79088-291">مالي</span><span class="sxs-lookup"><span data-stu-id="79088-291">Fiscal</span></span></td>
<td><span data-ttu-id="79088-292">2017</span><span class="sxs-lookup"><span data-stu-id="79088-292">2017</span></span></td>
<td><span data-ttu-id="79088-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-293">Period 1</span></span></td>
<td><span data-ttu-id="79088-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="79088-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="79088-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79088-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-298">Cost element</span></span></th>
<th><span data-ttu-id="79088-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-299">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-302">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-302">CC099</span></span></td>
<td><span data-ttu-id="79088-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-303">Default cost center</span></span></td>
<td><span data-ttu-id="79088-304">10001</span><span class="sxs-lookup"><span data-stu-id="79088-304">10001</span></span></td>
<td><span data-ttu-id="79088-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-305">Electricity</span></span></td>
<td><span data-ttu-id="79088-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-306">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="79088-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-309">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-309">CC099</span></span></td>
<td><span data-ttu-id="79088-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-310">Default cost center</span></span></td>
<td><span data-ttu-id="79088-311">10001</span><span class="sxs-lookup"><span data-stu-id="79088-311">10001</span></span></td>
<td><span data-ttu-id="79088-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-312">Electricity</span></span></td>
<td><span data-ttu-id="79088-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-313">Variable cost</span></span></td>
<td><span data-ttu-id="79088-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79088-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-317">Cost element</span></span></th>
<th><span data-ttu-id="79088-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-318">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-319">Amount</span></span></th>
<th><span data-ttu-id="79088-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-321">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-321">CC099</span></span></td>
<td><span data-ttu-id="79088-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-322">Default cost center</span></span></td>
<td><span data-ttu-id="79088-323">10001</span><span class="sxs-lookup"><span data-stu-id="79088-323">10001</span></span></td>
<td><span data-ttu-id="79088-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-324">Electricity</span></span></td>
<td><span data-ttu-id="79088-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-325">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="79088-326">-1,000.00</span></span></td>
<td><span data-ttu-id="79088-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-328">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-328">CC001</span></span></td>
<td><span data-ttu-id="79088-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-329">HR</span></span></td>
<td><span data-ttu-id="79088-330">10001</span><span class="sxs-lookup"><span data-stu-id="79088-330">10001</span></span></td>
<td><span data-ttu-id="79088-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-331">Electricity</span></span></td>
<td><span data-ttu-id="79088-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-332">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-333">500.00</span><span class="sxs-lookup"><span data-stu-id="79088-333">500.00</span></span></td>
<td><span data-ttu-id="79088-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-335">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-335">CC002</span></span></td>
<td><span data-ttu-id="79088-336">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-336">Finance</span></span></td>
<td><span data-ttu-id="79088-337">10001</span><span class="sxs-lookup"><span data-stu-id="79088-337">10001</span></span></td>
<td><span data-ttu-id="79088-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-338">Electricity</span></span></td>
<td><span data-ttu-id="79088-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-339">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-340">500.00</span><span class="sxs-lookup"><span data-stu-id="79088-340">500.00</span></span></td>
<td><span data-ttu-id="79088-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-342">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-342">CC099</span></span></td>
<td><span data-ttu-id="79088-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="79088-343">Default cost center</span></span></td>
<td><span data-ttu-id="79088-344">10001</span><span class="sxs-lookup"><span data-stu-id="79088-344">10001</span></span></td>
<td><span data-ttu-id="79088-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-345">Electricity</span></span></td>
<td><span data-ttu-id="79088-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-346">Variable cost</span></span></td>
<td><span data-ttu-id="79088-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="79088-347">-9,000.00</span></span></td>
<td><span data-ttu-id="79088-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-349">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-349">CC001</span></span></td>
<td><span data-ttu-id="79088-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-350">HR</span></span></td>
<td><span data-ttu-id="79088-351">10001</span><span class="sxs-lookup"><span data-stu-id="79088-351">10001</span></span></td>
<td><span data-ttu-id="79088-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-352">Electricity</span></span></td>
<td><span data-ttu-id="79088-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-353">Variable cost</span></span></td>
<td><span data-ttu-id="79088-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="79088-354">1,285.71</span></span></td>
<td><span data-ttu-id="79088-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-356">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-356">CC002</span></span></td>
<td><span data-ttu-id="79088-357">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-357">Finance</span></span></td>
<td><span data-ttu-id="79088-358">10001</span><span class="sxs-lookup"><span data-stu-id="79088-358">10001</span></span></td>
<td><span data-ttu-id="79088-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-359">Electricity</span></span></td>
<td><span data-ttu-id="79088-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-360">Variable cost</span></span></td>
<td><span data-ttu-id="79088-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="79088-361">7,714.29</span></span></td>
<td><span data-ttu-id="79088-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="79088-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="79088-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="79088-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="79088-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="79088-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="79088-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="79088-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="79088-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="79088-367">Define the overhead rate</span></span>

<span data-ttu-id="79088-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="79088-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="79088-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="79088-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-370">Cost object</span></span></th>
<th><span data-ttu-id="79088-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="79088-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-372">Proj 1</span></span></td>
<td><span data-ttu-id="79088-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-373">Project 1</span></span></td>
<td><span data-ttu-id="79088-374">3</span><span class="sxs-lookup"><span data-stu-id="79088-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-375">Proj 2</span></span></td>
<td><span data-ttu-id="79088-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-376">Project 2</span></span></td>
<td><span data-ttu-id="79088-377">1</span><span class="sxs-lookup"><span data-stu-id="79088-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-379">Cost object</span></span></th>
<th><span data-ttu-id="79088-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-380">Cost element</span></span></th>
<th><span data-ttu-id="79088-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-381">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="79088-382">Units</span></span></th>
<th><span data-ttu-id="79088-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="79088-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-384">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-384">CC001</span></span></td>
<td><span data-ttu-id="79088-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-385">HR</span></span></td>
<td><span data-ttu-id="79088-386">10001</span><span class="sxs-lookup"><span data-stu-id="79088-386">10001</span></span></td>
<td><span data-ttu-id="79088-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-387">Variable cost</span></span></td>
<td><span data-ttu-id="79088-388">1</span><span class="sxs-lookup"><span data-stu-id="79088-388">1</span></span></td>
<td><span data-ttu-id="79088-389">10</span><span class="sxs-lookup"><span data-stu-id="79088-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="79088-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-391">Cost object</span></span></th>
<th><span data-ttu-id="79088-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-392">Magnitude</span></span></th>
<th><span data-ttu-id="79088-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-393">Cost element</span></span></th>
<th><span data-ttu-id="79088-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-394">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-396">Proj 1</span></span></td>
<td><span data-ttu-id="79088-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-397">Project 1</span></span></td>
<td><span data-ttu-id="79088-398">3</span><span class="sxs-lookup"><span data-stu-id="79088-398">3</span></span></td>
<td><span data-ttu-id="79088-399">10001</span><span class="sxs-lookup"><span data-stu-id="79088-399">10001</span></span></td>
<td><span data-ttu-id="79088-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="79088-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="79088-401">30.00</span><span class="sxs-lookup"><span data-stu-id="79088-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-402">Proj 2</span></span></td>
<td><span data-ttu-id="79088-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-403">Project 2</span></span></td>
<td><span data-ttu-id="79088-404">1</span><span class="sxs-lookup"><span data-stu-id="79088-404">1</span></span></td>
<td><span data-ttu-id="79088-405">10001</span><span class="sxs-lookup"><span data-stu-id="79088-405">10001</span></span></td>
<td><span data-ttu-id="79088-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="79088-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="79088-407">10.00</span><span class="sxs-lookup"><span data-stu-id="79088-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="79088-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-409">Journal</span></span></th>
<th><span data-ttu-id="79088-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="79088-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79088-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="79088-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79088-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="79088-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-413">00003</span><span class="sxs-lookup"><span data-stu-id="79088-413">00003</span></span></td>
<td><span data-ttu-id="79088-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="79088-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="79088-415">مالي</span><span class="sxs-lookup"><span data-stu-id="79088-415">Fiscal</span></span></td>
<td><span data-ttu-id="79088-416">2017</span><span class="sxs-lookup"><span data-stu-id="79088-416">2017</span></span></td>
<td><span data-ttu-id="79088-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-417">Period 1</span></span></td>
<td><span data-ttu-id="79088-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="79088-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="79088-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79088-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-421">Cost object</span></span></th>
<th><span data-ttu-id="79088-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-424">Proj 1</span></span></td>
<td><span data-ttu-id="79088-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="79088-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="79088-426">3.00</span><span class="sxs-lookup"><span data-stu-id="79088-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-428">Proj 2</span></span></td>
<td><span data-ttu-id="79088-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="79088-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="79088-430">1.00</span><span class="sxs-lookup"><span data-stu-id="79088-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79088-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-433">Cost element</span></span></th>
<th><span data-ttu-id="79088-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-434">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-435">Amount</span></span></th>
<th><span data-ttu-id="79088-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="79088-437">CC0001</span></span></td>
<td><span data-ttu-id="79088-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-438">HR</span></span></td>
<td><span data-ttu-id="79088-439">10001</span><span class="sxs-lookup"><span data-stu-id="79088-439">10001</span></span></td>
<td><span data-ttu-id="79088-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-440">Electricity</span></span></td>
<td><span data-ttu-id="79088-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-441">Variable cost</span></span></td>
<td><span data-ttu-id="79088-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="79088-442">-30.00</span></span></td>
<td><span data-ttu-id="79088-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-444">Proj 1</span></span></td>
<td><span data-ttu-id="79088-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="79088-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="79088-446">10001</span><span class="sxs-lookup"><span data-stu-id="79088-446">10001</span></span></td>
<td><span data-ttu-id="79088-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-447">Electricity</span></span></td>
<td><span data-ttu-id="79088-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-448">Variable cost</span></span></td>
<td><span data-ttu-id="79088-449">30.00</span><span class="sxs-lookup"><span data-stu-id="79088-449">30.00</span></span></td>
<td><span data-ttu-id="79088-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-451">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-451">CC001</span></span></td>
<td><span data-ttu-id="79088-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-452">HR</span></span></td>
<td><span data-ttu-id="79088-453">10001</span><span class="sxs-lookup"><span data-stu-id="79088-453">10001</span></span></td>
<td><span data-ttu-id="79088-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-454">Electricity</span></span></td>
<td><span data-ttu-id="79088-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-455">Variable cost</span></span></td>
<td><span data-ttu-id="79088-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="79088-456">-10.00</span></span></td>
<td><span data-ttu-id="79088-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-458">Proj 2</span></span></td>
<td><span data-ttu-id="79088-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="79088-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="79088-460">10001</span><span class="sxs-lookup"><span data-stu-id="79088-460">10001</span></span></td>
<td><span data-ttu-id="79088-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-461">Electricity</span></span></td>
<td><span data-ttu-id="79088-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-462">Variable cost</span></span></td>
<td><span data-ttu-id="79088-463">10.00</span><span class="sxs-lookup"><span data-stu-id="79088-463">10.00</span></span></td>
<td><span data-ttu-id="79088-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="79088-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="79088-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="79088-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="79088-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="79088-468">يدعم تطبيق Finance and Operations طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="79088-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="79088-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="79088-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="79088-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="79088-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="79088-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="79088-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="79088-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="79088-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="79088-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="79088-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="79088-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="79088-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-475">Define the cost allocation</span></span>

<span data-ttu-id="79088-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="79088-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="79088-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="79088-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-479">Cost object</span></span></th>
<th><span data-ttu-id="79088-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-481">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-481">CC002</span></span></td>
<td><span data-ttu-id="79088-482">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-482">Finance</span></span></td>
<td><span data-ttu-id="79088-483">35</span><span class="sxs-lookup"><span data-stu-id="79088-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-484">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-484">CC003</span></span></td>
<td><span data-ttu-id="79088-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-485">Assembly</span></span></td>
<td><span data-ttu-id="79088-486">55</span><span class="sxs-lookup"><span data-stu-id="79088-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-487">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-487">CC004</span></span></td>
<td><span data-ttu-id="79088-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-488">Packaging</span></span></td>
<td><span data-ttu-id="79088-489">10</span><span class="sxs-lookup"><span data-stu-id="79088-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="79088-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="79088-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-492">Cost object</span></span></th>
<th><span data-ttu-id="79088-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="79088-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-494">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-494">CC003</span></span></td>
<td><span data-ttu-id="79088-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-495">Assembly</span></span></td>
<td><span data-ttu-id="79088-496">65</span><span class="sxs-lookup"><span data-stu-id="79088-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-497">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-497">CC004</span></span></td>
<td><span data-ttu-id="79088-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-498">Packaging</span></span></td>
<td><span data-ttu-id="79088-499">35</span><span class="sxs-lookup"><span data-stu-id="79088-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="79088-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="79088-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-502">Cost object</span></span></th>
<th><span data-ttu-id="79088-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="79088-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-504">Prod 1</span></span></td>
<td><span data-ttu-id="79088-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-505">Product 1</span></span></td>
<td><span data-ttu-id="79088-506">60</span><span class="sxs-lookup"><span data-stu-id="79088-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-507">Prod 2</span></span></td>
<td><span data-ttu-id="79088-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-508">Product 2</span></span></td>
<td><span data-ttu-id="79088-509">20</span><span class="sxs-lookup"><span data-stu-id="79088-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="79088-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="79088-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-512">Cost object</span></span></th>
<th><span data-ttu-id="79088-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="79088-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-514">Prod 1</span></span></td>
<td><span data-ttu-id="79088-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-515">Product 1</span></span></td>
<td><span data-ttu-id="79088-516">80</span><span class="sxs-lookup"><span data-stu-id="79088-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-517">Prod 2</span></span></td>
<td><span data-ttu-id="79088-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-518">Product 2</span></span></td>
<td><span data-ttu-id="79088-519">15</span><span class="sxs-lookup"><span data-stu-id="79088-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="79088-520">في Finance and Operations، بإمكان القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج أن تشتق من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="79088-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="79088-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="79088-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="79088-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="79088-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-523">Cost object</span></span></th>
<th><span data-ttu-id="79088-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-524">Magnitude</span></span></th>
<th><span data-ttu-id="79088-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-525">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-526">Amount</span></span></th>
<th><span data-ttu-id="79088-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-528">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-528">CC002</span></span></td>
<td><span data-ttu-id="79088-529">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-529">Finance</span></span></td>
<td><span data-ttu-id="79088-530">35</span><span class="sxs-lookup"><span data-stu-id="79088-530">35</span></span></td>
<td><span data-ttu-id="79088-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="79088-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="79088-532">175.00</span><span class="sxs-lookup"><span data-stu-id="79088-532">175.00</span></span></td>
<td><span data-ttu-id="79088-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-534">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-534">CC003</span></span></td>
<td><span data-ttu-id="79088-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-535">Assembly</span></span></td>
<td><span data-ttu-id="79088-536">55</span><span class="sxs-lookup"><span data-stu-id="79088-536">55</span></span></td>
<td><span data-ttu-id="79088-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="79088-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="79088-538">275.00</span><span class="sxs-lookup"><span data-stu-id="79088-538">275.00</span></span></td>
<td><span data-ttu-id="79088-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-540">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-540">CC004</span></span></td>
<td><span data-ttu-id="79088-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-541">Packaging</span></span></td>
<td><span data-ttu-id="79088-542">10</span><span class="sxs-lookup"><span data-stu-id="79088-542">10</span></span></td>
<td><span data-ttu-id="79088-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="79088-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="79088-544">50.00</span><span class="sxs-lookup"><span data-stu-id="79088-544">50.00</span></span></td>
<td><span data-ttu-id="79088-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-546">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-546">CC002</span></span></td>
<td><span data-ttu-id="79088-547">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-547">Finance</span></span></td>
<td><span data-ttu-id="79088-548">35</span><span class="sxs-lookup"><span data-stu-id="79088-548">35</span></span></td>
<td><span data-ttu-id="79088-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="79088-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="79088-550">436.00</span><span class="sxs-lookup"><span data-stu-id="79088-550">436.00</span></span></td>
<td><span data-ttu-id="79088-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-552">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-552">CC003</span></span></td>
<td><span data-ttu-id="79088-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-553">Assembly</span></span></td>
<td><span data-ttu-id="79088-554">55</span><span class="sxs-lookup"><span data-stu-id="79088-554">55</span></span></td>
<td><span data-ttu-id="79088-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="79088-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="79088-556">685.14</span><span class="sxs-lookup"><span data-stu-id="79088-556">685.14</span></span></td>
<td><span data-ttu-id="79088-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-558">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-558">CC004</span></span></td>
<td><span data-ttu-id="79088-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-559">Packaging</span></span></td>
<td><span data-ttu-id="79088-560">10</span><span class="sxs-lookup"><span data-stu-id="79088-560">10</span></span></td>
<td><span data-ttu-id="79088-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="79088-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="79088-562">124.57</span><span class="sxs-lookup"><span data-stu-id="79088-562">124.57</span></span></td>
<td><span data-ttu-id="79088-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="79088-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-565">Cost object</span></span></th>
<th><span data-ttu-id="79088-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-566">Magnitude</span></span></th>
<th><span data-ttu-id="79088-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-567">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-568">Amount</span></span></th>
<th><span data-ttu-id="79088-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-570">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-570">CC003</span></span></td>
<td><span data-ttu-id="79088-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-571">Assembly</span></span></td>
<td><span data-ttu-id="79088-572">65</span><span class="sxs-lookup"><span data-stu-id="79088-572">65</span></span></td>
<td><span data-ttu-id="79088-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="79088-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="79088-574">438.75</span><span class="sxs-lookup"><span data-stu-id="79088-574">438.75</span></span></td>
<td><span data-ttu-id="79088-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-576">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-576">CC004</span></span></td>
<td><span data-ttu-id="79088-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-577">Packaging</span></span></td>
<td><span data-ttu-id="79088-578">35</span><span class="sxs-lookup"><span data-stu-id="79088-578">35</span></span></td>
<td><span data-ttu-id="79088-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="79088-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="79088-580">236.25</span><span class="sxs-lookup"><span data-stu-id="79088-580">236.25</span></span></td>
<td><span data-ttu-id="79088-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-582">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-582">CC003</span></span></td>
<td><span data-ttu-id="79088-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-583">Assembly</span></span></td>
<td><span data-ttu-id="79088-584">65</span><span class="sxs-lookup"><span data-stu-id="79088-584">65</span></span></td>
<td><span data-ttu-id="79088-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="79088-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="79088-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="79088-586">5,297.69</span></span></td>
<td><span data-ttu-id="79088-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-588">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-588">CC004</span></span></td>
<td><span data-ttu-id="79088-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-589">Packaging</span></span></td>
<td><span data-ttu-id="79088-590">35</span><span class="sxs-lookup"><span data-stu-id="79088-590">35</span></span></td>
<td><span data-ttu-id="79088-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="79088-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="79088-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="79088-592">2,852.60</span></span></td>
<td><span data-ttu-id="79088-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="79088-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-595">Cost object</span></span></th>
<th><span data-ttu-id="79088-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-596">Magnitude</span></span></th>
<th><span data-ttu-id="79088-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-597">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-598">Amount</span></span></th>
<th><span data-ttu-id="79088-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-600">Prod 1</span></span></td>
<td><span data-ttu-id="79088-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-601">Product 1</span></span></td>
<td><span data-ttu-id="79088-602">60</span><span class="sxs-lookup"><span data-stu-id="79088-602">60</span></span></td>
<td><span data-ttu-id="79088-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="79088-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="79088-604">535.31</span><span class="sxs-lookup"><span data-stu-id="79088-604">535.31</span></span></td>
<td><span data-ttu-id="79088-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-606">Prod 2</span></span></td>
<td><span data-ttu-id="79088-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-607">Product 2</span></span></td>
<td><span data-ttu-id="79088-608">20</span><span class="sxs-lookup"><span data-stu-id="79088-608">20</span></span></td>
<td><span data-ttu-id="79088-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="79088-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="79088-610">178.44</span><span class="sxs-lookup"><span data-stu-id="79088-610">178.44</span></span></td>
<td><span data-ttu-id="79088-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-612">Prod 1</span></span></td>
<td><span data-ttu-id="79088-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-613">Product 1</span></span></td>
<td><span data-ttu-id="79088-614">60</span><span class="sxs-lookup"><span data-stu-id="79088-614">60</span></span></td>
<td><span data-ttu-id="79088-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="79088-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="79088-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="79088-616">4,487.12</span></span></td>
<td><span data-ttu-id="79088-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-618">Prod 2</span></span></td>
<td><span data-ttu-id="79088-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-619">Product 2</span></span></td>
<td><span data-ttu-id="79088-620">20</span><span class="sxs-lookup"><span data-stu-id="79088-620">20</span></span></td>
<td><span data-ttu-id="79088-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="79088-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="79088-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="79088-622">1,495.71</span></span></td>
<td><span data-ttu-id="79088-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79088-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="79088-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-625">Cost object</span></span></th>
<th><span data-ttu-id="79088-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="79088-626">Magnitude</span></span></th>
<th><span data-ttu-id="79088-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="79088-627">Allocation factor</span></span></th>
<th><span data-ttu-id="79088-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-628">Amount</span></span></th>
<th><span data-ttu-id="79088-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-630">Prod 1</span></span></td>
<td><span data-ttu-id="79088-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-631">Product 1</span></span></td>
<td><span data-ttu-id="79088-632">80</span><span class="sxs-lookup"><span data-stu-id="79088-632">80</span></span></td>
<td><span data-ttu-id="79088-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="79088-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="79088-634">241.05</span><span class="sxs-lookup"><span data-stu-id="79088-634">241.05</span></span></td>
<td><span data-ttu-id="79088-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-636">Prod 2</span></span></td>
<td><span data-ttu-id="79088-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-637">Product 2</span></span></td>
<td><span data-ttu-id="79088-638">15</span><span class="sxs-lookup"><span data-stu-id="79088-638">15</span></span></td>
<td><span data-ttu-id="79088-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="79088-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="79088-640">45.20</span><span class="sxs-lookup"><span data-stu-id="79088-640">45.20</span></span></td>
<td><span data-ttu-id="79088-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-642">Prod 1</span></span></td>
<td><span data-ttu-id="79088-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-643">Product 1</span></span></td>
<td><span data-ttu-id="79088-644">80</span><span class="sxs-lookup"><span data-stu-id="79088-644">80</span></span></td>
<td><span data-ttu-id="79088-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="79088-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="79088-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="79088-646">2,507.09</span></span></td>
<td><span data-ttu-id="79088-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-648">Prod 2</span></span></td>
<td><span data-ttu-id="79088-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-649">Product 2</span></span></td>
<td><span data-ttu-id="79088-650">15</span><span class="sxs-lookup"><span data-stu-id="79088-650">15</span></span></td>
<td><span data-ttu-id="79088-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="79088-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="79088-652">470.08</span><span class="sxs-lookup"><span data-stu-id="79088-652">470.08</span></span></td>
<td><span data-ttu-id="79088-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="79088-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="79088-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="79088-655">Journal</span></span></th>
<th><span data-ttu-id="79088-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="79088-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79088-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="79088-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79088-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="79088-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-659">00004</span><span class="sxs-lookup"><span data-stu-id="79088-659">00004</span></span></td>
<td><span data-ttu-id="79088-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="79088-661">مالي</span><span class="sxs-lookup"><span data-stu-id="79088-661">Fiscal</span></span></td>
<td><span data-ttu-id="79088-662">2017</span><span class="sxs-lookup"><span data-stu-id="79088-662">2017</span></span></td>
<td><span data-ttu-id="79088-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-663">Period 1</span></span></td>
<td><span data-ttu-id="79088-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="79088-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="79088-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="79088-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79088-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79088-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-668">Cost element</span></span></th>
<th><span data-ttu-id="79088-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-669">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-672">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-672">CC001</span></span></td>
<td><span data-ttu-id="79088-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-673">HR</span></span></td>
<td><span data-ttu-id="79088-674">10001</span><span class="sxs-lookup"><span data-stu-id="79088-674">10001</span></span></td>
<td><span data-ttu-id="79088-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-675">Electricity</span></span></td>
<td><span data-ttu-id="79088-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-676">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-677">500.00</span><span class="sxs-lookup"><span data-stu-id="79088-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-679">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-679">CC001</span></span></td>
<td><span data-ttu-id="79088-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-680">HR</span></span></td>
<td><span data-ttu-id="79088-681">10001</span><span class="sxs-lookup"><span data-stu-id="79088-681">10001</span></span></td>
<td><span data-ttu-id="79088-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-682">Electricity</span></span></td>
<td><span data-ttu-id="79088-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-683">Variable cost</span></span></td>
<td><span data-ttu-id="79088-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="79088-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-686">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-686">CC002</span></span></td>
<td><span data-ttu-id="79088-687">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-687">Finance</span></span></td>
<td><span data-ttu-id="79088-688">10001</span><span class="sxs-lookup"><span data-stu-id="79088-688">10001</span></span></td>
<td><span data-ttu-id="79088-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-689">Electricity</span></span></td>
<td><span data-ttu-id="79088-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-690">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-691">675.00</span><span class="sxs-lookup"><span data-stu-id="79088-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-693">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-693">CC002</span></span></td>
<td><span data-ttu-id="79088-694">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-694">Finance</span></span></td>
<td><span data-ttu-id="79088-695">10001</span><span class="sxs-lookup"><span data-stu-id="79088-695">10001</span></span></td>
<td><span data-ttu-id="79088-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-696">Electricity</span></span></td>
<td><span data-ttu-id="79088-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-697">Variable cost</span></span></td>
<td><span data-ttu-id="79088-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="79088-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-700">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-700">CC003</span></span></td>
<td><span data-ttu-id="79088-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-701">Assembly</span></span></td>
<td><span data-ttu-id="79088-702">10001</span><span class="sxs-lookup"><span data-stu-id="79088-702">10001</span></span></td>
<td><span data-ttu-id="79088-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-703">Electricity</span></span></td>
<td><span data-ttu-id="79088-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-704">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-705">713.75</span><span class="sxs-lookup"><span data-stu-id="79088-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-707">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-707">CC003</span></span></td>
<td><span data-ttu-id="79088-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-708">Assembly</span></span></td>
<td><span data-ttu-id="79088-709">10001</span><span class="sxs-lookup"><span data-stu-id="79088-709">10001</span></span></td>
<td><span data-ttu-id="79088-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-710">Electricity</span></span></td>
<td><span data-ttu-id="79088-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-711">Variable cost</span></span></td>
<td><span data-ttu-id="79088-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="79088-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-714">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-714">CC003</span></span></td>
<td><span data-ttu-id="79088-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-715">Packaging</span></span></td>
<td><span data-ttu-id="79088-716">10001</span><span class="sxs-lookup"><span data-stu-id="79088-716">10001</span></span></td>
<td><span data-ttu-id="79088-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-717">Electricity</span></span></td>
<td><span data-ttu-id="79088-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-718">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-719">286.25</span><span class="sxs-lookup"><span data-stu-id="79088-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-721">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-721">CC003</span></span></td>
<td><span data-ttu-id="79088-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-722">Packaging</span></span></td>
<td><span data-ttu-id="79088-723">10001</span><span class="sxs-lookup"><span data-stu-id="79088-723">10001</span></span></td>
<td><span data-ttu-id="79088-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-724">Electricity</span></span></td>
<td><span data-ttu-id="79088-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-725">Variable cost</span></span></td>
<td><span data-ttu-id="79088-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="79088-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-728">Prod 1</span></span></td>
<td><span data-ttu-id="79088-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-729">Product 1</span></span></td>
<td><span data-ttu-id="79088-730">10001</span><span class="sxs-lookup"><span data-stu-id="79088-730">10001</span></span></td>
<td><span data-ttu-id="79088-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-731">Electricity</span></span></td>
<td><span data-ttu-id="79088-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-732">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-733">776.36</span><span class="sxs-lookup"><span data-stu-id="79088-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-735">Prod 1</span></span></td>
<td><span data-ttu-id="79088-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-736">Product 1</span></span></td>
<td><span data-ttu-id="79088-737">10001</span><span class="sxs-lookup"><span data-stu-id="79088-737">10001</span></span></td>
<td><span data-ttu-id="79088-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-738">Electricity</span></span></td>
<td><span data-ttu-id="79088-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-739">Variable cost</span></span></td>
<td><span data-ttu-id="79088-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="79088-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-742">Prod 2</span></span></td>
<td><span data-ttu-id="79088-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-743">Product 1</span></span></td>
<td><span data-ttu-id="79088-744">10001</span><span class="sxs-lookup"><span data-stu-id="79088-744">10001</span></span></td>
<td><span data-ttu-id="79088-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-745">Electricity</span></span></td>
<td><span data-ttu-id="79088-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-746">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-747">223.64</span><span class="sxs-lookup"><span data-stu-id="79088-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="79088-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-749">Prod 2</span></span></td>
<td><span data-ttu-id="79088-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-750">Product 1</span></span></td>
<td><span data-ttu-id="79088-751">10001</span><span class="sxs-lookup"><span data-stu-id="79088-751">10001</span></span></td>
<td><span data-ttu-id="79088-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-752">Electricity</span></span></td>
<td><span data-ttu-id="79088-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-753">Variable cost</span></span></td>
<td><span data-ttu-id="79088-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="79088-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79088-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79088-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79088-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-757">Cost element</span></span></th>
<th><span data-ttu-id="79088-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-758">Cost behavior</span></span></th>
<th><span data-ttu-id="79088-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="79088-759">Amount</span></span></th>
<th><span data-ttu-id="79088-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="79088-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79088-761">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-761">CC001</span></span></td>
<td><span data-ttu-id="79088-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-762">HR</span></span></td>
<td><span data-ttu-id="79088-763">10001</span><span class="sxs-lookup"><span data-stu-id="79088-763">10001</span></span></td>
<td><span data-ttu-id="79088-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-764">Electricity</span></span></td>
<td><span data-ttu-id="79088-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-765">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="79088-766">-500.00</span></span></td>
<td><span data-ttu-id="79088-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-768">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-768">CC002</span></span></td>
<td><span data-ttu-id="79088-769">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-769">Finance</span></span></td>
<td><span data-ttu-id="79088-770">10001</span><span class="sxs-lookup"><span data-stu-id="79088-770">10001</span></span></td>
<td><span data-ttu-id="79088-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-771">Electricity</span></span></td>
<td><span data-ttu-id="79088-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-772">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-773">175.00</span><span class="sxs-lookup"><span data-stu-id="79088-773">175.00</span></span></td>
<td><span data-ttu-id="79088-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-775">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-775">CC003</span></span></td>
<td><span data-ttu-id="79088-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-776">Assembly</span></span></td>
<td><span data-ttu-id="79088-777">10001</span><span class="sxs-lookup"><span data-stu-id="79088-777">10001</span></span></td>
<td><span data-ttu-id="79088-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-778">Electricity</span></span></td>
<td><span data-ttu-id="79088-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-779">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-780">275.00</span><span class="sxs-lookup"><span data-stu-id="79088-780">275.00</span></span></td>
<td><span data-ttu-id="79088-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-782">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-782">CC004</span></span></td>
<td><span data-ttu-id="79088-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-783">Packaging</span></span></td>
<td><span data-ttu-id="79088-784">10001</span><span class="sxs-lookup"><span data-stu-id="79088-784">10001</span></span></td>
<td><span data-ttu-id="79088-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-785">Electricity</span></span></td>
<td><span data-ttu-id="79088-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-786">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-787">50,00</span><span class="sxs-lookup"><span data-stu-id="79088-787">50,00</span></span></td>
<td><span data-ttu-id="79088-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-789">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-789">CC001</span></span></td>
<td><span data-ttu-id="79088-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="79088-790">HR</span></span></td>
<td><span data-ttu-id="79088-791">10001</span><span class="sxs-lookup"><span data-stu-id="79088-791">10001</span></span></td>
<td><span data-ttu-id="79088-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-792">Electricity</span></span></td>
<td><span data-ttu-id="79088-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-793">Variable cost</span></span></td>
<td><span data-ttu-id="79088-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="79088-794">-1,245.71</span></span></td>
<td><span data-ttu-id="79088-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-796">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-796">CC002</span></span></td>
<td><span data-ttu-id="79088-797">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-797">Finance</span></span></td>
<td><span data-ttu-id="79088-798">10001</span><span class="sxs-lookup"><span data-stu-id="79088-798">10001</span></span></td>
<td><span data-ttu-id="79088-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-799">Electricity</span></span></td>
<td><span data-ttu-id="79088-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-800">Variable cost</span></span></td>
<td><span data-ttu-id="79088-801">436.00</span><span class="sxs-lookup"><span data-stu-id="79088-801">436.00</span></span></td>
<td><span data-ttu-id="79088-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-803">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-803">CC003</span></span></td>
<td><span data-ttu-id="79088-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-804">Assembly</span></span></td>
<td><span data-ttu-id="79088-805">10001</span><span class="sxs-lookup"><span data-stu-id="79088-805">10001</span></span></td>
<td><span data-ttu-id="79088-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-806">Electricity</span></span></td>
<td><span data-ttu-id="79088-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-807">Variable cost</span></span></td>
<td><span data-ttu-id="79088-808">685.14</span><span class="sxs-lookup"><span data-stu-id="79088-808">685.14</span></span></td>
<td><span data-ttu-id="79088-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-810">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-810">CC004</span></span></td>
<td><span data-ttu-id="79088-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-811">Packaging</span></span></td>
<td><span data-ttu-id="79088-812">10001</span><span class="sxs-lookup"><span data-stu-id="79088-812">10001</span></span></td>
<td><span data-ttu-id="79088-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-813">Electricity</span></span></td>
<td><span data-ttu-id="79088-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-814">Variable cost</span></span></td>
<td><span data-ttu-id="79088-815">124.57</span><span class="sxs-lookup"><span data-stu-id="79088-815">124.57</span></span></td>
<td><span data-ttu-id="79088-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-817">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-817">CC002</span></span></td>
<td><span data-ttu-id="79088-818">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-818">Finance</span></span></td>
<td><span data-ttu-id="79088-819">10001</span><span class="sxs-lookup"><span data-stu-id="79088-819">10001</span></span></td>
<td><span data-ttu-id="79088-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-820">Electricity</span></span></td>
<td><span data-ttu-id="79088-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-821">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="79088-822">-675.00</span></span></td>
<td><span data-ttu-id="79088-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-824">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-824">CC003</span></span></td>
<td><span data-ttu-id="79088-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-825">Assembly</span></span></td>
<td><span data-ttu-id="79088-826">10001</span><span class="sxs-lookup"><span data-stu-id="79088-826">10001</span></span></td>
<td><span data-ttu-id="79088-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-827">Electricity</span></span></td>
<td><span data-ttu-id="79088-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-828">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-829">438.75</span><span class="sxs-lookup"><span data-stu-id="79088-829">438.75</span></span></td>
<td><span data-ttu-id="79088-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-831">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-831">CC004</span></span></td>
<td><span data-ttu-id="79088-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-832">Packaging</span></span></td>
<td><span data-ttu-id="79088-833">10001</span><span class="sxs-lookup"><span data-stu-id="79088-833">10001</span></span></td>
<td><span data-ttu-id="79088-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-834">Electricity</span></span></td>
<td><span data-ttu-id="79088-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-835">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-836">236.25</span><span class="sxs-lookup"><span data-stu-id="79088-836">236.25</span></span></td>
<td><span data-ttu-id="79088-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-838">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-838">CC002</span></span></td>
<td><span data-ttu-id="79088-839">المالية</span><span class="sxs-lookup"><span data-stu-id="79088-839">Finance</span></span></td>
<td><span data-ttu-id="79088-840">10001</span><span class="sxs-lookup"><span data-stu-id="79088-840">10001</span></span></td>
<td><span data-ttu-id="79088-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-841">Electricity</span></span></td>
<td><span data-ttu-id="79088-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-842">Variable cost</span></span></td>
<td><span data-ttu-id="79088-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="79088-843">-8,150.29</span></span></td>
<td><span data-ttu-id="79088-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-845">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-845">CC003</span></span></td>
<td><span data-ttu-id="79088-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-846">Assembly</span></span></td>
<td><span data-ttu-id="79088-847">10001</span><span class="sxs-lookup"><span data-stu-id="79088-847">10001</span></span></td>
<td><span data-ttu-id="79088-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-848">Electricity</span></span></td>
<td><span data-ttu-id="79088-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-849">Variable cost</span></span></td>
<td><span data-ttu-id="79088-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="79088-850">5,297.69</span></span></td>
<td><span data-ttu-id="79088-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-852">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-852">CC004</span></span></td>
<td><span data-ttu-id="79088-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="79088-853">Packaging</span></span></td>
<td><span data-ttu-id="79088-854">10001</span><span class="sxs-lookup"><span data-stu-id="79088-854">10001</span></span></td>
<td><span data-ttu-id="79088-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-855">Electricity</span></span></td>
<td><span data-ttu-id="79088-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-856">Variable cost</span></span></td>
<td><span data-ttu-id="79088-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="79088-857">2,852.60</span></span></td>
<td><span data-ttu-id="79088-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-859">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-859">CC003</span></span></td>
<td><span data-ttu-id="79088-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-860">Assembly</span></span></td>
<td><span data-ttu-id="79088-861">10001</span><span class="sxs-lookup"><span data-stu-id="79088-861">10001</span></span></td>
<td><span data-ttu-id="79088-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-862">Electricity</span></span></td>
<td><span data-ttu-id="79088-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-863">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="79088-864">-713.75</span></span></td>
<td><span data-ttu-id="79088-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-866">Prod 1</span></span></td>
<td><span data-ttu-id="79088-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-867">Product 1</span></span></td>
<td><span data-ttu-id="79088-868">10001</span><span class="sxs-lookup"><span data-stu-id="79088-868">10001</span></span></td>
<td><span data-ttu-id="79088-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-869">Electricity</span></span></td>
<td><span data-ttu-id="79088-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-870">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-871">535.31</span><span class="sxs-lookup"><span data-stu-id="79088-871">535.31</span></span></td>
<td><span data-ttu-id="79088-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-873">Prod 2</span></span></td>
<td><span data-ttu-id="79088-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-874">Product 2</span></span></td>
<td><span data-ttu-id="79088-875">10001</span><span class="sxs-lookup"><span data-stu-id="79088-875">10001</span></span></td>
<td><span data-ttu-id="79088-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-876">Electricity</span></span></td>
<td><span data-ttu-id="79088-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-877">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-878">178.44</span><span class="sxs-lookup"><span data-stu-id="79088-878">178.44</span></span></td>
<td><span data-ttu-id="79088-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-880">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-880">CC003</span></span></td>
<td><span data-ttu-id="79088-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-881">Assembly</span></span></td>
<td><span data-ttu-id="79088-882">10001</span><span class="sxs-lookup"><span data-stu-id="79088-882">10001</span></span></td>
<td><span data-ttu-id="79088-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-883">Electricity</span></span></td>
<td><span data-ttu-id="79088-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-884">Variable cost</span></span></td>
<td><span data-ttu-id="79088-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="79088-885">-5,982.83</span></span></td>
<td><span data-ttu-id="79088-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-887">Prod 1</span></span></td>
<td><span data-ttu-id="79088-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-888">Product 1</span></span></td>
<td><span data-ttu-id="79088-889">10001</span><span class="sxs-lookup"><span data-stu-id="79088-889">10001</span></span></td>
<td><span data-ttu-id="79088-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-890">Electricity</span></span></td>
<td><span data-ttu-id="79088-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-891">Variable cost</span></span></td>
<td><span data-ttu-id="79088-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="79088-892">4,487.12</span></span></td>
<td><span data-ttu-id="79088-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-894">Prod 2</span></span></td>
<td><span data-ttu-id="79088-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-895">Product 2</span></span></td>
<td><span data-ttu-id="79088-896">10001</span><span class="sxs-lookup"><span data-stu-id="79088-896">10001</span></span></td>
<td><span data-ttu-id="79088-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-897">Electricity</span></span></td>
<td><span data-ttu-id="79088-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-898">Variable cost</span></span></td>
<td><span data-ttu-id="79088-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="79088-899">1,495.71</span></span></td>
<td><span data-ttu-id="79088-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-901">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-901">CC003</span></span></td>
<td><span data-ttu-id="79088-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-902">Assembly</span></span></td>
<td><span data-ttu-id="79088-903">10001</span><span class="sxs-lookup"><span data-stu-id="79088-903">10001</span></span></td>
<td><span data-ttu-id="79088-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-904">Electricity</span></span></td>
<td><span data-ttu-id="79088-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-905">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="79088-906">-286.25</span></span></td>
<td><span data-ttu-id="79088-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-908">Prod 1</span></span></td>
<td><span data-ttu-id="79088-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-909">Product 1</span></span></td>
<td><span data-ttu-id="79088-910">10001</span><span class="sxs-lookup"><span data-stu-id="79088-910">10001</span></span></td>
<td><span data-ttu-id="79088-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-911">Electricity</span></span></td>
<td><span data-ttu-id="79088-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-912">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-913">241.05</span><span class="sxs-lookup"><span data-stu-id="79088-913">241.05</span></span></td>
<td><span data-ttu-id="79088-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-915">Prod 2</span></span></td>
<td><span data-ttu-id="79088-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-916">Product 2</span></span></td>
<td><span data-ttu-id="79088-917">10001</span><span class="sxs-lookup"><span data-stu-id="79088-917">10001</span></span></td>
<td><span data-ttu-id="79088-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-918">Electricity</span></span></td>
<td><span data-ttu-id="79088-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-919">Fixed cost</span></span></td>
<td><span data-ttu-id="79088-920">45.20</span><span class="sxs-lookup"><span data-stu-id="79088-920">45.20</span></span></td>
<td><span data-ttu-id="79088-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-922">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-922">CC003</span></span></td>
<td><span data-ttu-id="79088-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="79088-923">Assembly</span></span></td>
<td><span data-ttu-id="79088-924">10001</span><span class="sxs-lookup"><span data-stu-id="79088-924">10001</span></span></td>
<td><span data-ttu-id="79088-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-925">Electricity</span></span></td>
<td><span data-ttu-id="79088-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-926">Variable cost</span></span></td>
<td><span data-ttu-id="79088-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="79088-927">-2,977.17</span></span></td>
<td><span data-ttu-id="79088-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-929">Prod 1</span></span></td>
<td><span data-ttu-id="79088-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-930">Product 1</span></span></td>
<td><span data-ttu-id="79088-931">10001</span><span class="sxs-lookup"><span data-stu-id="79088-931">10001</span></span></td>
<td><span data-ttu-id="79088-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-932">Electricity</span></span></td>
<td><span data-ttu-id="79088-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-933">Variable cost</span></span></td>
<td><span data-ttu-id="79088-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="79088-934">2,507.09</span></span></td>
<td><span data-ttu-id="79088-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79088-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-936">Prod 2</span></span></td>
<td><span data-ttu-id="79088-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-937">Product 2</span></span></td>
<td><span data-ttu-id="79088-938">10001</span><span class="sxs-lookup"><span data-stu-id="79088-938">10001</span></span></td>
<td><span data-ttu-id="79088-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-939">Electricity</span></span></td>
<td><span data-ttu-id="79088-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-940">Variable cost</span></span></td>
<td><span data-ttu-id="79088-941">470.08</span><span class="sxs-lookup"><span data-stu-id="79088-941">470.08</span></span></td>
<td><span data-ttu-id="79088-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="79088-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="79088-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="79088-943">Conclusion</span></span>
<span data-ttu-id="79088-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="79088-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="79088-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="79088-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="79088-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="79088-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="79088-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="79088-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="79088-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="79088-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="79088-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="79088-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="79088-951">CC099</span><span class="sxs-lookup"><span data-stu-id="79088-951">CC099</span></span></th>
<th><span data-ttu-id="79088-952">CC001</span><span class="sxs-lookup"><span data-stu-id="79088-952">CC001</span></span></th>
<th><span data-ttu-id="79088-953">CC002</span><span class="sxs-lookup"><span data-stu-id="79088-953">CC002</span></span></th>
<th><span data-ttu-id="79088-954">CC003</span><span class="sxs-lookup"><span data-stu-id="79088-954">CC003</span></span></th>
<th><span data-ttu-id="79088-955">CC004</span><span class="sxs-lookup"><span data-stu-id="79088-955">CC004</span></span></th>
<th><span data-ttu-id="79088-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="79088-956">Proj 1</span></span></th>
<th><span data-ttu-id="79088-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="79088-957">Proj 2</span></span></th>
<th><span data-ttu-id="79088-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="79088-958">Prod 1</span></span></th>
<th><span data-ttu-id="79088-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="79088-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="79088-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="79088-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="79088-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="79088-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="79088-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="79088-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="79088-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-971">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="79088-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="79088-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-973">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-974">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-975">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-976">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-977">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="79088-978">776.36</span><span class="sxs-lookup"><span data-stu-id="79088-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-979">223.64</span><span class="sxs-lookup"><span data-stu-id="79088-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="79088-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="79088-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-982">000</span><span class="sxs-lookup"><span data-stu-id="79088-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-983">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-984">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-985">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-986">0.00</span><span class="sxs-lookup"><span data-stu-id="79088-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-987">30.00</span><span class="sxs-lookup"><span data-stu-id="79088-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-988">10.00</span><span class="sxs-lookup"><span data-stu-id="79088-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="79088-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="79088-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79088-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="79088-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="79088-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="79088-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="79088-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="79088-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="79088-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="79088-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="79088-996">لمزيد من المعلومات، راجع [تجميع التكلفة](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="79088-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



