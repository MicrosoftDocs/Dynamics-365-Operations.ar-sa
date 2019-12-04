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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770794"
---
# <a name="overhead-calculation"></a><span data-ttu-id="a1b10-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="a1b10-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1b10-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="a1b10-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a1b10-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="a1b10-105">Term definition</span></span>
---------------

<span data-ttu-id="a1b10-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a1b10-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="a1b10-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a1b10-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="a1b10-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a1b10-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="a1b10-109">Rent</span></span>
-   <span data-ttu-id="a1b10-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-110">Electricity</span></span>
-   <span data-ttu-id="a1b10-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="a1b10-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a1b10-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="a1b10-112">Overhead calculation overview</span></span>
<span data-ttu-id="a1b10-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="a1b10-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a1b10-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a1b10-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a1b10-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="a1b10-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a1b10-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="a1b10-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a1b10-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="a1b10-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a1b10-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-119">Version type</span></span>
-   <span data-ttu-id="a1b10-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="a1b10-120">Date and time</span></span>
-   <span data-ttu-id="a1b10-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="a1b10-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a1b10-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-122">Fiscal year</span></span>
-   <span data-ttu-id="a1b10-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-123">Fiscal period</span></span>

<span data-ttu-id="a1b10-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="a1b10-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a1b10-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a1b10-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a1b10-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="a1b10-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a1b10-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="a1b10-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a1b10-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="a1b10-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a1b10-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="a1b10-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a1b10-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a1b10-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a1b10-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="a1b10-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a1b10-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a1b10-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a1b10-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a1b10-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="a1b10-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a1b10-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="a1b10-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a1b10-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="a1b10-140">Main account</span></span></th>
<th><span data-ttu-id="a1b10-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="a1b10-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a1b10-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-143">CC099</span></span></td>
<td><span data-ttu-id="a1b10-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-144">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-145">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-145">10001</span></span></td>
<td><span data-ttu-id="a1b10-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-146">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a1b10-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a1b10-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a1b10-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a1b10-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="a1b10-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a1b10-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a1b10-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="a1b10-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a1b10-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="a1b10-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a1b10-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="a1b10-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a1b10-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="a1b10-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a1b10-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a1b10-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="a1b10-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a1b10-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="a1b10-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a1b10-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-160">Journal</span></span></th>
<th><span data-ttu-id="a1b10-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1b10-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1b10-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-164">00001</span><span class="sxs-lookup"><span data-stu-id="a1b10-164">00001</span></span></td>
<td><span data-ttu-id="a1b10-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a1b10-166">مالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-166">Fiscal</span></span></td>
<td><span data-ttu-id="a1b10-167">2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-167">2017</span></span></td>
<td><span data-ttu-id="a1b10-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-168">Period 1</span></span></td>
<td><span data-ttu-id="a1b10-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a1b10-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="a1b10-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-173">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a1b10-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-177">CC099</span></span></td>
<td><span data-ttu-id="a1b10-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-178">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-179">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-179">10001</span></span></td>
<td><span data-ttu-id="a1b10-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-180">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="a1b10-181">Unclassified</span></span></td>
<td><span data-ttu-id="a1b10-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1b10-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-185">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-187">Amount</span></span></th>
<th><span data-ttu-id="a1b10-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-189">CC099</span></span></td>
<td><span data-ttu-id="a1b10-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-190">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-191">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-191">10001</span></span></td>
<td><span data-ttu-id="a1b10-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-192">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="a1b10-193">Unclassified</span></span></td>
<td><span data-ttu-id="a1b10-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-194">10,000.00</span></span></td>
<td><span data-ttu-id="a1b10-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-196">CC099</span></span></td>
<td><span data-ttu-id="a1b10-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-197">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-198">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-198">10001</span></span></td>
<td><span data-ttu-id="a1b10-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-199">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="a1b10-200">Unclassified</span></span></td>
<td><span data-ttu-id="a1b10-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a1b10-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-203">CC099</span></span></td>
<td><span data-ttu-id="a1b10-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-204">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-205">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-205">10001</span></span></td>
<td><span data-ttu-id="a1b10-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-206">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-208">1,000.00</span></span></td>
<td><span data-ttu-id="a1b10-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-210">CC099</span></span></td>
<td><span data-ttu-id="a1b10-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-211">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-212">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-212">10001</span></span></td>
<td><span data-ttu-id="a1b10-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-213">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-214">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-215">9,000.00</span></span></td>
<td><span data-ttu-id="a1b10-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-217">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="a1b10-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a1b10-218">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a1b10-219">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a1b10-220">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="a1b10-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a1b10-221">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-221">Define the cost distribution rule</span></span>

