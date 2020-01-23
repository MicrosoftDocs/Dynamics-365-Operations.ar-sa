---
title: إضافة صفحة موقع جديدة
description: يصف هذا الموضوع كيفية إضافة صفحة موقع جديدة في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1993e58108ad73aad4adf382bb03ec2e62231add
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945595"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="c339b-103">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="c339b-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c339b-104">يصف هذا الموضوع كيفية إضافة صفحة موقع جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c339b-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c339b-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c339b-105">Overview</span></span>

<span data-ttu-id="c339b-106">بعد إنشاء القوالب والأجزاء الخاصة بموقعك، فإن الخطوة التالية هي البدء في إنشاء صفحات تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="c339b-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="c339b-107">للبدء، يجب عليك تحديد قالب أو تخطيط واسم صفحة وعنوان URL للصفحة.</span><span class="sxs-lookup"><span data-stu-id="c339b-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="c339b-108">قالب أو تخطيط</span><span class="sxs-lookup"><span data-stu-id="c339b-108">Template or layout</span></span>

<span data-ttu-id="c339b-109">يمكنك استخدام قالب أو تخطيط لصفحتك الجديدة.</span><span class="sxs-lookup"><span data-stu-id="c339b-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="c339b-110">لمزيد من المعلومات ، راجع [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c339b-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="c339b-111">اسم الصفحة</span><span class="sxs-lookup"><span data-stu-id="c339b-111">Page name</span></span>

<span data-ttu-id="c339b-112">يجب أن يكون اسم الصفحة فريدًا لصفحتك.</span><span class="sxs-lookup"><span data-stu-id="c339b-112">The page name must be unique to your page.</span></span> <span data-ttu-id="c339b-113">يجب أن يكون وصفيًا، حتى تتمكن من العثور عليه بسهولة ويعرف الآخرون المقصود من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c339b-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="c339b-114">اختر اسم الصفحة بعناية، لأنه لا يمكن تغييره لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="c339b-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="c339b-115">عنوان URL للصفحة</span><span class="sxs-lookup"><span data-stu-id="c339b-115">Page URL</span></span>

<span data-ttu-id="c339b-116">يمكنك الحصول على خيار إدخال عنوان URL لصفحتك الجديدة.</span><span class="sxs-lookup"><span data-stu-id="c339b-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="c339b-117">عند إنشاء صفحة ، يمكنك إدخال سلسلة يتم استخدامها لتشكيل عنوان URL كامل.</span><span class="sxs-lookup"><span data-stu-id="c339b-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="c339b-118">تُعرف هذه السلسلة بعنوان URL المرتبط أو عنوان URL الوصفي.</span><span class="sxs-lookup"><span data-stu-id="c339b-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="c339b-119">ثم يتم إنشاء عنوان URL كامل استنادًا إلى عنوان URL الوصفي، ويتم تعيين الصفحة الجديدة إليها.</span><span class="sxs-lookup"><span data-stu-id="c339b-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="c339b-120">يمكنك تغيير عنوان URL في وقت لاحق، قبل نشر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c339b-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="c339b-121">لمزيد من المعلومات، راجع [إنشاء عنوان URL للصفحة](create-page-URL.md)</span><span class="sxs-lookup"><span data-stu-id="c339b-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c339b-122">يفصل Dynamics 365 Commerce عناوين URL والمحتوى.</span><span class="sxs-lookup"><span data-stu-id="c339b-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="c339b-123">بمعنى آخر، يمكن إنشاء صفحة غير مرتبطة بعنوان URL، ويمكن إنشاء عنوان URL غير مرتبط بصفحة.</span><span class="sxs-lookup"><span data-stu-id="c339b-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="c339b-124">لذلك، يمكن إجراء تبديل المحتوى لعنوان URL ولا يتطلب تعطيلاً، كما أن عمليات إعادة التوجيه أسهل في إدارتها.</span><span class="sxs-lookup"><span data-stu-id="c339b-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="c339b-125">إضافة صفحة جديدة</span><span class="sxs-lookup"><span data-stu-id="c339b-125">Add a new page</span></span>

