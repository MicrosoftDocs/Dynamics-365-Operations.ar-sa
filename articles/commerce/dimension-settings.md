---
title: تطبيق إعدادات العرض لأبعاد المنتج
description: يغطي هذا الموضوع إعدادات العرض الخاصة بأبعاد المنتج ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117207"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="f33ff-103">تطبيق إعدادات العرض لأبعاد المنتج</span><span class="sxs-lookup"><span data-stu-id="f33ff-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f33ff-104">يغطي هذا الموضوع إعدادات العرض الخاصة بأبعاد المنتج ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f33ff-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f33ff-105">يدعم Dynamics 365 Commerce أبعاد الحجم والنمط واللون لتمييز متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="f33ff-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="f33ff-106">عادة ما تظهر الأبعاد كقيم نصية، مثل "الصغيرة" و"المتوسطة" و"الكبيرة" للأحجام و"أسود" و"بني" للألوان.</span><span class="sxs-lookup"><span data-stu-id="f33ff-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="f33ff-107">ومع ذلك، إذا كان أحد المنتجات يدعم العديد من الاختلافات، قد يكون من الصعب استعراض متغيرات المنتجات، لأن التحديدات المتعددة مطلوبة لعرض الصورة لكل متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="f33ff-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="f33ff-108">ولتسهيل استعراض متغيرات المنتجات، فإن الإصدار 10.0.20 من Commerce يمكنه استخدام الصور والرموز السداسية العشرية لإظهار الأبعاد على شكل عينات ألوان.</span><span class="sxs-lookup"><span data-stu-id="f33ff-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="f33ff-109">في منشئ موقع Commerce، يتم تعريف إعدادات الأبعاد في **إعدادات الموقع \> الملحقات \> إدارة الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="f33ff-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="f33ff-110">يبين الرسم التوضيحي التالي مثالاً لإعدادات الأبعاد في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="f33ff-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![مثال على إعدادات الموقع في منشئ موقع Commerce](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="f33ff-112">ويتوفر إعدادان للبُعد:</span><span class="sxs-lookup"><span data-stu-id="f33ff-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="f33ff-113">**الأبعاد المراد عرضها كصورة** – حدد الأبعاد التي يجب أن تظهر كعينات ألوان في صفحات موقع التجارة الإلكترونية مثل صفحات تفاصيل المنتج (PDP) وصفحات قوائم نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="f33ff-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="f33ff-114">يمكن إظهار أي مجموعة من أبعاد اللون والحجم والنمط كعينات ألوان.</span><span class="sxs-lookup"><span data-stu-id="f33ff-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="f33ff-115">إذا تم تحديد بُعد للعرض كعينة ألوان، سيقوم عرض وحدة Commerce النمطية بالبحث عن تكوين متوفر لعينة ألوان رمز سداسي عشري.</span><span class="sxs-lookup"><span data-stu-id="f33ff-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="f33ff-116">في حالة عدم تكوين أي رمز سداسي عشري، سيقوم منطق النظام بالبحث عن تكوين لعينة ألوان لعنوان URL الخاص بالصورة.</span><span class="sxs-lookup"><span data-stu-id="f33ff-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="f33ff-117">إذا لم يتم تكوين رمز سداسي عشري أو عنوان صورة URL، سيتم عرض النص.</span><span class="sxs-lookup"><span data-stu-id="f33ff-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="f33ff-118">يبين الرسم التوضيحي التالي مثالاً لظهور صفحة تفاصيل المنتج على موقع تجارة إلكترونية تتضمن عينات اللون والحجم.</span><span class="sxs-lookup"><span data-stu-id="f33ff-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="f33ff-119">في هذا المثال، يتم تكوين رمز سداسي عشري لبُعد اللون.</span><span class="sxs-lookup"><span data-stu-id="f33ff-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="f33ff-120">لذا، فإن عينات الألوان تظهر كألوان.</span><span class="sxs-lookup"><span data-stu-id="f33ff-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="f33ff-121">ومع ذلك، لا يتم تكوين رمز سداسي عشري أو عنوان URL خاص بصورة لبُعد الحجم.</span><span class="sxs-lookup"><span data-stu-id="f33ff-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="f33ff-122">لذلك، يتم عرض النص.</span><span class="sxs-lookup"><span data-stu-id="f33ff-122">Therefore, text is shown.</span></span>

    ![مثال على بُعد اللون المعروض كعينات ألوان على صفحة تفاصيل المنتجات التجارية الإلكترونية](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="f33ff-124">**الأبعاد المراد عرضها في بطاقة المنتج** – حدد الأبعاد التي ينبغي أن تظهر في بطاقات المنتجات التي تظهر في القوائم وعلى صفحات القوائم.</span><span class="sxs-lookup"><span data-stu-id="f33ff-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="f33ff-125">قبل أن يظهر بُعد على بطاقة منتج، فإنه يجب تمكين هذا الإعداد لذلك البُعد.</span><span class="sxs-lookup"><span data-stu-id="f33ff-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="f33ff-126">يجب أيضًا تمكين **الأبعاد المراد عرضها كصورة**.</span><span class="sxs-lookup"><span data-stu-id="f33ff-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="f33ff-127">يتم تحسين سلوك تحديد عينات الألوان الموجود على بطاقات المنتجات لبُعد اللون.</span><span class="sxs-lookup"><span data-stu-id="f33ff-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="f33ff-128">بالنسبة لأبعاد أخرى، قد يكون ملحق العرض مطلوبًا لتخصيص سلوك تحديد عينة الألوان.</span><span class="sxs-lookup"><span data-stu-id="f33ff-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="f33ff-129">يبين الرسم التوضيحي التالي مثالاً لصفحة قائمة على موقع تجارة إلكترونية يحتوي على بطاقات المنتجات التي تتضمن عينات الألوان.</span><span class="sxs-lookup"><span data-stu-id="f33ff-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![مثال على بُعد اللون المعروض كعينات ألوان على صفحة التجارية الإلكترونية](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="f33ff-131">للحصول على معلومات حول كيفية تكوين أبعاد المنتج بحيث يتم عرضها كعينات على صفحات الموقع، راجع [تكوين قيم أبعاد المنتجات لتظهر كعينات](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="f33ff-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f33ff-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f33ff-132">Additional resources</span></span>

[<span data-ttu-id="f33ff-133">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="f33ff-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f33ff-134">وحدة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="f33ff-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="f33ff-135">وحدة صندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="f33ff-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f33ff-136">تكوين قيم أبعاد المنتج لتظهر كعينات ألوان</span><span class="sxs-lookup"><span data-stu-id="f33ff-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
