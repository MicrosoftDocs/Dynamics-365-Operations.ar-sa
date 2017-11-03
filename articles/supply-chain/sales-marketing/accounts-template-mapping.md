---
title: "مزامنة الحسابات من Sales إلى العملاء في Finance and Operations"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة حسابات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>مزامنة الحسابات من Sales إلى العملاء في Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة الحسابات من Microsoft Dynamics 365 for Sales (Sales) إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="template-and-task"></a>القالب والمهمة

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة الحسابات من Sales إلى Finance and Operations:

- **اسم القالب:** الحسابات (Sales إلى Fin and Ops)
- **اسم المهمة في المشروع:** الحسابات - الحساب - العملاء

مهام المزامنة المطلوبة قبل مزامنة الحساب/العميل: بلا

## <a name="entity-set"></a>مجموعة الكيانات

| ال‏‏مبيعات    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| الحسابات | الحساب | العملاء              |

## <a name="entity-flow"></a>تدفق الكيان

تُدار الحسابات في Sales وتتم مزامنتها إلى Finance and Operations كعملاء. يتم تعيين الخاصية **تتم المحافظة عليها خارجيًا** على هؤلاء العملاء إلى **نعم** لتعقب العملاء الناشئين من Sales. أثناء الفوترة، يتم استخدام هذه المعلومات لتصفية الفواتير التي سيتم مزامنتها إلى Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

يتوفر حقل **رقم الحساب** في صفحة **الحساب**. تم إنشاء مفتاح طبيعي وفريد له لدعم التكامل. قد تؤثر ميزة المفتاح الطبيعي في حل إدارة علاقات العملاء (CRM)‬ على العملاء الذين يستخدمون حقل **رقم الحساب**، ولكنهم لا يستخدمون قيم **رقم الحساب** لكل حساب. في الوقت الحالي، لا يدعم حل التكامل هذه الحالة.

عند إنشاء حساب جديد، إذا لم تكن قيمة **رقم الحساب** موجودة، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **ACC**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. فيما يلي مثال على ذلك: **ACC-01000-BVRCPS**

عند تطبيق حل التكامل على Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم الحساب** للحسابات الموجودة في Sales. في حال عدم وجود قيم في **رقم الحساب**، سيتم استخدام التسلسل الرقمي الذي تم وصفه في وقت سابق.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

- يجب تحديث تعيين **CustomerGroupId** من **CDS &gt; الوجهة** إلى قيمة صالحة في Finance and Operations. يمكنك تحديد قيمة افتراضية، أو يمكنك تعيين القيمة باستخدام تعيين القيمة. قيمة القالب الافتراضية هي **10**.
- يجب ملء **"كود بلد/منطقة العنوان** في Finance and Operations. لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في التعيين من **CDS &gt; الوجهة**. يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.

    - قيمة القالب الافتراضية للخيار **AddressCountryRegionISOCode** هي **USA**.
    - قيمة القالب الافتراضية للخيار **DeliveryAddressCountryRegionISOCode** هي **USA**.

- عن طريق إضافة التعيينات التالية من **‎CDS &gt;الوجهة**، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Finance and Operations. يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.

    - **SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations. يمكن أخذ موقع افتراضي إما من المنتج، أو من العميل من رأس الأمر. قيمة القالب الافتراضية للخيار **SiteId‎** هي **1**.
    - **WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Finance and Operations. يمكن أخذ مستودع افتراضي إما من المنتج، أو من العميل من رأس الأمر في Finance and Operations. قيمة القالب الافتراضية للخيار **WarehouseId** هي **13**.
    - **LanguageId** – اللغة مطلوبة لإنشاء أوامر المبيعات وعروض الأسعار في Finance and Operations. بشكل افتراضي، يتم استخدام اللغة من رأس الأمر من العميل. قيمة القالب الافتراضية للخيار **LanguageId** هي **en-us**.

- تحديث معرف مؤسسة CDS (**Organization_OrganizationId**) في تعيين**المصدر &gt; CDS**. قيمة القالب الافتراضية هي **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>تعيين القالب في موحد البيانات

> [!NOTE]
> لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة. تعتبر تعيينات القيم خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.

![تعيين القالب في موحد البيانات](./media/accounts-template-mapping-data-integrator-1.png)

![تعيين القالب للحسابات في موحد البيانات](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>مواضيع مرتبطة

[مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales](products-template-mapping.md)

[مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎](contacts-template-mapping.md)

[مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations](sales-quotation-template-mapping.md)

[مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales](sales-order-template-mapping.md)

[مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales](sales-invoice-template-mapping.md)




