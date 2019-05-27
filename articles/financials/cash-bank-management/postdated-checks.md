---
title: الشيكات التي تم تأخير تاريخها
description: توفر هذه المقالة معلومات حول دعم الشيكات بتاريخ لاحق في Microsoft Dynamics 365 for Finance and Operations. الشيكات بتاريخ لاحق هي عبارة عن شيكات تم إصدارها لإجراء مدفوعات واستلامها في تاريخ محدد في المستقبل. وبالتالي، لا يمكن صرف الشيك حتى التاريخ المحدد.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ea1cd9926f3ea55d82f9030372a15b3545ed824
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563775"
---
# <a name="postdated-checks"></a><span data-ttu-id="d8d43-105">الشيكات التي تم تأخير تاريخها</span><span class="sxs-lookup"><span data-stu-id="d8d43-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8d43-106">توفر هذه المقالة معلومات حول دعم الشيكات بتاريخ لاحق في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8d43-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d8d43-107">الشيكات بتاريخ لاحق هي عبارة عن شيكات تم إصدارها لإجراء مدفوعات واستلامها في تاريخ محدد في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="d8d43-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="d8d43-108">وبالتالي، لا يمكن صرف الشيك حتى التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="d8d43-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="d8d43-109">يدعم Microsoft Dynamics 365 for Finance and Operations دورة الإدارة الكاملة للشيكات بتاريخ لاحق في كلٍّ من الحسابات المدينة والحسابات الدائنة، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="d8d43-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8d43-110">سيناريو</span><span class="sxs-lookup"><span data-stu-id="d8d43-110">Scenario</span></span></th>
<th><span data-ttu-id="d8d43-111">تفاصيل</span><span class="sxs-lookup"><span data-stu-id="d8d43-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8d43-112">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="d8d43-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="d8d43-113">يجب إعداد طريقة دفع جديدة وتحديد روتين الدفع لتسوية حسابات الشيكات الصادرة والشيكات المستلمة وضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d8d43-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8d43-114">تسجيل شيك بتاريخ لاحق لمورد وترحيله</span><span class="sxs-lookup"><span data-stu-id="d8d43-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d8d43-115">سجّل تفاصيل الشيك بتاريخ لاحق الذي تصدره لمورّد.</span><span class="sxs-lookup"><span data-stu-id="d8d43-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="d8d43-116">عند ترحيل الدفع، يتم التعرف على التزام المورّد، ولكن المبلغ لم يُضف بعد إلى الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="d8d43-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="d8d43-117">بدلاً من ذلك، يتم استخدام حساب مقاصة لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="d8d43-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8d43-118">تسجيل شيك بتاريخ لاحق لعميل وترحيله</span><span class="sxs-lookup"><span data-stu-id="d8d43-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="d8d43-119">سجّل تفاصيل شيك بتاريخ لاحق استلمته من عميل.</span><span class="sxs-lookup"><span data-stu-id="d8d43-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="d8d43-120">عند ترحيل الدفع، يكون الحساب المدين للعميل دائنًا، ولكن الحساب البنكي غير مدين‬ بعد.</span><span class="sxs-lookup"><span data-stu-id="d8d43-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="d8d43-121">بدلاً من ذلك، يتم استخدام حساب مقاصة لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="d8d43-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8d43-122">تسجيل شيك إحلال بتاريخ لاحق لمورّد أو عميل وترحيله</span><span class="sxs-lookup"><span data-stu-id="d8d43-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="d8d43-123">في حالة فقدان الشيك الأصلي الصادر إلى مورّد أو من عميل أو تلفه، يمكنك إصدار شيك إحلال بتاريخ لاحق.</span><span class="sxs-lookup"><span data-stu-id="d8d43-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="d8d43-124">عند تسجيل تفاصيل الشيك، ينبغي تقديم مرجع للشيك الأصلي والإشارة إلى أن الشيك الجديد هو مجرد بديل للشيك الأصلي.</span><span class="sxs-lookup"><span data-stu-id="d8d43-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="d8d43-125">كما يمكنك ترحيل شيك الإحلال.</span><span class="sxs-lookup"><span data-stu-id="d8d43-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8d43-126">تحويل شيكات عميل بتاريخ لاحق إلى المورّد</span><span class="sxs-lookup"><span data-stu-id="d8d43-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="d8d43-127">عند استلام شيك بتاريخ لاحق‬ من أحد العملاء، يمكنك تحويل هذا الشيك إلى مورّد كدفعة.</span><span class="sxs-lookup"><span data-stu-id="d8d43-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8d43-128">تسوية شيك بتاريخ لاحق لعميل أو مورد</span><span class="sxs-lookup"><span data-stu-id="d8d43-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="d8d43-129">يمكنك تسوية شيك بتاريخ لاحق تم ترحيله إلى حساب وسيط لعميل أو مورّد عندما يستحق الشيك أخيرًا.</span><span class="sxs-lookup"><span data-stu-id="d8d43-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="d8d43-130">عند تسوية الشيك، يكون البنك أخيرًا مدينًا أو دائنًا في مقابل حساب المقاصة الذي تم استخدامه في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="d8d43-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8d43-131">إلغاء شيك بتاريخ لاحق لمورّد</span><span class="sxs-lookup"><span data-stu-id="d8d43-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d8d43-132">‏‫يمكنك إلغاء شيك مُرحَّل بتاريخ لاحق في الحالات التالية:‬ - ‏‫إرجاع البنك للشيك.‬</span><span class="sxs-lookup"><span data-stu-id="d8d43-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="d8d43-133">- تطبيق الشيك على فاتورة غير صحيحة.</span><span class="sxs-lookup"><span data-stu-id="d8d43-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="d8d43-134">- إجراء الدفع النقدي مقابل الشيك.</span><span class="sxs-lookup"><span data-stu-id="d8d43-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="d8d43-135">إيقاف دفع شيك بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="d8d43-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="d8d43-136">يمكنك إيقاف دفع شيك بتاريخ لاحق صادر إلى أحد المورّدين لأسباب كأرصدة غير كافية أو حدوث تغييرات في شروط الاتفاقية مع المورّد أو تزويد بضائع تالفة من قبل المورّد أو إرجاع البضائع إلى المورّد.</span><span class="sxs-lookup"><span data-stu-id="d8d43-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="d8d43-137">ويمكنك إيقاف الدفع فقط على الشيكات التي لم ترسل إلى المقاصة.</span><span class="sxs-lookup"><span data-stu-id="d8d43-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="d8d43-138">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="d8d43-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="d8d43-139">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="d8d43-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="d8d43-140">تسجيل شيك بتاريخ لاحق لعميل وترحيله</span><span class="sxs-lookup"><span data-stu-id="d8d43-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="d8d43-141">تسوية شيك بتاريخ لاحق من عميل</span><span class="sxs-lookup"><span data-stu-id="d8d43-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="d8d43-142">تسجيل شيك بتاريخ لاحق لمورد وترحيله</span><span class="sxs-lookup"><span data-stu-id="d8d43-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="d8d43-143">تسوية شيك بتاريخ لاحق لمورد</span><span class="sxs-lookup"><span data-stu-id="d8d43-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



