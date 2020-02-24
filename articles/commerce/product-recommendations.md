---
title: نظرة عامة على توصيات المنتجات
description: يوفر هذا الموضوع معلومات عامة حول توصيات المنتج. تسمح توصيات المنتجات للعملاء بالبحث عن المنتجات التي يريدونها بسهولة وسرعة، وحتى المنتجات التي لم يرغبون بشراءها.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024969"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="9bc37-104">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="9bc37-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9bc37-105">يمكن استخدام تطبيق Microsoft Dynamics 365 Commerce لعرض توصيات المنتجات على موقع التجارة الإلكترونية و جهاز نقطة البيع (POS).‬</span><span class="sxs-lookup"><span data-stu-id="9bc37-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="9bc37-106">توصيات المنتجات هي الأصناف التي قد يهتم بها العميل.</span><span class="sxs-lookup"><span data-stu-id="9bc37-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="9bc37-107">وتعتمد التوصيات على اتجهات الشراء للعملاء الآخرين في المتاجر التقليدية أو المتاجر الأخرى على الإنترنت .</span><span class="sxs-lookup"><span data-stu-id="9bc37-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="9bc37-108">تسمح توصيات المنتجات للعملاء بالبحث بسهولة وسرعة عن المنتجات التي يرغبون في شرائها مع الاستمتاع بتجربة الحصول عليها بشكل جيد.</span><span class="sxs-lookup"><span data-stu-id="9bc37-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="9bc37-109">يمكن استخدام البيع التكميلي والإضافي‬ لمساعدة العملاء في العثور على المنتجات الإضافية التي لا ينوون شراءها في الأصل.</span><span class="sxs-lookup"><span data-stu-id="9bc37-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="9bc37-110">عند استخدام التوصيات للمساعدة في اكتشاف المنتج، يمكنها إنشاء المزيد من فرص التحويل، والمساعدة على زيادة عائد المبيعات، وحتى المساعدة في تحسين رضا العميل والاحتفاظ به.</span><span class="sxs-lookup"><span data-stu-id="9bc37-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="9bc37-111">في تطبيق Commerce، يتم تشغيل توصيات المنتجات بواسطة تقنيات التعلم الآلي لتوصيات Microsoft على نطاق واسع.</span><span class="sxs-lookup"><span data-stu-id="9bc37-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="9bc37-112">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="9bc37-112">Scenarios</span></span>

<span data-ttu-id="9bc37-113">يتم توفير توصيات المنتج للسيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="9bc37-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="9bc37-114">**في أي صفحة من صفحات المتجر للاستعراض أو للصفحة المنتقل اليها في التجارة الإلكترونية:** إذا كان العملاء أو شركاء المتجر يزورون إحدى صفحات المتجر، فيمكن لمحرك التوصيات اقتراح المنتجات في القوائم **جديد**، و **الأكثر مبيعًا**، و **المتداول**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="9bc37-115">**في صفحة تفاصيل المنتج:** إذا كان العملاء أو شركاء المتجر يزورون صفحة **تفاصيل المنتج**، يقوم جهاز التوصيات باقتراح الأصناف الإضافية التي غالبًا ما يتم شراؤها.</span><span class="sxs-lookup"><span data-stu-id="9bc37-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="9bc37-116">تظهر هذه الأصناف في قائمة **‬‏‫أشخاص معجبون به أيضًا**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="9bc37-117">**في صفحة الحركة أو صفحة السداد مع الخروج:** يقوم محرك التوصيات باقتراح الأصناف، استنادا إلى إجمالي قائمة الأصناف في السلة.</span><span class="sxs-lookup"><span data-stu-id="9bc37-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="9bc37-118">تظهر هذه الأصناف في قائمة **الأغراض التي يتم شراؤها معًا كثيرًا**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="9bc37-119">**التوصيات المخصصة:** يمكن للتجار تزويد العملاء الذين سجلوا الدخول بقائمة **العناصر المقترحة لك**، بالاضافه إلى الوظائف الجديدة التي تسمح بتخصيص وحدات سيناريو القائمة الموجودة استنادا إلى هذا العميل.</span><span class="sxs-lookup"><span data-stu-id="9bc37-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="9bc37-120">لمعرفه المزيد، يُرجى مراجعة وثائق الميزات: [تمكين التوصيات المخصصة.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="9bc37-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="9bc37-121">خدمة التوصيات</span><span class="sxs-lookup"><span data-stu-id="9bc37-121">Recommendation service</span></span>

<span data-ttu-id="9bc37-122">تستخدم توصيات المنتج تقنيات التعلم الآلي للتوصيات بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="9bc37-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="9bc37-123">يتم استخراج البيانات بالتنسيق المطلوب من خلال خدمة التوصيات من قاعدة البيانات التشغيلية في تطبيق Commerce وإرسالها إلى مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="9bc37-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="9bc37-124">تستخدم خدمة التوصيات البيانات الخاصة بتدريب نماذج التوصيات للقوائم ‫‬‏‫**أشخاص معجبون به أيضًا‬‏‫**، و **الأغراض التي يتم شراؤها معًا كثيرًا**‬‏‫، و **جديد** و **الأفضل مبيعًا**‬‏‫، و **المتداول**.</span><span class="sxs-lookup"><span data-stu-id="9bc37-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bc37-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9bc37-125">Additional resources</span></span>

[<span data-ttu-id="9bc37-126">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="9bc37-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9bc37-127">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="9bc37-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9bc37-128">نظرة عامة على الوحدة النمطية لمجموعة المنتجات</span><span class="sxs-lookup"><span data-stu-id="9bc37-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="9bc37-129">إنشاء قوائم توصيات منتجات المختارة</span><span class="sxs-lookup"><span data-stu-id="9bc37-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9bc37-130">إدارة نتائج توصيات المنتجات المستندة إلى AI-ML</span><span class="sxs-lookup"><span data-stu-id="9bc37-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9bc37-131">إضافة قوائم توصيات المنتجات إلى الصفحات</span><span class="sxs-lookup"><span data-stu-id="9bc37-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
