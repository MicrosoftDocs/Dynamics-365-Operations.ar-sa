---
title: "عملية حساب المصروفات الزائدة"
description: "يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: be548959985a6fcaabf482f1e5951024633283cf
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="61dd3-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="61dd3-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61dd3-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="61dd3-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="61dd3-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="61dd3-105">Term definition</span></span>
---------------

<span data-ttu-id="61dd3-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="61dd3-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="61dd3-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="61dd3-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="61dd3-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="61dd3-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="61dd3-109">Rent</span></span>
-   <span data-ttu-id="61dd3-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-110">Electricity</span></span>
-   <span data-ttu-id="61dd3-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="61dd3-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="61dd3-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="61dd3-112">Overhead calculation overview</span></span>
<span data-ttu-id="61dd3-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="61dd3-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="61dd3-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="61dd3-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="61dd3-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="61dd3-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="61dd3-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="61dd3-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="61dd3-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="61dd3-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-119">Version type</span></span>
-   <span data-ttu-id="61dd3-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="61dd3-120">Date and time</span></span>
-   <span data-ttu-id="61dd3-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="61dd3-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="61dd3-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-122">Fiscal year</span></span>
-   <span data-ttu-id="61dd3-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-123">Fiscal period</span></span>

<span data-ttu-id="61dd3-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="61dd3-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="61dd3-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="61dd3-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="61dd3-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="61dd3-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="61dd3-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="61dd3-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="61dd3-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="61dd3-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="61dd3-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="61dd3-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="61dd3-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="61dd3-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="61dd3-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="61dd3-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="61dd3-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="61dd3-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="61dd3-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="61dd3-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="61dd3-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="61dd3-140">Main account</span></span></th>
<th><span data-ttu-id="61dd3-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="61dd3-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="61dd3-143">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-143">CC099</span></span></td>
<td><span data-ttu-id="61dd3-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-144">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-145">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-145">10001</span></span></td>
<td><span data-ttu-id="61dd3-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-146">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="61dd3-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="61dd3-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="61dd3-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="61dd3-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="61dd3-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="61dd3-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-151">Define the cost behavior rule</span></span>

<span data-ttu-id="61dd3-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="61dd3-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="61dd3-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="61dd3-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="61dd3-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="61dd3-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="61dd3-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="61dd3-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="61dd3-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="61dd3-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="61dd3-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="61dd3-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="61dd3-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="61dd3-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-160">Journal</span></span></th>
<th><span data-ttu-id="61dd3-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="61dd3-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="61dd3-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-164">00001</span><span class="sxs-lookup"><span data-stu-id="61dd3-164">00001</span></span></td>
<td><span data-ttu-id="61dd3-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="61dd3-166">مالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-166">Fiscal</span></span></td>
<td><span data-ttu-id="61dd3-167">2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-167">2017</span></span></td>
<td><span data-ttu-id="61dd3-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-168">Period 1</span></span></td>
<td><span data-ttu-id="61dd3-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="61dd3-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="61dd3-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-173">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-174">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="61dd3-177">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-177">CC099</span></span></td>
<td><span data-ttu-id="61dd3-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-178">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-179">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-179">10001</span></span></td>
<td><span data-ttu-id="61dd3-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-180">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="61dd3-181">Unclassified</span></span></td>
<td><span data-ttu-id="61dd3-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="61dd3-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-185">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-186">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-187">Amount</span></span></th>
<th><span data-ttu-id="61dd3-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-189">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-189">CC099</span></span></td>
<td><span data-ttu-id="61dd3-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-190">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-191">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-191">10001</span></span></td>
<td><span data-ttu-id="61dd3-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-192">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="61dd3-193">Unclassified</span></span></td>
<td><span data-ttu-id="61dd3-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-194">10,000.00</span></span></td>
<td><span data-ttu-id="61dd3-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-196">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-196">CC099</span></span></td>
<td><span data-ttu-id="61dd3-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-197">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-198">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-198">10001</span></span></td>
<td><span data-ttu-id="61dd3-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-199">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="61dd3-200">Unclassified</span></span></td>
<td><span data-ttu-id="61dd3-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-201">-10,000.00</span></span></td>
<td><span data-ttu-id="61dd3-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-203">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-203">CC099</span></span></td>
<td><span data-ttu-id="61dd3-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-204">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-205">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-205">10001</span></span></td>
<td><span data-ttu-id="61dd3-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-206">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-207">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-208">1,000.00</span></span></td>
<td><span data-ttu-id="61dd3-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-210">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-210">CC099</span></span></td>
<td><span data-ttu-id="61dd3-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-211">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-212">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-212">10001</span></span></td>
<td><span data-ttu-id="61dd3-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-213">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-214">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-215">9,000.00</span></span></td>
<td><span data-ttu-id="61dd3-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-217">للحصول على معلومات تفصيلية حول سلوك التكلفة، راجع سياسة سلوك التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="61dd3-218">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="61dd3-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="61dd3-219">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="61dd3-220">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="61dd3-221">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="61dd3-222">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-222">Define the cost distribution rule</span></span>

