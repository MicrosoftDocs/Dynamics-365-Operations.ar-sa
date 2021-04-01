---
title: وحدة كتلة النص‏‎
description: يتناول هذا الموضوع وحدات كتل النص ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206381"
---
# <a name="text-block-module"></a><span data-ttu-id="e5ede-103">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="e5ede-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5ede-104">يتناول هذا الموضوع وحدات كتل النص ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e5ede-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e5ede-105">وحدة كتلة النص عبارة عن وحدة تُستخدم لإضافة محتوى سياقي.</span><span class="sxs-lookup"><span data-stu-id="e5ede-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="e5ede-106">قد يكون هذا المحتوى معلوماتي أو ترويجي.</span><span class="sxs-lookup"><span data-stu-id="e5ede-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="e5ede-107">يتم التحكم في وحدات كتل النص بواسطة البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="e5ede-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="e5ede-108">فهي وحدات نمطية مستقلة لا تعتمد على سياق الصفحة أو على أي وحدات نمطية أخرى.</span><span class="sxs-lookup"><span data-stu-id="e5ede-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="e5ede-109">أمثلة عن وحدات كتل النص في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e5ede-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="e5ede-110">يُمكن استخدام وحدات كتلة النص بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="e5ede-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="e5ede-111">لإظهار ميزات المنتج في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="e5ede-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="e5ede-112">لأغراض إعلامية على أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="e5ede-112">For informational purposes on any page.</span></span> <span data-ttu-id="e5ede-113">على سبيل المثال، يُمكن لهذه الوحدات توضيح مزايا برامج الولاء وسرد سياسات الشحن والإرجاع والرد على الأسئلة الشائعة أو توفير محتوى "نبذة عنا".</span><span class="sxs-lookup"><span data-stu-id="e5ede-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="e5ede-114">لإضافة رسائل مخصصة في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="e5ede-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="e5ede-115">(على سبيل المثال، "شحن مجاني للأوامر التي تزيد عن 50 دولار").</span><span class="sxs-lookup"><span data-stu-id="e5ede-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="e5ede-116">بالنسبة لإخلاء المسؤولية وتفاصيل جهة الاتصال على صفحات تفاصيل المنتج وصفحات سلة التسوق وصفحات السداد مع الخروج والصفحات الأخرى (على سبيل المثال، "تخضع عمليات الشحن والإرجاع لسياسات المتجر").</span><span class="sxs-lookup"><span data-stu-id="e5ede-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="e5ede-117">تعرض الصورة التالية مثالاً عن وحدة كتلة النص المستخدمة في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="e5ede-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![مثال عن وحدة كتلة نص](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="e5ede-119">خصائص وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="e5ede-119">Text block module properties</span></span>

| <span data-ttu-id="e5ede-120">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="e5ede-120">Property name</span></span>     | <span data-ttu-id="e5ede-121">قيمة</span><span class="sxs-lookup"><span data-stu-id="e5ede-121">Value</span></span>                                            | <span data-ttu-id="e5ede-122">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e5ede-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="e5ede-123">نص منسق</span><span class="sxs-lookup"><span data-stu-id="e5ede-123">Rich text</span></span>         | <span data-ttu-id="e5ede-124">نص منسق</span><span class="sxs-lookup"><span data-stu-id="e5ede-124">Rich text</span></span>                                        | <span data-ttu-id="e5ede-125">نص الفقرة.</span><span class="sxs-lookup"><span data-stu-id="e5ede-125">Paragraph text.</span></span> <span data-ttu-id="e5ede-126">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل.</span><span class="sxs-lookup"><span data-stu-id="e5ede-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="e5ede-127">اسم فئة مخصصة</span><span class="sxs-lookup"><span data-stu-id="e5ede-127">Custom class name</span></span> | <span data-ttu-id="e5ede-128">اسم فئة أوراق الأنماط المتتالية (CSS)</span><span class="sxs-lookup"><span data-stu-id="e5ede-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="e5ede-129">اسم فئة CSS مخصصة CSS يوفرها المطور لتنسيق هذه الوحدة.</span><span class="sxs-lookup"><span data-stu-id="e5ede-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="e5ede-130">يجب تعريف اسم الفئة في حزمة النسق.</span><span class="sxs-lookup"><span data-stu-id="e5ede-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="e5ede-131">حجم الخط</span><span class="sxs-lookup"><span data-stu-id="e5ede-131">Font size</span></span>         | <span data-ttu-id="e5ede-132">**صغير** أو **متوسط** أو **كبير** أو **كبير‏‎ جدًا**</span><span class="sxs-lookup"><span data-stu-id="e5ede-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="e5ede-133">حجم خط المحتوى.</span><span class="sxs-lookup"><span data-stu-id="e5ede-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="e5ede-134">إضافة وحدة كتلة نص إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="e5ede-134">Add a text block module to a page</span></span>

<span data-ttu-id="e5ede-135">لإضافة وحدة كتلة نص إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e5ede-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e5ede-136">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="e5ede-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e5ede-137">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="e5ede-138">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e5ede-139">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e5ede-140">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="e5ede-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e5ede-141">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="e5ede-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="e5ede-142">في مربع الحوار **اختيار قالب**، حدد **قالب المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="e5ede-143">ضمن **اسم الصفحة**، أدخل **صفحة المحتوى**، ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="e5ede-144">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e5ede-145">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e5ede-146">في جزء الخاصية لوحدة الحاوية، عيّن خاصية **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e5ede-147">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e5ede-148">في مربع الحوار **إضافة وحدة**، حدد وحدة **كتلة النص‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="e5ede-149">في جزء الخصائص لوحدة كتلة النص، أضف نصًا إلى حقل **النص المنسق**.</span><span class="sxs-lookup"><span data-stu-id="e5ede-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="e5ede-150">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5ede-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e5ede-151">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="e5ede-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5ede-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e5ede-152">Additional resources</span></span>

[<span data-ttu-id="e5ede-153">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="e5ede-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e5ede-154">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="e5ede-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e5ede-155">وحدة دوارة</span><span class="sxs-lookup"><span data-stu-id="e5ede-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e5ede-156">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="e5ede-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="e5ede-157">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="e5ede-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]