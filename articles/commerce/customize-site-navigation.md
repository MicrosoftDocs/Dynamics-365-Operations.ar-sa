---
title: تخصيص التنقل في الموقع
description: يوضح هذا الموضوع كيفية إنشاء تسلسل هرمي مخصص للتنقل عبر الإنترنت لتنظيم منتجاتك لاستعراض موقع Microsoft Dynamics 365 Commerce الخاص بك.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914900"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="c7f07-103">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="c7f07-103">Customize site navigation</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c7f07-104">يوضح هذا الموضوع كيفية إنشاء تسلسل هرمي مخصص للتنقل عبر الإنترنت لتنظيم منتجاتك لاستعراض موقع Microsoft Dynamics 365 Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c7f07-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="c7f07-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c7f07-105">Overview</span></span>

<span data-ttu-id="c7f07-106">تتيح واجهات المتاجر على الإنترنت للعملاء اكتشاف المنتجات وتصفحها من خلال التنقل بين فئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="c7f07-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="c7f07-107">وعادةً ما يتم توفير هذه الإمكانية بواسطة علامات التبويب في أعلي الصفحة أو بواسطة شريط تنقل علي اليسار.</span><span class="sxs-lookup"><span data-stu-id="c7f07-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="c7f07-108">في Dynamics 365 Commerce، يمكنك إنشاء وإدارة البنية الهرمية الخاصة بالتنقل بين الفئات والمنتجات المضمنة في الفئات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="c7f07-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-retail-channel-navigation-hierarchy"></a><span data-ttu-id="c7f07-109">إنشاء تدرج هرمي للتنقل في قناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c7f07-109">Create a retail channel navigation hierarchy</span></span>

<span data-ttu-id="c7f07-110">لإنشاء تدرج هرمي للتنقل في قناه البيع بالتجزئة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7f07-110">To create a retail channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c7f07-111">انتقل إلى منتجات **Retail \> المنتجات والفئات \> إدارة الفئة والمنتج**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-111">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="c7f07-112">حدد **‏‫التدرجات الهرمية للفئات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="c7f07-113">اسم التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="c7f07-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7f07-114">وتعد الفئة العليا التي تقوم بإنشاءها هي عقدة فئة الجذر.</span><span class="sxs-lookup"><span data-stu-id="c7f07-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="c7f07-115">لن يتم إظهارها علي الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c7f07-115">It won't be shown on your site.</span></span> <span data-ttu-id="c7f07-116">لإنشاء تدرج هرمي للفئات حيث يتم عرض عقدة عُليا مفردة في موقعك، قم بإنشاء الفئة وتسميتها كتابع لفئة الجذر.</span><span class="sxs-lookup"><span data-stu-id="c7f07-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="c7f07-117">حدد **عقدة فئة جديدة**، ثم قم بتسمية الفئة.</span><span class="sxs-lookup"><span data-stu-id="c7f07-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="c7f07-118">تابع في إنشاء الفئات المشابهة والتابعة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="c7f07-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="c7f07-119">يمكنك الآن تعيين المنتجات لكل فئة قمت بإنشاءها ضمن فئة المستوي العلوي.</span><span class="sxs-lookup"><span data-stu-id="c7f07-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="c7f07-120">تخصيص ترتيب الفئات</span><span class="sxs-lookup"><span data-stu-id="c7f07-120">Customize the order of categories</span></span>

