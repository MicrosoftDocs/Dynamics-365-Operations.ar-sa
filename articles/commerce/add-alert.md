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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206573"
---
# <a name="promo-banner-module"></a><span data-ttu-id="ac8f5-103">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="ac8f5-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac8f5-104">يتناول هذا الموضوع وحدات الشعارات الترويجية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ac8f5-105">تستخدم وحدات الشعارات الترويجية لعرض رسائل المعلومات المضمنة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="ac8f5-106">ويُمكن استخدامها للعروض على مستوى الموقع التي تظهر في كافة صفحات موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="ac8f5-107">تدعم وحدات الشعارات الترويجية رسالة نصية وارتباطًا.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="ac8f5-108">إذا تمت إضافة رسائل متعددة إلى وحدة شعار ترويجي، تصبح شعارًا دوارًا يسمح للعملاء بالتنقل عبر الرسائل.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="ac8f5-109">يتم التحكم في وحدات الشعارات الترويجية بواسطة البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="ac8f5-110">أمثلة للاستخدام حول الشعارات الترويجية في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ac8f5-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="ac8f5-111">يمكن استخدام الشعارات الترويجية في رأس الموقع لإظهار العروض أو الرسائل الترويجية على مستوى الموقع، كما في الأمثلة التالية.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="ac8f5-112">"تنتهي المبيعات السنوية خلال 10 أيام" </span><span class="sxs-lookup"><span data-stu-id="ac8f5-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="ac8f5-113">"قم بحفظ big مع عمليات بيع العودة إلى المدرسة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-113">"Save big with back to school sale.</span></span> <span data-ttu-id="ac8f5-114">تسوق الآن. "</span><span class="sxs-lookup"><span data-stu-id="ac8f5-114">Shop Now."</span></span>

<span data-ttu-id="ac8f5-115">"تخفيضات خاصة لعيد الشكر!"</span><span class="sxs-lookup"><span data-stu-id="ac8f5-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="ac8f5-116">تبين الصورة التالية مثالاً عن شعار ترويجي.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-116">The following image shows an example of a promo banner.</span></span>

![مثال عن وحدة شعار ترويجي](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="ac8f5-118">خصائص وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="ac8f5-118">Promo banner module properties</span></span>

| <span data-ttu-id="ac8f5-119">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="ac8f5-119">Property name</span></span>             | <span data-ttu-id="ac8f5-120">قيمة</span><span class="sxs-lookup"><span data-stu-id="ac8f5-120">Value</span></span>                              | <span data-ttu-id="ac8f5-121">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="ac8f5-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="ac8f5-122">رسائل الافتة</span><span class="sxs-lookup"><span data-stu-id="ac8f5-122">Banner messages</span></span>           | <span data-ttu-id="ac8f5-123">نص وارتباطات</span><span class="sxs-lookup"><span data-stu-id="ac8f5-123">Text and links</span></span>                     | <span data-ttu-id="ac8f5-124">مجموعة من النصوص والارتباطات.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-124">An array of text and links.</span></span> |
| <span data-ttu-id="ac8f5-125">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="ac8f5-125">Autoplay</span></span>                  | <span data-ttu-id="ac8f5-126">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="ac8f5-126">**True** or **False**</span></span>              | <span data-ttu-id="ac8f5-127">قيمة تشير إلى ما إذا كان يتم التنقل عبر الرسائل بشكل تلقائي، إذا تم تكوين رسائل متعددة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="ac8f5-128">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="ac8f5-128">Slide transition interval</span></span> | <span data-ttu-id="ac8f5-129">عدد المللي ثواني</span><span class="sxs-lookup"><span data-stu-id="ac8f5-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="ac8f5-130">الفاصل الزمني الذي يتم استخدامه للتنقل بين الرسائل.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="ac8f5-131">السماح بالاستبعاد</span><span class="sxs-lookup"><span data-stu-id="ac8f5-131">Allow dismiss</span></span>             | <span data-ttu-id="ac8f5-132">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="ac8f5-132">**True** or **False**</span></span>              | <span data-ttu-id="ac8f5-133">إذا تم تعيين القيمة إلى **صحيح**، بإمكان العملاء استبعاد التنبيه.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="ac8f5-134">إظهار الذراع الدوار</span><span class="sxs-lookup"><span data-stu-id="ac8f5-134">Show carousel flipper</span></span>     | <span data-ttu-id="ac8f5-135">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="ac8f5-135">**True** or **False**</span></span>              | <span data-ttu-id="ac8f5-136">قيمة تشير إلى ما إذا كان يجب عرض القيمة الأذرع الدوارة، لتمكين العملاء من التنقل بطريقة يدوية عبر عناصر الشعار المتعددة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="ac8f5-137">محاذاة النص</span><span class="sxs-lookup"><span data-stu-id="ac8f5-137">Text alignment</span></span>            | <span data-ttu-id="ac8f5-138">**اليمين**, **اليسار**, أو **الوسط**</span><span class="sxs-lookup"><span data-stu-id="ac8f5-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="ac8f5-139">محاذاة النص في وحدة الشعار الترويجي.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="ac8f5-140">الارتباط</span><span class="sxs-lookup"><span data-stu-id="ac8f5-140">Link</span></span>                      | <span data-ttu-id="ac8f5-141">عنوان URL</span><span class="sxs-lookup"><span data-stu-id="ac8f5-141">A URL</span></span>                              | <span data-ttu-id="ac8f5-142">عنوان URL لارتباط اختياري.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="ac8f5-143">إضافة وحدة شعار ترويجي إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="ac8f5-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="ac8f5-144">لإضافة وحدة شعار ترويجي إلى صفحة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ac8f5-145">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="ac8f5-146">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب شعار ترويجي**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="ac8f5-147">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة **الصفحة الافتراضية** إلى فتحة **النص الأساسي**.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="ac8f5-148">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="ac8f5-149">استخدم القالب الذي أنشأته للتو لإنشاء صفحة مسماة **صفحة الشعار الترويجي**.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="ac8f5-150">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="ac8f5-151">في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="ac8f5-152">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة الشعار الترويجي إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="ac8f5-153">في إعدادات وحدة الشعار الترويجي، أضف رسالة شعار واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="ac8f5-154">بإمكان كل رسالة أن تتضمن نصًا مع ارتباط.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-154">Each message can have text together with a link.</span></span> <span data-ttu-id="ac8f5-155">يُمكنك تحرير الخصائص الأخرى إذا كنت ترغب في تخصيص الوحدة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="ac8f5-156">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="ac8f5-157">في أعلى الصفحة، يجب أن ترى تنبيهًا يُظهر النص الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="ac8f5-158">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="ac8f5-159">يتم استخدام الشعار الترويجي عادةً في فتحة رأس الصفحة أو فتحة رأس فرعي.</span><span class="sxs-lookup"><span data-stu-id="ac8f5-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ac8f5-160">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ac8f5-160">Additional resources</span></span>

[<span data-ttu-id="ac8f5-161">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="ac8f5-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ac8f5-162">وحدة دوارة</span><span class="sxs-lookup"><span data-stu-id="ac8f5-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="ac8f5-163">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="ac8f5-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ac8f5-164">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="ac8f5-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="ac8f5-165">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="ac8f5-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]