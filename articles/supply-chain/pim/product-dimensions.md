---
title: "أبعاد المنتجات"
description: "هناك أربعة أبعاد للمنتج - اللون والتكوين والحجم والنمط. يمكنك دمج أبعاد المنتج في مجموعات أبعاد، وتعيين مجموعات الأبعاد إلى أصول المنتج. تحدد مجموعات أبعاد المنتجات كيفية تعريف متغيرات المنتج."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ccb9d47bf6f081dbcc9590bddd4516cf7385ec23
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="product-dimensions"></a><span data-ttu-id="5f282-105">أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="5f282-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="5f282-106">هناك أربعة أبعاد للمنتج - اللون والتكوين والحجم والنمط.</span><span class="sxs-lookup"><span data-stu-id="5f282-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="5f282-107">يمكنك دمج أبعاد المنتج في مجموعات أبعاد، وتعيين مجموعات الأبعاد إلى أصول المنتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="5f282-108">تحدد مجموعات أبعاد المنتجات كيفية تعريف متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="5f282-109">أبعاد المنتج هي الخصائص التي تفيد في تحديد متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="5f282-110">يمكنك استخدام مجموعات أبعاد المنتج لتحديد متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="5f282-111">يجب عليك تحديد بُعد منتج واحد على الأقل لأصل منتج لإنشاء متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="5f282-112">متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="5f282-112">Product variants</span></span>
----------------