<span data-ttu-id="c7f07-121">بشكل افتراضي، سوف تظهر الفئات التي تقوم بتعريفها بترتيب أبجدي علي الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c7f07-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="c7f07-122">ومع ذلك، يمكنك أيضًا تخصيص ترتيب عرض الفئات.</span><span class="sxs-lookup"><span data-stu-id="c7f07-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="c7f07-123">تعيين نوع تدرج فئات هرمي</span><span class="sxs-lookup"><span data-stu-id="c7f07-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="c7f07-124">انتقل إلى منتجات **Retail \> المنتجات والفئات \> إدارة الفئة والمنتج**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-124">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="c7f07-125">حدد **التدرجات الهرمية للفئات**</span><span class="sxs-lookup"><span data-stu-id="c7f07-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="c7f07-126">في جزء الإجراءات، في علامة تبويب **التدرج الهرمي للفئات** ، في مجموعة **الإعداد‬** ، حدد **إقران نوع التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="c7f07-127">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-127">Select **New**.</span></span>
1. <span data-ttu-id="c7f07-128">في الحقل **إقران نوع التدرج الهرمي** ، حدد **تدرج هرمي للتنقل في قناة Retail**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-128">In the **Category hierarchy type** field, select **Retail channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="c7f07-129">في الحقل **التدرج الهرمي للفئات** ، حدد التدرج الهرمي للتنقل في القناة‬ الذي قمت بإنشاءه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="c7f07-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="c7f07-130">نشر ‏‫التدرجات الهرمية للتنقل الجديدة أو المحدثة</span><span class="sxs-lookup"><span data-stu-id="c7f07-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="c7f07-131">لجعل التدرج الهرمي للتنقل الخاص بك متاحًا لواجهة المتجر عبر الإنترنت الخاص بك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7f07-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="c7f07-132">انتقل إلي **Retail \> إعداد القناة \> فئات القنوات وسمات المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-132">Go to **Retail \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="c7f07-133">في الشجرة الموجودة علي اليسار، حدد المتجر الخاص بك علي الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="c7f07-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="c7f07-134">حدد **تحديثات نشر القناة**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="c7f07-135">انتقل إلى **Retail \> تكنولوجيا معلومات البيع بالتجزئة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-135">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="c7f07-136">في القائمة، ابحث وحدد **المهمة 1040**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="c7f07-137">حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="c7f07-137">Select **Run now**.</span></span>
1. <span data-ttu-id="c7f07-138">كرر الخطوتين 5 و 6 للمهام 1070 و 1150.</span><span class="sxs-lookup"><span data-stu-id="c7f07-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="c7f07-139">إظهار الفئات علي الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="c7f07-139">Show categories on your site</span></span>

<span data-ttu-id="c7f07-140">لإظهار التدرج الهرمي للفئات علي واجهة المتجر الخاص بك عبر الإنترنت، يجب عليك إضافة وحدة قائمة التنقل في الموقع المناسب في قالب أو جزء.</span><span class="sxs-lookup"><span data-stu-id="c7f07-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="c7f07-141">ثم تظهر الوحدة النمطية لقائمة التنقل التدرج الهرمي للتنقل، بشرط أن تكون قد قمت بنشر التدرج الهرمي للتنقل في البيع بالتجزئة إلى القناة التي يرتبط بها الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c7f07-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your retail navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="c7f07-142">تتيح الوحدة النمطية لقائمة التنقل المضمنة في مخزن أدوات البداية في المتجر للمستخدمين التنقل فقط إلى الفئات التي ليس لها فئات فرعية.</span><span class="sxs-lookup"><span data-stu-id="c7f07-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="c7f07-143">إذا كان بإمكان عملائك الانتقال إلى الفئات التي تحتوي على فئات فرعي ، فيجب عليك تخصيص الوحدة النمطية لقائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="c7f07-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="c7f07-144">إضافة خيارات التنقل المخصصة</span><span class="sxs-lookup"><span data-stu-id="c7f07-144">Add custom navigation options</span></span>

<span data-ttu-id="c7f07-145">في قائمة التنقل، يمكنك إضافة خيارات التنقل التي لا تشكل جزءًا من التدرج الهرمي لفئة المنتج الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c7f07-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="c7f07-146">علي سبيل المثال، في نهاية قائمة فئات المنتجات، يمكنك إضافة عنصر **اتصل بنا** الذي يُشير إلى صفحة اتصال قمت بإنشائها لموقعك.</span><span class="sxs-lookup"><span data-stu-id="c7f07-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="c7f07-147">لإضافة خيارات التنقل المخصصة إلى قائمة التنقل الخاصة بك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c7f07-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="c7f07-148">في القالب أو الجزء الذي تريد تخصيصه، حدد وحدة قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="c7f07-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="c7f07-149">في جزء الخصائص، ضمن علامة التبويب **بيانات** ، حدد **إضافة عنصر** لإنشاء عنصر تنقل جديد لنظام إدارة المحتوي (CMS).</span><span class="sxs-lookup"><span data-stu-id="c7f07-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="c7f07-150">ادخل نص ارتباط وعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="c7f07-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="c7f07-151">كرر الخطوتين 2 و 3 لإضافة مزيد من خيارات التنقل المخصصة.</span><span class="sxs-lookup"><span data-stu-id="c7f07-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="c7f07-152">وعند الانتهاء، احفظ القالب أو الجزء وقم بإيداعه.</span><span class="sxs-lookup"><span data-stu-id="c7f07-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7f07-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c7f07-153">Additional resources</span></span>

[<span data-ttu-id="c7f07-154">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="c7f07-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c7f07-155">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="c7f07-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="c7f07-156">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="c7f07-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="c7f07-157">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="c7f07-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="c7f07-158">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="c7f07-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="c7f07-159">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="c7f07-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="c7f07-160">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="c7f07-160">Work with publish groups</span></span>](publish-groups.md)
