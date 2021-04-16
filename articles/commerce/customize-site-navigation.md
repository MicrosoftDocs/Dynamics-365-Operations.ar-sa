---
title: تخصيص التنقل في الموقع
description: يوضح هذا الموضوع كيفية إنشاء تسلسل هرمي مخصص للتنقل عبر الإنترنت لتنظيم منتجاتك لاستعراض موقع Microsoft Dynamics 365 Commerce الخاص بك.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799339"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="2231d-103">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="2231d-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2231d-104">يوضح هذا الموضوع كيفية إنشاء تسلسل هرمي مخصص للتنقل عبر الإنترنت لتنظيم منتجاتك لاستعراض موقع Microsoft Dynamics 365 Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2231d-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="2231d-105">تتيح واجهات المتاجر على الإنترنت للعملاء اكتشاف المنتجات وتصفحها من خلال التنقل بين فئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="2231d-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="2231d-106">وعادةً ما يتم توفير هذه الإمكانية بواسطة علامات التبويب في أعلي الصفحة أو بواسطة شريط تنقل على اليسار.</span><span class="sxs-lookup"><span data-stu-id="2231d-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="2231d-107">في Dynamics 365 Commerce، يمكنك إنشاء وإدارة البنية الهرمية الخاصة بالتنقل بين الفئات والمنتجات المضمنة في الفئات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="2231d-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="2231d-108">إنشاء تدرج هرمي للتنقل في قناة</span><span class="sxs-lookup"><span data-stu-id="2231d-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="2231d-109">لإنشاء تدرج هرمي للتنقل في قناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2231d-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2231d-110">انتقل إلى **البيع بالتجزئة والتجارة \> المنتجات والفئات \> إدارة الفئات والمنتجات**.</span><span class="sxs-lookup"><span data-stu-id="2231d-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="2231d-111">حدد **‏‫التدرجات الهرمية للفئات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2231d-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="2231d-112">اسم التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="2231d-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2231d-113">وتعد الفئة العليا التي تقوم بإنشاءها هي عقدة فئة الجذر.</span><span class="sxs-lookup"><span data-stu-id="2231d-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="2231d-114">لن يتم إظهارها على الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2231d-114">It won't be shown on your site.</span></span> <span data-ttu-id="2231d-115">لإنشاء تدرج هرمي للفئات حيث يتم عرض عقدة عُليا مفردة في موقعك، قم بإنشاء الفئة وتسميتها كتابع لفئة الجذر.</span><span class="sxs-lookup"><span data-stu-id="2231d-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="2231d-116">حدد **عقدة فئة جديدة**، ثم قم بتسمية الفئة.</span><span class="sxs-lookup"><span data-stu-id="2231d-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="2231d-117">تابع في إنشاء الفئات المشابهة والتابعة على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="2231d-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="2231d-118">يمكنك الآن تعيين المنتجات لكل فئة قمت بإنشاءها ضمن فئة المستوي العلوي.</span><span class="sxs-lookup"><span data-stu-id="2231d-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="2231d-119">تخصيص ترتيب الفئات</span><span class="sxs-lookup"><span data-stu-id="2231d-119">Customize the order of categories</span></span>

<span data-ttu-id="2231d-120">بشكل افتراضي، سوف تظهر الفئات التي تقوم بتعريفها بترتيب أبجدي على الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2231d-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="2231d-121">ومع ذلك، يمكنك أيضًا تخصيص ترتيب عرض الفئات.</span><span class="sxs-lookup"><span data-stu-id="2231d-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="2231d-122">تعيين نوع تدرج فئات هرمي</span><span class="sxs-lookup"><span data-stu-id="2231d-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="2231d-123">انتقل إلى **البيع بالتجزئة والتجارة \> المنتجات والفئات \> إدارة الفئات والمنتجات**.</span><span class="sxs-lookup"><span data-stu-id="2231d-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="2231d-124">حدد **التدرجات الهرمية للفئات**</span><span class="sxs-lookup"><span data-stu-id="2231d-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="2231d-125">في جزء الإجراءات، في علامة تبويب **التدرج الهرمي للفئات** ، في مجموعة **الإعداد‬** ، حدد **إقران نوع التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="2231d-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="2231d-126">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2231d-126">Select **New**.</span></span>
1. <span data-ttu-id="2231d-127">في الحقل **نوع التدرج الهرمي للفئة**، حدد **التدرج الهرمي للتنقل في قناة**.</span><span class="sxs-lookup"><span data-stu-id="2231d-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="2231d-128">في الحقل **التدرج الهرمي للفئات** ، حدد التدرج الهرمي للتنقل في القناة‬ الذي قمت بإنشاءه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="2231d-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="2231d-129">نشر ‏‫التدرجات الهرمية للتنقل الجديدة أو المحدثة</span><span class="sxs-lookup"><span data-stu-id="2231d-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="2231d-130">لجعل التدرج الهرمي للتنقل الخاص بك متاحًا لواجهة المتجر عبر الإنترنت الخاص بك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2231d-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="2231d-131">انتقل إلى **البيع بالتجزئة والتجارة \>إعداد القناة \> فئات القنوات وسمات المنتج**.</span><span class="sxs-lookup"><span data-stu-id="2231d-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="2231d-132">في الشجرة الموجودة على اليسار، حدد المتجر الخاص بك على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="2231d-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="2231d-133">حدد **تحديثات نشر القناة**.</span><span class="sxs-lookup"><span data-stu-id="2231d-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="2231d-134">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="2231d-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="2231d-135">في القائمة، ابحث وحدد **المهمة 1040**.</span><span class="sxs-lookup"><span data-stu-id="2231d-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="2231d-136">حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="2231d-136">Select **Run now**.</span></span>
1. <span data-ttu-id="2231d-137">كرر الخطوتين 5 و 6 للمهام 1070 و 1150.</span><span class="sxs-lookup"><span data-stu-id="2231d-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="2231d-138">إظهار الفئات على الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="2231d-138">Show categories on your site</span></span>

