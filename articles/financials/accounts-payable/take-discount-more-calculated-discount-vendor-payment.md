---
title: "الحصول على خصم أكبر من الخصم المحتسب لدفعة المورد"
description: "ترشدك هذه المقالة عبر سيناريو حيث يؤخذ خصم نقدي لمبلغ أكبر من الخصم الذي كان متاحًا في الأصل على الفاتورة. قد يحدث هذا السيناريو إذا توصلت المؤسسة إلى إبرام اتفاقية مع المورّد لدفع مبلغ أصغر على الفاتورة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 66296bc22cb3b940ed914b77b8c3a7c054d4aa71
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="e900f-104">الحصول على خصم أكبر من الخصم المحتسب لدفعة المورد</span><span class="sxs-lookup"><span data-stu-id="e900f-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e900f-105">ترشدك هذه المقالة عبر سيناريو حيث يؤخذ خصم نقدي لمبلغ أكبر من الخصم الذي كان متاحًا في الأصل على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e900f-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="e900f-106">قد يحدث هذا السيناريو إذا توصلت المؤسسة إلى إبرام اتفاقية مع المورّد لدفع مبلغ أصغر على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e900f-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="e900f-107">يمنح المورد 3051 لشركة الاتحاد للتصنيع خصمًا نقديًا بنسبة 4 في المائة إذا تم دفع فاتورة في غضون سبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="e900f-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="e900f-108">وفي 29 حزيران/يونيو، تقوم فوزية بإدخال فاتورة بمبلغ 1,000.0.</span><span class="sxs-lookup"><span data-stu-id="e900f-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="e900f-109">ويتيح المورد لفوزية الحصول على خصم بمبلغ 60.00 بدلاً من الخصم الافتراضي بمبلغ 40.00 والمتوفر للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e900f-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="e900f-110">وتقوم فوزية بتسجيل دفعة لمرة واحدة من خلال استخدام دفتر يومية دفع الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="e900f-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="e900f-111">‏‫وتقوم بإدخال المورد للدفعة، ثم تفتح صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="e900f-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="e900f-112">وتقوم بتمييز الفاتورة وتغيير القيمة الموجودة في حقل **مبلغ الخصم النقدي‬‏‫** إلى **60.00**.</span><span class="sxs-lookup"><span data-stu-id="e900f-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="e900f-113">وضع علامة</span><span class="sxs-lookup"><span data-stu-id="e900f-113">Mark</span></span>     | <span data-ttu-id="e900f-114">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="e900f-114">Use cash discount</span></span> | <span data-ttu-id="e900f-115">الإيصال</span><span class="sxs-lookup"><span data-stu-id="e900f-115">Voucher</span></span>   | <span data-ttu-id="e900f-116">الحساب</span><span class="sxs-lookup"><span data-stu-id="e900f-116">Account</span></span> | <span data-ttu-id="e900f-117">التاريخ</span><span class="sxs-lookup"><span data-stu-id="e900f-117">Date</span></span>      | <span data-ttu-id="e900f-118">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="e900f-118">Due date</span></span>  | <span data-ttu-id="e900f-119">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="e900f-119">Invoice</span></span> | <span data-ttu-id="e900f-120">المبلغ بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="e900f-120">Amount in transaction currency</span></span> | <span data-ttu-id="e900f-121">عملة</span><span class="sxs-lookup"><span data-stu-id="e900f-121">Currency</span></span> | <span data-ttu-id="e900f-122">المبلغ المراد تسويته</span><span class="sxs-lookup"><span data-stu-id="e900f-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="e900f-123">محدَد</span><span class="sxs-lookup"><span data-stu-id="e900f-123">Selected</span></span> | <span data-ttu-id="e900f-124">عادي</span><span class="sxs-lookup"><span data-stu-id="e900f-124">Normal</span></span>            | <span data-ttu-id="e900f-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="e900f-125">Inv-10040</span></span> | <span data-ttu-id="e900f-126">3051</span><span class="sxs-lookup"><span data-stu-id="e900f-126">3051</span></span>    | <span data-ttu-id="e900f-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="e900f-127">6/29/2015</span></span> | <span data-ttu-id="e900f-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="e900f-128">7/29/2015</span></span> | <span data-ttu-id="e900f-129">10040</span><span class="sxs-lookup"><span data-stu-id="e900f-129">10040</span></span>   | <span data-ttu-id="e900f-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e900f-130">1,000.00</span></span>                       | <span data-ttu-id="e900f-131">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="e900f-131">USD</span></span>      | <span data-ttu-id="e900f-132">940.00</span><span class="sxs-lookup"><span data-stu-id="e900f-132">940.00</span></span>           |

<span data-ttu-id="e900f-133">تظهر معلومات الخصم أسفل صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="e900f-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="e900f-134">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="e900f-134">Cash discount date</span></span>           | <span data-ttu-id="e900f-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="e900f-135">7/12/2015</span></span> |
| <span data-ttu-id="e900f-136">مبلغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="e900f-136">Cash discount amount</span></span>         | <span data-ttu-id="e900f-137">60.00</span><span class="sxs-lookup"><span data-stu-id="e900f-137">60.00</span></span>     |
| <span data-ttu-id="e900f-138">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="e900f-138">Use cash discount</span></span>            | <span data-ttu-id="e900f-139">عادي</span><span class="sxs-lookup"><span data-stu-id="e900f-139">Normal</span></span>    |
| <span data-ttu-id="e900f-140">الخصم النقدي المستقطع</span><span class="sxs-lookup"><span data-stu-id="e900f-140">Cash discount taken</span></span>          | <span data-ttu-id="e900f-141">0.00</span><span class="sxs-lookup"><span data-stu-id="e900f-141">0.00</span></span>      |
| <span data-ttu-id="e900f-142">مبلغ الخصم النقدي المطلوب استقطاعه</span><span class="sxs-lookup"><span data-stu-id="e900f-142">Cash discount amount to take</span></span> | <span data-ttu-id="e900f-143">60.00</span><span class="sxs-lookup"><span data-stu-id="e900f-143">60.00</span></span>     |

<span data-ttu-id="e900f-144">وتقوم فوزية بترحيل دفتر يومية الدفع.</span><span class="sxs-lookup"><span data-stu-id="e900f-144">April posts the payment journal.</span></span> <span data-ttu-id="e900f-145">وتتم تسوية الفاتورة بالكامل باستخدام دفعة بمبلغ 940.00 وبخصم بمبلغ 60.00.</span><span class="sxs-lookup"><span data-stu-id="e900f-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




