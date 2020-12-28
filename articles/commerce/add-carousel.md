---
title: الوحدة النمطية الدوارة
description: يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f09f3f98d174f965a75e27ee6a5c2ed8599042fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409819"
---
# <a name="carousel-module"></a><span data-ttu-id="31951-103">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="31951-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31951-104">يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31951-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31951-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="31951-105">Overview</span></span>

<span data-ttu-id="31951-106">تُستخدم الوحدة النمطية الدوارة لوضع أصناف ترويجية متعددة (بما في ذلك الصور المنسقة) في شعار دوار يُمكن للعملاء استعراضه.</span><span class="sxs-lookup"><span data-stu-id="31951-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="31951-107">على سبيل المثال، يُمكن لبائع التجزئة استخدام الوحدة النمطية الدوارة في الصفحة الرئيسية لإظهار منتجات جديدة متعددة أو عروض.</span><span class="sxs-lookup"><span data-stu-id="31951-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="31951-108">يُمكنك إضافة وحدات كتلة المحتوى داخل الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="31951-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="31951-109">ثم تُحدد خصائص الوحدة النمطية الدوارة كيفية عرض هذه الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="31951-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="31951-110">أمثلة على الوحدات النمطية الدوارة في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="31951-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="31951-111">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="31951-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="31951-112">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="31951-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="31951-113">ويُمكن استخدام الوحدة الدوارة على أي صفحة تسويق لترقية العروض أو المنتجات المُتعدة.</span><span class="sxs-lookup"><span data-stu-id="31951-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="31951-114">تعرض الصورة التالية مثالاً عن وحدة نمطية دوارة‬ مستخدمة في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="31951-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="31951-115">تحتوي الوحدة النمطية الدوارة‬ على عناصر كتل محتويات متعددة.</span><span class="sxs-lookup"><span data-stu-id="31951-115">This carousel module contains multiple content block items.</span></span>

![مثال عن وحدة نمطية دوارة](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="31951-117">خصائص الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="31951-117">Carousel module properties</span></span>

| <span data-ttu-id="31951-118">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="31951-118">Property name</span></span>             | <span data-ttu-id="31951-119">قيمة</span><span class="sxs-lookup"><span data-stu-id="31951-119">Value</span></span>                 | <span data-ttu-id="31951-120">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="31951-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="31951-121">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="31951-121">Autoplay</span></span>                  | <span data-ttu-id="31951-122">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="31951-122">**True** or **False**</span></span> | <span data-ttu-id="31951-123">إذا تم تعيين القيمة إلى **صحيح**، يُحدث انتقال بين العناصر داخل الوحدة النمطية الدوارة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="31951-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="31951-124">إذا تم تعيين القيمة إلى **خطأ**، فلن يُحدث أي انتقال ما لم يستخدم العميل لوحة المفاتيح أو الماوس للانتقال من عنصر إلى العنصر التالي.</span><span class="sxs-lookup"><span data-stu-id="31951-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="31951-125">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="31951-125">Slide transition interval</span></span> | <span data-ttu-id="31951-126">القيمة بالثواني</span><span class="sxs-lookup"><span data-stu-id="31951-126">A value in seconds</span></span>    | <span data-ttu-id="31951-127">الفاصل الزمني للانتقال بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="31951-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="31951-128">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="31951-128">Transition type</span></span>           | <span data-ttu-id="31951-129">**شريحة** أو **Fade**</span><span class="sxs-lookup"><span data-stu-id="31951-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="31951-130">تأثير المرحلة الانتقالية بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="31951-130">The transition effect between items.</span></span> |
| <span data-ttu-id="31951-131">إخفاء الذراع الدوّار</span><span class="sxs-lookup"><span data-stu-id="31951-131">Hide carousel flipper</span></span>     | <span data-ttu-id="31951-132">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="31951-132">**True** or **False**</span></span> | <span data-ttu-id="31951-133">إذا تم تعيين القيمة إلى **صواب**، فسيتم إخفاء الذراع الدوّار ومؤشر التسلسل.</span><span class="sxs-lookup"><span data-stu-id="31951-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="31951-134">السماح باستبعاد الوحدة الدوّارة</span><span class="sxs-lookup"><span data-stu-id="31951-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="31951-135">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="31951-135">**True** or **False**</span></span> | <span data-ttu-id="31951-136">إذا تم تعيين القيمة إلى **صحيح**، فبإمكان العملاء استبعاد الوحدة الدوّارة.</span><span class="sxs-lookup"><span data-stu-id="31951-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="31951-137">إضافة الوحدة النمطية الدوارة إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="31951-137">Add a carousel module to a page</span></span>

<span data-ttu-id="31951-138">لإضافة الوحدة النمطية الدوارة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="31951-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="31951-139">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="31951-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="31951-140">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب دوار**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31951-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="31951-141">في فتحة **النص الأساسي**، أضف الوحدة النمطية **الصفحة الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="31951-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="31951-142">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="31951-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="31951-143">استخدم القالب الدوار الذي أنشأته للتو لإنشاء صفحة تسمى **صفحة دواره**.</span><span class="sxs-lookup"><span data-stu-id="31951-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="31951-144">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="31951-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="31951-145">في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الشاشة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="31951-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="31951-146">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة دوّارة إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="31951-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="31951-147">أضف الوحدة النمطية لكتلة المحتوى إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="31951-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="31951-148">قم بتعيين خصائص الوحدة النمطية لكتله المحتوى عن طريق توفير **عنوان** و **ارتباط** و **تخطيط** وخصائص أخرى.</span><span class="sxs-lookup"><span data-stu-id="31951-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="31951-149">أضف وحدة نمطية أخرى لكتلة المحتوى وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="31951-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="31951-150">قم بتعيين خصائص إضافية للوحدة النمطية الدوّارة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="31951-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="31951-151">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="31951-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="31951-152">يجب أن تُظهر الصفحة الوحدة النمطية الدوارة تحتوي على وحدتين نمطيتين بداخلها (الوحدة النمطية لجزء رئيسي والوحدة النمطية لميزة).</span><span class="sxs-lookup"><span data-stu-id="31951-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="31951-153">يُمكنك تغيير الخصائص الإضافية للوحدات النمطية الدوارة والجزء الرئيسي والميزة لتحقيق التأثير المطلوب.</span><span class="sxs-lookup"><span data-stu-id="31951-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="31951-154">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="31951-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31951-155">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="31951-155">Additional resources</span></span>

[<span data-ttu-id="31951-156">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="31951-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="31951-157">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="31951-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="31951-158">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="31951-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="31951-159">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="31951-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="31951-160">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="31951-160">Video player module</span></span>](add-video-player.md)
