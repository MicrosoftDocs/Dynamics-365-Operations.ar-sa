---
title: "إجراءات سير العمل"
description: "توضح هذه المقالة الإجراءات التي يمكن أن يتخذها كل مشارك في عملية موافقة على سير عمل."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a4717accfa7e5879ee757820c39f000fa7d3e95
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-actions"></a><span data-ttu-id="eb8dc-103">إجراءات سير العمل</span><span class="sxs-lookup"><span data-stu-id="eb8dc-103">Workflow actions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eb8dc-104">توضح هذه المقالة الإجراءات التي يمكن أن يتخذها كل مشارك في عملية موافقة على سير عمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="eb8dc-105">يمكن أن ينطوي سير العمل على عدة مجموعات من الأشخاص: المنشئ، والمعينين للمهام، وصانعي القرار، والمعتمدين.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="eb8dc-106">على سبيل المثال، في سير عمل تقرير المصروفات التالي، يعد سامي هو المنشئ، وأعضاء قائمة الانتظار هم المعينين للمهام، وسعيد هو صانع القرار، وسمر، وفيصل هم المعتمدون.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>   

<span data-ttu-id="eb8dc-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="eb8dc-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span> 

<span data-ttu-id="eb8dc-108">تشرح الأقسام التالية إجراءات سير العمل التي تستطيع كل مجموعة تنفيذها.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="eb8dc-109">الإجراءات التي يمكن أن يتخذها المنشئ</span><span class="sxs-lookup"><span data-stu-id="eb8dc-109">Actions that an originator can perform</span></span>
<span data-ttu-id="eb8dc-110">يبدأ المنشئ في إجراء مثيل سير عمل عن طريق إرسال مستند للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="eb8dc-111">على سبيل المثال، يجب على سامي النقر فوق الزر **إرسال** في صفحة **تقرير المصروفات** لإرسال تقرير المصروفات الخاص به.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="eb8dc-112">الإجراءات التي يمكن أن يتخذها معين لهمة</span><span class="sxs-lookup"><span data-stu-id="eb8dc-112">Actions that a task assignee can perform</span></span>
<span data-ttu-id="eb8dc-113">يمكن تعيين مهمة إلى عدة أشخاص أو إلى قائمة انتظار عنصر عمل تتم مراقبته من قِبل عدة أشخاص.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="eb8dc-114">ومع ذلك، يمكن لشخص واحد فقط إكمال مهمة.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-114">However, only one person can complete a task.</span></span> <span data-ttu-id="eb8dc-115">على سبيل المثال، قام سامي بإرسال تقرير مصروفات وتوجيه ايصالاته إلى إدارة تقارير المصروفات في المؤسسة الخاصة به لمراجعتها.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span> 

<span data-ttu-id="eb8dc-116">ويراقب أعضاء إدارة تقارير مصروفات شركة المنتجات التجارية قائمة الانتظار.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="eb8dc-117">وقبلت منال، وهي عضو في تلك الإدارة، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="eb8dc-118">ويمكنها الآن إجراء واحد من الإجراءات التالية: الإكمال أو الرفض أو التفويض أو طلب التغيير أو إعادة التعيين أو الإصدار.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span> 

<span data-ttu-id="eb8dc-119">**ملاحظة:** تتنوع الإجراءات المتاحة استنادًا إلى الطريقة التي قام بها مطور البرنامج بتصميم المهمة.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-119">**Note:** The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="eb8dc-120">الإكمال</span><span class="sxs-lookup"><span data-stu-id="eb8dc-120">Complete</span></span>

<span data-ttu-id="eb8dc-121">عندما يقوم مستخدم بإكمال مهمة، يتم تعيين المستند الذي تم إرساله للمعالجة إلى المستخدم التالي في سير العمل، عندما يكون هناك مستخدم تالي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="eb8dc-122">عند عدم الحاجة إلى إجراء مزيد من المعالجة، تنتهي عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-122">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="eb8dc-123">على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="eb8dc-124">وبعد أن تُكمل منال مراجعتها، يتم تعيين المستند إلى يحيى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="eb8dc-125">رفض</span><span class="sxs-lookup"><span data-stu-id="eb8dc-125">Reject</span></span>

