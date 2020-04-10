---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154403"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="7b57f-103">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="7b57f-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b57f-104">يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7b57f-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="7b57f-105">لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="7b57f-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="7b57f-106">توصيات قبل الفحص</span><span class="sxs-lookup"><span data-stu-id="7b57f-106">Recommendations pre-check</span></span>

<span data-ttu-id="7b57f-107">قبل التمكين، يرجى ملاحظة أن توصيات المنتج غير مدعومة إلا لعملاء Commerce ممن رحلوا التخزين الخاص بهم إلى باستخدام Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="7b57f-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="7b57f-108">لمعرفة خطوات تمكين ADLS، راجع [كيفية تمكين ADLS في بيئة Dynamics 365](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7b57f-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="7b57f-109">بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale.</span><span class="sxs-lookup"><span data-stu-id="7b57f-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="7b57f-110">لمعرفه المزيد حول عملية الإعداد هذه، انتقل إلى [هنا.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="7b57f-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="7b57f-111">تشغيل التوصيات</span><span class="sxs-lookup"><span data-stu-id="7b57f-111">Turn on recommendations</span></span>

<span data-ttu-id="7b57f-112">لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7b57f-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="7b57f-113">انتقل إلى ‏‫‏‫**البيع بالتجزئة والتجارة&gt; توصيات المنتج &gt; معلمات التوصية**.</span><span class="sxs-lookup"><span data-stu-id="7b57f-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="7b57f-114">في قائمة المعلمات المشتركة، حدد **قوائم التوصيات**.</span><span class="sxs-lookup"><span data-stu-id="7b57f-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="7b57f-115">عيّن الخيار **تمكين التوصيات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="7b57f-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![تمكين توصيات المنتجات](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="7b57f-117">يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="7b57f-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="7b57f-118">قد تكون هناك حاجة إلى عدة ساعات قبل توفر القوائم ويمكن رؤيتها في نقطة البيع (POS) أو في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7b57f-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="7b57f-119">تكوين معلمات قائمة  التوصيات</span><span class="sxs-lookup"><span data-stu-id="7b57f-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="7b57f-120">بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة.</span><span class="sxs-lookup"><span data-stu-id="7b57f-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="7b57f-121">يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك.</span><span class="sxs-lookup"><span data-stu-id="7b57f-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="7b57f-122">لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="7b57f-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="7b57f-123">إظهار التوصيات على أجهزة نقاط البيع</span><span class="sxs-lookup"><span data-stu-id="7b57f-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="7b57f-124">بعد تمكين التوصيات في مكتب دعم Commerce، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطة البيع بواسطة أداة التخطيط.</span><span class="sxs-lookup"><span data-stu-id="7b57f-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="7b57f-125">لمعرفه المزيد حول هذه العملية، راجع [إضافة عنصر تحكم التوصيات إلى شاشة الحركات على أجهزة نقطة البيع](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="7b57f-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="7b57f-126">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="7b57f-126">Enable personalized recommendations</span></span>

<span data-ttu-id="7b57f-127">لمعرفه المزيد حول كيفية تلقي توصيات مخصصة، راجع [تمكين التوصيات المخصصة](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="7b57f-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b57f-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7b57f-128">Additional resources</span></span>

[<span data-ttu-id="7b57f-129">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="7b57f-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="7b57f-130">تمكين ADLS في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7b57f-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="7b57f-131">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="7b57f-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="7b57f-132">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="7b57f-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="7b57f-133">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="7b57f-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="7b57f-134">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="7b57f-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="7b57f-135">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="7b57f-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="7b57f-136">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="7b57f-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="7b57f-137">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="7b57f-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="7b57f-138">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="7b57f-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

