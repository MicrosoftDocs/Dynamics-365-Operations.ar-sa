---
title: عمليات سير العمل للتدبير وتحديد الموارد
description: تتطلب بعض المؤسسات اعتماد طلبات الشراء وأوامر الشراء بواسطة مستخدم غير الشخص الذي أدخل الحركة. لإعداد عملية اعتماد، يمكنك إنشاء سير عمل.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909221"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="9202d-104">عمليات سير العمل للتدبير وتحديد الموارد</span><span class="sxs-lookup"><span data-stu-id="9202d-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9202d-105">تتطلب بعض المؤسسات اعتماد طلبات الشراء وأوامر الشراء بواسطة مستخدم غير الشخص الذي أدخل الحركة.</span><span class="sxs-lookup"><span data-stu-id="9202d-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="9202d-106">لإعداد عملية اعتماد، يمكنك إنشاء سير عمل.</span><span class="sxs-lookup"><span data-stu-id="9202d-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="9202d-107">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="9202d-107">A workflow represents a business process.</span></span> <span data-ttu-id="9202d-108">فهو يحدد كيفية تدفق المستند عبر النظام ويشير إلى الفرد المنوط بإكمال المهمة أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="9202d-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="9202d-109">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="9202d-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="9202d-110">**عمليات متسقة** — يمكنك تحديد عملية الموافقة على مستندات بعينها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="9202d-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="9202d-111">ويساعدك استخدام نظام سير العمل على ضمان معالجة المستندات والموافقة عليها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="9202d-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="9202d-112">**وضوح العمليات** - يمكنك تتبع حالة مثيل سير عمل معين وتاريخه ومعايير الأداء الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="9202d-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="9202d-113">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="9202d-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="9202d-114">**قائمة الأعمال المركزية**، يمكن للمستخدمين عرض قائمة أعمال مركزية لعرض مهام سير العمل واعتمادات معينة لها في كافة مهام سير العمل التي يشاركون فيها.</span><span class="sxs-lookup"><span data-stu-id="9202d-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="9202d-115">ويتوفر هذا في صفحة عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="9202d-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="9202d-116"> أنواع مهام سير العمل التي يمكنك إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="9202d-116">The types of workflows that you can create</span></span>

<span data-ttu-id="9202d-117">تتوفر مهام سير العمل التالية للتدبير وتحديد الموارد.</span><span class="sxs-lookup"><span data-stu-id="9202d-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="9202d-118">النوع</span><span class="sxs-lookup"><span data-stu-id="9202d-118">Type</span></span> | <span data-ttu-id="9202d-119">استخدم هذا النوع لـ</span><span class="sxs-lookup"><span data-stu-id="9202d-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="9202d-120">مراجعة طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="9202d-120">Purchase requisition review</span></span> | <span data-ttu-id="9202d-121">إنشاء عمليات مراجعة وعمليات سير عمل الاعتماد لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="9202d-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="9202d-122">مراجعة سطر طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="9202d-122">Purchase requisition line review</span></span> | <span data-ttu-id="9202d-123">إنشاء عمليات مراجعة وعمليات سير عمل الاعتماد لبنود طلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="9202d-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="9202d-124">سير عمل أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="9202d-124">Purchase order workflow</span></span> | <span data-ttu-id="9202d-125">إنشاء عمليات سير عمل المراجعة والاعتماد الخاصة بأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9202d-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="9202d-126">سير عمل سطر أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="9202d-126">Purchase order line workflow</span></span> | <span data-ttu-id="9202d-127">إنشاء عمليات سير عمل المراجعة والاعتماد الخاصة ببنود أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9202d-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="9202d-128">سير عمل تطبيق إضافة مورِّد</span><span class="sxs-lookup"><span data-stu-id="9202d-128">Vendor add application workflow</span></span> | <span data-ttu-id="9202d-129">إنشاء عمليات مراجعة وعمليات سير عمل الاعتماد لإضافة موردين جدد عبر طلبات الموردين.</span><span class="sxs-lookup"><span data-stu-id="9202d-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="9202d-130">عند أضافه سير عمل جديد ، قد تري أيضا مهام سير العمل القديمة التالية المدرجة في مربع الحوار **إنشاء سير عمل**.</span><span class="sxs-lookup"><span data-stu-id="9202d-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="9202d-131">ترتبط هذه الوظائف *بتاكيد وظيفة الاستلام* المتوفرة في [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows)، ولكنها أصبحت مهمله.</span><span class="sxs-lookup"><span data-stu-id="9202d-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="9202d-132">مهام سير العمل هذه غير معتمده في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="9202d-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="9202d-133">سير عمل الإخطار بتاريخ استحقاق التسليم</span><span class="sxs-lookup"><span data-stu-id="9202d-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="9202d-134">سير عمل الإخطار الخاص بالفاتورة المستلمة</span><span class="sxs-lookup"><span data-stu-id="9202d-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="9202d-135">سير عمل الإخطار بفشل إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="9202d-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="9202d-136">سير عمل الإخطار برفض إيصال استلام المنتجات غير المؤكد عليه</span><span class="sxs-lookup"><span data-stu-id="9202d-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="9202d-137">إنشاء سير عمل</span><span class="sxs-lookup"><span data-stu-id="9202d-137">Creating a workflow</span></span>

