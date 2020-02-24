---
title: المواقع والمستودعات المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وCommon Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019615"
---
# <a name="integrated-sites-and-warehouses"></a>المواقع والمستودعات المتكاملة

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

يوضح هذا الموضوع تكامل بيانات الموقع والمستودع بين تطبيقات Finance and Operations وCommon Data Service. تعتبر المواقع والمستودعات التشغيلية مفاهيم عامة في تطبيق Supply Chain Management. وهي تستخدم لصياغة سلسلة التوريد الخاصة بشركك.

## <a name="templates"></a>القوالب

من خلال التكامل مع Common Data Service، تتوفر هذه المفاهيم وكافة المعلومات المتعلقة بها في Common Data Service باستخدام كيانات بيانات المواقع والمستودعات في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Dynamics 365 الأخرى | ‏‏الوصف
--------------------------|---------------------------|---
المواقع | msdyn_operationalsites | 
المستودعات | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

