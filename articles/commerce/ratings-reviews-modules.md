---
title: وحدات التقييمات والمراجعات
description: يغطي هذا الموضوع الوحدات النمطية للتقييمات والمراجعات المستخدمة على صفحات تفاصيل المنتجات في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: dee9a6a7e2a5278f069958ce00689b1beb9b1bd7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792137"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="bfa58-103">الوحدات النمطية للتقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="bfa58-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bfa58-104">يغطي هذا الموضوع الوحدات النمطية للتقييمات والمراجعات المستخدمة على صفحات تفاصيل المنتجات (PDP) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfa58-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bfa58-105">تساعد التقييمات والمراجعات على مواقع التجارة الإلكترونية العملاء على التعرف على المنتجات قبل اتخاذ قرار الشراء، كما تعد بمثابة آلية لجمع ملاحظات العميل‬ بشأن هذه المنتجات.</span><span class="sxs-lookup"><span data-stu-id="bfa58-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="bfa58-106">تظهر التقييمات في صفحات قائمة المنتجات وصفحات قائمة الفئات وصفحات نتائج البحث وصفحات الموقع الأخرى.</span><span class="sxs-lookup"><span data-stu-id="bfa58-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="bfa58-107">يتم عرض مدرج تكراري للتقييمات ومراجعات المنتج على صفحات PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="bfa58-108">يُتيح زر **اكتب مراجعة** للعملاء إرسال تقييمات ومراجعات لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="bfa58-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="bfa58-109">ويتم التحكم في ميزات PDP بواسطة ‏‫الوحدات النمطية للتقييمات والمراجعات‬.</span><span class="sxs-lookup"><span data-stu-id="bfa58-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="bfa58-110">الوحدات النمطية للتقييمات والمراجعات على PDPs</span><span class="sxs-lookup"><span data-stu-id="bfa58-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="bfa58-111">تظهر ثلاث وحدات نمطية ملخص التقييمات والمراجعات على PDPs:</span><span class="sxs-lookup"><span data-stu-id="bfa58-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="bfa58-112">الوحدة النمطية لكتابة المراجعة</span><span class="sxs-lookup"><span data-stu-id="bfa58-112">Write review module</span></span>
- <span data-ttu-id="bfa58-113">الوحدة النمطية لقائمه مراجعات المنتج</span><span class="sxs-lookup"><span data-stu-id="bfa58-113">Product reviews list module</span></span>
- <span data-ttu-id="bfa58-114">الوحدة النمطية للمدرج التكراري للتقييمات</span><span class="sxs-lookup"><span data-stu-id="bfa58-114">Ratings histogram module</span></span>
 
