---
title: "العميل المتوقع إلى النقدية"
description: "يوفر الموضوع نظرة عامة حول العميل المتوقع إلى النقدية بين Dynamics 365 for Finance and Operations, Enterprise Edition وDynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>العميل المتوقع إلى النقدية  

[!include[banner](../includes/banner.md)]

يستخدم حل العميل المتوقع إلى النقدية [تكامل البيانات](/common-data-service/entity-reference/dynamics-365-integration) لمزامنة البيانات عبر Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ومثيلات Dynamics 365 for Sales عبر Common Data Service (CDS). تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأومر المبيعات وفواتير المبيعات بين Finance and Operations وSales. بينما تتدفق البيانات بين Finance and Operations وSales، يمكنك تنفيذ أنشطة المبيعات والتسويق في Sales والتعامل مع تنفيذ الأوامر باستخدام إدارة المخزون في Finance and Operations. 

يوفر هذا الحل التكامل في النواحي التالية: 

-   [المحافظة على الحسابات في Sales ومزامنتها إلى Finance and Operations.](accounts-template-mapping.md)
-   [المحافظة على جهات الاتصال في Sales ومزامنتها إلى Finance and Operations.](contacts-template-mapping.md)
-   [المحافظة على المنتجات في Finance and Operations ومزامنتها إلى Sales‎.](products-template-mapping.md)
-   [إنشاء عروض أسعار المبيعات في Sales ومزامنتها إلى Finance and Operations](sales-quotation-template-mapping.md)
-   [إنشاء أوامر المبيعات في Finance and Operations ومزامنتها إلى Sales](sales-order-template-mapping.md)
-   [إنشاء فواتير المبيعات في Finance and Operations ومزامنتها إلى Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>متطلبات النظام لتطبيق Dynamics 365 for Finance and Operations, Enterprise Edition

لاستخدام حل العميل المتوقع إلى النقدية، يجب تثبيت ما يلي:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (يوليو 2017) مع تحديث النظام الأساسي 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)

- إصلاحين عاجلين لتطبيق Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017).

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - يمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات مع ميزة تكامل البيانات من Finance and Operations إلى Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - يمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات مع ميزة تكامل البيانات من Finance and Operations إلى Sales.
    
**ملاحظة**: تحتاج فقط إلى تثبيت KB4036524 لأن التثبيت يتضمن التغييرات من KB4036461.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>متطلبات النظام لتطبيق Dynamics 365 for Sales

لاستخدام حل العميل المتوقع إلى النقدية، يجب تثبيت ما يلي:

- Dynamics 365 for Sales الإصدار 1612 (8.2.1.207) (DB 8.2.1.207) عبر الإنترنت أو إصدار لاحق.
- حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.14.0.0 (v14) أو إصدار لاحق.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>تثبيت حل العميل المتوقع إلى النقدية في Sales

- قم بتنزيل [الملف المضغوط لحزمة حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.

- تأكد من أن الملف المضغوط غير محظور لكي لا تتلقى الرسالة "لم يتم العثور على حزم استيراد" عند تثبيت حزمة الحل. لإلغاء حظر الملف، قم بما يلي:

    -  انقر بزر الماوس الأيمن فوق الملف المضغوط.
    -  حدد **خصائص** ثم حدد **إلغاء الحظر**. 

- قم بإلغاء الضغط وتشغيل PackageDeployer.exe.

- قم بتثبيت حل العميل المتوقع إلى النقدية في مثيل Sales.

    - حدد نوع نشر **Office 365**.
    - حدد **إظهار الخيارات المتقدمة**.
    - لإجراء تثبيت سريع، حدد **المنطقة**. إذا حددت **لا أعرف**، فسيبحث النظام بالبحث عن كافة المناطق وبالتالي تستغرق عملية التثبيت وقتًا أطول.
    - أدخل **اسم المستخدم** و**كلمة المرور** لمستخدم مسؤول لديه حقوق المستخدم لإجراء عملية تثبيت.

