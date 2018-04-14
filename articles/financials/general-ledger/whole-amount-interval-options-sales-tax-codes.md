---
title: "المبلغ بالكامل وخيارات حساب الفترات لأكواد ضريبة المبيعات"
description: "تشرح هذه المقالة خيارات حقل أسلوب حساب على أكواد ضريبة المبيعات وكيفية حساب ضريبة المبيعات للفترات والمبالغ كاملة."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8923f75370c6707ab6a4304dd139081807c6decd
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="7b6e5-103">المبلغ بالكامل وخيارات حساب الفترات لأكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="7b6e5-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

<span data-ttu-id="7b6e5-104">تشرح هذه المقالة خيارات حقل أسلوب حساب على أكواد ضريبة المبيعات وكيفية حساب ضريبة المبيعات للفترات والمبالغ كاملة.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="7b6e5-105">يمكنك إعداد كود ضريبة مبيعات ليتم حسابه على أساس مبلغ كامل أو مبلغ فترة.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="7b6e5-106">في صفحة أكواد ضريبة المبيعات، استخدام حقل طريقة الحساب في علامة التبويب السريع "الحساب" لتحديد كيفية حساب كود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="7b6e5-107">المبلغ الكامل – يتم تطبيق معدل الضريبة على المبلغ الخاضع للضريبة بالكامل.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="7b6e5-108">الفترة – يتم تقسيم المبلغ الخاضع للضريبة إلى أجزاء، يقع كل جزء منها في نطاق يحتوي على معدل ضريبة محدد.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="7b6e5-109">ويتم احتساب الضريبة على جزء المبلغ الذي يقع في فترة محددة وذلك وفقًا لمعدل الضريبة لهذه الفترة.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="7b6e5-110">ومعدل الضريبة هو مجموع مبالغ الضريبة التي يتم حسابها لكل فترة مبلغ.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="7b6e5-111">يتوفر خيار الفترة فقط عند تحديد بند في حقل طريقة الحساب في منطقة ضريبة المبيعات في صفحة معلمات دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="7b6e5-112">يتم إعداد الفواصل الزمنية في صفحة قيم أكواد ضريبة المبيعات عن طريق إدخال الحد الأدنى والحد الأقصى للمبالغ لكل معدل الضريبة.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="7b6e5-113">بالنسبة للضرائب التي ينبغي حسابها على كافة المبالغ الخاضعة للضريبة، بغض النظر عن الطريقة التي يتم تحديدها، فيجب أن تتوافق الفترات مع القواعد التالية:</span><span class="sxs-lookup"><span data-stu-id="7b6e5-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="7b6e5-114">يجب أن تشتمل الفترة الأولى حد أدنى قيمته صفر.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="7b6e5-115">يجب أن تشتمل الفترة الأخيرة على حد أقصى قيمته صفر يشير إلى اللانهاية.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="7b6e5-116">يجب أن يساوي الحد الأقصى للفترة الحد الأدنى للفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="7b6e5-117">إذا كان المبلغ هو الحد الأقصى للفترة السابقة والحد الأدنى للفترة التالية، فسيتم تطبيق معدل ضريبة المبيعات الفترة الأولى على المبلغ.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="7b6e5-118">إذا وقع المبلغ خارج الفترات المحددة وفقًا للحدين الأدنى والأعلى، فسيتم تطبيق معدل ضريبة مبيعات بمبلغ صفر.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="7b6e5-119">مثال: طريقة حساب إجمالي المبلغ</span><span class="sxs-lookup"><span data-stu-id="7b6e5-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="7b6e5-120">في صفحة قيم أكواد ضريبة المبيعات، يتم إعداد معدلات ضريبة المبيعات في الفترات التالية:</span><span class="sxs-lookup"><span data-stu-id="7b6e5-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="7b6e5-121">**حد الحد الأدنى**</span><span class="sxs-lookup"><span data-stu-id="7b6e5-121">**Minimum limit**</span></span> | <span data-ttu-id="7b6e5-122">**الحد الأقصى**</span><span class="sxs-lookup"><span data-stu-id="7b6e5-122">**Maximum limit**</span></span> | <span data-ttu-id="7b6e5-123">**معدل الضريبة**</span><span class="sxs-lookup"><span data-stu-id="7b6e5-123">**Tax rate**</span></span> |
| <span data-ttu-id="7b6e5-124">0.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-124">0.00</span></span>              | <span data-ttu-id="7b6e5-125">50.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-125">50.00</span></span>             | <span data-ttu-id="7b6e5-126">30%</span><span class="sxs-lookup"><span data-stu-id="7b6e5-126">30%</span></span>          |
| <span data-ttu-id="7b6e5-127">50.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-127">50.00</span></span>             | <span data-ttu-id="7b6e5-128">100.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-128">100.00</span></span>            | <span data-ttu-id="7b6e5-129">20%</span><span class="sxs-lookup"><span data-stu-id="7b6e5-129">20%</span></span>          |
| <span data-ttu-id="7b6e5-130">100.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-130">100.00</span></span>            | <span data-ttu-id="7b6e5-131">0.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-131">0.00</span></span>              | <span data-ttu-id="7b6e5-132">10%</span><span class="sxs-lookup"><span data-stu-id="7b6e5-132">10%</span></span>          |

