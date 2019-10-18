---
title: بيانات العرض التوضيحي لتوصيات منتج القناة متعددة الاتجاهات
description: يهدف هذا المستند إلى توفير إرشادات حول كيفية الاستفادة من توصيات المنتج متعدد القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي المعممة مسبقا.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225541"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="05c7f-103">بيانات العرض التوضيحي لتوصيات منتج القناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="05c7f-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="05c7f-104">يهدف هذا المستند إلى توفير إرشادات حول كيفية الاستفادة من توصيات المنتج متعدد القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي المعممة مسبقا.</span><span class="sxs-lookup"><span data-stu-id="05c7f-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="05c7f-105">توفر توصيات المنتج متعدد القنوات مجموعة من قوائم المنتجات المرتبة والتي تم إنشاؤها بشكل تحريري أو برمجيًا.</span><span class="sxs-lookup"><span data-stu-id="05c7f-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="05c7f-106">يمكن استخدام هذه القوائم في العديد من السيناريوهات، وفقًا لاحتياجات العمل.</span><span class="sxs-lookup"><span data-stu-id="05c7f-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="05c7f-107">لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [نظرة عامة على توصيات المنتجات.](product-recommendaitons-overview.md)</span><span class="sxs-lookup"><span data-stu-id="05c7f-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="05c7f-108">بالنسبة لبيئات المنتجات من المستوي 2 وما أعلي، تُحتسب توصيات منتج البيئات الديناميكية تلقائيًا بناء علي بيانات العملاء.</span><span class="sxs-lookup"><span data-stu-id="05c7f-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="05c7f-109">لا يؤدي استخدام البيانات التوضيحية لتوصيات المنتج إلى تعطيل اي حل توصيات للمنتج تم توفيرها بالفعل في البيئة وآية تكاليف مرتبطة باستخدامها.</span><span class="sxs-lookup"><span data-stu-id="05c7f-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="05c7f-110">بالنسبة لبيئات المستوي 1، تستند توصيات المنتج فقط على بيانات العرض التوضيحي الثابتة المخزنة في ملف csv.</span><span class="sxs-lookup"><span data-stu-id="05c7f-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="05c7f-111">تمكين بيانات العرض التوضيحي لتوصيات المنتج في البيئة</span><span class="sxs-lookup"><span data-stu-id="05c7f-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="05c7f-112">يحتاج العملاء إلى نشر **Dynamics 365 Commerce ملحق العرض التوضيحي للمعاينة** للبيئة المعنية، التي تمكن بيانات العرض التوضيحي لتوصيات المنتج تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="05c7f-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="05c7f-113">بيانات العرض التوضيحي الافتراضية</span><span class="sxs-lookup"><span data-stu-id="05c7f-113">Default demo data</span></span>
<span data-ttu-id="05c7f-114">تأتي كل بيئة من النوع Onebox مع مجموعه من بيانات العرض التوضيحي لتوصيات المنتج التي تم تحميلها مسبقًا من ملف **‘reco_demo_data.csv’** المفصول بالنقاط، والموجود في نفس مجلد هذا المستند علي خادم Retail.</span><span class="sxs-lookup"><span data-stu-id="05c7f-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="05c7f-115">يتم هيكلة هذه البيانات بمحاذاة الاعمده التالية</span><span class="sxs-lookup"><span data-stu-id="05c7f-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="05c7f-116">اسم العمود</span><span class="sxs-lookup"><span data-stu-id="05c7f-116">Column name</span></span>         | <span data-ttu-id="05c7f-117">إلزامي</span><span class="sxs-lookup"><span data-stu-id="05c7f-117">Mandatory</span></span>          | <span data-ttu-id="05c7f-118">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="05c7f-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="05c7f-119">القيم المحتملة</span><span class="sxs-lookup"><span data-stu-id="05c7f-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="05c7f-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="05c7f-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="05c7f-122">إنشاء نوع قائمه توصيات المنتج المحدد التي تشير إليها بيانات العرض التوضيحي منها.</span><span class="sxs-lookup"><span data-stu-id="05c7f-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="05c7f-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="05c7f-123">RecoBestSelling</span></span></li><li><span data-ttu-id="05c7f-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="05c7f-124">RecoNew</span></span></li><li><span data-ttu-id="05c7f-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="05c7f-125">RecoTrending</span></span></li><li><span data-ttu-id="05c7f-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="05c7f-126">RecoCart</span></span></li><li><span data-ttu-id="05c7f-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="05c7f-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="05c7f-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="05c7f-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="05c7f-130">رقم وحدة التشغيل المحددة التي يُتوقع ظهور توصيات المنتج لها.</span><span class="sxs-lookup"><span data-stu-id="05c7f-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="05c7f-131">فئة</span><span class="sxs-lookup"><span data-stu-id="05c7f-131">Category</span></span>            |                    |    <span data-ttu-id="05c7f-132">الفئة التي يجب أن يتم إرجاع القائمة المحددة إليها.</span><span class="sxs-lookup"><span data-stu-id="05c7f-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="05c7f-133">في حالة عدم تحديد أية فئة، تكون القائمة أعلى ‏‫التدرج الهرمي للتنقل فقط.</span><span class="sxs-lookup"><span data-stu-id="05c7f-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="05c7f-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="05c7f-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="05c7f-135">بالنسبة للقوائم التي تتطلب إضافة (RecoPeopleAlsoBuy وRecoCart) المنتج، يجب أن تعرض هذه القوائم منتجات إضافية.</span><span class="sxs-lookup"><span data-stu-id="05c7f-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="05c7f-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="05c7f-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="05c7f-138">وكنتيجة إذا تم إرجاع واحد أو أكثر من المنتجات، يتم الفصل بينهم بالعمة **‘;’**.</span><span class="sxs-lookup"><span data-stu-id="05c7f-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="05c7f-139">تخصيص بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="05c7f-139">Customize demo data</span></span>
<span data-ttu-id="05c7f-140">يمكن للعملاء تحرير بيانات العرض التوضيحي الافتراضية بآيه معلومات حول المنتج والفئة التي تم تكوينها في HQ.</span><span class="sxs-lookup"><span data-stu-id="05c7f-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="05c7f-141">بمجرد تحديث الملف CSV، تعكس توصيات المنتج التي يتم إرجاعها للعملاء التغييرات مباشرة.</span><span class="sxs-lookup"><span data-stu-id="05c7f-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="05c7f-142">يحتوي الملحق علي ملف بيانات يسمي RecoMockDataset.csv والذي يسمح للعميل بالتحكم في مجموعه البيانات المستخدمة لتشغيل نتائج توصيات وهمية.</span><span class="sxs-lookup"><span data-stu-id="05c7f-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="05c7f-143">يمكن التحكم في اسم الملف من خلال تكوين الملحق باستخدام إعداد **ext.Recommendations.DemoFilePath** .</span><span class="sxs-lookup"><span data-stu-id="05c7f-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="05c7f-144">ويؤدي ذلك إلى تمكين العملاء من جعل مجموعات البيانات المتعددة متاحة ويمكن التبديل بينها بسهولة خل التكوين.</span><span class="sxs-lookup"><span data-stu-id="05c7f-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="05c7f-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="05c7f-145">Additional resources</span></span>

[<span data-ttu-id="05c7f-146">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="05c7f-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="05c7f-147">تخطيط بيئة</span><span class="sxs-lookup"><span data-stu-id="05c7f-147">Environment planning</span></span>](environment-planning.md)
