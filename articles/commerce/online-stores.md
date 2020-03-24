---
title: إعداد قناة متجر عبر الإنترنت
description: توفر هذه المقالة معلومات حول قنوات المتاجر عبر الإنترنت وكيفية إعدادها في Dynamics 365 Commerce.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096884"
---
# <a name="set-up-an-online-store-channel"></a><span data-ttu-id="4936b-103">إعداد قناة متجر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="4936b-103">Set up an online store channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4936b-104">توفر هذه المقالة معلومات حول قنوات المتاجر عبر الإنترنت وكيفية إعدادها في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4936b-104">This article provides information about online store channels and how to set them up in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4936b-105">يدعم تطبيق Commerce قنوات بيع بالتجزئة متعددة.</span><span class="sxs-lookup"><span data-stu-id="4936b-105">Commerce supports multiple retail channels.</span></span> <span data-ttu-id="4936b-106">وتتضمن هذه القنوات المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية).</span><span class="sxs-lookup"><span data-stu-id="4936b-106">These channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="4936b-107">وتمنح المتاجر على الإنترنت وجودًا على الإنترنت لتاجر البيع بالتجزئة ليتمكن العملاء من شراء المنتجات من متجره على الإنترنت بالإضافة إلى متاجره للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="4936b-107">Online stores give an online presence to a retailer, so that customers can purchase products from the retailer's online store in addition to its retail stores.</span></span> <span data-ttu-id="4936b-108">وفي حالة قيام العملاء بشراء المنتجات من المتجر على الإنترنت، فإنه يمكن شحن تلك المنتجات إليهم، أو يستطيع العملاء اختيار المنتجات من المتجر المحلي.</span><span class="sxs-lookup"><span data-stu-id="4936b-108">If customers purchase products from the online store, those products can be shipped to them, or the customers can pick the products up at a local store.</span></span> 

<span data-ttu-id="4936b-109">تنشئ متجرًا عبر الإنترنت في عميل Commerce.</span><span class="sxs-lookup"><span data-stu-id="4936b-109">You create an online store in the Commerce client.</span></span> <span data-ttu-id="4936b-110">ويتم فيما بعد نشر هذا المتجر عبر الإنترنت إلى متجر عبر الإنترنت تابع لطرف ثالث يتكامل مع Commerce.</span><span class="sxs-lookup"><span data-stu-id="4936b-110">This online store is then published to a third-party online store that is integrated with Commerce.</span></span> <span data-ttu-id="4936b-111">ويقوم المتجر على الإنترنت لطرف ثالث بدور الواجهة (UI) للمتجر على الإنترنت، ويتيح لك اختيار نظام إدارة العملاء (CMS) وقدرات واجهة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4936b-111">The third-party online store serves as the storefront (UI) for the online store, and gives you a choice of customer management system (CMS) and UI capabilities.</span></span> <span data-ttu-id="4936b-112">تتوفر عدة عمليات دمج من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="4936b-112">Several integrations of this type are available.</span></span> 

<span data-ttu-id="4936b-113">تتحكم الخصائص التي تحددها للمتجر عبر الإنترنت في سلوك هذا المتجر بعد نشره.</span><span class="sxs-lookup"><span data-stu-id="4936b-113">The properties that you define for the online store control the behavior of the online store.</span></span> <span data-ttu-id="4936b-114">على سبيل المثال، يمكنك تحديد التدرج الهرمي لفئة التنقل وتعيينه للمتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-114">For example, you define the navigation category hierarchy and assign it to the online store.</span></span> <span data-ttu-id="4936b-115">وعندما تقوم بنشر المتجر على الإنترنت إلى المتجر على الإنترنت لطرف ثالث، يتم عرض التدرج الهرمي للتنقل في النسخة الإلكترونية من المتجر.</span><span class="sxs-lookup"><span data-stu-id="4936b-115">When you publish the online store to the third-party online store, the navigation category hierarchy appears in the online version of the store.</span></span> <span data-ttu-id="4936b-116">ويستخدم المتسوقون فيما بعد التسلسل الهرمي لفئة التنقل لاستعراض المتجر على الإنترنت والبحث عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="4936b-116">Shoppers then use the navigation category hierarchy to browse the online store and search for products.</span></span> 

<span data-ttu-id="4936b-117">ولإنشاء مخزن عبر الإنترنت، يجب إعداد المكونات التي تتيح معالجة الحركات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="4936b-117">To create an online store, you must set up the components that enable transactions to be processed for the store.</span></span> <span data-ttu-id="4936b-118">على سبيل المثال، يجب إضافة عمليات الفرز وتطبيق السمات وإعداد طرق الدفع وطرق الشحن.</span><span class="sxs-lookup"><span data-stu-id="4936b-118">For example, you must add assortments, apply attributes, and set up payment methods and shipping methods.</span></span> <span data-ttu-id="4936b-119">يمكنك أيضًا تعريف الأسعار والعروض والخصومات والاتفاقيات التجارية وشروط الشحن الخاصة بالمخزن عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-119">You can also define prices, promotions, discounts, trade agreements, and shipping terms that are specific to the online store.</span></span> 

