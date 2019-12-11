---
title: تكوين التقييمات والمراجعات
description: يوضح هذا الموضوع كيفية تكوين موقع التجارة الإلكترونية لإظهار تصنيفات العملاء ومراجعاتها في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770471"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="fe291-103">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="fe291-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fe291-104">يوضح هذا الموضوع كيفية تكوين موقع التجارة الإلكترونية لإظهار تصنيفات العملاء ومراجعاتها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe291-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fe291-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="fe291-105">Overview</span></span>

<span data-ttu-id="fe291-106">تساعد التقييمات والمراجعات على مواقع التجارة الإلكترونية العملاء على التعرف على المنتجات قبل اتخاذ قرار الشراء، وذلك من خلال إظهار ما يفكر فيه العملاء الآخرون بشأن هذه المنتجات.</span><span class="sxs-lookup"><span data-stu-id="fe291-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="fe291-107">بالنسبة لمواقع التجارة الإلكترونية، تعد التصنيفات والمراجعات أيضًا آلية لجمع تعليقات العملاء حول المنتجات.</span><span class="sxs-lookup"><span data-stu-id="fe291-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="fe291-108">تظهر التقييمات في صفحات قائمة المنتجات وصفحات قائمة الفئات وصفحات نتائج البحث وصفحات الموقع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="fe291-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="fe291-109">يتم عرض مدرج تكراري للتقييمات ومراجعات المنتج على صفحات تفاصيل المنتج (PDPs).</span><span class="sxs-lookup"><span data-stu-id="fe291-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="fe291-110">يُتيح زر **اكتب مراجعة** للعملاء إرسال تقييمات ومراجعات لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="fe291-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="fe291-111">الوحدات النمطية للتقييمات والمراجعات على PDPs</span><span class="sxs-lookup"><span data-stu-id="fe291-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="fe291-112">تظهر ثلاث وحدات نمطية ملخص التقييمات والمراجعات على PDPs:</span><span class="sxs-lookup"><span data-stu-id="fe291-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="fe291-113">الوحدة النمطية لكتابة المراجعة</span><span class="sxs-lookup"><span data-stu-id="fe291-113">Write review module</span></span>
- <span data-ttu-id="fe291-114">الوحدة النمطية لقائمه مراجعات المنتج</span><span class="sxs-lookup"><span data-stu-id="fe291-114">Product reviews list module</span></span>
- <span data-ttu-id="fe291-115">الوحدة النمطية للمدرج التكراري للتقييمات</span><span class="sxs-lookup"><span data-stu-id="fe291-115">Ratings histogram module</span></span>
 
