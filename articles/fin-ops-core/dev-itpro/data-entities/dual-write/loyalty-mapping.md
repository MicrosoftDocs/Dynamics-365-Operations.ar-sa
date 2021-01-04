---
title: بطاقات ولاء العملاء ونقاط المكافآت
description: يصف هذا الموضوع تكامل البيانات حول بطاقات ولاء العملاء ونقاط المكافأة في الكتابة المزدوجة.
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
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683488"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="0be87-103">بطاقات ولاء العملاء ونقاط المكافآت</span><span class="sxs-lookup"><span data-stu-id="0be87-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0be87-104">تعمل الشركات على تصنيف العملاء وتوفير خدمات معقدة، استنادًا إلى أنماط تسوق وانفاق العميل.</span><span class="sxs-lookup"><span data-stu-id="0be87-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="0be87-105">على سبيل المثال، يشتمل Dynamics 365 Commerce على البنية الأساسية والوظائف لتسهيل ومعالجة بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت والتسعير المستند إلى الولاء وخبرات الشراء المستندة إلى المكافآت.</span><span class="sxs-lookup"><span data-stu-id="0be87-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="0be87-106">عند مزامنة بيانات حول بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت في Commerce مع Dataverse، فإن تطبيقات Customer Engagement يمكنها استخدام هذه البيانات.</span><span class="sxs-lookup"><span data-stu-id="0be87-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="0be87-107">على سبيل المثال، يستطيع مستخدمو Dynamics 365 Customer Service استخدام البيانات لتوفير نفس الخدمات المعقدة من خلال مركز المساعدة.</span><span class="sxs-lookup"><span data-stu-id="0be87-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="0be87-108">القوالب</span><span class="sxs-lookup"><span data-stu-id="0be87-108">Templates</span></span>

| <span data-ttu-id="0be87-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0be87-109">Finance and Operations apps</span></span> | <span data-ttu-id="0be87-110">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0be87-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="0be87-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0be87-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="0be87-112">بطاقة الولاء</span><span class="sxs-lookup"><span data-stu-id="0be87-112">Loyalty card</span></span>                | <span data-ttu-id="0be87-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="0be87-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="0be87-114">يقوم هذا القالب بمزامنة معلومات بطاقات ولاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="0be87-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="0be87-115">نقاط مكافآت الولاء</span><span class="sxs-lookup"><span data-stu-id="0be87-115">Loyalty reward points</span></span>       | <span data-ttu-id="0be87-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="0be87-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="0be87-117">يقوم هذا القالب بمزامنة معلومات نقاط مكافآت العملاء.</span><span class="sxs-lookup"><span data-stu-id="0be87-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
