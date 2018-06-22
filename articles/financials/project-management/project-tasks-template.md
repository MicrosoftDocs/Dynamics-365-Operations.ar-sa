---
title: "مزامنة مهام المشروع من Project Service Automation"
description: "يوضح هذا الموضوع القالب والمهمة الأساسية التي يتم استخدامها لمزامنة مهام المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations."
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
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>مزامنة مهام المشروع من Project Service Automation مباشرة إلى أنشطة المشاريع في Finance and Operations

يوضح هذا الموضوع القالب والمهمة الأساسية التي يتم استخدامها لمزامنة مهام المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations.

> [!NOTE]
> تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations يتيح قالب التكامل المتوفر مع ميزة تكامل البيانات تدفق البيانات الخاصة بمهام المشاريع من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>القالب والمهمة

للوصول إلى القالب، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهمة الأساسية لمزامنة مهام المشروع من Project Service Automation إلى Finance and Operations.

-**اسم القالب في تكامل البيانات:** مهام المشاريع (PSA إلى Fin and Ops)-**اسم المهمة في المشروع:** مهام المشاريع

قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.

## <a name="entity-set"></a>مجموعة الكيانات

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| مهام المشروع                           | كيان التكامل لمهمة المشروع.   |

## <a name="entity-flow"></a>تدفق الكيان

تتم إدارة مهام المشاريع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كأنشطة مشاريع.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.

## <a name="power-query"></a>Power Query

يجب عليك استخدام Microsoft Power Query لتصفية البيانات في حالة تحقق هذه الشروط:

- لديم سجلات موارد محددة في مهمة مشروع.

إذا كنت مضطرًا إلى استخدام Power Query، اتبع هذه الإرشادات:

- يحتوي قالب مهام المشاريع (PSA إلى Fin and Ops) على عامل تصفية افتراضي لاستبعاد سجلات موارد معينة من ضمن مهمة مشروع من خلال تعيين عامل التصفية في **IsLineTask** إلى **خطأ**. إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيينات مهمام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


