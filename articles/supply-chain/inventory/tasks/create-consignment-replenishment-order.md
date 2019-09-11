---
title: إنشاء أمر تزويد شحن
description: يوضح هذا الموضوع كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن.
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f426dbf00eace23da2f26eb50dd9675fe22ed445
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914759"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="211f7-103">إنشاء أمر تزويد شحن</span><span class="sxs-lookup"><span data-stu-id="211f7-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="211f7-104">يوضح هذا الموضوع كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن.</span><span class="sxs-lookup"><span data-stu-id="211f7-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="211f7-105">ويوضح أيضًا كيفية تسجيل إيصال استلام المنتجات بحيث يتم تسجيل مخزون الشحن كمخزون فعلي يملكه المورّد.</span><span class="sxs-lookup"><span data-stu-id="211f7-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="211f7-106">يقوم عادةً أخصائي التدبير بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="211f7-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="211f7-107">ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="211f7-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="211f7-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="211f7-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="211f7-109">إنشاء أمر تزويد شحن</span><span class="sxs-lookup"><span data-stu-id="211f7-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="211f7-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > التدبير والتوريد > الشحن > أوامر تزويد الشحن‬**.</span><span class="sxs-lookup"><span data-stu-id="211f7-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="211f7-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="211f7-111">Select **New**.</span></span>
3. <span data-ttu-id="211f7-112">في الحقل **حساب المورّد**، حدد المورّد **US-104** (يجب تحديد مورّد غير مسجل كمالك في صفحة **ملاك المخزون**).</span><span class="sxs-lookup"><span data-stu-id="211f7-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="211f7-113">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="211f7-113">Select **OK**.</span></span>
5. <span data-ttu-id="211f7-114">حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="211f7-114">Select **Add line**.</span></span>
6. <span data-ttu-id="211f7-115">في الحقل **رقم الصنف**، اكتب `M9211CI` (يجب تحديد صنف تم إعداده لمخزون الشحن).</span><span class="sxs-lookup"><span data-stu-id="211f7-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="211f7-116">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="211f7-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="211f7-117">في حقل **‏‫تاريخ التسليم المطلوب‬‬**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="211f7-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="211f7-118">يتم استخدام التواريخ المطلوبة والمؤكدة بواسطة محرك MRP لوصول البضائع المنتظر.</span><span class="sxs-lookup"><span data-stu-id="211f7-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="211f7-119">في حقل **‏‫تاريخ التسليم المؤكد‬**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="211f7-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="211f7-120">قم بتوسيع قسم **تفاصيل البند**.</span><span class="sxs-lookup"><span data-stu-id="211f7-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="211f7-121">حدد علامة التبويب **أبعاد المخزون**.</span><span class="sxs-lookup"><span data-stu-id="211f7-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="211f7-122">لإظهار المالك في الحقل **مالك أبعاد المخزون**، قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="211f7-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="211f7-123">تم الآن إدراج المورّد US-104 كالمالك.</span><span class="sxs-lookup"><span data-stu-id="211f7-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="211f7-124">التحقق من حالة حركة المخزون</span><span class="sxs-lookup"><span data-stu-id="211f7-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="211f7-125">حدد **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="211f7-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="211f7-126">حدد **الحركات**.</span><span class="sxs-lookup"><span data-stu-id="211f7-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="211f7-127">في الصف المطلوب، لاحظ أنه تم تعيين حقل **الاستلام** إلى **مطلوب‬**.</span><span class="sxs-lookup"><span data-stu-id="211f7-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="211f7-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="211f7-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="211f7-129">استلام الأصناف</span><span class="sxs-lookup"><span data-stu-id="211f7-129">Receive items</span></span>
1. <span data-ttu-id="211f7-130">حدد **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="211f7-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="211f7-131">في الحقل **إيصال استلام المنتجات الخارجي‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="211f7-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="211f7-132">في حقل **الكمية**، أدخل رقمًا أقل من الرقم الذي يظهر هناك.</span><span class="sxs-lookup"><span data-stu-id="211f7-132">In the **Quantity** field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="211f7-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="211f7-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="211f7-134">التحقق من المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="211f7-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="211f7-135">حدد **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="211f7-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="211f7-136">حدد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="211f7-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="211f7-137">حدد **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="211f7-137">Select **Overview**.</span></span> <span data-ttu-id="211f7-138">تتوفر الأصناف التي تم استلامها كمخزون شحن مملوك من قِبل المورّد بشكل فعلي.</span><span class="sxs-lookup"><span data-stu-id="211f7-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="211f7-139">وتظهر الكمية المتبقية في أمر تزويد الشحن في حقل **الكمية المطلوبة إجمالاً‬**.</span><span class="sxs-lookup"><span data-stu-id="211f7-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="211f7-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="211f7-140">Close the page.</span></span>