<span data-ttu-id="c339b-126">لإضافة صفحة موقع جديدة إلى موقعك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c339b-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="c339b-127">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="c339b-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="c339b-128">حدد **صفحة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="c339b-128">Select **New Page**.</span></span>
1. <span data-ttu-id="c339b-129">في مربع الحوار **صفحة جديدة** ، حدد قالب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c339b-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="c339b-130">في الحقل **اسم الصفحة** ، ادخل اسم الصفحة (علي سبيل المثال، **صفحتي الجديدة**).</span><span class="sxs-lookup"><span data-stu-id="c339b-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="c339b-131">في الحقل **URL** ، أدخل سلسلة (URL slug) لإكمال عنوان URL (على سبيل المثال، **صفحتي_الجديدة**).</span><span class="sxs-lookup"><span data-stu-id="c339b-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="c339b-132">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c339b-132">Select **OK**.</span></span> <span data-ttu-id="c339b-133">يظهر محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c339b-133">The page editor appears.</span></span> <span data-ttu-id="c339b-134">لاحظ أنه يتم إضافة عنوان وتذييل تلقائيًا إلى الصفحة، استنادًا إلى القالب الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="c339b-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="c339b-135">في مخطط الصفحة، حدد فتحة **الرئيسية** ، وحدد زر علامة القطع (**...**) ، ثم حدد **إضافة وحدة نمطية**.</span><span class="sxs-lookup"><span data-stu-id="c339b-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c339b-136">حدد **الحاوية**، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c339b-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="c339b-137">حدد **حاوية السائل**، حدد زر علامة الحذف، ثم حدد **‏‫إضافة وحدة نمطية**‬.</span><span class="sxs-lookup"><span data-stu-id="c339b-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="c339b-138">حدد **كتلة تنسيق المحتوى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c339b-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="c339b-139">حدد **كتلة تنسيق المحتوى**، حدد زر علامة الحذف، ثم حدد **‏‫إضافة وحدة نمطية**‬.</span><span class="sxs-lookup"><span data-stu-id="c339b-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="c339b-140">حدد **عنصر كتلة تنسيق المحتوى**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c339b-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="c339b-141">في جزء الخصائص الموجود علي اليمين، حدد **فقرة**، ثم في الحقل، أدخل **نص الاختبار الخاص بي**.</span><span class="sxs-lookup"><span data-stu-id="c339b-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="c339b-142">حدد **حفظ**، ثم قم بتحديد **إيداع**.</span><span class="sxs-lookup"><span data-stu-id="c339b-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="c339b-143">في حقل **التعليقات** ، أدخل **إضافة صفحة جديدة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c339b-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c339b-144">حدد **معاينة** لمعاينه الصفحة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c339b-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="c339b-145">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="c339b-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="c339b-146">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c339b-146">Select **Publish**.</span></span>
1. <span data-ttu-id="c339b-147">في مسار التنقل (عناوين) ، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="c339b-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="c339b-148">في جزء التنقل علي اليسار، حدد **عناوين URL**.</span><span class="sxs-lookup"><span data-stu-id="c339b-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="c339b-149">ابحث عن وحدد عنوان URL لـ (**mynewpage**) الخاص بك في القائمة.</span><span class="sxs-lookup"><span data-stu-id="c339b-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="c339b-150">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c339b-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c339b-151">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c339b-151">Additional resources</span></span>

[<span data-ttu-id="c339b-152">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="c339b-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="c339b-153">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="c339b-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c339b-154">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="c339b-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="c339b-155">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="c339b-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c339b-156">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="c339b-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c339b-157">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="c339b-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="c339b-158">التحقق من إمكانية الوصول إلى محتوي الصفحة</span><span class="sxs-lookup"><span data-stu-id="c339b-158">Verify page content accessibility</span></span>](verify-accessibility.md)