<span data-ttu-id="4936b-120">وبعد نشر المتجر على الإنترنت للمتجر على الإنترنت لطرف ثالث، يمكنك إنشاء كتالوجات المنتجات للمتجر الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="4936b-120">After you publish the online store to the third-party online store, you can create product catalogs for the online store.</span></span> <span data-ttu-id="4936b-121">المنتجات في الكتالوج تصبح قوائم المنتجات في المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-121">The products in the catalog become product listings in the online store.</span></span> <span data-ttu-id="4936b-122">عند شراء المتسوقين للمنتجات من متجر عبر الإنترنت، يتم تحديثه ومزامنة المخزون المتوفر في العميل.</span><span class="sxs-lookup"><span data-stu-id="4936b-122">When a shopper purchases products from the online store, the available inventory is updated and synchronized in the client.</span></span> <span data-ttu-id="4936b-123">بالإضافة غلى ذلك،  يتم إنشاء أوامر التوريد للمشتريات وإرسالها إلى العميل لتلبية ومعالجة الطلبات.</span><span class="sxs-lookup"><span data-stu-id="4936b-123">Additionally, sales orders are generated for the purchases, and are sent to the client for order fulfillment and processing.</span></span>

## <a name="set-up-an-online-store"></a><span data-ttu-id="4936b-124">إعداد متجر على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="4936b-124">Set up an online store</span></span>

<span data-ttu-id="4936b-125">ولإعداد متجر على الإنترنت، يجب عليك إكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="4936b-125">To set up an online store, you must complete the following tasks.</span></span>

1. <span data-ttu-id="4936b-126">قم إنشاء متجر جديد على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="4936b-126">Create the online store.</span></span>
2. <span data-ttu-id="4936b-127">قم بإضافة المتجر الإلكتروني إلى التدرجات الهرمية المناسبة للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="4936b-127">Add the online store to the appropriate organization hierarchies.</span></span>
3. <span data-ttu-id="4936b-128">أضف عمليات فرز التي تشمل المنتجات المتوفرة في المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-128">Add assortments that include the products that are available in the online store.</span></span>
4. <span data-ttu-id="4936b-129">قم بتعيين أو إنشاء مجموعات سعر للمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-129">Assign or create price groups for the online store.</span></span>
5. <span data-ttu-id="4936b-130">قم بإعداد أوضاع التسليم المتوفرة للمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-130">Set up the modes of delivery that are available for the online store.</span></span>
6. <span data-ttu-id="4936b-131">قم بتعيين طرق الدفع التي تم قبولها للمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-131">Assign the payment methods that are accepted by the online store.</span></span>
7. <span data-ttu-id="4936b-132">إذا سمحت للمتسوقين بطلب المنتجات عبر الإنترنت ثم اختيارها من متجر محلي، قم بتعيين مجموعات محدد موقع المتجر للمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-132">If you allow shoppers to order products online and then pick them up at a local store, assign store locator groups to the online store.</span></span>
8. <span data-ttu-id="4936b-133">قم بتعيين سمات لأوامر المبيعات والمنتجات والقنوات للمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-133">Assign attributes for channels, products, and sales orders to the online store.</span></span> <span data-ttu-id="4936b-134">تطبق سمات القناة إلى المتجر بأكمله، وتطبق سمات المنتج للمنتجات التي يتم عرضها في المتجر على الإنترنت، وتطبق سمات أمر المبيعات لأوامر المبيعات التي تم إنشاؤها من المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-134">Channel attributes apply to the whole online store, product attributes apply to the products that are offered in the online store, and sales order attributes apply to the sales orders that are generated from the online store.</span></span>
9. <span data-ttu-id="4936b-135">قم بتعيين سمات لتعيين الخصائص التي تحدد سلوك السمات في المتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-135">Map attributes to define the properties that determine how those attributes behave in the online store.</span></span> <span data-ttu-id="4936b-136">على سبيل المثال، يمكنك تحديد السمات بحيث تكون مطلوبة أو قابلة للبحث.</span><span class="sxs-lookup"><span data-stu-id="4936b-136">For example, attributes can be defined as required or searchable.</span></span>
10. <span data-ttu-id="4936b-137">انشر هذا المتجر لإنشاء بنية المتجر في اختيارك للمتجر على الإنترنت لطرف ثالث.</span><span class="sxs-lookup"><span data-stu-id="4936b-137">Publish the online store to generate the store structure on your choice of third-party online store.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4936b-138">قبل نشر المتجر على الإنترنت، يجب إعداد موقع توزيع لهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="4936b-138">Before you publish the online store, you must set up a distribution location for it.</span></span>

## <a name="commerce-channel-navigation-hierarchies"></a><span data-ttu-id="4936b-139">التدرجات الهرمية للتنقل في قناة Commerce</span><span class="sxs-lookup"><span data-stu-id="4936b-139">Commerce channel navigation hierarchies</span></span>

