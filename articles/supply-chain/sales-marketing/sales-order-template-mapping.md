---
title: "مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales

[!include[banner](../includes/banner.md)]

يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>القوالب والمهام

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales:

- **اسم القالب في تكامل البيانات** 

    - أوامر المبيعات (Fin and Ops إلى Sales)
    
- **أسماء المهام في مشروع تكامل البيانات**

    - OrderHeader
    - OrderLine

مهام المزامنة المطلوبة قبل مزامنة رأس وبنود فواتير المبيعات:

- المنتجات (Fin and Ops إلى Sales)
- الحسابات (Sales إلى Fin and Ops) (في حال استخدامها)
- جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) (في حال استخدامها)

## <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations |    Common Data Service (CDS)         |     مبيعات      |
|------------------------|----------------|----------------|
| رؤوس أوامر المبيعات CDS| SalesOrder     | SalesOrders |
| بنود أمر مبيعات CDS  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء أوامر المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.

تضمن عوامل التصفية الموجودة في القالب من تضمين فقط أوامر المبيعات ذات الصلة فقط في المزامنة:

- ستتضمن عملية المزامنة عملاء الطلب والفوترة في أمر المبيعات الذي ينشأ من Sales. في Finance and Operations، يتم استخدام الحقلين **OrderingCustomerIsExternallyMaintained** و**InvoiceCustomerIsExternallyMaintained** لتعقب المزامنة في كيانات البيانات.

- يجب تأكيد **أمر المبيعات** في Finance and Operations. وحدها أوامر المبيعات المؤكدة أو أوامر المبيعات ذات حالة معالجة أعلى، مثل الحالة "مشحون" أو "مفوتر"، تتم مزامنتها إلى Sales.

- بعد إنشاء أمر مبيعات أو تعديله، يجب تنفيذ الوظيفة الدفعية **حساب إجماليات المبيعات‬** في Finance and Operations. وحدها أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها ستتم مزامنتها إلى CDS وSales.

> [!NOTE]
> لا يتم تضمين الضريبة المرتبطة بالتكاليف في **رأس أمر المبيعات‬** في الوقت الحالي من Finance and Operations إلى Sales. يعود سبب ذلك إلى عدم اعتماد Sales معلومات الضرائب على مستوى الرأس. يتم تضمين الضريبة المتعلقة بالمصاريف على مستوى البنود.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

تظهر على الصفحة الحقول الجديدة المضافة إلى كيان **الأمر**:

- **تتم المحافظة عليها خارجيًا‬‏‫‬‏‫** - عيّن هذا الخيار إلى **نعم** عندما يأتي الأمر من Finance and Operations.

- **حالة المعالجة** - يستخدم لعرض حالة معالجة الأمر في Finance and Operations. القيم هي:

    - نشط
    - أوامر المبيعات المؤكدة
    - كشف التعبئة
    - مفوتر
    - منتقي
    - منتقى جزئيًا
    - معبأ جزئيًا
    - مشحون
    - مشحون جزئيًا
    - مفوتر جزئيًا
    - تم الإلغاء

يُستخدم الإعداد **لديه منتجات تتم المحافظة عليها خارجيًا فقط** في سيناريوهات أخرى لأوامر المبيعات (مزامنة من Sales إلى Finance and Operations) لتعقب ما إذا كان أمر المبيعات عبارة عن **منتجات تتم المحافظة عليها خارجيًا** بشكل كامل، وفي هذه الحالة تتم المحافظة على المنتجات في Finance and Operations. يضمن هذا السلوك عدم محاولتك مزامنة بنود أمر المبيعات مع منتجات غير معروفة بالنسبة إلى Finance and Operations.
 
تكون الأزرار **"إنشاء فاتورة"** و**إلغاء الأمر** و**إعادة حساب** و**الحصول على منتجات"** و**البحث عن عنوان** على **أمر المبيعات** مخفية للأوامر التي تتم المحافظة عليها خارجيًا إذ سيتم إنشاء الفواتير في Finance and Operations وستتم مزامنتها إلى Sales. لا تكون صفحة الأمر قابلة للتحرير لأن مزامنة معلومات أمر المبيعات ستتم من Finance and Operations.
 
سوف تبقى **حالة أمر المبيعات** نشطة للتأكد من إمكانية انسياب التغييرات من Finance and Operations إلى **أمر المبيعات‏‎** في Sales. يتم التحكم في ذلك من خلال تعيين الإعداد الافتراضي **Statecode [الحالة]** إلى **نشط** في مشروع تكامل البيانات.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين 

قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الأنظمة بالإعداد التالي:

### <a name="setup-in-sales"></a>الإعداد في Sales

- تحقق من أذونات الفريق الذي تم تعيين المستخدم (من **إعداد الاتصال** في Sales) إليه. إذا كنت تستخدم بيانات العرض التوضيحي، فعادةً ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق. من دون ذلك سوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود عند تشغيل المشروع من موحد البيانات. 

    - ضمن **الإعدادات** > **الأمان** > **الفرق**، حدد الفريق المناسب، وانقر فوق **إدارة الأدوار** وحدد دورًا باستخدام الأذونات المطلوبة على سبيل المثال، مسؤول النظام.

- ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **استخدام حساب أسعار النظام** إلى **نعم**. 

- ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **أسلوب حساب الخصم** إلى **نعم**. 

### <a name="setup-in-finance-and-operations"></a>الإعداد في Finance and Operations

عيّن **المبيعات والتسويق** > **المهام الدورية** > **حساب إجماليات المبيعات‬** لتشغيلها كوظيفة دفعية، مع تعيين **حساب إجماليات أوامر المبيعات‬** إلى **نعم**. يُعد هذا الأمر ضروريًا لأن أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها هي فقط أوامر المبيعات التي ستتم مزامنتها إلى CDS وSales. يجب أن يكون مدى تكرار الوظيفة الدفعية متوافقًا مع مدى تكرار مزامنة أوامر المبيعات.

### <a name="setup-in-the-data-integration-project"></a>إعداد مشروع تكامل البيانات

#### <a name="salesheader-task"></a>مهمة SalesHeader

- حدّث تعيين **معرف مؤسسة CDS في المصدر** > **CDS**.

    - قيمة القالب الافتراضية للخيار **Account_Organization_OrganizationId** هي ORG001.
    - قيمة القالب الافتراضية للخيار **InvoiceAccount_Organization_OrganizationId** هي ORG001.
    - قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي ORG001.

- تأكد من وجود التعيين المطلوب في **المصدر** > **CDS لـ InvoiceCountryRegionId إلى BillingAddress_Country** ولـ **DeliveryCountryRegionId إلى DeliveryAddress_Country**.

    - قيمة القالب هي **ValueMap** مع تعيين عدد من الدول.

- **قائمة الأسعار** مطلوبة لإنشاء الأوامر في Sales. حدّث **ValueMap** في **CDS** > **وجهة** لـ **pricelevelid.name [اسم قائمة الأسعار]** إلى **قائمة الأسعار** المستخدمة في Sales لكل عملة. يمكنك استخدام إعداد **قائمة الأسعار** الافتراضية لعملة واحدة أو استخدام **ValueMap** إذا كان لديك **قوائم أسعار** بعملات متعددة.
    
    - قيمة القالب الافتراضية للخيار **pricelevelid.name [اسم قائمة الأسعار]** هو CRM Service USA (نموذج). 

#### <a name="salesline-task"></a>مهمة SalesLine

- حدّث تعيين **معرف مؤسسة CDS في المصدر** > **CDS**. 
    
    - قيمة القالب الافتراضية للخيار **SalesOrder_Organization_OrganizationId** هي ORG001.
    - قيمة القالب الافتراضية للخيار **Product_Organization_OrganizationId** هي ORG001.

- تأكد من وجود التعيين المطلوب في **المصدر** > **CDS** لـ **DeliveryCountryRegionId** إلى **DeliveryAddress_Country**.

    - قيمة القالب هي **ValueMap** مع تعيين عدد من الدول.
    
- تأكد من أن **ValueMap** المطلوبة من أجل **SalesUnitSymbol** في Finance and Operations موجودة في **المصدر** > **تعيين CDS**.

    - تم تعريف قيمة القالب بوسطة **ValueMap** من أجل **SalesUnitSymbol to Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>تعيين القالب في موحد البيانات

> [!NOTE]
> لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.

### <a name="orderheader"></a>OrderHeader

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-1.png)

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-3.png)

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>مواضيع مرتبطة

[مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales](products-template-mapping.md)

[مزامنة الحسابات من Sales للعملاء في Finance and Operations‎](accounts-template-mapping.md)

[مزامنة جهات الاتصال من Sales لجهات الاتصال في Finance and Operations‎](contacts-template-mapping.md)

[مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations](sales-quotation-template-mapping.md)

[مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales](sales-invoice-template-mapping.md)


