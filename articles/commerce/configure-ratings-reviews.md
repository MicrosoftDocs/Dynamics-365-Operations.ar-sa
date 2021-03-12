---
title: تكوين التقييمات والمراجعات
description: يوضح هذا الموضوع كيفية تكوين موقع التجارة الإلكترونية لإظهار تصنيفات العملاء ومراجعاتها في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fcdf571378c25d71b3ef4f3baad062a25390417
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993540"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="f0dd7-103">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f0dd7-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f0dd7-104">يوضح هذا الموضوع كيفية تكوين موقع التجارة الإلكترونية لإظهار تصنيفات العملاء ومراجعاتها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f0dd7-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="f0dd7-105">Overview</span></span>

<span data-ttu-id="f0dd7-106">تساعد التقييمات والمراجعات على مواقع التجارة الإلكترونية العملاء على التعرف على المنتجات قبل اتخاذ قرار الشراء وذلك من خلال إظهار ما يفكر فيه العملاء الآخرون بشأن هذه المنتجات.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="f0dd7-107">بالنسبة لمواقع التجارة الإلكترونية، تعد التصنيفات والمراجعات أيضًا آلية لجمع تعليقات العملاء حول المنتجات.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="f0dd7-108">تكوين موقع لإظهار التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f0dd7-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="f0dd7-109">يتم تكوين قيم التكوين الخاصة بالتقييمات والمراجعات، مثل معرف المستأجر وطول نص المراجعة وطول عنوان المراجعة، على مستوى الموقع.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="f0dd7-110">لتكوين موقع لإظهار التقييمات والمراجعات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="f0dd7-111">الانتقال **إلى الصفحة الرئيسية \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="f0dd7-112">حدد اسم موقعك.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="f0dd7-113">انتقل إلى **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="f0dd7-114">في الحقل **أقصى طول لنص المراجعة**، أدخل الحد الأقصى لعدد الأحرف التي يمكن أن يشتمل عليها نص المراجعة (على سبيل المثال، **1000**).</span><span class="sxs-lookup"><span data-stu-id="f0dd7-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="f0dd7-115">في الحقل **أقصى طول لعنوان المراجعة**، أدخل الحد الأقصى لعدد الأحرف التي يمكن أن يشتمل عليها عناوين المراجعة (على سبيل المثال، **55**).</span><span class="sxs-lookup"><span data-stu-id="f0dd7-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="f0dd7-116">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="f0dd7-117">يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![تكوين موقع لإظهار التقييمات والمراجعات](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="f0dd7-119">ربط تقييم المنتج بقسم المراجعات في PDP</span><span class="sxs-lookup"><span data-stu-id="f0dd7-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="f0dd7-120">يتم عرض تقييم المنتج أسفل عنوان المنتج أعلى PDP.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="f0dd7-121">يمكن تكوين تصنيف المنتج بحيث يكون مرتبطًا بقسم **المراجعات** لنفس PDP.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="f0dd7-122">لربط تقييم منتج بقسم **المراجعات** لـ PDP، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="f0dd7-123">افتح قالب PDP.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="f0dd7-124">انتقل إلى **إعدادات الوحدة النمطية لحاوية مربع الشراء**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="f0dd7-125">تحت **مربع الشراء**، حدد **تقييمات المنتج**، ثم حدد خانه الاختيار **ربط النقر بالوحدة النمطية للمراجعات الكاملة** .</span><span class="sxs-lookup"><span data-stu-id="f0dd7-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="f0dd7-126">يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![ربط تقييم المنتج بقسم المراجعات في PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="f0dd7-128">تكوين ارتباط صفحة الخصوصية والسياسة</span><span class="sxs-lookup"><span data-stu-id="f0dd7-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="f0dd7-129">لتكوين ارتباط صفحة الخصوصية والسياسة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="f0dd7-130">الانتقال **إلى الصفحة الرئيسية \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="f0dd7-131">حدد اسم موقعك.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="f0dd7-132">انتقل إلى **إعدادات الموقع \> الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="f0dd7-133">في علامة التبويب **المسارات** ، وتحت **خصوصية وسياسة RNR**، حدد **إضافة ارتباط**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="f0dd7-134">إذا تم إدخال ارتباط بالفعل وتريد استبداله، فحدد الارتباط.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="f0dd7-135">في مربع الحوار **إضافة ارتباط** ،حدد ارتباط صفحة الخصوصية والسياسة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="f0dd7-136">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="f0dd7-137">يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0dd7-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![تكوين ارتباط صفحة الخصوصية والسياسة](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="f0dd7-139">تكوين الوحدات النمطية للتصنيفات والمراجعات في صفحات تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="f0dd7-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="f0dd7-140">للحصول على معلومات حول تكوين الوحدات النمطية للتصنيفات والمراجعات على صفحات تفاصيل المنتج، راجع [الوحدات النمطية للتصنيفات والمراجعات](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd7-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0dd7-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f0dd7-141">Additional resources</span></span>

[<span data-ttu-id="f0dd7-142">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f0dd7-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f0dd7-143">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f0dd7-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f0dd7-144">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f0dd7-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="f0dd7-145">تكوين الوحدات النمطية للتصنيفات والمراجعات في صفحات تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="f0dd7-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="f0dd7-146">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="f0dd7-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
