---
title: وحدة التنبيه
description: يتناول هذا الموضوع وحدات التنبيه ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785342"
---
# <a name="alert-module"></a><span data-ttu-id="40619-103">وحدة التنبيه</span><span class="sxs-lookup"><span data-stu-id="40619-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="40619-104">يتناول هذا الموضوع وحدات التنبيه ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40619-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="40619-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="40619-105">Overview</span></span>

<span data-ttu-id="40619-106">تستخدم وحدة التنبيه لعرض رسائل المعلومات المضمنة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="40619-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="40619-107">تدعم وحدات التنبيه رسالة نصية وارتباط.</span><span class="sxs-lookup"><span data-stu-id="40619-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="40619-108">ويُمكن استخدامها للعروض على مستوى الموقع التي تظهر في كافة صفحات موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="40619-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="40619-109">يتم التحكم في وحدات التنبيه بواسطة البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="40619-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="40619-110">أمثلة على وحدات التنبيه في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="40619-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="40619-111">يُمكن استخدام وحدات التنبيه في عنوان الموقع للإشارة إلى العروض على مستوى الموقع أو الرسائل.</span><span class="sxs-lookup"><span data-stu-id="40619-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="40619-112">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="40619-112">Here are some examples:</span></span>

<span data-ttu-id="40619-113">"تنتهي المبيعات السنوية خلال 10 أيام" </span><span class="sxs-lookup"><span data-stu-id="40619-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="40619-114">"قم بحفظ big مع عمليات بيع العودة إلى المدرسة.</span><span class="sxs-lookup"><span data-stu-id="40619-114">"Save big with back to school sale.</span></span> <span data-ttu-id="40619-115">تسوق الآن. "</span><span class="sxs-lookup"><span data-stu-id="40619-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="40619-116">خصائص وحدة تنبيه</span><span class="sxs-lookup"><span data-stu-id="40619-116">Alert module properties</span></span>

| <span data-ttu-id="40619-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="40619-117">Property name</span></span>  | <span data-ttu-id="40619-118">القيمة</span><span class="sxs-lookup"><span data-stu-id="40619-118">Value</span></span>                              | <span data-ttu-id="40619-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="40619-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="40619-120">النص</span><span class="sxs-lookup"><span data-stu-id="40619-120">Text</span></span>           | <span data-ttu-id="40619-121">النص</span><span class="sxs-lookup"><span data-stu-id="40619-121">Text</span></span>                               | <span data-ttu-id="40619-122">الرسالة النصية التي تظهر في وحدة التنبيه.</span><span class="sxs-lookup"><span data-stu-id="40619-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="40619-123">محاذاة النص</span><span class="sxs-lookup"><span data-stu-id="40619-123">Text alignment</span></span> | <span data-ttu-id="40619-124">**اليمين**, **اليسار**, أو **الوسط**</span><span class="sxs-lookup"><span data-stu-id="40619-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="40619-125">القيمة التي تُحدد كيفية مُحاذاة النص في وحدة التنبيه.</span><span class="sxs-lookup"><span data-stu-id="40619-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="40619-126">رفض التنبيه</span><span class="sxs-lookup"><span data-stu-id="40619-126">Dismiss alert</span></span>  | <span data-ttu-id="40619-127">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="40619-127">**True** or **False**</span></span>              | <span data-ttu-id="40619-128">إذا تم تعيين القيمة إلى **صحيح**، يُمكن للعميل استبعاد التنبيه.</span><span class="sxs-lookup"><span data-stu-id="40619-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="40619-129">الارتباط</span><span class="sxs-lookup"><span data-stu-id="40619-129">Link</span></span>           | <span data-ttu-id="40619-130">عنوان URL</span><span class="sxs-lookup"><span data-stu-id="40619-130">URL</span></span>                                | <span data-ttu-id="40619-131">عنوان URL لارتباط اختياري.</span><span class="sxs-lookup"><span data-stu-id="40619-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="40619-132">إضافة وحدة تنبيه إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="40619-132">Add an alert module to a page</span></span> 

<span data-ttu-id="40619-133">لإضافة وحدة تنبيه إلى صفحة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="40619-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="40619-134">إنشاء قالب صفحة تُسمى **قالب تنبيه**.</span><span class="sxs-lookup"><span data-stu-id="40619-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="40619-135">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة وحدة تنبيه.</span><span class="sxs-lookup"><span data-stu-id="40619-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="40619-136">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="40619-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="40619-137">استخدم قالب التنبيه الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة التنبيه**.</span><span class="sxs-lookup"><span data-stu-id="40619-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="40619-138">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة تنبيه.</span><span class="sxs-lookup"><span data-stu-id="40619-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="40619-139">في إعدادات وحدة التنبيه، ادخل نص التنبيه.</span><span class="sxs-lookup"><span data-stu-id="40619-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="40619-140">يُمكنك تحرير الخصائص الأخرى إذا كنت ترغب في تخصيص وحدة التنبيه الأخرى.</span><span class="sxs-lookup"><span data-stu-id="40619-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="40619-141">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="40619-141">Save and preview the page.</span></span> <span data-ttu-id="40619-142">في أعلى الصفحة، يجب أن تُشاهد تنبيهًا يحتوي على النص الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="40619-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="40619-143">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="40619-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="40619-144">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="40619-144">Additional resources</span></span>

[<span data-ttu-id="40619-145">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="40619-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="40619-146">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="40619-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="40619-147">وحدة كتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="40619-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="40619-148">الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="40619-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="40619-149">الوحدة النمطية لميزة</span><span class="sxs-lookup"><span data-stu-id="40619-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="40619-150">الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="40619-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="40619-151">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="40619-151">Video player module</span></span>](add-video-player.md)