<span data-ttu-id="a1b10-222">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a1b10-223">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="a1b10-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a1b10-224">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="a1b10-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a1b10-225">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="a1b10-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a1b10-226">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="a1b10-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a1b10-227">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="a1b10-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-228">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-228">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-229">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="a1b10-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-230">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-230">CC001</span></span></td>
<td><span data-ttu-id="a1b10-231">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-231">HR</span></span></td>
<td><span data-ttu-id="a1b10-232">1,000</span><span class="sxs-lookup"><span data-stu-id="a1b10-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-233">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-233">CC002</span></span></td>
<td><span data-ttu-id="a1b10-234">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-234">Finance</span></span></td>
<td><span data-ttu-id="a1b10-235">6,000</span><span class="sxs-lookup"><span data-stu-id="a1b10-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-236">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-236">CC003</span></span></td>
<td><span data-ttu-id="a1b10-237">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-237">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-238">0</span><span class="sxs-lookup"><span data-stu-id="a1b10-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-239">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-240">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-240">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-241">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-241">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-242">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-242">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-243">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-244">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-244">CC001</span></span></td>
<td><span data-ttu-id="a1b10-245">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-245">HR</span></span></td>
<td><span data-ttu-id="a1b10-246">1,000</span><span class="sxs-lookup"><span data-stu-id="a1b10-246">1,000</span></span></td>
<td><span data-ttu-id="a1b10-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a1b10-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-249">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-249">CC002</span></span></td>
<td><span data-ttu-id="a1b10-250">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-250">Finance</span></span></td>
<td><span data-ttu-id="a1b10-251">6,000</span><span class="sxs-lookup"><span data-stu-id="a1b10-251">6,000</span></span></td>
<td><span data-ttu-id="a1b10-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a1b10-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a1b10-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-254">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-254">CC003</span></span></td>
<td><span data-ttu-id="a1b10-255">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-255">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-256">0</span><span class="sxs-lookup"><span data-stu-id="a1b10-256">0</span></span></td>
<td><span data-ttu-id="a1b10-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a1b10-258">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-259">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="a1b10-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a1b10-260">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-261">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-261">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-262">المعادلة</span><span class="sxs-lookup"><span data-stu-id="a1b10-262">Formula</span></span></th>
<th><span data-ttu-id="a1b10-263">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-263">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-264">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-264">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-265">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-266">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-266">CC001</span></span></td>
<td><span data-ttu-id="a1b10-267">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-267">HR</span></span></td>
<td><span data-ttu-id="a1b10-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a1b10-269">1</span><span class="sxs-lookup"><span data-stu-id="a1b10-269">1</span></span></td>
<td><span data-ttu-id="a1b10-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a1b10-271">500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-272">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-272">CC002</span></span></td>
<td><span data-ttu-id="a1b10-273">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-273">Finance</span></span></td>
<td><span data-ttu-id="a1b10-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a1b10-275">1</span><span class="sxs-lookup"><span data-stu-id="a1b10-275">1</span></span></td>
<td><span data-ttu-id="a1b10-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a1b10-277">500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-278">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-278">CC003</span></span></td>
<td><span data-ttu-id="a1b10-279">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-279">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a1b10-281">0</span><span class="sxs-lookup"><span data-stu-id="a1b10-281">0</span></span></td>
<td><span data-ttu-id="a1b10-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a1b10-283">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a1b10-284">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-285">Journal</span></span></th>
<th><span data-ttu-id="a1b10-286">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1b10-287">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1b10-288">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-289">00002</span><span class="sxs-lookup"><span data-stu-id="a1b10-289">00002</span></span></td>
<td><span data-ttu-id="a1b10-290">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a1b10-291">مالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-291">Fiscal</span></span></td>
<td><span data-ttu-id="a1b10-292">2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-292">2017</span></span></td>
<td><span data-ttu-id="a1b10-293">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-293">Period 1</span></span></td>
<td><span data-ttu-id="a1b10-294">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a1b10-295">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="a1b10-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-296">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-297">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-298">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-298">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-299">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-299">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-300">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-301">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-302">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-302">CC099</span></span></td>
<td><span data-ttu-id="a1b10-303">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-303">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-304">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-304">10001</span></span></td>
<td><span data-ttu-id="a1b10-305">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-305">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-306">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-306">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-307">1000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-308">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-309">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-309">CC099</span></span></td>
<td><span data-ttu-id="a1b10-310">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-310">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-311">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-311">10001</span></span></td>
<td><span data-ttu-id="a1b10-312">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-312">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-313">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-313">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1b10-315">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-316">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-317">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-317">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-318">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-318">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-319">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-319">Amount</span></span></th>
<th><span data-ttu-id="a1b10-320">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-321">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-321">CC099</span></span></td>
<td><span data-ttu-id="a1b10-322">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-322">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-323">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-323">10001</span></span></td>
<td><span data-ttu-id="a1b10-324">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-324">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-325">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-325">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-326">-1000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-326">-1,000.00</span></span></td>
<td><span data-ttu-id="a1b10-327">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-328">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-328">CC001</span></span></td>
<td><span data-ttu-id="a1b10-329">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-329">HR</span></span></td>
<td><span data-ttu-id="a1b10-330">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-330">10001</span></span></td>
<td><span data-ttu-id="a1b10-331">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-331">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-332">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-332">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-333">500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-333">500.00</span></span></td>
<td><span data-ttu-id="a1b10-334">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-335">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-335">CC002</span></span></td>
<td><span data-ttu-id="a1b10-336">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-336">Finance</span></span></td>
<td><span data-ttu-id="a1b10-337">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-337">10001</span></span></td>
<td><span data-ttu-id="a1b10-338">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-338">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-339">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-339">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-340">500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-340">500.00</span></span></td>
<td><span data-ttu-id="a1b10-341">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-342">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-342">CC099</span></span></td>
<td><span data-ttu-id="a1b10-343">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="a1b10-343">Default cost center</span></span></td>
<td><span data-ttu-id="a1b10-344">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-344">10001</span></span></td>
<td><span data-ttu-id="a1b10-345">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-345">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-346">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-346">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-347">-9,000.00</span></span></td>
<td><span data-ttu-id="a1b10-348">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-349">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-349">CC001</span></span></td>
<td><span data-ttu-id="a1b10-350">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-350">HR</span></span></td>
<td><span data-ttu-id="a1b10-351">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-351">10001</span></span></td>
<td><span data-ttu-id="a1b10-352">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-352">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-353">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-353">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-354">1,285.71</span></span></td>
<td><span data-ttu-id="a1b10-355">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-356">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-356">CC002</span></span></td>
<td><span data-ttu-id="a1b10-357">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-357">Finance</span></span></td>
<td><span data-ttu-id="a1b10-358">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-358">10001</span></span></td>
<td><span data-ttu-id="a1b10-359">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-359">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-360">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-360">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a1b10-361">7,714.29</span></span></td>
<td><span data-ttu-id="a1b10-362">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-363">للمزيد من المعلومات، راجع [إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="a1b10-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a1b10-364">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="a1b10-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a1b10-365">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="a1b10-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a1b10-366">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="a1b10-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a1b10-367">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="a1b10-367">Define the overhead rate</span></span>

