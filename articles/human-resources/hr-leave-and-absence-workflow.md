---
title: إنشاء سير عمل طلب إجازة
description: إنشاء سير عمل لطلب أجازه وغياب لأداره طلبات الإجازات بشكل مستمر في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428675"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="2291e-103">إنشاء سير عمل طلب إجازة</span><span class="sxs-lookup"><span data-stu-id="2291e-103">Create a leave request workflow</span></span>

<span data-ttu-id="2291e-104">يمكنك إنشاء سير عمل في Dynamics 365 Human Resources لإدارة طلبات الإجازة والغياب بشكل مستمر.</span><span class="sxs-lookup"><span data-stu-id="2291e-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="2291e-105">يتيح لك سير عمل **الإجازة والغياب** ما يلي:</span><span class="sxs-lookup"><span data-stu-id="2291e-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="2291e-106">تعريف المهام</span><span class="sxs-lookup"><span data-stu-id="2291e-106">Define tasks</span></span>
- <span data-ttu-id="2291e-107">تحديد من يجب أن يقوم بإكمال المهام</span><span class="sxs-lookup"><span data-stu-id="2291e-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="2291e-108">تحديد من يمكنه الموافقة على الطلبات أو رفضها</span><span class="sxs-lookup"><span data-stu-id="2291e-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="2291e-109">إنشاء سير عمل طلب إجازة وغياب</span><span class="sxs-lookup"><span data-stu-id="2291e-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="2291e-110">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="2291e-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2291e-111">ضمن **الإعداد**، حدد **سير عمل الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="2291e-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="2291e-112">حدد **جديد‬**، ثم حدد **طلب الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="2291e-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="2291e-113">عند ظهور مربع الرسالة **هل تريد فتح هذا الملف؟**، حدد **فتح** وتسجيل الدخول باستخدام بيانات اعتماد الشركة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2291e-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="2291e-114">استخدم محرر سير العمل لإنشاء سير عمل لطلبات الإجازة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2291e-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="2291e-115">لمزيد من المعلومات حول العمل مع مهام سير العمل، راجع [إنشاء نظرة عامة حول مهام سير العمل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="2291e-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="2291e-116">عناصر بيانات سير عمل طلب إجازة وغياب</span><span class="sxs-lookup"><span data-stu-id="2291e-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="2291e-117">يمكنك استخدام عناصر البيانات التالية لإنشاء الموافقات الشرطية أو التلقائية في عمليات سير العمل لطلبات الإجازة والغياب:</span><span class="sxs-lookup"><span data-stu-id="2291e-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="2291e-118">**المبلغ**</span><span class="sxs-lookup"><span data-stu-id="2291e-118">**Amount**</span></span>
- <span data-ttu-id="2291e-119">**تعليق**</span><span class="sxs-lookup"><span data-stu-id="2291e-119">**Comment**</span></span>
- <span data-ttu-id="2291e-120">**الشركة**</span><span class="sxs-lookup"><span data-stu-id="2291e-120">**Company**</span></span>
- <span data-ttu-id="2291e-121">**تم الإنشاء بواسطة**</span><span class="sxs-lookup"><span data-stu-id="2291e-121">**Created by**</span></span>
- <span data-ttu-id="2291e-122">**تاريخ  ووقت الإنشاء**</span><span class="sxs-lookup"><span data-stu-id="2291e-122">**Created date and time**</span></span>
- <span data-ttu-id="2291e-123">**تاريخ الإنهاء**</span><span class="sxs-lookup"><span data-stu-id="2291e-123">**End date**</span></span>
- <span data-ttu-id="2291e-124">**نوع الإجازة**</span><span class="sxs-lookup"><span data-stu-id="2291e-124">**Leave type**</span></span>
- <span data-ttu-id="2291e-125">**تعديل بواسطة**</span><span class="sxs-lookup"><span data-stu-id="2291e-125">**Modified by**</span></span>
- <span data-ttu-id="2291e-126">**تاريخ ووقت التعديل**</span><span class="sxs-lookup"><span data-stu-id="2291e-126">**Modified date and time**</span></span>
- <span data-ttu-id="2291e-127">**رمز السبب**</span><span class="sxs-lookup"><span data-stu-id="2291e-127">**Reason code**</span></span>
- <span data-ttu-id="2291e-128">**معرف الطلب**</span><span class="sxs-lookup"><span data-stu-id="2291e-128">**Request ID**</span></span>
- <span data-ttu-id="2291e-129">**تاريخ البدء**</span><span class="sxs-lookup"><span data-stu-id="2291e-129">**Start date**</span></span>
- <span data-ttu-id="2291e-130">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="2291e-130">**Status**</span></span> 
- <span data-ttu-id="2291e-131">**تاريخ الإرسال**</span><span class="sxs-lookup"><span data-stu-id="2291e-131">**Submission date**</span></span>
- <span data-ttu-id="2291e-132">**مُرسل بواسطة**</span><span class="sxs-lookup"><span data-stu-id="2291e-132">**Submitted by**</span></span>
- <span data-ttu-id="2291e-133">**مرسل بواسطة الموارد البشرية**</span><span class="sxs-lookup"><span data-stu-id="2291e-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="2291e-134">**مرسل بواسطة المدير**</span><span class="sxs-lookup"><span data-stu-id="2291e-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="2291e-135">**تم الإرسال بالنيابة**</span><span class="sxs-lookup"><span data-stu-id="2291e-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="2291e-136">**العامل**</span><span class="sxs-lookup"><span data-stu-id="2291e-136">**Worker**</span></span>
- <span data-ttu-id="2291e-137">**نوع العامل**</span><span class="sxs-lookup"><span data-stu-id="2291e-137">**Worker type**</span></span>

<span data-ttu-id="2291e-138">تظهر هذه الأمثله كيف يمكنك إنشاء أنواع مختلفة من شروط سير العمل باستخدام عناصر البيانات هذه:</span><span class="sxs-lookup"><span data-stu-id="2291e-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="2291e-139">استخدم **كود السبب** في العبارة الشرطية لتوجيه طلبات الإجازات المرضية مع كود السبب **جراحة** إلى الموارد البشرية للموافقة، بينما يتم توجيه كافة أكواد الأسباب الأخرى إلى المدير.</span><span class="sxs-lookup"><span data-stu-id="2291e-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="2291e-140">لمزيد من المعلومات حول العبارات الشرطية، راجع [‏‫تكوين القرارات الشرطية في سير عمل‬‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="2291e-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="2291e-141">استخدم **مرسل بواسطة الموارد البشرية‬‏‫** و **مرسل بواسطة المدير‬‏‫** في إجراء تلقائي للموافقة تلقائيا علي طلبات الإجازات التي تُرسلها هذه الأدوار نيابة عن الموظفين.</span><span class="sxs-lookup"><span data-stu-id="2291e-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="2291e-142">لمزيد من المعلومات حول الإجراءات التلقائية، راجع [‏‫‏‫تكوين عمليات الاعتماد في سير عمل‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="2291e-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="2291e-143">استخدم **نوع الإجازة** في عبارة شرطية أو إجراء تلقائي للتحكم في كيفيه قيام سير العمل بتوجيه الطلبات بأنواع إجازة معينة.</span><span class="sxs-lookup"><span data-stu-id="2291e-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="2291e-144">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="2291e-144">See also</span></span>

- [<span data-ttu-id="2291e-145">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="2291e-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
