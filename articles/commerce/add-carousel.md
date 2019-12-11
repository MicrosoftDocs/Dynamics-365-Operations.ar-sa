---
title: الوحدة النمطية الدوارة
description: يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785227"
---
# <a name="carousel-module"></a><span data-ttu-id="6c905-103">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="6c905-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6c905-104">يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c905-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c905-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6c905-105">Overview</span></span>

<span data-ttu-id="6c905-106">تُستخدم الوحدة النمطية الدوارة لوضع الأصناف الترويجية المتعددة في الوحدة النمطية الدوارة يُمكن للعملاء استعراضها.</span><span class="sxs-lookup"><span data-stu-id="6c905-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="6c905-107">وهي وحدة حاوية خاصة تستضيف الوحدات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="6c905-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="6c905-108">على سبيل المثال، يُمكن لبائع التجزئة استخدام الوحدة النمطية الدوارة في الصفحة الرئيسية لإظهار منتجات جديدة متعددة أو عروض.</span><span class="sxs-lookup"><span data-stu-id="6c905-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="6c905-109">يُمكنك إضافة وحدات نمطية خاصة لجزء رئيسي وميزات داخل الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="6c905-110">ثم تُحدد خصائص الوحدة النمطية الدوارة كيفية عرض هذه الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="6c905-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="6c905-111">أمثلة على الوحدات النمطية الدوارة في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6c905-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="6c905-112">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="6c905-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="6c905-113">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="6c905-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="6c905-114">ويُمكن استخدام الوحدة الدوارة على أي صفحة تسويق لترقية العروض أو المنتجات المُتعددة.</span><span class="sxs-lookup"><span data-stu-id="6c905-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="6c905-115">خصائص الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="6c905-115">Carousel module properties</span></span>

| <span data-ttu-id="6c905-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="6c905-116">Property name</span></span>             | <span data-ttu-id="6c905-117">القيمة</span><span class="sxs-lookup"><span data-stu-id="6c905-117">Value</span></span>                                | <span data-ttu-id="6c905-118">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="6c905-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="6c905-119">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="6c905-119">Autoplay</span></span>                  | <span data-ttu-id="6c905-120">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="6c905-120">**True** or **False**</span></span>                | <span data-ttu-id="6c905-121">إذا تم تعيين القيمة إلى **صحيح**، يُحدث انتقال بين العناصر داخل الوحدة النمطية الدوارة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6c905-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="6c905-122">إذا تم تعيين القيمة إلى **خطأ**، فلن يُحدث أي انتقال ما لم يستخدم العميل لوحة المفاتيح أو الماوس للانتقال من عنصر إلى العنصر التالي.</span><span class="sxs-lookup"><span data-stu-id="6c905-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="6c905-123">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="6c905-123">Slide transition interval</span></span> | <span data-ttu-id="6c905-124">القيمة بالثواني</span><span class="sxs-lookup"><span data-stu-id="6c905-124">A value in seconds</span></span>                   | <span data-ttu-id="6c905-125">الفاصل الزمني للانتقال بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="6c905-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="6c905-126">صورة الانتقال</span><span class="sxs-lookup"><span data-stu-id="6c905-126">Transition animation</span></span>      | <span data-ttu-id="6c905-127">**شريحة** أو **Fade**</span><span class="sxs-lookup"><span data-stu-id="6c905-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="6c905-128">أثر الانتقال.</span><span class="sxs-lookup"><span data-stu-id="6c905-128">The transition effect.</span></span> |
| <span data-ttu-id="6c905-129">العرض</span><span class="sxs-lookup"><span data-stu-id="6c905-129">Width</span></span>                     | <span data-ttu-id="6c905-130">**ملائمة الحاوية** أو **ملء الشاشة**</span><span class="sxs-lookup"><span data-stu-id="6c905-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="6c905-131">إذا تم تعيين القيمة إلى **ملائمة الحاوية**، فمن ثم تقتصر العناصر داخل الوحدة الدوارة على عرض الوحدة الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="6c905-132">إذا لم تعيين القيمة إلى **ملء الشاشة**، فلن تقتصر العناصر على عرض الوحدة الدوارة ولكن يُمكنها الانتقال إلى وضع ملء الشاشة.</span><span class="sxs-lookup"><span data-stu-id="6c905-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="6c905-133">يُمكنك تغيير القيمة لتحقيق التخطيط المرغوب.</span><span class="sxs-lookup"><span data-stu-id="6c905-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="6c905-134">إضافة الوحدة النمطية الدوارة إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="6c905-134">Add a carousel module to a page</span></span>

<span data-ttu-id="6c905-135">لإضافة الوحدة النمطية الدوارة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6c905-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6c905-136">إنشاء قالب صفحة تُسمى **قالب الدوارة**.</span><span class="sxs-lookup"><span data-stu-id="6c905-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="6c905-137">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="6c905-138">إضافة الوحدة النمطية الرئيسية إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="6c905-139">إضافة الوحدة النمطية لميزة إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="6c905-140">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="6c905-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="6c905-141">استخدم قالب الدوارة الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة الدوارة**.</span><span class="sxs-lookup"><span data-stu-id="6c905-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="6c905-142">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="6c905-143">قم بتعيين خاصية **العرض** في الوحدة النمطية الدوارة إلى **ملء الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="6c905-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="6c905-144">قم بتعيين خاصية **صورة الانتقال** إلى **شريحة**.</span><span class="sxs-lookup"><span data-stu-id="6c905-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="6c905-145">إضافة الوحدة النمطية الرئيسية إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="6c905-146">في الوحدة النمطية للجزء الرئيسي، أضف صورة وعنوان، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="6c905-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="6c905-147">إضافة الوحدة النمطية لميزة إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="6c905-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="6c905-148">في الوحدة النمطية لميزة، أضف صورة وعنوان وفقرة من النص.</span><span class="sxs-lookup"><span data-stu-id="6c905-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="6c905-149">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="6c905-149">Save and preview the page.</span></span> <span data-ttu-id="6c905-150">يجب أن تُظهر الصفحة الوحدة النمطية الدوارة تحتوي على وحدتين نمطيتين بداخلها (الوحدة النمطية لجزء رئيسي والوحدة النمطية لميزة).</span><span class="sxs-lookup"><span data-stu-id="6c905-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="6c905-151">يُمكنك تغيير الخصائص الإضافية للوحدات النمطية الدوارة والجزء الرئيسي والميزة لتحقيق التأثير المطلوب.</span><span class="sxs-lookup"><span data-stu-id="6c905-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="6c905-152">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="6c905-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c905-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6c905-153">Additional resources</span></span>

[<span data-ttu-id="6c905-154">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="6c905-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6c905-155">الوحدة النمطية للتنبيه</span><span class="sxs-lookup"><span data-stu-id="6c905-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="6c905-156">وحدة كتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="6c905-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6c905-157">الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="6c905-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="6c905-158">الوحدة النمطية لميزة</span><span class="sxs-lookup"><span data-stu-id="6c905-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="6c905-159">الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="6c905-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="6c905-160">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="6c905-160">Video player module</span></span>](add-video-player.md)
