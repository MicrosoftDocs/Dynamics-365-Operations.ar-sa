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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="072e5-103">عملية حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="072e5-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="072e5-104">يصف هذا الموضوع العمليات الأساسية لحساب المصروفات الزائدة وتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="072e5-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="072e5-105">تعريف المصطلح</span><span class="sxs-lookup"><span data-stu-id="072e5-105">Term definition</span></span>
---------------

<span data-ttu-id="072e5-106">المصروفات الزائدة هي المصروفات التي يتم تكبدها لإدارة شركة ما، ولكن لا يمكن عزوها إلى أي نشاط أو منتج أو خدمة معينة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="072e5-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="072e5-107">توفر المصروفات الزائدة الدعم الحساس لتوليد أنشطة تحقيق الأرباح.</span><span class="sxs-lookup"><span data-stu-id="072e5-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="072e5-108">فيما يلي بعض الأمثلة على تكاليف المصاريف الإضافية:</span><span class="sxs-lookup"><span data-stu-id="072e5-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="072e5-109">الإيجار</span><span class="sxs-lookup"><span data-stu-id="072e5-109">Rent</span></span>
-   <span data-ttu-id="072e5-110">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-110">Electricity</span></span>
-   <span data-ttu-id="072e5-111">الرواتب الإدارية</span><span class="sxs-lookup"><span data-stu-id="072e5-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="072e5-112">نظرة عامة على حساب المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="072e5-112">Overhead calculation overview</span></span>
<span data-ttu-id="072e5-113">تقوم عملية حساب المصروفات الزائدة بتشغيل سياسات محاسبة التكاليف بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="072e5-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="072e5-114">ويمكنك تشغيل عملية حساب المصروفات الزائدة عدة مرات لنفس الفترة المالية إذا طرأ تغيير على سياسات محاسبة التكاليف أو تم اكتشاف أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="072e5-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="072e5-115">يتم تخزين كل عملية من عمليات حساب المصروفات الزائدة وتتلقى معرف إصدار فريدًا يسمح لك بالمقارنة بين العمليات الحسابية في الإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="072e5-116">وتتلقى إدخالات التكلفة التي تنشأ نتيجة عملية حساب المصروفات الزائدة تاريخًا محاسبيًا.</span><span class="sxs-lookup"><span data-stu-id="072e5-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="072e5-117">ويتطابق هذا التاريخ المحاسبي مع تاريخ انتهاء للفترة المالية المستخدمة في العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="072e5-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="072e5-118">يتكون معرف الإصدار الفريد من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="072e5-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="072e5-119">نوع الإصدار</span><span class="sxs-lookup"><span data-stu-id="072e5-119">Version type</span></span>
-   <span data-ttu-id="072e5-120">التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="072e5-120">Date and time</span></span>
-   <span data-ttu-id="072e5-121">دفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="072e5-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="072e5-122">السنة المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-122">Fiscal year</span></span>
-   <span data-ttu-id="072e5-123">الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-123">Fiscal period</span></span>

<span data-ttu-id="072e5-124">يتم تشغيل حساب المصروفات الزائدة بشكل مستقل عن الإصدار.</span><span class="sxs-lookup"><span data-stu-id="072e5-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="072e5-125">لذلك، يمكنك حساب إصدار الموازنة قبل الإصدار الفعلي.</span><span class="sxs-lookup"><span data-stu-id="072e5-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="072e5-126">تتكون عملية حساب المصروفات الزائدة من أربع خطوات، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="072e5-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="072e5-127">في كل خطوة، يتم إنشاء رأس دفتر يومية يحتوي على إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="072e5-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="072e5-128">ويحتفظ رأس دفتر اليومية هذا بإدخال البيانات لكل خطوة من العملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="072e5-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="072e5-129">يتم تطبيق السياسات والقواعد على كل بند دفتر اليومية، ويتم إنشاء إدخالات التكلفة كمخرجات.</span><span class="sxs-lookup"><span data-stu-id="072e5-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="072e5-130">وبالتالي، ستكون لديك إمكانية تعقب كاملة في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="072e5-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="072e5-131">[![عملية حساب المصروفات الزائدة](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="072e5-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="072e5-132">حساب المصروفات الزائدة الخاصة بالكهرباء وتخصيصها</span><span class="sxs-lookup"><span data-stu-id="072e5-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="072e5-133">في المحاسبة المالية، يتم تسجيل بعض التكاليف، مثل الكهرباء، كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="072e5-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="072e5-134">وبالتالي، لا يتم توفير معلومات تفصيلية إدارية لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="072e5-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="072e5-135">في محاسبة التكاليف، لتوفير معلومات الإدارية الصحيحة عبر كافة الوحدات والمستويات التنظيمية، يجب أن تتدفق التكاليف عبر الوحدات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="072e5-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="072e5-136">يجب أن يعتمد هذا التدفق على بتسجيل دقيق للاستهلاك أو تقدير مناسب.</span><span class="sxs-lookup"><span data-stu-id="072e5-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="072e5-137">في دفتر الأستاذ العام، يمكن ترحيل تكلفة الكهرباء كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="072e5-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-138">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-139">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-140">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="072e5-140">Main account</span></span></th>
<th><span data-ttu-id="072e5-141">المبلغ بعملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="072e5-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-142">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="072e5-143">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-143">CC099</span></span></td>
<td><span data-ttu-id="072e5-144">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-144">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-145">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-145">10001</span></span></td>
<td><span data-ttu-id="072e5-146">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-146">Electricity</span></span></td>
<td><span data-ttu-id="072e5-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="072e5-148">الخطوة 1: معالجة حساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="072e5-149">بشكل افتراضي، عندما يتم استيراد إدخالات التكلفة من البيانات المصدر، تظهر **غير مصنف‬ة** في تصنيف سلوك التكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="072e5-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="072e5-150">من خلال تطبيق قواعد سياسة سلوك التكلفة، يمكنك إعادة تصنيف إدخالات التكلفة على أنها **تكلفة ثابتة** أو **تكلفة متغيرة**.</span><span class="sxs-lookup"><span data-stu-id="072e5-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="072e5-151">تعريف قاعدة سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-151">Define the cost behavior rule</span></span>

