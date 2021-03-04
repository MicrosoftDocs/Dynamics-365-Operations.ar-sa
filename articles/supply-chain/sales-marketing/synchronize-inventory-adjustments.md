---
title: مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421253"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القوالب والمهام الأساسية التالية لمزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management.

**القوالب في تكامل البيانات**
- عمليات تسوية المخزون (Field Service إلى Supply Chain Management)
- عمليات تحويل المخزون (Field Service إلى Supply Chain Management)

**المهام في مشاريع تكامل البيانات**
- عمليات تسوية المخزون
- عمليات تحويل المخزون

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   رؤوس دفتر يومية تعديل مخزون CDS وبنوده |
| msdyn_inventoryadjustmentproducts | رؤوس دفتر يومية نقل مخزون CDS وبنوده   |

## <a name="entity-flow"></a>تدفق الكيان
ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Supply Chain Management، عندما تتغير **حالة الترحيل** من **تم الإنشاء** إلى **مرحّل**. عند حدوث ذلك، سيتم تأمين أمر التحويل أو التسوية ويصبح للقراءة فقط. وهذا يعني أنه يمكن ترحيل عمليات التسوية والتحويل في Supply Chain Management، ولكن لا يمكن تعديلها. في Supply Chain Management، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت أثناء التكامل. راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.

## <a name="field-service-crm-solution"></a>حل Field Service CRM 
تمت إضافة حقل **وحدة المخزون** إلى "كيان **المنتج**. ثمة حاجة إلى هذا الحقل لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Supply Chain Management، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع في Supply Chain Management.
عندما تقوم بتعيين المنتج على منتج تسوية المخزون لعمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة منتج المخزون. إذا تم العثور على قيمة، فسيتم تأمين حقل **الوحدة** على منتج تسوية المخزون.

تمت إضافة حقل **حالة الترحيل** إلى كيان **تسوية المخزون** وكيان **تحويل المخزون**. يُستخدم هذا الحقل كعامل تصفية عند إرسال تسوية أو تحويل إلى Supply Chain Management. الإعداد الافتراضي لهذا الحقل هو تم الإنشاء (1)، ومع ذلك لا يتم إرساله إلى Supply Chain Management. عندما تقوم بتحديث القيمة إلى مرحّل (2)، يتم إرساله إلى Supply Chain Management، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة.

تمت إضافة حقل **التسلسل الرقمي** إلى كيان **منتج تسوية المخزون**. يضمن هذا الحقل حصول التكامل على رقم فريد، بحيث تتمكن عملية التكامل من إنشاء التسوية وتحديثها؟ عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في كيان **الرقم التلقائي P2C** للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="supply-chain-management"></a>Supply Chain Management
بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية. يتم تمكين ذلك من **إدارة المخزون > المهام الدورية > تكامل CDS > ترحيل دفاتر يومية مخزون التكامل**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>تسوية المخزون (Field Service إلى Supply Chain Management): تسوية المخزون

[![تعيين القالب في تكامل البيانات](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>تحويل المخزون (Field Service إلى Supply Chain Management): تحويل المخزون

[![تعيين القالب في تكامل البيانات](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]