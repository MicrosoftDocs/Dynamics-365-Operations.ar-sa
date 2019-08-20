---
title: مزامنة قائمة المشاريع من Finance and Operations إلى Field Service
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843543"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="f3300-103">مزامنة قائمة المشاريع من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="f3300-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f3300-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f3300-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f3300-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="f3300-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f3300-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="f3300-106">Templates and tasks</span></span>
<span data-ttu-id="f3300-107">يتم استخدام القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المشاريع من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f3300-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f3300-108">**قالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="f3300-108">**Template in Data integration**</span></span>
- <span data-ttu-id="f3300-109">المشاريع (Fin and Ops إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="f3300-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="f3300-110">**مهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="f3300-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="f3300-111">المشاريع</span><span class="sxs-lookup"><span data-stu-id="f3300-111">Projects</span></span>

<span data-ttu-id="f3300-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات قائمة المشاريع:</span><span class="sxs-lookup"><span data-stu-id="f3300-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="f3300-113">الحسابات (Sales إلى Fin and Ops)‬</span><span class="sxs-lookup"><span data-stu-id="f3300-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="f3300-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="f3300-114">Entity set</span></span>
| <span data-ttu-id="f3300-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="f3300-115">Field Service</span></span>           | <span data-ttu-id="f3300-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f3300-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="f3300-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="f3300-117">msdynce_externalprojects</span></span> | <span data-ttu-id="f3300-118">المشاريع</span><span class="sxs-lookup"><span data-stu-id="f3300-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="f3300-119">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="f3300-119">Entity flow</span></span>
<span data-ttu-id="f3300-120">يتم إنشاء المشاريع في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3300-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="f3300-121">ستتم مزامنة المشاريع التي تم فيها تعيين **نوع المشروع** إلى **الوقت والمادة** وتعيين **مرحلة المشروع** إلى **قيد التقدم** مع الكيان **مشروع خارجي** في Field Service، بما في ذلك رقم المشروع واسم المشروع ومرحلة المشروع ومعلومات حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="f3300-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="f3300-122">تُستخدم قائمة **المشروع الخارجي** لإقران أوامر عمل Field service مع مشاريع Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3300-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f3300-123">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="f3300-123">Field Service CRM solution</span></span>
<span data-ttu-id="f3300-124">يحصل الكيان **مشروع الخارجي** على جميع المشاريع من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3300-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="f3300-125">تمت إضافة الحقل **مشروع خارجي** إلى الكيان **أمر عمل**.</span><span class="sxs-lookup"><span data-stu-id="f3300-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="f3300-126">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3300-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="f3300-127">عندما تتغير **حالة النظام** من **مفتوح – قيد التقدم(690,970,000)** إلى حالة أعلى، سيتم تأمين الحقل **مشروع خارجي** وسيتعذر عليك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="f3300-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f3300-128">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="f3300-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="f3300-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f3300-129">Finance and Operations</span></span>
<span data-ttu-id="f3300-130">تمكين تعقب التغييرات لمشاريع كيان البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3300-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f3300-131">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="f3300-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="f3300-132">المشاريع (Fin and Ops إلى Field Service): المشاريع</span><span class="sxs-lookup"><span data-stu-id="f3300-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="f3300-133">[![تعيين القالب في تكامل البيانات](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="f3300-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
