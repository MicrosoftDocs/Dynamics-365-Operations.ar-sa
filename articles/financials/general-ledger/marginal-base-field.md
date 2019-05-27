---
title: معدلات ضريبة المبيعات على أساس طريقتي القاعدة الهامشية والعملية الحسابية
description: يوضح هذا الموضوع كيف تحدد القيم في حقلي القاعدة الهامشية وأسلوب الحساب معدل الضريبة في حركات المبيعات والمشتريات.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0128743e608ec56bea2301ac576551065a1ff290
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561512"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="dbcfc-103">معدلات ضريبة المبيعات على أساس طريقتي القاعدة الهامشية والعملية الحسابية</span><span class="sxs-lookup"><span data-stu-id="dbcfc-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbcfc-104">يوضح هذا الموضوع كيف تحدد القيم في حقلي القاعدة الهامشية وأسلوب الحساب معدل الضريبة في حركات المبيعات والمشتريات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="dbcfc-105">تحدد القاعدة الهامشية في علامة التبويب السريع "العملية الحسابية"في صفحة أكواد ضريبة المبيعات المبلغ، الذي يتم استخدامه لانتقاء معدل (معدلات) الضريبة المناسب من المعدلات الواردة في صفحة قيم أكواد ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="dbcfc-106">ويحدد نوع المبلغ في حقل القاعدة الهامشية مع الأسلوب في حقل أسلوب العملية الحسابية منطق العثور على معدل (معدلات) الضريبة الصحيح لحركة.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="dbcfc-107">ويعمل تجميع قيم هذه الحقول بشكل متنوع على إنتاج حسابات ضريبة مبيعات مختلفة تمامًا، كما هو موضح في الأمثلة التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="dbcfc-108">تستخدم الأمثلة نفس قيم فترة الضريبة، التي تم إعدادها لكل كود ضريبة في صفحة قيم أكواد ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="dbcfc-109">ولفتح هذه الصفحة، انقر فوق كود ضريبة المبيعات &gt; القيم في صفحة أكواد ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="dbcfc-110">إذا كانت القاعدة الهامشية في واحد أو أكثر من أكواد ضرائب المبيعات تستند إلى وحدات أو مبالغ البند، فإنه يجب تعيين قيمة الحقل أسلوب العملية الحسابية في صفحة معلمات دفتر الأستاذ العام إلى "بند".</span><span class="sxs-lookup"><span data-stu-id="dbcfc-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="dbcfc-111">المبلغ الصافي لكل بند</span><span class="sxs-lookup"><span data-stu-id="dbcfc-111">Net amount per line</span></span>
<span data-ttu-id="dbcfc-112">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى صافي مبلغ بنود الفاتورة، مستثنيًا أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="dbcfc-113">مثال</span><span class="sxs-lookup"><span data-stu-id="dbcfc-113">Example</span></span>

<span data-ttu-id="dbcfc-114">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="dbcfc-115">الفاصل الزمني للمبلغ</span><span class="sxs-lookup"><span data-stu-id="dbcfc-115">Amount interval</span></span>    | <span data-ttu-id="dbcfc-116">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="dbcfc-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="dbcfc-117">0 - 50</span></span>             | <span data-ttu-id="dbcfc-118">30%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-118">30%</span></span>      |
| <span data-ttu-id="dbcfc-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="dbcfc-119">50 - 100</span></span>           | <span data-ttu-id="dbcfc-120">20%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-120">20%</span></span>      |
| <span data-ttu-id="dbcfc-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="dbcfc-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="dbcfc-122">10%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="dbcfc-123">الحد الأعلى صفر (0) في آخر فاصل زمني يعني أن كافة المبالغ الأكثر من 100 مضمنة في الفاصل الزمني.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="dbcfc-124">‏‫القاعدة الهامشية: **‏‫المبلغ الصافي لكل بند‬**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="dbcfc-125">طريقة الحساب: **الفاصل الزمني‬**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="dbcfc-126">وتقوم أنت بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="dbcfc-127">ويبلغ صافي مبلغ بند الفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="dbcfc-128">يتم حساب الضريبة كالتالي:</span><span class="sxs-lookup"><span data-stu-id="dbcfc-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="dbcfc-129">إجمالي ضريبة المبيعات = 50 × 30% + 50 × 20% + 100 × 10% = 15 + 10 + 10 = 35.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="dbcfc-130">إجمالي مبلغ الفاتورة = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="dbcfc-131">**التباين**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-131">**Variation**</span></span> 

