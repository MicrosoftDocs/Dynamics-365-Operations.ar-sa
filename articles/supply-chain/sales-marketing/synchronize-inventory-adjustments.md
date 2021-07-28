---
title: مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 2fd0a9b10f86699739fb529487cee124f99a0175
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356965"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القوالب والمهام الأساسية التالية لمزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management.

**القوالب في تكامل البيانات**
- عمليات تسوية المخزون (Field Service إلى Supply Chain Management)
- عمليات تحويل المخزون (Field Service إلى Supply Chain Management)

**المهام في مشاريع تكامل البيانات**
- عمليات تسوية المخزون
- عمليات تحويل المخزون

## <a name="table-set"></a>مجموعه الجداول
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Dataverse رؤوس دفتر يومية تعديل مخزون CDS وبنوده |
| msdyn_inventoryadjustmentproducts | Dataverse رؤوس دفتر يومية نقل مخزون CDS وبنوده   |

## <a name="table-flow"></a>تدفق الجداول
ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Supply Chain Management، عندما تتغير **حالة الترحيل** من **تم الإنشاء** إلى **مرحّل**. عند حدوث ذلك، سيتم تأمين أمر التحويل أو التسوية ويصبح للقراءة فقط. وهذا يعني أنه يمكن ترحيل عمليات التسوية والتحويل في Supply Chain Management، ولكن لا يمكن تعديلها. في Supply Chain Management، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت أثناء التكامل. راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.

## <a name="field-service-crm-solution"></a>حل Field Service CRM 
تمت إضافة حقل **وحدة المخزون** إلى جدول **المنتج**. ثمة حاجة إلى هذا العمود لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Supply Chain Management، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع في Supply Chain Management.
عندما تقوم بتعيين المنتج على منتج تسوية المخزون لعمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة منتج المخزون. إذا تم العثور على قيمة، فسيتم تأمين عمود **الوحدة** على منتج تسوية المخزون.

تمت إضافة عمود **حالة الترحيل** إلى جدول **تسوية المخزون** وجدول **تحويل المخزون**. يُستخدم هذا العمود كعامل تصفية عند إرسال تسوية أو تحويل إلى Supply Chain Management. الإعداد الافتراضي لهذا العمود هو تم الإنشاء (1)، ومع ذلك لا يتم إرساله إلى Supply Chain Management. عندما تقوم بتحديث القيمة إلى مرحّل (2)، يتم إرساله إلى Supply Chain Management، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة.

تمت إضافة عمود **التسلسل الرقمي** إلى جدول **منتج تسوية المخزون**. يضمن هذا العمود حصول التكامل على رقم فريد، بحيث تتمكن عملية التكامل من إنشاء التسوية وتحديثها؟ عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في جدول **الرقم التلقائي P2C** للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="supply-chain-management"></a>Supply Chain Management
بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية. يتم تمكين ذلك من **إدارة المخزون > المهام الدورية > تكامل Dataverse > ترحيل دفاتر يومية مخزون التكامل**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>تسوية المخزون (Field Service إلى Supply Chain Management): تسوية المخزون

[![تعيين القالب في تكامل البيانات.](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>تحويل المخزون (Field Service إلى Supply Chain Management): تحويل المخزون

[![تعيين القالب في تكامل البيانات.](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]