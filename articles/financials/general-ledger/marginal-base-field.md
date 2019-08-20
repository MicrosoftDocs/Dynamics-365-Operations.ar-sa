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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e7e3f37d759953b7b4f70fe9eae78154da44d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846837"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="7cbdc-103">معدلات ضريبة المبيعات على أساس طريقتي القاعدة الهامشية والعملية الحسابية</span><span class="sxs-lookup"><span data-stu-id="7cbdc-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cbdc-104">يوضح هذا الموضوع كيف تحدد القيم في حقلي القاعدة الهامشية وأسلوب الحساب معدل الضريبة في حركات المبيعات والمشتريات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="7cbdc-105">تحدد القاعدة الهامشية في علامة التبويب السريع "العملية الحسابية"في صفحة أكواد ضريبة المبيعات المبلغ، الذي يتم استخدامه لانتقاء معدل (معدلات) الضريبة المناسب من المعدلات الواردة في صفحة قيم أكواد ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="7cbdc-106">ويحدد نوع المبلغ في حقل القاعدة الهامشية مع الأسلوب في حقل أسلوب العملية الحسابية منطق العثور على معدل (معدلات) الضريبة الصحيح لحركة.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="7cbdc-107">ويعمل تجميع قيم هذه الحقول بشكل متنوع على إنتاج حسابات ضريبة مبيعات مختلفة تمامًا، كما هو موضح في الأمثلة التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="7cbdc-108">تستخدم الأمثلة نفس قيم فترة الضريبة، التي تم إعدادها لكل كود ضريبة في صفحة قيم أكواد ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="7cbdc-109">ولفتح هذه الصفحة، انقر فوق كود ضريبة المبيعات &gt; القيم في صفحة أكواد ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="7cbdc-110">إذا كانت القاعدة الهامشية في واحد أو أكثر من أكواد ضرائب المبيعات تستند إلى وحدات أو مبالغ البند، فإنه يجب تعيين قيمة الحقل أسلوب العملية الحسابية في صفحة معلمات دفتر الأستاذ العام إلى "بند".</span><span class="sxs-lookup"><span data-stu-id="7cbdc-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="7cbdc-111">المبلغ الصافي لكل بند</span><span class="sxs-lookup"><span data-stu-id="7cbdc-111">Net amount per line</span></span>
<span data-ttu-id="7cbdc-112">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى صافي مبلغ بنود الفاتورة، مستثنيًا أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="7cbdc-113">مثال</span><span class="sxs-lookup"><span data-stu-id="7cbdc-113">Example</span></span>

<span data-ttu-id="7cbdc-114">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="7cbdc-115">الفاصل الزمني للمبلغ</span><span class="sxs-lookup"><span data-stu-id="7cbdc-115">Amount interval</span></span>    | <span data-ttu-id="7cbdc-116">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="7cbdc-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="7cbdc-117">0 - 50</span></span>             | <span data-ttu-id="7cbdc-118">30%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-118">30%</span></span>      |
| <span data-ttu-id="7cbdc-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="7cbdc-119">50 - 100</span></span>           | <span data-ttu-id="7cbdc-120">20%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-120">20%</span></span>      |
| <span data-ttu-id="7cbdc-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="7cbdc-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="7cbdc-122">10%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="7cbdc-123">الحد الأعلى صفر (0) في آخر فاصل زمني يعني أن كافة المبالغ الأكثر من 100 مضمنة في الفاصل الزمني.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="7cbdc-124">‏‫القاعدة الهامشية: **‏‫المبلغ الصافي لكل بند‬**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="7cbdc-125">طريقة الحساب: **الفاصل الزمني‬**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="7cbdc-126">وتقوم أنت بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="7cbdc-127">ويبلغ صافي مبلغ بند الفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="7cbdc-128">يتم حساب الضريبة كالتالي:</span><span class="sxs-lookup"><span data-stu-id="7cbdc-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="7cbdc-129">إجمالي ضريبة المبيعات = 50 × 30% + 50 × 20% + 100 × 10% = 15 + 10 + 10 = 35.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="7cbdc-130">إجمالي مبلغ الفاتورة = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="7cbdc-131">**التباين**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-131">**Variation**</span></span> 

