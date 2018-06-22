---
title: "مزامنة القيم الفعلية لمشروع من Project Service Automation مباشرة إلى دفتر يومية تكامل المشروع للترحيل في Finance and Operations"
description: "يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة القيم الفعلية لمشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>مزامنة القيم الفعلية لمشروع من Project Service Automation مباشرة إلى دفتر يومية تكامل المشروع للترحيل في Finance and Operations

يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة القيم الفعلية لمشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations.

يقوم القالب بمزامنة الحركات من Project Service Automation إلى جدول مرحلي في Finance and Operations. بعد اكتمال المزامنة، يجب عليك الاستيراد من الجدول المرحلي إلى دفتر يومية التكامل.

> [!NOTE]
> يتوافر تكامل القيم الفعلية للمشروع في Dynamics 365 for Finance and Operations إصدار 8.01.

> [!NOTE]
> إذا قمت بإدخال مبالغ ضريبة المبيعات في حركات الوقت أو المصروفات في Project Service Automation، يجب عليك تثبيت تحديث 7 من Project Service Automation. إذا لم يتم تثبيت هذا التحديث، فلن يتم ربط القيم الفعلية للضريبة بالوقت المقترن أو القيم الفعلية للمصروفات، ولن يتم مزامنتها مع Finance and Operations. تواصل مع الدعم لمزيد من المعلومات.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بالقيم الفعلية لمشروع من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهام الأساسية لمزامنة القيم الفعلية لمشروع من Project Service Automation إلى Finance and Operations.

-  **اسم القالب في تكامل البيانات:** القيم الفعلية للمشروع (PSA إلى Fin and Ops)

-  **أسماء المهام في المشروع:** 
    - المبالغ الفعلية 
    - TransactionConnections

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| المبالغ الفعلية                         | كيان التكامل للقيم الفعلية للمشروع                      |
| اتصالات الحركات         | كيان التكامل لعلاقات حركات المشروع    |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة القيم الفعلية للمشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations إلى دفتر يومية تكامل المشروع. سوف يتم تطبيق المحاسبة استنادًا إلى الأبعاد المالية الافتراضية وإعداد الترحيل.

## <a name="preconditions"></a>الشروط المسبقة:

قبل القيام بمزامنة القيم الفعلية، يجب عليك تكوين محددات تكامل Project Service Automation ومزامنة المشاريع ومهام المشاريع وفئات حركة مصروفات المشروع.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query في قالب القيم الفعلية لمشروع من أجل:
- تحويل **نوع الحركة** لـ Project Service Automation إلى **نوع الحركة** الصحيح في Finance and Operations. يحتوي قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops) على هذا التحويل المُحدد مسبقًا.
- تحويل **نوع الفوترة** لـ Project Service Automation إلى **نوع الفوترة** الصحيح في Finance and Operations. يحتوي قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops) على هذا التحويل المُحدد مسبقًا. بعد ذلك، يتم تعيين نوع الفوترة إلى **خاصية السطر** استناداً إلى التكوين في Dynamics 365 لنموذج محددات تكامل Project Service Automation.
- عامل التصفية لـ **الوحدات التنظيمية للمورد** الذي سيتم مزامنته باستخدام هذا القالب.
- إذا كان سيتم مزامنة **الوقت بين شركات شقيقة أو القيم الفعلية للمصروفات بين شركات شقيقة** إلى Finance and Operations، يجب عليك تحويل، يجب تحويل **الوحدة التنظيمية للعقد** إلى **الكيان القانوني** الصحيح في Finance and Operations. يحتوي قالب القيم الفعلية للمشروع (PSA إلى Fin and Operations) على عمود شرطي محدد استنادًا إلى بيانات العرض التوضيحي. يجب عليك تحديث عمود الشرط المُدرج حديثًا إلى الكيانات القانونية الصحيحة. قد يؤدي الفشل في ذلك إما إلى خطأ تكامل أو حركات قيم فعلية غير صحيحة تم استيرادها إلى Finance and Operations.
- إذا لم تتم مزامنة **الوقت بين شركات شقيقة أو القيم الفعلية للمصروفات بين شركات شقيقة** ، يجب عليك حذف عمود الشرط المُدرج حديثًا من القالب الخاص بك. قد يؤدي الفشل في ذلك إما إلى خطأ تكامل أو حركات قيم فعلية غير صحيحة تم استيرادها إلى Finance and Operations.

