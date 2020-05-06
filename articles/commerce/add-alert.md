---
title: وحدة الشعار الترويجي
description: يتناول هذا الموضوع وحدات الشعارات الترويجية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269764"
---
# <a name="promo-banner-module"></a><span data-ttu-id="10cb3-103">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="10cb3-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="10cb3-104">يتناول هذا الموضوع وحدات الشعارات الترويجية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="10cb3-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10cb3-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="10cb3-105">Overview</span></span>

<span data-ttu-id="10cb3-106">تستخدم وحدات الشعارات الترويجية لعرض رسائل المعلومات المضمنة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="10cb3-107">ويُمكن استخدامها للعروض على مستوى الموقع التي تظهر في كافة صفحات موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="10cb3-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="10cb3-108">تدعم وحدات الشعارات الترويجية رسالة نصية وارتباطًا.</span><span class="sxs-lookup"><span data-stu-id="10cb3-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="10cb3-109">إذا تمت إضافة رسائل متعددة إلى وحدة شعار ترويجي، تصبح شعارًا دوارًا يسمح للعملاء بالتنقل عبر الرسائل.</span><span class="sxs-lookup"><span data-stu-id="10cb3-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="10cb3-110">يتم التحكم في وحدات الشعارات الترويجية بواسطة البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="10cb3-111">أمثلة للاستخدام حول الشعارات الترويجية في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="10cb3-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="10cb3-112">يمكن استخدام الشعارات الترويجية في رأس الموقع لإظهار العروض أو الرسائل الترويجية على مستوى الموقع، كما في الأمثلة التالية.</span><span class="sxs-lookup"><span data-stu-id="10cb3-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="10cb3-113">"تنتهي المبيعات السنوية خلال 10 أيام" </span><span class="sxs-lookup"><span data-stu-id="10cb3-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="10cb3-114">"قم بحفظ big مع عمليات بيع العودة إلى المدرسة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-114">"Save big with back to school sale.</span></span> <span data-ttu-id="10cb3-115">تسوق الآن. "</span><span class="sxs-lookup"><span data-stu-id="10cb3-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="10cb3-116">خصائص وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="10cb3-116">Promo banner module properties</span></span>

