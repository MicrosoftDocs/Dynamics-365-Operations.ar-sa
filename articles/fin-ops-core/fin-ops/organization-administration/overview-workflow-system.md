---
title: نظرة عامة على نظام سير العمل
description: يصف هذا الموضوع نظام سير العمل.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef77a5d81d12ec92eea86b1dd9902d9e3d80b33
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812353"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="55644-103">نظرة عامة على نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55644-104">يصف هذا الموضوع نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="55644-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="55644-105">ما المقصود بسير العمل؟</span><span class="sxs-lookup"><span data-stu-id="55644-105">What is workflow?</span></span>

<span data-ttu-id="55644-106">المصطلح *سير* يمكن تعريفه بطريقتين: كنظام وكعملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="55644-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="55644-107">سير العمل كنظام</span><span class="sxs-lookup"><span data-stu-id="55644-107">Workflow is a system</span></span>

<span data-ttu-id="55644-108">يُمثل سير العمل نظامًا يتم تشغيله على Application Object Server (AOS). </span><span class="sxs-lookup"><span data-stu-id="55644-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="55644-109">يوفر نظام سير العمل الوظائف التي يمكن استخدامها في إنشاء سير عمل فردي، أو عمليات تجارية.</span><span class="sxs-lookup"><span data-stu-id="55644-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="55644-110">سير العمل كعملية تجارية</span><span class="sxs-lookup"><span data-stu-id="55644-110">Workflow is a business process</span></span>

<span data-ttu-id="55644-111">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="55644-111">A workflow represents a business process.</span></span> <span data-ttu-id="55644-112">فهو يحدد كيفية تدفق المستند، أو انتقاله عبر النظام عن طريق عرض الفرد المنوط بإكمال المهمة، أو اتخاذ القرار أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="55644-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="55644-113">على سبيل المثال، يُظهر الرسم التالي سير عمل لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="55644-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![سير عمل مع عناصر تم تعيينها للمستخدمين](./media/workflow_user.gif)

<span data-ttu-id="55644-115">لاستيعاب سير العمل هذا على نحو أفضل، لنفترض أن سامي يقدم تقرير مصروفات بمبلغ 7000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="55644-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="55644-116">في هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام التي يقوم سامي بتوجيهها له.</span><span class="sxs-lookup"><span data-stu-id="55644-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="55644-117">بعد ذلك يجب أن يقوم تميم وسلمان باعتماد تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="55644-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="55644-118">لنفترض الآن أن سامي يقدم تقرير مصروفات بمبلغ 11.000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="55644-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="55644-119">ففي هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام ولا بد من اعتماد التقرير من قبل تميم وسلمان وسليم.</span><span class="sxs-lookup"><span data-stu-id="55644-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="55644-120"> فوائد استخدام نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="55644-121">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="55644-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="55644-122">**عمليات متسقة** — يمكنك تحديدمستندات بعينها تمت معالجتها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="55644-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="55644-123">ومن خلال استخدام نظام سير العمل، فأنت تؤكد على أنه تتم معالجة المستندات واعتمادها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="55644-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="55644-124">**وضوح العمليات** - يمكنك تتبع حالة وتاريخ ومعايير أداء مثيلات سير العمل.</span><span class="sxs-lookup"><span data-stu-id="55644-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="55644-125">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="55644-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="55644-126">**قائمة العمل المركزية** — يمكن للمستخدمين عرض قائمة عمل مركزية تعرض مهام سير العمل والموافقات المعينة لهم.</span><span class="sxs-lookup"><span data-stu-id="55644-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="55644-127">محتوى سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-127">Workflow content</span></span>

+ [<span data-ttu-id="55644-128">بنية نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="55644-129">عناصر سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="55644-130">الإجراءات في عمليات الموافقة على سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="55644-131">نظرة عامة حول إنشاء عمليات سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="55644-132">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="55644-133">تكوين المهام اليدوية في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="55644-134">تكوين المهام المؤتمتة في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="55644-135">تكوين عمليات الاعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="55644-136">تكوين خطوات الاعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="55644-137">تكوين القرارات اليدوية في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="55644-138">تكوين القرارات الشرطية في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="55644-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="55644-139">تكوين أنشطة موازية في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="55644-140">تكوين فروع موازٍية في سير عمل</span><span class="sxs-lookup"><span data-stu-id="55644-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="55644-141">تكوين عمليات سير عمل لعنصر بند</span><span class="sxs-lookup"><span data-stu-id="55644-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="55644-142">الأسئلة المتداولة حول سير العمل</span><span class="sxs-lookup"><span data-stu-id="55644-142">Workflow FAQ</span></span>](workflow-FAQ.md)
