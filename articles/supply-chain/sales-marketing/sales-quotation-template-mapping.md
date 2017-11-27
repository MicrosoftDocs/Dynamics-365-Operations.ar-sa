---
title: "مزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>مزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات من Microsoft Dynamics 365 for Sales (Sales) إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations). 

## <a name="template-and-tasks"></a>القوالب والمهام

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations:

- **اسم القالب:** عروض أسعار المبيعات (Sales إلى Fin and Ops)
- **أسماء المهام في المشروع:**

    - QuoteHeader
    - QuoteLine

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود عروض أسعار المبيعات.

- المنتجات (Fin and Ops إلى Sales)
- الحسابات (Sales إلى Fin and Ops) (في حال استخدامها)
- جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) (في حال استخدامها)

## <a name="entity-set"></a>مجموعة الكيانات

| مبيعات        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| الاقتباسات       | عرض الأسعار     | رؤوس عروض أسعار المبيعات   |
| QuoteDetails | QuotationLine | بنود عروض أسعار مبيعات CDS |

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء عروض أسعار المبيعات في Sales وتتم مزامنتها إلى Finance and Operations.

تتم مزامنة عروض أسعار المبيعات من Sales فقط إذا تحققت الشروط التالية:

- تتم المحافظة على كافة المنتجات الموجودة في بنود عروض أسعار المبيعات خارجيًا.
- عرض أسعار المبيعات نشط أو تم تنشيطه.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

تمت إضافة الحقل **لديه منتجات تتم المحافظة عليها خارجيًا فقط** إلى كيان عروض الأسعار للتحقق بشكل مستمر مما إذا كان عرض أسعار المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا. إذا كان لعرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط، فستتم المحافظة على المنتجات في Finance and Operations. يساعد هذا السلوك على ضمان عدم محاولتك مزامنة بنود عروض أسعار المبيعات مع منتجات غير معروفة بالنسبة إلى Finance and Operations.

يتم تحديث كافة المنتجات والبنود في عرض الأسعار بواسطة معلومات **لديه منتجات تتم المحافظة عليها خارجيًا فقط** من رأس عرض الأسعار. يمكن العثور على هذه المعلومات في حقل **لدى عرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط** في كيان بنود عرض الأسعار.

تخضع حقول **الخصم** و**التكاليف** و**الضريبة** لمراقبة إعداد معقد في Finance and Operations. لا يعتمد هذا الإعداد حاليًا تعيين التكامل. في التصميم الحالي، تخضع حقول **السعر** و**الخصم** و**التكاليف**، و**الضريبة** لتطبيق Finance and Operations الذي يتولى إدارتها.

في Sales، يجعل الحل الحقول التالية للقراءة فقط، نظرًا لعدم مزامنة القيم إلى Finance and Operations:

- **حقول للقراءة فقط في رأس عرض أسعار المبيعات:** ‏‫% الخصم‬، الخصم، مبلغ الشحن
- **حقول للقراءة فقط في بنود عرض أسعار المبيعات:** الضريبة

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الأنظمة بالإعداد التالي:

### <a name="setup-in-sales"></a>الإعداد في Sales

- انتقل إلى **الإعدادات** &gt; **الإدارة** &gt; **إعدادات النظام** &gt; **Sales**، وتأكد من تعيين حقل **أسلوب حساب الخصم** إلى **لكل وحدة**. يساعد هذا الإعداد على ضمان مطابقة خصم البند من Sales مع الإعداد في Finance and Operations. وإلا، فلن يكون الخصم صحيحًا في Finance and Operations، لأن Finance and Operations سيقرأ الخصم على شكل خصم لكل وحدة حتى لو كان عبارة عن خصم لكل بند في Sales.

### <a name="setup-in-finance-and-operations"></a>الإعداد في Finance and Operations

- انتقل إلى **الحسابات المدينة** &gt; **الإعداد** &gt; **محددات الحسابات المدينة**. على علامة التبويب **التسلسل الرقمي**، حدد التسلسل الرقمي لعروض أسعار المبيعات، ثم انقر فوق **عرض التفاصيل**. ثم، ضمن **الإعداد العام‬**، قم بتعيين الحقل **يدوي** إلى **نعم**.
- انتقل إلى **الحسابات المدينة** &gt; **الإعداد** &gt; **محددات الحسابات المدينة**. ثم، على علامة تبويب **الشحنات**، قم بتعيين حقل **التحكم في تاريخ التسليم** إلى **بلا**. يساعد هذا الإعداد على منع المزامنة من الفشل لعروض أسعار المبيعات.

