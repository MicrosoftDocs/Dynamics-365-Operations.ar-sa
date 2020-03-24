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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112383"
---
# <a name="in-house-assets-for-servicing"></a>أصول داخلية لإخضاعها للصيانة

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

تم تصميم Microsoft Dynamics 365 Field Service لصيانة أصول العميل. تم تصميم إدارة الأصول في Dynamics 365 Supply Chain Management لصيانة الأصول الداخلية. يسمح لك تكامل هذين التطبيقين باستخدام Field Service لصيانة أصول العميل والأصول الداخلية. يمكنك أيضًا تصنيف الأصول، استنادًا إلى موقع العمل أو التدرج الهرمي، وتعقب الصيانة بشكل مفصل.

لمزيد من المعلومات، راجع [تكامل Dynamics 365 Field Service وSupply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>القوالب

تتضمن الأصول الداخلية مجموعة من خرائط الكيانات الرئيسية التي تعمل معًا أثناء تفاعل البيانات، كما هو موضح في الجدول التالي.

| تطبيقات Finance and Operations | التطبيقات المستندة إلى نموذج في Dynamics 365 | ‏‏الوصف |
|-----------------------------|-----------------------------------|-------------|
| نماذج دورة حياة الأصول في إدارة الأصول | msdyn\_assetlifecyclemodels | |
| حالات دورة حياة الأصول في إدارة الأصول | msdyn\_assetlifecyclestates | |
| أصول إدارة الأصول | msdyn\_customerassets | |
| أنواع الأصول في إدارة الأصول | msdyn\_customerassetcategories | |
| نماذج دورة حياة موقع العمل في إدارة الأصول | msdyn\_functionallocationlifecyclemodels | |
| حالات دورة حياة موقع العمل في إدارة الأصول | msdyn\_functionallocationlifecyclestates | |
| مواقع العمل في إدارة الأصول | msdyn\_functionallocations | |
| أنواع مواقع العمل في إدارة الأصول | msdyn\_functionallocationtypes | |
| الشركات المصنعة في إدارة الأصول | msdyn\_manufacturers | |
| نماذج إدارة الأصول | msdyn\_models | |
| ضمان إدارة الأصول | msdyn\_warranties | |

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
