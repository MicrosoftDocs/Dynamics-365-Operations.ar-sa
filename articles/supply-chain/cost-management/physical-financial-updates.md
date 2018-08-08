---
title: "التحديثات المادية والمالية"
description: "يقدم هذا الموضوع نظرة عامة على أنواع الحركات التي تؤدي إلى زيادة كميات المخزون أو تقليلها."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9ba628dbf63d3b124583e6b873530f1459b07562
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="16bc1-103">التحديثات المادية والمالية</span><span class="sxs-lookup"><span data-stu-id="16bc1-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16bc1-104">يقدم هذا الموضوع نظرة عامة على أنواع الحركات التي تؤدي إلى زيادة كميات المخزون أو تقليلها.</span><span class="sxs-lookup"><span data-stu-id="16bc1-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="16bc1-105">يمكن تحديث حركات المخزون فعليًا وتحديثها ماليًا في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16bc1-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="16bc1-106">وتزيد بعض أنواع الحركات الفعلية والمالية من كميات المخزون، بينما البعض الآخر يعمل على تقليل الكمية.</span><span class="sxs-lookup"><span data-stu-id="16bc1-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="16bc1-107">الزيادات الفعلية</span><span class="sxs-lookup"><span data-stu-id="16bc1-107">Physical increases</span></span>
<span data-ttu-id="16bc1-108">عند ترحيل حركة فعلية، تصبح حالة سجل الحركة**مستلم**.</span><span class="sxs-lookup"><span data-stu-id="16bc1-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="16bc1-109">وتعتبر الحركات التالية زيادات فعلية:</span><span class="sxs-lookup"><span data-stu-id="16bc1-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="16bc1-110">عملية استلام أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="16bc1-110">Purchase order receipt</span></span>
-   <span data-ttu-id="16bc1-111">إرجاع كشف تعبئة أوامر التوريد</span><span class="sxs-lookup"><span data-stu-id="16bc1-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="16bc1-112">الإبلاغ عن أمر إنتاج كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="16bc1-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="16bc1-113">منتج ثانوي في قائمة تعبئة أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="16bc1-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="16bc1-114">الزيادات المالية</span><span class="sxs-lookup"><span data-stu-id="16bc1-114">Financial increases</span></span>
<span data-ttu-id="16bc1-115">عند ترحيل حركة استلام مالية، تصبح حالة سجل الحركة التي تزيد الكمية هي **تم الشراء**.</span><span class="sxs-lookup"><span data-stu-id="16bc1-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="16bc1-116">وتعتبر الحركات التالية زيادات مالية:</span><span class="sxs-lookup"><span data-stu-id="16bc1-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="16bc1-117">فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="16bc1-117">Vendor invoice</span></span>
-   <span data-ttu-id="16bc1-118">فاتورة أمر التوريد لإرجاع</span><span class="sxs-lookup"><span data-stu-id="16bc1-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="16bc1-119">تكاليف أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="16bc1-119">Production order costing</span></span>
-   <span data-ttu-id="16bc1-120">دفاتر يومية مخزون الكميات ذات القيمة الموجبة، مثل النقل والأرباح والخسائر والجرد وقائمة مكونات الصنف والتحويل</span><span class="sxs-lookup"><span data-stu-id="16bc1-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="16bc1-121">حركات زيادة الكمية</span><span class="sxs-lookup"><span data-stu-id="16bc1-121">Transactions that increase quantity</span></span>
<span data-ttu-id="16bc1-122">يتم ترحيل الحركات التي تؤدي إلى زيادة الكمية في تشغيل متوسط سعر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="16bc1-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="16bc1-123">ويقوم Finance and Operations بحساب متوسط سعر التكلفة قيد التشغيل بناءً على تكلفة كل حركة من هذه الحركات لكل بعد مخزني يتم تتبعه ماليًا.</span><span class="sxs-lookup"><span data-stu-id="16bc1-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="16bc1-124">لمزيد من المعلومات حول متوسط أسعار التكاليف الحالية، راجع [متوسط سعر التكلفة الحالي](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="16bc1-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="16bc1-125">حركات تقليل الكمية</span><span class="sxs-lookup"><span data-stu-id="16bc1-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="16bc1-126">يستخدم Finance and Operations متوسط سعر التكلفة الحالي المحسوب عند ترحيل حركة تقلل الكمية، بغض النظر عن نموذج المخزون المقترن بهذا المخزون.</span><span class="sxs-lookup"><span data-stu-id="16bc1-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="16bc1-127">ويجب ألا يتم تمييز حركة تقليل الكمية لحركة أخرى قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="16bc1-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="16bc1-128">إذا أصبح المخزون الفعلي المتوفر سالبًا، يستخدم Finance and Operations تكلفة المخزون التي يتم تحديدها للصنف في صفحة **الصنف**.</span><span class="sxs-lookup"><span data-stu-id="16bc1-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="16bc1-129">**ملاحظة:** في حالة تمكين وظيفة المواقع المتعددة، ستصبح هذه التكلفة هي تكلفة المخزون المُعرَّفة لأحد المواقع بدلاً من ذلك في صفحة **إعدادات الأمر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="16bc1-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="16bc1-130">الإصدارات الفعلية مقابل الإصدارات المالية</span><span class="sxs-lookup"><span data-stu-id="16bc1-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="16bc1-131">عند ترحيل حركة إصدار فعلية، تكون حالة سجل الحركة هي **مخصوم**.</span><span class="sxs-lookup"><span data-stu-id="16bc1-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="16bc1-132">وتعتبر الحركات التالية إصدارات فعلية:</span><span class="sxs-lookup"><span data-stu-id="16bc1-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="16bc1-133">دفتر يومية قائمة الانتقاء لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="16bc1-133">Production order picking list journal</span></span>
-   <span data-ttu-id="16bc1-134">كشف تعبئة أمر التوريد</span><span class="sxs-lookup"><span data-stu-id="16bc1-134">Sales order packing slip</span></span>
-   <span data-ttu-id="16bc1-135">إرجاع كشف تعبئة أوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="16bc1-135">Purchase order packing slip return</span></span>

<span data-ttu-id="16bc1-136">عند ترحيل حركة مالية، تكون حالة سجل الحركة هي **تم البيع**.</span><span class="sxs-lookup"><span data-stu-id="16bc1-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="16bc1-137">وتعتبر الحركات التالية إصدارات مالية:</span><span class="sxs-lookup"><span data-stu-id="16bc1-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="16bc1-138">إنهاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="16bc1-138">Ending a production order</span></span>
-   <span data-ttu-id="16bc1-139">فاتورة أمر التوريد</span><span class="sxs-lookup"><span data-stu-id="16bc1-139">Sales order invoice</span></span>
-   <span data-ttu-id="16bc1-140">إرجاع فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="16bc1-140">Vendor invoice return</span></span>
-   <span data-ttu-id="16bc1-141">دفاتر يومية مخزون الكميات ذات القيمة السالبة، مثل النقل والأرباح والخسائر والجرد وقائمة مكونات الصنف والتحويل</span><span class="sxs-lookup"><span data-stu-id="16bc1-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="16bc1-142">يتم ترحيل الحركات التي تؤدي إلى تقليل الكمية في تشغيل متوسط سعر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="16bc1-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="16bc1-143">ولذلك، يتم من خلال إجراء إغلاق المخزون لتسوية حركات إصدار إلى حركات الإيصال وفقًا لنموذج المخزون الذي تم تعيينه لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="16bc1-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