<span data-ttu-id="5f282-113">تتم الإشارة إلى متغيرات المنتج كذلك على أنها أصناف.</span><span class="sxs-lookup"><span data-stu-id="5f282-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="5f282-114">الصنف هو منتج ملموس، ليس كالخدمة.</span><span class="sxs-lookup"><span data-stu-id="5f282-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="5f282-115">ومن الممكن أيضًا تحديد أصل منتج مع نوع الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="5f282-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="5f282-116">ومن خلال استخدام نوع الخدمة، يمكنك تحديد متغيرات المنتج التي تتضمن خدمات.</span><span class="sxs-lookup"><span data-stu-id="5f282-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="5f282-117">على سبيل المثال، يمكنك تحديد أصل منتج للخدمات الاستشارية ومتغيرات المنتج للعمل الذي يتم تنفيذه من قبل كبار المستشارين والمستشارين المبتدئين.</span><span class="sxs-lookup"><span data-stu-id="5f282-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="5f282-118">أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="5f282-118">Product dimensions</span></span>
<span data-ttu-id="5f282-119">‏‫تتوفر أبعاد المنتج التالية: اللون والتكوين والحجم والنمط.</span><span class="sxs-lookup"><span data-stu-id="5f282-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="5f282-120">ويمكن إنشاء متغير منتج استناداً إلى قيم الأبعاد الخاصة بالمنتج.‬</span><span class="sxs-lookup"><span data-stu-id="5f282-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="5f282-121">يمكن إنشاء قيم أبعاد المنتج، مثل الحجم واللون والنمط، في صفحات **الحجم**، و**اللون**، و**النمط**، التي يمكن الوصول إليها من المواقع التالية: **إدارة معلومات المنتج** &gt; **إعداد‏‎** &gt; **مجموعات الأبعاد والمتغيرات** &gt; **أحجام/ألوان/أنماط**.</span><span class="sxs-lookup"><span data-stu-id="5f282-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="5f282-122">يتم إنشاء قيم أبعاد المنتج لبُعد التكوين عادةً من خلال استخدام مكون المنتج أو المكون المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="5f282-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="5f282-123">كما يمكن إنشاء أبعاد المنتج والاحتفاظ بها في صفحة **أبعاد المنتج**، التي يمكن الوصول إليها من المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="5f282-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="5f282-124">‏‫انتقل إلى **إدارة معلومات المنتج** &gt; **المنتجات** &gt; **أصول المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="5f282-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="5f282-125">في **جزء الإجراءات**، انقر فوق **أبعاد المنتج**.</span><span class="sxs-lookup"><span data-stu-id="5f282-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="5f282-126">‏‫انقر فوق **إدارة معلومات المنتج** &gt; **المنتجات** &gt; **جميع المنتجات وأصول المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="5f282-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="5f282-127">قم بتحديد أصل منتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-127">Select a product master.</span></span> <span data-ttu-id="5f282-128">في **جزء الإجراءات**، انقر فوق **أبعاد المنتج**.</span><span class="sxs-lookup"><span data-stu-id="5f282-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="5f282-129">انقر فوق **‎إدارة معلومات المنتج** &gt; **‎المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="5f282-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="5f282-130">قم بتحديد أصل منتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-130">Select a product master.</span></span> <span data-ttu-id="5f282-131">في **جزء الإجراءات**، انقر فوق **المنتج**.</span><span class="sxs-lookup"><span data-stu-id="5f282-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="5f282-132">في مجموعة **أصل المنتج**، انقر فوق **أبعاد المنتج**.</span><span class="sxs-lookup"><span data-stu-id="5f282-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="5f282-133">يقتصر عدد المتغيرات التي يمكن إنشاؤها لصنف على عدد مجموعات أبعاد المنتج المحتملة.</span><span class="sxs-lookup"><span data-stu-id="5f282-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="5f282-134">**تلميح**</span><span class="sxs-lookup"><span data-stu-id="5f282-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f282-135">على سبيل المثال، عند استخدام منتج على سطر أمر، حدد أبعاد المنتج لتحديد متغير المنتج الذي تريد العمل به.</span><span class="sxs-lookup"><span data-stu-id="5f282-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="5f282-136">مثال</span><span class="sxs-lookup"><span data-stu-id="5f282-136">Example</span></span>
<span data-ttu-id="5f282-137">تبيع إحدى الشركات الجينز.</span><span class="sxs-lookup"><span data-stu-id="5f282-137">A company sells denim jeans.</span></span> <span data-ttu-id="5f282-138">ويستخدم الصنف ـ الجينز ـ أبعاد اللون والمقاس للمنتج.</span><span class="sxs-lookup"><span data-stu-id="5f282-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="5f282-139">ويتم بيعه بثلاثة ألوان مختلفة وستة مقاسات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="5f282-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="5f282-140">الألوان: أزرق، وأسود، وبني الأحجام: XS،S،M،L، XL، XXL لا تتوفر كافة الأحجام بجميع الألوان الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="5f282-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="5f282-141">إذا كانت جميع المجموعات متوفرة، فسينتج عنها 18 نوعًا مختلفًا من الجينز.</span><span class="sxs-lookup"><span data-stu-id="5f282-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="5f282-142">في هذا المثال، يتم إنتاج مجموعات متغيرات المنتج التسعة التالية فقط.</span><span class="sxs-lookup"><span data-stu-id="5f282-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="5f282-143">اللون</span><span class="sxs-lookup"><span data-stu-id="5f282-143">Color</span></span> | <span data-ttu-id="5f282-144">الحجم</span><span class="sxs-lookup"><span data-stu-id="5f282-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="5f282-145">أزرق</span><span class="sxs-lookup"><span data-stu-id="5f282-145">Blue</span></span>  | <span data-ttu-id="5f282-146">صغير جدًا</span><span class="sxs-lookup"><span data-stu-id="5f282-146">XS</span></span>   |
| <span data-ttu-id="5f282-147">أزرق</span><span class="sxs-lookup"><span data-stu-id="5f282-147">Blue</span></span>  | <span data-ttu-id="5f282-148">ق</span><span class="sxs-lookup"><span data-stu-id="5f282-148">S</span></span>    |
| <span data-ttu-id="5f282-149">أزرق</span><span class="sxs-lookup"><span data-stu-id="5f282-149">Blue</span></span>  | <span data-ttu-id="5f282-150">م</span><span class="sxs-lookup"><span data-stu-id="5f282-150">M</span></span>    |
| <span data-ttu-id="5f282-151">أسود</span><span class="sxs-lookup"><span data-stu-id="5f282-151">Black</span></span> | <span data-ttu-id="5f282-152">م</span><span class="sxs-lookup"><span data-stu-id="5f282-152">M</span></span>    |
| <span data-ttu-id="5f282-153">أسود</span><span class="sxs-lookup"><span data-stu-id="5f282-153">Black</span></span> | <span data-ttu-id="5f282-154">ل</span><span class="sxs-lookup"><span data-stu-id="5f282-154">L</span></span>    |
| <span data-ttu-id="5f282-155">أسود</span><span class="sxs-lookup"><span data-stu-id="5f282-155">Black</span></span> | <span data-ttu-id="5f282-156">كبير جدًا</span><span class="sxs-lookup"><span data-stu-id="5f282-156">XL</span></span>   |
| <span data-ttu-id="5f282-157">بني</span><span class="sxs-lookup"><span data-stu-id="5f282-157">Brown</span></span> | <span data-ttu-id="5f282-158">ل</span><span class="sxs-lookup"><span data-stu-id="5f282-158">L</span></span>    |
| <span data-ttu-id="5f282-159">بني</span><span class="sxs-lookup"><span data-stu-id="5f282-159">Brown</span></span> | <span data-ttu-id="5f282-160">كبير جدًا</span><span class="sxs-lookup"><span data-stu-id="5f282-160">XL</span></span>   |
| <span data-ttu-id="5f282-161">بني</span><span class="sxs-lookup"><span data-stu-id="5f282-161">Brown</span></span> | <span data-ttu-id="5f282-162">كبير جدًا جدًا</span><span class="sxs-lookup"><span data-stu-id="5f282-162">XXL</span></span>  |