| <span data-ttu-id="10cb3-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="10cb3-117">Property name</span></span>             | <span data-ttu-id="10cb3-118">قيمة</span><span class="sxs-lookup"><span data-stu-id="10cb3-118">Value</span></span>                              | <span data-ttu-id="10cb3-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="10cb3-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="10cb3-120">رسائل الافتة</span><span class="sxs-lookup"><span data-stu-id="10cb3-120">Banner messages</span></span>           | <span data-ttu-id="10cb3-121">نص وارتباطات</span><span class="sxs-lookup"><span data-stu-id="10cb3-121">Text and links</span></span>                     | <span data-ttu-id="10cb3-122">مجموعة من النصوص والارتباطات.</span><span class="sxs-lookup"><span data-stu-id="10cb3-122">An array of text and links.</span></span> |
| <span data-ttu-id="10cb3-123">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="10cb3-123">Autoplay</span></span>                  | <span data-ttu-id="10cb3-124">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="10cb3-124">**True** or **False**</span></span>              | <span data-ttu-id="10cb3-125">قيمة تشير إلى ما إذا كان يتم التنقل عبر الرسائل بشكل تلقائي، إذا تم تكوين رسائل متعددة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="10cb3-126">فاصل المراحل الانتقالية للشرائح</span><span class="sxs-lookup"><span data-stu-id="10cb3-126">Slide transition interval</span></span> | <span data-ttu-id="10cb3-127">عدد المللي ثواني</span><span class="sxs-lookup"><span data-stu-id="10cb3-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="10cb3-128">الفاصل الزمني الذي يتم استخدامه للتنقل بين الرسائل.</span><span class="sxs-lookup"><span data-stu-id="10cb3-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="10cb3-129">السماح بالاستبعاد</span><span class="sxs-lookup"><span data-stu-id="10cb3-129">Allow dismiss</span></span>             | <span data-ttu-id="10cb3-130">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="10cb3-130">**True** or **False**</span></span>              | <span data-ttu-id="10cb3-131">إذا تم تعيين القيمة إلى **صحيح**، بإمكان العملاء استبعاد التنبيه.</span><span class="sxs-lookup"><span data-stu-id="10cb3-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="10cb3-132">إظهار الذراع الدوار</span><span class="sxs-lookup"><span data-stu-id="10cb3-132">Show carousel flipper</span></span>     | <span data-ttu-id="10cb3-133">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="10cb3-133">**True** or **False**</span></span>              | <span data-ttu-id="10cb3-134">قيمة تشير إلى ما إذا كان يجب عرض القيمة الأذرع الدوارة، لتمكين العملاء من التنقل بطريقة يدوية عبر عناصر الشعار المتعددة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="10cb3-135">محاذاة النص</span><span class="sxs-lookup"><span data-stu-id="10cb3-135">Text alignment</span></span>            | <span data-ttu-id="10cb3-136">**اليمين**, **اليسار**, أو **الوسط**</span><span class="sxs-lookup"><span data-stu-id="10cb3-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="10cb3-137">محاذاة النص في وحدة الشعار الترويجي.</span><span class="sxs-lookup"><span data-stu-id="10cb3-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="10cb3-138">الارتباط</span><span class="sxs-lookup"><span data-stu-id="10cb3-138">Link</span></span>                      | <span data-ttu-id="10cb3-139">عنوان URL</span><span class="sxs-lookup"><span data-stu-id="10cb3-139">A URL</span></span>                              | <span data-ttu-id="10cb3-140">عنوان URL لارتباط اختياري.</span><span class="sxs-lookup"><span data-stu-id="10cb3-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="10cb3-141">إضافة وحدة شعار ترويجي إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="10cb3-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="10cb3-142">لإضافة وحدة شعار ترويجي إلى صفحة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="10cb3-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="10cb3-143">حدد **جديد**، لإنشاء قالب صفحة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="10cb3-144">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب شعار ترويجي**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="10cb3-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="10cb3-145">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة **الصفحة الافتراضية** إلى فتحة **النص الأساسي**.</span><span class="sxs-lookup"><span data-stu-id="10cb3-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="10cb3-146">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="10cb3-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="10cb3-147">استخدم القالب الذي أنشأته للتو لإنشاء صفحة مسماة **صفحة الشعار الترويجي**.</span><span class="sxs-lookup"><span data-stu-id="10cb3-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="10cb3-148">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="10cb3-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="10cb3-149">في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="10cb3-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="10cb3-150">ضمن **المخطط التفصيلي للصفحة**، أضف وحدة الشعار الترويجي إلى وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="10cb3-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="10cb3-151">في إعدادات وحدة الشعار الترويجي، أضف رسالة شعار واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="10cb3-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="10cb3-152">بإمكان كل رسالة أن تتضمن نصًا مع ارتباط.</span><span class="sxs-lookup"><span data-stu-id="10cb3-152">Each message can have text together with a link.</span></span> <span data-ttu-id="10cb3-153">يُمكنك تحرير الخصائص الأخرى إذا كنت ترغب في تخصيص الوحدة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="10cb3-154">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="10cb3-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="10cb3-155">في أعلى الصفحة، يجب أن ترى تنبيهًا يُظهر النص الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="10cb3-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="10cb3-156">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="10cb3-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="10cb3-157">يتم استخدام الشعار الترويجي عادةً في فتحة رأس الصفحة أو فتحة رأس فرعي.</span><span class="sxs-lookup"><span data-stu-id="10cb3-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="10cb3-158">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="10cb3-158">Additional resources</span></span>

[<span data-ttu-id="10cb3-159">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="10cb3-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="10cb3-160">وحدة نمطية دوارة</span><span class="sxs-lookup"><span data-stu-id="10cb3-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="10cb3-161">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="10cb3-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="10cb3-162">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="10cb3-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="10cb3-163">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="10cb3-163">Video player module</span></span>](add-video-player.md)
