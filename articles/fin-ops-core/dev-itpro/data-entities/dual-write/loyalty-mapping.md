---
title: بطاقات ولاء العملاء ونقاط المكافآت
description: يصف هذا الموضوع تكامل البيانات حول بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998003"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="e30f0-103">بطاقات ولاء العملاء ونقاط المكافآت</span><span class="sxs-lookup"><span data-stu-id="e30f0-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e30f0-104">تعمل الشركات على تصنيف العملاء وتوفير خدمات معقدة، استنادًا إلى أنماط تسوق وانفاق العميل.</span><span class="sxs-lookup"><span data-stu-id="e30f0-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="e30f0-105">في مجموعة تطبيقات Microsoft Dynamics 365 ، لدى Dynamics 365 Commerce البنية الأساسية والوظائف لتسهيل ومعالجة بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت والتسعير المستند إلى الولاء وخبرات الشراء المستندة إلى المكافآت.</span><span class="sxs-lookup"><span data-stu-id="e30f0-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="e30f0-106">عند مزامنة بيانات حول بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت في Commerce مع Common Data service، فإن التطبيقات المستندة إلى النماذج في Dynamics 365 يمكنها استخدام هذه البيانات.</span><span class="sxs-lookup"><span data-stu-id="e30f0-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="e30f0-107">على سبيل المثال، يستطيع مستخدمو Dynamics 365 Customer Service استخدام البيانات لتوفير نفس الخدمات المعقدة من خلال مركز المساعدة.</span><span class="sxs-lookup"><span data-stu-id="e30f0-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="e30f0-108">القوالب</span><span class="sxs-lookup"><span data-stu-id="e30f0-108">Templates</span></span>

| <span data-ttu-id="e30f0-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e30f0-109">Finance and Operations apps</span></span> | <span data-ttu-id="e30f0-110">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e30f0-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e30f0-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e30f0-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="e30f0-112">بطاقة الولاء</span><span class="sxs-lookup"><span data-stu-id="e30f0-112">Loyalty card</span></span>                | <span data-ttu-id="e30f0-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="e30f0-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="e30f0-114">يقوم هذا القالب بمزامنة معلومات بطاقات ولاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="e30f0-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="e30f0-115">نقاط مكافآت الولاء</span><span class="sxs-lookup"><span data-stu-id="e30f0-115">Loyalty reward points</span></span>       | <span data-ttu-id="e30f0-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="e30f0-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="e30f0-117">يقوم هذا القالب بمزامنة معلومات نقاط مكافآت العملاء.</span><span class="sxs-lookup"><span data-stu-id="e30f0-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
