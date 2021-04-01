---
title: إعادة تقييم العملة في شركة تجميع
description: يصف هذا الموضوع كيفية إعادة تقييم العملة في شركة تجميع.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212219"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="5094e-103">إعادة تقييم العملة في شركة تجميع</span><span class="sxs-lookup"><span data-stu-id="5094e-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5094e-104">عند تجميع بيانات من عملة محاسبة واحدة إلى أخرى، يمكنك الاستمرار في تشغيل إعادة تقييم العملة إذا لم يكن هناك تغيير أسعار الصرف، بحيث يُعاد تقييم أرصدة الحساب الخاص بك بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="5094e-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="5094e-105">وعندما تقوم بتجميع البيانات أصلاً، استخدم علامة التبويب **تحويل العملة** لتحديد أسعار الصرف الأولية للتحويل أثناء عملية التجميع.</span><span class="sxs-lookup"><span data-stu-id="5094e-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="5094e-106">وبعد إدخال سعر صرف جديد (على سبيل المثال، في الشهر التالي)، يجب عليك إعادة تقييم أرصدة الحسابات.</span><span class="sxs-lookup"><span data-stu-id="5094e-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="5094e-107">ويتم فيما بعد تحديث الأرباح أو الخسائر تبعاً لذلك، على أساس سعر الصرف الجديد والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="5094e-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="5094e-108">يوضح المثال التالي الإدخالات المحاسبية التي تم إنشاؤها أثناء العملية.</span><span class="sxs-lookup"><span data-stu-id="5094e-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="5094e-109">إعداد الشركة</span><span class="sxs-lookup"><span data-stu-id="5094e-109">Company setup</span></span>
-   <span data-ttu-id="5094e-110">**شركة التشغيل/المصدر (USMF)** – يتم استخدام الدولارات الأمريكية (USD) كعملة للمحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="5094e-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="5094e-111">**الشركة المجمعة (CON)** – يتم استخدام اليورو (EUR) كعلمة للمحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="5094e-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="5094e-112">**الأرباح المحققة** – حساب دفتر الأستاذ 801500</span><span class="sxs-lookup"><span data-stu-id="5094e-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="5094e-113">**الخسائر المحققة** – حساب دفتر الأستاذ 801600</span><span class="sxs-lookup"><span data-stu-id="5094e-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5094e-114">**الأرباح غير المحققة**– حساب دفتر الأستاذ 801600</span><span class="sxs-lookup"><span data-stu-id="5094e-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5094e-115">**الخسائر غير المحققة**– حساب دفتر الأستاذ 801400</span><span class="sxs-lookup"><span data-stu-id="5094e-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="5094e-116">الحركات الأصلية</span><span class="sxs-lookup"><span data-stu-id="5094e-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="5094e-117">حركات إيصال استلام النقدية في USMF</span><span class="sxs-lookup"><span data-stu-id="5094e-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="5094e-118">التاريخ</span><span class="sxs-lookup"><span data-stu-id="5094e-118">Date</span></span>       | <span data-ttu-id="5094e-119">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="5094e-119">Ledger account</span></span>               | <span data-ttu-id="5094e-120">عملة</span><span class="sxs-lookup"><span data-stu-id="5094e-120">Currency</span></span> | <span data-ttu-id="5094e-121">المبلغ</span><span class="sxs-lookup"><span data-stu-id="5094e-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="5094e-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="5094e-122">10/11/2015</span></span> | <span data-ttu-id="5094e-123">110110 – نقد</span><span class="sxs-lookup"><span data-stu-id="5094e-123">110110 – Cash</span></span>                | <span data-ttu-id="5094e-124">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="5094e-124">USD</span></span>      | <span data-ttu-id="5094e-125">500</span><span class="sxs-lookup"><span data-stu-id="5094e-125">500</span></span>    |
| <span data-ttu-id="5094e-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="5094e-126">10/11/2015</span></span> | <span data-ttu-id="5094e-127">130100 – الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="5094e-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="5094e-128">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="5094e-128">USD</span></span>      | <span data-ttu-id="5094e-129">-500</span><span class="sxs-lookup"><span data-stu-id="5094e-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="5094e-130">أسعار الصرف</span><span class="sxs-lookup"><span data-stu-id="5094e-130">Exchange rates</span></span>

