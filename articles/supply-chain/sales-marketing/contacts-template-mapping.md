---
title: "مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة جهة الاتصال (جهات الاتصال) وجهة الاتصال (العملاء) من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎

[!include[banner](../includes/banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهة الاتصال (جهات الاتصال) وجهة الاتصال (العملاء) من Microsoft Dynamics 365 for Sales (Sales) إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="templates-and-tasks"></a>القوالب والمهام

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة جهة الاتصال (جهات الاتصال) في Sales إلى جهة الاتصال (العملاء) في Finance and Operations:

- **أسماء القوالب:**

    - جهات اتصال (Sales إلى Fin and Ops)
    - جهات اتصال إلى عميل (Sales إلى Fin and Ops)

- **أسماء المهام في المشروع:**

    - جهات الاتصال
    - ContactToCustomer

يجب تنفيذ مهمة مزامنة التالية قبل مزامنة جهات الاتصال: الحسابات (Sales إلى Fin and Ops)

## <a name="entity-sets"></a>مجموعات الكيانات

| ال‏‏مبيعات    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| جهات الاتصال | جهة الاتصال | جهات اتصال CDS           |
| جهات الاتصال | الحساب | العملاء V2           |

## <a name="entity-flow"></a>تدفق الكيان

تُدار جهات الاتصال في Sales، وتتم مزامنتها إلى Common Data Service (CDS) وFinance and Operations.

يمكن أن تصبح جهة اتصال في Sales جهة اتصال في CDS وFinance and Operations. أو، يمكنها أن تصبح حسابًا في CDS وعميلاً في Finance and Operations. لتحديد ما إذا كان يجب انتقاء جهة اتصال في Sales لمزامنتها إلى CDS وFinance and Operations (على سبيل المثال، جهات اتصال في Sales &gt; جهة اتصال في CDS &gt; جهات اتصال في Finance and Operations)، يبحث النظام عن الخصائص التالية على جهة الاتصال في Sales.

- **مزامنة إلى الحساب في CDS وFinance and Operations:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **نعم**
- **مزامنة إلى جهة الاتصال في CDS وFinance and Operations:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **لا** وحيث تشير **الشركة** (الحساب الأصل‬/جهة الاتصال الأصل) إلى حساب (وليس إلى جهة اتصال)

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales 

تمت إضافة حقل **هو عميل نشط** جديد إلى جهة الاتصال. يستخدم هذا الحقل للتمييز بين جهات الاتصال التي لها نشاط في مجال المبيعات وجهات الاتصال التي ليس لديها نشاط في مجال المبيعات. تم تعيين **هو عميل نشط** إلى **نعم** فقط لجهات الاتصال التي لديها عروض أسعار أو أوامر أو فواتير ذات صلة. تتم مزامنة جهات الاتصال هذه فقط إلى Finance and Operations كعملاء.

تمت إضافة حقل **IsCompanyAnAccount‎** جديد إلى جهة الاتصال. يستخدم هذا الحقل للإشارة إلى ما إذا كانت جهة الاتصال مرتبطة بشركة (الحساب الأصل‬/جهة الاتصال الأصل) من النوع **حساب**. يتم استخدام هذه المعلومات لتحديد جهات الاتصال التي يجب أن تتم مزامنتها إلى Finance and Operations كجهات اتصال.

تمت إضافة حقل **رقم جهة الاتصال** جديد إلى جهة الاتصال للمساعدة في ضمان مفتاح طبيعي وفريد للتكامل. عند إنشاء جهة اتصال جديدة، يتم إنشاء **رقم جهة الاتصال** بشكل تلقائي باستخدام تسلسل رقمي. تتكون القيمة من **CON**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. فيما يلي مثال على ذلك: **CON-01000-BVRCPS**

عند إضافة حل تكامل Sales إلى Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم جهة الاتصال** لجهات الاتصال الموجودة باستخدام التسلسل الرقمي الذي تمت مناقشته سابقًا. يقوم أيضًا البرنامج النصي للترقية بتعيين الحقل **هو عميل نشط** إلى **نعم** لأي من جهات الاتصال التي لديها نشاط في مجال المبيعات.

## <a name="in-finance-and-operations"></a>في Finance and Operations 

توضع علامة على جهات الاتصال باستخدام الخاصية **IsContactPersonExternallyMaintained**. تشير هذه الخاصية إلى المحافظة على جهة اتصال معينة خارجيًا. في هذه الحالة، تتم المحافظة على جهات الاتصال التي تتم المحافظة عليها خارجيًا في Sales.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

### <a name="contact-to-contact"></a>جهة اتصال إلى جهة اتصال

- قم بتحديث **معرف مؤسسة** في تعيين **المصدر &gt; CDS**.

    - قيمة القالب الافتراضية للخيار **Organization_OrganizationId [معرف المؤسسة]** هي **ORG001**.
    - قيمة القالب الافتراضية للخيار **PrimaryAccount_Organization_OrganizationId [معرف المؤسسة]** هي **ORG001**.

- يجب ملء **"كود بلد/منطقة العنوان** في Finance and Operations. لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في تعيين **CDS &gt; Operations**. يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales. قيمة القالب الافتراضية للخيار **PrimaryAddressCountryRegionISOCode** هي **USA**.
- تأكد من وجود قيمة للحقل التالي في Finance and Operations. إذا لم تكن المعلومات مطلوبة في Finance and Operations، يمكنك إزالة التعيين من تعيين **CDS &gt; الوجهة**.

    - **اسم الحقل في Finance and Operations:** القرار
    - **التعيين:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>جهة اتصال إلى عميل

- قم بتحديث **معرف مؤسسة** في تعيين **المصدر &gt; CDS**. قيمة القالب الافتراضية للخيار **Organization_OrganizationId [معرف المؤسسة]** هي **ORG001**.
- يجب ملء **"كود بلد/منطقة العنوان** في Finance and Operations. لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في تعيين **CDS &gt; الوجهة**. يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales. قيمة القالب الافتراضية للخيار **PrimaryAddressCountryRegionISOCode** هي **USA**.
- يجب ملء **CustomerGroup** في Finance and Operations. لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في تعيين **CDS &gt; الوجهة**. يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales. قيمة القالب الافتراضية للخيار **CustomerGroupId** هي **10**.
- عن طريق إضافة التعيينات التالية من **‎CDS &gt;الوجهة**، يمكنك المساعدة على تقليل عدد التحديثات اليدوية في Finance and Operations. يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.

    - **SiteId** - يمكن أيضًا تعريف موقع افتراضي على المنتجات في Finance and Operations. يكون الموقع مطلوبًا لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations. قيمة قالب **SiteId** غير محددة.
    - **WarehouseId** - يمكن أيضًا تعريف مستودع افتراضي على المنتجات في Finance and Operations. يكون المستودع مطلوبًا لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations. قيمة قالب **WarehouseId** غير محددة.
    - **LanguageId** – اللغة مطلوبة لإنشاء أوامر المبيعات وعروض الأسعار في Finance and Operations. قيمة القالب الافتراضية للخيار **LanguageId** هي **en-us**.

## <a name="template-mapping-in-data-integrator"></a>تعيين القالب في موحد البيانات

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.

### <a name="contact-to-contact"></a>جهة اتصال إلى جهة اتصال

![تعيين القالب في موحد البيانات](./media/contacts-template-mapping-data-integrator-1.png)

![تعيين القالب لجهات الاتصال في موحد البيانات](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>جهة اتصال إلى عميل

![تعيين القالب في موحد البيانات](./media/contacts-template-mapping-data-integrator-3.png)

![تعيين القالب لجهات الاتصال في موحد البيانات](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>مواضيع مرتبطة

[مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales](products-template-mapping.md)

[مزامنة الحسابات من Sales إلى العملاء في Finance and Operations](accounts-template-mapping.md)

[مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations](sales-quotation-template-mapping.md)

[مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales](sales-order-template-mapping.md)

[مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales](sales-invoice-template-mapping.md)

