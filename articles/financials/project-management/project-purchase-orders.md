---
title: "أوامر الشراء لمشروع"
description: "توضح هذه المقالة مختف الأساليب التي يمكنك استخدامها لإنشاء أوامر شراء لمشروع. يتوقف الأسلوب الذي تستخدمه على غرض أمر الشراء، والوقت الذي يتم فيه استهلاك الأصناف التي تم شراؤها وتحميل المشروع تكاليفها."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1797bc49877f1c8c06797083d1c7b76934675ba3
ms.contentlocale: ar-sa
ms.lasthandoff: 02/07/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="6c5b4-104">أوامر الشراء لمشروع</span><span class="sxs-lookup"><span data-stu-id="6c5b4-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6c5b4-105">توضح هذه المقالة مختف الأساليب التي يمكنك استخدامها لإنشاء أوامر شراء لمشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="6c5b4-106">يتوقف الأسلوب الذي تستخدمه على غرض أمر الشراء، والوقت الذي يتم فيه استهلاك الأصناف التي تم شراؤها وتحميل المشروع تكاليفها.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="6c5b4-107">في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، يمكنك استخدام أساليب متعددة لإنشاء أوامر شراء لمشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="6c5b4-108">يتوقف الأسلوب الذي تستخدمه على غرض أمر الشراء، والوقت الذي يتم فيه استهلاك الأصناف التي تم شراؤها، والوقت الذي يتم فيه تحميل المشروع تكاليف الأصناف.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="6c5b4-109">أساليب لإنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="6c5b4-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="6c5b4-110">يمكنك استخدام أحد الأساليب التالية لإنشاء أمر شراء في المحاسبة وإدارة المشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="6c5b4-111">يحدد غرض أمر الشراء الوقت الذي سيتم فيه استهلاك فيه أمر الشراء، وبالتالي إلى تحديد الوقت الذي سيتم فيه تحميل المشروع تكاليف الأصناف.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c5b4-112">الأسلوب</span><span class="sxs-lookup"><span data-stu-id="6c5b4-112">Method</span></span></th>
<th><span data-ttu-id="6c5b4-113">الغرض</span><span class="sxs-lookup"><span data-stu-id="6c5b4-113">Purpose</span></span></th>
<th><span data-ttu-id="6c5b4-114">استهلاك الأصناف</span><span class="sxs-lookup"><span data-stu-id="6c5b4-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c5b4-115">إنشاء أمر شراء مباشرةً من مشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="6c5b4-116">استخدم هذه الطريقة لشراء أصناف من مورد خارجي للاستهلاك في مشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="6c5b4-117">يمكنك إنشاء أمر الشراء باستخدام طريقتين:</span><span class="sxs-lookup"><span data-stu-id="6c5b4-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="6c5b4-118">من المشروع نفسه.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-118">From the project itself.</span></span> <span data-ttu-id="6c5b4-119">وفي هذه الحالة يكون المشروع معرفًا بالفعل لأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="6c5b4-120">عن طريق الانتقال إلى أمر شراء المشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="6c5b4-121">يجب تحديد كل من المورد والمشروع المراد إنشاء أمر الشراء لهما.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="6c5b4-122">يتم استهلاك الأصناف عندما يتم تحديث فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c5b4-123">إنشاء أمر شراء من أمر توريد.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="6c5b4-124">استخدم هذا الأسلوب لشراء الأصناف عندما تنشئ أمر مبيعات من مشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="6c5b4-125">يتم استهلاك الأصناف عند فوترة أمر التوريد إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c5b4-126">إنشاء أمر شراء من أحد متطلبات الصنف.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="6c5b4-127">استخدم هذا الأسلوب لشراء الأصناف عندما تنشئ أحد متطلبات الصنف من مشروع.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="6c5b4-128">يتم استهلاك الأصناف عندما يتم تحديث إيصال تعبئة متطلبات الصنف.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="6c5b4-129">عند تحديث فاتورة المورد أو إيصال تعبئة، فإنه تتم مطالبتك بتحديث إيصال التعبئة الخاص بمتطلبات الصنف.</span><span class="sxs-lookup"><span data-stu-id="6c5b4-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="6c5b4-130">للحصول على مزيد من المعلومات، راجع [تلقي الأصناف على أمر شراء من طلبات الصنف‬](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="6c5b4-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


