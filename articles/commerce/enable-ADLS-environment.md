---
title: تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage لبيئة Dynamics 365 Commerce، وهو عبارة عن شرط أساسي لتمكين توصيات المنتج.
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
ms.openlocfilehash: 83b829306c2da2d10924e547fd3cac6ae6781db3
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404176"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="707ef-103">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="707ef-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="707ef-104">يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage لبيئة Dynamics 365 Commerce، وهو عبارة عن شرط أساسي لتمكين توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="707ef-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="707ef-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="707ef-105">Overview</span></span>

<span data-ttu-id="707ef-106">في الحل Dynamics 365 Commerce، يتم تعقب كل المنتجات والحركات في مخزن كيانات البيئة.</span><span class="sxs-lookup"><span data-stu-id="707ef-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="707ef-107">لتمكين وصول هذه البيانات لخدمات Dynamics 365 الأخرى، مثل تحليلات البيانات والمعلومات المهنية والتوصيات المخصصة، من الضروري توصيل البيئة بحل Azure Data Lake Storage Gen 2 الذي يملكه العميل.</span><span class="sxs-lookup"><span data-stu-id="707ef-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="707ef-108">مع تكوين Azure Data Lake Storage لبيئة، يتم إجراء نسخ متطابق لكل البيانات الضرورية من مخزن الوحدات وهي لا تزال محمية وخاضعة لمراقبة العميل.</span><span class="sxs-lookup"><span data-stu-id="707ef-108">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="707ef-109">في حالة تمكين توصيات المنتجات‬ أو التوصيات المخصصة أيضًا في البيئة، سيتم منح مكدس توصيات المنتجات إمكانية الوصول إلى المجلد المخصص في Azure Data Lake Storage لاسترداد بيانات العميل وحساب التوصيات استنادًا إليه.</span><span class="sxs-lookup"><span data-stu-id="707ef-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="707ef-110">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="707ef-110">Prerequisites</span></span>

<span data-ttu-id="707ef-111">يحتاج العملاء إلى تكوين Azure Data Lake Storage في أحد اشتراكات Azure التي يملكونها.</span><span class="sxs-lookup"><span data-stu-id="707ef-111">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="707ef-112">لا يتناول هذا الموضوع شراء اشتراك Azure أو إعداد حساب تخزين تم تمكين Azure Data Lake Storage له.</span><span class="sxs-lookup"><span data-stu-id="707ef-112">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="707ef-113">لمزيد من المعلومات حول Azure Data Lake Storage، راجع [ وثائق Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="707ef-113">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="707ef-114">خطوات التكوين</span><span class="sxs-lookup"><span data-stu-id="707ef-114">Configuration steps</span></span>

<span data-ttu-id="707ef-115">يغطي هذا القسم خطوات التكوين الضرورية لتمكين Azure Data Lake Storage في بيئة ما كما يتعلق بتوصيات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="707ef-115">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="707ef-116">للحصول على نظرة عامة أكثر عمقًا للخطوات المطلوبة لتمكين Azure Data Lake Storage، راجع [جعل مخزن الكيانات‬ متوفرًا كـ Data Lake‬](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="707ef-116">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="707ef-117">تمكين Azure Data Lake Storage في البيئة</span><span class="sxs-lookup"><span data-stu-id="707ef-117">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="707ef-118">سجل الدخول إلى مدخل المكتب الخلفي للبيئة.</span><span class="sxs-lookup"><span data-stu-id="707ef-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="707ef-119">ابحث عن **معلمات النظام** وانتقل إلى علامة التبويب **اتصالات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="707ef-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="707ef-120">عيِّن **تمكين تكامل Data Lake** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="707ef-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="707ef-121">عيِّن **تحديث Data Lake بشكل تدريجي** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="707ef-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="707ef-122">ثم أدخل المعلومات المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="707ef-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="707ef-123">**معرف التطبيق** // **سر التطبيق** // **اسم DNS** - مطلوب للاتصال ب KeyVault حيث يتم تخزين سر Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="707ef-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="707ef-124">**اسم السر** - اسم السر المخزن في KeyVault والمستخدم للمصادقة مع Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="707ef-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="707ef-125">احفظ التغييرات في الجزء العلوي الأيمن من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="707ef-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="707ef-126">تعرض الصورة التالية مثالاً لتكوين Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="707ef-126">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![مثال لتكوين Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="707ef-128">اختبار اتصال Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="707ef-128">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="707ef-129">اختبار الاتصال بـ KeyVault باستخدام ارتباط **اختبار Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="707ef-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="707ef-130">اختبر اتصال Azure Data Lake Storage باستخدام ارتباط **اختبار Azure Storage**.</span><span class="sxs-lookup"><span data-stu-id="707ef-130">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="707ef-131">في حالة فشل الاختبارات، تحقق مرة أخرى من صحة كل معلومات KeyVault المضافة أعلاه، ثم حاول مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="707ef-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="707ef-132">بمجرد نجاح اختبارات الاتصال، يجب تمكين التحديث التلقائي لمخزن الوحدات.</span><span class="sxs-lookup"><span data-stu-id="707ef-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="707ef-133">لتمكين التحديث التلقائي لمخزن الكيانات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="707ef-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="707ef-134">ابحث عن **مخزن الكيانات**.</span><span class="sxs-lookup"><span data-stu-id="707ef-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="707ef-135">في القائمة الموجودة على اليمين، انتقل إلى إدخال **RetailSales**، وحدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="707ef-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="707ef-136">تأكد من تعيين **تم تمكين التحديث التلقائي** على القيمة **نعم**، وحدد **تحديث**، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="707ef-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="707ef-137">تعرض الصورة التالية مثالاً لمخزن الكيانات مع تمكين التحديث التلقائي.</span><span class="sxs-lookup"><span data-stu-id="707ef-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![مثال على مخزن الكيانات مع تمكين التحديث التلقائي](./media/exampleADLSConfig2.png)

<span data-ttu-id="707ef-139">تم الآن تكوين Azure Data Lake Storage للبيئة.</span><span class="sxs-lookup"><span data-stu-id="707ef-139">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="707ef-140">في حالة عدم الاكتمال بالفعل، اتبع الخطوات [لتمكين توصيات المنتج والتخصيص](enable-product-recommendations.md) للبيئة.</span><span class="sxs-lookup"><span data-stu-id="707ef-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="707ef-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="707ef-141">Additional resources</span></span>

[<span data-ttu-id="707ef-142">جعل مخزن الكيانات‬ متوفرًا كـ Data Lake</span><span class="sxs-lookup"><span data-stu-id="707ef-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="707ef-143">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="707ef-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="707ef-144">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="707ef-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="707ef-145">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="707ef-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="707ef-146">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="707ef-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="707ef-147">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="707ef-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="707ef-148">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="707ef-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="707ef-149">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="707ef-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="707ef-150">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="707ef-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="707ef-151">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="707ef-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="707ef-152">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="707ef-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
