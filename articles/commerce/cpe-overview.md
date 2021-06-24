---
title: نظرة عامة على بيئة تقييم Dynamics 365 Commerce
description: يقدم هذا الموضوع نظرة عامة على بيئة تقييم Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c890d7c49b6607ab0cbad536bbf8a3649465a7c1
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193482"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="fbe37-103">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fbe37-104">يقدم هذا الموضوع نظرة عامة على بيئة تقييم Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbe37-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="fbe37-105">لا تتوفر بيئات تقييم Commerce بشكل عام، ويتم منحها للشركاء والعملاء على أساس كل طلب.</span><span class="sxs-lookup"><span data-stu-id="fbe37-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="fbe37-106">لمزيد من المعلومات، اتصل بجهة اتصال شريك Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fbe37-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="fbe37-107">بيئة تقييم Commerce هي بيئة اختيارية شاملة لـ Dynamics 365 Commerce تتيح للشركاء والعملاء المحتملين تجربة منتج Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbe37-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="fbe37-108">يتم تكوين بيئات التقييم مسبقًا بشكل جزئي لتقليل الخطوات التالية للتوفير المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="fbe37-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="fbe37-109">بصرف النظر عن بعض القيود البسيطة التي لا تؤثر على الميزات أو الوظائف، توفر بيئة تقييم Commerce تجربة Commerce بالكامل، ويمكن للعملاء وشركاء التنفيذ استخدامها لتقييم المنتج وتقديم الملاحظات وإجراء تحليل الملاءمة/الفروق.</span><span class="sxs-lookup"><span data-stu-id="fbe37-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="fbe37-110">قيود بيئة تقييم Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="fbe37-111">على الرغم من توفير بيئة تقييم Commerce مجموعة كاملة من ميزات Commerce ووظائفها، إلا أن هناك بعض القيود الثانوية:</span><span class="sxs-lookup"><span data-stu-id="fbe37-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="fbe37-112">على الرغم من عدم احتواء بيئة تقييم Commerce نفسها على قيود جغرافية، إلا أنه لا ينبغي توفير مكونات البيئة، مثل Retail Cloud Scale Unit (RCSU) وتطبيقات التجارة الإلكترونية، إلا في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="fbe37-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="fbe37-113">يوجد حد زمني لاستخدام بيئة تقييم Commerce بقيمة 30 يومًا من تاريخ توفير التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="fbe37-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="fbe37-114">لا يمكن نشر بيئة تقييم Commerce وتهيئتها بنجاح إلا في بيئة تستخدم مخطط العرض التوضيحي، حيث يتم نشر جميع مكونات البيئة في جهاز ظاهري واحد (VM) مُستضاف في سحابة.</span><span class="sxs-lookup"><span data-stu-id="fbe37-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="fbe37-115">والقيد الرئيسي للمخطط هو عدد المستخدمين المتزامنين الذين يمكن أن تدعمهم البيئة.</span><span class="sxs-lookup"><span data-stu-id="fbe37-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="fbe37-116">بدء الاستخدام</span><span class="sxs-lookup"><span data-stu-id="fbe37-116">Get started</span></span>

<span data-ttu-id="fbe37-117">لتوفير بيئة تقييم Commerce، راجع [توفير بيئة تقييم Commerce](provisioning-guide.md)</span><span class="sxs-lookup"><span data-stu-id="fbe37-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbe37-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fbe37-118">Additional resources</span></span>

[<span data-ttu-id="fbe37-119">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="fbe37-120">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="fbe37-121">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="fbe37-122">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="fbe37-123">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fbe37-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
