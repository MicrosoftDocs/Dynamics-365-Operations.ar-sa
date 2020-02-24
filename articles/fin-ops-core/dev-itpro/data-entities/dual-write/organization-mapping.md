---
title: التدرج الهرمي للمؤسسات في Common Data Service
description: يوضح هذا الموضوع تكامل بيانات المؤسسة بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019618"
---
# <a name="organization-hierarchy-in-common-data-service"></a>التدرج الهرمي للمؤسسات في Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة. ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.

على الرغم من أن Common Data Service لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي. كجزء من تكامل Common Data Service، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Common Data Service.

## <a name="data-flow"></a>تدفق البيانات

سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وCommon Data Service. تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations ولكنه يظهر في Common Data Service لأغراض تتعلق بالمعلومات وقابلية التوسعة. يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Common Data Service كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.

![صورة البنية الهندسية](media/dual-write-data-flow.png)

## <a name="templates"></a>القوالب

تتوفر مخططات كيان التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.

## <a name="templates"></a>القوالب

تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين. كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الكيانات لمزامنة المنتجات والمعلومات المتعلقة بها.

Finance and Operations | تطبيقات Dynamics 365 الأخرى | ‏‏الوصف
-----------------------|--------------------------------|---
أغراض التدرج الهرمي للمؤسسات | msdyn_internalorganizationhierarchypurposes | يقدم هذا القالب مزامنة أحادية الاتجاه لكيان غرض التدرج الهرمي للمؤسسات.
نوع التدرج الهرمي للمؤسسات | msdyn_internalorganizationhierarchytypes | يقدم هذا القالب مزامنة أحادية الاتجاه لكيان نوع التدرج الهرمي للمؤسسات.
التدرج الهرمي للمؤسسات - منشور | msdyn_internalorganizationhierarchies | يقدم هذا القالب مزامنة أحادية الاتجاه للكيان المنشور للتدرج الهرمي للمؤسسات.
وحدة التشغيل | msdyn_internalorganizations | 
الكيانات القانونية | msdyn_internalorganizations | 
الكيانات القانونية | cdm_companies | يوفر مزامنة ثنائيه الاتجاه لمعلومات الكيان القانوني (الشركة).


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>مؤسسة داخلية

تأتي معلومات المؤسسة الداخلية في Common Data Service من كيانين، **وحدة التشغيل** و**الكيانات القانونية**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

