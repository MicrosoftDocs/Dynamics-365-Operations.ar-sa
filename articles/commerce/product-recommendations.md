---
title: نظرة عامة على توصيات المنتجات
description: يوفر هذا الموضوع معلومات عامة حول توصيات المنتج. تسمح توصيات المنتجات للعملاء بالبحث عن المنتجات التي يريدونها بسهولة وسرعة، وحتى المنتجات التي لم يرغبون بشراءها.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1b01589322c26b6a7b69d1b992b03603f5f3d29a
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404338"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="d9da8-104">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d9da8-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9da8-105">يمكن استخدام تطبيق Microsoft Dynamics 365 Commerce لعرض توصيات المنتجات على موقع التجارة الإلكترونية و جهاز نقطة البيع (POS).‬</span><span class="sxs-lookup"><span data-stu-id="d9da8-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="d9da8-106">توصيات المنتجات هي الأصناف التي قد يهتم بها العميل.</span><span class="sxs-lookup"><span data-stu-id="d9da8-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="d9da8-107">وتعتمد التوصيات على اتجهات الشراء للعملاء الآخرين في المتاجر التقليدية أو المتاجر الأخرى على الإنترنت .</span><span class="sxs-lookup"><span data-stu-id="d9da8-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="d9da8-108">تسمح توصيات المنتجات للعملاء بالعثور بسهولة وسرعة عن المنتجات التي يرغبون في الحصول عليها مع الاستمتاع بتجربة مفيدة.</span><span class="sxs-lookup"><span data-stu-id="d9da8-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="d9da8-109">يمكن استخدام البيع التكميلي والإضافي‬ لمساعدة العملاء في العثور على المنتجات الإضافية التي لم يكن لديهم النية في شرائها في الأصل.</span><span class="sxs-lookup"><span data-stu-id="d9da8-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="d9da8-110">عند استخدام التوصيات لتحسين اكتشاف المنتج، يمكنها إنشاء المزيد من فرص التحويل، والمساعدة على زيادة عائد المبيعات، وحتى زيادة مستوى رضا العميل والاحتفاظ به.</span><span class="sxs-lookup"><span data-stu-id="d9da8-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="d9da8-111">في التجارة الإلكترونية، يتم تشغيل توصيات المنتجات بواسطة تقنيات التعلم الآلي لتوصيات Microsoft على نطاق واسع.</span><span class="sxs-lookup"><span data-stu-id="d9da8-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="d9da8-112">خدمة التوصيات</span><span class="sxs-lookup"><span data-stu-id="d9da8-112">Recommendation service</span></span>

<span data-ttu-id="d9da8-113">تستخدم خدمه توصيات المنتجات تقنيات الذكاء الاصطناعي والتعلم الآلي (AI-ML) بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="d9da8-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="d9da8-114">يتم استخراج البيانات بالتنسيق المطلوب من خلال خدمة التوصيات من قاعدة البيانات التشغيلية في تطبيق Commerce ويتم إرسالها إلى Azure Data Lake Storage أو مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="d9da8-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="d9da8-115">تستخدم خدمة التوصيات البيانات المخزنة لتدريب نماذج التوصيات للقوائم ‫‬‏‫**أشخاص معجبون به أيضًا‬‏‫**، و**الأغراض التي يتم شراؤها معًا كثيرًا**‬‏‫ و**جديد** و**الأفضل مبيعًا**‬‏‫ و**المتداول**.</span><span class="sxs-lookup"><span data-stu-id="d9da8-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="d9da8-116">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="d9da8-116">Scenarios</span></span>

<span data-ttu-id="d9da8-117">يتم توفير توصيات المنتج للسيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="d9da8-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="d9da8-118">**في أي صفحة من صفحات المتجر للاستعراض أو للصفحة المنتقل اليها في التجارة الإلكترونية:** إذا كان العملاء أو شركاء المتجر يزورون إحدى صفحات المتجر، فيمكن لمحرك التوصيات اقتراح المنتجات في القوائم **جديد**، و **الأكثر مبيعًا**، و **المتداول**.</span><span class="sxs-lookup"><span data-stu-id="d9da8-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="d9da8-119">**في صفحة تفاصيل المنتج:** إذا كان العملاء أو شركاء المتجر يزورون صفحة **تفاصيل المنتج**، يقوم جهاز التوصيات باقتراح الأصناف الإضافية التي غالبًا ما يتم شراؤها.</span><span class="sxs-lookup"><span data-stu-id="d9da8-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="d9da8-120">تظهر هذه الأصناف في قائمة **‬‏‫أشخاص معجبون به أيضًا**.</span><span class="sxs-lookup"><span data-stu-id="d9da8-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="d9da8-121">**في صفحة الحركة أو صفحة السداد مع الخروج:** يقوم محرك التوصيات باقتراح الأصناف، استنادا إلى إجمالي قائمة الأصناف في السلة.</span><span class="sxs-lookup"><span data-stu-id="d9da8-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="d9da8-122">تظهر هذه الأصناف في قائمة **الأغراض التي يتم شراؤها معًا كثيرًا**.</span><span class="sxs-lookup"><span data-stu-id="d9da8-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="d9da8-123">**التوصيات المخصصة:** يمكن للتجار تزويد العملاء الذين سجلوا الدخول بقائمة **العناصر المقترحة لك**، بالإضافة إلى الوظائف الجديدة التي تسمح بتخصيص وحدات سيناريو القائمة الموجودة استنادا إلى هذا العميل.</span><span class="sxs-lookup"><span data-stu-id="d9da8-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="d9da8-124">لمعرفة المزيد، راجع [تمكين التوصيات المخصصة.](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d9da8-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="d9da8-125">أنواع توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d9da8-125">Types of product recommendations</span></span>

