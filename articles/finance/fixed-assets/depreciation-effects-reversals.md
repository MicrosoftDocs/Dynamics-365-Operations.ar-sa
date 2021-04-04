---
title: آثار الإهلاك مع عمليات الإلغاء
description: تتناول هذه المقالة الآثار المحتملة لعكس حركة أصول ثابتة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4952f94d635a9c9cdc7892e6cc142cfe4d526e44
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241200"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="6fd37-103">آثار الإهلاك مع عمليات الإلغاء</span><span class="sxs-lookup"><span data-stu-id="6fd37-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fd37-104">تتناول هذه المقالة الآثار المحتملة لعكس حركة أصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="6fd37-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="6fd37-105">يمكنك إلغاء حركات الأصول الثابتة والحركات المقترنة بالأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="6fd37-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="6fd37-106">كما يمكنك إبطال حركة ملغاة.</span><span class="sxs-lookup"><span data-stu-id="6fd37-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="6fd37-107">ويمكنك إلغاء أو إبطال حركة لم تكن الحركة الأحدث التي تم ترحيلها إلى دفتر الأصل.</span><span class="sxs-lookup"><span data-stu-id="6fd37-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="6fd37-108">ويجب أولاً تحديد ما إذا كان تم ترحيل أية حركات إهلاك بعد الحركة التي تقوم بإلغائها.</span><span class="sxs-lookup"><span data-stu-id="6fd37-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="6fd37-109">وهذا هو سبب عدم إعادة حساب الإهلاك عند إلغاء حركة.</span><span class="sxs-lookup"><span data-stu-id="6fd37-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="6fd37-110">ولذلك، غالبًا ما تتم المبالغة في الإهلاك أو تقليله بعد الإلغاء، كما هو موضح في الأمثلة.</span><span class="sxs-lookup"><span data-stu-id="6fd37-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="6fd37-111">ولضمان صحة الإهلاك عند إلغاء الحركة، لا تستمر في عملية الإلغاء في حالة تلقي رسالة تفيد بأن الإهلاك لن تتم إعادة حسابه.</span><span class="sxs-lookup"><span data-stu-id="6fd37-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="6fd37-112">ولكن قم أولاً بإلغاء حركة الإهلاك التي تم ترحيلها بعد الحركة التي حاولت إلغائها، ثم استمر في عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="6fd37-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="6fd37-113">ولن تتلقى أية تحذيرات حول إعادة حساب الإهلاك، ويمكنك متابعة عملية الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="6fd37-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="6fd37-114">توضح الأمثلة التالية عمليات الحساب التي تتم في حالة المتابعة وتجاهل الرسالة دون إلغاء حركات الإهلاك أولاً.</span><span class="sxs-lookup"><span data-stu-id="6fd37-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="6fd37-115"> المثال 1: المبالغة في الإهلاك</span><span class="sxs-lookup"><span data-stu-id="6fd37-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="6fd37-116">يتم إعداد أحد الأصول بعمر افتراضي يصل إلى خمس سنوات والإهلاك بأقساط ثابتة (60 فترة إهلاك).</span><span class="sxs-lookup"><span data-stu-id="6fd37-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6fd37-117">ويتم في هذا المثال مبالغة الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="6fd37-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6fd37-118">سجل حركة الأصول</span><span class="sxs-lookup"><span data-stu-id="6fd37-118">Asset transaction history</span></span>

| <span data-ttu-id="6fd37-119">التاريخ</span><span class="sxs-lookup"><span data-stu-id="6fd37-119">Date</span></span>       | <span data-ttu-id="6fd37-120">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="6fd37-120">Transaction type</span></span>                                                          | <span data-ttu-id="6fd37-121">مبلغ</span><span class="sxs-lookup"><span data-stu-id="6fd37-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6fd37-122">1 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-122">January 1</span></span>  | <span data-ttu-id="6fd37-123">الامتلاك</span><span class="sxs-lookup"><span data-stu-id="6fd37-123">Acquisition</span></span>                                                               | <span data-ttu-id="6fd37-124">59000.00</span><span class="sxs-lookup"><span data-stu-id="6fd37-124">59,000.00</span></span>                                 |
| <span data-ttu-id="6fd37-125">1 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-125">January 1</span></span>  | <span data-ttu-id="6fd37-126">تسوية الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="6fd37-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="6fd37-127">1000.00</span><span class="sxs-lookup"><span data-stu-id="6fd37-127">1,000.00</span></span>                                  |
| <span data-ttu-id="6fd37-128">31 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-128">January 31</span></span> | <span data-ttu-id="6fd37-129">الإهلاك (تم إنشاؤه باستخدام مُقترح لفترة واحدة من فترات الإهلاك)</span><span class="sxs-lookup"><span data-stu-id="6fd37-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6fd37-130">عملية حساب 1000.00: القيمة الدفترية (59000 + 1000) / عدد فترات الإهلاك المتبقية (60)</span><span class="sxs-lookup"><span data-stu-id="6fd37-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6fd37-131">إجراء الإلغاء</span><span class="sxs-lookup"><span data-stu-id="6fd37-131">Reversal action</span></span>

| <span data-ttu-id="6fd37-132">التاريخ</span><span class="sxs-lookup"><span data-stu-id="6fd37-132">Date</span></span>      | <span data-ttu-id="6fd37-133">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="6fd37-133">Transaction type</span></span>                | <span data-ttu-id="6fd37-134">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6fd37-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="6fd37-135">1 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-135">January 1</span></span> | <span data-ttu-id="6fd37-136">إلغاء تسوية قيمة الامتلاك</span><span class="sxs-lookup"><span data-stu-id="6fd37-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="6fd37-137">–1000.00</span><span class="sxs-lookup"><span data-stu-id="6fd37-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6fd37-138">أثر الإهلاك</span><span class="sxs-lookup"><span data-stu-id="6fd37-138">Depreciation effect</span></span>

