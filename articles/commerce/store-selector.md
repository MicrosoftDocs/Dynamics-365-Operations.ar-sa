---
title: الوحدة النمطية لمحدد المتجر
description: يتناول هذا الموضوع وحدة محدّد المتجر ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378198"
---
# <a name="store-selector-module"></a><span data-ttu-id="abcd6-103">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="abcd6-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abcd6-104">يتناول هذا الموضوع وحدة محدّد المتجر ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="abcd6-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="abcd6-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="abcd6-105">Overview</span></span>

<span data-ttu-id="abcd6-106">يتم استخدام وحدة محدِّد المتجر لسيناريو العميل "الشراء عبر الإنترنت، الانتقاء في المتجر" "(BOPIS).</span><span class="sxs-lookup"><span data-stu-id="abcd6-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="abcd6-107">فهو يعرض قائمه بالمتاجر التي يكون فيها المنتج متوفرًا للالتقاط، وكذلك تخزين الساعات ومخزون المنتجات لكل متجر.</span><span class="sxs-lookup"><span data-stu-id="abcd6-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="abcd6-108">تتطلب وحدة محدد المخزن الحصول على سياق منتج وموقع بحث للعثور على المتاجر.</span><span class="sxs-lookup"><span data-stu-id="abcd6-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="abcd6-109">وفي حاله غياب أحد مواقع البحث، يتم تعيينه افتراضيا إلى موقع المستعرض الخاص بالعميل بشرط منح العميل الموافقة.</span><span class="sxs-lookup"><span data-stu-id="abcd6-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="abcd6-110">تحتوي الوحدة على مربع إدخال يسمح للعميل بإدخال موقع (الرمز البريدي أو مدينه أو ولاية) للعثور على المتاجر القريبة.</span><span class="sxs-lookup"><span data-stu-id="abcd6-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="abcd6-111">تتكامل وحدة محدد المتجر مع واجهة برمجة تطبيقات (API) للتشفير الجغرافي لخرائط Bing لتحويل الموقع الذي ادخله العميل إلى خط عرض وخط طول.</span><span class="sxs-lookup"><span data-stu-id="abcd6-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="abcd6-112">يلزم إدخال مفتاح API لخرائط Bing ويجب إضافته إلى صفحة المعلمات المشتركة للتجارة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="abcd6-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="abcd6-113">يمكن إضافة وحدة محدّد المتجر إلى وحدة مربع الشراء في صفحة تفاصيل المنتج (PDP) لعرض المتاجر التي يكون فيها المنتج متوفرًا للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="abcd6-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="abcd6-114">ويمكن إضافته أيضًا إلى وحدة سلة.</span><span class="sxs-lookup"><span data-stu-id="abcd6-114">It can also be added to a cart module.</span></span> <span data-ttu-id="abcd6-115">وعند إضافتها إلى وحدة السلة، تعرض وحدة محدد المتجر خيارات الانتقاء لكل صنف من بنود كل سلة.</span><span class="sxs-lookup"><span data-stu-id="abcd6-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="abcd6-116">بالإضافة إلى ذلك، مع الترميز المخصص يمكن إضافة هذه الوحدة إلى صفحات أو وحدات أخرى من خلال الملحقات والتخصيصات.</span><span class="sxs-lookup"><span data-stu-id="abcd6-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="abcd6-117">لكي يعمل سيناريو BOPIS، يجب تكوين المنتجات باستخدام وضع التسليم "الانتقاء الخاص بالعملاء".</span><span class="sxs-lookup"><span data-stu-id="abcd6-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="abcd6-118">وإلا، فلن تظهر الوحدة في الصفحات المعنية.</span><span class="sxs-lookup"><span data-stu-id="abcd6-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="abcd6-119">للحصول على تفاصيل حول كيفية تكوين وضع التسليم، راجع [إعداد أوضاع التسليم](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="abcd6-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="abcd6-120">تظهر الصورة التالية مثالاً على وحدة محدد المتجر المستخدمة في صفحة تفاصيل المنتج (PDP)</span><span class="sxs-lookup"><span data-stu-id="abcd6-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![مثال لوحدة محدِّد المتجر](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="abcd6-122">استخدام وحدة محدِّد المتجر في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="abcd6-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="abcd6-123">يمكن استخدام وحدة محدّد المتجر في وحدة تفاصيل المنتج (PDP) للبحث عن المتاجر القريبة التي يكون فيها المنتج متوفرًا للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="abcd6-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="abcd6-124">يمكن استخدام وحدة محدّد المتجر في صفحة سلة للبحث عن المتاجر القريبة التي يكون فيها المنتج الموجود في سلة متوفرًا للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="abcd6-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="abcd6-125">خصائص وحدة محدِّد المتجر</span><span class="sxs-lookup"><span data-stu-id="abcd6-125">Store selector module properties</span></span>

