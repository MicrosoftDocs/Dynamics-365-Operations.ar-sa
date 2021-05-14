---
title: أوامر إدخال مخزن العزل
description: يوضح هذا الموضوع كيفية استخدام أوامر إدخال مخزن الفحص لحظر المخزون.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956172"
---
# <a name="quarantine-orders"></a><span data-ttu-id="33a99-103">أوامر إدخال مخزن العزل</span><span class="sxs-lookup"><span data-stu-id="33a99-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33a99-104">يوضح هذا الموضوع كيفية استخدام أوامر إدخال مخزن الفحص لحظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="33a99-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="33a99-105">تتيح لك أوامر إدخال مخزن الفحص حظر المخزون.</span><span class="sxs-lookup"><span data-stu-id="33a99-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="33a99-106">‏‫على سبيل المثال، قد تحتاج إلى فحص الأصناف لأسباب تتعلق بالجودة.</span><span class="sxs-lookup"><span data-stu-id="33a99-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="33a99-107">يتم تحويل المخزون الذي تم عزله إلى مستودع فحص.</span><span class="sxs-lookup"><span data-stu-id="33a99-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="33a99-108">إذا كنت تستخدم عمليات إدارة المستودعات المتقدمة (في إدارة المستودعات)، فإن معالجة أوامر إدخال مخزن الفحص تُستخدم فقط لأوامر المبيعات المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="33a99-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="33a99-109">أصناف المخزون المتوفرة في مخزن الفحص</span><span class="sxs-lookup"><span data-stu-id="33a99-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="33a99-110">عندما تقوم بعزل العناصر، يمكنك إما إنشاء أوامر العزل يدويًا أو إعداد النظام لإنشائها تلقائيًا أثناء المعالجة الواردة.</span><span class="sxs-lookup"><span data-stu-id="33a99-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="33a99-111">لاعداد النظام لإنشاء أوامر إدخال مخزن الفحص تلقائيا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33a99-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="33a99-112">انتقل إلى **إدارة المخزون \> الإعداد \> المخزون \> مجموعات نماذج العناصر**.</span><span class="sxs-lookup"><span data-stu-id="33a99-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="33a99-113">حدد مجموعة نماذج ذات صلة في جزء القائمة، أو قم بإنشاء مجموعة نماذج جديدة.</span><span class="sxs-lookup"><span data-stu-id="33a99-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="33a99-114">في علامة التبويب السريعة **نهج المخزون**، حدد خانه الاختيار **إدارة العزل**.</span><span class="sxs-lookup"><span data-stu-id="33a99-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="33a99-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="33a99-115">Close the page.</span></span>
1. <span data-ttu-id="33a99-116">في حقل **مستودع العزل** بالنسبة لمستودعات الاستلام، حدد مستودع العزل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="33a99-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="33a99-117">عندما ينتمي عنصر مسجل على أنه تم استلامه في المستودع إلى مجموعة نماذج حيث تم تحديد خانة الاختيار **إدارة العزل**، يقوم النظام بإنشاء أمر عزل له.</span><span class="sxs-lookup"><span data-stu-id="33a99-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="33a99-118">يرشد أمر العزل العاملين لنقل الصنف إلى مستودع العزل.</span><span class="sxs-lookup"><span data-stu-id="33a99-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="33a99-119">عندما تقوم يدويًا بإنشاء أوامر عزل في صفحة **أوامر العزل**، لا يلزم إعداد العنصر لإدارة العزل في مجموعة نماذج الصنف المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="33a99-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="33a99-120">فيما يتعلق بهذه العملية، يجب تحديد المخزون الفعلي الذي يجب فحصه ومستودع الفحص الذي يجب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="33a99-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="33a99-121">يمكنك استخدام أوامر إدخال مخزن الفحص للمساعدة في التخطيط للعملية.</span><span class="sxs-lookup"><span data-stu-id="33a99-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="33a99-122">حالات أوامر الفحص</span><span class="sxs-lookup"><span data-stu-id="33a99-122">Quarantine order statuses</span></span>

<span data-ttu-id="33a99-123">يمكن أن تكون حالات أوامر إدخال مخزن الفحص كالتالي:</span><span class="sxs-lookup"><span data-stu-id="33a99-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="33a99-124">تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="33a99-124">Created</span></span>
- <span data-ttu-id="33a99-125">مبدوء</span><span class="sxs-lookup"><span data-stu-id="33a99-125">Started</span></span>
- <span data-ttu-id="33a99-126">تم الإبلاغ عنه كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="33a99-126">Reported as finished</span></span>
- <span data-ttu-id="33a99-127">منتهٍ</span><span class="sxs-lookup"><span data-stu-id="33a99-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="33a99-128">تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="33a99-128">Created</span></span>

