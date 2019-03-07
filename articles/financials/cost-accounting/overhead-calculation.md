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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "335107"
---
# <a name="overhead-calculation"></a><span data-ttu-id="0540e-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="0540e-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0540e-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="0540e-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="0540e-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="0540e-105">Term definition</span></span>
---------------

<span data-ttu-id="0540e-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="0540e-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="0540e-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="0540e-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="0540e-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="0540e-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="0540e-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="0540e-109">Rent</span></span>
-   <span data-ttu-id="0540e-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-110">Electricity</span></span>
-   <span data-ttu-id="0540e-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="0540e-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="0540e-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="0540e-112">Overhead calculation overview</span></span>
<span data-ttu-id="0540e-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="0540e-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="0540e-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="0540e-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="0540e-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="0540e-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="0540e-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="0540e-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="0540e-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="0540e-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="0540e-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="0540e-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="0540e-119">Version type</span></span>
-   <span data-ttu-id="0540e-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="0540e-120">Date and time</span></span>
-   <span data-ttu-id="0540e-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="0540e-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="0540e-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-122">Fiscal year</span></span>
-   <span data-ttu-id="0540e-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-123">Fiscal period</span></span>

<span data-ttu-id="0540e-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="0540e-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="0540e-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="0540e-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="0540e-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="0540e-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="0540e-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="0540e-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="0540e-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="0540e-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="0540e-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="0540e-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="0540e-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="0540e-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="0540e-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="0540e-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="0540e-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="0540e-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="0540e-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="0540e-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="0540e-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="0540e-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="0540e-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="0540e-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="0540e-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="0540e-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="0540e-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="0540e-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="0540e-140">Main account</span></span></th>
<th><span data-ttu-id="0540e-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="0540e-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="0540e-143">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-143">CC099</span></span></td>
<td><span data-ttu-id="0540e-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-144">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-145">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-145">10001</span></span></td>
<td><span data-ttu-id="0540e-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-146">Electricity</span></span></td>
<td><span data-ttu-id="0540e-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="0540e-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="0540e-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="0540e-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="0540e-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="0540e-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="0540e-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-151">Define the cost behavior rule</span></span>

<span data-ttu-id="0540e-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="0540e-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="0540e-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="0540e-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="0540e-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="0540e-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="0540e-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="0540e-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="0540e-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="0540e-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="0540e-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="0540e-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="0540e-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="0540e-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-160">Journal</span></span></th>
<th><span data-ttu-id="0540e-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="0540e-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0540e-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="0540e-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0540e-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="0540e-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-164">00001</span><span class="sxs-lookup"><span data-stu-id="0540e-164">00001</span></span></td>
<td><span data-ttu-id="0540e-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="0540e-166">مالي</span><span class="sxs-lookup"><span data-stu-id="0540e-166">Fiscal</span></span></td>
<td><span data-ttu-id="0540e-167">2017</span><span class="sxs-lookup"><span data-stu-id="0540e-167">2017</span></span></td>
<td><span data-ttu-id="0540e-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-168">Period 1</span></span></td>
<td><span data-ttu-id="0540e-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0540e-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="0540e-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-173">Cost element</span></span></th>
<th><span data-ttu-id="0540e-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-174">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="0540e-177">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-177">CC099</span></span></td>
<td><span data-ttu-id="0540e-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-178">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-179">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-179">10001</span></span></td>
<td><span data-ttu-id="0540e-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-180">Electricity</span></span></td>
<td><span data-ttu-id="0540e-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="0540e-181">Unclassified</span></span></td>
<td><span data-ttu-id="0540e-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0540e-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-185">Cost element</span></span></th>
<th><span data-ttu-id="0540e-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-186">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-187">Amount</span></span></th>
<th><span data-ttu-id="0540e-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-189">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-189">CC099</span></span></td>
<td><span data-ttu-id="0540e-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-190">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-191">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-191">10001</span></span></td>
<td><span data-ttu-id="0540e-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-192">Electricity</span></span></td>
<td><span data-ttu-id="0540e-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="0540e-193">Unclassified</span></span></td>
<td><span data-ttu-id="0540e-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-194">10,000.00</span></span></td>
<td><span data-ttu-id="0540e-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-196">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-196">CC099</span></span></td>
<td><span data-ttu-id="0540e-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-197">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-198">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-198">10001</span></span></td>
<td><span data-ttu-id="0540e-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-199">Electricity</span></span></td>
<td><span data-ttu-id="0540e-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="0540e-200">Unclassified</span></span></td>
<td><span data-ttu-id="0540e-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-201">-10,000.00</span></span></td>
<td><span data-ttu-id="0540e-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-203">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-203">CC099</span></span></td>
<td><span data-ttu-id="0540e-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-204">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-205">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-205">10001</span></span></td>
<td><span data-ttu-id="0540e-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-206">Electricity</span></span></td>
<td><span data-ttu-id="0540e-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-207">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-208">1,000.00</span></span></td>
<td><span data-ttu-id="0540e-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-210">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-210">CC099</span></span></td>
<td><span data-ttu-id="0540e-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-211">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-212">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-212">10001</span></span></td>
<td><span data-ttu-id="0540e-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-213">Electricity</span></span></td>
<td><span data-ttu-id="0540e-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-214">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-215">9,000.00</span></span></td>
<td><span data-ttu-id="0540e-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="0540e-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="0540e-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="0540e-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="0540e-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="0540e-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="0540e-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="0540e-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-221">Define the cost distribution rule</span></span>

