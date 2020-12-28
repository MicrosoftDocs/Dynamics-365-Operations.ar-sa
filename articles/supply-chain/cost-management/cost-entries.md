---
title: إدخالات التكلفة
description: توفر هذه المقالة معلومات حول إدخالات التكلفة والحالات التي يتم فيها إنشاء هذه الإدخالات. إدخال التكلفة هو سجل لتسجيل كمية وتكلفة لحدث محدد.
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
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3116f9fd2d1fe6a0967b114a069f495cea6217a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421035"
---
# <a name="cost-entries"></a><span data-ttu-id="4b0c6-104">إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b0c6-105">توفر هذه المقالة معلومات حول إدخالات التكلفة والحالات التي يتم فيها إنشاء هذه الإدخالات.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="4b0c6-106">إدخال التكلفة هو سجل لتسجيل كمية وتكلفة لحدث محدد.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="4b0c6-107">إدخالات التكلفة هي تجميعات حركات المخزون التي تم تسجيلها في أبعاد المخزون المالية النشطة.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="4b0c6-108">أمثلة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="4b0c6-109">مثال 1: لم يتم إنشاء أي إدخالات تكلفة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="4b0c6-110">يتم تسجيل حدث دفتر يومية نقل.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-110">A transfer journal event is registered.</span></span> <span data-ttu-id="4b0c6-111">وينقل الحدث قطعة واحدة من الصنف أ من الموقع أ إلى الموقع ب, ولا يعتبر بُعد مخزون الموقع جزءًا من كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="4b0c6-112">ولذلك، يُنشئ الحدث حركتي مخزون وأي إدخالات تكلفة.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="4b0c6-113">مثال 2: يتم إنشاء إدخالات تكلفة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="4b0c6-114">يتم تسجيل حدث دفتر يومية نقل.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-114">A transfer journal event is registered.</span></span> <span data-ttu-id="4b0c6-115">‏‫وينقل الحدث قطعة واحدة من الصنف أ من الموقع 1 إلى الموقع 2،</span><span class="sxs-lookup"><span data-stu-id="4b0c6-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="4b0c6-116">ولا يعتبر بُعد مخزون الموقع جزءًا من كائن التكلفة.‬</span><span class="sxs-lookup"><span data-stu-id="4b0c6-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="4b0c6-117">ولذلك، يُنشئ الحدث حركتي مخزون وإدخالي تكلفة.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="4b0c6-118">مثال 3: يتم إنشاء إدخال تكلفة واحد</span><span class="sxs-lookup"><span data-stu-id="4b0c6-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="4b0c6-119">يتم تسجيل حدث استلام منتج لأمر شراء.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="4b0c6-120">يسجل الحدث 100 قطعة من الصنف أ بتكلفة الوحدة 10.00 دولار أمريكي (USD).</span><span class="sxs-lookup"><span data-stu-id="4b0c6-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="4b0c6-121">ونظرًا لأن الصنف أ يستخدم رقمًا مسلسلاً لتعقب غرض إدارة المخزون، فإنه يتم إنشاء رقم تسلسلي فريد لكل صنف يتم استلامه.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="4b0c6-122">ولذلك، يُنشئ الحدث 100 حركة مخزون وإدخال تكلفة واحد.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="4b0c6-123">صفحة إدخالات التكلفة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-123">Cost entries page</span></span>
<span data-ttu-id="4b0c6-124">تتيح لك صفحة **إدخالات التكلفة** عرض والتحكم في التسجيلات الخاصة بالتكاليف والكميات.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="4b0c6-125">وتكمل هذه الصفحة صفحتي **حركة المخزون** و **تسوية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="4b0c6-126">ويتم تسجيل السجلات بترتيب زمني لحدث ما.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="4b0c6-127">ولذلك، يمكنك بسرعة العثور على والتحكم في التكاليف المتراكمة لحدث معين أو كافة الأحداث المرتبطة بمستند.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="4b0c6-128">وفيما يلي مثال على ذلك:</span><span class="sxs-lookup"><span data-stu-id="4b0c6-128">Here is an example:</span></span>

