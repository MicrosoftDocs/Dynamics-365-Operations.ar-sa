---
title: تمكين توصيات المنتجات المخصصة
description: يصف هذا الموضوع كيفيه جعل توصيات المنتج المخصصة متوفرة للعملاء في Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bdb56a1f45cdea1832bd269502e534efdb207b03
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127895"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="bce9c-103">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="bce9c-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bce9c-104">يصف هذا الموضوع كيفيه جعل توصيات المنتج المخصصة متوفرة للعملاء في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bce9c-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bce9c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="bce9c-105">Overview</span></span>

<span data-ttu-id="bce9c-106">وفي Dynamics 365 Commerce، يمكن لبائعي التجزئة اجراء توصيات للمنتجات الشخصية (والتي تعرف أيضا بالتخصيص) المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="bce9c-107">وبهذه الطريقة ، يمكن دمج التوصيات الشخصية في تجربه العميل عبر الإنترنت وفي نقطه البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="bce9c-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="bce9c-108">عند تشغيل وظيفة إضفاء الطابع الشخصي ، يمكن للنظام ربط معلومات الشراء والمنتج الخاصة بالمستخدم لإنشاء توصيات منتج إينديفيدواليزيد.</span><span class="sxs-lookup"><span data-stu-id="bce9c-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="bce9c-109">متطلبات التخصيص</span><span class="sxs-lookup"><span data-stu-id="bce9c-109">Personalization prerequisites</span></span>

<span data-ttu-id="bce9c-110">قبل توفير توصيات المنتج المخصصة للعملاء ، لاحظ ان توصيات المنتج معتمده فقط للمستخدمين التجاريين الذين قاموا بترحيل التخزين إلى متجر Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="bce9c-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="bce9c-111">قبل ان يتمكن العملاء من تلقي توصيات لمنتجات مخصصه، يجب على بائعي التجزئة [تشغيل توصيات المنتجات](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="bce9c-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="bce9c-112">وبتشغيل توصيات المنتج ، فانك تقوم أيضا بتشغيل التخصيص.</span><span class="sxs-lookup"><span data-stu-id="bce9c-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="bce9c-113">ومع ذلك ، إذا قمت بإيقاف تشغيل إضفاء الطابع الشخصي ، فلن تقوم بإيقاف تشغيل الأنواع الأخرى من توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="bce9c-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="bce9c-114">لمزيد من المعلومات حول توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="bce9c-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="bce9c-115">تشغيل التخصيص</span><span class="sxs-lookup"><span data-stu-id="bce9c-115">Turn on personalization</span></span>

<span data-ttu-id="bce9c-116">لتشغيل التخصيص‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bce9c-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="bce9c-117">انتقل إلى ‏‫‏‫**Retail and commerce \> توصيات المنتج \> معلمات التوصية**.</span><span class="sxs-lookup"><span data-stu-id="bce9c-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="bce9c-118">في قائمة معلمات Retail المشتركة، حدد **قوائم التوصيات**.</span><span class="sxs-lookup"><span data-stu-id="bce9c-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="bce9c-119">عيّن الخيار **تمكين التخصيص** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="bce9c-119">Set the **Enable personalization** option to **Yes**.</span></span>

