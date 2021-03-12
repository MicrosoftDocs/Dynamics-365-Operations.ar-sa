---
title: تمكين المشاركة عبر القنوات واستخدامها
description: يوضح هذا الموضوع كيفيه تمكين ميزه مشاركه القناة المتقاطعة لمنشئ مواقع Microsoft Dynamics 365 Commerce واستخدامها.
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3990365dda0a0cff7adcc1d97120293d43f6e858
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973105"
---
# <a name="enable-and-use-cross-channel-sharing"></a><span data-ttu-id="3d6a1-103">تمكين المشاركة عبر القنوات واستخدامها</span><span class="sxs-lookup"><span data-stu-id="3d6a1-103">Enable and use cross-channel sharing</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d6a1-104">يوضح هذا الموضوع كيفيه تمكين ميزه مشاركه القناة المتقاطعة لمنشئ مواقع Microsoft Dynamics 365 Commerce واستخدامها.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-104">This topic describes how to enable and use the cross-channel sharing feature of Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="3d6a1-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="3d6a1-105">Overview</span></span>

<span data-ttu-id="3d6a1-106">مشاركه القناة المشتركة لنفرض ان البائعين يقومون باعاده استخدام المحتوي ومشاركته بين عبر القنوات من أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-106">Cross-channel sharing lets retailers reuse and share content among multiple channels of a site.</span></span> <span data-ttu-id="3d6a1-107">وتكون هذه الامكانيه مفيده عندما يكون لقناات الموقع لغة أساسيه متوافقة، أو عندما يكون لديها عناصر محتوي متعددة مشتركه.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-107">This capability is useful when the site channels have a compatible base language, or when they have numerous content items in common.</span></span>

<span data-ttu-id="3d6a1-108">تعمل مشاركه القناة المشتركة عن طريق تمكين قناه افتراضيه يتم البحث فيها عن محتوي متوفر في حاله عدم العثور علي إصدار محدد للمحتوي المطلوب.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-108">Cross-channel sharing works by enabling a default channel that will be searched for available content when a channel-specific version of the requested content isn't found.</span></span> <span data-ttu-id="3d6a1-109">يتم إنشاء المحتوي المخصص الذي ستتم مشاركته بين القنوات في القناة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-109">Content that is intended to be shared among channels is created in the default channel.</span></span> <span data-ttu-id="3d6a1-110">يمكن ترجمه هذا المحتوي لأي إعدادات محليه يتم استخدامها علي إيه قناه موقع.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-110">That content can be localized for any locale that is used on any site channel.</span></span>

## <a name="when-to-use-cross-channel-sharing"></a><span data-ttu-id="3d6a1-111">حالات استخدام المشاركة عبر القنوات</span><span class="sxs-lookup"><span data-stu-id="3d6a1-111">When to use cross-channel sharing</span></span>

<span data-ttu-id="3d6a1-112">تعد المشاركة عبر القنوات المشتركة مفيده عندما تتمكن العديد من القنوات علي موقع واحد من مشاركه المحتوي.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-112">Cross-channel sharing is useful when multiple channels on a single site can share content.</span></span> <span data-ttu-id="3d6a1-113">علي سبيل المثال، يمكن لبائع التجزئة الذي يحتوي علي علامات تجاريه متعددة وواجهات متاجر مجمعه ضمن موقع واحد مشاركه بعض المحتوي بين بعض أو كافة واجهات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-113">For example, a retailer that has multiple brands and storefronts that are grouped under a single site can share some content among some or all of the storefronts.</span></span> <span data-ttu-id="3d6a1-114">يمكن ان يتضمن هذا المحتوي المشترك الصفحات الخاصة بالبنود والشروط، وشروط الدفع، وأساليب الشحن، والاسئله المتداولة (FAQ).</span><span class="sxs-lookup"><span data-stu-id="3d6a1-114">This shared content can include pages for terms and conditions, payment terms, shipment methods, and frequently asked questions (FAQ).</span></span>

