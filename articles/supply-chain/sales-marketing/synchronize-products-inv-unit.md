---
title: مزامنة المنتجات مع وحدة المخزون من Supply Chain Management إلى Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
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
ms.openlocfilehash: b65f23516d6be3d5d942d787261f5b8394c9f9c5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356941"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>مزامنة المنتجات مع وحدة المخزون من Supply Chain Management إلى Field Service

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

يستند القالب المستخدم **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service)** إلى القالب **منتجات Field Service (Supply Chain Management إلى Field Service)**. لمزيد من المعلومات، راجع [مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service](field-service-product.md).

يصف هذا الموضوع الاختلافات بين القالبين فقط: 
- **منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)**
- **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** 

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات:**

- منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)

**اسم المهمة في مشروع تكامل البيانات:**

- المنتجات

يحتوي القالب **منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Field Service)** على تعيين مضمّن في **منتجات Field Service (Supply Chain Management إلى Field Service)**. يضمن هذا التعيين تضمين وحدة المخزون المطلوبة للمزامنة على مستوى المخزون.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Field Service): المنتجات

[![تعيين القالب في تكامل البيانات.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]