![تشغيل التخصيص](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="bce9c-121">عند تشغيل إضفاء الطابع الشخصي ، يتم بدء عمليه إنشاء قوائم توصيات المنتج المخصصة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="bce9c-122">قد يكون مطلوبا حتى يوم واحد قبل ان تكون هذه القوائم متاحه ومرئية عبر الإنترنت وفي نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="bce9c-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="bce9c-123">القوائم المخصصة</span><span class="sxs-lookup"><span data-stu-id="bce9c-123">Personalized lists</span></span>

<span data-ttu-id="bce9c-124">بالإضافة إلى السماح بتخصيص القوائم التي تم إنشاؤها بالجهاز ، تسمح خدمه التوصيات بإضفاء طابع شخصي على خبره اكتشاف المنتج عبر الإنترنت وفي نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="bce9c-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="bce9c-125">وبعد تشغيل التخصيص ، يمكن لبائعي التجزئة إظهار قوائم المتسوقين المخصصة لقوائم الاتصالات الخاصة بك عبر الإنترنت أو "مستحسن للعميل" في المحطات الطرفية لنقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="bce9c-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="bce9c-126">بالإضافة إلى ذلك ، يمكن لبائعي التجزئة تطبيق التخصيص على قوائم توصيات المنتج الموجودة وتوفير جدبر الاشتراك العامة الخاصة بالمستخدمين المصادقين.</span><span class="sxs-lookup"><span data-stu-id="bce9c-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="bce9c-127">إذا قمت بإيقاف تشغيل التخصيص ، فانه يمكنك أيضا إيقاف تشغيل هذه الميزات.</span><span class="sxs-lookup"><span data-stu-id="bce9c-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="bce9c-128">قوائم "العناصر المقترحة" على الإنترنت لك</span><span class="sxs-lookup"><span data-stu-id="bce9c-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="bce9c-129">تعد قائمة  "اختيارات لك" هي قائمة  "التعرف على المعلومات الصناعية" (AI-ML) التي تعرض مستخدم مصادق قائمة  مخصصه من المنتجات المقترحة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="bce9c-130">تستند هذه القائمة إلى محفوظات شراء القناة متعددة الاتجاهات الخاصة بالمستخدم.</span><span class="sxs-lookup"><span data-stu-id="bce9c-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="bce9c-131">يتم تحديث التوصيات المخصصة بشكل حيوي عندما يقوم المستخدم بإنشاء المزيد من عمليات الشراء.</span><span class="sxs-lookup"><span data-stu-id="bce9c-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="bce9c-132">يدعم هذا النوع من القوائم أيضا تصفيه الفئة ، بحيث يمكن لبائعي التجزئة إظهار أفضل الاختيارات ، استنادا إلى التسلسلات الهرمية للتنقل.</span><span class="sxs-lookup"><span data-stu-id="bce9c-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="bce9c-133">قبل ان تظهر قائمة  "اختيارات لك" على إيه صفحه تجاره الكترونيه ، يجب الوفاء بمتطلبات المستخدم التالية:</span><span class="sxs-lookup"><span data-stu-id="bce9c-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="bce9c-134">يجب ان يقوم المستخدمون بتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="bce9c-134">Users must be signed in.</span></span> <span data-ttu-id="bce9c-135">لن يتمكن المستخدمون المجهولون من رؤية توصيات مخصصه.</span><span class="sxs-lookup"><span data-stu-id="bce9c-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="bce9c-136">يجب ان يكون لدي المستخدمين شراء واحد على الأقل على الحساب الخاص بهم.</span><span class="sxs-lookup"><span data-stu-id="bce9c-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="bce9c-137">يجب ان يقوم المستخدمون بالاشتراك لتلقي توصيات مخصصه.</span><span class="sxs-lookup"><span data-stu-id="bce9c-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="bce9c-138">يبين الرسم التوضيحي التالي مثالا على قائمة  "الاختيارات الخاصة بك" في صفحه المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="bce9c-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![قائمة العناصر المقترحة على الإنترنت لك](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="bce9c-140">قوائم "الموصي بها للعميل" عند نقطه البيع</span><span class="sxs-lookup"><span data-stu-id="bce9c-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="bce9c-141">لتحسين تجربه إعداد قاعدة العملاء‬ الخاصة بهم ، يمكن لبائعي التجزئة تخصيص صفحات تفاصيل العميل الموجودة عن طريق أضافه قائمة  "مستحسنه للعميل".</span><span class="sxs-lookup"><span data-stu-id="bce9c-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="bce9c-142">يبين الرسم التوضيحي التالي مثالا لقائمة "الموصى به للعميل في الوحدة الطرفية لنقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="bce9c-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![قائمة الموصي بها للعميل عند نقطه البيع](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="bce9c-144">تطبيق التخصيص على قوائم التوصيات الموجودة</span><span class="sxs-lookup"><span data-stu-id="bce9c-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="bce9c-145">يمكن لبائعي التجزئة تطبيق التخصيص على قوائم التوصيات الموجودة ، مثل "جديد" و"المتداول" و"الأفضل مبيعًا" و"الأخاص يحبون ذلك أيضًا" و"تم الشراء بشكل متكرر".</span><span class="sxs-lookup"><span data-stu-id="bce9c-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="bce9c-146">عند تطبيق التخصيص على القوائم الموجودة ، فان الأصناف التي اشترها مستخدم مسجل للدخول مسبقا يتم ازالتها من تلك القوائم.</span><span class="sxs-lookup"><span data-stu-id="bce9c-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="bce9c-147">بالنسبة لكل من المستخدمين المجهولين والمستخدمين الذين الغيوا الخروج من التوصيات المخصصة ، يتم عرض الإصدارات الافتراضية للقوائم الموجودة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="bce9c-148">التالي ، لا يلزم على بائعي التجزئة الاحتفاظ يدويا بخبرات الصفحة المنفصلة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="bce9c-149">علي سبيل المثال ، قام مستخدم مسجل للدخول مسبقا بشراء المراقب الأسود وتشغيل البنية التي تظهر في قائمة  "الافتراضي المتداول" في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="bce9c-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="bce9c-150">التالي ، سيشاهد المستخدم المنتجات الجديدة بدلا من تلك المنتجات ، كما هو موضح في قائمة  "التخصيص المتداول".</span><span class="sxs-lookup"><span data-stu-id="bce9c-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![تطبيق إضفاء الطابع الشخصي](./media/applypersonalization.png)

<span data-ttu-id="bce9c-152">لتطبيق إضفاء الطابع الشخصي على قائمة  توصيات موجودة في منشئ موقع التجارة ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bce9c-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bce9c-153">فتح صفحه منشئ موقع موجودة تحتوي على وحده نمطيه لمجموعه منتجات.</span><span class="sxs-lookup"><span data-stu-id="bce9c-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="bce9c-154">في جزء التنقل الأيسر، حدد وحدة تجميع المنتج.</span><span class="sxs-lookup"><span data-stu-id="bce9c-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="bce9c-155">في جزء التنقل الأيمن، ضمن **المنتجات**، حدد القائمة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="bce9c-156">في مربع الحوار **تحديد تكوين قائمة المنتجات**، ضمن  **النوع**، حدد نوع القائمة.</span><span class="sxs-lookup"><span data-stu-id="bce9c-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="bce9c-157">حدد خانة الاختيار **تطبيق التخصيص**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bce9c-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![تطبيق التخصيص على قائمة  متداوله](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="bce9c-159">احفظالصفحة وقم بانهاء تحريريها، ثم انشرها.</span><span class="sxs-lookup"><span data-stu-id="bce9c-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="bce9c-160">بعد نشر الصفحة، سيرة المستخدمون المسجل دخولهم قوائم متداوله مخصصه.</span><span class="sxs-lookup"><span data-stu-id="bce9c-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bce9c-161">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bce9c-161">Additional resources</span></span>

[<span data-ttu-id="bce9c-162">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="bce9c-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="bce9c-163">تمكين ADLS في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bce9c-163">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="bce9c-164">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="bce9c-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="bce9c-165">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="bce9c-165">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="bce9c-166">إضافة قوائم توصيات المنتجات إلى موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="bce9c-166">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="bce9c-167">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="bce9c-167">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="bce9c-168">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="bce9c-168">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="bce9c-169">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="bce9c-169">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="bce9c-170">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="bce9c-170">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="bce9c-171">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="bce9c-171">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="bce9c-172">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="bce9c-172">Product recommendations FAQ</span></span>](faq-recommendations.md)
