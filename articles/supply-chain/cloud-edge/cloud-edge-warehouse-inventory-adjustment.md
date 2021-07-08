---
title: تسوية مخزون المستودع
description: يوفر هذا الموضوع معلومات حول دفتر يومية تسوية مخزون المستودع ومعالجته عند استخدام وحدات القياس.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271222"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="53214-103">تسوية مخزون المستودع</span><span class="sxs-lookup"><span data-stu-id="53214-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53214-104">تُستخدم ميزة تسوية مخزون المستودع عند تشغيل وحدات النطاق السحابية والحافة لـ [أحمال عمل التصنيع](cloud-edge-workload-manufacturing.md) و[أحمال عمل إدارة المستودع](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="53214-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="53214-105">عندما يقوم عامل بإجراء تسوية مخزون باستخدام تطبيق المستودع مقابل حمل عمل إدارة المستودعات بوحدة القياس، يجب معالجة التحديث الفعلي المتاح بواسطة الوظيفة الدفعية **دفتر يومية تسوية مخزون المستودعات**، التي تقوم بإدارتها وجدولتها بالانتقال إلى **إدارة المستودعات > المهام الدورية > دفتر يومية تسوية مخزون المستودع**.</span><span class="sxs-lookup"><span data-stu-id="53214-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="53214-106">تستخدم عمليات عمل تطبيق المستودع التالية حاليًا **دفتر يومية تسوية مخزون المستودع** على أحمال عمل وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="53214-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="53214-107">تسوية واردة/صادرة</span><span class="sxs-lookup"><span data-stu-id="53214-107">Adjustment in/out</span></span>
- <span data-ttu-id="53214-108">الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="53214-108">Cycle counting</span></span>
- <span data-ttu-id="53214-109">تحميل لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="53214-109">License plate loading</span></span>

<span data-ttu-id="53214-110">يتم إنشاء العديد من حركات المخزون كجزء من كل تعديل المخزون لأن عمليات نشر الموزع ووحدة القياس تشترك في سجلات المخزون.</span><span class="sxs-lookup"><span data-stu-id="53214-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="53214-111">مثال تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="53214-111">Inventory adjustment example</span></span>

<span data-ttu-id="53214-112">في هذا المثال، استخدم عامل المستودع تطبيق المستودع لتسجيل إضافة المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="53214-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="53214-113">أولاً، يُنشئ حمل عمل وحدة القياس حركة تسوية مخزون المستودع من أجل التسوية المادية الإيجابية، والذي تتم مزامنته بعد ذلك مع المركز وينتج عن ذلك زيادة في المخزون الفعلي في المركز.</span><span class="sxs-lookup"><span data-stu-id="53214-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="53214-114">النوع</span><span class="sxs-lookup"><span data-stu-id="53214-114">Type</span></span>                                    | <span data-ttu-id="53214-115">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="53214-115">Scale unit</span></span> | <span data-ttu-id="53214-116">الاتجاه</span><span class="sxs-lookup"><span data-stu-id="53214-116">Direction</span></span> | <span data-ttu-id="53214-117">المركز</span><span class="sxs-lookup"><span data-stu-id="53214-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="53214-118">تسوية مخزون المستودع</span><span class="sxs-lookup"><span data-stu-id="53214-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="53214-119">+1</span><span class="sxs-lookup"><span data-stu-id="53214-119">+1</span></span>         | ->        | <span data-ttu-id="53214-120">+1</span><span class="sxs-lookup"><span data-stu-id="53214-120">+1</span></span>  |

