---
title: كود nomenclature لأرقام وأسماء متغيرات المنتج
description: يصف هذا الموضوع كيف يمكنك إعداد nomenclature رقم المنتج لاستبدال التنسيق الثابت [رقم أصل المنتج - التكوين - الحجم - اللون - النمط].
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f17f9e1401c68c11e23f327d96028663470b3245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011312"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="ac76b-103">كود nomenclature لأرقام وأسماء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="ac76b-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac76b-104">يصف هذا الموضوع كيف يمكنك إعداد nomenclature رقم المنتج لاستبدال التنسيق الثابت [رقم أصل المنتج - التكوين - الحجم - اللون - النمط].</span><span class="sxs-lookup"><span data-stu-id="ac76b-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="ac76b-105">يتميز كود nomenclature الجديد بتنسيق مستهدف يتضمن رقم أصل المنتج وأبعاد المنتج النشطة ومحددات النص التي تختارها.</span><span class="sxs-lookup"><span data-stu-id="ac76b-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="ac76b-106">يمكنك أيضًا إنشاء كود nomenclature لأسماء المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="ac76b-107">أخيرًا، يمكنك إنشاء كود nomenclature لتحديد التكوينات التي يتم إنشاؤها بواسطة مكون منتج يستند إلى القيد.</span><span class="sxs-lookup"><span data-stu-id="ac76b-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="ac76b-108">باستطاعة أكواد nomenclature هذه أن تحتوي على سمات تختارها أنت.</span><span class="sxs-lookup"><span data-stu-id="ac76b-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="ac76b-109">تسمح لك أكواد nomenclature الجديدة لأرقام متغيرات المنتجات وأسماء متغيرات المنتجات بتضمين أجزاء في معرفات متغيرات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="ac76b-110">بإمكان هذه الأجزاء أن تتضمن رقم واسم أصل المنتج ومعرفات وأسماء أبعاد المنتج والتسلسلات الرقمية‬ والثوابت النصية والسمات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="ac76b-111">وتسمح لك هذه الوظيفة بالعثور بسرعة على متغير منتج معين عندما تنشئ أمر مبيعات أو أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="ac76b-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="ac76b-112">يمكنك إنشاء أكواد nomenclatures لكل من أرقام متغيرات المنتجات وأسماء متغيرات المنتجات باستخدام **كود nomenclature للمنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="ac76b-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="ac76b-113">لفتح هذ الصفحة، انقر فوق **إدارة معلومات المنتج** &gt; **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="ac76b-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="ac76b-114">كود nomenclature لمتغيرات منتج معرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="ac76b-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="ac76b-115">يتم إنشاء متغيرات المنتج لأصول المنتج وفقًا لإحدى تقنيات التكوين الثلاث:</span><span class="sxs-lookup"><span data-stu-id="ac76b-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="ac76b-116">المتغيرات المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="ac76b-116">Predefined variants</span></span>
-   <span data-ttu-id="ac76b-117">على أساس القيد</span><span class="sxs-lookup"><span data-stu-id="ac76b-117">Constraint-based</span></span>
-   <span data-ttu-id="ac76b-118">على أساس البُعد</span><span class="sxs-lookup"><span data-stu-id="ac76b-118">Dimension-based</span></span>

<span data-ttu-id="ac76b-119">يتضمن كل متغير منتج رقمًا واسمًا ويسمح لك كود nomenclature لتعريف متغير المنتج بتحديد الأجزاء التي سيتم تضمينها في كل رقم أو اسم متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="ac76b-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="ac76b-120">يمكنك تحديد الأجزاء التالية في صفحة **كود nomenclature للمنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="ac76b-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ac76b-121">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="ac76b-121">Product master number</span></span>
-   <span data-ttu-id="ac76b-122">اسم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="ac76b-122">Product master name</span></span>
-   <span data-ttu-id="ac76b-123">قيمة التسلسل الرقمي</span><span class="sxs-lookup"><span data-stu-id="ac76b-123">Number sequence value</span></span>
-   <span data-ttu-id="ac76b-124">الثابت النصي</span><span class="sxs-lookup"><span data-stu-id="ac76b-124">Text constant</span></span>
-   <span data-ttu-id="ac76b-125">أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="ac76b-125">Product dimensions</span></span>
    -   <span data-ttu-id="ac76b-126">معرف أو اسم التكوين</span><span class="sxs-lookup"><span data-stu-id="ac76b-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="ac76b-127">معرف أو اسم اللون</span><span class="sxs-lookup"><span data-stu-id="ac76b-127">Color ID or name</span></span>
    -   <span data-ttu-id="ac76b-128">معرف أو اسم الحجم</span><span class="sxs-lookup"><span data-stu-id="ac76b-128">Size ID or name</span></span>
    -   <span data-ttu-id="ac76b-129">معرف أو اسم النمط</span><span class="sxs-lookup"><span data-stu-id="ac76b-129">Style ID or name</span></span>

