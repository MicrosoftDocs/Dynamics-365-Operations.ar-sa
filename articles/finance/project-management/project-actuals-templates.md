---
title: مزامنة القيم الفعلية لمشروع مباشرةً من Project Service Automation إلى دفتر يومية تكامل المشروع للترحيل في Finance and Operations
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة قيم المشروع الفعلية مباشرة من Dynamics 365 Project Service Automation Microsoftإلى Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 302ac0f456dd8a24dc02948ee657e359f5a9c844
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770325"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>مزامنة القيم الفعلية لمشروع مباشرةً من Project Service Automation إلى دفتر يومية تكامل المشروع للترحيل في Finance and Operations

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة قيم المشروع الفعلية مباشرة من Dynamics 365 Project Service Automation إلى Dynamics 365 Finance.

يقوم القالب بمزامنة الحركات من Project Service Automation إلى جدول مرحلي في Finance. بعد اكتمال المزامنة، **يجب** عليك استيراد البيانات من الجدول المرحلي إلى دفتر يومية التكامل.

> [!NOTE]
> - يتوفر تكامل قيم المشروع الفعلية بداية من الإصدار 8.0.1.
> - إذا كنت تستخدم , Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.
> - إذا كنت تستخدم الإصدار 7.3.0، وتعمل على إحضار حركات الرسوم من Project Service Automation، فيجب تثبيت KB 4345320 لتضمين تلك الرسوم في فاتورة المشروع.
> - إذا كنت تعمل على إدخال مبالغ ضريبة المبيعات في حركات الوقت أو المصروفات في Project Service Automation، فيجب تثبيت Project Service Automation Update 7. وإلا، فلن يتم ربط القيم الفعلية للضريبة بالقيم الفعلية للوقت أو المصروفات المقترنة، ولن تتم مزامنتها مع Finance. تواصل مع الدعم لمزيد من المعلومات.

## <a name="data-flow-for-project-service-automation-to-finance"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation وFinance تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بالقيم الفعلية لمشروع من Project Service Automation إلى Finance.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>القيم الفعلية من Project Service Automation

### <a name="template-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft Power Apps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهام الأساسية لمزامنة القيم الفعلية لمشروع من Project Service Automation إلى Finance.

- **اسم القالب في تكامل البيانات:** القيم الفعلية للمشروع (PSA إلى Fin and Ops)
- **أسماء المهام في المشروع:**

    - المبالغ الفعلية
    - TransactionConnections

### <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation | المالية                                   |
|----------------------------|----------------------------------------------------------|
| المبالغ الفعلية                    | كيان التكامل للقيم الفعلية للمشروع                   |
| اتصالات الحركات    | كيان التكامل لعلاقات حركات المشروع |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة القيم الفعلية للمشروع في Project Service Automation، ثم تتم مزامنتها إلى دفتر يومية تكامل المشروع في Finance. سوف يتم تطبيق المحاسبة استنادًا إلى الأبعاد المالية الافتراضية وإعداد الترحيل.

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل القيام بمزامنة القيم الفعلية، يجب عليك تكوين محددات تكامل Project Service Automation ومزامنة المشاريع ومهام المشاريع وفئات حركة مصروفات المشروع.

### <a name="power-query"></a>Power Query

في قالب القيم الفعلية للمشروع، يجب عليك استخدام Microsoft Power Query لـ Excel لإكمال هذه المهام:

- تحويل نوع الحركة في Project Service Automation إلى نوع الحركة الصحيح في Finance. تكون عملية التحويل هذه معرّفة في قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops).
- تحويل نوع الفوترة في Project Service Automation إلى نوع الفوترة الصحيح في Finance. تكون عملية التحويل هذه معرّفة في قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops). بعد ذلك، يتم تعيين نوع الفوترة إلى خاصية البند استنادًا إلى التكوين في صفحة **محددات تكامل Project Service Automation**.
- تصفية وحدات تنظيمية لموارد محددة يجب مزامنتها مع هذا القالب.
- إذا كانت مزامنة القيم الفعلية للوقت أو القيم الفعلية للمصروفات بين الشركات الشقيقة ستتم إلى Finance، فيجب عليك تحويل الوحدة التنظيمية للعقد إلى الكيان القانوني الصحيح في Finance. يحتوي قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops) على عمود شرطي محدد استنادًا إلى بيانات العرض التوضيحي. يجب عليك تحديث العمود الشرطي الأخير المُدرج إلى الكيانات القانونية الصحيحة. وإلا، فقد يحدث خطأ تكامل أو قد يتم استيراد حركات قيم فعلية غير صحيحة إلى Finance.
- إذا لم تتم مزامنة القيم الفعلية للوقت أو القيم الفعلية للمصروفات بين الشركات الشقيقة إلى Finance، فيجب حذف العمود الشرطي الأخير المُدرج من قالبك. وإلا، فقد يحدث خطأ تكامل أو قد يتم استيراد حركات قيم فعلية غير صحيحة إلى Finance.