<span data-ttu-id="dbcfc-132">إذا كانت الفاتورة تشتمل على بندين يحتوي كل منهما على 4 أصناف، فإن صافي المبلغ لكل بند هو 100.00، ويتم حساب ضريبة المبيعات كالتالي:</span><span class="sxs-lookup"><span data-stu-id="dbcfc-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="dbcfc-133">بند ضريبة المبيعات 1 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="dbcfc-134">بند ضريبة المبيعات 2 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="dbcfc-135">إجمالي ضريبة المبيعات = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="dbcfc-136">إجمالي مبلغ الفاتورة = 200.00 + 50.00 = 250.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="dbcfc-137">المبلغ الصافي لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-137">Net amount per unit</span></span>
<span data-ttu-id="dbcfc-138">حدد هذا الخيار لتحددي معدلات ضريبة المبيعات استنادًا إلى قيمة كل وحدة، مستثنيًا أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="dbcfc-139">وعندما يتم تحديد قاعدة هامشية للوحدة، فيجب أيضًا تحديد وحدة لكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="dbcfc-140">مثال</span><span class="sxs-lookup"><span data-stu-id="dbcfc-140">Example</span></span>

<span data-ttu-id="dbcfc-141">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="dbcfc-142">المبلغ</span><span class="sxs-lookup"><span data-stu-id="dbcfc-142">Amount</span></span>             | <span data-ttu-id="dbcfc-143">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="dbcfc-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="dbcfc-144">0 - 50</span></span>             | <span data-ttu-id="dbcfc-145">30%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-145">30%</span></span>      |
| <span data-ttu-id="dbcfc-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="dbcfc-146">50 - 100</span></span>           | <span data-ttu-id="dbcfc-147">20%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-147">20%</span></span>      |
| <span data-ttu-id="dbcfc-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="dbcfc-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="dbcfc-149">10%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-149">10%</span></span>      |

<span data-ttu-id="dbcfc-150">‏‫القاعدة الهامشية: **‏‫المبلغ الصافي لكل وحدة‬**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="dbcfc-151">طريقة الحساب: **إجمالي المبلغ**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="dbcfc-152">وتقوم أنت بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="dbcfc-153">ويبلغ صافي مبلغ بند الفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="dbcfc-154">يتم حساب الضريبة كما يلي: ضريبة المبيعات لكل وحدة = 25.00 × 30% = 7.50 إجمالي ضريبة المبيعات = 7.50 x‏ 8 وحدات = 60.00 مبلغ الفاتورة الإجمالي 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="dbcfc-155"> المبلغ الصافي لرصيد الفاتورة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-155">Net amount of invoice balance</span></span>

<span data-ttu-id="dbcfc-156">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى إجمالي قيمة الفاتورة، مستثنيًا أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="dbcfc-157">مثال</span><span class="sxs-lookup"><span data-stu-id="dbcfc-157">Example</span></span>

<span data-ttu-id="dbcfc-158">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="dbcfc-159">المبلغ</span><span class="sxs-lookup"><span data-stu-id="dbcfc-159">Amount</span></span>            | <span data-ttu-id="dbcfc-160">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="dbcfc-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="dbcfc-161">0 - 50</span></span>            | <span data-ttu-id="dbcfc-162">30%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-162">30%</span></span>      |
| <span data-ttu-id="dbcfc-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="dbcfc-163">50 - 100</span></span>          | <span data-ttu-id="dbcfc-164">20%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-164">20%</span></span>      |
| <span data-ttu-id="dbcfc-165">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="dbcfc-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="dbcfc-166">10%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-166">10%</span></span>      |