<span data-ttu-id="7b6e5-133">يتم حساب ضريبة المبيعات على إجمالي المبلغ الخاضع للضريبة.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="7b6e5-134">مبلغ خاضع للضريبة (السعر)</span><span class="sxs-lookup"><span data-stu-id="7b6e5-134">Taxable amount (price)</span></span> | <span data-ttu-id="7b6e5-135">حساب</span><span class="sxs-lookup"><span data-stu-id="7b6e5-135">Calculation</span></span>    | <span data-ttu-id="7b6e5-136">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="7b6e5-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="7b6e5-137">35.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-137">35.00</span></span>                  | <span data-ttu-id="7b6e5-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="7b6e5-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="7b6e5-139">1050</span><span class="sxs-lookup"><span data-stu-id="7b6e5-139">10.50</span></span>     |
| <span data-ttu-id="7b6e5-140">50.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-140">50.00</span></span>                  | <span data-ttu-id="7b6e5-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="7b6e5-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="7b6e5-142">15.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-142">15.00</span></span>     |
| <span data-ttu-id="7b6e5-143">85.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-143">85.00</span></span>                  | <span data-ttu-id="7b6e5-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="7b6e5-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="7b6e5-145">17.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-145">17.00</span></span>     |
| <span data-ttu-id="7b6e5-146">305.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-146">305.00</span></span>                 | <span data-ttu-id="7b6e5-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="7b6e5-147">305.00 \* 0.10</span></span> | <span data-ttu-id="7b6e5-148">30.50</span><span class="sxs-lookup"><span data-stu-id="7b6e5-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="7b6e5-149">مثال: طريقة حساب الفترة</span><span class="sxs-lookup"><span data-stu-id="7b6e5-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="7b6e5-150">في صفحة القيم، يتم إعداد معدلات ضرائب المبيعات في الفترات التالية:</span><span class="sxs-lookup"><span data-stu-id="7b6e5-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="7b6e5-151">**حد الحد الأدنى**</span><span class="sxs-lookup"><span data-stu-id="7b6e5-151">**Minimum limit**</span></span> | <span data-ttu-id="7b6e5-152">**الحد الأقصى**</span><span class="sxs-lookup"><span data-stu-id="7b6e5-152">**Maximum limit**</span></span> | <span data-ttu-id="7b6e5-153">**معدل الضريبة**</span><span class="sxs-lookup"><span data-stu-id="7b6e5-153">**Tax rate**</span></span> |
| <span data-ttu-id="7b6e5-154">0.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-154">0.00</span></span>              | <span data-ttu-id="7b6e5-155">50.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-155">50.00</span></span>             | <span data-ttu-id="7b6e5-156">30%</span><span class="sxs-lookup"><span data-stu-id="7b6e5-156">30%</span></span>          |
| <span data-ttu-id="7b6e5-157">50.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-157">50.00</span></span>             | <span data-ttu-id="7b6e5-158">100.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-158">100.00</span></span>            | <span data-ttu-id="7b6e5-159">20%</span><span class="sxs-lookup"><span data-stu-id="7b6e5-159">20%</span></span>          |
| <span data-ttu-id="7b6e5-160">100.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-160">100.00</span></span>            | <span data-ttu-id="7b6e5-161">0.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-161">0.00</span></span>              | <span data-ttu-id="7b6e5-162">10%</span><span class="sxs-lookup"><span data-stu-id="7b6e5-162">10%</span></span>          |

<span data-ttu-id="7b6e5-163">ومعدل الضريبة هو مجموع مبالغ الضريبة التي يتم حسابها لكل فترة مبلغ.</span><span class="sxs-lookup"><span data-stu-id="7b6e5-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="7b6e5-164">مبلغ خاضع للضريبة (السعر)</span><span class="sxs-lookup"><span data-stu-id="7b6e5-164">Taxable amount (price)</span></span> | <span data-ttu-id="7b6e5-165">حساب</span><span class="sxs-lookup"><span data-stu-id="7b6e5-165">Calculation</span></span>                                                               | <span data-ttu-id="7b6e5-166">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="7b6e5-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7b6e5-167">35.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-167">35.00</span></span>                  | <span data-ttu-id="7b6e5-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="7b6e5-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="7b6e5-169">1050</span><span class="sxs-lookup"><span data-stu-id="7b6e5-169">10.50</span></span>     |
| <span data-ttu-id="7b6e5-170">50.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-170">50.00</span></span>                  | <span data-ttu-id="7b6e5-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="7b6e5-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="7b6e5-172">15.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-172">15.00</span></span>     |
| <span data-ttu-id="7b6e5-173">85.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-173">85.00</span></span>                  | <span data-ttu-id="7b6e5-174">(50.00 \* 0.30 =‏ 15.00) + (35.00 \* ‏0.20 =‏ 7.00)</span><span class="sxs-lookup"><span data-stu-id="7b6e5-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="7b6e5-175">22.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-175">22.00</span></span>     |
| <span data-ttu-id="7b6e5-176">305.00</span><span class="sxs-lookup"><span data-stu-id="7b6e5-176">305.00</span></span>                 | <span data-ttu-id="7b6e5-177">(50.00 \* ‏0.30 =‏ 15.00) + (50.00 \* ‏0.20 =‏ 10.00) + (205 \* ‏0.10 =‏ 20.50)</span><span class="sxs-lookup"><span data-stu-id="7b6e5-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="7b6e5-178">45.50</span><span class="sxs-lookup"><span data-stu-id="7b6e5-178">45.50</span></span>     |



<span data-ttu-id="7b6e5-179">لمزيد من المعلومات، راجع [تحديد معدلات ضريبة المبيعات استنادًا إلى حقلي "القاعدة الهامشية" و"أسلوب الحساب"](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="7b6e5-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






