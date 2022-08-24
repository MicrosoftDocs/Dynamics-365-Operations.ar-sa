---
title: التدرج الهرمي للمؤسسات في Dataverse
description: توضح هذه المقالة تكامل البيانات التنظيمية بين تطبيقات التمويل والعمليات و Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289035"
---
# <a name="organization-hierarchy-in-dataverse"></a>التدرج الهرمي للمؤسسات في Dataverse

[!include [banner](../../includes/banner.md)]



بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة. ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.

على الرغم من أن Dataverse لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي. كجزء من تكامل Dataverse، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Dataverse.

## <a name="data-flow"></a>تدفق البيانات

سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات التمويل والعمليات و Dataverse. تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات التمويل والعمليات، ولكنه يظهر لأغراض تتعلق بالمعلومات وقابلية التوسعة في Dataverse. يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Dataverse كتدفق بيانات أحادي الاتجاه من تطبيقات التمويل والعمليات إلى Dataverse.

![صورة البنية الهندسية.](media/dual-write-data-flow.png)

تتوفر خرائط جدول التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات التمويل والعمليات إلى Dataverse.

## <a name="templates"></a>القوالب

المؤسسة هي عبارة عن مجموعة من الأشخاص يعملون معا لتنفيذ عملية تجارية أو تحقيق هدف. تمثل التدرجات الهرمية المؤسسية العلاقات بين المؤسسات التي تتألف منها أعمالك. يمكنك تحديد الأنواع التالية من المؤسسات الداخلية: الكيانات القانونية ووحدات التشغيل والفرق. كما يوضح الجدول التالي، يتم إنشاء مجموعة من خرائط الجدول لمزامنة الكيانات القانونية ووحدة التشغيل والقطاعات ومعلومات التسلسل الهرمي للتنظيم ذات الصلة.

تطبيقات التمويل والعمليات | تطبيقات Customer Engagement     | ‏‏الوصف‬
-----------------------|--------------------------------|---
[الكيانات القانونية](mapping-reference.md#102) | cdm_companies | 
[الكيانات القانونية](mapping-reference.md#142) | msdyn_internalorganizations |
[وحدة التشغيل](mapping-reference.md#143) | msdyn_internalorganizations |
[التدرج الهرمي للمؤسسات - منشور](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | يقدم هذا القالب مزامنة أحادية الاتجاه لجدول المنشور للتدرج الهرمي للمؤسسات.
[أغراض التدرج الهرمي للمؤسسات](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | يقدم هذا القالب مزامنة أحادية الاتجاه لجدول غرض التدرج الهرمي للمؤسسات.
[نوع التدرج الهرمي للمؤسسات](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | يقدم هذا القالب مزامنة أحادية الاتجاه لجدول نوع التدرج الهرمي للمؤسسات.

## <a name="internal-organization"></a>مؤسسة داخلية

تأتي معلومات المؤسسة الداخلية في Dataverse من جدولين، **وحدة التشغيل** و **الكيانات القانونية**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