<span data-ttu-id="4936b-140">قبل أن تتمكن من إنشاء متجر على الإنترنت، يجب عليك تعريف التدرج الهرمي للتنقل لقناة التجارة الذي تريد استخدامه في المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-140">Before you create an online store, you must define the commerce channel navigation hierarchy that you want to use for it.</span></span> <span data-ttu-id="4936b-141">يمثل التسلسل الهرمي لتنقل القنوات التدرج الهرمي للفئات التي يتم عرضها في المتجر على الإنترنت بعد نشر المتجر.</span><span class="sxs-lookup"><span data-stu-id="4936b-141">The channel navigation hierarchy represents the category hierarchy that is displayed in the online store after the store is published.</span></span> <span data-ttu-id="4936b-142">عند نشر كتالوجات المنتجات في المتجر على الإنترنت، يتم تعيين المنتجات في الكتالوج لفئات في التسلسل الهرمي لتنقل القنوات.</span><span class="sxs-lookup"><span data-stu-id="4936b-142">When you publish product catalogs to the online store, the products in the catalog are mapped to the categories in the channel navigation hierarchy.</span></span> <span data-ttu-id="4936b-143">ويستخدم المتسوقون فيما بعد التدرج الهرمي للتنقل في المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-143">Shoppers then use the hierarchy to navigate in the online store.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="4936b-144">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="4936b-144">Organization hierarchies</span></span>

<span data-ttu-id="4936b-145">يتم استخدام التدرجات الهرمية للمؤسسات لهيكلة قنوات التجارة ولتمثيل العلاقات بين المؤسسات التي تتألف منها أعمالك.</span><span class="sxs-lookup"><span data-stu-id="4936b-145">Organization hierarchies are used to structure commerce channels and to represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="4936b-146">عند إعداد المتاجر الإلكترونية، يمكنك إضافتها إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="4936b-146">When you set up online stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="4936b-147">وقتئذٍ تتشارك المتاجر البيانات المستخدمة لعمليات الفرز، والتزويد، وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="4936b-147">The stores then share the data that is used for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="4936b-148">عندما تقوم بإنشاء تدرج هرمي للمؤسسات، تقوم بتعيين غرض منه.</span><span class="sxs-lookup"><span data-stu-id="4936b-148">When you create an organization hierarchy, you assign a purpose to it.</span></span> <span data-ttu-id="4936b-149">يشير الغرض إلى كيفية استخدام التدرج الهرمي في بنية الأعمال.</span><span class="sxs-lookup"><span data-stu-id="4936b-149">The purpose indicates how the hierarchy is used in the business structure.</span></span> <span data-ttu-id="4936b-150">يمكنك إنشاء تدرج هرمي واحد للمؤسسات لعمليات المتجر الخاص بك، واستخدام هذا التدرج الهرمي لعمليات الفرز والتزويد وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="4936b-150">You can create one organization hierarchy for your store operations, and use that hierarchy for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="4936b-151">‏‫وكبديل لذلك، يمكنك إنشاء تدرج هرمي للمؤسسات منفصل لكل غرض.</span><span class="sxs-lookup"><span data-stu-id="4936b-151">Alternatively, you can create a separate organization hierarchy for each purpose.</span></span> <span data-ttu-id="4936b-152">يمكنك أيضًا إنشاء تدرجات هرمية متعددة لنفس الغرض وتعيين قناة لكل منهم.</span><span class="sxs-lookup"><span data-stu-id="4936b-152">You can also create multiple hierarchies that have the same purpose, and assign a separate channel to each one.</span></span> <span data-ttu-id="4936b-153">إذا كنت تنوي نشر كتالوجات المنتجات على المتجر على الإنترنت، يجب عليك، كحد أدنى، إضافة المتاجر على الإنترنت لتدرج هرمي تنظيمي لعمليات الفرز.</span><span class="sxs-lookup"><span data-stu-id="4936b-153">If you plan to publish product catalogs to the online store, you should, at a minimum, add the online store to an organization hierarchy for assortments.</span></span> <span data-ttu-id="4936b-154">يتم تحديد المنتجات في الكتالوج من تشكيلات منتجات يتم تعيينها إلى المتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-154">The products in a catalog are selected from the assortments that are assigned to the online store.</span></span> <span data-ttu-id="4936b-155">عند نشر الكتالوج، عملية النشر تقارن تواريخ السريان للفرز الذي تم تعيينه للمتجر على الإنترنت باستخدام المنتجات المتضمنة في الكتالوج لتحديد المنتجات التي تتوفر في المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4936b-155">When the catalog is published, the publishing process compares the effective dates for the assortment that is assigned to the online store with the products that are included in the catalog to determine which products to make available in the online store.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4936b-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4936b-156">Additional resources</span></span>

[<span data-ttu-id="4936b-157">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="4936b-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4936b-158">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="4936b-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4936b-159">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="4936b-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4936b-160">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="4936b-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4936b-161">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="4936b-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4936b-162">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="4936b-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4936b-163">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="4936b-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4936b-164">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="4936b-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4936b-165">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="4936b-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4936b-166">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="4936b-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4936b-167">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="4936b-167">Enable location-based store detection</span></span>](enable-store-detection.md)