<span data-ttu-id="eb8dc-126">وعندما يقوم مستخدم برفض مستند، تنتهي عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-126">When a user rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="eb8dc-127">على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="eb8dc-128">وإذا رفضت منال تقرير المصروفات، تنتهي عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-128">If Julie rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="eb8dc-129">ويمكن لسامي فيما بعد إعادة إرسال تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="eb8dc-130">ويمكنه إجراء التغييرات أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="eb8dc-131">فإذا أعاد سامي إرسال تقرير المصروفات، تبدأ عملية سير العمل في مهمة المراجعة اليدوية.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="eb8dc-132">التفويض</span><span class="sxs-lookup"><span data-stu-id="eb8dc-132">Delegate</span></span>

<span data-ttu-id="eb8dc-133">عندما يقوم مستخدم بتفويض مهمة، يتم تعيين المهمة إلى مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-133">When a user delegates a task, the task is assigned to another user.</span></span> 

<span data-ttu-id="eb8dc-134">على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="eb8dc-135">وتفوض منال هذه المهمة إلى تامر، وهو مساعد لها.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-135">Julie delegates this task to Tim, who is her assistant.</span></span> 

<span data-ttu-id="eb8dc-136">ويتصرف تامر بالنيابة عن منال فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="eb8dc-137">ولذلك، عندما يُكمل تامر مراجعته، فإنه يتم تعيين تقرير المصروفات إلى يحيى، كما لو أن منال أكملت المهمة.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="eb8dc-138">تغيير الطلب</span><span class="sxs-lookup"><span data-stu-id="eb8dc-138">Request change</span></span>

<span data-ttu-id="eb8dc-139">عندما يطالب مستخدم بإجراء تغيير في مستند تم إرساله، يتم إرسال المستند إلى المنشئ.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span> 

<span data-ttu-id="eb8dc-140">على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="eb8dc-141">وتلاحظ منال بعض الأخطاء في تقرير المصروفات وتطلب إجراء تغيير.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="eb8dc-142">ويتم إرسال تقرير المصروفات إلى سامي مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-142">The expense report is sent back to Sam.</span></span> 

<span data-ttu-id="eb8dc-143">ويمكن لسامي إعادة إرسال تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="eb8dc-144">ويمكنه إجراء التغييرات المطلوبة أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="eb8dc-145">وإذا أعاد سامي إرسال تقرير المصروفات، فيجب على عضو في قائمة انتظار عناصر العمل مراجعة تقرير المصروفات والإيصالات مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="eb8dc-146">إعادة تعيين</span><span class="sxs-lookup"><span data-stu-id="eb8dc-146">Reassign</span></span>

<span data-ttu-id="eb8dc-147">يمكن لأعضاء قائمة انتظار عناصر العمل إعادة تعيين المستندات الموجودة في قائمة الانتظار تلك إلى قائمة انتظار أخرى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span> 

<span data-ttu-id="eb8dc-148">على سبيل المثال، تراقب منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، قائمة الانتظار.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="eb8dc-149">وللمساعدة في موازنة حمل العمل، تقوم بإعادة تعيين تقرير المصروفات والإيصالات المشمولة فيه، إلى قائمة انتظار أخرى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="eb8dc-150">الإصدار</span><span class="sxs-lookup"><span data-stu-id="eb8dc-150">Release</span></span>

<span data-ttu-id="eb8dc-151">وفي بعض الأحيان، قد يقبل عضو قائمة انتظار عناصر العمل مهمة، ولكنه يقرر أو تقرر أنه لا يمكنه إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="eb8dc-152">وفي هذه الحالة، الشخص الذي قام بقبول المهمة يمكنه إصدار المستند مرة أخرى إلى قائمة انتظار عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span> 

