---
title: مزامنة معلومات مستوى المخزون من Supply Chain Management إلى Field Service
description: يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
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
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421251"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>مزامنة معلومات مستوى المخزون من Supply Chain Management إلى Field Service 

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القوالب والمهام الأساسية التالية لمزامنة مستويات المخزون الفعلي من Supply Chain Management إلى Field Service.

**قالب في تكامل البيانات**
- مخزون المنتج (Supply Chain Management إلى Field Service)
  
**مهمة في مشروع تكامل البيانات**
- مخزون المنتج

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:
- المستودعات (Supply Chain Management إلى Field Service) 
- منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales) 

## <a name="entity-set"></a>مجموعة الكيانات

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | مخزون CDS الفعلي حسب المستودع     |

## <a name="entity-flow"></a>تدفق الكيان
يتم إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة. تتضمن المعلومات على مستوى المخزون: 
- الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)
- الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر، على سبيل المثال، أمر مبيعات)
- الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬، على سبيل المثال، أوامر الشراء)

يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.

في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، بحيث تتطابق المستويات في Field Service مع المستويات في Supply Chain Management.

سيعمل Supply Chain Management كأساس لمستويات المخزون. وبالتالي، من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Supply Chain Management إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Supply Chain Management.

يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Supply Chain Management بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).

> [!NOTE]
> من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا = لا**) ثم تعيينها إلى مستودع واحد في Supply Chain Management، باستخدام وظائف التصفية والاستعلام المتقدمة. يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Supply Chain Management. في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Supply Chain Management. للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>حل Field Service CRM
يُستخدم كيان **مخزون المنتج الخارجي** فقط لواجهة التكامل الخلفية. ويتلقى هذا الكيان قيم مستوى المخزون من Supply Chain Management في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="data-integration"></a>تكامل البيانات
بالنسبة إلى المشروع الذي تعمل علبه، يجب التأكد من تحديث مفتاح التكامل لـ msdynce_externalproductinventories.
1.  انتقل إلى **تكامل البيانات > مجموعات الاتصال**.
2.  حدد مجموعة الاتصال المستخدمة.
3.  على علامة التبويب **مفتاح التكامل‬**، تأكد من إضافة المفاتيح التالية إلى msdynce_externalproductinventories:
      - msdynce_productnumber (رقم المنتج)
      - msdynce_warehouseid (معرف المستودع)
      
### <a name="data-integration-project"></a>مشروع تكامل البيانات
يمكنك تطبيق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام منتجات ومستودعات معينة فقط من إرسال معلومات على مستوى المخزون من Supply Chain Management إلى Field Service.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>مخزون المنتج (Supply Chain Management إلى Field Service): مخزون المنتج

[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]