---
title: وحدة مسار التنقل
description: يتناول هذا الموضوع وحدات مسار التنقل ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec9f5c72b03d9fd76055369e24491db5c7633cdf
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517150"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="2b024-103">وحدة مسار التنقل</span><span class="sxs-lookup"><span data-stu-id="2b024-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b024-104">يتناول هذا الموضوع وحدات مسار التنقل ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2b024-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b024-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="2b024-105">Overview</span></span>

<span data-ttu-id="2b024-106">تستخدم وحدات مسار التنقل لتوفير التنقل الثانوي في صفحات الموقع.</span><span class="sxs-lookup"><span data-stu-id="2b024-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="2b024-107">وتظهر عادة في أعلى الصفحة، أسفل الرأس.</span><span class="sxs-lookup"><span data-stu-id="2b024-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="2b024-108">على الرغم من إمكانية إضافة وحدات مسار التنقل إلى أي صفحة، فهي تُستخدم في معظم الأحيان في صفحات تفاصيل المنتجات (PDP)، لإظهار التدرج الهرمي لفئات المنتج وتوفير طريقة سريعة للتنقل في الموقع.</span><span class="sxs-lookup"><span data-stu-id="2b024-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="2b024-109">ويمكن أيضًا استخدام وحدة مسار التنقل لإظهار ارتباط "العودة إلى النتائج" عندما يقوم المستخدمون بفتح PDP من صفحة بحث أو قائمة.</span><span class="sxs-lookup"><span data-stu-id="2b024-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="2b024-110">وتسمح هذه الطريقة للمستخدمين بالعودة بسرعة إلى صفحة القائمة المصفاة لمتابعة التسوق.</span><span class="sxs-lookup"><span data-stu-id="2b024-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="2b024-111">في الصفحات التي تحتوي على سياق فئة المنتجات، مثل صفحات PDP وصفحات الفئات، تعرض وحدات مسار التنقل التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="2b024-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="2b024-112">في الصفحات التي لا تحتوي على سياق الفئة، تعرض وحدات مسار التنقل **&lt;جذر الموقع&gt; / &lt;الصفحة الحالية&gt;** بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="2b024-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="2b024-113">يمكن أيضًا تكوين وحدات مسار التنقل يدويًا على أنواع أخرى م صفحات الموقع لعرض ارتباطات إلى صفحات معينة في الموقع.</span><span class="sxs-lookup"><span data-stu-id="2b024-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="2b024-114">تتوفر الوحدة النمطية مسار التنقل في Dynamics 365 Commerce الإصدار 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="2b024-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="2b024-115">تظهر الصورة التالية مثالاً عن وحدة مسار تنقل تعرض التدرج الهرمي للفئات على صفحة PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![مثال عن وحدة مسار تنقل](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="2b024-117">إعدادات وحدة مسار التنقل</span><span class="sxs-lookup"><span data-stu-id="2b024-117">Breadcrumb module settings</span></span>

<span data-ttu-id="2b024-118">تعتمد وحدة مسار التنقل على الإعداد **نوع عرض مسار التنقل على PDP** المحدد في **إعدادات الموقع \> الملحقات** في منشئ الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="2b024-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="2b024-119">تتوفر لدى هذا الخيار ثلاث إعدادات ممكنة:</span><span class="sxs-lookup"><span data-stu-id="2b024-119">This setting has three possible values:</span></span>