<span data-ttu-id="53214-121">يقوم المركز بعد ذلك بمعالجة ترحيل دفتر يومية الجرد، والذي يتم استلامه من خلال[رسائل معالج الرسائل](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="53214-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="53214-122">يقوم هذا بتحديث المخزون الإضافي المتاح.</span><span class="sxs-lookup"><span data-stu-id="53214-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="53214-123">لمنع ازدواج المخزون في متناول اليد، ينشئ الموزع حركة إزاحة كجزء من هذه العملية ويزيل المخزون الفعلي المسجل مسبقًا والمرتبط بتسوية مخزون المستودع.</span><span class="sxs-lookup"><span data-stu-id="53214-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="53214-124">النوع</span><span class="sxs-lookup"><span data-stu-id="53214-124">Type</span></span>                                    | <span data-ttu-id="53214-125">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="53214-125">Scale unit</span></span> | <span data-ttu-id="53214-126">الاتجاه</span><span class="sxs-lookup"><span data-stu-id="53214-126">Direction</span></span> | <span data-ttu-id="53214-127">المركز</span><span class="sxs-lookup"><span data-stu-id="53214-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="53214-128">الجرد</span><span class="sxs-lookup"><span data-stu-id="53214-128">Counting</span></span>                                | <span data-ttu-id="53214-129">+1</span><span class="sxs-lookup"><span data-stu-id="53214-129">+1</span></span>         | <-        | <span data-ttu-id="53214-130">+1</span><span class="sxs-lookup"><span data-stu-id="53214-130">+1</span></span>  |
| <span data-ttu-id="53214-131">تسوية مخزون المستودع (الإزاحة)</span><span class="sxs-lookup"><span data-stu-id="53214-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="53214-132">1-</span><span class="sxs-lookup"><span data-stu-id="53214-132">-1</span></span>         | <-        | <span data-ttu-id="53214-133">1-</span><span class="sxs-lookup"><span data-stu-id="53214-133">-1</span></span>  |

<span data-ttu-id="53214-134">بعد أن قامت وحدة القياس بإنشاء **دفتر يومية تسوية مخزون المستودع** في المركز، يمكنك مراجعة كلٍّ من **دفتر يومية الجرد** و **دفتر يومية الإزاحة**، اللذين تم إنشاؤهما بواسطة المركز كجزء من عملية التسوية.</span><span class="sxs-lookup"><span data-stu-id="53214-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="53214-135">يمكنك مراجعة كل من إدخالات دفتر اليومية هذه والحركة في Supply Chain Management عن طريق القيام بالخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="53214-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="53214-136">قم بتسجيل الدخول إلى وحده القياس.</span><span class="sxs-lookup"><span data-stu-id="53214-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="53214-137">انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> دفتر يومية تسوية مخزون المستودع**.</span><span class="sxs-lookup"><span data-stu-id="53214-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="53214-138">في صفحة **دفتر يومية تسوية مخزون المستودع**، ابحث عن دفتر اليومية الذي تم تسجيله في تغيير المخزون الفعلي وقم بفتحه.</span><span class="sxs-lookup"><span data-stu-id="53214-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="53214-139">يعرض قسم **بنود دفتر اليومية** كل تسوية تم تسجيلها بواسطة دفتر اليومية هذا.</span><span class="sxs-lookup"><span data-stu-id="53214-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="53214-140">قم بتسجيل الدخول إلى المركز.</span><span class="sxs-lookup"><span data-stu-id="53214-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="53214-141">انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> دفتر يومية تسوية مخزون المستودع**.</span><span class="sxs-lookup"><span data-stu-id="53214-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="53214-142">في صفحة **دفتر يومية تسوية مخزون المستودع**، يجب أن ترى نفس دفتر اليومية المدرج في حالة مزامنة المركز ووحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="53214-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="53214-143">افتح دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="53214-143">Open the journal.</span></span> <span data-ttu-id="53214-144">في حالة معالجة [رسائل معالج الرسائل](cloud-edge-message-processor-messages.md)، ستشاهد ارتباطات إلى **دفتر يومية الجرد** و **دفتر يومية الإزاحة** في الرأس.</span><span class="sxs-lookup"><span data-stu-id="53214-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="53214-145">يجب أن يعرض **دفتر يومية الجرد** نفس قيم الأبعاد مثل بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="53214-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="53214-146">يجب أن يعرض **دفتر يومية الإزاحة** الإزاحة، التي تزيل تسوية الجرد المزدوج.</span><span class="sxs-lookup"><span data-stu-id="53214-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="53214-147">عند اكتمال جميع عمليات المزامنة والمعالجة، فإنه تتم مزامنة **دفتر يومية الجرد** و **دفتر يومية الإزاحة** مع وحدة القياس مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="53214-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="53214-148">يمكن عرضها أيضًا من صفحة **دفتر يومية تسوية مخزون المستودع**.</span><span class="sxs-lookup"><span data-stu-id="53214-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
