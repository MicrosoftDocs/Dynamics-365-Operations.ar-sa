---
title: الأسئلة المتداولة حول توصيات المنتجات
description: يوفر هذا الموضوع معلومات حول العمليات والأدوات التي يمكنك استخدامها لاستكشاف المشكلات المتعلقة بتوصيات المنتج أو النتائج الخاصة بها.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f4f053066ef9a10ca8a60e6eb081f73401760eb4
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770106"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="a7590-103">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a7590-103">Product recommendations FAQ</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a7590-104">يوفر هذا الموضوع معلومات حول العمليات والأدوات التي يمكنك استخدامها لاستكشاف المشكلات المتعلقة بـ [توصيات المنتج](product-recommendations.md) أو النتائج الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="a7590-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="a7590-105">أفضل الممارسات</span><span class="sxs-lookup"><span data-stu-id="a7590-105">Best practices</span></span>
<span data-ttu-id="a7590-106">من المهم جدًا استخدام مفهوم أصول المنتجات‬ والمتغيرات.</span><span class="sxs-lookup"><span data-stu-id="a7590-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="a7590-107">يساعد تجميع المتغيرات المعقولة للمنتج الرئيسي الأصلي خوارزميات القائمة والخدمة في إنشاء نماذج أفضل.</span><span class="sxs-lookup"><span data-stu-id="a7590-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="a7590-108">بالإضافة إلى ذلك، يمكن أن تقدم الخدمة مثيلًا واحدًا فقط للمنتج بدلاً من وضع كافة المتغيرات وثيقة الصلة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="a7590-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="a7590-109">عند وضع كافة المتغيرات وثيقة الصلة في القائمة، يمكن أن يؤدي ذلك إلى نتائج غير صحيحة أو مكررة.</span><span class="sxs-lookup"><span data-stu-id="a7590-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="a7590-110">لماذا لا توجد المنتجات في قوائم التوصيات الخاصة بي؟</span><span class="sxs-lookup"><span data-stu-id="a7590-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="a7590-111">عادةً، إذا كان هناك صنف مفقود من قائمة توصيات المنتج، فقد تكون هناك مشكلة في تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="a7590-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="a7590-112">على سبيل المثال، قد يكون هناك تاريخ غير صحيح لتاريخ بدء المنتج أو تاريخ انتهائه، أو قد يكون هناك خطأ في تكوين بُعد، أو قد لا يكون المنتج في مجموعة القنوات الصحيحة، وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="a7590-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="a7590-113">إذا كان هناك صنف مفقود من قائمة التوصيات التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML)، فقد لا يناسب الصنف معايير قائمة التوصيات، أو قد لا يحتوي على حركات شراء كافية لقائمة التوصيات لإظهارها.</span><span class="sxs-lookup"><span data-stu-id="a7590-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="a7590-114">نوصي بالتحقق من الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="a7590-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="a7590-115">**تأكد من تمكين توصيات المنتج في HQ.**</span><span class="sxs-lookup"><span data-stu-id="a7590-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="a7590-116">لمزيد من المعلومات حول كيفية تمكين هذه الخدمة، راجع [تمكين توصيات المنتج‬](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="a7590-117">**تأكد من تعيين خصائص المنتج الرئيسية.**</span><span class="sxs-lookup"><span data-stu-id="a7590-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="a7590-118">على سبيل المثال، يجب تعيين عمليات فرز‬ المنتجات إلى **تضمين**.</span><span class="sxs-lookup"><span data-stu-id="a7590-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="a7590-119">**بالنسبة للمنتجات المصنفة‬ حديثًا، قد يستغرق الأمر ما يصل إلى 3 ساعات قبل أن يبدأ المنتج في الظهور في القائمة الجديدة.**</span><span class="sxs-lookup"><span data-stu-id="a7590-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="a7590-120">**إذا كان المنتج لا يزال غير ظاهر في المُتداول أو الأفضل مبيعًا أو الأشخاص المعجبون به أيضًا أو المشتراة كثيرًا، فقد لا يكون لهذا المنتج محركات كافية.**</span><span class="sxs-lookup"><span data-stu-id="a7590-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="a7590-121">في هذه الحالة، يمكنك إما انتظار حدوث مزيد من الحركات أو تحديث معلمات قائمة التوصيات الافتراضية أو استخدام تدخل يدوي لتعديل نتائج قائمة منتجات التوصية.</span><span class="sxs-lookup"><span data-stu-id="a7590-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="a7590-122">لمزيد من المعلومات حول معلمات التوصيات، راجع [إدارة نتائج توصيات المنتج المستندة إلى AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="a7590-123">**تأكد أن المنتج يفي بمعايير التوصيات الخاصة بالقائمة.**</span><span class="sxs-lookup"><span data-stu-id="a7590-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="a7590-124">لمزيد من المعلومات حول معلمات توصيات المنتج، راجع [إدارة نتائج توصيات المنتج المستندة إلى AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="a7590-125">كيف يمكنني منع نتائج التوصية غير الصالحة من معاودة الظهور؟</span><span class="sxs-lookup"><span data-stu-id="a7590-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="a7590-126">تتطلب قوائم التوصيات حجمًا كبيرًا من الحركات لإنتاج النتائج.</span><span class="sxs-lookup"><span data-stu-id="a7590-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="a7590-127">لذلك، من المهم أن يقدم المستخدمون بيانات الحركة التاريخية الكاملة.</span><span class="sxs-lookup"><span data-stu-id="a7590-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="a7590-128">بالإضافة إلى ذلك، لا يكون لدى المنتجات التي ليس بها حركات أو حركات قليلة نتائج **أشخاص معجبون به أيضًا** أو **يتم شراؤها معًا بشكل متكرر** ، ولا تظهر في قوائم توصيات **المتداول** أو **الأفضل مبيعًا** .</span><span class="sxs-lookup"><span data-stu-id="a7590-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="a7590-129">غالبًا ما يمكن أن يحدث هذا الموقف للمنتجات الجديدة جدًا أو للمنتجات القديمة التي لديها عدد صغير من المشتريات.</span><span class="sxs-lookup"><span data-stu-id="a7590-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="a7590-130">ستتغلب الأصناف الجديدة الشائعة بسهولة على هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a7590-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="a7590-131">نوصي باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="a7590-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="a7590-132">**تأكد أن المنتج يفي بمعايير التوصيات الخاصة بتلك القائمة.**</span><span class="sxs-lookup"><span data-stu-id="a7590-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="a7590-133">لمزيد من المعلومات حول معلمات توصيات المنتج، راجع تعديل نتائج توصيات المنتج المستندة إلى AI-ML.</span><span class="sxs-lookup"><span data-stu-id="a7590-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="a7590-134">**إذا كان المنتج جديدًا، خذ بعين الاعتبار تعديل قائمة التوصيات حتى يتمكن المنتج من الحصول على المزيد من الحركات.**</span><span class="sxs-lookup"><span data-stu-id="a7590-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="a7590-135">لمزيد من المعلومات حول كيفية تعديل نتائج قائمة التوصيات، راجع [إدارة نتائج توصيات المنتج المستندة إلى AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="a7590-136">**تأكد أن المنتج يفي بمعايير التوصيات الخاصة بتلك القائمة.**</span><span class="sxs-lookup"><span data-stu-id="a7590-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="a7590-137">لمزيد من المعلومات حول معلمات توصيات المنتج، راجع [إدارة نتائج توصيات المنتج المستندة إلى AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="a7590-138">**إذا كان المنتج جديدًا، خذ بعين الاعتبار تعديل قائمة التوصيات حتى يتمكن المنتج من الحصول على المزيد من الحركات**.</span><span class="sxs-lookup"><span data-stu-id="a7590-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="a7590-139">لمزيد من المعلومات حول كيفية تعديل نتائج قائمة التوصيات، راجع [إدارة نتائج توصيات المنتج المستندة إلى AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="a7590-140">هل يمكنني إزالة منتج ولكن يظل مرئيًا في المتجر؟</span><span class="sxs-lookup"><span data-stu-id="a7590-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="a7590-141">يمكنك تعديل القوائم التي يتم إنشاؤها حسابيًا إذا دعت الحاجة إلى عمل ذلك.</span><span class="sxs-lookup"><span data-stu-id="a7590-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="a7590-142">ومع ذلك، إذا تمت إزالة منتج من قائمة التوصيات، فسيظل المنتج قابلاً للاكتشاف في المتجر.</span><span class="sxs-lookup"><span data-stu-id="a7590-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="a7590-143">لمزيد من المعلومات حول كيفية تعديل نتائج توصيات المنتج، راجع [إدارة نتائج توصيات المنتج المستندة إلى AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="a7590-144">إذا كان يجب عليك حظر أحد الأصناف من اكتشافه في المتجر، فيجب تغيير قيمة **عمليات فرز الصنف** إلى **استبعاد**.</span><span class="sxs-lookup"><span data-stu-id="a7590-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="a7590-145">كيف أضيف قائمة إلى صفحة التجارة الإلكترونية؟</span><span class="sxs-lookup"><span data-stu-id="a7590-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="a7590-146">للحصول على معلومات حول كيفية إضافة صفحات توصية المنتج إلى موقع التجارة الإلكترونية، راجع [إضافة قوائم توصيات المنتج إلى الصفحات](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="a7590-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="a7590-147">كيف يتم تمكين التوصيات علي نقطه البيع؟</span><span class="sxs-lookup"><span data-stu-id="a7590-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="a7590-148">بعد تمكين توصيات المنتج، سوف تحتاج إلى إضافة لوحة التوصيات إلى شاشة التحكم في نقاط البيع.</span><span class="sxs-lookup"><span data-stu-id="a7590-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="a7590-149">راجع [وثائق هذه الميزة](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) للحصول على مزيد من المعلومات حول كيفية إضافة لوحة التوصيات إلى تخطيط جهاز نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="a7590-149">See [this feature documentation](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) for more information on how to do add the recommendations panel to your POS device layout.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7590-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a7590-150">Additional resources</span></span>

[<span data-ttu-id="a7590-151">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a7590-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a7590-152">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a7590-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a7590-153">إدارة نتائج توصيات المنتجات المستندة إلى AI-ML</span><span class="sxs-lookup"><span data-stu-id="a7590-153">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)
