---
title: نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service
description: يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 22abe83f06b7fc57c73fb82ccafc4b426667e7c6
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865175"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service-overview"></a>نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

يمكّن Microsoft Dynamics 365 for Finance and Operations مزامنة عمليات الأعمال بين Finance and Operations وMicrosoft Dynamics 365 for Field Service. تم تكوين سيناريوهات التكامل باستخدام قوالب موحد البيانات القابلة للتوسيع وCommon Data Service (CDS) لتمكين مزامنة عمليات الأعمال.
يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة، حيث يمكن تعيين حقول وكيانات مخصصة وقياسية إضافية لضبط التكامل والوفاء بمتطلبات أعمال معينة. 

يستند تكامل Field Service إلى الوظيفة الموجودة "العميل المتوقع إلى النقدية‬".

![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/field-service-integration.png)

تنصب المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Finance and Operations. يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل لـ Finance and Operations كأوامر مبيعات. في Finance and Operations، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير. بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service لـ Finance and Operations. يقوم موحد البيانات في Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص. يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الحقول المخصصة والقياسية الإضافية، وكذلك الكيانات، لتعديل التكامل والوفاء بالمتطلبات المحددة.

تعمل المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين مزامنة العناصر التالية:

- [المنتجات في Finance and Operations للمنتجات في Field Service التي تشمل معلومات نوع المنتج](field-service-product.md)
- [أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations](field-service-work-order.md)
- [الفواتير في Field Service لفواتير النص الحر في Finance and Operations](field-service-invoice.md)

للاطلاع على مثال حول الطريقة التي يمكنك من خلالها مزامنة أمر عمل بين Field Service وFinance and Operations، شاهد فيديو YouTube القصير [كيفية مزامنة أمر عمل مع تكامل Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>التكامل مع Microsoft Dynamics 365 for Field Service، بما في ذلك معلومات حول المخزون والمشروع

تركز الوظيفة الإضافية في هذه المرحلة الثانية على تقديم معلومات لفنيي الخدمة حول معلومات المخزون من Finance and Operations، مما يسمح لهم بتحديث مستويات المخزون وإجراء عمليات تحويل المواد. بالإضافة إلى ذلك، فإن الشركات التي تقوم بتثبيت أو صيانة السلع المباعة تستفيد من إمكانية تحكم أفضل بالإضافة إلى رؤية أوضح لعملية البيع والخدمة الكاملة مع التكامل من المشاريع.

### <a name="functionality-includes-integration-of"></a>تتضمن الوظيفة تكامل:
- معلومات المستودع
- معلومات المخزون المتاح
- عمليات تحويل المخزون
- تعديلات المخزون
- مشاريع Dynamics 365 for Finance and Operations المتصلة بأوامر عمل Dynamics 365 for Field Service
- تقوم أوامر عمل Dynamics 365 for Field Service التي لديها ارتباط إلى مشاريع Dynamics 365 for Finance and Operations بتطبيق المشروع هذا على أمر مبيعات Dynamics 365 for Finance and Operations للسماح بالفوترة من المشروع. 

![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>تعمل المرحلة الثانية من التكامل بين Field Service وFinance and Operations على تمكين المزامنة مع القوالب التالية:
- المستودعات (Fin and Ops إلى Field Service) - المستودعات من Finance and Operations إلى Field Service [استعلام متقدم] 
- مخزون المنتج (Fin and Ops إلى Field Service) - معلومات مستوى المخزون من Finance and Operations إلى Field Service [استعلام متقدم] 
- تسوية المخزون (Field Service إلى Fin and Ops) - تسويات المخزون من Field Service إلى Finance and Operations [استعلام متقدم] 
- عمليات تحويل المخزون (Field Service إلى Fin and Ops) - عمليات تحويل المخزون من Field Service إلى Finance and Operations [استعلام متقدم] 
- المشاريع (Fin and Ops إلى Field Service) - قائمة المشاريع من Finance and Operations إلى Field Service 
- أوامر العمل مع المشروع (Field Service إلى Fin and Ops) - أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations، مع دعم للمشروع [استعلام متقدم] 
- منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)‏ - "منتجات قابلة للبيع تم إصدارها‬" في Finance and Operations إلى "منتجات" Sales لـ Field Service، بما في ذلك وحدة المخزون 

## <a name="system-requirements"></a>متطلبات النظام

### <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations
يدعم تكامل Field Service الإصدارات التالية:

- تم طرح الإصدار 8.1.2 من Dynamics 365 for Finance and Operations (ديسمبر 2018) في شهر ديسمبر 2018 وله رقم إصدار التطبيق 8.1.195 مع Platform Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>متطلبات النظام لـ Field Service
لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:

- Field Service for Dynamics 365 (الإصدار 8.2.0.286) أو إصدار لاحق على Dynamics 365 9.1.x - تم إطلاقه في شهر نوفمبر 2018
- حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- حل 'تكامل Field Service، والمشروع والمخزون' لبرنامج Dynamics 365، الإصدار 2.0.0.0 أو إصدار لاحق. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
