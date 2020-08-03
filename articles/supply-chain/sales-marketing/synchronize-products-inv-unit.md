---
title: مزامنة المنتجات مع وحدة المخزون من Supply Chain Management إلى Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
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
ms.openlocfilehash: 62ed33d101f7d7e47b560c417dc05e5aecc83478
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546328"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>مزامنة المنتجات مع وحدة المخزون من Supply Chain Management إلى Field Service

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

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

[![تعيين القالب في تكامل البيانات](./media/FSProduct1.png)](./media/FSProduct1.png)
