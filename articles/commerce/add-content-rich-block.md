---
title: وحدة نمطية لكتلة منسقة للمحتوى
description: يتناول هذا الموضوع الوحدات النمطية لكتلة تنسيق المحتوى ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785411"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="01d18-103">وحدة نمطية لكتلة منسقة للمحتوى</span><span class="sxs-lookup"><span data-stu-id="01d18-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="01d18-104">يتناول هذا الموضوع الوحدات النمطية لكتلة تنسيق المحتوى ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="01d18-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="01d18-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="01d18-105">Overview</span></span>

<span data-ttu-id="01d18-106">تُعد الوحدة النمطية لوحدة تنسيق المحتوى حاوية خاصة يُمكن وضع عنصر واحد أو أكثر من عناصر كتلة تنسيق المحتوى بداخلها.</span><span class="sxs-lookup"><span data-stu-id="01d18-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="01d18-107">تُستخدم الوحدات النمطية لكتلة تنسيق المحتوى للمحتوى السياقي في صفحة.</span><span class="sxs-lookup"><span data-stu-id="01d18-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="01d18-108">قد يكون هذا المحتوى معلوماتي أو ترويجي.</span><span class="sxs-lookup"><span data-stu-id="01d18-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="01d18-109">يتم التحكم في الوحدات النمطية لكتلة تنسيق المحتوى من خلال البيانات من نظام إدارة المحتوى (CMS) ويُمكن وضعها في أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="01d18-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="01d18-110">فهي وحدات نمطية مستقلة لا تعتمد على سياق الصفحة أو على أي وحدات نمطية أخرى.</span><span class="sxs-lookup"><span data-stu-id="01d18-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="01d18-111">أمثلة على الوحدات النمطية لكتلة تنسيق المحتوى في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="01d18-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="01d18-112">يُمكن استخدام الوحدات النمطية لكتلة تنسيق المحتوى بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="01d18-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="01d18-113">لإظهار ميزات المنتج في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="01d18-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="01d18-114">لأغراض إعلامية على أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="01d18-114">For informational purposes on any page.</span></span> <span data-ttu-id="01d18-115">على سبيل المثال، يُمكن لهذه الوحدات توضيح مزايا برامج الولاء وسرد سياسات الشحن والإرجاع والرد على الأسئلة الشائعة أو توفير محتوى "نبذة عنا".</span><span class="sxs-lookup"><span data-stu-id="01d18-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="01d18-116">لإضافة رسائل مخصصة في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="01d18-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="01d18-117">(على سبيل المثال، "شحن مجاني للأوامر التي تزيد عن 50 دولار").</span><span class="sxs-lookup"><span data-stu-id="01d18-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="01d18-118">بالنسبة لإخلاء المسؤولية وتفاصيل جهة الاتصال على صفحات تفاصيل المنتج وصفحات سلة التسوق وصفحات السداد مع الخروج والصفحات الأخرى (على سبيل المثال، "تخضع عمليات الشحن والإرجاع لسياسات المتجر").</span><span class="sxs-lookup"><span data-stu-id="01d18-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="01d18-119">خصائص الوحدة النمطية لكتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="01d18-119">Content rich block module properties</span></span>

| <span data-ttu-id="01d18-120">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="01d18-120">Property name</span></span>     | <span data-ttu-id="01d18-121">القيمة</span><span class="sxs-lookup"><span data-stu-id="01d18-121">Value</span></span>                                 | <span data-ttu-id="01d18-122">الخاصية</span><span class="sxs-lookup"><span data-stu-id="01d18-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="01d18-123">عدد الأعمدة</span><span class="sxs-lookup"><span data-stu-id="01d18-123">Number of columns</span></span> | <span data-ttu-id="01d18-124">رقم من **1** إلى **4**</span><span class="sxs-lookup"><span data-stu-id="01d18-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="01d18-125">عدد الأعمدة في كتلة تنسيق المحتوى.</span><span class="sxs-lookup"><span data-stu-id="01d18-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="01d18-126">يُمكن أن تكون أربعة أعمدة بحد أقصى.</span><span class="sxs-lookup"><span data-stu-id="01d18-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="01d18-127">العرض</span><span class="sxs-lookup"><span data-stu-id="01d18-127">Width</span></span>             | <span data-ttu-id="01d18-128">**ملء الحاوية** أو **ملء الشاشة**</span><span class="sxs-lookup"><span data-stu-id="01d18-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="01d18-129">إذا تم تعيين القيمة إلى **ملء الحاوية**، فمن ثم تقتصر العناصر داخل الحاوية على عرض الحاوية.</span><span class="sxs-lookup"><span data-stu-id="01d18-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="01d18-130">إذا لم تعيين القيمة إلى **ملء الشاشة**، فلن تقتصر العناصر على عرض الحاوية ولكن يُمكنها الانتقال إلى وضع ملء الشاشة.</span><span class="sxs-lookup"><span data-stu-id="01d18-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="01d18-131">يُمكنك تغيير القيمة لتحقيق التخطيط المرغوب.</span><span class="sxs-lookup"><span data-stu-id="01d18-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="01d18-132">خصائص الوحدة النمطية لعنصر كتلة تنسيق المحتوى</span><span class="sxs-lookup"><span data-stu-id="01d18-132">Content rich block item module properties</span></span>

