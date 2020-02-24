---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024946"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="a69b5-103">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a69b5-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a69b5-104">يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a69b5-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="a69b5-105">لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="a69b5-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="a69b5-106">توصيات قبل الفحص</span><span class="sxs-lookup"><span data-stu-id="a69b5-106">Recommendations pre-check</span></span>

<span data-ttu-id="a69b5-107">قبل التمكين، يرجى ملاحظة أن توصيات المنتج غير مدعومة إلا لعملاء Commerce ممن رحلوا التخزين الخاص بهم إلى باستخدام Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="a69b5-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="a69b5-108">لمعرفة خطوات تمكين ADLS، راجع [كيفية تمكين ADLS في بيئة Dynamics 365](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a69b5-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="a69b5-109">بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale.</span><span class="sxs-lookup"><span data-stu-id="a69b5-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="a69b5-110">لمعرفه المزيد حول عملية الإعداد هذه، انتقل إلى [هنا.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="a69b5-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="a69b5-111">تشغيل التوصيات</span><span class="sxs-lookup"><span data-stu-id="a69b5-111">Turn on recommendations</span></span>

<span data-ttu-id="a69b5-112">لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a69b5-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="a69b5-113">انتقل إلى ‏‫‏‫**البيع بالتجزئة والتجارة&gt; توصيات المنتج &gt; معلمات التوصية**.</span><span class="sxs-lookup"><span data-stu-id="a69b5-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="a69b5-114">في قائمة المعلمات المشتركة، حدد **قوائم التوصيات**.</span><span class="sxs-lookup"><span data-stu-id="a69b5-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="a69b5-115">عيّن الخيار **تمكين التوصيات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a69b5-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![تمكين توصيات المنتجات](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="a69b5-117">يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="a69b5-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="a69b5-118">قد تكون هناك حاجة إلى عدة ساعات قبل توفر القوائم ويمكن رؤيتها في نقطة البيع (POS) أو في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a69b5-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="a69b5-119">تكوين معلمات قائمه التوصيات</span><span class="sxs-lookup"><span data-stu-id="a69b5-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="a69b5-120">بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة.</span><span class="sxs-lookup"><span data-stu-id="a69b5-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="a69b5-121">يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك.</span><span class="sxs-lookup"><span data-stu-id="a69b5-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="a69b5-122">لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a69b5-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="a69b5-123">إظهار التوصيات علي أجهزة نقاط البيع</span><span class="sxs-lookup"><span data-stu-id="a69b5-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="a69b5-124">بعد تمكين التوصيات في مكتب دعم Commerce، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطة البيع بواسطة أداة التخطيط.</span><span class="sxs-lookup"><span data-stu-id="a69b5-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="a69b5-125">لمعرفه المزيد حول هذه العملية، راجع [إضافة عنصر تحكم التوصيات إلى شاشة الحركات على أجهزة نقطة البيع](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="a69b5-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="a69b5-126">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="a69b5-126">Enable personalized recommendations</span></span>

<span data-ttu-id="a69b5-127">لمعرفه المزيد حول كيفية تلقي توصيات مخصصة، راجع [تمكين التوصيات المخصصة](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a69b5-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a69b5-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a69b5-128">Additional resources</span></span>

[<span data-ttu-id="a69b5-129">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a69b5-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a69b5-130">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="a69b5-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a69b5-131">إضافة قوائم توصيات المنتجات إلى الصفحات</span><span class="sxs-lookup"><span data-stu-id="a69b5-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="a69b5-132">إضافة لوحة التوصيات إلى أجهزة نقاط البيع</span><span class="sxs-lookup"><span data-stu-id="a69b5-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a69b5-133">نظرة عامة على الوحدة النمطية لمجموعة المنتجات</span><span class="sxs-lookup"><span data-stu-id="a69b5-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="a69b5-134">تمكين ADLS في بيئة Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a69b5-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

