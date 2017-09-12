---
title: "كود nomenclature لأرقام وأسماء متغيرات المنتج"
description: "يصف هذا الموضوع كيف يمكنك إعداد nomenclature رقم المنتج لاستبدال التنسيق الثابت [رقم أصل المنتج - التكوين - الحجم - اللون - النمط]. يتميز كود nomenclature الجديد بتنسيق مستهدف يتضمن رقم أصل المنتج وأبعاد المنتج النشطة ومحددات النص التي تختارها. يمكنك أيضًا إنشاء كود nomenclature لأسماء المنتجات. أخيرًا، يمكنك إنشاء كود nomenclature لتحديد التكوينات التي يتم إنشاؤها بواسطة مكون منتج يستند إلى القيد. باستطاعة أكواد nomenclature هذه أن تحتوي على سمات تختارها أنت."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="cba52-107">كود nomenclature لأرقام وأسماء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="cba52-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="cba52-108">يصف هذا الموضوع كيف يمكنك إعداد nomenclature رقم المنتج لاستبدال التنسيق الثابت [رقم أصل المنتج - التكوين - الحجم - اللون - النمط].</span><span class="sxs-lookup"><span data-stu-id="cba52-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="cba52-109">يتميز كود nomenclature الجديد بتنسيق مستهدف يتضمن رقم أصل المنتج وأبعاد المنتج النشطة ومحددات النص التي تختارها.</span><span class="sxs-lookup"><span data-stu-id="cba52-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="cba52-110">يمكنك أيضًا إنشاء كود nomenclature لأسماء المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cba52-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="cba52-111">أخيرًا، يمكنك إنشاء كود nomenclature لتحديد التكوينات التي يتم إنشاؤها بواسطة مكون منتج يستند إلى القيد.</span><span class="sxs-lookup"><span data-stu-id="cba52-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="cba52-112">باستطاعة أكواد nomenclature هذه أن تحتوي على سمات تختارها أنت.</span><span class="sxs-lookup"><span data-stu-id="cba52-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="cba52-113">تسمح لك أكواد nomenclature الجديدة لأرقام متغيرات المنتجات وأسماء متغيرات المنتجات بتضمين أجزاء في معرفات متغيرات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cba52-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="cba52-114">بإمكان هذه الأجزاء أن تتضمن رقم واسم أصل المنتج ومعرفات وأسماء أبعاد المنتج والتسلسلات الرقمية‬ والثوابت النصية والسمات.</span><span class="sxs-lookup"><span data-stu-id="cba52-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="cba52-115">وتسمح لك هذه الوظيفة بالعثور بسرعة على متغير منتج معين عندما تنشئ أمر مبيعات أو أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="cba52-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="cba52-116">يمكنك إنشاء أكواد nomenclatures لكل من أرقام متغيرات المنتجات وأسماء متغيرات المنتجات باستخدام **كود nomenclature للمنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="cba52-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="cba52-117">لفتح هذ الصفحة، انقر فوق **إدارة معلومات المنتج** &gt; **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="cba52-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="cba52-118">كود nomenclature لمتغيرات منتج معرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="cba52-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="cba52-119">يتم إنشاء متغيرات المنتج لأصول المنتج وفقًا لإحدى تقنيات التكوين الثلاث:</span><span class="sxs-lookup"><span data-stu-id="cba52-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="cba52-120">المتغيرات المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="cba52-120">Predefined variants</span></span>
-   <span data-ttu-id="cba52-121">على أساس القيد</span><span class="sxs-lookup"><span data-stu-id="cba52-121">Constraint-based</span></span>
-   <span data-ttu-id="cba52-122">على أساس البُعد</span><span class="sxs-lookup"><span data-stu-id="cba52-122">Dimension-based</span></span>

