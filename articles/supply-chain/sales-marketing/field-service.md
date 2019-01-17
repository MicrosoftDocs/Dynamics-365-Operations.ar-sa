---
title: "التكامل مع Microsoft Dynamics 365 for Field Service"
description: "يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: ar-sa
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>التكامل مع Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

يعمل Microsoft Dynamics 365 for Finance and Operations على تمكين مزامنة عمليات الأعمال بين Finance and Operations وMicrosoft Dynamics 365 for Field Service. يتم تكوين سيناريوهات التكامل باستخدام قوالب مطور البيانات القابلة للتوسيع وCommon Data Service (CDS) لتمكين مزامنة عمليات الأعمال.
يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة، حيث يمكن تعيين حقول وكيانات مخصصة وقياسية إضافية لضبط التكامل والوفاء بمتطلبات أعمال معينة. 

يستند تكامل Field Service إلى الوظيفة الموجودة "العميل المتوقع إلى النقدية‬".

![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/field-service-integration.png)

تنصب المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Finance and Operations. يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل لـ Finance and Operations كأوامر مبيعات. في Finance and Operations، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير. بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service لـ Finance and Operations. يقوم مطور بيانات Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص. يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الحقول المخصصة والقياسية الإضافية، وكذلك الكيانات، لتعديل التكامل والوفاء بالمتطلبات المحددة.

تعمل المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين مزامنة العناصر التالية:

- [المنتجات في Finance and Operations للمنتجات في Field Service التي تشمل معلومات نوع المنتج](field-service-product.md)
- [أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations](field-service-work-order.md)
- [الفواتير في Field Service لفواتير النص الحر في Finance and Operations](field-service-invoice.md)

للاطلاع على مثال حول الطريقة التي يمكنك من خلالها مزامنة أمر عمل بين Field Service وFinance and Operations، شاهد فيديو YouTube القصير [كيفية مزامنة أمر عمل مع تكامل Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations
يدعم تكامل Field Service الإصدارات التالية:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations، إصدار 8.0 (إبريل 2018) أو إصدار أحدث

- تم إصدار Dynamics 365 for Finance and Operations، إصدار 8.0 في أبريل 2018 ويشتمل على رقم إصدار تطبيق 8.0.30.8020 مع تحديث النظام الأساسي 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>متطلبات النظام لـ Field Service
لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>الإصدار 9.0 من Microsoft Dynamics 365 for Field Service أو إصدار أحدث

- Dynamics 365 for Field Service، الإصدار 1612 (9.0.1.733) (DB 9.0.1.733) عبر الإنترنت أو إصدار أحدث.
- حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- حل تكامل Field Service، إصدار 1.0.0.0 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>التكامل مع Microsoft Dynamics 365 for Field Service، بما في ذلك معلومات المشروع والمخزون

تركز الوظيفة الإضافية في هذه المرحلة الثانية على تقديم معلومات لفنيي الخدمة حول معلومات المخزون من Finance and Operations، مما يسمح لهم بتحديث مستويات المخزون وإجراء عمليات تحويل المواد. بالإضافة إلى ذلك، فإن الشركات التي تقوم بتثبيت أو صيانة السلع المباعة تستفيد من إمكانية تحكم أفضل بالإضافة إلى رؤية أوضح لعملية البيع والخدمة الكاملة مع التكامل من المشاريع.

### <a name="functionality-includes-integration-of"></a>تتضمن الوظيفة تكامل:
- معلومات المستودع
- معلومات المخزون المتاح
- عمليات تحويل المخزون
- تعديلات المخزون
- مشاريع Dynamics 365 for Finance and Operations المتصلة بأوامر عمل Dynamics 365 for Field Service
- تطبق أوامر عمل Dynamics 365 for Field Service التي لديها ارتباط بمشاريع Dynamics 365 for Finance and Operations رقم المشروع هذا على أمر مبيعات Dynamics 365 for Finance and Operations للسماح بالفوترة من المشروع. 

![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>تعمل المرحلة الثانية من التكامل بين Field Service وFinance and Operations على تمكين المزامنة مع القوالب التالية:
- المستودعات (Fin and Ops إلى Field Service) - المستودعات من Finance and Operations إلى Field Service [استعلام متقدم] 
- مخزون المنتج (Fin and Ops إلى Field Service) - معلومات مستوى المخزون من Finance and Operations إلى Field Service [استعلام متقدم] 
- تسوية المخزون (Field Service إلى Fin and Ops) - تسويات المخزون من Field Service إلى Finance and Operations [استعلام متقدم] 
- عمليات تحويل المخزون (Field Service إلى Fin and Ops) - عمليات تحويل المخزون من Field Service إلى Finance and Operations [استعلام متقدم] 
- المشاريع (Fin and Ops إلى Field Service) - قائمة المشاريع من Finance and Operations إلى Field Service 
- أوامر العمل مع المشروع (Field Service إلى Fin and Ops) - أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations، مع دعم للمشروع [استعلام متقدم] 
- منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)‏ - "منتجات قابلة للبيع تم إصدارها‬" في Finance and Operations إلى "منتجات" Sales لـ Field Service، بما في ذلك وحدة المخزون 

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations
يدعم تكامل Field Service الإصدارات التالية:

- تم إطلاق الإصدار 8.1.2 من Dynamics 365 for Finance and Operations (ديسمبر 2019) في ديسمبر 2019 ويشتمل على رقم إصدار التطبيق 8.1.195 مع Platform Update 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>متطلبات النظام لـ Field Service
لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:

- Field Service for Dynamics 365 (الإصدار 8.2.0.286) أو إصدار لاحق على Dynamics 365 9.1.x - تم إطلاقه في نوفمبر 2018
- حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- حل 'تكامل Field Service، والمشروع والمخزون' لبرنامج Dynamics 365، الإصدار 2.0.0.0 أو إصدار لاحق. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

