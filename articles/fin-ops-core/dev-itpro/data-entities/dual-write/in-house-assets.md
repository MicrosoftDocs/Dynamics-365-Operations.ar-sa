---
title: أصول داخلية لإخضاعها للصيانة
description: توضح هذه المقالة كيف يمكنك استخدام Microsoft Dynamics 365 Field Service لخدمة أصول العملاء والأصول الداخلية.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289239"
---
# <a name="in-house-assets-for-servicing"></a>أصول داخلية لإخضاعها للصيانة

[!include [banner](../../includes/banner.md)]

تم تصميم Microsoft Dynamics 365 Field Service لخدمة أصول العميل. تم تصميم إدارة الأصول في Dynamics 365 Supply Chain Management لصيانة الأصول الداخلية. يسمح لك تكامل هذين التطبيقين باستخدام Field Service لصيانة أصول العميل والأصول الداخلية. يمكنك أيضًا تصنيف الأصول، استنادًا إلى موقع العمل أو التدرج الهرمي، وتعقب الصيانة بشكل مفصل.

لمزيد من المعلومات، راجع [تكامل Dynamics 365 Field Service وSupply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>القوالب

تتضمن الأصول الداخلية مجموعة من خرائط الجداول الرئيسية التي تعمل معًا أثناء تفاعل البيانات، كما هو موضح في الجدول التالي.

| تطبيقات Finance and Operations | تطبيقات Customer Engagement | الوصف |
|-----------------------------|-----------------------------------|-------------|
[نماذج دورة حياة الأصول في إدارة الأصول](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[حالات دورة حياة الأصول في إدارة الأصول](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[أنواع الأصول في إدارة الأصول](mapping-reference.md#124) | msdyn_customerassetcategories | |
[أصول إدارة الأصول](mapping-reference.md#125) | msdyn_customerassets | |
[نماذج دورة حياة موقع العمل في إدارة الأصول](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[حالات دورة حياة موقع العمل في إدارة الأصول](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[أنواع مواقع العمل في إدارة الأصول](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[مواقع العمل في إدارة الأصول](mapping-reference.md#136) | msdyn_functionallocations | |
[الشركات المصنعة في إدارة الأصول](mapping-reference.md#153) | msdyn_manufacturers | |
[نماذج إدارة الأصول](mapping-reference.md#154) | msdyn_models | |
[ضمان إدارة الأصول](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
