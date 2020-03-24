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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096964"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="ab939-103">تحميل ملفات غير صور ومقاطع فيديو</span><span class="sxs-lookup"><span data-stu-id="ab939-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab939-104">يصف هذا الموضوع كيفية تحميل ملفات غير الصور ومقاطع الفيديو في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab939-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="ab939-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="ab939-105">Overview</span></span>

<span data-ttu-id="ab939-106">تدعم مكتبة وسائط منشئ موقع Commerce تحميل أصول ثنائية غير الصور أو مقاطع الفيديو.</span><span class="sxs-lookup"><span data-stu-id="ab939-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="ab939-107">على سبيل المثال، قد تريد تحميل ملفات Microsoft Excel أو Microsoft Word أو Microsoft PowerPoint أو PDF.</span><span class="sxs-lookup"><span data-stu-id="ab939-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="ab939-108">أنواع الملفات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="ab939-108">The following document types are supported:</span></span>
- <span data-ttu-id="ab939-109">7Z</span><span class="sxs-lookup"><span data-stu-id="ab939-109">7Z</span></span>
- <span data-ttu-id="ab939-110">AVI</span><span class="sxs-lookup"><span data-stu-id="ab939-110">AVI</span></span>
- <span data-ttu-id="ab939-111">CS</span><span class="sxs-lookup"><span data-stu-id="ab939-111">CS</span></span>
- <span data-ttu-id="ab939-112">CSS</span><span class="sxs-lookup"><span data-stu-id="ab939-112">CSS</span></span>
- <span data-ttu-id="ab939-113">DOC</span><span class="sxs-lookup"><span data-stu-id="ab939-113">DOC</span></span>
- <span data-ttu-id="ab939-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="ab939-114">DOCX</span></span>
- <span data-ttu-id="ab939-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="ab939-115">EPUB</span></span>
- <span data-ttu-id="ab939-116">GIF</span><span class="sxs-lookup"><span data-stu-id="ab939-116">GIF</span></span>
- <span data-ttu-id="ab939-117">INDD</span><span class="sxs-lookup"><span data-stu-id="ab939-117">INDD</span></span>
- <span data-ttu-id="ab939-118">JAR</span><span class="sxs-lookup"><span data-stu-id="ab939-118">JAR</span></span>
- <span data-ttu-id="ab939-119">JPG</span><span class="sxs-lookup"><span data-stu-id="ab939-119">JPG</span></span>
- <span data-ttu-id="ab939-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="ab939-120">JPEG</span></span>
- <span data-ttu-id="ab939-121">JS</span><span class="sxs-lookup"><span data-stu-id="ab939-121">JS</span></span>
- <span data-ttu-id="ab939-122">MP3</span><span class="sxs-lookup"><span data-stu-id="ab939-122">MP3</span></span>
- <span data-ttu-id="ab939-123">MP4</span><span class="sxs-lookup"><span data-stu-id="ab939-123">MP4</span></span>
- <span data-ttu-id="ab939-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="ab939-124">MPEG</span></span>
- <span data-ttu-id="ab939-125">MPG</span><span class="sxs-lookup"><span data-stu-id="ab939-125">MPG</span></span>
- <span data-ttu-id="ab939-126">ODP</span><span class="sxs-lookup"><span data-stu-id="ab939-126">ODP</span></span>
- <span data-ttu-id="ab939-127">ODS</span><span class="sxs-lookup"><span data-stu-id="ab939-127">ODS</span></span>
- <span data-ttu-id="ab939-128">ODT</span><span class="sxs-lookup"><span data-stu-id="ab939-128">ODT</span></span>
- <span data-ttu-id="ab939-129">PDF</span><span class="sxs-lookup"><span data-stu-id="ab939-129">PDF</span></span>
- <span data-ttu-id="ab939-130">PNG</span><span class="sxs-lookup"><span data-stu-id="ab939-130">PNG</span></span>
- <span data-ttu-id="ab939-131">PPT</span><span class="sxs-lookup"><span data-stu-id="ab939-131">PPT</span></span>
- <span data-ttu-id="ab939-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="ab939-132">PPTX</span></span>
- <span data-ttu-id="ab939-133">PS</span><span class="sxs-lookup"><span data-stu-id="ab939-133">PS</span></span>
- <span data-ttu-id="ab939-134">QXP</span><span class="sxs-lookup"><span data-stu-id="ab939-134">QXP</span></span>
- <span data-ttu-id="ab939-135">RAR</span><span class="sxs-lookup"><span data-stu-id="ab939-135">RAR</span></span>
- <span data-ttu-id="ab939-136">RTF</span><span class="sxs-lookup"><span data-stu-id="ab939-136">RTF</span></span>
- <span data-ttu-id="ab939-137">SVG</span><span class="sxs-lookup"><span data-stu-id="ab939-137">SVG</span></span>
- <span data-ttu-id="ab939-138">TAR</span><span class="sxs-lookup"><span data-stu-id="ab939-138">TAR</span></span>
- <span data-ttu-id="ab939-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="ab939-139">TGZ</span></span>
- <span data-ttu-id="ab939-140">TXT</span><span class="sxs-lookup"><span data-stu-id="ab939-140">TXT</span></span>
- <span data-ttu-id="ab939-141">WMV</span><span class="sxs-lookup"><span data-stu-id="ab939-141">WMV</span></span>
- <span data-ttu-id="ab939-142">XLS</span><span class="sxs-lookup"><span data-stu-id="ab939-142">XLS</span></span>
- <span data-ttu-id="ab939-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="ab939-143">XLSX</span></span>
- <span data-ttu-id="ab939-144">XML</span><span class="sxs-lookup"><span data-stu-id="ab939-144">XML</span></span>
- <span data-ttu-id="ab939-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="ab939-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="ab939-146">تحميل ملف</span><span class="sxs-lookup"><span data-stu-id="ab939-146">Upload a file</span></span>

<span data-ttu-id="ab939-147">لتحميل ملف إلى منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ab939-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ab939-148">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="ab939-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="ab939-149">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="ab939-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="ab939-150">في "مستكشف الملفات"، حدد ملفًا أو أكثر، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="ab939-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="ab939-151">في مربع الحوار **تحميل عنصر الوسائط**، أدخل بيانات تعريف العنوان والوصف والكلمات الأساسية كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="ab939-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="ab939-152">لنشر الملف (الملفات) مباشرةً بعد التحميل، حدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.</span><span class="sxs-lookup"><span data-stu-id="ab939-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="ab939-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ab939-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab939-154">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ab939-154">Additional resources</span></span>

[<span data-ttu-id="ab939-155">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="ab939-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ab939-156">تحميل الصور</span><span class="sxs-lookup"><span data-stu-id="ab939-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ab939-157">تحميل مقطع فيديو</span><span class="sxs-lookup"><span data-stu-id="ab939-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="ab939-158">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="ab939-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="ab939-159">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="ab939-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
