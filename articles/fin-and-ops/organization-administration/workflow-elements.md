---
title: عناصر سير العمل
description: يوضح هذا الموضوع العناصر المختلفة التي تشكّل سير عمل.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fa9613b37fceeda1ea73c5fd5d4f7a7edc74cf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571901"
---
# <a name="workflow-elements"></a><span data-ttu-id="1ed7f-103">عناصر سير العمل</span><span class="sxs-lookup"><span data-stu-id="1ed7f-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ed7f-104">يوضح هذا الموضوع العناصر المختلفة التي تشكّل سير عمل.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="1ed7f-105">يتألف سير العمل من عناصر.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-105">A workflow consists of elements.</span></span> <span data-ttu-id="1ed7f-106">توضح الأقسام التالية كل نوع عنصر.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="1ed7f-107">مهام</span><span class="sxs-lookup"><span data-stu-id="1ed7f-107">Tasks</span></span>

<span data-ttu-id="1ed7f-108">تعتبر *المهمة* وحدة عمل يجب إجراؤها.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="1ed7f-109">يمكن إضافة نوعين من المهام لسير عمل: المهام اليدوية والمهام التلقائية.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="1ed7f-110">المهمة اليدوية</span><span class="sxs-lookup"><span data-stu-id="1ed7f-110">Manual task</span></span>

<span data-ttu-id="1ed7f-111">تعتبر *المهمة اليدوية* وحدة عمل يجب إجراؤها بواسطة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="1ed7f-112">على سبيل المثال، قد يشتمل سير عمل تقرير المصروفات على مهام يدوية تتطلب من المستخدمين المعينين إكمال الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="1ed7f-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="1ed7f-113">مراجعة الإيصالات التي تم إرسالها إلى جانب تقرير مصروفات.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="1ed7f-114">الاتصال بمدير موظف.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="1ed7f-115">مهمة مؤتمتة</span><span class="sxs-lookup"><span data-stu-id="1ed7f-115">Automated task</span></span>

<span data-ttu-id="1ed7f-116">تعتبر *المهمة التلقائية* وحدة عمل يجب إجراؤها بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="1ed7f-117">لا يلزم أي تفاعل بشري.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-117">No human interaction is required.</span></span> <span data-ttu-id="1ed7f-118">على سبيل المثال، قد يشتمل سير عمل أمر المبيعات على مهام تلقائية تتطلب من النظام إكمال الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="1ed7f-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="1ed7f-119">تنفيذ فحص ائتمان.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-119">Perform a credit check.</span></span>
- <span data-ttu-id="1ed7f-120">أنشئ سجل عميل للعميل، إذا لم يكن السجل موجودًا بالفعل.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="1ed7f-121">عمليات الاعتماد</span><span class="sxs-lookup"><span data-stu-id="1ed7f-121">Approval processes</span></span>

<span data-ttu-id="1ed7f-122">تعتبر *عملية الاعتماد* عملية تتألف من خطوات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="1ed7f-123">في كل خطوة من خطوات الاعتماد، يمكن للمستخدم تنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="1ed7f-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="1ed7f-124">اعتماد المستند.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-124">Approve the document.</span></span>
- <span data-ttu-id="1ed7f-125">رفض المستند.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-125">Reject the document.</span></span>
- <span data-ttu-id="1ed7f-126">طلب تغيير في المستند.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-126">Request a change to the document.</span></span>
- <span data-ttu-id="1ed7f-127">تعيين المستند إلى مستخدم آخر للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="1ed7f-128">عناصر سير عمل عنصر البند</span><span class="sxs-lookup"><span data-stu-id="1ed7f-128">Line-item workflow elements</span></span>

<span data-ttu-id="1ed7f-129">يمكن إنشاء سير عمل لمعالجة المستندات أو عناصر البنود الموجودة في مستند.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="1ed7f-130">على سبيل المثال، لقد قمت بإنشاء سير عمل اعتماد للجداول الزمنية.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="1ed7f-131">‏‫(سنشير إلى سير العمل هذا بصفته *سير عمل المستند*.) يمكنك إضافة *‬‏‫سير العمل عنصر الصنف* إلى سير عمل المستند هذا.‬</span><span class="sxs-lookup"><span data-stu-id="1ed7f-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="1ed7f-132">وعند تشغيل صنف البند، يتم إرسال كل صنف بند في المستند للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="1ed7f-133">قد تحتاج إلى معالجة كافة أصناف البند بنفس بند سير عمل صنف البند، أو قد تحتاج إلى معالجة كل صنف بند بواسطة سير عمل صنف بند مختلف.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="1ed7f-134">تخيل أن موظف قام بتقديم جدول زمني يشبه الشكل التالي.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![سير العمل مع عناصر البند](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="1ed7f-136">في هذا السيناريو، قد تحتاج إلى إنشاء مهام سير عمل لعناصر البنود التالية:</span><span class="sxs-lookup"><span data-stu-id="1ed7f-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="1ed7f-137">**سير عمل عنصر البند 1** – يتم استخدام سير العمل هذا لمعالجة عناصر البند حيث يكون معرف المشروع هو 1111.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="1ed7f-138">**سير عمل عنصر البند 2** – يتم استخدام سير العمل هذا لمعالجة عناصر البند حيث يكون معرف المشروع هو 2222.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="1ed7f-139">**سير عمل عنصر البند 3** – يتم استخدام سير العمل هذا لمعالجة عناصر البند حيث يكون معرف المشروع هو 3333.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="1ed7f-140">عناصر التحكم في التدفق</span><span class="sxs-lookup"><span data-stu-id="1ed7f-140">Flow-control elements</span></span>

<span data-ttu-id="1ed7f-141">تتيح لك العناصر التالية تصميم مهام سير العمل التي لها فروع بديلة أو فروع يتم تشغيلها في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="1ed7f-142">قرار يدوي</span><span class="sxs-lookup"><span data-stu-id="1ed7f-142">Manual decision</span></span>

<span data-ttu-id="1ed7f-143">*القرار اليدوي* هو نقطة ينقسم عندها سير العمل إلى فرعين.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="1ed7f-144">يجب على المستخدم اتخاذ قرار، ويحدد هذا القرار أي فرع يتم استخدامه لمعالجة المستند الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="1ed7f-145">قرار مشروط</span><span class="sxs-lookup"><span data-stu-id="1ed7f-145">Conditional decision</span></span>

<span data-ttu-id="1ed7f-146">*القرار المشروط* هو نقطة ينقسم عندها سير العمل إلى فرعين.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="1ed7f-147">ومع ذلك، يقرر النظام أي فرع يتم استخدامه لمعالجة المستند الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="1ed7f-148">ولاتخاذ هذا القرار، يقوم النظام بتقييم المستند لتحديد ما إذا كان يستوفي الشروط المحددة أم لا.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="1ed7f-149">نشاط موازٍ</span><span class="sxs-lookup"><span data-stu-id="1ed7f-149">Parallel activity</span></span>

<span data-ttu-id="1ed7f-150">*النشاط الموازي* هو عنصر سير عمل يشمل فرعي سير عمل أو أكثر يتم تشغيلهم في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="1ed7f-151">سير العمل الفرعي</span><span class="sxs-lookup"><span data-stu-id="1ed7f-151">Subworkflow</span></span>

<span data-ttu-id="1ed7f-152">*سير العمل الفرعي* هو سير عمل يتم تشغيله داخل سياق سير عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
