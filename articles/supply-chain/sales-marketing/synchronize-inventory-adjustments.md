---
title: مزامنة عمليات تحويل وتسوية المخزون من Field Service إلى Finance and Operations
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835708"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="9674b-103">مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9674b-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9674b-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="9674b-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9674b-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="9674b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9674b-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="9674b-106">Templates and tasks</span></span>
<span data-ttu-id="9674b-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة عمليات تحويل وتسوية المخزون من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9674b-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="9674b-108">**القوالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="9674b-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="9674b-109">تسوية المخزون (Field Service إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="9674b-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="9674b-110">تحويل المخزون‬ (Field Service إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="9674b-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="9674b-111">**المهام في مشاريع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="9674b-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="9674b-112">عمليات تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="9674b-112">Inventory Adjustments</span></span>
- <span data-ttu-id="9674b-113">عمليات تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="9674b-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="9674b-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="9674b-114">Entity set</span></span>
| <span data-ttu-id="9674b-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="9674b-115">Field Service</span></span>                     | <span data-ttu-id="9674b-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9674b-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="9674b-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="9674b-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="9674b-118">رؤوس دفتر يومية تعديل مخزون CDS وبنوده</span><span class="sxs-lookup"><span data-stu-id="9674b-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="9674b-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="9674b-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="9674b-120">رؤوس دفتر يومية نقل مخزون CDS وبنوده</span><span class="sxs-lookup"><span data-stu-id="9674b-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="9674b-121">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="9674b-121">Entity flow</span></span>
<span data-ttu-id="9674b-122">ستتم مزامنة عمليات تسوية وتحويل المخزون التي يتم تنفيذها في Field Service إلى Finance and Operations، عندما تتغير **حالة الترحيل** من **تم الإنشاء** إلى **مرحّل**.</span><span class="sxs-lookup"><span data-stu-id="9674b-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="9674b-123">عند حدوث ذلك، سيتم تأمين أمر التحويل أو التسوية ويصبح للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="9674b-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="9674b-124">وهذا يعني أنه يمكن ترحيل عمليات التسوية والتحويل في Finance and Operations، ولكن لا يمكن تعديلها.</span><span class="sxs-lookup"><span data-stu-id="9674b-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="9674b-125">في Finance and Operations، يمكنك إعداد وظيفة دفعية لترحيل دفاتر اليومية لعمليات تسوية أو تحويل المخزون التي نشأت أثناء التكامل.</span><span class="sxs-lookup"><span data-stu-id="9674b-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="9674b-126">راجع المتطلبات الأساسية التالية للحصول على تفاصيل حول كيفية تمكين الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="9674b-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="9674b-127">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="9674b-127">Field Service CRM solution</span></span> 
<span data-ttu-id="9674b-128">تمت إضافة حقل **وحدة المخزون** إلى "كيان **المنتج**.</span><span class="sxs-lookup"><span data-stu-id="9674b-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="9674b-129">ثمة حاجة إلى هذا الحقل لأن وحدة المبيعات والمخزون ليست دائمًا نفسها في Finance and Operations، ونحن نحتاج إلى وحدة المخزون لمخزون المستودع في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9674b-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="9674b-130">عندما تقوم بتعيين المنتج على منتج تسوية المخزون لعمليات تسوية المخزون وتحويل المخزون، سيتم إحضار الوحدة من قيمة منتج المخزون.</span><span class="sxs-lookup"><span data-stu-id="9674b-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="9674b-131">إذا تم العثور على قيمة، فسيتم تأمين حقل **الوحدة** على منتج تسوية المخزون.</span><span class="sxs-lookup"><span data-stu-id="9674b-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="9674b-132">تمت إضافة حقل **حالة الترحيل** إلى كيان **تسوية المخزون** وكيان **تحويل المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9674b-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="9674b-133">يُستخدم هذا الحقل كعامل تصفية عند إرسال تسوية أو تحويل إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9674b-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="9674b-134">الإعداد الافتراضي لهذا الحقل هو تم الإنشاء (1)، ومع ذلك لا يتم إرساله إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9674b-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="9674b-135">عندما تقوم بتحديث القيمة إلى مرحّل (2)، يتم إرساله إلى Finance and Operations، ولكن سيتعذر عليك بعد ذلك تغيير أي شيء في التسوية أو التحويل أو إضافة أية بنود جديدة.</span><span class="sxs-lookup"><span data-stu-id="9674b-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="9674b-136">تمت إضافة حقل **التسلسل الرقمي** إلى كيان **منتج تسوية المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9674b-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="9674b-137">يضمن هذا الحقل حصول التكامل على رقم فريد، بحيث تتمكن عملية التكامل من إنشاء التسوية وتحديثها؟</span><span class="sxs-lookup"><span data-stu-id="9674b-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="9674b-138">عندما تنشئ "منتج تسوية المخزون" الأول، سيؤدي ذلك إلى إنشاء سجل جديد في كيان **الرقم التلقائي P2C** للاحتفاظ بسلسلة الأرقام والبادئة المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="9674b-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9674b-139">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="9674b-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="9674b-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9674b-140">Finance and Operations</span></span>
<span data-ttu-id="9674b-141">بإمكان دفاتر يومية مخزون التكامل التي تم إنشاؤها بواسطة التكامل أن ترحّل بشكل تلقائي باستخدام وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="9674b-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="9674b-142">يتم تمكين ذلك من **إدارة المخزون > المهام الدورية > تكامل CDS > ترحيل دفاتر يومية مخزون التكامل**.</span><span class="sxs-lookup"><span data-stu-id="9674b-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9674b-143">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="9674b-143">Template mapping in Data integration</span></span>

<span data-ttu-id="9674b-144">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="9674b-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="9674b-145">تسوية المخزون (Field Service إلى Fin and Ops): تسوية المخزون</span><span class="sxs-lookup"><span data-stu-id="9674b-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="9674b-146">[![تعيين القالب في تكامل البيانات](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="9674b-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="9674b-147">تحويل المخزون (Field Service إلى Fin and Ops): تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="9674b-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="9674b-148">[![تعيين القالب في تكامل البيانات](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="9674b-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