<span data-ttu-id="dbcfc-167">‏‫القاعدة الهامشية: **‏‫المبلغ الصافي لرصيد الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="dbcfc-168">طريقة الحساب: **الفاصل الزمني** فاتورة مبيعات تشتمل على بندين مع 4 مصابيح في كل بند بتكلفة 25.00 لكلٍّ منها.‬</span><span class="sxs-lookup"><span data-stu-id="dbcfc-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="dbcfc-169">صافي رصيد الفاتورة يبلغ 4 × 25.00 + 4 × 25.00 = 200.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="dbcfc-170">يتم حساب الضريبة كما يلي: إجمالي ضريبة المبيعات = 50 × 0.30 + 50 × 0.20 + 100 × 0.10 = 15 + 10 + 10 = 35.00 مبلغ الفاتورة الإجمالي = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="dbcfc-171"> إجمالي المبلغ لكل بند</span><span class="sxs-lookup"><span data-stu-id="dbcfc-171">Gross amount per line</span></span>

<span data-ttu-id="dbcfc-172">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى قيمة البند بما في ذلك جميع الضرائب الأخرى لهذا البند.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="dbcfc-173">في إحدى مجموعات ضريبة المبيعات، يمكنك إدخال كود ضريبة مبيعات واحد فقط بهذا التحديد في حقل القاعدة الهامشية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="dbcfc-174">مثال</span><span class="sxs-lookup"><span data-stu-id="dbcfc-174">Example</span></span>

<span data-ttu-id="dbcfc-175">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="dbcfc-176">المبلغ</span><span class="sxs-lookup"><span data-stu-id="dbcfc-176">Amount</span></span>             | <span data-ttu-id="dbcfc-177">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="dbcfc-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="dbcfc-178">0 - 50</span></span>             | <span data-ttu-id="dbcfc-179">30%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-179">30%</span></span>      |
| <span data-ttu-id="dbcfc-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="dbcfc-180">50 - 100</span></span>           | <span data-ttu-id="dbcfc-181">20%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-181">20%</span></span>      |
| <span data-ttu-id="dbcfc-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="dbcfc-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="dbcfc-183">10%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-183">10%</span></span>      |

<span data-ttu-id="dbcfc-184">القاعدة الهامشية: **القيمة الإجمالية لكل بند** طريقة الحساب: **الفاصل الزمني** بالإضافة إلى ذلك هناك كود ضريبة آخر تم حسابه لرسم خاص بمبلغ 5.00 لكل مصباح.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="dbcfc-185">يضاف هذا الرسم على المبلغ الصافي قبل حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="dbcfc-186">تقوم بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="dbcfc-187">ويبلغ صافي مبلغ بند الفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="dbcfc-188">المبلغ الإجمالي لبند الفاتورة هو 8 x‏ 25.00 + 8 x‏ 5.00 = 240.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="dbcfc-189">يتم حساب الضريبة كما يلي: إجمالي ضريبة المبيعات = 50 × 0.30 + 50 × 0.20 + 140 × 0.10 = 15 + 20 + 14 = 39.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 إجمالي مبلغ الفاتورة = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="dbcfc-190">**التباين**</span><span class="sxs-lookup"><span data-stu-id="dbcfc-190">**Variation**</span></span> 

<span data-ttu-id="dbcfc-191">إذا تم إنشاء الفاتورة باستخدام بندين يحتوي كل منهما على 4 أصناف، فإن صافي المبلغ لكل بند هو 100.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="dbcfc-192">المبلغ الإجمالي (بما في ذلك رسوم 4 x‏ 5.00) لكل بند فاتورة سيبلغ 120.00، ويتم إنشاء ضريبة المبيعات كالتالي: بند فاتورة ضريبة المبيعات 1 = 50 × 0.30 + 50 × 0.20 + 20 × 0.10 = 15 + 10 + 2 = 27.00 بند فاتورة ضريبة المبيعات 2 = 50 × 0.30 + 50 × 0.20 + 20 × 0.10 = 15 + 10 + 2 = 27.00 إجمالي ضريبة المبيعات = 27.00 + 27.00 = 54.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 إجمالي مبلغ الفاتورة = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="dbcfc-193"> إجمالي المبلغ لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-193">Gross amount per unit</span></span>

<span data-ttu-id="dbcfc-194">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى قيمة الوحدة، بما في ذلك أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="dbcfc-195">في إحدى مجموعات ضريبة المبيعات، يمكنك إدخال كود ضريبة مبيعات واحد فقط بهذا التحديد في حقل القاعدة الهامشية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="dbcfc-196">مثال</span><span class="sxs-lookup"><span data-stu-id="dbcfc-196">Example</span></span>

