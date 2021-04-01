---
title: إنشاء عنوان URL لصفحة
description: يتناول هذا الموضوع المفاهيم والإجراءات الأساسية لإنشاء عنوان URL للصفحة علي الموقع الخاص بك.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e221bd975fd984379724b751f6c026acfda7b07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207885"
---
# <a name="create-a-page-url"></a><span data-ttu-id="5bda1-103">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="5bda1-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5bda1-104">يتناول هذا الموضوع المفاهيم والإجراءات الأساسية لإنشاء عنوان URL للصفحة علي الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5bda1-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="5bda1-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5bda1-105">Overview</span></span>

<span data-ttu-id="5bda1-106">يتكون عنوان URL الكامل أو المطلق الذي يشير إلى الصفحة علي الموقع الخاص بك من أجزاء مختلفة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="5bda1-107">علي سبيل المثال، يحتوي عنوان URL `https://www.contoso.com/en-us/contactus` من الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="5bda1-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="5bda1-108">`https://www.contoso.com` – بروتوكول HTTP ومجال الموقع.</span><span class="sxs-lookup"><span data-stu-id="5bda1-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="5bda1-109">`/en-us` - مسار لغة الموقع.</span><span class="sxs-lookup"><span data-stu-id="5bda1-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="5bda1-110">`/contactus` – عنوان URL المرتبط لصفحة **اتصل بنا** .</span><span class="sxs-lookup"><span data-stu-id="5bda1-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="5bda1-111">ويعرف عنوان URL المرتبط أيضا بعنوان URL لـ *حقل احتياط البريد الإلكتروني*.</span><span class="sxs-lookup"><span data-stu-id="5bda1-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="5bda1-112">قم بإنشاء المجال الخاص بموقعك ومسار اللغة الاختيارية عند إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="5bda1-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="5bda1-113">يمكنك إضافة المزيد من المجالات ومسارات اللغة إلى موقعك من خلال صفحة المتاجر عبر الإنترنت في إعدادات الموقع.</span><span class="sxs-lookup"><span data-stu-id="5bda1-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="5bda1-114">يوجد الحقل الاحتياطي للبريد الإلكتروني لعنوان URL لصفحة ككيان مستقل في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="5bda1-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="5bda1-115">يتكون عنوان URL للصفحة من جزئين: اسم يمثل الحقل الاحتياطي للبريد الإلكتروني لعنوان URL، ومؤشر إلى الصفحة في موقعك أو موقع خارجي.</span><span class="sxs-lookup"><span data-stu-id="5bda1-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="5bda1-116">يمكن أيضًا تكوين عنوان URL للصفحة ليكون بمثابة إعادة توجيه إلى صفحة أخرى إما على موقعك أو في موقع خارجي.</span><span class="sxs-lookup"><span data-stu-id="5bda1-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="5bda1-117">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="5bda1-117">Create a page URL</span></span>

<span data-ttu-id="5bda1-118">هناك طريقتان لإنشاء عناوين URL للصفحة:</span><span class="sxs-lookup"><span data-stu-id="5bda1-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="5bda1-119">تلقائيًا، عند إنشائك للصفحة</span><span class="sxs-lookup"><span data-stu-id="5bda1-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="5bda1-120">يدويًا، من صفحة **عناوين URL**</span><span class="sxs-lookup"><span data-stu-id="5bda1-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="5bda1-121">إنشاء عنوان URL للصفحة عند إنشاء الصفحة</span><span class="sxs-lookup"><span data-stu-id="5bda1-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="5bda1-122">إذا قمت بتوفير اسم في حقل **URL** عند إنشاء صفحة جديدة، يتم إنشاء URL الصفحة الذي يشير إلى هذه الصفحة تلقائيًا في صفحة **عناوين URL** .</span><span class="sxs-lookup"><span data-stu-id="5bda1-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="5bda1-123">بعد نشر عنوان URL والصفحة التي يشير إليها، يمكن لمستخدمي الموقع (عملائك) الوصول إلى الصفحة المرتبطة بعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="5bda1-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="5bda1-124">إذا قمت بنشر عنوان URL دون نشر الصفحة التي يشير إليها، فسيتلقى مستخدمو الموقع خطأ 404 عندما يحاولون الوصول إلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="5bda1-125">إذا قمت بنشر صفحة دون نشر عنوان URL الذي يشير إليها، فلن يمكن الوصول إلى الصفحة باستخدام عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="5bda1-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="5bda1-126">إنشاء عنوان URL للصفحة يدويًا</span><span class="sxs-lookup"><span data-stu-id="5bda1-126">Manually create a page URL</span></span>

<span data-ttu-id="5bda1-127">عند إنشاء صفحات جديدة، فأنت لست مطالبًا بتحديد عنوان URL للصفحة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="5bda1-128">إذا تركت حقل عنوان URL فارغًا، فسوف يتم إنشاء الصفحة في حالة غير مرتبط.</span><span class="sxs-lookup"><span data-stu-id="5bda1-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="5bda1-129">في هذه الحالة، لن يتمكن العملاء من الوصول إلى الصفحة، حتى لو تم نشرها.</span><span class="sxs-lookup"><span data-stu-id="5bda1-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="5bda1-130">لجعل الصفحة قابلة للوصول، يجب عليك إنشاء عنوان URL يدويًا وربطه بالصفحة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="5bda1-131">لإنشاء عنوان URL للصفحة يدويًا لصفحة معينة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5bda1-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="5bda1-132">في صفحة **عناوين URL‬** ، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5bda1-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="5bda1-133">حدد صفحة الموقع لربطها بعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="5bda1-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="5bda1-134">قم بإدخال الحقل الاحتياطي للبريد الإلكتروني لعنوان URL، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5bda1-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="5bda1-135">وفي هذه المرحلة، يكون عنوان URL في الحالة مسودة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="5bda1-136">ويجب نشرها قبل أن يتمكن مستخدمو الموقع من الوصول إلى الصفحة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="5bda1-137">تحديث عنوان URL للصفحة</span><span class="sxs-lookup"><span data-stu-id="5bda1-137">Update a page URL</span></span>

