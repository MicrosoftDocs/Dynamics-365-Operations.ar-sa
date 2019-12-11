---
title: الوحدة النمطية الرئيسية
description: يغطي هذا الموضوع الوحدات النمطية الرئيسية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785366"
---
# <a name="hero-module"></a><span data-ttu-id="15046-103">الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="15046-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="15046-104">يغطي هذا الموضوع الوحدات النمطية الرئيسية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15046-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="15046-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="15046-105">Overview</span></span>

<span data-ttu-id="15046-106">تُستخدم الوحدة النمطية الرئيسية لتسويق المنتجات أو العروض الترويجية من خلال مجموعة من الصور والنصوص.</span><span class="sxs-lookup"><span data-stu-id="15046-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="15046-107">على سبيل المثال، يمكن لبائع التجزئة إضافة الوحدة النمطية الرئيسية إلى الصفحة الرئيسية لموقع التجارة الإلكترونية للترويج لمنتج جديد وجذب انتباه العملاء.</span><span class="sxs-lookup"><span data-stu-id="15046-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="15046-108">يتم التحكم في الوحدة النمطية الرئيسية بواسطة البيانات من نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="15046-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="15046-109">وهي وحدة نمطية منفصلة لا تعتمد على أي وحدات نمطية أخرى في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="15046-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="15046-110">ويمكن وضع الوحدة النمطية الرئيسية على أي صفحة ويب يرغب بائع التجزئة في التسويق أو الترويج لشيء ما عليها (على سبيل المثال، المنتجات أو المبيعات أو الميزات).</span><span class="sxs-lookup"><span data-stu-id="15046-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="15046-111">أمثلة على الوحدات النمطية الرئيسية في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="15046-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="15046-112">يمكن استخدام الوحدة النمطية الرئيسية في الصفحة الرئيسية لموقع التجارة الإلكترونية لتمييز العروض الترويجية والمنتجات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="15046-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="15046-113">يمكن استخدام الوحدة النمطية الرئيسية في صفحة تفاصيل المنتج لتفصيل معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="15046-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="15046-114">يمكن وضع الوحدة النمطية الرئيسية المتعددة داخل الوحدة النمطية الدوارة‬ لتمييز عدة منتجات أو عروض.</span><span class="sxs-lookup"><span data-stu-id="15046-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="15046-115">خصائص الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="15046-115">Hero module properties</span></span>

| <span data-ttu-id="15046-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="15046-116">Property name</span></span>  | <span data-ttu-id="15046-117">القيم</span><span class="sxs-lookup"><span data-stu-id="15046-117">Values</span></span> | <span data-ttu-id="15046-118">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="15046-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="15046-119">الصورة</span><span class="sxs-lookup"><span data-stu-id="15046-119">Image</span></span>          | <span data-ttu-id="15046-120">ملف الصورة</span><span class="sxs-lookup"><span data-stu-id="15046-120">Image file</span></span> | <span data-ttu-id="15046-121">يمكن استخدام صورة لعرض منتج أو عرض ترويجي.</span><span class="sxs-lookup"><span data-stu-id="15046-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="15046-122">يمكن تحميل صورة إلى معرض الصور، أو يمكن استخدام صوره موجودة.</span><span class="sxs-lookup"><span data-stu-id="15046-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="15046-123">العنوان</span><span class="sxs-lookup"><span data-stu-id="15046-123">Heading</span></span>        | <span data-ttu-id="15046-124">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="15046-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="15046-125">يمكن أن يكون لكل الوحدة النمطية الرئيسية عنوان.</span><span class="sxs-lookup"><span data-stu-id="15046-125">Every hero module can have a heading.</span></span> <span data-ttu-id="15046-126">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="15046-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="15046-127">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="15046-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="15046-128">فقرة</span><span class="sxs-lookup"><span data-stu-id="15046-128">Paragraph</span></span>      | <span data-ttu-id="15046-129">نص الفقرة</span><span class="sxs-lookup"><span data-stu-id="15046-129">Paragraph text</span></span> | <span data-ttu-id="15046-130">تدعم الوحدة النمطية الرئيسية نص الفقرة في تنسيق نصي منسق.</span><span class="sxs-lookup"><span data-stu-id="15046-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="15046-131">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل، والارتباطات التشعبية.</span><span class="sxs-lookup"><span data-stu-id="15046-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="15046-132">يمكن تجاوز بعض هذه القدرات بواسطة سمة الصفحة التي يتم تطبيقها على الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="15046-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="15046-133">الارتباط</span><span class="sxs-lookup"><span data-stu-id="15046-133">Link</span></span>           | <span data-ttu-id="15046-134">ارتباط النص وارتباط عنوان URL والتسمية الخاصة بتطبيقات الإنترنت الغنية القابلة للوصول (ARIA) و **الارتباط المفتوح في علامة التبويب الجديدة**</span><span class="sxs-lookup"><span data-stu-id="15046-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="15046-135">تدعم الوحدات النمطية الرئيسية واحد أو أكثر من ارتباطات "استدعاء إجراء".</span><span class="sxs-lookup"><span data-stu-id="15046-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="15046-136">إذا تمت إضافة ارتباط، فمن ثم يلزم وجود نص الارتباط وعنوان URL وتسمية ARIA.</span><span class="sxs-lookup"><span data-stu-id="15046-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="15046-137">يجب ان تكون تسميات ARIA وصفية لتلبية متطلبات إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="15046-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="15046-138">يمكن تكوين الارتباطات بحيث يتم فتحها في علامة تبويب جديدة.</span><span class="sxs-lookup"><span data-stu-id="15046-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="15046-139">موضع النص</span><span class="sxs-lookup"><span data-stu-id="15046-139">Text placement</span></span> | <span data-ttu-id="15046-140">**أعلي اليسار**، **أعلي اليمين**، **أعلي الوسط**، **أسفل اليسار**، **أسفل اليمين**، **توسيط لأسفل**، **توسيط لليسار**، **توسيط لليمين**، أو **توسيط في المنتصف**</span><span class="sxs-lookup"><span data-stu-id="15046-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="15046-141">تحدد هذه الخاصية موضع الصورة بالنسبة للنص.</span><span class="sxs-lookup"><span data-stu-id="15046-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="15046-142">علي سبيل المثال ، إذا تم تحديد **يمين** ، تظهر الصورة علي يمين النص.</span><span class="sxs-lookup"><span data-stu-id="15046-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="15046-143">نسق النص</span><span class="sxs-lookup"><span data-stu-id="15046-143">Text theme</span></span>     | <span data-ttu-id="15046-144">**فاتح** أو **داكن**</span><span class="sxs-lookup"><span data-stu-id="15046-144">**Light** or **Dark**</span></span> | <span data-ttu-id="15046-145">يمكن تحديد نظام الألوان للنص، استنادًا إلى صورة الخلفية.</span><span class="sxs-lookup"><span data-stu-id="15046-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="15046-146">على سبيل المثال، إذا كانت الصورة ذات خلفية داكنة، يمكن تطبيق سمة الضوء لجعل النص أكثر وضوحًا وتلبية نسب تباين الألوان لأغراض إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="15046-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="15046-147">تدرج</span><span class="sxs-lookup"><span data-stu-id="15046-147">Gradient</span></span>       | <span data-ttu-id="15046-148">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="15046-148">**True** or **False**</span></span> | <span data-ttu-id="15046-149">يمكن تطبيق التدرج اللوني على الصورة لتلبية نسب تباين الألوان لأغراض إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="15046-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="15046-150">إضافة الوحدة النمطية الرئيسية إلى صفحة جديدة</span><span class="sxs-lookup"><span data-stu-id="15046-150">Add a hero module to a new page</span></span>

