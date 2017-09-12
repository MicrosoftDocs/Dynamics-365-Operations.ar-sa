---
title: "قيم كائن المخزون"
description: "توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4aec6e70325c7e4d00e6070293a1ab0c719e420b
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="inventory-object-values"></a><span data-ttu-id="03eff-103">قيم كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="03eff-103">Inventory object values</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="03eff-104">توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون.</span><span class="sxs-lookup"><span data-stu-id="03eff-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="03eff-105">تتيح لك وظائف جديدة باسم **الكمية الفعلية**مشاهدة قيم كائن المخزون المحدد.</span><span class="sxs-lookup"><span data-stu-id="03eff-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="03eff-106">ويمثل كائن التكلفة مستوى الكيان حيث يتم إجراء محاسبة المخزون.</span><span class="sxs-lookup"><span data-stu-id="03eff-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="03eff-107">لمزيد من المعلومات حول كائنات التكلفة، راجع [كائنات التكلفة](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="03eff-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="03eff-108">‏‫ولمشاهدة قيم كائن مخزون محدد، انقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="03eff-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="03eff-109">وإليك كيفية حساب قيمة كائن المخزون:</span><span class="sxs-lookup"><span data-stu-id="03eff-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="03eff-110">كائن المخزون.القيمة = كائن المخزون.متوسط تكلفة الوحدة × كائن المخزون.الكمية</span><span class="sxs-lookup"><span data-stu-id="03eff-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="03eff-111">يوضح المثال التالي كيفية حساب قيم كائن مخزون وكائن تكلفة.</span><span class="sxs-lookup"><span data-stu-id="03eff-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="03eff-112">تم تسجيل حدثي استلام منتجات في الصنف أ:</span><span class="sxs-lookup"><span data-stu-id="03eff-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="03eff-113">إيصال استلام المنتج 1: الكمية = 100 قطعة، مبلغ = 1000.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="03eff-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="03eff-114">= B1</span><span class="sxs-lookup"><span data-stu-id="03eff-114">= B1</span></span>
-   <span data-ttu-id="03eff-115">إيصال استلام المنتج 2: الكمية = 50 قطعة، مبلغ = 800.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="03eff-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="03eff-116">= B2</span><span class="sxs-lookup"><span data-stu-id="03eff-116">= B2</span></span>

