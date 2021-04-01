---
title: الوحدة النمطية لمشغل الفيديو
description: يتناول هذا الموضوع الوحدات النمطية لمشغل الفيديو ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 13072c8d6839fef1ab0dd55d626c23a2a1084d4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209169"
---
# <a name="video-player-module"></a><span data-ttu-id="2d463-103">وحدة مشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="2d463-103">Video player module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d463-104">يتناول هذا الموضوع الوحدات النمطية لمشغل الفيديو ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d463-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2d463-105">تُستخدم الوحدة النمطية لمشغل الفيديو لدعم تشغيل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="2d463-105">The video player module is used to support video playback.</span></span> <span data-ttu-id="2d463-106">ويمكن اضافتها إلى أي صفحة، شريطة أن يتم تحميل محتوى الفيديو وأن يكون متوفرًا في نظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="2d463-106">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="2d463-107">تدعم الوحدة النمطية لمشغل الفيديو نوع الوسائط mp4.</span><span class="sxs-lookup"><span data-stu-id="2d463-107">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="2d463-108">وحدة نمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="2d463-108">Video player module</span></span>

<span data-ttu-id="2d463-109">يمكن استخدام الوحدة النمطية لمشغل الفيديو لإظهار مقاطع الفيديو على موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2d463-109">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="2d463-110">وهي تدعم كافة إمكانيات التشغيل، مثل وضع التشغيل، والإيقاف المؤقت، ووضع الحجم الكامل، وأوصاف الصوت والتسميات التوضيحية المغلقة.</span><span class="sxs-lookup"><span data-stu-id="2d463-110">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="2d463-111">كما تدعم الوحدة النمطية لمشغل الفيديو تخصيص التسميات التوضيحية المغلقة لتلبية معايير إمكانية الوصول الخاصة بـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2d463-111">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="2d463-112">على سبيل المثال، يمكنك تخصيص حجم الخط ولون الخلفية.</span><span class="sxs-lookup"><span data-stu-id="2d463-112">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="2d463-113">تدعم وحدة مشغل الفيديو المسارات الصوتية الثانوية أيضًا.</span><span class="sxs-lookup"><span data-stu-id="2d463-113">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="2d463-114">عند تحميل مقطع فيديو إلى CMS، يمكن أيضًا تحميل مقطع صوتي ثانوي.</span><span class="sxs-lookup"><span data-stu-id="2d463-114">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="2d463-115">يمكن للوحدة النمطية لمشغل الفيديو تشغيل مسار الصوت الثانوي إذا قام المستخدم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="2d463-115">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="2d463-116">أمثله للوحدات النمطية لمشغل الفيديو في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2d463-116">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="2d463-117">مقاطع فيديو إرشادية على صفحات تفاصيل المنتج أو صفحات التسويق</span><span class="sxs-lookup"><span data-stu-id="2d463-117">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="2d463-118">مقاطع الفيديو الترويجية أو مقاطع الفيديو الخاصة بالسياسات في أي صفحة تسويق</span><span class="sxs-lookup"><span data-stu-id="2d463-118">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="2d463-119">تسويق مقاطع الفيديو التي تبرز ميزات المنتج في صفحات تفاصيل المنتج أو صفحات التسويق</span><span class="sxs-lookup"><span data-stu-id="2d463-119">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="2d463-120">تعرض الصورة التالية مثالاُ عن وحدة مشغل الفيديو في صفحة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="2d463-120">The following image shows an example of a video player module on a home page.</span></span>

