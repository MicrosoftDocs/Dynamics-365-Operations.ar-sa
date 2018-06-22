---
title: "مزامنة تقديرات المشروع من Project Service Automation مباشرة إلى تنبؤات المشروع في Finance and Operations"
description: "يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>مزامنة تقديرات المشروع من Project Service Automation مباشرة إلى تنبؤات المشروع في Finance and Operations

يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations.

> [!NOTE]
> تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات، تدفق البيانات حول تقديرات عدد ساعات المشروع وتقديرات مصروفات المشروع من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهام الأساسية لمزامنة تقديرات عدد ساعات المشروع من Project Service Automation إلى Finance and Operations.

-  **اسم القالب في تكامل البيانات:** تقديرات عدد ساعات المشروع (PSA إلى Fin and Ops)

-  **أسماء المهام في المشروع:** 
    - علاقات الحركات 
    - تقديرات المصروفات

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| مهام المشروع                   | كيان تكامل تقديرات عدد الساعات للمشروع   |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة تقديرات عدد ساعات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كتنبؤات عدد ساعات المشروع.

## <a name="preconditions"></a>الشروط المسبقة:

قبل القيام بمزامنة تقديرات عدد ساعات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query في قالب تقديرات عدد ساعات المشروع من أجل:
- قم بتعيين **معرف نموذج التنبؤ** التي سيتم استخدامها عندما يقوم التكامل بإنشاء تنبؤات عدد ساعات جديدة.
- تصفية أي سجلات موارد مُحددة ضمن المهمة التي سوف تفشل التكامل إلى تنبؤات عدد الساعات
- قم بتصفية أي صفوف فئات حركات فارغة. قد يؤدي الفشل في القيام بذلك إلى تنبؤات عدد ساعات غير صحيح.

### <a name="forecast-model-id"></a>معرف نموذج التنبؤ
لتحديث مُعرف نموذج التنبؤ الافتراضي في القالب، انقر فوق سهم **تعيين** لفتح التعيين. حدد لفتح الاستعلام المتقدم والتصفية.
- إذا كنت تستخدم قالب تقديرات عدد الساعات لمشروع Microsoft الافتراضي (PSA إلى Fin and Operations)، حدد **الشرط المُدرج** في قسم **الخطوات المُطبقة**. في إدخال **الوظيفة** ، استبدل **O_forcast** باسم **معرف نموذج التنبؤ** الذي يتعين استخدامه مع التكامل. يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.
- إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود. حدد **إضافة عمود شرطي** وقم بتسمية العمود، مثل ModelID. ادخل شرط للعمود بحيث إذا كانت مهمة المشروع فارغة، فمن ثم <enter the forecast model ID>; وإلا يترك فارغًا.

### <a name="filter-out-resource-specific-records"></a>تصفية سجلات مورد مُحدد
يحتوي قالب تقديرات عدد ساعات المشروع (PAS إلى Fin and Ops) على عامل تصفية افتراضي يقوم بإزالة أي سجلات موارد معينة. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا. في نموذج الاستعلام المتقدم والتصفة، حدد للتصفية على العمود **msdyn_islinetask** بحيث تتضمن فقط سجلات **خطأ** .

### <a name="filter-out-empty-transaction-category-rows"></a>تصفية صفوف فئات حركات فارغة
يجب إضافة عامل تصفية لإزالة أي صفوف بها فئات حركات فارغة. ويعد هذا الأمر مطلوبًا بغض النظر عما إذا كنت تستخدم القالب الافتراضي أو قمت بإنشاء القالب الخاص بك. سوف يقوم عامل التصفية هذا بإزالة أي صفوف ملخص واردة من Project Service Automation قد تتسبب في حدوث خطأ في تنبؤات عدد الساعات في Finance and Operations. في نموذج الاستعلام المتقدم والتصفية، حدد لتصفية السجلات الفارغة في العمود **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

يتم استخدام القالب التالي والمهمة الأساسية لمزامنة تقديرات مصروفات المشروع من Project Service Automation إلى Finance and Operations:

