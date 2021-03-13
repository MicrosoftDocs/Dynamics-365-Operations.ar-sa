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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 828dd1324c2692b7b3f4bc15c5e50b3dbee8b72c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010912"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="c3001-103">مزامنة معلومات مستوى المخزون من Supply Chain Management إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="c3001-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c3001-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات المعلومات على مستوى المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="c3001-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="c3001-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="c3001-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c3001-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="c3001-106">Templates and tasks</span></span>
<span data-ttu-id="c3001-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة مستويات المخزون الفعلي من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="c3001-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="c3001-108">**قالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="c3001-108">**Template in Data integration**</span></span>
- <span data-ttu-id="c3001-109">مخزون المنتج (Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="c3001-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="c3001-110">**مهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="c3001-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="c3001-111">مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="c3001-111">Product inventory</span></span>

<span data-ttu-id="c3001-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:</span><span class="sxs-lookup"><span data-stu-id="c3001-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="c3001-113">المستودعات (Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="c3001-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="c3001-114">منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="c3001-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c3001-115">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="c3001-115">Entity set</span></span>

| <span data-ttu-id="c3001-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="c3001-116">Field Service</span></span>                      | <span data-ttu-id="c3001-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c3001-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="c3001-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="c3001-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="c3001-119">المخزون الفعلي حسب المستودع Dataverse</span><span class="sxs-lookup"><span data-stu-id="c3001-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="c3001-120">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="c3001-120">Entity flow</span></span>
<span data-ttu-id="c3001-121">يتم إرسال معلومات على مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="c3001-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="c3001-122">تتضمن المعلومات على مستوى المخزون:</span><span class="sxs-lookup"><span data-stu-id="c3001-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="c3001-123">الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)</span><span class="sxs-lookup"><span data-stu-id="c3001-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="c3001-124">الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر، على سبيل المثال، أمر مبيعات)</span><span class="sxs-lookup"><span data-stu-id="c3001-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="c3001-125">الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬، على سبيل المثال، أوامر الشراء)</span><span class="sxs-lookup"><span data-stu-id="c3001-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="c3001-126">يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="c3001-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="c3001-127">في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، بحيث تتطابق المستويات في Field Service مع المستويات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3001-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="c3001-128">سيعمل Supply Chain Management كأساس لمستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="c3001-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="c3001-129">وبالتالي، من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Supply Chain Management إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3001-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="c3001-130">يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Supply Chain Management بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).</span><span class="sxs-lookup"><span data-stu-id="c3001-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="c3001-131">من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا = لا**) ثم تعيينها إلى مستودع واحد في Supply Chain Management، باستخدام وظائف التصفية والاستعلام المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="c3001-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="c3001-132">يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3001-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="c3001-133">في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3001-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="c3001-134">للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="c3001-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c3001-135">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="c3001-135">Field Service CRM solution</span></span>
<span data-ttu-id="c3001-136">يُستخدم كيان **مخزون المنتج الخارجي** فقط لواجهة التكامل الخلفية.</span><span class="sxs-lookup"><span data-stu-id="c3001-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="c3001-137">ويتلقى هذا الكيان قيم مستوى المخزون من Supply Chain Management في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="c3001-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c3001-138">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="c3001-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="c3001-139">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="c3001-139">Data integration</span></span>
<span data-ttu-id="c3001-140">بالنسبة إلى المشروع الذي تعمل علبه، يجب التأكد من تحديث مفتاح التكامل لـ msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="c3001-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="c3001-141">انتقل إلى **تكامل البيانات > مجموعات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="c3001-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="c3001-142">حدد مجموعة الاتصال المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="c3001-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="c3001-143">على علامة التبويب **مفتاح التكامل‬**، تأكد من إضافة المفاتيح التالية إلى msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="c3001-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="c3001-144">msdynce_productnumber (رقم المنتج)</span><span class="sxs-lookup"><span data-stu-id="c3001-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="c3001-145">msdynce_warehouseid (معرف المستودع)</span><span class="sxs-lookup"><span data-stu-id="c3001-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="c3001-146">مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="c3001-146">Data integration project</span></span>
<span data-ttu-id="c3001-147">يمكنك تطبيق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام منتجات ومستودعات معينة فقط من إرسال معلومات على مستوى المخزون من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="c3001-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c3001-148">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="c3001-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="c3001-149">مخزون المنتج (Supply Chain Management إلى Field Service): مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="c3001-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="c3001-150">[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="c3001-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
