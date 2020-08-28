---
title: تمكين توصيات "تسوق منتجات تبدو مماثلة"
description: يوضح هذا الموضوع كيفية تمكين توصيات منتجات "تسوق منتجات تبدو مماثلة" في Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2e57965a1073982a7b6c34b79dbf6e5b90d7ee30
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666298"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="d34cb-103">تمكين توصيات "تسوق منتجات تبدو مماثلة"</span><span class="sxs-lookup"><span data-stu-id="d34cb-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d34cb-104">يوضح هذا الموضوع كيفية تمكين توصيات منتجات "تسوق منتجات تبدو مماثلة" في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d34cb-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d34cb-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d34cb-105">Overview</span></span>

<span data-ttu-id="d34cb-106">تستخدم ميزة توصيات "تسوق منتجات تبدو مماثلة" في Dynamics 365 Commerce فعالية الذكاء الاصطناعي والتعلّم الآلي لتقديم توصيات حول منتجات تبدو مماثلة مرئيًا للعملاء.</span><span class="sxs-lookup"><span data-stu-id="d34cb-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="d34cb-107">ومن خلال جعل توصيات "تسوق منتجات تبدو مماثلة" متوفرة لجميع قنوات البيع بالتجزئة في Commerce، يمكن لبائعي بالتجزئة زيادة رضا العملاء من خلال مساعدتهم على العثور على ما يريدونه بسهولة.</span><span class="sxs-lookup"><span data-stu-id="d34cb-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="d34cb-108">تستخدم وظيفة توصيات "تسوق منتجات تبدو مماثلة" صور منتجات لمتغيرات منتجات أولية للبحث عن منتجات مماثلة مرئيًا والتوصية بها في كتالوج منتجات بائع التجزئة.</span><span class="sxs-lookup"><span data-stu-id="d34cb-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="d34cb-109">تتوفر توصيات "تسوق منتجات تبدو مماثلة" في تجارب كل من نقطة البيع (POS) والتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d34cb-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="d34cb-110">سيناريوهات مقدمة كمثال</span><span class="sxs-lookup"><span data-stu-id="d34cb-110">Example scenarios</span></span>

- <span data-ttu-id="d34cb-111">يشاهد العميل قميصًا مخططًا أسود اللون ويتلقى توصية حول قميص مماثل باللون الأحمر.</span><span class="sxs-lookup"><span data-stu-id="d34cb-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="d34cb-112">ويحدد العميل المنتج الموصي به بدلاً من المنتج الذي شاهده في الأصل، ثم يتلقى توصيات حول منتجات مماثلة باللون الأحمر.</span><span class="sxs-lookup"><span data-stu-id="d34cb-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="d34cb-113">يستخدم العميل توصيات "تسوق منتجات تبدو مماثلة"‬ لاكتشاف أقراط مطابقة لخاتم يهتم العميل بشرائه.</span><span class="sxs-lookup"><span data-stu-id="d34cb-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="d34cb-114">تمكين توصيات "تسوق منتجات تبدو مماثلة"‬ في مركز Commerce الرئيسي</span><span class="sxs-lookup"><span data-stu-id="d34cb-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="d34cb-115">تتوفر توصيات المنتجات فقط لعملاء Commerce ممن قاموا بترحيل مساحة التخزين إلى Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="d34cb-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d34cb-116">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="d34cb-116">Prerequisites</span></span>

<span data-ttu-id="d34cb-117">قبل ان يبدأ بائعو التجزئة بعرض توصيات "تسوق منتجات تبدو مماثلة" للعملاء، هناك خطوتان أساسيتان:</span><span class="sxs-lookup"><span data-stu-id="d34cb-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="d34cb-118">[تمكين توصيات المنتجات](enable-product-recommendations.md) في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d34cb-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="d34cb-119">التأكد من أن خادم الوسائط يدعم استدعاءات HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d34cb-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="d34cb-120">كي يتمكن محرك التوصيات من الوصول إلى صور المنتج، يجب أن يقوم بائعو التجزئة بإنشاء عناوين URL للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="d34cb-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="d34cb-121">لإنشاء عناوين URL للمنتجات في مركز Commerce الرئيسي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d34cb-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d34cb-122">انتقل إلى **صور المنتج**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="d34cb-123">في جزء الإجراءات، حدد **تعريف قالب الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="d34cb-124">في جزء خصائص **تعريف قالب الوسائط**، تحت **عناوين URL للوسائط**، حدد **إنشاء عناوين URL**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="d34cb-125">عند تمكين توصيات "تسوق منتجات تبدو مماثلة"‬، تبدأ عمليه إنشاء قوائم توصيات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="d34cb-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="d34cb-126">تحتاج هذه القوائم إلى فترة تصل إلى يوم واحد قبل أن تصبح متوفرة ومرئية عبر الإنترنت وعلى الوحدات الطرفية لنقاط البيع (POS).‬</span><span class="sxs-lookup"><span data-stu-id="d34cb-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="d34cb-127">لتمكين توصيات "تسوق منتجات تبدو مماثلة"‬، في مركز Commerce الرئيسي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d34cb-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d34cb-128">انتقل إلى **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="d34cb-129">في قائمة الميزات المتوفرة، ابحث عن **تسوق منتجات تبدو مماثلة** وحددها.</span><span class="sxs-lookup"><span data-stu-id="d34cb-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="d34cb-130">في الجزء الأيسر، حدد **تمكين** لتشغيل الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d34cb-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="d34cb-131">يبين الرسم التوضيحي التالي ميزة **تسوق منتجات تبدو مماثلة** في صفحة **إدارة الميزات** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d34cb-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![ميزة تسوق منتجات تبدو مماثلة في صفحة إدارة الميزات في مركز Commerce الرئيسي](./media/enableshopsimilarlooks.png)