### <a name="setup-in-the-data-integration-project"></a>إعداد مشروع تكامل البيانات

#### <a name="quoteheader"></a>QuoteHeader

- الحقل **تاريخ التسليم المطلوب** غير مطلوب في Finance and Operations، وسيحدث فشل في المزامنة في حالة ترك الحقل فارغًا. لمنع حدوث هذه المشكلة، إذا كان الحقل فارغًا، يتم أخذ تاريخ افتراضي من **المصدر &gt; CDS**. يجب تحديث التاريخ إلى قيمة مفضلة. في الوقت الحالي، لا يمكنك إدخال قيمة مثل **اليوم** لتمثيل تاريخ اليوم. يجب إدخال تاريخ معين. قيمة القالب الافتراضية للخيار **تاريخ التسليم المطلوب** هي **1/1/2020**.
- يجب ملء الحقل **"كود بلد/منطقة العنوان** في Finance and Operations. للمساعدة في منع أخطاء المزامنة، يمكنك تحديد قيمة افتراضية يتم استخدامها في حالة ترك الحقل فارغًا في Sales. هذه القيمة الافتراضية مفيدة هي أيضًا، لأنه لا يترتب عليك إدخال قيمة يدويًا في حقل **منطقة البلد‬** للعناوين المحلية. لا توجد قيمة قالب افتراضي لـ **DeliveryAddressCountryRegionISOCode**.
- قم بتحديث تعيين **معرف مؤسسة CDS** في **المصدر &gt; CDS** بحيث يتطابق مع **مؤسسة CDS** في كيان المؤسسة:

    - قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي **ORG001**.
    - قيمة القالب الافتراضية للخيار **Account_Organization_OrganizationId** هي **ORG001**.
    - قيمة القالب الافتراضية للخيار **InvoiceAccount_OrganizationId** هي **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- قم بتحديث تعيين **معرف مؤسسة CDS** في **المصدر &gt; CDS** بحيث يتطابق مع **مؤسسة CDS** في كيان المؤسسة:

    - قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي **ORG001**.
    - قيمة القالب الافتراضية للخيار **Product_Organization_Organization_OrganizationId** هي **ORG001**.
    - قيمة القالب الافتراضية للخيار **Quotation_Organization_Organization_OrganizationId** هي **ORG001**.

- الحقل **تاريخ التسليم المطلوب** غير مطلوب في Finance and Operations، وسيحدث فشل في المزامنة في حالة ترك الحقل فارغًا. لمنع حدوث هذه المشكلة، إذا كان الحقل فارغًا، يتم أخذ تاريخ افتراضي من **المصدر &gt; CDS**. يجب تحديث التاريخ إلى قيمة مفضلة. في الوقت الحالي، لا يمكنك إدخال قيمة مثل **اليوم** لتمثيل تاريخ اليوم. يجب إدخال تاريخ معين. قيمة القالب الافتراضية للخيار **تاريخ التسليم المطلوب** هي **1/1/2020**.
- يمكنك إضافة التعيينات التالية من **CDS &gt; الوجهة** للمساعدة في ضمان استيراد بنود عروض الأسعار إلى Finance and Operations إذا لم يكن هناك معلومات افتراضية من العميل أو المنتج:

    - **SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations. لا توجد قيمة قالب افتراضي لـ **SiteId**.
    - **WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Finance and Operations. لا توجد قيمة قالب افتراضي لـ **WarehouseId‎**.

- تأكد من أن تعيين القيمة المطلوب لوحدة القياس الخاصة بالبيع (UOM) في Finance and Operations موجود في تعيين **CDS &gt; الوجهة** للخيار **Quantity_UOM** إلى **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>تعيين القالب في موحد البيانات

> [!NOTE]
> - تخضع حقول **الخصم** و**التكاليف** و**الضريبة** لمراقبة إعداد معقد في Finance and Operations. لا يعتمد هذا الإعداد حاليًا تعيين التكامل. في التصميم الحالي، يتولى Finance and Operations إدارة حقول **السعر** و**الخصم** و**التكاليف**، و**الضريبة**.
> - لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.

### <a name="quoteheader"></a>QuoteHeader

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-1.png)

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-3.png)

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>مواضيع مرتبطة

[مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales](products-template-mapping.md)

[مزامنة الحسابات من Sales للعملاء في Finance and Operations‎](accounts-template-mapping.md)

[مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎](contacts-template-mapping.md)



