---
title: "معالجة الخصومات النقدية لحالات الدفع بالزيادة"
description: "توفر هذه المقالة سيناريوهات توضح كيفية معالجة الدفع عندما يأخذ العميل خصمًا نقديًا ولكنه يدفع أيضًا مبلغًا زائدًا."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 5604f806eed81c60dfcae7cb7b1a22bba25aa454
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017


---

# <a name="handling-cash-discounts-for-overpayments"></a><span data-ttu-id="049fa-103">معالجة الخصومات النقدية لحالات الدفع بالزيادة</span><span class="sxs-lookup"><span data-stu-id="049fa-103">Handling cash discounts for overpayments</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="049fa-104">توفر هذه المقالة سيناريوهات توضح كيفية معالجة الدفع عندما يأخذ العميل خصمًا نقديًا ولكنه يدفع أيضًا مبلغًا زائدًا.</span><span class="sxs-lookup"><span data-stu-id="049fa-104">This article provides scenarios that show how a payment is handled when the customer takes a cash discount but also overpays.</span></span> 

<span data-ttu-id="049fa-105">تعتبر الفاتورة زائدة الدفع عندما يكون مبلغ الدفع أكبر من مبلغ الفاتورة وأقل من الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="049fa-105">An invoice is considered overpaid when the payment amount is more than the invoice amount minus the cash discount.</span></span> <span data-ttu-id="049fa-106">ولتحديد كيفية التعامل مع وجود فرق خصم النقدي المتاح عند يتم دفع الفاتورة بالزيادة، استخدم حقلي **إدارة الخصم النقدي** و**الحد الأقصى للدفع بالزيادة أو النقصان** في صفحة **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="049fa-106">To specify how an obtainable cash discount difference is handled when an invoice is overpaid, use the **Cash discount administration** and **Maximum overpayment or underpayment** fields on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="049fa-107">في المثال التالي، دفع العميل زيادة على الفاتورة بمقدار 0.50.</span><span class="sxs-lookup"><span data-stu-id="049fa-107">In the following example, the customer has overpaid the invoice by 0.50.</span></span>

| <span data-ttu-id="049fa-108">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-108">Invoice total</span></span> | <span data-ttu-id="049fa-109">الخصم النقدي المتاح</span><span class="sxs-lookup"><span data-stu-id="049fa-109">Cash discount available</span></span> | <span data-ttu-id="049fa-110">المبلغ الذي سيتم دفعه شاملاً الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-110">Amount to be paid, which includes the cash discount</span></span> | <span data-ttu-id="049fa-111">المبلغ الذي يدفعه العميل فعليًا</span><span class="sxs-lookup"><span data-stu-id="049fa-111">Amount the customer actually pays</span></span> |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="049fa-112">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-112">105.00</span></span>        | <span data-ttu-id="049fa-113">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-113">10.50</span></span>                   | <span data-ttu-id="049fa-114">94.50</span><span class="sxs-lookup"><span data-stu-id="049fa-114">94.50</span></span>                                               | <span data-ttu-id="049fa-115">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-115">95.00</span></span>                             |

## <a name="cash-discount-administration--specific"></a><span data-ttu-id="049fa-116">إدارة الخصم النقدي = محدد</span><span class="sxs-lookup"><span data-stu-id="049fa-116">Cash discount administration = Specific</span></span>
<span data-ttu-id="049fa-117">عند تحديد **محدد** في حقل **إدارة الخصم النقدي** في صفحة **حسابات للحركات التلقائية**، يتم الحصول على الخصم النقدي بالكامل.</span><span class="sxs-lookup"><span data-stu-id="049fa-117">When **Specific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the full cash discount is taken.</span></span> <span data-ttu-id="049fa-118">إما أن يتم ترحيل مبلغ الدفع بالزيادة إلى حساب دفتر الأستاذ كفرق في الخصم النقدي أو أن يبقى رصيدًا في حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="049fa-118">The overpayment amount either is posted to a cash discount difference ledger account or remains a balance on the customer’s account.</span></span> <span data-ttu-id="049fa-119">ويعتمد السلوك على ما إذا كان مبلغ الدفع بالزيادة بين 0.00 والمبلغ الذي تم إدخاله في حقل **الحد الأقصى للدفع بالزيادة أو النقصان**، أو ما إذا كان مبلغ الدفع الزيادة أكبر من مبلغ **الحد الأقصى للدفع بالزيادة أو النقصان**.</span><span class="sxs-lookup"><span data-stu-id="049fa-119">The behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="049fa-120">السيناريو 1</span><span class="sxs-lookup"><span data-stu-id="049fa-120">Scenario 1</span></span>

