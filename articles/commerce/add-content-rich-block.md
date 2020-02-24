---
title: وحدة كتلة النص‏‎
description: يتناول هذا الموضوع وحدات كتل النص ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025587"
---
# <a name="text-block-module"></a><span data-ttu-id="8ebd7-103">وحدة كتلة النص‏‎</span><span class="sxs-lookup"><span data-stu-id="8ebd7-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8ebd7-104">يتناول هذا الموضوع وحدات كتل النص ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ebd7-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8ebd7-105">Overview</span></span>

<span data-ttu-id="8ebd7-106">وحدة كتلة النص عبارة عن وحدة تُستخدم لإضافة محتوى سياقي.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="8ebd7-107">قد يكون هذا المحتوى معلوماتي أو ترويجي.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="8ebd7-108">يتم التحكم في وحدات كتل النص بواسطة البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="8ebd7-109">فهي وحدات نمطية مستقلة لا تعتمد على سياق الصفحة أو على أي وحدات نمطية أخرى.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="8ebd7-110">أمثلة عن وحدات كتل النص في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="8ebd7-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="8ebd7-111">يُمكن استخدام وحدات كتلة النص بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="8ebd7-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="8ebd7-112">لإظهار ميزات المنتج في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="8ebd7-113">لأغراض إعلامية على أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-113">For informational purposes on any page.</span></span> <span data-ttu-id="8ebd7-114">على سبيل المثال، يُمكن لهذه الوحدات توضيح مزايا برامج الولاء وسرد سياسات الشحن والإرجاع والرد على الأسئلة الشائعة أو توفير محتوى "نبذة عنا".</span><span class="sxs-lookup"><span data-stu-id="8ebd7-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="8ebd7-115">لإضافة رسائل مخصصة في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="8ebd7-116">(على سبيل المثال، "شحن مجاني للأوامر التي تزيد عن 50 دولار").</span><span class="sxs-lookup"><span data-stu-id="8ebd7-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="8ebd7-117">بالنسبة لإخلاء المسؤولية وتفاصيل جهة الاتصال على صفحات تفاصيل المنتج وصفحات سلة التسوق وصفحات السداد مع الخروج والصفحات الأخرى (على سبيل المثال، "تخضع عمليات الشحن والإرجاع لسياسات المتجر").</span><span class="sxs-lookup"><span data-stu-id="8ebd7-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="8ebd7-118">خصائص وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="8ebd7-118">Text block module properties</span></span>

| <span data-ttu-id="8ebd7-119">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="8ebd7-119">Property name</span></span>     | <span data-ttu-id="8ebd7-120">قيمة</span><span class="sxs-lookup"><span data-stu-id="8ebd7-120">Value</span></span>                                            | <span data-ttu-id="8ebd7-121">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="8ebd7-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="8ebd7-122">نص منسق</span><span class="sxs-lookup"><span data-stu-id="8ebd7-122">Rich text</span></span>         | <span data-ttu-id="8ebd7-123">نص منسق</span><span class="sxs-lookup"><span data-stu-id="8ebd7-123">Rich text</span></span>                                        | <span data-ttu-id="8ebd7-124">نص الفقرة.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-124">Paragraph text.</span></span> <span data-ttu-id="8ebd7-125">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="8ebd7-126">اسم فئة مخصصة</span><span class="sxs-lookup"><span data-stu-id="8ebd7-126">Custom class name</span></span> | <span data-ttu-id="8ebd7-127">اسم فئة أوراق الأنماط المتتالية (CSS)</span><span class="sxs-lookup"><span data-stu-id="8ebd7-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="8ebd7-128">اسم فئة CSS مخصصة CSS يوفرها المطور لتنسيق هذه الوحدة.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="8ebd7-129">يجب تعريف اسم الفئة في حزمة النسق.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="8ebd7-130">حجم الخط</span><span class="sxs-lookup"><span data-stu-id="8ebd7-130">Font size</span></span>         | <span data-ttu-id="8ebd7-131">**صغير**أو **متوسط** أو **كبير** أو **كبير‏‎ جدًا**</span><span class="sxs-lookup"><span data-stu-id="8ebd7-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="8ebd7-132">حجم خط المحتوى.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="8ebd7-133">إضافة وحدة كتلة نص إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="8ebd7-133">Add a text block module to a page</span></span>

<span data-ttu-id="8ebd7-134">لإضافة وحدة كتلة نص إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8ebd7-135">إنشاء قالب صفحة تُسمى **قالب المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="8ebd7-136">في فتحة **النص الأساسي** ، أضف الوحدة النمطية **الصفحة الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="8ebd7-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="8ebd7-137">انشر القالب بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="8ebd7-138">استخدم قالب المحتوى الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="8ebd7-139">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="8ebd7-140">في جزء الخاصية لوحدة الحاوية، عيّن خاصية **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="8ebd7-141">أضف وحدة كتلة نص إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="8ebd7-142">في جزء الخصائص لوحدة كتلة النص، أضف نصًا إلى حقل **النص المنسق**.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="8ebd7-143">انشر الصفحة بعد الانتهاء من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="8ebd7-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ebd7-144">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8ebd7-144">Additional resources</span></span>

[<span data-ttu-id="8ebd7-145">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="8ebd7-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8ebd7-146">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="8ebd7-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="8ebd7-147">وحدة نمطية دوارة</span><span class="sxs-lookup"><span data-stu-id="8ebd7-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8ebd7-148">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="8ebd7-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="8ebd7-149">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="8ebd7-149">Video player module</span></span>](add-video-player.md)

