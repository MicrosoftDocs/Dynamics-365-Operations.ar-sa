---
title: مزامنة معلومات مستوى المخزون من Supply Chain Management إلى Field Service
description: يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: eefbfd1f8d7aa73cbb3330433b08efd889232818
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251191"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="edb5b-103">مزامنة معلومات مستوى المخزون من Supply Chain Management إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="edb5b-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="edb5b-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="edb5b-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="edb5b-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="edb5b-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="edb5b-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="edb5b-106">Templates and tasks</span></span>
<span data-ttu-id="edb5b-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة مستويات المخزون الفعلي من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="edb5b-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="edb5b-108">**قالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="edb5b-108">**Template in Data integration**</span></span>
- <span data-ttu-id="edb5b-109">مخزون المنتج (Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="edb5b-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="edb5b-110">**مهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="edb5b-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="edb5b-111">مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="edb5b-111">Product inventory</span></span>

<span data-ttu-id="edb5b-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:</span><span class="sxs-lookup"><span data-stu-id="edb5b-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="edb5b-113">المستودعات (Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="edb5b-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="edb5b-114">منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="edb5b-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="edb5b-115">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="edb5b-115">Entity set</span></span>

| <span data-ttu-id="edb5b-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="edb5b-116">Field Service</span></span>                      | <span data-ttu-id="edb5b-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="edb5b-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="edb5b-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="edb5b-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="edb5b-119">مخزون CDS الفعلي حسب المستودع</span><span class="sxs-lookup"><span data-stu-id="edb5b-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="edb5b-120">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="edb5b-120">Entity flow</span></span>
<span data-ttu-id="edb5b-121">يتم إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="edb5b-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="edb5b-122">تتضمن المعلومات على مستوى المخزون:</span><span class="sxs-lookup"><span data-stu-id="edb5b-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="edb5b-123">الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)</span><span class="sxs-lookup"><span data-stu-id="edb5b-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="edb5b-124">الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر، على سبيل المثال، أمر مبيعات)</span><span class="sxs-lookup"><span data-stu-id="edb5b-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="edb5b-125">الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬، على سبيل المثال، أوامر الشراء)</span><span class="sxs-lookup"><span data-stu-id="edb5b-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="edb5b-126">يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="edb5b-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="edb5b-127">في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، بحيث تتطابق المستويات في Field Service مع المستويات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edb5b-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="edb5b-128">سيعمل Supply Chain Management كأساس لمستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="edb5b-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="edb5b-129">وبالتالي، من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Supply Chain Management إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edb5b-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="edb5b-130">يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Supply Chain Management بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).</span><span class="sxs-lookup"><span data-stu-id="edb5b-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="edb5b-131">من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا = لا**) ثم تعيينها إلى مستودع واحد في Supply Chain Management، باستخدام وظائف التصفية والاستعلام المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="edb5b-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="edb5b-132">يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edb5b-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="edb5b-133">في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edb5b-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="edb5b-134">للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="edb5b-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="edb5b-135">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="edb5b-135">Field Service CRM solution</span></span>
<span data-ttu-id="edb5b-136">يُستخدم كيان **مخزون المنتج الخارجي** فقط لواجهة التكامل الخلفية.</span><span class="sxs-lookup"><span data-stu-id="edb5b-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="edb5b-137">ويتلقى هذا الكيان قيم مستوى المخزون من Supply Chain Management في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="edb5b-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="edb5b-138">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="edb5b-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="edb5b-139">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="edb5b-139">Data integration</span></span>
<span data-ttu-id="edb5b-140">بالنسبة إلى المشروع الذي تعمل علبه، يجب التأكد من تحديث مفتاح التكامل لـ msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="edb5b-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="edb5b-141">انتقل إلى **تكامل البيانات > مجموعات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="edb5b-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="edb5b-142">حدد مجموعة الاتصال المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="edb5b-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="edb5b-143">على علامة التبويب **مفتاح التكامل‬**، تأكد من إضافة المفاتيح التالية إلى msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="edb5b-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="edb5b-144">msdynce_productnumber (رقم المنتج)</span><span class="sxs-lookup"><span data-stu-id="edb5b-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="edb5b-145">msdynce_warehouseid (معرف المستودع)</span><span class="sxs-lookup"><span data-stu-id="edb5b-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="edb5b-146">مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="edb5b-146">Data integration project</span></span>
<span data-ttu-id="edb5b-147">يمكنك تطبيق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام منتجات ومستودعات معينة فقط من إرسال معلومات على مستوى المخزون من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="edb5b-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="edb5b-148">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="edb5b-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="edb5b-149">مخزون المنتج (Supply Chain Management إلى Field Service): مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="edb5b-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="edb5b-150">[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="edb5b-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
