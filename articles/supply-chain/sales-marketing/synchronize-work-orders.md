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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2019
ms.locfileid: "836432"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="0548a-103">مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0548a-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0548a-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0548a-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="0548a-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="0548a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="0548a-106">يستند قالب **أوامر العمل مع المشروع ‏(Field Service إلى Fin and Ops)** إلى قالب **أوامر العمل (Field Service إلى Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="0548a-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="0548a-107">لمزيد من المعلومات، راجع [مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="0548a-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="0548a-108">يصف هذا الموضوع الاختلافات بين القالبين فقط:</span><span class="sxs-lookup"><span data-stu-id="0548a-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="0548a-109">**أوامر العمل مع المشروع (Field Service إلى Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="0548a-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="0548a-110">**أوامر العمل (Field Service إلى Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="0548a-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="0548a-111">الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Finance and Operations يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="0548a-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="0548a-112">بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="0548a-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0548a-113">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="0548a-113">Templates and tasks</span></span>

<span data-ttu-id="0548a-114">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="0548a-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="0548a-115">أوامر العمل مع المشروع (Field Service إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0548a-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="0548a-116">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="0548a-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="0548a-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0548a-117">WorkOrderHeader</span></span>
- <span data-ttu-id="0548a-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="0548a-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="0548a-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="0548a-119">WorkOrderProduct</span></span>
- <span data-ttu-id="0548a-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="0548a-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="0548a-121">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="0548a-121">Field Service CRM solution</span></span>
<span data-ttu-id="0548a-122">تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="0548a-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="0548a-123">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0548a-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="0548a-124">عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="0548a-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0548a-125">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="0548a-125">Template mapping in Data integration</span></span>

<span data-ttu-id="0548a-126">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="0548a-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="0548a-127">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0548a-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="0548a-128">[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="0548a-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="0548a-129">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="0548a-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="0548a-130">[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="0548a-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="0548a-131">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="0548a-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="0548a-132">[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="0548a-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="0548a-133">أوامر العمل مع المشروع (Field Service إلى Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="0548a-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="0548a-134">[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="0548a-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
