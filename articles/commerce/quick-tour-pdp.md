---
title: نظرة عامة على صفحات تفاصيل المنتج
description: يقدم هذا الموضوع نظرة عامة حول صفحات تفاصيل المنتجات (PDP) في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792209"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="ad331-103">نظرة عامة على صفحات تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="ad331-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad331-104">يقدم هذا الموضوع نظرة عامة حول صفحات تفاصيل المنتجات (PDP) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad331-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ad331-105">يقدم الملف بتنسيق PDP معلومات مفصلة عن منتج ويُتيح للعملاء تحديد خيارات المنتج مثل الحجم والنمط واللون.</span><span class="sxs-lookup"><span data-stu-id="ad331-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="ad331-106">يجب أن يعمل ملف بتنسيق PDP على إظهار كافة معلومات المنتج التي يطلبها العميل لاتخاذ قرار شراء.</span><span class="sxs-lookup"><span data-stu-id="ad331-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="ad331-107">يبين الرسم التوضيحي التالي مثالاً على تنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="ad331-107">The following illustration shows an example of a PDP.</span></span>

![مثال على صفحة تفاصيل المنتج](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="ad331-109">الوحدات النمطية للرأس والتذييل</span><span class="sxs-lookup"><span data-stu-id="ad331-109">Header and footer modules</span></span>

<span data-ttu-id="ad331-110">يحتوي ملف بتنسيق PDF على رأس يعرض كافة فئات المنتجات والصفحات الأخرى التي يرغب بائع التجزئة في أن يقوم العملاء باستعراضها.</span><span class="sxs-lookup"><span data-stu-id="ad331-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="ad331-111">يوجد أسفل الصفحة تذييل يحتوي على ارتباطات سريعة إلى العديد من الموضوعات التي قد تهم العملاء.</span><span class="sxs-lookup"><span data-stu-id="ad331-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="ad331-112">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="ad331-112">Buy box module</span></span>

<span data-ttu-id="ad331-113">الوحدة النمطية الهامه علي PDP هي الوحدة النمطية لمربع الشراء ، والتي تظهر كاول عنصر في الجزء الرئيسي من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad331-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="ad331-114">تعرض الوحدة النمطية لصندوق الشراء معلومات هامه حول المنتج ، مثل اسم المنتج ووصف المنتج وسعر المنتج وصور المنتجات وتصنيفات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ad331-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="ad331-115">تتيح الوحدة النمطية لمربع الشراء للعميل تحديد خيارات المنتج (على سبيل المثال، الحجم والنمط واللون) وإضافة المنتج إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="ad331-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="ad331-116">كما تتيح للعميل كذلك شراء المنتج عبر الإنترنت واختياره في أحد المتاجر.</span><span class="sxs-lookup"><span data-stu-id="ad331-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="ad331-117">تستخدم الوحدة النمطية للشراء عبر الإنترنت والانتقاء في المتجر التكامل مع واجهات برمجة التطبيقات (واجهات API) الخاصة بخرائط Bing للعثور على المتاجر القريبة أو المتاجر في موقع آخر يقوم العميل بتحديده.</span><span class="sxs-lookup"><span data-stu-id="ad331-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="ad331-118">تتطلب الوحدة النمطية لمربع الشراء معرف منتج.</span><span class="sxs-lookup"><span data-stu-id="ad331-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="ad331-119">يتم اشتقاق هذا المعرف من سياق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad331-119">This ID is derived from the page context.</span></span> <span data-ttu-id="ad331-120">إذا تمت إضافة الوحدة النمطية لمربع شراء إلى سياق صفحة لا تتضمن سياق الصفحة معرف منتج، فلن يعرض المعلومات بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="ad331-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="ad331-121">الوحدة النمطية لمواصفات المنتج</span><span class="sxs-lookup"><span data-stu-id="ad331-121">Product specifications module</span></span>

<span data-ttu-id="ad331-122">يمكن استخدام الوحدة النمطية لمواصفات المنتج لإظهار تفاصيل إضافية حول المنتج.</span><span class="sxs-lookup"><span data-stu-id="ad331-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="ad331-123">ويتم أخذ هذه التفاصيل من سمات المنتج في Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad331-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="ad331-124">تعرض الوحدة النمطية لمواصفات المنتج كل سمة حيث يتم تعيين الخاصية **مرئي** على **صواب**.</span><span class="sxs-lookup"><span data-stu-id="ad331-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="ad331-125">وتتطلب معرف المنتج لاسترداد سمات المنتج.</span><span class="sxs-lookup"><span data-stu-id="ad331-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="ad331-126">الوحدة النمطية للتوصيات</span><span class="sxs-lookup"><span data-stu-id="ad331-126">Recommendations module</span></span>

<span data-ttu-id="ad331-127">إن الوحدة النمطية للتوصيات هي وحدة نمطية مهمة في ملف بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="ad331-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="ad331-128">بينما يقوم العملاء باستعراض المنتجات، يجب تقديم المزيد من خيارات المنتج، حتى يتمكنوا من العثور على المنتج الصحيح والقيام بعملية شراء.</span><span class="sxs-lookup"><span data-stu-id="ad331-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="ad331-129">تساعد التوصيات العملاء في اكتشاف المحتوى المرتبط ومتابعه التسوق بسهولة.</span><span class="sxs-lookup"><span data-stu-id="ad331-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="ad331-130">تتوفر أنواع مختلفة من قوائم التوصيات:</span><span class="sxs-lookup"><span data-stu-id="ad331-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="ad331-131">تستند قائمة **الأشخاص معجبون بهم أيضًا** إلى التعلم الآلي.</span><span class="sxs-lookup"><span data-stu-id="ad331-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="ad331-132">ويستخدم سجل الحركات الخاص بالعملاء الآخرين لتقديم توصيات.</span><span class="sxs-lookup"><span data-stu-id="ad331-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="ad331-133">يتم إنشاء هذه القائمة بواسطة خدمة التوصيات وتشبه قائمة "العملاء الذين اشتروا هذا قاموا أيضًا بشراء...".</span><span class="sxs-lookup"><span data-stu-id="ad331-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="ad331-134">معرف المنتج مطلوب لإنشاء هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="ad331-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="ad331-135">يمكن تكوين قائمة **مرتبطة** لمنتج في Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad331-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="ad331-136">على سبيل المثال، بالنسبة لحقيبة اليد بنية اللون للسفر، يمكن تكوين المزيد من حقائب اليد المصنعة من الجلد أو المصممة لأغراض السفر للقائمة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="ad331-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="ad331-137">يمكن أيضًا تكوين أنواع أخرى من القوائم المرتبطة، مثل **الإكسسوارات** و **الكثير مثل هذا** في Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad331-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="ad331-138">معرف المنتج مطلوب لإنشاء هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="ad331-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="ad331-139">ولذلك، إذا تمت اضافتها إلى صفحة رئيسية، حيث لا يتضمن سياق الصفحة معرف منتج، ستكون القائمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="ad331-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="ad331-140">يمكن استخدام قوائم التوصيات التي تم إنشائها حسابيًا، مثل **التداول** و **الأفضل مبيعًا** و **جديد** على ملفات بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="ad331-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="ad331-141">على الرغم من أن هذه القوائم قد لا ترتبط مباشرة بالمنتج على ملف بتنسيق PDF، إلا أنها طريقة أخرى لمساعدة العملاء في العثور على المنتجات التي قد تهمهم.</span><span class="sxs-lookup"><span data-stu-id="ad331-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="ad331-142">لا تتطلب أنواع القوائم هذه وجود معرف منتج.</span><span class="sxs-lookup"><span data-stu-id="ad331-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="ad331-143">وهي عبارة عن قوائم عامة يتم إنشاؤها استنادًا إلى أنماط التسوق عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="ad331-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="ad331-144">تُعد القوائم التحريرية قوائم مُختارة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ad331-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="ad331-145">على سبيل المثال، قد يقرر بائع التجزئة اختيار قوائم المنتجات التي يريد إظهارها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ad331-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="ad331-146">وحدات التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="ad331-146">Ratings and reviews modules</span></span>

<span data-ttu-id="ad331-147">يمكن استخدام ثلاثه وحدات لإظهار المراجعات وإضافتها:</span><span class="sxs-lookup"><span data-stu-id="ad331-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="ad331-148">**المراجعات** – تسرد الوحدات التقييمات والمراجعات على عرض التصنيفات والمراجعات التي قام العملاء الآخرين بتقديمها.</span><span class="sxs-lookup"><span data-stu-id="ad331-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="ad331-149">يمكن للعملاء فرز المراجعات وتصفيتها.</span><span class="sxs-lookup"><span data-stu-id="ad331-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="ad331-150">تتيح لك هذه الوحدة إبداء الإعجاب أو عدم الإعجاب بالمراجعات والإبلاغ عن المشكلات.</span><span class="sxs-lookup"><span data-stu-id="ad331-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="ad331-151">**كتابة المراجعة** – تتيح هذه الوحدة النمطية للعملاء ان يقوموا بكتابه المراجعات الخاصة بهم لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ad331-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="ad331-152">**رسم بياني التقييمات** - تتضمن هذه الوحدة رسمًا بيانيًا يبين اتجاه التقييمات لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="ad331-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="ad331-153">للحصول على مزيد من التفاصيل، راجع [نظرة عامة حول التصنيفات والمراجعات](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ad331-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="ad331-154">الوحدة النمطية للتسويق</span><span class="sxs-lookup"><span data-stu-id="ad331-154">Marketing modules</span></span>

<span data-ttu-id="ad331-155">إذا كان محتوى التسويق فريدًا لمنتج معين، فإنه يمكن إضافة أية وحدة نمطية للتسويق إلى الملف بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="ad331-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="ad331-156">يمكنك إضافة الوحدات النمطية للتسويق إلى ملف بتنسيق PDF عن طريق "إثراء" الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad331-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="ad331-157">لمزيد من التفاصيل، راجع [صفحة إثراء منتج](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="ad331-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad331-158">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ad331-158">Additional resources</span></span>

[<span data-ttu-id="ad331-159">نظرة عامة على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="ad331-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="ad331-160">نظرة عامة على صفحات سلة التسوق والسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="ad331-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="ad331-161">نظرة عامة على صفحات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="ad331-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="ad331-162">صفحة إثراء تفاصيل منتج</span><span class="sxs-lookup"><span data-stu-id="ad331-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
