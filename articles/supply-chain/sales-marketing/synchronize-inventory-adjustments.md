---
title: مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: c989e6efff88768f0b370fc81eea971c5c11bcef
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251605"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="7da81-103">مزامنة عمليات تسوية المخزون من Field Service إلى Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7da81-103">Synchronize inventory adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7da81-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="7da81-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="7da81-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="7da81-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7da81-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="7da81-106">Templates and tasks</span></span>
<span data-ttu-id="7da81-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7da81-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="7da81-108">**القوالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="7da81-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="7da81-109">عمليات تسوية المخزون (Field Service إلى Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7da81-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="7da81-110">عمليات تحويل المخزون (Field Service إلى Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7da81-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="7da81-111">**المهام في مشاريع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="7da81-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="7da81-112">عمليات تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="7da81-112">Inventory Adjustments</span></span>
- <span data-ttu-id="7da81-113">عمليات تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="7da81-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="7da81-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="7da81-114">Entity set</span></span>
| <span data-ttu-id="7da81-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="7da81-115">Field Service</span></span>                     | <span data-ttu-id="7da81-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7da81-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="7da81-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="7da81-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="7da81-118">رؤوس دفتر يومية تعديل مخزون CDS وبنوده</span><span class="sxs-lookup"><span data-stu-id="7da81-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="7da81-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="7da81-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="7da81-120">رؤوس دفتر يومية نقل مخزون CDS وبنوده</span><span class="sxs-lookup"><span data-stu-id="7da81-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="7da81-121">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="7da81-121">Entity flow</span></span>
<span data-ttu-id="7da81-122">ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Supply Chain Management، عندما تتغير **حالة الترحيل** من **تم الإنشاء** إلى **مرحّل**.</span><span class="sxs-lookup"><span data-stu-id="7da81-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="7da81-123">عند حدوث ذلك، سيتم تأمين أمر التحويل أو التسوية ويصبح للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="7da81-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="7da81-124">وهذا يعني أنه يمكن ترحيل عمليات التسوية والتحويل في Supply Chain Management، ولكن لا يمكن تعديلها.</span><span class="sxs-lookup"><span data-stu-id="7da81-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="7da81-125">في Supply Chain Management، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت أثناء التكامل.</span><span class="sxs-lookup"><span data-stu-id="7da81-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="7da81-126">راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="7da81-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="7da81-127">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="7da81-127">Field Service CRM solution</span></span> 
<span data-ttu-id="7da81-128">تمت إضافة حقل **وحدة المخزون** إلى "كيان **المنتج**.</span><span class="sxs-lookup"><span data-stu-id="7da81-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="7da81-129">ثمة حاجة إلى هذا الحقل لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Supply Chain Management، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7da81-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="7da81-130">عندما تقوم بتعيين المنتج على منتج تسوية المخزون لعمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة منتج المخزون.</span><span class="sxs-lookup"><span data-stu-id="7da81-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="7da81-131">إذا تم العثور على قيمة، فسيتم تأمين حقل **الوحدة** على منتج تسوية المخزون.</span><span class="sxs-lookup"><span data-stu-id="7da81-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="7da81-132">تمت إضافة حقل **حالة الترحيل** إلى كيان **تسوية المخزون** وكيان **تحويل المخزون**.</span><span class="sxs-lookup"><span data-stu-id="7da81-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="7da81-133">يُستخدم هذا الحقل كعامل تصفية عند إرسال تسوية أو تحويل إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7da81-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="7da81-134">الإعداد الافتراضي لهذا الحقل هو تم الإنشاء (1)، ومع ذلك لا يتم إرساله إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7da81-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="7da81-135">عندما تقوم بتحديث القيمة إلى مرحّل (2)، يتم إرساله إلى Supply Chain Management، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة.</span><span class="sxs-lookup"><span data-stu-id="7da81-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="7da81-136">تمت إضافة حقل **التسلسل الرقمي** إلى كيان **منتج تسوية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="7da81-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="7da81-137">يضمن هذا الحقل حصول التكامل على رقم فريد، بحيث تتمكن عملية التكامل من إنشاء التسوية وتحديثها؟</span><span class="sxs-lookup"><span data-stu-id="7da81-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="7da81-138">عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في كيان **الرقم التلقائي P2C** للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="7da81-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7da81-139">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="7da81-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="7da81-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7da81-140">Supply Chain Management</span></span>
<span data-ttu-id="7da81-141">بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="7da81-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="7da81-142">يتم تمكين ذلك من **إدارة المخزون > المهام الدورية > تكامل CDS > ترحيل دفاتر يومية مخزون التكامل**.</span><span class="sxs-lookup"><span data-stu-id="7da81-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7da81-143">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="7da81-143">Template mapping in Data integration</span></span>

<span data-ttu-id="7da81-144">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="7da81-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="7da81-145">تسوية المخزون (Field Service إلى Supply Chain Management): تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="7da81-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="7da81-146">[![تعيين القالب في تكامل البيانات](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="7da81-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="7da81-147">تحويل المخزون (Field Service إلى Supply Chain Management): تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="7da81-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="7da81-148">[![تعيين القالب في تكامل البيانات](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="7da81-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
