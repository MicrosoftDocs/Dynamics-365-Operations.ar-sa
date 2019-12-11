---
title: الوحدة النمطية لوضع المحتوى
description: يتناول هذا الموضوع الوحدة النمطية لوضع المحتوى والوحدة النمطية لعناصر وضع المحتوى، ويصف كيفية إضافتهم إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785282"
---
# <a name="content-placement-module"></a><span data-ttu-id="6abf1-103">الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="6abf1-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6abf1-104">يتناول هذا الموضوع الوحدة النمطية لوضع المحتوى والوحدة النمطية لعناصر وضع المحتوى، ويصف كيفية إضافتهم إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6abf1-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6abf1-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6abf1-105">Overview</span></span>

<span data-ttu-id="6abf1-106">تُمثل الوحدة النمطية لوضع المحتوى حاوية خاصة يُمكن وضع الوحدات النمطية الأخرى داخلها في تخطيط مُعين.</span><span class="sxs-lookup"><span data-stu-id="6abf1-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="6abf1-107">تعدم الوحدات النمطية لوضع المحتوى الأنواع التالية من الوحدات النمطية مثل الوحدات النمطية الفرعية: عنصر وضع المحتوى وعنصر رسالة ترحيب الحساب وعنصر أمر الحساب وعنصر قائمة الأمنيات في الحساب وعنصر ملف تعريف الحساب.</span><span class="sxs-lookup"><span data-stu-id="6abf1-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="6abf1-108">وتُشتق الوحدات النمطية لوضع المحتوى البيانات من الوحدات النمطية التابعة التي تدعمها.</span><span class="sxs-lookup"><span data-stu-id="6abf1-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="6abf1-109">وبالتالي، يُمكن استخدام الوحدات النمطية لوضع المحتوى بطرق متعددة، استنادًا إلى الوحدات النمطية التي تتم إضافتها إليها.</span><span class="sxs-lookup"><span data-stu-id="6abf1-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="6abf1-110">تستخدم الوحدات النمطية لعناصر وضع المحتوى كل من الصور والنص لإظهار العروض والسياسات وميزات المنتج.</span><span class="sxs-lookup"><span data-stu-id="6abf1-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="6abf1-111">على سبيل المثال، يُمكن استخدام الوحدة النمطية لعنصر وضع المحتوى في الصفحة الرئيسية لإظهار سياسات المتجر أو معلومات الشحن.</span><span class="sxs-lookup"><span data-stu-id="6abf1-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="6abf1-112">يتم التحكم في الوحدات النمطية لعناصر وضع المحتوى من خلال البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="6abf1-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="6abf1-113">ولكن، يُمكن استخدامها فقط داخل الوحدة النمطية لوضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="6abf1-114">أمثلة على الوحدات النمطية لوضع المحتوى في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6abf1-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="6abf1-115">يُمكن استخدام الوحدات النمطية لوضع المحتوى التي تحتوي على الوحدات النمطية لعناصر وضع المحتوى في صفحة رئيسية أو صفحات تسويق لعرض ميزات المنتج والعروض وسياسات المتجر ومعلومات الشحن والمعلومات الأخرى من خلال الصور والنص.</span><span class="sxs-lookup"><span data-stu-id="6abf1-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="6abf1-116">يُمكن استخدام الوحدات النمطية لوضع المحتوى التي تحتوي على وحدات نمطية لعناصر وضع المحتوى في صفحات تفاصيل المنتج لإظهار ميزات المنتج.</span><span class="sxs-lookup"><span data-stu-id="6abf1-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="6abf1-117">يُمكن استخدام الوحدات النمطية لوضع المحتوى التي تحتوي على عنصر رسالة ترحيب الحساب أو الوحدات النمطية لعناصر أمر الحساب في صفحات إدارة الحساب.</span><span class="sxs-lookup"><span data-stu-id="6abf1-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="6abf1-118">خصائص الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="6abf1-118">Content placement module properties</span></span>

