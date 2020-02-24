---
title: الوحدة النمطية لمشغل الفيديو
description: يتناول هذا الموضوع الوحدات النمطية لمشغل الفيديو ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025633"
---
# <a name="video-player-module"></a><span data-ttu-id="961b5-103">الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="961b5-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="961b5-104">يتناول هذا الموضوع الوحدات النمطية لمشغل الفيديو ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="961b5-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="961b5-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="961b5-105">Overview</span></span>

<span data-ttu-id="961b5-106">تُستخدم الوحدة النمطية لمشغل الفيديو لدعم تشغيل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="961b5-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="961b5-107">ويمكن اضافتها إلى أي صفحة، شريطة أن يتم تحميل محتوى الفيديو وأن يكون متوفرًا في نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="961b5-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="961b5-108">تدعم الوحدة النمطية لمشغل الفيديو نوع الوسائط mp4.</span><span class="sxs-lookup"><span data-stu-id="961b5-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="961b5-109">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="961b5-109">Video player module</span></span>

<span data-ttu-id="961b5-110">يمكن استخدام الوحدة النمطية لمشغل الفيديو لإظهار مقاطع الفيديو علي موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="961b5-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="961b5-111">وهي تدعم كافة إمكانيات التشغيل، مثل وضع التشغيل، والإيقاف المؤقت، ووضع الحجم الكامل، وأوصاف الصوت والتسميات التوضيحية المغلقة.</span><span class="sxs-lookup"><span data-stu-id="961b5-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="961b5-112">كما تدعم الوحدة النمطية لمشغل الفيديو تخصيص التسميات التوضيحية المغلقة لتلبية معايير إمكانية الوصول الخاصة بـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="961b5-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="961b5-113">على سبيل المثال، يمكنك تخصيص حجم الخط ولون الخلفية.</span><span class="sxs-lookup"><span data-stu-id="961b5-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="961b5-114">تدعم وحدة مشغل الفيديو المسارات الصوتية الثانوية أيضًا.</span><span class="sxs-lookup"><span data-stu-id="961b5-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="961b5-115">عند تحميل مقطع فيديو إلى CMS، يمكن أيضًا تحميل مقطع صوتي ثانوي.</span><span class="sxs-lookup"><span data-stu-id="961b5-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="961b5-116">يمكن للوحدة النمطية لمشغل الفيديو تشغيل مسار الصوت الثانوي إذا قام المستخدم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="961b5-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="961b5-117">أمثله للوحدات النمطية لمشغل الفيديو في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="961b5-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="961b5-118">مقاطع فيديو إرشادية على صفحات تفاصيل المنتج أو صفحات التسويق</span><span class="sxs-lookup"><span data-stu-id="961b5-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="961b5-119">مقاطع الفيديو الترويجية أو مقاطع الفيديو الخاصة بالسياسات في أي صفحة تسويق</span><span class="sxs-lookup"><span data-stu-id="961b5-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="961b5-120">تسويق مقاطع الفيديو التي تبرز ميزات المنتج في صفحات تفاصيل المنتج أو صفحات التسويق</span><span class="sxs-lookup"><span data-stu-id="961b5-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="961b5-121">خصائص الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="961b5-121">Video player module properties</span></span>

