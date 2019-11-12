---
title: التدرج الهرمي للمؤسسات في Common Data Service
description: يوضح هذا الموضوع تكامل البيانات التنظيمية بين تطبيقات Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572439"
---
# <a name="organization-hierarchy-in-common-data-service"></a>التدرج الهرمي للمؤسسات في Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة. ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.

على الرغم من أن Common Data Service لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي. كجزء من تكامل Common Data Service، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Common Data Service.

## <a name="data-flow"></a>تدفق البيانات

سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وCommon Data Service. تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations، ولكنه يظهر لأغراض تتعلق بالمعلومات وقابلية التوسعة في Common Data Service. يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Common Data Service كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.

![صورة البنية الهندسية](media/dual-write-data-flow.png)

## <a name="templates"></a>القوالب

تتوفر مخططات كيان التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>غرض التدرج الهرمي للمؤسسات الداخلي

يوفر هذا القالب المزامنة أحادية الاتجاه لكيان غرض التدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.

<!-- ![architecture image](media/dual-write-purpose.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>نوع التدرج الهرمي للمؤسسات الداخلية

يوفر هذا القالب المزامنة أحادية الاتجاه لكيان نوع التدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.

<!-- ![architecture image](media/dual-write-type.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
الاسم | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>التدرج الهرمي للمؤسسات الداخلية

يوفر هذا القالب المزامنة أحادية الاتجاه للكيان المنشور للتدرج الهرمي للمؤسسات من Finance and Operations إلى تطبيقات Dynamics 365 الأخرى.

<!-- ![architecture image](media/dual-write-organization.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>مؤسسة داخلية

تأتي معلومات المؤسسة الداخلية في Common Data Service من كيانين، **وحدة التشغيل** و**الكيانات القانونية**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>وحدة التشغيل

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NAME | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>كيان قانوني

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NAME | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
none | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>الشركة

يوفر مزامنة ثنائية الاتجاه لمعلومات الكيان القانوني (الشركة) بين Finance and Operations وتطبيقات Dynamics 365 الأخرى.

<!-- ![architecture image](media/dual-write-company.png) -->

حقل المصدر | نوع التعيين | حقل الوجهة
---|---|---
الاسم | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