<span data-ttu-id="072e5-152">في بعض الحالات، يكون جزء من التكلفة عبارة عن رسوم ثابتة فيما تستند التكلفة المتبقية إلى الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="072e5-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="072e5-153">غالبًا ما تطابق فواتير الكهرباء هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="072e5-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="072e5-154">بعد دفع رسوم ثابتة معينة، تدفع رسومًا في مقابل استهلاك الكيلووات في الساعة (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="072e5-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="072e5-155">على سبيل المثال، إذا كانت قيمة رسوم التكلفة الثابتة 1,000.00، فإليك كيفية تعريف قاعدة سلوك التكلفة:</span><span class="sxs-lookup"><span data-stu-id="072e5-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="072e5-156">المبلغ الثابت 1,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="072e5-157">0 &lt;= 1,000.00 = ثابت</span><span class="sxs-lookup"><span data-stu-id="072e5-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="072e5-158">1000,01 &lt; N = متغير</span><span class="sxs-lookup"><span data-stu-id="072e5-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="072e5-159">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-160">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-160">Journal</span></span></th>
<th><span data-ttu-id="072e5-161">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="072e5-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="072e5-162">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="072e5-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="072e5-163">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="072e5-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-164">00001</span><span class="sxs-lookup"><span data-stu-id="072e5-164">00001</span></span></td>
<td><span data-ttu-id="072e5-165">دفتر اليومية لحساب سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="072e5-166">مالي</span><span class="sxs-lookup"><span data-stu-id="072e5-166">Fiscal</span></span></td>
<td><span data-ttu-id="072e5-167">2017</span><span class="sxs-lookup"><span data-stu-id="072e5-167">2017</span></span></td>
<td><span data-ttu-id="072e5-168">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-168">Period 1</span></span></td>
<td><span data-ttu-id="072e5-169">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="072e5-170">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="072e5-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-171">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-172">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-173">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-173">Cost element</span></span></th>
<th><span data-ttu-id="072e5-174">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-174">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-175">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-176">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="072e5-177">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-177">CC099</span></span></td>
<td><span data-ttu-id="072e5-178">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-178">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-179">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-179">10001</span></span></td>
<td><span data-ttu-id="072e5-180">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-180">Electricity</span></span></td>
<td><span data-ttu-id="072e5-181">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="072e5-181">Unclassified</span></span></td>
<td><span data-ttu-id="072e5-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="072e5-183">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-184">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-185">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-185">Cost element</span></span></th>
<th><span data-ttu-id="072e5-186">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-186">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-187">Amount</span></span></th>
<th><span data-ttu-id="072e5-188">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-189">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-189">CC099</span></span></td>
<td><span data-ttu-id="072e5-190">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-190">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-191">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-191">10001</span></span></td>
<td><span data-ttu-id="072e5-192">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-192">Electricity</span></span></td>
<td><span data-ttu-id="072e5-193">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="072e5-193">Unclassified</span></span></td>
<td><span data-ttu-id="072e5-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-194">10,000.00</span></span></td>
<td><span data-ttu-id="072e5-195">3 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-196">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-196">CC099</span></span></td>
<td><span data-ttu-id="072e5-197">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-197">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-198">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-198">10001</span></span></td>
<td><span data-ttu-id="072e5-199">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-199">Electricity</span></span></td>
<td><span data-ttu-id="072e5-200">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="072e5-200">Unclassified</span></span></td>
<td><span data-ttu-id="072e5-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-201">-10,000.00</span></span></td>
<td><span data-ttu-id="072e5-202">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-203">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-203">CC099</span></span></td>
<td><span data-ttu-id="072e5-204">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-204">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-205">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-205">10001</span></span></td>
<td><span data-ttu-id="072e5-206">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-206">Electricity</span></span></td>
<td><span data-ttu-id="072e5-207">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-207">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-208">1000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-208">1,000.00</span></span></td>
<td><span data-ttu-id="072e5-209">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-210">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-210">CC099</span></span></td>
<td><span data-ttu-id="072e5-211">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-211">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-212">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-212">10001</span></span></td>
<td><span data-ttu-id="072e5-213">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-213">Electricity</span></span></td>
<td><span data-ttu-id="072e5-214">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-214">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-215">9,000.00</span></span></td>
<td><span data-ttu-id="072e5-216">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-217">للحصول على معلومات تفصيلية حول سلوك التكلفة، راجع سياسة سلوك التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="072e5-218">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="072e5-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="072e5-219">الخطوة 2: معالجة حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="072e5-220">يتم استخدام توزيع التكلفة لإعادة توزيع التكلفة من كائن تكلفة واحد إلى كائن تكلفة واحد أو أكثر عن طريق تطبيق أساس توزيع ذي صلة.</span><span class="sxs-lookup"><span data-stu-id="072e5-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="072e5-221">هناك اختلاف بين توزيع التكلفة وتخصيص التكلفة، حيث يحدث توزيع التكلفة دائمًا على مستوى عنصر التكلفة الأساسية‬‏‫ للتكلفة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="072e5-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="072e5-222">تعريف قاعدة توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-222">Define the cost distribution rule</span></span>

<span data-ttu-id="072e5-223">في المحاسبة المالية، يتم تسجيل تكاليف الكهرباء في أغلب الأحيان كمبلغ إجمالي.</span><span class="sxs-lookup"><span data-stu-id="072e5-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="072e5-224">في محاسبة التكاليف، لا يعتبر هذا الأسلوب مفصلاً بشكل كافٍ.</span><span class="sxs-lookup"><span data-stu-id="072e5-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="072e5-225">يجب توزيع التكلفة المتغيرة على كائنات التكلفة الفردية على أساس مناسب.</span><span class="sxs-lookup"><span data-stu-id="072e5-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="072e5-226">يُعتبر أساس التخصيص الأكثر منطقية استهلاك الكهرباء (كيلووات في الساعة).</span><span class="sxs-lookup"><span data-stu-id="072e5-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="072e5-227">يتم إنشاء عضو بُعد إحصائي يسمى الكهرباء، ويتم تسجيل استهلاك الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="072e5-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="072e5-228">بشكل افتراضي، يتوفر كافة أعضاء الأبعاد الإحصائية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="072e5-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-229">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-229">Cost object</span></span></th>
<th><span data-ttu-id="072e5-230">كيلووات في الساعة</span><span class="sxs-lookup"><span data-stu-id="072e5-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-231">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-231">CC001</span></span></td>
<td><span data-ttu-id="072e5-232">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-232">HR</span></span></td>
<td><span data-ttu-id="072e5-233">1,000</span><span class="sxs-lookup"><span data-stu-id="072e5-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-234">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-234">CC002</span></span></td>
<td><span data-ttu-id="072e5-235">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-235">Finance</span></span></td>
<td><span data-ttu-id="072e5-236">6,000</span><span class="sxs-lookup"><span data-stu-id="072e5-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-237">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-237">CC003</span></span></td>
<td><span data-ttu-id="072e5-238">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-238">Assembly</span></span></td>
<td><span data-ttu-id="072e5-239">0</span><span class="sxs-lookup"><span data-stu-id="072e5-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-240">يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="072e5-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-241">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-241">Cost object</span></span></th>
<th><span data-ttu-id="072e5-242">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-242">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-243">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-243">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-244">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-245">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-245">CC001</span></span></td>
<td><span data-ttu-id="072e5-246">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-246">HR</span></span></td>
<td><span data-ttu-id="072e5-247">1,000</span><span class="sxs-lookup"><span data-stu-id="072e5-247">1,000</span></span></td>
<td><span data-ttu-id="072e5-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="072e5-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="072e5-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-250">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-250">CC002</span></span></td>
<td><span data-ttu-id="072e5-251">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-251">Finance</span></span></td>
<td><span data-ttu-id="072e5-252">6,000</span><span class="sxs-lookup"><span data-stu-id="072e5-252">6,000</span></span></td>
<td><span data-ttu-id="072e5-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="072e5-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="072e5-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-255">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-255">CC003</span></span></td>
<td><span data-ttu-id="072e5-256">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-256">Assembly</span></span></td>
<td><span data-ttu-id="072e5-257">0</span><span class="sxs-lookup"><span data-stu-id="072e5-257">0</span></span></td>
<td><span data-ttu-id="072e5-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="072e5-259">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-260">يجب توزيع التكلفة الثابتة بالتساوي على كائنات التكلفة الفردية التي استهلكت الكهرباء.</span><span class="sxs-lookup"><span data-stu-id="072e5-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="072e5-261">يمكن تحقيق هذه النتيجة باستخدام عضو البُعد الإحصائي الكهرباء في أساس توزيع صيغة: (الكهرباء &gt; 0.00) يعرض الجدول التالي النتيجة عند تطبيق استهلاك الكهرباء كأساس توزيع الأساسية للتكاليف المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="072e5-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-262">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-262">Cost object</span></span></th>
<th><span data-ttu-id="072e5-263">المعادلة</span><span class="sxs-lookup"><span data-stu-id="072e5-263">Formula</span></span></th>
<th><span data-ttu-id="072e5-264">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-264">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-265">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-265">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-266">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-267">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-267">CC001</span></span></td>
<td><span data-ttu-id="072e5-268">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-268">HR</span></span></td>
<td><span data-ttu-id="072e5-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="072e5-270">1</span><span class="sxs-lookup"><span data-stu-id="072e5-270">1</span></span></td>
<td><span data-ttu-id="072e5-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="072e5-272">500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-273">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-273">CC002</span></span></td>
<td><span data-ttu-id="072e5-274">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-274">Finance</span></span></td>
<td><span data-ttu-id="072e5-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="072e5-276">1</span><span class="sxs-lookup"><span data-stu-id="072e5-276">1</span></span></td>
<td><span data-ttu-id="072e5-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="072e5-278">500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-279">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-279">CC003</span></span></td>
<td><span data-ttu-id="072e5-280">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-280">Assembly</span></span></td>
<td><span data-ttu-id="072e5-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="072e5-282">0</span><span class="sxs-lookup"><span data-stu-id="072e5-282">0</span></span></td>
<td><span data-ttu-id="072e5-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="072e5-284">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="072e5-285">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-286">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-286">Journal</span></span></th>
<th><span data-ttu-id="072e5-287">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="072e5-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="072e5-288">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="072e5-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="072e5-289">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="072e5-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-290">00002</span><span class="sxs-lookup"><span data-stu-id="072e5-290">00002</span></span></td>
<td><span data-ttu-id="072e5-291">دفتر يومية حساب توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="072e5-292">مالي</span><span class="sxs-lookup"><span data-stu-id="072e5-292">Fiscal</span></span></td>
<td><span data-ttu-id="072e5-293">2017</span><span class="sxs-lookup"><span data-stu-id="072e5-293">2017</span></span></td>
<td><span data-ttu-id="072e5-294">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-294">Period 1</span></span></td>
<td><span data-ttu-id="072e5-295">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="072e5-296">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="072e5-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-297">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-298">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-299">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-299">Cost element</span></span></th>
<th><span data-ttu-id="072e5-300">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-300">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-301">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-302">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-303">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-303">CC099</span></span></td>
<td><span data-ttu-id="072e5-304">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-304">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-305">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-305">10001</span></span></td>
<td><span data-ttu-id="072e5-306">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-306">Electricity</span></span></td>
<td><span data-ttu-id="072e5-307">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-307">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-308">1000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-309">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-310">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-310">CC099</span></span></td>
<td><span data-ttu-id="072e5-311">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-311">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-312">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-312">10001</span></span></td>
<td><span data-ttu-id="072e5-313">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-313">Electricity</span></span></td>
<td><span data-ttu-id="072e5-314">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-314">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="072e5-316">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-317">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-318">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-318">Cost element</span></span></th>
<th><span data-ttu-id="072e5-319">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-319">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-320">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-320">Amount</span></span></th>
<th><span data-ttu-id="072e5-321">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-322">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-322">CC099</span></span></td>
<td><span data-ttu-id="072e5-323">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-323">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-324">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-324">10001</span></span></td>
<td><span data-ttu-id="072e5-325">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-325">Electricity</span></span></td>
<td><span data-ttu-id="072e5-326">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-326">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-327">-1000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-327">-1,000.00</span></span></td>
<td><span data-ttu-id="072e5-328">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-329">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-329">CC001</span></span></td>
<td><span data-ttu-id="072e5-330">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-330">HR</span></span></td>
<td><span data-ttu-id="072e5-331">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-331">10001</span></span></td>
<td><span data-ttu-id="072e5-332">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-332">Electricity</span></span></td>
<td><span data-ttu-id="072e5-333">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-333">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-334">500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-334">500.00</span></span></td>
<td><span data-ttu-id="072e5-335">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-336">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-336">CC002</span></span></td>
<td><span data-ttu-id="072e5-337">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-337">Finance</span></span></td>
<td><span data-ttu-id="072e5-338">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-338">10001</span></span></td>
<td><span data-ttu-id="072e5-339">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-339">Electricity</span></span></td>
<td><span data-ttu-id="072e5-340">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-340">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-341">500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-341">500.00</span></span></td>
<td><span data-ttu-id="072e5-342">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-343">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-343">CC099</span></span></td>
<td><span data-ttu-id="072e5-344">مركز التكلفة الافتراضي</span><span class="sxs-lookup"><span data-stu-id="072e5-344">Default cost center</span></span></td>
<td><span data-ttu-id="072e5-345">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-345">10001</span></span></td>
<td><span data-ttu-id="072e5-346">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-346">Electricity</span></span></td>
<td><span data-ttu-id="072e5-347">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-347">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="072e5-348">-9,000.00</span></span></td>
<td><span data-ttu-id="072e5-349">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-350">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-350">CC001</span></span></td>
<td><span data-ttu-id="072e5-351">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-351">HR</span></span></td>
<td><span data-ttu-id="072e5-352">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-352">10001</span></span></td>
<td><span data-ttu-id="072e5-353">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-353">Electricity</span></span></td>
<td><span data-ttu-id="072e5-354">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-354">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="072e5-355">1,285.71</span></span></td>
<td><span data-ttu-id="072e5-356">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-357">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-357">CC002</span></span></td>
<td><span data-ttu-id="072e5-358">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-358">Finance</span></span></td>
<td><span data-ttu-id="072e5-359">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-359">10001</span></span></td>
<td><span data-ttu-id="072e5-360">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-360">Electricity</span></span></td>
<td><span data-ttu-id="072e5-361">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-361">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="072e5-362">7,714.29</span></span></td>
<td><span data-ttu-id="072e5-363">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-364">للحصول على معلومات تفصيلية حول توزيع التكلفة وأسس التوزيع، راجع سياسة توزيع التكلفة وأسس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="072e5-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="072e5-365">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="072e5-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="072e5-366">الخطوة 3: معالجة حساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="072e5-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="072e5-367">يتم استخدام معدل المصروفات الزائدة لتحميل التكاليف لكائن تكلفة محدد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="072e5-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="072e5-368">تستند التكلفة إلى معدل تكلفة محدد مسبقًا والمقدار من أساس التوزيع المعين.</span><span class="sxs-lookup"><span data-stu-id="072e5-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="072e5-369">تحديد معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="072e5-369">Define the overhead rate</span></span>

<span data-ttu-id="072e5-370">يساهم كائن التكلفة CC001 الموارد البشرية في مجموعة من المشاريع الداخلية.</span><span class="sxs-lookup"><span data-stu-id="072e5-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="072e5-371">يتم إنشاء عضو بُعد إحصائي يعرف باسم مشاريع الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="072e5-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-372">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-372">Cost object</span></span></th>
<th><span data-ttu-id="072e5-373">الساعات</span><span class="sxs-lookup"><span data-stu-id="072e5-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-374">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-374">Proj 1</span></span></td>
<td><span data-ttu-id="072e5-375">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-375">Project 1</span></span></td>
<td><span data-ttu-id="072e5-376">3</span><span class="sxs-lookup"><span data-stu-id="072e5-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-377">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-377">Proj 2</span></span></td>
<td><span data-ttu-id="072e5-378">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-378">Project 2</span></span></td>
<td><span data-ttu-id="072e5-379">1</span><span class="sxs-lookup"><span data-stu-id="072e5-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-380">تم تعريف معدل تكلفة محدد مسبقًا للمساهمة في مشاريع التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-381">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-381">Cost object</span></span></th>
<th><span data-ttu-id="072e5-382">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-382">Cost element</span></span></th>
<th><span data-ttu-id="072e5-383">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-383">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-384">الوحدات</span><span class="sxs-lookup"><span data-stu-id="072e5-384">Units</span></span></th>
<th><span data-ttu-id="072e5-385">المعدل</span><span class="sxs-lookup"><span data-stu-id="072e5-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-386">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-386">CC001</span></span></td>
<td><span data-ttu-id="072e5-387">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-387">HR</span></span></td>
<td><span data-ttu-id="072e5-388">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-388">10001</span></span></td>
<td><span data-ttu-id="072e5-389">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-389">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-390">1</span><span class="sxs-lookup"><span data-stu-id="072e5-390">1</span></span></td>
<td><span data-ttu-id="072e5-391">10</span><span class="sxs-lookup"><span data-stu-id="072e5-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-392">يُظهر الجدول التالي النتيجة عند تطبيق مشاريع الموارد البشرية كأساس توزيع.</span><span class="sxs-lookup"><span data-stu-id="072e5-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-393">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-393">Cost object</span></span></th>
<th><span data-ttu-id="072e5-394">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-394">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-395">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-395">Cost element</span></span></th>
<th><span data-ttu-id="072e5-396">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-396">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-397">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-398">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-398">Proj 1</span></span></td>
<td><span data-ttu-id="072e5-399">المشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-399">Project 1</span></span></td>
<td><span data-ttu-id="072e5-400">3</span><span class="sxs-lookup"><span data-stu-id="072e5-400">3</span></span></td>
<td><span data-ttu-id="072e5-401">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-401">10001</span></span></td>
<td><span data-ttu-id="072e5-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="072e5-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="072e5-403">30.00</span><span class="sxs-lookup"><span data-stu-id="072e5-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-404">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-404">Proj 2</span></span></td>
<td><span data-ttu-id="072e5-405">المشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-405">Project 2</span></span></td>
<td><span data-ttu-id="072e5-406">1</span><span class="sxs-lookup"><span data-stu-id="072e5-406">1</span></span></td>
<td><span data-ttu-id="072e5-407">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-407">10001</span></span></td>
<td><span data-ttu-id="072e5-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="072e5-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="072e5-409">10.00</span><span class="sxs-lookup"><span data-stu-id="072e5-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="072e5-410">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-411">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-411">Journal</span></span></th>
<th><span data-ttu-id="072e5-412">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="072e5-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="072e5-413">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="072e5-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="072e5-414">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="072e5-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-415">00003</span><span class="sxs-lookup"><span data-stu-id="072e5-415">00003</span></span></td>
<td><span data-ttu-id="072e5-416">دفتر اليومية لحساب معدل المصروفات الزائدة</span><span class="sxs-lookup"><span data-stu-id="072e5-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="072e5-417">مالي</span><span class="sxs-lookup"><span data-stu-id="072e5-417">Fiscal</span></span></td>
<td><span data-ttu-id="072e5-418">2017</span><span class="sxs-lookup"><span data-stu-id="072e5-418">2017</span></span></td>
<td><span data-ttu-id="072e5-419">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-419">Period 1</span></span></td>
<td><span data-ttu-id="072e5-420">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="072e5-421">إدخالات دفتر اليومية (إدخالات دفتر اليومية لحساب معدل المصروفات الزائدة)</span><span class="sxs-lookup"><span data-stu-id="072e5-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-422">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-423">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-423">Cost object</span></span></th>
<th><span data-ttu-id="072e5-424">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-425">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-426">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-426">Proj 1</span></span></td>
<td><span data-ttu-id="072e5-427">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="072e5-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="072e5-428">3.00</span><span class="sxs-lookup"><span data-stu-id="072e5-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-429">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-430">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-430">Proj 2</span></span></td>
<td><span data-ttu-id="072e5-431">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="072e5-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="072e5-432">1.00</span><span class="sxs-lookup"><span data-stu-id="072e5-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="072e5-433">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-434">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-435">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-435">Cost element</span></span></th>
<th><span data-ttu-id="072e5-436">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-436">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-437">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-437">Amount</span></span></th>
<th><span data-ttu-id="072e5-438">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="072e5-439">CC0001</span></span></td>
<td><span data-ttu-id="072e5-440">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-440">HR</span></span></td>
<td><span data-ttu-id="072e5-441">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-441">10001</span></span></td>
<td><span data-ttu-id="072e5-442">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-442">Electricity</span></span></td>
<td><span data-ttu-id="072e5-443">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-443">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="072e5-444">-30.00</span></span></td>
<td><span data-ttu-id="072e5-445">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-446">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-446">Proj 1</span></span></td>
<td><span data-ttu-id="072e5-447">مشروع داخلي 1</span><span class="sxs-lookup"><span data-stu-id="072e5-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="072e5-448">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-448">10001</span></span></td>
<td><span data-ttu-id="072e5-449">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-449">Electricity</span></span></td>
<td><span data-ttu-id="072e5-450">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-450">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-451">30.00</span><span class="sxs-lookup"><span data-stu-id="072e5-451">30.00</span></span></td>
<td><span data-ttu-id="072e5-452">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-453">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-453">CC001</span></span></td>
<td><span data-ttu-id="072e5-454">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-454">HR</span></span></td>
<td><span data-ttu-id="072e5-455">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-455">10001</span></span></td>
<td><span data-ttu-id="072e5-456">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-456">Electricity</span></span></td>
<td><span data-ttu-id="072e5-457">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-457">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="072e5-458">-10.00</span></span></td>
<td><span data-ttu-id="072e5-459">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-460">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-460">Proj 2</span></span></td>
<td><span data-ttu-id="072e5-461">مشروع داخلي 2</span><span class="sxs-lookup"><span data-stu-id="072e5-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="072e5-462">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-462">10001</span></span></td>
<td><span data-ttu-id="072e5-463">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-463">Electricity</span></span></td>
<td><span data-ttu-id="072e5-464">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-464">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-465">10.00</span><span class="sxs-lookup"><span data-stu-id="072e5-465">10.00</span></span></td>
<td><span data-ttu-id="072e5-466">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-467">للحصول على معلومات تفصيلية حول سياسة معدل المصروفات الزائدة، راجع سياسة معدل المصروفات الزائدة وأسس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="072e5-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="072e5-468">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="072e5-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="072e5-469">الخطوة 4: معالجة حساب تخصيص التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="072e5-470">يُستخدم التخصيص لتخصيص رصيد كائن التكلفة إلى كائنات تكلفة أخرى عن طريق تطبيق أساس التوزيع.</span><span class="sxs-lookup"><span data-stu-id="072e5-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="072e5-471">يدعم تطبيق Finance and Operations طريقة التوزيع المتبادل.</span><span class="sxs-lookup"><span data-stu-id="072e5-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="072e5-472">في أسلوب التخصيص المتبادل، يتم التعرّف بشكل كامل على الخدمات المتبادلة التي تتبادلها كائنات التكلفة المساعدة.</span><span class="sxs-lookup"><span data-stu-id="072e5-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="072e5-473">يحدد النظام بشكل تلقائي الترتيب الصحيح لتنفيذ عمليات التخصيص فيه.</span><span class="sxs-lookup"><span data-stu-id="072e5-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="072e5-474">يتم تخصيص الرصيد الخاص بكائن التكلفة بواسطة أساس توزيع فردي.</span><span class="sxs-lookup"><span data-stu-id="072e5-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="072e5-475">يتم دعم عمليات التخصيص عبر أبعاد كائنات التكلفة وأعضائها.</span><span class="sxs-lookup"><span data-stu-id="072e5-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="072e5-476">يتم التحكم بترتيب التخصيص بواسطة وحدة التحكم في التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="072e5-477">[![الأسلوب المتبادل](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="072e5-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="072e5-478">تعريف توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-478">Define the cost allocation</span></span>

<span data-ttu-id="072e5-479">فيما يلي مثال بسيط يشرح كيف يمكن تتبع تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="072e5-480">يساهم كائن التكلفة CC001 الموارد البشرية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="072e5-481">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات الموارد البشرية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="072e5-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-482">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-482">Cost object</span></span></th>
<th><span data-ttu-id="072e5-483">خدمات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-484">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-484">CC002</span></span></td>
<td><span data-ttu-id="072e5-485">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-485">Finance</span></span></td>
<td><span data-ttu-id="072e5-486">35</span><span class="sxs-lookup"><span data-stu-id="072e5-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-487">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-487">CC003</span></span></td>
<td><span data-ttu-id="072e5-488">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-488">Assembly</span></span></td>
<td><span data-ttu-id="072e5-489">55</span><span class="sxs-lookup"><span data-stu-id="072e5-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-490">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-490">CC004</span></span></td>
<td><span data-ttu-id="072e5-491">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-491">Packaging</span></span></td>
<td><span data-ttu-id="072e5-492">10</span><span class="sxs-lookup"><span data-stu-id="072e5-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-493">يساهم كائن التكلفة CC002 المالية في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="072e5-494">يتم إنشاء عضو بُعد إحصائي يعرف باسم الخدمات المالية لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="072e5-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-495">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-495">Cost object</span></span></th>
<th><span data-ttu-id="072e5-496">الخدمات المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-497">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-497">CC003</span></span></td>
<td><span data-ttu-id="072e5-498">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-498">Assembly</span></span></td>
<td><span data-ttu-id="072e5-499">65</span><span class="sxs-lookup"><span data-stu-id="072e5-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-500">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-500">CC004</span></span></td>
<td><span data-ttu-id="072e5-501">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-501">Packaging</span></span></td>
<td><span data-ttu-id="072e5-502">35</span><span class="sxs-lookup"><span data-stu-id="072e5-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-503">يساهم كائن التكلفة CC003 التجميع في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="072e5-504">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التجميع‬ لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="072e5-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-505">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-505">Cost object</span></span></th>
<th><span data-ttu-id="072e5-506">خدمات التجميع (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="072e5-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-507">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-507">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-508">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-508">Product 1</span></span></td>
<td><span data-ttu-id="072e5-509">60</span><span class="sxs-lookup"><span data-stu-id="072e5-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-510">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-510">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-511">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-511">Product 2</span></span></td>
<td><span data-ttu-id="072e5-512">20</span><span class="sxs-lookup"><span data-stu-id="072e5-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-513">يساهم كائن التكلفة CC004 التعبئة في عدة كائنات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="072e5-514">يتم إنشاء عضو بُعد إحصائي يعرف باسم خدمات التعبئة لقياس المقدار المستهلك.</span><span class="sxs-lookup"><span data-stu-id="072e5-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-515">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-515">Cost object</span></span></th>
<th><span data-ttu-id="072e5-516">خدمات التعبئة (بالساعات)</span><span class="sxs-lookup"><span data-stu-id="072e5-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-517">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-517">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-518">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-518">Product 1</span></span></td>
<td><span data-ttu-id="072e5-519">80</span><span class="sxs-lookup"><span data-stu-id="072e5-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-520">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-520">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-521">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-521">Product 2</span></span></td>
<td><span data-ttu-id="072e5-522">15</span><span class="sxs-lookup"><span data-stu-id="072e5-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-523">**ملاحظة:** في Finance and Operations، بإمكان القياسات الإحصائية مثل ساعات الإنتاج التي يستهلكها المنتج أن تشتق من البيانات المصدر.</span><span class="sxs-lookup"><span data-stu-id="072e5-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="072e5-524">للحصول على معلومات أكثر تفصيلاً حول موفري القياسات الإحصائية، راجع قالب موفر القياسات الإحصائية.</span><span class="sxs-lookup"><span data-stu-id="072e5-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="072e5-525">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)‬ يعرض الجدول التالي النتيجة عند تطبيق خدمات الموارد البشرية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="072e5-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-526">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-526">Cost object</span></span></th>
<th><span data-ttu-id="072e5-527">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-527">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-528">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-528">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-529">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-529">Amount</span></span></th>
<th><span data-ttu-id="072e5-530">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-531">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-531">CC002</span></span></td>
<td><span data-ttu-id="072e5-532">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-532">Finance</span></span></td>
<td><span data-ttu-id="072e5-533">35</span><span class="sxs-lookup"><span data-stu-id="072e5-533">35</span></span></td>
<td><span data-ttu-id="072e5-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="072e5-535">175.00</span><span class="sxs-lookup"><span data-stu-id="072e5-535">175.00</span></span></td>
<td><span data-ttu-id="072e5-536">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-537">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-537">CC003</span></span></td>
<td><span data-ttu-id="072e5-538">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-538">Assembly</span></span></td>
<td><span data-ttu-id="072e5-539">55</span><span class="sxs-lookup"><span data-stu-id="072e5-539">55</span></span></td>
<td><span data-ttu-id="072e5-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="072e5-541">275.00</span><span class="sxs-lookup"><span data-stu-id="072e5-541">275.00</span></span></td>
<td><span data-ttu-id="072e5-542">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-543">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-543">CC004</span></span></td>
<td><span data-ttu-id="072e5-544">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-544">Packaging</span></span></td>
<td><span data-ttu-id="072e5-545">10</span><span class="sxs-lookup"><span data-stu-id="072e5-545">10</span></span></td>
<td><span data-ttu-id="072e5-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="072e5-547">50.00</span><span class="sxs-lookup"><span data-stu-id="072e5-547">50.00</span></span></td>
<td><span data-ttu-id="072e5-548">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-549">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-549">CC002</span></span></td>
<td><span data-ttu-id="072e5-550">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-550">Finance</span></span></td>
<td><span data-ttu-id="072e5-551">35</span><span class="sxs-lookup"><span data-stu-id="072e5-551">35</span></span></td>
<td><span data-ttu-id="072e5-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="072e5-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="072e5-553">436.00</span><span class="sxs-lookup"><span data-stu-id="072e5-553">436.00</span></span></td>
<td><span data-ttu-id="072e5-554">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-555">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-555">CC003</span></span></td>
<td><span data-ttu-id="072e5-556">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-556">Assembly</span></span></td>
<td><span data-ttu-id="072e5-557">55</span><span class="sxs-lookup"><span data-stu-id="072e5-557">55</span></span></td>
<td><span data-ttu-id="072e5-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="072e5-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="072e5-559">685.14</span><span class="sxs-lookup"><span data-stu-id="072e5-559">685.14</span></span></td>
<td><span data-ttu-id="072e5-560">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-561">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-561">CC004</span></span></td>
<td><span data-ttu-id="072e5-562">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-562">Packaging</span></span></td>
<td><span data-ttu-id="072e5-563">10</span><span class="sxs-lookup"><span data-stu-id="072e5-563">10</span></span></td>
<td><span data-ttu-id="072e5-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="072e5-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="072e5-565">124.57</span><span class="sxs-lookup"><span data-stu-id="072e5-565">124.57</span></span></td>
<td><span data-ttu-id="072e5-566">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-567">يعرض الجدول التالي النتيجة عند تطبيق الخدمات المالية كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="072e5-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-568">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-568">Cost object</span></span></th>
<th><span data-ttu-id="072e5-569">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-569">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-570">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-570">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-571">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-571">Amount</span></span></th>
<th><span data-ttu-id="072e5-572">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-573">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-573">CC003</span></span></td>
<td><span data-ttu-id="072e5-574">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-574">Assembly</span></span></td>
<td><span data-ttu-id="072e5-575">65</span><span class="sxs-lookup"><span data-stu-id="072e5-575">65</span></span></td>
<td><span data-ttu-id="072e5-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="072e5-577">438.75</span><span class="sxs-lookup"><span data-stu-id="072e5-577">438.75</span></span></td>
<td><span data-ttu-id="072e5-578">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-579">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-579">CC004</span></span></td>
<td><span data-ttu-id="072e5-580">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-580">Packaging</span></span></td>
<td><span data-ttu-id="072e5-581">35</span><span class="sxs-lookup"><span data-stu-id="072e5-581">35</span></span></td>
<td><span data-ttu-id="072e5-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="072e5-583">236.25</span><span class="sxs-lookup"><span data-stu-id="072e5-583">236.25</span></span></td>
<td><span data-ttu-id="072e5-584">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-585">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-585">CC003</span></span></td>
<td><span data-ttu-id="072e5-586">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-586">Assembly</span></span></td>
<td><span data-ttu-id="072e5-587">65</span><span class="sxs-lookup"><span data-stu-id="072e5-587">65</span></span></td>
<td><span data-ttu-id="072e5-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="072e5-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="072e5-589">5,297.69</span></span></td>
<td><span data-ttu-id="072e5-590">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-591">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-591">CC004</span></span></td>
<td><span data-ttu-id="072e5-592">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-592">Packaging</span></span></td>
<td><span data-ttu-id="072e5-593">35</span><span class="sxs-lookup"><span data-stu-id="072e5-593">35</span></span></td>
<td><span data-ttu-id="072e5-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="072e5-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="072e5-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="072e5-595">2,852.60</span></span></td>
<td><span data-ttu-id="072e5-596">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-597">يعرض الجدول التالي النتيجة عند تطبيق خدمات التجميع كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="072e5-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-598">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-598">Cost object</span></span></th>
<th><span data-ttu-id="072e5-599">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-599">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-600">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-600">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-601">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-601">Amount</span></span></th>
<th><span data-ttu-id="072e5-602">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-603">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-603">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-604">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-604">Product 1</span></span></td>
<td><span data-ttu-id="072e5-605">60</span><span class="sxs-lookup"><span data-stu-id="072e5-605">60</span></span></td>
<td><span data-ttu-id="072e5-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="072e5-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="072e5-607">535.31</span><span class="sxs-lookup"><span data-stu-id="072e5-607">535.31</span></span></td>
<td><span data-ttu-id="072e5-608">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-609">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-609">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-610">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-610">Product 2</span></span></td>
<td><span data-ttu-id="072e5-611">20</span><span class="sxs-lookup"><span data-stu-id="072e5-611">20</span></span></td>
<td><span data-ttu-id="072e5-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="072e5-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="072e5-613">178.44</span><span class="sxs-lookup"><span data-stu-id="072e5-613">178.44</span></span></td>
<td><span data-ttu-id="072e5-614">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-615">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-615">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-616">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-616">Product 1</span></span></td>
<td><span data-ttu-id="072e5-617">60</span><span class="sxs-lookup"><span data-stu-id="072e5-617">60</span></span></td>
<td><span data-ttu-id="072e5-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="072e5-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="072e5-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="072e5-619">4,487.12</span></span></td>
<td><span data-ttu-id="072e5-620">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-621">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-621">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-622">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-622">Product 2</span></span></td>
<td><span data-ttu-id="072e5-623">20</span><span class="sxs-lookup"><span data-stu-id="072e5-623">20</span></span></td>
<td><span data-ttu-id="072e5-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="072e5-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="072e5-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="072e5-625">1,495.71</span></span></td>
<td><span data-ttu-id="072e5-626">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="072e5-627">يعرض الجدول التالي النتيجة عند تطبيق خدمات التعبئة كأساس توزيع لإجمالي التكلفة (التكلفة الثابتة والتكلفة المتغيرة).</span><span class="sxs-lookup"><span data-stu-id="072e5-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-628">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-628">Cost object</span></span></th>
<th><span data-ttu-id="072e5-629">المقدار</span><span class="sxs-lookup"><span data-stu-id="072e5-629">Magnitude</span></span></th>
<th><span data-ttu-id="072e5-630">عامل التوزيع</span><span class="sxs-lookup"><span data-stu-id="072e5-630">Allocation factor</span></span></th>
<th><span data-ttu-id="072e5-631">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-631">Amount</span></span></th>
<th><span data-ttu-id="072e5-632">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-633">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-633">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-634">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-634">Product 1</span></span></td>
<td><span data-ttu-id="072e5-635">80</span><span class="sxs-lookup"><span data-stu-id="072e5-635">80</span></span></td>
<td><span data-ttu-id="072e5-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="072e5-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="072e5-637">241.05</span><span class="sxs-lookup"><span data-stu-id="072e5-637">241.05</span></span></td>
<td><span data-ttu-id="072e5-638">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-639">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-639">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-640">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-640">Product 2</span></span></td>
<td><span data-ttu-id="072e5-641">15</span><span class="sxs-lookup"><span data-stu-id="072e5-641">15</span></span></td>
<td><span data-ttu-id="072e5-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="072e5-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="072e5-643">45.20</span><span class="sxs-lookup"><span data-stu-id="072e5-643">45.20</span></span></td>
<td><span data-ttu-id="072e5-644">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-645">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-645">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-646">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-646">Product 1</span></span></td>
<td><span data-ttu-id="072e5-647">80</span><span class="sxs-lookup"><span data-stu-id="072e5-647">80</span></span></td>
<td><span data-ttu-id="072e5-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="072e5-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="072e5-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="072e5-649">2,507.09</span></span></td>
<td><span data-ttu-id="072e5-650">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-651">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-651">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-652">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-652">Product 2</span></span></td>
<td><span data-ttu-id="072e5-653">15</span><span class="sxs-lookup"><span data-stu-id="072e5-653">15</span></span></td>
<td><span data-ttu-id="072e5-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="072e5-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="072e5-655">470.08</span><span class="sxs-lookup"><span data-stu-id="072e5-655">470.08</span></span></td>
<td><span data-ttu-id="072e5-656">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="072e5-657">إدخالات دفتر اليومية (إدخالات دفتر اليومية لرصيد كائن التكلفة)</span><span class="sxs-lookup"><span data-stu-id="072e5-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-658">دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="072e5-658">Journal</span></span></th>
<th><span data-ttu-id="072e5-659">نوع دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="072e5-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="072e5-660">فترة التقويم المالي</span><span class="sxs-lookup"><span data-stu-id="072e5-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="072e5-661">‏‏الإصدار</span><span class="sxs-lookup"><span data-stu-id="072e5-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-662">00004</span><span class="sxs-lookup"><span data-stu-id="072e5-662">00004</span></span></td>
<td><span data-ttu-id="072e5-663">دفتر يومية توزيع التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="072e5-664">مالي</span><span class="sxs-lookup"><span data-stu-id="072e5-664">Fiscal</span></span></td>
<td><span data-ttu-id="072e5-665">2017</span><span class="sxs-lookup"><span data-stu-id="072e5-665">2017</span></span></td>
<td><span data-ttu-id="072e5-666">الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-666">Period 1</span></span></td>
<td><span data-ttu-id="072e5-667">حساب المصروفات الزائدة / 01-02-2017 11:51:00 م / دفتر الأستاذ العام /2017 / الفترة 1</span><span class="sxs-lookup"><span data-stu-id="072e5-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="072e5-668">سطور دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="072e5-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="072e5-669">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-670">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-671">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-671">Cost element</span></span></th>
<th><span data-ttu-id="072e5-672">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-672">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-673">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-674">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-675">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-675">CC001</span></span></td>
<td><span data-ttu-id="072e5-676">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-676">HR</span></span></td>
<td><span data-ttu-id="072e5-677">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-677">10001</span></span></td>
<td><span data-ttu-id="072e5-678">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-678">Electricity</span></span></td>
<td><span data-ttu-id="072e5-679">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-679">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-680">500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-681">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-682">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-682">CC001</span></span></td>
<td><span data-ttu-id="072e5-683">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-683">HR</span></span></td>
<td><span data-ttu-id="072e5-684">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-684">10001</span></span></td>
<td><span data-ttu-id="072e5-685">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-685">Electricity</span></span></td>
<td><span data-ttu-id="072e5-686">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-686">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="072e5-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-688">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-689">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-689">CC002</span></span></td>
<td><span data-ttu-id="072e5-690">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-690">Finance</span></span></td>
<td><span data-ttu-id="072e5-691">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-691">10001</span></span></td>
<td><span data-ttu-id="072e5-692">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-692">Electricity</span></span></td>
<td><span data-ttu-id="072e5-693">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-693">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-694">675.00</span><span class="sxs-lookup"><span data-stu-id="072e5-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-695">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-696">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-696">CC002</span></span></td>
<td><span data-ttu-id="072e5-697">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-697">Finance</span></span></td>
<td><span data-ttu-id="072e5-698">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-698">10001</span></span></td>
<td><span data-ttu-id="072e5-699">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-699">Electricity</span></span></td>
<td><span data-ttu-id="072e5-700">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-700">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="072e5-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-702">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-703">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-703">CC003</span></span></td>
<td><span data-ttu-id="072e5-704">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-704">Assembly</span></span></td>
<td><span data-ttu-id="072e5-705">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-705">10001</span></span></td>
<td><span data-ttu-id="072e5-706">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-706">Electricity</span></span></td>
<td><span data-ttu-id="072e5-707">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-707">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-708">713.75</span><span class="sxs-lookup"><span data-stu-id="072e5-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-709">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-710">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-710">CC003</span></span></td>
<td><span data-ttu-id="072e5-711">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-711">Assembly</span></span></td>
<td><span data-ttu-id="072e5-712">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-712">10001</span></span></td>
<td><span data-ttu-id="072e5-713">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-713">Electricity</span></span></td>
<td><span data-ttu-id="072e5-714">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-714">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="072e5-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-716">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-717">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-717">CC003</span></span></td>
<td><span data-ttu-id="072e5-718">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-718">Packaging</span></span></td>
<td><span data-ttu-id="072e5-719">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-719">10001</span></span></td>
<td><span data-ttu-id="072e5-720">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-720">Electricity</span></span></td>
<td><span data-ttu-id="072e5-721">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-721">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-722">286.25</span><span class="sxs-lookup"><span data-stu-id="072e5-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-723">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-724">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-724">CC003</span></span></td>
<td><span data-ttu-id="072e5-725">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-725">Packaging</span></span></td>
<td><span data-ttu-id="072e5-726">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-726">10001</span></span></td>
<td><span data-ttu-id="072e5-727">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-727">Electricity</span></span></td>
<td><span data-ttu-id="072e5-728">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-728">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="072e5-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-730">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-731">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-731">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-732">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-732">Product 1</span></span></td>
<td><span data-ttu-id="072e5-733">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-733">10001</span></span></td>
<td><span data-ttu-id="072e5-734">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-734">Electricity</span></span></td>
<td><span data-ttu-id="072e5-735">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-735">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-736">776.36</span><span class="sxs-lookup"><span data-stu-id="072e5-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-737">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-738">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-738">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-739">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-739">Product 1</span></span></td>
<td><span data-ttu-id="072e5-740">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-740">10001</span></span></td>
<td><span data-ttu-id="072e5-741">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-741">Electricity</span></span></td>
<td><span data-ttu-id="072e5-742">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-742">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="072e5-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-744">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-745">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-745">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-746">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-746">Product 1</span></span></td>
<td><span data-ttu-id="072e5-747">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-747">10001</span></span></td>
<td><span data-ttu-id="072e5-748">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-748">Electricity</span></span></td>
<td><span data-ttu-id="072e5-749">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-749">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-750">223.64</span><span class="sxs-lookup"><span data-stu-id="072e5-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-751">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="072e5-752">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-752">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-753">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-753">Product 1</span></span></td>
<td><span data-ttu-id="072e5-754">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-754">10001</span></span></td>
<td><span data-ttu-id="072e5-755">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-755">Electricity</span></span></td>
<td><span data-ttu-id="072e5-756">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-756">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="072e5-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="072e5-758">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="072e5-759">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="072e5-760">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-760">Cost element</span></span></th>
<th><span data-ttu-id="072e5-761">سلوك التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-761">Cost behavior</span></span></th>
<th><span data-ttu-id="072e5-762">المبلغ</span><span class="sxs-lookup"><span data-stu-id="072e5-762">Amount</span></span></th>
<th><span data-ttu-id="072e5-763">التاريخ المحاسبي</span><span class="sxs-lookup"><span data-stu-id="072e5-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="072e5-764">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-764">CC001</span></span></td>
<td><span data-ttu-id="072e5-765">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-765">HR</span></span></td>
<td><span data-ttu-id="072e5-766">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-766">10001</span></span></td>
<td><span data-ttu-id="072e5-767">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-767">Electricity</span></span></td>
<td><span data-ttu-id="072e5-768">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-768">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="072e5-769">-500.00</span></span></td>
<td><span data-ttu-id="072e5-770">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-771">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-771">CC002</span></span></td>
<td><span data-ttu-id="072e5-772">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-772">Finance</span></span></td>
<td><span data-ttu-id="072e5-773">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-773">10001</span></span></td>
<td><span data-ttu-id="072e5-774">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-774">Electricity</span></span></td>
<td><span data-ttu-id="072e5-775">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-775">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-776">175.00</span><span class="sxs-lookup"><span data-stu-id="072e5-776">175.00</span></span></td>
<td><span data-ttu-id="072e5-777">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-778">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-778">CC003</span></span></td>
<td><span data-ttu-id="072e5-779">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-779">Assembly</span></span></td>
<td><span data-ttu-id="072e5-780">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-780">10001</span></span></td>
<td><span data-ttu-id="072e5-781">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-781">Electricity</span></span></td>
<td><span data-ttu-id="072e5-782">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-782">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-783">275.00</span><span class="sxs-lookup"><span data-stu-id="072e5-783">275.00</span></span></td>
<td><span data-ttu-id="072e5-784">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-785">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-785">CC004</span></span></td>
<td><span data-ttu-id="072e5-786">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-786">Packaging</span></span></td>
<td><span data-ttu-id="072e5-787">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-787">10001</span></span></td>
<td><span data-ttu-id="072e5-788">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-788">Electricity</span></span></td>
<td><span data-ttu-id="072e5-789">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-789">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-790">50,00</span><span class="sxs-lookup"><span data-stu-id="072e5-790">50,00</span></span></td>
<td><span data-ttu-id="072e5-791">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-792">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-792">CC001</span></span></td>
<td><span data-ttu-id="072e5-793">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="072e5-793">HR</span></span></td>
<td><span data-ttu-id="072e5-794">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-794">10001</span></span></td>
<td><span data-ttu-id="072e5-795">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-795">Electricity</span></span></td>
<td><span data-ttu-id="072e5-796">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-796">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="072e5-797">-1,245.71</span></span></td>
<td><span data-ttu-id="072e5-798">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-799">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-799">CC002</span></span></td>
<td><span data-ttu-id="072e5-800">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-800">Finance</span></span></td>
<td><span data-ttu-id="072e5-801">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-801">10001</span></span></td>
<td><span data-ttu-id="072e5-802">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-802">Electricity</span></span></td>
<td><span data-ttu-id="072e5-803">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-803">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-804">436.00</span><span class="sxs-lookup"><span data-stu-id="072e5-804">436.00</span></span></td>
<td><span data-ttu-id="072e5-805">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-806">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-806">CC003</span></span></td>
<td><span data-ttu-id="072e5-807">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-807">Assembly</span></span></td>
<td><span data-ttu-id="072e5-808">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-808">10001</span></span></td>
<td><span data-ttu-id="072e5-809">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-809">Electricity</span></span></td>
<td><span data-ttu-id="072e5-810">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-810">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-811">685.14</span><span class="sxs-lookup"><span data-stu-id="072e5-811">685.14</span></span></td>
<td><span data-ttu-id="072e5-812">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-813">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-813">CC004</span></span></td>
<td><span data-ttu-id="072e5-814">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-814">Packaging</span></span></td>
<td><span data-ttu-id="072e5-815">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-815">10001</span></span></td>
<td><span data-ttu-id="072e5-816">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-816">Electricity</span></span></td>
<td><span data-ttu-id="072e5-817">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-817">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-818">124.57</span><span class="sxs-lookup"><span data-stu-id="072e5-818">124.57</span></span></td>
<td><span data-ttu-id="072e5-819">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-820">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-820">CC002</span></span></td>
<td><span data-ttu-id="072e5-821">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-821">Finance</span></span></td>
<td><span data-ttu-id="072e5-822">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-822">10001</span></span></td>
<td><span data-ttu-id="072e5-823">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-823">Electricity</span></span></td>
<td><span data-ttu-id="072e5-824">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-824">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="072e5-825">-675.00</span></span></td>
<td><span data-ttu-id="072e5-826">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-827">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-827">CC003</span></span></td>
<td><span data-ttu-id="072e5-828">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-828">Assembly</span></span></td>
<td><span data-ttu-id="072e5-829">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-829">10001</span></span></td>
<td><span data-ttu-id="072e5-830">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-830">Electricity</span></span></td>
<td><span data-ttu-id="072e5-831">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-831">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-832">438.75</span><span class="sxs-lookup"><span data-stu-id="072e5-832">438.75</span></span></td>
<td><span data-ttu-id="072e5-833">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-834">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-834">CC004</span></span></td>
<td><span data-ttu-id="072e5-835">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-835">Packaging</span></span></td>
<td><span data-ttu-id="072e5-836">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-836">10001</span></span></td>
<td><span data-ttu-id="072e5-837">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-837">Electricity</span></span></td>
<td><span data-ttu-id="072e5-838">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-838">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-839">236.25</span><span class="sxs-lookup"><span data-stu-id="072e5-839">236.25</span></span></td>
<td><span data-ttu-id="072e5-840">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-841">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-841">CC002</span></span></td>
<td><span data-ttu-id="072e5-842">المالية</span><span class="sxs-lookup"><span data-stu-id="072e5-842">Finance</span></span></td>
<td><span data-ttu-id="072e5-843">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-843">10001</span></span></td>
<td><span data-ttu-id="072e5-844">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-844">Electricity</span></span></td>
<td><span data-ttu-id="072e5-845">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-845">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="072e5-846">-8,150.29</span></span></td>
<td><span data-ttu-id="072e5-847">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-848">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-848">CC003</span></span></td>
<td><span data-ttu-id="072e5-849">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-849">Assembly</span></span></td>
<td><span data-ttu-id="072e5-850">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-850">10001</span></span></td>
<td><span data-ttu-id="072e5-851">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-851">Electricity</span></span></td>
<td><span data-ttu-id="072e5-852">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-852">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="072e5-853">5,297.69</span></span></td>
<td><span data-ttu-id="072e5-854">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-855">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-855">CC004</span></span></td>
<td><span data-ttu-id="072e5-856">التعبئة</span><span class="sxs-lookup"><span data-stu-id="072e5-856">Packaging</span></span></td>
<td><span data-ttu-id="072e5-857">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-857">10001</span></span></td>
<td><span data-ttu-id="072e5-858">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-858">Electricity</span></span></td>
<td><span data-ttu-id="072e5-859">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-859">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="072e5-860">2,852.60</span></span></td>
<td><span data-ttu-id="072e5-861">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-862">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-862">CC003</span></span></td>
<td><span data-ttu-id="072e5-863">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-863">Assembly</span></span></td>
<td><span data-ttu-id="072e5-864">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-864">10001</span></span></td>
<td><span data-ttu-id="072e5-865">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-865">Electricity</span></span></td>
<td><span data-ttu-id="072e5-866">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-866">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="072e5-867">-713.75</span></span></td>
<td><span data-ttu-id="072e5-868">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-869">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-869">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-870">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-870">Product 1</span></span></td>
<td><span data-ttu-id="072e5-871">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-871">10001</span></span></td>
<td><span data-ttu-id="072e5-872">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-872">Electricity</span></span></td>
<td><span data-ttu-id="072e5-873">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-873">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-874">535.31</span><span class="sxs-lookup"><span data-stu-id="072e5-874">535.31</span></span></td>
<td><span data-ttu-id="072e5-875">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-876">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-876">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-877">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-877">Product 2</span></span></td>
<td><span data-ttu-id="072e5-878">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-878">10001</span></span></td>
<td><span data-ttu-id="072e5-879">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-879">Electricity</span></span></td>
<td><span data-ttu-id="072e5-880">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-880">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-881">178.44</span><span class="sxs-lookup"><span data-stu-id="072e5-881">178.44</span></span></td>
<td><span data-ttu-id="072e5-882">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-883">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-883">CC003</span></span></td>
<td><span data-ttu-id="072e5-884">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-884">Assembly</span></span></td>
<td><span data-ttu-id="072e5-885">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-885">10001</span></span></td>
<td><span data-ttu-id="072e5-886">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-886">Electricity</span></span></td>
<td><span data-ttu-id="072e5-887">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-887">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="072e5-888">-5,982.83</span></span></td>
<td><span data-ttu-id="072e5-889">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-890">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-890">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-891">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-891">Product 1</span></span></td>
<td><span data-ttu-id="072e5-892">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-892">10001</span></span></td>
<td><span data-ttu-id="072e5-893">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-893">Electricity</span></span></td>
<td><span data-ttu-id="072e5-894">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-894">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="072e5-895">4,487.12</span></span></td>
<td><span data-ttu-id="072e5-896">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-897">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-897">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-898">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-898">Product 2</span></span></td>
<td><span data-ttu-id="072e5-899">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-899">10001</span></span></td>
<td><span data-ttu-id="072e5-900">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-900">Electricity</span></span></td>
<td><span data-ttu-id="072e5-901">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-901">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="072e5-902">1,495.71</span></span></td>
<td><span data-ttu-id="072e5-903">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-904">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-904">CC003</span></span></td>
<td><span data-ttu-id="072e5-905">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-905">Assembly</span></span></td>
<td><span data-ttu-id="072e5-906">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-906">10001</span></span></td>
<td><span data-ttu-id="072e5-907">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-907">Electricity</span></span></td>
<td><span data-ttu-id="072e5-908">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-908">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="072e5-909">-286.25</span></span></td>
<td><span data-ttu-id="072e5-910">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-911">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-911">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-912">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-912">Product 1</span></span></td>
<td><span data-ttu-id="072e5-913">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-913">10001</span></span></td>
<td><span data-ttu-id="072e5-914">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-914">Electricity</span></span></td>
<td><span data-ttu-id="072e5-915">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-915">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-916">241.05</span><span class="sxs-lookup"><span data-stu-id="072e5-916">241.05</span></span></td>
<td><span data-ttu-id="072e5-917">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-918">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-918">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-919">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-919">Product 2</span></span></td>
<td><span data-ttu-id="072e5-920">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-920">10001</span></span></td>
<td><span data-ttu-id="072e5-921">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-921">Electricity</span></span></td>
<td><span data-ttu-id="072e5-922">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-922">Fixed cost</span></span></td>
<td><span data-ttu-id="072e5-923">45.20</span><span class="sxs-lookup"><span data-stu-id="072e5-923">45.20</span></span></td>
<td><span data-ttu-id="072e5-924">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-925">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-925">CC003</span></span></td>
<td><span data-ttu-id="072e5-926">التجميع</span><span class="sxs-lookup"><span data-stu-id="072e5-926">Assembly</span></span></td>
<td><span data-ttu-id="072e5-927">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-927">10001</span></span></td>
<td><span data-ttu-id="072e5-928">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-928">Electricity</span></span></td>
<td><span data-ttu-id="072e5-929">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-929">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="072e5-930">-2,977.17</span></span></td>
<td><span data-ttu-id="072e5-931">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-932">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-932">Prod 1</span></span></td>
<td><span data-ttu-id="072e5-933">المنتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-933">Product 1</span></span></td>
<td><span data-ttu-id="072e5-934">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-934">10001</span></span></td>
<td><span data-ttu-id="072e5-935">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-935">Electricity</span></span></td>
<td><span data-ttu-id="072e5-936">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-936">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="072e5-937">2,507.09</span></span></td>
<td><span data-ttu-id="072e5-938">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="072e5-939">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-939">Prod 2</span></span></td>
<td><span data-ttu-id="072e5-940">المنتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-940">Product 2</span></span></td>
<td><span data-ttu-id="072e5-941">10001</span><span class="sxs-lookup"><span data-stu-id="072e5-941">10001</span></span></td>
<td><span data-ttu-id="072e5-942">الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-942">Electricity</span></span></td>
<td><span data-ttu-id="072e5-943">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-943">Variable cost</span></span></td>
<td><span data-ttu-id="072e5-944">470.08</span><span class="sxs-lookup"><span data-stu-id="072e5-944">470.08</span></span></td>
<td><span data-ttu-id="072e5-945">31 يناير 2017</span><span class="sxs-lookup"><span data-stu-id="072e5-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="072e5-946">الخاتمة</span><span class="sxs-lookup"><span data-stu-id="072e5-946">Conclusion</span></span>
<span data-ttu-id="072e5-947">في المحاسبة المالية، يتم ترحيل تكلفة مقدارها 10,000.00 للكهرباء إلى معرف مركز تكلفة وهمي.</span><span class="sxs-lookup"><span data-stu-id="072e5-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="072e5-948">لذلك، سيعلم محاسبو التكلفة أنه من الضروري تخصيص هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="072e5-949">في محاسبة التكاليف، تتدفق التكاليف عبر الوحدات والمستويات التنظيمية، استنادًا إلى السياسات والقواعد المطبقة.</span><span class="sxs-lookup"><span data-stu-id="072e5-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="072e5-950">تم إقران كل تكلفة بأساس توزيع يوفر أفضل تقييم لتخصيص التكاليف.</span><span class="sxs-lookup"><span data-stu-id="072e5-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="072e5-951">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="072e5-952">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="072e5-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="072e5-953">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="072e5-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="072e5-954">CC099</span><span class="sxs-lookup"><span data-stu-id="072e5-954">CC099</span></span></th>
<th><span data-ttu-id="072e5-955">CC001</span><span class="sxs-lookup"><span data-stu-id="072e5-955">CC001</span></span></th>
<th><span data-ttu-id="072e5-956">CC002</span><span class="sxs-lookup"><span data-stu-id="072e5-956">CC002</span></span></th>
<th><span data-ttu-id="072e5-957">CC003</span><span class="sxs-lookup"><span data-stu-id="072e5-957">CC003</span></span></th>
<th><span data-ttu-id="072e5-958">CC004</span><span class="sxs-lookup"><span data-stu-id="072e5-958">CC004</span></span></th>
<th><span data-ttu-id="072e5-959">مشروع 1</span><span class="sxs-lookup"><span data-stu-id="072e5-959">Proj 1</span></span></th>
<th><span data-ttu-id="072e5-960">مشروع 2</span><span class="sxs-lookup"><span data-stu-id="072e5-960">Proj 2</span></span></th>
<th><span data-ttu-id="072e5-961">منتج 1</span><span class="sxs-lookup"><span data-stu-id="072e5-961">Prod 1</span></span></th>
<th><span data-ttu-id="072e5-962">منتج 2</span><span class="sxs-lookup"><span data-stu-id="072e5-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="072e5-963">10001 الكهرباء</span><span class="sxs-lookup"><span data-stu-id="072e5-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="072e5-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="072e5-973">غير مصنف</span><span class="sxs-lookup"><span data-stu-id="072e5-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-974">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="072e5-975">تكلفة ثابتة</span><span class="sxs-lookup"><span data-stu-id="072e5-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-976">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-977">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-978">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-979">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-980">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="072e5-981">776.36</span><span class="sxs-lookup"><span data-stu-id="072e5-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-982">223.64</span><span class="sxs-lookup"><span data-stu-id="072e5-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="072e5-984">تكلفة متغيرة</span><span class="sxs-lookup"><span data-stu-id="072e5-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-985">000</span><span class="sxs-lookup"><span data-stu-id="072e5-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-986">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-987">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-988">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-989">0.00</span><span class="sxs-lookup"><span data-stu-id="072e5-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-990">30.00</span><span class="sxs-lookup"><span data-stu-id="072e5-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-991">10.00</span><span class="sxs-lookup"><span data-stu-id="072e5-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="072e5-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="072e5-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="072e5-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="072e5-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="072e5-995">يُظهر هذا الموضوع كيفية تدفق عنصر تكلفة أساسية، 10001 الكهرباء، عبر كائنات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="072e5-996">لذلك، يتم تخصيص تكلفة هذه المصروفات الزائدة إلى أدنى مستوى في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="072e5-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="072e5-997">بمعنى آخر، كانئات التكلفة في أدنى مستوى هي التي تتحمل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="072e5-998">إذا احتجت إلى تدفق مرئي للتكلفة بين كائنات التكلفة، فيمكنك استخدام قواعد سياسة زيادة التكاليف‬ لرؤية تدفق التكلفة.</span><span class="sxs-lookup"><span data-stu-id="072e5-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="072e5-999">لمزيد من المعلومات المفصلة، انظر سياسة زيادة التكاليف‬.</span><span class="sxs-lookup"><span data-stu-id="072e5-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="072e5-1000">(لاحظ أن هذا الموضوع غير مكتمل بعد ولكنه سينشر قريبًا.)</span><span class="sxs-lookup"><span data-stu-id="072e5-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




