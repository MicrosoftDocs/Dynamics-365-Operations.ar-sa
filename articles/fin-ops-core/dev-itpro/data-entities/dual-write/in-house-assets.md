---
title: أصول داخلية لإخضاعها للصيانة
description: يصف هذا الموضوع كيفية استخدام Microsoft Dynamics 365 Field Service لمعالجة أصول العميل والأصول الداخلية.
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
ms.openlocfilehash: 040f9d26a137ebce1edc6adf28ff226b3a81e1ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748583"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="de96e-103">أصول داخلية لإخضاعها للصيانة</span><span class="sxs-lookup"><span data-stu-id="de96e-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="de96e-104">تم تصميم Microsoft Dynamics 365 Field Service لخدمة أصول العميل.</span><span class="sxs-lookup"><span data-stu-id="de96e-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="de96e-105">تم تصميم إدارة الأصول في Dynamics 365 Supply Chain Management لصيانة الأصول الداخلية.</span><span class="sxs-lookup"><span data-stu-id="de96e-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="de96e-106">يسمح لك تكامل هذين التطبيقين باستخدام Field Service لصيانة أصول العميل والأصول الداخلية.</span><span class="sxs-lookup"><span data-stu-id="de96e-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="de96e-107">يمكنك أيضًا تصنيف الأصول، استنادًا إلى موقع العمل أو التدرج الهرمي، وتعقب الصيانة بشكل مفصل.</span><span class="sxs-lookup"><span data-stu-id="de96e-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="de96e-108">لمزيد من المعلومات، راجع [تكامل Dynamics 365 Field Service وSupply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="de96e-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="de96e-109">القوالب</span><span class="sxs-lookup"><span data-stu-id="de96e-109">Templates</span></span>

<span data-ttu-id="de96e-110">تتضمن الأصول الداخلية مجموعة من خرائط الجداول الرئيسية التي تعمل معًا أثناء تفاعل البيانات، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="de96e-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="de96e-111">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="de96e-111">Finance and Operations apps</span></span> | <span data-ttu-id="de96e-112">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="de96e-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="de96e-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="de96e-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="de96e-114">نماذج دورة حياة الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="de96e-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="de96e-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="de96e-116">حالات دورة حياة الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="de96e-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="de96e-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="de96e-118">أصول إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-118">Asset management assets</span></span> | <span data-ttu-id="de96e-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="de96e-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="de96e-120">أنواع الأصول في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-120">Asset management asset types</span></span> | <span data-ttu-id="de96e-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="de96e-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="de96e-122">نماذج دورة حياة موقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="de96e-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="de96e-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="de96e-124">حالات دورة حياة موقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="de96e-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="de96e-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="de96e-126">مواقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-126">Asset management functional locations</span></span> | <span data-ttu-id="de96e-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="de96e-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="de96e-128">أنواع مواقع العمل في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-128">Asset management functional location types</span></span> | <span data-ttu-id="de96e-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="de96e-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="de96e-130">الشركات المصنعة في إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-130">Asset management manufacturers</span></span> | <span data-ttu-id="de96e-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="de96e-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="de96e-132">نماذج إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-132">Asset management models</span></span> | <span data-ttu-id="de96e-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="de96e-133">msdyn\_models</span></span> | |
| <span data-ttu-id="de96e-134">ضمان إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="de96e-134">Asset management warranty</span></span> | <span data-ttu-id="de96e-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="de96e-135">msdyn\_warranties</span></span> | |

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