<span data-ttu-id="03eff-117">يعرض الجدول التالي نتيجة عملية الحساب لكائن تكلفة.</span><span class="sxs-lookup"><span data-stu-id="03eff-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="03eff-118">يمكنك عرض النتيجة في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="03eff-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="03eff-119">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="03eff-119">Object type</span></span></th>
<th><span data-ttu-id="03eff-120">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="03eff-120">Item number</span></span></th>
<th><span data-ttu-id="03eff-121">الموقع</span><span class="sxs-lookup"><span data-stu-id="03eff-121">Site</span></span></th>
<th><span data-ttu-id="03eff-122">الكمية</span><span class="sxs-lookup"><span data-stu-id="03eff-122">Quantity</span></span></th>
<th><span data-ttu-id="03eff-123">وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="03eff-123">Inventory unit</span></span></th>
<th><span data-ttu-id="03eff-124">القيمة</span><span class="sxs-lookup"><span data-stu-id="03eff-124">Value</span></span></th>
<th><span data-ttu-id="03eff-125">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="03eff-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03eff-126">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="03eff-126">Cost object</span></span></td>
<td><span data-ttu-id="03eff-127">أ</span><span class="sxs-lookup"><span data-stu-id="03eff-127">A</span></span></td>
<td><span data-ttu-id="03eff-128">1</span><span class="sxs-lookup"><span data-stu-id="03eff-128">1</span></span></td>
<td><span data-ttu-id="03eff-129">150</span><span class="sxs-lookup"><span data-stu-id="03eff-129">150</span></span></td>
<td><span data-ttu-id="03eff-130">أجزاء</span><span class="sxs-lookup"><span data-stu-id="03eff-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="03eff-131">1800.00 دولار</span><span class="sxs-lookup"><span data-stu-id="03eff-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="03eff-132">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="03eff-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="03eff-133">يعرض الجدول التالي نتيجة عملية الحساب لكائن مخزون.</span><span class="sxs-lookup"><span data-stu-id="03eff-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="03eff-134">يمكنك عرض النتيجة بالنقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="03eff-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="03eff-135">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="03eff-135">Object type</span></span></th>
<th><span data-ttu-id="03eff-136">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="03eff-136">Item number</span></span></th>
<th><span data-ttu-id="03eff-137">الموقع</span><span class="sxs-lookup"><span data-stu-id="03eff-137">Site</span></span></th>
<th><span data-ttu-id="03eff-138">المستودع</span><span class="sxs-lookup"><span data-stu-id="03eff-138">Warehouse</span></span></th>
<th><span data-ttu-id="03eff-139">رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="03eff-139">Batch No.</span></span></th>
<th><span data-ttu-id="03eff-140">الكمية</span><span class="sxs-lookup"><span data-stu-id="03eff-140">Quantity</span></span></th>
<th><span data-ttu-id="03eff-141">وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="03eff-141">Inventory unit</span></span></th>
<th><span data-ttu-id="03eff-142">القيمة</span><span class="sxs-lookup"><span data-stu-id="03eff-142">Value</span></span></th>
<th><span data-ttu-id="03eff-143">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="03eff-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03eff-144">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="03eff-144">Inventory object</span></span></td>
<td><span data-ttu-id="03eff-145">أ</span><span class="sxs-lookup"><span data-stu-id="03eff-145">A</span></span></td>
<td><span data-ttu-id="03eff-146">1</span><span class="sxs-lookup"><span data-stu-id="03eff-146">1</span></span></td>
<td><span data-ttu-id="03eff-147">11</span><span class="sxs-lookup"><span data-stu-id="03eff-147">11</span></span></td>
<td><span data-ttu-id="03eff-148">ب1</span><span class="sxs-lookup"><span data-stu-id="03eff-148">B1</span></span></td>
<td><span data-ttu-id="03eff-149">100</span><span class="sxs-lookup"><span data-stu-id="03eff-149">100</span></span></td>
<td><span data-ttu-id="03eff-150">أجزاء</span><span class="sxs-lookup"><span data-stu-id="03eff-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="03eff-151">1200.00 دولار</span><span class="sxs-lookup"><span data-stu-id="03eff-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="03eff-152">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="03eff-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eff-153">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="03eff-153">Inventory object</span></span></td>
<td><span data-ttu-id="03eff-154">أ</span><span class="sxs-lookup"><span data-stu-id="03eff-154">A</span></span></td>
<td><span data-ttu-id="03eff-155">1</span><span class="sxs-lookup"><span data-stu-id="03eff-155">1</span></span></td>
<td><span data-ttu-id="03eff-156">11</span><span class="sxs-lookup"><span data-stu-id="03eff-156">11</span></span></td>
<td><span data-ttu-id="03eff-157">ب2</span><span class="sxs-lookup"><span data-stu-id="03eff-157">B2</span></span></td>
<td><span data-ttu-id="03eff-158">50</span><span class="sxs-lookup"><span data-stu-id="03eff-158">50</span></span></td>
<td><span data-ttu-id="03eff-159">أجزاء</span><span class="sxs-lookup"><span data-stu-id="03eff-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="03eff-160">600.00 دولار</span><span class="sxs-lookup"><span data-stu-id="03eff-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="03eff-161">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="03eff-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="03eff-162">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="03eff-162">See also</span></span>
--------

[<span data-ttu-id="03eff-163">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="03eff-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="03eff-164">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="03eff-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="03eff-165">الميزات الجديدة والمتغيرة</span><span class="sxs-lookup"><span data-stu-id="03eff-165">What's new and changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)




