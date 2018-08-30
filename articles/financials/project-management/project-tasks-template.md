---
title: "مزامنة مهام المشروع مباشرةً من Project Service Automation إلى Finance and Operations"
description: "يصف هذا الموضوع القالب والمهمة الأساسية المستخدمين لمزامنة مهام المشروع مباشرةً من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations."
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
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>مزامنة مهام المشروع مباشرةً من Project Service Automation إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القالب والمهمة الأساسية المستخدمين لمزامنة مهام المشروع مباشرةً من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations.
> - إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستتمكن من استخدام القوالب لإجراء تكامل لمهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية ولتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.
> - يتوافر تكامل القيم الفعلية في Microsoft Dynamics 365 for Finance and Operations، الإصدار 8.01 أو إصدار لاحق.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations يتيح قالب التكامل المتوفر مع ميزة تكامل البيانات تدفق البيانات الخاصة بمهام المشاريع من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>القالب والمهمة

للوصول إلى القالب، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يُستخدم القالب التالي والمهمة الأساسية التالية لمزامنة مهام المشروع من Project Service Automation إلى Finance and Operations.

- **اسم القالب في تكامل البيانات:** مهام المشروع (PSA إلى Fin and Ops)
- **اسم المهمة في المشروع:** مهام المشروع

قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.

## <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| مهام المشروع              | كيان تكامل مهام المشروع |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة مهام المشاريع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كأنشطة مشاريع.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query لـ Excel لتصفية البيانات في حالة تحقق الشرط التالي:

- لديك سجلات خاصة بالموارد في مهمة مشروع.

إذا كنت مضطرًا إلى استخدام Power Query، فاتبع هذه الإرشادات:

- يتضمن قالب مهام المشروع (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يستبعد سجلات خاصة بالموارد من ضمن مهمة مشروع من خلال تعيين عامل التصفية في **IsLineTask** إلى **False**. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيينات مهمام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)

