---
title: "مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>القالب والمهمة

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) إلى Microsoft Dynamics 365 for Sales (Sales).

-   اسم القالب: المنتجات (Fin and Ops إلى Sales)

-   اسم المهمة في المشروع: المنتجات

مهام المزامنة المطلوبة قبل مزامنة المنتج: بلا

## <a name="entity-set"></a>مجموعة الكيانات

| **Finance and Operations** | **CDS** | **المبيعات**  |
|----------------------------|---------|------------|
| منتجات قابلة للبيع تم إصدارها | منتج | المنتجات   |

## <a name="entity-flow"></a>تدفق الكيان

تُدار المنتجات في Finance and Operations وتتم مزامنتها إلى Sales. يقوم كيان البيانات **منتجات قابلة للبيع تم إصدارها‬** في Finance and Operations بتصدير المنتجات القابلة للبيع فقط، مما يعني أن المنتجات تتضمن المعلومات المطلوبة لاستخدامها في أمر المبيعات. تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.

يُستخدم **رقم المنتج** كمفتاح، مما يعني مزامنة متغيرات المنتج إلى CDS وSales مع **معرفات منتجات** فردية لكل **متغير منتج**.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

في Sales، يُضاف حقل جديد على المنتجات **تتم المحافظة عليها خارجيًا‬‏‫** للإشارة إلى المحافظة على منتج محدد خارجيًا‬‏‫‏‎. يتم تعيين القيمة إلى **نعم** بشكل افتراضي أثناء عملية الاستيراد إلى Sales.

-   **تتم المحافظة عليها خارجيًا‬‏‫ = نعم**: ينشأ المنتج من Finance and Operations ولن يكون قابلاً للتحرير في Sales.

-   **تتم المحافظة عليها خارجيًا‬‏‫ = لا**: يتم إدخال المنتج مباشرةً في Sales.

-   **تتم المحافظة عليها خارجيًا = فارغ**: المنتج موجود في Sales قبل تمكين حل العميل المتوقع إلى النقدية.

تُستخدم معلومات **تتم المحافظة عليها خارجيًا** لضمان إمكانية مزامنة فقط **عروض الأسعار** و**أوامر المبيعات** ذات **منتجات تتم المحافظة عليها خارجيًا** إلى Finance and Operations.

تُضاف **المنتجات التي تتم المحافظة عليها خارجيًا** بشكل تلقائي إلى أول **قائمة أسعار** صالحة باستخدام العملة نفسها. لاحظ أن القائمة مرتبة أبجديًا حسب **الاسم**. يتم استخدام سعر مبيعات المنتج من Finance and Operations كسعر على **قائمة الأسعار**. وهذا يعني أنه من الضروري وجود **قائمة أسعار** في Sales لكل **عملة بيع المنتج** في Finance and Operations. يتم تعيين العملة على المنتجات القابلة البيع إلى عمله المحاسبة في الكيان القانوني، الذي تم تصدير المنتج منه.

> [!NOTE]
> لن تنجح عملية مزامنة المنتج من دون **قائمة أسعار** مع العملة المطابقة.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

-   قبل أن تقوم بتشغيل المزامنة الأولى، يتعين عليك ملء **جدول المنتج المميز** للمنتجات الموجودة في Finance and Operations. لن تتم مزامنة المنتجات الموجودة حتى استكمال هذه الوظيفة.

    -   في Finance and Operations، استخدم "البحث" للبحث عن **تعبئة جدول المنتج المميز‬**.

    -   انقر فوق **تعبئة جدول المنتج المميز‬** لتشغيل الوظيفة. يجب تشغيل هذه الوظيفة مرة واحدة فقط.

-   تأكد من أن **ValueMap** المطلوب من أجل **وحدة القياس** (UOM) الخاصة بالبيع في Finance and Operations موحود في تعيين **المصدر -\> CDS SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   قم بتحديث **معرف مؤسسة CDS Organization_OrganizationId** في **المصدر -\> CDS**.

    -   قيمة القالب هي بشكل افتراضي ORG001.

-   قم بتحديث **ValueMap** من أجل **مجموعة الوحدات** (**defaultuomscheduleid.name**) في **CDS -\> الوجهة** لمطابقة **مجموعات الوحدات** في Sales.

    -   قيمة القالب هي بشكل افتراضي **الوحدة الافتراضية**.

-   تأكد من وجود كافة وحدات القياس الخاصة ببيع المنتجات من Finance and Operations في Sales مع قيمة **قوائم انتقاء CDS**.

-   تأكد من أن **قوائم الأسعار** الموجودة في Sales لكل عملة مبيعات المنتج في Finance and Operations.

-   يمكن إنشاء المنتجات في Sales بالحالة **مسودة** أو **نشطة**. ويتم التحكم في ذلك بواسطة **إعدادات النظام** ضمن **Sales** في Sales.

    -   يجب تنشيط المنتجات التي تم إنشاؤها بالحالة "مسودة" قبل إضافتها إلى **عرض أسعار** أو **أمر مبيعات**.

## <a name="template-mapping-in-data-integrator"></a>تعيين القالب في موحد البيانات

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.

![تعيين القالب في موحد البيانات](./media/products-template-mapping-data-integrator-1.png)

![تعيين القالب للمنتجات في موحد البيانات](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>مواضيع مرتبطة

[مزامنة الحسابات من Sales إلى العملاء في Finance and Operations](accounts-template-mapping.md)

[مزامنة جهات الاتصال من Sales لجهات الاتصال في Finance and Operations‎](contacts-template-mapping.md)

[مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations](sales-quotation-template-mapping.md)

[مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales](sales-order-template-mapping.md)

[مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales](sales-invoice-template-mapping.md)