<span data-ttu-id="ac76b-130">بعد تعريف كود nomenclature لرقم تعريف متغير المنتج، يمكن إقرانه بمجموعة أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="ac76b-131">سيتم عندئذٍ تعيين أرقام متغيرات المنتج لكافة أصول المنتجات التي ترجع إلى مجموعة أبعاد المنتجات هذه وفقًا لكود nomenclature.</span><span class="sxs-lookup"><span data-stu-id="ac76b-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="ac76b-132">ومع ذلك، لا يمكن إقران أكواد nomenclature لأسماء متغيرات المنتجات بمجموعات أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="ac76b-133">يمكنك أيضًا تعيين كود nomenclature لعريف متغير المنتج إلى أصل المنتج بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="ac76b-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="ac76b-134">في هذه الحالة، سوف يتم تعيين أرقام وأسماء متغيرات المنتجات لمتغيرات المنتجات التي تنتمي إلى أصل المنتج وفقًا لأكواد nomenclature.</span><span class="sxs-lookup"><span data-stu-id="ac76b-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="ac76b-135">مثال</span><span class="sxs-lookup"><span data-stu-id="ac76b-135">Example</span></span>

<span data-ttu-id="ac76b-136">يتم إنتاج قميص (TS1234) بثلاثة أحجام (صغير ومتوسط وكبير) وأربعه ألوان (أحمر، أخضر، أزرق، أصفر) ونمطين (بولو، V).</span><span class="sxs-lookup"><span data-stu-id="ac76b-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="ac76b-137">وبالتالي، يمكن الحصول على 24 من متغيرات المنتج (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="ac76b-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="ac76b-138">يمكنك إنشاء كود nomenclature لرقم متغير المنتج لديه الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ac76b-139">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="ac76b-139">Product master number</span></span>
2.  <span data-ttu-id="ac76b-140">الثابت النصي: "-"</span><span class="sxs-lookup"><span data-stu-id="ac76b-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="ac76b-141">اللون</span><span class="sxs-lookup"><span data-stu-id="ac76b-141">Color</span></span>
4.  <span data-ttu-id="ac76b-142">الثابت النصي: "-"</span><span class="sxs-lookup"><span data-stu-id="ac76b-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="ac76b-143">الحجم</span><span class="sxs-lookup"><span data-stu-id="ac76b-143">Size</span></span>
6.  <span data-ttu-id="ac76b-144">الثابت النصي: "-"</span><span class="sxs-lookup"><span data-stu-id="ac76b-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="ac76b-145">نمط</span><span class="sxs-lookup"><span data-stu-id="ac76b-145">Style</span></span>

<span data-ttu-id="ac76b-146">في هذه الحالة، سيكون رقم متغير المنتج للقميص الأحمر الصغير من نوع بولو: ، TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="ac76b-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="ac76b-147">كود nomenclature للتكوينات المستنِد إلى قيد</span><span class="sxs-lookup"><span data-stu-id="ac76b-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="ac76b-148">‏‫بالنسبة إلى التكوينات المستندة إلى قيد، يمكنك إنشاء nomenclature مخصص لبُعد المنتج - التكوين‬.</span><span class="sxs-lookup"><span data-stu-id="ac76b-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="ac76b-149">يمكنك تحديد الأجزاء التالية في صفحة **كود nomenclature للمنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="ac76b-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ac76b-150">قيمة التسلسل الرقمي</span><span class="sxs-lookup"><span data-stu-id="ac76b-150">Number sequence value</span></span>
-   <span data-ttu-id="ac76b-151">الثابت النصي</span><span class="sxs-lookup"><span data-stu-id="ac76b-151">Text constant</span></span>
-   <span data-ttu-id="ac76b-152">قيمة السمة</span><span class="sxs-lookup"><span data-stu-id="ac76b-152">Attribute value</span></span>