<span data-ttu-id="61dd3-223">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="61dd3-224">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="61dd3-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="61dd3-225">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="61dd3-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="61dd3-226">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="61dd3-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="61dd3-227">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="61dd3-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="61dd3-228">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="61dd3-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-229">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-229">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-230">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="61dd3-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-231">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-231">CC001</span></span></td>
<td><span data-ttu-id="61dd3-232">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-232">HR</span></span></td>
<td><span data-ttu-id="61dd3-233">1,000</span><span class="sxs-lookup"><span data-stu-id="61dd3-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-234">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-234">CC002</span></span></td>
<td><span data-ttu-id="61dd3-235">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-235">Finance</span></span></td>
<td><span data-ttu-id="61dd3-236">6,000</span><span class="sxs-lookup"><span data-stu-id="61dd3-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-237">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-237">CC003</span></span></td>
<td><span data-ttu-id="61dd3-238">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-238">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-239">0</span><span class="sxs-lookup"><span data-stu-id="61dd3-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-240">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-241">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-241">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-242">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-242">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-243">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-243">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-244">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-245">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-245">CC001</span></span></td>
<td><span data-ttu-id="61dd3-246">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-246">HR</span></span></td>
<td><span data-ttu-id="61dd3-247">1,000</span><span class="sxs-lookup"><span data-stu-id="61dd3-247">1,000</span></span></td>
<td><span data-ttu-id="61dd3-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="61dd3-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-250">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-250">CC002</span></span></td>
<td><span data-ttu-id="61dd3-251">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-251">Finance</span></span></td>
<td><span data-ttu-id="61dd3-252">6,000</span><span class="sxs-lookup"><span data-stu-id="61dd3-252">6,000</span></span></td>
<td><span data-ttu-id="61dd3-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="61dd3-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="61dd3-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-255">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-255">CC003</span></span></td>
<td><span data-ttu-id="61dd3-256">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-256">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-257">0</span><span class="sxs-lookup"><span data-stu-id="61dd3-257">0</span></span></td>
<td><span data-ttu-id="61dd3-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="61dd3-259">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-260">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="61dd3-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="61dd3-261">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-262">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-262">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-263">المعادلة</span><span class="sxs-lookup"><span data-stu-id="61dd3-263">Formula</span></span></th>
<th><span data-ttu-id="61dd3-264">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-264">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-265">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-265">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-266">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-267">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-267">CC001</span></span></td>
<td><span data-ttu-id="61dd3-268">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-268">HR</span></span></td>
<td><span data-ttu-id="61dd3-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="61dd3-270">1</span><span class="sxs-lookup"><span data-stu-id="61dd3-270">1</span></span></td>
<td><span data-ttu-id="61dd3-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="61dd3-272">500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-273">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-273">CC002</span></span></td>
<td><span data-ttu-id="61dd3-274">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-274">Finance</span></span></td>
<td><span data-ttu-id="61dd3-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="61dd3-276">1</span><span class="sxs-lookup"><span data-stu-id="61dd3-276">1</span></span></td>
<td><span data-ttu-id="61dd3-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="61dd3-278">500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-279">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-279">CC003</span></span></td>
<td><span data-ttu-id="61dd3-280">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-280">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="61dd3-282">0</span><span class="sxs-lookup"><span data-stu-id="61dd3-282">0</span></span></td>
<td><span data-ttu-id="61dd3-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="61dd3-284">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="61dd3-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-286">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-286">Journal</span></span></th>
<th><span data-ttu-id="61dd3-287">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="61dd3-288">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="61dd3-289">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-290">00002</span><span class="sxs-lookup"><span data-stu-id="61dd3-290">00002</span></span></td>
<td><span data-ttu-id="61dd3-291">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="61dd3-292">مالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-292">Fiscal</span></span></td>
<td><span data-ttu-id="61dd3-293">2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-293">2017</span></span></td>
<td><span data-ttu-id="61dd3-294">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-294">Period 1</span></span></td>
<td><span data-ttu-id="61dd3-295">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="61dd3-296">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="61dd3-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-297">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-298">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-299">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-299">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-300">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-300">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-301">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-302">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-303">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-303">CC099</span></span></td>
<td><span data-ttu-id="61dd3-304">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-304">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-305">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-305">10001</span></span></td>
<td><span data-ttu-id="61dd3-306">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-306">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-307">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-307">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-308">1000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-309">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-310">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-310">CC099</span></span></td>
<td><span data-ttu-id="61dd3-311">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-311">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-312">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-312">10001</span></span></td>
<td><span data-ttu-id="61dd3-313">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-313">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-314">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-314">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="61dd3-316">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-317">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-318">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-318">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-319">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-319">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-320">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-320">Amount</span></span></th>
<th><span data-ttu-id="61dd3-321">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-322">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-322">CC099</span></span></td>
<td><span data-ttu-id="61dd3-323">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-323">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-324">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-324">10001</span></span></td>
<td><span data-ttu-id="61dd3-325">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-325">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-326">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-326">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-327">-1000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-327">-1,000.00</span></span></td>
<td><span data-ttu-id="61dd3-328">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-329">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-329">CC001</span></span></td>
<td><span data-ttu-id="61dd3-330">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-330">HR</span></span></td>
<td><span data-ttu-id="61dd3-331">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-331">10001</span></span></td>
<td><span data-ttu-id="61dd3-332">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-332">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-333">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-333">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-334">500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-334">500.00</span></span></td>
<td><span data-ttu-id="61dd3-335">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-336">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-336">CC002</span></span></td>
<td><span data-ttu-id="61dd3-337">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-337">Finance</span></span></td>
<td><span data-ttu-id="61dd3-338">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-338">10001</span></span></td>
<td><span data-ttu-id="61dd3-339">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-339">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-340">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-340">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-341">500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-341">500.00</span></span></td>
<td><span data-ttu-id="61dd3-342">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-343">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-343">CC099</span></span></td>
<td><span data-ttu-id="61dd3-344">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="61dd3-344">Default cost center</span></span></td>
<td><span data-ttu-id="61dd3-345">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-345">10001</span></span></td>
<td><span data-ttu-id="61dd3-346">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-346">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-347">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-347">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-348">-9,000.00</span></span></td>
<td><span data-ttu-id="61dd3-349">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-350">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-350">CC001</span></span></td>
<td><span data-ttu-id="61dd3-351">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-351">HR</span></span></td>
<td><span data-ttu-id="61dd3-352">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-352">10001</span></span></td>
<td><span data-ttu-id="61dd3-353">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-353">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-354">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-354">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-355">1,285.71</span></span></td>
<td><span data-ttu-id="61dd3-356">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-357">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-357">CC002</span></span></td>
<td><span data-ttu-id="61dd3-358">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-358">Finance</span></span></td>
<td><span data-ttu-id="61dd3-359">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-359">10001</span></span></td>
<td><span data-ttu-id="61dd3-360">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-360">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-361">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-361">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="61dd3-362">7,714.29</span></span></td>
<td><span data-ttu-id="61dd3-363">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-364">للحصول على معلومات تفصيلية حول توزيع التكلفة وأسس التوزيع، راجع سياسة توزيع التكلفة وأسس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="61dd3-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="61dd3-365">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="61dd3-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="61dd3-366">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="61dd3-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="61dd3-367">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="61dd3-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="61dd3-368">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="61dd3-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="61dd3-369">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="61dd3-369">Define the overhead rate</span></span>

