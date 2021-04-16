---
title: الوحدة النمطية الدوارة
description: يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797877"
---
# <a name="carousel-module"></a><span data-ttu-id="33b76-103">وحدة دوارة</span><span class="sxs-lookup"><span data-stu-id="33b76-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33b76-104">يتناول هذا الموضوع الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="33b76-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="33b76-105">تُستخدم الوحدة النمطية الدوارة لوضع أصناف ترويجية متعددة (بما في ذلك الصور المنسقة) في شعار دوار يُمكن للعملاء استعراضه.</span><span class="sxs-lookup"><span data-stu-id="33b76-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="33b76-106">على سبيل المثال، يُمكن لبائع التجزئة استخدام الوحدة النمطية الدوارة في الصفحة الرئيسية لإظهار منتجات جديدة متعددة أو عروض.</span><span class="sxs-lookup"><span data-stu-id="33b76-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="33b76-107">يُمكنك إضافة وحدات كتلة المحتوى داخل الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="33b76-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="33b76-108">ثم تُحدد خصائص الوحدة النمطية الدوارة كيفية عرض هذه الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="33b76-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="33b76-109">أمثلة على الوحدات النمطية الدوارة في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="33b76-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="33b76-110">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="33b76-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="33b76-111">يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="33b76-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="33b76-112">ويُمكن استخدام الوحدة الدوارة على أي صفحة تسويق لترقية العروض أو المنتجات المُتعدة.</span><span class="sxs-lookup"><span data-stu-id="33b76-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="33b76-113">تعرض الصورة التالية مثالاً عن وحدة نمطية دوارة‬ مستخدمة في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="33b76-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="33b76-114">تحتوي الوحدة النمطية الدوارة‬ على عناصر كتل محتويات متعددة.</span><span class="sxs-lookup"><span data-stu-id="33b76-114">This carousel module contains multiple content block items.</span></span>

![مثال عن وحدة نمطية دوارة](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="33b76-116">خصائص الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="33b76-116">Carousel module properties</span></span>

| <span data-ttu-id="33b76-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="33b76-117">Property name</span></span>             | <span data-ttu-id="33b76-118">قيمة</span><span class="sxs-lookup"><span data-stu-id="33b76-118">Value</span></span>                 | <span data-ttu-id="33b76-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="33b76-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="33b76-120">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="33b76-120">Autoplay</span></span>                  | <span data-ttu-id="33b76-121">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="33b76-121">**True** or **False**</span></span> | <span data-ttu-id="33b76-122">إذا تم تعيين القيمة إلى **صحيح**، يُحدث انتقال بين العناصر داخل الوحدة النمطية الدوارة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="33b76-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="33b76-123">إذا تم تعيين القيمة إلى **خطأ**، فلن يُحدث أي انتقال ما لم يستخدم العميل لوحة المفاتيح أو الماوس للانتقال من عنصر إلى العنصر التالي.</span><span class="sxs-lookup"><span data-stu-id="33b76-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="33b76-124">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="33b76-124">Slide transition interval</span></span> | <span data-ttu-id="33b76-125">القيمة بالثواني</span><span class="sxs-lookup"><span data-stu-id="33b76-125">A value in seconds</span></span>    | <span data-ttu-id="33b76-126">الفاصل الزمني للانتقال بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="33b76-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="33b76-127">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="33b76-127">Transition type</span></span>           | <span data-ttu-id="33b76-128">**شريحة** أو **Fade**</span><span class="sxs-lookup"><span data-stu-id="33b76-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="33b76-129">تأثير المرحلة الانتقالية بين العناصر.</span><span class="sxs-lookup"><span data-stu-id="33b76-129">The transition effect between items.</span></span> |
| <span data-ttu-id="33b76-130">إخفاء الذراع الدوّار</span><span class="sxs-lookup"><span data-stu-id="33b76-130">Hide carousel flipper</span></span>     | <span data-ttu-id="33b76-131">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="33b76-131">**True** or **False**</span></span> | <span data-ttu-id="33b76-132">إذا تم تعيين القيمة إلى **صواب**، فسيتم إخفاء الذراع الدوّار ومؤشر التسلسل.</span><span class="sxs-lookup"><span data-stu-id="33b76-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="33b76-133">السماح باستبعاد الوحدة الدوّارة</span><span class="sxs-lookup"><span data-stu-id="33b76-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="33b76-134">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="33b76-134">**True** or **False**</span></span> | <span data-ttu-id="33b76-135">إذا تم تعيين القيمة إلى **صحيح**، فبإمكان العملاء استبعاد الوحدة الدوّارة.</span><span class="sxs-lookup"><span data-stu-id="33b76-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="33b76-136">إضافة الوحدة النمطية الدوارة إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="33b76-136">Add a carousel module to a page</span></span>

<span data-ttu-id="33b76-137">لإضافة الوحدة النمطية الدوارة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="33b76-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="33b76-138">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="33b76-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="33b76-139">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب دوار**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="33b76-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="33b76-140">في فتحة **النص الأساسي**، أضف الوحدة النمطية **الصفحة الافتراضية** .</span><span class="sxs-lookup"><span data-stu-id="33b76-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="33b76-141">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="33b76-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="33b76-142">استخدم القالب الدوار الذي أنشأته للتو لإنشاء صفحة تسمى **صفحة دواره**.</span><span class="sxs-lookup"><span data-stu-id="33b76-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="33b76-143">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="33b76-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="33b76-144">في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الشاشة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="33b76-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="33b76-145">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة دوّارة إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="33b76-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="33b76-146">أضف الوحدة النمطية لكتلة المحتوى إلى الوحدة النمطية الدوارة.</span><span class="sxs-lookup"><span data-stu-id="33b76-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="33b76-147">قم بتعيين خصائص الوحدة النمطية لكتله المحتوى عن طريق توفير **عنوان** و **ارتباط** و **تخطيط** وخصائص أخرى.</span><span class="sxs-lookup"><span data-stu-id="33b76-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="33b76-148">أضف وحدة نمطية أخرى لكتلة المحتوى وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="33b76-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="33b76-149">قم بتعيين خصائص إضافية للوحدة النمطية الدوّارة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="33b76-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="33b76-150">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="33b76-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="33b76-151">يجب أن تُظهر الصفحة الوحدة النمطية الدوارة تحتوي على وحدتين نمطيتين بداخلها (الوحدة النمطية لجزء رئيسي والوحدة النمطية لميزة).</span><span class="sxs-lookup"><span data-stu-id="33b76-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="33b76-152">يُمكنك تغيير الخصائص الإضافية للوحدات النمطية الدوارة والجزء الرئيسي والميزة لتحقيق التأثير المطلوب.</span><span class="sxs-lookup"><span data-stu-id="33b76-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="33b76-153">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="33b76-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33b76-154">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="33b76-154">Additional resources</span></span>

[<span data-ttu-id="33b76-155">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="33b76-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="33b76-156">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="33b76-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="33b76-157">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="33b76-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="33b76-158">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="33b76-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="33b76-159">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="33b76-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]