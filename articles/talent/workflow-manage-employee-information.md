---
title: "استخدم عمليات سير العمل لإدارة معلومات الموظف"
description: "يشرح هذا الموضوع كيف يمكن استخدام إمكانات سير العمل للموارد البشرية لإدارة معلومات الموظف. على سبيل المثال، يمكنك إقران سير عمل مع موضع وتكوين سير عمل موافقة يتم تشغيله عندما يقوم الموظفون بتغيير سجلهم."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47c569f3531bf00795078b7b042bf899b51bad8d
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="fef26-104">استخدم عمليات سير العمل لإدارة معلومات الموظف</span><span class="sxs-lookup"><span data-stu-id="fef26-104">Use workflows to manage employee information</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="fef26-105">يشرح هذا الموضوع كيف يمكن استخدام إمكانات سير العمل للموارد البشرية لإدارة معلومات الموظف.</span><span class="sxs-lookup"><span data-stu-id="fef26-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="fef26-106">على سبيل المثال، يمكنك إقران سير عمل مع موضع وتكوين سير عمل موافقة يتم تشغيله عندما يقوم الموظفون بتغيير سجلهم.</span><span class="sxs-lookup"><span data-stu-id="fef26-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="fef26-107">توفر إمكانات سير العمل للموارد البشرية العديد من مهام سير العمل لإدارة أنشطة الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="fef26-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="fef26-108">بالإضافة إلى ذلك، تتوفر خيارات عديدة وبذلك يمكنك تعديل عمليات سير عمل معينة وإقرانها بالتدرج الهرمي للتقارير.</span><span class="sxs-lookup"><span data-stu-id="fef26-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="fef26-109">تتوفر عمليات سير العمل للمساعدة في إدارة التغييرات للعديد من الأنواع القياسية لمعلومات الموظف.</span><span class="sxs-lookup"><span data-stu-id="fef26-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="fef26-110">يمكنك إقران سير عمل بمنصب.</span><span class="sxs-lookup"><span data-stu-id="fef26-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="fef26-111">وبالتالي، إذا قام الموظفون بتغيير سجل الموظف الخاص بهم، يتم بدء تشغيل سير عمل يتطلب موافقة قبل حفظ المعلومات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="fef26-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="fef26-112">يتم تعريف عمليات سير العمل مسبقًا لأنواع المعلومات التالية لمساعدتك في إدارة التغييرات بكفاءة، والحفاظ على دقة بيانات موظفيك:</span><span class="sxs-lookup"><span data-stu-id="fef26-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="fef26-113">أرقام التعريف</span><span class="sxs-lookup"><span data-stu-id="fef26-113">Identification numbers</span></span>
-   <span data-ttu-id="fef26-114">الدورات التدريبية</span><span class="sxs-lookup"><span data-stu-id="fef26-114">Courses</span></span>
-   <span data-ttu-id="fef26-115">التعليم</span><span class="sxs-lookup"><span data-stu-id="fef26-115">Education</span></span>
-   <span data-ttu-id="fef26-116">صورة</span><span class="sxs-lookup"><span data-stu-id="fef26-116">Image</span></span>
-   <span data-ttu-id="fef26-117">الأصناف المقترضة</span><span class="sxs-lookup"><span data-stu-id="fef26-117">Loaned items</span></span>
-   <span data-ttu-id="fef26-118">الخبرة المهنية</span><span class="sxs-lookup"><span data-stu-id="fef26-118">Professional experience</span></span>
-   <span data-ttu-id="fef26-119">خبرة المشروع</span><span class="sxs-lookup"><span data-stu-id="fef26-119">Project experience</span></span>
-   <span data-ttu-id="fef26-120">المهارات</span><span class="sxs-lookup"><span data-stu-id="fef26-120">Skills</span></span>
-   <span data-ttu-id="fef26-121">مراكز الثقة</span><span class="sxs-lookup"><span data-stu-id="fef26-121">Positions of trust</span></span>
-   <span data-ttu-id="fef26-122">إجراءات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="fef26-122">Human resources actions</span></span>
-   <span data-ttu-id="fef26-123">تسجيل الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="fef26-123">Course registration</span></span>