-   <span data-ttu-id="4b0c6-129">يتم تسجيل حدث استلام منتج للصنف أ. ويتم استلام مائة قطعة بتكلفة وحدة 10.00 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="4b0c6-130">وبعد تسجيل حدث الفاتورة بأيام قليلة، تزداد التكلفة إلى 11.00 دولاراً أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="4b0c6-131">ولذلك، يبلغ إجمالي المبلغ 1,100 دولارًا أمريكيًا.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="4b0c6-132">ويتم إنشاء إيصال ثاني لحساب الفرق بمبلغ 100 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="4b0c6-133">بعد بضعة أيام، يتم تسجيل مصاريف متنوعة بمبلغ 15.00 دولاراً أمريكيًا لتغطية تكلفة النقل في أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="4b0c6-134">الإيصال</span><span class="sxs-lookup"><span data-stu-id="4b0c6-134">Voucher</span></span> | <span data-ttu-id="4b0c6-135">التاريخ</span><span class="sxs-lookup"><span data-stu-id="4b0c6-135">Date</span></span>       | <span data-ttu-id="4b0c6-136">المرجع</span><span class="sxs-lookup"><span data-stu-id="4b0c6-136">Reference</span></span>      | <span data-ttu-id="4b0c6-137">العدد</span><span class="sxs-lookup"><span data-stu-id="4b0c6-137">Number</span></span> | <span data-ttu-id="4b0c6-138">كود الشحنة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-138">Lot ID</span></span>  | <span data-ttu-id="4b0c6-139">الكمية</span><span class="sxs-lookup"><span data-stu-id="4b0c6-139">Quantity</span></span> | <span data-ttu-id="4b0c6-140">المبلغ</span><span class="sxs-lookup"><span data-stu-id="4b0c6-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="4b0c6-141">00001</span><span class="sxs-lookup"><span data-stu-id="4b0c6-141">00001</span></span>   | <span data-ttu-id="4b0c6-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="4b0c6-142">01-01-2015</span></span> | <span data-ttu-id="4b0c6-143">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="4b0c6-143">Purchase order</span></span> | <span data-ttu-id="4b0c6-144">100001</span><span class="sxs-lookup"><span data-stu-id="4b0c6-144">100001</span></span> | <span data-ttu-id="4b0c6-145">0000101</span><span class="sxs-lookup"><span data-stu-id="4b0c6-145">0000101</span></span> | <span data-ttu-id="4b0c6-146">100.00</span><span class="sxs-lookup"><span data-stu-id="4b0c6-146">100.00</span></span>   | <span data-ttu-id="4b0c6-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="4b0c6-147">1000.00</span></span> |
| <span data-ttu-id="4b0c6-148">00002</span><span class="sxs-lookup"><span data-stu-id="4b0c6-148">00002</span></span>   | <span data-ttu-id="4b0c6-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="4b0c6-149">20-01-2015</span></span> | <span data-ttu-id="4b0c6-150">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="4b0c6-150">Purchase order</span></span> | <span data-ttu-id="4b0c6-151">100001</span><span class="sxs-lookup"><span data-stu-id="4b0c6-151">100001</span></span> | <span data-ttu-id="4b0c6-152">0000101</span><span class="sxs-lookup"><span data-stu-id="4b0c6-152">0000101</span></span> |          | <span data-ttu-id="4b0c6-153">100.00</span><span class="sxs-lookup"><span data-stu-id="4b0c6-153">100.00</span></span>  |
| <span data-ttu-id="4b0c6-154">00003</span><span class="sxs-lookup"><span data-stu-id="4b0c6-154">00003</span></span>   | <span data-ttu-id="4b0c6-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="4b0c6-155">31-01-2015</span></span> | <span data-ttu-id="4b0c6-156">التسوية</span><span class="sxs-lookup"><span data-stu-id="4b0c6-156">Adjustment</span></span>     | <span data-ttu-id="4b0c6-157">100001</span><span class="sxs-lookup"><span data-stu-id="4b0c6-157">100001</span></span> | <span data-ttu-id="4b0c6-158">0000101</span><span class="sxs-lookup"><span data-stu-id="4b0c6-158">0000101</span></span> |          | <span data-ttu-id="4b0c6-159">15.00</span><span class="sxs-lookup"><span data-stu-id="4b0c6-159">15.00</span></span>   |

<span data-ttu-id="4b0c6-160">تتيح صفحة **إدخالات التكلفة** التصفية حسب معرف المستند وتاريخ المستند.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b0c6-161">تتوفر إدخالات التكلفة فقط [لكائنات التكلفة](cost-object.md) أو المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="4b0c6-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4b0c6-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4b0c6-162">Additional resources</span></span>
--------

[<span data-ttu-id="4b0c6-163">كائنات التكلفة</span><span class="sxs-lookup"><span data-stu-id="4b0c6-163">Cost objects</span></span>](cost-object.md)



