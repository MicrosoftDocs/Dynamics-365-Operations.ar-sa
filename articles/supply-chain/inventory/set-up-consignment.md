---
title: "إعداد الشحن"
description: "يشرح هذا الموضوع كيفية تكوين عمليات مخزون الشحن الوارد."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 758ea8b658693910edeada3a4c27c34ae187b28c
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-consignment"></a><span data-ttu-id="d2386-103">إعداد الشحن</span><span class="sxs-lookup"><span data-stu-id="d2386-103">Set up consignment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2386-104">يشرح هذا الموضوع كيفية تكوين عمليات مخزون الشحن الوارد.</span><span class="sxs-lookup"><span data-stu-id="d2386-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="d2386-105">إن مخزون الشحن هو المخزون الذي يملكه المورد، ولكنه مخزن في موقعك.</span><span class="sxs-lookup"><span data-stu-id="d2386-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="d2386-106">عندما تصبح جاهزًا لاستهلاك المخزون أو استخدامه، يمكنك الحصول على ملكية المخزون.</span><span class="sxs-lookup"><span data-stu-id="d2386-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="d2386-107">يصف هذا الموضوع الإعداد المطلوب لتمكين عمليات الشحن.</span><span class="sxs-lookup"><span data-stu-id="d2386-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="d2386-108">للحصول على مزيد من المعلومات حول عمليات الشحن، راجع [الشحن](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="d2386-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="d2386-109">ملاك المخزون</span><span class="sxs-lookup"><span data-stu-id="d2386-109">Inventory owners</span></span>
<span data-ttu-id="d2386-110">من أجل تسجيل المخزون الفعلي للشحن الوارد، يجب تعريف المالك المورّد.</span><span class="sxs-lookup"><span data-stu-id="d2386-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="d2386-111">ويتم ذلك في صفحة **مالك المخزون**.</span><span class="sxs-lookup"><span data-stu-id="d2386-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="d2386-112">عند تحديد **حساب المورد**، يؤدي ذلك إلى إنشاء القيم الافتراضية لحقلي **الاسم** و **المالك**.</span><span class="sxs-lookup"><span data-stu-id="d2386-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="d2386-113">ستكون القيمة في حقل **المالك** مرئية للمورد، لذا قد ترغب في تغييرها إذا لم يكن من السهل على الأشخاص الخارجيين التعرف على أسماء حسابات المورد.</span><span class="sxs-lookup"><span data-stu-id="d2386-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="d2386-114">من الممكن تحرير حقل **المالك**، لكن فقط إلى المرحلة التي تقوم فيها بحفظ سجل **مالك المخزون**.</span><span class="sxs-lookup"><span data-stu-id="d2386-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="d2386-115">تتم تعبئة حقل **الاسم** باسم الطرف الذي يقترن حساب المورد به، ولا يمكن تغيير ذلك.</span><span class="sxs-lookup"><span data-stu-id="d2386-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="d2386-116">[![ملاك المخزون](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="d2386-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="d2386-117">مجموعة أبعاد التعقب</span><span class="sxs-lookup"><span data-stu-id="d2386-117">Tracking dimension group</span></span>
<span data-ttu-id="d2386-118">يجب أن تقترن الأصناف التي سيتم استخدامها في عمليات الشحن **بمجموعة أبعاد التعقب** حيث تم تعيين بُعد **المالك** إلى **نشط**.</span><span class="sxs-lookup"><span data-stu-id="d2386-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="d2386-119">في بُعد المالك، يكون الخياران **المخزون الفعلي** و**المخزون المالي** محددين بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="d2386-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="d2386-120">ولا يتم تحديد الخيار **خطة التغطية حسب البُعد‬** إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="d2386-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="d2386-121">[![مجموعة أبعاد التعقب](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="d2386-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="d2386-122">دفتر يومية تغييرات ملكية المخزون</span><span class="sxs-lookup"><span data-stu-id="d2386-122">Inventory ownership change journal</span></span>
<span data-ttu-id="d2386-123">يُستخدم **دفتر يومية تغيير ملكية المخزون**لتسجيل تحويل ملكية مخزون الشحن من المورّد إلى الكيان القانوني الذي يستهلكه.</span><span class="sxs-lookup"><span data-stu-id="d2386-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="d2386-124">وكما هو الحال في أي دفتر يومية مخزون، يجب تعريفه بواسطة اسم دفتر يومية المخزون.</span><span class="sxs-lookup"><span data-stu-id="d2386-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="d2386-125">يتم إنشاء هذه الأسماء في صفحة **أسماء دفتر يومية المخزون** الصفحة، ويجب تعيين **نوع دفتر اليومية** إلى **تغيير الملكية**.</span><span class="sxs-lookup"><span data-stu-id="d2386-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="d2386-126">[![دفتر يومية تغييرات ملكية المخزون](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="d2386-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="d2386-127">تعاون المورد في عمليات الشحن</span><span class="sxs-lookup"><span data-stu-id="d2386-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="d2386-128">عندما يستخدم الموردون واجهة تعاون المورد، يمكنهم استخدامها لمراقبة استهلاك المخزون في موقعك.</span><span class="sxs-lookup"><span data-stu-id="d2386-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="d2386-129">لمزيد من المعلومات حول إعداد الموردين لاستخدام تعاون المورِّد‏‎، راجع [تكوين الأمان لمستخدمي تعاون المورِّد](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="d2386-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

