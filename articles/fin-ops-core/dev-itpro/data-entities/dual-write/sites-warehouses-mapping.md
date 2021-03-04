---
title: المواقع والمستودعات المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وDataverse.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679310"
---
# <a name="integrated-sites-and-warehouses"></a>المواقع والمستودعات المتكاملة

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وDataverse. تعتبر المواقع والمستودعات التشغيلية مفاهيم عامة في تطبيق Supply Chain Management. وهي تستخدم لصياغة سلسلة التوريد الخاصة بشركك.

## <a name="templates"></a>القوالب

من خلال التكامل مع Dataverse، تتوفر هذه المفاهيم وكافة المعلومات المتعلقة بها في Dataverse باستخدام جداول بيانات المواقع والمستودعات في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Dynamics 365 الأخرى | الوصف
--------------------------|---------------------------|---
المواقع | msdyn_operationalsites | 
المستودعات | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]