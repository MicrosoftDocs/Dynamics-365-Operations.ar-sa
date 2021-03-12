---
title: إنشاء منتج جديد في Commerce
description: يوضح هذا الموضوع كيفية إنشاء منتج جديد في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b578c1bdfe1c6b4bf66cc85cc09ed906fb812a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965293"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="c9aee-103">إنشاء منتج جديد في Commerce</span><span class="sxs-lookup"><span data-stu-id="c9aee-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c9aee-104">يوضح هذا الموضوع كيفية إنشاء منتج جديد في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9aee-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9aee-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c9aee-105">Overview</span></span>

<span data-ttu-id="c9aee-106">يتحدد المنتج بشكل أساسي بواسطة رقمه واسمه ووصفه.</span><span class="sxs-lookup"><span data-stu-id="c9aee-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="c9aee-107">ومع ذلك، هناك بيانات أخرى مطلوبة أيضًا لوصف المنتج أو الخدمة:</span><span class="sxs-lookup"><span data-stu-id="c9aee-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="c9aee-108">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="c9aee-108">Create a new product</span></span>

1. <span data-ttu-id="c9aee-109">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> المنتجات حسب الفئة**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="c9aee-110">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c9aee-111">في القائمة المنسدلة **نوع المنتج**، حدد **الصنف** أو **الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="c9aee-112">في القائمة المنسدلة **النوع الفرعي للمنتج**، حدد **المنتج** (إذا كان المنتج لن يحتوي على أي متغيرات) أو **أصل المنتج** (إذا كان المنتج سيكون له متغيرات).</span><span class="sxs-lookup"><span data-stu-id="c9aee-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="c9aee-113">في المربع **رقم المنتج**، أدخل رقم المنتج إذا لم يكن قد تمت تعبئته بالفعل مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="c9aee-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="c9aee-114">في المربع **اسم المنتج**، أدخل اسم منتج.</span><span class="sxs-lookup"><span data-stu-id="c9aee-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="c9aee-115">في المربع **اسم البحث**، أدخل اسما للبحث.</span><span class="sxs-lookup"><span data-stu-id="c9aee-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="c9aee-116">في القائمة المنسدلة **فئة البيع بالتجزئة**، حدد الفئة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="c9aee-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="c9aee-117">إذا كان المنتج عبارة عن مجموعة، فحدد **نعم** لـ **مجموعة منتجات**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="c9aee-118">إذا كان النوع الفرعي للمنتج هو أصل المنتج، فعيِّن **‏‫مجموعة أبعاد المنتجات** لتضمين المتغيرات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="c9aee-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="c9aee-119">تتضمن الخيارات كل من **اللون** و **الحجم** و **النمط** و **التكوين**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="c9aee-120">قد تحتاج إلى إنشاء مجموعات أبعاد منتجات إضافية إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c9aee-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="c9aee-121">في القائمة المنسدلة **تقنية التكوين**، حدد الخيار المناسب.</span><span class="sxs-lookup"><span data-stu-id="c9aee-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="c9aee-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-122">Select **OK**.</span></span>

<span data-ttu-id="c9aee-123">تعرض الصورة التالية مثالاً لمنتج تمت إضافته.</span><span class="sxs-lookup"><span data-stu-id="c9aee-123">The following image shows an example product being added.</span></span>

![إنشاء منتج](media/create-new-product.png)

<span data-ttu-id="c9aee-125">بمجرد إضافة المنتج يمكن تعيين بيانات إضافية له، مثل **وصف المنتج** و **مجموعات المتغيرات** و **مجموعات الأبعاد** و **سمات المنتج** و **المنتجات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="c9aee-126">تعرض الصورة التالية تفاصيل المنتج الإضافية.</span><span class="sxs-lookup"><span data-stu-id="c9aee-126">The following image shows a product's additional details.</span></span>

![تفاصيل المنتج](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="c9aee-128">إنشاء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="c9aee-128">Create product variants</span></span>

<span data-ttu-id="c9aee-129">إذا كان النوع الفرعي للمنتج هو **أصل المنتج**، ستحتاج إلى إنشاء متغيرات معينة.</span><span class="sxs-lookup"><span data-stu-id="c9aee-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="c9aee-130">لإنشاء متغيرات منتج، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c9aee-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="c9aee-131">في جزء الإجراءات، حدد **متغيرات المنتج**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="c9aee-132">في حالة تحديد مجموعات المتغير في جزء الإجراءات، حدد \**‏‫اقتراحات المتغيرات‬*.</span><span class="sxs-lookup"><span data-stu-id="c9aee-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="c9aee-133">حدد المتغيرات التي تريد دعمها للمنتج.</span><span class="sxs-lookup"><span data-stu-id="c9aee-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="c9aee-134">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="c9aee-135">إصدار منتج</span><span class="sxs-lookup"><span data-stu-id="c9aee-135">Release a product</span></span>

<span data-ttu-id="c9aee-136">لبيع منتج، يجب إصداره أولاً إلى كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="c9aee-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="c9aee-137">من صفحة المنت ، حدد **إصدار المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-137">From the product page, select **Release products**.</span></span>

    ![إصدار المنتج](media/create-new-product-3.png)

1. <span data-ttu-id="c9aee-139">حدد المنتج الذي تريد إصداره، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-139">Select the product to release, and then select **Next**.</span></span>

    ![اختر منتجًا لإصداره](media/create-new-product-4.png)

1. <span data-ttu-id="c9aee-141">حدد مجموعة متغيرات المنتج الذي تريد إصداره، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![اختر متغيرات لإصدارها](media/create-new-product-5.png)

1. <span data-ttu-id="c9aee-143">حدد الكيان القانوني، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-143">Select the legal entity, and then select **Next**.</span></span>

    ![اختيار الكيان القانوني](media/create-new-product-6.png)

1. <span data-ttu-id="c9aee-145">حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-145">Select **Finish**.</span></span>

    ![إنهاء إصدار المنتج](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="c9aee-147">تكوين منتج تم إصداره</span><span class="sxs-lookup"><span data-stu-id="c9aee-147">Configure a released product</span></span>

<span data-ttu-id="c9aee-148">بمجرد إصدار المنتج، فإنه يتطلب تكوينًا إضافيًا يتضمن إضافة سعر إلى المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9aee-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="c9aee-149">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \>المنتجات التي تم إصدارها حسب الفئة**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="c9aee-150">حدد عقدة فئة المنتج للمنتج الذي تم إصداره، ثم حدد المنتج من قائمة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c9aee-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="c9aee-151">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="c9aee-152">في قسم **الشراء**، كوِّن أي خصائص مطلوبة بما في ذلك **الوحدة** و **السعر** و **الكمية**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="c9aee-153">في جزء الإجراءات، حدد **التحقق من الصحة** للتأكد من عدم الإبلاغ عن أي أخطاء بالحقول المفقودة.</span><span class="sxs-lookup"><span data-stu-id="c9aee-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="c9aee-154">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c9aee-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c9aee-155">تعرض الصورة التالية مثالاً لتكوين منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="c9aee-155">The following image shows an example configuration for a released product.</span></span>

![تكوين منتج تم إصداره](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="c9aee-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c9aee-157">Additional resources</span></span>

[<span data-ttu-id="c9aee-158">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="c9aee-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c9aee-159">إنشاء مجموعة متغير</span><span class="sxs-lookup"><span data-stu-id="c9aee-159">Create a variant group</span></span>](create-variant-group.md) 
