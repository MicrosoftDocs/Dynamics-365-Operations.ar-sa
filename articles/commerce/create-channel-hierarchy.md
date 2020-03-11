---
title: إنشاء تدرج هرمي للتنقل في قناة
description: يوضح هذا الموضوع ‏‫التدرج الهرمي للتنقل في قناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002026"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="d9632-103">إنشاء تدرج هرمي للتنقل في قناة</span><span class="sxs-lookup"><span data-stu-id="d9632-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d9632-104">يوضح هذا الموضوع ‏‫التدرج الهرمي للتنقل في قناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9632-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d9632-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d9632-105">Overview</span></span>

<span data-ttu-id="d9632-106">يُستخدم ‏‫التدرج الهرمي للتنقل في قناة لتجميع المنتجات وتنظيمها في فئات حتى يمكن استعراض المنتجات على الإنترنت أو في نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="d9632-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="d9632-107">إنشاء تدرج هرمي للتنقل في قناة</span><span class="sxs-lookup"><span data-stu-id="d9632-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="d9632-108">لإنشاء تدرج هرمي للتنقل في قناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d9632-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="d9632-109">في جزء التنقل، انتقل إلى الوحدات **النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> فئات التنقل في القنوات**.</span><span class="sxs-lookup"><span data-stu-id="d9632-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="d9632-110">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d9632-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d9632-111">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="d9632-112">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="d9632-113">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="d9632-113">Select **Create**.</span></span>
1. <span data-ttu-id="d9632-114">في جزء الإجراءات، حدد **عقدة فئة جديدة‬‏‫** لإنشاء عقدة جذر.</span><span class="sxs-lookup"><span data-stu-id="d9632-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="d9632-115">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="d9632-116">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="d9632-117">في المربع **الاسم المألوف**، أدخل اسمًا مألوفًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="d9632-118">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9632-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d9632-119">تعرض الصورة التالية مثالاً لعقدة جذر.</span><span class="sxs-lookup"><span data-stu-id="d9632-119">The following image shows a example root node.</span></span>

![نموذج عقدة الجذر](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="d9632-121">إنشاء عقد فئات التنقل</span><span class="sxs-lookup"><span data-stu-id="d9632-121">Create navigation category nodes</span></span>

<span data-ttu-id="d9632-122">لإنشاء أي عقد فئات تنقل إضافية لتمثيل فئات المنتجات في القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d9632-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="d9632-123">في جزء التنقل، حدد العقدة الأصلية لإضافة فئة إليها.</span><span class="sxs-lookup"><span data-stu-id="d9632-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="d9632-124">في جزء الإجراءات، حدد **عقدة الفئة الجديدة‬**.</span><span class="sxs-lookup"><span data-stu-id="d9632-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="d9632-125">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="d9632-126">في مربع **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="d9632-127">في المربع **الاسم المألوف**، أدخل اسمًا مألوفًا.</span><span class="sxs-lookup"><span data-stu-id="d9632-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="d9632-128">في مربع **ترتيب العرض**، أدخل ترتيبًا للعرض (اختياري).</span><span class="sxs-lookup"><span data-stu-id="d9632-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="d9632-129">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9632-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d9632-130">تعرض الصورة التالية مثالاً لتدرج هرمي للتنقل في قناة مكتمل.</span><span class="sxs-lookup"><span data-stu-id="d9632-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![نموذج تدرج هرمي لقناة](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="d9632-132">إضافة منتجات إلى عقد الفئات</span><span class="sxs-lookup"><span data-stu-id="d9632-132">Add products to category nodes</span></span>

<span data-ttu-id="d9632-133">لإضافة منتجات إلى عقد الفئات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d9632-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="d9632-134">حدد عقدة فئة.</span><span class="sxs-lookup"><span data-stu-id="d9632-134">Select a category node.</span></span>
1. <span data-ttu-id="d9632-135">ضمن **المنتجات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d9632-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="d9632-136">ابحث عن المنتجات الجديدة التي ترغب في إضافتها باستخدام رقم المنتج أو اسم المنتج، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d9632-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="d9632-137">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9632-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="d9632-138">لا يعد إضافة منتجات إلى عقدة داخل التدرج الهرمي للتنقل في القناة أمرًا كافيًا لإظهار المنتجات على قناة محددة، يجب أيضًا تصنيف المنتجات إلى منتج.</span><span class="sxs-lookup"><span data-stu-id="d9632-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="d9632-139">تعرض الصورة التالية مثالاً لعقدة بمنتجات تمت إضافتها.</span><span class="sxs-lookup"><span data-stu-id="d9632-139">The following image shows an example node with products added.</span></span>

![المنتجات المضافة إلى عقده فئة](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="d9632-141">أضف مجموعات سمات المنتجات إلى عقد الفئات</span><span class="sxs-lookup"><span data-stu-id="d9632-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="d9632-142">يجب إنشاء مجموعات السمات قبل أن تتمكن من إضافتها إلى عقدة داخل التدرج الهرمي للتنقل في القناة.</span><span class="sxs-lookup"><span data-stu-id="d9632-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="d9632-143">لإضافة مجموعة سمات منتج لعقدة فئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d9632-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="d9632-144">حدد عقدة فئة.</span><span class="sxs-lookup"><span data-stu-id="d9632-144">Select a category node.</span></span>
1. <span data-ttu-id="d9632-145">ضمن **مجموعة سمات المنتج**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d9632-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="d9632-146">ابحث عن مجموعات السمات التي ترغب في إضافتها ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d9632-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="d9632-147">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d9632-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d9632-148">تعرض الصورة التالية نموذج عقدة تحتوي على مجموعة سمات منتج مضافة.</span><span class="sxs-lookup"><span data-stu-id="d9632-148">The following image shows a sample node with product attribute groups added.</span></span>

![مجموعات سمات المنتج في عقدة](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="d9632-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d9632-150">Additional resources</span></span>

[<span data-ttu-id="d9632-151">إعداد عمليات الفرز</span><span class="sxs-lookup"><span data-stu-id="d9632-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="d9632-152">إدارة السمات ومجموعات السمات</span><span class="sxs-lookup"><span data-stu-id="d9632-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)