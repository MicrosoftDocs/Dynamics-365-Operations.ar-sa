---
title: إنشاء سير عمل طلب شراء إجازة وبيعها
description: إنشاء سير عمل لطلب شراء إجازة وبيعها لإدارة طلبات شراء وبيع الإجازة بشكل مستمر في Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ec21cda4779fea8c28b73d25842219da900da9d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271463"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="6d0e0-103">إنشاء سير عمل طلب شراء إجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6d0e0-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6d0e0-104">يمكنك إنشاء سير عمل في Dynamics 365 Human Resources لإدارة طلبات شراء وبيع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="6d0e0-105">يتيح لك سير عمل **شراء وبيع الإجازة** ما يلي:</span><span class="sxs-lookup"><span data-stu-id="6d0e0-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="6d0e0-106">تعريف المهام</span><span class="sxs-lookup"><span data-stu-id="6d0e0-106">Define tasks</span></span>
- <span data-ttu-id="6d0e0-107">تحديد من يجب أن يقوم بإكمال المهام</span><span class="sxs-lookup"><span data-stu-id="6d0e0-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="6d0e0-108">تحديد من يمكنه الموافقة على الطلبات أو رفضها</span><span class="sxs-lookup"><span data-stu-id="6d0e0-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="6d0e0-109">إنشاء سير عمل طلب شراء إجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6d0e0-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="6d0e0-110">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6d0e0-111">ضمن **الإعداد**، حدد **سير عمل الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="6d0e0-112">حدد **جديد** ، ثم حدد **شراء وبيع طلب إجازة**.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="6d0e0-113">عند ظهور مربع الرسالة **هل تريد فتح هذا الملف؟**، حدد **فتح** وتسجيل الدخول باستخدام بيانات اعتماد الشركة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="6d0e0-114">استخدم محرر سير العمل لإنشاء سير عمل لطلبات الإجازة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="6d0e0-115">لمزيد من المعلومات حول العمل مع مهام سير العمل، راجع [إنشاء نظرة عامة حول مهام سير العمل](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="6d0e0-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="6d0e0-116">عناصر بيانات سير عمل طلب إجازة وغياب</span><span class="sxs-lookup"><span data-stu-id="6d0e0-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="6d0e0-117">يمكنك استخدام عناصر البيانات التالية لإنشاء الموافقات الشرطية أو التلقائية في عمليات سير العمل لطلبات بيع وشراء الإجازة:</span><span class="sxs-lookup"><span data-stu-id="6d0e0-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="6d0e0-118">**المبلغ**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-118">**Amount**</span></span>
- <span data-ttu-id="6d0e0-119">**سياسة شراء الإجازة وبيعها**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="6d0e0-120">**الشركة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-120">**Company**</span></span>
- <span data-ttu-id="6d0e0-121">**تم الإنشاء بواسطة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-121">**Created by**</span></span>
- <span data-ttu-id="6d0e0-122">**تاريخ  ووقت الإنشاء**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-122">**Created date and time**</span></span>
- <span data-ttu-id="6d0e0-123">**تاريخ الانتهاء**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-123">**End date**</span></span>
- <span data-ttu-id="6d0e0-124">**نوع الإجازة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-124">**Leave type**</span></span>
- <span data-ttu-id="6d0e0-125">**تعديل بواسطة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-125">**Modified by**</span></span>
- <span data-ttu-id="6d0e0-126">**تاريخ ووقت التعديل**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-126">**Modified date and time**</span></span>
- <span data-ttu-id="6d0e0-127">**معرف الطلب**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-127">**Request ID**</span></span>
- <span data-ttu-id="6d0e0-128">**تاريخ البدء**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-128">**Start date**</span></span>
- <span data-ttu-id="6d0e0-129">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-129">**Status**</span></span> 
- <span data-ttu-id="6d0e0-130">**تاريخ الإرسال**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-130">**Submission date**</span></span>
- <span data-ttu-id="6d0e0-131">**مُرسل بواسطة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-131">**Submitted by**</span></span>
- <span data-ttu-id="6d0e0-132">**مرسل بواسطة الموارد البشرية**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="6d0e0-133">**مرسل بواسطة المدير**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="6d0e0-134">**تم الإرسال بالنيابة**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="6d0e0-135">**العامل**</span><span class="sxs-lookup"><span data-stu-id="6d0e0-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="6d0e0-136">أمثلة سير العمل</span><span class="sxs-lookup"><span data-stu-id="6d0e0-136">Workflow examples</span></span>

<span data-ttu-id="6d0e0-137">تظهر هذه الأمثله كيف يمكنك إنشاء أنواع مختلفة من شروط سير العمل باستخدام عناصر البيانات هذه:</span><span class="sxs-lookup"><span data-stu-id="6d0e0-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="6d0e0-138">استخدم **مرسل بواسطة الموارد البشرية‬‏‫** و **مرسل بواسطة المدير‬‏‫** في إجراء تلقائي للموافقة تلقائيا علي طلبات شراء وبيع الإجازة التي تُرسلها هذه الأدوار نيابة عن الموظفين.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="6d0e0-139">لمزيد من المعلومات حول الإجراءات التلقائية، راجع [‏‫‏‫تكوين عمليات الاعتماد في سير عمل‬](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="6d0e0-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="6d0e0-140">استخدم **نوع الإجازة** في عبارة شرطية أو إجراء تلقائي للتحكم في كيفيه قيام سير العمل بتوجيه الطلبات بأنواع إجازة معينة.</span><span class="sxs-lookup"><span data-stu-id="6d0e0-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d0e0-141">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="6d0e0-141">See also</span></span>

[<span data-ttu-id="6d0e0-142">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="6d0e0-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="6d0e0-143">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6d0e0-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[<span data-ttu-id="6d0e0-144">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="6d0e0-144">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