<span data-ttu-id="0540e-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="0540e-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="0540e-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="0540e-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="0540e-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="0540e-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="0540e-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="0540e-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="0540e-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="0540e-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="0540e-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="0540e-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-228">Cost object</span></span></th>
<th><span data-ttu-id="0540e-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="0540e-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-230">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-230">CC001</span></span></td>
<td><span data-ttu-id="0540e-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-231">HR</span></span></td>
<td><span data-ttu-id="0540e-232">1,000</span><span class="sxs-lookup"><span data-stu-id="0540e-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-233">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-233">CC002</span></span></td>
<td><span data-ttu-id="0540e-234">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-234">Finance</span></span></td>
<td><span data-ttu-id="0540e-235">6,000</span><span class="sxs-lookup"><span data-stu-id="0540e-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-236">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-236">CC003</span></span></td>
<td><span data-ttu-id="0540e-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-237">Assembly</span></span></td>
<td><span data-ttu-id="0540e-238">0</span><span class="sxs-lookup"><span data-stu-id="0540e-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="0540e-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-240">Cost object</span></span></th>
<th><span data-ttu-id="0540e-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-241">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-242">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-244">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-244">CC001</span></span></td>
<td><span data-ttu-id="0540e-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-245">HR</span></span></td>
<td><span data-ttu-id="0540e-246">1,000</span><span class="sxs-lookup"><span data-stu-id="0540e-246">1,000</span></span></td>
<td><span data-ttu-id="0540e-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0540e-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="0540e-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-249">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-249">CC002</span></span></td>
<td><span data-ttu-id="0540e-250">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-250">Finance</span></span></td>
<td><span data-ttu-id="0540e-251">6,000</span><span class="sxs-lookup"><span data-stu-id="0540e-251">6,000</span></span></td>
<td><span data-ttu-id="0540e-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0540e-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="0540e-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-254">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-254">CC003</span></span></td>
<td><span data-ttu-id="0540e-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-255">Assembly</span></span></td>
<td><span data-ttu-id="0540e-256">0</span><span class="sxs-lookup"><span data-stu-id="0540e-256">0</span></span></td>
<td><span data-ttu-id="0540e-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0540e-258">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="0540e-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="0540e-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="0540e-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-261">Cost object</span></span></th>
<th><span data-ttu-id="0540e-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="0540e-262">Formula</span></span></th>
<th><span data-ttu-id="0540e-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-263">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-264">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-266">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-266">CC001</span></span></td>
<td><span data-ttu-id="0540e-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-267">HR</span></span></td>
<td><span data-ttu-id="0540e-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0540e-269">1</span><span class="sxs-lookup"><span data-stu-id="0540e-269">1</span></span></td>
<td><span data-ttu-id="0540e-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0540e-271">500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-272">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-272">CC002</span></span></td>
<td><span data-ttu-id="0540e-273">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-273">Finance</span></span></td>
<td><span data-ttu-id="0540e-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0540e-275">1</span><span class="sxs-lookup"><span data-stu-id="0540e-275">1</span></span></td>
<td><span data-ttu-id="0540e-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0540e-277">500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-278">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-278">CC003</span></span></td>
<td><span data-ttu-id="0540e-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-279">Assembly</span></span></td>
<td><span data-ttu-id="0540e-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0540e-281">0</span><span class="sxs-lookup"><span data-stu-id="0540e-281">0</span></span></td>
<td><span data-ttu-id="0540e-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0540e-283">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="0540e-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-285">Journal</span></span></th>
<th><span data-ttu-id="0540e-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="0540e-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0540e-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="0540e-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0540e-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="0540e-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-289">00002</span><span class="sxs-lookup"><span data-stu-id="0540e-289">00002</span></span></td>
<td><span data-ttu-id="0540e-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="0540e-291">مالي</span><span class="sxs-lookup"><span data-stu-id="0540e-291">Fiscal</span></span></td>
<td><span data-ttu-id="0540e-292">2017</span><span class="sxs-lookup"><span data-stu-id="0540e-292">2017</span></span></td>
<td><span data-ttu-id="0540e-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-293">Period 1</span></span></td>
<td><span data-ttu-id="0540e-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0540e-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="0540e-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-298">Cost element</span></span></th>
<th><span data-ttu-id="0540e-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-299">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-302">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-302">CC099</span></span></td>
<td><span data-ttu-id="0540e-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-303">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-304">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-304">10001</span></span></td>
<td><span data-ttu-id="0540e-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-305">Electricity</span></span></td>
<td><span data-ttu-id="0540e-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-306">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-309">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-309">CC099</span></span></td>
<td><span data-ttu-id="0540e-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-310">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-311">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-311">10001</span></span></td>
<td><span data-ttu-id="0540e-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-312">Electricity</span></span></td>
<td><span data-ttu-id="0540e-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-313">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0540e-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-317">Cost element</span></span></th>
<th><span data-ttu-id="0540e-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-318">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-319">Amount</span></span></th>
<th><span data-ttu-id="0540e-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-321">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-321">CC099</span></span></td>
<td><span data-ttu-id="0540e-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-322">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-323">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-323">10001</span></span></td>
<td><span data-ttu-id="0540e-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-324">Electricity</span></span></td>
<td><span data-ttu-id="0540e-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-325">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-326">-1,000.00</span></span></td>
<td><span data-ttu-id="0540e-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-328">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-328">CC001</span></span></td>
<td><span data-ttu-id="0540e-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-329">HR</span></span></td>
<td><span data-ttu-id="0540e-330">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-330">10001</span></span></td>
<td><span data-ttu-id="0540e-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-331">Electricity</span></span></td>
<td><span data-ttu-id="0540e-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-332">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-333">500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-333">500.00</span></span></td>
<td><span data-ttu-id="0540e-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-335">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-335">CC002</span></span></td>
<td><span data-ttu-id="0540e-336">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-336">Finance</span></span></td>
<td><span data-ttu-id="0540e-337">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-337">10001</span></span></td>
<td><span data-ttu-id="0540e-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-338">Electricity</span></span></td>
<td><span data-ttu-id="0540e-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-339">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-340">500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-340">500.00</span></span></td>
<td><span data-ttu-id="0540e-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-342">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-342">CC099</span></span></td>
<td><span data-ttu-id="0540e-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="0540e-343">Default cost center</span></span></td>
<td><span data-ttu-id="0540e-344">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-344">10001</span></span></td>
<td><span data-ttu-id="0540e-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-345">Electricity</span></span></td>
<td><span data-ttu-id="0540e-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-346">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="0540e-347">-9,000.00</span></span></td>
<td><span data-ttu-id="0540e-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-349">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-349">CC001</span></span></td>
<td><span data-ttu-id="0540e-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-350">HR</span></span></td>
<td><span data-ttu-id="0540e-351">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-351">10001</span></span></td>
<td><span data-ttu-id="0540e-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-352">Electricity</span></span></td>
<td><span data-ttu-id="0540e-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-353">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="0540e-354">1,285.71</span></span></td>
<td><span data-ttu-id="0540e-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-356">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-356">CC002</span></span></td>
<td><span data-ttu-id="0540e-357">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-357">Finance</span></span></td>
<td><span data-ttu-id="0540e-358">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-358">10001</span></span></td>
<td><span data-ttu-id="0540e-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-359">Electricity</span></span></td>
<td><span data-ttu-id="0540e-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-360">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="0540e-361">7,714.29</span></span></td>
<td><span data-ttu-id="0540e-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="0540e-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="0540e-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="0540e-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="0540e-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="0540e-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="0540e-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="0540e-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="0540e-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="0540e-367">Define the overhead rate</span></span>

