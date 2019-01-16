---
title: "مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Finance and Operations"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يُستخدم القالب التالي والمهام الأساسية لتشغيل مزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.

**اسم القوالب في تكامل البيانات:**
- تسوية المخزون (Field Service إلى Finance and Operations)
- تحويل المخزون (Field Service إلى Finance and Operations)

**أسماء المهام في مشاريع تكامل البيانات:**
- عمليات تسوية المخزون
- عمليات تحويل المخزون

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   رؤوس دفتر يومية تعديل مخزون CDS وبنوده |
| msdyn_inventoryadjustmentproducts | رؤوس دفتر يومية نقل مخزون CDS وبنوده   |

## <a name="entity-flow"></a>تدفق الكيان
ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Finance and Operations، عندما تتغير  **حالة الترحيل** من "تم الإنشاء" إلى "مرحّل". عندما يحدث هذا الأمر، سيتم تأمين أمر التسوية أو التحويل وسيصبح للقراءة فقط، إذ يتم ترحيل عمليات التسوية أو التحويل في Finance and Operations وبالتالي يتعذر تعديلها.
في Finance and Operations، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت مع التكامل. راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.

## <a name="field-service-crm-solution"></a>حل Field Service CRM 
تمت إضافة حقل "وحدة المخزون" إلى "كيان المنتج". ثمة حاجة إلى هذا الحقل لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Operations، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع.
عندما تقوم بتعيين المنتج على "منتج تسوية المخزون" لكل من عمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة "منتج مخزون المنتجات". إذا تم العثور على قيمة، فسيتم تأمين حقل الوحدة على منتج تسوية المخزون

تمت إضافة حقل "حالة الترحيل" إلى كيان تسوية المخزون وكيان تحويل المخزون. يُستخدم هذا الحقل كعامل تصفية عند إرسال تسوية أو تحويل إلى Operations. تم تعيين هذا الحقل إلى تم الإنشاء (1) بشكل افتراضي، وبالتالي لن يتم إرساله إلى Operations. عندما تقوم بتغييره إلى مرحّل (2)، يتم إرساله إلى Operations، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة إليه.
تمت إضافة حقل "التسلسل الرقمي" إلى "كيان المنتج". يساعد هذا الحقل في حصول عملية التكامل على رقم فريد، وبالتالي تعلم هذه العملية متى يجب تنفيذ عمليات إنشاء ومتى يجب تنفيذ عمليات تحديث. عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في كيان الرقم التلقائي P2C للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="in-finance-and-operations"></a>في Finance and Operations
بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية. يتم تمكين ذلك من: إدارة المخزون > المهام الدورية > تكامل CDS > ترحيل دفاتر يومية مخزون التكامل‬

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>تسوية المخزون (Field Service إلى Finance and Operations): تسوية المخزون

[![تعيين القالب في تكامل البيانات](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>تحويل المخزون (Field Service إلى Finance and Operations): تحويل المخزون

[![تعيين القالب في تكامل البيانات](./media/FSTrans1.png)](./media/FSTrans1.png)

