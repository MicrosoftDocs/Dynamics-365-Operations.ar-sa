---
title: العمل باستخدام نمط الإعدادات المسبقة
description: يصف هذا الموضوع كيفية استخدام الإعدادات المسبقة لأنماط الموقع في منشئ الموقع في Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7279b52f801c2cb2f156d220d1a456b773d10f33
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791741"
---
# <a name="work-with-style-presets"></a><span data-ttu-id="536a6-103">العمل باستخدام نمط الإعدادات المسبقة</span><span class="sxs-lookup"><span data-stu-id="536a6-103">Work with style presets</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="536a6-104">يصف هذا الموضوع كيفية استخدام الإعدادات المسبقة لأنماط الموقع في منشئ الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="536a6-104">This topic describes how to work with site style presets in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="536a6-105">الإعداد المسبق للنمط هو مجموعة مخزنة من جميع قيم النمط القابلة للاستخدام في نسق نمط.</span><span class="sxs-lookup"><span data-stu-id="536a6-105">A style preset is a stored set of all authorable style values across a site's theme.</span></span> <span data-ttu-id="536a6-106">ويمكن استخدامه لتغيير شكل أحد المواقع على الفور من منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="536a6-106">It can be used to immediately change the look of a site from site builder.</span></span> <span data-ttu-id="536a6-107">تسمح الإعدادات المسبقة للأنماط للمؤلفين في منشئ الموقع في Commerce بتغيير مجموعة من قيم الأنماط في موقعهم ومعاينتها وتنشيطها، من دون استخدام أوراق الأنماط المتتالية (CSS) أو نشر النُسق.</span><span class="sxs-lookup"><span data-stu-id="536a6-107">Style presets let Commerce site builder authors quickly change, preview, and activate a set of style values across their site, without having to use Cascading Style Sheets (CSS) or deploy themes.</span></span> <span data-ttu-id="536a6-108">تعتبر أنماط الخطوط وأنماط الأزرار وألوان الموقع أمثلة نموذجية عن متغيرات الأنماط التي يمكن إدارتها عبر الإعدادات المسبقة للأنماط.</span><span class="sxs-lookup"><span data-stu-id="536a6-108">Font styles, button styles, and site colors are typical examples of style variables that can be managed through style presets.</span></span>

<span data-ttu-id="536a6-109">تتحدد مجموعة متغيرات الأنماط المتوفرة في موقع ما حسب مكتبة النُسق والوحدات النمطية التي يتم نشرها في مستأجر الموقع.</span><span class="sxs-lookup"><span data-stu-id="536a6-109">The set of style variables that is available in a site is determined by the theme and module library that is deployed to a site's tenant.</span></span> <span data-ttu-id="536a6-110">تسمح مجموعة تطوير البرامج (SDK) الخاصة بـ Dynamics 365 Commerce عبر الإنترنت (SDK) للمطورين بتطبيق العدد الذي يحتاجون إليه من متغيرات الأنماط القابلة للاستخدام لنسق معين.</span><span class="sxs-lookup"><span data-stu-id="536a6-110">The Dynamics 365 Commerce online software development kit (SDK) lets developers implement as many (or as few) authorable style variables as they require for a given theme.</span></span> <span data-ttu-id="536a6-111">ومن خلال تمكين عدد أكبر من متغيرات الأنماط، بإمكان مطور النسق تقديم الاختيارات النهائية حول أنماط الموقع للمؤلفين في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="536a6-111">By enabling more style variables, a theme developer can put final choices about site styles into the hands of site builder authors.</span></span> <span data-ttu-id="536a6-112">وبالتالي، بإمكان المستخدمين من غير المطورين تحديث أنماط الموقع ومعاينتها باستخدام مجموعة الأدوات.</span><span class="sxs-lookup"><span data-stu-id="536a6-112">Therefore, non-developers can update and preview site styles by using the toolset.</span></span> <span data-ttu-id="536a6-113">تعتبر الإمكانية مفيدة أيضًا لأي سيناريو حيث ستؤدي التغييرات المباشرة على النُسق أو CSS إلى مصروفات زائدة غير ضرورية.</span><span class="sxs-lookup"><span data-stu-id="536a6-113">The capability is also useful for any scenario where direct changes to themes or CSS will cause unnecessary overhead.</span></span>

