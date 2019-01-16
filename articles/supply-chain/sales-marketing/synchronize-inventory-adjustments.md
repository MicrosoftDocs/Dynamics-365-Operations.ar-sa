---
title: "مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Finance and Operations"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="cc2ac-103">مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2ac-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cc2ac-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cc2ac-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="cc2ac-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cc2ac-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="cc2ac-106">Templates and tasks</span></span>
<span data-ttu-id="cc2ac-107">يُستخدم القالب التالي والمهام الأساسية لتشغيل مزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="cc2ac-108">**اسم القوالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="cc2ac-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="cc2ac-109">تسوية المخزون (Field Service إلى Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="cc2ac-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="cc2ac-110">تحويل المخزون (Field Service إلى Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="cc2ac-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="cc2ac-111">**أسماء المهام في مشاريع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="cc2ac-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="cc2ac-112">عمليات تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="cc2ac-112">Inventory Adjustments</span></span>
- <span data-ttu-id="cc2ac-113">عمليات تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="cc2ac-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="cc2ac-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="cc2ac-114">Entity set</span></span>
| <span data-ttu-id="cc2ac-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="cc2ac-115">Field Service</span></span>                     | <span data-ttu-id="cc2ac-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2ac-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="cc2ac-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="cc2ac-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="cc2ac-118">رؤوس دفتر يومية تعديل مخزون CDS وبنوده</span><span class="sxs-lookup"><span data-stu-id="cc2ac-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="cc2ac-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="cc2ac-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="cc2ac-120">رؤوس دفتر يومية نقل مخزون CDS وبنوده</span><span class="sxs-lookup"><span data-stu-id="cc2ac-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="cc2ac-121">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="cc2ac-121">Entity flow</span></span>
<span data-ttu-id="cc2ac-122">ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Finance and Operations، عندما تتغير  **حالة الترحيل** من "تم الإنشاء" إلى "مرحّل".</span><span class="sxs-lookup"><span data-stu-id="cc2ac-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="cc2ac-123">عندما يحدث هذا الأمر، سيتم تأمين أمر التسوية أو التحويل وسيصبح للقراءة فقط، إذ يتم ترحيل عمليات التسوية أو التحويل في Finance and Operations وبالتالي يتعذر تعديلها.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="cc2ac-124">في Finance and Operations، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت مع التكامل.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="cc2ac-125">راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cc2ac-126">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="cc2ac-126">Field Service CRM solution</span></span> 
<span data-ttu-id="cc2ac-127">تمت إضافة حقل "وحدة المخزون" إلى "كيان المنتج".</span><span class="sxs-lookup"><span data-stu-id="cc2ac-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="cc2ac-128">ثمة حاجة إلى هذا الحقل لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Operations، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="cc2ac-129">عندما تقوم بتعيين المنتج على "منتج تسوية المخزون" لكل من عمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة "منتج مخزون المنتجات".</span><span class="sxs-lookup"><span data-stu-id="cc2ac-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="cc2ac-130">إذا تم العثور على قيمة، فسيتم تأمين حقل الوحدة على منتج تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="cc2ac-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="cc2ac-131">تمت إضافة حقل "حالة الترحيل" إلى كيان تسوية المخزون وكيان تحويل المخزون.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="cc2ac-132">يُستخدم هذا الحقل كعامل تصفية عند إرسال تسوية أو تحويل إلى Operations.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="cc2ac-133">تم تعيين هذا الحقل إلى تم الإنشاء (1) بشكل افتراضي، وبالتالي لن يتم إرساله إلى Operations.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="cc2ac-134">عندما تقوم بتغييره إلى مرحّل (2)، يتم إرساله إلى Operations، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة إليه.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="cc2ac-135">تمت إضافة حقل "التسلسل الرقمي" إلى "كيان المنتج".</span><span class="sxs-lookup"><span data-stu-id="cc2ac-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="cc2ac-136">يساعد هذا الحقل في حصول عملية التكامل على رقم فريد، وبالتالي تعلم هذه العملية متى يجب تنفيذ عمليات إنشاء ومتى يجب تنفيذ عمليات تحديث.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="cc2ac-137">عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في كيان الرقم التلقائي P2C للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cc2ac-138">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="cc2ac-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="cc2ac-139">في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2ac-139">In Finance and Operations</span></span>
<span data-ttu-id="cc2ac-140">بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="cc2ac-141">يتم تمكين ذلك من: إدارة المخزون > المهام الدورية > تكامل CDS > ترحيل دفاتر يومية مخزون التكامل‬</span><span class="sxs-lookup"><span data-stu-id="cc2ac-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cc2ac-142">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="cc2ac-142">Template mapping in Data integration</span></span>

<span data-ttu-id="cc2ac-143">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="cc2ac-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="cc2ac-144">تسوية المخزون (Field Service إلى Finance and Operations): تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="cc2ac-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="cc2ac-145">[![تعيين القالب في تكامل البيانات](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="cc2ac-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="cc2ac-146">تحويل المخزون (Field Service إلى Finance and Operations): تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="cc2ac-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="cc2ac-147">[![تعيين القالب في تكامل البيانات](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="cc2ac-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