| <span data-ttu-id="abcd6-126">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="abcd6-126">Property name</span></span>             | <span data-ttu-id="abcd6-127">قيمة</span><span class="sxs-lookup"><span data-stu-id="abcd6-127">Value</span></span>                 | <span data-ttu-id="abcd6-128">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="abcd6-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="abcd6-129">نصف قطر البحث</span><span class="sxs-lookup"><span data-stu-id="abcd6-129">Search radius</span></span> | <span data-ttu-id="abcd6-130">رقم</span><span class="sxs-lookup"><span data-stu-id="abcd6-130">Number</span></span> | <span data-ttu-id="abcd6-131">تحديد نصف قطر البحث للمتاجر، بالأميال.</span><span class="sxs-lookup"><span data-stu-id="abcd6-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="abcd6-132">إذا لم يتم تحديد قيمة، يتم استخدام نصف قطر البحث الافتراضي، 50 ميلاً.</span><span class="sxs-lookup"><span data-stu-id="abcd6-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="abcd6-133">شروط الخدمة</span><span class="sxs-lookup"><span data-stu-id="abcd6-133">Terms of Service</span></span> | <span data-ttu-id="abcd6-134">URL</span><span class="sxs-lookup"><span data-stu-id="abcd6-134">URL</span></span>    |  <span data-ttu-id="abcd6-135">عنوان URL لشروط الخدمة المطلوب لخدمة خرائط Bing.</span><span class="sxs-lookup"><span data-stu-id="abcd6-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="abcd6-136">إضافة وحدة محدِّد متجر إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="abcd6-136">Add a store selector module to a page</span></span>

<span data-ttu-id="abcd6-137">تحتاج وحدة محدِّد المتجر إلى سياق منتج، لذا يمكن استخدامه فقط داخل مربع الشراء ووحدات السلال.</span><span class="sxs-lookup"><span data-stu-id="abcd6-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="abcd6-138">لا تعمل وحدات محدد المتجر خارج هذه الوحدات.</span><span class="sxs-lookup"><span data-stu-id="abcd6-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="abcd6-139">للحصول على معلومات حول كيفية إضافة وحدة محدِّد المتجر إلى وحدة مربع شراء، راجع [وحدة مربع الشراء](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="abcd6-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="abcd6-140">للحصول على معلومات حول كيفية إضافة وحدة محدِّد المتجر إلى وحدة السلة، راجع [وحدة السلة](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="abcd6-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abcd6-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="abcd6-141">Additional resources</span></span>

[<span data-ttu-id="abcd6-142">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="abcd6-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="abcd6-143">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="abcd6-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="abcd6-144">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="abcd6-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="abcd6-145">جولة سريعة في صفحة تفاصيل المنتج (PDP)</span><span class="sxs-lookup"><span data-stu-id="abcd6-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="abcd6-146">جولة سريعة في السلة والسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="abcd6-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="abcd6-147">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="abcd6-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="abcd6-148">إدارة خرائط Bing لمؤسستك</span><span class="sxs-lookup"><span data-stu-id="abcd6-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
