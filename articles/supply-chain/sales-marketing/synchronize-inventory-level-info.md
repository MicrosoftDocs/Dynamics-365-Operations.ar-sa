---
title: مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service
description: يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "356773"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service 

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القالب التالي والمهام الأساسية التالية لمزامنة مستويات المخزون الفعلي من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

**قالب في تكامل البيانات**
- مخزون المنتج (Finance and Operations إلى Field Service)
  
**مهمة في مشروع تكامل البيانات**
- مخزون المنتج

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:
- المستودعات (Finance and Operations إلى Field Service) 
- منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Sales) 

## <a name="entity-set"></a>مجموعة الكيانات

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | مخزون CDS الفعلي حسب المستودع     |

## <a name="entity-flow"></a>تدفق الكيان
يتم إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة. تتضمن المعلومات على مستوى المخزون: 
- الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)
- الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر ، على سبيل المثال، أمر مبيعات)
- الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬، على سبيل المثال، أوامر الشراء)

يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.

في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، بحيث تتطابق المستويات في Field Service مع المستويات في Finance and Operations.

سيعمل Finance and Operations كأساس لمستويات المخزون. وبالتالي، من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Finance and Operations إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Finance and Operations.

يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Finance and Operations بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).

> [!NOTE]
> من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا = لا**) ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف التصفية والاستعلام المتقدمة. يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations. في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Finance and Operations. للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>حل Field Service CRM
يُستخدم كيان **مخزون المنتج الخارجي** فقط لواجهة التكامل الخلفية. ويتلقى هذا الكيان قيم مستوى المخزون من Finance and Operations في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="data-integration-project"></a>مشروع تكامل البيانات
يمكنك تطبيق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام منتجات ومستودعات معينة فقط من إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>مخزون المنتج (Finance and Operations إلى Field Service): مخزون المنتج

[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