<span data-ttu-id="536a6-114">تحتاج النُسق حيث تم تمكين متغيرات الأنماط القابلة للاستخدام إلى إعداد مسبق افتراضي للنمط.</span><span class="sxs-lookup"><span data-stu-id="536a6-114">Themes where authorable style variables are enabled require a default style preset.</span></span> <span data-ttu-id="536a6-115">وبإمكانها أن تتضمن، بشكل اختياري، خيارات إعدادات مسبقة إضافية كجزء من حزمة نُسق منشورة.</span><span class="sxs-lookup"><span data-stu-id="536a6-115">They can optionally include additional preset options as part of a deployed theme package.</span></span> <span data-ttu-id="536a6-116">على سبيل المثال، يمكن نشر نسق يتضمن إعدادًا مسبقًا واحدًا افتراضيًا للنمط "الضوء العصري".</span><span class="sxs-lookup"><span data-stu-id="536a6-116">For example, a theme can be deployed that has a single default "modern light" style preset.</span></span> <span data-ttu-id="536a6-117">أو قد تتضمن خيارات إعدادات مسبقة إضافية إلى جانب الإعداد الافتراضي، مثل "داكن حديث" أو "فاتح عتيق" أو "داكن عتيق".</span><span class="sxs-lookup"><span data-stu-id="536a6-117">Alternatively, it might include additional style preset options besides the default preset, such as "modern dark," "vintage light," or "vintage dark."</span></span> <span data-ttu-id="536a6-118">يتم إنشاء هذه الإعدادات المسبقة المضمنة للنُسق من قبل المطورين ويمكن استخدامها كنقاط بداية لتصميمات مواقع الجديدة.</span><span class="sxs-lookup"><span data-stu-id="536a6-118">These built-in theme presets are created by developers and can be used as starting points for new site designs.</span></span>

<span data-ttu-id="536a6-119">في منشئ الموقع، بإمكان المؤلفين الاختيار من ضمن مجموعة من الإعدادات المسبقة المضمنة لنسق، أو يمكنهم إنشاء إعدادات مسبقة لأنماط خاصة بهم وتخصيصها باستخدام متغيرات الأنماط التي تم تمكينها.</span><span class="sxs-lookup"><span data-stu-id="536a6-119">In site builder, authors can select among a theme's built-in presets, or they can create their own style presets and customizations by using the enabled style variables.</span></span> <span data-ttu-id="536a6-120">يمكن معاينة الإعدادات المسبقة للنمط في منشئ الموقع قبل تنشيطها في الموقع المباشر.</span><span class="sxs-lookup"><span data-stu-id="536a6-120">A style preset can be previewed in site builder before it's activated on the live site.</span></span> <span data-ttu-id="536a6-121">بعد مراجعة تغييرات النمط التي قام بها المؤلف، يمكنك عندئذٍ تعيين الإعداد المسبق للنمط إلى "نشط" في الموقع المباشر.</span><span class="sxs-lookup"><span data-stu-id="536a6-121">After an author's style changes are reviewed, the style preset can then be set to "active" for the live site.</span></span>

## <a name="preview-a-style-preset"></a><span data-ttu-id="536a6-122">معاينة إعداد مسبق لنمط</span><span class="sxs-lookup"><span data-stu-id="536a6-122">Preview a style preset</span></span>

<span data-ttu-id="536a6-123">لمعاينة إعداد مسبق لنمط على موقعك في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="536a6-123">To preview a style preset on your site in site builder, follow these steps.</span></span>