<span data-ttu-id="049fa-121">في هذا السيناريو: يتراوح مبلغ الدفع بالزيادة بين 0.00 والحد الأقصى للدفع بالزيادة أو النقصان.</span><span class="sxs-lookup"><span data-stu-id="049fa-121">In this scenario, the overpayment amount is between 0.00 and the maximum overpayment or underpayment.</span></span> <span data-ttu-id="049fa-122">ويتم إدخال فاتورة بمبلغ 105.00، ويتوفر خصم نقدي إذا تم دفع الفاتورة في غضون سبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="049fa-122">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="049fa-123">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-123">Invoice total</span></span> | <span data-ttu-id="049fa-124">الخصم النقدي المتاح</span><span class="sxs-lookup"><span data-stu-id="049fa-124">Cash discount available</span></span> | <span data-ttu-id="049fa-125">المبلغ الذي سيتم دفعه شاملاً الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-125">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="049fa-126">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-126">105.00</span></span>        | <span data-ttu-id="049fa-127">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-127">10.50</span></span>                   | <span data-ttu-id="049fa-128">94.50</span><span class="sxs-lookup"><span data-stu-id="049fa-128">94.50</span></span>                                               |

<span data-ttu-id="049fa-129">يُرسل العميل عملية دفعة بمبلغ 95.00 خلال فترة الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="049fa-129">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="049fa-130">يتم تسوية الدفع مقابل الفاتورة بمبلغ 105.00.</span><span class="sxs-lookup"><span data-stu-id="049fa-130">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="049fa-131">وبعد تسوية الفاتورة والدفع، يتم إنشاء الحركات التالية للعميل في الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="049fa-131">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="049fa-132">الحركة</span><span class="sxs-lookup"><span data-stu-id="049fa-132">Transaction</span></span>   | <span data-ttu-id="049fa-133">المبلغ</span><span class="sxs-lookup"><span data-stu-id="049fa-133">Amount</span></span> | <span data-ttu-id="049fa-134">الرصيد</span><span class="sxs-lookup"><span data-stu-id="049fa-134">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="049fa-135">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-135">Invoice</span></span>       | <span data-ttu-id="049fa-136">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-136">105.00</span></span> | <span data-ttu-id="049fa-137">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-137">0.00</span></span>    |
| <span data-ttu-id="049fa-138">الدفع</span><span class="sxs-lookup"><span data-stu-id="049fa-138">Payment</span></span>       | <span data-ttu-id="049fa-139">-95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-139">-95.00</span></span> | <span data-ttu-id="049fa-140">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-140">0.00</span></span>    |
| <span data-ttu-id="049fa-141">الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-141">Cash discount</span></span> | <span data-ttu-id="049fa-142">-10.50</span><span class="sxs-lookup"><span data-stu-id="049fa-142">-10.50</span></span> | <span data-ttu-id="049fa-143">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-143">0.00</span></span>    |

<span data-ttu-id="049fa-144">يتم إنشاء الإدخالات المحاسبية التالية للدفع والتسوية.</span><span class="sxs-lookup"><span data-stu-id="049fa-144">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="049fa-145">**الدفع**</span><span class="sxs-lookup"><span data-stu-id="049fa-145">**Payment**</span></span>

| <span data-ttu-id="049fa-146">الحساب</span><span class="sxs-lookup"><span data-stu-id="049fa-146">Account</span></span>             | <span data-ttu-id="049fa-147">المبلغ المدين</span><span class="sxs-lookup"><span data-stu-id="049fa-147">Debit amount</span></span> | <span data-ttu-id="049fa-148">المبلغ الدائن</span><span class="sxs-lookup"><span data-stu-id="049fa-148">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="049fa-149">نقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-149">Cash</span></span>                | <span data-ttu-id="049fa-150">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-150">95.00</span></span>        |               |
| <span data-ttu-id="049fa-151">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-151">Accounts receivable</span></span> |              | <span data-ttu-id="049fa-152">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-152">95.00</span></span>         |

<span data-ttu-id="049fa-153">**التسوية**</span><span class="sxs-lookup"><span data-stu-id="049fa-153">**Settlement**</span></span>

