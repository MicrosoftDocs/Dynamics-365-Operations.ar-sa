---
title: المبلغ بالكامل وخيارات حساب الفترات لأكواد ضريبة المبيعات
description: تشرح هذه المقالة خيارات حقل أسلوب حساب على أكواد ضريبة المبيعات وكيفية حساب ضريبة المبيعات للفترات والمبالغ كاملة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0414f835b7797d2ed554f8d9dbd95b2ad47bba43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234107"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="48e0e-103">المبلغ بالكامل وخيارات حساب الفترات لأكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="48e0e-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48e0e-104">تشرح هذه المقالة خيارات حقل أسلوب حساب على أكواد ضريبة المبيعات وكيفية حساب ضريبة المبيعات للفترات والمبالغ كاملة.</span><span class="sxs-lookup"><span data-stu-id="48e0e-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="48e0e-105">يمكنك إعداد كود ضريبة مبيعات ليتم حسابه على أساس مبلغ كامل أو مبلغ فترة.</span><span class="sxs-lookup"><span data-stu-id="48e0e-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="48e0e-106">في صفحة أكواد ضريبة المبيعات، استخدام حقل طريقة الحساب في علامة التبويب السريع "الحساب" لتحديد كيفية حساب كود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="48e0e-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="48e0e-107">المبلغ الكامل – يتم تطبيق معدل الضريبة على المبلغ الخاضع للضريبة بالكامل.</span><span class="sxs-lookup"><span data-stu-id="48e0e-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="48e0e-108">الفترة – يتم تقسيم المبلغ الخاضع للضريبة إلى أجزاء، يقع كل جزء منها في نطاق يحتوي على معدل ضريبة محدد.</span><span class="sxs-lookup"><span data-stu-id="48e0e-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="48e0e-109">ويتم احتساب الضريبة على جزء المبلغ الذي يقع في فترة محددة وذلك وفقًا لمعدل الضريبة لهذه الفترة.</span><span class="sxs-lookup"><span data-stu-id="48e0e-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="48e0e-110">ومعدل الضريبة هو مجموع مبالغ الضريبة التي يتم حسابها لكل فترة مبلغ.</span><span class="sxs-lookup"><span data-stu-id="48e0e-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="48e0e-111">يتوفر خيار الفترة فقط عند تحديد بند في حقل طريقة الحساب في منطقة ضريبة المبيعات في صفحة معلمات دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="48e0e-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="48e0e-112">يتم إعداد الفواصل الزمنية في صفحة قيم أكواد ضريبة المبيعات عن طريق إدخال الحد الأدنى والحد الأقصى للمبالغ لكل معدل الضريبة.</span><span class="sxs-lookup"><span data-stu-id="48e0e-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="48e0e-113">بالنسبة للضرائب التي ينبغي حسابها على كافة المبالغ الخاضعة للضريبة، بغض النظر عن الطريقة التي يتم تحديدها، فيجب أن تتوافق الفترات مع القواعد التالية:</span><span class="sxs-lookup"><span data-stu-id="48e0e-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="48e0e-114">يجب أن تشتمل الفترة الأولى حد أدنى قيمته صفر.</span><span class="sxs-lookup"><span data-stu-id="48e0e-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="48e0e-115">يجب أن تشتمل الفترة الأخيرة على حد أقصى قيمته صفر يشير إلى اللانهاية.</span><span class="sxs-lookup"><span data-stu-id="48e0e-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="48e0e-116">يجب أن يساوي الحد الأقصى للفترة الحد الأدنى للفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="48e0e-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="48e0e-117">إذا كان المبلغ هو الحد الأقصى للفترة السابقة والحد الأدنى للفترة التالية، فسيتم تطبيق معدل ضريبة المبيعات الفترة الأولى على المبلغ.</span><span class="sxs-lookup"><span data-stu-id="48e0e-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="48e0e-118">إذا وقع المبلغ خارج الفترات المحددة وفقًا للحدين الأدنى والأعلى، فسيتم تطبيق معدل ضريبة مبيعات بمبلغ صفر.</span><span class="sxs-lookup"><span data-stu-id="48e0e-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="48e0e-119">مثال: طريقة حساب إجمالي المبلغ</span><span class="sxs-lookup"><span data-stu-id="48e0e-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="48e0e-120">في صفحة قيم أكواد ضريبة المبيعات، يتم إعداد معدلات ضريبة المبيعات في الفترات التالية:</span><span class="sxs-lookup"><span data-stu-id="48e0e-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="48e0e-121">**حد الحد الأدنى**</span><span class="sxs-lookup"><span data-stu-id="48e0e-121">**Minimum limit**</span></span> | <span data-ttu-id="48e0e-122">**الحد الأقصى**</span><span class="sxs-lookup"><span data-stu-id="48e0e-122">**Maximum limit**</span></span> | <span data-ttu-id="48e0e-123">**معدل الضريبة**</span><span class="sxs-lookup"><span data-stu-id="48e0e-123">**Tax rate**</span></span> |
| <span data-ttu-id="48e0e-124">0.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-124">0.00</span></span>              | <span data-ttu-id="48e0e-125">50.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-125">50.00</span></span>             | <span data-ttu-id="48e0e-126">30%</span><span class="sxs-lookup"><span data-stu-id="48e0e-126">30%</span></span>          |
| <span data-ttu-id="48e0e-127">50.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-127">50.00</span></span>             | <span data-ttu-id="48e0e-128">100.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-128">100.00</span></span>            | <span data-ttu-id="48e0e-129">20%</span><span class="sxs-lookup"><span data-stu-id="48e0e-129">20%</span></span>          |
| <span data-ttu-id="48e0e-130">100.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-130">100.00</span></span>            | <span data-ttu-id="48e0e-131">0.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-131">0.00</span></span>              | <span data-ttu-id="48e0e-132">10%</span><span class="sxs-lookup"><span data-stu-id="48e0e-132">10%</span></span>          |