1. <span data-ttu-id="536a6-124">في جزء التنقل الأيمن الخاص بموقعك، انتقل إلى **إعدادات الموقع \> تصميم**.</span><span class="sxs-lookup"><span data-stu-id="536a6-124">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="536a6-125">في صفحة **الإعدادات المسبقة للأنماط** في أعلى محرر التصميم، في قائمة **الإعدادات المسبقة المتوفرة**، حدد إعدادًا مسبقًا، ثم حدد **عرض** للانتقال إلى محرر الإعداد المسبق.</span><span class="sxs-lookup"><span data-stu-id="536a6-125">On the **Style presets** tab at the top of the design editor, in the **Available presets** list, select a preset, and then select **View** to go to the preset editor.</span></span>

    <span data-ttu-id="536a6-126">في حال عدم وجود إعدادات مسبقة في قائمة **الإعدادات المسبقة المتوفرة**، راجع [إنشاء إعداد مسبق مخصص لنمط](#create-a-custom-style-preset) للحصول على معلومات حول كيفية إنشاء إعداد مسبق مخصص لنمط.</span><span class="sxs-lookup"><span data-stu-id="536a6-126">If there are currently no presets in the **Available presets** list, see [Create a custom style preset](#create-a-custom-style-preset) for information about how to create a custom style preset.</span></span>

    > [!NOTE]
    > <span data-ttu-id="536a6-127">يشار إلى الإعدادات المسبقة التي كانت مضمنة مع النسق بشارة **مضمن**.</span><span class="sxs-lookup"><span data-stu-id="536a6-127">Presets that were included with the theme are indicated by a **Built-in** badge.</span></span> <span data-ttu-id="536a6-128">هذه الإعدادات المسبقة المضمنة هي للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="536a6-128">These built-in presets are read-only.</span></span> <span data-ttu-id="536a6-129">لنسخ إعداد مسبق مضمن كإعداد مسبق جديد قابل للتخصيص، حدد زر علامة القطع (**...**) للإعداد المسبق، ثم حدد **حفظ باسم**.</span><span class="sxs-lookup"><span data-stu-id="536a6-129">To copy a built-in preset as a new customizable preset, select the ellipsis button (**...**) for the preset, and then select **Save as**.</span></span>

1. <span data-ttu-id="536a6-130">في شريط الأوامر، حدد **معاينة**.</span><span class="sxs-lookup"><span data-stu-id="536a6-130">On the command bar, select **Preview**.</span></span>
1. <span data-ttu-id="536a6-131">حدد عنوان URL من موقعك لاستخدامه لمعاينة الإعداد المسبق للنمط، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="536a6-131">Select a URL from your site to use to preview the style preset, and then select **OK**.</span></span>
1. <span data-ttu-id="536a6-132">حدد متغير عنوان URL الخاص بالقناة والخاص بالإعدادات المحلية لمعاينته عن طريق تحديد اسم المتغير.</span><span class="sxs-lookup"><span data-stu-id="536a6-132">Select the channel-specific and locale-specific URL variant to preview by selecting the variant's name.</span></span> <span data-ttu-id="536a6-133">تفتح نافذة مستعرض جديدة للمعاينة، حيث يتم تطبيق الإعداد المسبق للنمط على الصفحة المحددة.</span><span class="sxs-lookup"><span data-stu-id="536a6-133">A new preview browser window is opened, where the selected style preset is applied to the specified page.</span></span>

> [!NOTE]
> <span data-ttu-id="536a6-134">عنوان URL الخاص بالمعاينة دائم ومصادق عليه.</span><span class="sxs-lookup"><span data-stu-id="536a6-134">The preview URL is persistent and authenticated.</span></span> <span data-ttu-id="536a6-135">وبالتالي، يمكنك نسخه ولصقه وإرساله إلى زملاء آخرين مصادق عليه لمراجعته قبل أن تقوم بتعيينه إلى "نشط" على موقعك المباشر.</span><span class="sxs-lookup"><span data-stu-id="536a6-135">Therefore, you can copy, paste, and send it to other authenticated co-workers for review before you set it to "active" on your live site.</span></span> <span data-ttu-id="536a6-136">ويعتبر أيضًا عنوان URL للمعاينة مفيدًا لتدقيق الأنماط على أجهزة مختلفة وفي مستعرضات مختلفة وعلى شاشات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="536a6-136">The preview URL is also useful for checking styles on different devices, in different browsers, and on different screens.</span></span>

> [!TIP]
> <span data-ttu-id="536a6-137">بينما تقوم بتحرير إعداد مسبق لنمط، قد يتبين لك أنه من المفيد ترك نافذة مستعرض المعاينة الخاصة به مفتوحة في نافذة مستعرض منفصلة، بحيث يمكنك التحقق بسرعة من صحة تغييراتك</span><span class="sxs-lookup"><span data-stu-id="536a6-137">While you edit a style preset, you might find it helpful to leave the preview browser window for it open in a separate browser window, so that you can quickly validate your changes.</span></span> <span data-ttu-id="536a6-138">بعد حفظ تغييراتك في إعداد مسبق، يمكنك تحديث نافذة مستعرض المعاينة المفتوحة للتحقق من تجربة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="536a6-138">After you save your changes to a preset, refresh the open preview browser window to validate the user experience.</span></span>

## <a name="create-a-custom-style-preset"></a><span data-ttu-id="536a6-139">إنشاء إعداد مسبق مخصص لنمط</span><span class="sxs-lookup"><span data-stu-id="536a6-139">Create a custom style preset</span></span>

<span data-ttu-id="536a6-140">لإنشاء إنشاء إعداد مسبق مخصص لنمط في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="536a6-140">To create a custom style preset in site builder, follow these steps.</span></span>

1. <span data-ttu-id="536a6-141">في جزء التنقل الأيمن الخاص بموقعك، انتقل إلى **إعدادات الموقع \> تصميم**.</span><span class="sxs-lookup"><span data-stu-id="536a6-141">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="536a6-142">على علامة التبويب **الإعدادات المسبقة للأنماط** في أعلى محرر التصميم، على شريط الأوامر، حدد **إعداد مسبق جديد**.</span><span class="sxs-lookup"><span data-stu-id="536a6-142">On the **Style presets** tab at the top of the design editor, on the command bar, select **New preset**.</span></span>
1. <span data-ttu-id="536a6-143">أدخل اسمًا ووصفًا للإعداد الجديد، ثم حدد **حفظ**</span><span class="sxs-lookup"><span data-stu-id="536a6-143">Enter a name and description for the new preset, and then select **Save**.</span></span> <span data-ttu-id="536a6-144">يتم إنشاء إعداد مسبق جديد قابل للتخصيص يستخدم القيم الافتراضية للنسق كنقطة بداية.</span><span class="sxs-lookup"><span data-stu-id="536a6-144">A new customizable preset is created that uses the theme's default values as a starting point.</span></span>

> [!NOTE]
> <span data-ttu-id="536a6-145">يمكنك أيضًا إنشاء إعداد مسبق مخصص للنمط من أي إعداد مسبق موجود عن طريق تحديد زر علامة القطع (**...**) لهذا الإعداد المسبق ثم تحديد **حفظ باسم**.</span><span class="sxs-lookup"><span data-stu-id="536a6-145">You can also create a new custom style preset from any existing preset by selecting the ellipsis button (**...**) for that preset and then selecting **Save as**.</span></span> <span data-ttu-id="536a6-146">أو يمكنك تحديد **حفظ باسم** على شريط الأوامر في محرر الإعداد المسبق.</span><span class="sxs-lookup"><span data-stu-id="536a6-146">Alternatively, select **Save as** on the command bar in the preset editor.</span></span>

## <a name="modify-global-and-module-type-style-values"></a><span data-ttu-id="536a6-147">تعديل قيم الأنماط العمومية ومن نوع الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="536a6-147">Modify global and module type style values</span></span>

<span data-ttu-id="536a6-148">تتم مشاركة بعض متغيرات أنماط النسق بين أنواع وحدات نمطية متعددة.</span><span class="sxs-lookup"><span data-stu-id="536a6-148">Some of a theme's style variables are shared among multiple module types.</span></span> <span data-ttu-id="536a6-149">يشار إلى متغيرات الأنماط هذه باسم متغيرات الأنماط *العمومية*.</span><span class="sxs-lookup"><span data-stu-id="536a6-149">These style variables are referred to as *global* style variables.</span></span> <span data-ttu-id="536a6-150">تتضمن الأمثلة ألوان الموقع الأساسية وأنماط الخطوط الافتراضية وأنماط الأزرار.</span><span class="sxs-lookup"><span data-stu-id="536a6-150">Examples include primary site colors, default font styles, and button styles.</span></span> <span data-ttu-id="536a6-151">ومن خلال تعيين المتغيرات العامة، قد تقوم بتغيير شكل الموقع عبر عدة أنواع مختلفة من الوحدات النمطية.</span><span class="sxs-lookup"><span data-stu-id="536a6-151">By setting global variables, you might change the look across many different module types.</span></span>

<span data-ttu-id="536a6-152">بإمكان بعض قيم الأنماط أن تكون فريدة لنوع وحدة نمطية، أو قد تحتاج إلى تجاوز قيمة عمومية افتراضية بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="536a6-152">Some style values can be unique to a module type, or they might have to optionally override a default global value.</span></span> <span data-ttu-id="536a6-153">إذا قام نسق موقع بتطبيق متغيرات أنماط من نوع الوحدة النمطية، فبإمكان المؤلفين في منشئ الموقع تخصيص نمط من نوع الوحدة النمطية بشكل مستقل عن الإعدادات العمومية.</span><span class="sxs-lookup"><span data-stu-id="536a6-153">If a site's theme has implemented module type style variables, site builder authors can customize the style of a module type independently of the global settings.</span></span> <span data-ttu-id="536a6-154">بإمكان المتغيرات من نوع الوحدة النمطية أن تزيد أو تتجاوز متغيرات الأنماط العمومية في النسق.</span><span class="sxs-lookup"><span data-stu-id="536a6-154">Module type variables can either augment or override the global style variables in a theme.</span></span>

> [!NOTE]
> <span data-ttu-id="536a6-155">سلوك التدرج الهرمي لقيم النمط في موقع ما هو كالتالي:</span><span class="sxs-lookup"><span data-stu-id="536a6-155">The hierarchy of style values in a site behaves in the following manner.</span></span> <span data-ttu-id="536a6-156">تتجاوز قيم الأنماط التي تظهر إلى أقصى اليمين قيم الأنماط الموجودة إلى يسارها.</span><span class="sxs-lookup"><span data-stu-id="536a6-156">Style values that appear farther to the right override the style values to the left of them.</span></span>
>
> <span data-ttu-id="536a6-157">القيم الافتراضية للنسق \< القيم العمومية للأنماط \< قيم الأنماط من نوع الوحدة النمطية \< تجاوز CSS</span><span class="sxs-lookup"><span data-stu-id="536a6-157">Theme default values \< Global style values \< Module type style values \< CSS override</span></span>

<span data-ttu-id="536a6-158">لتغيير القيم العمومية أو القيم من نوع الوحدة النمطية لنمط معين في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="536a6-158">To change a style preset's global or module type values in site builder, follow these steps.</span></span>

1. <span data-ttu-id="536a6-159">في جزء التنقل الأيمن الخاص بموقعك، انتقل إلى **إعدادات الموقع \> تصميم**.</span><span class="sxs-lookup"><span data-stu-id="536a6-159">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="536a6-160">على علامة التبويب **الإعدادات المسبقة للأنماط** في أعلى محرر التصميم، حدد **عرض** لأي إعداد مسبق للنمط للانتقال إلى محرر الإعداد المسبق.</span><span class="sxs-lookup"><span data-stu-id="536a6-160">On the **Style presets** tab at the top of the design editor, select **View** for any style preset to go to the preset editor.</span></span>
1. <span data-ttu-id="536a6-161">حدد **معاينة**، ثم اتبع خطوات تحديد عنوان URL لفتح معاينة نافذة مستعرض كاملة لإعدادك المسبق.</span><span class="sxs-lookup"><span data-stu-id="536a6-161">Select **Preview**, and then follow the URL selection steps to open a full-browser-window preview for your preset.</span></span> <span data-ttu-id="536a6-162">اترك نافذة مستعرض المعاينة هذه مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="536a6-162">Leave this preview browser window open.</span></span>
1. <span data-ttu-id="536a6-163">في محرر الإعداد المسبق، حدد **تحرير** في الجزء الأيمن العلوي.</span><span class="sxs-lookup"><span data-stu-id="536a6-163">In the preset editor, select **Edit** in the upper right.</span></span>
1. <span data-ttu-id="536a6-164">استخدم عناصر تحكم متغيرات الأنماط في المحرر لتغيير بعض قيم الأنماط العمومية.</span><span class="sxs-lookup"><span data-stu-id="536a6-164">Use the style variable controls in the editor to change some global style values.</span></span>
1. <span data-ttu-id="536a6-165">في أعلى المحرر، على علامة تبويب **الوحدات النمطية** إلى يسار علامة التبويب **عمومي**، حدد نوع وحدة نمطية لتطبيق الأنماط عليها.</span><span class="sxs-lookup"><span data-stu-id="536a6-165">At the top of the editor, on the **Modules** tab to the right of the **Global** tab, select a module type that must be styled.</span></span>
1. <span data-ttu-id="536a6-166">استخدم عناصر تحكم النمط لتغيير بعض القيم لنوع الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="536a6-166">Use the style controls to change some values for the module type.</span></span>
1. <span data-ttu-id="536a6-167">عندما تصبح جاهزًا لمعاينة التغييرات، حدد **حفظ** على شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="536a6-167">When you're ready to preview your changes, select **Save** on the command bar.</span></span>
1. <span data-ttu-id="536a6-168">عد إلى نافذه مستعرض المعاينة المفتوحة، وقم بتحديثها.</span><span class="sxs-lookup"><span data-stu-id="536a6-168">Return to the open preview browser window, and refresh it.</span></span> <span data-ttu-id="536a6-169">تعتبر المعاينة في نافذة المستعرض الكاملة مفيدة للتحقق من تغييرات الأنماط عند نقاط توقف مختلفة في طريقة العرض وفي مستعرضات مختلفة وعلى أنظمة أساسية لأجهزة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="536a6-169">The full-browser-window preview is useful for checking style changes at different view breakpoints, in different browsers, and on different device platforms.</span></span>
1. <span data-ttu-id="536a6-170">عند اكتمال كافة التغييرات والتحقق من صحتها، حدد **إنهاء** في أعلى يسار المحرر.</span><span class="sxs-lookup"><span data-stu-id="536a6-170">When all changes have been completed and validated, select **Finish editing** in the upper right of the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="536a6-171">إذا كنت تعمل على تحرير إعداد مسبق لنمط نشط حاليًا في موقعك، سترى الشارة الزرقاء **نشط** في المحرر.</span><span class="sxs-lookup"><span data-stu-id="536a6-171">If you're editing the style preset that is currently active on your site, you will see a blue **Active** badge in the editor.</span></span> <span data-ttu-id="536a6-172">تشير هذه الشارة إلى أن الإعداد المسبق موجود حاليًا في العرض المباشر على موقعك على الويب.</span><span class="sxs-lookup"><span data-stu-id="536a6-172">This badge indicates that the preset is currently live on your website.</span></span> <span data-ttu-id="536a6-173">إذا قمت بتغيير الإعداد المسبق النشط، فحدد **نشر** لدفع تلك التغييرات إلى موقعك المباشر.</span><span class="sxs-lookup"><span data-stu-id="536a6-173">If you change the active preset, select **Publish** to push those changes to your live site.</span></span>

## <a name="make-a-new-style-preset-active-on-your-live-site"></a><span data-ttu-id="536a6-174">تنشيط إعداد مسبق لنمط جديد في موقعك المباشر</span><span class="sxs-lookup"><span data-stu-id="536a6-174">Make a new style preset active on your live site</span></span>

<span data-ttu-id="536a6-175">لتعيين إعداد مسبق لنمط على أنه الإعداد المسبق النشط الجديد في موقعك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="536a6-175">To set a style preset as the new active preset on your site, follow these steps.</span></span>

- <span data-ttu-id="536a6-176">حدد **الزر تعيين كنشط** في أحد الأماكن التالية:</span><span class="sxs-lookup"><span data-stu-id="536a6-176">Select the **Set as active button** in one of these places:</span></span>

    - <span data-ttu-id="536a6-177">شريط الأوامر في محرر الإعداد المسبق للنمط</span><span class="sxs-lookup"><span data-stu-id="536a6-177">The command bar in the style preset editor</span></span>
    - <span data-ttu-id="536a6-178">قائمة زر القطع (**...**) لأي إعداد مسبق متوفر في طريقة إعداد الرئيسية على علامة التبويب **الإعدادات المسبقة للأنماط** في **إعدادات الموقع \> التصميم**</span><span class="sxs-lookup"><span data-stu-id="536a6-178">The ellipsis menu (**...**) for any available preset in the main view on the **Style presets** tab at **Site Settings \> Design**</span></span>

<span data-ttu-id="536a6-179">يتم تنشيط قيم أنماط الإعداد المسبق عبر موقعك العام على الويب.</span><span class="sxs-lookup"><span data-stu-id="536a6-179">The preset's style values are made active across your public-facing website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="536a6-180">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="536a6-180">Additional resources</span></span>

[<span data-ttu-id="536a6-181">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="536a6-181">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="536a6-182">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="536a6-182">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="536a6-183">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="536a6-183">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="536a6-184">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="536a6-184">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="536a6-185">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="536a6-185">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="536a6-186">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="536a6-186">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="536a6-187">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="536a6-187">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="536a6-188">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="536a6-188">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
