---
title: إدارة نتائج توصيات المنتجات المستندة إلى AI-ML
description: يوضح هذا الموضوع كيفية نفصيل نتائج توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) مع احتياجات أعمالك.
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770060"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="6a7f8-103">إدارة نتائج توصيات المنتجات المستندة إلى AI-ML</span><span class="sxs-lookup"><span data-stu-id="6a7f8-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6a7f8-104">يوضح هذا الموضوع كيفية نفصيل نتائج توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) مع احتياجات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="6a7f8-105">بعد تمكين توصيات المنتج، ستصبح الإعدادات الافتراضية نافذة المفعول؛ أي أن هذه المعلمات ستؤدي دورها لتلبية العديد من الاحتياجات.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="6a7f8-106">من الأفضل التخطيط لقضاء بعض الوقت في تقييم ما إذا كانت النتائج تناسب حركه بيع المنتجات أم لا.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="6a7f8-107">نقترح عليك تقييم النتائج لأيام قليلة قبل تغيير المعلمات حسب الحاجة قبل الاختبار مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="6a7f8-108">فهم معلمات قائمة التوصيات</span><span class="sxs-lookup"><span data-stu-id="6a7f8-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="6a7f8-109">قبل تغيير المعلمات، تعرف على كيفية تأييرها على النتائج أدناه.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="6a7f8-110">فرز قائمة التداول</span><span class="sxs-lookup"><span data-stu-id="6a7f8-110">Trending product list</span></span>