<span data-ttu-id="15046-151">لإضافة الوحدة النمطية الرئيسية إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="15046-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="15046-152">انتقل إلى **القوالب**، وقم بإنشاء قالب صفحة يسمي **"قالب رئيسي**.</span><span class="sxs-lookup"><span data-stu-id="15046-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="15046-153">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة الوحدة النمطية الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="15046-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="15046-154">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="15046-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="15046-155">استخدم القالب الرئيسي الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **الصفحة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="15046-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="15046-156">في الصفحة الافتراضية، حدد فتحة **الرئيسية** ، وحدد زر علامة الحذف (**...**) ، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="15046-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="15046-157">في مربع الحوار **إضافة وحدة نمطية** ، ضمن **الوحدات النمطية**، حدد الوحدة النمطية الرئيسية، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="15046-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="15046-158">في شجرة المخطط التفصيلي على اليسار، حدد الوحدة النمطية الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="15046-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="15046-159">في جزء الخصائص الموجود على اليمين، حدد **إضافة صورة**.</span><span class="sxs-lookup"><span data-stu-id="15046-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="15046-160">ثم قم إما بتحديد صورة موجودة أو تحميل صوره جديدة.</span><span class="sxs-lookup"><span data-stu-id="15046-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="15046-161">حدد **‏‫العنوان‬**.</span><span class="sxs-lookup"><span data-stu-id="15046-161">Select **Heading**.</span></span>
1. <span data-ttu-id="15046-162">في مربع الحوار **العنوان** ، أضف نص العنوان، وحدد مستوي العنوان، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="15046-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="15046-163">تحت **نص منسق**، قم بإضافة النص على النحو الذي تُريده.</span><span class="sxs-lookup"><span data-stu-id="15046-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="15046-164">حدد **إضافة ارتباط إجراء**.</span><span class="sxs-lookup"><span data-stu-id="15046-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="15046-165">في مربع الحوار **ارتباط الإجراء** ، قم بإضافة نص الارتباط وعنوان URL للارتباط وتسمية ARIA للارتباط، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="15046-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="15046-166">قم بحفظ الصفحة، ومعاينة تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="15046-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="15046-167">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="15046-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15046-168">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="15046-168">Additional resources</span></span>

[<span data-ttu-id="15046-169">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="15046-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="15046-170">الوحدة النمطية للتنبيه</span><span class="sxs-lookup"><span data-stu-id="15046-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="15046-171">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="15046-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="15046-172">وحدة كتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="15046-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="15046-173">الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="15046-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="15046-174">الوحدة النمطية لميزة</span><span class="sxs-lookup"><span data-stu-id="15046-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="15046-175">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="15046-175">Video player module</span></span>](add-video-player.md)