<span data-ttu-id="bfa58-115">يوضح الرسم التوضيحي التالي شكل وحدات التقييم والمراجعات على PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![الوحدات النمطية للتقييمات والمراجعات على PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="bfa58-117">للحصول على معلومات حول كيفية تحسين قوالب وتخطيطات PDP بحيث يمكنك مشاركة تكوينات الوحدات النمطية للتقييمات والمراجعات بين عدة PDPs على موقع التجارة الإلكترونية الخاص بك، راجع [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bfa58-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="bfa58-118">يبين الرسم التوضيحي التالي كيف يعرض مربع الحوار **إضافة وحدة نمطية** الوحدات النمطية للتقييمات والمراجعات في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfa58-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="bfa58-119">![إضافة مربع حوار وحدة نمطية](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="bfa58-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="bfa58-120">الوحدة النمطية لكتابة المراجعة</span><span class="sxs-lookup"><span data-stu-id="bfa58-120">Write review module</span></span>

<span data-ttu-id="bfa58-121">تتضمن الوحدة النمطية لكتابة المراجعة زر **كتابة المراجعة** الذي يتيح للمستخدمين تسجيل الدخول، وتعيين تقييم، وكتابة مراجعة لمنتج.</span><span class="sxs-lookup"><span data-stu-id="bfa58-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="bfa58-122">تتيح هذه الوحدة النمطية أيضًا للمستخدمين تحرير تقييم أو مراجعة ارسلوها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="bfa58-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="bfa58-123">تظهر هذه الوحدة النمطية عادةً فوق المدرج التكراري للتقييمات والوحدات النمطية لقائمة المنتجات على PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="bfa58-124">يعرض الرسم التوضيحي التالي مربع الحوار **كتابة مراجعة** والذي يظهر عندما يحدد العميل **كتابة مراجعة**.</span><span class="sxs-lookup"><span data-stu-id="bfa58-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="bfa58-125">يمكن للعميل استخدام مربع الحوار هذا لإرسال تقييم ومراجعة.</span><span class="sxs-lookup"><span data-stu-id="bfa58-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="bfa58-126">![‏‫مربع حوار كتابة مراجعة‬](media/rnr-eCommerce-write-review-module.png) يعرض الجدول التالي خاصية الوحدة النمطية مراجعة الكتابة التي يجب تكوينها في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="bfa58-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="bfa58-127">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="bfa58-127">Property name</span></span> | <span data-ttu-id="bfa58-128">القيمة</span><span class="sxs-lookup"><span data-stu-id="bfa58-128">Value</span></span>        | <span data-ttu-id="bfa58-129">وصف الخاصية</span><span class="sxs-lookup"><span data-stu-id="bfa58-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="bfa58-130">الاسم</span><span class="sxs-lookup"><span data-stu-id="bfa58-130">Name</span></span>          | <span data-ttu-id="bfa58-131">كتابة مراجعة</span><span class="sxs-lookup"><span data-stu-id="bfa58-131">Write review</span></span> | <span data-ttu-id="bfa58-132">اسم الوحدة النمطية لكتابة مراجعة.</span><span class="sxs-lookup"><span data-stu-id="bfa58-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="bfa58-133">الوحدة النمطية للمدرج التكراري للتقييمات</span><span class="sxs-lookup"><span data-stu-id="bfa58-133">Ratings histogram module</span></span>

<span data-ttu-id="bfa58-134">تعرض الوحدة النمطية المدرج التكراري للتقييمات مدرج تكراري للتقييمات.</span><span class="sxs-lookup"><span data-stu-id="bfa58-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="bfa58-135">وعادةً ما تظهر هذه الوحدة النمطية بين الوحدة النمطية لكتابة مراجعة والوحدة النمطية لقائمة مراجعات المنتجات على PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="bfa58-136">لا تتطلب الوحدة النمطية المدرج التكراري للتقييمات أي تكوين.</span><span class="sxs-lookup"><span data-stu-id="bfa58-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="bfa58-137">عليك فقط إضافة الوحدة النمطية في قالب PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="bfa58-138">توضح الرسوم التوضيحية التالية كيف يبدو قالب PDP في Dynamics 365 Commerce عند تكوين الوحدات النمطية للتقييمات والمراجعات للعرض على PDPs.</span><span class="sxs-lookup"><span data-stu-id="bfa58-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="bfa58-139">![يتم تكوين قالب PDP عند التقييمات والمراجعات للعرض على PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="bfa58-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="bfa58-140">الوحدة النمطية لقائمه مراجعات المنتج</span><span class="sxs-lookup"><span data-stu-id="bfa58-140">Product reviews list module</span></span>

<span data-ttu-id="bfa58-141">تعرض الوحدة النمطية قائمة مراجعات المنتج قائمة بمراجعات المنتج مع خيارات الفرز والترشيح وترقيم الصفحات.</span><span class="sxs-lookup"><span data-stu-id="bfa58-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="bfa58-142">عادةً ما تظهر هذه الوحدة النمطية بعد الوحدة النمطية المدرج التكراري للتقييمات على PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="bfa58-143">يعرض الجدول التالي خصائص الوحدة النمطية قائمة مراجعات المنتج التي يجب تكوينها في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="bfa58-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="bfa58-144">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="bfa58-144">Property name</span></span>              | <span data-ttu-id="bfa58-145">القيمة</span><span class="sxs-lookup"><span data-stu-id="bfa58-145">Value</span></span> | <span data-ttu-id="bfa58-146">وصف الخاصية</span><span class="sxs-lookup"><span data-stu-id="bfa58-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="bfa58-147">تظهر المراجعات في كل صفحة</span><span class="sxs-lookup"><span data-stu-id="bfa58-147">Reviews shown on each page</span></span> | <span data-ttu-id="bfa58-148">10</span><span class="sxs-lookup"><span data-stu-id="bfa58-148">10</span></span>    | <span data-ttu-id="bfa58-149">عدد المراجعات التي يجب أن تظهر في وقت واحد على PDP.</span><span class="sxs-lookup"><span data-stu-id="bfa58-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="bfa58-150">يتم تضمين الزرين **التالي** و **السابق** ، بحيث يمكن للمستخدمين التنقل من خلال صفحات الاستعراضات.</span><span class="sxs-lookup"><span data-stu-id="bfa58-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="bfa58-151">المدرج التكراري للتقييمات -عرض ملخص</span><span class="sxs-lookup"><span data-stu-id="bfa58-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="bfa58-152">تشتمل الوحدة النمطية قائمة مراجعات المنتج على فتحة حيث يمكنك إضافة الوحدة النمطية مدرج تكراري للتقييمات.</span><span class="sxs-lookup"><span data-stu-id="bfa58-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="bfa58-153">يوضح الرسم التوضيحي التالي كيف يمكنك إضافة الوحدة النمطية مدرج تكراري للتقييمات في الوحدة النمطية قائمة مراجعات المنتج في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfa58-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![إضافة الوحدة النمطية مدرج تكراري للتقييمات في الوحدة النمطية قائمة مراجعات المنتج](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="bfa58-155">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bfa58-155">Additional resources</span></span>

[<span data-ttu-id="bfa58-156">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="bfa58-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bfa58-157">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="bfa58-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bfa58-158">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="bfa58-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bfa58-159">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="bfa58-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bfa58-160">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="bfa58-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bfa58-161">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="bfa58-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bfa58-162">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="bfa58-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]