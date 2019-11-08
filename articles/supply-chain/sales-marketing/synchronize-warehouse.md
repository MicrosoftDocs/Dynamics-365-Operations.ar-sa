---
title: مزامنة المستودعات من Supply Chain Management إلى Field Service
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
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
ms.openlocfilehash: b55a0b9e54eabdcdbd3f858cf3725b8fe833f65d
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653384"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="dd8b2-103">مزامنة المستودعات من Supply Chain Management إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="dd8b2-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dd8b2-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="dd8b2-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="dd8b2-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="dd8b2-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="dd8b2-106">Templates and tasks</span></span>
<span data-ttu-id="dd8b2-107">يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة المستودعات من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="dd8b2-108">**قالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="dd8b2-108">**Template in Data integration**</span></span>
- <span data-ttu-id="dd8b2-109">المستودعات (Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="dd8b2-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="dd8b2-110">**مهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="dd8b2-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="dd8b2-111">المستودع</span><span class="sxs-lookup"><span data-stu-id="dd8b2-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="dd8b2-112">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="dd8b2-112">Entity set</span></span>
| <span data-ttu-id="dd8b2-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="dd8b2-113">Field Service</span></span>    | <span data-ttu-id="dd8b2-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dd8b2-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="dd8b2-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="dd8b2-115">msdyn_warehouses</span></span> | <span data-ttu-id="dd8b2-116">المستودعات</span><span class="sxs-lookup"><span data-stu-id="dd8b2-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="dd8b2-117">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="dd8b2-117">Entity flow</span></span>
<span data-ttu-id="dd8b2-118">يمكن مزامنة المستودعات التي يتم إنشاؤها وصيانتها في Supply Chain Management إلى Field Service عبر مشروع تكامل بيانات Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="dd8b2-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="dd8b2-119">يمكن التحكم في المستودعات التي تريد مزامنتها مع Field Service بواسطة وظائف الاستعلام والتصفية المتقدمة على المشروع.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="dd8b2-120">ويتم إنشاء المستودعات التي تتزامن من Supply Chain Management في Field Service مع تعيين الحقل **تتم المحافظة عليه خارجيًا‬** إلى **نعم** والسجل محدد للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="dd8b2-121">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="dd8b2-121">Field Service CRM solution</span></span>
<span data-ttu-id="dd8b2-122">لدعم التكامل بين Field Service وSupply Chain Management، يلزم وجود وظيفة إضافية من حل Field Service CRM.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="dd8b2-123">في الحل، تمت إضافة الحقل **تتم المحافظة عليه خارجيًا** إلى كيان **المستودع (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="dd8b2-124">يساعد هذا الحقل في تحديد ما إذا كانت معالجة المستودع تتم من Supply Chain Management أو إذا كان موجودًا فقط في Field Service.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="dd8b2-125">تتضمن إعدادات هذا الحقل:</span><span class="sxs-lookup"><span data-stu-id="dd8b2-125">The settings for this field include:</span></span>
- <span data-ttu-id="dd8b2-126">**نعم** – نشأ المستودع من Supply Chain Management ولن يكون قابلاً للتحرير في Sales.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="dd8b2-127">**لا** – تم إدخال المستودع مباشرة في Field Service ويتم الاحتفاظ به هنا.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="dd8b2-128">يساعد الحقل **تتم المحافظة عليه خارجيًا** في التحكم في مزامنة مستويات المخزون والتسويات وعمليات التحويل والاستخدام في أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="dd8b2-129">يمكن استخدام فقط المستودعات حيث تم تعيين الخيار **تتم المحافظة عليها خارجيًا‬‏‫** إلى **نعم** للمزامنة مباشرة إلى المستودع نفسه في النظام الآخر.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd8b2-130">من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا‬‏‫** = لا") ثم تعيينها إلى مستودع واحد باستخدام وظائف التصفية والاستعلام المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="dd8b2-131">يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="dd8b2-132">في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="dd8b2-133">للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="dd8b2-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="dd8b2-134">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="dd8b2-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="dd8b2-135">مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="dd8b2-135">Data Integration project</span></span>
<span data-ttu-id="dd8b2-136">قبل مزامنة المستودعات، تأكد من تحديث وظائف الاستعلام والتصفية المتقدمة بحيث تتضمن فقط المستودعات التي تريد إحضارها من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="dd8b2-137">لاحظ أنك ستحتاج إلى المستودع في Field Service لتطبيقه على أوامر العمل والتسويات وعمليات التحويل.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="dd8b2-138">للتأكد من وجود **مفتاح تكامل** لـ **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="dd8b2-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="dd8b2-139">انتقل إلى "تكامل البيانات".</span><span class="sxs-lookup"><span data-stu-id="dd8b2-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="dd8b2-140">حدد علامة التبويب **مجموعة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="dd8b2-141">حدد مجموعة الاتصال المستخدمة لمزامنة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="dd8b2-142">حدد علامة التبويب **مفتاح التكامل**.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="dd8b2-143">ابحث عن msdyn_warehouses وتأكد من إضافة المفتاح **msdyn_name (الاسم)**.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="dd8b2-144">إذا لم يظهر، فأضفه بالنقر فوق **إضافة مفتاح**، ثم انقر فوق **حفظ** في الجزء العلوي من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dd8b2-145">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="dd8b2-145">Template mapping in Data integration</span></span>

<span data-ttu-id="dd8b2-146">يبين الشكل التوضيحي التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="dd8b2-147">المستودعات (Supply Chain Management إلى Field Service): المستودع</span><span class="sxs-lookup"><span data-stu-id="dd8b2-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="dd8b2-148">[![تعيين القالب في تكامل البيانات](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="dd8b2-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
