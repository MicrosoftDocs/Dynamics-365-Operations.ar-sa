---
title: مزامنة مهام المشروع مباشرةً من Project Service Automation إلى Finance and Operations
description: يصف هذا الموضوع القالب والمهمة الأساسية التي يتم استخدامها لمزامنة مهام المشروع مباشرة من Dynamics 365 Project Service Automation Microsoft إلى Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770256"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="1c1dd-103">مزامنة مهام المشروع مباشرةً من Project Service Automation إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1c1dd-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1c1dd-104">يصف هذا الموضوع القالب والمهمة الأساسية التي يتم استخدامها لمزامنة مهام المشروع مباشرة من Dynamics 365 Project Service Automation إلى Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1c1dd-105">تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="1c1dd-106">إذا كنت تستخدم , Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="1c1dd-107">إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="1c1dd-108">يتوفر تكامل القيم الفعلية في الإصدار 8.0.1 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="1c1dd-109">تدفق البيانات الخاصة بـ Project Service Automation إلى Finance</span><span class="sxs-lookup"><span data-stu-id="1c1dd-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="1c1dd-110">يستخدم الحل المتكامل لـ Project Service Automation إلى Finance ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation وFinance</span><span class="sxs-lookup"><span data-stu-id="1c1dd-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1c1dd-111">يُتيح قالب التكامل المتوفر مع ميزة تكامل البيانات تدفق البيانات الخاصة بمهام المشروع من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1c1dd-112">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1c1dd-113">[![تدفق البيانات الخاصة بتكامل Project Service Automation مع Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1c1dd-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="1c1dd-114">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="1c1dd-114">Template and task</span></span>

<span data-ttu-id="1c1dd-115">للوصول إلى القالب، في مركز إدارة Microsoft Power Apps، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1c1dd-116">يتم استخدام القالب والمهام الأساسية التالية لمزامنة مهام المشروع من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1c1dd-117">**اسم القالب في تكامل البيانات:** مهام المشروع (PSA إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1c1dd-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1c1dd-118">**اسم المهمة في المشروع:** مهام المشروع</span><span class="sxs-lookup"><span data-stu-id="1c1dd-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="1c1dd-119">قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="1c1dd-120">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="1c1dd-120">Entity set</span></span>

| <span data-ttu-id="1c1dd-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1c1dd-121">Project Service Automation</span></span> | <span data-ttu-id="1c1dd-122">المالية</span><span class="sxs-lookup"><span data-stu-id="1c1dd-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="1c1dd-123">مهام المشروع</span><span class="sxs-lookup"><span data-stu-id="1c1dd-123">Project Tasks</span></span>              | <span data-ttu-id="1c1dd-124">كيان تكامل مهام المشروع</span><span class="sxs-lookup"><span data-stu-id="1c1dd-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="1c1dd-125">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="1c1dd-125">Entity flow</span></span>

<span data-ttu-id="1c1dd-126">تتم إدارة مهام المشاريع في Project Service Automation، ثم تتم مزامنتها إلى Finance كأنشطة مشاريع.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1c1dd-127">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="1c1dd-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="1c1dd-128">قبل القيام بمزامنة مهام المشروع، يجب عليك مزامنة عقود المشاريع والمشاريع.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="1c1dd-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="1c1dd-129">Power Query</span></span>

<span data-ttu-id="1c1dd-130">يجب عليك استخدام Microsoft Power Query لـ Excel لتصفية البيانات في حالة تحقق الشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="1c1dd-131">لديك سجلات خاصة بالموارد في مهمة مشروع.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="1c1dd-132">إذا كنت مضطرًا إلى استخدام Power Query، فاتبع هذه الإرشادات:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="1c1dd-133">يتضمن قالب مهام المشروع (PSA إلى Fin and Ops) عامل تصفية افتراضيًا يستبعد سجلات خاصة بالموارد من ضمن مهمة مشروع من خلال تعيين عامل التصفية في **IsLineTask** إلى **False**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="1c1dd-134">إذا قمت بإنشاء القالب الخاص بك، يجب عليك إضافة عامل التصفية هذا.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1c1dd-135">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="1c1dd-135">Template mapping in Data integration</span></span>

<span data-ttu-id="1c1dd-136">يبين الشكل التوضيحي التالي مثالاً لتعيينات مهمام القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="1c1dd-137">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1c1dd-138">[![تعيين القالب](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="1c1dd-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
