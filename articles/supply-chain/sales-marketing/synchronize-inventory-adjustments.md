---
title: مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Finance and Operations
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: e94fa87c2f8b66574d6c5b2930cebf2e1b144fea
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536286"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القوالب والمهام الأساسية التالية لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.

**القوالب في تكامل البيانات**
- تسوية المخزون (Field Service إلى Fin and Ops)
- تحويل المخزون‬ (Field Service إلى Fin and Ops)

**المهام في مشاريع تكامل البيانات**
- عمليات تسوية المخزون
- عمليات تحويل المخزون

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   رؤوس دفتر يومية تعديل مخزون CDS وبنوده |
| msdyn_inventoryadjustmentproducts | رؤوس دفتر يومية نقل مخزون CDS وبنوده   |

## <a name="entity-flow"></a>تدفق الكيان
ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Finance and Operations، عندما تتغير **حالة الترحيل** من **تم الإنشاء** إلى **مرحّل**. عند حدوث ذلك، سيتم تأمين أمر التحويل أو التسوية ويصبح للقراءة فقط. وهذا يعني أنه يمكن ترحيل عمليات التسوية والتحويل في Finance and Operations، ولكن لا يمكن تعديلها. في Finance and Operations، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت أثناء التكامل. راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.

## <a name="field-service-crm-solution"></a>حل Field Service CRM 
تمت إضافة حقل **وحدة المخزون** إلى "كيان **المنتج**. ثمة حاجة إلى هذا الحقل لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Finance and Operations، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع في Finance and Operations.
عندما تقوم بتعيين المنتج على منتج تسوية المخزون لعمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة منتج المخزون. إذا تم العثور على قيمة، فسيتم تأمين حقل **الوحدة** على منتج تسوية المخزون.

تمت إضافة حقل **حالة الترحيل** إلى كيان **تسوية المخزون** وكيان **تحويل المخزون**. يُستخدم هذا الحقل كعامل تصفية عند إرسال تسوية أو تحويل إلى Finance and Operations. الإعداد الافتراضي لهذا الحقل هو تم الإنشاء (1)، ومع ذلك لا يتم إرساله إلى Finance and Operations. عندما تقوم بتحديث القيمة إلى مرحّل (2)، يتم إرساله إلى Finance and Operations، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة.

تمت إضافة حقل **التسلسل الرقمي** إلى كيان **منتج تسوية المخزون**. يضمن هذا الحقل حصول التكامل على رقم فريد، بحيث تتمكن عملية التكامل من إنشاء التسوية وتحديثها؟ عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في كيان **الرقم التلقائي P2C** للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="finance-and-operations"></a>Finance and Operations
بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية. يتم تمكين ذلك من **إدارة المخزون > المهام الدورية > تكامل CDS > ترحيل دفاتر يومية مخزون التكامل**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>تسوية المخزون (Field Service إلى Fin and Ops): تسوية المخزون

[![تعيين القالب في تكامل البيانات](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>تحويل المخزون (Field Service إلى Fin and Ops): تحويل المخزون

[![تعيين القالب في تكامل البيانات](./media/FSTrans1.png)](./media/FSTrans1.png)
