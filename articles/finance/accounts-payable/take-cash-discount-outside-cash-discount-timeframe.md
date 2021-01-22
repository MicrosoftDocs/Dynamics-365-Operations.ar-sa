---
title: الحصول على خصم نقدي خارج فترة الخصم النقدي
description: توفر هذه المقالة سيناريوهين يظهران كيف يمكن أخذ خصم نقدي حتى لو تم إجراء الدفع خارج فترة الخصم النقدي.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a166e9a0d43da80986dd63d6739b104745b115
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189466"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a><span data-ttu-id="75ef2-103">الحصول على خصم نقدي خارج فترة الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-103">Take a cash discount outside the cash discount period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75ef2-104">توفر هذه المقالة سيناريوهين يظهران كيف يمكن أخذ خصم نقدي حتى لو تم إجراء الدفع خارج فترة الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="75ef2-104">This article provides two scenarios that show how a cash discount can be taken even if the payment is made outside the cash discount period.</span></span>

<span data-ttu-id="75ef2-105">في 28 حزيران/يونيو، تقوم فوزية بإنشاء فاتورة بمبلغ 2,000.00 للمورد 3052.</span><span class="sxs-lookup"><span data-stu-id="75ef2-105">On June 28, April creates an invoice for 2,000.00 for vendor 3052.</span></span> <span data-ttu-id="75ef2-106">وتشمل الفاتورة خصمًا نقديًا قدره 1 في المائة، إذا تم دفع الفاتورة في غضون 14 يومًا.‬</span><span class="sxs-lookup"><span data-stu-id="75ef2-106">The invoice has a cash discount of 1 percent if the invoice is paid in 14 days.</span></span>

## <a name="use-cash-discount-option--always"></a><span data-ttu-id="75ef2-107">استخدم خيار الخصم النقدي = دوماً</span><span class="sxs-lookup"><span data-stu-id="75ef2-107">Use cash discount option = Always</span></span>
<span data-ttu-id="75ef2-108">تقوم فوزية بإنشاء دفعة في الأول من يوليو، بعد تاريخ الخصم.</span><span class="sxs-lookup"><span data-stu-id="75ef2-108">April creates a payment on July 1, which is after the discount date.</span></span> <span data-ttu-id="75ef2-109">وتقوم فوزية بفتح صفحة **تسوية الحركات** لعرض الحركات التي يمكن تسويتها.</span><span class="sxs-lookup"><span data-stu-id="75ef2-109">April opens the **Settle transactions** page to view the transactions that can be settled.</span></span> 

<span data-ttu-id="75ef2-110">وتقوم فوزية بتمييز فاتورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="75ef2-110">April marks the invoice for payment.</span></span> <span data-ttu-id="75ef2-111">لم يتم الحصول على أي خصم نقدي، لأن الدفع بعد تاريخ الخصم.</span><span class="sxs-lookup"><span data-stu-id="75ef2-111">No cash discount is taken, because the payment is after the discount date.</span></span> <span data-ttu-id="75ef2-112">‏‫ومع ذلك، أعطى المورد فوزية موافقة لإدخال الخصم النقدي على أية حال.</span><span class="sxs-lookup"><span data-stu-id="75ef2-112">However, the vendor has given April approval to take the cash discount anyway.</span></span> <span data-ttu-id="75ef2-113">ولذلك، تقوم فوزية بتغيير القيمة في حقل **استخدام الخصم النقدي** إلى **دوماً**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-113">Therefore, April changes the value in the **Use cash discount** field to **Always**.</span></span>

