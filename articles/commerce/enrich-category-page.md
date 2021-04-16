---
title: إثراء الصفحة المتنقل إليها‬ لفئة
description: يتناول هذا الموضوع تحسين صفحات الفئة في Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799001"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="c6da8-103">إثراء صفحة فئة منتقل إليها‬</span><span class="sxs-lookup"><span data-stu-id="c6da8-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6da8-104">يتناول هذا الموضوع تحسين صفحات الفئة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c6da8-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c6da8-105">يوفر Commerce ‏‫الصفحة المتنقل إليها‬ للفئة الافتراضية المستخدمة عند عرض بيانات الفئة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="c6da8-106">تحتوي صفحة الفئة الافتراضية على عناصر مطلوبة، مثل المصافي، ووضع المنتج المصنف، وخيارات الفرز، وملخص الاختيار، وأدوات ترقيم الصفحات.</span><span class="sxs-lookup"><span data-stu-id="c6da8-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="c6da8-107">ومع ذلك، بدلاً من استخدام صفحة الفئة الافتراضية، قد ترغب في استخدام الصفحة المتنقل إليها للفئة "التي تم تحسينها" والتي تحتوي على المزيد من المحتوى وعناصر أكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="c6da8-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="c6da8-108">قد يتضمن التحسين النموذجي إضافة محتوى تسويقي خاص بفئة إلى صفحة الفئة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="c6da8-109">قد يتضمن هذا المحتوي وضع المنتج عبر الفئة لأغراض البيع بين عملاء متعديين والقوائم التحريرية والصور ومقاطع الفيديو والنصوص الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c6da8-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="c6da8-110">يمكنك إما تعديل صفحة الفئة الافتراضية أو تحديد صفحة فئة مختلفة لفئة معينة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![الصفحة المتنقل إليها‬ للفئة المُحسنة](./media/CategoryLandingPages.png)

<span data-ttu-id="c6da8-112">في منشئ مواقع Commerce، تتضمن صفحة **المنتجات** قائمة بالفئات من القناة التي تم تعيينها للموقع.</span><span class="sxs-lookup"><span data-stu-id="c6da8-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="c6da8-113">في حال تحديد الحالة **مُحسن** لصفحه فئة، يتم تحسين صفحة الفئة هذه.</span><span class="sxs-lookup"><span data-stu-id="c6da8-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="c6da8-114">وإلا، يتم استخدام صفحة الفئة الافتراضية والمحتوى للفئة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="c6da8-115">يمكنك معاينة كل من صفحات الفئة التي تم تحسينها والذي لم يتم تحسينها للفئة من خلال تحديد اسم الفئة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="c6da8-116">لتحسين صفحه فئة، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="c6da8-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="c6da8-117">في صفحة **المنتجات** ، حدد اسم الفئة التي ترغب في تحسين صفحة الفئة لها.</span><span class="sxs-lookup"><span data-stu-id="c6da8-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="c6da8-118">يتم فتح صفحة الفئة الافتراضية للفئة المحددة في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="c6da8-119">قم بتحديد **تحسين صفحة الفئة**.</span><span class="sxs-lookup"><span data-stu-id="c6da8-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="c6da8-120">حدد قالبًا لصفحة الفئة التي تم تحسينها.</span><span class="sxs-lookup"><span data-stu-id="c6da8-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="c6da8-121">إذا كنت تقوم بإجراء تغييرات ثانوية فقط، فيمكنك تحديد صفحة الفئة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="c6da8-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="c6da8-122">وبدلاً من ذلك، يمكنك تحديد قالب صفحة فئة معين.</span><span class="sxs-lookup"><span data-stu-id="c6da8-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="c6da8-123">عند تحديد القالب، يتم فتح محرر الصفحة، ويتم استخدام القالب المحدد لإنشاء صفحة فئة جديدة للفئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="c6da8-124">تم سحب الصفحة لك، ويمكنك الآن اجراء التغييرات التي تريد إجراؤها.</span><span class="sxs-lookup"><span data-stu-id="c6da8-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="c6da8-125">تستخدم الوحدات النمطية التي تستخدم بيانات مواصفات الفئة البيانات من الفئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c6da8-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="c6da8-126">تحدد إعدادات القالب الذي تحدده التغييرات التي يمكنك اجراؤها.</span><span class="sxs-lookup"><span data-stu-id="c6da8-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6da8-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c6da8-127">Additional resources</span></span>

[<span data-ttu-id="c6da8-128">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="c6da8-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="c6da8-129">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="c6da8-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="c6da8-130">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="c6da8-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c6da8-131">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="c6da8-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="c6da8-132">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="c6da8-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c6da8-133">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="c6da8-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c6da8-134">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="c6da8-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="c6da8-135">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="c6da8-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
