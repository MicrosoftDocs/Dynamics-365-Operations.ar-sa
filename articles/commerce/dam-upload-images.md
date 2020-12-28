---
title: تحميل الصور
description: يصف هذا الموضوع كيفية تحميل الصور في منشئ موقع Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594273"
---
# <a name="upload-images"></a><span data-ttu-id="2d21a-103">تحميل الصور</span><span class="sxs-lookup"><span data-stu-id="2d21a-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d21a-104">يصف هذا الموضوع كيفية تحميل الصور في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d21a-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="2d21a-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2d21a-105">Overview</span></span>

<span data-ttu-id="2d21a-106">تسمح لك مكتبة وسائط منشئ موقع Commerce بتحميل الصور، أو بشكل فردي أو بشكل مجمع باستخدام المجلدات.</span><span class="sxs-lookup"><span data-stu-id="2d21a-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="2d21a-107">يجب أن تقوم دائمًا بتحميل إصدار الصورة الأعلى دقة وجودة، لأن مكون تغيير حجم الصورة سيقوم تلقائيًا بتحسين الصورة لمنافذ عرض مختلفة ونقاط التوقف الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="2d21a-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="2d21a-108">معلومات الصورة التي يتم تحديدها أثناء التحميل</span><span class="sxs-lookup"><span data-stu-id="2d21a-108">Image information specified during upload</span></span>

<span data-ttu-id="2d21a-109">عند تحميل صورة، يمكن تحديد المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="2d21a-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="2d21a-110">**العنوان والنص البديل والوصف والكلمات الأساسية**: بيانات تعريف الصورة أو الصور.</span><span class="sxs-lookup"><span data-stu-id="2d21a-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="2d21a-111">العنوان والنص البديل هما قيم مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2d21a-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="2d21a-112">**تحديد فئة**:</span><span class="sxs-lookup"><span data-stu-id="2d21a-112">**Select category**:</span></span>
    - <span data-ttu-id="2d21a-113">**بلا**: يُستخدم هذا الخيار لصورة أو صور تتعلق برواية قصة تجارة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2d21a-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="2d21a-114">**المنتج، الفئة، العميل، الموظف، الكتالوج**: تُستخدم لصورة أو صور في القناة متعددة الاتجاهات في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d21a-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="2d21a-115">**نشر الأصول بعد التحميل**: عند تحديد خانة الاختيار هذه، يتم نشر الصورة أو الصور مباشرةً بعد التحميل.</span><span class="sxs-lookup"><span data-stu-id="2d21a-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="2d21a-116">يتم أيضًا تمييز صور الأصول ذات فئة معينة لها بشكل تلقائي بواسطة الفئة ككلمة أساسية للمساعدة في البحث عن أصول خاصة بفئة معينة.</span><span class="sxs-lookup"><span data-stu-id="2d21a-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="2d21a-117">اصطلاحات التسمية لصور القناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="2d21a-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="2d21a-118">إذا قمت بتكوين مكتبة الوسائط كخلفية صورة قناة متعددة الاتجاهات، يمكنك استخدام فئات الصور للإشارة إلى الفئة التي تنتمي اليها الصورة التي تم تحميلها.</span><span class="sxs-lookup"><span data-stu-id="2d21a-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="2d21a-119">هناك أيضًا اصطلاح تسمية يجب اتباعه للتأكد من استرداد الصور بشكل صحيح بواسطة القنوات الأخرى، مثل نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="2d21a-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="2d21a-120">يختلف اصطلاح التسمية الافتراضي بالاستناد إلى الفئة:</span><span class="sxs-lookup"><span data-stu-id="2d21a-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="2d21a-121">يجب تسمية صور الكتالوجات "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="2d21a-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="2d21a-122">يجب تسمية صور الفئات "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="2d21a-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="2d21a-123">يجب تسمية صور العملاء "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="2d21a-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="2d21a-124">يجب تسمية صور الموظفين "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="2d21a-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="2d21a-125">يجب تسمية صور المنتجات "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="2d21a-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="2d21a-126">يمثل 001 تسلسل الصورة ويمكنها أن يكون 001 أو 002 أو 003 أو 004 أو 005</span><span class="sxs-lookup"><span data-stu-id="2d21a-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="2d21a-127">يجب تسمية صور متغيرات المنتجات "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="2d21a-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="2d21a-128">تحميل صورة</span><span class="sxs-lookup"><span data-stu-id="2d21a-128">Upload an image</span></span>

<span data-ttu-id="2d21a-129">لتحميل صورة في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2d21a-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2d21a-130">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="2d21a-131">في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="2d21a-132">في نافذة مستكشف الملفات، انتقل إلى صورة أو أكثر لتحميلها، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="2d21a-133">في مربع الحوار **تحميل عنصر الوسائط**، أدخل العنوان والنص البديل المطلوبين.</span><span class="sxs-lookup"><span data-stu-id="2d21a-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="2d21a-134">أدخل وصفًا اختياريًا وكلمات أساسية اختيارية، وحدد فئة إذا أردت ذلك.</span><span class="sxs-lookup"><span data-stu-id="2d21a-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="2d21a-135">إذا أردت نشر الصورة (الصور) مباشرةً بعد التحميل، فحدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="2d21a-136">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="2d21a-137">تحميل مجلد صور</span><span class="sxs-lookup"><span data-stu-id="2d21a-137">Upload a folder of images</span></span>

<span data-ttu-id="2d21a-138">لإجراء تحميل مجمع لمجلد صور في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2d21a-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2d21a-139">في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="2d21a-140">في شريط الأوامر، حدد **تحميل \> تحميل مجلد**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="2d21a-141">في نافذة مستكشف الملفات، انتقل إلى مجلد لتحميله، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="2d21a-142">في مربع الحوار **تحميل عناصر الوسائط**، أدخل كلمات أساسية اختيارية وحدد فئة إذا أردت ذلك.</span><span class="sxs-lookup"><span data-stu-id="2d21a-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="2d21a-143">إذا أردت نشر الصور مباشرةً بعد التحميل، فحدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="2d21a-144">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d21a-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2d21a-145">Additional resources</span></span>

[<span data-ttu-id="2d21a-146">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="2d21a-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="2d21a-147">تحميل فيديو</span><span class="sxs-lookup"><span data-stu-id="2d21a-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="2d21a-148">تحميل الملفات</span><span class="sxs-lookup"><span data-stu-id="2d21a-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="2d21a-149">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="2d21a-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="2d21a-150">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="2d21a-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="2d21a-151">تحميل الملفات الثابتة وخدمتها</span><span class="sxs-lookup"><span data-stu-id="2d21a-151">Upload and serve static files</span></span>](upload-serve-static-files.md)