| <span data-ttu-id="75ef2-114">وضع علامة</span><span class="sxs-lookup"><span data-stu-id="75ef2-114">Mark</span></span>     | <span data-ttu-id="75ef2-115">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-115">Use cash discount</span></span> | <span data-ttu-id="75ef2-116">الإيصال</span><span class="sxs-lookup"><span data-stu-id="75ef2-116">Voucher</span></span>   | <span data-ttu-id="75ef2-117">الحساب</span><span class="sxs-lookup"><span data-stu-id="75ef2-117">Account</span></span> | <span data-ttu-id="75ef2-118">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-118">Cash discount date</span></span> | <span data-ttu-id="75ef2-119">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="75ef2-119">Due date</span></span>  | <span data-ttu-id="75ef2-120">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="75ef2-120">Invoice</span></span> | <span data-ttu-id="75ef2-121">المبلغ بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="75ef2-121">Amount in transaction currency</span></span> | <span data-ttu-id="75ef2-122">عملة</span><span class="sxs-lookup"><span data-stu-id="75ef2-122">Currency</span></span> | <span data-ttu-id="75ef2-123">المبلغ المراد تسويته</span><span class="sxs-lookup"><span data-stu-id="75ef2-123">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="75ef2-124">محدَد</span><span class="sxs-lookup"><span data-stu-id="75ef2-124">Selected</span></span> | <span data-ttu-id="75ef2-125">دائمًا</span><span class="sxs-lookup"><span data-stu-id="75ef2-125">Always</span></span>            | <span data-ttu-id="75ef2-126">Inv-10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-126">Inv-10030</span></span> | <span data-ttu-id="75ef2-127">3052</span><span class="sxs-lookup"><span data-stu-id="75ef2-127">3052</span></span>    | <span data-ttu-id="75ef2-128">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-128">6/28/2015</span></span>          | <span data-ttu-id="75ef2-129">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-129">7/12/2015</span></span> | <span data-ttu-id="75ef2-130">10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-130">10030</span></span>   | <span data-ttu-id="75ef2-131">-2,000.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-131">-2,000.00</span></span>                      | <span data-ttu-id="75ef2-132">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="75ef2-132">USD</span></span>      | <span data-ttu-id="75ef2-133">-1,980.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-133">-1,980.00</span></span>        |

<span data-ttu-id="75ef2-134">تظهر معلومات الخصم أسفل صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-134">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="75ef2-135">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-135">Cash discount date</span></span>           | <span data-ttu-id="75ef2-136">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-136">7/12/2015</span></span> |
| <span data-ttu-id="75ef2-137">مبلغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-137">Cash discount amount</span></span>         | <span data-ttu-id="75ef2-138">-20.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-138">-20.00</span></span>    |
| <span data-ttu-id="75ef2-139">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-139">Use cash discount</span></span>            | <span data-ttu-id="75ef2-140">دائمًا</span><span class="sxs-lookup"><span data-stu-id="75ef2-140">Always</span></span>    |
| <span data-ttu-id="75ef2-141">الخصم النقدي المستقطع</span><span class="sxs-lookup"><span data-stu-id="75ef2-141">Cash discount taken</span></span>          | <span data-ttu-id="75ef2-142">0.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-142">0.00</span></span>      |
| <span data-ttu-id="75ef2-143">مبلغ الخصم النقدي المطلوب استقطاعه</span><span class="sxs-lookup"><span data-stu-id="75ef2-143">Cash discount amount to take</span></span> | <span data-ttu-id="75ef2-144">-20.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-144">-20.00</span></span>    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a><span data-ttu-id="75ef2-145">التاريخ المستخدم لحساب الخصومات = التاريخ المحدد</span><span class="sxs-lookup"><span data-stu-id="75ef2-145">Date to use for calculating discounts = Selected date</span></span>
<span data-ttu-id="75ef2-146">إذا تم ترحيل الفاتورة والدفع على حد سواء، فإنه لا يزال يمكن الحصول على الخصم النقدي عند تسوية الحركات في صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-146">If both the invoice and the payment have been posted, the cash discount can still be taken when the transactions are settled on the **Settle transactions** page.</span></span> <span data-ttu-id="75ef2-147">وتقوم فوزية بتغيير القيمة في حقل **التاريخ المطلوب استخدامه لحساب الخصومات** إلى **التاريخ المحدد**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-147">April changes the value in the **Date to use for calculating discounts** field to **Selected date**.</span></span> <span data-ttu-id="75ef2-148">وتقوم فيما بعد بإدخال تاريخ 28 يونيو، في فترة الخصم النقدي للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="75ef2-148">She then enters a date of June 28, which is in the cash discount period for the invoice.</span></span> <span data-ttu-id="75ef2-149">ويتم استخدام هذا التاريخ لحساب خصم نقدي للحركة.</span><span class="sxs-lookup"><span data-stu-id="75ef2-149">That date is used to calculate a cash discount for the transaction.</span></span> <span data-ttu-id="75ef2-150">وفي صفحة **تسوية الحركات المفتوحة** تشاهد فوزية الخصم الكامل بمبلغ 20.00  يظهر بشكل افتراضي،</span><span class="sxs-lookup"><span data-stu-id="75ef2-150">On the **Settle open transactions** page, April sees that, by default, the full discount of 20.00 appears.</span></span> <span data-ttu-id="75ef2-151">يعرض بند الفاتورة المبلغ المراد تسويته بمبلغ 1,980.00.</span><span class="sxs-lookup"><span data-stu-id="75ef2-151">The invoice line shows that the amount to settle is 1,980.00.</span></span>

