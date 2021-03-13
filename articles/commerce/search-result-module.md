---
title: وحدة نتائج البحث
description: يتناول هذا الموضوع وحدات نتائج البحث ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097168"
---
# <a name="search-results-module"></a><span data-ttu-id="295b5-103">وحدة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="295b5-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="295b5-104">يتناول هذا الموضوع وحدات نتائج البحث ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="295b5-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="295b5-105">تقوم الوحدة النمطية لنتائج البحث بإرجاع نتائج البحث عن المنتج وقائمة بالمدققات المعمول بها للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="295b5-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="295b5-106">يمكن استخدام الوحدات النمطية لنتائج البحث في Dynamics 365 Commerce لعرض الصفحات للسيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="295b5-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="295b5-107">نتائج البحث التي تم بدؤها بواسطة البحث عن مستخدم</span><span class="sxs-lookup"><span data-stu-id="295b5-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="295b5-108">نتائج البحث التي تعرض مجموعة معينه من المنتجات، مثل "تسوق منتجات تبدو مماثلة"</span><span class="sxs-lookup"><span data-stu-id="295b5-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="295b5-109">قوائم المنتجات التي تنتمي إلى فئة ما</span><span class="sxs-lookup"><span data-stu-id="295b5-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="295b5-110">لمزيد من المعلومات حول صفحات الفئة ونتائج البحث، راجع [نظره عامة عن ‏‫الصفحة المنتقل إليها‬ للفئة الافتراضية وصفحة نتائج البحث](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="295b5-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="295b5-111">يبين الرسم التوضيحي التالي مثالاً لصفحة نتائج البحث لفئة معروضة في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="295b5-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![مثال عن صفحة نتائج البحث في موقع Fabrikam](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="295b5-113">خصائص وحدة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="295b5-113">Search results module properties</span></span>

<span data-ttu-id="295b5-114">يسرد الجدول التالي خصائص الوحدات النمطية لنتائج البحث، إلى جانب القيم والأوصاف الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="295b5-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="295b5-115">الخاصية</span><span class="sxs-lookup"><span data-stu-id="295b5-115">Property</span></span> | <span data-ttu-id="295b5-116">القيم</span><span class="sxs-lookup"><span data-stu-id="295b5-116">Values</span></span> | <span data-ttu-id="295b5-117">الوصف</span><span class="sxs-lookup"><span data-stu-id="295b5-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="295b5-118">العناصر في كل صفحة</span><span class="sxs-lookup"><span data-stu-id="295b5-118">Items per page</span></span> | <span data-ttu-id="295b5-119">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="295b5-119">Integer</span></span> | <span data-ttu-id="295b5-120">عدد العناصر التي يجب إظهارها على كل صفحة.</span><span class="sxs-lookup"><span data-stu-id="295b5-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="295b5-121">السماح بالرجوع من PDP</span><span class="sxs-lookup"><span data-stu-id="295b5-121">Allow back on PDP</span></span> | <span data-ttu-id="295b5-122">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="295b5-122">**True** or **False**</span></span> | <span data-ttu-id="295b5-123">إذا تم تعيين هذه الخاصية على **صحيح**، عندما يقوم مستخدم بتحديد منتج على صفحة نتائج البحث، سيظهر التنقل التفصيلي في صفحة تفاصيل المنتج (PDP) التي تم فتحها في ارتباط "العودة إلى النتائج".</span><span class="sxs-lookup"><span data-stu-id="295b5-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="295b5-124">توسيع المدققات</span><span class="sxs-lookup"><span data-stu-id="295b5-124">Expand Refiners</span></span> | <span data-ttu-id="295b5-125">**الكل** أو **1** أو **2** أو **3** أو **4**</span><span class="sxs-lookup"><span data-stu-id="295b5-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="295b5-126">عدد أهم المدققات التي يجب توسيعها عند تحميل صفحة.</span><span class="sxs-lookup"><span data-stu-id="295b5-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="295b5-127">على سبيل المثال، إذا تم تعيين هذه الخاصية إلى **3**، سيتم توسيع أول ثلاث مدققات على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="295b5-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="295b5-128">إخفاء عرض التدرج الهرمي للفئة</span><span class="sxs-lookup"><span data-stu-id="295b5-128">Hide category hierarchy display</span></span> | <span data-ttu-id="295b5-129">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="295b5-129">**True** or **False**</span></span> | <span data-ttu-id="295b5-130">إذا تم تعيين هذه الخاصية على **صحيح**، سيتم إخفاء عرض التدرج الهرمي للفئات على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="295b5-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="295b5-131">يجب تعيين هذه الخاصية على **صحيح** إذا كنت تستخدم [وحدة مسار التنقل‬](add-breadcrumb.md) لإظهار التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="295b5-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="295b5-132">تضمين سمات المنتج في نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="295b5-132">Include product attributes in search results</span></span> | <span data-ttu-id="295b5-133">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="295b5-133">**True** or **False**</span></span> | <span data-ttu-id="295b5-134">إذا تم تعيين هذه الخاصية على **صحيح**، سيتم إرجاع السمات للمنتجات الموجودة في نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="295b5-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="295b5-135">على الرغم من أنه يمكن إظهار هذه السمات على موقع Commerce، لكن يلزم وجود ملحق.</span><span class="sxs-lookup"><span data-stu-id="295b5-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="295b5-136">إظهار الأسعار المقترنة</span><span class="sxs-lookup"><span data-stu-id="295b5-136">Show affiliation prices</span></span> | <span data-ttu-id="295b5-137">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="295b5-137">**True** or **False**</span></span> | <span data-ttu-id="295b5-138">إذا تم تعيين هذه الخاصية على **صحيح**، سيتم عرض الأسعار التبعية للمنتجات في نتائج البحث عندما يقوم مستخدم مسجل الدخول باستعراض الصفحة.</span><span class="sxs-lookup"><span data-stu-id="295b5-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="295b5-139">في Dynamics 365 Commerce الإصدار 10.0.16 والإصدارات الأحدث، يمكن استخدام التكوين **عرض الأسعار التبعية** لإظهار الأسعار التبعية على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="295b5-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="295b5-140">الوحدات المدعومة</span><span class="sxs-lookup"><span data-stu-id="295b5-140">Supported modules</span></span>

