---
title: مثال أيام التخفيض
description: مثال أيام التخفيض.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975646"
---
# <a name="reduction-days-example"></a><span data-ttu-id="65d88-103">مثال أيام التخفيض</span><span class="sxs-lookup"><span data-stu-id="65d88-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="65d88-104">لقد قمت بإنشاء حركة اشتراك للاشتراك في الحفاظ على العميل، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="65d88-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65d88-105">من تاريخ</span><span class="sxs-lookup"><span data-stu-id="65d88-105">From date</span></span></p></th>
<th><p><span data-ttu-id="65d88-106">إلى تاريخ</span><span class="sxs-lookup"><span data-stu-id="65d88-106">To date</span></span></p></th>
<th><p><span data-ttu-id="65d88-107">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="65d88-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="65d88-108">نوع الاشتراك</span><span class="sxs-lookup"><span data-stu-id="65d88-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="65d88-109">Project</span><span class="sxs-lookup"><span data-stu-id="65d88-109">Project</span></span></p></th>
<th><p><span data-ttu-id="65d88-110">الفئة</span><span class="sxs-lookup"><span data-stu-id="65d88-110">Category</span></span></p></th>
<th><p><span data-ttu-id="65d88-111">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="65d88-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="65d88-112">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="65d88-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65d88-113">01 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="65d88-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="65d88-114">31 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="65d88-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="65d88-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="65d88-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="65d88-116"><strong>عادي</strong></span><span class="sxs-lookup"><span data-stu-id="65d88-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="65d88-117">9013</span><span class="sxs-lookup"><span data-stu-id="65d88-117">9013</span></span></p></td>
<td><p><span data-ttu-id="65d88-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="65d88-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="65d88-119">يورو</span><span class="sxs-lookup"><span data-stu-id="65d88-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="65d88-120">200.00</span><span class="sxs-lookup"><span data-stu-id="65d88-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65d88-121">تقارير العملاء التي لا تحتاج لتغطية خدمة لمدة يومين (10 مارس و11 مارس).</span><span class="sxs-lookup"><span data-stu-id="65d88-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="65d88-122">حيث توافق على تخفيض الاشتراك بمقدار هذين اليومين.</span><span class="sxs-lookup"><span data-stu-id="65d88-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="65d88-123">يمكنك إنشاء حركة جديدة من نوع **أيام التخفيض** كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="65d88-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65d88-124">من تاريخ</span><span class="sxs-lookup"><span data-stu-id="65d88-124">From date</span></span></p></th>
<th><p><span data-ttu-id="65d88-125">إلى تاريخ</span><span class="sxs-lookup"><span data-stu-id="65d88-125">To date</span></span></p></th>
<th><p><span data-ttu-id="65d88-126">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="65d88-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="65d88-127">نوع الاشتراك</span><span class="sxs-lookup"><span data-stu-id="65d88-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="65d88-128">Project</span><span class="sxs-lookup"><span data-stu-id="65d88-128">Project</span></span></p></th>
<th><p><span data-ttu-id="65d88-129">الفئة</span><span class="sxs-lookup"><span data-stu-id="65d88-129">Category</span></span></p></th>
<th><p><span data-ttu-id="65d88-130">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="65d88-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="65d88-131">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="65d88-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65d88-132">10 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="65d88-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="65d88-133">11 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="65d88-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="65d88-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="65d88-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="65d88-135"><strong>أيام التخفيض</strong></span><span class="sxs-lookup"><span data-stu-id="65d88-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="65d88-136">9013</span><span class="sxs-lookup"><span data-stu-id="65d88-136">9013</span></span></p></td>
<td><p><span data-ttu-id="65d88-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="65d88-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="65d88-138">يورو</span><span class="sxs-lookup"><span data-stu-id="65d88-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="65d88-139">12.90-</span><span class="sxs-lookup"><span data-stu-id="65d88-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65d88-140">عندما تتم فوترة الحركات لشهر مارس 2011، سيتم تخفيض سعر البيع من 200 يورو إلى 12.90 يورو.</span><span class="sxs-lookup"><span data-stu-id="65d88-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="65d88-141">وسيكون المبلغ الخاضع للرسوم لحركة الاشتراك هو 187.10 يورو، حيث تتم فوترة حركتين بإجمالي سعر يبلغ 187.10 يورو.</span><span class="sxs-lookup"><span data-stu-id="65d88-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="65d88-142">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="65d88-142">See also</span></span>

[<span data-ttu-id="65d88-143">تقليل الأيام على رسوم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="65d88-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