-  **اسم القالب في تكامل البيانات:** تقديرات مصروفات المشروع (PSA إلى Fin and Ops)
-  **أسماء المهام في المشروع:** 
     - علاقات الحركات 
     - تقديرات المصروفات

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| اتصالات الحركات         | كيان التكامل لعلاقات حركات المشروع.   |
| بنود التقدير                  | كيان تكامل تقديرات المصروفات للمشروع.           |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة تقديرات مصروفات المشروع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كتنبؤات مصروفات المشروع.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل القيام بمزامنة تقديرات مصروفات المشروع، يجب عليك مزامنة المشاريع ومهام المشاريع وفئات حركات مصروفات المشاريع.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query في قالب تقديرات مصروفات المشروع من أجل:
- التصفية لتضمين سجلات بنود تقدير المصروفات فقط
- قم بتعيين **معرف نموذج التنبؤ** التي سيتم استخدامها عندما يقوم التكامل بإنشاء تنبؤات عدد ساعات جديدة.
- تحويل أنواع الفوترة.
- تحويل أنواع الحركات.

### <a name="filter-to-include-only-expense-estimate-lines"></a>التصفية لتضمين بنود تقدير المصروفات فقط
يحتوي قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) على عامل تصفية افتراضي بحيث يقوم بتضمين بنود المصروفات فقط في التكامل. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا. حدد مهمة علاقات الحركة، ثم انقر فوق سهم **تعيين**. حدد **الاستعلام المتقدم والتصفية**. قم بتصفية عمود **msdyn_transactiontype1** لتضمين **msdyn_estimateline** فقط.

### <a name="forecast-model-id"></a>معرف نموذج التنبؤ
لتحديث مُعرف نموذج التنبؤ الافتراضي في القالب، لمهمة تقديرات المصروفات، انقر فوق سهم **تعيين** لفتح التعيين. حدد لفتح الاستعلام المتقدم والتصفية.
- إذا كنت تستخدم قالب تقديرات مصروفات المشروع Microsoft الافتراضي (PSA إلى Fin and Operations)، حدد أولًا **الشرط المُدرج** في قسم **الخطوات المُطبقة**. في إدخال **الوظيفة** ، استبدل **O_forcast** باسم **معرف نموذج التنبؤ** الذي يتعين استخدامه مع التكامل. يحتوي القالب الافتراضي على معرف نموذج تنبؤ من بيانات العرض التوضيحي.
- إذا كنت تقوم بإنشاء قالب جديد، يجب إضافة هذا العمود. حدد **إضافة عمود شرطي** وقم بتسمية العمود، مثل ModelID. ادخل الشرط للعمود بحيث إذا لم يكن معرف بند التقدير فارغًا، فمن ثم < ادخل معرف نموذج التنبؤ >; وإلا يترك فارغًا.

### <a name="transform-the-billing-types"></a>تحويل أنواع الفوترة
يحتوي قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) على عمود شرطي تمت إضافته لتحويل أنواع الفوترة المستلمة من Project Service Automation خلال التكامل.
- إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا. في نموذج الاستعلام المتقدم والتصفية، حدد **إضافة عمود شرطي**. قم بتسمية العمود، على سبيل المثال "BilingType". يجب أن يكون الشرط الذي يتم إدخاله كما يلي:

    إذا كان **msdyn_billingtype** = 192350000, فيكون **NonChargeable** وغير ذلك، إذا كان **msdyn_billingtype** = 192350001، فيكون **Chargeable** وغير ذلك، إذا كان **msdyn_billingtype** = 192350002، فيكون **Complimentary** وإلا **NotAvailable**

### <a name="transform-the-transaction-types"></a>تحويل أنواع الحركات
يحتوي قالب تقديرات مصروفات المشروع (PSA إلى Fin and Ops) على عمود شرطي تمت إضافته لتحويل أنواع الحركات المستلمة من Project Service Automation خلال التكامل.
- إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة العمود الشرطي هذا. في نموذج الاستعلام المتقدم والتصفية، حدد **إضافة عمود شرطي**. قم بتسمية العمود ، على سبيل المثال "TransactionType". يكون الشرط الذي يتم إدخاله كما يلي: في حالة **msdyn_transactiontypecode** = 192350000، فيكون **تكلفة** وإلا **msdyn_transactiontypecode** = 192350005، يكون **المبيعات** آخر **فارغة**

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![تعيين القالب](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




