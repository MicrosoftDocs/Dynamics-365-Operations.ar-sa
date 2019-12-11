---
title: الوحدة النمطية لميزة
description: يتناول هذا الموضوع الوحدات النمطية لميزة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785273"
---
# <a name="feature-module"></a><span data-ttu-id="97bbe-103">الوحدة النمطية لميزة</span><span class="sxs-lookup"><span data-stu-id="97bbe-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="97bbe-104">يتناول هذا الموضوع الوحدات النمطية لميزة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97bbe-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97bbe-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="97bbe-105">Overview</span></span>

<span data-ttu-id="97bbe-106">تستخدم الوحدة لميزة في تسويق المنتجات أو العروض من خلال مجموعة من الصور والنصوص.</span><span class="sxs-lookup"><span data-stu-id="97bbe-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="97bbe-107">على سبيل المثال، يُمكن لبائع التجزئة إضافة الوحدة النمطية لميزة إلى صفحة تفاصيل منتج لتمييز ميزات المنتج.</span><span class="sxs-lookup"><span data-stu-id="97bbe-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="97bbe-108">يتم التحكم في الوحدة النمطية لميزة بواسطة البيانات من نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="97bbe-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="97bbe-109">وهي وحدة نمطية منفصلة لا تعتمد على أي وحدات نمطية أخرى في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="97bbe-110">ويمكن وضع وحدة نمطية لمزية على أي صفحة ويب يرغب بائع التجزئة في التسويق أو الترويج لشيء ما عليها (على سبيل المثال، المنتجات أو المبيعات أو الميزات).</span><span class="sxs-lookup"><span data-stu-id="97bbe-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="97bbe-111">أمثلة على وحدات الميزة النمطية في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="97bbe-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="97bbe-112">يُمكن استخدام الوحدة النمطية لميزة في الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="97bbe-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="97bbe-113">صفحة تفاصيل المنتج، لإظهار ميزات المنتج.</span><span class="sxs-lookup"><span data-stu-id="97bbe-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="97bbe-114">الصفحة الرئيسية، للعرض الترويجي للمنتجات</span><span class="sxs-lookup"><span data-stu-id="97bbe-114">The home page, to promote products</span></span>
- <span data-ttu-id="97bbe-115">صفحه الفئة، لتمييز فئة من المنتجات</span><span class="sxs-lookup"><span data-stu-id="97bbe-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="97bbe-116">خصائص ‏‫الوحدة النمطية للميزات‬</span><span class="sxs-lookup"><span data-stu-id="97bbe-116">Feature module properties</span></span>

