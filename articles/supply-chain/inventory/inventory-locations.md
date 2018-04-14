---
title: "مواقع المخزون"
description: "تُستخدم مواقع المخزون مع التخزين الأساسي (WMS I) لتحديد المكان الذي يتم فيه تخزين الأصناف والمكان الذي يتم منه انتقاء الأصناف من مستودع (WMS I)."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2a0af10d1d94f9ead2b024e1afd009d60ee13590
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="inventory-locations"></a><span data-ttu-id="b6d87-103">مواقع المخزون</span><span class="sxs-lookup"><span data-stu-id="b6d87-103">Inventory locations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b6d87-104">تُستخدم مواقع المخزون مع التخزين الأساسي (WMS I) لتحديد المكان الذي يتم فيه تخزين الأصناف والمكان الذي يتم منه انتقاء الأصناف من مستودع (WMS I).</span><span class="sxs-lookup"><span data-stu-id="b6d87-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="b6d87-105">ينطبق هذا الموضوع على ميزات في وحدة إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="b6d87-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="b6d87-106">ولا ينطبق على الميزات الموجودة في وحدة إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="b6d87-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="b6d87-107">يشير مصطلح الموقع إلى المكان الذي يتم فيه تخزين الأصناف وسحبها منه.</span><span class="sxs-lookup"><span data-stu-id="b6d87-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="b6d87-108">وبالنسبة لكل موقع، يمكنك أيضًا تحديد مكان إدراج الصنف.</span><span class="sxs-lookup"><span data-stu-id="b6d87-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="b6d87-109">افتراضيًا، فإنهم يمثلون نفس الشيء.</span><span class="sxs-lookup"><span data-stu-id="b6d87-109">By default, they are the same.</span></span> <span data-ttu-id="b6d87-110">وعادة ما يتم إدراج الأصناف وسحبها من نفس الجانب بالموقع، إلا أن ذلك لا يتم في جميع الأحيان.</span><span class="sxs-lookup"><span data-stu-id="b6d87-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="b6d87-111">فمثلاً، يتم إدراج الأصناف المخزنة في حوامل تخزين مباشر من ممر واحد وسحبها من ممر آخر.</span><span class="sxs-lookup"><span data-stu-id="b6d87-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="b6d87-112">يتم توفير الإدخال الرئيسي حسب اسم الموقع، والذي يتم تحديده عادةً حسب إحداثياته: مستودع، وممر، ورف، وصندوق.</span><span class="sxs-lookup"><span data-stu-id="b6d87-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="b6d87-113">يمكنك إدخال هذا الاسم أو المعرّف يدويًا أو الحصول عليه من خلال إحداثيات الموقع؛ مثلاً 01-02-03-4 للممر 1 والحامل 2 والرّف 3 والصندوق 4 في صفحة مواقع المخزون.</span><span class="sxs-lookup"><span data-stu-id="b6d87-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="b6d87-114">خصائص الموقع</span><span class="sxs-lookup"><span data-stu-id="b6d87-114">Location properties</span></span>

<span data-ttu-id="b6d87-115">يتميز الموقع بالخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="b6d87-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="b6d87-116">الحجم (الارتفاع، والعرض، والعمق، ومن ثمَّ الحجم)</span><span class="sxs-lookup"><span data-stu-id="b6d87-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="b6d87-117">موضع المستودع، والممر، والحامل، والرف، والصندوق</span><span class="sxs-lookup"><span data-stu-id="b6d87-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="b6d87-118">نوع الموقع (موقع كبير، أو موقع انتقاء، أو رصيف داخلي، أو رصيف خارجي، أو موقع إدخال الإنتاج، أو موقع الفحص أو سوبر ماركت كانبان)</span><span class="sxs-lookup"><span data-stu-id="b6d87-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="b6d87-119">يمكنك استخدام نص تحقق في الأنظمة عبر الإنترنت للتأكد من أن المشغل قد قام بتحديد الموقع الصحيح لصنف محدد.</span><span class="sxs-lookup"><span data-stu-id="b6d87-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="b6d87-120">ويمكنك إنشاء نص التحقق هذا يدويًا أو بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="b6d87-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="b6d87-121">أكواد الفرز</span><span class="sxs-lookup"><span data-stu-id="b6d87-121">Sort codes</span></span>
<span data-ttu-id="b6d87-122">تستخدم أكواد الفرز لتحسين معالجة بنود الانتقاء، والتي تحتوي على وصفًا للمعلومات المطلوبة لانتقاء الأصناف من المخزون، بما في ذلك أمر الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="b6d87-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="b6d87-123">يمكنك تحديد أكواد الفرز حسب الممر والإحداثيات الأخرى أو تعيينها يدويًا للموقع.</span><span class="sxs-lookup"><span data-stu-id="b6d87-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="b6d87-124">المواقع المحظورة</span><span class="sxs-lookup"><span data-stu-id="b6d87-124">Blocked locations</span></span>
<span data-ttu-id="b6d87-125">أحيانًا، قد ترغب في الإشارة إلى حظر موقع لفترة من الوقت، للسماح بالقيام بعمليات الإصلاح مثلاً.</span><span class="sxs-lookup"><span data-stu-id="b6d87-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="b6d87-126">كما قد ترغب في أحيان أخرى في الإشارة إلى حظر الإدخال فقط أو الإخراج فقط.</span><span class="sxs-lookup"><span data-stu-id="b6d87-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="b6d87-127">بنية الشجرة</span><span class="sxs-lookup"><span data-stu-id="b6d87-127">Tree structure</span></span>

<span data-ttu-id="b6d87-128">في صفحة "مواقع المخزون"، يمكنك عرض تخطيط المستودع في بنية شجرة استناداً إلى إحداثيات مواقع المخزون، في تنسيق عرض محدد.</span><span class="sxs-lookup"><span data-stu-id="b6d87-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="b6d87-129">الاحتفاظ بمواقع المخزون عبر نموذج المستودع</span><span class="sxs-lookup"><span data-stu-id="b6d87-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="b6d87-130">من الممكن نسخ المواقع من مستودع واحد إلى آخر وإنشاء مواقع عبر معالج.</span><span class="sxs-lookup"><span data-stu-id="b6d87-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="b6d87-131">وقبل تشغيل المعالج، يجب التأكد من أن قمت بتحديد أسماء المواقع الافتراضية في صفحة المستودع.</span><span class="sxs-lookup"><span data-stu-id="b6d87-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="see-also"></a><span data-ttu-id="b6d87-132">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b6d87-132">See also</span></span>
--------

[<span data-ttu-id="b6d87-133">إنشاء تخطيط مستودع جديد (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="b6d87-133">Create a new warehouse layout (Task guide)</span></span>](tasks/create-new-warehouse-layout.md)

