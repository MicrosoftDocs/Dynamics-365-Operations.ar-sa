---
title: المشكلات المعروفة لدمج بنية Dynamics 365 Human Resources الأساسية
description: تسرد هذه المقالة المشكلات التي يمكن أن تحدث أثناء دمج بنية Microsoft Dynamics 365 Human Resources الأساسية.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752680"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>المشكلات المعروفة لدمج بنية Dynamics 365 Human Resources الأساسية

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>بيئات Dataverse المشتركة

لا يدعم إطار الكتابة المزدوجة ربط بيئتين من بيئات تطبيقات التمويل والعمليات بنفس بيئة Dataverse. إذا كانت لديك بيئة Dataverse مشتركة مع كلا العنصرين التاليين، فيجب عليك إما تكرار بيئة Dataverse أو تقسيمها:

- تطبيق Finance and Operations
- بيئة Human Resources حالية

## <a name="environment-type-requirements"></a>متطلبات نوع البيئة

يجب توفر أنواع البيئات التالية قبل أن تتمكن من إجراء الترحيل:

- إذا لم يكن لديك أية بيئات وضع حماية مستقلة، فيجب عليك إنشاء بيئة للتحقق من صحة الترحيل.
- إذا كانت لديك بيئات تشغيل متعددة مستقلة، فيمكن ترحيل واحدة منها. اتصل بدعم Microsoft لوضع علامة على البيئات الأخرى كبيئات وضع حماية.

## <a name="teams-integration"></a>التكامل مع Teams

يتم حاليًا نقل تطبيق Human Resources الموجود في Teams إلى أحد حلول Microsoft Power Platform. لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](hr-admin-teams-leave-app.md).