<span data-ttu-id="cba52-123">يتضمن كل متغير منتج رقمًا واسمًا ويسمح لك كود nomenclature لتعريف متغير المنتج بتحديد الأجزاء التي سيتم تضمينها في كل رقم أو اسم متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="cba52-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="cba52-124">يمكنك تحديد الأجزاء التالية في صفحة **كود nomenclature للمنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="cba52-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="cba52-125">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="cba52-125">Product master number</span></span>
-   <span data-ttu-id="cba52-126">اسم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="cba52-126">Product master name</span></span>
-   <span data-ttu-id="cba52-127">قيمة التسلسل الرقمي</span><span class="sxs-lookup"><span data-stu-id="cba52-127">Number sequence value</span></span>
-   <span data-ttu-id="cba52-128">الثابت النصي</span><span class="sxs-lookup"><span data-stu-id="cba52-128">Text constant</span></span>
-   <span data-ttu-id="cba52-129">أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="cba52-129">Product dimensions</span></span>
    -   <span data-ttu-id="cba52-130">معرف أو اسم التكوين</span><span class="sxs-lookup"><span data-stu-id="cba52-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="cba52-131">معرف أو اسم اللون</span><span class="sxs-lookup"><span data-stu-id="cba52-131">Color ID or name</span></span>
    -   <span data-ttu-id="cba52-132">معرف أو اسم الحجم</span><span class="sxs-lookup"><span data-stu-id="cba52-132">Size ID or name</span></span>
    -   <span data-ttu-id="cba52-133">معرف أو اسم النمط</span><span class="sxs-lookup"><span data-stu-id="cba52-133">Style ID or name</span></span>

<span data-ttu-id="cba52-134">بعد تعريف كود nomenclature لرقم تعريف متغير المنتج، يمكن إقرانه بمجموعة أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cba52-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="cba52-135">سيتم عندئذٍ تعيين أرقام متغيرات المنتج لكافة أصول المنتجات التي ترجع إلى مجموعة أبعاد المنتجات هذه وفقًا لكود nomenclature.</span><span class="sxs-lookup"><span data-stu-id="cba52-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="cba52-136">ومع ذلك، لا يمكن إقران أكواد nomenclature لأسماء متغيرات المنتجات بمجموعات أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cba52-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="cba52-137">يمكنك أيضًا تعيين كود nomenclature لعريف متغير المنتج إلى أصل المنتج بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="cba52-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="cba52-138">في هذه الحالة، سوف يتم تعيين أرقام وأسماء متغيرات المنتجات لمتغيرات المنتجات التي تنتمي إلى أصل المنتج وفقًا لأكواد nomenclature.</span><span class="sxs-lookup"><span data-stu-id="cba52-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="cba52-139">مثال</span><span class="sxs-lookup"><span data-stu-id="cba52-139">Example</span></span>

<span data-ttu-id="cba52-140">يتم إنتاج قميص (TS1234) بثلاثة أحجام (صغير ومتوسط وكبير) وأربعه ألوان (أحمر، أخضر، أزرق، أصفر) ونمطين (بولو، V).</span><span class="sxs-lookup"><span data-stu-id="cba52-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="cba52-141">وبالتالي، يمكن الحصول على 24 من متغيرات المنتج (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="cba52-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="cba52-142">يمكنك إنشاء كود nomenclature لرقم متغير المنتج لديه الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="cba52-143">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="cba52-143">Product master number</span></span>
2.  <span data-ttu-id="cba52-144">الثابت النصي: "-"</span><span class="sxs-lookup"><span data-stu-id="cba52-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="cba52-145">اللون</span><span class="sxs-lookup"><span data-stu-id="cba52-145">Color</span></span>
4.  <span data-ttu-id="cba52-146">الثابت النصي: "-"</span><span class="sxs-lookup"><span data-stu-id="cba52-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="cba52-147">الحجم</span><span class="sxs-lookup"><span data-stu-id="cba52-147">Size</span></span>
6.  <span data-ttu-id="cba52-148">الثابت النصي: "-"</span><span class="sxs-lookup"><span data-stu-id="cba52-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="cba52-149">نمط</span><span class="sxs-lookup"><span data-stu-id="cba52-149">Style</span></span>

<span data-ttu-id="cba52-150">في هذه الحالة، سيكون رقم متغير المنتج للقميص الأحمر الصغير من نوع بولو: ، TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="cba52-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="cba52-151">كود nomenclature للتكوينات المستنِدة إلى قيد</span><span class="sxs-lookup"><span data-stu-id="cba52-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="cba52-152">‏‫بالنسبة إلى التكوينات المستندة إلى قيد، يمكنك إنشاء nomenclature مخصص لبُعد المنتج - التكوين‬.</span><span class="sxs-lookup"><span data-stu-id="cba52-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="cba52-153">يمكنك تحديد الأجزاء التالية في صفحة **كود nomenclature للمنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="cba52-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="cba52-154">قيمة التسلسل الرقمي</span><span class="sxs-lookup"><span data-stu-id="cba52-154">Number sequence value</span></span>
-   <span data-ttu-id="cba52-155">الثابت النصي</span><span class="sxs-lookup"><span data-stu-id="cba52-155">Text constant</span></span>
-   <span data-ttu-id="cba52-156">قيمة السمة</span><span class="sxs-lookup"><span data-stu-id="cba52-156">Attribute value</span></span>