| <span data-ttu-id="6fd37-139">التاريخ</span><span class="sxs-lookup"><span data-stu-id="6fd37-139">Date</span></span>        | <span data-ttu-id="6fd37-140">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="6fd37-140">Transaction type</span></span>        | <span data-ttu-id="6fd37-141">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6fd37-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd37-142">28 فبراير</span><span class="sxs-lookup"><span data-stu-id="6fd37-142">February 28</span></span> | <span data-ttu-id="6fd37-143">الإهلاك (اقتراح)</span><span class="sxs-lookup"><span data-stu-id="6fd37-143">Depreciation (proposal)</span></span> | <span data-ttu-id="6fd37-144">عملية حساب 983.05: القيمة الدفترية (95000 - 1000 إهلاك) / عدد فترات الإهلاك المتبقية (59)</span><span class="sxs-lookup"><span data-stu-id="6fd37-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6fd37-145">تمت مبالغة الإهلاك بمقدار 16.95 (1000 - 983.05).</span><span class="sxs-lookup"><span data-stu-id="6fd37-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="6fd37-146"> المثال رقم 2: يتم تقليل الإهلاك</span><span class="sxs-lookup"><span data-stu-id="6fd37-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="6fd37-147">يتم إعداد أحد الأصول بعمر افتراضي يصل إلى خمس سنوات والإهلاك بأقساط ثابتة (60 فترة إهلاك).</span><span class="sxs-lookup"><span data-stu-id="6fd37-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6fd37-148">ويتم في هذا المثال تقليل الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="6fd37-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6fd37-149">سجل حركة الأصول</span><span class="sxs-lookup"><span data-stu-id="6fd37-149">Asset transaction history</span></span>

| <span data-ttu-id="6fd37-150">التاريخ</span><span class="sxs-lookup"><span data-stu-id="6fd37-150">Date</span></span>       | <span data-ttu-id="6fd37-151">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="6fd37-151">Transaction type</span></span>                                                          | <span data-ttu-id="6fd37-152">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6fd37-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="6fd37-153">1 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-153">January 1</span></span>  | <span data-ttu-id="6fd37-154">الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="6fd37-154">Acquisition</span></span>                                                               | <span data-ttu-id="6fd37-155">59000.00</span><span class="sxs-lookup"><span data-stu-id="6fd37-155">59,000.00</span></span>                                   |
| <span data-ttu-id="6fd37-156">1 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-156">January 1</span></span>  | <span data-ttu-id="6fd37-157">تسوية بالنقصان</span><span class="sxs-lookup"><span data-stu-id="6fd37-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="6fd37-158">1000.00</span><span class="sxs-lookup"><span data-stu-id="6fd37-158">1,000.00</span></span>                                    |
| <span data-ttu-id="6fd37-159">31 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-159">January 31</span></span> | <span data-ttu-id="6fd37-160">الإهلاك (تم إنشاؤه باستخدام مُقترح لفترة واحدة من فترات الإهلاك)</span><span class="sxs-lookup"><span data-stu-id="6fd37-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6fd37-161">عملية حساب 966.67: القيمة الدفترية (59000 - 1000) / عدد فترات الإهلاك المتبقية (60)</span><span class="sxs-lookup"><span data-stu-id="6fd37-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6fd37-162">إجراء الإلغاء</span><span class="sxs-lookup"><span data-stu-id="6fd37-162">Reversal action</span></span>

| <span data-ttu-id="6fd37-163">التاريخ</span><span class="sxs-lookup"><span data-stu-id="6fd37-163">Date</span></span>      | <span data-ttu-id="6fd37-164">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="6fd37-164">Transaction type</span></span>               | <span data-ttu-id="6fd37-165">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6fd37-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="6fd37-166">1 يناير</span><span class="sxs-lookup"><span data-stu-id="6fd37-166">January 1</span></span> | <span data-ttu-id="6fd37-167">إلغاء التسوية بالنقصان</span><span class="sxs-lookup"><span data-stu-id="6fd37-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="6fd37-168">–1000.00</span><span class="sxs-lookup"><span data-stu-id="6fd37-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6fd37-169">أثر الإهلاك</span><span class="sxs-lookup"><span data-stu-id="6fd37-169">Depreciation effect</span></span>

| <span data-ttu-id="6fd37-170">التاريخ</span><span class="sxs-lookup"><span data-stu-id="6fd37-170">Date</span></span>        | <span data-ttu-id="6fd37-171">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="6fd37-171">Transaction type</span></span>        | <span data-ttu-id="6fd37-172">المبلغ</span><span class="sxs-lookup"><span data-stu-id="6fd37-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd37-173">28 فبراير</span><span class="sxs-lookup"><span data-stu-id="6fd37-173">February 28</span></span> | <span data-ttu-id="6fd37-174">الإهلاك (اقتراح)</span><span class="sxs-lookup"><span data-stu-id="6fd37-174">Depreciation (proposal)</span></span> | <span data-ttu-id="6fd37-175">عملية حساب 983.62: القيمة الدفترية (إهلاك 59000 - 966.67) / عدد فترات الإهلاك المتبقية (59)</span><span class="sxs-lookup"><span data-stu-id="6fd37-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6fd37-176">يتم تقليل الإهلاك بمقدار 16.95 (983.62 - 966.67).</span><span class="sxs-lookup"><span data-stu-id="6fd37-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="6fd37-177">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6fd37-177">Additional resources</span></span>
--------

[<span data-ttu-id="6fd37-178">إهلاك الأصل الثابت</span><span class="sxs-lookup"><span data-stu-id="6fd37-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]