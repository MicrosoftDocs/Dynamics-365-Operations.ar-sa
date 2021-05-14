---
title: أصول داخلية لإخضاعها للصيانة
description: يصف هذا الموضوع كيف يمكنك استخدام Microsoft Dynamics 365 Field Service لخدمة أصول العملاء والأصول الداخلية.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941404"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="757ac-103">أصول داخلية لإخضاعها للصيانة</span><span class="sxs-lookup"><span data-stu-id="757ac-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="757ac-104">تم تصميم Microsoft Dynamics 365 Field Service لخدمة أصول العميل.</span><span class="sxs-lookup"><span data-stu-id="757ac-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="757ac-105">تم تصميم إدارة الأصول في Dynamics 365 Supply Chain Management لصيانة الأصول الداخلية.</span><span class="sxs-lookup"><span data-stu-id="757ac-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="757ac-106">يسمح لك تكامل هذين التطبيقين باستخدام Field Service لصيانة أصول العميل والأصول الداخلية.</span><span class="sxs-lookup"><span data-stu-id="757ac-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="757ac-107">يمكنك أيضًا تصنيف الأصول، استنادًا إلى موقع العمل أو التدرج الهرمي، وتعقب الصيانة بشكل مفصل.</span><span class="sxs-lookup"><span data-stu-id="757ac-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="757ac-108">لمزيد من المعلومات، راجع [تكامل Dynamics 365 Field Service وSupply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="757ac-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="757ac-109">القوالب</span><span class="sxs-lookup"><span data-stu-id="757ac-109">Templates</span></span>

<span data-ttu-id="757ac-110">تتضمن الأصول الداخلية مجموعة من خرائط الجداول الرئيسية التي تعمل معًا أثناء تفاعل البيانات، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="757ac-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="757ac-111">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="757ac-111">Finance and Operations apps</span></span> | <span data-ttu-id="757ac-112">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="757ac-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="757ac-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="757ac-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="757ac-114">نماذج دورة حياة الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="757ac-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="757ac-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="757ac-116">حالات دورة حياة الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="757ac-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="757ac-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="757ac-118">أصول إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-118">Asset management assets</span></span> | <span data-ttu-id="757ac-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="757ac-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="757ac-120">أنواع الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-120">Asset management asset types</span></span> | <span data-ttu-id="757ac-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="757ac-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="757ac-122">نماذج دورة حياة موقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="757ac-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="757ac-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="757ac-124">حالات دورة حياة موقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="757ac-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="757ac-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="757ac-126">مواقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-126">Asset management functional locations</span></span> | <span data-ttu-id="757ac-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="757ac-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="757ac-128">أنواع مواقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-128">Asset management functional location types</span></span> | <span data-ttu-id="757ac-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="757ac-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="757ac-130">الشركات المصنعة في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-130">Asset management manufacturers</span></span> | <span data-ttu-id="757ac-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="757ac-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="757ac-132">نماذج إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-132">Asset management models</span></span> | <span data-ttu-id="757ac-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="757ac-133">msdyn\_models</span></span> | |
| <span data-ttu-id="757ac-134">ضمان إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="757ac-134">Asset management warranty</span></span> | <span data-ttu-id="757ac-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="757ac-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]