<span data-ttu-id="d9da8-126">يصف الجدول التالي مختلف أنواع توصيات المنتجات التلقائية المتوفرة لبائعي التجزئة لتنفيذها في حل Dynamics 365 Commerce عبر [الوحدة النمطية مجموعة منتجات‬](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9da8-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="d9da8-127">بإمكان بائعي التجزئة أيضًا عرض النتائج المخصصة لمستخدم سجل دخوله إذا اختار مؤلف الموقع هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="d9da8-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="d9da8-128">الوحدة النمطية لمجموعة المنتجات</span><span class="sxs-lookup"><span data-stu-id="d9da8-128">Product collection module</span></span>  | <span data-ttu-id="d9da8-129">النوع</span><span class="sxs-lookup"><span data-stu-id="d9da8-129">Type</span></span> | <span data-ttu-id="d9da8-130">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="d9da8-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="d9da8-131">القيمة الجديدة</span><span class="sxs-lookup"><span data-stu-id="d9da8-131">New</span></span>                        | <span data-ttu-id="d9da8-132">حسابي</span><span class="sxs-lookup"><span data-stu-id="d9da8-132">Algorithmic</span></span> | <span data-ttu-id="d9da8-133">تعرض هذه الوحدة قائمة بأحدث المنتجات التي تم تصنيفها مؤخرًا إلى القنوات والكتالوجات.</span><span class="sxs-lookup"><span data-stu-id="d9da8-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="d9da8-134">الأعلى مبيعًا</span><span class="sxs-lookup"><span data-stu-id="d9da8-134">Best selling</span></span>               | <span data-ttu-id="d9da8-135">حسابي</span><span class="sxs-lookup"><span data-stu-id="d9da8-135">Algorithmic</span></span> | <span data-ttu-id="d9da8-136">تعرض هذه الوحدة النمطية قائمة بالمنتجات التي تم تصنيفها حسب أعلى عدد من المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d9da8-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="d9da8-137">المتصدر</span><span class="sxs-lookup"><span data-stu-id="d9da8-137">Trending</span></span>                   | <span data-ttu-id="d9da8-138">حسابي</span><span class="sxs-lookup"><span data-stu-id="d9da8-138">Algorithmic</span></span> | <span data-ttu-id="d9da8-139">تعرض هذه الوحدة قائمة بالمنتجات ذات الأداء الأعلى لفترة معينة، وقد تم ترتيبها حسب أعلى رقم مبيعات.</span><span class="sxs-lookup"><span data-stu-id="d9da8-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="d9da8-140">منتجات يتكرر شراؤها معًا</span><span class="sxs-lookup"><span data-stu-id="d9da8-140">Frequently bought together</span></span> | <span data-ttu-id="d9da8-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="d9da8-141">AI-ML</span></span> | <span data-ttu-id="d9da8-142">توصي هذه الوحدة النمطية بقائمة المنتجات التي يتم عادة شراؤها مع محتويات سلة التسوق الحالية للعملاء.</span><span class="sxs-lookup"><span data-stu-id="d9da8-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="d9da8-143">أعجب الأشخاص أيضًا بـ</span><span class="sxs-lookup"><span data-stu-id="d9da8-143">People also like</span></span>           | <span data-ttu-id="d9da8-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="d9da8-144">AI-ML</span></span> | <span data-ttu-id="d9da8-145">توصي هذه الوحدة النمطية بمنتجات لمنتج أولي معين استنادًا إلى أنماط الشراء لدى العميل.</span><span class="sxs-lookup"><span data-stu-id="d9da8-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="d9da8-146">العناصر المقترحة</span><span class="sxs-lookup"><span data-stu-id="d9da8-146">Picks for you</span></span>              | <span data-ttu-id="d9da8-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="d9da8-147">AI-ML</span></span> | <span data-ttu-id="d9da8-148">توصي هذه الوحدة النمطية بقائمة مخصصة للمنتجات استنادًا إلى أنماط الشراء الخاصة بالمستخدم الذي سجل دخوله.</span><span class="sxs-lookup"><span data-stu-id="d9da8-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="d9da8-149">بالنسبة لمستخدم ضيف، سيتم طي هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="d9da8-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d9da8-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d9da8-150">Additional resources</span></span>

[<span data-ttu-id="d9da8-151">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d9da8-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d9da8-152">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d9da8-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d9da8-153">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="d9da8-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d9da8-154">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="d9da8-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d9da8-155">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="d9da8-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d9da8-156">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="d9da8-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d9da8-157">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="d9da8-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d9da8-158">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="d9da8-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d9da8-159">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="d9da8-159">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d9da8-160">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d9da8-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