### <a name="contract-organizational-unit"></a>الوحدة التنظيمية للعقد
لتحديث عمود الشرط المُدرج في القالب، انقر فوق سهم **تعيين** لفتح التعيين. حدد لفتح الاستعلام المتقدم والتصفية.
- إذا كنت تستخدم قالب القيم الفعلية لمشروع Microsoft الافتراضي (PSA إلى Fin and Operations)، حدد **الشرط المُدرج** حديثًا في قسم **الخطوات المُطبقة**. في إدخال **الوظيفة** ، استبدل **USSI** باسم **الكيان القانوني** الذي يتعين استخدامه مع التكامل. قم بإضافة شروط إضافية حسب الحاجة إلى إدخال **الوظيفة** ، وقم بتحديث شرط **آخر** من **USMF** إلى **الكيان القانوني** الصحيح.
- إذا كنت تقوم بإنشاء قالب جديد، يجب عليك إضافة هذا العمود لدعم الوقت بين الشركات الشقيقة والمصروفات. حدد **إضافة عمود شرطي** وقم بتسمية العمود، مثل LegalEntity. ادخل شرط للعمود إذا كان msdyn_contractorganizationalunitid.msdyn_name هو <organizational unit>، فمن ثم <enter the Legal entity>; وغير ذلك يكون فارغًا.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![تعيين القالب](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>استيراد من جدول مرحلي

يجب تشغيل الاستيراد من عملية دورية لجدول مرحلي بعد مزامنة القيم الفعلية من Project Service Automation إلى Finance and Operations. سوف تستورد هذه العملية حركات المشروع من الجدول المرحلي إلى دفتر يومية تكامل Project Service Automation، حيث يتم تطبيق المحاسبة ويمكن ترحيل الحركات التي تم استيرادها. من المستحسن أن تقوم بتشغيل هذه العملية في وضع الدفعة، ويمكنك بشكل اختياري إعداد التشغيل كمجموعة متكررة.

## <a name="update-actuals"></a>تحديث القيم الفعلية

يتم استخدام القالب التالي والمهام الأساسية لمزامنة رقم الإيصال وضرائب المبيعات لحركات المشروعات المُرحلة من Finance and Operations إلى Project Service Automation:

-  **اسم القالب في تكامل البيانات:** تحديث القيم الفعلية للمشروع (Fin and Ops إلى PSA)
-  **أسماء المهام في المشروع:** 
     - المبالغ الفعلية 
     - TransactionConnections

## <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| كيان التكامل للقيم الفعلية للمشروع                         | المبالغ الفعلية                           |
| كيان التكامل لعلاقات حركات المشروع       | اتصالات الحركات           |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة القيم الفعلية للمشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations إلى دفتر يومية تكامل المشروع. بمجرد الترحيل في Finance and Operations، يتم تحديث القيم الفعلية في Project Service Automation باستخدام رقم الإيصال من Finance and Operations. إذا تمت إضافة ضرائب المبيعات في Finance and Operations، سوف يتم إنشاء قيم فعلية جديدة للضريبة في PRoject Service Automation.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query في قالب تحديث القيم الفعلية لمشروع من أجل:
- تحويل **نوع الحركة** لـ Finance and Operations إلى **نوع الحركة** الصحيح في Project Service Automation. يحتوي قالب تحديث القيم الفعلية للمشروع (Fin OPs إلى PSA) على هذا التحويل المُحدد مسبقًا.
- تحويل **نوع الفوترة** لـ Finance and Operations إلى **نوع الفوترة** الصحيح في Project Service Automation. يحتوي قالب تحديث القيم الفعلية للمشروع (Fin OPs إلى PSA) على هذا التحويل المُحدد مسبقًا.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance and Operations إلى Project Service Automation.

[![تعيين القالب](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![تعيين القالب](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




