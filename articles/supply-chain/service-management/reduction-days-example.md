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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "334095"
---
# <a name="reduction-days-example"></a><span data-ttu-id="d83cf-103">مثال أيام التخفيض</span><span class="sxs-lookup"><span data-stu-id="d83cf-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d83cf-104">لقد قمت بإنشاء حركة اشتراك للاشتراك في الحفاظ على العميل، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="d83cf-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="d83cf-105">من تاريخ</span><span class="sxs-lookup"><span data-stu-id="d83cf-105">From date</span></span></p></th>
<th><p><span data-ttu-id="d83cf-106">إلى تاريخ</span><span class="sxs-lookup"><span data-stu-id="d83cf-106">To date</span></span></p></th>
<th><p><span data-ttu-id="d83cf-107">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="d83cf-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d83cf-108">نوع الاشتراك</span><span class="sxs-lookup"><span data-stu-id="d83cf-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="d83cf-109">Project</span><span class="sxs-lookup"><span data-stu-id="d83cf-109">Project</span></span></p></th>
<th><p><span data-ttu-id="d83cf-110">الفئة</span><span class="sxs-lookup"><span data-stu-id="d83cf-110">Category</span></span></p></th>
<th><p><span data-ttu-id="d83cf-111">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="d83cf-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d83cf-112">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="d83cf-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d83cf-113">01 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="d83cf-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="d83cf-114">31 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="d83cf-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="d83cf-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="d83cf-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="d83cf-116"><strong>عادي</strong></span><span class="sxs-lookup"><span data-stu-id="d83cf-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="d83cf-117">9013</span><span class="sxs-lookup"><span data-stu-id="d83cf-117">9013</span></span></p></td>
<td><p><span data-ttu-id="d83cf-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d83cf-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d83cf-119">يورو</span><span class="sxs-lookup"><span data-stu-id="d83cf-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="d83cf-120">200.00</span><span class="sxs-lookup"><span data-stu-id="d83cf-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d83cf-121">تقارير العملاء التي لا تحتاج لتغطية خدمة لمدة يومين (10 مارس و11 مارس).</span><span class="sxs-lookup"><span data-stu-id="d83cf-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="d83cf-122">حيث توافق على تخفيض الاشتراك بمقدار هذين اليومين.</span><span class="sxs-lookup"><span data-stu-id="d83cf-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="d83cf-123">يمكنك إنشاء حركة جديدة من نوع **أيام التخفيض** كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="d83cf-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="d83cf-124">من تاريخ</span><span class="sxs-lookup"><span data-stu-id="d83cf-124">From date</span></span></p></th>
<th><p><span data-ttu-id="d83cf-125">إلى تاريخ</span><span class="sxs-lookup"><span data-stu-id="d83cf-125">To date</span></span></p></th>
<th><p><span data-ttu-id="d83cf-126">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="d83cf-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d83cf-127">نوع الاشتراك</span><span class="sxs-lookup"><span data-stu-id="d83cf-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="d83cf-128">Project</span><span class="sxs-lookup"><span data-stu-id="d83cf-128">Project</span></span></p></th>
<th><p><span data-ttu-id="d83cf-129">الفئة</span><span class="sxs-lookup"><span data-stu-id="d83cf-129">Category</span></span></p></th>
<th><p><span data-ttu-id="d83cf-130">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="d83cf-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d83cf-131">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="d83cf-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d83cf-132">10 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="d83cf-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="d83cf-133">11 مارس، 2011</span><span class="sxs-lookup"><span data-stu-id="d83cf-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="d83cf-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="d83cf-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="d83cf-135"><strong>أيام التخفيض</strong></span><span class="sxs-lookup"><span data-stu-id="d83cf-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="d83cf-136">9013</span><span class="sxs-lookup"><span data-stu-id="d83cf-136">9013</span></span></p></td>
<td><p><span data-ttu-id="d83cf-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d83cf-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d83cf-138">يورو</span><span class="sxs-lookup"><span data-stu-id="d83cf-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="d83cf-139">12.90-</span><span class="sxs-lookup"><span data-stu-id="d83cf-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d83cf-140">عندما تتم فوترة الحركات لشهر مارس 2011، سيتم تخفيض سعر البيع من 200 يورو إلى 12.90 يورو.</span><span class="sxs-lookup"><span data-stu-id="d83cf-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="d83cf-141">وسيكون المبلغ الخاضع للرسوم لحركة الاشتراك هو 187.10 يورو، حيث تتم فوترة حركتين بإجمالي سعر يبلغ 187.10 يورو.</span><span class="sxs-lookup"><span data-stu-id="d83cf-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="d83cf-142">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d83cf-142">See also</span></span>

[<span data-ttu-id="d83cf-143">تقليل الأيام على رسوم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="d83cf-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