<span data-ttu-id="ac76b-153">بإمكان كل مكون في نموذج تكوين المنتج أن يكون له كود nomenclature للتكوين خاص به.</span><span class="sxs-lookup"><span data-stu-id="ac76b-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="ac76b-154">يمكن استخدام فقط السمات التي تنتمي إلى المكون.</span><span class="sxs-lookup"><span data-stu-id="ac76b-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="ac76b-155">ولا يمكن استخدام السمات من المكونات الفرعية أو متطلبات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="ac76b-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="ac76b-156">مثال</span><span class="sxs-lookup"><span data-stu-id="ac76b-156">Example</span></span>

<span data-ttu-id="ac76b-157">يتضمن نموذج تكوين المنتج مكون جذر مع سمتين:</span><span class="sxs-lookup"><span data-stu-id="ac76b-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="ac76b-158">المواد (البلاستيك الخشب والفولاذ)</span><span class="sxs-lookup"><span data-stu-id="ac76b-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="ac76b-159">الطول (10... 100)</span><span class="sxs-lookup"><span data-stu-id="ac76b-159">Length (10...100)</span></span>

<span data-ttu-id="ac76b-160">يمكنك إنشاء كود nomenclature للتكوين لديه الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ac76b-161">قيمة السمة: المواد</span><span class="sxs-lookup"><span data-stu-id="ac76b-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="ac76b-162">الثابت النصي: "AAA"</span><span class="sxs-lookup"><span data-stu-id="ac76b-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="ac76b-163">قيمة السمة: الطول</span><span class="sxs-lookup"><span data-stu-id="ac76b-163">Attribute value: Length</span></span>

<span data-ttu-id="ac76b-164">في هذه الحالة، سيكون WoodAAA78 معرف التكوين لمواد خشبية يبلغ طولها 78.</span><span class="sxs-lookup"><span data-stu-id="ac76b-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="ac76b-165">كود nomenclature للتكوينات المستندة إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="ac76b-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="ac76b-166">‏‫بالنسبة إلى التكوينات المستندة إلى بُعد، يمكنك إنشاء nomenclature مخصص لبُعد المنتج - التكوين‬.</span><span class="sxs-lookup"><span data-stu-id="ac76b-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="ac76b-167">يمكنك تحديد الأجزاء التالية في صفحة **كود nomenclature للمنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="ac76b-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ac76b-168">قيمة التسلسل الرقمي</span><span class="sxs-lookup"><span data-stu-id="ac76b-168">Number sequence value</span></span>
-   <span data-ttu-id="ac76b-169">الثابت النصي</span><span class="sxs-lookup"><span data-stu-id="ac76b-169">Text constant</span></span>
-   <span data-ttu-id="ac76b-170">صنف مجموعة التكوين</span><span class="sxs-lookup"><span data-stu-id="ac76b-170">Configuration group item</span></span>

<span data-ttu-id="ac76b-171">يمكن تعريف كود nomenclature للتكوين لقائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="ac76b-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="ac76b-172">مثال</span><span class="sxs-lookup"><span data-stu-id="ac76b-172">Example</span></span>

<span data-ttu-id="ac76b-173">تتضمن قائمة مكونات صنف أربعة بنود لقائمة مكونات صنف مقسمة إلى مجموعتي تكوين:</span><span class="sxs-lookup"><span data-stu-id="ac76b-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="ac76b-174">بند قائمة مكونات الصنف: M0007, خزانة قياسية</span><span class="sxs-lookup"><span data-stu-id="ac76b-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="ac76b-175">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="ac76b-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="ac76b-176">بند قائمة مكونات الصنف: M0008، خزانة عالية الجودة</span><span class="sxs-lookup"><span data-stu-id="ac76b-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="ac76b-177">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="ac76b-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="ac76b-178">بند قائمة مكونات الصنف: M0021، قماشة الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="ac76b-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="ac76b-179">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="ac76b-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="ac76b-180">بند قائمة مكونات الصنف: M0022، معدن الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="ac76b-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="ac76b-181">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="ac76b-181">Configuration group: Front grill</span></span>

<span data-ttu-id="ac76b-182">يمكنك إنشاء كود nomenclature للتكوين لديه الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ac76b-183">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="ac76b-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="ac76b-184">الثابت النصي: "&"</span><span class="sxs-lookup"><span data-stu-id="ac76b-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="ac76b-185">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="ac76b-185">Configuration group: Front grill</span></span>

