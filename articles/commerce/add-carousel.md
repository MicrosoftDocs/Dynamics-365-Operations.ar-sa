---
title: الوحدة النمطية الدوارة
description: يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025771"
---
# <a name="carousel-module"></a><span data-ttu-id="4ccba-103">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="4ccba-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4ccba-104">يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4ccba-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4ccba-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="4ccba-105">Overview</span></span>

<span data-ttu-id="4ccba-106">تُستخدم الوحدة النمطية الدوارة لوضع أصناف ترويجية متعددة (بما في ذلك الصور المنسقة) في شعار دوار يُمكن للعملاء استعراضه.</span><span class="sxs-lookup"><span data-stu-id="4ccba-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="4ccba-107">على سبيل المثال، يُمكن لبائع التجزئة استخدام الوحدة النمطية الدوارة في الصفحة الرئيسية لإظهار منتجات جديدة متعددة أو عروض.</span><span class="sxs-lookup"><span data-stu-id="4ccba-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="4ccba-108">يُمكنك إضافة وحدات كتلة المحتوى داخل الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="4ccba-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="4ccba-109">ثم تُحدد خصائص الوحدة النمطية الدوارة كيفية عرض هذه الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="4ccba-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="4ccba-110">أمثلة على الوحدات النمطية الدوارة في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="4ccba-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="4ccba-111">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="4ccba-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="4ccba-112">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="4ccba-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="4ccba-113">ويُمكن استخدام الوحدة الدوارة على أي صفحة تسويق لترقية العروض أو المنتجات المُتعددة.</span><span class="sxs-lookup"><span data-stu-id="4ccba-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="4ccba-114">خصائص الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="4ccba-114">Carousel module properties</span></span>

| <span data-ttu-id="4ccba-115">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="4ccba-115">Property name</span></span>             | <span data-ttu-id="4ccba-116">القيمة</span><span class="sxs-lookup"><span data-stu-id="4ccba-116">Value</span></span>                 | <span data-ttu-id="4ccba-117">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4ccba-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4ccba-118">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="4ccba-118">Autoplay</span></span>                  | <span data-ttu-id="4ccba-119">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="4ccba-119">**True** or **False**</span></span> | <span data-ttu-id="4ccba-120">إذا تم تعيين القيمة إلى **صحيح**، يُحدث انتقال بين العناصر داخل الوحدة النمطية الدوارة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="4ccba-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="4ccba-121">إذا تم تعيين القيمة إلى **خطأ**، فلن يُحدث أي انتقال ما لم يستخدم العميل لوحة المفاتيح أو الماوس للانتقال من عنصر إلى العنصر التالي.</span><span class="sxs-lookup"><span data-stu-id="4ccba-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="4ccba-122">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="4ccba-122">Slide transition interval</span></span> | <span data-ttu-id="4ccba-123">القيمة بالثواني</span><span class="sxs-lookup"><span data-stu-id="4ccba-123">A value in seconds</span></span>    | <span data-ttu-id="4ccba-124">الفاصل الزمني للانتقال بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="4ccba-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="4ccba-125">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="4ccba-125">Transition type</span></span>           | <span data-ttu-id="4ccba-126">**شريحة** أو **Fade**</span><span class="sxs-lookup"><span data-stu-id="4ccba-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="4ccba-127">تأثير المرحلة الانتقالية بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="4ccba-127">The transition effect between items.</span></span> |
| <span data-ttu-id="4ccba-128">إخفاء الذراع الدوّار</span><span class="sxs-lookup"><span data-stu-id="4ccba-128">Hide carousel flipper</span></span>     | <span data-ttu-id="4ccba-129">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="4ccba-129">**True** or **False**</span></span> | <span data-ttu-id="4ccba-130">إذا تم تعيين القيمة إلى **صواب**، فسيتم إخفاء الذراع الدوّار ومؤشر التسلسل.</span><span class="sxs-lookup"><span data-stu-id="4ccba-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="4ccba-131">السماح باستبعاد الوحدة الدوّارة</span><span class="sxs-lookup"><span data-stu-id="4ccba-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="4ccba-132">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="4ccba-132">**True** or **False**</span></span> | <span data-ttu-id="4ccba-133">إذا تم تعيين القيمة إلى **صحيح**، فبإمكان العملاء استبعاد الوحدة الدوّارة.</span><span class="sxs-lookup"><span data-stu-id="4ccba-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="4ccba-134">إضافة الوحدة النمطية الدوارة إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="4ccba-134">Add a carousel module to a page</span></span>

<span data-ttu-id="4ccba-135">لإضافة الوحدة النمطية الدوارة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4ccba-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4ccba-136">إنشاء قالب صفحة تُسمى **قالب الدوارة**.</span><span class="sxs-lookup"><span data-stu-id="4ccba-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="4ccba-137">في فتحة **النص الأساسي** ، أضف الوحدة النمطية **الصفحة الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="4ccba-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="4ccba-138">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="4ccba-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="4ccba-139">استخدم قالب الدوارة الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة الدوارة**.</span><span class="sxs-lookup"><span data-stu-id="4ccba-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="4ccba-140">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="4ccba-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="4ccba-141">في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الشاشة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="4ccba-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="4ccba-142">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة دوّارة إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="4ccba-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="4ccba-143">أضف الوحدة النمطية لكتلة المحتوى إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="4ccba-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="4ccba-144">قم بتعيين خصائص الوحدة النمطية لكتله المحتوى عن طريق توفير **عنوان** و**ارتباط** و**تخطيط** وخصائص أخرى.</span><span class="sxs-lookup"><span data-stu-id="4ccba-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="4ccba-145">أضف وحدة نمطية أخرى لكتلة المحتوى وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="4ccba-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="4ccba-146">قم بتعيين خصائص إضافية للوحدة النمطية الدوّارة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="4ccba-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="4ccba-147">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="4ccba-147">Save and preview the page.</span></span> <span data-ttu-id="4ccba-148">يجب أن تُظهر الصفحة الوحدة النمطية الدوارة تحتوي على وحدتين نمطيتين بداخلها (الوحدة النمطية لجزء رئيسي والوحدة النمطية لميزة).</span><span class="sxs-lookup"><span data-stu-id="4ccba-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="4ccba-149">يُمكنك تغيير الخصائص الإضافية للوحدات النمطية الدوارة والجزء الرئيسي والميزة لتحقيق التأثير المطلوب.</span><span class="sxs-lookup"><span data-stu-id="4ccba-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="4ccba-150">انشر الصفحة بعد الانتهاء من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="4ccba-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ccba-151">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4ccba-151">Additional resources</span></span>

[<span data-ttu-id="4ccba-152">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="4ccba-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4ccba-153">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="4ccba-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="4ccba-154">وحدة كتلة النص‏‎</span><span class="sxs-lookup"><span data-stu-id="4ccba-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="4ccba-155">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="4ccba-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="4ccba-156">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="4ccba-156">Video player module</span></span>](add-video-player.md)