<span data-ttu-id="d34cb-133">بعد إتمام المهام السابقة، يتم تحسين الوحدات الطرفية لنقطة البيع بشكل تلقائي بواسطة اللوحة **تسوق منتجات تبدو مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="d34cb-134">ومن خلال تحديد **معرفة المزيد**، يمكن نقل مستخدمي الوحدة الطرفية لنقطة البيع إلى صفحة "تسوق منتجات تبدو مماثل" يمكنك إجراء المزيد من عمليات التصفية عليها.</span><span class="sxs-lookup"><span data-stu-id="d34cb-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="d34cb-135">إذا أوقفت تشغيل ميزة توصيات "تسوق منتجات تبدو مماثلة"‬، لا تتأثر أي أنواع أخرى من توصيات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="d34cb-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="d34cb-136">لمزيد من المعلومات حول توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d34cb-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="d34cb-137">إضافة الزر "تسوق منتجات تبدو مماثلة‬‏‫" إلى صفحات تفاصيل المنتجات باستخدام منشئ مواقع Commerce</span><span class="sxs-lookup"><span data-stu-id="d34cb-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="d34cb-138">بعد تمكين ميزة توصيات "تسوق منتجات تبدو مماثلة"‬، في مركز Commerce الرئيسي، يسمح خيار في منشئ مواقع Commerce لبائعي التجزئة بإضافة الزر **تسوق منتجات تبدو مماثلة** إلى مربع الشراء في أي صفحة من صفحات تفاصيل المنتجات (PDP).</span><span class="sxs-lookup"><span data-stu-id="d34cb-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="d34cb-139">يُنقل العميل الذي يحدد هذا الزر إلى صفحة مخصص "تسوق منتجات تبدو مماثلة" تقوم بإرجاع منتجات مماثلة مرئيًا.</span><span class="sxs-lookup"><span data-stu-id="d34cb-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="d34cb-140">هناك، يمكن للعميل استخدام المحددات لإجراء المزيد من عمليات التصفية على المنتجات.</span><span class="sxs-lookup"><span data-stu-id="d34cb-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="d34cb-141">لإضافة الزر **تسوق منتجات تبدو مماثلة**‫ إلى صفحات تفاصيل المنتجات باستخدام منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d34cb-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d34cb-142">افتح صفحة منشئ مواقع موجودة تحتوي على وحدة مربع شراء.</span><span class="sxs-lookup"><span data-stu-id="d34cb-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="d34cb-143">في جزء التنقل الأيسر، حدد وحدة مربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="d34cb-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="d34cb-144">في جزء التنقل الأيمن، حدد خانة الاختيار **ارتباط تسوق منتجات تبدو مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="d34cb-145">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="d34cb-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="d34cb-146">بعد نشر الصفحة، ستتضمن PDP الزر **تسوق منتجات تبدو مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="d34cb-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="d34cb-147">يبين الرسم التوضيحي التالي خانة الاختيار **ارتباط تسوق منتجات تبدو مماثلة** والزر **تسوق منتجات تبدو مماثلة** على مثال عن PDP في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="d34cb-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![خانة الاختيار "ارتباط تسوق منتجات تبدو مماثلة" والزر "تسوق منتجات تبدو مماثلة" على PDP في منشئ المواقع.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="d34cb-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d34cb-149">Additional resources</span></span>

[<span data-ttu-id="d34cb-150">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d34cb-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d34cb-151">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d34cb-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d34cb-152">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d34cb-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d34cb-153">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="d34cb-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d34cb-154">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="d34cb-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d34cb-155">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="d34cb-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d34cb-156">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="d34cb-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d34cb-157">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="d34cb-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d34cb-158">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="d34cb-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d34cb-159">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d34cb-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
