---
title: تمكين توصيات "تسوق منتجات تبدو مماثلة"
description: يوضح هذا الموضوع كيفية تمكين توصيات منتجات "تسوق منتجات تبدو مماثلة" في Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 06b5721c423330b8840bb546bdb144c3189c25bb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795371"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="96af3-103">تمكين توصيات "تسوق أشكال مماثلة"</span><span class="sxs-lookup"><span data-stu-id="96af3-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96af3-104">يوضح هذا الموضوع كيفية تمكين توصيات منتجات "تسوق منتجات تبدو مماثلة" في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="96af3-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="96af3-105">تستخدم ميزة توصيات "تسوق منتجات تبدو مماثلة" في Dynamics 365 Commerce فعالية الذكاء الاصطناعي والتعلّم الآلي لتقديم توصيات حول منتجات تبدو مماثلة مرئيًا للعملاء.</span><span class="sxs-lookup"><span data-stu-id="96af3-105">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="96af3-106">ومن خلال جعل توصيات "تسوق منتجات تبدو مماثلة" متوفرة لجميع قنوات البيع بالتجزئة في Commerce، يمكن لبائعي بالتجزئة زيادة رضا العملاء من خلال مساعدتهم على العثور على ما يريدونه بسهولة.</span><span class="sxs-lookup"><span data-stu-id="96af3-106">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="96af3-107">تستخدم وظيفة توصيات "تسوق منتجات تبدو مماثلة" صور منتجات لمتغيرات منتجات أولية للبحث عن منتجات مماثلة مرئيًا والتوصية بها في كتالوج منتجات بائع التجزئة.</span><span class="sxs-lookup"><span data-stu-id="96af3-107">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="96af3-108">تتوفر توصيات "تسوق منتجات تبدو مماثلة" في تجارب كل من نقطة البيع (POS) والتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="96af3-108">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="96af3-109">سيناريوهات مقدمة كمثال</span><span class="sxs-lookup"><span data-stu-id="96af3-109">Example scenarios</span></span>

- <span data-ttu-id="96af3-110">يشاهد العميل قميصًا مخططًا أسود اللون ويتلقى توصية حول قميص مماثل باللون الأحمر.</span><span class="sxs-lookup"><span data-stu-id="96af3-110">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="96af3-111">ويحدد العميل المنتج الموصي به بدلاً من المنتج الذي شاهده في الأصل، ثم يتلقى توصيات حول منتجات مماثلة باللون الأحمر.</span><span class="sxs-lookup"><span data-stu-id="96af3-111">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="96af3-112">يستخدم العميل توصيات "تسوق منتجات تبدو مماثلة"‬ لاكتشاف أقراط مطابقة لخاتم يهتم العميل بشرائه.</span><span class="sxs-lookup"><span data-stu-id="96af3-112">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="96af3-113">تمكين توصيات "تسوق منتجات تبدو مماثلة"‬ في مركز Commerce الرئيسي</span><span class="sxs-lookup"><span data-stu-id="96af3-113">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="96af3-114">تتوفر توصيات المنتجات فقط لعملاء Commerce ممن قاموا بترحيل مساحة التخزين إلى Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="96af3-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="96af3-115">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="96af3-115">Prerequisites</span></span>

<span data-ttu-id="96af3-116">قبل ان يبدأ بائعو التجزئة بعرض توصيات "تسوق منتجات تبدو مماثلة" للعملاء، هناك خطوتان أساسيتان:</span><span class="sxs-lookup"><span data-stu-id="96af3-116">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="96af3-117">[تمكين توصيات المنتجات](enable-product-recommendations.md) في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="96af3-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="96af3-118">التأكد من أن خادم الوسائط يدعم استدعاءات HTTPS.</span><span class="sxs-lookup"><span data-stu-id="96af3-118">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="96af3-119">كي يتمكن محرك التوصيات من الوصول إلى صور المنتج، يجب أن يقوم بائعو التجزئة بإنشاء عناوين URL للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="96af3-119">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="96af3-120">لإنشاء عناوين URL للمنتجات في مركز Commerce الرئيسي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="96af3-120">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="96af3-121">انتقل إلى **صور المنتج**.</span><span class="sxs-lookup"><span data-stu-id="96af3-121">Go to **Product images**.</span></span>
1. <span data-ttu-id="96af3-122">في جزء الإجراءات، حدد **تعريف قالب الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="96af3-122">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="96af3-123">في جزء خصائص **تعريف قالب الوسائط**، تحت **عناوين URL للوسائط**، حدد **إنشاء عناوين URL**.</span><span class="sxs-lookup"><span data-stu-id="96af3-123">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="96af3-124">عند تمكين توصيات "تسوق منتجات تبدو مماثلة"‬، تبدأ عمليه إنشاء قوائم توصيات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="96af3-124">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="96af3-125">تحتاج هذه القوائم إلى فترة تصل إلى يوم واحد قبل أن تصبح متوفرة ومرئية عبر الإنترنت وعلى الوحدات الطرفية لنقاط البيع (POS).‬</span><span class="sxs-lookup"><span data-stu-id="96af3-125">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="96af3-126">لتمكين توصيات "تسوق منتجات تبدو مماثلة"‬، في مركز Commerce الرئيسي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="96af3-126">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="96af3-127">انتقل إلى **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="96af3-127">Go to **Feature management**.</span></span>
1. <span data-ttu-id="96af3-128">في قائمة الميزات المتوفرة، ابحث عن **تسوق منتجات تبدو مماثلة** وحددها.</span><span class="sxs-lookup"><span data-stu-id="96af3-128">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="96af3-129">في الجزء الأيسر، حدد **تمكين** لتشغيل الخدمة.</span><span class="sxs-lookup"><span data-stu-id="96af3-129">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="96af3-130">يبين الرسم التوضيحي التالي ميزة **تسوق منتجات تبدو مماثلة** في صفحة **إدارة الميزات** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="96af3-130">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![ميزة تسوق منتجات تبدو مماثلة في صفحة إدارة الميزات في مركز Commerce الرئيسي](./media/enableshopsimilarlooks.png)