<span data-ttu-id="fe291-116">يوضح الرسم التوضيحي التالي شكل وحدات التقييم والمراجعات على PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![الوحدات النمطية للتقييمات والمراجعات على PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="fe291-118">للحصول على معلومات حول كيفية تحسين قوالب وتخطيطات PDP بحيث يمكنك مشاركة تكوينات الوحدات النمطية للتقييمات والمراجعات بين عدة PDPs على موقع التجارة الإلكترونية الخاص بك، راجع [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fe291-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="fe291-119">يبين الرسم التوضيحي التالي كيف يعرض مربع الحوار **إضافة وحدة نمطية** الوحدات النمطية للتقييمات والمراجعات في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe291-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![إضافة مربع حوار وحدة نمطية](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="fe291-121">الوحدة النمطية لكتابة المراجعة</span><span class="sxs-lookup"><span data-stu-id="fe291-121">Write review module</span></span>

<span data-ttu-id="fe291-122">تتضمن الوحدة النمطية لكتابة المراجعة زر **كتابة المراجعة** الذي يتيح للمستخدمين تسجيل الدخول، وتعيين تقييم، وكتابة مراجعة لمنتج.</span><span class="sxs-lookup"><span data-stu-id="fe291-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="fe291-123">تتيح هذه الوحدة النمطية أيضًا للمستخدمين تحرير تقييم أو مراجعة ارسلوها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="fe291-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="fe291-124">تظهر هذه الوحدة النمطية عادةً فوق المدرج التكراري للتقييمات والوحدات النمطية لقائمة المنتجات على PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="fe291-125">يعرض الرسم التوضيحي التالي مربع الحوار **كتابة مراجعة** والذي يظهر عندما يحدد العميل **كتابة مراجعة**.</span><span class="sxs-lookup"><span data-stu-id="fe291-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="fe291-126">يمكن للعميل استخدام مربع الحوار هذا لإرسال تقييم ومراجعة.</span><span class="sxs-lookup"><span data-stu-id="fe291-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![مربع حوار كتابة مراجعة](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="fe291-128">يعرض الجدول التالي خاصية الوحدة النمطية مراجعة الكتابة التي يجب تكوينها في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="fe291-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="fe291-129">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="fe291-129">Property name</span></span> | <span data-ttu-id="fe291-130">القيمة</span><span class="sxs-lookup"><span data-stu-id="fe291-130">Value</span></span>        | <span data-ttu-id="fe291-131">وصف الخاصية</span><span class="sxs-lookup"><span data-stu-id="fe291-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="fe291-132">الاسم</span><span class="sxs-lookup"><span data-stu-id="fe291-132">Name</span></span>          | <span data-ttu-id="fe291-133">كتابة مراجعة</span><span class="sxs-lookup"><span data-stu-id="fe291-133">Write review</span></span> | <span data-ttu-id="fe291-134">اسم الوحدة النمطية لكتابة مراجعة.</span><span class="sxs-lookup"><span data-stu-id="fe291-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="fe291-135">الوحدة النمطية للمدرج التكراري للتقييمات</span><span class="sxs-lookup"><span data-stu-id="fe291-135">Ratings histogram module</span></span>

<span data-ttu-id="fe291-136">تعرض الوحدة النمطية المدرج التكراري للتقييمات مدرج تكراري للتقييمات.</span><span class="sxs-lookup"><span data-stu-id="fe291-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="fe291-137">وعادةً ما تظهر هذه الوحدة النمطية بين الوحدة النمطية لكتابة مراجعة والوحدة النمطية لقائمة مراجعات المنتجات على PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="fe291-138">لا تتطلب الوحدة النمطية المدرج التكراري للتقييمات أي تكوين.</span><span class="sxs-lookup"><span data-stu-id="fe291-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="fe291-139">عليك فقط إضافة الوحدة النمطية في قالب PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="fe291-140">توضح الرسوم التوضيحية التالية كيف يبدو قالب PDP في Dynamics 365 Commerce عند تكوين الوحدات النمطية للتقييمات والمراجعات للعرض على PDPs.</span><span class="sxs-lookup"><span data-stu-id="fe291-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![يتم تكوين قالب PDP عند التقييمات والمراجعات للعرض على PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="fe291-142">الوحدة النمطية لقائمه مراجعات المنتج</span><span class="sxs-lookup"><span data-stu-id="fe291-142">Product reviews list module</span></span>

<span data-ttu-id="fe291-143">تعرض الوحدة النمطية قائمة مراجعات المنتج قائمة بمراجعات المنتج مع خيارات الفرز والترشيح وترقيم الصفحات.</span><span class="sxs-lookup"><span data-stu-id="fe291-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="fe291-144">عادةً ما تظهر هذه الوحدة النمطية بعد الوحدة النمطية المدرج التكراري للتقييمات على PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="fe291-145">يعرض الجدول التالي خصائص الوحدة النمطية قائمة مراجعات المنتج التي يجب تكوينها في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="fe291-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="fe291-146">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="fe291-146">Property name</span></span>              | <span data-ttu-id="fe291-147">القيمة</span><span class="sxs-lookup"><span data-stu-id="fe291-147">Value</span></span> | <span data-ttu-id="fe291-148">وصف الخاصية</span><span class="sxs-lookup"><span data-stu-id="fe291-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="fe291-149">تظهر المراجعات في كل صفحة</span><span class="sxs-lookup"><span data-stu-id="fe291-149">Reviews shown on each page</span></span> | <span data-ttu-id="fe291-150">10</span><span class="sxs-lookup"><span data-stu-id="fe291-150">10</span></span>    | <span data-ttu-id="fe291-151">عدد المراجعات التي يجب أن تظهر في وقت واحد على PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="fe291-152">يتم تضمين الزرين**التالي** و **السابق** ، بحيث يمكن للمستخدمين التنقل من خلال صفحات الاستعراضات.</span><span class="sxs-lookup"><span data-stu-id="fe291-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="fe291-153">المدرج التكراري للتقييمات -عرض ملخص</span><span class="sxs-lookup"><span data-stu-id="fe291-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="fe291-154">تشتمل الوحدة النمطية قائمة مراجعات المنتج على فتحة حيث يمكنك إضافة الوحدة النمطية مدرج تكراري للتقييمات.</span><span class="sxs-lookup"><span data-stu-id="fe291-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="fe291-155">يوضح الرسم التوضيحي التالي كيف يمكنك إضافة الوحدة النمطية مدرج تكراري للتقييمات في الوحدة النمطية قائمة مراجعات المنتج في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe291-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![إضافة الوحدة النمطية مدرج تكراري للتقييمات في الوحدة النمطية قائمة مراجعات المنتج](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="fe291-157">تكوين موقع لإظهار التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="fe291-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="fe291-158">يتم تكوين قيم التكوين الخاصة بالتقييمات والمراجعات، مثل معرف المستأجر وطول نص المراجعة وطول عنوان المراجعة، على مستوى الموقع.</span><span class="sxs-lookup"><span data-stu-id="fe291-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="fe291-159">لتكوين موقع لإظهار التقييمات والمراجعات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fe291-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="fe291-160">الانتقال **إلى الصفحة الرئيسية \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="fe291-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="fe291-161">حدد اسم موقعك.</span><span class="sxs-lookup"><span data-stu-id="fe291-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="fe291-162">انتقل إلى **إدارة الموقع \> ‏‫قابلية التوسعة**.</span><span class="sxs-lookup"><span data-stu-id="fe291-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="fe291-163">في الحقل **أقصى طول لنص المراجعة** ، أدخل الحد الأقصى لعدد الأحرف التي يمكن أن يشتمل عليها نص المراجعة (على سبيل المثال، **1000**).</span><span class="sxs-lookup"><span data-stu-id="fe291-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="fe291-164">في الحقل **أقصى طول لعنوان المراجعة** ، أدخل الحد الأقصى لعدد الأحرف التي يمكن أن يشتمل عليها عناوين المراجعة (على سبيل المثال، **55**).</span><span class="sxs-lookup"><span data-stu-id="fe291-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="fe291-165">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="fe291-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="fe291-166">يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe291-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![تكوين موقع لإظهار التقييمات والمراجعات](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="fe291-168">ربط تقييم المنتج بقسم المراجعات في PDP</span><span class="sxs-lookup"><span data-stu-id="fe291-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="fe291-169">يتم عرض تقييم المنتج أسفل عنوان المنتج أعلى PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="fe291-170">يمكن تكوين تصنيف المنتج بحيث يكون مرتبطًا بقسم **المراجعات** لنفس PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="fe291-171">لربط تقييم منتج بقسم **المراجعات** لـ PDP، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="fe291-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="fe291-172">افتح قالب PDP.</span><span class="sxs-lookup"><span data-stu-id="fe291-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="fe291-173">انتقل إلى **إعدادات الوحدة النمطية لحاوية مربع الشراء**.</span><span class="sxs-lookup"><span data-stu-id="fe291-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="fe291-174">تحت **مربع الشراء**، حدد **تقييمات المنتج**، ثم حدد خانه الاختيار **ربط النقر بالوحدة النمطية للمراجعات الكاملة** .</span><span class="sxs-lookup"><span data-stu-id="fe291-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="fe291-175">يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe291-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![ربط تقييم المنتج بقسم المراجعات في PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="fe291-177">تكوين ارتباط صفحة الخصوصية والسياسة</span><span class="sxs-lookup"><span data-stu-id="fe291-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="fe291-178">لتكوين ارتباط صفحة الخصوصية والسياسة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fe291-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="fe291-179">الانتقال **إلى الصفحة الرئيسية \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="fe291-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="fe291-180">حدد اسم موقعك.</span><span class="sxs-lookup"><span data-stu-id="fe291-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="fe291-181">انتقل إلى **إدارة الموقع \> ‏‫قابلية التوسعة**.</span><span class="sxs-lookup"><span data-stu-id="fe291-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="fe291-182">في علامة التبويب **المسارات** ، وتحت **خصوصية وسياسة RNR**، حدد **إضافة ارتباط**.</span><span class="sxs-lookup"><span data-stu-id="fe291-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="fe291-183">إذا تم إدخال ارتباط بالفعل وتريد استبداله، فحدد الارتباط.</span><span class="sxs-lookup"><span data-stu-id="fe291-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="fe291-184">في مربع الحوار **إضافة ارتباط** ،حدد ارتباط صفحة الخصوصية والسياسة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fe291-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="fe291-185">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="fe291-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="fe291-186">يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe291-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![تكوين ارتباط صفحة الخصوصية والسياسة](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="fe291-188">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fe291-188">Additional resources</span></span>

[<span data-ttu-id="fe291-189">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="fe291-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="fe291-190">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="fe291-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="fe291-191">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="fe291-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="fe291-192">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="fe291-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