<span data-ttu-id="33a99-129">عند إنشاء أمر إدخال مخزن الفحص يدويًا، ولكن الصنف لم يوضع بعد في مستودع الفحص، يكون أمر إدخال مخزن الفحص بحالة **تم إنشاؤه**.</span><span class="sxs-lookup"><span data-stu-id="33a99-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="33a99-130">ويتم إنشاء حركتي مخزون.</span><span class="sxs-lookup"><span data-stu-id="33a99-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="33a99-131">تكون إحداهما حركة إصدار يمكن أن تكون بحالة **تحت الطلب‬** أو **الفعلي المحجوز‬** أو **منتقاة**.</span><span class="sxs-lookup"><span data-stu-id="33a99-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="33a99-132">أما الثانية فهي حركة استلام يمكن أن تكون بحالة **تحت الطلب** أو **مسجلة** في مستودع الفحص.</span><span class="sxs-lookup"><span data-stu-id="33a99-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="33a99-133">يمكنك حجز تحديثات المخزون وانتقاؤها وتسجيلها باستخدام العمليات المعتادة.</span><span class="sxs-lookup"><span data-stu-id="33a99-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="33a99-134">مبدوء</span><span class="sxs-lookup"><span data-stu-id="33a99-134">Started</span></span>

<span data-ttu-id="33a99-135">عندما يكون أمر إدخال مخزن الفحص بحالة **مبدوء**، يتم نقل المخزون من المستودع المعتاد إلى مستودع الفحص، ويتم إنشاء حركتي مخزون.</span><span class="sxs-lookup"><span data-stu-id="33a99-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="33a99-136">وتكون حركة واحدة بحالة **مخصومة**، والحركة أخرى بحالة **مستلمة**.</span><span class="sxs-lookup"><span data-stu-id="33a99-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="33a99-137">في نفس الوقت، يتم إنشاء حركتي مخزون لمعالجة نقل العائد.</span><span class="sxs-lookup"><span data-stu-id="33a99-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="33a99-138">ولا تكون هذه الحركات مؤرخة.</span><span class="sxs-lookup"><span data-stu-id="33a99-138">These transactions aren't dated.</span></span> <span data-ttu-id="33a99-139">وتكون حركة واحدة بحالة **محجوزة فعليًا**، والحركة أخرى بحالة **مطلوبة**.</span><span class="sxs-lookup"><span data-stu-id="33a99-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="33a99-140">تم الإبلاغ عنه كمنته</span><span class="sxs-lookup"><span data-stu-id="33a99-140">Reported as finished</span></span>

<span data-ttu-id="33a99-141">للإبلاغ عن أمر إدخال مخزن الفحص الذي تم بدؤه كمنتهي، قم بفتح الأمر، وحدد **الإعلام كمنته** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="33a99-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="33a99-142">يتم إصدار الصنف من الفحص، ولكن لم يتم بعد إرجاعه إلى المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="33a99-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="33a99-143">يمكن معالجة إعادة الصنف إلى المستودع العادي عبر دفتر يومية وصول الصنف‬ الذي يمكن تهيئته أثناء إنشاء التقرير كعملية منتهية.</span><span class="sxs-lookup"><span data-stu-id="33a99-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="33a99-144">تم الإنهاء</span><span class="sxs-lookup"><span data-stu-id="33a99-144">Ended</span></span>

<span data-ttu-id="33a99-145">عند إنهاء أمر إدخال مخزن الفحص، يتم نقل الصنف من مستودع الفحص مرة أخرى إلى المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="33a99-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="33a99-146">ويتم تعيين حالة حركة الصنف إلى *مباع* في مستودع الفحص و *مشترى* في المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="33a99-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="33a99-147">خردة أمر الفحص</span><span class="sxs-lookup"><span data-stu-id="33a99-147">Quarantine order scrap</span></span>

<span data-ttu-id="33a99-148">كجزء من عملية أمر إدخال مخزن الفحص، من الممكن تخريد المخزون.</span><span class="sxs-lookup"><span data-stu-id="33a99-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="33a99-149">وعند معالجة الخردة، يتم تعيين حالة المخزون إلى *تم البيع* بحركة إصدار من مستودع العزل.</span><span class="sxs-lookup"><span data-stu-id="33a99-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33a99-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="33a99-150">Additional resources</span></span>

- [<span data-ttu-id="33a99-151">حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="33a99-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