| <span data-ttu-id="01d18-133">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="01d18-133">Property name</span></span> | <span data-ttu-id="01d18-134">القيمة</span><span class="sxs-lookup"><span data-stu-id="01d18-134">Value</span></span>          | <span data-ttu-id="01d18-135">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="01d18-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="01d18-136">فقرة</span><span class="sxs-lookup"><span data-stu-id="01d18-136">Paragraph</span></span>     | <span data-ttu-id="01d18-137">نص الفقرة</span><span class="sxs-lookup"><span data-stu-id="01d18-137">Paragraph text</span></span> | <span data-ttu-id="01d18-138">النص المُصاحب لكل عنصر كتلة تنسيق المحتوى.</span><span class="sxs-lookup"><span data-stu-id="01d18-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="01d18-139">يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل النص الغامق والمُسطر والمائل.</span><span class="sxs-lookup"><span data-stu-id="01d18-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="01d18-140">إضافة وحدة نمطية لكتلة منسقة للمحتوى إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="01d18-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="01d18-141">لإضافة وحدة نمطية لكتلة تنسيق المحتوى إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="01d18-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="01d18-142">إنشاء قالب صفحة تُسمى **قالب المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="01d18-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="01d18-143">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة الوحدة النمطية لكتلة تنسيق المحتوى.</span><span class="sxs-lookup"><span data-stu-id="01d18-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="01d18-144">قم بإيداع القالب ونشره.</span><span class="sxs-lookup"><span data-stu-id="01d18-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="01d18-145">استخدم قالب المحتوى الذي قمت بإنشاءه للتو لإنشاء صفحة تُسمى **صفحة المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="01d18-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="01d18-146">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة الوحدة النمطية لكتلة تنسيق المحتوى.</span><span class="sxs-lookup"><span data-stu-id="01d18-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="01d18-147">في خصائص الوحدة النمطية لكتلة تنسيق المحتوى، قم بتعيين عدد الأعمدة إلى **2**.</span><span class="sxs-lookup"><span data-stu-id="01d18-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="01d18-148">في الوحدة النمطية لكتلة تنسيق المحتوى، حدد **إضافة وحدة نمطية**، ثم أضف عنصر كتلة تنسيق المحتوى (على سبيل المثال، **item1**).</span><span class="sxs-lookup"><span data-stu-id="01d18-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="01d18-149">في عنصر كتلة تنسيق المحتوى الجديد، أضف نص فقرة.</span><span class="sxs-lookup"><span data-stu-id="01d18-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="01d18-150">في الوحدة النمطية لكتلة تنسيق المحتوى، حدد **إضافة وحدة نمطية**، ثم أضف عنصر كتلة تنسيق المحتوى (على سبيل المثال، **item2**).</span><span class="sxs-lookup"><span data-stu-id="01d18-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="01d18-151">في عنصر كتلة تنسيق المحتوى الجديد، أضف نص فقرة.</span><span class="sxs-lookup"><span data-stu-id="01d18-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="01d18-152">قم بحفظ الصفحة، ومعاينة التغييرات.</span><span class="sxs-lookup"><span data-stu-id="01d18-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="01d18-153">يجب أن تشاهد كتلتين نصيتين منسقتين في طريقة عرض العمودين.</span><span class="sxs-lookup"><span data-stu-id="01d18-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="01d18-154">قم بإيداع الصفحة ونشرها.</span><span class="sxs-lookup"><span data-stu-id="01d18-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="01d18-155">إذا قمت بإضافة عنصر كتلة تنسيق محتوى ثالث، فسوف يتم تكديسه أسفل العنصرين اللذين قمت بإضافتهم مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="01d18-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="01d18-156">من خلال تغيير عدد الأعمدة والعناصر في الحاوية، يُمكنك تحقيق تخطيطات مختلفة للمحتوى النصي.</span><span class="sxs-lookup"><span data-stu-id="01d18-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01d18-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="01d18-157">Additional resources</span></span>

[<span data-ttu-id="01d18-158">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="01d18-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="01d18-159">الوحدة النمطية للتنبيه</span><span class="sxs-lookup"><span data-stu-id="01d18-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="01d18-160">الوحدة النمطية الدوارة</span><span class="sxs-lookup"><span data-stu-id="01d18-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="01d18-161">الوحدة النمطية لوضع المحتوى</span><span class="sxs-lookup"><span data-stu-id="01d18-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="01d18-162">الوحدة النمطية لميزة</span><span class="sxs-lookup"><span data-stu-id="01d18-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="01d18-163">الوحدة النمطية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="01d18-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="01d18-164">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="01d18-164">Video player module</span></span>](add-video-player.md)