<span data-ttu-id="6a7f8-111">تحتوي قائمة منتجات **التداول** على معلمتين يمكن تغييرهما: ![مثال: المعلمات الافتراضية لقائمة التداول](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="6a7f8-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="6a7f8-112">**تضمين منتجات جديدة من آخر X يوم/أيام**- المنتجات التي تمت إضافتها خلال عدد محدد من الأيام قبل إمكانية استخدام التاريخ الحالي لتحديد مرشحي المنتج.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="6a7f8-113">تقترح القيمة الافتراضية في الصورة أن المنتجات القديمة التي لها 180 يومًا يمكن استخدامها في قائمة المنتجات المتداولة.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="6a7f8-114">**تضمين منتجات جديدة من آخر X يوم/أيام**- المنتجات التي تمت إضافتها خلال عدد محدد من الأيام قبل إمكانية استخدام التاريخ الحالي لطلب المنتجات.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="6a7f8-115">تقترح القيمة الافتراضية المذكورة أعلاه أن كافة عمليات الشراء التي تم اجراؤها لأحد المنتجات في آخر 30 يومًا سيتم استخدامها لتحديد موضع المنتج في قائمة المنتجات المتداولة.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="6a7f8-116">قائمة المنتجات الأفضل مبيعًا</span><span class="sxs-lookup"><span data-stu-id="6a7f8-116">Best selling product list</span></span>

<span data-ttu-id="6a7f8-117">بناء على أعمالك، تجلب المنتجات الأفضل مبيعا نتائج مختلفة عن المتداول، على الرغم من أنهما يستخدمان بيانات الحركة لطلب المنتجات.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="6a7f8-118">ونظرًا لأن المنتجات الأفضل مبيعا ليس لها تاريخ انقطاع استنادا إلى تاريخ الفرز، فإنها تظل تميز المنتجات الشائعة جدًا؛ المنتجات الأقدم التي ربما تم إسقاطها من القائمة المتداولة.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="6a7f8-119">تحتوي قائمة منتجات **الأفضل مبيعًا** على معلمة واحدة يمكن تغييرها:</span><span class="sxs-lookup"><span data-stu-id="6a7f8-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![مثال: المعلمة الافتراضية لقائمة منتجات الأفضل مبيعًا](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="6a7f8-121">**تضمين منتجات جديدة من آخر X يوم/أيام**- المنتجات التي تمت إضافتها خلال عدد محدد من الأيام قبل إمكانية استخدام التاريخ الحالي لطلب المنتجات.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="6a7f8-122">تقترح القيمة الافتراضية المذكورة أعلاه أن كافة عمليات الشراء التي تم اجراؤها لأحد المنتجات في آخر 30 يومًا سيتم استخدامها لتحديد موضع المنتج في قائمة المنتجات الأفضل مبيعا.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="6a7f8-123">إضافة منتجات أو ازالتها يدويًا من قوائم التوصيات</span><span class="sxs-lookup"><span data-stu-id="6a7f8-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="6a7f8-124">بالنسبة للمنتجات الجديد أو المتداولة أو الأفضل مبيعاً</span><span class="sxs-lookup"><span data-stu-id="6a7f8-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="6a7f8-125">انتقل إلى **Retail‎** > **توصيات المنتج** > **معلمات التوصية**.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="6a7f8-126">في قائمة معلمات البيع بالتجزئة المشتركة، حدد **قوائم التوصيات**.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="6a7f8-127">حدد القائمة التي تريد إضافة أو إزالة منتجات منها.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="6a7f8-128">لإضافة منتجات إلى الجدول، حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="6a7f8-129">أسفل عمود المنتج، ابحث عن المنتج حسب **الاسم** أو **رقم المنتج.**
![مثال للبحث عن منتج في قائمة المنتجات الجديدة](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="6a7f8-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="6a7f8-130">أسفل عمود نوع البند، حدد خيار من خيارين:</span><span class="sxs-lookup"><span data-stu-id="6a7f8-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="6a7f8-131">**تضمين** -فرض وجود المنتج في مقدمة القائمة</span><span class="sxs-lookup"><span data-stu-id="6a7f8-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="6a7f8-132">**استبعاد** – إزالة المنتج من القائمة ![مثال لتضمين منتج أو استبعاده من قائمه المنتجات الجديدة](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="6a7f8-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="6a7f8-133">سيؤدي تغيير **ترتيب العرض** إلى تغيير الترتيب الذي تظهر المنتجات عنده معلمة كـ **تضمين** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="6a7f8-134">إذا كان لمنتجين نفس قيمة **ترتيب العرض**، فقد يختلف الترتيب النهائي لهاتين النتيجتين عن مكتب الدعم.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="6a7f8-135">لإزالة منتجات من الجدول: حدد البند المراد إزالته وحدد **إزالة**.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="6a7f8-136">بالنسبة للقائمتين "أشخاص معجبون به أيضًا‬‏‫" أو "الأغراض التي يتم شراؤها معًا كثيرا"</span><span class="sxs-lookup"><span data-stu-id="6a7f8-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="6a7f8-137">في سياق قائمة **الأغراض التي يتم شراؤها معًا كثيرًا** أو قائمة **أشخاص معجبون به أيضًا**، يتم استخدام تعلم الآلة لتحليل أنماط الشراء الخاصة بالمستهلك للتوصية بالمنتجات المرتبطة التي يتم شراؤها معًا بشكل متكرر لمنتج أساسي فريد.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="6a7f8-138">**المنتج الأساسي** هو المنتج الذي ترغب في إنشاء نتائج له.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="6a7f8-139">في سياق ضبط قوائم التوصيات يدويًا، تقوم بإضافة نتائج لهذا المنتج أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="6a7f8-140">اتبع هذه الخطوات لإضافة نتائج لمنتج أساسي أو إزالتها يدويًا:</span><span class="sxs-lookup"><span data-stu-id="6a7f8-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="6a7f8-141">حدد **المنتج الأساسي**.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="6a7f8-142">أسفل عمود **المنتج**، ابحث عن المنتج حسب **الاسم** أو **رقم المنتج**
![مثال للبحث عن منتج في قائمة الأغراض التي يتم شراؤها معًا كثيرًا‬](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="6a7f8-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="6a7f8-143">أسفل عمود **نوع البند**، حدد خيار من خيارين:</span><span class="sxs-lookup"><span data-stu-id="6a7f8-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="6a7f8-144">**تضمين** -فرض وجود المنتج في مقدمة القائمة</span><span class="sxs-lookup"><span data-stu-id="6a7f8-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="6a7f8-145">**استبعاد** – إزالة منتج من الظهور في القائمة</span><span class="sxs-lookup"><span data-stu-id="6a7f8-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="6a7f8-146">![مثال لتضمين أو استبعاد منتج في قائمة الأغراض التي يتم شراؤها معًا كثيرًا‬](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="6a7f8-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="6a7f8-147">لإزالة منتجات من الجدول: حدد البند المراد إزالته وحدد إزالة.</span><span class="sxs-lookup"><span data-stu-id="6a7f8-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6a7f8-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a7f8-148">Additional resources</span></span>

[<span data-ttu-id="6a7f8-149">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="6a7f8-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6a7f8-150">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="6a7f8-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6a7f8-151">إضافة قوائم توصيات المنتجات إلى الصفحات</span><span class="sxs-lookup"><span data-stu-id="6a7f8-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
