---
title: "العميل المتوقع إلى النقدية"
description: "يوفر هذاالموضوع نظرة عامة حول العميل المتوقع إلى النقدية بين Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition وMicrosoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: ar-sa
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a>العميل المتوقع إلى النقدية

[!include[banner](../includes/banner.md)]

يوفر العميل المتوقع إلى النقدية مزامنة مباشرة بين Dynamics 365 for Finance and Operations, Enterprise Edition و Dynamics 365 for Sales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales. بينما تتدفق البيانات بين Finance and Operations وSales، يمكنك تنفيذ أنشطة المبيعات والتسويق في Sales والتعامل مع تنفيذ الأوامر باستخدام إدارة المخزون في Finance and Operations.

في الإصدار الحالي، يوفر العميل المتوقع للنقدية الأنواع التالية من المزامنة المباشرة:

- [المحافظة على الحسابات في Sales ومزامنتها مباشرة من Sales إلى Finance and Operations.](accounts-template-mapping-direct.md)
- [المحافظة على المنتجات في Finance and Operations ومزامنتها مباشرةً إلى Sales](products-template-mapping-direct.md)
- [‬‏‫المحافظة على جهات الاتصال في Sales ومزامنتها مباشرةً إلى جهات الاتصال أو العملاء في Finance and Operations‎](contacts-template-mapping-direct.md)
- [مزامنة عرض أسعار المبيعات‬ مباشرةً من Sales إلى Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [مزامنة عروض أسعار المبيعات‬ مباشرةً من Finance and Operations إلى Sales‎](sales-order-template-mapping-direct.md)
- [مزامنة عروض أسعار المبيعات‬ بين Sales وFinance and Operations‎](sales-order-template-mapping-direct-two-ways.md)
- [مزامنة فاتورة المبيعات‬ مباشرةً من Finance and Operations إلى Sales‎](sales-invoice-template-mapping-direct.md)

في الإصدارات السابقة، يوفر العميل المتوقع للنقدية الأنواع التالية من المزامنة غير المباشرة:

- [المحافظة على الحسابات في Sales ومزامنتها إلى Finance and Operations.](accounts-template-mapping.md)
- [المحافظة على جهات الاتصال في Sales ومزامنتها إلى Finance and Operations](contacts-template-mapping.md)
- [المحافظة على المنتجات في Finance and Operations ومزامنتها إلى Sales](products-template-mapping.md)
- [إنشاء عروض أسعار المبيعات في Sales ومزامنتها إلى Finance and Operations](sales-quotation-template-mapping.md)
- [إنشاء أومر المبيعات في Finance and Operations ومزامنتها إلى Sales‎](sales-order-template-mapping.md)
- [إنشاء فواتير المبيعات في Finance and Operations ومزامنتها إلى Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations

لاستخدام حل العميل المتوقع للنقدية، يجب تثبيت المكونات التالية:

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (يوليو 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (يوليو 2017) مع تحديث النظام الأساسي 8 (إصدار التطبيق 7.2.11792.56024 مع إصدار النظام الأساسي 7.0.4565.16212)
- الإصلاحات التالية مطلوبة:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – يُمكّن هذا الإصلاح العاجل مزامنة أوامر المبيعات من Sales إلى Finance and Operations من خلال ميزة تكامل البيانات. كما يوفر العديد من التحسينات الأخرى.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – يُمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات من Finance and Operations إلى Sales من خلال ميزة تكامل البيانات.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – يُمكّن هذا الإصلاح العاجل مزامنة أوامر المبيعات من Finance and Operations إلى Sales من خلال ميزة تكامل البيانات.

    > [!NOTE]
    > تحتاج فقط إلى تثبيت KB4045570 لأن التثبيت يتضمن التغييرات من الإصلاحات الأخرى. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations إصدار 1611 (نوفمبر 2016) 

- Dynamics 365 for Finance and Operations، إصدار 1611 (نوفمبر 2016) مع تحديث النظام الأساسي 8 أو إصدار أحدث

- الإصلاحات التالية مطلوبة:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - تمكين مزامنة أوامر المبيعات باستخدام موحد البيانات من Finance and Operations لـ Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - تمكين مزامنة عنوان أوامر التوريد باستخدام موحد البيانات من Finance and Operations لـ Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - مطلوب دعم تكامل العميل المتوقع للنقدية من خلال كيانات بيانات.
    
    > [!NOTE]
    > بعد تثبيت الإصلاحات العاجلة، يجب عليك بدء تشغيل وظيفة الدُفعة التالية من نموذج **SalesPopulateProspectToCash**. يتم إخفاء هذا النموذج لأنك لا تحتاج إليه إلا مرة واحدة. للوصول إلى النموذج، قم بتسجيل الدخول إلى البيئة وقم بإضافة التالي إلى عنوان URL التالي في عنوان المستعرض الخاص بك: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash. عند فتح النموذج، انقر فوق موافق. سوف يقوم هذا بتعبئة حقل **LineCreationSequnceNumber** في **SalesLine**، و **SalesQuotationLine**، وجداول **CustInvoiceTrans** بالقيم الفريدة، وسوف يتم تحديث قائمة المنتجات. ويُعد هذا مطلوبًا للعميل المتوقع لتكامل النقدية للعمل.


## <a name="system-requirements-for-sales"></a>متطلبات النظام لـ Sales

لاستخدام حل العميل المتوقع للنقدية، يجب تثبيت المكونات التالية:

- Dynamics 365 for Sales الإصدار 1612 (8.2.1.207) (DB 8.2.1.207) عبر الإنترنت
- حل العميل المتوقع للنقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.15.0.0 (إصدار 15) 

   > [!NOTE]
   >
   > القوالب في الإصدار 1.0.0.0 و1.0.0.1 مدعومة في حل العميل المتوقع للنقدية لتطبيق Dynamics 365 for Sales، إصدار 1.14.1.0
   >
   > القوالب في الإصدار 2.0.0.0 و1.0.0.1 مدعومة في حل العميل المتوقع للنقدية لتطبيق Dynamics 365 for Sales، إصدار 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>تثبيت حل العميل المتوقع إلى النقدية في Sales

1. قم بتنزيل [الملف المضغوط لحزمة حل العميل المتوقع للنقدية لتطبيق Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) من CustomerSource.
2. تأكد من أن الملف المضغوط غير محظور. وبخلاف ذلك، عند محاولة تثبيت حزمة الحلول، قد تظهر لك رسالة الخطأ التالية، "لم يتم العثور على أي حزم استيراد". لإلغاء حظر الملف المضغوط، انقر بزر الماوس فوقه، وحدد **خصائص**. حدد **إلغاء حظر**.
3. قم بفك الضغط وتشغيل **PackageDeployer.exe**.
4. قم بتثبيت حل العميل المتوقع للنقدية في مثيل Sales:

    1. حدد **Office 365** كنوع نشر.
    2. حدد **إظهار الخيارات المتقدمة**.
    3. لإجراء تثبيت سريع، حدد منطقة. إذا حددت **لا أعرف**، فسيبحث النظام عن جميع المناطقن وستستغرق عملية التثبيت وقتًا أطول.
    4. أدخل اسم مستخدم وكلمة مرور مستخدم مسؤول لديه حقوق التثبيت.

