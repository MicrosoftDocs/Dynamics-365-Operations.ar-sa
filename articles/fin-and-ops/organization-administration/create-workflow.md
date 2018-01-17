---
title: "إنشاء سير عمل"
description: "يوضح هذا الموضوع كيفية إنشاء سير عمل."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: e7136c2e13b0e4fd3315e91f281174bdd8a45cb0
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="create-a-workflow"></a><span data-ttu-id="a7369-103">إنشاء سير عمل</span><span class="sxs-lookup"><span data-stu-id="a7369-103">Create a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7369-104">يوضح هذا الموضوع كيفية إنشاء سير عمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-104">This topic explains how to create a workflow.</span></span>

<a name="open-the-workflow-editor"></a><span data-ttu-id="a7369-105">فتح محرر سير العمل</span><span class="sxs-lookup"><span data-stu-id="a7369-105">Open the workflow editor</span></span>
------------------------

<span data-ttu-id="a7369-106">تحدد وحدة Microsoft Dynamics 365 for Finance and Operations النمطية التي تعمل فيها أنواع سير العمل التي يمكنك إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="a7369-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="a7369-107">اتبع الخطوات التالية لتحديد نوع سير العمل لإنشاء محرر سير العمل وفتحه.</span><span class="sxs-lookup"><span data-stu-id="a7369-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1.  <span data-ttu-id="a7369-108">افتح الوحدة النمطية التي تريد إنشاء سير عمل جديد لها.</span><span class="sxs-lookup"><span data-stu-id="a7369-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="a7369-109">على سبيل المثال، لإنشاء سير عمل لطلبات الشراء، انقر فوق **التدبير وتحديد الموارد**.</span><span class="sxs-lookup"><span data-stu-id="a7369-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2.  <span data-ttu-id="a7369-110">انقر فوق **الإعداد** &gt; **\[اسم الوحدة النمطية\] مهام سير عمل**.</span><span class="sxs-lookup"><span data-stu-id="a7369-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3.  <span data-ttu-id="a7369-111">في صفحة القائمة التي تظهر، في جزء الإجراءات، انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a7369-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4.  <span data-ttu-id="a7369-112">في صفحة **إنشاء سير عمل**، حدد نوع سير العمل الذي ترغب في إنشائه، ثم انقر فوق **إنشاء سير عمل**.</span><span class="sxs-lookup"><span data-stu-id="a7369-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="a7369-113">يظهر محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-113">The workflow editor appears.</span></span> <span data-ttu-id="a7369-114">يمكنك الآن استخدام الإجراءات التالية لتصميم سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="a7369-115">سحب عناصر سير العمل فوق اللوحة القماشية</span><span class="sxs-lookup"><span data-stu-id="a7369-115">Drag workflow elements onto the canvas</span></span>
<span data-ttu-id="a7369-116">تتضمن منطقة **عناصر سير العمل** في محرر سير العمل العناصر التي يمكنك إضافتها إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="a7369-117">لإضافة عناصر إلى سير العمل، اسحبها إلى لوحة الرسم.</span><span class="sxs-lookup"><span data-stu-id="a7369-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="a7369-118">ربط العناصر</span><span class="sxs-lookup"><span data-stu-id="a7369-118">Connect the elements</span></span>
<span data-ttu-id="a7369-119">لربط بين عنصر واحد من عناصر سير العمل وبين عنصر آخر، اضغط باستمرار على المؤشر فوق العنصر إلى أن تظهر نقاط الربط.</span><span class="sxs-lookup"><span data-stu-id="a7369-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="a7369-120">انقر فوق نقطة اتصال، واسحبها إلى عنصر آخر.</span><span class="sxs-lookup"><span data-stu-id="a7369-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="a7369-121">وتأكد من ربط جميع العناصر.</span><span class="sxs-lookup"><span data-stu-id="a7369-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="a7369-122">تكوين خصائص سير العمل</span><span class="sxs-lookup"><span data-stu-id="a7369-122">Configure the properties of the workflow</span></span>
<span data-ttu-id="a7369-123">اتبع الخطوات التالية لتكوين خصائص سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-123">Follow these steps to configure the properties of the workflow.</span></span>

