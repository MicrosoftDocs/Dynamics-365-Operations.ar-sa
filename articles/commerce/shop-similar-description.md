---
title: تمكين توصيات "وصف تسوق منتجات مماثلة"
description: يوضح هذا الموضوع كيفية تمكين توصيات "وصف تسوق منتجات تبدو مماثلة" في Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234379"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="463c1-103">تمكين توصيات "تسوق وصف مماثل"</span><span class="sxs-lookup"><span data-stu-id="463c1-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="463c1-104">يوضح هذا الموضوع كيفية تمكين توصيات "وصف تسوق منتجات تبدو مماثلة" في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="463c1-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="463c1-105">تستخدم ميزة توصيات "وصف تسوق منتجات مماثلة" في Dynamics 365 Commerce الذكاء الاصطناعي والتعلّم الآلي لتقديم توصيات حول منتجات ذات أوصاف تبدو مماثلة لما يبحث عنه العملاء.</span><span class="sxs-lookup"><span data-stu-id="463c1-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="463c1-106">ومن خلال جعل توصيات "وصف تسوق منتجات مماثلة" متوفرة لجميع قنوات البيع بالتجزئة في Commerce، يمكن لبائعي بالتجزئة مساعدة العملاء في العثور على ما يريدونه بسهولة.</span><span class="sxs-lookup"><span data-stu-id="463c1-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="463c1-107">تستخدم وظيفة توصيات "وصف تسوق منتجات مماثلة" اسم المنتج ووصف المنتجات الأولية للبحث عن منتجات مماثلة والتوصية بها في كتالوج منتجات بائع التجزئة.</span><span class="sxs-lookup"><span data-stu-id="463c1-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="463c1-108">تتوفر توصيات "وصف تسوق منتجات مماثلة" في تجارب كل من نقطة البيع (POS) والتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="463c1-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="463c1-109">سيناريوهات مقدمة كمثال</span><span class="sxs-lookup"><span data-stu-id="463c1-109">Example scenarios</span></span>

<span data-ttu-id="463c1-110">تُظهر سيناريوهات الامثلة التالية أنواع التوصيات التي يمكن أن توفرها وظيفة "وصف تسوق منتجات مماثلة":</span><span class="sxs-lookup"><span data-stu-id="463c1-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="463c1-111">يستعرض العميل زوجًا من النظارات بنمط قديم وبحافة من القرون ويتلقى مجموعة من التوصيات لنظارات أخرى تحتوي على تصميم مشابة، في سياق صناعة بائع التجزئة.</span><span class="sxs-lookup"><span data-stu-id="463c1-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="463c1-112">يستخدم العميل توصيات وصف تسوق منتجات مماثلة لاكتشاف نكهات القهوة التي تشبه النكهة التي اشتريتها سابقا من البائع.</span><span class="sxs-lookup"><span data-stu-id="463c1-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="463c1-113">إعداد توصيات "وصف تسوق منتجات مماثلة"</span><span class="sxs-lookup"><span data-stu-id="463c1-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="463c1-114">تتوفر توصيات المنتجات فقط لعملاء Commerce ممن قاموا بترحيل مساحة التخزين إلى Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="463c1-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="463c1-115">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="463c1-115">Prerequisites</span></span>

