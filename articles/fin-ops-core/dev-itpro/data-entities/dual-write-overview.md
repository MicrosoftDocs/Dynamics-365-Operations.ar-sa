---
title: تكامل البيانات في وقت قريب من الحقيقي مع Common Data Service
description: يصف هذا الموضوع نظرة عامة على التكامل بين Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853896"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>تكامل البيانات في وقت قريب من الحقيقي مع Common Data Service

[!include [banner](../includes/banner.md)]

في العالم الرقمي الحالي، تستخدم الأنظمة البيئية للأعمال تطبيقات Microsoft Dynamics 365 كوحدة متكاملة. نظرًا لتدفق البيانات من الأشخاص والعملاء والعمليات وأجهزة إنترنت الأشياء (IoT) إلى مصدر واحد، فهناك فرصة لحلقات الملاحظات الرقمية. لتحقيق هذه التجربة، يعتبر التكامل بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى أمرًا أساسيًا. تم بناء بعض التطبيقات بالاستناد إلى Common Data Service. يسمح التكامل بين بيانات تطبيقات Finance and Operations وCommon Data Service لتطبيقات أخرى بالتواصل بطريقة متماسكة وسلسة مع Finance and Operations.

توفر تطبيقات Finance and Operations وCommon Data Service إمكانية مزامنة البيانات في وقت قريب من الحقيقي بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى من خلال إطار عمل الكتابة المزدوجة. تعتبر هذه التغطية واسعة النطاق وتشمل 28 مجالاً من التطبيق. الهدف هو توفير تجربة مستخدم "One Dynamics 365" من خلال تدفقات البيانات السلسة التي تربط العمليات التجارية عبر التطبيقات.

![رسم تخطيطي للنظرة عامة على البنية الهندسية](media/dual-write-overview.jpg)

تتوفر مقترحات القيمة التالية:

+ [التدرج الهرمي للمؤسسات في Common Data Service](dual-write-organization.md)
+ [مفهوم الشركة في Common Data Service](dual-write-company.md)
+ [أصل العميل المتكامل](dual-write-customer.md)
+ [دفتر الأستاذ المتكامل](dual-write-ledger.md)
+ [تجربه المنتج الموحدة](dual-write-product.md)
+ [أصل المورّد المتكامل](dual-write-vendor.md)
+ [المواقع والمستودعات المتكاملة](dual-write-sites-and-warehouses.md)
+ [أصل الضريبة المتكامل](dual-write-tax.md)

## <a name="system-requirements"></a>متطلبات النظام

تحتاج تدفقات البيانات المتزامنة وثنائية الاتجاه وفي الوقت الحقيقي تقريبًا الإصدارات التالية:

+ Microsoft Dynamics 365 for Finance and Operations الإصدار 10.0.4 (يوليو 2019) مع platform update 28 أو أعلى
+ Microsoft Dynamics 365 for Customer Engagement، إصدار Platform 9.1 (4.2) أو إصدار لاحق

## <a name="setup-instructions"></a>تعليمات الإعداد

اتبع هذه الخطوات لإعداد التكامل بين تطبيقات Finance and Operations وCommon Data Service.
    
1. فيما يتعلق بإعداد نظام الكتابة المزدوجة، راجع [الدليل المفصل خطوة بخطوة](https://aka.ms/dualwrite-docs) حول الإعلان عن معاينة الكتابة المزدوجة.
2. تحميل وتثبيت الحل من [Fin Ops وتكامل CDS/CE عبر الكتابة المزدوجة](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) مجموعة Yammer . تحتوي الحزمة على خمسة حلول:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. اتبع ترتيب التنفيذ من أجل [مزامنة البيانات المرجعية الأولية](dual-write-initial.md).
4. إذا واجهت مشكلات تتعلق بمزامنة الكتابة المزدوجة، فراجع [دليل استكشاف أخطاء تكامل البيانات وإصلاحها](dual-write-troubleshooting.md).

> [!IMPORTANT]
> لا يمكنك تشغيل الكتابة المزدوجة‏‎ جنبًا إلى جنب مع حل [العميل المتوقع إلى النقدية‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct). إذا كنت تقوم بتشغيل حل "العميل المتوقع إلى النقدية‬"، فيجب إلغاء تثبيته. يجب أيضًا تعطيل قوالب الكتابة المزدوجة للعميل والمورد التي تشكل جزءًا من الحل "العميل المتوقع إلى النقدية‬".