| <span data-ttu-id="75ef2-152">وضع علامة</span><span class="sxs-lookup"><span data-stu-id="75ef2-152">Mark</span></span>                     | <span data-ttu-id="75ef2-153">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-153">Use cash discount</span></span> | <span data-ttu-id="75ef2-154">الإيصال</span><span class="sxs-lookup"><span data-stu-id="75ef2-154">Voucher</span></span>   | <span data-ttu-id="75ef2-155">الحساب</span><span class="sxs-lookup"><span data-stu-id="75ef2-155">Account</span></span> | <span data-ttu-id="75ef2-156">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-156">Cash discount date</span></span> | <span data-ttu-id="75ef2-157">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="75ef2-157">Due date</span></span>  | <span data-ttu-id="75ef2-158">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="75ef2-158">Invoice</span></span> | <span data-ttu-id="75ef2-159">المبلغ بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="75ef2-159">Amount in transaction currency</span></span> | <span data-ttu-id="75ef2-160">عملة</span><span class="sxs-lookup"><span data-stu-id="75ef2-160">Currency</span></span> | <span data-ttu-id="75ef2-161">المبلغ المراد تسويته</span><span class="sxs-lookup"><span data-stu-id="75ef2-161">Amount to settle</span></span> |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="75ef2-162">المحددة والمميزة</span><span class="sxs-lookup"><span data-stu-id="75ef2-162">Selected and highlighted</span></span> | <span data-ttu-id="75ef2-163">عادي</span><span class="sxs-lookup"><span data-stu-id="75ef2-163">Normal</span></span>            | <span data-ttu-id="75ef2-164">Inv-10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-164">Inv-10030</span></span> | <span data-ttu-id="75ef2-165">3052</span><span class="sxs-lookup"><span data-stu-id="75ef2-165">3052</span></span>    | <span data-ttu-id="75ef2-166">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-166">6/28/2015</span></span>          | <span data-ttu-id="75ef2-167">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-167">7/12/2015</span></span> | <span data-ttu-id="75ef2-168">10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-168">10030</span></span>   | <span data-ttu-id="75ef2-169">-2,000.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-169">-2,000.00</span></span>                      | <span data-ttu-id="75ef2-170">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="75ef2-170">USD</span></span>      | <span data-ttu-id="75ef2-171">-1,980.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-171">-1,980.00</span></span>        |
| <span data-ttu-id="75ef2-172">محدَد</span><span class="sxs-lookup"><span data-stu-id="75ef2-172">Selected</span></span>                 | <span data-ttu-id="75ef2-173">عادي</span><span class="sxs-lookup"><span data-stu-id="75ef2-173">Normal</span></span>            | <span data-ttu-id="75ef2-174">APP-10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-174">APP-10030</span></span> | <span data-ttu-id="75ef2-175">3052</span><span class="sxs-lookup"><span data-stu-id="75ef2-175">3052</span></span>    | <span data-ttu-id="75ef2-176">7/15/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-176">7/15/2015</span></span>          | <span data-ttu-id="75ef2-177">7/15/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-177">7/15/2015</span></span> |         | <span data-ttu-id="75ef2-178">500.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-178">500.00</span></span>                         | <span data-ttu-id="75ef2-179">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="75ef2-179">USD</span></span>      | <span data-ttu-id="75ef2-180">500.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-180">500.00</span></span>           |

