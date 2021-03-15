---
title: نظرة عامة على التكامل مع Microsoft Dynamics 365 Field Service
description: يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1b1f88c77ed891839adb57c2ba5e2f72f35fda6d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998468"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>نظرة عامة على التكامل مع Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يتيح Supply Chain Management مزامنة عمليات الأعمال بين Dynamics 365 Supply Chain Management وDynamics 365 Field Service. تم تكوين سيناريوهات التكامل باستخدام قوالب "موحد البيانات" القابلة للتوسعة وMicrosoft Dataverse لتمكين مزامنة عمليات الأعمال.
يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة، حيث يمكن تعيين أعمدة وحداول مخصصة وقياسية إضافية لضبط التكامل والوفاء بمتطلبات أعمال معينة. 

يستند تكامل Field Service إلى الوظيفة الموجودة "العميل المتوقع إلى النقدية‬".

![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/field-service-integration.png)

تركز المرحلة الأولى من التكامل بين Field Service وSupply Chain Management على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Supply Chain Management. يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل إلى Supply Chain Management كأوامر مبيعات. في Supply Chain Management، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير. بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service إلى Supply Chain Management. يقوم موحد البيانات في Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص. يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الأعمدة المخصصة والقياسية الإضافية، وكذلك الجداول، لتعديل التكامل والوفاء بالمتطلبات المحددة.

تعمل المرحلة الأولى من التكامل بين Field Service وSupply Chain Management على تمكين مزامنة العناصر التالية:

- [مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service](field-service-product.md)
- [مزامنة أوامر العمل في Field Service مع أوامر المبيعات في Supply Chain Management](field-service-work-order.md)
- [مزامنة فواتير الاتفاقيات في Field Service مع فواتير النص الحر في Supply Chain Management](field-service-invoice.md)

للاطلاع على مثال حول الطريقة التي يمكنك من خلالها مزامنة أمر عمل بين Field Service وSupply Chain Management، شاهد مقطع فيديو YouTube القصير [كيفية مزامنة أمر عمل مع تكامل Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>التكامل مع Field Service، بما في ذلك معلومات حول المخزون والمشروع

تركز الوظيفة الإضافية في هذه المرحلة الثانية على تقديم معلومات لفنيي الخدمة حول معلومات المخزون من Supply Chain Management، مما يسمح لهم بتحديث مستويات المخزون وإجراء عمليات تحويل المواد. بالإضافة إلى ذلك، فإن الشركات التي تقوم بتثبيت أو صيانة السلع المباعة تستفيد من إمكانية تحكم أفضل بالإضافة إلى رؤية أوضح لعملية البيع والخدمة الكاملة مع التكامل من المشاريع.

### <a name="functionality-includes-integration-of"></a>تتضمن الوظيفة تكامل:
- معلومات المستودع
- معلومات المخزون المتاح
- عمليات تحويل المخزون
- تعديلات المخزون
- ربط مشاريع Supply Chain Management مع أوامر عمل Dynamics 365 Field Service
- تقوم أوامر عمل Dynamics 365 Field Service التي لديها ارتباط مع مشاريع Supply Chain Management بتطبيق رقم المشروع هذا على أمر مبيعات للسماح بالفوترة من المشروع. 

![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>تعمل المرحلة الثانية من التكامل بين Field Service وSupply Chain Management على تمكين المزامنة مع القوالب التالية:
- المستودعات (Supply Chain Management إلى Field Service) - المستودعات من Supply Chain Management إلى Field Service [استعلام متقدم] 
- مخزون المنتجات (Supply Chain Management إلى Field Service) - معلومات مستوى المخزون من Supply Chain Management إلى Field Service [استعلام متقدم] 
- تسوية المخزون (Field Service إلى Supply Chain Management) - تسويات المخزون من Field Service إلى Supply Chain Management [استعلام متقدم] 
- عمليات تحويل المخزون‬ (Field Service إلى Supply Chain Management) - عمليات تحويل المخزون‬ من Field Service إلى Supply Chain Management [استعلام متقدم] 
- المشاريع (Supply Chain Management إلى Field Service) - قائمة المشاريع من Supply Chain Management إلى Field Service 
- أوامر العمل مع المشروع (Field Service إلى Supply Chain Management) - أوامر العمل في Field Service إلى أوامر المبيعات في Supply Chain Management، مع دعم للمشروع [استعلام متقدم] 
- منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)‏ - "منتجات قابلة للبيع تم إصدارها‬" في Supply Chain Management إلى "منتجات" Sales لـ Field Service، بما في ذلك وحدة المخزون 

## <a name="system-requirements"></a>متطلبات النظام

### <a name="system-requirements-for-supply-chain-management"></a>متطلبات النظام في Supply Chain Management
يدعم تكامل Field Service الإصدارات التالية:

- تم طرح الإصدار 8.1.2 من Dynamics 365 for Finance and Operations (ديسمبر 2018) في شهر ديسمبر 2018 وله رقم إصدار التطبيق 8.1.195 مع Platform update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>متطلبات النظام لـ Field Service
لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:

- Field Service (الإصدار 8.2.0.286) أو إصدار لاحق على Dynamics 365 9.1.x - تم إطلاقه في شهر نوفمبر 2018
- حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- حل 'تكامل Field Service، والمشروع والمخزون' لبرنامج Dynamics 365، الإصدار 2.0.0.0 أو إصدار لاحق. الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]