- <span data-ttu-id="2b024-120">**إظهار التدرج الهرمي للفئات** – عند تحديد هذه القيمة، سوف تعرض وحدة مسار التنقل التدرج الهرمي الكامل للفئات‏‎ للمنتج الذي يتم عرضه على PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="2b024-121">**إظهار "العودة إلى النتائج"** – عند تحديد هذه القيمة، سوف تعرض وحدة مسار التنقل ارتباط "العودة إلى النتائج" على PDP إذا قام المستخدم بفتح PDP من وحدة تسمح بظهور ارتباط "العودة إلى النتائج".</span><span class="sxs-lookup"><span data-stu-id="2b024-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="2b024-122">تتوفر هذه الوظيفة عندما ينتقل المستخدمون من صفحات الفئات والبحث والقوائم وقوائم التوصيات.</span><span class="sxs-lookup"><span data-stu-id="2b024-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="2b024-123">لدعم هذه الوظيفة، تتوفر الخاصية **السماح بالعودة إلى النتائج على PDP‎** لوحدات مجموعة المنتجات ونتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="2b024-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="2b024-124">تمنحك هذه الخاصية المرونة التي تسمح لك بتعريف الوحدات التي يجب أن تدعم وظيفة ارتباط "العودة إلى النتائج" في PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="2b024-125">على سبيل المثال، عند تحديد **إظهار العودة إلى النتائج** للإعداد **نوع عرض مسار التنقل على PDP** وتحديد **السماح بالعودة إلى النتائج على PDP** لوحدة نتائج البحث على صفحة البحث، سيظهر ارتباط "العودة إلى النتائج" عندما ينتقل المستخدمون من صفحة البحث إلى PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="2b024-126">**إظهار التدرج الهرمي للفئات والعودة إلى النتائج** – هذه القيمة عبارة عن مجموعة تتكوّن من القيمتين السابقتين</span><span class="sxs-lookup"><span data-stu-id="2b024-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="2b024-127">عند تحديد هذه القيمة، ستعرض وحدة مسار التنقل التدرج الهرمي الكامل للفئات‏‎ لشريط وارتباط "العودة إلى النتائج" (إذا تم تكوينه) على PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b024-128">تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="2b024-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="2b024-129">إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2b024-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="2b024-130">للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="2b024-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="2b024-131">خصائص وحدة مسار التنقل</span><span class="sxs-lookup"><span data-stu-id="2b024-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="2b024-132">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="2b024-132">Property name</span></span> | <span data-ttu-id="2b024-133">القيم</span><span class="sxs-lookup"><span data-stu-id="2b024-133">Values</span></span> | <span data-ttu-id="2b024-134">الوصف</span><span class="sxs-lookup"><span data-stu-id="2b024-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="2b024-135">الجذر</span><span class="sxs-lookup"><span data-stu-id="2b024-135">Root</span></span> | <span data-ttu-id="2b024-136">نص أو ارتباط</span><span class="sxs-lookup"><span data-stu-id="2b024-136">Text or link</span></span>| <span data-ttu-id="2b024-137">تحدد هذه الخاصية الاختيارية نص الارتباط وهدف الارتباط لجذر موقع مسار التنقل.</span><span class="sxs-lookup"><span data-stu-id="2b024-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="2b024-138">إذا لم يتم تكوين هذه الخاصية، لن يتم تعريف أي جذر.</span><span class="sxs-lookup"><span data-stu-id="2b024-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="2b024-139">ارتباط مسار التنقل</span><span class="sxs-lookup"><span data-stu-id="2b024-139">Breadcrumb link</span></span> | <span data-ttu-id="2b024-140">ربط</span><span class="sxs-lookup"><span data-stu-id="2b024-140">Link</span></span> | <span data-ttu-id="2b024-141">تحدد هذه الخاصية الاختيارية ارتباطات مسار التنقل المكوّن بطريقة يدوية، إذا كانت هذه الارتباطات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2b024-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="2b024-142">تظهر الارتباطات بالترتيب الذي تم إدراجها به.</span><span class="sxs-lookup"><span data-stu-id="2b024-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="2b024-143">إضافة وحدة مسار تنقل إلى صفحة جديدة</span><span class="sxs-lookup"><span data-stu-id="2b024-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="2b024-144">لإضافة إضافة وحدة مسار تنقل إلى PDP وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="2b024-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2b024-145">انتقل إلى **إعدادات الموقع \> الملحقات**، وللإعداد ‬‏‫‬‏‫**نوع عرض مسار التنقل على PDP‬‏‫‬‏‫** ، حدد ‬‏‫‬‏‫**إظهار التدرج الهرمي للفئات‬‏‫**.‬</span><span class="sxs-lookup"><span data-stu-id="2b024-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="2b024-146">انتقل إلى **القوالب**، وحدد القالب PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="2b024-147">في فتحة **الحاوية** التي تحتوي على صندوق الشراء، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2b024-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b024-148">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**مسار التنقل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b024-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b024-149">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="2b024-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2b024-150">انتقل إلى **الصفحات**، وافتح صفحة PDP التي تستخدم قالب PDP.</span><span class="sxs-lookup"><span data-stu-id="2b024-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="2b024-151">في حال عدم وجود صفحة PDP، فيمكنك إنشاء واحدة.</span><span class="sxs-lookup"><span data-stu-id="2b024-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="2b024-152">في فتحة **الحاوية** التي تحتوي على صندوق الشراء، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="2b024-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b024-153">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**مسار التنقل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b024-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b024-154">في جزء الخصائص لفتحة **مسار التنقل**، تحت **الجذر**، حدد **نص الارتباط**.</span><span class="sxs-lookup"><span data-stu-id="2b024-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="2b024-155">في مربع الحوار **نص الارتباط**، أدخل إلى **الصفحة الرئيسية**، ثم تحت **هدف الارتباط**، حدد **إضافة ارتباط**.</span><span class="sxs-lookup"><span data-stu-id="2b024-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="2b024-156">في مربع الحوار **إضافة ارتباط**، حدد ارتباطًا لجذر مسار التنقل، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="2b024-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="2b024-157">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2b024-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="2b024-158">حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="2b024-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b024-159">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2b024-159">Additional resources</span></span>

[<span data-ttu-id="2b024-160">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="2b024-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2b024-161">الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="2b024-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="2b024-162">الوحدة النمطية لمحدد الموقع</span><span class="sxs-lookup"><span data-stu-id="2b024-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="2b024-163">نظرة عامة على الصفحة المنتقل إليها‬ للفئة الافتراضية وصفحة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="2b024-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="2b024-164">وحدات مجموعة المنتجات</span><span class="sxs-lookup"><span data-stu-id="2b024-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="2b024-165">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="2b024-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2b024-166">تحديثات SDK ومكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="2b024-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
