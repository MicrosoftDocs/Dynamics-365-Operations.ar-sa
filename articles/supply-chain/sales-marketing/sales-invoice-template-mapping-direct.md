---
title: "مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales

[!include [banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration). حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales:

- **اسم القالب في تكامل البيانات:** فواتير المبيعات (Fin and Ops إلى Sales)‬ - مباشر
- **أسماء المهام في مشروع تكامل البيانات:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.

- ‏‫المنتجات (Fin and Ops إلى Sales)‬ - مباشر
- الحسابات (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)
- جهات الاتصال (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)
- رأس وبنود أوامر المبيعات (Fin and Ops إلى Sales) - مباشر

## <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations                               | مبيعات          |
|------------------------------------------------------|----------------|
| رؤوس فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا | الفواتير       |
| بنود فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا   | InvoiceDetails |

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء فواتير المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.

> [!NOTE]
> في الوقت الحالي، لا يتم تضمين الضريبة المرتبطة بالتكاليف في رأس فاتورة المبيعات في المزامنة من Finance and Operations إلى Sales. يعود سبب ذلك إلى عدم دعم Sales لمعلومات الضرائب على مستوى الرأس. ومع ذلك، يتم تضمين الضريبة المرتبطة بالتكاليف على مستوى البند في المزامنة.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

- تمت إضافة حقل **رقم الفاتورة** إلى كيان **الفاتورة** ويتم عرضه على الصفحة.
- يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Finance and Operations وستتم مزامنتها إلى Sales. لا تكون صفحة **الفاتورة** قابلة للتحرير لأن مزامنة الفواتير ستتم من Finance and Operations.
- تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Finance and Operations إلى Sales. بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة منه كمالك للفاتورة. لذلك، يمكن لمالك أمر المبيعات عرض الفاتورة.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

قبل إجراء مزامنة لفواتير المبيعات، لا بد من تحديث الإعدادات التالية في النظام.

### <a name="setup-in-sales"></a>الإعداد في Sales

انتقل إلى **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، وتأكد من أنه يتم استخدام الإعدادات التالية:

- يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.
- يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.

### <a name="setup-in-the-data-integration-project"></a>إعداد مشروع تكامل البيانات

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader task

- تأكد من وجود التعيين المطلوب لـ **InvoiceCountryRegionId** إلى **BillingAddress\_Country**.

    قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.

- تكون قائمة الأسعار مطلوبة لإنشاء الفواتير في Sales. حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة. يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة. بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.

    قيمة القالب لـ **pricelevelid.name \[اسم قائمة الأسعار\]** هي تعيين قيمة يستند إلى العملة بالدولار الأمريكي = CRM Service USA (نموذج).  
    
#### <a name="salesinvoiceline-task"></a>مهمة SalesInvoiceLine

- تأكد من وجود التعيين المطلوب لـ **وحدة القياس**.
- تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Finance and Operations.

    يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE]
> لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎](accounts-template-mapping-direct.md)

[مزامنة المنتجات مباشرةً من Finance and Operations إلى المنتجات في Sales‎](products-template-mapping-direct.md)

[مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال في Finance and Operations‎](contacts-template-mapping-direct.md)

[مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales](sales-order-template-mapping-direct-two-ways.md)







