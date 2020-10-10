---
title: وحدة كتلة المحتوى
description: يتناول هذا الموضوع وحدات كتل المحتوى ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a8b1c214ba31b7c47cecbe67bef493f5fa450fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817344"
---
# <a name="content-block-module"></a><span data-ttu-id="cb392-103">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="cb392-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb392-104">يتناول هذا الموضوع وحدات كتل المحتوى ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb392-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb392-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="cb392-105">Overview</span></span>

<span data-ttu-id="cb392-106">تُستخدم وحدة كتبة المحتوى لتسويق المنتجات أو العروض الترويجية من خلال مجموعة من الصور والنصوص.</span><span class="sxs-lookup"><span data-stu-id="cb392-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="cb392-107">على سبيل المثال، يمكن لبائع التجزئة إضافة وحدة كتلة محتوى إلى الصفحة الرئيسية لموقع التجارة الإلكترونية للترويج لمنتج جديد وجذب انتباه العملاء.</span><span class="sxs-lookup"><span data-stu-id="cb392-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="cb392-108">يتم التحكم في وحدة كتلة المحتوى بواسطة البيانات من نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="cb392-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="cb392-109">وهي وحدة نمطية منفصلة لا تعتمد على أي وحدات نمطية أخرى في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cb392-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="cb392-110">ويمكن وضع وحدة كتلة المحتوى على أي صفحة ويب يرغب بائع التجزئة في التسويق أو الترويج لشيء ما عليها (على سبيل المثال، المنتجات أو المبيعات أو الميزات).</span><span class="sxs-lookup"><span data-stu-id="cb392-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="cb392-111">أمثلة عن وحدة كتلة المحتوى في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="cb392-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="cb392-112">يمكن استخدام وحدة كتلة المحتوى في الصفحة الرئيسية لموقع التجارة الإلكترونية لتمييز العروض الترويجية والمنتجات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="cb392-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="cb392-113">يمكن استخدام وحدة كتلة المحتوى في صفحة تفاصيل المنتج لتفصيل معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="cb392-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="cb392-114">يمكن وضع وحدات كتل محتوى متعددة داخل الوحدة النمطية الدوارة‬ لتمييز عدة منتجات أو عروض.</span><span class="sxs-lookup"><span data-stu-id="cb392-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="cb392-115">وحدات كتل المحتوى النمطية والنُسق</span><span class="sxs-lookup"><span data-stu-id="cb392-115">Content block modules and themes</span></span>

<span data-ttu-id="cb392-116">بإمكان وحدات كتل المحتوى أن تدعم تخطيطات وأنماط متنوعة بالاستناد إلى نسق.</span><span class="sxs-lookup"><span data-stu-id="cb392-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="cb392-117">على سبيل المثال، يدعم النسق Fabrikam ثلاثة أشكال مختلفة لتخطيط وحدة كتلة المحتوى: التخطيط الرئيسي والميزة والإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="cb392-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="cb392-118">يعرض التخطيط الرئيسي صورة على الخلفية مع تراكب نصي.</span><span class="sxs-lookup"><span data-stu-id="cb392-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="cb392-119">يعرض تخطيط الميزة صورة ونصًا جنبًا إلى جنب.</span><span class="sxs-lookup"><span data-stu-id="cb392-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="cb392-120">يسمح تخطيط الإطار المتجانب بكتل محتوى متعددة في تنسيق إطار متجانب.</span><span class="sxs-lookup"><span data-stu-id="cb392-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="cb392-121">علاوةً على ذلك، بإمكان النسق عرض خصائص مختلفة لكل تخطيط.</span><span class="sxs-lookup"><span data-stu-id="cb392-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="cb392-122">بإمكان مطور النسق إنشاء المزيد من التخطيطات باستخدام مزيد من الأنماط باستخدام وحدة كتلة المحتوى.</span><span class="sxs-lookup"><span data-stu-id="cb392-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="cb392-123">تعرض الصورة التالية مثالاً لوحدة كتلة المحتوى مع تخطيط رئيسي.</span><span class="sxs-lookup"><span data-stu-id="cb392-123">The following image shows an example of a content block module with a hero layout.</span></span>

![مثال لوحدة نمطية لجزء رئيسي](./media/Hero.PNG)

<span data-ttu-id="cb392-125">تعرض الصورة التالية مثالاً لوحدة كتلة المحتوى مع تخطيط ميزة.</span><span class="sxs-lookup"><span data-stu-id="cb392-125">The following image shows an example of a content block module with a feature layout.</span></span>

