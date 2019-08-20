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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835684"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="23ae7-103">مزامنة المنتجات مع وحدة المخزون من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="23ae7-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="23ae7-104">يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="23ae7-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="23ae7-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="23ae7-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="23ae7-106">يستند القالب المستخدم **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service)** إلى القالب **منتجات Field Service (Fin and Ops إلى Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="23ae7-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="23ae7-107">للحصول على مزيد من المعلومات، راجع [منتجات Field Service (Finance and Operations إلى Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="23ae7-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="23ae7-108">يصف هذا الموضوع الاختلافات بين القالبين فقط:</span><span class="sxs-lookup"><span data-stu-id="23ae7-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="23ae7-109">**منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)**</span><span class="sxs-lookup"><span data-stu-id="23ae7-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="23ae7-110">**منتجات Field Service ‏(Fin and Ops إلى Field Service)**</span><span class="sxs-lookup"><span data-stu-id="23ae7-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="23ae7-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="23ae7-111">Templates and tasks</span></span>

<span data-ttu-id="23ae7-112">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="23ae7-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="23ae7-113">منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="23ae7-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="23ae7-114">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="23ae7-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="23ae7-115">المنتجات</span><span class="sxs-lookup"><span data-stu-id="23ae7-115">Products</span></span>

<span data-ttu-id="23ae7-116">يتضمن قالب **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service)** تعيينًا واحدًا غير مضمن في قالب **منتجات Field Service (Fin and Ops إلى Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="23ae7-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="23ae7-117">يضمن هذا التعيين تضمين وحدة المخزون المطلوبة للمزامنة على مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="23ae7-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="23ae7-118">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="23ae7-118">Template mapping in Data integration</span></span>

<span data-ttu-id="23ae7-119">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="23ae7-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="23ae7-120">منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service): المنتجات</span><span class="sxs-lookup"><span data-stu-id="23ae7-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="23ae7-121">[![تعيين القالب في تكامل البيانات](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="23ae7-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