<span data-ttu-id="61dd3-370">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="61dd3-371">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="61dd3-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-372">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-372">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-373">الساعات</span><span class="sxs-lookup"><span data-stu-id="61dd3-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-374">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-374">Proj 1</span></span></td>
<td><span data-ttu-id="61dd3-375">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-375">Project 1</span></span></td>
<td><span data-ttu-id="61dd3-376">3</span><span class="sxs-lookup"><span data-stu-id="61dd3-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-377">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-377">Proj 2</span></span></td>
<td><span data-ttu-id="61dd3-378">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-378">Project 2</span></span></td>
<td><span data-ttu-id="61dd3-379">1</span><span class="sxs-lookup"><span data-stu-id="61dd3-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-380">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-381">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-381">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-382">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-382">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-383">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-383">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-384">الوحدات</span><span class="sxs-lookup"><span data-stu-id="61dd3-384">Units</span></span></th>
<th><span data-ttu-id="61dd3-385">المعدل</span><span class="sxs-lookup"><span data-stu-id="61dd3-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-386">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-386">CC001</span></span></td>
<td><span data-ttu-id="61dd3-387">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-387">HR</span></span></td>
<td><span data-ttu-id="61dd3-388">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-388">10001</span></span></td>
<td><span data-ttu-id="61dd3-389">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-389">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-390">1</span><span class="sxs-lookup"><span data-stu-id="61dd3-390">1</span></span></td>
<td><span data-ttu-id="61dd3-391">10</span><span class="sxs-lookup"><span data-stu-id="61dd3-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-392">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="61dd3-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-393">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-393">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-394">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-394">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-395">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-395">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-396">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-396">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-397">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-398">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-398">Proj 1</span></span></td>
<td><span data-ttu-id="61dd3-399">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-399">Project 1</span></span></td>
<td><span data-ttu-id="61dd3-400">3</span><span class="sxs-lookup"><span data-stu-id="61dd3-400">3</span></span></td>
<td><span data-ttu-id="61dd3-401">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-401">10001</span></span></td>
<td><span data-ttu-id="61dd3-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="61dd3-403">30.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-404">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-404">Proj 2</span></span></td>
<td><span data-ttu-id="61dd3-405">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-405">Project 2</span></span></td>
<td><span data-ttu-id="61dd3-406">1</span><span class="sxs-lookup"><span data-stu-id="61dd3-406">1</span></span></td>
<td><span data-ttu-id="61dd3-407">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-407">10001</span></span></td>
<td><span data-ttu-id="61dd3-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="61dd3-409">10.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="61dd3-410">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-411">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-411">Journal</span></span></th>
<th><span data-ttu-id="61dd3-412">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="61dd3-413">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="61dd3-414">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-415">00003</span><span class="sxs-lookup"><span data-stu-id="61dd3-415">00003</span></span></td>
<td><span data-ttu-id="61dd3-416">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="61dd3-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="61dd3-417">مالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-417">Fiscal</span></span></td>
<td><span data-ttu-id="61dd3-418">2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-418">2017</span></span></td>
<td><span data-ttu-id="61dd3-419">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-419">Period 1</span></span></td>
<td><span data-ttu-id="61dd3-420">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="61dd3-421">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="61dd3-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-422">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-423">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-423">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-424">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-425">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-426">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-426">Proj 1</span></span></td>
<td><span data-ttu-id="61dd3-427">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="61dd3-428">3.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-429">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-430">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-430">Proj 2</span></span></td>
<td><span data-ttu-id="61dd3-431">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="61dd3-432">1.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="61dd3-433">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-434">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-435">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-435">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-436">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-436">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-437">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-437">Amount</span></span></th>
<th><span data-ttu-id="61dd3-438">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="61dd3-439">CC0001</span></span></td>
<td><span data-ttu-id="61dd3-440">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-440">HR</span></span></td>
<td><span data-ttu-id="61dd3-441">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-441">10001</span></span></td>
<td><span data-ttu-id="61dd3-442">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-442">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-443">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-443">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-444">-30.00</span></span></td>
<td><span data-ttu-id="61dd3-445">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-446">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-446">Proj 1</span></span></td>
<td><span data-ttu-id="61dd3-447">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="61dd3-448">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-448">10001</span></span></td>
<td><span data-ttu-id="61dd3-449">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-449">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-450">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-450">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-451">30.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-451">30.00</span></span></td>
<td><span data-ttu-id="61dd3-452">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-453">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-453">CC001</span></span></td>
<td><span data-ttu-id="61dd3-454">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-454">HR</span></span></td>
<td><span data-ttu-id="61dd3-455">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-455">10001</span></span></td>
<td><span data-ttu-id="61dd3-456">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-456">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-457">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-457">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-458">-10.00</span></span></td>
<td><span data-ttu-id="61dd3-459">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-460">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-460">Proj 2</span></span></td>
<td><span data-ttu-id="61dd3-461">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="61dd3-462">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-462">10001</span></span></td>
<td><span data-ttu-id="61dd3-463">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-463">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-464">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-464">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-465">10.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-465">10.00</span></span></td>
<td><span data-ttu-id="61dd3-466">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-467">للحصول على معلومات تفصيلية حول سياسة معدل المصروفات الزائدة، راجع سياسة معدل المصروفات الزائدة وأسس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="61dd3-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="61dd3-468">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="61dd3-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="61dd3-469">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="61dd3-470">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="61dd3-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="61dd3-471">يدعم تطبيق Finance and Operations طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="61dd3-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="61dd3-472">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="61dd3-473">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="61dd3-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="61dd3-474">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="61dd3-475">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="61dd3-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="61dd3-476">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="61dd3-477">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="61dd3-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="61dd3-478">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-478">Define the cost allocation</span></span>

