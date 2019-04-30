---
title: مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/14/2019
ms.locfileid: "842452"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

يستند القالب المستخدم **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service)** إلى القالب **منتجات Field Service (Fin and Ops إلى Field Service)**. للحصول على مزيد من المعلومات، راجع [منتجات Field Service (Finance and Operations إلى Field Service)](field-service-product.md).

يصف هذا الموضوع الاختلافات بين القالبين فقط: 
- **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)**
- **منتجات Field Service ‏(Fin and Ops إلى Field Service)** 

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات:**

- منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)

**اسم المهمة في مشروع تكامل البيانات:**

- المنتجات

يتضمن قالب **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service)** تعيينًا واحدًا غير مضمن في قالب **منتجات Field Service (Fin and Ops إلى Field Service)**. يضمن هذا التعيين تضمين وحدة المخزون المطلوبة للمزامنة على مستوى المخزون.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service): المنتجات

[![تعيين القالب في تكامل البيانات](./media/FSProduct1.png)](./media/FSProduct1.png)