<span data-ttu-id="eb8dc-153">على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="eb8dc-154">إذا قررت منال أنه لا يمكنها إكمال المهمة، فيمكنها تحرير المستند.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="eb8dc-155">ويتم إرجاع تقرير المصروفات إلى قائمة الانتظار، بحيث يستطيع أعضاء آخرون في إدارة تقارير المصروفات شركة المنتجات التجارية إنجاز المهمة.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="eb8dc-156">الإجراءات التي يمكن أن يتخذها صانع قرار</span><span class="sxs-lookup"><span data-stu-id="eb8dc-156">Actions that a decision maker can perform</span></span>
<span data-ttu-id="eb8dc-157">بشكل عام، يتم تعيين مستند إلى صانع قرار، لأن هناك سؤال يجب على متخذ القرار الإجابة عنه.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="eb8dc-158">والإجابة على السؤال عادةً ما تكون **نعم** أو **لا**، أو **صحيح** أو **خطأ**.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="eb8dc-159">إذا لم يحدد متخذ القرار واحد من هذه الخيارات، فيمكنه أو يمكنها تفويض القرار.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="eb8dc-160">\[الخيار 1\] أو \[الخيار 2\]</span><span class="sxs-lookup"><span data-stu-id="eb8dc-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="eb8dc-161">يجب على صانع قرار الإجابة عن سؤال مرتبط بالمستند.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="eb8dc-162">والإجابة على السؤال عادةً ما تكون **نعم** أو **لا**، أو **صحيح** أو **خطأ**.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="eb8dc-163">وتحدد الإجابة التي يحددها متخذ القرار فرع سير العمل الذي يتم استخدامه لمعالجة المستند.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span> 

<span data-ttu-id="eb8dc-164">على سبيل المثال، يتم تعيين تقرير مصروفات سامي إلى يحيى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="eb8dc-165">ويجب أن يقرر يحيى ما إذا كانت المعلومات الموجودة في المستند تتطلب الاتصال بمدير سامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="eb8dc-166">وإذا قرر يحيى ضرورة الاتصال، فإنه يتم تعيين تقرير المصروفات إلى إسراء، التي يجب عليها الاتصال بمدير سامي لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="eb8dc-167">وإذا قرر يحيى أن الاتصال غير ضروري، فإنه يتم تعيين تقرير المصروفات إلى سعيد للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="eb8dc-168">التفويض</span><span class="sxs-lookup"><span data-stu-id="eb8dc-168">Delegate</span></span>

<span data-ttu-id="eb8dc-169">عندما يفوض متخذ قرار قرارًا، يتم تعيين المستند إلى مستخدم آخر يجب عليه اتخاذ القرار.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span> 

<span data-ttu-id="eb8dc-170">على سبيل المثال، يتم تعيين تقرير مصروفات سامي إلى يحيى.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="eb8dc-171">ويفوض يحيى قرارًا لمريم، وهي مساعدة له.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-171">John delegates the decision to Maria, who is his assistant.</span></span> 

<span data-ttu-id="eb8dc-172">وتتصرف مريم بالنيابة عن يحيى فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="eb8dc-173">وإذا قررت مريم أنه من غير الضروري الاتصال بمدير سامي، فإنه يتم تعيين تقرير المصروفات إلى إسراء، التي يجب عليها الاتصال بمدير سامي لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="eb8dc-174">وإذا قررت مريم أن الاتصال غير ضروري، فإنه يتم تعيين تقرير المصروفات إلى سعيد للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="eb8dc-175">الإجراءات التي يمكن أن يتخذها معتمد</span><span class="sxs-lookup"><span data-stu-id="eb8dc-175">Actions that an approver can perform</span></span>
<span data-ttu-id="eb8dc-176">عند تعيين مستند إلى معتمد، يمكن للمعتمد اتخاذ أحد الإجراءات التالية: اععتماد أو رفض أو تفويض أو طلب تغيير.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="eb8dc-177">اعتماد</span><span class="sxs-lookup"><span data-stu-id="eb8dc-177">Approve</span></span>

