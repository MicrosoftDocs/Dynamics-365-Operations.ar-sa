---
title: مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
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
ms.openlocfilehash: d7f104b3f2e132b5b517443577a020fda7fa9af3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975000"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>مزامنة رؤوس وبنود فاتورة المبيعات مباشرةً من Finance and Operations إلى Sales

[!include [banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://preview.admin.powerapps.com/dataintegration) . حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود فاتورة المبيعات من Supply Chain Management إلى المبيعات:

- **اسم القالب في تكامل البيانات:** فواتير المبيعات (Fin and Ops إلى Sales)‬ - مباشر
- **أسماء المهام في مشروع تكامل البيانات:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.

- المنتجات (من Supply Chain Management إلى Sales) - مباشر
- الحسابات (من Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)
- جهات الاتصال (Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)
- رؤوس وبنود أوامر المبيعات (من Supply Chain Management إلى Sales) - مباشرةً

## <a name="entity-set"></a>مجموعة الكيانات

| Supply Chain Management                              | ال‏‏مبيعات          |
|------------------------------------------------------|----------------|
| رؤوس فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا | الفواتير       |
| بنود فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا   | InvoiceDetails |

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء فواتير المبيعات في Supply Chain Management وتتم مزامنتها إلى Sales.

> [!NOTE]
> في الوقت الحالي، لا يتم تضمين الضريبة المرتبطة بالتكاليف في رأس فاتورة المبيعات في المزامنة من Supply Chain Management إلى Sales. يعود سبب ذلك إلى عدم دعم Sales لمعلومات الضرائب على مستوى الرأس. ومع ذلك، يتم تضمين الضريبة المرتبطة بالتكاليف على مستوى البند في المزامنة.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

- تمت إضافة حقل **رقم الفاتورة** إلى كيان **الفاتورة** ويتم عرضه على الصفحة.
- يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Supply Chain Management وستتم مزامنتها إلى Sales. لا تكون صفحة **الفاتورة** قابلة للتحرير، لأن مزامنة الفواتير ستتم من Supply Chain Management.
- تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Supply Chain Management إلى Sales. بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة منه كمالك للفاتورة. لذلك، يمكن لمالك أمر المبيعات عرض الفاتورة.

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
- تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Supply Chain Management.

    يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE]
> لا يتم تضمين الحقول **شروط الدفع** و **شروط الشحن** و **شروط التسليم** و **أسلوب الشحن** و **وضع التسليم** في التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎](accounts-template-mapping-direct.md)

[مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎](products-template-mapping-direct.md)

[مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎](contacts-template-mapping-direct.md)

[مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]