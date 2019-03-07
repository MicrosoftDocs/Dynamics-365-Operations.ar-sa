---
title: مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "359234"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

يستند قالب **منتجات Field Service ‏(Finance and Operations إلى Field Service)** إلى قالب **المنتجات (Finance and Operations إلى Sales) - مباشر** من العميل المتوقع إلى النقدية. للحصول على مزيد من المعلومات، راجع [المنتجات (Finance and Operations إلى Sales) - مباشر](products-template-mapping-direct.md).

يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Finance and Operations إلى Field Service)** و**منتجات Field Service (Finance and Operations إلى Field Service) – مباشر**.

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات:**

- منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Sales)

**اسم المهمة في مشروع تكامل البيانات:**

- المنتجات

يتضمن قالب **منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Field Service)** تعيينًا واحدًا غير مضمن في قالب **منتجات Field Service (Finance and Operations إلى Field Service)**. يضمن هذا التعيين تضمين وحدة المخزون المطلوبة للمزامنة على مستوى المخزون.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>منتجات Field Service مع وحدة المخزون (Finance and Operations to Field Service): المنتجات

[![تعيين القالب في تكامل البيانات](./media/FSProduct1.png)](./media/FSProduct1.png)