<span data-ttu-id="dbcfc-197">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="dbcfc-198">المبلغ</span><span class="sxs-lookup"><span data-stu-id="dbcfc-198">Amount</span></span>             | <span data-ttu-id="dbcfc-199">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="dbcfc-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="dbcfc-200">0 - 50</span></span>             | <span data-ttu-id="dbcfc-201">30%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-201">30%</span></span>      |
| <span data-ttu-id="dbcfc-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="dbcfc-202">50 - 100</span></span>           | <span data-ttu-id="dbcfc-203">20%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-203">20%</span></span>      |
| <span data-ttu-id="dbcfc-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="dbcfc-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="dbcfc-205">10%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-205">10%</span></span>      |

<span data-ttu-id="dbcfc-206">القاعدة الهامشية: **المبلغ الإجمالي لكل وحدة** هناك رسم خاص بمبلغ 5.00 لكل مصباح.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="dbcfc-207">يضاف هذا الرسم على المبلغ الصافي قبل حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="dbcfc-208">وتقوم أنت بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="dbcfc-209">ويبلغ إجمالي المبلغ لكل وحدة 30.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="dbcfc-210">يتم حساب الضريبة كما يلي: ضريبة المبيعات لكل وحدة = 30 x‏ 30% = 9.00 إجمالي ضريبة المبيعات = 9.00 x‏ 8 = 72.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 مبلغ الفاتورة الإجمالي = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="dbcfc-211"> إجمالي الفاتورة متضمنًا مبالغ ضريبة المبيعات الأخرى</span><span class="sxs-lookup"><span data-stu-id="dbcfc-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="dbcfc-212">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى إجمالي قيمة الفاتورة، بما في ذلك أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="dbcfc-213">في إحدى مجموعات ضريبة المبيعات، يمكنك إدخال كود ضريبة مبيعات واحد فقط بهذا التحديد في حقل القاعدة الهامشية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="dbcfc-214">مثال</span><span class="sxs-lookup"><span data-stu-id="dbcfc-214">Example</span></span>

<span data-ttu-id="dbcfc-215">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="dbcfc-216">المبلغ</span><span class="sxs-lookup"><span data-stu-id="dbcfc-216">Amount</span></span>             | <span data-ttu-id="dbcfc-217">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="dbcfc-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="dbcfc-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="dbcfc-218">0 - 50</span></span>             | <span data-ttu-id="dbcfc-219">30%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-219">30%</span></span>      |
| <span data-ttu-id="dbcfc-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="dbcfc-220">50 - 100</span></span>           | <span data-ttu-id="dbcfc-221">20%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-221">20%</span></span>      |
| <span data-ttu-id="dbcfc-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="dbcfc-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="dbcfc-223">10%</span><span class="sxs-lookup"><span data-stu-id="dbcfc-223">10%</span></span>      |

<span data-ttu-id="dbcfc-224">القاعدة الهامشية: **‏‫إجمالي الفاتورة متضمنًا مبالغ ضريبة المبيعات الأخرى‬** طريقة الحساب: **الفاصل الزمني** </span><span class="sxs-lookup"><span data-stu-id="dbcfc-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="dbcfc-225">هناك رسم خاص بمبلغ 5.00 لكل مصباح.‬</span><span class="sxs-lookup"><span data-stu-id="dbcfc-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="dbcfc-226">يضاف هذا الرسم على المبلغ الصافي قبل حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="dbcfc-227">تقوم بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="dbcfc-228">يبلغ المبلغ الصافي للفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="dbcfc-229">وإجمالي مبلغ الفاتورة يبلغ 200.00 + (8 x‏ 5.00) = 240.00.</span><span class="sxs-lookup"><span data-stu-id="dbcfc-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="dbcfc-230">يتم حساب الضريبة كما يلي: إجمالي ضريبة المبيعات = 50 × 0.30 + 50 × 0.20 + 140 × 0.10 = 15 + 10 + 14 = 39.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 إجمالي مبلغ الفاتورة = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="dbcfc-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="dbcfc-231">‏‫لمزيد من المعلومات، راجع [خيارا الحساب المبلغ بالكامل والفاصل الزمني لأكواد ضريبة المبيعات](whole-amount-interval-options-sales-tax-codes.md) و[طرق حساب ضريبة المبيعات في الحقل الأصل](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="dbcfc-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