<span data-ttu-id="7cbdc-132">إذا كانت الفاتورة تشتمل على بندين يحتوي كل منهما على 4 أصناف، فإن صافي المبلغ لكل بند هو 100.00، ويتم حساب ضريبة المبيعات كالتالي:</span><span class="sxs-lookup"><span data-stu-id="7cbdc-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="7cbdc-133">بند ضريبة المبيعات 1 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="7cbdc-134">بند ضريبة المبيعات 2 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="7cbdc-135">إجمالي ضريبة المبيعات = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="7cbdc-136">إجمالي مبلغ الفاتورة = 200.00 + 50.00 = 250.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="7cbdc-137">المبلغ الصافي لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-137">Net amount per unit</span></span>
<span data-ttu-id="7cbdc-138">حدد هذا الخيار لتحددي معدلات ضريبة المبيعات استنادًا إلى قيمة كل وحدة، مستثنيًا أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="7cbdc-139">وعندما يتم تحديد قاعدة هامشية للوحدة، فيجب أيضًا تحديد وحدة لكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="7cbdc-140">مثال</span><span class="sxs-lookup"><span data-stu-id="7cbdc-140">Example</span></span>

<span data-ttu-id="7cbdc-141">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="7cbdc-142">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cbdc-142">Amount</span></span>             | <span data-ttu-id="7cbdc-143">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="7cbdc-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="7cbdc-144">0 - 50</span></span>             | <span data-ttu-id="7cbdc-145">30%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-145">30%</span></span>      |
| <span data-ttu-id="7cbdc-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="7cbdc-146">50 - 100</span></span>           | <span data-ttu-id="7cbdc-147">20%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-147">20%</span></span>      |
| <span data-ttu-id="7cbdc-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="7cbdc-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="7cbdc-149">10%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-149">10%</span></span>      |

<span data-ttu-id="7cbdc-150">‏‫القاعدة الهامشية: **‏‫المبلغ الصافي لكل وحدة‬**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="7cbdc-151">طريقة الحساب: **إجمالي المبلغ**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="7cbdc-152">وتقوم أنت بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="7cbdc-153">ويبلغ صافي مبلغ بند الفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="7cbdc-154">يتم حساب الضريبة كما يلي: ضريبة المبيعات لكل وحدة = 25.00 × 30% = 7.50 إجمالي ضريبة المبيعات = 7.50 x‏ 8 وحدات = 60.00 مبلغ الفاتورة الإجمالي 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="7cbdc-155"> المبلغ الصافي لرصيد الفاتورة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-155">Net amount of invoice balance</span></span>

<span data-ttu-id="7cbdc-156">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى إجمالي قيمة الفاتورة، مستثنيًا أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="7cbdc-157">مثال</span><span class="sxs-lookup"><span data-stu-id="7cbdc-157">Example</span></span>

<span data-ttu-id="7cbdc-158">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="7cbdc-159">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cbdc-159">Amount</span></span>            | <span data-ttu-id="7cbdc-160">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="7cbdc-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="7cbdc-161">0 - 50</span></span>            | <span data-ttu-id="7cbdc-162">30%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-162">30%</span></span>      |
| <span data-ttu-id="7cbdc-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="7cbdc-163">50 - 100</span></span>          | <span data-ttu-id="7cbdc-164">20%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-164">20%</span></span>      |
| <span data-ttu-id="7cbdc-165">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="7cbdc-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="7cbdc-166">10%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-166">10%</span></span>      |

<span data-ttu-id="7cbdc-167">‏‫القاعدة الهامشية: **‏‫المبلغ الصافي لرصيد الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="7cbdc-168">طريقة الحساب: **الفاصل الزمني** فاتورة مبيعات تشتمل على بندين مع 4 مصابيح في كل بند بتكلفة 25.00 لكلٍّ منها.‬</span><span class="sxs-lookup"><span data-stu-id="7cbdc-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="7cbdc-169">صافي رصيد الفاتورة يبلغ 4 × 25.00 + 4 × 25.00 = 200.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="7cbdc-170">يتم حساب الضريبة كما يلي: إجمالي ضريبة المبيعات = 50 × 0.30 + 50 × 0.20 + 100 × 0.10 = 15 + 10 + 10 = 35.00 مبلغ الفاتورة الإجمالي = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="7cbdc-171"> إجمالي المبلغ لكل بند</span><span class="sxs-lookup"><span data-stu-id="7cbdc-171">Gross amount per line</span></span>

