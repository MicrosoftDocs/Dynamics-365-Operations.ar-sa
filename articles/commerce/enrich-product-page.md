---
title: إثراء صفحة منتج
description: يوضح هذا الموضوع كيفية تحسين صفحة منتج في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097328"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="96686-103">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="96686-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="96686-104">يوضح هذا الموضوع كيفية تحسين صفحة منتج في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="96686-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="96686-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="96686-105">Overview</span></span>

<span data-ttu-id="96686-106">بشكل افتراضي، يستخدم الموقع الخاص بك صفحة عامة لإظهار بيانات المنتج.</span><span class="sxs-lookup"><span data-stu-id="96686-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="96686-107">تتضمن هذه الصفحة المعلومات الأساسية حول المنتج وعناصر التحكم المطلوبة لبيعه.</span><span class="sxs-lookup"><span data-stu-id="96686-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="96686-108">ولكن يمكنك تكملة المعلومات القادمة من Commerce Scale Unit بصور أو نصوص إضافية لمنتج معين.</span><span class="sxs-lookup"><span data-stu-id="96686-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="96686-109">تُعرف هذه العملية بعملية تحسين صفحة المنتج.</span><span class="sxs-lookup"><span data-stu-id="96686-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="96686-110">في الكثير من الحالات، ستحتاج إلى استخدام محتوي إضافي محدد لمنتجاتك.</span><span class="sxs-lookup"><span data-stu-id="96686-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="96686-111">عند الانتقال إلى **البيع بالتحزئة والتجارة** في أداة التأليف، ستظهر قائمة بالمنتجات من القناة المعينة للموقع.</span><span class="sxs-lookup"><span data-stu-id="96686-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="96686-112">وفي هذه القائمة ، يشير العمود **مُحسن** إلى ما إذا كان قد تم تحسين صفحة المنتج لأحد المنتجات أم لا.</span><span class="sxs-lookup"><span data-stu-id="96686-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="96686-113">في حاله ظهور علامة اختيار في العمود، توجد صفحة منتج تم تحسينه للمنتج.</span><span class="sxs-lookup"><span data-stu-id="96686-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="96686-114">في حالة عدم ظهور علامة اختيار، يتم استخدام صفحة ومحتوي المنتج الافتراضيين للمنتج.</span><span class="sxs-lookup"><span data-stu-id="96686-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="96686-115">يمكنك معاينة كلاً من صفحات المنتج الذي تم تحسينه والذي لم يتم تحسينه من خلال تحديد اسم منتج في القائمة.</span><span class="sxs-lookup"><span data-stu-id="96686-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="96686-116">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="96686-116">Enrich a product page</span></span>

<span data-ttu-id="96686-117">لتحسين صفحة المنتج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="96686-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="96686-118">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="96686-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="96686-119">في جزء التنقل علي اليسار، حدد **المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="96686-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="96686-120">حدد أي منتج لا يحتوي علي صفحة منتج تم تحسينه.</span><span class="sxs-lookup"><span data-stu-id="96686-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="96686-121">في جزء الإجراءات، حدد **تحسين صفحة المنتج**.</span><span class="sxs-lookup"><span data-stu-id="96686-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="96686-122">حدد **قالب-PDP**، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="96686-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="96686-123">في شجره المخطط التفصيلي الخاصة بالصفحة الموجودة علي اليسار، قم بتوسيع الفتحة **الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="96686-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="96686-124">تحديد زر علامة الحذف(**...**) للفتحة **الرئيسية** ، ثم حدد **‏‫إضافة وحدة نمطية‬**.</span><span class="sxs-lookup"><span data-stu-id="96686-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="96686-125">حدد **الحاوية 2**، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="96686-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="96686-126">تحديد زر علامة الحذف لـ **الحاوية 2** ، ثم حدد **‏‫إضافة وحدة نمطية**‬.</span><span class="sxs-lookup"><span data-stu-id="96686-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="96686-127">حدد **ميزة**، ثم قم بتحديد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="96686-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="96686-128">في جزء الخصائص الموجود علي اليمين، في حقل **النص المنسق** ، ادخل الوصف المحدث للمنتج.</span><span class="sxs-lookup"><span data-stu-id="96686-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="96686-129">في حقل **العنوان** ، ادخل نص العنوان ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="96686-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="96686-130">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="96686-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="96686-131">في حقل **التعليقات** ، ادخل **تحسين منتج**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="96686-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="96686-132">حدد **معاينة** لمعاينة صفحة تحسين منتج.</span><span class="sxs-lookup"><span data-stu-id="96686-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="96686-133">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="96686-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="96686-134">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="96686-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96686-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="96686-135">Additional resources</span></span>

[<span data-ttu-id="96686-136">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="96686-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="96686-137">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="96686-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="96686-138">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="96686-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="96686-139">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="96686-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="96686-140">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="96686-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="96686-141">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="96686-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="96686-142">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="96686-142">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="96686-143">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="96686-143">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