| <span data-ttu-id="049fa-154">الحساب</span><span class="sxs-lookup"><span data-stu-id="049fa-154">Account</span></span>                                                                                                          | <span data-ttu-id="049fa-155">المبلغ المدين</span><span class="sxs-lookup"><span data-stu-id="049fa-155">Debit amount</span></span> | <span data-ttu-id="049fa-156">المبلغ الدائن</span><span class="sxs-lookup"><span data-stu-id="049fa-156">Credit amount</span></span> |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="049fa-157">الخصم النقدي (حقل **الحساب الرئيسي لخصومات العميل** في صفحة **الخصومات النقدية**)</span><span class="sxs-lookup"><span data-stu-id="049fa-157">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span>                 | <span data-ttu-id="049fa-158">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-158">10.50</span></span>        |               |
| <span data-ttu-id="049fa-159">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-159">Accounts receivable</span></span>                                                                                              |              | <span data-ttu-id="049fa-160">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-160">10.50</span></span>         |
| <span data-ttu-id="049fa-161">الخصم النقدي للعميل (حقل **الخصم النقدي للعميل** في صفحة **حساب الحركات التلقائية**)</span><span class="sxs-lookup"><span data-stu-id="049fa-161">Customer cash discount (the **Customer cash discount** field on the **Account for automatic transactions** page)</span></span> |              | <span data-ttu-id="049fa-162">0.50</span><span class="sxs-lookup"><span data-stu-id="049fa-162">0.50</span></span>          |
| <span data-ttu-id="049fa-163">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-163">Accounts receivable</span></span>                                                                                              | <span data-ttu-id="049fa-164">0.50</span><span class="sxs-lookup"><span data-stu-id="049fa-164">0.50</span></span>         |               |

### <a name="scenario-2"></a><span data-ttu-id="049fa-165">السيناريو 2</span><span class="sxs-lookup"><span data-stu-id="049fa-165">Scenario 2</span></span>

<span data-ttu-id="049fa-166">في هذا ‎السيناريو، ‎يتجاوز مبلغ الدفع بالزيادة الحد الأقصى لمبلغ الدفع بالزيادة أو النقصان.</span><span class="sxs-lookup"><span data-stu-id="049fa-166">In this scenario, the overpayment amount exceeds the maximum overpayment or underpayment amount.</span></span> <span data-ttu-id="049fa-167">ويتم إدخال فاتورة بمبلغ 105.00، ويتوفر خصم نقدي إذا تم دفع الفاتورة في غضون سبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="049fa-167">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="049fa-168">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-168">Invoice total</span></span> | <span data-ttu-id="049fa-169">الخصم النقدي المتاح</span><span class="sxs-lookup"><span data-stu-id="049fa-169">Cash discount available</span></span> | <span data-ttu-id="049fa-170">المبلغ الذي سيتم دفعه شاملاً الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-170">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="049fa-171">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-171">105.00</span></span>        | <span data-ttu-id="049fa-172">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-172">10.50</span></span>                   | <span data-ttu-id="049fa-173">94.50</span><span class="sxs-lookup"><span data-stu-id="049fa-173">94.50</span></span>                                               |

<span data-ttu-id="049fa-174">يُرسل العميل عملية دفعة بمبلغ 95.00 خلال فترة الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="049fa-174">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="049fa-175">يتم تسوية الدفع مقابل الفاتورة بمبلغ 105.00.</span><span class="sxs-lookup"><span data-stu-id="049fa-175">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="049fa-176">وبعد تسوية الفاتورة والدفع، يتم إنشاء الحركات التالية للعميل في الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="049fa-176">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="049fa-177">الحركة</span><span class="sxs-lookup"><span data-stu-id="049fa-177">Transaction</span></span>   | <span data-ttu-id="049fa-178">المبلغ</span><span class="sxs-lookup"><span data-stu-id="049fa-178">Amount</span></span> | <span data-ttu-id="049fa-179">الرصيد</span><span class="sxs-lookup"><span data-stu-id="049fa-179">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="049fa-180">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-180">Invoice</span></span>       | <span data-ttu-id="049fa-181">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-181">105.00</span></span> | <span data-ttu-id="049fa-182">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-182">0.00</span></span>    |
| <span data-ttu-id="049fa-183">الدفع</span><span class="sxs-lookup"><span data-stu-id="049fa-183">Payment</span></span>       | <span data-ttu-id="049fa-184">-95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-184">-95.00</span></span> | <span data-ttu-id="049fa-185">-0.50</span><span class="sxs-lookup"><span data-stu-id="049fa-185">-0.50</span></span>   |
| <span data-ttu-id="049fa-186">الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-186">Cash discount</span></span> | <span data-ttu-id="049fa-187">-10.50</span><span class="sxs-lookup"><span data-stu-id="049fa-187">-10.50</span></span> | <span data-ttu-id="049fa-188">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-188">0.00</span></span>    |