| <span data-ttu-id="961b5-122">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="961b5-122">Property name</span></span>         | <span data-ttu-id="961b5-123">القيمة</span><span class="sxs-lookup"><span data-stu-id="961b5-123">Value</span></span>                               | <span data-ttu-id="961b5-124">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="961b5-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="961b5-125">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="961b5-125">Auto play</span></span>             | <span data-ttu-id="961b5-126">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-126">**True** or **False**</span></span>               | <span data-ttu-id="961b5-127">عند تعيين القيمة علي **صحيح**، يتم تشغيل الفيديو تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="961b5-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="961b5-128">كتم الصوت</span><span class="sxs-lookup"><span data-stu-id="961b5-128">Mute</span></span>                  | <span data-ttu-id="961b5-129">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-129">**True** or **False**</span></span>               | <span data-ttu-id="961b5-130">عند تعيين القيمة إلى **صحيح**، يتم كتم الصوت.</span><span class="sxs-lookup"><span data-stu-id="961b5-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="961b5-131">بالنسبة لهذا المشغل، تكون القيمة الافتراضية هي **خطأ**.</span><span class="sxs-lookup"><span data-stu-id="961b5-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="961b5-132">في المستعرض Chrome، يتم كتم صوت مقاطع الفيديو تلقائيًا، ويتم تشغيل الصوت فقط إذا قام المستخدم بتشغيل الفيديو يدويًا.</span><span class="sxs-lookup"><span data-stu-id="961b5-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="961b5-133">حلقة</span><span class="sxs-lookup"><span data-stu-id="961b5-133">Loop</span></span>                  | <span data-ttu-id="961b5-134">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-134">**True** or **False**</span></span>               | <span data-ttu-id="961b5-135">عند تعيين القيمة إلى **صحيح**، يتكرر الفيديو في حلقة.</span><span class="sxs-lookup"><span data-stu-id="961b5-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="961b5-136">الوسائط</span><span class="sxs-lookup"><span data-stu-id="961b5-136">Media</span></span>                 | <span data-ttu-id="961b5-137">مسار ملف الفيديو واسمه.</span><span class="sxs-lookup"><span data-stu-id="961b5-137">Video file path and name</span></span> | <span data-ttu-id="961b5-138">ملف الفيديو الذي يتم تشغيله في مشغل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="961b5-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="961b5-139">تشغيل وضع ‏‫ملء الشاشة‬</span><span class="sxs-lookup"><span data-stu-id="961b5-139">Play fullscreen</span></span>       | <span data-ttu-id="961b5-140">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-140">**True** or **False**</span></span>               | <span data-ttu-id="961b5-141">عند تعيين القيمة إلى **صحيح**، يتم تشغيل الفيديو في وضع ‏‫ملء الشاشة‬.</span><span class="sxs-lookup"><span data-stu-id="961b5-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="961b5-142">‏‫تشغيل/إيقاف مؤقت‬ المشغل</span><span class="sxs-lookup"><span data-stu-id="961b5-142">Play pause trigger</span></span>    | <span data-ttu-id="961b5-143">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-143">**True** or **False**</span></span>               | <span data-ttu-id="961b5-144">عند تعيين القيمة إلى **صحيح** ، يظهر الزر "تشغيل/إيقاف مؤقت" في الفيديو.</span><span class="sxs-lookup"><span data-stu-id="961b5-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="961b5-145">عناصر تحكم مشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="961b5-145">Video player controls</span></span> | <span data-ttu-id="961b5-146">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-146">**True** or **False**</span></span>               | <span data-ttu-id="961b5-147">عند تعيين القيمة إلى **صحيح**، تظهر كافة عناصر تحكم مشغل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="961b5-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="961b5-148">تتضمن عناصر التحكم هذه أزرار التشغيل والإيقاف المؤقت ومؤشر التقدم وخيارات التسميات التوضيحية المغلقة.</span><span class="sxs-lookup"><span data-stu-id="961b5-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="961b5-149">إخفاء صورة الملصق</span><span class="sxs-lookup"><span data-stu-id="961b5-149">Hide poster image</span></span>     | <span data-ttu-id="961b5-150">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="961b5-150">**True** or **False**</span></span>               | <span data-ttu-id="961b5-151">يمكن أن يكون للفيديو صورة أولية.</span><span class="sxs-lookup"><span data-stu-id="961b5-151">A video can have a poster frame.</span></span> <span data-ttu-id="961b5-152">عند تعيين قيمه هذه الخاصية إلى **صحيح**، يتم إخفاء الصورة الأولية.</span><span class="sxs-lookup"><span data-stu-id="961b5-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="961b5-153">مستوى القناع</span><span class="sxs-lookup"><span data-stu-id="961b5-153">Mask level</span></span>            | <span data-ttu-id="961b5-154">الرقم من **0** إلى **100**</span><span class="sxs-lookup"><span data-stu-id="961b5-154">A number from **0** through **100**</span></span> | <span data-ttu-id="961b5-155">القناع المطبق علي الفيديو للتنميط.</span><span class="sxs-lookup"><span data-stu-id="961b5-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="961b5-156">إضافة الوحدة النمطية لمشغل الفيديو إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="961b5-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="961b5-157">قبل إنشاء الوحدة النمطية لمشغل الفيديو، يجب أولاً تحميل فيديو إلى مكتبة الوسائط.</span><span class="sxs-lookup"><span data-stu-id="961b5-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="961b5-158">لإضافة الوحدة النمطية لمشغل الفيديو إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="961b5-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="961b5-159">إنشاء قالب صفحة يُسمى **قالب مشغل الفيديو**.</span><span class="sxs-lookup"><span data-stu-id="961b5-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="961b5-160">في الفتحة **الرئيسية** للصفحة الافتراضية، قم بإضافة وحدة الحاوية.</span><span class="sxs-lookup"><span data-stu-id="961b5-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="961b5-161">في الوحدة النمطية للحاوية، أضف مشغل الفيديو والوحدات النمطية لمشغل الفيديو المحيطي.</span><span class="sxs-lookup"><span data-stu-id="961b5-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="961b5-162">انشر القالب بعد الانتهاء من تحريره.</span><span class="sxs-lookup"><span data-stu-id="961b5-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="961b5-163">استخدم قالب مشغل الفيديو الذي أنشأته للتو لإنشاء صفحة مسماة **صفحة مشغل فيديو**.</span><span class="sxs-lookup"><span data-stu-id="961b5-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="961b5-164">في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة الوحدة النمطية لمشغل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="961b5-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="961b5-165">في جزء الخصائص للوحدة النمطية لمشغل الفيديو، حدد **إضافة فيديو**.</span><span class="sxs-lookup"><span data-stu-id="961b5-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="961b5-166">في مربع حوار **منتقي‏‎ الوسائط**، حدد مقطع فيديو ، ثم حدد **تحميل عنصر وسائط جديد**.</span><span class="sxs-lookup"><span data-stu-id="961b5-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="961b5-167">احفظ الصفحة وقم بمعاينتها.</span><span class="sxs-lookup"><span data-stu-id="961b5-167">Save and preview the page.</span></span> <span data-ttu-id="961b5-168">من المفترض أن ترى وحدة الفيديو في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="961b5-168">You should see the video module on the page.</span></span> <span data-ttu-id="961b5-169">يمكنك تغيير الإعدادات الإضافية لتخصيص سلوك الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="961b5-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="961b5-170">انشر الصفحة بعد الانتهاء من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="961b5-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="961b5-171">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="961b5-171">Additional resources</span></span>

[<span data-ttu-id="961b5-172">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="961b5-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="961b5-173">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="961b5-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="961b5-174">وحدة نمطية دوارة</span><span class="sxs-lookup"><span data-stu-id="961b5-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="961b5-175">وحدة كتلة النص‏‎</span><span class="sxs-lookup"><span data-stu-id="961b5-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="961b5-176">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="961b5-176">Content block module</span></span>](add-hero-module.md)
