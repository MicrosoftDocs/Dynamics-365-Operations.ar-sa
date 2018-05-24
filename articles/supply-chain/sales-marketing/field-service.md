---
title: "التكامل مع Microsoft Dynamics 365 for Field Service"
description: "يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>التكامل مع Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

يعمل Microsoft Dynamics 365 for Field Service على تمكين مزامنة عمليات الأعمال بين Finance and Operations وMicrosoft Dynamics 365 for Field Service. يتم تكوين سيناريوهات التكامل باستخدام قوالب مطور البيانات القابلة للتوسيع وCommon Data Service (CDS) لتمكين مزامنة عمليات الأعمال.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/field-service-integration.png)](./media/field-service-integration.png)

تنصب المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Finance and Operations. يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل لـ Finance and Operations كأوامر مبيعات. في Finance and Operations، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير. بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service لـ Finance and Operations. يقوم مطور بيانات Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص. يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الحقول المخصصة والقياسية الإضافية، وكذلك الكيانات، لتعديل التكامل والوفاء بالمتطلبات المحددة.

تعمل المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين مزامنة العناصر التالية:

- [المنتجات في Finance and Operations للمنتجات في Field Service التي تشمل معلومات نوع المنتج](field-service-product.md)
- [أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations](field-service-work-order.md)
- [الفواتير في Field Service لفواتير النص الحر في Finance and Operations](field-service-invoice.md)

لمشاهدة مثال عن كيف يمكن مزامنة أمر عمل بين Field Service وFinance and Operations، شاهد فيديو YouTube القصير:

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[مزامنة أمر عمل بين Field Service and Finance وOperations (فيديو YouTube)](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations
يدعم تكامل Field Service الإصدارات التالية:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations، إصدار 8.0 (إبريل 2018) أو إصدار أحدث

- تم إصدار Dynamics 365 for Finance and Operations، إصدار 8.0 في أبريل 2018 ويشتمل على رقم إصدار تطبيق 8.0.30.8020 مع تحديث النظام الأساسي 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>متطلبات النظام لـ Field Service
لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>الإصدار 9.0 من Microsoft Dynamics 365 for Field Service أو إصدار أحدث

- Dynamics 365 for Field Service، الإصدار 1612 (9.0.1.733) (DB 9.0.1.733) عبر الإنترنت أو إصدار أحدث.
- حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- حل تكامل Field Service، إصدار 1.0.0.0 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

