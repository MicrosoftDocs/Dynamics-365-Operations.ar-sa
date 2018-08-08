---
title: "إدخالات التكلفة"
description: "توفر هذه المقالة معلومات حول إدخالات التكلفة والحالات التي يتم فيها إنشاء هذه الإدخالات. إدخال التكلفة هو سجل لتسجيل كمية وتكلفة لحدث محدد."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: cb1a218dd5e6ab3f8029788af359b89521d6afdc
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="cost-entries"></a><span data-ttu-id="62d7c-104">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="62d7c-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62d7c-105">توفر هذه المقالة معلومات حول إدخالات التكلفة والحالات التي يتم فيها إنشاء هذه الإدخالات.</span><span class="sxs-lookup"><span data-stu-id="62d7c-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="62d7c-106">إدخال التكلفة هو سجل لتسجيل كمية وتكلفة لحدث محدد.</span><span class="sxs-lookup"><span data-stu-id="62d7c-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="62d7c-107">إدخالات التكلفة هي تجميعات حركات المخزون التي تم تسجيلها في أبعاد المخزون المالية النشطة.</span><span class="sxs-lookup"><span data-stu-id="62d7c-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="62d7c-108">أمثلة</span><span class="sxs-lookup"><span data-stu-id="62d7c-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="62d7c-109">مثال 1: لم يتم إنشاء أي إدخالات تكلفة</span><span class="sxs-lookup"><span data-stu-id="62d7c-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="62d7c-110">يتم تسجيل حدث دفتر يومية نقل.</span><span class="sxs-lookup"><span data-stu-id="62d7c-110">A transfer journal event is registered.</span></span> <span data-ttu-id="62d7c-111">وينقل الحدث قطعة واحدة من الصنف أ من الموقع أ إلى الموقع ب, ولا يعتبر بُعد مخزون الموقع جزءًا من كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="62d7c-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="62d7c-112">ولذلك، يُنشئ الحدث حركتي مخزون وأي إدخالات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="62d7c-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="62d7c-113">مثال 2: يتم إنشاء إدخالات تكلفة</span><span class="sxs-lookup"><span data-stu-id="62d7c-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="62d7c-114">يتم تسجيل حدث دفتر يومية نقل.</span><span class="sxs-lookup"><span data-stu-id="62d7c-114">A transfer journal event is registered.</span></span> <span data-ttu-id="62d7c-115">‏‫وينقل الحدث قطعة واحدة من الصنف أ من الموقع 1 إلى الموقع 2،</span><span class="sxs-lookup"><span data-stu-id="62d7c-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="62d7c-116">ولا يعتبر بُعد مخزون الموقع جزءًا من كائن التكلفة.‬</span><span class="sxs-lookup"><span data-stu-id="62d7c-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="62d7c-117">ولذلك، يُنشئ الحدث حركتي مخزون وإدخالي تكلفة.</span><span class="sxs-lookup"><span data-stu-id="62d7c-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="62d7c-118">مثال 3: يتم إنشاء إدخال تكلفة واحد</span><span class="sxs-lookup"><span data-stu-id="62d7c-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="62d7c-119">يتم تسجيل حدث استلام منتج لأمر شراء.</span><span class="sxs-lookup"><span data-stu-id="62d7c-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="62d7c-120">يسجل الحدث 100 قطعة من الصنف أ بتكلفة الوحدة 10.00 دولار أمريكي (USD).</span><span class="sxs-lookup"><span data-stu-id="62d7c-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="62d7c-121">ونظرًا لأن الصنف أ يستخدم رقمًا مسلسلاً لتعقب غرض إدارة المخزون، فإنه يتم إنشاء رقم تسلسلي فريد لكل صنف يتم استلامه.</span><span class="sxs-lookup"><span data-stu-id="62d7c-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="62d7c-122">ولذلك، يُنشئ الحدث 100 حركة مخزون وإدخال تكلفة واحد.</span><span class="sxs-lookup"><span data-stu-id="62d7c-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="62d7c-123">صفحة إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="62d7c-123">Cost entries page</span></span>
<span data-ttu-id="62d7c-124">تتيح لك صفحة **إدخالات التكلفة**عرض والتحكم في التسجيلات الخاصة بالتكاليف والكميات.</span><span class="sxs-lookup"><span data-stu-id="62d7c-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="62d7c-125">وتكمل هذه الصفحة صفحتي **حركة المخزون** و**تسوية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="62d7c-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="62d7c-126">ويتم تسجيل السجلات بترتيب زمني لحدث ما.</span><span class="sxs-lookup"><span data-stu-id="62d7c-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="62d7c-127">ولذلك، يمكنك بسرعة العثور على والتحكم في التكاليف المتراكمة لحدث معين أو كافة الأحداث المرتبطة بمستند.</span><span class="sxs-lookup"><span data-stu-id="62d7c-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="62d7c-128">وفيما يلي مثال على ذلك:</span><span class="sxs-lookup"><span data-stu-id="62d7c-128">Here is an example:</span></span>

