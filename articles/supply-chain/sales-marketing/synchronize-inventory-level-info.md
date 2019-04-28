---
title: مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service
description: يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 6b2bdf1ca6f6ae43cd85c8a1353ee8305052761d
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/14/2019
ms.locfileid: "842546"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="d0418-103">مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="d0418-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d0418-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="d0418-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d0418-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="d0418-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d0418-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="d0418-106">Templates and tasks</span></span>
<span data-ttu-id="d0418-107">يتم استخدام القالب التالي والمهام الأساسية التالية لمزامنة مستويات المخزون الفعلي من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="d0418-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d0418-108">**قالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="d0418-108">**Template in Data integration**</span></span>
- <span data-ttu-id="d0418-109">مخزون المنتج (Fin and Ops إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="d0418-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="d0418-110">**مهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="d0418-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="d0418-111">مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="d0418-111">Product inventory</span></span>

<span data-ttu-id="d0418-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:</span><span class="sxs-lookup"><span data-stu-id="d0418-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="d0418-113">المستودعات (Fin and Ops إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="d0418-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="d0418-114">منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="d0418-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="d0418-115">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="d0418-115">Entity set</span></span>

| <span data-ttu-id="d0418-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="d0418-116">Field Service</span></span>                      | <span data-ttu-id="d0418-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d0418-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="d0418-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="d0418-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="d0418-119">مخزون CDS الفعلي حسب المستودع</span><span class="sxs-lookup"><span data-stu-id="d0418-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="d0418-120">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="d0418-120">Entity flow</span></span>
<span data-ttu-id="d0418-121">يتم إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="d0418-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="d0418-122">تتضمن المعلومات على مستوى المخزون:</span><span class="sxs-lookup"><span data-stu-id="d0418-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="d0418-123">الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)</span><span class="sxs-lookup"><span data-stu-id="d0418-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="d0418-124">الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر ، على سبيل المثال، أمر مبيعات)</span><span class="sxs-lookup"><span data-stu-id="d0418-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="d0418-125">الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬، على سبيل المثال، أوامر الشراء)</span><span class="sxs-lookup"><span data-stu-id="d0418-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="d0418-126">يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="d0418-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="d0418-127">في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، بحيث تتطابق المستويات في Field Service مع المستويات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d0418-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="d0418-128">سيعمل Finance and Operations كأساس لمستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="d0418-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="d0418-129">وبالتالي، من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Finance and Operations إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d0418-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="d0418-130">يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Finance and Operations بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).</span><span class="sxs-lookup"><span data-stu-id="d0418-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="d0418-131">من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا = لا**) ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف التصفية والاستعلام المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="d0418-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="d0418-132">يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d0418-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="d0418-133">في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d0418-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="d0418-134">للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="d0418-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d0418-135">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="d0418-135">Field Service CRM solution</span></span>
<span data-ttu-id="d0418-136">يُستخدم كيان **مخزون المنتج الخارجي** فقط لواجهة التكامل الخلفية.</span><span class="sxs-lookup"><span data-stu-id="d0418-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="d0418-137">ويتلقى هذا الكيان قيم مستوى المخزون من Finance and Operations في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="d0418-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d0418-138">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="d0418-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="d0418-139">مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="d0418-139">Data integration project</span></span>
<span data-ttu-id="d0418-140">يمكنك تطبيق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام منتجات ومستودعات معينة فقط من إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="d0418-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d0418-141">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="d0418-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="d0418-142">مخزون المنتج (Fin and Ops إلى Field Service): مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="d0418-142">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="d0418-143">[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="d0418-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