<span data-ttu-id="75ef2-181">تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-181">Discount information appears at the bottom of the **Settle open transactions** page.</span></span> <span data-ttu-id="75ef2-182">مبلغ الخصم الذي يتم الحصول عليه هو 20.00، لأن مبلغ المراد تسويته للفاتورة هو المبلغ الافتراضي 1,980.00.</span><span class="sxs-lookup"><span data-stu-id="75ef2-182">The discount amount that is taken is 20.00, because the amount to settle for the invoice is the default amount, 1,980.00.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="75ef2-183">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-183">Cash discount date</span></span>           | <span data-ttu-id="75ef2-184">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-184">7/12/2015</span></span> |
| <span data-ttu-id="75ef2-185">مبلغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-185">Cash discount amount</span></span>         | <span data-ttu-id="75ef2-186">-20.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-186">-20.00</span></span>    |
| <span data-ttu-id="75ef2-187">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-187">Use cash discount</span></span>            | <span data-ttu-id="75ef2-188">عادي</span><span class="sxs-lookup"><span data-stu-id="75ef2-188">Normal</span></span>    |
| <span data-ttu-id="75ef2-189">الخصم النقدي المستقطع</span><span class="sxs-lookup"><span data-stu-id="75ef2-189">Cash discount taken</span></span>          | <span data-ttu-id="75ef2-190">0.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-190">0.00</span></span>      |
| <span data-ttu-id="75ef2-191">مبلغ الخصم النقدي المطلوب استقطاعه</span><span class="sxs-lookup"><span data-stu-id="75ef2-191">Cash discount amount to take</span></span> | <span data-ttu-id="75ef2-192">-20.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-192">-20.00</span></span>    |

<span data-ttu-id="75ef2-193">تقوم فوزية بتحديث القيمة في حقل **المبلغ المُراد تسويته** إلى **500.00**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-193">April updates the value in the **Amount to settle** field to **500.00**.</span></span> <span data-ttu-id="75ef2-194">ويتم حساب القيمة في حقل **مبلغ الخصم النقدي المراد الحصول عليه** بمبلغ **5.05**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-194">The value in the **Cash discount amount to take** field is calculated as **5.05**.</span></span>