#### <a name="contract-organizational-unit"></a>الوحدة التنظيمية للعقد
لتحديث العمود الشرطي الأخير المُدرج في القالب، انقر فوق سهم **تعيين** لفتح التعيين. حدد الارتباط **الاستعلام المتقدم والتصفية** لفتح Power Query.

- إذا كنت تستخدم قالب القيم الفعلية للمشروع الافتراضي (PSA إلى Fin and Ops)، فحدد **الشرط المُدرج** الأخير من قسم **الخطوات المُطبقة** في Power Query. في إدخال **الوظيفة**، استبدل **USSI** باسم الكيان القانوني الذي الذي يجب استخدامه مع التكامل. قم بإضافة شروط إضافية حسب الحاجة إلى إدخال **الوظيفة**، وقم بتحديث شرط **else** من **USMF** إلى الكيان القانوني الصحيح.
- إذا كنت تقوم بإنشاء قالب جديد، يجب عليك إضافة العمود لدعم الوقت والمصروفات بين الشركات الشقيقة. حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود مثل **LegalEntity**. أدخل شرطًا للعمود، حيث إذا **msdyn\_contractorganizationalunitid.msdyn\_الاسم** هو \<وحدة تنظيمية\>، ثم \<أدخل الكيان القانوني\>؛ else null.

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance.

[![تعيين القالب](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![تعيين القالب](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>الاستيراد من جدول مرحلي‬ بعد التكامل من Project Service Automation

يجب تشغيل الاستيراد من عملية دورية لجدول مرحلي بعد مزامنة القيم الفعلية من Project Service Automation إلى Finance. سوف تستورد هذه العملية حركات المشروع من الجدول المرحلي إلى دفتر يومية تكامل Project Service Automation، حيث يتم تطبيق المحاسبة ويمكن ترحيل الحركات التي تم استيرادها. ننصح بأن تقوم بتشغيل هذه العملية في الوضع الدفعي، ويمكنك بشكل اختياري إعداد التشغيل كمجموعة متكررة.

## <a name="update-actuals-from-finance"></a>تحديث القيم الفعلية من Finance

### <a name="template-and-tasks"></a>القوالب والمهام

يتم استخدام القالب التالي والمهام الأساسية لمزامنة رقم الإيصال وضرائب المبيعات لحركات المشروعات المُرحلة من Finance إلى Project Service Automation:

- **اسم القالب في تكامل البيانات:** تحديث القيم الفعلية للمشروع (Fin and Ops إلى PSA)
- **أسماء المهام في المشروع:**

    - المبالغ الفعلية 
    - TransactionConnections

### <a name="entity-set"></a>مجموعة الكيانات

| المالية                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| كيان التكامل للقيم الفعلية للمشروع                   | المبالغ الفعلية                    |
| كيان التكامل لعلاقات حركات المشروع | اتصالات الحركات    |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة القيم الفعلية للمشروع في Project Service Automation، ثم تتم مزامنتها إلى دفتر يومية تكامل المشروع في Finance. بعد ترحيل القيم الفعلية في Finance، يتم تحديثها في Project Service Automation باستخدام رقم الإيصال من Finance. إذا تمت إضافة ضرائب المبيعات في Finance، سوف يتم إنشاء قيم ضريبية فعلية جديدة في Project Service Automation.

### <a name="power-query"></a>Power Query

في قالب تحديث القيم الفعلية للمشروع، يجب عليك استخدام Power Query لإكمال هذه المهام:

- تحويل نوع الحركة في Finance إلى نوع الحركة الصحيح في Project Service Automation. تكون عملية التحويل هذه معرّفة في تحديث قالب القيم الفعلية للمشروع (Fin Ops إلى PSA).
- تحويل نوع الفوترة في Finance إلى نوع الفوترة الصحيح في Project Service Automation. تكون عملية التحويل هذه معرّفة في تحديث قالب القيم الفعلية للمشروع (Fin Ops إلى PSA).

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance إلى Project Service Automation.

[![تعيين القالب](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![تعيين القالب](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
