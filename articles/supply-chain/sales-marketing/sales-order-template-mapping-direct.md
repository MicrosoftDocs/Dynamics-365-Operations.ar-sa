---
title: "مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration). حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales:

- **اسم القالب في تكامل البيانات:** أوامر المبيعات (Fin and Ops إلى Sales)‬ - مباشر
- **أسماء المهام في مشروع تكامل البيانات:**

    - OrderHeader
    - OrderLine

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.

- ‏‫المنتجات (Fin and Ops إلى Sales)‬ - مباشر
- الحسابات (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)
- جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)

## <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations  | مبيعات             |
|-------------------------|-------------------|
| رؤوس أوامر المبيعات CDS | SalesOrders       |
| بنود أمر مبيعات CDS   | SalesOrderDetails |

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء أوامر المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.

تساعد عوامل التصفية الموجودة في القالب على ضمان عدم تضمين غير أوامر المبيعات ذات الصلة في المزامنة:

- في أمر المبيعات، سيتم تضمين كل من عميل الأمر وعميل الفوترة اللذين يتم إنشاؤهما من Sales في المزامنة. في Finance and Operations، يتم استخدام الحقلين **OrderingCustomerIsExternallyMaintained** و**InvoiceCustomerIsExternallyMaintained** لتعقب المزامنة في كيانات البيانات.
- يجب تأكيد أمر المبيعات في Finance and Operations. لا تتم مزامنة غير أوامر المبيعات المؤكدة أو أوامر المبيعات التي لها حالة معالجة أعلى، مثل الحالة **مشحون** أو **مفوتر** إلى Sales.
- بعد إنشاء أمر مبيعات أو تعديله، يجب تنفيذ وظيفة الدُفعة **حساب إجماليات المبيعات‬** في Finance and Operations. لن تتم مزامنة غير أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها إلى Sales.

> [!NOTE]
> في الوقت الحالي، لا يتم تضمين الضريبة المرتبطة بالتكاليف في رأس أمر المبيعات في المزامنة من Finance and Operations إلى Sales. يعود سبب ذلك إلى عدم دعم Sales لمعلومات الضرائب على مستوى الرأس. ومع ذلك، يتم تضمين الضريبة المرتبطة بالتكاليف على مستوى البند في المزامنة.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

تمت إضافة حقول جديدة إلى كيان **الأمر** وهي تظهر على الصفحة:

- **تتم المحافظة عليها خارجيًا‬‏‫‬‏‫** - عيّن هذا الخيار إلى **نعم** عندما يأتي الأمر من Finance and Operations.
- **حالة المعالجة** - يستخدم هذا الحقل لعرض حالة معالجة الأمر في Finance and Operations. تتوفر القيم التالية:

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

يُستخدم الإعداد **لديه منتجات تتم المحافظة عليها خارجيًا فقط** في سيناريوهات أخرى لأوامر المبيعات (على سبيل المثال، مزامنة من Sales إلى Finance and Operations) للتحقق بشكل مستمر مما إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا.‬ إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا، فستتم المحافظة على المنتجات في Finance and Operations. يساعد هذا الإعداد على ضمان عدم محاولة مزامنة بنود أوامر المبيعات التي تشتمل على منتجات غير معروفة إلى Finance and Operations.

تكون الأزرار **إنشاء فاتورة** و**إلغاء الأمر** و**إعادة الحساب** و**الحصول على منتجات** و**البحث عن عنوان** في صفحة **أمر المبيعات** مخفية للأوامر التي تتم المحافظة عليها خارجيًا إذ سيتم إنشاء الفواتير في Finance and Operations وستتم مزامنتها إلى Sales. لا يمكن تحرير صفحة الأمر، لأنه ستتم مزامنة معلومات أمر المبيعات من Finance and Operations.

ستبقى حالة أمر المبيعات **نشط** للمساعدة في ضمان إمكانية انسياب التغييرات من Finance and Operations إلى أمر المبيعات في Sales. للتحكم في هذا السلوك، قم بتعيين الإعداد الافتراضي **Statecode \[الحالة\]** إلى **نشط** في مشروع تكامل البيانات.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الإعدادات التالية في النظام.

### <a name="setup-in-sales"></a>الإعداد في Sales

- تأكد من إعداد الأذونات للفريق الذي تم تعيين المستخدم من إعداد الاتصال في Sales إليه. إذا كنت تستخدم بيانات العرض التوضيحي، فعادة ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق. إذا لم يكن لدى الفريق حق وصول المسؤول أيضًا، عند تشغيل المشروع من تكامل البيانات، فسوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود.

    انتقل إلى **‎الإعدادات** > **الأمان** > **الفرق**، حدد الفريق المناسب، وحدد **إدارة الأدوار**‎، ثم حدد دورًا يملك الأذونات المطلوبة على سبيل المثال، **مسؤول النظام**.

- انتقل إلى **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، وتأكد من أنه يتم استخدام الإعدادات التالية:

    - يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.
    - يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.

### <a name="setup-in-finance-and-operations"></a>الإعداد في Finance and Operations

انتقل إلى **المبيعات والتسويق** > **المهام الدورية** > **حساب إجماليات المبيعات**‎، وعيِّن الوظيفة لتشغيلها كوظيفة دُفعة. عيّن الخيار **‏‫حساب إجماليات أوامر المبيعات‬** إلى **نعم**. ‏‫تعد هذه الخطوة هامة لأن أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها هي فقط أوامر المبيعات التي ستتم مزامنتها إلى Sales. يجب أن يكون مدى تكرار وظيفة الدُفعة متوافقًا مع مدى تكرار مزامنة أوامر المبيعات.

### <a name="setup-in-the-data-integration-project"></a>إعداد مشروع تكامل البيانات

#### <a name="salesheader-task"></a>مهمة SalesHeader

- تأكد من وجود التعيين المطلوب لـ **InvoiceCountryRegionId** إلى **BillingAddress\_Country** ولـ **DeliveryCountryRegionId** إلى **DeliveryAddress\_Country**.

    قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.

- تكون قائمة الأسعار مطلوبة لإنشاء الأوامر في Sales. حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة. يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة. بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.

    قيمة القالب الافتراضية لـ **pricelevelid.name \[اسم قائمة الأسعار\]** تكون **CRM Service USA (نموذج)**.

#### <a name="salesline-task"></a>مهمة SalesLine

- تأكد من وجود التعيين المطلوب لـ **DeliveryCountryRegionId** إلى **DeliveryAddress\_Country**.

    قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.

- تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Finance and Operations.

    يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE]
> لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![تعيين القالب في موحد البيانات](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![تعيين القالب في موحد البيانات](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎](accounts-template-mapping-direct.md)

[مزامنة المنتجات مباشرةً من Finance and Operations للمنتجات في Sales‎](products-template-mapping-direct.md)

[مزامنة جهات الاتصال مباشرةً من Sales لجهات الاتصال في Finance and Operations‎](contacts-template-mapping-direct.md)

[مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales](sales-invoice-template-mapping-direct.md)