<span data-ttu-id="3d6a1-115">وتدعم المشاركة عبر القنوات الأجزاء أيضا.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-115">Cross-channel sharing also supports fragments.</span></span> <span data-ttu-id="3d6a1-116">لذلك، يمكن إنشاء صفحه محتوي تتضمن أجزاء خاصه بالقناة كمحتوي عبر القنوات المشتركة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-116">Therefore, a content page that contains channel-specific fragments can be created as cross-channel content.</span></span> <span data-ttu-id="3d6a1-117">في هذه الحالة ، علي الرغم من ان معظم المحتوي ستتم مشاركته بين القنوات ، الا ان الأجزاء الخاصة بالقناة في الصفحة عبر القنوات سيتم عرضها فقط عند طلبها من قناه واجهة المتجر المقابلة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-117">In this case, although most of the content will be shared among channels, channel-specific fragments on a cross-channel page will be rendered only when they are requested from the corresponding storefront channel.</span></span>

<span data-ttu-id="3d6a1-118">لن تستفيد المواقع التي تحتوي علي قناه واحده أو مواقع تحتوي علي قنوات متعددة لا يمكنها مشاركه المحتوي، من المشاركه عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-118">Sites that have only one channel, or sites that have multiple channels that can't share content, won't benefit from cross-channel sharing.</span></span>

## <a name="enable-cross-channel-sharing"></a><span data-ttu-id="3d6a1-119">تمكين المشاركة عبر القنوات</span><span class="sxs-lookup"><span data-stu-id="3d6a1-119">Enable cross-channel sharing</span></span>

<span data-ttu-id="3d6a1-120">يتم تمكين المشاركة عبر القنوات علي مستوى الموقع.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-120">Cross-channel sharing is enabled at the site level.</span></span> <span data-ttu-id="3d6a1-121">هذه العملية هي أحاديه الاتجاه.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-121">This operation is one-way.</span></span> <span data-ttu-id="3d6a1-122">بمعني آخر، بعد تمكين المشاركة عبر القنوات، لا يمكن تعطيلها.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-122">In other words, after cross-channel sharing is enabled, it can't be disabled.</span></span>

<span data-ttu-id="3d6a1-123">لتمكين المشاركة عبر القنوات في منشئ موقع التجارة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-123">To enable cross-channel sharing in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3d6a1-124">انتقل إلى **إعدادات الموقع \> الميزات**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-124">Go to **Site settings \> Features**.</span></span>
1. <span data-ttu-id="3d6a1-125">قم بتعيين الخيار لميزه **القناة المتداخلة** على **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-125">Set the option for the **Cross Channel** feature to **On**.</span></span>

    ![تم تعيين خيار عبر القنوات علي التشغيل في منشئ موقع التجارة](./media/enabling-cross-channel-sharing.png)

<span data-ttu-id="3d6a1-127">بعد تمكين المشاركة عبر القنوات، ستظهر المعلومات عبر القنوات في مقطع **القنوات** في **إعدادات الموقع\>الميزات**، كما في المثال الموجود في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-127">After you enable cross-channel sharing, cross-channel information will appear in the **Channels** section at **Site settings \> Features**, as the example in the following illustration shows.</span></span>

![معلومات القنوات مرئية بعد تمكين المشاركة عبر القنوات](./media/channels-cross-channel.png)

<span data-ttu-id="3d6a1-129">بالاضافه إلى ذلك، بعد تمكين المشاركة عبر القنوات، سيتضمن حقل **القناة** الموجود في اعلي اليمين من منشئ موقع التجارة خيار **مخزن القناة عبر الإنترنت** الذي يمكنك استخدامه لأداره محتوي القناة المتقاطعة، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-129">Additionally, after you enable cross-channel sharing, the **Channel** field in the upper right of Commerce site builder will include a **Cross Channel Online Store** option that you can use to manage cross-channel content, as shown in the following illustration.</span></span>

