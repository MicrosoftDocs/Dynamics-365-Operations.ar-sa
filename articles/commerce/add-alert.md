---
title: وحدة الشعار الترويجي
description: يتناول هذا الموضوع وحدات الشعارات الترويجية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: d9debd16b18300d090bde1862a16920d8e9185eb
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817244"
---
# <a name="promo-banner-module"></a><span data-ttu-id="6a2a6-103">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="6a2a6-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a2a6-104">يتناول هذا الموضوع وحدات الشعارات الترويجية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a2a6-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6a2a6-105">Overview</span></span>

<span data-ttu-id="6a2a6-106">تستخدم وحدات الشعارات الترويجية لعرض رسائل المعلومات المضمنة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="6a2a6-107">ويُمكن استخدامها للعروض على مستوى الموقع التي تظهر في كافة صفحات موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="6a2a6-108">تدعم وحدات الشعارات الترويجية رسالة نصية وارتباطًا.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="6a2a6-109">إذا تمت إضافة رسائل متعددة إلى وحدة شعار ترويجي، تصبح شعارًا دوارًا يسمح للعملاء بالتنقل عبر الرسائل.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="6a2a6-110">يتم التحكم في وحدات الشعارات الترويجية بواسطة البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="6a2a6-111">أمثلة للاستخدام حول الشعارات الترويجية في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6a2a6-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="6a2a6-112">يمكن استخدام الشعارات الترويجية في رأس الموقع لإظهار العروض أو الرسائل الترويجية على مستوى الموقع، كما في الأمثلة التالية.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="6a2a6-113">"تنتهي المبيعات السنوية خلال 10 أيام" </span><span class="sxs-lookup"><span data-stu-id="6a2a6-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="6a2a6-114">"قم بحفظ big مع عمليات بيع العودة إلى المدرسة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-114">"Save big with back to school sale.</span></span> <span data-ttu-id="6a2a6-115">تسوق الآن. "</span><span class="sxs-lookup"><span data-stu-id="6a2a6-115">Shop Now."</span></span>

<span data-ttu-id="6a2a6-116">"تخفيضات خاصة لعيد الشكر!"</span><span class="sxs-lookup"><span data-stu-id="6a2a6-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="6a2a6-117">تبين الصورة التالية مثالاً عن شعار ترويجي.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-117">The following image shows an example of a promo banner.</span></span>

![مثال عن وحدة شعار ترويجي](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="6a2a6-119">خصائص وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="6a2a6-119">Promo banner module properties</span></span>

| <span data-ttu-id="6a2a6-120">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="6a2a6-120">Property name</span></span>             | <span data-ttu-id="6a2a6-121">قيمة</span><span class="sxs-lookup"><span data-stu-id="6a2a6-121">Value</span></span>                              | <span data-ttu-id="6a2a6-122">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="6a2a6-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="6a2a6-123">رسائل الافتة</span><span class="sxs-lookup"><span data-stu-id="6a2a6-123">Banner messages</span></span>           | <span data-ttu-id="6a2a6-124">نص وارتباطات</span><span class="sxs-lookup"><span data-stu-id="6a2a6-124">Text and links</span></span>                     | <span data-ttu-id="6a2a6-125">مجموعة من النصوص والارتباطات.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-125">An array of text and links.</span></span> |
| <span data-ttu-id="6a2a6-126">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="6a2a6-126">Autoplay</span></span>                  | <span data-ttu-id="6a2a6-127">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="6a2a6-127">**True** or **False**</span></span>              | <span data-ttu-id="6a2a6-128">قيمة تشير إلى ما إذا كان يتم التنقل عبر الرسائل بشكل تلقائي، إذا تم تكوين رسائل متعددة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="6a2a6-129">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="6a2a6-129">Slide transition interval</span></span> | <span data-ttu-id="6a2a6-130">عدد المللي ثواني</span><span class="sxs-lookup"><span data-stu-id="6a2a6-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="6a2a6-131">الفاصل الزمني الذي يتم استخدامه للتنقل بين الرسائل.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="6a2a6-132">السماح بالاستبعاد</span><span class="sxs-lookup"><span data-stu-id="6a2a6-132">Allow dismiss</span></span>             | <span data-ttu-id="6a2a6-133">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="6a2a6-133">**True** or **False**</span></span>              | <span data-ttu-id="6a2a6-134">إذا تم تعيين القيمة إلى **صحيح**، بإمكان العملاء استبعاد التنبيه.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="6a2a6-135">إظهار الذراع الدوار</span><span class="sxs-lookup"><span data-stu-id="6a2a6-135">Show carousel flipper</span></span>     | <span data-ttu-id="6a2a6-136">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="6a2a6-136">**True** or **False**</span></span>              | <span data-ttu-id="6a2a6-137">قيمة تشير إلى ما إذا كان يجب عرض القيمة الأذرع الدوارة، لتمكين العملاء من التنقل بطريقة يدوية عبر عناصر الشعار المتعددة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="6a2a6-138">محاذاة النص</span><span class="sxs-lookup"><span data-stu-id="6a2a6-138">Text alignment</span></span>            | <span data-ttu-id="6a2a6-139">**اليمين**, **اليسار**, أو **الوسط**</span><span class="sxs-lookup"><span data-stu-id="6a2a6-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="6a2a6-140">محاذاة النص في وحدة الشعار الترويجي.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="6a2a6-141">الارتباط</span><span class="sxs-lookup"><span data-stu-id="6a2a6-141">Link</span></span>                      | <span data-ttu-id="6a2a6-142">عنوان URL</span><span class="sxs-lookup"><span data-stu-id="6a2a6-142">A URL</span></span>                              | <span data-ttu-id="6a2a6-143">عنوان URL لارتباط اختياري.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="6a2a6-144">إضافة وحدة شعار ترويجي إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="6a2a6-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="6a2a6-145">لإضافة وحدة شعار ترويجي إلى صفحة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6a2a6-146">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6a2a6-147">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب شعار ترويجي**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6a2a6-148">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة **الصفحة الافتراضية** إلى فتحة **النص الأساسي**.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="6a2a6-149">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="6a2a6-150">استخدم القالب الذي أنشأته للتو لإنشاء صفحة مسماة **صفحة الشعار الترويجي**.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="6a2a6-151">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="6a2a6-152">في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="6a2a6-153">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة الشعار الترويجي إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="6a2a6-154">في إعدادات وحدة الشعار الترويجي، أضف رسالة شعار واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="6a2a6-155">بإمكان كل رسالة أن تتضمن نصًا مع ارتباط.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-155">Each message can have text together with a link.</span></span> <span data-ttu-id="6a2a6-156">يُمكنك تحرير الخصائص الأخرى إذا كنت ترغب في تخصيص الوحدة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="6a2a6-157">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="6a2a6-158">في أعلى الصفحة، يجب أن ترى تنبيهًا يُظهر النص الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="6a2a6-159">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="6a2a6-160">يتم استخدام الشعار الترويجي عادةً في فتحة رأس الصفحة أو فتحة رأس فرعي.</span><span class="sxs-lookup"><span data-stu-id="6a2a6-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6a2a6-161">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a2a6-161">Additional resources</span></span>

[<span data-ttu-id="6a2a6-162">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="6a2a6-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6a2a6-163">وحدة دوارة</span><span class="sxs-lookup"><span data-stu-id="6a2a6-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="6a2a6-164">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="6a2a6-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6a2a6-165">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="6a2a6-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="6a2a6-166">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="6a2a6-166">Video player module</span></span>](add-video-player.md)