<span data-ttu-id="463c1-116">قبل إظهار توصيات "وصف تسوق منتجات مماثلة" للعملاء، يجب إكمال المتطلبات الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="463c1-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="463c1-117">[تمكين توصيات المنتجات](enable-product-recommendations.md) في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="463c1-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="463c1-118">التأكد من أن خادم الوسائط يدعم استدعاءات HTTPS.</span><span class="sxs-lookup"><span data-stu-id="463c1-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="463c1-119">تشغيل ميزة توصيات "وصف تسوق منتجات مماثلة"</span><span class="sxs-lookup"><span data-stu-id="463c1-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="463c1-120">لتمكين توصيات "وصف تسوق منتجات مماثلة"‬، في مركز Commerce الرئيسي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="463c1-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="463c1-121">في مساحة عمل **إدارة الميزات**، في قائمة الميزات المتوفرة، ابحث عن **وصف تسوق منتجات مماثلة** وحدده.</span><span class="sxs-lookup"><span data-stu-id="463c1-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="463c1-122">من الجزء الأيمن، حدد **تمكين** .</span><span class="sxs-lookup"><span data-stu-id="463c1-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="463c1-123">عند تشغيل الميزة، يبدأ النظام في إنشاء قوائم توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="463c1-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="463c1-124">قد يستغرق الأمر يومًا واحدًا قبل أن تصبح هذه القوائم متوفرة ومرئية عبر الإنترنت وعلى الوحدات الطرفية لنقاط البيع (POS).‬</span><span class="sxs-lookup"><span data-stu-id="463c1-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="463c1-125">في حاله إيقاف تشغيل الميزة، لا تتأثر الأنواع الأخرى من توصيات المنتج بذلك.</span><span class="sxs-lookup"><span data-stu-id="463c1-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="463c1-126">لمزيد من المعلومات حول توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="463c1-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="463c1-127">إضافة زر وصف تسوق منتجات مماثلة إلى صفحات تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="463c1-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="463c1-128">بعد تشغيل ميزة توصيات "وصف تسوق منتجات مماثلة"‬، في مركز Commerce الرئيسي، يمكنك إضافة الزر **وصف تسوق منتجات مماثلة** إلى مربع الشراء في أي صفحة من صفحات تفاصيل المنتجات (PDP).</span><span class="sxs-lookup"><span data-stu-id="463c1-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="463c1-129">يُنقل العميل الذي يحدد هذا الزر إلى صفحة **تسوق منتجات مماثلة** مخصصة تعرض منتجات مماثلة مرئيًا.</span><span class="sxs-lookup"><span data-stu-id="463c1-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="463c1-130">ويمكن للعميل استخدام المحددات لإجراء المزيد من عمليات التصفية على المنتجات.</span><span class="sxs-lookup"><span data-stu-id="463c1-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="463c1-131">لإضافة زر **وصف تسوق منتجات مماثلة**‫ إلى إحدى صفحات تفاصيل المنتجات باستخدام منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="463c1-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="463c1-132">افتح صفحة منشئ مواقع موجودة تحتوي على وحدة مربع شراء.</span><span class="sxs-lookup"><span data-stu-id="463c1-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="463c1-133">في جزء التنقل الأيسر، حدد وحدة مربع الشراء.</span><span class="sxs-lookup"><span data-stu-id="463c1-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="463c1-134">في جزء التنقل الأيمن، حدد خانة الاختيار **ارتباط وصف تسوق منتجات مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="463c1-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="463c1-135">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="463c1-135">Select **Save**.</span></span>
1. <span data-ttu-id="463c1-136">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="463c1-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="463c1-137">بعد نشر الصفحة، ستتضمن صفحة تفاصيل المنتج PDP الزر **وصف تسوق منتجات مماثلة**.</span><span class="sxs-lookup"><span data-stu-id="463c1-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="463c1-138">يبين الرسم التوضيحي التالي خانة الاختيار **ارتباط وصف تسوق منتجات مماثلة** والزر **وصف تسوق منتجات مماثلة** على مثال صفحة تفاصيل المنتج PDP في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="463c1-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![تمكين خانة الاختيار "ارتباط وصف تسوق منتجات مماثلة" والزر "وصف تسوق منتجات مماثلة" على صفحة تفاصيل المنتج PDP في منشئ المواقع.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="463c1-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="463c1-140">Additional resources</span></span>

[<span data-ttu-id="463c1-141">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="463c1-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="463c1-142">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="463c1-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="463c1-143">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="463c1-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="463c1-144">تمكين توصيات "تسوق أشكال مماثلة"</span><span class="sxs-lookup"><span data-stu-id="463c1-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="463c1-145">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="463c1-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="463c1-146">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="463c1-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="463c1-147">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="463c1-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]