![خيار مخزن عبر القنوات على الإنترنت في حقل القنوات بعد تمكين المشاركة عبر القنوات](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a><span data-ttu-id="3d6a1-131">إنشاء محتوى عبر القنوات واستخدامه</span><span class="sxs-lookup"><span data-stu-id="3d6a1-131">Create and use cross-channel content</span></span>

<span data-ttu-id="3d6a1-132">يمكنك إنشاء محتوي عبر القنوات واستخدامه بطرق متعددة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-132">You can create and use cross-channel content in multiple ways.</span></span> <span data-ttu-id="3d6a1-133">علي سبيل المثال، يمكنك إنشاء الأجزاء ذات القنوات التبادلية، وإنشاء صفحات عبر القنوات التي تستخدم محتويات القناة العرضية والقنوات المحددة، وتخطي الأجزاء عبر القنوات بالنسخ الخاصة بالقنوات من الأجزاء.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-133">For example, you can create cross-channel fragments, create cross-channel pages that use cross-channel and channel-specific content, and override cross-channel fragments with channel-specific versions of fragments.</span></span>

### <a name="create-a-cross-channel-fragment"></a><span data-ttu-id="3d6a1-134">إنشاء جزء متعدد القنوات</span><span class="sxs-lookup"><span data-stu-id="3d6a1-134">Create a cross-channel fragment</span></span>

<span data-ttu-id="3d6a1-135">لإنشاء جزء عبر القنوات في منشئ موقع التجارة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-135">To create a cross-channel fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3d6a1-136">انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-136">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="3d6a1-137">في مربع الحوار **الجزء الجديد**، حدد الوحدة النمطية **شعار العرض الترويجي**، ثم، ضمن **اسم الجزء**، ادخل اسمًا (على سبيل المثال، **شعار عبر القنوات**).</span><span class="sxs-lookup"><span data-stu-id="3d6a1-137">In the **New fragment** dialog box, select the **Promo banner** module, and then, under **Fragment name**, enter a name (for example, **Cross-channel banner**).</span></span> <span data-ttu-id="3d6a1-138">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-138">Then select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-139">في جزء الخاصية في الوحدة النمطية **شعار العرض الترويجي**، حدد **إضافة رسالة**، ثم حدد **الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-139">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="3d6a1-140">في مربع حوار **الرسالة**، ضمن **نص**، ادخل **عبر القنوات** ، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-140">In the **Message** dialog box, under **Text**, enter **Cross-channel**, and the select **OK**.</span></span> 
1. <span data-ttu-id="3d6a1-141">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3d6a1-142">يمكن استخدام جزء عبر القنوات هذا علي صفحات عبر القنوات المتقاطعة أو القنوات الخاصة التي يتم إنشاؤها علي اي قناه موقع.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-142">This cross-channel fragment can be used on cross-channel or channel-specific pages that are created on any site channel.</span></span>

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a><span data-ttu-id="3d6a1-143">إنشاء صفحه عبر القناة تستخدم محتوي عبر القنوات</span><span class="sxs-lookup"><span data-stu-id="3d6a1-143">Create a cross-channel page that uses cross-channel content</span></span>

<span data-ttu-id="3d6a1-144">يمكن استخدام الصفحات عبر القنوات علي إيه قناه في الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-144">Cross-channel pages can be used on any channel of your site.</span></span> <span data-ttu-id="3d6a1-145">ولذلك، يمكنك إنشاء صفحه محتوي مشتركه مره واحده واجراء إيه تحديثات تاليه في مكان واحد.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-145">Therefore, you can create a shared content page one time and make any subsequent updates in a single place.</span></span> <span data-ttu-id="3d6a1-146">علي سبيل المثال، يمكن مشاركه صفحه **شروط وبنود** عبر القنوات التي لها URL `/toc` بين كافة القنوات في أحد المواقع.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-146">For example, a cross-channel **Terms and conditions** page that has the URL `/toc` can be shared among all the channels of a site.</span></span> <span data-ttu-id="3d6a1-147">إذا كانت عناوين URL الاساسيه الخاصة بقنوات الموقع هي `www.fabrikam.com/brand1` و`www.fabrikam.com/brand2`، ستتوفر صفحه **البنود والشروط المشتركة** من كل من عنوان URL لقناه الموقع، عند `www.fabrikam.com/brand1/toc` و`www.fabrikam.com/brand2/toc` على التوالي.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-147">If the base URLs for the site channels are `www.fabrikam.com/brand1` and `www.fabrikam.com/brand2`, the same cross-channel, shared **Terms and conditions** page will be available from both site channel URLs, at `www.fabrikam.com/brand1/toc` and `www.fabrikam.com/brand2/toc`, respectively.</span></span> <span data-ttu-id="3d6a1-148">إذا كان يجب تحديث **صفحه البنود والشروط** لاحقا، يجب تحديث الصفحة المشتركة الفردية فقط.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-148">If the **Terms and conditions** page must be updated later, you have to update only the single, shared page.</span></span>

<span data-ttu-id="3d6a1-149">لإنشاء صفحه عبر القنوات في منشئ المواقع التجارية الذي يستخدم محتوي عبر القنوات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-149">To create a cross-channel page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="3d6a1-150">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-150">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3d6a1-151">في مربع الحوار **اختيار قالب**، حدد قالب مثل **التسويق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-151">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="3d6a1-152">ضمن **اسم الصفحة**، ادخل اسم الصفحة (علي سبيل المثال، **صفحة عبر القنوات**).</span><span class="sxs-lookup"><span data-stu-id="3d6a1-152">Under **Page name**, enter a name for the page (for example, **Cross-channel page**).</span></span>
1. <span data-ttu-id="3d6a1-153">ضمن **عنوان URL للصفحة**، ادخل عنوان URL للصفحة (علي سبيل المثال، **examplepage**)، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-153">Under **Page URL**, enter a page URL (for example, **examplepage**), and then select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-154">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-154">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="3d6a1-155">في مربع الحوار **إضافة جزء**، حدد جزء عبر القنوات الذي قمت بإنشائه سابقًا والذي يحتوي على شعار عرض ترويجي، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-155">In the **Add fragment** dialog box, select the cross-channel fragment that you created earlier that has a promo banner, and then select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-156">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="3d6a1-157">يجب ان تشاهد شعار العرض الترويج الذي يقول، "عبر القنوات".</span><span class="sxs-lookup"><span data-stu-id="3d6a1-157">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="3d6a1-158">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a><span data-ttu-id="3d6a1-159">إنشاء صفحه خاصة بقناة تستخدم محتوي عبر القنوات</span><span class="sxs-lookup"><span data-stu-id="3d6a1-159">Create a channel-specific page that uses cross-channel content</span></span>

<span data-ttu-id="3d6a1-160">باستخدام محتوي عبر القنوات علي الصفحات الخاصة بالقناة، يمكنك إنشاء جزء محتوي مشترك مره واحده ثم استخدامه علي الصفحات الخاصة بقناة معينه.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-160">By using cross-channel content on channel-specific pages, you can create a shared content fragment one time and then use it on channel-specific pages.</span></span> <span data-ttu-id="3d6a1-161">يعد "المصدر الواحد" مفيدا للمحتوي المشترك مثل البنود والشروط أو شروط الدفع أو معلومات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-161">This "single sourcing" is useful for shared content such as terms and conditions, payment terms, or contact information.</span></span>

<span data-ttu-id="3d6a1-162">لإنشاء صفحه قناة معينة في منشئ المواقع التجارية الذي يستخدم محتوي عبر القنوات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-162">To create a channel-specific page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="3d6a1-163">من داخل قناه معينه، مثل **متجر Fabrikam الممتد علي الإنترنت**، انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحه جديده.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-163">From within a specific channel, such as **Fabrikam extended online store**, go to **Pages**, and then select **New** to create a new page.</span></span>
1. <span data-ttu-id="3d6a1-164">في مربع الحوار **اختيار قالب**، حدد قالب مثل **التسويق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-164">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="3d6a1-165">ضمن **اسم الصفحة**، ادخل اسم الصفحة (علي سبيل المثال، **صفحة قناة معينة**).</span><span class="sxs-lookup"><span data-stu-id="3d6a1-165">Under **Page name**, enter a name for the page (for example, **Channel-specific page**).</span></span>
1. <span data-ttu-id="3d6a1-166">ضمن **عنوان URL للصفحة**، ادخل عنوان URL للصفحة (علي سبيل المثال، **channelspecificpage**)، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-166">Under **Page URL**, enter a page URL (for example, **channelspecificpage**), and then select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-167">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-167">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="3d6a1-168">في مربع الحوار **إضافة جزء**، ضمن **القناة**، حدد **المتجر على الإنترنت عبر القنوات**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-168">In the **Add fragment** dialog box, under **Channel**, select **Cross Channel Online Store**.</span></span> <span data-ttu-id="3d6a1-169">يجب ان يظهر جزء عبر القنوات الذي قمت بإنشائه سابقا في القائمة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-169">The cross-channel fragment that you created earlier should appear in the list.</span></span> <span data-ttu-id="3d6a1-170">حدده، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-170">Select it, and then select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-171">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-171">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="3d6a1-172">يجب ان تشاهد شعار العرض الترويج الذي يقول، "عبر القنوات".</span><span class="sxs-lookup"><span data-stu-id="3d6a1-172">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="3d6a1-173">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a><span data-ttu-id="3d6a1-174">إنشاء إصدار خاص بقناة تستخدم محتوي عبر القنوات</span><span class="sxs-lookup"><span data-stu-id="3d6a1-174">Create a channel-specific version of a cross-channel page</span></span>

<span data-ttu-id="3d6a1-175">تدعم المشاركه عبر القنوات تجاوزات المحتوي عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-175">Cross-channel sharing supports overrides of cross-channel content.</span></span> <span data-ttu-id="3d6a1-176">علي سبيل المثال ، تشترك كل قناه من قنوات الموقع الخاصة بك في نفس جزء المحتوي.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-176">For example, all but one of your site channels share the same piece of content.</span></span> <span data-ttu-id="3d6a1-177">تتطلب أحدي قنوات الموقع وجود محتوي مختلف.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-177">That one site channel requires different content.</span></span> <span data-ttu-id="3d6a1-178">لتنفيذ المحتوي المختلف له، فانك تتجاوز المحتوي عبر القنوات بمحتوي خاص بالقناة بإنشاء إصدار خاص بقناة من الصفحة عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-178">To implement the different content for it, you override the cross-channel content with channel-specific content by creating a channel-specific version of the cross-channel page.</span></span>

<span data-ttu-id="3d6a1-179">لإنشاء إصدار قناة معينة لصفحة عبر القنوات في منشئ المواقع التجارية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-179">To create a channel-specific version of a cross-channel page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3d6a1-180">في حقل **القناة** في الركن الأيسر العلوي، حدد **متجر عبر الإنترنت عبر القنوات**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-180">In the **Channel** field in the upper right, select **Cross Channel Online Store**.</span></span>
1. <span data-ttu-id="3d6a1-181">افتح الصفحة عبر القنوات التي قمت بإنشائها مسبقا.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-181">Open the cross-channel page that you created earlier.</span></span>
1. <span data-ttu-id="3d6a1-182">في حقل **القناة** في الجزء الأيمن العلوي، حدد القناة التي يجب ان يكون لها محتوي محدد.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-182">In the **Channel** field in the upper right, select the channel that should have specific content.</span></span> <span data-ttu-id="3d6a1-183">يعرض محرر الصفحة رسالة تطالبك بإنشاء متغير صفحه جديد.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-183">The page editor shows a message that prompts you to create a new page variant.</span></span>
1. <span data-ttu-id="3d6a1-184">حدد **إنشاء متغير صفحة**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-184">Select **Create page variant**.</span></span>
1. <span data-ttu-id="3d6a1-185">في الفترة **الرئيسية‏‎** لمتغير الصفحة، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-185">In the **Main** slot of the page variant, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3d6a1-186">في مربع الحوار **إضافة وحدة نمطية**، حدد وحدة ‬‏‫**شعار العرض الترويجي‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-186">In the **Add Module** dialog box, select the **Promo banner** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-187">في جزء الخاصية في الوحدة النمطية **شعار العرض الترويجي**، حدد **إضافة رسالة**، ثم حدد **الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-187">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="3d6a1-188">في مربع حوار **الرسالة**، ضمن **نص**، ادخل **خاص بالقناة**، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-188">In the **Message** dialog box, under **Text**, enter **Channel-specific**, and the select **OK**.</span></span>
1. <span data-ttu-id="3d6a1-189">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-189">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="3d6a1-190">يجب ان تشاهد شعار العرض الترويج الذي يقول، "خاصة بالقناة".</span><span class="sxs-lookup"><span data-stu-id="3d6a1-190">You should see the promo banner that says, "Channel-specific."</span></span>
1. <span data-ttu-id="3d6a1-191">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-191">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3d6a1-192">والآن، إذا كنت تستخدم محدد موقع المعلومات الأساسي الخاص بالقناة وانتقلت إلى عنوان URL الخاص بالصفحة عبر القنوات الموجودة علي هذا الموقع، ستشاهد محتوي القناة الخاصة بها بدلا من المحتوي عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="3d6a1-192">Now, if you use the base URL of the channel and go to the URL of the cross-channel page on that site, you will see the channel-specific content instead of the cross-channel content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d6a1-193">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3d6a1-193">Additional resources</span></span>

[<span data-ttu-id="3d6a1-194">طرق إضافة المحتوى</span><span class="sxs-lookup"><span data-stu-id="3d6a1-194">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="3d6a1-195">مصطلحات نموذج الصفحة</span><span class="sxs-lookup"><span data-stu-id="3d6a1-195">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="3d6a1-196">حالات المستند ودورة الحياة</span><span class="sxs-lookup"><span data-stu-id="3d6a1-196">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="3d6a1-197">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="3d6a1-197">Work with publish groups</span></span>](publish-groups.md)
