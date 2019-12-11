---
title: إثراء الصفحة المتنقل إليها‬ لفئة
description: يتناول هذا الموضوع تحسين صفحات الفئة في Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8d735b215132b90ca786d6967589496bee73f4d9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697579"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="2e784-103">إثراء الصفحة المتنقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="2e784-103">Enrich a category landing page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2e784-104">يتناول هذا الموضوع تحسين صفحات الفئة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e784-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e784-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2e784-105">Overview</span></span>

<span data-ttu-id="2e784-106">يوفر Commerce ‏‫الصفحة المتنقل إليها‬ للفئة الافتراضية المستخدمة عند عرض بيانات الفئة.</span><span class="sxs-lookup"><span data-stu-id="2e784-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="2e784-107">تحتوي صفحة الفئة الافتراضية على عناصر مطلوبة، مثل المصافي، ووضع المنتج المصنف، وخيارات الفرز، وملخص الاختيار، وأدوات ترقيم الصفحات.</span><span class="sxs-lookup"><span data-stu-id="2e784-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="2e784-108">ومع ذلك، بدلاً من استخدام صفحة الفئة الافتراضية، قد ترغب في استخدام الصفحة المتنقل إليها للفئة "التي تم تحسينها" والتي تحتوي على المزيد من المحتوى وعناصر أكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="2e784-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="2e784-109">قد يتضمن التحسين النموذجي إضافة محتوى تسويقي خاص بفئة إلى صفحة الفئة.</span><span class="sxs-lookup"><span data-stu-id="2e784-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="2e784-110">قد يتضمن هذا المحتوي وضع المنتج عبر الفئة لأغراض البيع بين عملاء متعديين والقوائم التحريرية والصور ومقاطع الفيديو والنصوص الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2e784-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="2e784-111">يمكنك إما تعديل صفحة الفئة الافتراضية أو تحديد صفحة فئة مختلفة لفئة معينة.</span><span class="sxs-lookup"><span data-stu-id="2e784-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![الصفحة المتنقل إليها‬ للفئة المُحسنة](./media/CategoryLandingPages.png)

<span data-ttu-id="2e784-113">في أداة التأليف، تتضمن صفحة **المنتج** قائمة بالفئات من القناة التي تم تعيينها للموقع.</span><span class="sxs-lookup"><span data-stu-id="2e784-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="2e784-114">في حال تحديد الحالة **مُحسن** لصفحه فئة، يتم تحسين صفحة الفئة هذه.</span><span class="sxs-lookup"><span data-stu-id="2e784-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="2e784-115">وإلا، يتم استخدام صفحة الفئة الافتراضية والمحتوى للفئة.</span><span class="sxs-lookup"><span data-stu-id="2e784-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="2e784-116">يمكنك معاينة كل من صفحات الفئة التي تم تحسينها والذي لم يتم تحسينها للفئة من خلال تحديد اسم الفئة.</span><span class="sxs-lookup"><span data-stu-id="2e784-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="2e784-117">لتحسين صفحه فئة، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="2e784-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="2e784-118">في صفحة **المنتجات** ، حدد اسم الفئة التي ترغب في تحسين صفحه الفئة لها.</span><span class="sxs-lookup"><span data-stu-id="2e784-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="2e784-119">يتم فتح صفحة الفئة الافتراضية للفئة المحددة في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2e784-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="2e784-120">قم بتحديد **تحسين صفحة الفئة**.</span><span class="sxs-lookup"><span data-stu-id="2e784-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="2e784-121">حدد قالبًا لصفحة الفئة التي تم تحسينها.</span><span class="sxs-lookup"><span data-stu-id="2e784-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="2e784-122">إذا كنت تقوم بإجراء تغييرات ثانوية فقط، فيمكنك تحديد صفحة الفئة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="2e784-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="2e784-123">وبدلاً من ذلك، يمكنك تحديد قالب صفحة فئة معين.</span><span class="sxs-lookup"><span data-stu-id="2e784-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="2e784-124">عند تحديد القالب، يتم فتح محرر الصفحة، ويتم استخدام القالب المحدد لإنشاء صفحة فئة جديدة للفئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="2e784-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="2e784-125">تم سحب الصفحة لك، ويمكنك الآن اجراء التغييرات التي تريد إجراؤها.</span><span class="sxs-lookup"><span data-stu-id="2e784-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="2e784-126">تستخدم الوحدات النمطية التي تستخدم بيانات مواصفات الفئة البيانات من الفئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="2e784-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="2e784-127">تحدد إعدادات القالب الذي تحدده التغييرات التي يمكنك اجراؤها.</span><span class="sxs-lookup"><span data-stu-id="2e784-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e784-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2e784-128">Additional resources</span></span>

[<span data-ttu-id="2e784-129">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="2e784-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2e784-130">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="2e784-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2e784-131">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="2e784-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2e784-132">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="2e784-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2e784-133">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="2e784-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2e784-134">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="2e784-134">Enrich a product page</span></span>](enrich-product-page.md)
