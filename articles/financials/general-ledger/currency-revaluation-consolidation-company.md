---
title: إعادة تقييم العملة في شركة تجميع
description: يصف هذا الموضوع كيفية إعادة تقييم العملة في شركة تجميع.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "338741"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="51212-103">إعادة تقييم العملة في شركة تجميع</span><span class="sxs-lookup"><span data-stu-id="51212-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51212-104">عند تجميع بيانات من عملة محاسبة واحدة إلى أخرى، يمكنك الاستمرار في تشغيل إعادة تقييم العملة إذا لم يكن هناك تغيير أسعار الصرف، بحيث يُعاد تقييم أرصدة الحساب الخاص بك بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="51212-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="51212-105">وعندما تقوم بتجميع البيانات أصلاً، استخدم علامة التبويب **تحويل العملة** لتحديد أسعار الصرف الأولية للتحويل أثناء عملية التجميع.</span><span class="sxs-lookup"><span data-stu-id="51212-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="51212-106">وبعد إدخال سعر صرف جديد (على سبيل المثال، في الشهر التالي)، يجب عليك إعادة تقييم أرصدة الحسابات.</span><span class="sxs-lookup"><span data-stu-id="51212-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="51212-107">ويتم فيما بعد تحديث الأرباح أو الخسائر تبعاً لذلك، على أساس سعر الصرف الجديد والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="51212-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="51212-108">يوضح المثال التالي الإدخالات المحاسبية التي تم إنشاؤها أثناء العملية.</span><span class="sxs-lookup"><span data-stu-id="51212-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="51212-109">إعداد الشركة</span><span class="sxs-lookup"><span data-stu-id="51212-109">Company setup</span></span>
-   <span data-ttu-id="51212-110">**شركة التشغيل/المصدر (USMF)** – يتم استخدام الدولارات الأمريكية (USD) كعملة للمحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="51212-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="51212-111">**الشركة المجمعة (CON)** – يتم استخدام اليورو (EUR) كعلمة للمحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="51212-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="51212-112">**الأرباح المحققة** – حساب دفتر الأستاذ 801500</span><span class="sxs-lookup"><span data-stu-id="51212-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="51212-113">**الخسائر المحققة** – حساب دفتر الأستاذ 801600</span><span class="sxs-lookup"><span data-stu-id="51212-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="51212-114">**الأرباح غير المحققة**– حساب دفتر الأستاذ 801600</span><span class="sxs-lookup"><span data-stu-id="51212-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="51212-115">**الخسائر غير المحققة**– حساب دفتر الأستاذ 801400</span><span class="sxs-lookup"><span data-stu-id="51212-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="51212-116">الحركات الأصلية</span><span class="sxs-lookup"><span data-stu-id="51212-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="51212-117">حركات إيصال استلام النقدية في USMF</span><span class="sxs-lookup"><span data-stu-id="51212-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="51212-118">التاريخ</span><span class="sxs-lookup"><span data-stu-id="51212-118">Date</span></span>       | <span data-ttu-id="51212-119">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="51212-119">Ledger account</span></span>               | <span data-ttu-id="51212-120">عملة</span><span class="sxs-lookup"><span data-stu-id="51212-120">Currency</span></span> | <span data-ttu-id="51212-121">المبلغ</span><span class="sxs-lookup"><span data-stu-id="51212-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="51212-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="51212-122">10/11/2015</span></span> | <span data-ttu-id="51212-123">110110 – نقد</span><span class="sxs-lookup"><span data-stu-id="51212-123">110110 – Cash</span></span>                | <span data-ttu-id="51212-124">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="51212-124">USD</span></span>      | <span data-ttu-id="51212-125">500</span><span class="sxs-lookup"><span data-stu-id="51212-125">500</span></span>    |
| <span data-ttu-id="51212-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="51212-126">10/11/2015</span></span> | <span data-ttu-id="51212-127">130100 – الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="51212-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="51212-128">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="51212-128">USD</span></span>      | <span data-ttu-id="51212-129">-500</span><span class="sxs-lookup"><span data-stu-id="51212-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="51212-130">أسعار الصرف</span><span class="sxs-lookup"><span data-stu-id="51212-130">Exchange rates</span></span>

