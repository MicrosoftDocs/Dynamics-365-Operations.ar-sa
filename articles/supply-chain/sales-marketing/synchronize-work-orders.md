---
title: "مزامنة أوامر العمل من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations."
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="6d6e4-103">مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6d6e4-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6d6e4-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="6d6e4-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="6d6e4-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="6d6e4-106">يستند قالب **منتجات Field Service ‏(Finance and Operations إلى Field Service)** إلى قالب **المنتجات (Finance and Operations إلى Sales) - مباشر** من العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="6d6e4-107">للحصول على مزيد من المعلومات، راجع [المنتجات (Finance and Operations إلى Sales) - مباشر](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="6d6e4-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="6d6e4-108">يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Finance and Operations إلى Field Service)** و**منتجات Field Service (Finance and Operations إلى Field Service) – مباشر**.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="6d6e4-109">الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Finance and Operations يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="6d6e4-110">بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6d6e4-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="6d6e4-111">Templates and tasks</span></span>

<span data-ttu-id="6d6e4-112">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="6d6e4-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="6d6e4-113">أوامر العمل مع المشروع (Field Service إلى Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="6d6e4-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="6d6e4-114">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="6d6e4-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="6d6e4-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6d6e4-115">WorkOrderHeader</span></span>
- <span data-ttu-id="6d6e4-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="6d6e4-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="6d6e4-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="6d6e4-117">WorkOrderProduct</span></span>
- <span data-ttu-id="6d6e4-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="6d6e4-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6d6e4-119">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="6d6e4-119">Field Service CRM solution</span></span>
<span data-ttu-id="6d6e4-120">تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="6d6e4-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="6d6e4-121">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="6d6e4-122">عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6d6e4-123">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="6d6e4-123">Template mapping in Data integration</span></span>

<span data-ttu-id="6d6e4-124">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="6d6e4-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="6d6e4-125">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6d6e4-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="6d6e4-126">[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="6d6e4-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="6d6e4-127">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="6d6e4-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="6d6e4-128">[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="6d6e4-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="6d6e4-129">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="6d6e4-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="6d6e4-130">[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="6d6e4-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="6d6e4-131">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="6d6e4-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="6d6e4-132">[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="6d6e4-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

