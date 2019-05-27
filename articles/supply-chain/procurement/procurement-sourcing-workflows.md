---
title: عمليات سير العمل للتدبير وتحديد الموارد
description: تتطلب بعض المؤسسات اعتماد طلبات الشراء وأوامر الشراء بواسطة مستخدم غير الشخص الذي أدخل الحركة. لإعداد عملية اعتماد، يمكنك إنشاء سير عمل.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d25ca64fb6a3fa7d7898ec68568703f3de7b1595
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572709"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="c9393-104">عمليات سير العمل للتدبير وتحديد الموارد</span><span class="sxs-lookup"><span data-stu-id="c9393-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9393-105">تتطلب بعض المؤسسات اعتماد طلبات الشراء وأوامر الشراء بواسطة مستخدم غير الشخص الذي أدخل الحركة.</span><span class="sxs-lookup"><span data-stu-id="c9393-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="c9393-106">لإعداد عملية اعتماد، يمكنك إنشاء سير عمل.</span><span class="sxs-lookup"><span data-stu-id="c9393-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="c9393-107">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="c9393-107">A workflow represents a business process.</span></span> <span data-ttu-id="c9393-108">فهو يحدد كيفية تدفق المستند عبر النظام ويشير إلى الفرد المنوط بإكمال المهمة أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="c9393-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="c9393-109">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="c9393-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="c9393-110">**عمليات متسقة** — يمكنك تحديد عملية الموافقة على مستندات بعينها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="c9393-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="c9393-111">ويساعدك استخدام نظام سير العمل على ضمان معالجة المستندات والموافقة عليها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="c9393-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="c9393-112">**وضوح العمليات** - يمكنك تتبع حالة مثيل سير عمل معين وتاريخه ومعايير الأداء الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="c9393-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="c9393-113">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="c9393-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="c9393-114">**قائمة الأعمال المركزية**، يمكن للمستخدمين عرض قائمة أعمال مركزية لعرض مهام سير العمل واعتمادات معينة لها في كافة مهام سير العمل التي يشاركون فيها.</span><span class="sxs-lookup"><span data-stu-id="c9393-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="c9393-115">ويتوفر هذا في صفحة عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="c9393-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="c9393-116"> أنواع مهام سير العمل التي يمكنك إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="c9393-116">The types of workflows that you can create</span></span>
<span data-ttu-id="c9393-117">تتوفر مهام سير العمل التالية للتدبير وتحديد الموارد.</span><span class="sxs-lookup"><span data-stu-id="c9393-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c9393-118">**النوع**</span><span class="sxs-lookup"><span data-stu-id="c9393-118">**Type**</span></span>                         | <span data-ttu-id="c9393-119">**استخدم هذا النوع لـ**</span><span class="sxs-lookup"><span data-stu-id="c9393-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="c9393-120">مراجعة طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="c9393-120">Purchase requisition review</span></span>      | <span data-ttu-id="c9393-121">إنشاء عمليات مراجعة وعمليات سير عمل الاعتماد لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="c9393-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="c9393-122">مراجعة سطر طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="c9393-122">Purchase requisition line review</span></span> | <span data-ttu-id="c9393-123">إنشاء عمليات مراجعة وعمليات سير عمل الاعتماد لبنود طلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="c9393-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="c9393-124">سير عمل أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="c9393-124">Purchase order workflow</span></span>          | <span data-ttu-id="c9393-125">إنشاء عمليات سير عمل المراجعة والاعتماد الخاصة بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="c9393-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="c9393-126">سير عمل سطر أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="c9393-126">Purchase order line workflow</span></span>     | <span data-ttu-id="c9393-127">إنشاء عمليات سير عمل المراجعة والاعتماد الخاصة ببنود أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="c9393-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="c9393-128">سير عمل تطبيق إضافة مورِّد</span><span class="sxs-lookup"><span data-stu-id="c9393-128">Vendor add application workflow</span></span>  | <span data-ttu-id="c9393-129">إنشاء عمليات مراجعة وعمليات سير عمل الاعتماد لإضافة موردين جدد عبر طلبات الموردين.</span><span class="sxs-lookup"><span data-stu-id="c9393-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="c9393-130">إنشاء سير عمل</span><span class="sxs-lookup"><span data-stu-id="c9393-130">Creating a workflow</span></span>

<span data-ttu-id="c9393-131">لإنشاء سير عمل، انتقل إلى التدبير وتحديد الموارد &gt; الإعداد &gt; عمليات سير التدبير وتحديد الموارد وأنشئ سير عمل جديدًا عن طريق تحديد نوع سير العمل الذي تريد إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="c9393-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="c9393-132">وفي لوحة سير العمل، يمكنك سحب عناصر سير العمل في المصمم وربط العناصر في تدفق.</span><span class="sxs-lookup"><span data-stu-id="c9393-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="c9393-133">ويجب تكوين عناصر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="c9393-133">The workflow elements should be configured.</span></span> <span data-ttu-id="c9393-134">للحصول على الاعتماد وعناصر سير عمل المهام، يمكنك تكوين المشارك الذي يجب أن يتخذ إجراء.</span><span class="sxs-lookup"><span data-stu-id="c9393-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="c9393-135">نوع المشاركين</span><span class="sxs-lookup"><span data-stu-id="c9393-135">Types of participants</span></span>

<span data-ttu-id="c9393-136">يمكنك تعيين خطوة موافقة على المجموعات التالية من المشاركين.</span><span class="sxs-lookup"><span data-stu-id="c9393-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="c9393-137">مجموعة المستخدمين</span><span class="sxs-lookup"><span data-stu-id="c9393-137">User group</span></span>    | <span data-ttu-id="c9393-138">الوصف</span><span class="sxs-lookup"><span data-stu-id="c9393-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c9393-139">المشارك</span><span class="sxs-lookup"><span data-stu-id="c9393-139">Participant</span></span>   | <span data-ttu-id="c9393-140">قم بتعيين خطوة موافقة لأعضاء في مجموعة أو دور.</span><span class="sxs-lookup"><span data-stu-id="c9393-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="c9393-141">التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="c9393-141">Hierarchy</span></span>     | <span data-ttu-id="c9393-142">قم بتعيين خطوة الموافقة لمستخدمين في تسلسل هرمي مؤسسي معين.</span><span class="sxs-lookup"><span data-stu-id="c9393-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="c9393-143">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="c9393-143">Workflow user</span></span> | <span data-ttu-id="c9393-144">قم بتعيين خطوة الموافقة لمستخدمي سير العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="c9393-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="c9393-145">قائمة الانتظار</span><span class="sxs-lookup"><span data-stu-id="c9393-145">Queue</span></span>         | <span data-ttu-id="c9393-146">قم بتعيين خطوة الموافقة إلى قائمة انتظار عناصر عمل.</span><span class="sxs-lookup"><span data-stu-id="c9393-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="c9393-147">المستخدم</span><span class="sxs-lookup"><span data-stu-id="c9393-147">User</span></span>          | <span data-ttu-id="c9393-148">قم بتعيين خطوة الاعتماد لمستخدمين معينين.</span><span class="sxs-lookup"><span data-stu-id="c9393-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="c9393-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c9393-149">Additional resources</span></span>

- [<span data-ttu-id="c9393-150">تعريف مهام سير عمل العمليات التجارية لطلبات الشراء</span><span class="sxs-lookup"><span data-stu-id="c9393-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="c9393-151">سير عمل طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="c9393-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="c9393-152">إعداد المورّدين</span><span class="sxs-lookup"><span data-stu-id="c9393-152">Onboarding vendors</span></span>](vendor-onboarding.md)