-   <span data-ttu-id="62d7c-129">يتم تسجيل حدث استلام منتج للصنف أ. ويتم استلام مائة قطعة بتكلفة وحدة 10.00 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="62d7c-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="62d7c-130">وبعد تسجيل حدث الفاتورة بأيام قليلة، تزداد التكلفة إلى 11.00 دولاراً أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="62d7c-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="62d7c-131">ولذلك، يبلغ إجمالي المبلغ 1,100 دولارًا أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="62d7c-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="62d7c-132">ويتم إنشاء إيصال ثاني لحساب الفرق بمبلغ 100 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="62d7c-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="62d7c-133">بعد بضعة أيام، يتم تسجيل مصاريف متنوعة بمبلغ 15.00 دولاراً أمريكيًا لتغطية تكلفة النقل في أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="62d7c-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="62d7c-134">الإيصال</span><span class="sxs-lookup"><span data-stu-id="62d7c-134">Voucher</span></span> | <span data-ttu-id="62d7c-135">التاريخ</span><span class="sxs-lookup"><span data-stu-id="62d7c-135">Date</span></span>       | <span data-ttu-id="62d7c-136">المرجع</span><span class="sxs-lookup"><span data-stu-id="62d7c-136">Reference</span></span>      | <span data-ttu-id="62d7c-137">العدد</span><span class="sxs-lookup"><span data-stu-id="62d7c-137">Number</span></span> | <span data-ttu-id="62d7c-138">كود الشحنة</span><span class="sxs-lookup"><span data-stu-id="62d7c-138">Lot ID</span></span>  | <span data-ttu-id="62d7c-139">الكمية</span><span class="sxs-lookup"><span data-stu-id="62d7c-139">Quantity</span></span> | <span data-ttu-id="62d7c-140">المبلغ</span><span class="sxs-lookup"><span data-stu-id="62d7c-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="62d7c-141">00001</span><span class="sxs-lookup"><span data-stu-id="62d7c-141">00001</span></span>   | <span data-ttu-id="62d7c-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="62d7c-142">01-01-2015</span></span> | <span data-ttu-id="62d7c-143">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="62d7c-143">Purchase order</span></span> | <span data-ttu-id="62d7c-144">100001</span><span class="sxs-lookup"><span data-stu-id="62d7c-144">100001</span></span> | <span data-ttu-id="62d7c-145">0000101</span><span class="sxs-lookup"><span data-stu-id="62d7c-145">0000101</span></span> | <span data-ttu-id="62d7c-146">100.00</span><span class="sxs-lookup"><span data-stu-id="62d7c-146">100.00</span></span>   | <span data-ttu-id="62d7c-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="62d7c-147">1000.00</span></span> |
| <span data-ttu-id="62d7c-148">00002</span><span class="sxs-lookup"><span data-stu-id="62d7c-148">00002</span></span>   | <span data-ttu-id="62d7c-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="62d7c-149">20-01-2015</span></span> | <span data-ttu-id="62d7c-150">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="62d7c-150">Purchase order</span></span> | <span data-ttu-id="62d7c-151">100001</span><span class="sxs-lookup"><span data-stu-id="62d7c-151">100001</span></span> | <span data-ttu-id="62d7c-152">0000101</span><span class="sxs-lookup"><span data-stu-id="62d7c-152">0000101</span></span> |          | <span data-ttu-id="62d7c-153">100.00</span><span class="sxs-lookup"><span data-stu-id="62d7c-153">100.00</span></span>  |
| <span data-ttu-id="62d7c-154">00003</span><span class="sxs-lookup"><span data-stu-id="62d7c-154">00003</span></span>   | <span data-ttu-id="62d7c-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="62d7c-155">31-01-2015</span></span> | <span data-ttu-id="62d7c-156">التسوية</span><span class="sxs-lookup"><span data-stu-id="62d7c-156">Adjustment</span></span>     | <span data-ttu-id="62d7c-157">100001</span><span class="sxs-lookup"><span data-stu-id="62d7c-157">100001</span></span> | <span data-ttu-id="62d7c-158">0000101</span><span class="sxs-lookup"><span data-stu-id="62d7c-158">0000101</span></span> |          | <span data-ttu-id="62d7c-159">15.00</span><span class="sxs-lookup"><span data-stu-id="62d7c-159">15.00</span></span>   |

<span data-ttu-id="62d7c-160">تتيح صفحة **إدخالات التكلفة** التصفية حسب معرف المستند وتاريخ المستند.</span><span class="sxs-lookup"><span data-stu-id="62d7c-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="62d7c-161">تتوفر إدخالات التكلفة فقط [لكائنات التكلفة](cost-object.md) أو المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="62d7c-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="62d7c-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="62d7c-162">Additional resources</span></span>
--------

[<span data-ttu-id="62d7c-163">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="62d7c-163">Cost objects</span></span>](cost-object.md)




