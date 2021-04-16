---
title: إدارة بيانات تعريف SEO
description: يوضح هذا الموضوع كيفية إدارة بيانات تعريف تحسين محرك البحث في Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794201"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="21f05-103">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="21f05-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="21f05-104">يوضح هذا الموضوع كيفية إدارة بيانات تعريف تحسين محرك البحث في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21f05-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="21f05-105">يمكن إدارة بيانات تعريف تحسين محرك البحث لموقع باستخدام خريطة الموقع وبيانات تعريف الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21f05-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="21f05-106">خرائط المواقع</span><span class="sxs-lookup"><span data-stu-id="21f05-106">Site maps</span></span>

<span data-ttu-id="21f05-107">خريطة الموقع هي عبارة عن قائمة يمكن للجهاز قراءتها، بتنسيق XML، للصفحات الموجودة على موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="21f05-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="21f05-108">والهدف منها هو استخدامها من قبل محركات البحث، بحيث يمكنها توفير نتائج بحث أفضل من الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="21f05-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="21f05-109">يمكن تضمين خرائط المواقع يدويًا من خلال محركات البحث أو نشرها في ملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="21f05-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="21f05-110">يدعم تطبيق Dynamics 365 Commerce الإنشاء التلقائي لخرائط المواقع.</span><span class="sxs-lookup"><span data-stu-id="21f05-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="21f05-111">يتم تحديث خرائط المواقع تلقائيًا عند نشر الصفحات وإلغاء نشرها.</span><span class="sxs-lookup"><span data-stu-id="21f05-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="21f05-112">تشغيل إنشاء خريطة الموقع</span><span class="sxs-lookup"><span data-stu-id="21f05-112">Turn on site map generation</span></span>

1. <span data-ttu-id="21f05-113">سجل الدخول إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="21f05-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="21f05-114">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="21f05-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="21f05-115">في جزء التنقل علي اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="21f05-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="21f05-116">تأكد من تشغيل الخيار **خريطة الموقع ممكنة**.</span><span class="sxs-lookup"><span data-stu-id="21f05-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="21f05-117">بيانات تعريف الصفحة</span><span class="sxs-lookup"><span data-stu-id="21f05-117">Page metadata</span></span>

<span data-ttu-id="21f05-118">يتيح لك تطبيق Dynamics 365 Commerce إدارة بيانات تعريف تحسين محرك البحث للصفحات الفردية.</span><span class="sxs-lookup"><span data-stu-id="21f05-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="21f05-119">يمكنك عرض هذه المعلومات وتعديلها في الجزء **خصائص SEO** لحاوية الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21f05-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="21f05-120">يتم حاليًا اعتماد خصائص بيانات تعريف SEO التالية:</span><span class="sxs-lookup"><span data-stu-id="21f05-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="21f05-121">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="21f05-121">Title</span></span>
- <span data-ttu-id="21f05-122">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="21f05-122">Description</span></span>
- <span data-ttu-id="21f05-123">كلمات SEO الأساسية</span><span class="sxs-lookup"><span data-stu-id="21f05-123">SEO keywords</span></span>
- <span data-ttu-id="21f05-124">تسميات Aria</span><span class="sxs-lookup"><span data-stu-id="21f05-124">Aria labels</span></span>
- <span data-ttu-id="21f05-125">noindex</span><span class="sxs-lookup"><span data-stu-id="21f05-125">noindex</span></span>
- <span data-ttu-id="21f05-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="21f05-126">nofollow</span></span>
- <span data-ttu-id="21f05-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="21f05-127">noarchive</span></span>
- <span data-ttu-id="21f05-128">nocache</span><span class="sxs-lookup"><span data-stu-id="21f05-128">nocache</span></span>
- <span data-ttu-id="21f05-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="21f05-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="21f05-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="21f05-130">nosnippet</span></span>
- <span data-ttu-id="21f05-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="21f05-131">noImageIndex</span></span>
- <span data-ttu-id="21f05-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="21f05-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="21f05-133">تعديل بيانات تعريف الصفحة</span><span class="sxs-lookup"><span data-stu-id="21f05-133">Modify page metadata</span></span>

<span data-ttu-id="21f05-134">لتعديل بيانات تعريف صفحة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="21f05-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="21f05-135">ضمن **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="21f05-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="21f05-136">في جزء التنقل على اليسار، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="21f05-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="21f05-137">حدد الصفحة الرئيسية لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21f05-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="21f05-138">في شريط الأوامر، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="21f05-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="21f05-139">في جزء الخصائص الموجود على اليسار، قم بتوسيع **علامات التعريف الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="21f05-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="21f05-140">لإضافة علامة تعريف جديدة، حدد **إضافة**، ثم أدخل العلامة في الحقل.</span><span class="sxs-lookup"><span data-stu-id="21f05-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="21f05-141">لإزالة علامة تعريفموجودة، حدد رمز سلة المهملات على اليمين.</span><span class="sxs-lookup"><span data-stu-id="21f05-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="21f05-142">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="21f05-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="21f05-143">في حقل **التعليقات**، أدخل **علامات التعريف المحدثة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="21f05-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="21f05-144">حدد **معاينة** لمعاينه الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="21f05-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="21f05-145">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="21f05-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="21f05-146">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="21f05-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21f05-147">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="21f05-147">Additional resources</span></span>

[<span data-ttu-id="21f05-148">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="21f05-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="21f05-149">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="21f05-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="21f05-150">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="21f05-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="21f05-151">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="21f05-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="21f05-152">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="21f05-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="21f05-153">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="21f05-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="21f05-154">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="21f05-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="21f05-155">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="21f05-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
