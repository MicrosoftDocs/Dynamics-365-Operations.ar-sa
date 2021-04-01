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
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222527"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="05378-103">تحميل ملفات غير الصور ومقاطع الفيديو</span><span class="sxs-lookup"><span data-stu-id="05378-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05378-104">يصف هذا الموضوع كيفية تحميل ملفات غير الصور ومقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="05378-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="05378-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="05378-105">Overview</span></span>

<span data-ttu-id="05378-106">تدعم مكتبة وسائط منشئ موقع Commerce تحميل أصول ثنائية غير الصور أو مقاطع الفيديو.</span><span class="sxs-lookup"><span data-stu-id="05378-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="05378-107">على سبيل المثال، قد تريد تحميل ملفات Microsoft Excel أو Microsoft Word أو Microsoft PowerPoint أو PDF.</span><span class="sxs-lookup"><span data-stu-id="05378-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="05378-108">أنواع الملفات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="05378-108">The following document types are supported:</span></span>
- <span data-ttu-id="05378-109">7Z</span><span class="sxs-lookup"><span data-stu-id="05378-109">7Z</span></span>
- <span data-ttu-id="05378-110">AVI</span><span class="sxs-lookup"><span data-stu-id="05378-110">AVI</span></span>
- <span data-ttu-id="05378-111">CS</span><span class="sxs-lookup"><span data-stu-id="05378-111">CS</span></span>
- <span data-ttu-id="05378-112">CSS</span><span class="sxs-lookup"><span data-stu-id="05378-112">CSS</span></span>
- <span data-ttu-id="05378-113">DOC</span><span class="sxs-lookup"><span data-stu-id="05378-113">DOC</span></span>
- <span data-ttu-id="05378-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="05378-114">DOCX</span></span>
- <span data-ttu-id="05378-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="05378-115">EPUB</span></span>
- <span data-ttu-id="05378-116">GIF</span><span class="sxs-lookup"><span data-stu-id="05378-116">GIF</span></span>
- <span data-ttu-id="05378-117">INDD</span><span class="sxs-lookup"><span data-stu-id="05378-117">INDD</span></span>
- <span data-ttu-id="05378-118">JAR</span><span class="sxs-lookup"><span data-stu-id="05378-118">JAR</span></span>
- <span data-ttu-id="05378-119">JPG</span><span class="sxs-lookup"><span data-stu-id="05378-119">JPG</span></span>
- <span data-ttu-id="05378-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="05378-120">JPEG</span></span>
- <span data-ttu-id="05378-121">JS</span><span class="sxs-lookup"><span data-stu-id="05378-121">JS</span></span>
- <span data-ttu-id="05378-122">MP3</span><span class="sxs-lookup"><span data-stu-id="05378-122">MP3</span></span>
- <span data-ttu-id="05378-123">MP4</span><span class="sxs-lookup"><span data-stu-id="05378-123">MP4</span></span>
- <span data-ttu-id="05378-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="05378-124">MPEG</span></span>
- <span data-ttu-id="05378-125">MPG</span><span class="sxs-lookup"><span data-stu-id="05378-125">MPG</span></span>
- <span data-ttu-id="05378-126">ODP</span><span class="sxs-lookup"><span data-stu-id="05378-126">ODP</span></span>
- <span data-ttu-id="05378-127">ODS</span><span class="sxs-lookup"><span data-stu-id="05378-127">ODS</span></span>
- <span data-ttu-id="05378-128">ODT</span><span class="sxs-lookup"><span data-stu-id="05378-128">ODT</span></span>
- <span data-ttu-id="05378-129">PDF</span><span class="sxs-lookup"><span data-stu-id="05378-129">PDF</span></span>
- <span data-ttu-id="05378-130">PNG</span><span class="sxs-lookup"><span data-stu-id="05378-130">PNG</span></span>
- <span data-ttu-id="05378-131">PPT</span><span class="sxs-lookup"><span data-stu-id="05378-131">PPT</span></span>
- <span data-ttu-id="05378-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="05378-132">PPTX</span></span>
- <span data-ttu-id="05378-133">PS</span><span class="sxs-lookup"><span data-stu-id="05378-133">PS</span></span>
- <span data-ttu-id="05378-134">QXP</span><span class="sxs-lookup"><span data-stu-id="05378-134">QXP</span></span>
- <span data-ttu-id="05378-135">RAR</span><span class="sxs-lookup"><span data-stu-id="05378-135">RAR</span></span>
- <span data-ttu-id="05378-136">RTF</span><span class="sxs-lookup"><span data-stu-id="05378-136">RTF</span></span>
- <span data-ttu-id="05378-137">SVG</span><span class="sxs-lookup"><span data-stu-id="05378-137">SVG</span></span>
- <span data-ttu-id="05378-138">TAR</span><span class="sxs-lookup"><span data-stu-id="05378-138">TAR</span></span>
- <span data-ttu-id="05378-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="05378-139">TGZ</span></span>
- <span data-ttu-id="05378-140">TXT</span><span class="sxs-lookup"><span data-stu-id="05378-140">TXT</span></span>
- <span data-ttu-id="05378-141">WMV</span><span class="sxs-lookup"><span data-stu-id="05378-141">WMV</span></span>
- <span data-ttu-id="05378-142">XLS</span><span class="sxs-lookup"><span data-stu-id="05378-142">XLS</span></span>
- <span data-ttu-id="05378-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="05378-143">XLSX</span></span>
- <span data-ttu-id="05378-144">XML</span><span class="sxs-lookup"><span data-stu-id="05378-144">XML</span></span>
- <span data-ttu-id="05378-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="05378-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="05378-146">تحميل ملف</span><span class="sxs-lookup"><span data-stu-id="05378-146">Upload a file</span></span>

<span data-ttu-id="05378-147">لتحميل ملف إلى منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="05378-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="05378-148">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="05378-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="05378-149">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="05378-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="05378-150">في "مستكشف الملفات"، حدد ملفًا أو أكثر، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="05378-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="05378-151">في مربع الحوار **تحميل عنصر الوسائط**، أدخل بيانات تعريف العنوان والوصف والكلمات الأساسية كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="05378-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="05378-152">لنشر الملف (الملفات) مباشرةً بعد التحميل، حدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.</span><span class="sxs-lookup"><span data-stu-id="05378-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="05378-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="05378-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05378-154">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="05378-154">Additional resources</span></span>

[<span data-ttu-id="05378-155">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="05378-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="05378-156">تحميل صور</span><span class="sxs-lookup"><span data-stu-id="05378-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="05378-157">تحميل فيديو</span><span class="sxs-lookup"><span data-stu-id="05378-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="05378-158">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="05378-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="05378-159">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="05378-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="05378-160">تحميل الملفات الثابتة وخدمتها</span><span class="sxs-lookup"><span data-stu-id="05378-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]