<span data-ttu-id="049fa-189">سيبقى مبلغ الدفع بالزيادة الذي يبلغ 0.50 كرصيد مفتوح في الدفع ويمكن تسويته مقابل فاتورة أخرى.</span><span class="sxs-lookup"><span data-stu-id="049fa-189">The overpayment amount of 0.50 will remain as an open balance on the payment and can be settled against another invoice.</span></span> <span data-ttu-id="049fa-190">يتم إنشاء الإدخالات المحاسبية التالية للدفع والتسوية.</span><span class="sxs-lookup"><span data-stu-id="049fa-190">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="049fa-191">**الدفع**</span><span class="sxs-lookup"><span data-stu-id="049fa-191">**Payment**</span></span>

| <span data-ttu-id="049fa-192">الحساب</span><span class="sxs-lookup"><span data-stu-id="049fa-192">Account</span></span>             | <span data-ttu-id="049fa-193">المبلغ المدين</span><span class="sxs-lookup"><span data-stu-id="049fa-193">Debit amount</span></span> | <span data-ttu-id="049fa-194">المبلغ الدائن</span><span class="sxs-lookup"><span data-stu-id="049fa-194">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="049fa-195">نقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-195">Cash</span></span>                | <span data-ttu-id="049fa-196">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-196">95.00</span></span>        |               |
| <span data-ttu-id="049fa-197">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-197">Accounts receivable</span></span> |              | <span data-ttu-id="049fa-198">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-198">95.00</span></span>         |

<span data-ttu-id="049fa-199">**التسوية**</span><span class="sxs-lookup"><span data-stu-id="049fa-199">**Settlement**</span></span>

| <span data-ttu-id="049fa-200">الحساب</span><span class="sxs-lookup"><span data-stu-id="049fa-200">Account</span></span>                                                                                          | <span data-ttu-id="049fa-201">المبلغ المدين</span><span class="sxs-lookup"><span data-stu-id="049fa-201">Debit amount</span></span> | <span data-ttu-id="049fa-202">المبلغ الدائن</span><span class="sxs-lookup"><span data-stu-id="049fa-202">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="049fa-203">الخصم النقدي (حقل **الحساب الرئيسي لخصومات العميل** في صفحة **الخصومات النقدية**)</span><span class="sxs-lookup"><span data-stu-id="049fa-203">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="049fa-204">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-204">10.50</span></span>        |               |
| <span data-ttu-id="049fa-205">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-205">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="049fa-206">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-206">10.50</span></span>         |

## <a name="cash-discount-administration--unspecific"></a><span data-ttu-id="049fa-207">إدارة الخصم النقدي = غير محدد</span><span class="sxs-lookup"><span data-stu-id="049fa-207">Cash discount administration = Unspecific</span></span>
<span data-ttu-id="049fa-208">عند تحديد **غير محدد** في حقل **إدارة الخصم النقدي** في صفحة **حسابات للحركات التلقائية**، يتم إنقاص مبلغ الخصم النقدي بمبلغ الدفع بالزيادة.</span><span class="sxs-lookup"><span data-stu-id="049fa-208">When **Unspecific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="049fa-209">ينطبق هذا السلوك دائماً، بغض النظر عما إذا كان مبلغ الدفع بالزيادة أكبر أو أقل من المبلغ الذي تم إدخاله في حقل **الحد الأقصى للدفع بالزيادة أو النقصان**.</span><span class="sxs-lookup"><span data-stu-id="049fa-209">This behavior always applies, regardless of whether the overpayment amount is over or under the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>

### <a name="scenario-3"></a><span data-ttu-id="049fa-210">السيناريو 3</span><span class="sxs-lookup"><span data-stu-id="049fa-210">Scenario 3</span></span>

<span data-ttu-id="049fa-211">في هذا السيناريو، يتم إدخال فاتورة بمبلغ 105.00، ويتوفر خصم نقدي إذا تم دفع الفاتورة في غضون سبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="049fa-211">In this scenario, an invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="049fa-212">إجمالي الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-212">Invoice total</span></span> | <span data-ttu-id="049fa-213">الخصم النقدي المتاح</span><span class="sxs-lookup"><span data-stu-id="049fa-213">Cash discount available</span></span> | <span data-ttu-id="049fa-214">المبلغ الذي سيتم دفعه شاملاً الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-214">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="049fa-215">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-215">105.00</span></span>        | <span data-ttu-id="049fa-216">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-216">10.50</span></span>                   | <span data-ttu-id="049fa-217">94.50</span><span class="sxs-lookup"><span data-stu-id="049fa-217">94.50</span></span>                                               |