<span data-ttu-id="ac76b-186">في هذه الحالة، سيكون معرف التكوين لخزانة قياسية لديها قماشة شبكة أمامية: M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="ac76b-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="ac76b-187">كود Nomenclature لمجموعة من متغيرات المنتج والتكوينات</span><span class="sxs-lookup"><span data-stu-id="ac76b-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="ac76b-188">عند استخدام تقنية التكوين المستند إلى قيد أو التكوين المستند إلى بُعد لتكوين متغيرات المنتج لأصل منتج، بإمكان أرقام متغيرات المنتج لمتغيرات المنتج أن تتضمن كود nomenclature من بُعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="ac76b-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="ac76b-189">اتبع الخطوات التالية لتكوين المتغيرات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="ac76b-190">في صفحة **كود nomenclature للمنتج**، حدد كود nomenclature لرقم متغير المنتج يتضمن بُعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="ac76b-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="ac76b-191">عيّن كود nomenclature إلى مجموعة أبعاد المنتجات لديها بُعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="ac76b-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="ac76b-192">حدد كود nomenclature للتكوين للمكونات أو قوائم مكونات الأصناف التي سيتم استخدامها لتكوين متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="ac76b-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="ac76b-193">يمكنك أيضًا إنشاء كود nomenclature لأسماء متغيرات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="ac76b-194">يمكن تكوين أسماء متغيرات المنتجات بحيث تتضمن اسم أو معرف التكوين.</span><span class="sxs-lookup"><span data-stu-id="ac76b-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="ac76b-195">مثال عن التكوينات المستندة إلى قيد</span><span class="sxs-lookup"><span data-stu-id="ac76b-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="ac76b-196">لهذا المثال، يمكنك استخدام كود nomenclature لرقم متغير منتج يتكون من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="ac76b-197">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="ac76b-197">Product master number</span></span>
2.  <span data-ttu-id="ac76b-198">الثابت النصي "\_"</span><span class="sxs-lookup"><span data-stu-id="ac76b-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="ac76b-199">التكوين</span><span class="sxs-lookup"><span data-stu-id="ac76b-199">Configuration</span></span>

<span data-ttu-id="ac76b-200">يتكون كود nomenclature للتكوين من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="ac76b-201">قيمة السمة: المواد</span><span class="sxs-lookup"><span data-stu-id="ac76b-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="ac76b-202">الثابت النصي: "AAA"</span><span class="sxs-lookup"><span data-stu-id="ac76b-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="ac76b-203">قيمة السمة: الطول</span><span class="sxs-lookup"><span data-stu-id="ac76b-203">Attribute value: Length</span></span>

<span data-ttu-id="ac76b-204">يمكنك إدخال القيم التالية للأجزاء:</span><span class="sxs-lookup"><span data-stu-id="ac76b-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="ac76b-205">رقم أصل المنتج = **M0099**</span><span class="sxs-lookup"><span data-stu-id="ac76b-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="ac76b-206">المواد = **البلاستيك**</span><span class="sxs-lookup"><span data-stu-id="ac76b-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="ac76b-207">الطول = **12**</span><span class="sxs-lookup"><span data-stu-id="ac76b-207">Length = **12**</span></span>

<span data-ttu-id="ac76b-208">في هذه الحالة، سيصبح رقم متغير المنتج M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="ac76b-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="ac76b-209">مثال عن التكوينات المستندة إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="ac76b-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="ac76b-210">لهذا المثال، يمكنك استخدام كود nomenclature لرقم متغير منتج يتكون من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="ac76b-211">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="ac76b-211">Product master number</span></span>
2.  <span data-ttu-id="ac76b-212">الثابت النصي "//"</span><span class="sxs-lookup"><span data-stu-id="ac76b-212">Text constant "//"</span></span>
3.  <span data-ttu-id="ac76b-213">التكوين</span><span class="sxs-lookup"><span data-stu-id="ac76b-213">Configuration</span></span>

<span data-ttu-id="ac76b-214">يتكون كود nomenclature للتكوين من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="ac76b-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="ac76b-215">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="ac76b-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="ac76b-216">الثابت النصي: "&"</span><span class="sxs-lookup"><span data-stu-id="ac76b-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="ac76b-217">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="ac76b-217">Configuration group: Front grill</span></span>

<span data-ttu-id="ac76b-218">يمكنك إدخال القيم التالية للأجزاء:</span><span class="sxs-lookup"><span data-stu-id="ac76b-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="ac76b-219">رقم أصل المنتج = **D0123**</span><span class="sxs-lookup"><span data-stu-id="ac76b-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="ac76b-220">الخزانة = **M0008**</span><span class="sxs-lookup"><span data-stu-id="ac76b-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="ac76b-221">الشبكة الأمامية = **M0022**</span><span class="sxs-lookup"><span data-stu-id="ac76b-221">Front grill = **M0022**</span></span>