| <span data-ttu-id="6abf1-119">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="6abf1-119">Property name</span></span> | <span data-ttu-id="6abf1-120">القيمة</span><span class="sxs-lookup"><span data-stu-id="6abf1-120">Value</span></span> | <span data-ttu-id="6abf1-121">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="6abf1-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="6abf1-122">العرض</span><span class="sxs-lookup"><span data-stu-id="6abf1-122">Width</span></span>         | <span data-ttu-id="6abf1-123">**ملائمة الحاوية** أو **ملء الشاشة**</span><span class="sxs-lookup"><span data-stu-id="6abf1-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="6abf1-124">إذا تم تعيين القيمة إلى **ملائمة الحاوية**، فمن ثم تقتصر العناصر داخل الوحدة النمطية لوضع المحتوى على عرض الوحدة النمطية لوضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="6abf1-125">إذا لم تعيين القيمة إلى **ملء الشاشة**، فلن تقتصر العناصر على عرض الوحدة النمطية لوضع المحتوى ولكن يُمكنها الانتقال إلى وضع ملء الشاشة.</span><span class="sxs-lookup"><span data-stu-id="6abf1-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="6abf1-126">خصائص الوحدة النمطية لعنصر وضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="6abf1-126">Content placement item module properties</span></span>

| <span data-ttu-id="6abf1-127">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="6abf1-127">Property name</span></span> | <span data-ttu-id="6abf1-128">القيمة</span><span class="sxs-lookup"><span data-stu-id="6abf1-128">Value</span></span> | <span data-ttu-id="6abf1-129">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="6abf1-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="6abf1-130">العنوان</span><span class="sxs-lookup"><span data-stu-id="6abf1-130">Heading</span></span>       | <span data-ttu-id="6abf1-131">نص العنوان وعلامات العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**)</span><span class="sxs-lookup"><span data-stu-id="6abf1-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="6abf1-132">يُمكن أن يكون لكل وحدة نمطية لعنصر وضع المحتوى عنوانًا.</span><span class="sxs-lookup"><span data-stu-id="6abf1-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="6abf1-133">تدعم خاصية **العنوان** علامات العنوان.</span><span class="sxs-lookup"><span data-stu-id="6abf1-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="6abf1-134">وبشكل افتراضي، يتم استخدام علامة العنوان **H2** ، ولكن يُمكن تغيير علامة العنوان لتتوافق مع متطلبات الوصول.</span><span class="sxs-lookup"><span data-stu-id="6abf1-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="6abf1-135">فقرة</span><span class="sxs-lookup"><span data-stu-id="6abf1-135">Paragraph</span></span>     | <span data-ttu-id="6abf1-136">نص الفقرة</span><span class="sxs-lookup"><span data-stu-id="6abf1-136">Paragraph text</span></span> | <span data-ttu-id="6abf1-137">تدعم الوحدات النمطية لعناصر وضع المحتوى نص الفقرة في تنسيق نص منسق.</span><span class="sxs-lookup"><span data-stu-id="6abf1-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="6abf1-138">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل، والارتباطات التشعبية.</span><span class="sxs-lookup"><span data-stu-id="6abf1-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="6abf1-139">يمكن تجاوز بعض هذه القدرات بواسطة سمة الصفحة التي يتم تطبيقها على الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="6abf1-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="6abf1-140">الصورة</span><span class="sxs-lookup"><span data-stu-id="6abf1-140">Image</span></span>         | <span data-ttu-id="6abf1-141">ملف الصورة</span><span class="sxs-lookup"><span data-stu-id="6abf1-141">Image file</span></span> | <span data-ttu-id="6abf1-142">ويُمكن ربط الصورة بالنص.</span><span class="sxs-lookup"><span data-stu-id="6abf1-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="6abf1-143">الارتباط</span><span class="sxs-lookup"><span data-stu-id="6abf1-143">Link</span></span>          | <span data-ttu-id="6abf1-144">اربط عنوان URL ونص الارتباط</span><span class="sxs-lookup"><span data-stu-id="6abf1-144">Link URL and link text</span></span> | <span data-ttu-id="6abf1-145">يُمكن إضافة ارتباط إلى النص لإعادة توجيه المستخدمين إلى صفحة مُحددة.</span><span class="sxs-lookup"><span data-stu-id="6abf1-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="6abf1-146">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="6abf1-146">Tile size</span></span>     | <span data-ttu-id="6abf1-147">رقم من **1** إلى **12**</span><span class="sxs-lookup"><span data-stu-id="6abf1-147">A number from **1** through **12**</span></span> | <span data-ttu-id="6abf1-148">بالنسبة لكل عنصر وضع محتوى، تُحدد هذه الخاصية عدد الفتحات الذي يجب أن يقوم العنصر بملئها في الوحدة النمطية لوضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="6abf1-149">الحد الأقصى لحجم الوحدة النمطية لوضع المحتوى هو 12 فتحة.</span><span class="sxs-lookup"><span data-stu-id="6abf1-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="6abf1-150">إذا تجاوز إجمالي حجم التجانب للعناصر *n* الأولى في الوحدة النمطية لوضع المحتوى 12 فتحة، يتم تدوير العناصر إلى الصف التالي.</span><span class="sxs-lookup"><span data-stu-id="6abf1-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="6abf1-151">إضافة الوحدة النمطية لوضع المحتوى التي تحتوي على الوحدة النمطية لعنصر وضع المحتوى إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="6abf1-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="6abf1-152">لإضافة الوحدة النمطية لوضع المحتوى تحتوي على وحدة نمطية لعنصر وضع المحتوى إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6abf1-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6abf1-153">قم بإنشاء قالب يُسمى **قالب وضع المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="6abf1-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="6abf1-154">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة الوحدة النمطية لوضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="6abf1-155">في الوحدة النمطية لوضع المحتوى، أضف الوحدة النمطية لعنصر وضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="6abf1-156">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="6abf1-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="6abf1-157">استخدم قالب وضع المحتوى الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة وضع المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="6abf1-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="6abf1-158">في الفتحة **الرئيسية** في الصفحة الجديدة، قم بإضافة الوحدة النمطية لوضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="6abf1-159">في الوحدة النمطية لوضع المحتوى، أضف الوحدة النمطية لعنصر وضع المحتوى.</span><span class="sxs-lookup"><span data-stu-id="6abf1-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="6abf1-160">في جزء الخصائص للوحدة النمطية لعنصر وضع المحتوى، حدد صورة، وأضف عنونًا وأضف فقرة وأضف ارتباط، وقم بتعيين عنوان URL للارتباط، ثم قم بتعيين حجم التجانب إلى **6**.</span><span class="sxs-lookup"><span data-stu-id="6abf1-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="6abf1-161">كرر الخطوتين 7 و8 لإضافة وحدة نمطية لعنصر وضع محتوى أخرى لها نفس حجم التجانب.</span><span class="sxs-lookup"><span data-stu-id="6abf1-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="6abf1-162">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="6abf1-162">Save and preview the page.</span></span> <span data-ttu-id="6abf1-163">يجب أن ترى عنصري وضع المحتوى يظهران بجوار بعضهما.</span><span class="sxs-lookup"><span data-stu-id="6abf1-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="6abf1-164">يُمكنك ضبط خاصية **حجم التجانب** لكل وحدة نمطية لعنصر وضع محتوى أو إضافة المزيد من الوحدات النمطية لتحقيق التخطيط المرغوب فيه.</span><span class="sxs-lookup"><span data-stu-id="6abf1-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="6abf1-165">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="6abf1-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6abf1-166">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6abf1-166">Additional resources</span></span>

[<span data-ttu-id="6abf1-167">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="6abf1-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6abf1-168">الوحدة النمطية للتنبيه</span><span class="sxs-lookup"><span data-stu-id="6abf1-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="6abf1-169">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="6abf1-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="6abf1-170">وحدة كتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="6abf1-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6abf1-171">الوحدة النمطية لميزة</span><span class="sxs-lookup"><span data-stu-id="6abf1-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="6abf1-172">الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="6abf1-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="6abf1-173">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="6abf1-173">Video player module</span></span>](add-video-player.md)
