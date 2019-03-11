---
title: مزامنة فئات مصروفات المشروع بين Finance and Operations و Project Service Automation
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بين Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "347826"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>مزامنة فئات مصروفات المشروع بين Finance and Operations و Project Service Automation

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بين Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Project Service Automation.

> [!NOTE]
> - تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations.
> - يتوفر تكامل القيم الفعلية في الإصدار 8.0.1 أو إصدار لاحق من Microsoft Dynamics 365 for Finance and Operations.
> - إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation و Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation و Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بفئات حركات مصروفات المشروع بين Finance and Operations وProject Service Automation.

إذا تمت إدارة في فئات مصروفات المشروع في Finance and Operations، فيكون تدفق التكامل أولًا من Finance and Operations إلى Project Service Automation. يتم عندئذٍ تحديث معرّفات التكامل لفئات مصروفات المشروع عبر المزامنة من Project Service Automation إلى Finance and Operations.

إذا تم التحكم في فئات مصروفات المشروع في Project Service Automation، فيكون تدفق التكامل أولًا من Project Service Automation إلى Finance and Operations. يجب تكوين فئات المشروع بشكل مسبق في Finance and Operations قبل إجراء المزامنة من Project Service Automation. ثم نفّذ المزامنة من Finance and Operations مرة أخرى إلى Project Service Automation، ثم من Project Service Automation إلى Finance and Operations مرة أخرى. بهذه الطريقة، يمكنك المساعدة في ضمان الحصول على فئات مرتبطة وعدم إنشاء أي تكرارات.

> [!NOTE]
> تتم عادةً إدارة فئات مصروفات المشروع في Finance and Operations. ومع ذلك، إذا لم تتم إدارتها في Finance and Operations، أو إذا تم إنشاء فئات المصروفات بشكل مسبق في Project Service Automation، فيجب عليك إجراء المزامنة أولاً باستخدام قالب فئات حركات مصروفات المشروع (PSA إلى Fin and Ops). ثم نفّذ المزامنة باستخدام قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA). يجب بعد ذلك تشغيل المزامنة من Project Service Automation إلى Finance and Operations مرة أخرى.
>
> إذ أجريت المزامنة من Project Service Automation أولاً، فيجب تلبية المتطلبات التالية في Finance and Operations قبل تشغيل عملية المزامنة:
>
> - يلزم وجود الفئة المشتركة التي تتطابق مع فئة المشروع التي تم إعدادها في Project Service Automation، ويجب تمكينها لكل من **المشروع** و**المصروفات**.
> - لكل كيان قانوني في Finance and Operations يجب دمجه فيه، يلزم وجود فئات المشروع التالية:
>
>     - **فئة المشروع** موجودة. 
>     - تمكين **الاستخدام في المصروفات**.
>     - تمكين **نشط في دفتر اليومية**.
>     - تعيين **نوع الحركة** إلى **مصروفات**.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>مزامنة فئات مصروفات المشروع من Finance and Operations إلى Project Service Automation

### <a name="template-and-task"></a>القالب والمهمة

للوصول إلى القالب، في مركز إدارة Microsoft PowerApps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب والمهمة الأساسية التالية لمزامنة فئات مصروفات المشروع من Finance and Operations إلى Project Service Automation:

- **اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (Fin and Ops إلى PSA)
- **اسم المهمة في المشروع:** مزامنة الفئات إلى PSA

### <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| كيان التكامل للفئات | فئات الحركات     |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة فئات مصروفات المشروع في Finance and Operations، وتتم مزامنتها لـ Project Service Automation كفئات حركات.

### <a name="power-query"></a>Power Query

عند المزامنة إلى Project Service Automation، يجب عليك استخدام Microsoft Power Query لـ Excel لتعيين نوع الفوترة في فئة الحركة. يوفر قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA) تعيينًا وعمودًا افتراضيًا. إذا قمت بإنشاء قالبك الخاص، يجب عليك إضافة عمود شرطي في Power Query. اتبع الخطوات التالية.

1. انقر فوق السهم لفتح تعيين مهمة فئات حركات مصروفات المشروع في قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA).
2. انقر فوق الارتباط **الاستعلام المتقدم والتصفية** لفتح Power Query.
2. حدد **إضافة عمود شرطي**.
3. أدخل اسمًا للعمود الجديد، مثل **BillingType‎**.
4. أدخل الشرط التالي: **إذا لم تكن قيمة CATEGORYID تساوي null، عندئذٍ 19235001، وإلا null**.
5. انقر فوق **موافق** في العمود.
6. تأكد من تعيين هذا العمود الجديد في صفحة التعيين.

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance and Operations إلى Project Service Automation.

[![تعيين القالب](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>مزامنة فئات مصروفات المشروع من Project Service Automation إلى Finance and Operations

### <a name="template-and-task"></a>القالب والمهمة

يتم استخدام القالب والمهمة الأساسية التالية لمزامنة فئات مصروفات المشروع من Project Service Automation إلى Finance and Operations:

- **اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (PSA إلى Fin and Ops)
- **اسم المهمة في المشروع:** مزامنة الفئات إلى Fin Ops

### <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| فئات الحركات     | كيان التكامل للفئات |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة فئات مصروفات المشروع في Finance and Operations، وتتم مزامنتها لـ Project Service Automation كفئات حركات. تؤدي المزامنة مرة أخرى إلى Finance and Operations إلى تحديث فئة المشروع في Finance and Operations مع معرّف التكامل من Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
