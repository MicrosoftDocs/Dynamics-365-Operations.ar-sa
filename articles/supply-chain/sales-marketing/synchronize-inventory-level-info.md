---
title: "مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة معلومات مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="d8836-103">مزامنة معلومات مستوى المخزون من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="d8836-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d8836-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة معلومات مستوى المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8836-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d8836-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="d8836-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d8836-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="d8836-106">Templates and tasks</span></span>
<span data-ttu-id="d8836-107">يُستخدم القالب التالي والمهام الأساسية التالية لتشغيل مزامنة مستويات المخزون المتاح من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8836-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d8836-108">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="d8836-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="d8836-109">مخزون المنتج (Finance and Operations إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="d8836-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="d8836-110">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="d8836-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="d8836-111">مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="d8836-111">Product inventory</span></span>

<span data-ttu-id="d8836-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات المخزون:</span><span class="sxs-lookup"><span data-stu-id="d8836-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="d8836-113">المستودعات (Finance and Operations إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="d8836-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="d8836-114">منتجات Field Service مع وحدة المخزون (Finance and Operations إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="d8836-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="d8836-115">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="d8836-115">Entity set</span></span>

| <span data-ttu-id="d8836-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="d8836-116">Field Service</span></span>                      | <span data-ttu-id="d8836-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d8836-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="d8836-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="d8836-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="d8836-119">مخزون CDS الفعلي حسب المستودع</span><span class="sxs-lookup"><span data-stu-id="d8836-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="d8836-120">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="d8836-120">Entity flow</span></span>
<span data-ttu-id="d8836-121">يتم إرسال معلومات مستوى المخزون من Finance and Operations إلى Field Service لمنتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="d8836-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="d8836-122">تتضمن معلومات مستوى المخزون:</span><span class="sxs-lookup"><span data-stu-id="d8836-122">The inventory level information include:</span></span> 
- <span data-ttu-id="d8836-123">الكمية المتاحة‬ (الكمية الفعلية المسجلة الموجودة في المستودع)</span><span class="sxs-lookup"><span data-stu-id="d8836-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="d8836-124">الكمية تحت الطلب‬ (إجمالي الكمية المسجلة في أمر - على سبيل المثال، أمر مبيعات)</span><span class="sxs-lookup"><span data-stu-id="d8836-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="d8836-125">الكمية المطلوبة‬‬ (إجمالي الكمية المسجلة المطلوبة‬ - على سبيل المثال، أوامر الشراء)</span><span class="sxs-lookup"><span data-stu-id="d8836-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="d8836-126">يتم التقاط هذه المعلومات لكل منتج صادر لكل مستودع وتتم مزامنتها استنادًا إلى تعقب التغييرات، وذلك عند حدوث تغيير في مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="d8836-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="d8836-127">في Field Service، ينشئ حل التكامل دفاتر يومية المخزون للدلتا، للحصول على المستويات في Field Service لمطابقة المستويات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8836-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="d8836-128">سيعمل Finance and Operations كأساس لمستويات المخزون.</span><span class="sxs-lookup"><span data-stu-id="d8836-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="d8836-129">وهكذا من الضروري إعداد التكامل لأوامر العمل وعمليات التحويل والتسوية من Field Service إلى Finance and Operations إذا كانت هذه الوظيفة مستخدمة في Field Service مع مزامنة مستويات المخزون من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8836-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="d8836-130">يمكن مراقبة المنتجات والمستودعات حيث تستند مستويات المخزون إلى Finance and Operations بواسطة وظائف الاستعلام والتصفية المتقدمة (Power Query).</span><span class="sxs-lookup"><span data-stu-id="d8836-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="d8836-131">ملاحظة: من الممكن إنشاء عدة مستودعات في Field Services (باستخدام "تتم المحافظة عليه خارجيًا‬‏‫ = لا") ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف الاستعلام والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="d8836-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="d8836-132">يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8836-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="d8836-133">في هذه الحالة، لن تحصل Field service على تحديثات مستوى المخزون من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8836-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="d8836-134">اطلع على معلومات إضافية في "مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬" و"مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations‬".</span><span class="sxs-lookup"><span data-stu-id="d8836-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d8836-135">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="d8836-135">Field Service CRM solution</span></span>
<span data-ttu-id="d8836-136">يعتبر كيان "مخزون المنتج الخارجي" كيانًا جديدًا يستخدم فقط لواجهة التكامل الخلفية.</span><span class="sxs-lookup"><span data-stu-id="d8836-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="d8836-137">إنه يتلقى قيم مستوى المخزون من Finance and Operations في التكامل، ثم يحوّل هذه القيم إلى دفاتر يومية المخزون اليدوي، الذي يحوّل عندئذٍ منتجات المخزون في المستودع.</span><span class="sxs-lookup"><span data-stu-id="d8836-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d8836-138">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="d8836-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="d8836-139">في مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="d8836-139">In the Data Integration project</span></span>
<span data-ttu-id="d8836-140">طبّق عوامل التصفية باستخدام الاستعلام المتقدم والتصفية المتقدمة للتأكد من قيام المنتجات والمستودعات المطلوبة فقط بإرسال معلومات حول مستوى المخزون من Finance and Operations إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8836-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d8836-141">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="d8836-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="d8836-142">مخزون المنتج (Finance and Operations إلى Field Service): مخزون المنتج</span><span class="sxs-lookup"><span data-stu-id="d8836-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="d8836-143">[![تعيين القالب في تكامل البيانات](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="d8836-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

