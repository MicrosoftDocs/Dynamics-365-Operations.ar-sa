---
title: مزامنة المنتجات مع وحدة المخزون من Supply Chain Management إلى Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
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
ms.openlocfilehash: 741b823d6cc5dbd23cda4f07e463f28d6bbe77d6
ms.sourcegitcommit: a2f9dce06322dada6b5f1c82051ef2359f8c0f12
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/24/2020
ms.locfileid: "3081854"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="ab912-103">مزامنة المنتجات مع وحدة المخزون من Supply Chain Management إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="ab912-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab912-104">يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات مع وحدة المخزون المشروع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ab912-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="ab912-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="ab912-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="ab912-106">يستند القالب المستخدم **منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Field Service)** إلى القالب **منتجات Field Service (Supply Chain Management إلى Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="ab912-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="ab912-107">لمزيد من المعلومات، راجع [مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="ab912-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="ab912-108">يصف هذا الموضوع الاختلافات بين القالبين فقط:</span><span class="sxs-lookup"><span data-stu-id="ab912-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="ab912-109">**منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)**</span><span class="sxs-lookup"><span data-stu-id="ab912-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="ab912-110">**منتجات Field Service ‏(Supply Chain Management إلى Field Service)**</span><span class="sxs-lookup"><span data-stu-id="ab912-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="ab912-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="ab912-111">Templates and tasks</span></span>

<span data-ttu-id="ab912-112">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="ab912-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ab912-113">منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="ab912-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="ab912-114">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="ab912-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="ab912-115">المنتجات</span><span class="sxs-lookup"><span data-stu-id="ab912-115">Products</span></span>

<span data-ttu-id="ab912-116">يحتوي القالب **منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Field Service)** على تعيين مضمّن في **منتجات Field Service (Supply Chain Management إلى Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="ab912-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="ab912-117">يضمن هذا التعيين تضمين وحدة المخزون المطلوبة للمزامنة على مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="ab912-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ab912-118">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="ab912-118">Template mapping in Data integration</span></span>

<span data-ttu-id="ab912-119">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ab912-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="ab912-120">منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Field Service): المنتجات</span><span class="sxs-lookup"><span data-stu-id="ab912-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="ab912-121">[![تعيين القالب في تكامل البيانات](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="ab912-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
