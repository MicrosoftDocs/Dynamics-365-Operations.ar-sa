---
title: "مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales

[!include[banner](../includes/banner.md)]

يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>القوالب والمهام

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales:

- **اسم القالب في تكامل البيانات** 

     - فواتر المبيعات (Fin and Ops إلى Sales)

- **أسماء المهام في مشروع تكامل البيانات**

    - SalesInvoiceHeader
    - SalesInvoiceLine

مهام المزامنة المطلوبة قبل مزامنة رأس وبنود فواتير المبيعات:
-   المنتجات (Fin and Ops إلى Sales)
-   الحسابات (Sales إلى Fin and Ops) (في حال استخدامها)
-   جهات الاتصال (Sales إلى Fin and Ops) (في حال استخدامها)
-   رأس وبنود أوامر المبيعات (Fin and Ops إلى Sales)

## <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations                               | Common Data Service (CDS)              | مبيعات          |
|------------------------------------------------------|------------------|----------------|
| رؤوس فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا | SalesInvoice     | الفواتير       |
| بنود فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء فواتير المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.

> [!NOTE]
> لا يتم تضمين الضريبة المرتبطة بالتكاليف في **رأس فاتورة المبيعات** في الوقت الحالي من Finance and Operations إلى Sales. يعود سبب ذلك إلى عدم اعتماد Sales معلومات الضرائب على مستوى الرأس. يتم تضمين الضريبة المتعلقة بالمصاريف على مستوى البنود.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

-  يُضاف **حقل رقم الفاتورة** إلى كيان **الفاتورة** ويتم عرضه على الصفحة.
 
-  يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Finance and Operations وستتم مزامنتها إلى Sales. لا تكون صفحة **الفاتورة** قابلة للتحرير لأن مزامنة الفواتير ستتم من Finance and Operations.
 
-  تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Finance and Operations إلى Sales. بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة له كمالك للفاتورة. يؤدي ذلك إلى منح المالك أمر المبيعات القدرة على عرض الفاتورة.
 
## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

قبل إجراء مزامنة لفواتير المبيعات، لا بد من تحديث الأنظمة بالإعداد التالي:

### <a name="setup-in-sales"></a>الإعداد في Sales

- ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **استخدام حساب أسعار النظام** إلى **نعم**. 

- ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **أسلوب حساب الخصم** إلى **نعم**. 

### <a name="setup-in-the-data-integration-project"></a>إعداد مشروع تكامل البيانات

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader task

- حدّث تعيين **معرف مؤسسة CDS** في **المصدر** > **CDS**. 

    -  قيمة القالب الافتراضية للخيار **SalesOrder_Organization_OrganizationId** هي ORG001.
    -  قيمة القالب الافتراضية للخيار **Account_Organization_OrganizationId** هي ORG001.
    -  قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي ORG001.

- تأكد من وجود التعيين المطلوب في **المصدر** > **CDS لـ InvoiceCountryRegionId** إلى **BillingAddress_Country**.

    -  قيمة القالب هي **ValueMap** مع تعيين عدد من الدول.

- **قائمة الأسعار** مطلوبة لإنشاء الفواتير في Sales. حدّث **ValueMap** في **CDS** > **وجهة pricelevelid.name [اسم قائمة الأسعار]** إلى **قائمة الأسعار** المستخدمة في Sales لكل عملة. يمكنك استخدام إعداد **قائمة الأسعار** الافتراضية لعملة واحدة أو استخدام **ValueMap** إذا كان لديك **قوائم أسعار** بعملات متعددة.

    -  قيمة قالب **pricelevelid.name [اسم قائمة الأسعار]** هي **ValueMap** استنادًا إلى **العملة**.
    -  usd: CRM Service USA (نموذج). 

#### <a name="salesinvoiceline-task"></a>مهمة SalesInvoiceLine

- تأكد من وجود التعيين المطلوب في **المصدر** > **CDS لوحدة القياس**.

- تأكد من أن **ValueMap** المطلوبة من أجل **SalesUnitSymbol** في Finance and Operations موجودة في **المصدر** > **تعيين CDS**. 
    
    - تم تعريف قيمة القالب بوسطة **ValueMap** من أجل **SalesUnitSymbol to Quantity_UOM**.
    
-  حدّث تعيين **معرف مؤسسة CDS في المصدر** > **CDS**. 

    -  قيمة القالب الافتراضية للخيار **SalesInvoicer_Organization_OrganizationId** هي ORG001.
    -  قيمة القالب الافتراضية للخيار **Product_Organization_OrganizationId** هي ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>تعيين القالب في موحد البيانات

> [!NOTE]
> لا تشكل خيارات **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية. يتطلب تعيين هذه الحقول إعداد تعيين القيمة، وهي خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-1.png)

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-2.png)

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-3.png)

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>مواضيع مرتبطة

[مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales](products-template-mapping.md)

[مزامنة الحسابات من Sales للعملاء في Finance and Operations‎](accounts-template-mapping.md)

[مزامنة جهات الاتصال من Sales لجهات الاتصال في Finance and Operations‎](contacts-template-mapping.md)

[مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations](sales-quotation-template-mapping.md)

[مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales](sales-order-template-mapping.md)