<span data-ttu-id="0540e-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="0540e-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="0540e-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="0540e-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-370">Cost object</span></span></th>
<th><span data-ttu-id="0540e-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="0540e-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-372">Proj 1</span></span></td>
<td><span data-ttu-id="0540e-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-373">Project 1</span></span></td>
<td><span data-ttu-id="0540e-374">3</span><span class="sxs-lookup"><span data-stu-id="0540e-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-375">Proj 2</span></span></td>
<td><span data-ttu-id="0540e-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-376">Project 2</span></span></td>
<td><span data-ttu-id="0540e-377">1</span><span class="sxs-lookup"><span data-stu-id="0540e-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-379">Cost object</span></span></th>
<th><span data-ttu-id="0540e-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-380">Cost element</span></span></th>
<th><span data-ttu-id="0540e-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-381">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="0540e-382">Units</span></span></th>
<th><span data-ttu-id="0540e-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="0540e-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-384">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-384">CC001</span></span></td>
<td><span data-ttu-id="0540e-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-385">HR</span></span></td>
<td><span data-ttu-id="0540e-386">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-386">10001</span></span></td>
<td><span data-ttu-id="0540e-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-387">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-388">1</span><span class="sxs-lookup"><span data-stu-id="0540e-388">1</span></span></td>
<td><span data-ttu-id="0540e-389">10</span><span class="sxs-lookup"><span data-stu-id="0540e-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="0540e-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-391">Cost object</span></span></th>
<th><span data-ttu-id="0540e-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-392">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-393">Cost element</span></span></th>
<th><span data-ttu-id="0540e-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-394">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-396">Proj 1</span></span></td>
<td><span data-ttu-id="0540e-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-397">Project 1</span></span></td>
<td><span data-ttu-id="0540e-398">3</span><span class="sxs-lookup"><span data-stu-id="0540e-398">3</span></span></td>
<td><span data-ttu-id="0540e-399">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-399">10001</span></span></td>
<td><span data-ttu-id="0540e-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="0540e-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="0540e-401">30.00</span><span class="sxs-lookup"><span data-stu-id="0540e-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-402">Proj 2</span></span></td>
<td><span data-ttu-id="0540e-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-403">Project 2</span></span></td>
<td><span data-ttu-id="0540e-404">1</span><span class="sxs-lookup"><span data-stu-id="0540e-404">1</span></span></td>
<td><span data-ttu-id="0540e-405">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-405">10001</span></span></td>
<td><span data-ttu-id="0540e-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="0540e-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="0540e-407">10.00</span><span class="sxs-lookup"><span data-stu-id="0540e-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="0540e-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-409">Journal</span></span></th>
<th><span data-ttu-id="0540e-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="0540e-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0540e-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="0540e-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0540e-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="0540e-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-413">00003</span><span class="sxs-lookup"><span data-stu-id="0540e-413">00003</span></span></td>
<td><span data-ttu-id="0540e-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="0540e-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="0540e-415">مالي</span><span class="sxs-lookup"><span data-stu-id="0540e-415">Fiscal</span></span></td>
<td><span data-ttu-id="0540e-416">2017</span><span class="sxs-lookup"><span data-stu-id="0540e-416">2017</span></span></td>
<td><span data-ttu-id="0540e-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-417">Period 1</span></span></td>
<td><span data-ttu-id="0540e-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="0540e-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="0540e-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-421">Cost object</span></span></th>
<th><span data-ttu-id="0540e-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-424">Proj 1</span></span></td>
<td><span data-ttu-id="0540e-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="0540e-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="0540e-426">3.00</span><span class="sxs-lookup"><span data-stu-id="0540e-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-428">Proj 2</span></span></td>
<td><span data-ttu-id="0540e-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="0540e-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="0540e-430">1.00</span><span class="sxs-lookup"><span data-stu-id="0540e-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0540e-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-433">Cost element</span></span></th>
<th><span data-ttu-id="0540e-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-434">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-435">Amount</span></span></th>
<th><span data-ttu-id="0540e-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="0540e-437">CC0001</span></span></td>
<td><span data-ttu-id="0540e-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-438">HR</span></span></td>
<td><span data-ttu-id="0540e-439">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-439">10001</span></span></td>
<td><span data-ttu-id="0540e-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-440">Electricity</span></span></td>
<td><span data-ttu-id="0540e-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-441">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="0540e-442">-30.00</span></span></td>
<td><span data-ttu-id="0540e-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-444">Proj 1</span></span></td>
<td><span data-ttu-id="0540e-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="0540e-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="0540e-446">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-446">10001</span></span></td>
<td><span data-ttu-id="0540e-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-447">Electricity</span></span></td>
<td><span data-ttu-id="0540e-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-448">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-449">30.00</span><span class="sxs-lookup"><span data-stu-id="0540e-449">30.00</span></span></td>
<td><span data-ttu-id="0540e-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-451">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-451">CC001</span></span></td>
<td><span data-ttu-id="0540e-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-452">HR</span></span></td>
<td><span data-ttu-id="0540e-453">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-453">10001</span></span></td>
<td><span data-ttu-id="0540e-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-454">Electricity</span></span></td>
<td><span data-ttu-id="0540e-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-455">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="0540e-456">-10.00</span></span></td>
<td><span data-ttu-id="0540e-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-458">Proj 2</span></span></td>
<td><span data-ttu-id="0540e-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="0540e-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="0540e-460">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-460">10001</span></span></td>
<td><span data-ttu-id="0540e-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-461">Electricity</span></span></td>
<td><span data-ttu-id="0540e-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-462">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-463">10.00</span><span class="sxs-lookup"><span data-stu-id="0540e-463">10.00</span></span></td>
<td><span data-ttu-id="0540e-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="0540e-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="0540e-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="0540e-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="0540e-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="0540e-468">يدعم تطبيق Finance and Operations طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="0540e-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="0540e-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="0540e-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="0540e-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="0540e-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="0540e-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="0540e-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="0540e-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="0540e-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="0540e-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="0540e-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="0540e-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="0540e-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-475">Define the cost allocation</span></span>