<span data-ttu-id="48e0e-133">يتم حساب ضريبة المبيعات على إجمالي المبلغ الخاضع للضريبة.</span><span class="sxs-lookup"><span data-stu-id="48e0e-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="48e0e-134">مبلغ خاضع للضريبة (السعر)</span><span class="sxs-lookup"><span data-stu-id="48e0e-134">Taxable amount (price)</span></span> | <span data-ttu-id="48e0e-135">حساب</span><span class="sxs-lookup"><span data-stu-id="48e0e-135">Calculation</span></span>    | <span data-ttu-id="48e0e-136">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="48e0e-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="48e0e-137">35.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-137">35.00</span></span>                  | <span data-ttu-id="48e0e-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="48e0e-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="48e0e-139">1050</span><span class="sxs-lookup"><span data-stu-id="48e0e-139">10.50</span></span>     |
| <span data-ttu-id="48e0e-140">50.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-140">50.00</span></span>                  | <span data-ttu-id="48e0e-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="48e0e-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="48e0e-142">15.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-142">15.00</span></span>     |
| <span data-ttu-id="48e0e-143">85.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-143">85.00</span></span>                  | <span data-ttu-id="48e0e-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="48e0e-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="48e0e-145">17.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-145">17.00</span></span>     |
| <span data-ttu-id="48e0e-146">305.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-146">305.00</span></span>                 | <span data-ttu-id="48e0e-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="48e0e-147">305.00 \* 0.10</span></span> | <span data-ttu-id="48e0e-148">30.50</span><span class="sxs-lookup"><span data-stu-id="48e0e-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="48e0e-149">مثال: طريقة حساب الفترة</span><span class="sxs-lookup"><span data-stu-id="48e0e-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="48e0e-150">في صفحة القيم، يتم إعداد معدلات ضرائب المبيعات في الفترات التالية:</span><span class="sxs-lookup"><span data-stu-id="48e0e-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="48e0e-151">**حد الحد الأدنى**</span><span class="sxs-lookup"><span data-stu-id="48e0e-151">**Minimum limit**</span></span> | <span data-ttu-id="48e0e-152">**الحد الأقصى**</span><span class="sxs-lookup"><span data-stu-id="48e0e-152">**Maximum limit**</span></span> | <span data-ttu-id="48e0e-153">**معدل الضريبة**</span><span class="sxs-lookup"><span data-stu-id="48e0e-153">**Tax rate**</span></span> |
| <span data-ttu-id="48e0e-154">0.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-154">0.00</span></span>              | <span data-ttu-id="48e0e-155">50.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-155">50.00</span></span>             | <span data-ttu-id="48e0e-156">30%</span><span class="sxs-lookup"><span data-stu-id="48e0e-156">30%</span></span>          |
| <span data-ttu-id="48e0e-157">50.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-157">50.00</span></span>             | <span data-ttu-id="48e0e-158">100.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-158">100.00</span></span>            | <span data-ttu-id="48e0e-159">20%</span><span class="sxs-lookup"><span data-stu-id="48e0e-159">20%</span></span>          |
| <span data-ttu-id="48e0e-160">100.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-160">100.00</span></span>            | <span data-ttu-id="48e0e-161">0.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-161">0.00</span></span>              | <span data-ttu-id="48e0e-162">10%</span><span class="sxs-lookup"><span data-stu-id="48e0e-162">10%</span></span>          |

