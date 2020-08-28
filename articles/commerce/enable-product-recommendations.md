---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2dacd4a94f706be5aa65947c0b6a92e281733ca
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665016"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="011bf-103">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="011bf-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="011bf-104">يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="011bf-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="011bf-105">لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="011bf-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="011bf-106">توصيات قبل الفحص</span><span class="sxs-lookup"><span data-stu-id="011bf-106">Recommendations pre-check</span></span>

<span data-ttu-id="011bf-107">قبل التمكين، يرجى العلم أن توصيات المنتج غير مدعومة إلا لعملاء Commerce ممن قاموا بترحيل مساحة التخزين باستخدام Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="011bf-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="011bf-108">يجب تمكين التكوينات التالية في المكتب الخلفي قبل تمكين التوصيات:</span><span class="sxs-lookup"><span data-stu-id="011bf-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="011bf-109">تأكد من شراء Azure Data Lake Storage والتحقق منه في البيئة بنجاح.</span><span class="sxs-lookup"><span data-stu-id="011bf-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="011bf-110">لمزيد من المعلومات، راجع [التأكد من شراء Azure Data Lake Storage والتحقق منه في البيئة بنجاح](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="011bf-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="011bf-111">التأكد من تعيين التنفيذ التلقائي لتحديث مخزن الكيانات‬.</span><span class="sxs-lookup"><span data-stu-id="011bf-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="011bf-112">لمزيد من المعلومات، راجع [التأكد من تعيين التنفيذ التلقائي لتحديث مخزن الكيانات](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="011bf-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="011bf-113">التأكد من أن تكوين الهوية في Azure AD يحتوي على إدخال للتوصيات.</span><span class="sxs-lookup"><span data-stu-id="011bf-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="011bf-114">توجد أدناه معلومات اضافيه حول كيفية تنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="011bf-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="011bf-115">بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale.</span><span class="sxs-lookup"><span data-stu-id="011bf-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="011bf-116">لمعرفة المزيد عن عملية الإعداد هذه، راجع [التعامل مع المقاييس](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="011bf-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="011bf-117">تكوين الهوية في Azure AD</span><span class="sxs-lookup"><span data-stu-id="011bf-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="011bf-118">هذه الخطوة مطلوبة لجميع العملاء الذين يقومون بتشغيل بنية تحتية على أنها تكوين كخدمة (IaaS).</span><span class="sxs-lookup"><span data-stu-id="011bf-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="011bf-119">بالنسبة إلى العملاء الذين يقومون بتشغيل Service Fabric (SF)، يجب أن تكون هذه الخطوة تلقائية، وننصح بالتحقق من تكوين الإعداد كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="011bf-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="011bf-120">الإعداد</span><span class="sxs-lookup"><span data-stu-id="011bf-120">Setup</span></span>

1. <span data-ttu-id="011bf-121">من المكتب الخلفي، ابحث عن صفحة **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="011bf-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="011bf-122">تحقق من وجود إدخال لـ "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="011bf-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="011bf-123">في حال عدم وجود الإدخال، أضف إدخالاً جديدًا يتضمن المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="011bf-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="011bf-124">**معرف العميل** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="011bf-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="011bf-125">**الاسم‏‎** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="011bf-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="011bf-126">**معرف المستخدم** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="011bf-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="011bf-127">احفظ الصفحة وإغلاقها.</span><span class="sxs-lookup"><span data-stu-id="011bf-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="011bf-128">تشغيل التوصيات</span><span class="sxs-lookup"><span data-stu-id="011bf-128">Turn on recommendations</span></span>

<span data-ttu-id="011bf-129">لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="011bf-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="011bf-130">انتقل إلى ‏‫‏‫**البيع بالتجزئة والتجارة&gt; توصيات المنتج &gt; معلمات التوصية**.</span><span class="sxs-lookup"><span data-stu-id="011bf-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="011bf-131">في قائمة المعلمات المشتركة، حدد **قوائم التوصيات**.</span><span class="sxs-lookup"><span data-stu-id="011bf-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="011bf-132">عيّن الخيار **تمكين التوصيات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="011bf-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![تشغيل التوصيات](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="011bf-134">يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="011bf-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="011bf-135">قد تحتاج إلى عدة ساعات قبل أن تصبح القوائم متوفرة ويمكن عرضها في نقطة البيع أو في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="011bf-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="011bf-136">تكوين معلمات قائمة التوصيات</span><span class="sxs-lookup"><span data-stu-id="011bf-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="011bf-137">بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة.</span><span class="sxs-lookup"><span data-stu-id="011bf-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="011bf-138">يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك.</span><span class="sxs-lookup"><span data-stu-id="011bf-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="011bf-139">لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="011bf-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="011bf-140">إظهار التوصيات على أجهزة نقاط البيع</span><span class="sxs-lookup"><span data-stu-id="011bf-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="011bf-141">بعد تمكين التوصيات في مكتب دعم Commerce، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطة البيع بواسطة أداة التخطيط.</span><span class="sxs-lookup"><span data-stu-id="011bf-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="011bf-142">لمعرفه المزيد حول هذه العملية، راجع [إضافة عنصر تحكم التوصيات إلى شاشة الحركات على أجهزة نقطة البيع](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="011bf-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="011bf-143">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="011bf-143">Enable personalized recommendations</span></span>

<span data-ttu-id="011bf-144">وفي Dynamics 365 Commerce، يمكن لبائعي التجزئة إجراء توصيات للمنتجات الشخصية (والتي تعرف أيضا بالتخصيص) المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="011bf-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="011bf-145">وبهذه الطريقة، يمكن دمج التوصيات الشخصية في تجربه العميل عبر الإنترنت وفي نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="011bf-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="011bf-146">عند تشغيل وظيفة إضفاء الطابع الشخصي، يمكن للنظام ربط معلومات الشراء والمنتج الخاصة بالمستخدم لإنشاء توصيات منتج إينديفيدواليزيد.</span><span class="sxs-lookup"><span data-stu-id="011bf-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="011bf-147">لمعرفة المزيد حول كيفية تلقي توصيات مخصصة، راجع [تمكين التوصيات المخصصة](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="011bf-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="011bf-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="011bf-148">Additional resources</span></span>

[<span data-ttu-id="011bf-149">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="011bf-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="011bf-150">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="011bf-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="011bf-151">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="011bf-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="011bf-152">تمكين توصيات "تسوق منتجات تبدو مماثلة"</span><span class="sxs-lookup"><span data-stu-id="011bf-152">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="011bf-153">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="011bf-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="011bf-154">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="011bf-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="011bf-155">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="011bf-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="011bf-156">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="011bf-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="011bf-157">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="011bf-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="011bf-158">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="011bf-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="011bf-159">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="011bf-159">Product recommendations FAQ</span></span>](faq-recommendations.md)