<span data-ttu-id="049fa-218">يُرسل العميل عملية دفعة بمبلغ 95.00 خلال تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="049fa-218">The customer submits a payment for 95.00 within the cash discount date.</span></span> <span data-ttu-id="049fa-219">يتم تسوية الدفع مقابل الفاتورة بمبلغ 105.00.</span><span class="sxs-lookup"><span data-stu-id="049fa-219">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="049fa-220">وبعد تسوية الفاتورة والدفع، يتم إنشاء الحركات التالية للعميل في الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="049fa-220">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="049fa-221">الحركة</span><span class="sxs-lookup"><span data-stu-id="049fa-221">Transaction</span></span>   | <span data-ttu-id="049fa-222">المبلغ</span><span class="sxs-lookup"><span data-stu-id="049fa-222">Amount</span></span> | <span data-ttu-id="049fa-223">الرصيد</span><span class="sxs-lookup"><span data-stu-id="049fa-223">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="049fa-224">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="049fa-224">Invoice</span></span>       | <span data-ttu-id="049fa-225">105.00</span><span class="sxs-lookup"><span data-stu-id="049fa-225">105.00</span></span> | <span data-ttu-id="049fa-226">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-226">0.00</span></span>    |
| <span data-ttu-id="049fa-227">الدفع</span><span class="sxs-lookup"><span data-stu-id="049fa-227">Payment</span></span>       | <span data-ttu-id="049fa-228">-95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-228">-95.00</span></span> | <span data-ttu-id="049fa-229">-0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-229">-0.00</span></span>   |
| <span data-ttu-id="049fa-230">الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-230">Cash discount</span></span> | <span data-ttu-id="049fa-231">-10.00</span><span class="sxs-lookup"><span data-stu-id="049fa-231">-10.00</span></span> | <span data-ttu-id="049fa-232">0.00</span><span class="sxs-lookup"><span data-stu-id="049fa-232">0.00</span></span>    |

<span data-ttu-id="049fa-233">يتم تقليل مبلغ الخصم النقدي من 10.50 إلى 10.00.</span><span class="sxs-lookup"><span data-stu-id="049fa-233">The cash discount amount is reduced from 10.50 to 10.00.</span></span> <span data-ttu-id="049fa-234">يعتبر الدفع والفاتورة تمت تسويتهما.</span><span class="sxs-lookup"><span data-stu-id="049fa-234">The payment and invoice are considered settled.</span></span> <span data-ttu-id="049fa-235">**الدفع**</span><span class="sxs-lookup"><span data-stu-id="049fa-235">**Payment**</span></span>

| <span data-ttu-id="049fa-236">الحساب</span><span class="sxs-lookup"><span data-stu-id="049fa-236">Account</span></span>             | <span data-ttu-id="049fa-237">المبلغ المدين</span><span class="sxs-lookup"><span data-stu-id="049fa-237">Debit amount</span></span> | <span data-ttu-id="049fa-238">المبلغ الدائن</span><span class="sxs-lookup"><span data-stu-id="049fa-238">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="049fa-239">نقدي</span><span class="sxs-lookup"><span data-stu-id="049fa-239">Cash</span></span>                | <span data-ttu-id="049fa-240">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-240">95.00</span></span>        |               |
| <span data-ttu-id="049fa-241">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-241">Accounts receivable</span></span> |              | <span data-ttu-id="049fa-242">95.00</span><span class="sxs-lookup"><span data-stu-id="049fa-242">95.00</span></span>         |

<span data-ttu-id="049fa-243">**التسوية**</span><span class="sxs-lookup"><span data-stu-id="049fa-243">**Settlement**</span></span>

| <span data-ttu-id="049fa-244">الحساب</span><span class="sxs-lookup"><span data-stu-id="049fa-244">Account</span></span>                                                                                          | <span data-ttu-id="049fa-245">المبلغ المدين</span><span class="sxs-lookup"><span data-stu-id="049fa-245">Debit amount</span></span> | <span data-ttu-id="049fa-246">المبلغ الدائن</span><span class="sxs-lookup"><span data-stu-id="049fa-246">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="049fa-247">الخصم النقدي (حقل **الحساب الرئيسي لخصومات العميل** في صفحة **الخصومات النقدية**)</span><span class="sxs-lookup"><span data-stu-id="049fa-247">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="049fa-248">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-248">10.50</span></span>        |               |
| <span data-ttu-id="049fa-249">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="049fa-249">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="049fa-250">1050</span><span class="sxs-lookup"><span data-stu-id="049fa-250">10.50</span></span>         |