<span data-ttu-id="48e0e-163">ومعدل الضريبة هو مجموع مبالغ الضريبة التي يتم حسابها لكل فترة مبلغ.</span><span class="sxs-lookup"><span data-stu-id="48e0e-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="48e0e-164">مبلغ خاضع للضريبة (السعر)</span><span class="sxs-lookup"><span data-stu-id="48e0e-164">Taxable amount (price)</span></span> | <span data-ttu-id="48e0e-165">حساب</span><span class="sxs-lookup"><span data-stu-id="48e0e-165">Calculation</span></span>                                                               | <span data-ttu-id="48e0e-166">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="48e0e-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="48e0e-167">35.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-167">35.00</span></span>                  | <span data-ttu-id="48e0e-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="48e0e-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="48e0e-169">1050</span><span class="sxs-lookup"><span data-stu-id="48e0e-169">10.50</span></span>     |
| <span data-ttu-id="48e0e-170">50.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-170">50.00</span></span>                  | <span data-ttu-id="48e0e-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="48e0e-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="48e0e-172">15.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-172">15.00</span></span>     |
| <span data-ttu-id="48e0e-173">85.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-173">85.00</span></span>                  | <span data-ttu-id="48e0e-174">(50.00 \* 0.30 =‏ 15.00) + (35.00 \* ‏0.20 =‏ 7.00)</span><span class="sxs-lookup"><span data-stu-id="48e0e-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="48e0e-175">22.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-175">22.00</span></span>     |
| <span data-ttu-id="48e0e-176">305.00</span><span class="sxs-lookup"><span data-stu-id="48e0e-176">305.00</span></span>                 | <span data-ttu-id="48e0e-177">(50.00 \* ‏0.30 =‏ 15.00) + (50.00 \* ‏0.20 =‏ 10.00) + (205 \* ‏0.10 =‏ 20.50)</span><span class="sxs-lookup"><span data-stu-id="48e0e-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="48e0e-178">45.50</span><span class="sxs-lookup"><span data-stu-id="48e0e-178">45.50</span></span>     |



<span data-ttu-id="48e0e-179">لمزيد من المعلومات، راجع [تحديد معدلات ضريبة المبيعات استنادًا إلى حقلي "القاعدة الهامشية" وأساليب الحساب](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="48e0e-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]