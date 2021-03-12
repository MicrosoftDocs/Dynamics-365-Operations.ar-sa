---
title: اعتبارات تحسين محرك البحث (SEO) لموقعك
description: يغطي هذا الموضوع اعتبارات تحسين محرك البحث (SEO) للموقع الخاص بك من التطوير إلى الإنتاج.
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 639d6fa74954b5f74560c7e51523ab2b4d2b7f62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989342"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="a4f03-103">اعتبارات تحسين محرك البحث (SEO) لموقعك</span><span class="sxs-lookup"><span data-stu-id="a4f03-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a4f03-104">يغطي هذا الموضوع اعتبارات تحسين محرك البحث (SEO) للموقع الخاص بك من التطوير إلى الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a4f03-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="a4f03-105">موقع تحت التطوير</span><span class="sxs-lookup"><span data-stu-id="a4f03-105">A site that is under development</span></span>

<span data-ttu-id="a4f03-106">بينما يكون الموقع تحت التطوير، يجب أن تحتوي كافة الصفحات على علامات التعريف **NOINDEX** و **NOFOLLOW**، بحيث لا تقوم محركات البحث بفهرسة الصفحات وتخزين إصدارات تطوير الموقع الخاص بك في ذاكرة التخزين المؤقت الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="a4f03-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="a4f03-107">للقيام بهذا التكوين، يجب عليك إضافة الوحدة النمطية الافتراضية لعلامات التعريف إلى قالب صفحة الموقع.</span><span class="sxs-lookup"><span data-stu-id="a4f03-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="a4f03-108">ستتوفر خصائص علامات التعريف الافتراضية في قسم خصائص SEO في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a4f03-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="a4f03-109">يمكنك استخدام هذه الخصائص لإدارة علامات التعريف.</span><span class="sxs-lookup"><span data-stu-id="a4f03-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="a4f03-110">التشغيل التجريبي لموقع</span><span class="sxs-lookup"><span data-stu-id="a4f03-110">Soft launch of a site</span></span>

<span data-ttu-id="a4f03-111">أثناء "التشغيل التجريبي"، يقتصر توافر موقع ويب على جمهور أو سوق قبل الإصدار الكامل.</span><span class="sxs-lookup"><span data-stu-id="a4f03-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="a4f03-112">إذا قمت بالتشغيل التجريبي لموقع الويب الخاص بك، فإنه يجب عليك ترك علامات التعريف **NOINDEX** من مكانها.</span><span class="sxs-lookup"><span data-stu-id="a4f03-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="a4f03-113">وبهذه الطريقة، فإنك تساعد على ضمان اقتصار التشغيل التجريبي على جمهور محدد تود أن يصل إلى الموقع.</span><span class="sxs-lookup"><span data-stu-id="a4f03-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="a4f03-114">موقع قيد الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a4f03-114">A site that is in production</span></span>

<span data-ttu-id="a4f03-115">عندما يكون موقع قيد الإنتاج، يجب عليك التأكد من وضع علامات على كافة صفحات الموقع بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="a4f03-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="a4f03-116">تستخدم Microsoft Dynamics 365 Commerce المعلومات التي يتم إدخالها لصفحة لإظهار كافة معلومات SEO في تلك الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a4f03-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="a4f03-117">توفر الوحدات النمطية التالية هذه الوظيفة: ملخص صفحة الفئة وملخص صفحة القائمة وملخص صفحة المنتج.</span><span class="sxs-lookup"><span data-stu-id="a4f03-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="a4f03-118">لتحسين فهرسه محرك البحث، يستخدم إطار العمل الظاهر كلاً من المعومات وخصائص SEO التي تم تكوينها في Dynamics 365 Commerce والمعلومات الخاصة بالوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="a4f03-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="a4f03-119">بالنسبة للموقع الموجود في الإنتاج، يجب التأكد من أن الملف robots.txt يسمح بفهرسة موقعك بالكامل، وإنه يحتوي على ارتباطات إلى مستند خريطة الموقع المنشور الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="a4f03-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="a4f03-120">يجب عليك تشغيل وظيفة إنشاء خريطة الموقع عند **إعدادات الموقع \> خريطة الموقع ممكنة**.</span><span class="sxs-lookup"><span data-stu-id="a4f03-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="a4f03-121">إعدادات SEO الخاصة بالصفحة للمعاينة الداخلية وشرائح الجمهور المحدودة وكافة شرائح الجمهور.</span><span class="sxs-lookup"><span data-stu-id="a4f03-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="a4f03-122">لأن Dynamics 365 Commerce يدعم المعاينات المصادقة "ما تشاهده هو ما تحصل عليه"(WYSIWYG) في أداة إنشاء الصفحات المرئية، يستطيع المؤلفون إعداد محتوى الصفحة دون القلق عن المعلومات التي ستصبح مرئية إلى زائري الموقع.</span><span class="sxs-lookup"><span data-stu-id="a4f03-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="a4f03-123">إذا كان يجب نشر الصفحة، ولكن يجب أن يكون العرض الخاص بها محدودًا، فإنها يجب أن تحتوي على علامة تعريف **NOINDEX**، بحيث لن تتم فهرستها بواسطة محركات البحث.</span><span class="sxs-lookup"><span data-stu-id="a4f03-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="a4f03-124">وبعد ذلك، عندما تكون الصفحة جاهزة لكافة شرائح الجمهور المستهدفة، يجب أن تكون كافة بيانات تعريف SEO الأساسية موجودة، لزيادة فعالية فهرسة محرك البحث.</span><span class="sxs-lookup"><span data-stu-id="a4f03-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="a4f03-125">بالإضافة إلى ذلك، يجب إزالة علامة التعريف **NOLIMIT**.</span><span class="sxs-lookup"><span data-stu-id="a4f03-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4f03-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a4f03-126">Additional resources</span></span>

[<span data-ttu-id="a4f03-127">إدارة المستخدمين والأدوار في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a4f03-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="a4f03-128">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="a4f03-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="a4f03-129">إدارة سياسة أمان المحتوى (CSP)</span><span class="sxs-lookup"><span data-stu-id="a4f03-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
