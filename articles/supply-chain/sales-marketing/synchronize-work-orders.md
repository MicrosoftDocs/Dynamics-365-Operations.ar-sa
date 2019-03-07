---
title: مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "329840"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="1050d-103">مزامنة أوامر العمل مع مشروع من Field Service إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1050d-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1050d-104">يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل مع رقم مشروع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1050d-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="1050d-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1050d-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="1050d-106">يستند قالب **منتجات Field Service ‏(Finance and Operations إلى Field Service)** إلى قالب **المنتجات (Finance and Operations إلى Sales) - مباشر** من العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="1050d-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="1050d-107">للحصول على مزيد من المعلومات، راجع [المنتجات (Finance and Operations إلى Sales) - مباشر](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="1050d-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="1050d-108">يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Finance and Operations إلى Field Service)** و**منتجات Field Service (Finance and Operations إلى Field Service) – مباشر**.</span><span class="sxs-lookup"><span data-stu-id="1050d-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="1050d-109">الفارق الأساسي هو أن هذا القالب يتضمن تعيين رقم المشروع المعين إلى أمر العمل في Field Service، مما يضمن أن أمر المبيعات المنشأ في Finance and Operations يتضمن رقم المشروع وأنه بإمكان الفوترة أن تحدث على المشروع ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="1050d-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="1050d-110">بالإضافة إلى ذلك، يستخدم القالب وظائف الاستعلام والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="1050d-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1050d-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="1050d-111">Templates and tasks</span></span>

<span data-ttu-id="1050d-112">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="1050d-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="1050d-113">أوامر العمل مع المشروع (Field Service إلى Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="1050d-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="1050d-114">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="1050d-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="1050d-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="1050d-115">WorkOrderHeader</span></span>
- <span data-ttu-id="1050d-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="1050d-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="1050d-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="1050d-117">WorkOrderProduct</span></span>
- <span data-ttu-id="1050d-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="1050d-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1050d-119">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="1050d-119">Field Service CRM solution</span></span>
<span data-ttu-id="1050d-120">تمت إضافة حقل **المشروع الخارجي** إلى كيان "أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="1050d-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="1050d-121">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1050d-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="1050d-122">عندما تتغير **حالة النظام** من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل **المشروع الخارجي** ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="1050d-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1050d-123">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="1050d-123">Template mapping in Data integration</span></span>

<span data-ttu-id="1050d-124">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="1050d-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="1050d-125">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="1050d-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="1050d-126">[![تعيين القالب في تكامل البيانات](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="1050d-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="1050d-127">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="1050d-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="1050d-128">[![تعيين القالب في تكامل البيانات](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="1050d-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="1050d-129">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="1050d-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="1050d-130">[![تعيين القالب في تكامل البيانات](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="1050d-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="1050d-131">أوامر العمل مع المشروع (Field Service إلى Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="1050d-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="1050d-132">[![تعيين القالب في تكامل البيانات](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="1050d-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
