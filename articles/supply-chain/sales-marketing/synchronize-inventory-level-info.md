---
title: "مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة معلومات مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service 

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة معلومات مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يُستخدم القالب التالي والمهام الأساسية التالية لتشغيل مزامنة مستويات المخزون المتاح من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.

**اسم القالب في تكامل البيانات:**
- مخزون المنتج (Finance and Operations إلى Field Service)
  
**أسماء المهام في مشروع تكامل البيانات:**
- مخزون المنتج

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:
- المستودعات (Finance and Operations إلى Field Service) 
- منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Sales) 

## <a name="entity-set"></a>مجموعة الكيانات

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | مخزون CDS الفعلي حسب المستودع     |

## <a name="entity-flow"></a>تدفق الكيان
يتم إرسال معلومات مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة. تتضمن معلومات مستوى المخزون: 
- الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)
- الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر - على سبيل المثال، أمر مبيعات)
- الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬ - على سبيل المثال، أوامر الشراء)

يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.

في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، للحصول على المستويات في Field Service لمطابقة المستويات في Finance and Operations.

سيعمل Finance and Operations كأساس لمستويات المخزون. وهكذا من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Finance and Operations إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Finance and Operations.

يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Finance and Operations بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).

ملاحظة: من الممكن إنشاء عدة مستودعات في Field Services (باستخدام "تتم المحافظة عليه خارجيًا‬‏‫ = لا") ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف الاستعلام والتصفية المتقدمة. يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations. في هذه الحالة، لن تحصل Field service على تحديثات مستوى المخزون من Finance and Operations. اطلع على معلومات إضافية في "مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬" و"مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations‬".

## <a name="field-service-crm-solution"></a>حل Field Service CRM
يعتبر كيان "مخزون المنتج الخارجي" كيانًا جديدًا يستخدم فقط لواجهة التكامل الخلفية. إنه يتلقى قيم مستوى المخزون من Finance and Operations في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع. 

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="in-the-data-integration-project"></a>في مشروع تكامل البيانات
طبّق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام المنتجات والمستودعات المطلوبة فقط بإرسال معلومات حول مستوى المخزون من Finance and Operations إلى Field Service.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>مخزون المنتج (Finance and Operations إلى Field Service): مخزون المنتج

[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

