---
title: "نقل المخزون مع العمل المقترن في إدارة المستودعات"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق تأكيد انتقاء الأجزاء من جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 463e438418c4bc1b38fd1bde8251d1383cb44a13
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="14f28-103">نقل المخزون مع العمل المقترن في إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="14f28-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="14f28-104">باستخدام نقل المخزون، يمكنك أن تحدد العاملين في المستودع الذين يتم السماح لهم بنقل المخزون المحجوز.</span><span class="sxs-lookup"><span data-stu-id="14f28-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="14f28-105">من شأن ذلك أن يوفر مرونة في المستودعات المنظمة حيث يمكنك تحديد عدم السماح لعامل باختيار موقع انتقاء جديد لعمل الانتقاء الذي أنشأه.</span><span class="sxs-lookup"><span data-stu-id="14f28-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="14f28-106">ويسمح أيضًا لمدير المستودع بمراقبة القدرات التي ينبغي أن تكون لدى بعض العاملين ذوي خبرات أقل.</span><span class="sxs-lookup"><span data-stu-id="14f28-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="14f28-107">قد تكون المرونة في إدارة العمليات اليومية للعاملين في المستودعات مفيدة في سيناريوهات كتلك التي تلي:</span><span class="sxs-lookup"><span data-stu-id="14f28-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="14f28-108">السيناريو 1</span><span class="sxs-lookup"><span data-stu-id="14f28-108">Scenario 1</span></span>
<span data-ttu-id="14f28-109">شركة لديها مساحة استلام صغيرة نسبيًا، وهي مزدحمة بالبالتات والصناديق المخزنة فيها.</span><span class="sxs-lookup"><span data-stu-id="14f28-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="14f28-110">من المتوقع وصول شحنة كبيرة في اليوم الحالي، لذلك يقرر موظف الاستلام‬ تحرير منطقة الاستلام عن طريق نقل بعض البالتات‬ إلى منطقة إعداد داخلية ثانوية.</span><span class="sxs-lookup"><span data-stu-id="14f28-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="14f28-111">السيناريو 2</span><span class="sxs-lookup"><span data-stu-id="14f28-111">Scenario 2</span></span>
<span data-ttu-id="14f28-112">يلاحظ عامل مستودع من ذوي الخبرة فرصة في مستودع ما لتجميع العناصر في مكان واحد بدلاً من تقسيمها عبر 3 مواقع مجاورة يحتوي كل واحد منها على كمية صغيرة.</span><span class="sxs-lookup"><span data-stu-id="14f28-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="14f28-113">يريد العامل تجميع الكمية عن طريق نقل العناصر من كل واحد من هذه المواقع إلى الموقع نفسه وإلى لوحة الترخيص نفسها.</span><span class="sxs-lookup"><span data-stu-id="14f28-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="14f28-114">السيناريو 3</span><span class="sxs-lookup"><span data-stu-id="14f28-114">Scenario 3</span></span>
<span data-ttu-id="14f28-115">هناك بالتة تنتظر الشحن في موقع إعداد، مثل STAGE01، القريب من BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="14f28-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="14f28-116">ومع ذلك، ونظرًا لتغيير الخطط تم جدولة وصول الشاحنة إلى BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="14f28-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="14f28-117">موظف الشحن يدرك ذلك ويريد التأكد من أن الشاحنة لن تنتظر تحميلها من STAGE01.</span><span class="sxs-lookup"><span data-stu-id="14f28-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="14f28-118">يقرر موظف الشحن نقل الأصناف في هذه الشحنة من STAGE01 إلى STAGE04، الأقرب إلى الوجهة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="14f28-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="14f28-119">القيود الحالية</span><span class="sxs-lookup"><span data-stu-id="14f28-119">Current limitations</span></span>

<span data-ttu-id="14f28-120">تقتصر عمليات حجز العمل التي يمكنك نقلها على أمر المبيعات وإصدار أمر التحويل واستلام أمر التحويل وأمر الشراء وعمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="14f28-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="14f28-121">يتم تقييد نقل الأصناف لمنع تقسيم بنود العمل.</span><span class="sxs-lookup"><span data-stu-id="14f28-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="14f28-122">وهذا يعني أنه إذا كان لديك بند عمل من 100 قطعة للصنف A من الموقع Loc1، فلن تتمكن من نقل 30 قطعة فقط للصنف A من هناك إلى موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="14f28-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="14f28-123">قد يؤدي هذا إلى تقسيم بند العمل موجود إلى 30 و70، لأن المواقع باتت الآن مختلفة.</span><span class="sxs-lookup"><span data-stu-id="14f28-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="14f28-124">بالنسبة إلى سيناريوهات الإعداد، حيث تم تعيين لوحة الترخيص التي تنقل الأصناف منها أو لوحة الترخيص التي تنقل الأصناف إليها كلوحة الترخيص الهدف‬ لأمر عمل، يسمح فقط بنقل لوحة الترخيص بكاملها لكي لا يتم تقسيم لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="14f28-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="14f28-125">في الوقت الحالي، يتم دعم الحركة المخصصة فقط.</span><span class="sxs-lookup"><span data-stu-id="14f28-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="14f28-126">وهذا يعني أنك لن تتمكن من نقل المخزون المحجوز من خلال عملية النقل بواسطة عناصر قائمة الجهاز المحمول للقالب.</span><span class="sxs-lookup"><span data-stu-id="14f28-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="14f28-127">إعداد إذن لنقل المخزون المحجوز لعاملين فرديين</span><span class="sxs-lookup"><span data-stu-id="14f28-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="14f28-128">بالنسبة إلى العامل الذي من المفترض أن يسمح له بنقل المخزون المحجوز، حدد خانة الاختيار **السماح بنقل المخزون مع العمل المقترن‬** ضمن **إدارة المستودعات** > **الإعداد** > **العامل**.</span><span class="sxs-lookup"><span data-stu-id="14f28-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="14f28-129">الحمل العكسي</span><span class="sxs-lookup"><span data-stu-id="14f28-129">Backported</span></span>

<span data-ttu-id="14f28-130">تم أيضًا إجراء تحميل عكسي لهذه الميزة إلى Microsoft Dynamics AX 2012 R3 وسيتكون متوفرة كجزء من CU12.</span><span class="sxs-lookup"><span data-stu-id="14f28-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="14f28-131">يمكن أيضًا تنزيلها بشكل فردي من خلال رقم قاعدة المعارف 3192548.</span><span class="sxs-lookup"><span data-stu-id="14f28-131">It can also be downloaded individually through KB number 3192548.</span></span> 


