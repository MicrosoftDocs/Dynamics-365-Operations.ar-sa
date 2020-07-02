---
title: إنشاء توصيات بواسطة بيانات العرض التوضيحي
description: يوفر هذا الموضوع إرشادات حول كيفية الاستفادة من توصيات منتج القناة متعددة الاتجاهات القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي القابلة للتخصيص والتي تمت تعبئتها بشكل مسبق.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 59b4dd7a29af739d92a20f6fe55eff9f201fcb6d
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454546"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="07892-103">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="07892-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="07892-104">يوفر هذا الموضوع إرشادات حول كيفية الاستفادة من توصيات منتج القناة متعددة الاتجاهات القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي القابلة للتخصيص والتي تمت تعبئتها بشكل مسبق.</span><span class="sxs-lookup"><span data-stu-id="07892-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="07892-105">توفر توصيات المنتج متعدد القنوات مجموعة من قوائم المنتجات تم إنشاؤها بشكل تحريري أو برمجيًا.</span><span class="sxs-lookup"><span data-stu-id="07892-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="07892-106">يمكن استخدام هذه القوائم في العديد من السيناريوهات، وفقًا لاحتياجات العمل.</span><span class="sxs-lookup"><span data-stu-id="07892-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="07892-107">لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="07892-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="07892-108">بالنسبة لبيئات المنتجات من المستوي 2 وما أعلي، وبيئات Dynamics 365، تُحتسب توصيات منتج البيئات الديناميكية تلقائيًا بناء على بيانات العملاء.</span><span class="sxs-lookup"><span data-stu-id="07892-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="07892-109">لا يؤدي استخدام البيانات التوضيحية لتوصيات المنتج إلى تعطيل اي حل توصيات للمنتج تم توفيرها بالفعل في البيئة وآية تكاليف مرتبطة باستخدامها.</span><span class="sxs-lookup"><span data-stu-id="07892-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="07892-110">بالنسبة لبيئات المستوي 1، تستند توصيات المنتج فقط على بيانات العرض التوضيحي الثابتة المخزنة في ملف csv..</span><span class="sxs-lookup"><span data-stu-id="07892-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="07892-111">تمكين بيانات العرض التوضيحي لتوصيات المنتج في البيئة</span><span class="sxs-lookup"><span data-stu-id="07892-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="07892-112">لتمكين بيانات العرض التوضيحي لتوصيات المنتج، تحتاج إلى نشر ملحق العرض التوضيحي للمعاينة لـ Dynamics 365 Commerce للبيئة المعينة.</span><span class="sxs-lookup"><span data-stu-id="07892-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="07892-113">يؤدي ذلك إلى تمكين بيانات العرض التوضيحي لتوصيات المنتج تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="07892-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="07892-114">بيانات العرض التوضيحي الافتراضية</span><span class="sxs-lookup"><span data-stu-id="07892-114">Default demo data</span></span>
<span data-ttu-id="07892-115">تأتي كل بيئة من النوع OneBox مع مجموعة من بيانات العرض التوضيحي لتوصيات المنتج التي تم تحميلها مسبقًا من ملف ‘reco_demo_data.csv’ المفصول بوسطة فاصلة، والموجود في Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="07892-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="07892-116">يتم هيكلة هذه البيانات بمحاذاة الأعمده التالية.</span><span class="sxs-lookup"><span data-stu-id="07892-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="07892-117">اسم العمود</span><span class="sxs-lookup"><span data-stu-id="07892-117">Column name</span></span>         | <span data-ttu-id="07892-118">إلزامي</span><span class="sxs-lookup"><span data-stu-id="07892-118">Mandatory</span></span>          | <span data-ttu-id="07892-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="07892-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="07892-120">القيم المحتملة</span><span class="sxs-lookup"><span data-stu-id="07892-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="07892-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="07892-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="07892-123">إنشاء نوع قائمة توصيات المنتج المحدد التي تشير إليها بيانات العرض التوضيحي منها.</span><span class="sxs-lookup"><span data-stu-id="07892-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="07892-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="07892-124">RecoBestSelling</span></span></li><li><span data-ttu-id="07892-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="07892-125">RecoNew</span></span></li><li><span data-ttu-id="07892-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="07892-126">RecoTrending</span></span></li><li><span data-ttu-id="07892-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="07892-127">RecoCart</span></span></li><li><span data-ttu-id="07892-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="07892-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="07892-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="07892-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="07892-131">رقم وحدة التشغيل المحددة التي يُتوقع ظهور توصيات المنتج لها.</span><span class="sxs-lookup"><span data-stu-id="07892-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="07892-132">فئة</span><span class="sxs-lookup"><span data-stu-id="07892-132">Category</span></span>            |                    |    <span data-ttu-id="07892-133">الفئة التي يجب أن يتم إرجاع القائمة المحددة إليها.</span><span class="sxs-lookup"><span data-stu-id="07892-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="07892-134">في حالة عدم تحديد أية فئة، تكون القائمة أعلى ‏‫التدرج الهرمي للتنقل فقط.</span><span class="sxs-lookup"><span data-stu-id="07892-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="07892-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="07892-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="07892-136">بالنسبة للقوائم التي تتطلب إضافة (RecoPeopleAlsoBuy وRecoCart) المنتج، يجب أن تعرض هذه القوائم منتجات إضافية.</span><span class="sxs-lookup"><span data-stu-id="07892-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="07892-137">معرف العميل</span><span class="sxs-lookup"><span data-stu-id="07892-137">CustomerId</span></span>          |                    |    <span data-ttu-id="07892-138">للقوائم التي تتطلب معرف عميل (RecoPicks).</span><span class="sxs-lookup"><span data-stu-id="07892-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="07892-139">تنطبق القيمة الافتراضية '0' على كافة العملاء.</span><span class="sxs-lookup"><span data-stu-id="07892-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="07892-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="07892-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="07892-142">إرجاع منتج أو أكثر كنتيجة، مفصول بواسطة ';'.</span><span class="sxs-lookup"><span data-stu-id="07892-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="07892-143">تخصيص بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="07892-143">Customize demo data</span></span>
<span data-ttu-id="07892-144">يمكنك تحرير بيانات العرض التوضيحي الافتراضية بآيه معلومات حول المنتج والفئة التي تم تكوينها في HQ.</span><span class="sxs-lookup"><span data-stu-id="07892-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="07892-145">بعد تحديث ملف CSV.، تعكس توصيات المنتج التي يتم إرجاعها للعملاء التغييرات مباشرة.</span><span class="sxs-lookup"><span data-stu-id="07892-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="07892-146">يحتوي الملحق على ملف بيانات يسمي 'RecoMockDataset.csv'، يسمح لك بالتحكم في مجموعة البيانات المستخدمة لتشغيل نتائج توصيات وهمية.</span><span class="sxs-lookup"><span data-stu-id="07892-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="07892-147">يمكن التحكم في اسم الملف من خلال تكوين الملحق باستخدام إعداد **ext.Recommendations.DemoFilePath** .</span><span class="sxs-lookup"><span data-stu-id="07892-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="07892-148">ويؤدي ذلك إلى تمكينك من جعل مجموعات البيانات المتعددة متاحة ويمكن التبديل بينها بسهولة خل التكوين.</span><span class="sxs-lookup"><span data-stu-id="07892-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="07892-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="07892-149">Additional resources</span></span>

[<span data-ttu-id="07892-150">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="07892-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="07892-151">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="07892-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="07892-152">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="07892-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="07892-153">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="07892-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="07892-154">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="07892-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="07892-155">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="07892-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="07892-156">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="07892-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="07892-157">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="07892-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="07892-158">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="07892-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="07892-159">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="07892-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