<span data-ttu-id="ac76b-222">في هذه الحالة، سيكون رقم متغير المنتج D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="ac76b-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="ac76b-223">تعارضات الترقيم</span><span class="sxs-lookup"><span data-stu-id="ac76b-223">Numbering conflicts</span></span>
<span data-ttu-id="ac76b-224">في بعض الحالات، قد لا ينتج كود nomenclature الذي تقوم بإعداده لرقم متغير المنتج أرقام متغيرات منتجات فريدة.</span><span class="sxs-lookup"><span data-stu-id="ac76b-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="ac76b-225">على سبيل المثال، لن تكون أرقام متغيرات المنتجات فريدة إذا لم يتم تضمين بُعد منتج نشط واحد في كود nomenclature لأصل منتج يستخدم تقنية تكوين المتغيرات المعرفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="ac76b-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="ac76b-226">تختلف طريقة تعاملك مع التعارضات، استنادًا إلى تقنية التكوين.</span><span class="sxs-lookup"><span data-stu-id="ac76b-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="ac76b-227">المتغيرات المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="ac76b-227">Predefined variants</span></span>

<span data-ttu-id="ac76b-228">سيحدث خطأ إذا حاولت أن تقوم يدويًا أو تلقائيًا بإنشاء متغيرات منتج، وينتهي واحد أو أكثر من متغيرات المنتج برقم متغير المنتج نفسه.</span><span class="sxs-lookup"><span data-stu-id="ac76b-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="ac76b-229">لتجنب حدوث هذا السيناريو، يجب استخدام كافة أبعاد المنتج نشطة في مجموعة أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="ac76b-230">أو، يمكنك تضمين تسلسل رقمي للمساعدة في ضمان أن تكون أرقام متغيرات المنتجات فريدة.</span><span class="sxs-lookup"><span data-stu-id="ac76b-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="ac76b-231">التكوينات المستندة إلى قيد</span><span class="sxs-lookup"><span data-stu-id="ac76b-231">Constraint-based configurations</span></span>

<span data-ttu-id="ac76b-232">تبعًا لكود nomenclature، قد يحاول النظام تعيين رقم متغير منتج غير فريد لأحد التكوينات.</span><span class="sxs-lookup"><span data-stu-id="ac76b-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="ac76b-233">في هذه الحالة، يستخدم النظام التسلسل الرقمي لبُعد التكوين كرقم متغير منتج بدلاً منه، وستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="ac76b-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="ac76b-234">لتجنب حدوث هذا السيناريو، يجب عليك تضمين سمات كافية في كود nomenclature للمساعدة في ضمان الحصول على أرقام متغيرات منتج فريدة.</span><span class="sxs-lookup"><span data-stu-id="ac76b-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="ac76b-235">يجب أيضًا أن تتأكد من تشغيل الخيار **إعادة استخدام** للمكون.</span><span class="sxs-lookup"><span data-stu-id="ac76b-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="ac76b-236">التكوينات المستنِد إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="ac76b-236">Dimension-based configurations</span></span>

<span data-ttu-id="ac76b-237">خلال تنفيذ خطوة من عملية التكوين، يقترح النظام قيمة تكوين وفقًا لكود nomenclature.</span><span class="sxs-lookup"><span data-stu-id="ac76b-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="ac76b-238">في هذه الخطوة، يمكنك تغيير قيمة التكوين يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ac76b-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="ac76b-239">عندما تحفظ التكوين، يتحقق النظام مما إذا كانت قيمة التكوين فريدة.</span><span class="sxs-lookup"><span data-stu-id="ac76b-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="ac76b-240">إذا لم تكن القيمة التي أدخلتها فريدة، فستتلقى رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="ac76b-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="ac76b-241">لحفظ التكوين، يجب إدخال قيمة تكوين فريدة.</span><span class="sxs-lookup"><span data-stu-id="ac76b-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ac76b-242">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ac76b-242">Additional resources</span></span>
--------

[<span data-ttu-id="ac76b-243">إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="ac76b-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="ac76b-244">إنشاء كود nomenclature لرقم المنتج لمتغيرات المنتج المكوّنة</span><span class="sxs-lookup"><span data-stu-id="ac76b-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