<span data-ttu-id="61dd3-479">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="61dd3-480">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="61dd3-481">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="61dd3-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-482">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-482">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-483">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-484">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-484">CC002</span></span></td>
<td><span data-ttu-id="61dd3-485">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-485">Finance</span></span></td>
<td><span data-ttu-id="61dd3-486">35</span><span class="sxs-lookup"><span data-stu-id="61dd3-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-487">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-487">CC003</span></span></td>
<td><span data-ttu-id="61dd3-488">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-488">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-489">55</span><span class="sxs-lookup"><span data-stu-id="61dd3-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-490">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-490">CC004</span></span></td>
<td><span data-ttu-id="61dd3-491">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-491">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-492">10</span><span class="sxs-lookup"><span data-stu-id="61dd3-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-493">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="61dd3-494">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="61dd3-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-495">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-495">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-496">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-497">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-497">CC003</span></span></td>
<td><span data-ttu-id="61dd3-498">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-498">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-499">65</span><span class="sxs-lookup"><span data-stu-id="61dd3-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-500">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-500">CC004</span></span></td>
<td><span data-ttu-id="61dd3-501">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-501">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-502">35</span><span class="sxs-lookup"><span data-stu-id="61dd3-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-503">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="61dd3-504">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="61dd3-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-505">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-505">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-506">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="61dd3-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-507">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-507">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-508">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-508">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-509">60</span><span class="sxs-lookup"><span data-stu-id="61dd3-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-510">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-510">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-511">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-511">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-512">20</span><span class="sxs-lookup"><span data-stu-id="61dd3-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-513">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="61dd3-514">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="61dd3-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-515">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-515">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-516">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="61dd3-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-517">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-517">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-518">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-518">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-519">80</span><span class="sxs-lookup"><span data-stu-id="61dd3-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-520">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-520">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-521">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-521">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-522">15</span><span class="sxs-lookup"><span data-stu-id="61dd3-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-523">**ملاحظة:** في Finance and Operations، بإمكان القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج أن تشتق من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="61dd3-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="61dd3-524">للحصول على معلومات أكثر تفصيلاً حول موفري القياسات الإحصائية، راجع قالب موفر القياسات الإحصائية.</span><span class="sxs-lookup"><span data-stu-id="61dd3-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="61dd3-525">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)‬ يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="61dd3-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-526">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-526">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-527">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-527">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-528">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-528">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-529">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-529">Amount</span></span></th>
<th><span data-ttu-id="61dd3-530">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-531">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-531">CC002</span></span></td>
<td><span data-ttu-id="61dd3-532">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-532">Finance</span></span></td>
<td><span data-ttu-id="61dd3-533">35</span><span class="sxs-lookup"><span data-stu-id="61dd3-533">35</span></span></td>
<td><span data-ttu-id="61dd3-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="61dd3-535">175.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-535">175.00</span></span></td>
<td><span data-ttu-id="61dd3-536">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-537">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-537">CC003</span></span></td>
<td><span data-ttu-id="61dd3-538">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-538">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-539">55</span><span class="sxs-lookup"><span data-stu-id="61dd3-539">55</span></span></td>
<td><span data-ttu-id="61dd3-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="61dd3-541">275.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-541">275.00</span></span></td>
<td><span data-ttu-id="61dd3-542">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-543">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-543">CC004</span></span></td>
<td><span data-ttu-id="61dd3-544">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-544">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-545">10</span><span class="sxs-lookup"><span data-stu-id="61dd3-545">10</span></span></td>
<td><span data-ttu-id="61dd3-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="61dd3-547">50.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-547">50.00</span></span></td>
<td><span data-ttu-id="61dd3-548">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-549">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-549">CC002</span></span></td>
<td><span data-ttu-id="61dd3-550">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-550">Finance</span></span></td>
<td><span data-ttu-id="61dd3-551">35</span><span class="sxs-lookup"><span data-stu-id="61dd3-551">35</span></span></td>
<td><span data-ttu-id="61dd3-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="61dd3-553">436.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-553">436.00</span></span></td>
<td><span data-ttu-id="61dd3-554">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-555">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-555">CC003</span></span></td>
<td><span data-ttu-id="61dd3-556">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-556">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-557">55</span><span class="sxs-lookup"><span data-stu-id="61dd3-557">55</span></span></td>
<td><span data-ttu-id="61dd3-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="61dd3-559">685.14</span><span class="sxs-lookup"><span data-stu-id="61dd3-559">685.14</span></span></td>
<td><span data-ttu-id="61dd3-560">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-561">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-561">CC004</span></span></td>
<td><span data-ttu-id="61dd3-562">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-562">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-563">10</span><span class="sxs-lookup"><span data-stu-id="61dd3-563">10</span></span></td>
<td><span data-ttu-id="61dd3-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="61dd3-565">124.57</span><span class="sxs-lookup"><span data-stu-id="61dd3-565">124.57</span></span></td>
<td><span data-ttu-id="61dd3-566">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-567">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="61dd3-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-568">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-568">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-569">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-569">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-570">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-570">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-571">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-571">Amount</span></span></th>
<th><span data-ttu-id="61dd3-572">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-573">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-573">CC003</span></span></td>
<td><span data-ttu-id="61dd3-574">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-574">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-575">65</span><span class="sxs-lookup"><span data-stu-id="61dd3-575">65</span></span></td>
<td><span data-ttu-id="61dd3-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="61dd3-577">438.75</span><span class="sxs-lookup"><span data-stu-id="61dd3-577">438.75</span></span></td>
<td><span data-ttu-id="61dd3-578">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-579">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-579">CC004</span></span></td>
<td><span data-ttu-id="61dd3-580">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-580">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-581">35</span><span class="sxs-lookup"><span data-stu-id="61dd3-581">35</span></span></td>
<td><span data-ttu-id="61dd3-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="61dd3-583">236.25</span><span class="sxs-lookup"><span data-stu-id="61dd3-583">236.25</span></span></td>
<td><span data-ttu-id="61dd3-584">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-585">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-585">CC003</span></span></td>
<td><span data-ttu-id="61dd3-586">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-586">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-587">65</span><span class="sxs-lookup"><span data-stu-id="61dd3-587">65</span></span></td>
<td><span data-ttu-id="61dd3-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="61dd3-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="61dd3-589">5,297.69</span></span></td>
<td><span data-ttu-id="61dd3-590">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-591">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-591">CC004</span></span></td>
<td><span data-ttu-id="61dd3-592">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-592">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-593">35</span><span class="sxs-lookup"><span data-stu-id="61dd3-593">35</span></span></td>
<td><span data-ttu-id="61dd3-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="61dd3-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="61dd3-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="61dd3-595">2,852.60</span></span></td>
<td><span data-ttu-id="61dd3-596">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-597">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="61dd3-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-598">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-598">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-599">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-599">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-600">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-600">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-601">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-601">Amount</span></span></th>
<th><span data-ttu-id="61dd3-602">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-603">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-603">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-604">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-604">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-605">60</span><span class="sxs-lookup"><span data-stu-id="61dd3-605">60</span></span></td>
<td><span data-ttu-id="61dd3-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="61dd3-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="61dd3-607">535.31</span><span class="sxs-lookup"><span data-stu-id="61dd3-607">535.31</span></span></td>
<td><span data-ttu-id="61dd3-608">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-609">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-609">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-610">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-610">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-611">20</span><span class="sxs-lookup"><span data-stu-id="61dd3-611">20</span></span></td>
<td><span data-ttu-id="61dd3-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="61dd3-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="61dd3-613">178.44</span><span class="sxs-lookup"><span data-stu-id="61dd3-613">178.44</span></span></td>
<td><span data-ttu-id="61dd3-614">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-615">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-615">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-616">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-616">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-617">60</span><span class="sxs-lookup"><span data-stu-id="61dd3-617">60</span></span></td>
<td><span data-ttu-id="61dd3-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="61dd3-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="61dd3-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="61dd3-619">4,487.12</span></span></td>
<td><span data-ttu-id="61dd3-620">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-621">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-621">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-622">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-622">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-623">20</span><span class="sxs-lookup"><span data-stu-id="61dd3-623">20</span></span></td>
<td><span data-ttu-id="61dd3-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="61dd3-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="61dd3-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-625">1,495.71</span></span></td>
<td><span data-ttu-id="61dd3-626">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61dd3-627">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="61dd3-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-628">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-628">Cost object</span></span></th>
<th><span data-ttu-id="61dd3-629">المقدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-629">Magnitude</span></span></th>
<th><span data-ttu-id="61dd3-630">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="61dd3-630">Allocation factor</span></span></th>
<th><span data-ttu-id="61dd3-631">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-631">Amount</span></span></th>
<th><span data-ttu-id="61dd3-632">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-633">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-633">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-634">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-634">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-635">80</span><span class="sxs-lookup"><span data-stu-id="61dd3-635">80</span></span></td>
<td><span data-ttu-id="61dd3-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="61dd3-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="61dd3-637">241.05</span><span class="sxs-lookup"><span data-stu-id="61dd3-637">241.05</span></span></td>
<td><span data-ttu-id="61dd3-638">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-639">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-639">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-640">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-640">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-641">15</span><span class="sxs-lookup"><span data-stu-id="61dd3-641">15</span></span></td>
<td><span data-ttu-id="61dd3-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="61dd3-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="61dd3-643">45.20</span><span class="sxs-lookup"><span data-stu-id="61dd3-643">45.20</span></span></td>
<td><span data-ttu-id="61dd3-644">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-645">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-645">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-646">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-646">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-647">80</span><span class="sxs-lookup"><span data-stu-id="61dd3-647">80</span></span></td>
<td><span data-ttu-id="61dd3-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="61dd3-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="61dd3-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="61dd3-649">2,507.09</span></span></td>
<td><span data-ttu-id="61dd3-650">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-651">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-651">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-652">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-652">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-653">15</span><span class="sxs-lookup"><span data-stu-id="61dd3-653">15</span></span></td>
<td><span data-ttu-id="61dd3-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="61dd3-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="61dd3-655">470.08</span><span class="sxs-lookup"><span data-stu-id="61dd3-655">470.08</span></span></td>
<td><span data-ttu-id="61dd3-656">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="61dd3-657">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="61dd3-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-658">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-658">Journal</span></span></th>
<th><span data-ttu-id="61dd3-659">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="61dd3-660">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="61dd3-661">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="61dd3-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-662">00004</span><span class="sxs-lookup"><span data-stu-id="61dd3-662">00004</span></span></td>
<td><span data-ttu-id="61dd3-663">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="61dd3-664">مالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-664">Fiscal</span></span></td>
<td><span data-ttu-id="61dd3-665">2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-665">2017</span></span></td>
<td><span data-ttu-id="61dd3-666">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-666">Period 1</span></span></td>
<td><span data-ttu-id="61dd3-667">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="61dd3-668">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="61dd3-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61dd3-669">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-670">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-671">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-671">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-672">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-672">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-673">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-674">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-675">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-675">CC001</span></span></td>
<td><span data-ttu-id="61dd3-676">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-676">HR</span></span></td>
<td><span data-ttu-id="61dd3-677">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-677">10001</span></span></td>
<td><span data-ttu-id="61dd3-678">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-678">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-679">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-679">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-680">500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-681">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-682">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-682">CC001</span></span></td>
<td><span data-ttu-id="61dd3-683">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-683">HR</span></span></td>
<td><span data-ttu-id="61dd3-684">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-684">10001</span></span></td>
<td><span data-ttu-id="61dd3-685">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-685">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-686">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-686">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-688">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-689">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-689">CC002</span></span></td>
<td><span data-ttu-id="61dd3-690">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-690">Finance</span></span></td>
<td><span data-ttu-id="61dd3-691">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-691">10001</span></span></td>
<td><span data-ttu-id="61dd3-692">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-692">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-693">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-693">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-694">675.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-695">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-696">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-696">CC002</span></span></td>
<td><span data-ttu-id="61dd3-697">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-697">Finance</span></span></td>
<td><span data-ttu-id="61dd3-698">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-698">10001</span></span></td>
<td><span data-ttu-id="61dd3-699">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-699">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-700">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-700">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="61dd3-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-702">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-703">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-703">CC003</span></span></td>
<td><span data-ttu-id="61dd3-704">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-704">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-705">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-705">10001</span></span></td>
<td><span data-ttu-id="61dd3-706">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-706">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-707">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-707">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-708">713.75</span><span class="sxs-lookup"><span data-stu-id="61dd3-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-709">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-710">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-710">CC003</span></span></td>
<td><span data-ttu-id="61dd3-711">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-711">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-712">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-712">10001</span></span></td>
<td><span data-ttu-id="61dd3-713">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-713">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-714">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-714">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="61dd3-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-716">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-717">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-717">CC003</span></span></td>
<td><span data-ttu-id="61dd3-718">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-718">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-719">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-719">10001</span></span></td>
<td><span data-ttu-id="61dd3-720">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-720">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-721">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-721">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-722">286.25</span><span class="sxs-lookup"><span data-stu-id="61dd3-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-723">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-724">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-724">CC003</span></span></td>
<td><span data-ttu-id="61dd3-725">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-725">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-726">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-726">10001</span></span></td>
<td><span data-ttu-id="61dd3-727">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-727">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-728">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-728">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="61dd3-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-730">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-731">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-731">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-732">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-732">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-733">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-733">10001</span></span></td>
<td><span data-ttu-id="61dd3-734">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-734">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-735">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-735">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-736">776.36</span><span class="sxs-lookup"><span data-stu-id="61dd3-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-737">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-738">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-738">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-739">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-739">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-740">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-740">10001</span></span></td>
<td><span data-ttu-id="61dd3-741">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-741">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-742">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-742">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="61dd3-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-744">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-745">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-745">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-746">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-746">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-747">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-747">10001</span></span></td>
<td><span data-ttu-id="61dd3-748">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-748">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-749">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-749">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-750">223.64</span><span class="sxs-lookup"><span data-stu-id="61dd3-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-751">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="61dd3-752">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-752">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-753">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-753">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-754">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-754">10001</span></span></td>
<td><span data-ttu-id="61dd3-755">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-755">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-756">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-756">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="61dd3-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="61dd3-758">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="61dd3-759">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="61dd3-760">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-760">Cost element</span></span></th>
<th><span data-ttu-id="61dd3-761">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-761">Cost behavior</span></span></th>
<th><span data-ttu-id="61dd3-762">المبلغ</span><span class="sxs-lookup"><span data-stu-id="61dd3-762">Amount</span></span></th>
<th><span data-ttu-id="61dd3-763">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="61dd3-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61dd3-764">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-764">CC001</span></span></td>
<td><span data-ttu-id="61dd3-765">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-765">HR</span></span></td>
<td><span data-ttu-id="61dd3-766">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-766">10001</span></span></td>
<td><span data-ttu-id="61dd3-767">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-767">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-768">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-768">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-769">-500.00</span></span></td>
<td><span data-ttu-id="61dd3-770">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-771">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-771">CC002</span></span></td>
<td><span data-ttu-id="61dd3-772">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-772">Finance</span></span></td>
<td><span data-ttu-id="61dd3-773">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-773">10001</span></span></td>
<td><span data-ttu-id="61dd3-774">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-774">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-775">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-775">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-776">175.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-776">175.00</span></span></td>
<td><span data-ttu-id="61dd3-777">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-778">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-778">CC003</span></span></td>
<td><span data-ttu-id="61dd3-779">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-779">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-780">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-780">10001</span></span></td>
<td><span data-ttu-id="61dd3-781">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-781">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-782">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-782">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-783">275.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-783">275.00</span></span></td>
<td><span data-ttu-id="61dd3-784">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-785">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-785">CC004</span></span></td>
<td><span data-ttu-id="61dd3-786">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-786">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-787">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-787">10001</span></span></td>
<td><span data-ttu-id="61dd3-788">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-788">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-789">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-789">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-790">50,00</span><span class="sxs-lookup"><span data-stu-id="61dd3-790">50,00</span></span></td>
<td><span data-ttu-id="61dd3-791">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-792">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-792">CC001</span></span></td>
<td><span data-ttu-id="61dd3-793">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="61dd3-793">HR</span></span></td>
<td><span data-ttu-id="61dd3-794">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-794">10001</span></span></td>
<td><span data-ttu-id="61dd3-795">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-795">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-796">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-796">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-797">-1,245.71</span></span></td>
<td><span data-ttu-id="61dd3-798">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-799">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-799">CC002</span></span></td>
<td><span data-ttu-id="61dd3-800">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-800">Finance</span></span></td>
<td><span data-ttu-id="61dd3-801">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-801">10001</span></span></td>
<td><span data-ttu-id="61dd3-802">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-802">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-803">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-803">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-804">436.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-804">436.00</span></span></td>
<td><span data-ttu-id="61dd3-805">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-806">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-806">CC003</span></span></td>
<td><span data-ttu-id="61dd3-807">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-807">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-808">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-808">10001</span></span></td>
<td><span data-ttu-id="61dd3-809">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-809">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-810">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-810">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-811">685.14</span><span class="sxs-lookup"><span data-stu-id="61dd3-811">685.14</span></span></td>
<td><span data-ttu-id="61dd3-812">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-813">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-813">CC004</span></span></td>
<td><span data-ttu-id="61dd3-814">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-814">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-815">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-815">10001</span></span></td>
<td><span data-ttu-id="61dd3-816">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-816">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-817">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-817">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-818">124.57</span><span class="sxs-lookup"><span data-stu-id="61dd3-818">124.57</span></span></td>
<td><span data-ttu-id="61dd3-819">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-820">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-820">CC002</span></span></td>
<td><span data-ttu-id="61dd3-821">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-821">Finance</span></span></td>
<td><span data-ttu-id="61dd3-822">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-822">10001</span></span></td>
<td><span data-ttu-id="61dd3-823">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-823">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-824">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-824">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-825">-675.00</span></span></td>
<td><span data-ttu-id="61dd3-826">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-827">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-827">CC003</span></span></td>
<td><span data-ttu-id="61dd3-828">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-828">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-829">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-829">10001</span></span></td>
<td><span data-ttu-id="61dd3-830">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-830">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-831">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-831">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-832">438.75</span><span class="sxs-lookup"><span data-stu-id="61dd3-832">438.75</span></span></td>
<td><span data-ttu-id="61dd3-833">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-834">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-834">CC004</span></span></td>
<td><span data-ttu-id="61dd3-835">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-835">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-836">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-836">10001</span></span></td>
<td><span data-ttu-id="61dd3-837">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-837">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-838">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-838">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-839">236.25</span><span class="sxs-lookup"><span data-stu-id="61dd3-839">236.25</span></span></td>
<td><span data-ttu-id="61dd3-840">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-841">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-841">CC002</span></span></td>
<td><span data-ttu-id="61dd3-842">المالية</span><span class="sxs-lookup"><span data-stu-id="61dd3-842">Finance</span></span></td>
<td><span data-ttu-id="61dd3-843">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-843">10001</span></span></td>
<td><span data-ttu-id="61dd3-844">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-844">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-845">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-845">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="61dd3-846">-8,150.29</span></span></td>
<td><span data-ttu-id="61dd3-847">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-848">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-848">CC003</span></span></td>
<td><span data-ttu-id="61dd3-849">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-849">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-850">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-850">10001</span></span></td>
<td><span data-ttu-id="61dd3-851">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-851">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-852">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-852">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="61dd3-853">5,297.69</span></span></td>
<td><span data-ttu-id="61dd3-854">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-855">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-855">CC004</span></span></td>
<td><span data-ttu-id="61dd3-856">التعبئة</span><span class="sxs-lookup"><span data-stu-id="61dd3-856">Packaging</span></span></td>
<td><span data-ttu-id="61dd3-857">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-857">10001</span></span></td>
<td><span data-ttu-id="61dd3-858">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-858">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-859">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-859">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="61dd3-860">2,852.60</span></span></td>
<td><span data-ttu-id="61dd3-861">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-862">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-862">CC003</span></span></td>
<td><span data-ttu-id="61dd3-863">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-863">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-864">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-864">10001</span></span></td>
<td><span data-ttu-id="61dd3-865">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-865">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-866">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-866">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="61dd3-867">-713.75</span></span></td>
<td><span data-ttu-id="61dd3-868">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-869">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-869">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-870">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-870">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-871">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-871">10001</span></span></td>
<td><span data-ttu-id="61dd3-872">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-872">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-873">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-873">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-874">535.31</span><span class="sxs-lookup"><span data-stu-id="61dd3-874">535.31</span></span></td>
<td><span data-ttu-id="61dd3-875">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-876">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-876">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-877">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-877">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-878">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-878">10001</span></span></td>
<td><span data-ttu-id="61dd3-879">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-879">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-880">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-880">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-881">178.44</span><span class="sxs-lookup"><span data-stu-id="61dd3-881">178.44</span></span></td>
<td><span data-ttu-id="61dd3-882">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-883">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-883">CC003</span></span></td>
<td><span data-ttu-id="61dd3-884">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-884">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-885">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-885">10001</span></span></td>
<td><span data-ttu-id="61dd3-886">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-886">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-887">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-887">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="61dd3-888">-5,982.83</span></span></td>
<td><span data-ttu-id="61dd3-889">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-890">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-890">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-891">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-891">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-892">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-892">10001</span></span></td>
<td><span data-ttu-id="61dd3-893">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-893">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-894">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-894">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="61dd3-895">4,487.12</span></span></td>
<td><span data-ttu-id="61dd3-896">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-897">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-897">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-898">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-898">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-899">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-899">10001</span></span></td>
<td><span data-ttu-id="61dd3-900">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-900">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-901">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-901">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="61dd3-902">1,495.71</span></span></td>
<td><span data-ttu-id="61dd3-903">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-904">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-904">CC003</span></span></td>
<td><span data-ttu-id="61dd3-905">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-905">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-906">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-906">10001</span></span></td>
<td><span data-ttu-id="61dd3-907">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-907">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-908">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-908">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="61dd3-909">-286.25</span></span></td>
<td><span data-ttu-id="61dd3-910">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-911">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-911">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-912">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-912">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-913">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-913">10001</span></span></td>
<td><span data-ttu-id="61dd3-914">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-914">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-915">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-915">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-916">241.05</span><span class="sxs-lookup"><span data-stu-id="61dd3-916">241.05</span></span></td>
<td><span data-ttu-id="61dd3-917">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-918">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-918">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-919">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-919">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-920">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-920">10001</span></span></td>
<td><span data-ttu-id="61dd3-921">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-921">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-922">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-922">Fixed cost</span></span></td>
<td><span data-ttu-id="61dd3-923">45.20</span><span class="sxs-lookup"><span data-stu-id="61dd3-923">45.20</span></span></td>
<td><span data-ttu-id="61dd3-924">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-925">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-925">CC003</span></span></td>
<td><span data-ttu-id="61dd3-926">التجميع</span><span class="sxs-lookup"><span data-stu-id="61dd3-926">Assembly</span></span></td>
<td><span data-ttu-id="61dd3-927">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-927">10001</span></span></td>
<td><span data-ttu-id="61dd3-928">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-928">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-929">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-929">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="61dd3-930">-2,977.17</span></span></td>
<td><span data-ttu-id="61dd3-931">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-932">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-932">Prod 1</span></span></td>
<td><span data-ttu-id="61dd3-933">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-933">Product 1</span></span></td>
<td><span data-ttu-id="61dd3-934">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-934">10001</span></span></td>
<td><span data-ttu-id="61dd3-935">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-935">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-936">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-936">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="61dd3-937">2,507.09</span></span></td>
<td><span data-ttu-id="61dd3-938">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61dd3-939">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-939">Prod 2</span></span></td>
<td><span data-ttu-id="61dd3-940">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-940">Product 2</span></span></td>
<td><span data-ttu-id="61dd3-941">10001</span><span class="sxs-lookup"><span data-stu-id="61dd3-941">10001</span></span></td>
<td><span data-ttu-id="61dd3-942">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-942">Electricity</span></span></td>
<td><span data-ttu-id="61dd3-943">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-943">Variable cost</span></span></td>
<td><span data-ttu-id="61dd3-944">470.08</span><span class="sxs-lookup"><span data-stu-id="61dd3-944">470.08</span></span></td>
<td><span data-ttu-id="61dd3-945">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="61dd3-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="61dd3-946">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="61dd3-946">Conclusion</span></span>
<span data-ttu-id="61dd3-947">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="61dd3-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="61dd3-948">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="61dd3-949">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="61dd3-950">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="61dd3-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="61dd3-951">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="61dd3-952">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="61dd3-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="61dd3-953">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="61dd3-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="61dd3-954">CC099</span><span class="sxs-lookup"><span data-stu-id="61dd3-954">CC099</span></span></th>
<th><span data-ttu-id="61dd3-955">CC001</span><span class="sxs-lookup"><span data-stu-id="61dd3-955">CC001</span></span></th>
<th><span data-ttu-id="61dd3-956">CC002</span><span class="sxs-lookup"><span data-stu-id="61dd3-956">CC002</span></span></th>
<th><span data-ttu-id="61dd3-957">CC003</span><span class="sxs-lookup"><span data-stu-id="61dd3-957">CC003</span></span></th>
<th><span data-ttu-id="61dd3-958">CC004</span><span class="sxs-lookup"><span data-stu-id="61dd3-958">CC004</span></span></th>
<th><span data-ttu-id="61dd3-959">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-959">Proj 1</span></span></th>
<th><span data-ttu-id="61dd3-960">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-960">Proj 2</span></span></th>
<th><span data-ttu-id="61dd3-961">منتج 1</span><span class="sxs-lookup"><span data-stu-id="61dd3-961">Prod 1</span></span></th>
<th><span data-ttu-id="61dd3-962">منتج 2</span><span class="sxs-lookup"><span data-stu-id="61dd3-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="61dd3-963">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="61dd3-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="61dd3-973">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="61dd3-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-974">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="61dd3-975">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="61dd3-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-976">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-977">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-978">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-979">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-980">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-981">776.36</span><span class="sxs-lookup"><span data-stu-id="61dd3-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-982">223.64</span><span class="sxs-lookup"><span data-stu-id="61dd3-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="61dd3-984">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="61dd3-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-985">000</span><span class="sxs-lookup"><span data-stu-id="61dd3-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-986">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-987">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-988">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-989">0.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-990">30.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-991">10.00</span><span class="sxs-lookup"><span data-stu-id="61dd3-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="61dd3-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="61dd3-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="61dd3-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="61dd3-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="61dd3-995">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="61dd3-996">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="61dd3-997">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="61dd3-998">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="61dd3-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="61dd3-999">لمزيد من المعلومات المفصلة، انظر سياسة زيادة التكاليف‬.</span><span class="sxs-lookup"><span data-stu-id="61dd3-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="61dd3-1000">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="61dd3-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




