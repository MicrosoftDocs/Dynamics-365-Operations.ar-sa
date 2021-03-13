---
title: إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL
description: يوضح هذا الموضوع كيفية إعداد صفحة تجارة إلكترونية في Microsoft Dynamics 365 Commerce التي يمكنها خدمة المحتوى الديناميكي، استنادا إلى معلمات URL.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098609"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="5655d-103">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="5655d-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="5655d-104">يوضح هذا الموضوع كيفية إعداد صفحة تجارة إلكترونية في Microsoft Dynamics 365 Commerce التي يمكنها خدمة المحتوى الديناميكي، استنادا إلى معلمات URL.</span><span class="sxs-lookup"><span data-stu-id="5655d-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="5655d-105">يمكن تكوين صفحة التجارة الإلكترونية لخدمه محتوى مختلف، استنادا إلى شريحة في مسار URL.</span><span class="sxs-lookup"><span data-stu-id="5655d-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="5655d-106">لذلك، تعرف الصفحة كصفحة ديناميكية.</span><span class="sxs-lookup"><span data-stu-id="5655d-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="5655d-107">يتم استخدام الشريحة كمعلمة لاسترداد محتوى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5655d-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="5655d-108">على سبيل المثال، يتم إنشاء الصفحة مسماة **عارض\_المدونة** وربطها بعنوان URL `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="5655d-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="5655d-109">يمكن استخدام هذه الصفحة بعد ذلك لإظهار محتوى مختلف، استنادا إلى الشريحة الأخيرة في مسار URL.</span><span class="sxs-lookup"><span data-stu-id="5655d-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="5655d-110">على سبيل المثال، الشريحة الأخيرة في عنوان URL `https://fabrikam.com/blog/article-1` هي **article-1**.</span><span class="sxs-lookup"><span data-stu-id="5655d-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="5655d-111">يمكن أن تقترن الصفحات المخصصة المنفصلة التي تتجاوز الصفحة الديناميكية أيضًا بالشرائح الموجودة في مسار URL.</span><span class="sxs-lookup"><span data-stu-id="5655d-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="5655d-112">على سبيل المثال، يتم إنشاء الصفحة مسماة **ملخص\_المدونة** وربطها بعنوان URL `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="5655d-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="5655d-113">عند طلب عنوان URL هذا، يتم إرجاح صفحة **ملخص\_المدونة** المقترنة بمعملة **/about-this-blog** بدلا من صفحة **عارض\_المدونة**.</span><span class="sxs-lookup"><span data-stu-id="5655d-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="5655d-114">يتم تنفيذ وظيفة استضافة محتوى الصفحة الديناميكية واسترداده وإظهاره باستخدام وحدة نمطية مخصصة.</span><span class="sxs-lookup"><span data-stu-id="5655d-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="5655d-115">لمزيد من المعلومات، راجع [قابلية توسعة القناة عبر الإنترنت](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5655d-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="5655d-116">إعداد صفحة تجارة إلكترونية ديناميكية</span><span class="sxs-lookup"><span data-stu-id="5655d-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="5655d-117">لإعداد صفحة تجارة إلكترونية ديناميكية، يجب إنشاء الصفحة الديناميكية وإنشاء عنوان URL الأساسي وتكوين المسار إلى الصفحة الديناميكية.</span><span class="sxs-lookup"><span data-stu-id="5655d-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="5655d-118">إنشاء الصفحة التي ستخدم المحتوى الديناميكي</span><span class="sxs-lookup"><span data-stu-id="5655d-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="5655d-119">لإنشاء صفحة تقوم بخدمة المحتوى الديناميكي، اتبع الخطوات الموجودة في [إضافة صفحة موقع جديدة](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="5655d-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="5655d-120">ستتطلب الصفحة التي تقوم بإنشائها تنفيذ وحدة نمطية تستخدم الشريحة الأخيرة في مسار URL لاسترداد المحتوى من مصدر بيانات خارجي.</span><span class="sxs-lookup"><span data-stu-id="5655d-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="5655d-121">للحصول على مزيد من المعلومات حول تطوير الوحدة النمطية المخصصة، راجع [‏‫قابلية توسعة القناة عبر الإنترنت](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5655d-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="5655d-122">إنشاء URL أساسي للصفحة الديناميكية</span><span class="sxs-lookup"><span data-stu-id="5655d-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="5655d-123">لإنشاء عنوان URL أساسي للصفحة الديناميكية في منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5655d-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5655d-124">انتقل إلى **عناوين URL**، ثم حدد **جديد \> عنوان URL جديد**.</span><span class="sxs-lookup"><span data-stu-id="5655d-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="5655d-125">في مربع الحوار **إنشاء URL جديد**، حدد **صفحة داخلية**.</span><span class="sxs-lookup"><span data-stu-id="5655d-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="5655d-126">ضمن **مسار عنوان URL**، أدخل المسار الذي سيقوم بدور جذر الصفحة الديناميكية (في هذا المثال، **/المدونة**).</span><span class="sxs-lookup"><span data-stu-id="5655d-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="5655d-127">بعد ذلك حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5655d-127">Then select **Next**.</span></span>
1. <span data-ttu-id="5655d-128">في مربع الحوار **حدد الصفحة**، حدد صفحة التي قمت بإنشائها للقيام بدور الصفحة الديناميكية، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5655d-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="5655d-129">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="5655d-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="5655d-130">تكوين المسار للصفحة الديناميكية</span><span class="sxs-lookup"><span data-stu-id="5655d-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="5655d-131">لتكوين المسار إلى الصفحة الديناميكية في منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5655d-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5655d-132">انتقل إلى **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="5655d-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="5655d-133">ضمن **مسارات URL ذات معلمات**، حدد **إضافة**، ثم أدخل مسار URL الذي قمت بإدخاله عند إنشاء عنوان URL (في هذا المثال ، **/المدونة**).</span><span class="sxs-lookup"><span data-stu-id="5655d-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="5655d-134">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="5655d-134">Select **Save and publish**.</span></span>

<span data-ttu-id="5655d-135">بعد تكوين المسار، تقوم كافة طلبات مسار URL ذي المعلمات بإرجاع الصفحة المقترنة بعنوان URL هذا.</span><span class="sxs-lookup"><span data-stu-id="5655d-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="5655d-136">إذا احتوت أية طلبات على شريحة إضافية، سيتم إرجاع الصفحة المقترنة، وسيتم استرداد محتوى الصفحة باستخدام الشريحة كمعلمة.</span><span class="sxs-lookup"><span data-stu-id="5655d-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="5655d-137">علي سبيل المثال، سيقوم `https://fabrikam.com/blog/article-1` بإرجاع صفحة **ملخص\_المدونة**، سيتم استرداد محتوى الصفحة باستخدام المعلمة **المدونة**.</span><span class="sxs-lookup"><span data-stu-id="5655d-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="5655d-138">تجاوز محدد عناوين URL ذات معلمات بصفحة مخصصة</span><span class="sxs-lookup"><span data-stu-id="5655d-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="5655d-139">لتجاوز عنوان URL ذي معلمات بصفحة مخصصة في منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5655d-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5655d-140">انتقل إلى **عناوين URL**، ثم حدد **جديد \> عنوان URL جديد**.</span><span class="sxs-lookup"><span data-stu-id="5655d-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="5655d-141">في مربع الحوار **إنشاء URL جديد**، حدد **صفحة داخلية**.</span><span class="sxs-lookup"><span data-stu-id="5655d-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="5655d-142">ضمن **مسار URL**، أدخل المسار الذي يتضمن الشريحة إلى التجاوز (في هذا المثال، **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="5655d-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="5655d-143">بعد ذلك حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5655d-143">Then select **Next**.</span></span>
1. <span data-ttu-id="5655d-144">في مربع الحوار **تحديد صفحة**، حدد الصفحة المخصصة، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5655d-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="5655d-145">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="5655d-145">Select **Publish**.</span></span>
1. <span data-ttu-id="5655d-146">إذا لم يتم نشر الصفحة المخصصة بعد، انتقل إلى **الصفحات**، وحدد الصفحة المخصصة، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="5655d-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="5655d-147">بعد نشر الصفحة المخصصة، سيتم تقديمها بدلا من الصفحة الديناميكية التي تحتوي على محتوى ذي معلمات.</span><span class="sxs-lookup"><span data-stu-id="5655d-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5655d-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5655d-148">Additional resources</span></span>

[<span data-ttu-id="5655d-149">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="5655d-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="5655d-150">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="5655d-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5655d-151">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="5655d-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="5655d-152">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="5655d-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="5655d-153">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="5655d-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="5655d-154">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="5655d-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="5655d-155">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="5655d-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="5655d-156">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="5655d-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="5655d-157">قابلية توسعة القناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5655d-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
