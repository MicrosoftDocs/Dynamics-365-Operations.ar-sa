---
title: "مزامنة مهام المشروع من Project Service Automation"
description: "يوضح هذا الموضوع القالب والمهمة الأساسية التي يتم استخدامها لمزامنة مهام المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="ac121-103">مزامنة مهام المشروع من Project Service Automation مباشرة إلى أنشطة المشاريع في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac121-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="ac121-104">يوضح هذا الموضوع القالب والمهمة الأساسية التي يتم استخدامها لمزامنة مهام المشروع مباشرةً من Microsoft Dynamics 365 لـ Project Service Automation إلى Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac121-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="ac121-105">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في Dynamics 365 for Finance and Operations إصدار 8.0.</span><span class="sxs-lookup"><span data-stu-id="ac121-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ac121-106">تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac121-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="ac121-107">يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac121-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="ac121-108">يتيح قالب التكامل المتوفر مع ميزة تكامل البيانات تدفق البيانات الخاصة بمهام المشاريع من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac121-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ac121-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac121-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="ac121-110">[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ac121-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="ac121-111">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="ac121-111">Template and task</span></span>

<span data-ttu-id="ac121-112">للوصول إلى القالب، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="ac121-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ac121-113">يتم استخدام القالب التالي والمهمة الأساسية لمزامنة مهام المشروع من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac121-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="ac121-114">-**اسم القالب في تكامل البيانات:** مهام المشاريع (PSA إلى Fin and Ops)-**اسم المهمة في المشروع:** مهام المشاريع</span><span class="sxs-lookup"><span data-stu-id="ac121-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="ac121-115">قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.</span><span class="sxs-lookup"><span data-stu-id="ac121-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="ac121-116">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="ac121-116">Entity set</span></span>

|<span data-ttu-id="ac121-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ac121-117">Project Service Automation</span></span>               | <span data-ttu-id="ac121-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac121-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="ac121-119">مهام المشروع</span><span class="sxs-lookup"><span data-stu-id="ac121-119">Project Tasks</span></span>                           | <span data-ttu-id="ac121-120">كيان التكامل لمهمة المشروع.</span><span class="sxs-lookup"><span data-stu-id="ac121-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="ac121-121">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="ac121-121">Entity flow</span></span>

<span data-ttu-id="ac121-122">تتم إدارة مهام المشاريع في Project Service Automation، ثم تتم مزامنتها إلى Finance and Operations كأنشطة مشاريع.</span><span class="sxs-lookup"><span data-stu-id="ac121-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ac121-123">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="ac121-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="ac121-124">قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.</span><span class="sxs-lookup"><span data-stu-id="ac121-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="ac121-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="ac121-125">Power Query</span></span>

<span data-ttu-id="ac121-126">يجب عليك استخدام Microsoft Power Query لتصفية البيانات في حالة تحقق هذه الشروط:</span><span class="sxs-lookup"><span data-stu-id="ac121-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="ac121-127">لديم سجلات موارد محددة في مهمة مشروع.</span><span class="sxs-lookup"><span data-stu-id="ac121-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="ac121-128">إذا كنت مضطرًا إلى استخدام Power Query، اتبع هذه الإرشادات:</span><span class="sxs-lookup"><span data-stu-id="ac121-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="ac121-129">يحتوي قالب مهام المشاريع (PSA إلى Fin and Ops) على عامل تصفية افتراضي لاستبعاد سجلات موارد معينة من ضمن مهمة مشروع من خلال تعيين عامل التصفية في **IsLineTask** إلى **خطأ**.</span><span class="sxs-lookup"><span data-stu-id="ac121-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="ac121-130">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.</span><span class="sxs-lookup"><span data-stu-id="ac121-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ac121-131">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="ac121-131">Template mapping in Data integration</span></span>

<span data-ttu-id="ac121-132">يبين الشكل التوضيحي التالي مثالاً لتعيينات مهمام القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ac121-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="ac121-133">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac121-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ac121-134">[![تعيين القالب](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="ac121-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


