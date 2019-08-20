---
title: مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843399"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="82d72-103">مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="82d72-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82d72-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82d72-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="82d72-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="82d72-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="82d72-106">يستند قالب **أوامر العمل مع المشروع ‏(Field Service إلى Fin and Ops)** إلى قالب **أوامر العمل (Field Service إلى Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="82d72-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="82d72-107">لمزيد من المعلومات، راجع [مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="82d72-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="82d72-108">يصف هذا الموضوع الاختلافات بين القالبين فقط:</span><span class="sxs-lookup"><span data-stu-id="82d72-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="82d72-109">**أوامر العمل مع المشروع (Field Service إلى Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="82d72-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="82d72-110">**أوامر العمل (Field Service إلى Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="82d72-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="82d72-111">الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Finance and Operations يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="82d72-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="82d72-112">بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="82d72-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="82d72-113">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="82d72-113">Templates and tasks</span></span>

<span data-ttu-id="82d72-114">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="82d72-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="82d72-115">أوامر العمل مع المشروع (Field Service إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="82d72-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="82d72-116">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="82d72-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="82d72-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="82d72-117">WorkOrderHeader</span></span>
- <span data-ttu-id="82d72-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="82d72-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="82d72-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="82d72-119">WorkOrderProduct</span></span>
- <span data-ttu-id="82d72-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="82d72-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="82d72-121">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="82d72-121">Field Service CRM solution</span></span>
<span data-ttu-id="82d72-122">تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="82d72-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="82d72-123">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82d72-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="82d72-124">عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="82d72-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="82d72-125">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="82d72-125">Template mapping in Data integration</span></span>

<span data-ttu-id="82d72-126">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="82d72-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="82d72-127">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="82d72-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="82d72-128">[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="82d72-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="82d72-129">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="82d72-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="82d72-130">[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="82d72-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="82d72-131">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="82d72-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="82d72-132">[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="82d72-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="82d72-133">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="82d72-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="82d72-134">[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="82d72-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
