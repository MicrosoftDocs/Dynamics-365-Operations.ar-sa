---
title: العميل المتوقع إلى النقدية
description: يوفر هذا الموضوع نظرة عامة حول حل العميل المتوقع إلى النقدية بين Microsoft Dynamics 365 for Finance and Operations وMicrosoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
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
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554611"
---
# <a name="prospect-to-cash"></a>العميل المتوقع إلى النقدية

[!include [banner](../includes/banner.md)]

يوفر حل العميل المتوقع إلى النقدية التزامن المباشر عبر Dynamics 365 for Finance and Operations وDynamics 365 for Sales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales. بينما تتدفق البيانات بين Finance and Operations وSales، يمكنك تنفيذ أنشطة المبيعات والتسويق في Sales والتعامل مع تنفيذ الأوامر باستخدام إدارة المخزون في Finance and Operations. 

لمزيد من المعلومات حول تكامل العميل المتوقع إلى النقدية‬، شاهد الفيديو القصير على YouTube [تكامل العميل المتوقع إلى النقدية](https://www.youtube.com/watch?v=AVV9x5x-XCg).

في الإصدار الحالي، يوفر العميل المتوقع للنقدية الأنواع التالية من المزامنة المباشرة:

- [المحافظة على الحسابات في Sales ومزامنتها مباشرة من Sales إلى Finance and Operations.](accounts-template-mapping-direct.md)
- [المحافظة على المنتجات في Finance and Operations ومزامنتها مباشرةً إلى Sales](products-template-mapping-direct.md)
- [‬‏‫المحافظة على جهات الاتصال في Sales ومزامنتها مباشرةً إلى جهات الاتصال أو العملاء في Finance and Operations‎](contacts-template-mapping-direct.md)
- [مزامنة عرض أسعار المبيعات‬ مباشرةً من Sales إلى Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [مزامنة عروض أسعار المبيعات‬ بين Sales وFinance and Operations‎](sales-order-template-mapping-direct-two-ways.md)
- [مزامنة فاتورة المبيعات‬ مباشرةً من Finance and Operations إلى Sales‎](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>متطلبات النظام لـ Finance and Operations
يتم دعم العميل المتوقع لتكامل النقدية في الإصدارات التالية:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (ديسمبر 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (ديسمبر 2017) - إصدار التطبيق 7.3.11971.56116 مع Platform Update 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (يوليو 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (يوليو 2017) - مع platform update 8 (إصدار التطبيق 7.2.11792.56024 مع إصدار النظام الأساسي 7.0.4565.16212).
- الإصلاحات التالية مطلوبة:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – يُمكّن هذا الإصلاح العاجل مزامنة أوامر المبيعات من Sales إلى Finance and Operations من خلال ميزة تكامل البيانات. كما يوفر العديد من التحسينات الأخرى.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – يُمكّن هذا الإصلاح العاجل مزامنة بنود أوامر المبيعات من Finance and Operations إلى Sales من خلال ميزة تكامل البيانات.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – يُمكّن هذا الإصلاح العاجل مزامنة أوامر المبيعات من Finance and Operations إلى Sales من خلال ميزة تكامل البيانات.

    > [!NOTE]
    > تحتاج فقط إلى تثبيت KB4045570 لأن التثبيت يتضمن التغييرات من الإصلاحات الأخرى. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations الإصدار 1611 (نوفمبر 2016)

- Dynamics 365 for Finance and Operations الإصدار 1611 (نوفمبر 2016) مع platform update 8 أو أعلى

- الإصلاحات التالية مطلوبة:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - تمكين مزامنة أوامر المبيعات باستخدام موحد البيانات من Finance and Operations لـ Sales 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - تمكين مزامنة عنوان أوامر التوريد باستخدام موحد البيانات من Finance and Operations لـ Sales
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - مطلوب دعم تكامل العميل المتوقع للنقدية من خلال كيانات بيانات.
    
    > [!NOTE]
    > بعد تثبيت الإصلاحات العاجلة، يجب عليك بدء تشغيل وظيفة الدُفعة التالية من نموذج **SalesPopulateProspectToCash**. يتم إخفاء هذا النموذج لأنك لا تحتاج إليه إلا مرة واحدة. للوصول إلى النموذج، سجّل دخولك إلى البيئة وأضف عنوان URL التاليفي عنوان المستعرض: *&mi=action:SalesPopulateProspectToCash*، على سبيل المثال، `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. عند فتح النموذج، انقر فوق موافق. سوف يقوم هذا بتعبئة حقل **LineCreationSequnceNumber** في **SalesLine**، و **SalesQuotationLine**، وجداول **CustInvoiceTrans** بالقيم الفريدة، وسوف يتم تحديث قائمة المنتجات. ويُعد هذا مطلوبًا للعميل المتوقع لتكامل النقدية للعمل.


## <a name="system-requirements-for-sales"></a>متطلبات النظام لـ Sales

لاستخدام حل العميل المتوقع للنقدية، يجب تثبيت المكونات التالية:

- Dynamics 365 for Sales الإصدار 1612 (8.2.1.207) (DB 8.2.1.207) عبر الإنترنت أو إصدار لاحق
- حل العميل المتوقع إلى النقدية لتطبيق Dynamics 365 for Sales، الإصدار 1.15.0.0 أو إصدار لاحق. الحل متوفر للتنزيل من AppSource. [تنزيل Dynamics 365، عميل متوقع إلى النقد](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
