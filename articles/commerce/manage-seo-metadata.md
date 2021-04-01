---
title: إدارة بيانات تعريف SEO
description: يوضح هذا الموضوع كيفية إدارة بيانات تعريف تحسين محرك البحث في Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00942befef9f9b6a878766bbbb5341426e31db2c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252596"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="1bcf0-103">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="1bcf0-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1bcf0-104">يوضح هذا الموضوع كيفية إدارة بيانات تعريف تحسين محرك البحث في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1bcf0-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-105">Overview</span></span>

<span data-ttu-id="1bcf0-106">يمكن إدارة بيانات تعريف تحسين محرك البحث لموقع باستخدام خريطة الموقع وبيانات تعريف الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="1bcf0-107">خرائط المواقع</span><span class="sxs-lookup"><span data-stu-id="1bcf0-107">Site maps</span></span>

<span data-ttu-id="1bcf0-108">خريطة الموقع هي عبارة عن قائمة يمكن للجهاز قراءتها، بتنسيق XML، للصفحات الموجودة على موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="1bcf0-109">والهدف منها هو استخدامها من قبل محركات البحث، بحيث يمكنها توفير نتائج بحث أفضل من الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="1bcf0-110">يمكن تضمين خرائط المواقع يدويًا من خلال محركات البحث أو نشرها في ملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="1bcf0-111">يدعم تطبيق Dynamics 365 Commerce الإنشاء التلقائي لخرائط المواقع.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="1bcf0-112">يتم تحديث خرائط المواقع تلقائيًا عند نشر الصفحات وإلغاء نشرها.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="1bcf0-113">تشغيل إنشاء خريطة الموقع</span><span class="sxs-lookup"><span data-stu-id="1bcf0-113">Turn on site map generation</span></span>

1. <span data-ttu-id="1bcf0-114">سجل الدخول إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="1bcf0-115">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="1bcf0-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1bcf0-116">في جزء التنقل علي اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="1bcf0-117">تأكد من تشغيل الخيار **خريطة الموقع ممكنة**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="1bcf0-118">بيانات تعريف الصفحة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-118">Page metadata</span></span>

<span data-ttu-id="1bcf0-119">يتيح لك تطبيق Dynamics 365 Commerce إدارة بيانات تعريف تحسين محرك البحث للصفحات الفردية.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="1bcf0-120">يمكنك عرض هذه المعلومات وتعديلها في الجزء **خصائص SEO** لحاوية الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="1bcf0-121">يتم حاليًا اعتماد خصائص بيانات تعريف SEO التالية:</span><span class="sxs-lookup"><span data-stu-id="1bcf0-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="1bcf0-122">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="1bcf0-122">Title</span></span>
- <span data-ttu-id="1bcf0-123">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="1bcf0-123">Description</span></span>
- <span data-ttu-id="1bcf0-124">كلمات SEO الأساسية</span><span class="sxs-lookup"><span data-stu-id="1bcf0-124">SEO keywords</span></span>
- <span data-ttu-id="1bcf0-125">تسميات Aria</span><span class="sxs-lookup"><span data-stu-id="1bcf0-125">Aria labels</span></span>
- <span data-ttu-id="1bcf0-126">noindex</span><span class="sxs-lookup"><span data-stu-id="1bcf0-126">noindex</span></span>
- <span data-ttu-id="1bcf0-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="1bcf0-127">nofollow</span></span>
- <span data-ttu-id="1bcf0-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="1bcf0-128">noarchive</span></span>
- <span data-ttu-id="1bcf0-129">nocache</span><span class="sxs-lookup"><span data-stu-id="1bcf0-129">nocache</span></span>
- <span data-ttu-id="1bcf0-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="1bcf0-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="1bcf0-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="1bcf0-131">nosnippet</span></span>
- <span data-ttu-id="1bcf0-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="1bcf0-132">noImageIndex</span></span>
- <span data-ttu-id="1bcf0-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="1bcf0-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="1bcf0-134">تعديل بيانات تعريف الصفحة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-134">Modify page metadata</span></span>

<span data-ttu-id="1bcf0-135">لتعديل بيانات تعريف صفحة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="1bcf0-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="1bcf0-136">ضمن **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="1bcf0-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1bcf0-137">في جزء التنقل على اليسار، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="1bcf0-138">حدد الصفحة الرئيسية لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="1bcf0-139">في شريط الأوامر، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="1bcf0-140">في جزء الخصائص الموجود على اليسار، قم بتوسيع **علامات التعريف الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="1bcf0-141">لإضافة علامة تعريف جديدة، حدد **إضافة**، ثم أدخل العلامة في الحقل.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="1bcf0-142">لإزالة علامة تعريفموجودة، حدد رمز سلة المهملات على اليمين.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="1bcf0-143">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="1bcf0-144">في حقل **التعليقات**، أدخل **علامات التعريف المحدثة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="1bcf0-145">حدد **معاينة** لمعاينه الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="1bcf0-146">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="1bcf0-147">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="1bcf0-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bcf0-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1bcf0-148">Additional resources</span></span>

[<span data-ttu-id="1bcf0-149">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="1bcf0-150">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1bcf0-151">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1bcf0-152">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="1bcf0-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1bcf0-153">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="1bcf0-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1bcf0-154">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="1bcf0-155">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="1bcf0-155">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="1bcf0-156">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="1bcf0-156">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]