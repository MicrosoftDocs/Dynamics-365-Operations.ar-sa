---
title: أصول داخلية لإخضاعها للصيانة
description: يصف هذا الموضوع كيفية استخدام Microsoft Dynamics 365 Field Service لمعالجة أصول العميل والأصول الداخلية.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebc9c1fbb7c0738af13b2a16aafeeb03fa6aaed0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683995"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="94f45-103">أصول داخلية لإخضاعها للصيانة</span><span class="sxs-lookup"><span data-stu-id="94f45-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="94f45-104">تم تصميم Microsoft Dynamics 365 Field Service لصيانة أصول العميل.</span><span class="sxs-lookup"><span data-stu-id="94f45-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="94f45-105">تم تصميم إدارة الأصول في Dynamics 365 Supply Chain Management لصيانة الأصول الداخلية.</span><span class="sxs-lookup"><span data-stu-id="94f45-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="94f45-106">يسمح لك تكامل هذين التطبيقين باستخدام Field Service لصيانة أصول العميل والأصول الداخلية.</span><span class="sxs-lookup"><span data-stu-id="94f45-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="94f45-107">يمكنك أيضًا تصنيف الأصول، استنادًا إلى موقع العمل أو التدرج الهرمي، وتعقب الصيانة بشكل مفصل.</span><span class="sxs-lookup"><span data-stu-id="94f45-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="94f45-108">لمزيد من المعلومات، راجع [تكامل Dynamics 365 Field Service وSupply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="94f45-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="94f45-109">القوالب</span><span class="sxs-lookup"><span data-stu-id="94f45-109">Templates</span></span>

<span data-ttu-id="94f45-110">تتضمن الأصول الداخلية مجموعة من خرائط الجداول الرئيسية التي تعمل معًا أثناء تفاعل البيانات، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="94f45-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="94f45-111">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94f45-111">Finance and Operations apps</span></span> | <span data-ttu-id="94f45-112">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="94f45-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="94f45-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="94f45-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="94f45-114">نماذج دورة حياة الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="94f45-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="94f45-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="94f45-116">حالات دورة حياة الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="94f45-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="94f45-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="94f45-118">أصول إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-118">Asset management assets</span></span> | <span data-ttu-id="94f45-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="94f45-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="94f45-120">أنواع الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-120">Asset management asset types</span></span> | <span data-ttu-id="94f45-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="94f45-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="94f45-122">نماذج دورة حياة موقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="94f45-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="94f45-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="94f45-124">حالات دورة حياة موقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="94f45-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="94f45-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="94f45-126">مواقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-126">Asset management functional locations</span></span> | <span data-ttu-id="94f45-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="94f45-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="94f45-128">أنواع مواقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-128">Asset management functional location types</span></span> | <span data-ttu-id="94f45-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="94f45-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="94f45-130">الشركات المصنعة في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-130">Asset management manufacturers</span></span> | <span data-ttu-id="94f45-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="94f45-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="94f45-132">نماذج إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-132">Asset management models</span></span> | <span data-ttu-id="94f45-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="94f45-133">msdyn\_models</span></span> | |
| <span data-ttu-id="94f45-134">ضمان إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="94f45-134">Asset management warranty</span></span> | <span data-ttu-id="94f45-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="94f45-135">msdyn\_warranties</span></span> | |

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
