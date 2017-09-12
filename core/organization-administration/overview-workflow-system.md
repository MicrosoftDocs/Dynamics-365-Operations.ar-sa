---
title: "نظرة عامة على نظام سير العمل"
description: "يوضح هذا الموضوع نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations."
author: sericks007
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 9a236c6505812e468eea1149a74671ec7bb63793
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="workflow-system-overview"></a><span data-ttu-id="bebdb-103">نظرة عامة على نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-103">Workflow system overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bebdb-104">يوضح هذا الموضوع نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bebdb-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="bebdb-105">ما المقصود بسير العمل؟</span><span class="sxs-lookup"><span data-stu-id="bebdb-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="bebdb-106">المصطلح *سير* يمكن تعريفه بطريقتين: كنظام وكعملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="bebdb-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="bebdb-107">سير العمل كنظام</span><span class="sxs-lookup"><span data-stu-id="bebdb-107">Workflow is a system</span></span>

<span data-ttu-id="bebdb-108">سير العمل عبارة عن نظام مثبت مع Finance and Operations ويتم تشغيله على خادم كائنات التطبيق‬ (AOS).</span><span class="sxs-lookup"><span data-stu-id="bebdb-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="bebdb-109">يوفر نظام سير العمل الوظائف التي يمكن استخدامها في إنشاء سير عمل فردي، أو عمليات تجارية.</span><span class="sxs-lookup"><span data-stu-id="bebdb-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="bebdb-110">سير العمل كعملية تجارية</span><span class="sxs-lookup"><span data-stu-id="bebdb-110">Workflow is a business process</span></span>

<span data-ttu-id="bebdb-111">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="bebdb-111">A workflow represents a business process.</span></span> <span data-ttu-id="bebdb-112">فهو يحدد كيفية تدفق المستند، أو انتقاله عبر النظام عن طريق عرض الفرد المنوط بإكمال المهمة، أو اتخاذ القرار أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="bebdb-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="bebdb-113">على سبيل المثال، يُظهر الرسم التالي سير عمل لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="bebdb-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![سير عمل مع عناصر تم تعيينها للمستخدمين](./media/workflow_user.gif) 

<span data-ttu-id="bebdb-115">لاستيعاب سير العمل هذا على نحو أفضل، لنفترض أن سامي يقدم تقرير مصروفات بمبلغ 7000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="bebdb-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="bebdb-116">في هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام التي يقوم سامي بتوجيهها له.</span><span class="sxs-lookup"><span data-stu-id="bebdb-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="bebdb-117">بعد ذلك يجب أن يقوم تميم وسلمان باعتماد تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="bebdb-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="bebdb-118">لنفترض الآن أن سامي يقدم تقرير مصروفات بمبلغ 11.000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="bebdb-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="bebdb-119">ففي هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام ولا بد من اعتماد التقرير من قبل تميم وسلمان وسليم.</span><span class="sxs-lookup"><span data-stu-id="bebdb-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="bebdb-120"> فوائد استخدام نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="bebdb-121">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="bebdb-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="bebdb-122">**عمليات متسقة** — يمكنك تحديدمستندات بعينها تمت معالجتها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="bebdb-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="bebdb-123">ومن خلال استخدام نظام سير العمل، فأنت تؤكد على أنه تتم معالجة المستندات واعتمادها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="bebdb-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="bebdb-124">**وضوح العمليات** - يمكنك تتبع حالة وتاريخ ومعايير أداء مثيلات سير العمل.</span><span class="sxs-lookup"><span data-stu-id="bebdb-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="bebdb-125">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="bebdb-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="bebdb-126">**قائمة العمل المركزية** — يمكن للمستخدمين عرض قائمة عمل مركزية تعرض مهام سير العمل والموافقات المعينة لهم.</span><span class="sxs-lookup"><span data-stu-id="bebdb-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="bebdb-127">محتوى سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-127">Workflow content</span></span>

+ [<span data-ttu-id="bebdb-128">بنية سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="bebdb-129">عناصر سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="bebdb-130">إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="bebdb-131">إنشاء سير عمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="bebdb-132">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="bebdb-133">تكوين مهمة يدوية في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="bebdb-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="bebdb-134">تكوين مهمة مؤتمتة في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="bebdb-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="bebdb-135">تكوين عملية اعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="bebdb-136">تكوين خطوة اعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="bebdb-137">تكوين قرار يدوي في سير عمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="bebdb-138">تكوين قرار شرطي في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="bebdb-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="bebdb-139">تكوين نشاط موازٍ في سير عمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="bebdb-140">تكوين فرع موازٍ في سير عمل</span><span class="sxs-lookup"><span data-stu-id="bebdb-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="bebdb-141">تكوين سير عمل لعنصر بند</span><span class="sxs-lookup"><span data-stu-id="bebdb-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