![أمثلةللوحدات النمطية لميزة](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="cb392-127">خصائص وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="cb392-127">Content block module properties</span></span>

| <span data-ttu-id="cb392-128">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="cb392-128">Property name</span></span>  | <span data-ttu-id="cb392-129">القيم</span><span class="sxs-lookup"><span data-stu-id="cb392-129">Values</span></span> | <span data-ttu-id="cb392-130">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cb392-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="cb392-131">الصورة</span><span class="sxs-lookup"><span data-stu-id="cb392-131">Image</span></span>          | <span data-ttu-id="cb392-132">ملف الصورة</span><span class="sxs-lookup"><span data-stu-id="cb392-132">Image file</span></span> | <span data-ttu-id="cb392-133">يمكن استخدام صورة لعرض منتج أو عرض ترويجي.</span><span class="sxs-lookup"><span data-stu-id="cb392-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="cb392-134">يمكن تحميل صورة إلى معرض الصور، أو يمكن استخدام صوره موجودة.</span><span class="sxs-lookup"><span data-stu-id="cb392-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="cb392-135">العنوان</span><span class="sxs-lookup"><span data-stu-id="cb392-135">Heading</span></span>        | <span data-ttu-id="cb392-136">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="cb392-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="cb392-137">يمكن أن يكون لكل الوحدة النمطية الرئيسية عنوان.</span><span class="sxs-lookup"><span data-stu-id="cb392-137">Every hero module can have a heading.</span></span> <span data-ttu-id="cb392-138">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="cb392-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="cb392-139">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="cb392-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="cb392-140">فقرة</span><span class="sxs-lookup"><span data-stu-id="cb392-140">Paragraph</span></span>      | <span data-ttu-id="cb392-141">نص الفقرة</span><span class="sxs-lookup"><span data-stu-id="cb392-141">Paragraph text</span></span> | <span data-ttu-id="cb392-142">تدعم الوحدة النمطية الرئيسية نص الفقرة في تنسيق نصي منسق.</span><span class="sxs-lookup"><span data-stu-id="cb392-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="cb392-143">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل، والارتباطات التشعبية.</span><span class="sxs-lookup"><span data-stu-id="cb392-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="cb392-144">يمكن تجاوز بعض هذه القدرات بواسطة سمة الصفحة التي يتم تطبيقها على الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="cb392-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="cb392-145">الارتباط</span><span class="sxs-lookup"><span data-stu-id="cb392-145">Link</span></span>           | <span data-ttu-id="cb392-146">ارتباط النص وارتباط عنوان URL والتسمية الخاصة بتطبيقات الإنترنت الغنية القابلة للوصول (ARIA) و **الارتباط المفتوح في علامة التبويب الجديدة**</span><span class="sxs-lookup"><span data-stu-id="cb392-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="cb392-147">تدعم الوحدات النمطية الرئيسية واحد أو أكثر من ارتباطات "استدعاء إجراء".</span><span class="sxs-lookup"><span data-stu-id="cb392-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="cb392-148">إذا تمت إضافة ارتباط، فمن ثم يلزم وجود نص الارتباط وعنوان URL وتسمية ARIA.</span><span class="sxs-lookup"><span data-stu-id="cb392-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="cb392-149">يجب ان تكون تسميات ARIA وصفية لتلبية متطلبات إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="cb392-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="cb392-150">يمكن تكوين الارتباطات بحيث يتم فتحها في علامة تبويب جديدة.</span><span class="sxs-lookup"><span data-stu-id="cb392-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="cb392-151">خصائص وحدة كتلة المحتوى المعروضة بواسطة نسق Fabrikam</span><span class="sxs-lookup"><span data-stu-id="cb392-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="cb392-152">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="cb392-152">Property name</span></span>  | <span data-ttu-id="cb392-153">القيم</span><span class="sxs-lookup"><span data-stu-id="cb392-153">Values</span></span> | <span data-ttu-id="cb392-154">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cb392-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="cb392-155">موضع النص</span><span class="sxs-lookup"><span data-stu-id="cb392-155">Text placement</span></span> | <span data-ttu-id="cb392-156">**يسار**، **يمين**، **وسط**</span><span class="sxs-lookup"><span data-stu-id="cb392-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="cb392-157">تحدد هذه الخاصية موضع النص على الصورة.</span><span class="sxs-lookup"><span data-stu-id="cb392-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="cb392-158">وتنطبق فقط على التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="cb392-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="cb392-159">نسق النص</span><span class="sxs-lookup"><span data-stu-id="cb392-159">Text theme</span></span>     | <span data-ttu-id="cb392-160">**فاتح** أو **داكن**</span><span class="sxs-lookup"><span data-stu-id="cb392-160">**Light** or **Dark**</span></span> | <span data-ttu-id="cb392-161">يمكن تحديد نظام الألوان للنص، استنادًا إلى صورة الخلفية.</span><span class="sxs-lookup"><span data-stu-id="cb392-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="cb392-162">على سبيل المثال، إذا كانت الصورة ذات خلفية داكنة، يمكن تطبيق سمة الضوء لجعل النص أكثر وضوحًا وتلبية نسب تباين الألوان لأغراض إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="cb392-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="cb392-163">وتنطبق فقط على التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="cb392-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="cb392-164">موضع الصورة</span><span class="sxs-lookup"><span data-stu-id="cb392-164">Image placement</span></span>       | <span data-ttu-id="cb392-165">**يسار**، **يمين**</span><span class="sxs-lookup"><span data-stu-id="cb392-165">**Left**,  **Right**</span></span> | <span data-ttu-id="cb392-166">تحدد هذه الخاصية ما إذا كان يجب وضع الصورة إلى يسار النص أو يمينه.</span><span class="sxs-lookup"><span data-stu-id="cb392-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="cb392-167">وتنطبق فقط على تخطيط الميزة.</span><span class="sxs-lookup"><span data-stu-id="cb392-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="cb392-168">إضافة وحدة كتلة محتوى إلى صفحة جديدة</span><span class="sxs-lookup"><span data-stu-id="cb392-168">Add a content block module to a new page</span></span>

<span data-ttu-id="cb392-169">لإضافة الوحدة النمطية الرئيسية إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cb392-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cb392-170">اذهب إلى **القوالب**، وقم بإنشاء قالب صفحة يسمى **قالب كتلة المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="cb392-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="cb392-171">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة الوحدة النمطية الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="cb392-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="cb392-172">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="cb392-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="cb392-173">استخدم القالب الرئيسي الذي أنشأته للتو لإنشاء صفحة تسمى **صفحة كتلة المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="cb392-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="cb392-174">في الصفحة الافتراضية، حدد فتحة **الرئيسية** ، وحدد زر علامة الحذف (**...**) ، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="cb392-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb392-175">في مربع الحوار **إضافة وحدة نمطية** ، ضمن **الوحدات النمطية**، حدد الوحدة النمطية الرئيسية، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb392-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="cb392-176">في شجرة المخطط التفصيلي على اليسار، حدد وحدة كتلة المحتوى.</span><span class="sxs-lookup"><span data-stu-id="cb392-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="cb392-177">في جزء الخصائص الموجود على اليمين، حدد **إضافة صورة**.</span><span class="sxs-lookup"><span data-stu-id="cb392-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="cb392-178">ثم قم إما بتحديد صورة موجودة أو تحميل صوره جديدة.</span><span class="sxs-lookup"><span data-stu-id="cb392-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="cb392-179">حدد **‏‫العنوان‬**.</span><span class="sxs-lookup"><span data-stu-id="cb392-179">Select **Heading**.</span></span>
1. <span data-ttu-id="cb392-180">في مربع الحوار **العنوان** ، أضف نص العنوان، وحدد مستوي العنوان، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb392-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="cb392-181">تحت **نص منسق**، قم بإضافة النص على النحو الذي تُريده.</span><span class="sxs-lookup"><span data-stu-id="cb392-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="cb392-182">حدد **إضافة ارتباط**.</span><span class="sxs-lookup"><span data-stu-id="cb392-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="cb392-183">في مربع الحوار **ارتباط**، أضف نص الارتباط وعنوان URL للارتباط وتسمية ARIA للارتباط، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb392-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="cb392-184">حدد التخطيط **الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="cb392-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="cb392-185">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cb392-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="cb392-186">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="cb392-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="cb392-187">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb392-187">Additional resources</span></span>

[<span data-ttu-id="cb392-188">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="cb392-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cb392-189">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="cb392-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="cb392-190">وحدة دوارة</span><span class="sxs-lookup"><span data-stu-id="cb392-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="cb392-191">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="cb392-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="cb392-192">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="cb392-192">Video player module</span></span>](add-video-player.md)
