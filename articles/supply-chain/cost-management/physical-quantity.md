---
title: قيم كائن المخزون
description: توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 543253714b3cf318ad5f6092b190e777772f956f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910127"
---
# <a name="inventory-object-values"></a><span data-ttu-id="8c6ed-103">قيم كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="8c6ed-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c6ed-104">توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="8c6ed-105">تتيح لك وظائف جديدة باسم **الكمية الفعلية** مشاهدة قيم كائن المخزون المحدد.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="8c6ed-106">ويمثل كائن التكلفة مستوى الكيان حيث يتم إجراء محاسبة المخزون.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="8c6ed-107">لمزيد من المعلومات حول كائنات التكلفة، راجع [كائنات التكلفة](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="8c6ed-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="8c6ed-108">‏‫ولمشاهدة قيم كائن مخزون محدد، انقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="8c6ed-109">وإليك كيفية حساب قيمة كائن المخزون:</span><span class="sxs-lookup"><span data-stu-id="8c6ed-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="8c6ed-110">كائن المخزون.القيمة = كائن المخزون.متوسط تكلفة الوحدة × كائن المخزون.الكمية</span><span class="sxs-lookup"><span data-stu-id="8c6ed-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="8c6ed-111">يوضح المثال التالي كيفية حساب قيم كائن مخزون وكائن تكلفة.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="8c6ed-112">تم تسجيل حدثي استلام منتجات في الصنف أ:</span><span class="sxs-lookup"><span data-stu-id="8c6ed-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="8c6ed-113">إيصال استلام المنتج 1: الكمية = 100 قطعة، مبلغ = 1000.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="8c6ed-114">= B1</span><span class="sxs-lookup"><span data-stu-id="8c6ed-114">= B1</span></span>
-   <span data-ttu-id="8c6ed-115">إيصال استلام المنتج 2: الكمية = 50 قطعة، مبلغ = 800.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="8c6ed-116">= B2</span><span class="sxs-lookup"><span data-stu-id="8c6ed-116">= B2</span></span>