<span data-ttu-id="2231d-139">لإظهار التدرج الهرمي للفئات على واجهة المتجر الخاص بك عبر الإنترنت، يجب عليك إضافة وحدة قائمة التنقل في الموقع المناسب في قالب أو جزء.</span><span class="sxs-lookup"><span data-stu-id="2231d-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="2231d-140">ستعرض الوحدة النمطية لقائمة التنقل التدرج الهرمي للتنقل، بشرط أن تكون قد قمت بنشر التدرج الهرمي للتنقل في القناة التي يرتبط بها موقعك.</span><span class="sxs-lookup"><span data-stu-id="2231d-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="2231d-141">تتيح الوحدة النمطية لقائمة التنقل المضمنة في مكتبة الوحدات النمطية للمستخدمين التنقل فقط إلى الفئات التي ليس لها فئات فرعية.</span><span class="sxs-lookup"><span data-stu-id="2231d-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="2231d-142">إذا كان بإمكان عملائك الانتقال إلى الفئات التي تحتوي على فئات فرعي ، فيجب عليك تخصيص الوحدة النمطية لقائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="2231d-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="2231d-143">إضافة خيارات التنقل المخصصة</span><span class="sxs-lookup"><span data-stu-id="2231d-143">Add custom navigation options</span></span>

<span data-ttu-id="2231d-144">في قائمة التنقل، يمكنك إضافة خيارات التنقل التي لا تشكل جزءًا من التدرج الهرمي لفئة المنتج الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2231d-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="2231d-145">على سبيل المثال، في نهاية قائمة فئات المنتجات، يمكنك إضافة عنصر **اتصل بنا** الذي يُشير إلى صفحة اتصال قمت بإنشائها لموقعك.</span><span class="sxs-lookup"><span data-stu-id="2231d-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="2231d-146">لإضافة خيارات التنقل المخصصة إلى قائمة التنقل الخاصة بك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2231d-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="2231d-147">في القالب أو الجزء الذي تريد تخصيصه، حدد وحدة قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="2231d-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="2231d-148">في جزء الخصائص، ضمن علامة التبويب **بيانات** ، حدد **إضافة عنصر** لإنشاء عنصر تنقل جديد لنظام إدارة المحتوي (CMS).</span><span class="sxs-lookup"><span data-stu-id="2231d-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="2231d-149">ادخل نص ارتباط وعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="2231d-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="2231d-150">كرر الخطوتين 2 و 3 لإضافة مزيد من خيارات التنقل المخصصة.</span><span class="sxs-lookup"><span data-stu-id="2231d-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="2231d-151">عند الانتهاء، حدد **حفظ** لحفظ قالب أو جزء، ثم حدد **إنهاء التحرير** لإيداعه.</span><span class="sxs-lookup"><span data-stu-id="2231d-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2231d-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2231d-152">Additional resources</span></span>

[<span data-ttu-id="2231d-153">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="2231d-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2231d-154">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="2231d-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="2231d-155">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="2231d-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="2231d-156">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="2231d-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2231d-157">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2231d-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2231d-158">إنشاء عنوان URL لصفحة</span><span class="sxs-lookup"><span data-stu-id="2231d-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="2231d-159">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="2231d-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
