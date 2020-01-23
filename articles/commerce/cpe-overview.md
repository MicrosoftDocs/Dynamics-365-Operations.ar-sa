---
title: نظرة عامة على بيئة معاينة التجارة
description: يقدم هذا الموضوع نظرة عامة على بيئة معاينة Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906060"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="9ca62-103">نظرة عامة على بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="9ca62-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9ca62-104">يقدم هذا الموضوع نظرة عامة على بيئة معاينة Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9ca62-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="9ca62-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="9ca62-105">Overview</span></span>

<span data-ttu-id="9ca62-106">بيئة معاينة التجارة هي بيئة معاينة شاملة لـ Dynamics 365 Commerce تتيح للعملاء المحتملين تجربة منتج التجارة قبل صدوره بشكل عام للجمهور.</span><span class="sxs-lookup"><span data-stu-id="9ca62-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="9ca62-107">بصرف النظر عن بعض القيود البسيطة التي لا تؤثر على الميزات أو الوظائف، توفر بيئة معاينة التجارة تجربة التجارة الكاملة، ويمكن استخدامها من قبل العملاء وشركاء التنفيذ لتقييم المنتج ، وتقديم الملاحظات ، وتحليل الملاءمة / الفجوة.</span><span class="sxs-lookup"><span data-stu-id="9ca62-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="9ca62-108">قيود بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="9ca62-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="9ca62-109">على الرغم من أن بيئة معاينة التجارة توفر مجموعة كاملة من ميزات ووظائف التجارة، إلا أن هناك بعض القيود الثانوية:</span><span class="sxs-lookup"><span data-stu-id="9ca62-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="9ca62-110">على الرغم من أن بيئة معاينة التجارة نفسها لا تحتوي على قيود جغرافية، إلا أنه لا يمكن توفير مكونات البيئة، مثل Retail Cloud Scale Unit (RCSU) وتطبيقات التجارة الإلكترونية، إلا في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="9ca62-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="9ca62-111">يقتصر استخدام بيئة المعاينة التجارية على مهلة 30 يومًا من تاريخ توفير التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9ca62-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="9ca62-112">يمكن نشر بيئة معاينة التجارة بنجاح وتهيئتها فقط في بيئة تستخدم طوبولوجيا العرض التوضيحي، حيث يتم نشر جميع مكونات البيئة في جهاز ظاهري واحد (VM).</span><span class="sxs-lookup"><span data-stu-id="9ca62-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="9ca62-113">القيد الرئيسي لمخطط الجهاز الظاهري OneBox هو عدد المستخدمين المتزامنين الذين يمكن أن تدعمهم بيئة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="9ca62-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="9ca62-114">لا يمكن تقييم بيئة معاينة التجارة إلا إلى أن يكون التوافر العام (GA) لمنتج التجارة.</span><span class="sxs-lookup"><span data-stu-id="9ca62-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="9ca62-115">ستكون البيئات التجريبية الجديدة متاحة بعد التوافر العام.</span><span class="sxs-lookup"><span data-stu-id="9ca62-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="9ca62-116">البدء</span><span class="sxs-lookup"><span data-stu-id="9ca62-116">Get started</span></span>

<span data-ttu-id="9ca62-117">لتوفير بيئة معاينة التجارة، راجع [توفير بيئة معاينة التجارة](provisioning-guide.md)</span><span class="sxs-lookup"><span data-stu-id="9ca62-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ca62-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9ca62-118">Additional resources</span></span>

[<span data-ttu-id="9ca62-119">توفير بيئة معاينة Commerce</span><span class="sxs-lookup"><span data-stu-id="9ca62-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="9ca62-120">تكوين بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="9ca62-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="9ca62-121">تكوين الميزات الاختيارية لبيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="9ca62-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9ca62-122">الأسئلة المتداولة حول بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="9ca62-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
