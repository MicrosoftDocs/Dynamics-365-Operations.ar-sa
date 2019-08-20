---
title: الحصول على خصم أكبر من الخصم المحتسب لدفعة المورد
description: ترشدك هذه المقالة عبر سيناريو حيث يؤخذ خصم نقدي لمبلغ أكبر من الخصم الذي كان متاحًا في الأصل على الفاتورة. قد يحدث هذا السيناريو إذا توصلت المؤسسة إلى إبرام اتفاقية مع المورّد لدفع مبلغ أصغر على الفاتورة.
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
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843255"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="1196e-104">الحصول على خصم أكبر من الخصم المحتسب لدفعة المورد</span><span class="sxs-lookup"><span data-stu-id="1196e-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1196e-105">ترشدك هذه المقالة عبر سيناريو حيث يؤخذ خصم نقدي لمبلغ أكبر من الخصم الذي كان متاحًا في الأصل على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="1196e-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="1196e-106">قد يحدث هذا السيناريو إذا توصلت المؤسسة إلى إبرام اتفاقية مع المورّد لدفع مبلغ أصغر على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="1196e-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="1196e-107">يمنح المورد 3051 لشركة الاتحاد للتصنيع خصمًا نقديًا بنسبة 4 في المائة إذا تم دفع فاتورة في غضون سبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="1196e-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="1196e-108">وفي 29 حزيران/يونيو، تقوم فوزية بإدخال فاتورة بمبلغ 1,000.0.</span><span class="sxs-lookup"><span data-stu-id="1196e-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="1196e-109">ويتيح المورد لفوزية الحصول على خصم بمبلغ 60.00 بدلاً من الخصم الافتراضي بمبلغ 40.00 والمتوفر للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="1196e-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="1196e-110">وتقوم فوزية بتسجيل دفعة لمرة واحدة من خلال استخدام دفتر يومية دفع الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="1196e-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="1196e-111">‏‫وتقوم بإدخال المورد للدفعة، ثم تفتح صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="1196e-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="1196e-112">وتقوم بتمييز الفاتورة وتغيير القيمة الموجودة في حقل **مبلغ الخصم النقدي‬‏‫** إلى **60.00**.</span><span class="sxs-lookup"><span data-stu-id="1196e-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="1196e-113">وضع علامة</span><span class="sxs-lookup"><span data-stu-id="1196e-113">Mark</span></span>     | <span data-ttu-id="1196e-114">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="1196e-114">Use cash discount</span></span> | <span data-ttu-id="1196e-115">الإيصال</span><span class="sxs-lookup"><span data-stu-id="1196e-115">Voucher</span></span>   | <span data-ttu-id="1196e-116">الحساب</span><span class="sxs-lookup"><span data-stu-id="1196e-116">Account</span></span> | <span data-ttu-id="1196e-117">التاريخ</span><span class="sxs-lookup"><span data-stu-id="1196e-117">Date</span></span>      | <span data-ttu-id="1196e-118">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="1196e-118">Due date</span></span>  | <span data-ttu-id="1196e-119">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1196e-119">Invoice</span></span> | <span data-ttu-id="1196e-120">المبلغ بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="1196e-120">Amount in transaction currency</span></span> | <span data-ttu-id="1196e-121">عملة</span><span class="sxs-lookup"><span data-stu-id="1196e-121">Currency</span></span> | <span data-ttu-id="1196e-122">المبلغ المراد تسويته</span><span class="sxs-lookup"><span data-stu-id="1196e-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="1196e-123">محدَد</span><span class="sxs-lookup"><span data-stu-id="1196e-123">Selected</span></span> | <span data-ttu-id="1196e-124">عادي</span><span class="sxs-lookup"><span data-stu-id="1196e-124">Normal</span></span>            | <span data-ttu-id="1196e-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="1196e-125">Inv-10040</span></span> | <span data-ttu-id="1196e-126">3051</span><span class="sxs-lookup"><span data-stu-id="1196e-126">3051</span></span>    | <span data-ttu-id="1196e-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="1196e-127">6/29/2015</span></span> | <span data-ttu-id="1196e-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="1196e-128">7/29/2015</span></span> | <span data-ttu-id="1196e-129">10040</span><span class="sxs-lookup"><span data-stu-id="1196e-129">10040</span></span>   | <span data-ttu-id="1196e-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1196e-130">1,000.00</span></span>                       | <span data-ttu-id="1196e-131">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="1196e-131">USD</span></span>      | <span data-ttu-id="1196e-132">940.00</span><span class="sxs-lookup"><span data-stu-id="1196e-132">940.00</span></span>           |

<span data-ttu-id="1196e-133">تظهر معلومات الخصم أسفل صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="1196e-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="1196e-134">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="1196e-134">Cash discount date</span></span>           | <span data-ttu-id="1196e-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="1196e-135">7/12/2015</span></span> |
| <span data-ttu-id="1196e-136">مبلغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="1196e-136">Cash discount amount</span></span>         | <span data-ttu-id="1196e-137">60.00</span><span class="sxs-lookup"><span data-stu-id="1196e-137">60.00</span></span>     |
| <span data-ttu-id="1196e-138">استخدام الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="1196e-138">Use cash discount</span></span>            | <span data-ttu-id="1196e-139">عادي</span><span class="sxs-lookup"><span data-stu-id="1196e-139">Normal</span></span>    |
| <span data-ttu-id="1196e-140">الخصم النقدي المستقطع</span><span class="sxs-lookup"><span data-stu-id="1196e-140">Cash discount taken</span></span>          | <span data-ttu-id="1196e-141">0.00</span><span class="sxs-lookup"><span data-stu-id="1196e-141">0.00</span></span>      |
| <span data-ttu-id="1196e-142">مبلغ الخصم النقدي المطلوب استقطاعه</span><span class="sxs-lookup"><span data-stu-id="1196e-142">Cash discount amount to take</span></span> | <span data-ttu-id="1196e-143">60.00</span><span class="sxs-lookup"><span data-stu-id="1196e-143">60.00</span></span>     |

<span data-ttu-id="1196e-144">وتقوم فوزية بترحيل دفتر يومية الدفع.</span><span class="sxs-lookup"><span data-stu-id="1196e-144">April posts the payment journal.</span></span> <span data-ttu-id="1196e-145">وتتم تسوية الفاتورة بالكامل باستخدام دفعة بمبلغ 940.00 وبخصم بمبلغ 60.00.</span><span class="sxs-lookup"><span data-stu-id="1196e-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