<span data-ttu-id="9202d-138">لإنشاء سير عمل، انتقل إلى التدبير وتحديد الموارد &gt; الإعداد &gt; عمليات سير التدبير وتحديد الموارد وأنشئ سير عمل جديدًا عن طريق تحديد نوع سير العمل الذي تريد إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="9202d-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="9202d-139">وفي لوحة سير العمل، يمكنك سحب عناصر سير العمل في المصمم وربط العناصر في تدفق.</span><span class="sxs-lookup"><span data-stu-id="9202d-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="9202d-140">ويجب تكوين عناصر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="9202d-140">The workflow elements should be configured.</span></span> <span data-ttu-id="9202d-141">للحصول على الاعتماد وعناصر سير عمل المهام، يمكنك تكوين المشارك الذي يجب أن يتخذ إجراء.</span><span class="sxs-lookup"><span data-stu-id="9202d-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="9202d-142">نوع المشاركين</span><span class="sxs-lookup"><span data-stu-id="9202d-142">Types of participants</span></span>

<span data-ttu-id="9202d-143">يمكنك تعيين خطوة موافقة على المجموعات التالية من المشاركين.</span><span class="sxs-lookup"><span data-stu-id="9202d-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="9202d-144">مجموعة المستخدمين</span><span class="sxs-lookup"><span data-stu-id="9202d-144">User group</span></span> | <span data-ttu-id="9202d-145">الوصف</span><span class="sxs-lookup"><span data-stu-id="9202d-145">Description</span></span> |
|---|---|
| <span data-ttu-id="9202d-146">المشارك</span><span class="sxs-lookup"><span data-stu-id="9202d-146">Participant</span></span> | <span data-ttu-id="9202d-147">قم بتعيين خطوة موافقة لأعضاء في مجموعة أو دور.</span><span class="sxs-lookup"><span data-stu-id="9202d-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="9202d-148">التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="9202d-148">Hierarchy</span></span> | <span data-ttu-id="9202d-149">قم بتعيين خطوة الموافقة لمستخدمين في تسلسل هرمي مؤسسي معين.</span><span class="sxs-lookup"><span data-stu-id="9202d-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="9202d-150">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="9202d-150">Workflow user</span></span> | <span data-ttu-id="9202d-151">قم بتعيين خطوة الموافقة لمستخدمي سير العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="9202d-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="9202d-152">قائمة الانتظار</span><span class="sxs-lookup"><span data-stu-id="9202d-152">Queue</span></span> | <span data-ttu-id="9202d-153">قم بتعيين خطوة الموافقة إلى قائمة انتظار عناصر عمل.</span><span class="sxs-lookup"><span data-stu-id="9202d-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="9202d-154">المستخدم</span><span class="sxs-lookup"><span data-stu-id="9202d-154">User</span></span> | <span data-ttu-id="9202d-155">قم بتعيين خطوة الاعتماد لمستخدمين معينين.</span><span class="sxs-lookup"><span data-stu-id="9202d-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9202d-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9202d-156">Additional resources</span></span>

- [<span data-ttu-id="9202d-157">تعريف مهام سير عمل العمليات التجارية لطلبات الشراء</span><span class="sxs-lookup"><span data-stu-id="9202d-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="9202d-158">سير عمل طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="9202d-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="9202d-159">إعداد المورّدين</span><span class="sxs-lookup"><span data-stu-id="9202d-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]