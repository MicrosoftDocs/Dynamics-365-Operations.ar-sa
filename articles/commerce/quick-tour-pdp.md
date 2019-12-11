---
title: نظرة عامة حول صفحات تفاصيل المنتج
description: يقدم هذا الموضوع نظرة عامة حول صفحات تفاصيل المنتجات (بتنسيق PDP) في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697855"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="6b382-103">نظرة عامة حول صفحات تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="6b382-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6b382-104">يقدم هذا الموضوع نظرة عامة حول صفحات تفاصيل المنتجات (بتنسيق PDP) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6b382-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6b382-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6b382-105">Overview</span></span>

<span data-ttu-id="6b382-106">يقدم الملف بتنسيق PDP معلومات مفصلة عن منتج ويُتيح للعملاء تحديد خيارات المنتج مثل الحجم والنمط واللون.</span><span class="sxs-lookup"><span data-stu-id="6b382-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="6b382-107">يجب أن يعمل ملف بتنسيق PDP على إظهار كافة معلومات المنتج التي يطلبها العميل لاتخاذ قرار شراء.</span><span class="sxs-lookup"><span data-stu-id="6b382-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="6b382-108">يبين الرسم التوضيحي التالي مثالاً على تنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="6b382-108">The following illustration shows an example of a PDP.</span></span>