<span data-ttu-id="cba52-157">بإمكان كل مكون في نموذج تكوين المنتج أن يكون له كود nomenclature للتكوين خاص به.</span><span class="sxs-lookup"><span data-stu-id="cba52-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="cba52-158">يمكن استخدام فقط السمات التي تنتمي إلى المكون.</span><span class="sxs-lookup"><span data-stu-id="cba52-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="cba52-159">ولا يمكن استخدام السمات من المكونات الفرعية أو متطلبات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="cba52-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="cba52-160">مثال</span><span class="sxs-lookup"><span data-stu-id="cba52-160">Example</span></span>

<span data-ttu-id="cba52-161">يتضمن نموذج تكوين المنتج مكون جذر مع سمتين:</span><span class="sxs-lookup"><span data-stu-id="cba52-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="cba52-162">المواد (البلاستيك الخشب والفولاذ)</span><span class="sxs-lookup"><span data-stu-id="cba52-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="cba52-163">الطول (10... 100)</span><span class="sxs-lookup"><span data-stu-id="cba52-163">Length (10...100)</span></span>

<span data-ttu-id="cba52-164">يمكنك إنشاء كود nomenclature للتكوين لديه الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="cba52-165">قيمة السمة: المواد</span><span class="sxs-lookup"><span data-stu-id="cba52-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="cba52-166">الثابت النصي: "AAA"</span><span class="sxs-lookup"><span data-stu-id="cba52-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="cba52-167">قيمة السمة: الطول</span><span class="sxs-lookup"><span data-stu-id="cba52-167">Attribute value: Length</span></span>

<span data-ttu-id="cba52-168">في هذه الحالة، سيكون WoodAAA78 معرف التكوين لمواد خشبية يبلغ طولها 78.</span><span class="sxs-lookup"><span data-stu-id="cba52-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="cba52-169">كود nomenclature للتكوينات المستندة إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="cba52-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="cba52-170">‏‫بالنسبة إلى التكوينات المستندة إلى بُعد، يمكنك إنشاء nomenclature مخصص لبُعد المنتج - التكوين‬.</span><span class="sxs-lookup"><span data-stu-id="cba52-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="cba52-171">يمكنك تحديد الأجزاء التالية في صفحة **كود nomenclature للمنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="cba52-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="cba52-172">قيمة التسلسل الرقمي</span><span class="sxs-lookup"><span data-stu-id="cba52-172">Number sequence value</span></span>
-   <span data-ttu-id="cba52-173">الثابت النصي</span><span class="sxs-lookup"><span data-stu-id="cba52-173">Text constant</span></span>
-   <span data-ttu-id="cba52-174">صنف مجموعة التكوين</span><span class="sxs-lookup"><span data-stu-id="cba52-174">Configuration group item</span></span>

<span data-ttu-id="cba52-175">يمكن تعريف كود nomenclature للتكوين لقائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="cba52-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="cba52-176">مثال</span><span class="sxs-lookup"><span data-stu-id="cba52-176">Example</span></span>

<span data-ttu-id="cba52-177">تتضمن قائمة مكونات صنف أربعة بنود لقائمة مكونات صنف مقسمة إلى مجموعتي تكوين:</span><span class="sxs-lookup"><span data-stu-id="cba52-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="cba52-178">بند قائمة مكونات الصنف: M0007, خزانة قياسية</span><span class="sxs-lookup"><span data-stu-id="cba52-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="cba52-179">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="cba52-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="cba52-180">بند قائمة مكونات الصنف: M0008، خزانة عالية الجودة</span><span class="sxs-lookup"><span data-stu-id="cba52-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="cba52-181">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="cba52-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="cba52-182">بند قائمة مكونات الصنف: M0021، قماشة الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="cba52-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="cba52-183">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="cba52-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="cba52-184">بند قائمة مكونات الصنف: M0022، معدن الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="cba52-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="cba52-185">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="cba52-185">Configuration group: Front grill</span></span>

<span data-ttu-id="cba52-186">يمكنك إنشاء كود nomenclature للتكوين لديه الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="cba52-187">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="cba52-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="cba52-188">الثابت النصي: "&"</span><span class="sxs-lookup"><span data-stu-id="cba52-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="cba52-189">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="cba52-189">Configuration group: Front grill</span></span>

