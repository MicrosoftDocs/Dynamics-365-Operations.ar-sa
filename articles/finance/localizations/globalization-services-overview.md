---
title: خدمات العولمة في Dynamics 365
description: توفر هذه المقالة نظرة عامة على خدمات العولمة في Microsoft Dynamics 365.
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278221"
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
| Dynamics 365 Finance | ‏‏نعم‬ | ‏‏نعم‬ | ‏‏نعم‬ | 
| Dynamics 365 Supply Chain Management | ‏‏نعم‬ | ‏‏نعم‬ | ‏‏نعم‬ | 
| Dynamics 365 Project Operations | ‏‏نعم‬ | ‏‏نعم‬ | غير قابل للتطبيق | 
| Dynamics 365 Commerce | ‏‏نعم‬ | غير قابل للتطبيق | غير قابل للتطبيق | 

> [!NOTE]
> نظرًا للاختلافات في توفر المواقع الجغرافية الخاصة بـ Azure لخدمة RCS، قد يتسبب تكوين هذه الخدمة في تحويل بيانات العميل خارج المواقع الجغرافية التي تم تحديدها لخدمه Dynamics 365 عبر الإنترنت القابلة للتطبيق. لمزيد من المعلومات، راجع [Dynamics 365 وPower Platform: التوافر وموقع البيانات واللغة والترجمة](https://aka.ms/rcs/D365Productavailabilityguide).
