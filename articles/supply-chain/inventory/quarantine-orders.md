---
title: "أوامر إدخال مخزن الفحص"
description: "توضح هذه المقالة كيفية استخدام أوامر إدخال مخزن الفحص لحظر المخزون."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="quarantine-orders"></a><span data-ttu-id="bb9d5-103">أوامر إدخال مخزن الفحص</span><span class="sxs-lookup"><span data-stu-id="bb9d5-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bb9d5-104">توضح هذه المقالة كيفية استخدام أوامر إدخال مخزن الفحص لحظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-104">This article describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="bb9d5-105">يمكن استخدام أوامر إدخال مخزن الفحص لحظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="bb9d5-106">‏‫على سبيل المثال، قد تحتاج إلى فحص الأصناف لأسباب تتعلق بالجودة.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="bb9d5-107">يتم تحويل المخزون الذي تم عزله إلى مستودع فحص.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="bb9d5-108">**ملاحظة:** إذا كنت تستخدم عمليات إدارة المستودعات المتقدمة (في إدارة المستودعات)، فإن معالجة أوامر إدخال مخزن الفحص تُستخدم فقط لأوامر المبيعات المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-onhand-inventory-items"></a><span data-ttu-id="bb9d5-109">أصناف المخزون المتوفرة في مخزن الفحص</span><span class="sxs-lookup"><span data-stu-id="bb9d5-109">Quarantine onhand inventory items</span></span>
<span data-ttu-id="bb9d5-110">عند قيامك بإدخال الأصناف في مخزن الفحص، يمكنك إنشاء أوامر إدخال مخزن الفحص يدويًا أو إعداد النظام لإنشاء هذه الأوامر تلقائيًا أثناء المعالجة الداخلية.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="bb9d5-111">لإنشاء أوامر إدخال مخزن الفحص تلقائيًا، حدد الخيار **إدارة الفحص** على علامة التبويب **سياسات المخزون‬** في صفحة **مجموعات نموذج الصنف**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="bb9d5-112">يجب أيضًا تحديد مستودع فحص افتراضي في حقل **مخزون الفحص** للمستودعات التي تتلقى الأصناف.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="bb9d5-113">عند تسجيل المخزون الفعلي في أمر شراء أو أمر إنتاج، يتم نقل العناصر التي تم عزلها إلى مخزون الفحص بشكل تلقائي في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="bb9d5-114">تحدث هذه الحركة لأن أمر إدخال مخزن الفحص تغيّر إلى **مبدوء‬**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="bb9d5-115">عندما تنشئ أوامر إدخال مخزن الفحص يدويًا، لا حاجة إلى إعداد الصنف لإدارة الفحص في مجموعة نماذج الأصناف المقترنة.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="bb9d5-116">فيما يتعلق بهذه العملية، يجب تحديد المخزون الفعلي الذي يجب فحصه ومستودع الفحص الذي يجب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="bb9d5-117">يمكنك استخدام أوامر إدخال مخزن الفحص للمساعدة في التخطيط للعملية.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="bb9d5-118">حالات أوامر الفحص</span><span class="sxs-lookup"><span data-stu-id="bb9d5-118">Quarantine order statuses</span></span>
<span data-ttu-id="bb9d5-119">يمكن أن تكون حالات أوامر إدخال مخزن الفحص كالتالي:</span><span class="sxs-lookup"><span data-stu-id="bb9d5-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="bb9d5-120">تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="bb9d5-120">Created</span></span>
-   <span data-ttu-id="bb9d5-121">مبدوء</span><span class="sxs-lookup"><span data-stu-id="bb9d5-121">Started</span></span>
-   <span data-ttu-id="bb9d5-122">تم الإبلاغ عنه كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="bb9d5-122">Reported as finished</span></span>
-   <span data-ttu-id="bb9d5-123">منتهٍ</span><span class="sxs-lookup"><span data-stu-id="bb9d5-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="bb9d5-124">تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="bb9d5-124">Created</span></span>

<span data-ttu-id="bb9d5-125">عند إنشاء أمر إدخال مخزن الفحص يدويًا، ولكن الصنف لم يوضع بعد في مستودع الفحص، يكون أمر إدخال مخزن الفحص بحالة **تم إنشاؤه**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="bb9d5-126">ويتم إنشاء حركتي مخزون.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="bb9d5-127">تكون إحداهما حركة إصدار يمكن أن تكون بحالة **تحت الطلب‬** أو **الفعلي المحجوز‬** أو**منتقاة**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="bb9d5-128">أما الثانية فهي حركة استلام يمكن أن تكون بحالة **تحت الطلب** أو**مسجلة** في مستودع الفحص.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="bb9d5-129">يمكنك حجز تحديثات المخزون وانتقاؤها وتسجيلها باستخدام العمليات المعتادة.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="bb9d5-130">مبدوء</span><span class="sxs-lookup"><span data-stu-id="bb9d5-130">Started</span></span>

<span data-ttu-id="bb9d5-131">عندما يكون أمر إدخال مخزن الفحص بحالة **مبدوء**، يتم نقل المخزون من المستودع المعتاد إلى مستودع الفحص، ويتم إنشاء حركتي مخزون.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="bb9d5-132">وتكون حركة واحدة بحالة **مخصومة**، والحركة أخرى بحالة **مستلمة**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="bb9d5-133">في نفس الوقت، يتم إنشاء حركتي مخزون لمعالجة نقل العائد.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="bb9d5-134">ولا تكون هذه الحركات مؤرخة.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-134">These transactions aren't dated.</span></span> <span data-ttu-id="bb9d5-135">وتكون حركة واحدة بحالة **محجوزة فعليًا**، والحركة أخرى بحالة **مطلوبة**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="bb9d5-136">تم الإبلاغ عنه كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="bb9d5-136">Reported as finished</span></span>

<span data-ttu-id="bb9d5-137">وبالنقر فوق **الإبلاغ عنه كمنتهٍ**، يمكنك الإبلاغ عن أمر إدخال مخزن الفحص الذي تم البدء فيه كمنتهٍ.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="bb9d5-138">يتم إصدار الصنف من الفحص، ولكن لم يتم بعد إرجاعه إلى المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="bb9d5-139">يمكن معالجة إعادة الصنف إلى المستودع العادي عبر دفتر يومية وصول الصنف‬ الذي يمكن تهيئته أثناء إنشاء التقرير كعملية منتهية.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-139">The movement back to the regular warehouse can be procesed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="bb9d5-140">منتهٍ</span><span class="sxs-lookup"><span data-stu-id="bb9d5-140">Ended</span></span>

<span data-ttu-id="bb9d5-141">عند إنهاء أمر إدخال مخزن الفحص، يتم نقل الصنف من مستودع الفحص مرة أخرى إلى المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="bb9d5-142">ويتم تعيين حالة حركة الصنف إلى **مباع** في مستودع الفحص و**مشترى** في المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="bb9d5-143">خردة أمر الفحص</span><span class="sxs-lookup"><span data-stu-id="bb9d5-143">Quarantine order scrap</span></span>
<span data-ttu-id="bb9d5-144">كجزء من عملية أمر إدخال مخزن الفحص، من الممكن تخريد المخزون.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="bb9d5-145">وعند معالجة الخردة، سيتم تعيين حالة المخزون إلى **تم البيع** بحركة إصدار من مستودع الفحص.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="bb9d5-146">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="bb9d5-146">See also</span></span>
--------

[<span data-ttu-id="bb9d5-147">حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="bb9d5-147">Inventory blocking</span></span>](inventory-blocking.md)

