---
title: "إعادة تقييم العملة في شركة تجميع"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="e0a73-102">إعادة تقييم العملة في شركة تجميع</span><span class="sxs-lookup"><span data-stu-id="e0a73-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="e0a73-103">عند تجميع بيانات من عملة محاسبة واحدة إلى أخرى، يمكنك الاستمرار في تشغيل إعادة تقييم العملة إذا لم يكن هناك تغيير أسعار الصرف، بحيث يُعاد تقييم أرصدة الحساب الخاص بك بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="e0a73-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="e0a73-104">وعندما تقوم بتجميع البيانات أصلاً، استخدم علامة التبويب **تحويل العملة** لتحديد أسعار الصرف الأولية للتحويل أثناء عملية التجميع.</span><span class="sxs-lookup"><span data-stu-id="e0a73-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="e0a73-105">وبعد إدخال سعر صرف جديد (على سبيل المثال، في الشهر التالي)، يجب عليك إعادة تقييم أرصدة الحسابات.</span><span class="sxs-lookup"><span data-stu-id="e0a73-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="e0a73-106">ويتم فيما بعد تحديث الأرباح أو الخسائر تبعاً لذلك، على أساس سعر الصرف الجديد والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="e0a73-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="e0a73-107">يوضح المثال التالي الإدخالات المحاسبية التي تم إنشاؤها أثناء العملية.</span><span class="sxs-lookup"><span data-stu-id="e0a73-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="e0a73-108">إعداد الشركة</span><span class="sxs-lookup"><span data-stu-id="e0a73-108">Company setup</span></span>
-   <span data-ttu-id="e0a73-109">**شركة التشغيل/المصدر (USMF)** – يتم استخدام الدولارات الأمريكية (USD) كعملة للمحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="e0a73-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="e0a73-110">**الشركة المجمعة (CON)** – يتم استخدام اليورو (EUR) كعلمة للمحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="e0a73-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="e0a73-111">**الأرباح المحققة **– حساب دفتر الأستاذ 801500</span><span class="sxs-lookup"><span data-stu-id="e0a73-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="e0a73-112">**الخسائر المحققة**– حساب دفتر الأستاذ 801600</span><span class="sxs-lookup"><span data-stu-id="e0a73-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="e0a73-113">**الأرباح غير المحققة**– حساب دفتر الأستاذ 801600</span><span class="sxs-lookup"><span data-stu-id="e0a73-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="e0a73-114">**الخسائر غير المحققة**– حساب دفتر الأستاذ 801400</span><span class="sxs-lookup"><span data-stu-id="e0a73-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="e0a73-115">الحركات الأصلية</span><span class="sxs-lookup"><span data-stu-id="e0a73-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="e0a73-116">حركات إيصال استلام النقدية في USMF</span><span class="sxs-lookup"><span data-stu-id="e0a73-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="e0a73-117">التاريخ</span><span class="sxs-lookup"><span data-stu-id="e0a73-117">Date</span></span>       | <span data-ttu-id="e0a73-118">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e0a73-118">Ledger account</span></span>               | <span data-ttu-id="e0a73-119">عملة</span><span class="sxs-lookup"><span data-stu-id="e0a73-119">Currency</span></span> | <span data-ttu-id="e0a73-120">المبلغ</span><span class="sxs-lookup"><span data-stu-id="e0a73-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="e0a73-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-121">10/11/2015</span></span> | <span data-ttu-id="e0a73-122">110110 – نقد</span><span class="sxs-lookup"><span data-stu-id="e0a73-122">110110 – Cash</span></span>                | <span data-ttu-id="e0a73-123">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="e0a73-123">USD</span></span>      | <span data-ttu-id="e0a73-124">500</span><span class="sxs-lookup"><span data-stu-id="e0a73-124">500</span></span>    |
| <span data-ttu-id="e0a73-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-125">10/11/2015</span></span> | <span data-ttu-id="e0a73-126">130100 – الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="e0a73-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="e0a73-127">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="e0a73-127">USD</span></span>      | <span data-ttu-id="e0a73-128">-500</span><span class="sxs-lookup"><span data-stu-id="e0a73-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="e0a73-129">أسعار الصرف</span><span class="sxs-lookup"><span data-stu-id="e0a73-129">Exchange rates</span></span>
| <span data-ttu-id="e0a73-130">من العملة</span><span class="sxs-lookup"><span data-stu-id="e0a73-130">From currency</span></span> | <span data-ttu-id="e0a73-131">إلى العملة</span><span class="sxs-lookup"><span data-stu-id="e0a73-131">To currency</span></span> | <span data-ttu-id="e0a73-132">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="e0a73-132">Start date</span></span> | <span data-ttu-id="e0a73-133">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="e0a73-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="e0a73-134">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-134">EUR</span></span>           | <span data-ttu-id="e0a73-135">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="e0a73-135">USD</span></span>         | <span data-ttu-id="e0a73-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-136">10/1/2015</span></span>  | <span data-ttu-id="e0a73-137">200</span><span class="sxs-lookup"><span data-stu-id="e0a73-137">200</span></span>           |
| <span data-ttu-id="e0a73-138">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-138">EUR</span></span>           | <span data-ttu-id="e0a73-139">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="e0a73-139">USD</span></span>         | <span data-ttu-id="e0a73-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-140">11/1/2015</span></span>  | <span data-ttu-id="e0a73-141">150</span><span class="sxs-lookup"><span data-stu-id="e0a73-141">150</span></span>           |
| <span data-ttu-id="e0a73-142">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-142">EUR</span></span>           | <span data-ttu-id="e0a73-143">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="e0a73-143">USD</span></span>         | <span data-ttu-id="e0a73-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="e0a73-144">12/1/2012</span></span>  | <span data-ttu-id="e0a73-145">100</span><span class="sxs-lookup"><span data-stu-id="e0a73-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="e0a73-146">إجراء التجميع لأكتوبر 2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e0a73-147">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="e0a73-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="e0a73-148">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e0a73-148">Ledger account</span></span> | <span data-ttu-id="e0a73-149">عملة</span><span class="sxs-lookup"><span data-stu-id="e0a73-149">Currency</span></span> | <span data-ttu-id="e0a73-150">المبلغ</span><span class="sxs-lookup"><span data-stu-id="e0a73-150">Amount</span></span> | <span data-ttu-id="e0a73-151">الحساب</span><span class="sxs-lookup"><span data-stu-id="e0a73-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="e0a73-152">110110</span><span class="sxs-lookup"><span data-stu-id="e0a73-152">110110</span></span>         | <span data-ttu-id="e0a73-153">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-153">EUR</span></span>      | <span data-ttu-id="e0a73-154">250</span><span class="sxs-lookup"><span data-stu-id="e0a73-154">250</span></span>    | <span data-ttu-id="e0a73-155">500 دولار أمريكي × 50%</span><span class="sxs-lookup"><span data-stu-id="e0a73-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="e0a73-156">130100</span><span class="sxs-lookup"><span data-stu-id="e0a73-156">130100</span></span>         | <span data-ttu-id="e0a73-157">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-157">EUR</span></span>      | <span data-ttu-id="e0a73-158">-250</span><span class="sxs-lookup"><span data-stu-id="e0a73-158">-250</span></span>   | <span data-ttu-id="e0a73-159">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="e0a73-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="e0a73-160">إجراء إعادة تقييم العملة للحسابات من 1 تشرين الأول/أكتوبر 2015 حتى 30 تشرين الثاني/نوفمبر عام 2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e0a73-161">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="e0a73-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="e0a73-162">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e0a73-162">Ledger account</span></span> | <span data-ttu-id="e0a73-163">عملة</span><span class="sxs-lookup"><span data-stu-id="e0a73-163">Currency</span></span> | <span data-ttu-id="e0a73-164">المبلغ</span><span class="sxs-lookup"><span data-stu-id="e0a73-164">Amount</span></span>  | <span data-ttu-id="e0a73-165">الحساب</span><span class="sxs-lookup"><span data-stu-id="e0a73-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="e0a73-166">110110</span><span class="sxs-lookup"><span data-stu-id="e0a73-166">110110</span></span>         | <span data-ttu-id="e0a73-167">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-167">EUR</span></span>      | <span data-ttu-id="e0a73-168">333.33</span><span class="sxs-lookup"><span data-stu-id="e0a73-168">333.33</span></span>  | <span data-ttu-id="e0a73-169">المبلغ الأصلي 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="e0a73-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="e0a73-170">130100</span><span class="sxs-lookup"><span data-stu-id="e0a73-170">130100</span></span>         | <span data-ttu-id="e0a73-171">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-171">EUR</span></span>      | <span data-ttu-id="e0a73-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="e0a73-172">-333.33</span></span> | <span data-ttu-id="e0a73-173">المبلغ الأصلي -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="e0a73-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="e0a73-174">801400</span><span class="sxs-lookup"><span data-stu-id="e0a73-174">801400</span></span>         | <span data-ttu-id="e0a73-175">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-175">EUR</span></span>      | <span data-ttu-id="e0a73-176">83.33</span><span class="sxs-lookup"><span data-stu-id="e0a73-176">83.33</span></span>   | <span data-ttu-id="e0a73-177">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="e0a73-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="e0a73-178">801600</span><span class="sxs-lookup"><span data-stu-id="e0a73-178">801600</span></span>         | <span data-ttu-id="e0a73-179">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-179">EUR</span></span>      | <span data-ttu-id="e0a73-180">-83.33</span><span class="sxs-lookup"><span data-stu-id="e0a73-180">-83.33</span></span>  | <span data-ttu-id="e0a73-181">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="e0a73-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="e0a73-182">سوف تشاهد حركات إضافية للعملات المشمولة بالتقرير.</span><span class="sxs-lookup"><span data-stu-id="e0a73-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="e0a73-183">إجراء إعادة تقييم العملة للحسابات من 1 تشرين الأول/أكتوبر 2015 حتى 31 تشرين الأول/ديسمبر عام 2015</span><span class="sxs-lookup"><span data-stu-id="e0a73-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e0a73-184">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="e0a73-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="e0a73-185">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e0a73-185">Ledger account</span></span> | <span data-ttu-id="e0a73-186">عملة</span><span class="sxs-lookup"><span data-stu-id="e0a73-186">Currency</span></span> | <span data-ttu-id="e0a73-187">المبلغ</span><span class="sxs-lookup"><span data-stu-id="e0a73-187">Amount</span></span>  | <span data-ttu-id="e0a73-188">الحساب</span><span class="sxs-lookup"><span data-stu-id="e0a73-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="e0a73-189">110110</span><span class="sxs-lookup"><span data-stu-id="e0a73-189">110110</span></span>         | <span data-ttu-id="e0a73-190">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-190">EUR</span></span>      | <span data-ttu-id="e0a73-191">500.00</span><span class="sxs-lookup"><span data-stu-id="e0a73-191">500.00</span></span>  | <span data-ttu-id="e0a73-192">المبلغ الأصلي 500 × 1</span><span class="sxs-lookup"><span data-stu-id="e0a73-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="e0a73-193">130100</span><span class="sxs-lookup"><span data-stu-id="e0a73-193">130100</span></span>         | <span data-ttu-id="e0a73-194">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-194">EUR</span></span>      | <span data-ttu-id="e0a73-195">-500.00</span><span class="sxs-lookup"><span data-stu-id="e0a73-195">-500.00</span></span> | <span data-ttu-id="e0a73-196">المبلغ الأصلي -500 × 1</span><span class="sxs-lookup"><span data-stu-id="e0a73-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="e0a73-197">801400</span><span class="sxs-lookup"><span data-stu-id="e0a73-197">801400</span></span>         | <span data-ttu-id="e0a73-198">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-198">EUR</span></span>      | <span data-ttu-id="e0a73-199">250</span><span class="sxs-lookup"><span data-stu-id="e0a73-199">250</span></span>     | <span data-ttu-id="e0a73-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="e0a73-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="e0a73-201">801600</span><span class="sxs-lookup"><span data-stu-id="e0a73-201">801600</span></span>         | <span data-ttu-id="e0a73-202">يورو</span><span class="sxs-lookup"><span data-stu-id="e0a73-202">EUR</span></span>      | <span data-ttu-id="e0a73-203">-250</span><span class="sxs-lookup"><span data-stu-id="e0a73-203">-250</span></span>    | <span data-ttu-id="e0a73-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="e0a73-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