| <span data-ttu-id="97bbe-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="97bbe-117">Property name</span></span>     | <span data-ttu-id="97bbe-118">القيم</span><span class="sxs-lookup"><span data-stu-id="97bbe-118">Values</span></span> | <span data-ttu-id="97bbe-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="97bbe-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="97bbe-120">الصورة</span><span class="sxs-lookup"><span data-stu-id="97bbe-120">Image</span></span>             | <span data-ttu-id="97bbe-121">ملف الصورة</span><span class="sxs-lookup"><span data-stu-id="97bbe-121">Image file</span></span> | <span data-ttu-id="97bbe-122">يمكن استخدام صورة لتسويق المنتج أو العرض الترويجي.</span><span class="sxs-lookup"><span data-stu-id="97bbe-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="97bbe-123">يمكن تحميل صورة إلى معرض الصور، أو يمكن استخدام صوره موجودة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="97bbe-124">العنوان</span><span class="sxs-lookup"><span data-stu-id="97bbe-124">Heading</span></span>           | <span data-ttu-id="97bbe-125">نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="97bbe-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="97bbe-126">يمكن ان يكون لكل الوحدة النمطية لميزة عنوان.</span><span class="sxs-lookup"><span data-stu-id="97bbe-126">Every feature module can have a heading.</span></span> <span data-ttu-id="97bbe-127">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان.</span><span class="sxs-lookup"><span data-stu-id="97bbe-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="97bbe-128">ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="97bbe-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="97bbe-129">فقرة</span><span class="sxs-lookup"><span data-stu-id="97bbe-129">Paragraph</span></span>         | <span data-ttu-id="97bbe-130">نص الفقرة</span><span class="sxs-lookup"><span data-stu-id="97bbe-130">Paragraph text</span></span> | <span data-ttu-id="97bbe-131">تدعم الوحدات النمطية للميزة نص الفقرة في تنسيق نص منسق.</span><span class="sxs-lookup"><span data-stu-id="97bbe-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="97bbe-132">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل، والارتباطات التشعبية.</span><span class="sxs-lookup"><span data-stu-id="97bbe-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="97bbe-133">يمكن تجاوز بعض هذه القدرات بواسطة سمة الصفحة التي يتم تطبيقها على الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="97bbe-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="97bbe-134">الارتباط</span><span class="sxs-lookup"><span data-stu-id="97bbe-134">Link</span></span>              | <span data-ttu-id="97bbe-135">ارتباط النص وارتباط عنوان URL والتسمية الخاصة بتطبيقات الإنترنت الغنية القابلة للوصول (ARIA) و **الارتباط المفتوح في علامة التبويب الجديدة**</span><span class="sxs-lookup"><span data-stu-id="97bbe-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="97bbe-136">تدعم الوحدات النمطية للميزات واحد أو أكثر من ارتباطات "استدعاء إجراء".</span><span class="sxs-lookup"><span data-stu-id="97bbe-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="97bbe-137">إذا تمت إضافة ارتباط، فمن ثم يلزم وجود نص الارتباط وعنوان URL وتسمية ARIA.</span><span class="sxs-lookup"><span data-stu-id="97bbe-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="97bbe-138">يجب ان تكون تسميات ARIA وصفية لتلبية متطلبات إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="97bbe-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="97bbe-139">يمكن تكوين الارتباطات بحيث يتم فتحها في علامة تبويب جديدة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="97bbe-140">موضع الصورة</span><span class="sxs-lookup"><span data-stu-id="97bbe-140">Image placement</span></span>   | <span data-ttu-id="97bbe-141">**يمين**، **يسار**، **أعلى**، أو **أسفل**</span><span class="sxs-lookup"><span data-stu-id="97bbe-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="97bbe-142">تحدد هذه الخاصية موضع الصورة بالنسبة للنص.</span><span class="sxs-lookup"><span data-stu-id="97bbe-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="97bbe-143">علي سبيل المثال ، إذا تم تحديد **يمين** ، تظهر الصورة علي يمين النص.</span><span class="sxs-lookup"><span data-stu-id="97bbe-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="97bbe-144">حجم عمود الصورة</span><span class="sxs-lookup"><span data-stu-id="97bbe-144">Image column size</span></span> | <span data-ttu-id="97bbe-145">قيمة من **1** إلى **12**</span><span class="sxs-lookup"><span data-stu-id="97bbe-145">A value from **1** through **12**</span></span> | <span data-ttu-id="97bbe-146">تحدد هذه الخاصية حجم الصورة بالنسبة للنص.</span><span class="sxs-lookup"><span data-stu-id="97bbe-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="97bbe-147">يتم التعبير عن الحجم كعدد من الأعمدة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="97bbe-148">هناك 12 عمودًا في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-148">There are 12 columns on a page.</span></span> <span data-ttu-id="97bbe-149">بشكل افتراضي، يكون للصورة والنص حجم متساوي (ستة أعمدة لكلاً منهما).</span><span class="sxs-lookup"><span data-stu-id="97bbe-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="97bbe-150">ومع ذلك، يمكنك تعديل الحجم كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="97bbe-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="97bbe-151">إضافة الوحدة النمطية لميزة إلى صفحة جديدة</span><span class="sxs-lookup"><span data-stu-id="97bbe-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="97bbe-152">لإضافة الوحدة النمطية للميزة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="97bbe-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="97bbe-153">انتقل إلى **القوالب**، وقم بإنشاء قالب صفحة يسمي **"قالب ميزة**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="97bbe-154">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة الوحدة النمطية لميزة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="97bbe-155">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="97bbe-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="97bbe-156">استخدم قالب ميزة الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة ميزة**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="97bbe-157">في الصفحة الافتراضية، حدد فتحة **الرئيسية** ، وحدد زر علامة الحذف (**...**) ، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97bbe-158">في مربع الحوار **إضافة وحدة نمطية** ، ضمن **الوحدات النمطية**، حدد الوحدة النمطية لميزة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="97bbe-159">في شجرة المخطط التفصيلي على اليسار، حدد الوحدة النمطية لميزة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="97bbe-160">في جزء الخصائص الموجود على اليمين، حدد **إضافة صورة**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="97bbe-161">ثم قم إما بتحديد صورة موجودة أو تحميل صوره جديدة.</span><span class="sxs-lookup"><span data-stu-id="97bbe-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="97bbe-162">حدد **‏‫العنوان‬**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-162">Select **Heading**.</span></span>
1. <span data-ttu-id="97bbe-163">في مربع الحوار **العنوان** ، أضف نص العنوان، وحدد مستوي العنوان، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="97bbe-164">تحت **نص منسق**، قم بإضافة النص على النحو الذي تُريده.</span><span class="sxs-lookup"><span data-stu-id="97bbe-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="97bbe-165">حدد **إضافة ارتباط إجراء**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="97bbe-166">في مربع الحوار **ارتباط الإجراء** ، قم بإضافة نص الارتباط وعنوان URL للارتباط وتسمية ARIA للارتباط، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="97bbe-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="97bbe-167">قم بحفظ الصفحة، ومعاينة تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="97bbe-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="97bbe-168">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="97bbe-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97bbe-169">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="97bbe-169">Additional resources</span></span>

[<span data-ttu-id="97bbe-170">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="97bbe-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="97bbe-171">الوحدة النمطية للتنبيه</span><span class="sxs-lookup"><span data-stu-id="97bbe-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="97bbe-172">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="97bbe-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="97bbe-173">وحدة كتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="97bbe-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="97bbe-174">الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="97bbe-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="97bbe-175">الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="97bbe-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="97bbe-176">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="97bbe-176">Video player module</span></span>](add-video-player.md)