<span data-ttu-id="7cbdc-172">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى قيمة البند بما في ذلك جميع الضرائب الأخرى لهذا البند.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="7cbdc-173">في إحدى مجموعات ضريبة المبيعات، يمكنك إدخال كود ضريبة مبيعات واحد فقط بهذا التحديد في حقل القاعدة الهامشية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="7cbdc-174">مثال</span><span class="sxs-lookup"><span data-stu-id="7cbdc-174">Example</span></span>

<span data-ttu-id="7cbdc-175">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="7cbdc-176">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cbdc-176">Amount</span></span>             | <span data-ttu-id="7cbdc-177">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="7cbdc-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="7cbdc-178">0 - 50</span></span>             | <span data-ttu-id="7cbdc-179">30%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-179">30%</span></span>      |
| <span data-ttu-id="7cbdc-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="7cbdc-180">50 - 100</span></span>           | <span data-ttu-id="7cbdc-181">20%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-181">20%</span></span>      |
| <span data-ttu-id="7cbdc-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="7cbdc-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="7cbdc-183">10%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-183">10%</span></span>      |

<span data-ttu-id="7cbdc-184">القاعدة الهامشية: **القيمة الإجمالية لكل بند** طريقة الحساب: **الفاصل الزمني** بالإضافة إلى ذلك هناك كود ضريبة آخر تم حسابه لرسم خاص بمبلغ 5.00 لكل مصباح.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="7cbdc-185">يضاف هذا الرسم على المبلغ الصافي قبل حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="7cbdc-186">تقوم بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="7cbdc-187">ويبلغ صافي مبلغ بند الفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="7cbdc-188">المبلغ الإجمالي لبند الفاتورة هو 8 x‏ 25.00 + 8 x‏ 5.00 = 240.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="7cbdc-189">يتم حساب الضريبة كما يلي: إجمالي ضريبة المبيعات = 50 × 0.30 + 50 × 0.20 + 140 × 0.10 = 15 + 20 + 14 = 39.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 إجمالي مبلغ الفاتورة = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="7cbdc-190">**التباين**</span><span class="sxs-lookup"><span data-stu-id="7cbdc-190">**Variation**</span></span> 

<span data-ttu-id="7cbdc-191">إذا تم إنشاء الفاتورة باستخدام بندين يحتوي كل منهما على 4 أصناف، فإن صافي المبلغ لكل بند هو 100.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="7cbdc-192">المبلغ الإجمالي (بما في ذلك رسوم 4 x‏ 5.00) لكل بند فاتورة سيبلغ 120.00، ويتم إنشاء ضريبة المبيعات كالتالي: بند فاتورة ضريبة المبيعات 1 = 50 × 0.30 + 50 × 0.20 + 20 × 0.10 = 15 + 10 + 2 = 27.00 بند فاتورة ضريبة المبيعات 2 = 50 × 0.30 + 50 × 0.20 + 20 × 0.10 = 15 + 10 + 2 = 27.00 إجمالي ضريبة المبيعات = 27.00 + 27.00 = 54.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 إجمالي مبلغ الفاتورة = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="7cbdc-193"> إجمالي المبلغ لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-193">Gross amount per unit</span></span>

<span data-ttu-id="7cbdc-194">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى قيمة الوحدة، بما في ذلك أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="7cbdc-195">في إحدى مجموعات ضريبة المبيعات، يمكنك إدخال كود ضريبة مبيعات واحد فقط بهذا التحديد في حقل القاعدة الهامشية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="7cbdc-196">مثال</span><span class="sxs-lookup"><span data-stu-id="7cbdc-196">Example</span></span>

<span data-ttu-id="7cbdc-197">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="7cbdc-198">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cbdc-198">Amount</span></span>             | <span data-ttu-id="7cbdc-199">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="7cbdc-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="7cbdc-200">0 - 50</span></span>             | <span data-ttu-id="7cbdc-201">30%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-201">30%</span></span>      |
| <span data-ttu-id="7cbdc-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="7cbdc-202">50 - 100</span></span>           | <span data-ttu-id="7cbdc-203">20%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-203">20%</span></span>      |
| <span data-ttu-id="7cbdc-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="7cbdc-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="7cbdc-205">10%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-205">10%</span></span>      |

