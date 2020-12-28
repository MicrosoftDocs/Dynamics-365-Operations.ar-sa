---
title: وحدات التقييمات والمراجعات
description: يغطي هذا الموضوع الوحدات النمطية للتقييمات والمراجعات المستخدمة على صفحات تفاصيل المنتجات في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409993"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="86edb-103">وحدات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="86edb-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86edb-104">يغطي هذا الموضوع الوحدات النمطية للتقييمات والمراجعات المستخدمة على صفحات تفاصيل المنتجات (PDP) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86edb-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86edb-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="86edb-105">Overview</span></span>

<span data-ttu-id="86edb-106">تساعد التقييمات والمراجعات على مواقع التجارة الإلكترونية العملاء على التعرف على المنتجات قبل اتخاذ قرار الشراء، كما تعد بمثابة آلية لجمع ملاحظات العميل‬ بشأن هذه المنتجات.</span><span class="sxs-lookup"><span data-stu-id="86edb-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="86edb-107">تظهر التقييمات في صفحات قائمة المنتجات وصفحات قائمة الفئات وصفحات نتائج البحث وصفحات الموقع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="86edb-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="86edb-108">يتم عرض مدرج تكراري للتقييمات ومراجعات المنتج على صفحات PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="86edb-109">يُتيح زر **اكتب مراجعة** للعملاء إرسال تقييمات ومراجعات لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="86edb-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="86edb-110">ويتم التحكم في ميزات PDP بواسطة ‏‫الوحدات النمطية للتقييمات والمراجعات‬.</span><span class="sxs-lookup"><span data-stu-id="86edb-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="86edb-111">الوحدات النمطية للتقييمات والمراجعات على PDPs</span><span class="sxs-lookup"><span data-stu-id="86edb-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="86edb-112">تظهر ثلاث وحدات نمطية ملخص التقييمات والمراجعات على PDPs:</span><span class="sxs-lookup"><span data-stu-id="86edb-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="86edb-113">الوحدة النمطية لكتابة المراجعة</span><span class="sxs-lookup"><span data-stu-id="86edb-113">Write review module</span></span>
- <span data-ttu-id="86edb-114">الوحدة النمطية لقائمه مراجعات المنتج</span><span class="sxs-lookup"><span data-stu-id="86edb-114">Product reviews list module</span></span>
- <span data-ttu-id="86edb-115">الوحدة النمطية للمدرج التكراري للتقييمات</span><span class="sxs-lookup"><span data-stu-id="86edb-115">Ratings histogram module</span></span>
 
