---
title: إنشاء مجموعة متغير
description: يوضح هذا الموضوع كيفية إنشاء مجموعة متغير لون أو نمط أو مقاس لمنتج في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4c34aca043f10fef38f186800c429cac36c41ce7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207837"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="c16cd-103">إنشاء مجموعة متغيرات</span><span class="sxs-lookup"><span data-stu-id="c16cd-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c16cd-104">يوضح هذا الموضوع كيفية إنشاء مجموعة متغير لون أو نمط أو مقاس لمنتج في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c16cd-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c16cd-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c16cd-105">Overview</span></span>

<span data-ttu-id="c16cd-106">يدعم Dynamics 365 Commerce متغيرات متعددة للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="c16cd-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="c16cd-107">ويعد من المثالي إعداد مجموعات المتغير لفئات منتجات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="c16cd-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="c16cd-108">على سبيل المثال، يمكن إنشاء مجموعة حجم لقمصان بالمقاسات صغير جدًا وصغير ومتوسط وكبير وكبيرة جدًا، أو مجموعة لون يمكن إنشاؤها لتضمين كافة الألوان المتوفرة لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c16cd-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="c16cd-109">يجب إضافة مجموعات المتغير قبل إضافة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c16cd-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="c16cd-110">في هذا الموضوع، سيتم إنشاء مجموعة مقاس وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="c16cd-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="c16cd-111">يمكن استخدام إجراءات مشابهة لإضافة مجموعات النمط ومجموعات اللون وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="c16cd-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="c16cd-112">إنشاء مجموعة مقاس</span><span class="sxs-lookup"><span data-stu-id="c16cd-112">Create a size group</span></span>

<span data-ttu-id="c16cd-113">لإنشاء مجموعة مقاس، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c16cd-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="c16cd-114">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> مجموعات المتغير \> مجموعات المقاس**.</span><span class="sxs-lookup"><span data-stu-id="c16cd-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="c16cd-115">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c16cd-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c16cd-116">في المربع **مجموعة المقاس**، أدخل اسمًا لمجموعة المقاس.</span><span class="sxs-lookup"><span data-stu-id="c16cd-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="c16cd-117">في مربع **الوصف**، أدخل وصفًا مناسبًا.</span><span class="sxs-lookup"><span data-stu-id="c16cd-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="c16cd-118">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c16cd-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="c16cd-119">إضافة سمات إلى مجموعة المقاس</span><span class="sxs-lookup"><span data-stu-id="c16cd-119">Add attributes to the size group</span></span>

<span data-ttu-id="c16cd-120">لإضافة سمات إلى مجموعة المقاس، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c16cd-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="c16cd-121">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> مجموعات المتغير \> مجموعات المقاس**</span><span class="sxs-lookup"><span data-stu-id="c16cd-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="c16cd-122">في جزء التنقل، حدد مجموعة المقاس.</span><span class="sxs-lookup"><span data-stu-id="c16cd-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="c16cd-123">ضمن **سطور مجموعة المقاس**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c16cd-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="c16cd-124">في مربع **المقاس**، أدخل سلسلة لتمثيل المقاس (على سبيل المثال "XL").</span><span class="sxs-lookup"><span data-stu-id="c16cd-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="c16cd-125">في المربع **اسم المقاس**، أدخل اسمًا للمقاس (على سبيل المثال، "كبير جدًا").</span><span class="sxs-lookup"><span data-stu-id="c16cd-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="c16cd-126">في المربع **وزن التزويد**، أدخل رقمًا يمثل وزن التزويد.</span><span class="sxs-lookup"><span data-stu-id="c16cd-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="c16cd-127">في المربع **الرقم في الكود الشريطي**، أدخل رقمًا يمثل الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="c16cd-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="c16cd-128">في المربع **ترتيب العرض**، أدخل رقمًا يمثل ترتيب العرض.</span><span class="sxs-lookup"><span data-stu-id="c16cd-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="c16cd-129">عند الانتهاء من إضافة المقاسات، حدد **حفظ** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="c16cd-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="c16cd-130">تعرض الصورة التالية مثالاً لمجموعة مقاس "لمقاسات قمصان غير رسمية".</span><span class="sxs-lookup"><span data-stu-id="c16cd-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![إنشاء مجموعة مقاس](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="c16cd-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c16cd-132">Additional resources</span></span>

[<span data-ttu-id="c16cd-133">نظرة عامة على معلومات المنتجات</span><span class="sxs-lookup"><span data-stu-id="c16cd-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c16cd-134">إعداد منتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c16cd-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="c16cd-135">أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="c16cd-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]