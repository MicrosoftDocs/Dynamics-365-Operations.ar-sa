---
title: إضافة صفحة موقع جديدة
description: يصف هذا الموضوع كيفية إضافة صفحة موقع جديدة في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797541"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="acbe3-103">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="acbe3-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="acbe3-104">يصف هذا الموضوع كيفية إضافة صفحة موقع جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="acbe3-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="acbe3-105">بعد إنشاء القوالب والأجزاء الخاصة بموقعك، فإن الخطوة التالية هي البدء في إنشاء صفحات تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="acbe3-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="acbe3-106">للبدء، يجب عليك تحديد قالب أو تخطيط واسم صفحة وعنوان URL للصفحة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="acbe3-107">قالب أو تخطيط</span><span class="sxs-lookup"><span data-stu-id="acbe3-107">Template or layout</span></span>

<span data-ttu-id="acbe3-108">يمكنك استخدام قالب أو تخطيط لصفحتك الجديدة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="acbe3-109">لمزيد من المعلومات ، راجع [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="acbe3-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="acbe3-110">اسم الصفحة</span><span class="sxs-lookup"><span data-stu-id="acbe3-110">Page name</span></span>

<span data-ttu-id="acbe3-111">يجب أن يكون اسم الصفحة فريدًا لصفحتك.</span><span class="sxs-lookup"><span data-stu-id="acbe3-111">The page name must be unique to your page.</span></span> <span data-ttu-id="acbe3-112">يجب أن يكون وصفيًا، حتى تتمكن من العثور عليه بسهولة ويعرف الآخرون المقصود من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="acbe3-113">اختر اسم الصفحة بعناية، لأنه لا يمكن تغييره لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="acbe3-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="acbe3-114">عنوان URL للصفحة</span><span class="sxs-lookup"><span data-stu-id="acbe3-114">Page URL</span></span>

<span data-ttu-id="acbe3-115">يمكنك الحصول على خيار إدخال عنوان URL لصفحتك الجديدة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="acbe3-116">عند إنشاء صفحة ، يمكنك إدخال سلسلة يتم استخدامها لتشكيل عنوان URL كامل.</span><span class="sxs-lookup"><span data-stu-id="acbe3-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="acbe3-117">تُعرف هذه السلسلة بعنوان URL المرتبط أو عنوان URL الوصفي.</span><span class="sxs-lookup"><span data-stu-id="acbe3-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="acbe3-118">ثم يتم إنشاء عنوان URL كامل استنادًا إلى عنوان URL الوصفي، ويتم تعيين الصفحة الجديدة إليها.</span><span class="sxs-lookup"><span data-stu-id="acbe3-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="acbe3-119">يمكنك تغيير عنوان URL في وقت لاحق، قبل نشر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="acbe3-120">لمزيد من المعلومات، راجع [إنشاء عنوان URL للصفحة](create-page-URL.md)</span><span class="sxs-lookup"><span data-stu-id="acbe3-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="acbe3-121">يفصل Dynamics 365 Commerce عناوين URL والمحتوى.</span><span class="sxs-lookup"><span data-stu-id="acbe3-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="acbe3-122">بمعنى آخر، يمكن إنشاء صفحة غير مرتبطة بعنوان URL، ويمكن إنشاء عنوان URL غير مرتبط بصفحة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="acbe3-123">لذلك، يمكن إجراء تبديل المحتوى لعنوان URL ولا يتطلب تعطيلاً، كما أن عمليات إعادة التوجيه أسهل في إدارتها.</span><span class="sxs-lookup"><span data-stu-id="acbe3-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="acbe3-124">إضافة صفحة جديدة</span><span class="sxs-lookup"><span data-stu-id="acbe3-124">Add a new page</span></span>

<span data-ttu-id="acbe3-125">لإضافة صفحة موقع جديدة إلى موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="acbe3-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="acbe3-126">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="acbe3-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="acbe3-127">حدد **صفحة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-127">Select **New Page**.</span></span>
1. <span data-ttu-id="acbe3-128">في مربع الحوار **صفحة جديدة** ، حدد قالب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="acbe3-129">في الحقل **اسم الصفحة** ، ادخل اسم الصفحة (علي سبيل المثال، **صفحتي الجديدة**).</span><span class="sxs-lookup"><span data-stu-id="acbe3-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="acbe3-130">في الحقل **URL** ، أدخل سلسلة (URL slug) لإكمال عنوان URL (على سبيل المثال، **صفحتي_الجديدة**).</span><span class="sxs-lookup"><span data-stu-id="acbe3-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="acbe3-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-131">Select **OK**.</span></span> <span data-ttu-id="acbe3-132">يظهر محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-132">The page editor appears.</span></span> <span data-ttu-id="acbe3-133">لاحظ أنه يتم إضافة عنوان وتذييل تلقائيًا إلى الصفحة، استنادًا إلى القالب الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="acbe3-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="acbe3-134">في مخطط الصفحة، حدد فتحة **الرئيسية** ، وحدد زر علامة القطع (**...**) ، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="acbe3-135">حدد **الحاوية**، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="acbe3-136">حدد **حاوية السائل**، حدد زر علامة الحذف، ثم حدد **‏‫إضافة وحدة نمطية**‬.</span><span class="sxs-lookup"><span data-stu-id="acbe3-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="acbe3-137">حدد **كتلة تنسيق المحتوى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="acbe3-138">حدد **كتلة تنسيق المحتوى**، حدد زر علامة الحذف، ثم حدد **‏‫إضافة وحدة نمطية**‬.</span><span class="sxs-lookup"><span data-stu-id="acbe3-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="acbe3-139">حدد **عنصر كتلة تنسيق المحتوى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="acbe3-140">في جزء الخصائص الموجود علي اليمين، حدد **فقرة**، ثم في الحقل، أدخل **نص الاختبار الخاص بي**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="acbe3-141">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="acbe3-142">في حقل **التعليقات** ، أدخل **إضافة صفحة جديدة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="acbe3-143">حدد **معاينة** لمعاينه الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="acbe3-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="acbe3-144">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="acbe3-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="acbe3-145">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-145">Select **Publish**.</span></span>
1. <span data-ttu-id="acbe3-146">في مسار التنقل (عناوين) ، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="acbe3-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="acbe3-147">في جزء التنقل علي اليسار، حدد **عناوين URL**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="acbe3-148">ابحث عن وحدد عنوان URL لـ (**mynewpage**) الخاص بك في القائمة.</span><span class="sxs-lookup"><span data-stu-id="acbe3-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="acbe3-149">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="acbe3-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acbe3-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="acbe3-150">Additional resources</span></span>

[<span data-ttu-id="acbe3-151">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="acbe3-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="acbe3-152">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="acbe3-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="acbe3-153">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="acbe3-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="acbe3-154">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="acbe3-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="acbe3-155">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="acbe3-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="acbe3-156">إثراء صفحة فئة منتقل إليها‬</span><span class="sxs-lookup"><span data-stu-id="acbe3-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="acbe3-157">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="acbe3-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="acbe3-158">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="acbe3-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