<span data-ttu-id="eb8dc-178">وعندما يقوم معتمد باعتماد مستند، يتم تعيين المستند إلى المستخدم التالي في سير العمل، إذا كان مستخدم تالي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="eb8dc-179">عند عدم الحاجة إلى إجراء مزيد من المعالجة، تنتهي عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-179">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="eb8dc-180">على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 6,000 دولار أمريكي، وتم تعيين هذا المستند إلى سعيد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="eb8dc-181">وعندما يعتمد سعيد المستند، يتم تعيينه إلى سمر للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="eb8dc-182">وعندما تقوم سمر باعتماد تقرير المصروفات، تنتهي عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="eb8dc-183">رفض</span><span class="sxs-lookup"><span data-stu-id="eb8dc-183">Reject</span></span>

<span data-ttu-id="eb8dc-184">عندما يقوم معتمد برفض مستند، تنتهي معالجة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-184">When an approver rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="eb8dc-185">على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 12,000 دولار أمريكي، وتم تعيين هذا المستند إلى سمر.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="eb8dc-186">إذا رفضت سمر تقرير المصروفات، تنتهي عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-186">If Sue rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="eb8dc-187">ويمكن لسامي إعادة إرسال تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="eb8dc-188">ويمكنه إجراء التغييرات أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية لتقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="eb8dc-189">فإذا أعاد سامي إرسال تقرير المصروفات، تبدأ عملية سير العمل من عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="eb8dc-190">التفويض</span><span class="sxs-lookup"><span data-stu-id="eb8dc-190">Delegate</span></span>

<span data-ttu-id="eb8dc-191">عندما يقوم معتمد بتفويض مستند، يتم تعيين المستند إلى مستخدم آخر للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span> 

<span data-ttu-id="eb8dc-192">على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 12,000 دولار أمريكي، وتم تعيين هذا المستند إلى سعيد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="eb8dc-193">يقوم سعيد بتفويض تقرير المصروفات إلى فيصل.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-193">Frank delegates the expense report to Ann.</span></span> 

<span data-ttu-id="eb8dc-194">عندئذٍ يتصرف فيصل نيابةً عن سعيد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="eb8dc-195">ولذلك، عندما يقوم فيصل باعتماد المستند، فإنه يتم تعيين المستند إلى سمر للاعتماد، تمامًا كما لو أن سعيد قد اعتمده.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="eb8dc-196">وبعد أن تعتمد سمر المستند، يتم إرساله إلى فيصل للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="eb8dc-197">تغيير الطلب</span><span class="sxs-lookup"><span data-stu-id="eb8dc-197">Request change</span></span>

<span data-ttu-id="eb8dc-198">عندما يطلب معتمد إجراء تغيير في مستند، تتم إعادة إرسال المستند إلى المنشئ.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span> 

<span data-ttu-id="eb8dc-199">على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 12,000 دولار أمريكي، وتم تعيين هذا المستند إلى سمر.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="eb8dc-200">وإذا طلبت سمر إجراء تغيير، فإنه تتم إعادة إرسال تقرير المصروفات إلى سامي.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-200">If Sue requests a change, the expense report is sent back to Sam.</span></span> 

<span data-ttu-id="eb8dc-201">ويمكن لسامي إعادة إرسال تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="eb8dc-202">ويمكنه إجراء التغييرات المطلوبة أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية لتقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="eb8dc-203">وإذا أعاد سامي إرسال تقرير المصروفات، فسيتم إرساله إلى سعيد للاعتماد نظرًا لأن سعيد هو المعتمد الأول في عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="eb8dc-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>