![مثال على صفحة تفاصيل المنتج](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="6b382-110">الوحدات النمطية للرأس والتذييل</span><span class="sxs-lookup"><span data-stu-id="6b382-110">Header and footer modules</span></span>

<span data-ttu-id="6b382-111">يحتوي ملف بتنسيق PDF على رأس يعرض كافة فئات المنتجات والصفحات الأخرى التي يرغب بائع التجزئة في أن يقوم العملاء باستعراضها.</span><span class="sxs-lookup"><span data-stu-id="6b382-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="6b382-112">يوجد أسفل الصفحة تذييل يحتوي على ارتباطات سريعة إلى العديد من الموضوعات التي قد تهم العملاء.</span><span class="sxs-lookup"><span data-stu-id="6b382-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="6b382-113">وحدة مربع شراء</span><span class="sxs-lookup"><span data-stu-id="6b382-113">Buy box module</span></span>

<span data-ttu-id="6b382-114">إن الوحدة النمطية الأكثر أهمية في ملف بتنسيق PDF هو وحدة نمطية لمربع شراء.</span><span class="sxs-lookup"><span data-stu-id="6b382-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="6b382-115">وبالتالي، تكون العنصر الأول في القسم الرئيسي من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6b382-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="6b382-116">تُعد الوحدة النمطية لمربع الشراء وحدة حاوية نمطية تستضيف العديد من الوحدات النمطية التي تحتوي على المعلومات الأكثر أهمية المتعلقة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="6b382-117">تتضمن هذه المعلومات اسم المنتج وصور المنتجات والوصف والسعر وتصنيفات المنتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="6b382-118">تتيح الوحدة النمطية لمربع الشراء للعميل تحديد خيارات المنتج (على سبيل المثال، الحجم والنمط واللون) وإضافة المنتج إلى سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="6b382-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="6b382-119">كما تتيح للعميل كذلك شراء المنتج عبر الإنترنت واختياره في أحد المتاجر.</span><span class="sxs-lookup"><span data-stu-id="6b382-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="6b382-120">تستخدم الوحدة النمطية للشراء عبر الإنترنت والانتقاء في المتجر التكامل مع واجهات برمجة التطبيقات (واجهات API) الخاصة بخرائط Bing للعثور على المتاجر القريبة أو المتاجر في موقع آخر يقوم العميل بتحديده.</span><span class="sxs-lookup"><span data-stu-id="6b382-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="6b382-121">تتطلب الوحدة النمطية لمربع الشراء معرف منتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="6b382-122">يتم اشتقاق هذا المعرف من سياق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6b382-122">This ID is derived from the page context.</span></span> <span data-ttu-id="6b382-123">إذا تمت إضافة الوحدة النمطية لمربع شراء إلى سياق صفحة لا تتضمن سياق الصفحة معرف منتج، فلن يعرض المعلومات بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="6b382-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="6b382-124">الوحدة النمطية لمواصفات المنتج</span><span class="sxs-lookup"><span data-stu-id="6b382-124">Product specifications module</span></span>

<span data-ttu-id="6b382-125">يمكن استخدام الوحدة النمطية لمواصفات المنتج لإظهار تفاصيل إضافية حول المنتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="6b382-126">ويتم أخذ هذه التفاصيل من سمات المنتج في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="6b382-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="6b382-127">تعرض الوحدة النمطية لمواصفات المنتج كل سمة حيث يتم تعيين الخاصية **مرئي** على **صواب**.</span><span class="sxs-lookup"><span data-stu-id="6b382-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="6b382-128">وتتطلب معرف المنتج لاسترداد سمات المنتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="6b382-129">الوحدة النمطية للتوصيات</span><span class="sxs-lookup"><span data-stu-id="6b382-129">Recommendations module</span></span>

<span data-ttu-id="6b382-130">إن الوحدة النمطية للتوصيات هي وحدة نمطية مهمة في ملف بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="6b382-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="6b382-131">بينما يقوم العملاء باستعراض المنتجات، يجب تقديم المزيد من خيارات المنتج، حتى يتمكنوا من العثور على المنتج الصحيح والقيام بعملية شراء.</span><span class="sxs-lookup"><span data-stu-id="6b382-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="6b382-132">تساعد التوصيات العملاء في اكتشاف المحتوى المرتبط ومتابعه التسوق بسهولة.</span><span class="sxs-lookup"><span data-stu-id="6b382-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="6b382-133">تتوفر أنواع مختلفة من قوائم التوصيات:</span><span class="sxs-lookup"><span data-stu-id="6b382-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="6b382-134">تستند قائمة **الأشخاص معجبون بهم أيضًا** إلى التعلم الآلي.</span><span class="sxs-lookup"><span data-stu-id="6b382-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="6b382-135">ويستخدم سجل الحركات الخاص بالعملاء الآخرين لتقديم توصيات.</span><span class="sxs-lookup"><span data-stu-id="6b382-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="6b382-136">يتم إنشاء هذه القائمة بواسطة خدمة التوصيات وتشبه قائمة "العملاء الذين اشتروا هذا قاموا أيضًا بشراء...".</span><span class="sxs-lookup"><span data-stu-id="6b382-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="6b382-137">معرف المنتج مطلوب لإنشاء هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="6b382-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="6b382-138">يمكن تكوين قائمة **مرتبطة** لمنتج في Retail.</span><span class="sxs-lookup"><span data-stu-id="6b382-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="6b382-139">على سبيل المثال، بالنسبة لحقيبة اليد بنية اللون للسفر، يمكن تكوين المزيد من حقائب اليد المصنعة من الجلد أو المصممة لأغراض السفر للقائمة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="6b382-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="6b382-140">يمكن أيضًا تكوين أنواع أخرى من القوائم المرتبطة، مثل **الإكسسوارات** و**الكثير مثل هذا** في Retail.</span><span class="sxs-lookup"><span data-stu-id="6b382-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="6b382-141">معرف المنتج مطلوب لإنشاء هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="6b382-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="6b382-142">ولذلك، إذا تمت اضافتها إلى صفحة رئيسية، حيث لا يتضمن سياق الصفحة معرف منتج، ستكون القائمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="6b382-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="6b382-143">يمكن استخدام قوائم التوصيات التي تم إنشائها حسابيًا، مثل **التداول** و**الأفضل مبيعًا** و**جديد** على ملفات بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="6b382-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="6b382-144">على الرغم من أن هذه القوائم قد لا ترتبط مباشرة بالمنتج على ملف بتنسيق PDF، إلا أنها طريقة أخرى لمساعدة العملاء في العثور على المنتجات التي قد تهمهم.</span><span class="sxs-lookup"><span data-stu-id="6b382-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="6b382-145">لا تتطلب أنواع القوائم هذه وجود معرف منتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="6b382-146">وهي عبارة عن قوائم عامة يتم إنشاؤها استنادًا إلى أنماط التسوق عبر الموقع.</span><span class="sxs-lookup"><span data-stu-id="6b382-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="6b382-147">تُعد القوائم التحريرية قوائم مُختارة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="6b382-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="6b382-148">على سبيل المثال، قد يقرر بائع التجزئة اختيار قوائم المنتجات التي يريد إظهارها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="6b382-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="6b382-149">الوحدة النمطية للتقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="6b382-149">Ratings and reviews module</span></span>

<span data-ttu-id="6b382-150">تعمل الوحدة النمطية للتصنيفات والمراجعات على عرض التصنيفات والمراجعات التي قام العملاء الآخرين بتقديمها.</span><span class="sxs-lookup"><span data-stu-id="6b382-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="6b382-151">وتتيح للعميل كذلك كتابة مراجعة المنتج الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="6b382-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="6b382-152">بالإضافة إلى ذلك، فإنها تتضمن الرسم البياني الذي يعرض اتجاه التصنيفات الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="6b382-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="6b382-153">للحصول على مزيد من التفاصيل، راجع [نظرة عامة حول التصنيفات والمراجعات](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6b382-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="6b382-154">الوحدة النمطية للتسويق</span><span class="sxs-lookup"><span data-stu-id="6b382-154">Marketing modules</span></span>

<span data-ttu-id="6b382-155">إذا كان محتوى التسويق فريدًا لمنتج معين، فإنه يمكن إضافة أية وحدة نمطية للتسويق إلى الملف بتنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="6b382-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="6b382-156">يمكنك إضافة الوحدات النمطية للتسويق إلى ملف بتنسيق PDF عن طريق "إثراء" الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6b382-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="6b382-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6b382-157">Additional resources</span></span>

[<span data-ttu-id="6b382-158">نظرة عامة على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="6b382-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="6b382-159">نظرة عامة على الصفحة المنتقل إليها‬ للفئة الافتراضية وصفحة نتائج البحث</span><span class="sxs-lookup"><span data-stu-id="6b382-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="6b382-160">نظرة عامة على صفحات سلة التسوق والسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="6b382-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="6b382-161">نظرة عامة على صفحات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="6b382-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
