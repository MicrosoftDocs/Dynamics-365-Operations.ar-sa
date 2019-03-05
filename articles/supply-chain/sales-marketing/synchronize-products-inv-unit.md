---
title: "مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c4ecb-103">مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="c4ecb-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c4ecb-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c4ecb-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c4ecb-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="c4ecb-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="c4ecb-106">يستند قالب **منتجات Field Service ‏(Finance and Operations إلى Field Service)** إلى قالب **المنتجات (Finance and Operations إلى Sales) - مباشر** من العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="c4ecb-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="c4ecb-107">للحصول على مزيد من المعلومات، راجع [المنتجات (Finance and Operations إلى Sales) - مباشر](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="c4ecb-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="c4ecb-108">يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Finance and Operations إلى Field Service)** و**منتجات Field Service (Finance and Operations إلى Field Service) – مباشر**.</span><span class="sxs-lookup"><span data-stu-id="c4ecb-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c4ecb-109">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="c4ecb-109">Templates and tasks</span></span>

<span data-ttu-id="c4ecb-110">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="c4ecb-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c4ecb-111">منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="c4ecb-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="c4ecb-112">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="c4ecb-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c4ecb-113">المنتجات</span><span class="sxs-lookup"><span data-stu-id="c4ecb-113">Products</span></span>

<span data-ttu-id="c4ecb-114">يتضمن قالب **منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Field Service)** تعيينًا واحدًا غير مضمن في قالب **منتجات Field Service (Finance and Operations إلى Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="c4ecb-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c4ecb-115">يضمن هذا التعيين تضمين وحدة المخزون المطلوبة للمزامنة على مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="c4ecb-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c4ecb-116">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="c4ecb-116">Template mapping in Data integration</span></span>

<span data-ttu-id="c4ecb-117">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="c4ecb-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="c4ecb-118">منتجات Field Service مع وحدة المخزون (Finance and Operations to Field Service): المنتجات</span><span class="sxs-lookup"><span data-stu-id="c4ecb-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="c4ecb-119">[![تعيين القالب في تكامل البيانات](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="c4ecb-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