<span data-ttu-id="cba52-190">في هذه الحالة، سيكون معرف التكوين لخزانة قياسية لديها قماشة شبكة أمامية: M0007&M0021</span><span class="sxs-lookup"><span data-stu-id="cba52-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="cba52-191">كود Nomenclature لمجموعة من متغيرات المنتج والتكوينات</span><span class="sxs-lookup"><span data-stu-id="cba52-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="cba52-192">عند استخدام تقنية التكوين المستند إلى قيد أو التكوين المستند إلى بُعد لتكوين متغيرات المنتج لأصل منتج، بإمكان أرقام متغيرات المنتج لمتغيرات المنتج أن تتضمن كود nomenclature من بُعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="cba52-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="cba52-193">اتبع الخطوات التالية لتكوين المتغيرات.</span><span class="sxs-lookup"><span data-stu-id="cba52-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="cba52-194">في صفحة **كود nomenclature للمنتج**، حدد كود nomenclature لرقم متغير المنتج يتضمن بُعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="cba52-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="cba52-195">عيّن كود nomenclature إلى مجموعة أبعاد المنتجات لديها بُعد التكوين.</span><span class="sxs-lookup"><span data-stu-id="cba52-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="cba52-196">حدد كود nomenclature للتكوين للمكونات أو قوائم مكونات الأصناف التي سيتم استخدامها لتكوين متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="cba52-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="cba52-197">يمكنك أيضًا إنشاء كود nomenclature لأسماء متغيرات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cba52-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="cba52-198">يمكن تكوين أسماء متغيرات المنتجات بحيث تتضمن اسم أو معرف التكوين.</span><span class="sxs-lookup"><span data-stu-id="cba52-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="cba52-199">مثال عن التكوينات المستندة إلى قيد</span><span class="sxs-lookup"><span data-stu-id="cba52-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="cba52-200">لهذا المثال، يمكنك استخدام كود nomenclature لرقم متغير منتج يتكون من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="cba52-201">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="cba52-201">Product master number</span></span>
2.  <span data-ttu-id="cba52-202">الثابت النصي "\_"</span><span class="sxs-lookup"><span data-stu-id="cba52-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="cba52-203">التكوين</span><span class="sxs-lookup"><span data-stu-id="cba52-203">Configuration</span></span>

<span data-ttu-id="cba52-204">يتكون كود nomenclature للتكوين من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="cba52-205">قيمة السمة: المواد</span><span class="sxs-lookup"><span data-stu-id="cba52-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="cba52-206">الثابت النصي: "AAA"</span><span class="sxs-lookup"><span data-stu-id="cba52-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="cba52-207">قيمة السمة: الطول</span><span class="sxs-lookup"><span data-stu-id="cba52-207">Attribute value: Length</span></span>

<span data-ttu-id="cba52-208">يمكنك إدخال القيم التالية للأجزاء:</span><span class="sxs-lookup"><span data-stu-id="cba52-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="cba52-209">رقم أصل المنتج = **M0099**</span><span class="sxs-lookup"><span data-stu-id="cba52-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="cba52-210">المواد = **البلاستيك**</span><span class="sxs-lookup"><span data-stu-id="cba52-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="cba52-211">الطول = **12**</span><span class="sxs-lookup"><span data-stu-id="cba52-211">Length = **12**</span></span>

<span data-ttu-id="cba52-212">في هذه الحالة، سيصبح رقم متغير المنتج M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="cba52-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="cba52-213">مثال عن التكوينات المستندة إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="cba52-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="cba52-214">لهذا المثال، يمكنك استخدام كود nomenclature لرقم متغير منتج يتكون من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="cba52-215">رقم أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="cba52-215">Product master number</span></span>
2.  <span data-ttu-id="cba52-216">الثابت النصي "//"</span><span class="sxs-lookup"><span data-stu-id="cba52-216">Text constant "//"</span></span>
3.  <span data-ttu-id="cba52-217">التكوين</span><span class="sxs-lookup"><span data-stu-id="cba52-217">Configuration</span></span>

<span data-ttu-id="cba52-218">يتكون كود nomenclature للتكوين من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="cba52-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="cba52-219">مجموعة التكوين: خزانة</span><span class="sxs-lookup"><span data-stu-id="cba52-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="cba52-220">الثابت النصي: "&"</span><span class="sxs-lookup"><span data-stu-id="cba52-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="cba52-221">مجموعة التكوين: الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="cba52-221">Configuration group: Front grill</span></span>

<span data-ttu-id="cba52-222">يمكنك إدخال القيم التالية للأجزاء:</span><span class="sxs-lookup"><span data-stu-id="cba52-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="cba52-223">رقم أصل المنتج = **D0123**</span><span class="sxs-lookup"><span data-stu-id="cba52-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="cba52-224">الخزانة = **M0008**</span><span class="sxs-lookup"><span data-stu-id="cba52-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="cba52-225">الشبكة الأمامية = **M0022**</span><span class="sxs-lookup"><span data-stu-id="cba52-225">Front grill = **M0022**</span></span>