![مثال عن وحدة مشغل الفيديو](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="2d463-122">خصائص الوحدة النمطية لمشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="2d463-122">Video player module properties</span></span>

| <span data-ttu-id="2d463-123">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="2d463-123">Property name</span></span>         | <span data-ttu-id="2d463-124">قيمة</span><span class="sxs-lookup"><span data-stu-id="2d463-124">Value</span></span>                               | <span data-ttu-id="2d463-125">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2d463-125">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="2d463-126">تشغيل تلقائي</span><span class="sxs-lookup"><span data-stu-id="2d463-126">Auto play</span></span>             | <span data-ttu-id="2d463-127">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-127">**True** or **False**</span></span>               | <span data-ttu-id="2d463-128">عند تعيين القيمة على **صحيح**، يتم تشغيل الفيديو تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="2d463-128">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="2d463-129">كتم الصوت</span><span class="sxs-lookup"><span data-stu-id="2d463-129">Mute</span></span>                  | <span data-ttu-id="2d463-130">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-130">**True** or **False**</span></span>               | <span data-ttu-id="2d463-131">عند تعيين القيمة إلى **صحيح**، يتم كتم الصوت.</span><span class="sxs-lookup"><span data-stu-id="2d463-131">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="2d463-132">بالنسبة لهذا المشغل، تكون القيمة الافتراضية هي **خطأ**.</span><span class="sxs-lookup"><span data-stu-id="2d463-132">For this player, the default value is **False**.</span></span> <span data-ttu-id="2d463-133">في المستعرض Chrome، يتم كتم صوت مقاطع الفيديو تلقائيًا، ويتم تشغيل الصوت فقط إذا قام المستخدم بتشغيل الفيديو يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2d463-133">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="2d463-134">حلقة</span><span class="sxs-lookup"><span data-stu-id="2d463-134">Loop</span></span>                  | <span data-ttu-id="2d463-135">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-135">**True** or **False**</span></span>               | <span data-ttu-id="2d463-136">عند تعيين القيمة إلى **صحيح**، يتكرر الفيديو في حلقة.</span><span class="sxs-lookup"><span data-stu-id="2d463-136">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="2d463-137">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2d463-137">Media</span></span>                 | <span data-ttu-id="2d463-138">مسار ملف الفيديو واسمه.</span><span class="sxs-lookup"><span data-stu-id="2d463-138">Video file path and name</span></span> | <span data-ttu-id="2d463-139">ملف الفيديو الذي يتم تشغيله في مشغل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="2d463-139">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="2d463-140">تشغيل وضع ‏‫ملء الشاشة‬</span><span class="sxs-lookup"><span data-stu-id="2d463-140">Play fullscreen</span></span>       | <span data-ttu-id="2d463-141">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-141">**True** or **False**</span></span>               | <span data-ttu-id="2d463-142">عند تعيين القيمة إلى **صحيح**، يتم تشغيل الفيديو في وضع ‏‫ملء الشاشة‬.</span><span class="sxs-lookup"><span data-stu-id="2d463-142">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="2d463-143">‏‫تشغيل/إيقاف مؤقت‬ المشغل</span><span class="sxs-lookup"><span data-stu-id="2d463-143">Play pause trigger</span></span>    | <span data-ttu-id="2d463-144">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-144">**True** or **False**</span></span>               | <span data-ttu-id="2d463-145">عند تعيين القيمة إلى **صحيح**، يظهر الزر "تشغيل/إيقاف مؤقت" في الفيديو.</span><span class="sxs-lookup"><span data-stu-id="2d463-145">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="2d463-146">عناصر تحكم مشغل الفيديو</span><span class="sxs-lookup"><span data-stu-id="2d463-146">Video player controls</span></span> | <span data-ttu-id="2d463-147">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-147">**True** or **False**</span></span>               | <span data-ttu-id="2d463-148">عند تعيين القيمة إلى **صحيح**، تظهر كافة عناصر تحكم مشغل الفيديو.</span><span class="sxs-lookup"><span data-stu-id="2d463-148">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="2d463-149">تتضمن عناصر التحكم هذه أزرار التشغيل والإيقاف المؤقت ومؤشر التقدم وخيارات التسميات التوضيحية المغلقة.</span><span class="sxs-lookup"><span data-stu-id="2d463-149">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="2d463-150">إخفاء صورة الملصق</span><span class="sxs-lookup"><span data-stu-id="2d463-150">Hide poster image</span></span>     | <span data-ttu-id="2d463-151">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="2d463-151">**True** or **False**</span></span>               | <span data-ttu-id="2d463-152">يمكن أن يكون للفيديو صورة أولية.</span><span class="sxs-lookup"><span data-stu-id="2d463-152">A video can have a poster frame.</span></span> <span data-ttu-id="2d463-153">عند تعيين قيمه هذه الخاصية إلى **صحيح**، يتم إخفاء الصورة الأولية.</span><span class="sxs-lookup"><span data-stu-id="2d463-153">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="2d463-154">مستوى القناع</span><span class="sxs-lookup"><span data-stu-id="2d463-154">Mask level</span></span>            | <span data-ttu-id="2d463-155">الرقم من **0** إلى **100**</span><span class="sxs-lookup"><span data-stu-id="2d463-155">A number from **0** through **100**</span></span> | <span data-ttu-id="2d463-156">القناع المطبق على الفيديو للتنميط.</span><span class="sxs-lookup"><span data-stu-id="2d463-156">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="2d463-157">إضافة الوحدة النمطية لمشغل الفيديو إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="2d463-157">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="2d463-158">قبل إنشاء الوحدة النمطية لمشغل الفيديو، يجب أولاً تحميل فيديو إلى مكتبة الوسائط.</span><span class="sxs-lookup"><span data-stu-id="2d463-158">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="2d463-159">لإضافة الوحدة النمطية لمشغل الفيديو إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2d463-159">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2d463-160">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="2d463-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2d463-161">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب مشغل الفيديو**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-161">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-162">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2d463-162">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d463-163">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-163">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-164">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2d463-164">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d463-165">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-165">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-166">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2d463-166">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d463-167">في مربع الحوار **إضافة وحدة**، حدد وحدة **مشغل الفيديو‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-167">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-168">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="2d463-168">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="2d463-169">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="2d463-169">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2d463-170">في مربع الحوار **اختيار قالب**، حدد قالب مشغل الفيديو الذي أنشأته.</span><span class="sxs-lookup"><span data-stu-id="2d463-170">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="2d463-171">ضمن **اسم الصفحة**، أدخل **صفحة مشغل الفيديو**، ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="2d463-171">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-172">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="2d463-172">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d463-173">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-173">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-174">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2d463-174">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d463-175">في مربع الحوار **إضافة وحدة**، حدد وحدة **مشغل الفيديو‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-175">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-176">في جزء الخصائص لوحدة مشغل الفيديو، حدد **إضافة فيديو**.</span><span class="sxs-lookup"><span data-stu-id="2d463-176">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="2d463-177">في مربع حوار **منتقي‏‎ الوسائط**، حدد مقطع فيديو، ثم حدد **تحميل عنصر وسائط جديد**.</span><span class="sxs-lookup"><span data-stu-id="2d463-177">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="2d463-178">في "مستكشف الملفات"، حدد ملف فيديو، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="2d463-178">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="2d463-179">في مربع الحوار **تحميل عنصر الوسائط**، أدخل عنوانًا ومعلومات أخرى كما تقتضي الحاجة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-179">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="2d463-180">في مربع حوار **منتقي الوسائط**، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="2d463-180">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="2d463-181">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2d463-181">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2d463-182">من المفترض أن ترى وحدة الفيديو في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2d463-182">You should see the video module on the page.</span></span> <span data-ttu-id="2d463-183">يمكنك تغيير الإعدادات الإضافية لتخصيص سلوك الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="2d463-183">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="2d463-184">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="2d463-184">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2d463-185">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2d463-185">Additional resources</span></span>

[<span data-ttu-id="2d463-186">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2d463-186">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2d463-187">وحدة الشعار الترويجي</span><span class="sxs-lookup"><span data-stu-id="2d463-187">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2d463-188">وحدة دوارة</span><span class="sxs-lookup"><span data-stu-id="2d463-188">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2d463-189">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="2d463-189">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2d463-190">وحدة كتلة المحتوى</span><span class="sxs-lookup"><span data-stu-id="2d463-190">Content block module</span></span>](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]