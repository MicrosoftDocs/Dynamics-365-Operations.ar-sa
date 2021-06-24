---
title: تحميل مقاطع فيديو
description: يصف هذا الموضوع كيفية تحميل الفيديوهات في منشئ موقع Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e3579b54c58898b79c84406480a3b58f541c4621
ms.sourcegitcommit: 257437a57e146496a49782bc8aad179c92fbf6e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/11/2021
ms.locfileid: "6224528"
---
# <a name="upload-videos"></a><span data-ttu-id="4f5f0-103">تحميل مقاطع فيديو</span><span class="sxs-lookup"><span data-stu-id="4f5f0-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f5f0-104">يصف هذا الموضوع كيفية تحميل الفيديوهات في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="4f5f0-105">تسمح لك مكتبة وسائط منشئ موقع Commerce بتحميل مقاطع الفيديو.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="4f5f0-106">يجب أن تقوم دائمًا بتحميل إصدار فيديو بأعلى معدل بت ودقة، إذ سيتم تحويل الفيديو بشكل تلقائي بحيث يكون ملائمًا لمنافذ عرض مختلفة ونقاط التوقف الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="4f5f0-107">معلومات الفيديو التي يتم تحديدها أثناء التحميل</span><span class="sxs-lookup"><span data-stu-id="4f5f0-107">Video information specified during upload</span></span>

<span data-ttu-id="4f5f0-108">عند تحميل مقطع فيديو ، يمكن تحديد المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="4f5f0-109">**العنوان والوصف والكلمات الأساسية**: بيانات تعريف الفيديو.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="4f5f0-110">**إنشاء تسميات توضيحية مغلقة تلقائيًا**: تحديد ما إذا كان يجب إنشاء تسميات توضيحية مغلقة تلقائيًا للفيديو (في حالة تدعيم اللغة الإنجليزية فقط).</span><span class="sxs-lookup"><span data-stu-id="4f5f0-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video (only English language is supported).</span></span> 
- <span data-ttu-id="4f5f0-111">**تسمية توضيحية مغلقة**: تحديد التسميات التوضيحية المغلقة‏‎ التي سيتم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="4f5f0-112">**صوت عادي**: تحديد مسار الصوت العادي المطلوب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="4f5f0-113">**صورة مصغرة**: تحديد صورة مصغرة للفيديو.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="4f5f0-114">إذا لم يتم تحديدها، فسيتم إنشاؤها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="4f5f0-115">**صوت وصفي**: تحديد مسار الصوت الوصفي المطلوب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="4f5f0-116">تحميل مقطع فيديو</span><span class="sxs-lookup"><span data-stu-id="4f5f0-116">Upload a video</span></span>

<span data-ttu-id="4f5f0-117">لتحميل فيديو في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4f5f0-118">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="4f5f0-119">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="4f5f0-120">في نافذة مستكشف الملفات، انتقل إلى ملف فيديو أو أكثر لتحميله، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="4f5f0-121">في مربع الحوار **تحميل عنصر الوسائط**، أدخل العنوان والنص البديل المطلوبين.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="4f5f0-122">أدخل وصفًا اختياريًا وكلمات أساسية اختيارية، وحدد فئة إذا أردت ذلك.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="4f5f0-123">إذا أردت نشر الصورة (الصور) مباشرةً بعد التحميل، فحدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**</span><span class="sxs-lookup"><span data-stu-id="4f5f0-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="4f5f0-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-124">Select **OK**.</span></span>

<span data-ttu-id="4f5f0-125">إذا كنت تعمل على تحميل أنواع متعددة من الأصول في وقت واحد (على سبيل المثال، صور ومقاطع فيديو)، في مربع الحوار **تحميل عنصر الوسائط**، ستتمكن من تحديد الكلمات الأساسية فقط، سواء كان يجب نشر الملفات مباشرةً بعد التحميل، وما إذا كان يجب إنشاء التسميات التوضيحية المغلقة لملفات الفيديو بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="4f5f0-126">ستشارك جميع الكلمات الأساسية نفسها.</span><span class="sxs-lookup"><span data-stu-id="4f5f0-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f5f0-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4f5f0-127">Additional resources</span></span>

[<span data-ttu-id="4f5f0-128">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="4f5f0-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="4f5f0-129">تحميل صور</span><span class="sxs-lookup"><span data-stu-id="4f5f0-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="4f5f0-130">تحميل الملفات</span><span class="sxs-lookup"><span data-stu-id="4f5f0-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="4f5f0-131">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="4f5f0-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="4f5f0-132">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="4f5f0-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="4f5f0-133">تحميل الملفات الثابتة وخدمتها</span><span class="sxs-lookup"><span data-stu-id="4f5f0-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