<span data-ttu-id="a1b10-368">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="a1b10-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a1b10-369">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="a1b10-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-370">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-370">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-371">الساعات</span><span class="sxs-lookup"><span data-stu-id="a1b10-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-372">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-372">Proj 1</span></span></td>
<td><span data-ttu-id="a1b10-373">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-373">Project 1</span></span></td>
<td><span data-ttu-id="a1b10-374">3</span><span class="sxs-lookup"><span data-stu-id="a1b10-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-375">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-375">Proj 2</span></span></td>
<td><span data-ttu-id="a1b10-376">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-376">Project 2</span></span></td>
<td><span data-ttu-id="a1b10-377">1</span><span class="sxs-lookup"><span data-stu-id="a1b10-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-378">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-379">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-379">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-380">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-380">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-381">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-381">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-382">الوحدات</span><span class="sxs-lookup"><span data-stu-id="a1b10-382">Units</span></span></th>
<th><span data-ttu-id="a1b10-383">المعدل</span><span class="sxs-lookup"><span data-stu-id="a1b10-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-384">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-384">CC001</span></span></td>
<td><span data-ttu-id="a1b10-385">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-385">HR</span></span></td>
<td><span data-ttu-id="a1b10-386">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-386">10001</span></span></td>
<td><span data-ttu-id="a1b10-387">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-387">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-388">1</span><span class="sxs-lookup"><span data-stu-id="a1b10-388">1</span></span></td>
<td><span data-ttu-id="a1b10-389">10</span><span class="sxs-lookup"><span data-stu-id="a1b10-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-390">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="a1b10-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-391">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-391">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-392">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-392">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-393">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-393">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-394">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-394">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-395">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-396">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-396">Proj 1</span></span></td>
<td><span data-ttu-id="a1b10-397">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-397">Project 1</span></span></td>
<td><span data-ttu-id="a1b10-398">3</span><span class="sxs-lookup"><span data-stu-id="a1b10-398">3</span></span></td>
<td><span data-ttu-id="a1b10-399">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-399">10001</span></span></td>
<td><span data-ttu-id="a1b10-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a1b10-401">30.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-402">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-402">Proj 2</span></span></td>
<td><span data-ttu-id="a1b10-403">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-403">Project 2</span></span></td>
<td><span data-ttu-id="a1b10-404">1</span><span class="sxs-lookup"><span data-stu-id="a1b10-404">1</span></span></td>
<td><span data-ttu-id="a1b10-405">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-405">10001</span></span></td>
<td><span data-ttu-id="a1b10-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a1b10-407">10.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a1b10-408">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-409">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-409">Journal</span></span></th>
<th><span data-ttu-id="a1b10-410">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1b10-411">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1b10-412">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-413">00003</span><span class="sxs-lookup"><span data-stu-id="a1b10-413">00003</span></span></td>
<td><span data-ttu-id="a1b10-414">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="a1b10-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a1b10-415">مالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-415">Fiscal</span></span></td>
<td><span data-ttu-id="a1b10-416">2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-416">2017</span></span></td>
<td><span data-ttu-id="a1b10-417">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-417">Period 1</span></span></td>
<td><span data-ttu-id="a1b10-418">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a1b10-419">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="a1b10-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-420">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-421">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-421">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-422">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-423">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-424">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-424">Proj 1</span></span></td>
<td><span data-ttu-id="a1b10-425">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a1b10-426">3.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-427">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-428">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-428">Proj 2</span></span></td>
<td><span data-ttu-id="a1b10-429">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a1b10-430">1.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1b10-431">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-432">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-433">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-433">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-434">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-434">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-435">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-435">Amount</span></span></th>
<th><span data-ttu-id="a1b10-436">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="a1b10-437">CC0001</span></span></td>
<td><span data-ttu-id="a1b10-438">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-438">HR</span></span></td>
<td><span data-ttu-id="a1b10-439">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-439">10001</span></span></td>
<td><span data-ttu-id="a1b10-440">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-440">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-441">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-441">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-442">-30.00</span></span></td>
<td><span data-ttu-id="a1b10-443">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-444">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-444">Proj 1</span></span></td>
<td><span data-ttu-id="a1b10-445">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a1b10-446">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-446">10001</span></span></td>
<td><span data-ttu-id="a1b10-447">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-447">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-448">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-448">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-449">30.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-449">30.00</span></span></td>
<td><span data-ttu-id="a1b10-450">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-451">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-451">CC001</span></span></td>
<td><span data-ttu-id="a1b10-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-452">HR</span></span></td>
<td><span data-ttu-id="a1b10-453">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-453">10001</span></span></td>
<td><span data-ttu-id="a1b10-454">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-454">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-455">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-455">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-456">-10.00</span></span></td>
<td><span data-ttu-id="a1b10-457">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-458">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-458">Proj 2</span></span></td>
<td><span data-ttu-id="a1b10-459">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a1b10-460">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-460">10001</span></span></td>
<td><span data-ttu-id="a1b10-461">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-461">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-462">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-462">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-463">10.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-463">10.00</span></span></td>
<td><span data-ttu-id="a1b10-464">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-465">لمزيد من المعلومات، راجع [إجراء حسابات المصروفات الإضافية](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="a1b10-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a1b10-466">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a1b10-467">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="a1b10-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a1b10-468">يدعم تطبيق Finance طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="a1b10-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="a1b10-469">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a1b10-470">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="a1b10-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a1b10-471">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a1b10-472">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="a1b10-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a1b10-473">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a1b10-474">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a1b10-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a1b10-475">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-475">Define the cost allocation</span></span>

