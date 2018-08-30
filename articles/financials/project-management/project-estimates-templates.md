---
title: "مزامنة تقديرات المشروع مباشرةً من Project Service Automation إلى Finance and Operations"
description: "يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرةً من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>مزامنة تقديرات المشروع مباشرةً من Project Service Automation إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations.

> [!NOTE]
> - تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations.
> - يتوافر تكامل القيم الفعلية في Microsoft Dynamics 365 for Finance and Operations، الإصدار 8.01 أو إصدار لاحق.
> - إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستتمكن من استخدام القوالب لإجراء تكامل لمهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية ولتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات، تدفق البيانات حول تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>تقديرات ساعات المشروع

### <a name="template-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهام الأساسية لمزامنة تقديرات عدد ساعات المشروع من Project Service Automation إلى Finance and Operations.

- **اسم القالب في تكامل البيانات:** تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops)
- **أسماء المهام في المشروع:**

    - علاقات الحركات
    - تقديرات المصروفات

### <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| مهام المشروع              | كيان تكامل تقديرات عدد الساعات للمشروع |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة تقديرات عدد ساعات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كتنبؤات عدد ساعات المشروع.

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل القيام بمزامنة تقديرات عدد ساعات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.

### <a name="power-query"></a>Power Query

في قالب تقديرات ساعات المشروع، يجب عليك استخدام Microsoft Power Query لـ Excel لإكمال هذه المهام:

- تعيين معرّف نموذج التنبؤ الافتراضي الذي سيتم استخدامه عندما ينشئ التكامل تنبؤات عدد ساعات جديدة.
- تصفية سجلات خاصة بالموارد في المهمة التي سوف تفشل التكامل في تنبؤات عدد الساعات .
- قم بتصفية أي صفوف فئات حركات فارغة. قد يؤدي الفشل في إكمال هذه المهمة إلى تنبؤات عدد ساعات غير صحيح.

#### <a name="set-the-default-forecast-model-id"></a>تعيين معرّف نموذج التنبؤ الافتراضي

لتحديث مُعرف نموذج التنبؤ الافتراضي في القالب، انقر فوق سهم **تعيين** لفتح التعيين. ثم حدد الارتباط **الاستعلام المتقدم والتصفية**.

- إذا كنت تستخدم قالب تقديرات ساعات المشروع الافتراضية (PSA إلى Fin and Ops)، فحدد **الشرط المُدرج** في قائمة **الخطوات المُطبقة**. في إدخال **الوظيفة**، استبدل **O\_forecast** باسم معرّف نموذج التنبؤ الذي يتعين استخدامه مع التكامل. يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.
- إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود. في Power Query، حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود الجديد، مثل **ModelID**. أدخل الشرط للعمود بحيث إذا لم تكن مهمة المشروع بقيمة null، عندئذٍ \<أدخل معرّف نموذج التنبؤ\>؛ وإلا null.

#### <a name="filter-out-resource-specific-records"></a>تصفية سجلات خاصة بالموارد

يحتوي قالب تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops) على عامل تصفية افتراضي يقوم بإزالة أي سجلات خاصة بالموارد. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا. حدد الارتباط **الاستعلام المتقدم والتصفية** لإجراء التصفية على العمود **msdyn\_islinetask** بحيث لا يتم تضمين سوى السجلات ذات القيمة **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>تصفية صفوف فئات حركات فارغة

يجب إضافة عامل تصفية لإزالة أي صفوف تتضمن فئات حركات فارغة. تعتبر هذه المهمة ضرورية، بصرف النظر عما إذا كنت تستخدم القالب الافتراضي أو تعمل على إنشاء قالبك الخاص. يزيل عامل التصفية هذا بإزالة أي صفوف ملخص واردة من Project Service Automation قد تتسبب في حدوث خطأ في تنبؤات عدد الساعات في Finance and Operations. حدد الارتباط **الاستعلام المتقدم والتصفية** لتصفية السجلات ذات القيمة null في العمود **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>‏‏تقديرات مصروفات المشروع

### <a name="template-and-tasks"></a>القوالب والمهام

يتم استخدام القالب التالي والمهام الأساسية التالية لمزامنة تقديرات مصروفات المشروع من Project Service Automation إلى Finance and Operations:

- **اسم القالب في تكامل البيانات:** تقديرات مصروفات المشروع (PSA إلى Fin and Ops)
- **أسماء المهام في المشروع:**

    - علاقات الحركات 
    - تقديرات المصروفات

### <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| اتصالات الحركات    | كيان التكامل لعلاقات حركات المشروع |
| بنود التقدير             | كيان تكامل تقديرات المصروفات للمشروع         |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة تقديرات مصروفات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كتنبؤات مصروفات المشروع.

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل القيام بمزامنة تقديرات مصروفات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.

### <a name="power-query"></a>Power Query

يجب عليك استخدام Power Query في قالب تقديرات مصروفات المشروع لإكمال المهام التالية:

- التصفية لتضمين سجلات بنود تقدير المصروفات فقط.
- تعيين معرّف نموذج التنبؤ الافتراضي الذي سيتم استخدامه عندما ينشئ التكامل تنبؤات عدد ساعات جديدة.
- تحويل أنواع الفوترة.
- تحويل أنواع الحركات.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>التصفية لتضمين بنود تقدير المصروفات فقط

يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يتضمن فقط بنود المصروفات في التكامل. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا. حدد مهمة **علاقات الحركة** ثم انقر فوق السهم **تعيين‏‎** لفتح التعيين. حدد الارتباط **الاستعلام المتقدم والتصفية**. قم بتصفية العمود **msdyn\_transactiontype1** بحيث يتضمن **msdyn\_estimateline** فقط.

#### <a name="set-the-default-forecast-model-id"></a>تعيين معرّف نموذج التنبؤ الافتراضي

لتحديث معرّف نموذج التنبؤ الافتراضي في القالب، حدد مهمة **تقديرات المصروفات**، ثم انقر فوق السهم **تعيين‏‎** لفتح التعيين. حدد الارتباط **الاستعلام المتقدم والتصفية**.

- إذا كنت تستخدم قالب تقديرات مصروفات المشروع الافتراضي (PSA إلى Fin and Ops)، في Power Query، حدد **الشرط المُدرج** الأول من قسم **الخطوات المُطبقة**. في إدخال **الوظيفة**، استبدل **O\_forecast** باسم معرّف نموذج التنبؤ الذي يتعين استخدامه مع التكامل. يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.
- إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود. في Power Query، حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود الجديد، مثل **ModelID**. أدخل الشرط للعمود بحيث إذا لم يكن معرّف بند التقدير بقيمة null، عندئذٍ \<أدخل معرّف نموذج التنبؤ\>؛ وإلا null.‬

#### <a name="transform-the-billing-types"></a>تحويل أنواع الفوترة

يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عمودًا شرطيُا يُستخدم لتحويل أنواع الفوترة المستلمة من Project Service Automation خلال التكامل. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا. حدد الارتباط **الاستعلام المتقدم والتصفية** ثم حدد **إضافة عمود شرطي**. أدخل اسمًا للعمود الجديد، مثل **BillingType‎**. بعد ذلك، أدخل الشرط التالي:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>تحويل أنواع الحركات

يتضمن قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) عمودًا شرطيُا يُستخدم لتحويل أنواع الحركات المستلمة من Project Service Automation خلال التكامل. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا. حدد الارتباط **الاستعلام المتقدم والتصفية** ثم حدد **إضافة عمود شرطي**. أدخل اسمًا للعمود الجديد، مثل **TransactionType**. بعد ذلك، أدخل الشرط التالي:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![تعيين القالب](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)

