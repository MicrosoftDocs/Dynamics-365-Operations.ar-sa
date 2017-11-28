---
title: "مزامنة جهات الاتصال مباشرةً من Sales لجهات الاتصال في Finance and Operations‎"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهة الاتصال (جهات الاتصال) وجهة الاتصال (العملاء) من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>مزامنة جهات الاتصال مباشرةً من Sales لجهات الاتصال في Finance and Operations‎

[!include[banner](../includes/banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهة الاتصال (جهات الاتصال) وجهة الاتصال (العملاء) مباشرةً من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration). حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة كيانات جهة الاتصال (جهات الاتصال) في Sales إلى كيانات جهة الاتصال (العملاء) في Finance and Operations:

- **أسماء القوالب في تكامل البيانات:**

    - جهات اتصال (Sales إلى Fin and Ops) - مباشر
    - جهات اتصال إلى عميل (Sales إلى Fin and Ops) - مباشر

- **أسماء المهام في مشروع تكامل البيانات:**

    - جهات الاتصال
    - ContactToCustomer

يجب تنفيذ مهمة المزامنة التالية قبل إجراء مزامنة جهة الاتصال: الحسابات (Sales إلى Fin and Ops)

## <a name="entity-sets"></a>مجموعات الكيانات

| مبيعات    | Finance and Operations |
|----------|------------------------|
| جهات الاتصال | جهات اتصال CDS           |
| جهات الاتصال | العملاء V2           |

## <a name="entity-flow"></a>تدفق الكيان

تُدار جهات الاتصال في Sales وتتم مزامنتها إلى Finance and Operations.

يمكن أن تصبح جهة اتصال في Sales إما جهة اتصال أو عميل في Finance and Operations. لتحديد ما إذا كانت جهة اتصال في Sales يفترض أن تتم مزامنتها إلى Finance and Operations كجهة اتصال أو كعميل، يبحث النظام في الخصائص التالية في جهة الاتصال في Sales:

- **المزامنة إلى عميل في Finance and Operations:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **نعم**
- **المزامنة إلى جهة اتصال في Finance and Operations:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **لا** وحيث تشير **الشركة** (الحساب الأصل‬/جهة الاتصال الأصل) إلى حساب (وليس إلى جهة اتصال)

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

تمت إضافة حقل **هو عميل نشط** جديد إلى جهة الاتصال. يستخدم هذا الحقل للتمييز بين جهات الاتصال التي لها نشاط في مجال المبيعات وجهات الاتصال التي ليس لديها نشاط في مجال المبيعات. تم تعيين **هو عميل نشط** إلى **نعم** فقط لجهات الاتصال التي لديها عروض أسعار أو أوامر أو فواتير ذات صلة. تتم مزامنة جهات الاتصال هذه فقط إلى Finance and Operations كعملاء.

تمت إضافة حقل **IsCompanyAnAccount‎** جديد إلى جهة الاتصال. يشير هذا الحقل إلى ما إذا كانت جهة الاتصال مرتبطة بشركة (الحساب الأصل‬/جهة الاتصال الأصل) من النوع **حساب**. يتم استخدام هذه المعلومات لتحديد جهات الاتصال التي يجب أن تتم مزامنتها إلى Finance and Operations كجهات اتصال.

تمت إضافة حقل **رقم جهة الاتصال** جديد إلى جهة الاتصال للمساعدة في ضمان مفتاح طبيعي وفريد للتكامل. عند إنشاء جهة اتصال جديدة، يتم إنشاء قيمة **رقم جهة الاتصال** بشكل تلقائي باستخدام تسلسل رقمي. تتكون القيمة من **CON**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. فيما يلي مثال على ذلك: **CON-01000-BVRCPS**

عند تطبيق حل التكامل لـ Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم جهة الاتصال** لجهات الاتصال الموجودة باستخدام التسلسل الرقمي الذي تم ذكره سابقًا. يقوم أيضًا البرنامج النصي للترقية بتعيين الحقل **هو عميل نشط** إلى **نعم** لأي من جهات الاتصال التي لديها نشاط في مجال المبيعات.

## <a name="in-finance-and-operations"></a>في Finance and Operations

توضع علامة على جهات الاتصال باستخدام الخاصية **IsContactPersonExternallyMaintained**. تشير هذه الخاصية إلى الاحتفاظ بجهة اتصال معينة خارجيًا. في هذه الحالة، يتم الاحتفاظ بجهات الاتصال التي تم الاحتفاظ بها خارجيًا في Sales.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

### <a name="contact-to-customer"></a>جهة اتصال إلى عميل

- يجب ملء **CustomerGroup** في Finance and Operations. للمساعدة على منع أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في التعيين. يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.

    قيمة القالب الافتراضية هي **10**.

- عن طريق إضافة التعيينات التالية، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Finance and Operations. يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.

    - **SiteId** - يمكن أيضًا تعريف موقع افتراضي على المنتجات في Finance and Operations. يكون الموقع مطلوبًا لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.

        قيمة قالب **SiteId** غير محددة.

    - **WarehouseId** - يمكن أيضًا تعريف مستودع افتراضي على المنتجات في Finance and Operations. يكون المستودع مطلوبًا لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.

        قيمة قالب **WarehouseId** غير محددة.

    - **LanguageId** – اللغة مطلوبة لإنشاء أوامر المبيعات وعروض الأسعار في Finance and Operations.
    
        قيمة القالب الافتراضية هي **ar-sa**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.

### <a name="contact-to-contact"></a>جهة اتصال إلى جهة اتصال

![تعيين القالب في موحد البيانات](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>جهة اتصال إلى عميل

![تعيين القالب في موحد البيانات](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎](accounts-template-mapping-direct.md)

[مزامنة المنتجات مباشرةً من Finance and Operations للمنتجات في Sales‎](products-template-mapping-direct.md)

[مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales](sales-order-template-mapping-direct.md)

[مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales](sales-invoice-template-mapping-direct.md)