<span data-ttu-id="96af3-132">بعد إتمام المهام السابقة، يتم تحسين الوحدات الطرفية لنقطة البيع بشكل تلقائي بواسطة اللوحة **تسوق منتجات تبدو مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="96af3-132">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="96af3-133">ومن خلال تحديد **معرفة المزيد**، يمكن نقل مستخدمي الوحدة الطرفية لنقطة البيع إلى صفحة "تسوق منتجات تبدو مماثل" يمكنك إجراء المزيد من عمليات التصفية عليها.</span><span class="sxs-lookup"><span data-stu-id="96af3-133">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="96af3-134">إذا أوقفت تشغيل ميزة توصيات "تسوق منتجات تبدو مماثلة"‬، لا تتأثر أي أنواع أخرى من توصيات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="96af3-134">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="96af3-135">لمزيد من المعلومات حول توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="96af3-135">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="96af3-136">إضافة الزر "تسوق منتجات تبدو مماثلة‬‏‫" إلى صفحات تفاصيل المنتجات باستخدام منشئ مواقع Commerce</span><span class="sxs-lookup"><span data-stu-id="96af3-136">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="96af3-137">بعد تمكين ميزة توصيات "تسوق منتجات تبدو مماثلة"‬، في مركز Commerce الرئيسي، يسمح خيار في منشئ مواقع Commerce لبائعي التجزئة بإضافة الزر **تسوق منتجات تبدو مماثلة** إلى مربع الشراء في أي صفحة من صفحات تفاصيل المنتجات (PDP).</span><span class="sxs-lookup"><span data-stu-id="96af3-137">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="96af3-138">يُنقل العميل الذي يحدد هذا الزر إلى صفحة مخصص "تسوق منتجات تبدو مماثلة" تقوم بإرجاع منتجات مماثلة مرئيًا.</span><span class="sxs-lookup"><span data-stu-id="96af3-138">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="96af3-139">هناك، يمكن للعميل استخدام المحددات لإجراء المزيد من عمليات التصفية على المنتجات.</span><span class="sxs-lookup"><span data-stu-id="96af3-139">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="96af3-140">لإضافة الزر **تسوق منتجات تبدو مماثلة**‫ إلى صفحات تفاصيل المنتجات باستخدام منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="96af3-140">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="96af3-141">افتح صفحة منشئ مواقع موجودة تحتوي على وحدة مربع شراء.</span><span class="sxs-lookup"><span data-stu-id="96af3-141">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="96af3-142">في جزء التنقل الأيسر، حدد وحدة مربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="96af3-142">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="96af3-143">في جزء التنقل الأيمن، حدد خانة الاختيار **ارتباط تسوق منتجات تبدو مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="96af3-143">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="96af3-144">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="96af3-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="96af3-145">بعد نشر الصفحة، ستتضمن PDP الزر **تسوق منتجات تبدو مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="96af3-145">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="96af3-146">يبين الرسم التوضيحي التالي خانة الاختيار **ارتباط تسوق منتجات تبدو مماثلة** والزر **تسوق منتجات تبدو مماثلة** على مثال عن PDP في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="96af3-146">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![خانة الاختيار "ارتباط تسوق منتجات تبدو مماثلة" والزر "تسوق منتجات تبدو مماثلة" على PDP في منشئ المواقع.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="96af3-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="96af3-148">Additional resources</span></span>

[<span data-ttu-id="96af3-149">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="96af3-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="96af3-150">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="96af3-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="96af3-151">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="96af3-151">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="96af3-152">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="96af3-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="96af3-153">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="96af3-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="96af3-154">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="96af3-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="96af3-155">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="96af3-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="96af3-156">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="96af3-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="96af3-157">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="96af3-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="96af3-158">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="96af3-158">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