<span data-ttu-id="7cbdc-206">القاعدة الهامشية: **المبلغ الإجمالي لكل وحدة** هناك رسم خاص بمبلغ 5.00 لكل مصباح.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="7cbdc-207">يضاف هذا الرسم على المبلغ الصافي قبل حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="7cbdc-208">وتقوم أنت بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="7cbdc-209">ويبلغ إجمالي المبلغ لكل وحدة 30.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="7cbdc-210">يتم حساب الضريبة كما يلي: ضريبة المبيعات لكل وحدة = 30 x‏ 30% = 9.00 إجمالي ضريبة المبيعات = 9.00 x‏ 8 = 72.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 مبلغ الفاتورة الإجمالي = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="7cbdc-211"> إجمالي الفاتورة متضمنًا مبالغ ضريبة المبيعات الأخرى</span><span class="sxs-lookup"><span data-stu-id="7cbdc-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="7cbdc-212">حدد هذا الخيار لتحديد معدلات ضريبة المبيعات استنادًا إلى إجمالي قيمة الفاتورة، بما في ذلك أية ضرائب أخرى.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="7cbdc-213">في إحدى مجموعات ضريبة المبيعات، يمكنك إدخال كود ضريبة مبيعات واحد فقط بهذا التحديد في حقل القاعدة الهامشية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="7cbdc-214">مثال</span><span class="sxs-lookup"><span data-stu-id="7cbdc-214">Example</span></span>

<span data-ttu-id="7cbdc-215">يتم إعداد معدلات ضرائب المبيعات في الفواصل الزمنية التالية.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="7cbdc-216">المبلغ</span><span class="sxs-lookup"><span data-stu-id="7cbdc-216">Amount</span></span>             | <span data-ttu-id="7cbdc-217">نسبة الضريبة</span><span class="sxs-lookup"><span data-stu-id="7cbdc-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="7cbdc-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="7cbdc-218">0 - 50</span></span>             | <span data-ttu-id="7cbdc-219">30%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-219">30%</span></span>      |
| <span data-ttu-id="7cbdc-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="7cbdc-220">50 - 100</span></span>           | <span data-ttu-id="7cbdc-221">20%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-221">20%</span></span>      |
| <span data-ttu-id="7cbdc-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="7cbdc-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="7cbdc-223">10%</span><span class="sxs-lookup"><span data-stu-id="7cbdc-223">10%</span></span>      |

<span data-ttu-id="7cbdc-224">القاعدة الهامشية: **‏‫إجمالي الفاتورة متضمنًا مبالغ ضريبة المبيعات الأخرى‬** طريقة الحساب: **الفاصل الزمني** </span><span class="sxs-lookup"><span data-stu-id="7cbdc-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="7cbdc-225">هناك رسم خاص بمبلغ 5.00 لكل مصباح.‬</span><span class="sxs-lookup"><span data-stu-id="7cbdc-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="7cbdc-226">يضاف هذا الرسم على المبلغ الصافي قبل حساب ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="7cbdc-227">تقوم بشراء 8 مصابيح بتكلفة 25.00 لكلٍّ منها.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="7cbdc-228">يبلغ المبلغ الصافي للفاتورة 200.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="7cbdc-229">وإجمالي مبلغ الفاتورة يبلغ 200.00 + (8 x‏ 5.00) = 240.00.</span><span class="sxs-lookup"><span data-stu-id="7cbdc-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="7cbdc-230">يتم حساب الضريبة كما يلي: إجمالي ضريبة المبيعات = 50 × 0.30 + 50 × 0.20 + 140 × 0.10 = 15 + 10 + 14 = 39.00 إجمالي الرسوم = 5.00 x‏ 8 = 40.00 إجمالي مبلغ الفاتورة = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="7cbdc-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="7cbdc-231">‏‫لمزيد من المعلومات، راجع [خيارا الحساب المبلغ بالكامل والفاصل الزمني لأكواد ضريبة المبيعات](whole-amount-interval-options-sales-tax-codes.md) و[طرق حساب ضريبة المبيعات في الحقل الأصل](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="7cbdc-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



