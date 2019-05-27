---
title: نظام سير العمل
description: يصف هذا الموضوع نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
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
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545797"
---
# <a name="workflow-system"></a><span data-ttu-id="a5a82-103">نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5a82-104">يصف هذا الموضوع نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5a82-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="a5a82-105">ما المقصود بسير العمل؟</span><span class="sxs-lookup"><span data-stu-id="a5a82-105">What is workflow?</span></span>

<span data-ttu-id="a5a82-106">المصطلح *سير* يمكن تعريفه بطريقتين: كنظام وكعملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="a5a82-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="a5a82-107">سير العمل كنظام</span><span class="sxs-lookup"><span data-stu-id="a5a82-107">Workflow is a system</span></span>

<span data-ttu-id="a5a82-108">سير العمل عبارة عن نظام مثبت مع Finance and Operations ويتم تشغيله على خادم كائنات التطبيق‬ (AOS).</span><span class="sxs-lookup"><span data-stu-id="a5a82-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="a5a82-109">يوفر نظام سير العمل الوظائف التي يمكن استخدامها في إنشاء سير عمل فردي، أو عمليات تجارية.</span><span class="sxs-lookup"><span data-stu-id="a5a82-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="a5a82-110">سير العمل كعملية تجارية</span><span class="sxs-lookup"><span data-stu-id="a5a82-110">Workflow is a business process</span></span>

<span data-ttu-id="a5a82-111">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="a5a82-111">A workflow represents a business process.</span></span> <span data-ttu-id="a5a82-112">فهو يحدد كيفية تدفق المستند، أو انتقاله عبر النظام عن طريق عرض الفرد المنوط بإكمال المهمة، أو اتخاذ القرار أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="a5a82-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="a5a82-113">على سبيل المثال، يُظهر الرسم التالي سير عمل لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="a5a82-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![سير عمل مع عناصر تم تعيينها للمستخدمين](./media/workflow_user.gif)

<span data-ttu-id="a5a82-115">لاستيعاب سير العمل هذا على نحو أفضل، لنفترض أن سامي يقدم تقرير مصروفات بمبلغ 7000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="a5a82-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="a5a82-116">في هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام التي يقوم سامي بتوجيهها له.</span><span class="sxs-lookup"><span data-stu-id="a5a82-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="a5a82-117">بعد ذلك يجب أن يقوم تميم وسلمان باعتماد تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="a5a82-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="a5a82-118">لنفترض الآن أن سامي يقدم تقرير مصروفات بمبلغ 11.000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="a5a82-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="a5a82-119">ففي هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام ولا بد من اعتماد التقرير من قبل تميم وسلمان وسليم.</span><span class="sxs-lookup"><span data-stu-id="a5a82-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="a5a82-120"> فوائد استخدام نظام سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="a5a82-121">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="a5a82-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="a5a82-122">**عمليات متسقة** — يمكنك تحديدمستندات بعينها تمت معالجتها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="a5a82-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="a5a82-123">ومن خلال استخدام نظام سير العمل، فأنت تؤكد على أنه تتم معالجة المستندات واعتمادها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="a5a82-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="a5a82-124">**وضوح العمليات** - يمكنك تتبع حالة وتاريخ ومعايير أداء مثيلات سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a5a82-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="a5a82-125">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="a5a82-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="a5a82-126">**قائمة العمل المركزية** — يمكن للمستخدمين عرض قائمة عمل مركزية تعرض مهام سير العمل والموافقات المعينة لهم.</span><span class="sxs-lookup"><span data-stu-id="a5a82-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="a5a82-127">محتوى سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-127">Workflow content</span></span>

+ [<span data-ttu-id="a5a82-128">بنية سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="a5a82-129">عناصر سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="a5a82-130">إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="a5a82-131">إنشاء سير عمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="a5a82-132">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="a5a82-133">تكوين مهمة يدوية في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="a5a82-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="a5a82-134">تكوين مهمة مؤتمتة في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="a5a82-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="a5a82-135">تكوين عملية اعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="a5a82-136">تكوين خطوة اعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="a5a82-137">تكوين قرار يدوي في سير عمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="a5a82-138">تكوين قرار شرطي في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="a5a82-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="a5a82-139">تكوين نشاط موازٍ في سير عمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="a5a82-140">تكوين فرع موازٍ في سير عمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="a5a82-141">تكوين سير عمل لعنصر بند</span><span class="sxs-lookup"><span data-stu-id="a5a82-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="a5a82-142">الأسئلة المتداولة حول سير العمل</span><span class="sxs-lookup"><span data-stu-id="a5a82-142">Workflow FAQ</span></span>](workflow-FAQ.md)