<span data-ttu-id="cba52-226">في هذه الحالة، سيكون رقم متغير المنتج D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="cba52-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="cba52-227">تعارضات الترقيم</span><span class="sxs-lookup"><span data-stu-id="cba52-227">Numbering conflicts</span></span>
<span data-ttu-id="cba52-228">في بعض الحالات، قد لا ينتج كود nomenclature الذي تقوم بإعداده لرقم متغير المنتج أرقام متغيرات منتجات فريدة.</span><span class="sxs-lookup"><span data-stu-id="cba52-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="cba52-229">على سبيل المثال، لن تكون أرقام متغيرات المنتجات فريدة إذا لم يتم تضمين بُعد منتج نشط واحد في كود nomenclature لأصل منتج يستخدم تقنية تكوين المتغيرات المعرفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="cba52-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="cba52-230">تختلف طريقة تعاملك مع التعارضات، استنادًا إلى تقنية التكوين.</span><span class="sxs-lookup"><span data-stu-id="cba52-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="cba52-231">المتغيرات المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="cba52-231">Predefined variants</span></span>

<span data-ttu-id="cba52-232">سيحدث خطأ إذا حاولت أن تقوم يدويًا أو تلقائيًا بإنشاء متغيرات منتج، وينتهي واحد أو أكثر من متغيرات المنتج برقم متغير المنتج نفسه.</span><span class="sxs-lookup"><span data-stu-id="cba52-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="cba52-233">لتجنب حدوث هذا السيناريو، يجب استخدام كافة أبعاد المنتج نشطة في مجموعة أبعاد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cba52-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="cba52-234">أو، يمكنك تضمين تسلسل رقمي للمساعدة في ضمان أن تكون أرقام متغيرات المنتجات فريدة.</span><span class="sxs-lookup"><span data-stu-id="cba52-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="cba52-235">التكوينات المستندة إلى قيد</span><span class="sxs-lookup"><span data-stu-id="cba52-235">Constraint-based configurations</span></span>

<span data-ttu-id="cba52-236">تبعًا لكود nomenclature، قد يحاول النظام تعيين رقم متغير منتج غير فريد لأحد التكوينات.</span><span class="sxs-lookup"><span data-stu-id="cba52-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="cba52-237">في هذه الحالة، يستخدم النظام التسلسل الرقمي لبُعد التكوين كرقم متغير منتج بدلاً منه، وستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="cba52-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="cba52-238">لتجنب حدوث هذا السيناريو، يجب عليك تضمين سمات كافية في كود nomenclature للمساعدة في ضمان الحصول على أرقام متغيرات منتج فريدة.</span><span class="sxs-lookup"><span data-stu-id="cba52-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="cba52-239">يجب أيضًا أن تتأكد من تشغيل الخيار **إعادة استخدام** للمكون.</span><span class="sxs-lookup"><span data-stu-id="cba52-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="cba52-240">التكوينات المستنِد إلى بُعد</span><span class="sxs-lookup"><span data-stu-id="cba52-240">Dimension-based configurations</span></span>

<span data-ttu-id="cba52-241">خلال تنفيذ خطوة من عملية التكوين، يقترح النظام قيمة تكوين وفقًا لكود nomenclature.</span><span class="sxs-lookup"><span data-stu-id="cba52-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="cba52-242">في هذه الخطوة، يمكنك تغيير قيمة التكوين يدويًا.</span><span class="sxs-lookup"><span data-stu-id="cba52-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="cba52-243">عندما تحفظ التكوين، يتحقق النظام مما إذا كانت قيمة التكوين فريدة.</span><span class="sxs-lookup"><span data-stu-id="cba52-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="cba52-244">إذا لم تكن القيمة التي أدخلتها فريدة، فستتلقى رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="cba52-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="cba52-245">لحفظ التكوين، يجب إدخال قيمة تكوين فريدة.</span><span class="sxs-lookup"><span data-stu-id="cba52-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="cba52-246">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="cba52-246">See also</span></span>
--------

[<span data-ttu-id="cba52-247">إنشاء كود nomenclature لرقم المنتج لمتغيرات المنتج المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="cba52-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="cba52-248">إنشاء كود nomenclature لرقم المنتج لمتغيرات المنتج المكوّنة</span><span class="sxs-lookup"><span data-stu-id="cba52-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


