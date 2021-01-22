---
title: تخصيص نقاط تركيز الصورة
description: يصف هذا الموضوع كيفية تخصيص نقاط تركيز الصورة في منشئ موقع Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: af922e857e6bd7a58c0b9891939c8265568b549b
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269511"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="ea8d3-103">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="ea8d3-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea8d3-104">يصف هذا الموضوع كيفية تخصيص نقاط تركيز الصورة في منشئ موقع Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="ea8d3-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="ea8d3-105">Overview</span></span>

<span data-ttu-id="ea8d3-106">عند تحميل صورة إلى مكتبه الوسائط الخاصة بمنشئ موقع Commerce، يحاول النظام تحديد نقطة تركيز الصورة.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="ea8d3-107">على سبيل المثال، عند وجود شخص في الصورة، سيقوم النظام بتعيين نقطة التركيز إلى وجه الشخص بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="ea8d3-108">في معظم الحالات، تعمل نقطة التركيز بشكل جيد لجميع مناف العرض، ولكنك قد ترغب في بعض الأحيان بضبط نقطة التركيز للتأكيد من أن جزءًا معينًا من الصورة مرئي دائمًا.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="ea8d3-109">تحديد نقطة تركيز مخصصة لصورة</span><span class="sxs-lookup"><span data-stu-id="ea8d3-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="ea8d3-110">لتحديد نقطة تركيز مخصصة لصورة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="ea8d3-111">في جزء التنقل الأيمن في منشئ موقع Commerce، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="ea8d3-112">في النافذة الرئيسية،، حدد الصورة التي تريد تعديلها.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="ea8d3-113">في شريط الأوامر، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="ea8d3-114">حدد الصورة التي تريد إدخالها في **وضع التحرير**.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="ea8d3-115">ضمن **وضع التحرير**، حدد **تغيير نقطة التركيز**.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="ea8d3-116">يظهر عنصر تحكم نقطة تركيز فوق الصورة.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="ea8d3-117">حدد عنصر تحكم نقطة التركيز لتحريكه فوق نقطة التركيز التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="ea8d3-118">عند الانتهاء، حدد **حفظ** على شريط الأوامر، ثم حدد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="ea8d3-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea8d3-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ea8d3-119">Additional resources</span></span>

[<span data-ttu-id="ea8d3-120">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="ea8d3-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ea8d3-121">تحميل صور</span><span class="sxs-lookup"><span data-stu-id="ea8d3-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ea8d3-122">تحميل فيديو</span><span class="sxs-lookup"><span data-stu-id="ea8d3-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="ea8d3-123">تحميل الملفات</span><span class="sxs-lookup"><span data-stu-id="ea8d3-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="ea8d3-124">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="ea8d3-124">Crop images</span></span>](dam-crop-images.md)