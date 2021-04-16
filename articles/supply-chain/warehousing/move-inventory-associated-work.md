---
title: حركة المخزون مع العمل المقترن في إدارة المستودعات
description: باستخدام نقل المخزون، يمكنك أن تحدد العاملين في المستودع الذين يتم السماح لهم بنقل المخزون المحجوز.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6477a91b3c65e8be5ab527eaff12c92ae7918b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808740"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="1c10a-103">حركة المخزون مع العمل المقترن في إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="1c10a-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c10a-104">باستخدام نقل المخزون، يمكنك أن تحدد العاملين في المستودع الذين يتم السماح لهم بنقل المخزون المحجوز.</span><span class="sxs-lookup"><span data-stu-id="1c10a-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="1c10a-105">من شأن ذلك أن يوفر مرونة في المستودعات المنظمة حيث يمكنك تحديد عدم السماح لعامل باختيار موقع انتقاء جديد لعمل الانتقاء الذي أنشأه.</span><span class="sxs-lookup"><span data-stu-id="1c10a-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="1c10a-106">ويسمح أيضًا لمدير المستودع بمراقبة القدرات التي ينبغي أن تكون لدى بعض العاملين ذوي خبرات أقل.</span><span class="sxs-lookup"><span data-stu-id="1c10a-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="1c10a-107">قد تكون المرونة في إدارة العمليات اليومية للعاملين في المستودعات مفيدة في سيناريوهات كتلك التي تلي:</span><span class="sxs-lookup"><span data-stu-id="1c10a-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="1c10a-108">السيناريو 1</span><span class="sxs-lookup"><span data-stu-id="1c10a-108">Scenario 1</span></span>

<span data-ttu-id="1c10a-109">شركة لديها مساحة استلام صغيرة نسبيًا، وهي مزدحمة بالبالتات والصناديق المخزنة فيها.</span><span class="sxs-lookup"><span data-stu-id="1c10a-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="1c10a-110">من المتوقع وصول شحنة كبيرة في اليوم الحالي، لذلك يقرر موظف الاستلام‬ تحرير منطقة الاستلام عن طريق نقل بعض البالتات‬ إلى منطقة إعداد داخلية ثانوية.</span><span class="sxs-lookup"><span data-stu-id="1c10a-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="1c10a-111">السيناريو 2</span><span class="sxs-lookup"><span data-stu-id="1c10a-111">Scenario 2</span></span>

<span data-ttu-id="1c10a-112">يلاحظ عامل مستودع من ذوي الخبرة فرصة في مستودع ما لتجميع العناصر في مكان واحد بدلاً من تقسيمها عبر ثلاثة مواقع مجاورة يحتوي كل واحد منها على كمية صغيرة.</span><span class="sxs-lookup"><span data-stu-id="1c10a-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across three nearby locations with little quantity on each.</span></span> <span data-ttu-id="1c10a-113">يريد العامل تجميع الكمية عن طريق نقل العناصر من كل واحد من هذه المواقع إلى الموقع نفسه وإلى لوحة الترخيص نفسها.</span><span class="sxs-lookup"><span data-stu-id="1c10a-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="1c10a-114">السيناريو 3</span><span class="sxs-lookup"><span data-stu-id="1c10a-114">Scenario 3</span></span>

<span data-ttu-id="1c10a-115">هناك بالتة تنتظر الشحن في موقع إعداد، مثل STAGE01، القريب من BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="1c10a-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="1c10a-116">ومع ذلك، ونظرًا لتغيير الخطط تم جدولة وصول الشاحنة إلى BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="1c10a-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="1c10a-117">موظف الشحن يدرك ذلك ويريد التأكد من أن الشاحنة لن تنتظر تحميلها من STAGE01.</span><span class="sxs-lookup"><span data-stu-id="1c10a-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="1c10a-118">يقرر موظف الشحن نقل الأصناف في هذه الشحنة من STAGE01 إلى STAGE04، الأقرب إلى الوجهة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1c10a-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="1c10a-119">القيود الحالية</span><span class="sxs-lookup"><span data-stu-id="1c10a-119">Current limitations</span></span>

<span data-ttu-id="1c10a-120">تقتصر عمليات حجز العمل التي يمكنك نقلها على أمر المبيعات وإصدار أمر التحويل واستلام أمر التحويل وأمر الشراء وعمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="1c10a-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="1c10a-121">يتم تقييد نقل الأصناف لمنع تقسيم بنود العمل.</span><span class="sxs-lookup"><span data-stu-id="1c10a-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="1c10a-122">وهذا يعني أنه إذا كان لديك بند عمل من 100 قطعة للصنف A من الموقع Loc1، فلن تتمكن من نقل 30 قطعة فقط للصنف A من هناك إلى موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="1c10a-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="1c10a-123">قد يؤدي هذا إلى تقسيم بند العمل موجود إلى 30 و70، لأن المواقع باتت الآن مختلفة.</span><span class="sxs-lookup"><span data-stu-id="1c10a-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="1c10a-124">بالنسبة إلى سيناريوهات الإعداد، حيث تم تعيين لوحة الترخيص التي تنقل الأصناف منها أو لوحة الترخيص التي تنقل الأصناف إليها كلوحة الترخيص الهدف‬ لأمر عمل، يسمح فقط بنقل لوحة الترخيص بكاملها لكي لا يتم تقسيم لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="1c10a-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>

<span data-ttu-id="1c10a-125">في الوقت الحالي، يتم دعم الحركة المخصصة فقط.</span><span class="sxs-lookup"><span data-stu-id="1c10a-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="1c10a-126">وهذا يعني أنك لن تتمكن من نقل المخزون المحجوز من خلال عملية النقل بواسطة عناصر قائمة الجهاز المحمول للقالب.</span><span class="sxs-lookup"><span data-stu-id="1c10a-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="1c10a-127">إعداد إذن لنقل المخزون المحجوز لعاملين فرديين</span><span class="sxs-lookup"><span data-stu-id="1c10a-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="1c10a-128">بالنسبة إلى العامل الذي من المفترض أن يسمح له بنقل المخزون المحجوز، حدد خانة الاختيار **السماح بنقل المخزون مع العمل المقترن** ضمن **إدارة المستودعات \> الإعداد \> العامل**.</span><span class="sxs-lookup"><span data-stu-id="1c10a-128">For the worker who is allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management \> Setup \> Worker**.</span></span>  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
