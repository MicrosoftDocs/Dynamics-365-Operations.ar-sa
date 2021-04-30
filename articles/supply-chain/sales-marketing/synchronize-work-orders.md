---
title: مزامنة أوامر العمل مع المشروع من Field Service إلى Supply Chain Management
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Dynamics 365 Field Service إلى Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0956e7aa51973014ee474d97829d3d15dfdea3b3
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909933"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="d0e3f-103">مزامنة أوامر العمل مع المشروع من Field Service إلى Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d0e3f-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d0e3f-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Dynamics 365 Field Service إلى Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d0e3f-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="d0e3f-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="d0e3f-106">يستند قالب **أوامر العمل مع المشروع ‏(Field Service إلى Supply Chain Management)** إلى قالب **أوامر العمل (Field Service إلى Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="d0e3f-107">لمزيد من المعلومات، راجع [مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="d0e3f-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="d0e3f-108">يصف هذا الموضوع الاختلافات بين القالبين فقط:</span><span class="sxs-lookup"><span data-stu-id="d0e3f-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="d0e3f-109">**أوامر العمل مع المشروع (Field Service إلى Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="d0e3f-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="d0e3f-110">**أوامر العمل (Field Service إلى Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="d0e3f-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="d0e3f-111">الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Supply Chain Management يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="d0e3f-112">بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d0e3f-113">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="d0e3f-113">Templates and tasks</span></span>

<span data-ttu-id="d0e3f-114">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="d0e3f-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="d0e3f-115">أوامر العمل مع المشروع (Field Service إلى Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="d0e3f-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="d0e3f-116">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="d0e3f-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="d0e3f-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="d0e3f-117">WorkOrderHeader</span></span>
- <span data-ttu-id="d0e3f-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="d0e3f-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="d0e3f-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="d0e3f-119">WorkOrderProduct</span></span>
- <span data-ttu-id="d0e3f-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="d0e3f-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d0e3f-121">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="d0e3f-121">Field Service CRM solution</span></span>
<span data-ttu-id="d0e3f-122">تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="d0e3f-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="d0e3f-123">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="d0e3f-124">عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d0e3f-125">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="d0e3f-125">Template mapping in Data integration</span></span>

<span data-ttu-id="d0e3f-126">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="d0e3f-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="d0e3f-127">أوامر العمل مع المشروع (Field Service إلى ‎Supply Chain Management)‎:‎‎ ‎‎WorkOrderHeader‎</span><span class="sxs-lookup"><span data-stu-id="d0e3f-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="d0e3f-128">[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="d0e3f-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="d0e3f-129">أوامر العمل مع المشروع (Field Service إلى Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="d0e3f-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="d0e3f-130">[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="d0e3f-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="d0e3f-131">أوامر العمل مع المشروع (Field Service إلى Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="d0e3f-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="d0e3f-132">[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="d0e3f-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="d0e3f-133">أوامر العمل مع المشروع (Field Service إلى Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="d0e3f-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="d0e3f-134">[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="d0e3f-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]