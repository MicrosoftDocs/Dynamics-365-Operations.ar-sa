---
title: إضافة توصيات المنتجات على نقطة البيع
description: ‏‫يصف هذا الموضوع استخدام توصيات المنتج على جهاز نقطه البيع (POS).
author: bebeale
manager: AnnBe
ms.date: 05/26/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a1dc1e8934bcd6a8cb94b780bbfe247f64067912
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404246"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="c15c5-103">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="c15c5-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c15c5-104">‏‫في أساسه، تُعد توصيات المنتج بمثابة أحد تطبيقات الاعمال التحويلية الذي يمتد عبر جميع مساحات التجارة لخلق تجارب اكتشاف منتج غنية وجذابة ومخصصة.</span><span class="sxs-lookup"><span data-stu-id="c15c5-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="c15c5-105">لتطبيق هذه الميزة في نقطه البيع، اتبع الخطوات الخاصة [بكيفية إضافة توصيات إلى أجهزة نقطة البيع.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="c15c5-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="c15c5-106">لمزيد من المعلومات حول ميزات توصيات المنتجات، راجع [نظرة عامة على توصيات المنتجات.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="c15c5-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="c15c5-107">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="c15c5-107">Scenarios</span></span>

<span data-ttu-id="c15c5-108">يتم تمكين توصيات المنتج لسيناريوهات نقطة البيع التالية.</span><span class="sxs-lookup"><span data-stu-id="c15c5-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="c15c5-109">تتوافر في نقطة بيع المجموعة (POS) أو نقطة بيع حديثة (MPOS).</span><span class="sxs-lookup"><span data-stu-id="c15c5-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="c15c5-110">في صفحة **تفاصيل المنتجات**:</span><span class="sxs-lookup"><span data-stu-id="c15c5-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="c15c5-111">إذا قام شريك في المتجر بزيارة صفحة **تفاصيل المنتج** عند النظر في الحركات السابقة عبر القنوات المختلفة، فإن خدمة التوصيات تقترح بنود إضافية والتي من المرجح شرائها معًا.</span><span class="sxs-lookup"><span data-stu-id="c15c5-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="c15c5-112">[![التوصيات في صفحة تفاصيل المنتج](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="c15c5-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="c15c5-113">في صفحة **الحركة**:</span><span class="sxs-lookup"><span data-stu-id="c15c5-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="c15c5-114">يقوم محرك التوصيات باقتراح الأصناف التي تستند إلى قائمة الأصناف بأكملها في السلة التي يتم شراؤها بشكل متكرر معًا.</span><span class="sxs-lookup"><span data-stu-id="c15c5-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c15c5-115">لعرض التوصيات على صفحة **الحركة**، يحتاج تاجر التجزئة إلى تحديث تخطيط الشاشة في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c15c5-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c15c5-116">يجب إسقاط عنصر تحكم **التوصيات** داخل صفحة **الحركة** .</span><span class="sxs-lookup"><span data-stu-id="c15c5-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="c15c5-117">[![التوصيات في صفحة الحركة](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="c15c5-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="c15c5-118">تكوين Commerce لتمكين توصيات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="c15c5-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="c15c5-119">لإعداد توصيات المنتج‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="c15c5-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="c15c5-120">تأكد من تحديث الخدمة الخاصة بك **للإصدار 10.0.6.**</span><span class="sxs-lookup"><span data-stu-id="c15c5-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="c15c5-121">اتبع الإرشادات حول كيفية [تمكين توصيات المنتج](../commerce/enable-product-recommendations.md) لأعمالك.</span><span class="sxs-lookup"><span data-stu-id="c15c5-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="c15c5-122">اختياري: لعرض التوصيات على شاشة الحركة، انتقل إلى **تخطيط الشاشة**، واختر تخطيط الشاشة وابدأ تشغيل **مصمم تخطيط الشاشة**، ثم قم بإفلات عنصر تحكم **التوصيات** حيث تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="c15c5-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="c15c5-123">انتقل إلى **معلمات Commerce**، وحدد **التعلم الآلي**، ثم حدد **نعم** ضمن **تمكين توصيات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="c15c5-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="c15c5-124">لمشاهدة التوصيات في نقطة البيع، قم بتشغيل وظيفة التكوين العمومي **1110**.</span><span class="sxs-lookup"><span data-stu-id="c15c5-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="c15c5-125">لعكس التغييرات التي تم إجراؤها لمصم تخطيط شاشة نقطة البيع، قم بتشغيل وظيفة تكوين قناة **1070**.</span><span class="sxs-lookup"><span data-stu-id="c15c5-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="c15c5-126">استكشاف الأخطاء وإصلاحها التي يكون لك فيها توصيات منتج مُمكنة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="c15c5-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="c15c5-127">انتقل إلى **معلمات Commerce‬** \> **قوائم التوصيات** \> **تعطيل توصيات المنتج** وقم بتشغيل **وظيفة التكوين العمومي \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="c15c5-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="c15c5-128">إذا قمت بإضافة **عناصر التحكم في التوصيات** إلى شاشة الحركة الخاصة بك باستخدام **مصمم تخطيط الشاشة**، الرجاء إزالتها أيضًا.</span><span class="sxs-lookup"><span data-stu-id="c15c5-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="c15c5-129">إذا كانت لديك المزيد من الاستفسارات، وللحصول على المزيد من المعلومات، راجع [الاسئلة المتداولة حول توصيات المنتجات](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c15c5-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c15c5-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c15c5-130">Additional resources</span></span>

[<span data-ttu-id="c15c5-131">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="c15c5-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c15c5-132">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c15c5-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="c15c5-133">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="c15c5-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c15c5-134">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="c15c5-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c15c5-135">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="c15c5-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="c15c5-136">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="c15c5-136">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c15c5-137">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="c15c5-137">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c15c5-138">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="c15c5-138">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c15c5-139">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="c15c5-139">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="c15c5-140">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="c15c5-140">Product recommendations FAQ</span></span>](faq-recommendations.md)