<span data-ttu-id="295b5-141">تدعم الوحدة النمطية لنتائج البحث [الوحدة النمطية للعرض السريع](quick-view-module.md)، والتي تتيح للمستخدمين عرض معلومات المنتج وإضافة الأصناف إلى سلة التسوق من صفحة نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="295b5-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="295b5-142">أضافة وحدة نمطية لنتائج البحث إلى صفحة الفئة</span><span class="sxs-lookup"><span data-stu-id="295b5-142">Add a search results module to a category page</span></span>

<span data-ttu-id="295b5-143">لإضافة وحدة نمطية لنتائج البحث إلى صفحة فئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="295b5-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="295b5-144">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="295b5-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="295b5-145">في مربع الحوار **قالب جديد**، أدخل الاسم **نتائج البحث**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="295b5-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="295b5-146">في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (...)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="295b5-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="295b5-147">في مربع الحوار **إضافة وحدة**، حدد وحدة **الصفحة الافتراضية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="295b5-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="295b5-148">في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (...)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="295b5-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="295b5-149">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="295b5-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="295b5-150">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (...)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="295b5-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="295b5-151">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**مسار التنقل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="295b5-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="295b5-152">في جزء خصائص **مسار التنقل**، أدخل القيمة **1** لـ **الحد الأدنى لمرات الحدوث**.</span><span class="sxs-lookup"><span data-stu-id="295b5-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="295b5-153">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (...)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="295b5-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="295b5-154">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**نتائج البحث‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="295b5-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="295b5-155">في جزء خصائص **نتائج البحث**، أدخل القيمة **1** لـ **الحد الأدنى لمرات الحدوث**، ثم قم بتعيين أي خصائص مطلوبى أخرى للوحدة النمطية لنتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="295b5-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="295b5-156">بتعيين هذه الخصائص في القالب، تضمن أن يتم تلقائيًا تضمين أي تخصيصات لصفحة فئة خاصة تلقائيًا في هذه الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="295b5-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="295b5-157">حدد **إنهاء التحرير** ثم حدد **نشر** لنشر القالب.</span><span class="sxs-lookup"><span data-stu-id="295b5-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="295b5-158">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="295b5-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="295b5-159">في مربع الحوار **اختيار قالب** ، حدد قالب **نتائج البحث** الذي قمت بإنشائه، وأدخل **صفحة الفئة** لـ **اسم الصفحة**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="295b5-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="295b5-160">نظرا لأنه تم تعيين كافة القيم في القالب، تكون الصفحة جاهزة للنشر.</span><span class="sxs-lookup"><span data-stu-id="295b5-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="295b5-161">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="295b5-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="295b5-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="295b5-162">Additional resources</span></span>

[<span data-ttu-id="295b5-163">نظرة عامة على الصفحة المنتقل إليها‬ للفئة الافتراضية وصفحة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="295b5-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="295b5-164">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="295b5-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="295b5-165">الوحدة النمطية للعرض السريع</span><span class="sxs-lookup"><span data-stu-id="295b5-165">Quick view module</span></span>](quick-view-module.md)
