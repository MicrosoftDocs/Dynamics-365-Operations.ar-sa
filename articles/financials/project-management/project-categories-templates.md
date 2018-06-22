---
title: "مزامنة فئات مصروفات المشروع من Project Service Automation"
description: "يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بينMicrosoft Dynamics 365 for  Finance and Operations و Dynamics 365 for Project Service Automation."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>مزامنة فئات مصروفات المشروع بين Finance and Operations و Project Service Automation

يوضح هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فئات مصروفات المشروع بينMicrosoft Dynamics 365 for  Finance and Operations و Dynamics 365 for Project Service Automation.

> [!NOTE]
> تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation و Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation و Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بفئات حركات مصروفات المشروع بين Project Service Automation و Finance and Operations.

إذا تم التحكم في فئات مصروفات المشروع في Finance and Operations، يكون تدفق التكامل أولًا من Finance and Operations إلى Project Service Automation، ومن ثم تحديث معرفات تكامل فئات مصروفات المشروع عن طريق المزامنة من Project Service Automation إلى Finance and Operations.

إذا تم التحكم في فئات مصروفات المشروع في Project Service Automation، فيكون تدفق التكامل أولًا من Project Service Automation إلى Finance and Operations. يجب أن تكون فئات المشروع قد تم تكوينها مسبقًا في Finance and Operations للمزامنة من Project Service Automation. ثم المزامنة من Finance and Operations مرة أخرى إلى Project Service Automation، ثم من Project Service Automation إلى Finance and Operations مرة أخرى. يضمن ذلك ارتباط الفئات وعدم إنشاء تكرارات.

> [!NOTE]
> وعادةً، سوف يتم التحكم في فئات مصروفات المشروع في Finance and Operations. وإذا كان الموقف غير ذلك، أو إذا كان لديك فئات مصروفات تم إنشاؤها مسبقًا في Project Service Automation، يجب عليك أولًا المزامنة باستخدام فئات حركات مصروفات المشروعات (PSA إلى Fin and Ops)، ثم المزامنة باستخدام فئات حركات مصروفات المشروعات (Fin and Ops إلى PSA). بعد ذلك، يجب تشغيل المزامنة من PSA إلى Fin and Ops مرة أخرى.

> إذا تمت المزامنة لأول مرة من Project Service Automation، يجب أن يتم إعداد فئات المشروع مسبقًا في Finance and Operations، ويجب إعداد فئات المشروع التي تتطلب المزامنة مع فئات حركات Project Service Automation لتكون **نشط في دفاتر اليومية**.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهمة الأساسية لمزامنة فئات مصروفات المشروع من Finance and Operations إلى Project Service Automation:

-  **اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (Fin and Ops إلى PSA)
-  **اسم المهمة في المشروع:** مزامنة الفئات إلى PSA

## <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| كيان التكامل للفئات    | فئات الحركات        |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة فئات مصروفات المشروع في Finance and Operations، وتتم مزامنتها لـ Project Service Automation كفئات حركات.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query لتعيين نوع الفوترة في فئة الحركة عند المزامنة إلى Project Service Automation. يحتوي قالب فئات حركات مصروفات المشروع (Fin and Ops إلى PSA) على عمود افتراضي وتعيين متوفر مسبقًا. إذا قمت بإنشاء قالبك الخاص، يجب عليك إضافة عمود شرطي في Power Query.
- افتح استعلام متقدم ونموذج تصفية ضمن مهمة تعيين فئات مصروفات المشروع.
- حدد **إضافة عمود شرطي**.
- قم بتسمية العمود الجديد، على سبيل المثال BilingType.
- إدخال الشرط التالي: إذا **كان CATEGORYID لا يساوي قيمة فارغة فمن ثم يساوي 19235001، وإلا يكون فارغًا**.
- انقر فوق **موافق** في العمود.
- تأكد من تعيين هذا العمود الجديد في صفحة التعيين.

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance and Operations إلى Project Service Automation.

[![تعيين القالب](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

يتم استخدام القالب التالي والمهمة الأساسية لمزامنة فئات مصروفات المشروع من Project Service Automation إلى Finance and Operations:

-**اسم القالب في تكامل البيانات:** فئات حركات مصروفات المشروع (PSA إلى Fin and Ops)-**اسم المهمة في المشروع:** مزامنة الفئات إلى Fin Ops

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| فئات الحركات          | كيان التكامل للفئات  | 

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة فئات مصروفات المشروع في Finance and Operations، وتتم مزامنتها لـ Project Service Automation كفئات حركات. تُحدث المزامنة مرة أخرى إلى Finance and Operation مُعرف التكامل من Project Service Automation في فئة مشروع Finance and Operations .

يبين الشكل التوضيحي التالي مثالاً لتعيين مهمة القالب في تكامل البيانات.

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

