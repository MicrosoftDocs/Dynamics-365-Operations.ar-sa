---
title: نظرة عامة حول Project Service Automation
description: يوفر هذا الموضوع معلومات حل تكامل Dynamics 365 Project Service Automation إلى Dynamics 365 Finance .
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250543"
---
# <a name="project-service-automation-overview"></a>نظرة عامة حول Project Service Automation

[!include[banner](../includes/banner.md)]

يستخدم حل تكامل Project Service Automation مع Finance ميزة "تكامل البيانات" لمزامنة البيانات عبر مثيلات Dynamics 365 Finance وDynamics 365 Project Service Automation عبر Common Data Service. تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق المشاريع وعقود المشاريع وبنود عقود المشاريع والمراحل الرئيسية لبنود عقود المشاريع ومهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات من Project Service Automation إلى Finance.

> [!NOTE]
> - إذا كنت تستخدم الإصدار 7.3.0، فيجب تثبيت قاعدة المعارف 4074835. سوف يسمح لك هذا بإجراء تكامل للمشاريع ثابتة السعر.
> - إذا كنت تستخدم الإصدار 7.3.0، وتعمل على إحضار حركات الرسوم من Project Service Automation، فيجب تثبيت KB 4345320 لتضمين تلك الرسوم في فاتورة المشروع.
> - إذا كنت تستخدم الإصدار 8.0، ستتمكن من استخدام ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة.
> - إذا كنت تستخدم الإصدار 8.0.1 أو إصدار لاحق، فستتمكن من مزامنة القيم الفعلية.

قبل أن تتمكن من دمج Project Service Automation مع Finance، يجب عليك تكوين محددات تكامل Project Service Automation. لمزيد من المعلومات، راجع [محددات تكامل Project Service Automation](PSA-parameters.md).

يتيح حل التكامل هذا مزامنة مباشرة في السيناريوهات التالية:

- الحفاظ على عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.
- إنشاء مشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance.
- الحفاظ على بنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.
- الحفاظ على النقاط الرئيسية ببنود عقود المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.
- الحفاظ على مهام المشاريع في Project Service Automation، ومزامنتهم مباشرة من Project Service Automation إلى Finance.
- الحفاظ على فئات حركات المصروفات في Finance، ومزامنتهم مباشرةً من Finance إلى Project Service Automation.
- إنشاء تقديرات عدد ساعات المشاريع في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance.
- إنشاء تقديرات المصروفات للمشروع‬ات في Project Service Automation، ومزامنتها مباشرة من Project Service Automation إلى Finance.
- إنشاء قيم فعلية للوقت والمصروفات والرسوم في Project Service Automation، وإنشاء حركات المشروع في دفتر يومية تكامل Project Service Automation لتمكين ترحيلها في Finance.

## <a name="data-synchronization"></a>مزامنة البيانات

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات كجزء من التكامل بين Project Service Automation و Finance.

> [!NOTE]
> لا تتوافر جميع القوالب في الوقت الحالي. سوف يتم إصدار القوالب بمجرد اكتمالها.

[![تكامل Project Service Automation مع Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>متطلبات النظام لـ Finance

لاستخدام حل تكامل Project Service Automation مع Finance، يجب عليك تثبيت , Enterprise edition 7.3 مع platform update 12 أو إصدار لاحق.

## <a name="system-requirements-for-project-service-automation"></a>متطلبات النظام لـ Project Service Automation

لاستخدام حل تكامل Project Service Automation إلى Finance، يجب عليك تثبيت المكونات التالية:

- الإصدار 9.0.0.0 من Dynamics 365 Project Service Automation أو إصدار لاحق
- حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.
- حل Project Service Automation إلى Finance للإصدار 1.0.0.0 أو إصدار لاحق من Dynamics 365 Project Service Automation .

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>تثبيت حل تكامل Project Service Automation إلى Finance في مثيل Project Service Automation الخاص بك

قم بتنزيل حل تكامل Project Service Automation إلى Finance من [مركز التنزيل لـ Microsoft](https://www.microsoft.com/download/details.aspx?id=57016)، واتبع الإرشادات المضمنة مع الحل.