<span data-ttu-id="a1b10-476">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a1b10-477">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a1b10-478">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="a1b10-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-479">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-479">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-480">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-481">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-481">CC002</span></span></td>
<td><span data-ttu-id="a1b10-482">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-482">Finance</span></span></td>
<td><span data-ttu-id="a1b10-483">35</span><span class="sxs-lookup"><span data-stu-id="a1b10-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-484">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-484">CC003</span></span></td>
<td><span data-ttu-id="a1b10-485">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-485">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-486">55</span><span class="sxs-lookup"><span data-stu-id="a1b10-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-487">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-487">CC004</span></span></td>
<td><span data-ttu-id="a1b10-488">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-488">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-489">10</span><span class="sxs-lookup"><span data-stu-id="a1b10-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-490">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a1b10-491">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="a1b10-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-492">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-492">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-493">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-494">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-494">CC003</span></span></td>
<td><span data-ttu-id="a1b10-495">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-495">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-496">65</span><span class="sxs-lookup"><span data-stu-id="a1b10-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-497">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-497">CC004</span></span></td>
<td><span data-ttu-id="a1b10-498">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-498">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-499">35</span><span class="sxs-lookup"><span data-stu-id="a1b10-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-500">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a1b10-501">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="a1b10-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-502">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-502">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-503">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="a1b10-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-504">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-504">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-505">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-505">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-506">60</span><span class="sxs-lookup"><span data-stu-id="a1b10-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-507">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-507">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-508">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-508">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-509">20</span><span class="sxs-lookup"><span data-stu-id="a1b10-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-510">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a1b10-511">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="a1b10-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-512">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-512">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-513">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="a1b10-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-514">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-514">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-515">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-515">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-516">80</span><span class="sxs-lookup"><span data-stu-id="a1b10-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-517">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-517">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-518">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-518">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-519">15</span><span class="sxs-lookup"><span data-stu-id="a1b10-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a1b10-520">يُمكن اشتقاق القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="a1b10-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a1b10-521">للمزيد من المعلومات، راجع [قالب موفر القياسات الإحصائية](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="a1b10-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="a1b10-522">يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="a1b10-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-523">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-523">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-524">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-524">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-525">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-525">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-526">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-526">Amount</span></span></th>
<th><span data-ttu-id="a1b10-527">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-528">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-528">CC002</span></span></td>
<td><span data-ttu-id="a1b10-529">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-529">Finance</span></span></td>
<td><span data-ttu-id="a1b10-530">35</span><span class="sxs-lookup"><span data-stu-id="a1b10-530">35</span></span></td>
<td><span data-ttu-id="a1b10-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a1b10-532">175.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-532">175.00</span></span></td>
<td><span data-ttu-id="a1b10-533">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-534">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-534">CC003</span></span></td>
<td><span data-ttu-id="a1b10-535">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-535">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-536">55</span><span class="sxs-lookup"><span data-stu-id="a1b10-536">55</span></span></td>
<td><span data-ttu-id="a1b10-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a1b10-538">275.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-538">275.00</span></span></td>
<td><span data-ttu-id="a1b10-539">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-540">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-540">CC004</span></span></td>
<td><span data-ttu-id="a1b10-541">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-541">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-542">10</span><span class="sxs-lookup"><span data-stu-id="a1b10-542">10</span></span></td>
<td><span data-ttu-id="a1b10-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a1b10-544">50.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-544">50.00</span></span></td>
<td><span data-ttu-id="a1b10-545">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-546">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-546">CC002</span></span></td>
<td><span data-ttu-id="a1b10-547">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-547">Finance</span></span></td>
<td><span data-ttu-id="a1b10-548">35</span><span class="sxs-lookup"><span data-stu-id="a1b10-548">35</span></span></td>
<td><span data-ttu-id="a1b10-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a1b10-550">436.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-550">436.00</span></span></td>
<td><span data-ttu-id="a1b10-551">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-552">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-552">CC003</span></span></td>
<td><span data-ttu-id="a1b10-553">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-553">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-554">55</span><span class="sxs-lookup"><span data-stu-id="a1b10-554">55</span></span></td>
<td><span data-ttu-id="a1b10-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a1b10-556">685.14</span><span class="sxs-lookup"><span data-stu-id="a1b10-556">685.14</span></span></td>
<td><span data-ttu-id="a1b10-557">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-558">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-558">CC004</span></span></td>
<td><span data-ttu-id="a1b10-559">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-559">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-560">10</span><span class="sxs-lookup"><span data-stu-id="a1b10-560">10</span></span></td>
<td><span data-ttu-id="a1b10-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a1b10-562">124.57</span><span class="sxs-lookup"><span data-stu-id="a1b10-562">124.57</span></span></td>
<td><span data-ttu-id="a1b10-563">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-564">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="a1b10-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-565">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-565">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-566">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-566">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-567">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-567">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-568">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-568">Amount</span></span></th>
<th><span data-ttu-id="a1b10-569">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-570">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-570">CC003</span></span></td>
<td><span data-ttu-id="a1b10-571">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-571">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-572">65</span><span class="sxs-lookup"><span data-stu-id="a1b10-572">65</span></span></td>
<td><span data-ttu-id="a1b10-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a1b10-574">438.75</span><span class="sxs-lookup"><span data-stu-id="a1b10-574">438.75</span></span></td>
<td><span data-ttu-id="a1b10-575">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-576">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-576">CC004</span></span></td>
<td><span data-ttu-id="a1b10-577">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-577">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-578">35</span><span class="sxs-lookup"><span data-stu-id="a1b10-578">35</span></span></td>
<td><span data-ttu-id="a1b10-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a1b10-580">236.25</span><span class="sxs-lookup"><span data-stu-id="a1b10-580">236.25</span></span></td>
<td><span data-ttu-id="a1b10-581">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-582">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-582">CC003</span></span></td>
<td><span data-ttu-id="a1b10-583">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-583">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-584">65</span><span class="sxs-lookup"><span data-stu-id="a1b10-584">65</span></span></td>
<td><span data-ttu-id="a1b10-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a1b10-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a1b10-586">5,297.69</span></span></td>
<td><span data-ttu-id="a1b10-587">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-588">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-588">CC004</span></span></td>
<td><span data-ttu-id="a1b10-589">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-589">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-590">35</span><span class="sxs-lookup"><span data-stu-id="a1b10-590">35</span></span></td>
<td><span data-ttu-id="a1b10-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="a1b10-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a1b10-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a1b10-592">2,852.60</span></span></td>
<td><span data-ttu-id="a1b10-593">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-594">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="a1b10-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-595">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-595">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-596">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-596">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-597">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-597">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-598">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-598">Amount</span></span></th>
<th><span data-ttu-id="a1b10-599">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-600">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-600">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-601">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-601">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-602">60</span><span class="sxs-lookup"><span data-stu-id="a1b10-602">60</span></span></td>
<td><span data-ttu-id="a1b10-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="a1b10-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a1b10-604">535.31</span><span class="sxs-lookup"><span data-stu-id="a1b10-604">535.31</span></span></td>
<td><span data-ttu-id="a1b10-605">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-606">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-606">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-607">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-607">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-608">20</span><span class="sxs-lookup"><span data-stu-id="a1b10-608">20</span></span></td>
<td><span data-ttu-id="a1b10-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="a1b10-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a1b10-610">178.44</span><span class="sxs-lookup"><span data-stu-id="a1b10-610">178.44</span></span></td>
<td><span data-ttu-id="a1b10-611">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-612">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-612">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-613">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-613">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-614">60</span><span class="sxs-lookup"><span data-stu-id="a1b10-614">60</span></span></td>
<td><span data-ttu-id="a1b10-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="a1b10-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a1b10-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a1b10-616">4,487.12</span></span></td>
<td><span data-ttu-id="a1b10-617">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-618">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-618">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-619">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-619">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-620">20</span><span class="sxs-lookup"><span data-stu-id="a1b10-620">20</span></span></td>
<td><span data-ttu-id="a1b10-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="a1b10-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a1b10-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-622">1,495.71</span></span></td>
<td><span data-ttu-id="a1b10-623">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b10-624">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="a1b10-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-625">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-625">Cost object</span></span></th>
<th><span data-ttu-id="a1b10-626">المقدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-626">Magnitude</span></span></th>
<th><span data-ttu-id="a1b10-627">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="a1b10-627">Allocation factor</span></span></th>
<th><span data-ttu-id="a1b10-628">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-628">Amount</span></span></th>
<th><span data-ttu-id="a1b10-629">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-630">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-630">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-631">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-631">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-632">80</span><span class="sxs-lookup"><span data-stu-id="a1b10-632">80</span></span></td>
<td><span data-ttu-id="a1b10-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="a1b10-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a1b10-634">241.05</span><span class="sxs-lookup"><span data-stu-id="a1b10-634">241.05</span></span></td>
<td><span data-ttu-id="a1b10-635">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-636">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-636">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-637">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-637">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-638">15</span><span class="sxs-lookup"><span data-stu-id="a1b10-638">15</span></span></td>
<td><span data-ttu-id="a1b10-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="a1b10-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a1b10-640">45.20</span><span class="sxs-lookup"><span data-stu-id="a1b10-640">45.20</span></span></td>
<td><span data-ttu-id="a1b10-641">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-642">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-642">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-643">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-643">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-644">80</span><span class="sxs-lookup"><span data-stu-id="a1b10-644">80</span></span></td>
<td><span data-ttu-id="a1b10-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="a1b10-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a1b10-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a1b10-646">2,507.09</span></span></td>
<td><span data-ttu-id="a1b10-647">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-648">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-648">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-649">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-649">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-650">15</span><span class="sxs-lookup"><span data-stu-id="a1b10-650">15</span></span></td>
<td><span data-ttu-id="a1b10-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="a1b10-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a1b10-652">470.08</span><span class="sxs-lookup"><span data-stu-id="a1b10-652">470.08</span></span></td>
<td><span data-ttu-id="a1b10-653">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a1b10-654">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="a1b10-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-655">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-655">Journal</span></span></th>
<th><span data-ttu-id="a1b10-656">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1b10-657">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1b10-658">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="a1b10-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-659">00004</span><span class="sxs-lookup"><span data-stu-id="a1b10-659">00004</span></span></td>
<td><span data-ttu-id="a1b10-660">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a1b10-661">مالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-661">Fiscal</span></span></td>
<td><span data-ttu-id="a1b10-662">2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-662">2017</span></span></td>
<td><span data-ttu-id="a1b10-663">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-663">Period 1</span></span></td>
<td><span data-ttu-id="a1b10-664">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a1b10-665">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="a1b10-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1b10-666">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-667">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-668">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-668">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-669">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-669">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-670">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-671">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-672">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-672">CC001</span></span></td>
<td><span data-ttu-id="a1b10-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-673">HR</span></span></td>
<td><span data-ttu-id="a1b10-674">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-674">10001</span></span></td>
<td><span data-ttu-id="a1b10-675">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-675">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-676">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-676">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-677">500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-678">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-679">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-679">CC001</span></span></td>
<td><span data-ttu-id="a1b10-680">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-680">HR</span></span></td>
<td><span data-ttu-id="a1b10-681">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-681">10001</span></span></td>
<td><span data-ttu-id="a1b10-682">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-682">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-683">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-683">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-685">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-686">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-686">CC002</span></span></td>
<td><span data-ttu-id="a1b10-687">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-687">Finance</span></span></td>
<td><span data-ttu-id="a1b10-688">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-688">10001</span></span></td>
<td><span data-ttu-id="a1b10-689">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-689">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-690">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-690">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-691">675.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-692">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-693">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-693">CC002</span></span></td>
<td><span data-ttu-id="a1b10-694">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-694">Finance</span></span></td>
<td><span data-ttu-id="a1b10-695">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-695">10001</span></span></td>
<td><span data-ttu-id="a1b10-696">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-696">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-697">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-697">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a1b10-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-699">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-700">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-700">CC003</span></span></td>
<td><span data-ttu-id="a1b10-701">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-701">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-702">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-702">10001</span></span></td>
<td><span data-ttu-id="a1b10-703">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-703">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-704">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-704">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-705">713.75</span><span class="sxs-lookup"><span data-stu-id="a1b10-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-706">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-707">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-707">CC003</span></span></td>
<td><span data-ttu-id="a1b10-708">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-708">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-709">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-709">10001</span></span></td>
<td><span data-ttu-id="a1b10-710">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-710">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-711">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-711">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a1b10-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-713">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-714">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-714">CC003</span></span></td>
<td><span data-ttu-id="a1b10-715">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-715">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-716">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-716">10001</span></span></td>
<td><span data-ttu-id="a1b10-717">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-717">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-718">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-718">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-719">286.25</span><span class="sxs-lookup"><span data-stu-id="a1b10-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-720">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-721">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-721">CC003</span></span></td>
<td><span data-ttu-id="a1b10-722">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-722">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-723">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-723">10001</span></span></td>
<td><span data-ttu-id="a1b10-724">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-724">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-725">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-725">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a1b10-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-727">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-728">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-728">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-729">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-729">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-730">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-730">10001</span></span></td>
<td><span data-ttu-id="a1b10-731">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-731">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-732">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-732">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-733">776.36</span><span class="sxs-lookup"><span data-stu-id="a1b10-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-734">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-735">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-735">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-736">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-736">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-737">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-737">10001</span></span></td>
<td><span data-ttu-id="a1b10-738">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-738">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-739">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-739">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a1b10-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-741">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-742">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-742">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-743">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-743">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-744">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-744">10001</span></span></td>
<td><span data-ttu-id="a1b10-745">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-745">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-746">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-746">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-747">223.64</span><span class="sxs-lookup"><span data-stu-id="a1b10-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-748">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1b10-749">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-749">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-750">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-750">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-751">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-751">10001</span></span></td>
<td><span data-ttu-id="a1b10-752">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-752">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-753">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-753">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a1b10-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1b10-755">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1b10-756">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1b10-757">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-757">Cost element</span></span></th>
<th><span data-ttu-id="a1b10-758">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-758">Cost behavior</span></span></th>
<th><span data-ttu-id="a1b10-759">المبلغ</span><span class="sxs-lookup"><span data-stu-id="a1b10-759">Amount</span></span></th>
<th><span data-ttu-id="a1b10-760">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="a1b10-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1b10-761">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-761">CC001</span></span></td>
<td><span data-ttu-id="a1b10-762">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-762">HR</span></span></td>
<td><span data-ttu-id="a1b10-763">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-763">10001</span></span></td>
<td><span data-ttu-id="a1b10-764">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-764">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-765">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-765">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-766">-500.00</span></span></td>
<td><span data-ttu-id="a1b10-767">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-768">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-768">CC002</span></span></td>
<td><span data-ttu-id="a1b10-769">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-769">Finance</span></span></td>
<td><span data-ttu-id="a1b10-770">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-770">10001</span></span></td>
<td><span data-ttu-id="a1b10-771">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-771">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-772">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-772">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-773">175.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-773">175.00</span></span></td>
<td><span data-ttu-id="a1b10-774">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-775">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-775">CC003</span></span></td>
<td><span data-ttu-id="a1b10-776">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-776">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-777">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-777">10001</span></span></td>
<td><span data-ttu-id="a1b10-778">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-778">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-779">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-779">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-780">275.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-780">275.00</span></span></td>
<td><span data-ttu-id="a1b10-781">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-782">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-782">CC004</span></span></td>
<td><span data-ttu-id="a1b10-783">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-783">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-784">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-784">10001</span></span></td>
<td><span data-ttu-id="a1b10-785">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-785">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-786">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-786">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-787">50,00</span><span class="sxs-lookup"><span data-stu-id="a1b10-787">50,00</span></span></td>
<td><span data-ttu-id="a1b10-788">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-789">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-789">CC001</span></span></td>
<td><span data-ttu-id="a1b10-790">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="a1b10-790">HR</span></span></td>
<td><span data-ttu-id="a1b10-791">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-791">10001</span></span></td>
<td><span data-ttu-id="a1b10-792">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-792">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-793">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-793">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-794">-1,245.71</span></span></td>
<td><span data-ttu-id="a1b10-795">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-796">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-796">CC002</span></span></td>
<td><span data-ttu-id="a1b10-797">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-797">Finance</span></span></td>
<td><span data-ttu-id="a1b10-798">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-798">10001</span></span></td>
<td><span data-ttu-id="a1b10-799">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-799">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-800">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-800">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-801">436.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-801">436.00</span></span></td>
<td><span data-ttu-id="a1b10-802">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-803">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-803">CC003</span></span></td>
<td><span data-ttu-id="a1b10-804">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-804">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-805">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-805">10001</span></span></td>
<td><span data-ttu-id="a1b10-806">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-806">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-807">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-807">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-808">685.14</span><span class="sxs-lookup"><span data-stu-id="a1b10-808">685.14</span></span></td>
<td><span data-ttu-id="a1b10-809">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-810">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-810">CC004</span></span></td>
<td><span data-ttu-id="a1b10-811">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-811">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-812">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-812">10001</span></span></td>
<td><span data-ttu-id="a1b10-813">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-813">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-814">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-814">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-815">124.57</span><span class="sxs-lookup"><span data-stu-id="a1b10-815">124.57</span></span></td>
<td><span data-ttu-id="a1b10-816">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-817">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-817">CC002</span></span></td>
<td><span data-ttu-id="a1b10-818">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-818">Finance</span></span></td>
<td><span data-ttu-id="a1b10-819">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-819">10001</span></span></td>
<td><span data-ttu-id="a1b10-820">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-820">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-821">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-821">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-822">-675.00</span></span></td>
<td><span data-ttu-id="a1b10-823">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-824">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-824">CC003</span></span></td>
<td><span data-ttu-id="a1b10-825">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-825">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-826">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-826">10001</span></span></td>
<td><span data-ttu-id="a1b10-827">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-827">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-828">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-828">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-829">438.75</span><span class="sxs-lookup"><span data-stu-id="a1b10-829">438.75</span></span></td>
<td><span data-ttu-id="a1b10-830">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-831">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-831">CC004</span></span></td>
<td><span data-ttu-id="a1b10-832">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-832">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-833">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-833">10001</span></span></td>
<td><span data-ttu-id="a1b10-834">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-834">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-835">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-835">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-836">236.25</span><span class="sxs-lookup"><span data-stu-id="a1b10-836">236.25</span></span></td>
<td><span data-ttu-id="a1b10-837">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-838">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-838">CC002</span></span></td>
<td><span data-ttu-id="a1b10-839">المالية</span><span class="sxs-lookup"><span data-stu-id="a1b10-839">Finance</span></span></td>
<td><span data-ttu-id="a1b10-840">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-840">10001</span></span></td>
<td><span data-ttu-id="a1b10-841">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-841">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-842">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-842">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="a1b10-843">-8,150.29</span></span></td>
<td><span data-ttu-id="a1b10-844">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-845">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-845">CC003</span></span></td>
<td><span data-ttu-id="a1b10-846">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-846">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-847">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-847">10001</span></span></td>
<td><span data-ttu-id="a1b10-848">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-848">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-849">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-849">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a1b10-850">5,297.69</span></span></td>
<td><span data-ttu-id="a1b10-851">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-852">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-852">CC004</span></span></td>
<td><span data-ttu-id="a1b10-853">التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1b10-853">Packaging</span></span></td>
<td><span data-ttu-id="a1b10-854">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-854">10001</span></span></td>
<td><span data-ttu-id="a1b10-855">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-855">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-856">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-856">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a1b10-857">2,852.60</span></span></td>
<td><span data-ttu-id="a1b10-858">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-859">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-859">CC003</span></span></td>
<td><span data-ttu-id="a1b10-860">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-860">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-861">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-861">10001</span></span></td>
<td><span data-ttu-id="a1b10-862">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-862">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-863">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-863">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="a1b10-864">-713.75</span></span></td>
<td><span data-ttu-id="a1b10-865">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-866">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-866">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-867">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-867">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-868">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-868">10001</span></span></td>
<td><span data-ttu-id="a1b10-869">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-869">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-870">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-870">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-871">535.31</span><span class="sxs-lookup"><span data-stu-id="a1b10-871">535.31</span></span></td>
<td><span data-ttu-id="a1b10-872">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-873">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-873">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-874">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-874">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-875">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-875">10001</span></span></td>
<td><span data-ttu-id="a1b10-876">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-876">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-877">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-877">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-878">178.44</span><span class="sxs-lookup"><span data-stu-id="a1b10-878">178.44</span></span></td>
<td><span data-ttu-id="a1b10-879">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-880">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-880">CC003</span></span></td>
<td><span data-ttu-id="a1b10-881">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-881">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-882">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-882">10001</span></span></td>
<td><span data-ttu-id="a1b10-883">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-883">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-884">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-884">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="a1b10-885">-5,982.83</span></span></td>
<td><span data-ttu-id="a1b10-886">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-887">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-887">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-888">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-888">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-889">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-889">10001</span></span></td>
<td><span data-ttu-id="a1b10-890">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-890">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-891">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-891">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a1b10-892">4,487.12</span></span></td>
<td><span data-ttu-id="a1b10-893">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-894">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-894">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-895">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-895">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-896">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-896">10001</span></span></td>
<td><span data-ttu-id="a1b10-897">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-897">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-898">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-898">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a1b10-899">1,495.71</span></span></td>
<td><span data-ttu-id="a1b10-900">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-901">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-901">CC003</span></span></td>
<td><span data-ttu-id="a1b10-902">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-902">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-903">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-903">10001</span></span></td>
<td><span data-ttu-id="a1b10-904">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-904">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-905">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-905">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="a1b10-906">-286.25</span></span></td>
<td><span data-ttu-id="a1b10-907">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-908">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-908">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-909">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-909">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-910">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-910">10001</span></span></td>
<td><span data-ttu-id="a1b10-911">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-911">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-912">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-912">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-913">241.05</span><span class="sxs-lookup"><span data-stu-id="a1b10-913">241.05</span></span></td>
<td><span data-ttu-id="a1b10-914">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-915">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-915">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-916">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-916">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-917">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-917">10001</span></span></td>
<td><span data-ttu-id="a1b10-918">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-918">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-919">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-919">Fixed cost</span></span></td>
<td><span data-ttu-id="a1b10-920">45.20</span><span class="sxs-lookup"><span data-stu-id="a1b10-920">45.20</span></span></td>
<td><span data-ttu-id="a1b10-921">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-922">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-922">CC003</span></span></td>
<td><span data-ttu-id="a1b10-923">التجميع</span><span class="sxs-lookup"><span data-stu-id="a1b10-923">Assembly</span></span></td>
<td><span data-ttu-id="a1b10-924">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-924">10001</span></span></td>
<td><span data-ttu-id="a1b10-925">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-925">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-926">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-926">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="a1b10-927">-2,977.17</span></span></td>
<td><span data-ttu-id="a1b10-928">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-929">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-929">Prod 1</span></span></td>
<td><span data-ttu-id="a1b10-930">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-930">Product 1</span></span></td>
<td><span data-ttu-id="a1b10-931">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-931">10001</span></span></td>
<td><span data-ttu-id="a1b10-932">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-932">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-933">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-933">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a1b10-934">2,507.09</span></span></td>
<td><span data-ttu-id="a1b10-935">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1b10-936">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-936">Prod 2</span></span></td>
<td><span data-ttu-id="a1b10-937">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-937">Product 2</span></span></td>
<td><span data-ttu-id="a1b10-938">10001</span><span class="sxs-lookup"><span data-stu-id="a1b10-938">10001</span></span></td>
<td><span data-ttu-id="a1b10-939">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-939">Electricity</span></span></td>
<td><span data-ttu-id="a1b10-940">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-940">Variable cost</span></span></td>
<td><span data-ttu-id="a1b10-941">470.08</span><span class="sxs-lookup"><span data-stu-id="a1b10-941">470.08</span></span></td>
<td><span data-ttu-id="a1b10-942">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="a1b10-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a1b10-943">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="a1b10-943">Conclusion</span></span>
<span data-ttu-id="a1b10-944">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="a1b10-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a1b10-945">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a1b10-946">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a1b10-947">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a1b10-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a1b10-948">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a1b10-949">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="a1b10-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a1b10-950">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="a1b10-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a1b10-951">CC099</span><span class="sxs-lookup"><span data-stu-id="a1b10-951">CC099</span></span></th>
<th><span data-ttu-id="a1b10-952">CC001</span><span class="sxs-lookup"><span data-stu-id="a1b10-952">CC001</span></span></th>
<th><span data-ttu-id="a1b10-953">CC002</span><span class="sxs-lookup"><span data-stu-id="a1b10-953">CC002</span></span></th>
<th><span data-ttu-id="a1b10-954">CC003</span><span class="sxs-lookup"><span data-stu-id="a1b10-954">CC003</span></span></th>
<th><span data-ttu-id="a1b10-955">CC004</span><span class="sxs-lookup"><span data-stu-id="a1b10-955">CC004</span></span></th>
<th><span data-ttu-id="a1b10-956">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-956">Proj 1</span></span></th>
<th><span data-ttu-id="a1b10-957">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-957">Proj 2</span></span></th>
<th><span data-ttu-id="a1b10-958">منتج 1</span><span class="sxs-lookup"><span data-stu-id="a1b10-958">Prod 1</span></span></th>
<th><span data-ttu-id="a1b10-959">منتج 2</span><span class="sxs-lookup"><span data-stu-id="a1b10-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a1b10-960">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="a1b10-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a1b10-970">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="a1b10-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-971">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a1b10-972">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="a1b10-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-973">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-974">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-975">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-976">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-977">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-978">776.36</span><span class="sxs-lookup"><span data-stu-id="a1b10-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-979">223.64</span><span class="sxs-lookup"><span data-stu-id="a1b10-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a1b10-981">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="a1b10-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-982">000</span><span class="sxs-lookup"><span data-stu-id="a1b10-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-983">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-984">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-985">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-986">0.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-987">30.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-988">10.00</span><span class="sxs-lookup"><span data-stu-id="a1b10-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a1b10-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a1b10-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1b10-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1b10-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a1b10-992">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a1b10-993">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a1b10-994">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a1b10-995">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a1b10-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a1b10-996">لمزيد من المعلومات، راجع [سياسة التكاليف وحساب المصروفات الإضافية](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="a1b10-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



