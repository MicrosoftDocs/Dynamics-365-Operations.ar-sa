---
title: نظرة عامة على التقييمات والمراجعات
description: يغطي هذا الموضوع التقييمات والمراجعات في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 45a6710a10fe3d33457c1327c8fc339c9ad0082a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698178"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="f5969-103">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f5969-103">Ratings and reviews overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f5969-104">يغطي هذا الموضوع التقييمات والمراجعات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f5969-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f5969-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="f5969-105">Overview</span></span>

<span data-ttu-id="f5969-106">تُعد التقييمات والمراجعات ضرورية لعملاء التجارة الإلكترونية الذين يريدون معرفة رأي العملاء الآخرين في المنتج.</span><span class="sxs-lookup"><span data-stu-id="f5969-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="f5969-107">كما يمكنهم أيضًا مساعدة العملاء على اتخاذ قرارات في الشراء.</span><span class="sxs-lookup"><span data-stu-id="f5969-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="f5969-108">في Dynamics 365 Commerce، يتيح حل التقييمات والمراجعات لبائعي التجزئة بالحصول على مراجعات وتقييمات المنتجات من العملاء.</span><span class="sxs-lookup"><span data-stu-id="f5969-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="f5969-109">يمكن لبائعي التجزئة حينها عرض متوسط التقييمات ومراجعة المعلومات عبر موقع الويب الخاص بالتجارة الإكترونية.</span><span class="sxs-lookup"><span data-stu-id="f5969-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="f5969-110">يتم عرض متوسط معلومات التصنيف بنقطة بيع (POS) وقنوات مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="f5969-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="f5969-111">وبالتالي، فان إقرانات المبيعات يمكن استخدامها لمساعدة المستخدمين في اتخاذ قرارات.</span><span class="sxs-lookup"><span data-stu-id="f5969-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="f5969-112">كذلك، يمكن أن تمثل التقييمات والمراجعات آلية ملاحظات يمكن لبائعي التجزئة استخدامها لتحسين جودة منتج وبالتالي زيادة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f5969-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="f5969-113">تُعد وظيفة التقييمات والمراجعات Dynamics 365 Commerce حلاً متعدد الاتجاهات وتكون متوفرة أصلاً كجزء من النظام الأساسي.</span><span class="sxs-lookup"><span data-stu-id="f5969-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="f5969-114">ويستند حل التقييمات والمراجعات إلى أعلى Microsoft Azure، والذي يقدم إمكانية التوسع والموثوقية العالية.</span><span class="sxs-lookup"><span data-stu-id="f5969-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="f5969-115">يبين الرسم التوضيحي التالي كيفية عمل حل التقييمات والمراجعات في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f5969-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![التقييمات والمراجعات في Dynamics 365 for Commerce](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="f5969-117">يستخدم حل التقييمات والمراجعات في Dynamics 365 Commerce Azure Cognitive Services لتقديم الإشراف التلقائي على الكلمات البذيئة بـ 40 لغة.</span><span class="sxs-lookup"><span data-stu-id="f5969-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="f5969-118">ونظرًا لأن الموافقة البشرية غير مطلوبة، يتم تقليل الإشراف.</span><span class="sxs-lookup"><span data-stu-id="f5969-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="f5969-119">كما يوفر النظام أدوات المشرف التي يمكن استخدامها للاستجابة إلى الطلبات الخاصة بالعملاء والملاحظات والطلبات التي يتم إجراؤها ومعالجة طلبات البيانات من المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f5969-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="f5969-120">يوفر حل التقييمات والمراجعات الأدوات التي تُظهر ملخصات التقييم في قوائم المنتجات وفي نتائج البحث وفي صفحة تفاصيل المنتج وفي أماكن أخرى.</span><span class="sxs-lookup"><span data-stu-id="f5969-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="f5969-121">وتقوم الأدوات بإظهار قوائم المراجعة الكاملة، كما توفر خيارات الفرز والتصفية.</span><span class="sxs-lookup"><span data-stu-id="f5969-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="f5969-122">يوفر حل التقييمات والمراجعات أيضًا قالب المعلومات المهنية (BI) الذي يتضمن مجموعة من المقاييس لتوفير الرؤى في التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="f5969-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="f5969-123">يمكن تصدير بيانات التقييمات والمراجعات للحصول على تحليل إضافي.</span><span class="sxs-lookup"><span data-stu-id="f5969-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5969-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f5969-124">Additional resources</span></span>

[<span data-ttu-id="f5969-125">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f5969-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f5969-126">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f5969-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="f5969-127">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="f5969-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="f5969-128">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="f5969-128">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
