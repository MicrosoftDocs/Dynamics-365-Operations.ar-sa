---
title: تحميل ملفات غير صور ومقاطع فيديو
description: يصف هذا الموضوع كيفية تحميل ملفات ثنائية غير الصور ومقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995760"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="f9e38-103">تحميل ملفات غير صور ومقاطع فيديو</span><span class="sxs-lookup"><span data-stu-id="f9e38-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9e38-104">يصف هذا الموضوع كيفية تحميل ملفات غير الصور ومقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f9e38-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="f9e38-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="f9e38-105">Overview</span></span>

<span data-ttu-id="f9e38-106">تدعم مكتبة وسائط منشئ موقع Commerce تحميل أصول ثنائية غير الصور أو مقاطع الفيديو.</span><span class="sxs-lookup"><span data-stu-id="f9e38-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="f9e38-107">على سبيل المثال، قد تريد تحميل ملفات Microsoft Excel أو Microsoft Word أو Microsoft PowerPoint أو PDF.</span><span class="sxs-lookup"><span data-stu-id="f9e38-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="f9e38-108">أنواع الملفات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="f9e38-108">The following document types are supported:</span></span>
- <span data-ttu-id="f9e38-109">7Z</span><span class="sxs-lookup"><span data-stu-id="f9e38-109">7Z</span></span>
- <span data-ttu-id="f9e38-110">AVI</span><span class="sxs-lookup"><span data-stu-id="f9e38-110">AVI</span></span>
- <span data-ttu-id="f9e38-111">CS</span><span class="sxs-lookup"><span data-stu-id="f9e38-111">CS</span></span>
- <span data-ttu-id="f9e38-112">CSS</span><span class="sxs-lookup"><span data-stu-id="f9e38-112">CSS</span></span>
- <span data-ttu-id="f9e38-113">DOC</span><span class="sxs-lookup"><span data-stu-id="f9e38-113">DOC</span></span>
- <span data-ttu-id="f9e38-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="f9e38-114">DOCX</span></span>
- <span data-ttu-id="f9e38-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="f9e38-115">EPUB</span></span>
- <span data-ttu-id="f9e38-116">GIF</span><span class="sxs-lookup"><span data-stu-id="f9e38-116">GIF</span></span>
- <span data-ttu-id="f9e38-117">INDD</span><span class="sxs-lookup"><span data-stu-id="f9e38-117">INDD</span></span>
- <span data-ttu-id="f9e38-118">JAR</span><span class="sxs-lookup"><span data-stu-id="f9e38-118">JAR</span></span>
- <span data-ttu-id="f9e38-119">JPG</span><span class="sxs-lookup"><span data-stu-id="f9e38-119">JPG</span></span>
- <span data-ttu-id="f9e38-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="f9e38-120">JPEG</span></span>
- <span data-ttu-id="f9e38-121">JS</span><span class="sxs-lookup"><span data-stu-id="f9e38-121">JS</span></span>
- <span data-ttu-id="f9e38-122">MP3</span><span class="sxs-lookup"><span data-stu-id="f9e38-122">MP3</span></span>
- <span data-ttu-id="f9e38-123">MP4</span><span class="sxs-lookup"><span data-stu-id="f9e38-123">MP4</span></span>
- <span data-ttu-id="f9e38-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="f9e38-124">MPEG</span></span>
- <span data-ttu-id="f9e38-125">MPG</span><span class="sxs-lookup"><span data-stu-id="f9e38-125">MPG</span></span>
- <span data-ttu-id="f9e38-126">ODP</span><span class="sxs-lookup"><span data-stu-id="f9e38-126">ODP</span></span>
- <span data-ttu-id="f9e38-127">ODS</span><span class="sxs-lookup"><span data-stu-id="f9e38-127">ODS</span></span>
- <span data-ttu-id="f9e38-128">ODT</span><span class="sxs-lookup"><span data-stu-id="f9e38-128">ODT</span></span>
- <span data-ttu-id="f9e38-129">PDF</span><span class="sxs-lookup"><span data-stu-id="f9e38-129">PDF</span></span>
- <span data-ttu-id="f9e38-130">PNG</span><span class="sxs-lookup"><span data-stu-id="f9e38-130">PNG</span></span>
- <span data-ttu-id="f9e38-131">PPT</span><span class="sxs-lookup"><span data-stu-id="f9e38-131">PPT</span></span>
- <span data-ttu-id="f9e38-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="f9e38-132">PPTX</span></span>
- <span data-ttu-id="f9e38-133">PS</span><span class="sxs-lookup"><span data-stu-id="f9e38-133">PS</span></span>
- <span data-ttu-id="f9e38-134">QXP</span><span class="sxs-lookup"><span data-stu-id="f9e38-134">QXP</span></span>
- <span data-ttu-id="f9e38-135">RAR</span><span class="sxs-lookup"><span data-stu-id="f9e38-135">RAR</span></span>
- <span data-ttu-id="f9e38-136">RTF</span><span class="sxs-lookup"><span data-stu-id="f9e38-136">RTF</span></span>
- <span data-ttu-id="f9e38-137">SVG</span><span class="sxs-lookup"><span data-stu-id="f9e38-137">SVG</span></span>
- <span data-ttu-id="f9e38-138">TAR</span><span class="sxs-lookup"><span data-stu-id="f9e38-138">TAR</span></span>
- <span data-ttu-id="f9e38-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="f9e38-139">TGZ</span></span>
- <span data-ttu-id="f9e38-140">TXT</span><span class="sxs-lookup"><span data-stu-id="f9e38-140">TXT</span></span>
- <span data-ttu-id="f9e38-141">WMV</span><span class="sxs-lookup"><span data-stu-id="f9e38-141">WMV</span></span>
- <span data-ttu-id="f9e38-142">XLS</span><span class="sxs-lookup"><span data-stu-id="f9e38-142">XLS</span></span>
- <span data-ttu-id="f9e38-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="f9e38-143">XLSX</span></span>
- <span data-ttu-id="f9e38-144">XML</span><span class="sxs-lookup"><span data-stu-id="f9e38-144">XML</span></span>
- <span data-ttu-id="f9e38-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="f9e38-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="f9e38-146">تحميل ملف</span><span class="sxs-lookup"><span data-stu-id="f9e38-146">Upload a file</span></span>

<span data-ttu-id="f9e38-147">لتحميل ملف إلى منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f9e38-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f9e38-148">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="f9e38-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f9e38-149">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="f9e38-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="f9e38-150">في "مستكشف الملفات"، حدد ملفًا أو أكثر، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="f9e38-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="f9e38-151">في مربع الحوار **تحميل عنصر الوسائط**، أدخل بيانات تعريف العنوان والوصف والكلمات الأساسية كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="f9e38-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="f9e38-152">لنشر الملف (الملفات) مباشرةً بعد التحميل، حدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.</span><span class="sxs-lookup"><span data-stu-id="f9e38-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="f9e38-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f9e38-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9e38-154">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f9e38-154">Additional resources</span></span>

[<span data-ttu-id="f9e38-155">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="f9e38-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="f9e38-156">تحميل صور</span><span class="sxs-lookup"><span data-stu-id="f9e38-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="f9e38-157">تحميل فيديو</span><span class="sxs-lookup"><span data-stu-id="f9e38-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="f9e38-158">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="f9e38-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="f9e38-159">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="f9e38-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="f9e38-160">تحميل الملفات الثابتة وخدمتها</span><span class="sxs-lookup"><span data-stu-id="f9e38-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