<span data-ttu-id="fef26-124">عندما يتم توظيف الموظفين أو نقلهم أو إنهاء خدمتهم، يمكن لسير العمل تضمين عملية مراجعة.</span><span class="sxs-lookup"><span data-stu-id="fef26-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="fef26-125">وبهذه الطريقة، يمكن مراجعة مستند أو تحديد شروط إجراء كجزء من سير العمل.</span><span class="sxs-lookup"><span data-stu-id="fef26-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="fef26-126">عند الانتهاء من عملية المراجعة، يتم إكمال المستد أو الإجراء، وينتقل سير العمل إلى خطوة الموافقة النهائية.</span><span class="sxs-lookup"><span data-stu-id="fef26-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="fef26-127">إقران سير عمل بتدرج هرمي للمناصب</span><span class="sxs-lookup"><span data-stu-id="fef26-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="fef26-128">يمكنك إقران سير عمل بأي تدرج هرمي قمت بتكوينه.</span><span class="sxs-lookup"><span data-stu-id="fef26-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="fef26-129">على سبيل المثال، إذا تم إقران منصب بتدرج هرمي لتقارير مصفوفة، يمكنك تكوين سير عمل يقوم بتوجيه نفقات لمشروع محدد إلى رئيس المشروع بدلًا من مدير الموظف المقترن بهذا المنصب.</span><span class="sxs-lookup"><span data-stu-id="fef26-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="fef26-130">لإنشاء سير عمل جديد أو تعديل سير عمل موجود، على صفحة **عمليات سير العميل للموارد البشرية**، انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="fef26-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="fef26-131">حدد سير عمل في القائمة لبدء تشغيل مصمم سير العمل.</span><span class="sxs-lookup"><span data-stu-id="fef26-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="fef26-132">يمكنك استخدام المصمم لإنشاء سير عمل جديد أو تغيير الخطوات في سير عمل موجود.</span><span class="sxs-lookup"><span data-stu-id="fef26-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="fef26-133">عند تغيير سير عمل موجود، يتم حفظ تغييراتك كإصدار جديد.</span><span class="sxs-lookup"><span data-stu-id="fef26-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="fef26-134">ولذلك، يمكنك دائمًا العودة إلى إصدار سابق إذا اضطررت لذلك.</span><span class="sxs-lookup"><span data-stu-id="fef26-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="fef26-135">تكوين سير عمل الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="fef26-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="fef26-136">لتكوين سير عمل أساسي يتم تشغيله عندما يطلب موظفين تغيير لهويتهم الشخصية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="fef26-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="fef26-137">على صفحة **سير عمل الموارد البشرية**، انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="fef26-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="fef26-138">في قائمة مهام سير العمل المتاحة، حدد **أرقام التعريف**.</span><span class="sxs-lookup"><span data-stu-id="fef26-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="fef26-139">انقر فوق **تشغيل** لبدء تشغيل مصمم سير العمل، ثم أدخل اسم المستخدم وكلمة المرور الخاصة بك عندما تتم مطالبتك بها.</span><span class="sxs-lookup"><span data-stu-id="fef26-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="fef26-140">اسحب عنصر **اعتماد رقم التعريف** من قائمة عناصر سير العمل إلى اللوحة القماشية للمصمم.</span><span class="sxs-lookup"><span data-stu-id="fef26-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="fef26-141">الاتصال بعنصر الموافقة لـ **بدء** و **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="fef26-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="fef26-142">انقر نقراً مزدوجاً فوق **عنصر الموافقة**، ثم انقر بالزر الأيمن، وحدد **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="fef26-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="fef26-143">اتبع هذه الخطوات لإضافة إرشادات صنف العمل:</span><span class="sxs-lookup"><span data-stu-id="fef26-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="fef26-144">حدد **مهمة**، ثم قم بتحديد **التدرج الهرمي** تحت نوع المهمة.</span><span class="sxs-lookup"><span data-stu-id="fef26-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="fef26-145">تحت تحديد **التسلسل الهرمي**، حدد **التدرج الهرمي القابل للتكوين**.</span><span class="sxs-lookup"><span data-stu-id="fef26-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="fef26-146">إضافة حالة توقف، ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fef26-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="fef26-147">قم بإكمال أي إرشادات إضافية (لا يجب وجود تحذيرات إضافية).</span><span class="sxs-lookup"><span data-stu-id="fef26-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="fef26-148">انقر فوق **حفظ وإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="fef26-148">Click **Save and close**.</span></span> <span data-ttu-id="fef26-149">تنشيط سير العمل الجديد عند فتح مربع حوار، وحدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="fef26-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="fef26-150">الانتقال إلى **الموارد البشرية** &gt; **مناصب** &gt; **أنواع التدرجات الهرمية للمناصب**.</span><span class="sxs-lookup"><span data-stu-id="fef26-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="fef26-151">حدد **مصفوفة**.</span><span class="sxs-lookup"><span data-stu-id="fef26-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="fef26-152">إضافة سير عمل **رقم تعريف العامل** إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="fef26-152">Add the **Worker identification number** workflow to the list.</span></span>





