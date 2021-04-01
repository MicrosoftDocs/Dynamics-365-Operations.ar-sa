---
title: قيم كائن المخزون
description: توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f14248ffa8f9f5a460b090ca5754442cd50bf45a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263532"
---
# <a name="inventory-object-values"></a><span data-ttu-id="02d8a-103">قيم كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="02d8a-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02d8a-104">توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون.</span><span class="sxs-lookup"><span data-stu-id="02d8a-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="02d8a-105">تتيح لك وظائف جديدة باسم **الكمية الفعلية** مشاهدة قيم كائن المخزون المحدد.</span><span class="sxs-lookup"><span data-stu-id="02d8a-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="02d8a-106">ويمثل كائن التكلفة مستوى الكيان حيث يتم إجراء محاسبة المخزون.</span><span class="sxs-lookup"><span data-stu-id="02d8a-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="02d8a-107">لمزيد من المعلومات حول كائنات التكلفة، راجع [كائنات التكلفة](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="02d8a-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="02d8a-108">‏‫ولمشاهدة قيم كائن مخزون محدد، انقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="02d8a-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="02d8a-109">وإليك كيفية حساب قيمة كائن المخزون:</span><span class="sxs-lookup"><span data-stu-id="02d8a-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="02d8a-110">كائن المخزون.القيمة = كائن المخزون.متوسط تكلفة الوحدة × كائن المخزون.الكمية</span><span class="sxs-lookup"><span data-stu-id="02d8a-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="02d8a-111">يوضح المثال التالي كيفية حساب قيم كائن مخزون وكائن تكلفة.</span><span class="sxs-lookup"><span data-stu-id="02d8a-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="02d8a-112">تم تسجيل حدثي استلام منتجات في الصنف أ:</span><span class="sxs-lookup"><span data-stu-id="02d8a-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="02d8a-113">إيصال استلام المنتج 1: الكمية = 100 قطعة، مبلغ = 1000.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="02d8a-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="02d8a-114">= B1</span><span class="sxs-lookup"><span data-stu-id="02d8a-114">= B1</span></span>
-   <span data-ttu-id="02d8a-115">إيصال استلام المنتج 2: الكمية = 50 قطعة، مبلغ = 800.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="02d8a-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="02d8a-116">= B2</span><span class="sxs-lookup"><span data-stu-id="02d8a-116">= B2</span></span>