<span data-ttu-id="86edb-116">يوضح الرسم التوضيحي التالي شكل وحدات التقييم والمراجعات على PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![الوحدات النمطية للتقييمات والمراجعات على PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="86edb-118">للحصول على معلومات حول كيفية تحسين قوالب وتخطيطات PDP بحيث يمكنك مشاركة تكوينات الوحدات النمطية للتقييمات والمراجعات بين عدة PDPs على موقع التجارة الإلكترونية الخاص بك، راجع [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="86edb-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="86edb-119">يبين الرسم التوضيحي التالي كيف يعرض مربع الحوار **إضافة وحدة نمطية** الوحدات النمطية للتقييمات والمراجعات في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86edb-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="86edb-120">![إضافة مربع حوار وحدة نمطية](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="86edb-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="86edb-121">الوحدة النمطية لكتابة المراجعة</span><span class="sxs-lookup"><span data-stu-id="86edb-121">Write review module</span></span>

<span data-ttu-id="86edb-122">تتضمن الوحدة النمطية لكتابة المراجعة زر **كتابة المراجعة** الذي يتيح للمستخدمين تسجيل الدخول، وتعيين تقييم، وكتابة مراجعة لمنتج.</span><span class="sxs-lookup"><span data-stu-id="86edb-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="86edb-123">تتيح هذه الوحدة النمطية أيضًا للمستخدمين تحرير تقييم أو مراجعة ارسلوها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="86edb-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="86edb-124">تظهر هذه الوحدة النمطية عادةً فوق المدرج التكراري للتقييمات والوحدات النمطية لقائمة المنتجات على PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="86edb-125">يعرض الرسم التوضيحي التالي مربع الحوار **كتابة مراجعة** والذي يظهر عندما يحدد العميل **كتابة مراجعة**.</span><span class="sxs-lookup"><span data-stu-id="86edb-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="86edb-126">يمكن للعميل استخدام مربع الحوار هذا لإرسال تقييم ومراجعة.</span><span class="sxs-lookup"><span data-stu-id="86edb-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="86edb-127">![‏‫مربع حوار كتابة مراجعة‬](media/rnr-eCommerce-write-review-module.png) يعرض الجدول التالي خاصية الوحدة النمطية مراجعة الكتابة التي يجب تكوينها في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="86edb-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="86edb-128">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="86edb-128">Property name</span></span> | <span data-ttu-id="86edb-129">القيمة</span><span class="sxs-lookup"><span data-stu-id="86edb-129">Value</span></span>        | <span data-ttu-id="86edb-130">وصف الخاصية</span><span class="sxs-lookup"><span data-stu-id="86edb-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="86edb-131">الاسم</span><span class="sxs-lookup"><span data-stu-id="86edb-131">Name</span></span>          | <span data-ttu-id="86edb-132">كتابة مراجعة</span><span class="sxs-lookup"><span data-stu-id="86edb-132">Write review</span></span> | <span data-ttu-id="86edb-133">اسم الوحدة النمطية لكتابة مراجعة.</span><span class="sxs-lookup"><span data-stu-id="86edb-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="86edb-134">الوحدة النمطية للمدرج التكراري للتقييمات</span><span class="sxs-lookup"><span data-stu-id="86edb-134">Ratings histogram module</span></span>

<span data-ttu-id="86edb-135">تعرض الوحدة النمطية المدرج التكراري للتقييمات مدرج تكراري للتقييمات.</span><span class="sxs-lookup"><span data-stu-id="86edb-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="86edb-136">وعادةً ما تظهر هذه الوحدة النمطية بين الوحدة النمطية لكتابة مراجعة والوحدة النمطية لقائمة مراجعات المنتجات على PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="86edb-137">لا تتطلب الوحدة النمطية المدرج التكراري للتقييمات أي تكوين.</span><span class="sxs-lookup"><span data-stu-id="86edb-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="86edb-138">عليك فقط إضافة الوحدة النمطية في قالب PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="86edb-139">توضح الرسوم التوضيحية التالية كيف يبدو قالب PDP في Dynamics 365 Commerce عند تكوين الوحدات النمطية للتقييمات والمراجعات للعرض على PDPs.</span><span class="sxs-lookup"><span data-stu-id="86edb-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="86edb-140">![يتم تكوين قالب PDP عند التقييمات والمراجعات للعرض على PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="86edb-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="86edb-141">الوحدة النمطية لقائمه مراجعات المنتج</span><span class="sxs-lookup"><span data-stu-id="86edb-141">Product reviews list module</span></span>

<span data-ttu-id="86edb-142">تعرض الوحدة النمطية قائمة مراجعات المنتج قائمة بمراجعات المنتج مع خيارات الفرز والترشيح وترقيم الصفحات.</span><span class="sxs-lookup"><span data-stu-id="86edb-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="86edb-143">عادةً ما تظهر هذه الوحدة النمطية بعد الوحدة النمطية المدرج التكراري للتقييمات على PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="86edb-144">يعرض الجدول التالي خصائص الوحدة النمطية قائمة مراجعات المنتج التي يجب تكوينها في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="86edb-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="86edb-145">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="86edb-145">Property name</span></span>              | <span data-ttu-id="86edb-146">القيمة</span><span class="sxs-lookup"><span data-stu-id="86edb-146">Value</span></span> | <span data-ttu-id="86edb-147">وصف الخاصية</span><span class="sxs-lookup"><span data-stu-id="86edb-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="86edb-148">تظهر المراجعات في كل صفحة</span><span class="sxs-lookup"><span data-stu-id="86edb-148">Reviews shown on each page</span></span> | <span data-ttu-id="86edb-149">10</span><span class="sxs-lookup"><span data-stu-id="86edb-149">10</span></span>    | <span data-ttu-id="86edb-150">عدد المراجعات التي يجب أن تظهر في وقت واحد على PDP.</span><span class="sxs-lookup"><span data-stu-id="86edb-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="86edb-151">يتم تضمين الزرين **التالي** و **السابق** ، بحيث يمكن للمستخدمين التنقل من خلال صفحات الاستعراضات.</span><span class="sxs-lookup"><span data-stu-id="86edb-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="86edb-152">المدرج التكراري للتقييمات -عرض ملخص</span><span class="sxs-lookup"><span data-stu-id="86edb-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="86edb-153">تشتمل الوحدة النمطية قائمة مراجعات المنتج على فتحة حيث يمكنك إضافة الوحدة النمطية مدرج تكراري للتقييمات.</span><span class="sxs-lookup"><span data-stu-id="86edb-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="86edb-154">يوضح الرسم التوضيحي التالي كيف يمكنك إضافة الوحدة النمطية مدرج تكراري للتقييمات في الوحدة النمطية قائمة مراجعات المنتج في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86edb-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![إضافة الوحدة النمطية مدرج تكراري للتقييمات في الوحدة النمطية قائمة مراجعات المنتج](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="86edb-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="86edb-156">Additional resources</span></span>

[<span data-ttu-id="86edb-157">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="86edb-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="86edb-158">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="86edb-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="86edb-159">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="86edb-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="86edb-160">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="86edb-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="86edb-161">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="86edb-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="86edb-162">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="86edb-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="86edb-163">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="86edb-163">Footer module</span></span>](author-footer-module.md)
