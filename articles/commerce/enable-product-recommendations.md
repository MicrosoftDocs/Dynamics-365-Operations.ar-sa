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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770129"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="6c23f-103">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="6c23f-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6c23f-104">يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c23f-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="6c23f-105">لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="6c23f-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="6c23f-106">توصيات قبل الفحص</span><span class="sxs-lookup"><span data-stu-id="6c23f-106">Recommendations pre-check</span></span>
<span data-ttu-id="6c23f-107">قبل التمكين، يرجى ملاحظ أن توصيات المنتج مدعومة فقط بالنسبة لعملاء F&O الذي يدعم الإصدار 10.0.6 وقد قمت بترحيل التخزين الخاص بهم إلى باستخدام BDL.</span><span class="sxs-lookup"><span data-stu-id="6c23f-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="6c23f-108">بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale.</span><span class="sxs-lookup"><span data-stu-id="6c23f-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="6c23f-109">لمعرفه المزيد حول عملية الإعداد هذه، انتقل إلى [هنا.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="6c23f-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="6c23f-110">تشغيل التوصيات</span><span class="sxs-lookup"><span data-stu-id="6c23f-110">Turn on recommendations</span></span>

<span data-ttu-id="6c23f-111">لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6c23f-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="6c23f-112">انتقل إلى **‏‫‏‫Retail‬‬** &gt; **توصيات المنتج** &gt; **معلمات التوصية**.</span><span class="sxs-lookup"><span data-stu-id="6c23f-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="6c23f-113">في قائمه معلمات البيع بالتجزئة المشتركة، حدد **قوائم التوصيات**.</span><span class="sxs-lookup"><span data-stu-id="6c23f-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="6c23f-114">عيّن الخيار **تمكين التوصيات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="6c23f-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![تمكين توصيات المنتجات](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="6c23f-116">يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج.</span><span class="sxs-lookup"><span data-stu-id="6c23f-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="6c23f-117">قد تكون هناك حاجة إلى عدة ساعات قبل توفر القوائم ويمكن رؤيتها في نقطة البيع (POS) أو في Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c23f-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="6c23f-118">تكوين معلمات قائمه التوصيات</span><span class="sxs-lookup"><span data-stu-id="6c23f-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="6c23f-119">بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة.</span><span class="sxs-lookup"><span data-stu-id="6c23f-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="6c23f-120">يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك.</span><span class="sxs-lookup"><span data-stu-id="6c23f-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="6c23f-121">لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="6c23f-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="6c23f-122">إظهار التوصيات علي أجهزة نقاط البيع</span><span class="sxs-lookup"><span data-stu-id="6c23f-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="6c23f-123">بعد تمكين التوصيات في مكتب الدعم، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطه البيع بواسطة أداة التخطيط.</span><span class="sxs-lookup"><span data-stu-id="6c23f-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="6c23f-124">لمعرفه المزيد حول هذه العملية، انتقل إلى [هنا.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="6c23f-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6c23f-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6c23f-125">Additional resources</span></span>

[<span data-ttu-id="6c23f-126">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="6c23f-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6c23f-127">إضافة قوائم توصيات المنتجات إلى الصفحات</span><span class="sxs-lookup"><span data-stu-id="6c23f-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="6c23f-128">إضافة لوحة التوصيات إلى أجهزة نقاط البيع</span><span class="sxs-lookup"><span data-stu-id="6c23f-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