| <span data-ttu-id="5094e-131">من العملة</span><span class="sxs-lookup"><span data-stu-id="5094e-131">From currency</span></span> | <span data-ttu-id="5094e-132">إلى العملة</span><span class="sxs-lookup"><span data-stu-id="5094e-132">To currency</span></span> | <span data-ttu-id="5094e-133">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="5094e-133">Start date</span></span> | <span data-ttu-id="5094e-134">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="5094e-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="5094e-135">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-135">EUR</span></span>           | <span data-ttu-id="5094e-136">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="5094e-136">USD</span></span>         | <span data-ttu-id="5094e-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="5094e-137">10/1/2015</span></span>  | <span data-ttu-id="5094e-138">200</span><span class="sxs-lookup"><span data-stu-id="5094e-138">200</span></span>           |
| <span data-ttu-id="5094e-139">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-139">EUR</span></span>           | <span data-ttu-id="5094e-140">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="5094e-140">USD</span></span>         | <span data-ttu-id="5094e-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="5094e-141">11/1/2015</span></span>  | <span data-ttu-id="5094e-142">150</span><span class="sxs-lookup"><span data-stu-id="5094e-142">150</span></span>           |
| <span data-ttu-id="5094e-143">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-143">EUR</span></span>           | <span data-ttu-id="5094e-144">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="5094e-144">USD</span></span>         | <span data-ttu-id="5094e-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="5094e-145">12/1/2012</span></span>  | <span data-ttu-id="5094e-146">100</span><span class="sxs-lookup"><span data-stu-id="5094e-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="5094e-147">إجراء التجميع لأكتوبر 2015</span><span class="sxs-lookup"><span data-stu-id="5094e-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5094e-148">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="5094e-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="5094e-149">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="5094e-149">Ledger account</span></span> | <span data-ttu-id="5094e-150">عملة</span><span class="sxs-lookup"><span data-stu-id="5094e-150">Currency</span></span> | <span data-ttu-id="5094e-151">المبلغ</span><span class="sxs-lookup"><span data-stu-id="5094e-151">Amount</span></span> | <span data-ttu-id="5094e-152">الحساب</span><span class="sxs-lookup"><span data-stu-id="5094e-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="5094e-153">110110</span><span class="sxs-lookup"><span data-stu-id="5094e-153">110110</span></span>         | <span data-ttu-id="5094e-154">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-154">EUR</span></span>      | <span data-ttu-id="5094e-155">250</span><span class="sxs-lookup"><span data-stu-id="5094e-155">250</span></span>    | <span data-ttu-id="5094e-156">500 دولار أمريكي × 50%</span><span class="sxs-lookup"><span data-stu-id="5094e-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="5094e-157">130100</span><span class="sxs-lookup"><span data-stu-id="5094e-157">130100</span></span>         | <span data-ttu-id="5094e-158">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-158">EUR</span></span>      | <span data-ttu-id="5094e-159">-250</span><span class="sxs-lookup"><span data-stu-id="5094e-159">-250</span></span>   | <span data-ttu-id="5094e-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="5094e-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="5094e-161">إجراء إعادة تقييم العملة للحسابات من 1 تشرين الأول/أكتوبر 2015 حتى 30 تشرين الثاني/نوفمبر عام 2015</span><span class="sxs-lookup"><span data-stu-id="5094e-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5094e-162">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="5094e-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="5094e-163">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="5094e-163">Ledger account</span></span> | <span data-ttu-id="5094e-164">عملة</span><span class="sxs-lookup"><span data-stu-id="5094e-164">Currency</span></span> | <span data-ttu-id="5094e-165">المبلغ</span><span class="sxs-lookup"><span data-stu-id="5094e-165">Amount</span></span>  | <span data-ttu-id="5094e-166">الحساب</span><span class="sxs-lookup"><span data-stu-id="5094e-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="5094e-167">110110</span><span class="sxs-lookup"><span data-stu-id="5094e-167">110110</span></span>         | <span data-ttu-id="5094e-168">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-168">EUR</span></span>      | <span data-ttu-id="5094e-169">333.33</span><span class="sxs-lookup"><span data-stu-id="5094e-169">333.33</span></span>  | <span data-ttu-id="5094e-170">المبلغ الأصلي 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="5094e-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="5094e-171">130100</span><span class="sxs-lookup"><span data-stu-id="5094e-171">130100</span></span>         | <span data-ttu-id="5094e-172">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-172">EUR</span></span>      | <span data-ttu-id="5094e-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="5094e-173">-333.33</span></span> | <span data-ttu-id="5094e-174">المبلغ الأصلي -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="5094e-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="5094e-175">801400</span><span class="sxs-lookup"><span data-stu-id="5094e-175">801400</span></span>         | <span data-ttu-id="5094e-176">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-176">EUR</span></span>      | <span data-ttu-id="5094e-177">83.33</span><span class="sxs-lookup"><span data-stu-id="5094e-177">83.33</span></span>   | <span data-ttu-id="5094e-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="5094e-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="5094e-179">801600</span><span class="sxs-lookup"><span data-stu-id="5094e-179">801600</span></span>         | <span data-ttu-id="5094e-180">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-180">EUR</span></span>      | <span data-ttu-id="5094e-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="5094e-181">-83.33</span></span>  | <span data-ttu-id="5094e-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="5094e-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="5094e-183">سوف تشاهد حركات إضافية للعملات المشمولة بالتقرير.</span><span class="sxs-lookup"><span data-stu-id="5094e-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="5094e-184">إجراء إعادة تقييم العملة للحسابات من 1 تشرين الأول/أكتوبر 2015 حتى 31 تشرين الأول/ديسمبر عام 2015</span><span class="sxs-lookup"><span data-stu-id="5094e-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5094e-185">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="5094e-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="5094e-186">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="5094e-186">Ledger account</span></span> | <span data-ttu-id="5094e-187">عملة</span><span class="sxs-lookup"><span data-stu-id="5094e-187">Currency</span></span> | <span data-ttu-id="5094e-188">المبلغ</span><span class="sxs-lookup"><span data-stu-id="5094e-188">Amount</span></span>  | <span data-ttu-id="5094e-189">الحساب</span><span class="sxs-lookup"><span data-stu-id="5094e-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="5094e-190">110110</span><span class="sxs-lookup"><span data-stu-id="5094e-190">110110</span></span>         | <span data-ttu-id="5094e-191">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-191">EUR</span></span>      | <span data-ttu-id="5094e-192">500.00</span><span class="sxs-lookup"><span data-stu-id="5094e-192">500.00</span></span>  | <span data-ttu-id="5094e-193">المبلغ الأصلي 500 × 1</span><span class="sxs-lookup"><span data-stu-id="5094e-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="5094e-194">130100</span><span class="sxs-lookup"><span data-stu-id="5094e-194">130100</span></span>         | <span data-ttu-id="5094e-195">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-195">EUR</span></span>      | <span data-ttu-id="5094e-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="5094e-196">-500.00</span></span> | <span data-ttu-id="5094e-197">المبلغ الأصلي -500 × 1</span><span class="sxs-lookup"><span data-stu-id="5094e-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="5094e-198">801400</span><span class="sxs-lookup"><span data-stu-id="5094e-198">801400</span></span>         | <span data-ttu-id="5094e-199">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-199">EUR</span></span>      | <span data-ttu-id="5094e-200">250</span><span class="sxs-lookup"><span data-stu-id="5094e-200">250</span></span>     | <span data-ttu-id="5094e-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="5094e-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="5094e-202">801600</span><span class="sxs-lookup"><span data-stu-id="5094e-202">801600</span></span>         | <span data-ttu-id="5094e-203">يورو</span><span class="sxs-lookup"><span data-stu-id="5094e-203">EUR</span></span>      | <span data-ttu-id="5094e-204">-250</span><span class="sxs-lookup"><span data-stu-id="5094e-204">-250</span></span>    | <span data-ttu-id="5094e-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="5094e-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]