<span data-ttu-id="0540e-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="0540e-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="0540e-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="0540e-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-479">Cost object</span></span></th>
<th><span data-ttu-id="0540e-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-481">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-481">CC002</span></span></td>
<td><span data-ttu-id="0540e-482">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-482">Finance</span></span></td>
<td><span data-ttu-id="0540e-483">35</span><span class="sxs-lookup"><span data-stu-id="0540e-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-484">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-484">CC003</span></span></td>
<td><span data-ttu-id="0540e-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-485">Assembly</span></span></td>
<td><span data-ttu-id="0540e-486">55</span><span class="sxs-lookup"><span data-stu-id="0540e-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-487">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-487">CC004</span></span></td>
<td><span data-ttu-id="0540e-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-488">Packaging</span></span></td>
<td><span data-ttu-id="0540e-489">10</span><span class="sxs-lookup"><span data-stu-id="0540e-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="0540e-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="0540e-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-492">Cost object</span></span></th>
<th><span data-ttu-id="0540e-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-494">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-494">CC003</span></span></td>
<td><span data-ttu-id="0540e-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-495">Assembly</span></span></td>
<td><span data-ttu-id="0540e-496">65</span><span class="sxs-lookup"><span data-stu-id="0540e-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-497">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-497">CC004</span></span></td>
<td><span data-ttu-id="0540e-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-498">Packaging</span></span></td>
<td><span data-ttu-id="0540e-499">35</span><span class="sxs-lookup"><span data-stu-id="0540e-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="0540e-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="0540e-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-502">Cost object</span></span></th>
<th><span data-ttu-id="0540e-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="0540e-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-504">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-505">Product 1</span></span></td>
<td><span data-ttu-id="0540e-506">60</span><span class="sxs-lookup"><span data-stu-id="0540e-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-507">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-508">Product 2</span></span></td>
<td><span data-ttu-id="0540e-509">20</span><span class="sxs-lookup"><span data-stu-id="0540e-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="0540e-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="0540e-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-512">Cost object</span></span></th>
<th><span data-ttu-id="0540e-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="0540e-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-514">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-515">Product 1</span></span></td>
<td><span data-ttu-id="0540e-516">80</span><span class="sxs-lookup"><span data-stu-id="0540e-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-517">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-518">Product 2</span></span></td>
<td><span data-ttu-id="0540e-519">15</span><span class="sxs-lookup"><span data-stu-id="0540e-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0540e-520">في Finance and Operations، بإمكان القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج أن تشتق من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="0540e-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="0540e-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="0540e-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="0540e-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="0540e-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-523">Cost object</span></span></th>
<th><span data-ttu-id="0540e-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-524">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-525">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-526">Amount</span></span></th>
<th><span data-ttu-id="0540e-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-528">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-528">CC002</span></span></td>
<td><span data-ttu-id="0540e-529">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-529">Finance</span></span></td>
<td><span data-ttu-id="0540e-530">35</span><span class="sxs-lookup"><span data-stu-id="0540e-530">35</span></span></td>
<td><span data-ttu-id="0540e-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0540e-532">175.00</span><span class="sxs-lookup"><span data-stu-id="0540e-532">175.00</span></span></td>
<td><span data-ttu-id="0540e-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-534">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-534">CC003</span></span></td>
<td><span data-ttu-id="0540e-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-535">Assembly</span></span></td>
<td><span data-ttu-id="0540e-536">55</span><span class="sxs-lookup"><span data-stu-id="0540e-536">55</span></span></td>
<td><span data-ttu-id="0540e-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0540e-538">275.00</span><span class="sxs-lookup"><span data-stu-id="0540e-538">275.00</span></span></td>
<td><span data-ttu-id="0540e-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-540">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-540">CC004</span></span></td>
<td><span data-ttu-id="0540e-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-541">Packaging</span></span></td>
<td><span data-ttu-id="0540e-542">10</span><span class="sxs-lookup"><span data-stu-id="0540e-542">10</span></span></td>
<td><span data-ttu-id="0540e-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0540e-544">50.00</span><span class="sxs-lookup"><span data-stu-id="0540e-544">50.00</span></span></td>
<td><span data-ttu-id="0540e-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-546">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-546">CC002</span></span></td>
<td><span data-ttu-id="0540e-547">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-547">Finance</span></span></td>
<td><span data-ttu-id="0540e-548">35</span><span class="sxs-lookup"><span data-stu-id="0540e-548">35</span></span></td>
<td><span data-ttu-id="0540e-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="0540e-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0540e-550">436.00</span><span class="sxs-lookup"><span data-stu-id="0540e-550">436.00</span></span></td>
<td><span data-ttu-id="0540e-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-552">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-552">CC003</span></span></td>
<td><span data-ttu-id="0540e-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-553">Assembly</span></span></td>
<td><span data-ttu-id="0540e-554">55</span><span class="sxs-lookup"><span data-stu-id="0540e-554">55</span></span></td>
<td><span data-ttu-id="0540e-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="0540e-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0540e-556">685.14</span><span class="sxs-lookup"><span data-stu-id="0540e-556">685.14</span></span></td>
<td><span data-ttu-id="0540e-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-558">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-558">CC004</span></span></td>
<td><span data-ttu-id="0540e-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-559">Packaging</span></span></td>
<td><span data-ttu-id="0540e-560">10</span><span class="sxs-lookup"><span data-stu-id="0540e-560">10</span></span></td>
<td><span data-ttu-id="0540e-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="0540e-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0540e-562">124.57</span><span class="sxs-lookup"><span data-stu-id="0540e-562">124.57</span></span></td>
<td><span data-ttu-id="0540e-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="0540e-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-565">Cost object</span></span></th>
<th><span data-ttu-id="0540e-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-566">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-567">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-568">Amount</span></span></th>
<th><span data-ttu-id="0540e-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-570">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-570">CC003</span></span></td>
<td><span data-ttu-id="0540e-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-571">Assembly</span></span></td>
<td><span data-ttu-id="0540e-572">65</span><span class="sxs-lookup"><span data-stu-id="0540e-572">65</span></span></td>
<td><span data-ttu-id="0540e-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="0540e-574">438.75</span><span class="sxs-lookup"><span data-stu-id="0540e-574">438.75</span></span></td>
<td><span data-ttu-id="0540e-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-576">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-576">CC004</span></span></td>
<td><span data-ttu-id="0540e-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-577">Packaging</span></span></td>
<td><span data-ttu-id="0540e-578">35</span><span class="sxs-lookup"><span data-stu-id="0540e-578">35</span></span></td>
<td><span data-ttu-id="0540e-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="0540e-580">236.25</span><span class="sxs-lookup"><span data-stu-id="0540e-580">236.25</span></span></td>
<td><span data-ttu-id="0540e-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-582">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-582">CC003</span></span></td>
<td><span data-ttu-id="0540e-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-583">Assembly</span></span></td>
<td><span data-ttu-id="0540e-584">65</span><span class="sxs-lookup"><span data-stu-id="0540e-584">65</span></span></td>
<td><span data-ttu-id="0540e-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="0540e-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="0540e-586">5,297.69</span></span></td>
<td><span data-ttu-id="0540e-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-588">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-588">CC004</span></span></td>
<td><span data-ttu-id="0540e-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-589">Packaging</span></span></td>
<td><span data-ttu-id="0540e-590">35</span><span class="sxs-lookup"><span data-stu-id="0540e-590">35</span></span></td>
<td><span data-ttu-id="0540e-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="0540e-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="0540e-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="0540e-592">2,852.60</span></span></td>
<td><span data-ttu-id="0540e-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="0540e-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-595">Cost object</span></span></th>
<th><span data-ttu-id="0540e-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-596">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-597">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-598">Amount</span></span></th>
<th><span data-ttu-id="0540e-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-600">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-601">Product 1</span></span></td>
<td><span data-ttu-id="0540e-602">60</span><span class="sxs-lookup"><span data-stu-id="0540e-602">60</span></span></td>
<td><span data-ttu-id="0540e-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="0540e-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="0540e-604">535.31</span><span class="sxs-lookup"><span data-stu-id="0540e-604">535.31</span></span></td>
<td><span data-ttu-id="0540e-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-606">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-607">Product 2</span></span></td>
<td><span data-ttu-id="0540e-608">20</span><span class="sxs-lookup"><span data-stu-id="0540e-608">20</span></span></td>
<td><span data-ttu-id="0540e-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="0540e-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="0540e-610">178.44</span><span class="sxs-lookup"><span data-stu-id="0540e-610">178.44</span></span></td>
<td><span data-ttu-id="0540e-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-612">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-613">Product 1</span></span></td>
<td><span data-ttu-id="0540e-614">60</span><span class="sxs-lookup"><span data-stu-id="0540e-614">60</span></span></td>
<td><span data-ttu-id="0540e-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="0540e-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="0540e-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="0540e-616">4,487.12</span></span></td>
<td><span data-ttu-id="0540e-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-618">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-619">Product 2</span></span></td>
<td><span data-ttu-id="0540e-620">20</span><span class="sxs-lookup"><span data-stu-id="0540e-620">20</span></span></td>
<td><span data-ttu-id="0540e-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="0540e-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="0540e-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="0540e-622">1,495.71</span></span></td>
<td><span data-ttu-id="0540e-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0540e-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="0540e-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-625">Cost object</span></span></th>
<th><span data-ttu-id="0540e-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="0540e-626">Magnitude</span></span></th>
<th><span data-ttu-id="0540e-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="0540e-627">Allocation factor</span></span></th>
<th><span data-ttu-id="0540e-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-628">Amount</span></span></th>
<th><span data-ttu-id="0540e-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-630">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-631">Product 1</span></span></td>
<td><span data-ttu-id="0540e-632">80</span><span class="sxs-lookup"><span data-stu-id="0540e-632">80</span></span></td>
<td><span data-ttu-id="0540e-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="0540e-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="0540e-634">241.05</span><span class="sxs-lookup"><span data-stu-id="0540e-634">241.05</span></span></td>
<td><span data-ttu-id="0540e-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-636">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-637">Product 2</span></span></td>
<td><span data-ttu-id="0540e-638">15</span><span class="sxs-lookup"><span data-stu-id="0540e-638">15</span></span></td>
<td><span data-ttu-id="0540e-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="0540e-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="0540e-640">45.20</span><span class="sxs-lookup"><span data-stu-id="0540e-640">45.20</span></span></td>
<td><span data-ttu-id="0540e-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-642">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-643">Product 1</span></span></td>
<td><span data-ttu-id="0540e-644">80</span><span class="sxs-lookup"><span data-stu-id="0540e-644">80</span></span></td>
<td><span data-ttu-id="0540e-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="0540e-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="0540e-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="0540e-646">2,507.09</span></span></td>
<td><span data-ttu-id="0540e-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-648">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-649">Product 2</span></span></td>
<td><span data-ttu-id="0540e-650">15</span><span class="sxs-lookup"><span data-stu-id="0540e-650">15</span></span></td>
<td><span data-ttu-id="0540e-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="0540e-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="0540e-652">470.08</span><span class="sxs-lookup"><span data-stu-id="0540e-652">470.08</span></span></td>
<td><span data-ttu-id="0540e-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0540e-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="0540e-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="0540e-655">Journal</span></span></th>
<th><span data-ttu-id="0540e-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="0540e-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0540e-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="0540e-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0540e-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="0540e-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-659">00004</span><span class="sxs-lookup"><span data-stu-id="0540e-659">00004</span></span></td>
<td><span data-ttu-id="0540e-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="0540e-661">مالي</span><span class="sxs-lookup"><span data-stu-id="0540e-661">Fiscal</span></span></td>
<td><span data-ttu-id="0540e-662">2017</span><span class="sxs-lookup"><span data-stu-id="0540e-662">2017</span></span></td>
<td><span data-ttu-id="0540e-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-663">Period 1</span></span></td>
<td><span data-ttu-id="0540e-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="0540e-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="0540e-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="0540e-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0540e-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-668">Cost element</span></span></th>
<th><span data-ttu-id="0540e-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-669">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-672">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-672">CC001</span></span></td>
<td><span data-ttu-id="0540e-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-673">HR</span></span></td>
<td><span data-ttu-id="0540e-674">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-674">10001</span></span></td>
<td><span data-ttu-id="0540e-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-675">Electricity</span></span></td>
<td><span data-ttu-id="0540e-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-676">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-677">500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-679">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-679">CC001</span></span></td>
<td><span data-ttu-id="0540e-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-680">HR</span></span></td>
<td><span data-ttu-id="0540e-681">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-681">10001</span></span></td>
<td><span data-ttu-id="0540e-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-682">Electricity</span></span></td>
<td><span data-ttu-id="0540e-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-683">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="0540e-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-686">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-686">CC002</span></span></td>
<td><span data-ttu-id="0540e-687">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-687">Finance</span></span></td>
<td><span data-ttu-id="0540e-688">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-688">10001</span></span></td>
<td><span data-ttu-id="0540e-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-689">Electricity</span></span></td>
<td><span data-ttu-id="0540e-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-690">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-691">675.00</span><span class="sxs-lookup"><span data-stu-id="0540e-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-693">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-693">CC002</span></span></td>
<td><span data-ttu-id="0540e-694">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-694">Finance</span></span></td>
<td><span data-ttu-id="0540e-695">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-695">10001</span></span></td>
<td><span data-ttu-id="0540e-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-696">Electricity</span></span></td>
<td><span data-ttu-id="0540e-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-697">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="0540e-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-700">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-700">CC003</span></span></td>
<td><span data-ttu-id="0540e-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-701">Assembly</span></span></td>
<td><span data-ttu-id="0540e-702">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-702">10001</span></span></td>
<td><span data-ttu-id="0540e-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-703">Electricity</span></span></td>
<td><span data-ttu-id="0540e-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-704">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-705">713.75</span><span class="sxs-lookup"><span data-stu-id="0540e-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-707">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-707">CC003</span></span></td>
<td><span data-ttu-id="0540e-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-708">Assembly</span></span></td>
<td><span data-ttu-id="0540e-709">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-709">10001</span></span></td>
<td><span data-ttu-id="0540e-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-710">Electricity</span></span></td>
<td><span data-ttu-id="0540e-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-711">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="0540e-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-714">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-714">CC003</span></span></td>
<td><span data-ttu-id="0540e-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-715">Packaging</span></span></td>
<td><span data-ttu-id="0540e-716">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-716">10001</span></span></td>
<td><span data-ttu-id="0540e-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-717">Electricity</span></span></td>
<td><span data-ttu-id="0540e-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-718">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-719">286.25</span><span class="sxs-lookup"><span data-stu-id="0540e-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-721">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-721">CC003</span></span></td>
<td><span data-ttu-id="0540e-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-722">Packaging</span></span></td>
<td><span data-ttu-id="0540e-723">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-723">10001</span></span></td>
<td><span data-ttu-id="0540e-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-724">Electricity</span></span></td>
<td><span data-ttu-id="0540e-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-725">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="0540e-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-728">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-729">Product 1</span></span></td>
<td><span data-ttu-id="0540e-730">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-730">10001</span></span></td>
<td><span data-ttu-id="0540e-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-731">Electricity</span></span></td>
<td><span data-ttu-id="0540e-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-732">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-733">776.36</span><span class="sxs-lookup"><span data-stu-id="0540e-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-735">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-736">Product 1</span></span></td>
<td><span data-ttu-id="0540e-737">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-737">10001</span></span></td>
<td><span data-ttu-id="0540e-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-738">Electricity</span></span></td>
<td><span data-ttu-id="0540e-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-739">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="0540e-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-742">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-743">Product 1</span></span></td>
<td><span data-ttu-id="0540e-744">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-744">10001</span></span></td>
<td><span data-ttu-id="0540e-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-745">Electricity</span></span></td>
<td><span data-ttu-id="0540e-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-746">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-747">223.64</span><span class="sxs-lookup"><span data-stu-id="0540e-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="0540e-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-749">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-750">Product 1</span></span></td>
<td><span data-ttu-id="0540e-751">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-751">10001</span></span></td>
<td><span data-ttu-id="0540e-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-752">Electricity</span></span></td>
<td><span data-ttu-id="0540e-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-753">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="0540e-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0540e-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0540e-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0540e-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-757">Cost element</span></span></th>
<th><span data-ttu-id="0540e-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-758">Cost behavior</span></span></th>
<th><span data-ttu-id="0540e-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="0540e-759">Amount</span></span></th>
<th><span data-ttu-id="0540e-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="0540e-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0540e-761">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-761">CC001</span></span></td>
<td><span data-ttu-id="0540e-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-762">HR</span></span></td>
<td><span data-ttu-id="0540e-763">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-763">10001</span></span></td>
<td><span data-ttu-id="0540e-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-764">Electricity</span></span></td>
<td><span data-ttu-id="0540e-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-765">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="0540e-766">-500.00</span></span></td>
<td><span data-ttu-id="0540e-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-768">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-768">CC002</span></span></td>
<td><span data-ttu-id="0540e-769">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-769">Finance</span></span></td>
<td><span data-ttu-id="0540e-770">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-770">10001</span></span></td>
<td><span data-ttu-id="0540e-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-771">Electricity</span></span></td>
<td><span data-ttu-id="0540e-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-772">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-773">175.00</span><span class="sxs-lookup"><span data-stu-id="0540e-773">175.00</span></span></td>
<td><span data-ttu-id="0540e-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-775">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-775">CC003</span></span></td>
<td><span data-ttu-id="0540e-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-776">Assembly</span></span></td>
<td><span data-ttu-id="0540e-777">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-777">10001</span></span></td>
<td><span data-ttu-id="0540e-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-778">Electricity</span></span></td>
<td><span data-ttu-id="0540e-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-779">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-780">275.00</span><span class="sxs-lookup"><span data-stu-id="0540e-780">275.00</span></span></td>
<td><span data-ttu-id="0540e-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-782">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-782">CC004</span></span></td>
<td><span data-ttu-id="0540e-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-783">Packaging</span></span></td>
<td><span data-ttu-id="0540e-784">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-784">10001</span></span></td>
<td><span data-ttu-id="0540e-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-785">Electricity</span></span></td>
<td><span data-ttu-id="0540e-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-786">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-787">50,00</span><span class="sxs-lookup"><span data-stu-id="0540e-787">50,00</span></span></td>
<td><span data-ttu-id="0540e-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-789">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-789">CC001</span></span></td>
<td><span data-ttu-id="0540e-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="0540e-790">HR</span></span></td>
<td><span data-ttu-id="0540e-791">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-791">10001</span></span></td>
<td><span data-ttu-id="0540e-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-792">Electricity</span></span></td>
<td><span data-ttu-id="0540e-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-793">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="0540e-794">-1,245.71</span></span></td>
<td><span data-ttu-id="0540e-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-796">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-796">CC002</span></span></td>
<td><span data-ttu-id="0540e-797">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-797">Finance</span></span></td>
<td><span data-ttu-id="0540e-798">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-798">10001</span></span></td>
<td><span data-ttu-id="0540e-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-799">Electricity</span></span></td>
<td><span data-ttu-id="0540e-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-800">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-801">436.00</span><span class="sxs-lookup"><span data-stu-id="0540e-801">436.00</span></span></td>
<td><span data-ttu-id="0540e-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-803">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-803">CC003</span></span></td>
<td><span data-ttu-id="0540e-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-804">Assembly</span></span></td>
<td><span data-ttu-id="0540e-805">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-805">10001</span></span></td>
<td><span data-ttu-id="0540e-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-806">Electricity</span></span></td>
<td><span data-ttu-id="0540e-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-807">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-808">685.14</span><span class="sxs-lookup"><span data-stu-id="0540e-808">685.14</span></span></td>
<td><span data-ttu-id="0540e-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-810">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-810">CC004</span></span></td>
<td><span data-ttu-id="0540e-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-811">Packaging</span></span></td>
<td><span data-ttu-id="0540e-812">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-812">10001</span></span></td>
<td><span data-ttu-id="0540e-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-813">Electricity</span></span></td>
<td><span data-ttu-id="0540e-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-814">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-815">124.57</span><span class="sxs-lookup"><span data-stu-id="0540e-815">124.57</span></span></td>
<td><span data-ttu-id="0540e-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-817">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-817">CC002</span></span></td>
<td><span data-ttu-id="0540e-818">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-818">Finance</span></span></td>
<td><span data-ttu-id="0540e-819">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-819">10001</span></span></td>
<td><span data-ttu-id="0540e-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-820">Electricity</span></span></td>
<td><span data-ttu-id="0540e-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-821">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="0540e-822">-675.00</span></span></td>
<td><span data-ttu-id="0540e-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-824">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-824">CC003</span></span></td>
<td><span data-ttu-id="0540e-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-825">Assembly</span></span></td>
<td><span data-ttu-id="0540e-826">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-826">10001</span></span></td>
<td><span data-ttu-id="0540e-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-827">Electricity</span></span></td>
<td><span data-ttu-id="0540e-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-828">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-829">438.75</span><span class="sxs-lookup"><span data-stu-id="0540e-829">438.75</span></span></td>
<td><span data-ttu-id="0540e-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-831">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-831">CC004</span></span></td>
<td><span data-ttu-id="0540e-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-832">Packaging</span></span></td>
<td><span data-ttu-id="0540e-833">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-833">10001</span></span></td>
<td><span data-ttu-id="0540e-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-834">Electricity</span></span></td>
<td><span data-ttu-id="0540e-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-835">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-836">236.25</span><span class="sxs-lookup"><span data-stu-id="0540e-836">236.25</span></span></td>
<td><span data-ttu-id="0540e-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-838">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-838">CC002</span></span></td>
<td><span data-ttu-id="0540e-839">المالية</span><span class="sxs-lookup"><span data-stu-id="0540e-839">Finance</span></span></td>
<td><span data-ttu-id="0540e-840">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-840">10001</span></span></td>
<td><span data-ttu-id="0540e-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-841">Electricity</span></span></td>
<td><span data-ttu-id="0540e-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-842">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="0540e-843">-8,150.29</span></span></td>
<td><span data-ttu-id="0540e-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-845">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-845">CC003</span></span></td>
<td><span data-ttu-id="0540e-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-846">Assembly</span></span></td>
<td><span data-ttu-id="0540e-847">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-847">10001</span></span></td>
<td><span data-ttu-id="0540e-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-848">Electricity</span></span></td>
<td><span data-ttu-id="0540e-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-849">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="0540e-850">5,297.69</span></span></td>
<td><span data-ttu-id="0540e-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-852">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-852">CC004</span></span></td>
<td><span data-ttu-id="0540e-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="0540e-853">Packaging</span></span></td>
<td><span data-ttu-id="0540e-854">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-854">10001</span></span></td>
<td><span data-ttu-id="0540e-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-855">Electricity</span></span></td>
<td><span data-ttu-id="0540e-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-856">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="0540e-857">2,852.60</span></span></td>
<td><span data-ttu-id="0540e-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-859">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-859">CC003</span></span></td>
<td><span data-ttu-id="0540e-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-860">Assembly</span></span></td>
<td><span data-ttu-id="0540e-861">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-861">10001</span></span></td>
<td><span data-ttu-id="0540e-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-862">Electricity</span></span></td>
<td><span data-ttu-id="0540e-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-863">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="0540e-864">-713.75</span></span></td>
<td><span data-ttu-id="0540e-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-866">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-867">Product 1</span></span></td>
<td><span data-ttu-id="0540e-868">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-868">10001</span></span></td>
<td><span data-ttu-id="0540e-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-869">Electricity</span></span></td>
<td><span data-ttu-id="0540e-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-870">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-871">535.31</span><span class="sxs-lookup"><span data-stu-id="0540e-871">535.31</span></span></td>
<td><span data-ttu-id="0540e-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-873">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-874">Product 2</span></span></td>
<td><span data-ttu-id="0540e-875">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-875">10001</span></span></td>
<td><span data-ttu-id="0540e-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-876">Electricity</span></span></td>
<td><span data-ttu-id="0540e-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-877">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-878">178.44</span><span class="sxs-lookup"><span data-stu-id="0540e-878">178.44</span></span></td>
<td><span data-ttu-id="0540e-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-880">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-880">CC003</span></span></td>
<td><span data-ttu-id="0540e-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-881">Assembly</span></span></td>
<td><span data-ttu-id="0540e-882">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-882">10001</span></span></td>
<td><span data-ttu-id="0540e-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-883">Electricity</span></span></td>
<td><span data-ttu-id="0540e-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-884">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="0540e-885">-5,982.83</span></span></td>
<td><span data-ttu-id="0540e-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-887">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-888">Product 1</span></span></td>
<td><span data-ttu-id="0540e-889">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-889">10001</span></span></td>
<td><span data-ttu-id="0540e-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-890">Electricity</span></span></td>
<td><span data-ttu-id="0540e-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-891">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="0540e-892">4,487.12</span></span></td>
<td><span data-ttu-id="0540e-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-894">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-895">Product 2</span></span></td>
<td><span data-ttu-id="0540e-896">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-896">10001</span></span></td>
<td><span data-ttu-id="0540e-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-897">Electricity</span></span></td>
<td><span data-ttu-id="0540e-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-898">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="0540e-899">1,495.71</span></span></td>
<td><span data-ttu-id="0540e-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-901">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-901">CC003</span></span></td>
<td><span data-ttu-id="0540e-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-902">Assembly</span></span></td>
<td><span data-ttu-id="0540e-903">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-903">10001</span></span></td>
<td><span data-ttu-id="0540e-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-904">Electricity</span></span></td>
<td><span data-ttu-id="0540e-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-905">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="0540e-906">-286.25</span></span></td>
<td><span data-ttu-id="0540e-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-908">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-909">Product 1</span></span></td>
<td><span data-ttu-id="0540e-910">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-910">10001</span></span></td>
<td><span data-ttu-id="0540e-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-911">Electricity</span></span></td>
<td><span data-ttu-id="0540e-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-912">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-913">241.05</span><span class="sxs-lookup"><span data-stu-id="0540e-913">241.05</span></span></td>
<td><span data-ttu-id="0540e-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-915">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-916">Product 2</span></span></td>
<td><span data-ttu-id="0540e-917">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-917">10001</span></span></td>
<td><span data-ttu-id="0540e-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-918">Electricity</span></span></td>
<td><span data-ttu-id="0540e-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-919">Fixed cost</span></span></td>
<td><span data-ttu-id="0540e-920">45.20</span><span class="sxs-lookup"><span data-stu-id="0540e-920">45.20</span></span></td>
<td><span data-ttu-id="0540e-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-922">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-922">CC003</span></span></td>
<td><span data-ttu-id="0540e-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="0540e-923">Assembly</span></span></td>
<td><span data-ttu-id="0540e-924">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-924">10001</span></span></td>
<td><span data-ttu-id="0540e-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-925">Electricity</span></span></td>
<td><span data-ttu-id="0540e-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-926">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="0540e-927">-2,977.17</span></span></td>
<td><span data-ttu-id="0540e-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-929">Prod 1</span></span></td>
<td><span data-ttu-id="0540e-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-930">Product 1</span></span></td>
<td><span data-ttu-id="0540e-931">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-931">10001</span></span></td>
<td><span data-ttu-id="0540e-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-932">Electricity</span></span></td>
<td><span data-ttu-id="0540e-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-933">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="0540e-934">2,507.09</span></span></td>
<td><span data-ttu-id="0540e-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0540e-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-936">Prod 2</span></span></td>
<td><span data-ttu-id="0540e-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-937">Product 2</span></span></td>
<td><span data-ttu-id="0540e-938">10001</span><span class="sxs-lookup"><span data-stu-id="0540e-938">10001</span></span></td>
<td><span data-ttu-id="0540e-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-939">Electricity</span></span></td>
<td><span data-ttu-id="0540e-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-940">Variable cost</span></span></td>
<td><span data-ttu-id="0540e-941">470.08</span><span class="sxs-lookup"><span data-stu-id="0540e-941">470.08</span></span></td>
<td><span data-ttu-id="0540e-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="0540e-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="0540e-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="0540e-943">Conclusion</span></span>
<span data-ttu-id="0540e-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="0540e-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="0540e-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="0540e-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="0540e-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="0540e-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="0540e-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="0540e-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="0540e-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="0540e-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="0540e-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="0540e-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0540e-951">CC099</span><span class="sxs-lookup"><span data-stu-id="0540e-951">CC099</span></span></th>
<th><span data-ttu-id="0540e-952">CC001</span><span class="sxs-lookup"><span data-stu-id="0540e-952">CC001</span></span></th>
<th><span data-ttu-id="0540e-953">CC002</span><span class="sxs-lookup"><span data-stu-id="0540e-953">CC002</span></span></th>
<th><span data-ttu-id="0540e-954">CC003</span><span class="sxs-lookup"><span data-stu-id="0540e-954">CC003</span></span></th>
<th><span data-ttu-id="0540e-955">CC004</span><span class="sxs-lookup"><span data-stu-id="0540e-955">CC004</span></span></th>
<th><span data-ttu-id="0540e-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="0540e-956">Proj 1</span></span></th>
<th><span data-ttu-id="0540e-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="0540e-957">Proj 2</span></span></th>
<th><span data-ttu-id="0540e-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="0540e-958">Prod 1</span></span></th>
<th><span data-ttu-id="0540e-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="0540e-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="0540e-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="0540e-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="0540e-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="0540e-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="0540e-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-971">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="0540e-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="0540e-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-973">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-974">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-975">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-976">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-977">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="0540e-978">776.36</span><span class="sxs-lookup"><span data-stu-id="0540e-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-979">223.64</span><span class="sxs-lookup"><span data-stu-id="0540e-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="0540e-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="0540e-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-982">000</span><span class="sxs-lookup"><span data-stu-id="0540e-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-983">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-984">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-985">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-986">0.00</span><span class="sxs-lookup"><span data-stu-id="0540e-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-987">30.00</span><span class="sxs-lookup"><span data-stu-id="0540e-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-988">10.00</span><span class="sxs-lookup"><span data-stu-id="0540e-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="0540e-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="0540e-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0540e-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="0540e-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0540e-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="0540e-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="0540e-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="0540e-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="0540e-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0540e-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="0540e-996">لمزيد من المعلومات، راجع [تجميع التكلفة](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="0540e-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