| <span data-ttu-id="51212-131">من العملة</span><span class="sxs-lookup"><span data-stu-id="51212-131">From currency</span></span> | <span data-ttu-id="51212-132">إلى العملة</span><span class="sxs-lookup"><span data-stu-id="51212-132">To currency</span></span> | <span data-ttu-id="51212-133">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="51212-133">Start date</span></span> | <span data-ttu-id="51212-134">سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="51212-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="51212-135">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-135">EUR</span></span>           | <span data-ttu-id="51212-136">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="51212-136">USD</span></span>         | <span data-ttu-id="51212-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="51212-137">10/1/2015</span></span>  | <span data-ttu-id="51212-138">200</span><span class="sxs-lookup"><span data-stu-id="51212-138">200</span></span>           |
| <span data-ttu-id="51212-139">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-139">EUR</span></span>           | <span data-ttu-id="51212-140">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="51212-140">USD</span></span>         | <span data-ttu-id="51212-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="51212-141">11/1/2015</span></span>  | <span data-ttu-id="51212-142">150</span><span class="sxs-lookup"><span data-stu-id="51212-142">150</span></span>           |
| <span data-ttu-id="51212-143">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-143">EUR</span></span>           | <span data-ttu-id="51212-144">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="51212-144">USD</span></span>         | <span data-ttu-id="51212-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="51212-145">12/1/2012</span></span>  | <span data-ttu-id="51212-146">100</span><span class="sxs-lookup"><span data-stu-id="51212-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="51212-147">إجراء التجميع لأكتوبر 2015</span><span class="sxs-lookup"><span data-stu-id="51212-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="51212-148">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="51212-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="51212-149">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="51212-149">Ledger account</span></span> | <span data-ttu-id="51212-150">عملة</span><span class="sxs-lookup"><span data-stu-id="51212-150">Currency</span></span> | <span data-ttu-id="51212-151">المبلغ</span><span class="sxs-lookup"><span data-stu-id="51212-151">Amount</span></span> | <span data-ttu-id="51212-152">الحساب</span><span class="sxs-lookup"><span data-stu-id="51212-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="51212-153">110110</span><span class="sxs-lookup"><span data-stu-id="51212-153">110110</span></span>         | <span data-ttu-id="51212-154">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-154">EUR</span></span>      | <span data-ttu-id="51212-155">250</span><span class="sxs-lookup"><span data-stu-id="51212-155">250</span></span>    | <span data-ttu-id="51212-156">500 دولار أمريكي × 50%</span><span class="sxs-lookup"><span data-stu-id="51212-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="51212-157">130100</span><span class="sxs-lookup"><span data-stu-id="51212-157">130100</span></span>         | <span data-ttu-id="51212-158">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-158">EUR</span></span>      | <span data-ttu-id="51212-159">-250</span><span class="sxs-lookup"><span data-stu-id="51212-159">-250</span></span>   | <span data-ttu-id="51212-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="51212-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="51212-161">إجراء إعادة تقييم العملة للحسابات من 1 تشرين الأول/أكتوبر 2015 حتى 30 تشرين الثاني/نوفمبر عام 2015</span><span class="sxs-lookup"><span data-stu-id="51212-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="51212-162">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="51212-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="51212-163">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="51212-163">Ledger account</span></span> | <span data-ttu-id="51212-164">عملة</span><span class="sxs-lookup"><span data-stu-id="51212-164">Currency</span></span> | <span data-ttu-id="51212-165">المبلغ</span><span class="sxs-lookup"><span data-stu-id="51212-165">Amount</span></span>  | <span data-ttu-id="51212-166">الحساب</span><span class="sxs-lookup"><span data-stu-id="51212-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="51212-167">110110</span><span class="sxs-lookup"><span data-stu-id="51212-167">110110</span></span>         | <span data-ttu-id="51212-168">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-168">EUR</span></span>      | <span data-ttu-id="51212-169">333.33</span><span class="sxs-lookup"><span data-stu-id="51212-169">333.33</span></span>  | <span data-ttu-id="51212-170">المبلغ الأصلي 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="51212-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="51212-171">130100</span><span class="sxs-lookup"><span data-stu-id="51212-171">130100</span></span>         | <span data-ttu-id="51212-172">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-172">EUR</span></span>      | <span data-ttu-id="51212-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="51212-173">-333.33</span></span> | <span data-ttu-id="51212-174">المبلغ الأصلي -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="51212-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="51212-175">801400</span><span class="sxs-lookup"><span data-stu-id="51212-175">801400</span></span>         | <span data-ttu-id="51212-176">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-176">EUR</span></span>      | <span data-ttu-id="51212-177">83.33</span><span class="sxs-lookup"><span data-stu-id="51212-177">83.33</span></span>   | <span data-ttu-id="51212-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="51212-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="51212-179">801600</span><span class="sxs-lookup"><span data-stu-id="51212-179">801600</span></span>         | <span data-ttu-id="51212-180">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-180">EUR</span></span>      | <span data-ttu-id="51212-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="51212-181">-83.33</span></span>  | <span data-ttu-id="51212-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="51212-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="51212-183">سوف تشاهد حركات إضافية للعملات المشمولة بالتقرير.</span><span class="sxs-lookup"><span data-stu-id="51212-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="51212-184">إجراء إعادة تقييم العملة للحسابات من 1 تشرين الأول/أكتوبر 2015 حتى 31 تشرين الأول/ديسمبر عام 2015</span><span class="sxs-lookup"><span data-stu-id="51212-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="51212-185">الأرصدة في الشركة المجمعة</span><span class="sxs-lookup"><span data-stu-id="51212-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="51212-186">حساب دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="51212-186">Ledger account</span></span> | <span data-ttu-id="51212-187">عملة</span><span class="sxs-lookup"><span data-stu-id="51212-187">Currency</span></span> | <span data-ttu-id="51212-188">المبلغ</span><span class="sxs-lookup"><span data-stu-id="51212-188">Amount</span></span>  | <span data-ttu-id="51212-189">الحساب</span><span class="sxs-lookup"><span data-stu-id="51212-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="51212-190">110110</span><span class="sxs-lookup"><span data-stu-id="51212-190">110110</span></span>         | <span data-ttu-id="51212-191">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-191">EUR</span></span>      | <span data-ttu-id="51212-192">500.00</span><span class="sxs-lookup"><span data-stu-id="51212-192">500.00</span></span>  | <span data-ttu-id="51212-193">المبلغ الأصلي 500 × 1</span><span class="sxs-lookup"><span data-stu-id="51212-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="51212-194">130100</span><span class="sxs-lookup"><span data-stu-id="51212-194">130100</span></span>         | <span data-ttu-id="51212-195">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-195">EUR</span></span>      | <span data-ttu-id="51212-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="51212-196">-500.00</span></span> | <span data-ttu-id="51212-197">المبلغ الأصلي -500 × 1</span><span class="sxs-lookup"><span data-stu-id="51212-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="51212-198">801400</span><span class="sxs-lookup"><span data-stu-id="51212-198">801400</span></span>         | <span data-ttu-id="51212-199">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-199">EUR</span></span>      | <span data-ttu-id="51212-200">250</span><span class="sxs-lookup"><span data-stu-id="51212-200">250</span></span>     | <span data-ttu-id="51212-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="51212-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="51212-202">801600</span><span class="sxs-lookup"><span data-stu-id="51212-202">801600</span></span>         | <span data-ttu-id="51212-203">يورو</span><span class="sxs-lookup"><span data-stu-id="51212-203">EUR</span></span>      | <span data-ttu-id="51212-204">-250</span><span class="sxs-lookup"><span data-stu-id="51212-204">-250</span></span>    | <span data-ttu-id="51212-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="51212-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