| <span data-ttu-id="75ef2-195">وضع علامة</span><span class="sxs-lookup"><span data-stu-id="75ef2-195">Mark</span></span>                     | <span data-ttu-id="75ef2-196">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-196">Use cash discount</span></span> | <span data-ttu-id="75ef2-197">الإيصال</span><span class="sxs-lookup"><span data-stu-id="75ef2-197">Voucher</span></span>   | <span data-ttu-id="75ef2-198">الحساب</span><span class="sxs-lookup"><span data-stu-id="75ef2-198">Account</span></span> | <span data-ttu-id="75ef2-199">التاريخ</span><span class="sxs-lookup"><span data-stu-id="75ef2-199">Date</span></span>      | <span data-ttu-id="75ef2-200">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="75ef2-200">Due date</span></span>  | <span data-ttu-id="75ef2-201">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="75ef2-201">Invoice</span></span> | <span data-ttu-id="75ef2-202">المبلغ بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="75ef2-202">Amount in transaction currency</span></span> | <span data-ttu-id="75ef2-203">عملة</span><span class="sxs-lookup"><span data-stu-id="75ef2-203">Currency</span></span> | <span data-ttu-id="75ef2-204">المبلغ المراد تسويته</span><span class="sxs-lookup"><span data-stu-id="75ef2-204">Amount to settle</span></span> |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="75ef2-205">المحددة والمميزة</span><span class="sxs-lookup"><span data-stu-id="75ef2-205">Selected and highlighted</span></span> | <span data-ttu-id="75ef2-206">عادي</span><span class="sxs-lookup"><span data-stu-id="75ef2-206">Normal</span></span>            | <span data-ttu-id="75ef2-207">Inv-10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-207">Inv-10030</span></span> | <span data-ttu-id="75ef2-208">3052</span><span class="sxs-lookup"><span data-stu-id="75ef2-208">3052</span></span>    | <span data-ttu-id="75ef2-209">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-209">6/28/2015</span></span> | <span data-ttu-id="75ef2-210">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-210">7/12/2015</span></span> | <span data-ttu-id="75ef2-211">10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-211">10030</span></span>   | <span data-ttu-id="75ef2-212">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-212">2,000.00</span></span>                       | <span data-ttu-id="75ef2-213">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="75ef2-213">USD</span></span>      | <span data-ttu-id="75ef2-214">-500.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-214">-500.00</span></span>          |
| <span data-ttu-id="75ef2-215">محدَد</span><span class="sxs-lookup"><span data-stu-id="75ef2-215">Selected</span></span>                 | <span data-ttu-id="75ef2-216">عادي</span><span class="sxs-lookup"><span data-stu-id="75ef2-216">Normal</span></span>            | <span data-ttu-id="75ef2-217">APP-10030</span><span class="sxs-lookup"><span data-stu-id="75ef2-217">APP-10030</span></span> | <span data-ttu-id="75ef2-218">3052</span><span class="sxs-lookup"><span data-stu-id="75ef2-218">3052</span></span>    | <span data-ttu-id="75ef2-219">7/15/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-219">7/15/2015</span></span> | <span data-ttu-id="75ef2-220">7/15/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-220">7/15/2015</span></span> |         | <span data-ttu-id="75ef2-221">500.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-221">500.00</span></span>                         | <span data-ttu-id="75ef2-222">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="75ef2-222">USD</span></span>      | <span data-ttu-id="75ef2-223">500.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-223">500.00</span></span>           |

<span data-ttu-id="75ef2-224">تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="75ef2-224">Discount information appears at the bottom of the **Settle open transactions** page.</span></span> <span data-ttu-id="75ef2-225">والقيمة في حقل **مبلغ الخصم النقدي المراد الحصول عليه** هو **5.05**، لأن المبلغ المراد تسويته للفاتورة تم تغييره إلى مبلغ الدفع 500.00.</span><span class="sxs-lookup"><span data-stu-id="75ef2-225">The value in the **Cash discount amount to take** field is **5.05**, because the amount to settle for the invoice was changed to the payment amount, 500.00.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="75ef2-226">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-226">Cash discount date</span></span>           | <span data-ttu-id="75ef2-227">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="75ef2-227">7/12/2015</span></span> |
| <span data-ttu-id="75ef2-228">مبلغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-228">Cash discount amount</span></span>         | <span data-ttu-id="75ef2-229">-20.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-229">-20.00</span></span>    |
| <span data-ttu-id="75ef2-230">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="75ef2-230">Use cash discount</span></span>            | <span data-ttu-id="75ef2-231">عادي</span><span class="sxs-lookup"><span data-stu-id="75ef2-231">Normal</span></span>    |
| <span data-ttu-id="75ef2-232">الخصم النقدي المستقطع</span><span class="sxs-lookup"><span data-stu-id="75ef2-232">Cash discount taken</span></span>          | <span data-ttu-id="75ef2-233">0.00</span><span class="sxs-lookup"><span data-stu-id="75ef2-233">0.00</span></span>      |
| <span data-ttu-id="75ef2-234">مبلغ الخصم النقدي المطلوب استقطاعه</span><span class="sxs-lookup"><span data-stu-id="75ef2-234">Cash discount amount to take</span></span> | <span data-ttu-id="75ef2-235">-5.05</span><span class="sxs-lookup"><span data-stu-id="75ef2-235">-5.05</span></span>     |