<span data-ttu-id="8c6ed-117">يعرض الجدول التالي نتيجة عملية الحساب لكائن تكلفة.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="8c6ed-118">يمكنك عرض النتيجة في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="8c6ed-119">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="8c6ed-119">Object type</span></span></th>
<th><span data-ttu-id="8c6ed-120">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="8c6ed-120">Item number</span></span></th>
<th><span data-ttu-id="8c6ed-121">الموقع</span><span class="sxs-lookup"><span data-stu-id="8c6ed-121">Site</span></span></th>
<th><span data-ttu-id="8c6ed-122">الكمية</span><span class="sxs-lookup"><span data-stu-id="8c6ed-122">Quantity</span></span></th>
<th><span data-ttu-id="8c6ed-123">وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="8c6ed-123">Inventory unit</span></span></th>
<th><span data-ttu-id="8c6ed-124">القيمة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-124">Value</span></span></th>
<th><span data-ttu-id="8c6ed-125">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c6ed-126">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-126">Cost object</span></span></td>
<td><span data-ttu-id="8c6ed-127">أ</span><span class="sxs-lookup"><span data-stu-id="8c6ed-127">A</span></span></td>
<td><span data-ttu-id="8c6ed-128">1</span><span class="sxs-lookup"><span data-stu-id="8c6ed-128">1</span></span></td>
<td><span data-ttu-id="8c6ed-129">150</span><span class="sxs-lookup"><span data-stu-id="8c6ed-129">150</span></span></td>
<td><span data-ttu-id="8c6ed-130">أجزاء</span><span class="sxs-lookup"><span data-stu-id="8c6ed-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="8c6ed-131">1800.00 دولار</span><span class="sxs-lookup"><span data-stu-id="8c6ed-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-132">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="8c6ed-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8c6ed-133">يعرض الجدول التالي نتيجة عملية الحساب لكائن مخزون.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="8c6ed-134">يمكنك عرض النتيجة بالنقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="8c6ed-135">نوع الكائن</span><span class="sxs-lookup"><span data-stu-id="8c6ed-135">Object type</span></span></th>
<th><span data-ttu-id="8c6ed-136">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="8c6ed-136">Item number</span></span></th>
<th><span data-ttu-id="8c6ed-137">الموقع</span><span class="sxs-lookup"><span data-stu-id="8c6ed-137">Site</span></span></th>
<th><span data-ttu-id="8c6ed-138">المستودع</span><span class="sxs-lookup"><span data-stu-id="8c6ed-138">Warehouse</span></span></th>
<th><span data-ttu-id="8c6ed-139">رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-139">Batch No.</span></span></th>
<th><span data-ttu-id="8c6ed-140">الكمية</span><span class="sxs-lookup"><span data-stu-id="8c6ed-140">Quantity</span></span></th>
<th><span data-ttu-id="8c6ed-141">وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="8c6ed-141">Inventory unit</span></span></th>
<th><span data-ttu-id="8c6ed-142">القيمة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-142">Value</span></span></th>
<th><span data-ttu-id="8c6ed-143">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c6ed-144">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="8c6ed-144">Inventory object</span></span></td>
<td><span data-ttu-id="8c6ed-145">أ</span><span class="sxs-lookup"><span data-stu-id="8c6ed-145">A</span></span></td>
<td><span data-ttu-id="8c6ed-146">1</span><span class="sxs-lookup"><span data-stu-id="8c6ed-146">1</span></span></td>
<td><span data-ttu-id="8c6ed-147">11</span><span class="sxs-lookup"><span data-stu-id="8c6ed-147">11</span></span></td>
<td><span data-ttu-id="8c6ed-148">ب1</span><span class="sxs-lookup"><span data-stu-id="8c6ed-148">B1</span></span></td>
<td><span data-ttu-id="8c6ed-149">100</span><span class="sxs-lookup"><span data-stu-id="8c6ed-149">100</span></span></td>
<td><span data-ttu-id="8c6ed-150">أجزاء</span><span class="sxs-lookup"><span data-stu-id="8c6ed-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="8c6ed-151">1200.00 دولار</span><span class="sxs-lookup"><span data-stu-id="8c6ed-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-152">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="8c6ed-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6ed-153">كائن المخزون</span><span class="sxs-lookup"><span data-stu-id="8c6ed-153">Inventory object</span></span></td>
<td><span data-ttu-id="8c6ed-154">و</span><span class="sxs-lookup"><span data-stu-id="8c6ed-154">A</span></span></td>
<td><span data-ttu-id="8c6ed-155">1</span><span class="sxs-lookup"><span data-stu-id="8c6ed-155">1</span></span></td>
<td><span data-ttu-id="8c6ed-156">11</span><span class="sxs-lookup"><span data-stu-id="8c6ed-156">11</span></span></td>
<td><span data-ttu-id="8c6ed-157">ب2</span><span class="sxs-lookup"><span data-stu-id="8c6ed-157">B2</span></span></td>
<td><span data-ttu-id="8c6ed-158">50</span><span class="sxs-lookup"><span data-stu-id="8c6ed-158">50</span></span></td>
<td><span data-ttu-id="8c6ed-159">أجزاء</span><span class="sxs-lookup"><span data-stu-id="8c6ed-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="8c6ed-160">600.00 دولار</span><span class="sxs-lookup"><span data-stu-id="8c6ed-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-161">12.00 دولارًا</span><span class="sxs-lookup"><span data-stu-id="8c6ed-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="8c6ed-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8c6ed-162">Additional resources</span></span>
--------

[<span data-ttu-id="8c6ed-163">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="8c6ed-164">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="8c6ed-165">الميزات الجديدة والمتغيرة</span><span class="sxs-lookup"><span data-stu-id="8c6ed-165">What's new and changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]