<span data-ttu-id="02d8a-117">يعرض الجدول التالي نتيجة عملية الحساب لكائن تكلفة.</span><span class="sxs-lookup"><span data-stu-id="02d8a-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="02d8a-118">يمكنك عرض النتيجة في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="02d8a-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02d8a-119">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="02d8a-119">Object type</span></span></th>
<th><span data-ttu-id="02d8a-120">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="02d8a-120">Item number</span></span></th>
<th><span data-ttu-id="02d8a-121">الموقع</span><span class="sxs-lookup"><span data-stu-id="02d8a-121">Site</span></span></th>
<th><span data-ttu-id="02d8a-122">الكمية</span><span class="sxs-lookup"><span data-stu-id="02d8a-122">Quantity</span></span></th>
<th><span data-ttu-id="02d8a-123">وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="02d8a-123">Inventory unit</span></span></th>
<th><span data-ttu-id="02d8a-124">القيمة</span><span class="sxs-lookup"><span data-stu-id="02d8a-124">Value</span></span></th>
<th><span data-ttu-id="02d8a-125">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="02d8a-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02d8a-126">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="02d8a-126">Cost object</span></span></td>
<td><span data-ttu-id="02d8a-127">أ</span><span class="sxs-lookup"><span data-stu-id="02d8a-127">A</span></span></td>
<td><span data-ttu-id="02d8a-128">1</span><span class="sxs-lookup"><span data-stu-id="02d8a-128">1</span></span></td>
<td><span data-ttu-id="02d8a-129">150</span><span class="sxs-lookup"><span data-stu-id="02d8a-129">150</span></span></td>
<td><span data-ttu-id="02d8a-130">أجزاء</span><span class="sxs-lookup"><span data-stu-id="02d8a-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="02d8a-131">1800.00 دولار</span><span class="sxs-lookup"><span data-stu-id="02d8a-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="02d8a-132">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="02d8a-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="02d8a-133">يعرض الجدول التالي نتيجة عملية الحساب لكائن مخزون.</span><span class="sxs-lookup"><span data-stu-id="02d8a-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="02d8a-134">يمكنك عرض النتيجة بالنقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="02d8a-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02d8a-135">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="02d8a-135">Object type</span></span></th>
<th><span data-ttu-id="02d8a-136">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="02d8a-136">Item number</span></span></th>
<th><span data-ttu-id="02d8a-137">الموقع</span><span class="sxs-lookup"><span data-stu-id="02d8a-137">Site</span></span></th>
<th><span data-ttu-id="02d8a-138">المستودع</span><span class="sxs-lookup"><span data-stu-id="02d8a-138">Warehouse</span></span></th>
<th><span data-ttu-id="02d8a-139">رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="02d8a-139">Batch No.</span></span></th>
<th><span data-ttu-id="02d8a-140">الكمية</span><span class="sxs-lookup"><span data-stu-id="02d8a-140">Quantity</span></span></th>
<th><span data-ttu-id="02d8a-141">وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="02d8a-141">Inventory unit</span></span></th>
<th><span data-ttu-id="02d8a-142">القيمة</span><span class="sxs-lookup"><span data-stu-id="02d8a-142">Value</span></span></th>
<th><span data-ttu-id="02d8a-143">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="02d8a-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02d8a-144">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="02d8a-144">Inventory object</span></span></td>
<td><span data-ttu-id="02d8a-145">أ</span><span class="sxs-lookup"><span data-stu-id="02d8a-145">A</span></span></td>
<td><span data-ttu-id="02d8a-146">1</span><span class="sxs-lookup"><span data-stu-id="02d8a-146">1</span></span></td>
<td><span data-ttu-id="02d8a-147">11</span><span class="sxs-lookup"><span data-stu-id="02d8a-147">11</span></span></td>
<td><span data-ttu-id="02d8a-148">ب1</span><span class="sxs-lookup"><span data-stu-id="02d8a-148">B1</span></span></td>
<td><span data-ttu-id="02d8a-149">100</span><span class="sxs-lookup"><span data-stu-id="02d8a-149">100</span></span></td>
<td><span data-ttu-id="02d8a-150">أجزاء</span><span class="sxs-lookup"><span data-stu-id="02d8a-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="02d8a-151">1200.00 دولار</span><span class="sxs-lookup"><span data-stu-id="02d8a-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="02d8a-152">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="02d8a-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02d8a-153">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="02d8a-153">Inventory object</span></span></td>
<td><span data-ttu-id="02d8a-154">و</span><span class="sxs-lookup"><span data-stu-id="02d8a-154">A</span></span></td>
<td><span data-ttu-id="02d8a-155">1</span><span class="sxs-lookup"><span data-stu-id="02d8a-155">1</span></span></td>
<td><span data-ttu-id="02d8a-156">11</span><span class="sxs-lookup"><span data-stu-id="02d8a-156">11</span></span></td>
<td><span data-ttu-id="02d8a-157">ب2</span><span class="sxs-lookup"><span data-stu-id="02d8a-157">B2</span></span></td>
<td><span data-ttu-id="02d8a-158">50</span><span class="sxs-lookup"><span data-stu-id="02d8a-158">50</span></span></td>
<td><span data-ttu-id="02d8a-159">أجزاء</span><span class="sxs-lookup"><span data-stu-id="02d8a-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="02d8a-160">600.00 دولار</span><span class="sxs-lookup"><span data-stu-id="02d8a-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="02d8a-161">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="02d8a-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="02d8a-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="02d8a-162">Additional resources</span></span>
--------

[<span data-ttu-id="02d8a-163">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="02d8a-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="02d8a-164">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="02d8a-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="02d8a-165">الميزات الجديدة والمتغيرة</span><span class="sxs-lookup"><span data-stu-id="02d8a-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]