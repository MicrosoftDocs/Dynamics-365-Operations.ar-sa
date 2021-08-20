---
title: التدرج الهرمي للمؤسسات في Dataverse
description: يوضح هذا الموضوع تكامل بيانات المؤسسة بين تطبيقات Finance and Operations وDataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 30826bf69525a85bede6ec0b64ec1a579aea26a0a6c487583739ad3fcb787a28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769235"
---
# <a name="organization-hierarchy-in-dataverse"></a>التدرج الهرمي للمؤسسات في Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

بما أن Dynamics 365 Finance عبارة عن نظام مالي، فإن *المؤسسة* عبارة عن مفهوم أساسي، ويبدأ إعداد النظام بتكوين التدرج الهرمي للمؤسسة. ويمكن بعد ذلك تتبع البيانات المالية للشركة على مستوى المؤسسة وكذلك على أي مستوى في التدرج الهرمي للمؤسسة.

على الرغم من أن Dataverse لا يتضمن مفهوم التدرج الهرمي للمؤسسة، إلا أنه يتضمن عددًا قليلاً من المفاهيم الفضفاضة، مثل إيراد المبيعات الإجمالي. كجزء من تكامل Dataverse، تتم إضافة بنية بيانات التدرج الهرمي للمؤسسات إلى Dataverse.

## <a name="data-flow"></a>تدفق البيانات

سيستمر وجود التدرج الهرمي للمؤسسات في النظام البيئي للأعمال الذي يتكون من تطبيقات Finance and Operations وDataverse. تم بناء هذا التدرج الهرمي للمؤسسات استنادًا إلى تطبيقات Finance and Operations ولكنه يظهر في Dataverse لأغراض تتعلق بالمعلومات وقابلية التوسعة. يبين الرسم التوضيحي التالي معلومات التدرج الهرمي للمؤسسات التي تظهر في Dataverse كتدفق بيانات أحادي الاتجاه من تطبيقات Finance and Operations إلى Dataverse.

![صورة البنية الهندسية.](media/dual-write-data-flow.png)

تتوفر مخططات جدول التدرج الهرمي للمؤسسات لمزامنة البيانات أحادية الاتجاه من تطبيقات Finance and Operations إلى Dataverse.

## <a name="templates"></a>القوالب

تحتوي معلومات المنتج على كافة المعلومات المرتبطة بالمنتج وتعريفه، مثل أبعاد المنتج أو أبعاد التعقب والتخزين. كما يوضح الجدول التالي، يتم إنشاء مجموعة من مخططات الجداول لمزامنة المنتجات والمعلومات المتعلقة بها.

تطبيقات Finance and Operations | تطبيقات Customer Engagement     | الوصف
-----------------------|--------------------------------|---
[الكيانات القانونية](mapping-reference.md#102) | cdm_companies | يوفر مزامنة ثنائيه الاتجاه لمعلومات الكيان القانوني (الشركة).
[الكيانات القانونية](mapping-reference.md#142) | msdyn_internalorganizations |
[وحدة التشغيل](mapping-reference.md#143) | msdyn_internalorganizations |
[التدرج الهرمي للمؤسسات - منشور](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | يقدم هذا القالب مزامنة أحادية الاتجاه لجدول المنشور للتدرج الهرمي للمؤسسات.
[أغراض التدرج الهرمي للمؤسسات](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | يقدم هذا القالب مزامنة أحادية الاتجاه لجدول غرض التدرج الهرمي للمؤسسات.
[نوع التدرج الهرمي للمؤسسات](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | يقدم هذا القالب مزامنة أحادية الاتجاه لجدول نوع التدرج الهرمي للمؤسسات.

## <a name="internal-organization"></a>مؤسسة داخلية

تأتي معلومات المؤسسة الداخلية في Dataverse من جدولين، **وحدة التشغيل** و **الكيانات القانونية**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
