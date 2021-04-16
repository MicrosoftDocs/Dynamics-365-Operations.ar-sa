---
title: تحميل ملفات غير صور ومقاطع فيديو
description: يصف هذا الموضوع كيفية تحميل ملفات ثنائية غير الصور ومقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 03/03/2020
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799243"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="d2519-103">تحميل ملفات غير الصور ومقاطع الفيديو</span><span class="sxs-lookup"><span data-stu-id="d2519-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2519-104">يصف هذا الموضوع كيفية تحميل ملفات غير الصور ومقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2519-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="d2519-105">تدعم مكتبة وسائط منشئ موقع Commerce تحميل أصول ثنائية غير الصور أو مقاطع الفيديو.</span><span class="sxs-lookup"><span data-stu-id="d2519-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="d2519-106">على سبيل المثال، قد تريد تحميل ملفات Microsoft Excel أو Microsoft Word أو Microsoft PowerPoint أو PDF.</span><span class="sxs-lookup"><span data-stu-id="d2519-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="d2519-107">أنواع الملفات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="d2519-107">The following document types are supported:</span></span>
- <span data-ttu-id="d2519-108">7Z</span><span class="sxs-lookup"><span data-stu-id="d2519-108">7Z</span></span>
- <span data-ttu-id="d2519-109">AVI</span><span class="sxs-lookup"><span data-stu-id="d2519-109">AVI</span></span>
- <span data-ttu-id="d2519-110">CS</span><span class="sxs-lookup"><span data-stu-id="d2519-110">CS</span></span>
- <span data-ttu-id="d2519-111">CSS</span><span class="sxs-lookup"><span data-stu-id="d2519-111">CSS</span></span>
- <span data-ttu-id="d2519-112">DOC</span><span class="sxs-lookup"><span data-stu-id="d2519-112">DOC</span></span>
- <span data-ttu-id="d2519-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="d2519-113">DOCX</span></span>
- <span data-ttu-id="d2519-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="d2519-114">EPUB</span></span>
- <span data-ttu-id="d2519-115">GIF</span><span class="sxs-lookup"><span data-stu-id="d2519-115">GIF</span></span>
- <span data-ttu-id="d2519-116">INDD</span><span class="sxs-lookup"><span data-stu-id="d2519-116">INDD</span></span>
- <span data-ttu-id="d2519-117">JAR</span><span class="sxs-lookup"><span data-stu-id="d2519-117">JAR</span></span>
- <span data-ttu-id="d2519-118">JPG</span><span class="sxs-lookup"><span data-stu-id="d2519-118">JPG</span></span>
- <span data-ttu-id="d2519-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="d2519-119">JPEG</span></span>
- <span data-ttu-id="d2519-120">JS</span><span class="sxs-lookup"><span data-stu-id="d2519-120">JS</span></span>
- <span data-ttu-id="d2519-121">MP3</span><span class="sxs-lookup"><span data-stu-id="d2519-121">MP3</span></span>
- <span data-ttu-id="d2519-122">MP4</span><span class="sxs-lookup"><span data-stu-id="d2519-122">MP4</span></span>
- <span data-ttu-id="d2519-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="d2519-123">MPEG</span></span>
- <span data-ttu-id="d2519-124">MPG</span><span class="sxs-lookup"><span data-stu-id="d2519-124">MPG</span></span>
- <span data-ttu-id="d2519-125">ODP</span><span class="sxs-lookup"><span data-stu-id="d2519-125">ODP</span></span>
- <span data-ttu-id="d2519-126">ODS</span><span class="sxs-lookup"><span data-stu-id="d2519-126">ODS</span></span>
- <span data-ttu-id="d2519-127">ODT</span><span class="sxs-lookup"><span data-stu-id="d2519-127">ODT</span></span>
- <span data-ttu-id="d2519-128">PDF</span><span class="sxs-lookup"><span data-stu-id="d2519-128">PDF</span></span>
- <span data-ttu-id="d2519-129">PNG</span><span class="sxs-lookup"><span data-stu-id="d2519-129">PNG</span></span>
- <span data-ttu-id="d2519-130">PPT</span><span class="sxs-lookup"><span data-stu-id="d2519-130">PPT</span></span>
- <span data-ttu-id="d2519-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="d2519-131">PPTX</span></span>
- <span data-ttu-id="d2519-132">PS</span><span class="sxs-lookup"><span data-stu-id="d2519-132">PS</span></span>
- <span data-ttu-id="d2519-133">QXP</span><span class="sxs-lookup"><span data-stu-id="d2519-133">QXP</span></span>
- <span data-ttu-id="d2519-134">RAR</span><span class="sxs-lookup"><span data-stu-id="d2519-134">RAR</span></span>
- <span data-ttu-id="d2519-135">RTF</span><span class="sxs-lookup"><span data-stu-id="d2519-135">RTF</span></span>
- <span data-ttu-id="d2519-136">SVG</span><span class="sxs-lookup"><span data-stu-id="d2519-136">SVG</span></span>
- <span data-ttu-id="d2519-137">TAR</span><span class="sxs-lookup"><span data-stu-id="d2519-137">TAR</span></span>
- <span data-ttu-id="d2519-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="d2519-138">TGZ</span></span>
- <span data-ttu-id="d2519-139">TXT</span><span class="sxs-lookup"><span data-stu-id="d2519-139">TXT</span></span>
- <span data-ttu-id="d2519-140">WMV</span><span class="sxs-lookup"><span data-stu-id="d2519-140">WMV</span></span>
- <span data-ttu-id="d2519-141">XLS</span><span class="sxs-lookup"><span data-stu-id="d2519-141">XLS</span></span>
- <span data-ttu-id="d2519-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="d2519-142">XLSX</span></span>
- <span data-ttu-id="d2519-143">XML</span><span class="sxs-lookup"><span data-stu-id="d2519-143">XML</span></span>
- <span data-ttu-id="d2519-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="d2519-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="d2519-145">تحميل ملف</span><span class="sxs-lookup"><span data-stu-id="d2519-145">Upload a file</span></span>

<span data-ttu-id="d2519-146">لتحميل ملف إلى منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d2519-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d2519-147">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="d2519-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="d2519-148">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="d2519-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="d2519-149">في "مستكشف الملفات"، حدد ملفًا أو أكثر، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="d2519-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="d2519-150">في مربع الحوار **تحميل عنصر الوسائط**، أدخل بيانات تعريف العنوان والوصف والكلمات الأساسية كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d2519-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="d2519-151">لنشر الملف (الملفات) مباشرةً بعد التحميل، حدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.</span><span class="sxs-lookup"><span data-stu-id="d2519-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="d2519-152">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d2519-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2519-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d2519-153">Additional resources</span></span>

[<span data-ttu-id="d2519-154">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="d2519-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="d2519-155">تحميل صور</span><span class="sxs-lookup"><span data-stu-id="d2519-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="d2519-156">تحميل فيديو</span><span class="sxs-lookup"><span data-stu-id="d2519-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="d2519-157">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="d2519-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="d2519-158">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="d2519-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="d2519-159">تحميل الملفات الثابتة وخدمتها</span><span class="sxs-lookup"><span data-stu-id="d2519-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
