---
title: "مزامنة قائمة المشاريع من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cbd48-103">مزامنة قائمة المشاريع من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="cbd48-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cbd48-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="cbd48-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cbd48-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="cbd48-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cbd48-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="cbd48-106">Templates and tasks</span></span>
<span data-ttu-id="cbd48-107">يُستخدم القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المشاريع من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cbd48-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cbd48-108">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="cbd48-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="cbd48-109">المشاريع (Finance and Operations إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="cbd48-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="cbd48-110">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="cbd48-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="cbd48-111">المشاريع</span><span class="sxs-lookup"><span data-stu-id="cbd48-111">Projects</span></span>

<span data-ttu-id="cbd48-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات قائمة المشاريع:</span><span class="sxs-lookup"><span data-stu-id="cbd48-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="cbd48-113">الحسابات (Sales إلى Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="cbd48-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="cbd48-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="cbd48-114">Entity set</span></span>
<span data-ttu-id="cbd48-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbd48-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="cbd48-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="cbd48-116">Field Service</span></span>           | <span data-ttu-id="cbd48-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbd48-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="cbd48-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="cbd48-118">msdynce_externalprojects</span></span> | <span data-ttu-id="cbd48-119">المشاريع</span><span class="sxs-lookup"><span data-stu-id="cbd48-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="cbd48-120">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="cbd48-120">Entity flow</span></span>
<span data-ttu-id="cbd48-121">يتم إنشاء المشاريع في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cbd48-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="cbd48-122">ستتم مزامنة المشاريع ذات **نوع مشروع** الوقت والمادة و**مرحلة مشروع** قيد التقدم إلى كيان **المشروع الخارجي** في Field Service، بما في ذلك رقم المشروع واسم المشروع ومرحلة المشروع ومعلومات حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="cbd48-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="cbd48-123">تُستخدم قائمة **المشروع الخارجي** لإقران أوامر عمل Field service مع مشاريع Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cbd48-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="cbd48-124">حل Field Service CRM المشروع الخارجي عبارة عن كيان جديد يحصل على جميع المشاريع من Operations.</span><span class="sxs-lookup"><span data-stu-id="cbd48-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="cbd48-125">تمت إضافة حقل "المشروع الخارجي" إلى كيان "أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="cbd48-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="cbd48-126">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Operations.</span><span class="sxs-lookup"><span data-stu-id="cbd48-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="cbd48-127">عندما تتغير حالة النظام من مفتوح - قيد التقديم(690,970,000) إلى حالة أعلى، سيتم تأمين حقل المشروع الخارجي ولا يمكنك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="cbd48-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cbd48-128">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="cbd48-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="cbd48-129">في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbd48-129">In Finance and Operations</span></span>
<span data-ttu-id="cbd48-130">تمكين تعقب التغييرات لمشاريع كيان البيانات</span><span class="sxs-lookup"><span data-stu-id="cbd48-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cbd48-131">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="cbd48-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="cbd48-132">المشاريع (Finance and Operations to Field Service): المشاريع</span><span class="sxs-lookup"><span data-stu-id="cbd48-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="cbd48-133">[![تعيين القالب في تكامل البيانات](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="cbd48-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