<span data-ttu-id="5bda1-138">لتحديث الصفحة الهدف لعنوان URL للصفحة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5bda1-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="5bda1-139">في الصفحة **عناوين URL** ، حدد عنوان URL المطلوب تحديثه.</span><span class="sxs-lookup"><span data-stu-id="5bda1-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="5bda1-140">في جزء الخصائص على اليمين، حدد زر علامة الحذف (**...**) بجانب حقل الصفحة الهدف.</span><span class="sxs-lookup"><span data-stu-id="5bda1-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="5bda1-141">في مربع الحوار، حدد صفحة مختلفة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5bda1-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="5bda1-142">احفظ عنوان URL وقم بنشره.</span><span class="sxs-lookup"><span data-stu-id="5bda1-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="5bda1-143">إعادة توجيه عنوان URL للصفحة</span><span class="sxs-lookup"><span data-stu-id="5bda1-143">Redirect a page URL</span></span>

<span data-ttu-id="5bda1-144">في بعض الأحيان، قد ترغب في أن يعرض عملائك صفحة مختلفة عندما يطلبون عنوان URL محددًا.</span><span class="sxs-lookup"><span data-stu-id="5bda1-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="5bda1-145">وفي هذه الحالات، يكون الأسلوب الأفضل والأسهل في كثير من الأحيان هو تغيير الصفحة التي يشير إليها عنوان URL للصفحة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="5bda1-146">ومع ذلك، قد يكون لديك أسباب مشروعة لاستخدام عمليات إعادة التوجيه HTTP 301 أو 3023 لإعادة توجيه طلبات عنوان URL إلى عنوان URL مختلف.</span><span class="sxs-lookup"><span data-stu-id="5bda1-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="5bda1-147">لإعادة توجيه عنوان URL إلى عنوان URL مختلف، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5bda1-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="5bda1-148">في الصفحة **عناوين URL** ، حدد عنوان URL المطلوب تحديثه.</span><span class="sxs-lookup"><span data-stu-id="5bda1-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="5bda1-149">في جزء الخصائص على اليمين، حدد **إعادة توجيه**.</span><span class="sxs-lookup"><span data-stu-id="5bda1-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="5bda1-150">حدد وجهة لإعادة التوجيه:</span><span class="sxs-lookup"><span data-stu-id="5bda1-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="5bda1-151">للإشارة إلى صفحة أخرى على موقعك، حدد **عنوان URL داخلي** ، وحدد زر علامة الحذف (**...**)، ثم حدد عنوان URL المراد إعادة التوجيه إليه.</span><span class="sxs-lookup"><span data-stu-id="5bda1-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="5bda1-152">للإشارة إلى صفحة على موقع خارجي، حدد **عنوان URL الخارجي**، ثم أدخل عنوان URL الكامل لتلك الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5bda1-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="5bda1-153">تأكد من تضمين البروتوكول.</span><span class="sxs-lookup"><span data-stu-id="5bda1-153">Be sure to include the protocol.</span></span> <span data-ttu-id="5bda1-154">على سبيل المثال، أدخل `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="5bda1-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="5bda1-155">إذا كان عنوان URL يعيد التوجيه بالفعل إلى عنوان URL داخلي، فيجب تحديد **مسح التحديد** قبل أن تتمكن من إدخال عنوان URL خارجي.</span><span class="sxs-lookup"><span data-stu-id="5bda1-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="5bda1-156">حدد نوع إعادة التوجيه:</span><span class="sxs-lookup"><span data-stu-id="5bda1-156">Select a redirect type:</span></span>

    - <span data-ttu-id="5bda1-157">**إعادة توجيه دائم (301)** – حدد هذا الخيار عندما تعلم أن المحتوى الخاص بك يتحرك بشكل دائم ولن يعود إلى عنوان URL السابق.</span><span class="sxs-lookup"><span data-stu-id="5bda1-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="5bda1-158">تقوم محركات البحث بتعيين قيمة تحسين محرك البحث (SEO) لعنوان URL الخاص بإعادة التوجيه إلى عنوان URL الذي تتم إعادة توجيهه وتحديث سجله لإظهار عنوان URL الجديد.</span><span class="sxs-lookup"><span data-stu-id="5bda1-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="5bda1-159">**إعادة التوجيه المؤقت (302)** – حدد هذا الخيار لإعادة توجيه حركة المرور دون تحديث محركات البحث.</span><span class="sxs-lookup"><span data-stu-id="5bda1-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="5bda1-160">عادةً ما يتم استخدام هذا الأسلوب إذا كان المحتوى سيعود قريبًا إلى عنوان URL السابق الخاص به.</span><span class="sxs-lookup"><span data-stu-id="5bda1-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="5bda1-161">عندما تكون جاهزًا لتنفيذ إعادة التوجيه، قم بحفظ عنوان URL ونشره.</span><span class="sxs-lookup"><span data-stu-id="5bda1-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bda1-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5bda1-162">Additional resources</span></span>

[<span data-ttu-id="5bda1-163">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="5bda1-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="5bda1-164">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="5bda1-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5bda1-165">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="5bda1-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5bda1-166">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="5bda1-166">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]