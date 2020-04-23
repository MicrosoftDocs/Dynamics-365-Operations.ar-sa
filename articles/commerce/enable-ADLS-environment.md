---
title: تمكين ADLS في بيئة Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage (ADLS) لإحدى بيئات Dynamics 365 Commerce، والتي تعتبر متطلبًا أساسيًا لتمكين توصيات المنتج.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259738"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="8229f-103">تمكين ADLS في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8229f-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8229f-104">يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage (ADLS) لإحدى بيئات Dynamics 365 Commerce، والتي تعتبر متطلبًا أساسيًا لتمكين توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="8229f-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="8229f-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8229f-105">Overview</span></span>

<span data-ttu-id="8229f-106">في الحل Dynamics 365 Commerce، يتم تعقب كل المنتجات والحركات في مخزن كيانات البيئة.</span><span class="sxs-lookup"><span data-stu-id="8229f-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="8229f-107">لتمكين وصول هذه البيانات لخدمات Dynamics 365 الأخرى، مثل تحليلات البيانات والمعلومات المهنية والتوصيات المخصصة، من الضروري توصيل البيئة بحل Azure Data Lake Storage (ADLS) المملوك للعميل من الجيل الثاني.</span><span class="sxs-lookup"><span data-stu-id="8229f-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="8229f-108">بتكوين ADLS لإحدى البيئات، يتم إجراء نسخًا متطابقًا لكل البيانات الضرورية من مخزن الوحدات أثناء حمايتها والاحتفاظ بها في تحكم العميل.</span><span class="sxs-lookup"><span data-stu-id="8229f-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="8229f-109">في حالة تمكين توصيات المنتج أو التوصيات المخصصة أيضًا في البيئة، سيتم منح مكدس توصيات المنتجات إمكانية الوصول إلى المجلد المخصص في ADLS لاسترداد بيانات العميل وحساب التوصيات استنادًا إليه.</span><span class="sxs-lookup"><span data-stu-id="8229f-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8229f-110">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="8229f-110">Prerequisites</span></span>

<span data-ttu-id="8229f-111">يحتاج العملاء إلى تكوين ADLS في أحد اشتراكات Azure التي يملكونها.</span><span class="sxs-lookup"><span data-stu-id="8229f-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="8229f-112">لا يتناول هذا الموضوع شراء اشتراك Azure أو إعداد حساب تخزين تم تمكين ADLS له.</span><span class="sxs-lookup"><span data-stu-id="8229f-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="8229f-113">لمزيد من المعلومات حول ADLS، راجع [وثائق ADLS الرسمية](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="8229f-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="8229f-114">خطوات التكوين</span><span class="sxs-lookup"><span data-stu-id="8229f-114">Configuration steps</span></span>

<span data-ttu-id="8229f-115">يغطي هذا القسم خطوات التكوين الضرورية لتمكين ADLS في بيئة ما كما يتعلق بتوصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="8229f-115">This section covers the configuration steps necessary for enabling ADLS in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="8229f-116">للحصول على نظرة عامة أكثر عمقًا للخطوات المطلوبة لتمكين ADLS، راجع [جعل مخزن الكيانات‬ متوفرًا كـ Data Lake‬](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="8229f-116">For a more in-depth overview of the steps required to enable ADLS, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="8229f-117">تمكين ADLS في البيئة</span><span class="sxs-lookup"><span data-stu-id="8229f-117">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="8229f-118">سجل الدخول إلى مدخل المكتب الخلفي للبيئة.</span><span class="sxs-lookup"><span data-stu-id="8229f-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="8229f-119">ابحث عن **معلمات النظام** وانتقل إلى علامة التبويب **اتصالات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="8229f-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="8229f-120">عيِّن **تمكين تكامل Data Lake** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8229f-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="8229f-121">عيِّن **تحديث Data Lake بشكل تدريجي** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8229f-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="8229f-122">ثم أدخل المعلومات المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="8229f-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="8229f-123">**معرف التطبيق** // **سر التطبيق** // **اسم DNS** - المطلوب للاتصال ب KeyVault حيث يتم تخزين سر ADLS.</span><span class="sxs-lookup"><span data-stu-id="8229f-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="8229f-124">**الاسم السري** - الاسم السري المخزن في KeyVault والمستخدم للمصادقة مع ADLS.</span><span class="sxs-lookup"><span data-stu-id="8229f-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="8229f-125">احفظ التغييرات في الجزء العلوي الأيمن من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8229f-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="8229f-126">تعرض الصورة التالية مثالاً لتكوين ADLS.</span><span class="sxs-lookup"><span data-stu-id="8229f-126">The following image shows an example ADLS configuration.</span></span>

![مثال لتكوين ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="8229f-128">اختبار اتصال ADLS</span><span class="sxs-lookup"><span data-stu-id="8229f-128">Test the ADLS connection</span></span>

1. <span data-ttu-id="8229f-129">اختبار الاتصال بـ KeyVault باستخدام ارتباط **اختبار Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="8229f-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="8229f-130">اختبار الاتصال بـ ADLS باستخدام ارتباط **اختبار Azure Storage**.</span><span class="sxs-lookup"><span data-stu-id="8229f-130">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="8229f-131">في حالة فشل الاختبارات، تحقق مرة أخرى من صحة كل معلومات KeyVault المضافة أعلاه، ثم حاول مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="8229f-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="8229f-132">بمجرد نجاح اختبارات الاتصال، يجب تمكين التحديث التلقائي لمخزن الوحدات.</span><span class="sxs-lookup"><span data-stu-id="8229f-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="8229f-133">لتمكين التحديث التلقائي لمخزن الكيانات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8229f-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="8229f-134">ابحث عن **مخزن الكيانات**.</span><span class="sxs-lookup"><span data-stu-id="8229f-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="8229f-135">في القائمة الموجودة على اليمين، انتقل إلى إدخال **RetailSales**، وحدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8229f-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="8229f-136">تأكد من تعيين **تم تمكين التحديث التلقائي** على القيمة **نعم**، وحدد **تحديث**، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8229f-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="8229f-137">تعرض الصورة التالية مثالاً لمخزن الكيانات مع تمكين التحديث التلقائي.</span><span class="sxs-lookup"><span data-stu-id="8229f-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![مثال على مخزن الكيانات مع تمكين التحديث التلقائي](./media/exampleADLSConfig2.png)

<span data-ttu-id="8229f-139">تم تكوين ADLS الآن للبيئة.</span><span class="sxs-lookup"><span data-stu-id="8229f-139">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="8229f-140">في حالة عدم الاكتمال بالفعل، اتبع الخطوات [لتمكين توصيات المنتج والتخصيص](enable-product-recommendations.md) للبيئة.</span><span class="sxs-lookup"><span data-stu-id="8229f-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8229f-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8229f-141">Additional resources</span></span>

[<span data-ttu-id="8229f-142">جعل مخزن الكيانات‬ متوفرًا كـ Data Lake</span><span class="sxs-lookup"><span data-stu-id="8229f-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="8229f-143">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="8229f-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8229f-144">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="8229f-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8229f-145">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="8229f-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8229f-146">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="8229f-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8229f-147">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="8229f-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8229f-148">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="8229f-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8229f-149">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="8229f-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8229f-150">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="8229f-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8229f-151">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="8229f-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8229f-152">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="8229f-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