1.  <span data-ttu-id="a7369-124">انقر فوق اللوحة القماشية للتأكد من عدم تحديد أي عنصر سير عمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2.  <span data-ttu-id="a7369-125">انقر فوق **خصائص** لفتح الصفحة **خصائص** لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3.  <span data-ttu-id="a7369-126">اتبع الإجراءات المذكورة في الموضوع [تكوين خصائص سير العمل](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a7369-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="a7369-127">تكوين عناصر سير العمل</span><span class="sxs-lookup"><span data-stu-id="a7369-127">Configure the elements of the workflow</span></span>
<span data-ttu-id="a7369-128">قم بتكوين كل عنصر قمت بسحبه إلى اللوحة القماشية.</span><span class="sxs-lookup"><span data-stu-id="a7369-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="a7369-129">لمزيد من المعلومات حول كيفية تكوين كل عنصر سير عمل، راجع المواضيع التالية:</span><span class="sxs-lookup"><span data-stu-id="a7369-129">For information about how to configure each workflow element, see the following topics:</span></span>

-   [<span data-ttu-id="a7369-130">تكوين مهمة يدوية</span><span class="sxs-lookup"><span data-stu-id="a7369-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
-   [<span data-ttu-id="a7369-131">تكوين مهمة تلقائية</span><span class="sxs-lookup"><span data-stu-id="a7369-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
-   [<span data-ttu-id="a7369-132">تكوين عملية اعتماد</span><span class="sxs-lookup"><span data-stu-id="a7369-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
-   [<span data-ttu-id="a7369-133">تكوين خطوة اعتماد</span><span class="sxs-lookup"><span data-stu-id="a7369-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
-   [<span data-ttu-id="a7369-134">تكوين قرار يدوي</span><span class="sxs-lookup"><span data-stu-id="a7369-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
-   [<span data-ttu-id="a7369-135">تكوين قرار شرطي</span><span class="sxs-lookup"><span data-stu-id="a7369-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
-   [<span data-ttu-id="a7369-136">تكوين نشاط موازٍ</span><span class="sxs-lookup"><span data-stu-id="a7369-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
-   [<span data-ttu-id="a7369-137">تكوين فرع موازٍ</span><span class="sxs-lookup"><span data-stu-id="a7369-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
-   [<span data-ttu-id="a7369-138">تكوين سير عمل لعنصر بند</span><span class="sxs-lookup"><span data-stu-id="a7369-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="a7369-139">حل أية أخطاء أو تحذيرات</span><span class="sxs-lookup"><span data-stu-id="a7369-139">Resolve any errors or warnings</span></span>
<span data-ttu-id="a7369-140">يعرض جزء **الأخطاء والتحذيرات** في الجزء السفلي من محرر سير العمل الرسائل التي تم إنشاؤها لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="a7369-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="a7369-141">لتحديد العنصر حيث حدث خطأ أو تحذير ما، انقر نقرا مزدوجًا فوق رسالة الخطأ أو التحذير.</span><span class="sxs-lookup"><span data-stu-id="a7369-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="a7369-142">يجب حل كل الأخطاء والتحذيرات قبل جعل سير العمل نشطًا.</span><span class="sxs-lookup"><span data-stu-id="a7369-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="a7369-143">حفظ سير العمل وتنشيطه</span><span class="sxs-lookup"><span data-stu-id="a7369-143">Save and activate the workflow</span></span>
<span data-ttu-id="a7369-144">عندما تصبح جاهزًا لحفظ سير العمل وتنشيطه، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a7369-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="a7369-145">انقر فوق **حفظ وإغلاق** لإغلاق محرر سير العمل وفتح الصفحة **حفظ سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="a7369-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2.  <span data-ttu-id="a7369-146">أدخل تعليقات على التغييرات التي أدخلتها على سير العمل، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a7369-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3.  <span data-ttu-id="a7369-147">إذا تم حل جميع الأخطاء والتحذيرات، فستظهر صفحة **تنشيط سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="a7369-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="a7369-148">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="a7369-148">Select one of the following options:</span></span>
    -   <span data-ttu-id="a7369-149">لتنشيط هذا الإصدار من سير العمل، انقر فوق **تنشيط الإصدار الجديد**.</span><span class="sxs-lookup"><span data-stu-id="a7369-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="a7369-150">عندما يكون سير عمل ما نشطًا، يمكن للمستخدمين إرسال المستندات إليه للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="a7369-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    -   <span data-ttu-id="a7369-151">إذا لم ترغب في تنشيط هذا الإصدار، فانقر فوق **عدم تنشيط الإصدار الجديد‬**.</span><span class="sxs-lookup"><span data-stu-id="a7369-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="a7369-152">يمكنك تنشيط سير العمل في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="a7369-152">You can activate the workflow later.</span></span>






