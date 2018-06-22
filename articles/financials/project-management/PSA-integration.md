---
title: Project Service Automation
description: "يستخدم هذا الحل ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations و Microsoft Dynamics 365 for Project Service Automation عبر Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

يستخدم حل تكامل Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations و Microsoft Dynamics 365 for Project Service Automation عبر Common Data Service (CDS). تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق المشاريع وعقود المشاريع وبنود عقود المشاريع والمراحل الرئيسية لبنود عقود المشاريع ومهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات من  Project Service Automation إلى Finance and Operations.

> [!NOTE] 
> إذا كنت تستخدم Dynamics 365 for Finance and Operations، إصدار Enterprise edition 7.3.0، فيجب عليك تثبيت قاعدة المعارف 4074835. سوف يسمح لك هذا بتكامل المشاريع ثابتة السعر.
>
> إذا كنت تستخدم  Dynamics 365 for Finance and Operations إصدار 8.0، فسوف تكون قادرًا على استخدام ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.
>
> إذا كنت تستخدم Dynamics 365 for Finance and Operations إصدار 8.0.1، فسوف تكون قادرًا على مزامنة القيم الفعلية.
>
> إذا كنت تستخدم Dynamics 365 for Finance and Operations، إصدار Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، فسوف تكون قادرًا على استخدام القوالب لتكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.

قبل أن تتمكن من دمج Project Service Automation مع Finance and Operations، يجب عليك تكوين محددات تكامل Project Service Automation. للحصول على المزيد من المعلومات، راجع محددات تكامل Project Service Automation.

يتيح حل التكامل هذا مزامنة مباشرة في السيناريوهات التالية:

- الحفاظ على عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- إنشاء مشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ بنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ على المراحل الرئيسية لبنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ على مهام المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ على فئات حركات المصروفات في Finance and Operations، ومزامنتهم مباشرةً من Finance and Operations إلى Project Service Automation.
- إنشاء تقديرات عدد ساعات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.
- إنشاء تقديرات مصروفات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.

## <a name="data-synchronization"></a>مزامنة البيانات
يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات كجزء من التكامل بين Project Service Automation و Finance and Operations.

> [!NOTE]
> لا تتوافر جميع القوالب في الوقت الحالي. سوف يتم إصدار القوالب بمجرد اكتمالها.

[![تكامل Project Service Automation مع Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations

لاستخدام Project Service Automation لحل تكامل Finance and Operations، يجب عليك تثبيت Microsoft Dynamics 365 for Finance and Operations إصدار Enterprise edition 7.3 مع تحديث النظام الأساسي 12 أو إصدار أحدث.

## <a name="system-requirements-for-project-service-automation"></a>متطلبات النظام لـ Project Service Automation

لاستخدام حل تكامل Project Service Automation إلى Finance and Operations، يجب عليك تثبيت المكونات التالية:

- Microsoft Dynamics 365 for Project Service Automation إصدار 9.0.0.0 أو أحدث.
- حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.
- حل Project Service Automation to Operations لـ Dynamics 365 for Project Service Automation إصدار 1.0.0.0 أو أحدث.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>تثبيت حل تكامل Project Service Automation إلى Finance and Operations في مثيل Project Service Automation الخاص بك



