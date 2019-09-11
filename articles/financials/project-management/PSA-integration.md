---
title: نظرة عامة حول Project Service Automation
description: يوفر هذا الموضوع معلومات حول حل تكامل Project Service Automation إلى Finance and Operations. يستخدم حل التكامل هذا ميزة "تكامل البيانات" لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Project Service Automation عبر Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865618"
---
# <a name="project-service-automation-overview"></a>نظرة عامة حول Project Service Automation

[!include[banner](../includes/banner.md)]

يستخدم حل تكامل Project Service Automation مع Finance and Operations ميزة "تكامل البيانات" لمزامنة البيانات عبر مثيلات Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Project Service Automation عبر Common Data Service. تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق المشاريع وعقود المشاريع وبنود عقود المشاريع والمراحل الرئيسية لبنود عقود المشاريع ومهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات من Project Service Automation إلى Finance and Operations.

> [!NOTE]
> - إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.
> - إذا كنت تستخدم Finance and Operations 7.3.0، فيجب تثبيت KB 4074835. سوف يسمح لك هذا بإجراء تكامل للمشاريع ثابتة السعر.
> - إذا كنت تستخدم Finance and Operations 7.3.0، وتعمل على إحضار حركات الرسوم من Project Service Automation، فيجب تثبيت KB 4345320 لتضمين تلك الرسوم في فاتورة المشروع.
> - إذا كنت تستخدم الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations، ستتمكن من استخدام ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة.
> - إذا كنت تستخدم الإصدار 8.0.1 من Microsoft Dynamics 365 for Finance and Operations أو إصدار لاحق، فستتمكن من مزامنة القيم الفعلية.

قبل أن تتمكن من دمج Project Service Automation مع Finance and Operations، يجب عليك تكوين محددات تكامل Project Service Automation. لمزيد من المعلومات، راجع [محددات تكامل Project Service Automation](PSA-parameters.md).

يتيح حل التكامل هذا مزامنة مباشرة في السيناريوهات التالية:

- الحفاظ على عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- إنشاء مشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ بنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ على المراحل الرئيسية لبنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ على مهام المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance and Operations.
- الحفاظ على فئات حركات المصروفات في Finance and Operations، ومزامنتهم مباشرةً من Finance and Operations إلى Project Service Automation.
- إنشاء تقديرات عدد ساعات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.
- إنشاء تقديرات مصروفات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance and Operations.
- إنشاء قيم فعلية للوقت والمصروفات والرسوم في Project Service Automation، وإنشاء حركات المشروع في دفتر يومية تكامل Project Service Automation لتمكين ترحيلها في Finance and Operations.

## <a name="data-synchronization"></a>مزامنة البيانات

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات كجزء من التكامل بين Project Service Automation و Finance and Operations.

> [!NOTE]
> لا تتوافر جميع القوالب في الوقت الحالي. سوف يتم إصدار القوالب بمجرد اكتمالها.

[![تكامل Project Service Automation مع Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations

لاستخدام حل تكامل Project Service Automation مع Finance and Operations، يجب عليك تثبيت Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 مع platform update 12 أو إصدار لاحق.

## <a name="system-requirements-for-project-service-automation"></a>متطلبات النظام لـ Project Service Automation

لاستخدام حل تكامل Project Service Automation إلى Finance and Operations، يجب عليك تثبيت المكونات التالية:

- الإصدار 9.0.0.0 من Microsoft Dynamics 365 for Project Service Automation أو إصدار لاحق
- حل العميل المتوقع إلى النقدية لتطبيق Microsoft Dynamics 365 for Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.
- حل Project Service Automation إلى Finance and Operations للإصدار 1.0.0.0 أو إصدار لاحق من Microsoft Dynamics 365 for Project Service Automation

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>تثبيت حل تكامل Project Service Automation إلى Finance and Operations في مثيل Project Service Automation الخاص بك

قم بتنزيل حل تكامل Project Service Automation إلى Finance and Operations من [مركز التنزيل لـ Microsoft](https://www.microsoft.com/download/details.aspx?id=57016)، واتبع الإرشادات المضمنة مع الحل.
