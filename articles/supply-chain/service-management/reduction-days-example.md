---
title: مثال أيام التخفيض
description: مثال أيام التخفيض.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564498"
---
# <a name="reduction-days-example"></a><span data-ttu-id="71733-103">مثال أيام التخفيض</span><span class="sxs-lookup"><span data-stu-id="71733-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="71733-104">لقد قمت بإنشاء حركة اشتراك للاشتراك في الحفاظ على العميل، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="71733-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="71733-105">من تاريخ</span><span class="sxs-lookup"><span data-stu-id="71733-105">From date</span></span></p></th>
<th><p><span data-ttu-id="71733-106">إلى تاريخ</span><span class="sxs-lookup"><span data-stu-id="71733-106">To date</span></span></p></th>
<th><p><span data-ttu-id="71733-107">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="71733-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="71733-108">نوع الاشتراك</span><span class="sxs-lookup"><span data-stu-id="71733-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="71733-109">Project</span><span class="sxs-lookup"><span data-stu-id="71733-109">Project</span></span></p></th>
<th><p><span data-ttu-id="71733-110">الفئة</span><span class="sxs-lookup"><span data-stu-id="71733-110">Category</span></span></p></th>
<th><p><span data-ttu-id="71733-111">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="71733-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="71733-112">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="71733-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71733-113">01 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="71733-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="71733-114">31 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="71733-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="71733-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="71733-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="71733-116"><strong>عادي</strong></span><span class="sxs-lookup"><span data-stu-id="71733-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="71733-117">9013</span><span class="sxs-lookup"><span data-stu-id="71733-117">9013</span></span></p></td>
<td><p><span data-ttu-id="71733-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="71733-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="71733-119">يورو</span><span class="sxs-lookup"><span data-stu-id="71733-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="71733-120">200.00</span><span class="sxs-lookup"><span data-stu-id="71733-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71733-121">تقارير العملاء التي لا تحتاج لتغطية خدمة لمدة يومين (10 مارس و11 مارس).</span><span class="sxs-lookup"><span data-stu-id="71733-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="71733-122">حيث توافق على تخفيض الاشتراك بمقدار هذين اليومين.</span><span class="sxs-lookup"><span data-stu-id="71733-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="71733-123">يمكنك إنشاء حركة جديدة من نوع **أيام التخفيض** كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="71733-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="71733-124">من تاريخ</span><span class="sxs-lookup"><span data-stu-id="71733-124">From date</span></span></p></th>
<th><p><span data-ttu-id="71733-125">إلى تاريخ</span><span class="sxs-lookup"><span data-stu-id="71733-125">To date</span></span></p></th>
<th><p><span data-ttu-id="71733-126">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="71733-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="71733-127">نوع الاشتراك</span><span class="sxs-lookup"><span data-stu-id="71733-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="71733-128">Project</span><span class="sxs-lookup"><span data-stu-id="71733-128">Project</span></span></p></th>
<th><p><span data-ttu-id="71733-129">الفئة</span><span class="sxs-lookup"><span data-stu-id="71733-129">Category</span></span></p></th>
<th><p><span data-ttu-id="71733-130">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="71733-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="71733-131">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="71733-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71733-132">10 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="71733-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="71733-133">11 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="71733-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="71733-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="71733-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="71733-135"><strong>أيام التخفيض</strong></span><span class="sxs-lookup"><span data-stu-id="71733-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="71733-136">9013</span><span class="sxs-lookup"><span data-stu-id="71733-136">9013</span></span></p></td>
<td><p><span data-ttu-id="71733-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="71733-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="71733-138">يورو</span><span class="sxs-lookup"><span data-stu-id="71733-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="71733-139">12.90-</span><span class="sxs-lookup"><span data-stu-id="71733-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71733-140">عندما تتم فوترة الحركات لشهر مارس 2011، سيتم تخفيض سعر البيع من 200 يورو إلى 12.90 يورو.</span><span class="sxs-lookup"><span data-stu-id="71733-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="71733-141">وسيكون المبلغ الخاضع للرسوم لحركة الاشتراك هو 187.10 يورو، حيث تتم فوترة حركتين بإجمالي سعر يبلغ 187.10 يورو.</span><span class="sxs-lookup"><span data-stu-id="71733-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="71733-142">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="71733-142">See also</span></span>

[<span data-ttu-id="71733-143">تقليل الأيام على رسوم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="71733-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


