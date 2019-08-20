---
title: تكامل البيانات في وقت قريب من الحقيقي‬ بين Finance and Operations وCommon Data Service
description: يوفر هذا الموضوع نظرة عامة على التكامل بين Microsoft Dynamics 365 for Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797218"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>تكامل البيانات في وقت قريب من الحقيقي‬ بين Finance and Operations وCommon Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

في العالم الرقمي الحالي، تستخدم الأنظمة البيئية للأعمال مجموعة Microsoft Dynamics 365 كوحدة متكاملة. نظرًا لتدفق البيانات من الأشخاص والعملاء والعمليات وأجهزة إنترنت الأشياء (IoT) إلى مصدر واحد، فهناك فرصة لحلقات الملاحظات الرقمية. لتحقيق هذه التجربة، يعتبر التكامل بين Dynamics 365 for Finance and Operations وتطبيقات Dynamics 365 for Customer Engagement أمرًا أساسيًا. تم بناء تطبيقات Customer Engagement بالاستناد إلى Common Data Service. يسمح التكامل بين بيانات Finance and Operations وCommon Data Service لتطبيقات Customer Engagement بالتواصل بطريقة متماسكة وسلسة مع Finance and Operations.

يوفر Finance and Operations وCommon Data Service إمكانية مزامنة البيانات في وقت قريب من بين Finance and Operations وتطبيقات Customer Engagement من خلال إطار عمل الكتابة المزدوجة. تعتبر هذه التغطية واسعة النطاق وتشمل 28 من مجالات Finance and Operations. الهدف هو توفير تجربة مستخدم "One Dynamics 365" من خلال تدفقات البيانات السلسة التي تربط العمليات التجارية عبر التطبيقات.

![رسم تخطيطي للنظرة عامة على البنية الهندسية](media/dual-write-overview.jpg)

تتوفر مقترحات القيمة التالية للعملاء:

+ [التدرج الهرمي للمؤسسات في Common Data Service](dual-write-organization.md)
+ [مفهوم الشركة في Common Data Service](dual-write-company.md)
+ [أصل العميل المتكامل](dual-write-customer.md)
+ [أصل المورّد المتكامل](dual-write-vendor.md)
+ أصل المنتج الموحد

## <a name="system-requirements"></a>متطلبات النظام

تحتاج تدفقات البيانات المتزامنة وثنائية الاتجاه وفي الوقت الحقيقي تقريبًا الإصدارات التالية:

+ Microsoft Dynamics 365 for Finance and Operations الإصدار 10.0.4 (يوليو 2019) مع platform update 28 أو أعلى
+ Microsoft Dynamics 365 for Customer Engagement، إصدار Platform 9.1 (4.2) أو إصدار لاحق

## <a name="setup-instructions"></a>تعليمات الإعداد

اتبع هذه الخطوات لإعداد التكامل بين Finance and Operations وCommon Data Service.
    
1. فيما يتعلق بإعداد نظام الكتابة المزدوجة، راجع [الدليل المفصل خطوة بخطوة](https://aka.ms/dualwrite-docs) حول الإعلان عن معاينة الكتابة المزدوجة.
2. يمكنك تنزيل الحل وتثبيته من مجموعة [تكامل Finance and Operations وCommon Data Service وCustomer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer. تحتوي الحزمة على خمسة حلول:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. اتبع ترتيب التنفيذ من أجل [مزامنة البيانات المرجعية الأولية](dual-write-initial.md).
4. إذا واجهت مشكلات تتعلق بمزامنة الكتابة المزدوجة، فراجع [دليل استكشاف أخطاء تكامل البيانات وإصلاحها](dual-write-troubleshooting.md).

> [!IMPORTANT]
> لا يمكنك تشغيل الكتابة المزدوجة‏‎ جنبًا إلى جنب مع حل [العميل المتوقع إلى النقدية‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct). إذا كنت تقوم بتشغيل حل "العميل المتوقع إلى النقدية‬"، فيجب إلغاء تثبيته. يجب أيضًا تعطيل قوالب الكتابة المزدوجة للعميل والمورد التي تشكل جزءًا من الحل "العميل المتوقع إلى النقدية‬".
