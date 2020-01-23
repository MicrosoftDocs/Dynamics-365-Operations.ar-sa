---
title: إدارة بيانات تعريف SEO
description: يوضح هذا الموضوع كيفية إدارة بيانات تعريف تحسين محرك البحث في Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ea06713af69659c205686a971393892fa584072
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945710"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="c68a6-103">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="c68a6-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c68a6-104">يوضح هذا الموضوع كيفية إدارة بيانات تعريف تحسين محرك البحث في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c68a6-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c68a6-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c68a6-105">Overview</span></span>

<span data-ttu-id="c68a6-106">يمكن إدارة بيانات تعريف تحسين محرك البحث لموقع باستخدام خريطة الموقع وبيانات تعريف الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c68a6-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="c68a6-107">خرائط المواقع</span><span class="sxs-lookup"><span data-stu-id="c68a6-107">Site maps</span></span>

<span data-ttu-id="c68a6-108">خريطة الموقع هي عبارة عن قائمة يمكن للجهاز قراءتها، بتنسيق XML، للصفحات الموجودة على موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c68a6-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="c68a6-109">والهدف منها هو استخدامها من قبل محركات البحث، بحيث يمكنها توفير نتائج بحث أفضل من الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c68a6-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="c68a6-110">يمكن تضمين خرائط المواقع يدويًا من خلال محركات البحث أو نشرها في ملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="c68a6-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="c68a6-111">يدعم تطبيق Dynamics 365 Commerce الإنشاء التلقائي لخرائط المواقع.</span><span class="sxs-lookup"><span data-stu-id="c68a6-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="c68a6-112">يتم تحديث خرائط المواقع تلقائيًا عند نشر الصفحات وإلغاء نشرها.</span><span class="sxs-lookup"><span data-stu-id="c68a6-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="c68a6-113">تشغيل إنشاء خريطة الموقع</span><span class="sxs-lookup"><span data-stu-id="c68a6-113">Turn on site map generation</span></span>

1. <span data-ttu-id="c68a6-114">سجل الدخول إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="c68a6-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="c68a6-115">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="c68a6-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="c68a6-116">في جزء التنقل علي اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="c68a6-117">تأكد من تشغيل الخيار **خريطة الموقع ممكنة**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="c68a6-118">بيانات تعريف الصفحة</span><span class="sxs-lookup"><span data-stu-id="c68a6-118">Page metadata</span></span>

<span data-ttu-id="c68a6-119">يتيح لك تطبيق Dynamics 365 Commerce إدارة بيانات تعريف تحسين محرك البحث للصفحات الفردية.</span><span class="sxs-lookup"><span data-stu-id="c68a6-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="c68a6-120">يمكنك عرض هذه المعلومات وتعديلها في الجزء **خصائص SEO** لحاوية الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c68a6-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="c68a6-121">يتم حاليًا اعتماد خصائص بيانات تعريف SEO التالية:</span><span class="sxs-lookup"><span data-stu-id="c68a6-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="c68a6-122">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="c68a6-122">Title</span></span>
- <span data-ttu-id="c68a6-123">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="c68a6-123">Description</span></span>
- <span data-ttu-id="c68a6-124">كلمات SEO الأساسية</span><span class="sxs-lookup"><span data-stu-id="c68a6-124">SEO keywords</span></span>
- <span data-ttu-id="c68a6-125">تسميات Aria</span><span class="sxs-lookup"><span data-stu-id="c68a6-125">Aria labels</span></span>
- <span data-ttu-id="c68a6-126">noindex</span><span class="sxs-lookup"><span data-stu-id="c68a6-126">noindex</span></span>
- <span data-ttu-id="c68a6-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="c68a6-127">nofollow</span></span>
- <span data-ttu-id="c68a6-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="c68a6-128">noarchive</span></span>
- <span data-ttu-id="c68a6-129">nocache</span><span class="sxs-lookup"><span data-stu-id="c68a6-129">nocache</span></span>
- <span data-ttu-id="c68a6-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="c68a6-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="c68a6-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="c68a6-131">nosnippet</span></span>
- <span data-ttu-id="c68a6-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="c68a6-132">noImageIndex</span></span>
- <span data-ttu-id="c68a6-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="c68a6-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="c68a6-134">تعديل بيانات تعريف الصفحة</span><span class="sxs-lookup"><span data-stu-id="c68a6-134">Modify page metadata</span></span>

<span data-ttu-id="c68a6-135">لتعديل بيانات تعريف صفحة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c68a6-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="c68a6-136">ضمن **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="c68a6-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="c68a6-137">في جزء التنقل على اليسار، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="c68a6-138">حدد الصفحة الرئيسية لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c68a6-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="c68a6-139">في جزء الإجراءات، حدد **سحب**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="c68a6-140">في جزء الخصائص الموجود على اليسار، قم بتوسيع **علامات التعريف الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="c68a6-141">لإضافة علامة تعريف جديدة، حدد **إضافة**، ثم أدخل العلامة في الحقل.</span><span class="sxs-lookup"><span data-stu-id="c68a6-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="c68a6-142">لإزالة علامة تعريفموجودة، حدد رمز سلة المهملات على اليمين.</span><span class="sxs-lookup"><span data-stu-id="c68a6-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="c68a6-143">حدد **حفظ**، ثم قم بتحديد **إيداع**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="c68a6-144">في حقل **التعليقات**، أدخل **علامات التعريف المحدثة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="c68a6-145">حدد **معاينة** لمعاينه الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c68a6-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="c68a6-146">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="c68a6-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="c68a6-147">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c68a6-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c68a6-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c68a6-148">Additional resources</span></span>

[<span data-ttu-id="c68a6-149">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="c68a6-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="c68a6-150">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="c68a6-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="c68a6-151">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="c68a6-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c68a6-152">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="c68a6-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c68a6-153">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="c68a6-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c68a6-154">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="c68a6-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="c68a6-155">التحقق من إمكانية الوصول إلى محتوي الصفحة</span><span class="sxs-lookup"><span data-stu-id="c68a6-155">Verify page content accessibility</span></span>](verify-accessibility.md)
