---
title: التحديثات المادية والمالية
description: يقدم هذا الموضوع نظرة عامة على أنواع الحركات التي تؤدي إلى زيادة كميات المخزون أو تقليلها.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea79bd9c6561c4e4f6fad2c177f44fe62bdea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421554"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="4c793-103">التحديثات المادية والمالية</span><span class="sxs-lookup"><span data-stu-id="4c793-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c793-104">يقدم هذا الموضوع نظرة عامة على أنواع الحركات التي تؤدي إلى زيادة كميات المخزون أو تقليلها.</span><span class="sxs-lookup"><span data-stu-id="4c793-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="4c793-105">يمكن تحديث حركات المخزون فعليًا وتحديثها ماليًا في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4c793-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4c793-106">وتزيد بعض أنواع الحركات الفعلية والمالية من كميات المخزون، بينما البعض الآخر يعمل على تقليل الكمية.</span><span class="sxs-lookup"><span data-stu-id="4c793-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="4c793-107">الزيادات الفعلية</span><span class="sxs-lookup"><span data-stu-id="4c793-107">Physical increases</span></span>
<span data-ttu-id="4c793-108">عند ترحيل حركة فعلية، تصبح حالة سجل الحركة **مستلم**.</span><span class="sxs-lookup"><span data-stu-id="4c793-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="4c793-109">وتعتبر الحركات التالية زيادات فعلية:</span><span class="sxs-lookup"><span data-stu-id="4c793-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="4c793-110">عملية استلام أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="4c793-110">Purchase order receipt</span></span>
-   <span data-ttu-id="4c793-111">إرجاع كشف تعبئة أوامر التوريد</span><span class="sxs-lookup"><span data-stu-id="4c793-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="4c793-112">الإبلاغ عن أمر إنتاج كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="4c793-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="4c793-113">منتج ثانوي في قائمة تعبئة أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="4c793-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="4c793-114">الزيادات المالية</span><span class="sxs-lookup"><span data-stu-id="4c793-114">Financial increases</span></span>
<span data-ttu-id="4c793-115">عند ترحيل حركة استلام مالية، تصبح حالة سجل الحركة التي تزيد الكمية هي **تم الشراء**.</span><span class="sxs-lookup"><span data-stu-id="4c793-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="4c793-116">وتعتبر الحركات التالية زيادات مالية:</span><span class="sxs-lookup"><span data-stu-id="4c793-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="4c793-117">فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="4c793-117">Vendor invoice</span></span>
-   <span data-ttu-id="4c793-118">فاتورة أمر التوريد لإرجاع</span><span class="sxs-lookup"><span data-stu-id="4c793-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="4c793-119">تكاليف أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="4c793-119">Production order costing</span></span>
-   <span data-ttu-id="4c793-120">دفاتر يومية مخزون الكميات ذات القيمة الموجبة، مثل النقل والأرباح والخسائر والجرد وقائمة مكونات الصنف والتحويل</span><span class="sxs-lookup"><span data-stu-id="4c793-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="4c793-121">حركات زيادة الكمية</span><span class="sxs-lookup"><span data-stu-id="4c793-121">Transactions that increase quantity</span></span>
<span data-ttu-id="4c793-122">يتم ترحيل الحركات التي تؤدي إلى زيادة الكمية في تشغيل متوسط سعر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4c793-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="4c793-123">يستند متوسط سعر التكلفة قيد التشغيل المحسوب إلي تكلفة كل حركة من هذه الحركات لكل بعد مخزني يتم تتبعه ماليًا.</span><span class="sxs-lookup"><span data-stu-id="4c793-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="4c793-124">لمزيد من المعلومات حول متوسط أسعار التكاليف الحالية، راجع [متوسط سعر التكلفة الحالي](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="4c793-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="4c793-125">حركات تقليل الكمية</span><span class="sxs-lookup"><span data-stu-id="4c793-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="4c793-126">يُستخدم متوسط سعر التكلفة الحالي المحسوب عند ترحيل حركة تقلل الكمية، بغض النظر عن نموذج المخزون المقترن بهذا المخزون.</span><span class="sxs-lookup"><span data-stu-id="4c793-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="4c793-127">ويجب ألا يتم تمييز حركة تقليل الكمية لحركة أخرى قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="4c793-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="4c793-128">إذا أصبح المخزون الفعلي المتوفر سالبًا، يُستخدم تكلفة المخزون التي يتم تحديدها للصنف في صفحة **الصنف**.</span><span class="sxs-lookup"><span data-stu-id="4c793-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="4c793-129">في حالة تمكين وظيفة المواقع المتعددة، ستصبح هذه التكلفة هي تكلفة المخزون المُعرَّفة لأحد المواقع بدلاً من ذلك في صفحة **إعدادات الأمر الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="4c793-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="4c793-130">الإصدارات الفعلية مقابل الإصدارات المالية</span><span class="sxs-lookup"><span data-stu-id="4c793-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="4c793-131">عند ترحيل حركة إصدار فعلية، تكون حالة سجل الحركة هي **مخصوم**.</span><span class="sxs-lookup"><span data-stu-id="4c793-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="4c793-132">وتعتبر الحركات التالية إصدارات فعلية:</span><span class="sxs-lookup"><span data-stu-id="4c793-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="4c793-133">دفتر يومية قائمة الانتقاء لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="4c793-133">Production order picking list journal</span></span>
-   <span data-ttu-id="4c793-134">كشف تعبئة أمر التوريد</span><span class="sxs-lookup"><span data-stu-id="4c793-134">Sales order packing slip</span></span>
-   <span data-ttu-id="4c793-135">إرجاع كشف تعبئة أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="4c793-135">Purchase order packing slip return</span></span>

<span data-ttu-id="4c793-136">عند ترحيل حركة مالية، تكون حالة سجل الحركة هي **تم البيع**.</span><span class="sxs-lookup"><span data-stu-id="4c793-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="4c793-137">وتعتبر الحركات التالية إصدارات مالية:</span><span class="sxs-lookup"><span data-stu-id="4c793-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="4c793-138">إنهاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="4c793-138">Ending a production order</span></span>
-   <span data-ttu-id="4c793-139">فاتورة أمر التوريد</span><span class="sxs-lookup"><span data-stu-id="4c793-139">Sales order invoice</span></span>
-   <span data-ttu-id="4c793-140">إرجاع فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="4c793-140">Vendor invoice return</span></span>
-   <span data-ttu-id="4c793-141">دفاتر يومية مخزون الكميات ذات القيمة السالبة، مثل النقل والأرباح والخسائر والجرد وقائمة مكونات الصنف والتحويل</span><span class="sxs-lookup"><span data-stu-id="4c793-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="4c793-142">يتم ترحيل الحركات التي تؤدي إلى تقليل الكمية في تشغيل متوسط سعر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4c793-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="4c793-143">ولذلك، يتم من خلال إجراء إغلاق المخزون لتسوية حركات إصدار إلى حركات الإيصال وفقًا لنموذج المخزون الذي تم تعيينه لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="4c793-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>
