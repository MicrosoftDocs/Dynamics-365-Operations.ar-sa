---
title: تحميل مقاطع فيديو
description: يصف هذا الموضوع كيفية تحميل مقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096967"
---
# <a name="upload-videos"></a><span data-ttu-id="3f3bd-103">تحميل مقاطع الفيديو</span><span class="sxs-lookup"><span data-stu-id="3f3bd-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f3bd-104">يصف هذا الموضوع كيفية تحميل مقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="3f3bd-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="3f3bd-105">Overview</span></span>

<span data-ttu-id="3f3bd-106">تسمح لك مكتبة وسائط منشئ موقع Commerce بتحميل مقاطع الفيديو.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="3f3bd-107">يجب أن تقوم دائمًا بتحميل إصدار فيديو بأعلى معدل بت ودقة، إذ سيتم تحويل الفيديو بشكل تلقائي بحيث يكون ملائمًا لمنافذ عرض مختلفة ونقاط التوقف الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="3f3bd-108">معلومات الفيديو التي يتم تحديدها أثناء التحميل</span><span class="sxs-lookup"><span data-stu-id="3f3bd-108">Video information specified during upload</span></span>

<span data-ttu-id="3f3bd-109">عند تحميل مقطع فيديو ، يمكن تحديد المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="3f3bd-110">**العنوان والوصف والكلمات الأساسية**: بيانات تعريف الفيديو.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="3f3bd-111">**إنشاء تسميات توضيحية مغلقة تلقائيًا**: تحديد ما إذا كان يجب إنشاء تسميات توضيحية مغلقة تلقائيًا للفيديو.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="3f3bd-112">**تسمية توضيحية مغلقة**: تحديد التسميات التوضيحية المغلقة‏‎ التي سيتم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="3f3bd-113">**صوت عادي**: تحديد مسار الصوت العادي المطلوب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="3f3bd-114">**صورة مصغرة**: تحديد صورة مصغرة للفيديو.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="3f3bd-115">إذا لم يتم تحديدها، فسيتم إنشاؤها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="3f3bd-116">**صوت وصفي**: تحديد مسار الصوت الوصفي المطلوب استخدامه.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="3f3bd-117">تحميل مقطع فيديو</span><span class="sxs-lookup"><span data-stu-id="3f3bd-117">Upload a video</span></span>

<span data-ttu-id="3f3bd-118">لتحميل فيديو في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3f3bd-119">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3f3bd-120">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="3f3bd-121">في نافذة مستكشف الملفات، انتقل إلى ملف فيديو أو أكثر لتحميله، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="3f3bd-122">في مربع الحوار **تحميل عنصر الوسائط**، أدخل العنوان والنص البديل المطلوبين.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="3f3bd-123">أدخل وصفًا اختياريًا وكلمات أساسية اختيارية، وحدد فئة إذا أردت ذلك.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="3f3bd-124">إذا أردت نشر الصورة (الصور) مباشرةً بعد التحميل، فحدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**</span><span class="sxs-lookup"><span data-stu-id="3f3bd-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="3f3bd-125">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-125">Select **OK**.</span></span>

<span data-ttu-id="3f3bd-126">إذا كنت تعمل على تحميل أنواع متعددة من الأصول في وقت واحد (على سبيل المثال، صور ومقاطع فيديو)، في مربع الحوار **تحميل عنصر الوسائط**، ستتمكن من تحديد الكلمات الأساسية فقط، سواء كان يجب نشر الملفات مباشرةً بعد التحميل، وما إذا كان يجب إنشاء التسميات التوضيحية المغلقة لملفات الفيديو بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="3f3bd-127">ستشارك جميع الكلمات الأساسية نفسها.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f3bd-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3f3bd-128">Additional resources</span></span>

[<span data-ttu-id="3f3bd-129">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="3f3bd-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3f3bd-130">تحميل الصور</span><span class="sxs-lookup"><span data-stu-id="3f3bd-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="3f3bd-131">تحميل الملفات</span><span class="sxs-lookup"><span data-stu-id="3f3bd-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="3f3bd-132">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="3f3bd-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3f3bd-133">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="3f3bd-133">Customize image focal points</span></span>](dam-custom-focal-point.md)
