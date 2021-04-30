---
title: خدمات العولمة في Dynamics 365
description: يقدم هذا الموضوع نظرة عامة على خدمات العولمة في Microsoft Dynamics 365.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893037"
---
# <a name="dynamics-365-globalization-services"></a>خدمات العولمة في Dynamics 365

[!include [banner](../includes/banner.md)]

يمكن تكوين خدمات العولمة التالية لتوسيع الإمكانيات الموجودة في بعض خدمات Microsoft Dynamics 365 عبر الإنترنت:

- تدعم خدمة **Regulatory Configuration Service (RCS)** تكوين أنواع مختلفة من المستندات والتقارير الإلكترونية. توفر RCS إصدارًا محسنًا لمصمم التقارير الإلكترونية حيث مستودع التكوين هو خدمة مستقلة. لمزيد من المعلومات، راجع [Regulatory Configuration Service](rcs-overview.md).
- تجمع **الفوترة الإلكترونية** تنسيقات قابلة للتكوين الخاصة بعمليات التحويل والتوقيعات الرقمية وعمليات التكامل القابلة للتكوين للاتصال بخدمات الويب الخارجية، بما في ذلك معالجة الشهادات والردود.. لمزيد من المعلومات، راجع [الفوترة الإلكترونية‎](e-invoicing-service-overview.md).
- يوفر **حساب الضريبة** مرونة محسنة من خلال دعم معرفات ضرائب متعددة وتحديد كود الضريبة ومصمم حساب الضريبة ومشغل وقت التشغيل للتوافق مع اللوائح الضريبية المعقدة على مستوى العالم. لمزيد من المعلومات، راجع [حساب الضريبة](global-tax-calcuation-service-overview.md).

توفر خدمات العولمة هذه تكاملاً جاهزًا مع خدمات Dynamics 365 عبر الإنترنت التالية.

| الخدمة عبر الإنترنت | خدمة التكوين التنظيمية | الفوترة الإلكترونية | (إصدار أولي) حساب الضرائب |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | نعم | نعم | نعم | 
| Dynamics 365 Supply Chain Management | نعم | نعم | نعم | 
| Dynamics 365 Project Operations | نعم | نعم | غير قابل للتطبيق | 
| Dynamics 365 Commerce | نعم | غير قابل للتطبيق | غير قابل للتطبيق | 

> [!NOTE]
> نظرًا للاختلافات في توفر المواقع الجغرافية الخاصة بـ Azure لخدمة RCS، قد يتسبب تكوين هذه الخدمة في تحويل بيانات العميل خارج المواقع الجغرافية التي تم تحديدها لخدمه Dynamics 365 عبر الإنترنت القابلة للتطبيق. لمزيد من المعلومات، راجع [Dynamics 365 وPower Platform: التوافر وموقع البيانات واللغة والترجمة](https://aka.ms/rcs/D365Productavailabilityguide).