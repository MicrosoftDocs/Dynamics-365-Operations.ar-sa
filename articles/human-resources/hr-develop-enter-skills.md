---
title: إدخال المهارات
description: يمكن للعمال والمديرين إدخال المهارات في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193967"
---
# <a name="enter-skills"></a><span data-ttu-id="b38de-103">إدخال المهارات</span><span class="sxs-lookup"><span data-stu-id="b38de-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b38de-104">يمكنك إدخال المهارات المستهدفة أو المهارات الفعلية للعمال أو مقدمي الطلبات أو جهات الاتصال في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b38de-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b38de-105">المهارة المستهدفة هي المهارة التي يخطط الشخص لتحقيقها.</span><span class="sxs-lookup"><span data-stu-id="b38de-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="b38de-106">المهارة الفعلية هي مهارات لدى الشخص حاليًا.</span><span class="sxs-lookup"><span data-stu-id="b38de-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="b38de-107">إنشاء سير عمل لاعتماد المهارات تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="b38de-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="b38de-108">لإدخال المهارات دون الحاجة إلى اعتماد، يجب إنشاء سير عمل لاعتماد المهارات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b38de-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="b38de-109">تتطلب المهارات التي تم إدخالها بواسطة العاملين اعتماد المدير دائمًا.</span><span class="sxs-lookup"><span data-stu-id="b38de-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="b38de-110">يقوم سير العمل هذا بالاعتماد التلقائي على المهارات التي يتم إدخالها بواسطة المديرين نيابةً عن العمال.</span><span class="sxs-lookup"><span data-stu-id="b38de-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="b38de-111">في مساحة عمل **إدارة العاملين**، حدد **ارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="b38de-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b38de-112">ضمن **الإعداد**، حدد **سير عمل الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="b38de-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="b38de-113">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b38de-113">Select **New**.</span></span>

4. <span data-ttu-id="b38de-114">في الجزء **إنشاء سير عمل**، حدد **مهارات العامل**.</span><span class="sxs-lookup"><span data-stu-id="b38de-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="b38de-115">[![تحديد سير عمل مهارات العامل](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="b38de-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="b38de-116">في مربع الخوار **هل تريد فتح هذا الملف؟**، حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="b38de-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="b38de-117">عند المطالبة، أدخل بيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="b38de-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="b38de-118">في محرر سير العمل، حدد عنصر سير العمل **اعتماد المهارات** واسحبه إلى اللوحة.</span><span class="sxs-lookup"><span data-stu-id="b38de-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="b38de-119">[![تحديد عنصر سير عمل مهارات الاعتماد](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="b38de-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="b38de-120">قم بتوصيل العنصر **البدء** لعنصر **اعتماد المهارات**، ثم قم بتوصيل العنصر **اعتماد المهارات** بالعنصر **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="b38de-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="b38de-121">قد تحتاج إلى التمرير لأسفل لرؤية العنصر **النهاية**.</span><span class="sxs-lookup"><span data-stu-id="b38de-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="b38de-122">يمكنك سحبه بالقرب من العناصر الأخرى.</span><span class="sxs-lookup"><span data-stu-id="b38de-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="b38de-123">[![توصيل عناصر سير العمل](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="b38de-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="b38de-124">انقر نقرًا مزدوجًا فوق عنصر سير العمل **اعتماد المهارات 1**، ثم انقر بزر الماوس الأيمن فوق العنصر **الخطوة 1**.</span><span class="sxs-lookup"><span data-stu-id="b38de-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="b38de-125">انقر بزر الماوس الأيمن فوق العنصر **الخطوة 1**، ثم حدد **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="b38de-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="b38de-126">في النافذة **الخصائص**، حدد **شرط** من شريط التنقل الموجود على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="b38de-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="b38de-127">حدد **تشغيل هذه الخطوة فقط عند الوفاء بالشرط التالي**.</span><span class="sxs-lookup"><span data-stu-id="b38de-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="b38de-128">حدد **إضافة الشرط**.</span><span class="sxs-lookup"><span data-stu-id="b38de-128">Select **Add condition**.</span></span> <span data-ttu-id="b38de-129">بعد **المكان**، حدد **مهارات خدمة الموظف الذاتية**، ثم حدد **خدمة الموظف الذاتيةskills.Person**.</span><span class="sxs-lookup"><span data-stu-id="b38de-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="b38de-130">بعد **يكون**، حدد **الحقل**، ثم حدد **المستخدم إلى الشخص relationship.Person**.</span><span class="sxs-lookup"><span data-stu-id="b38de-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="b38de-131">[![تحديد شرط](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="b38de-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="b38de-132">حدد **مهمة** في شريط التنقل بالجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="b38de-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="b38de-133">في علامة التبويب **نوع المهمة**، حدد **التدرج الهرمي**.</span><span class="sxs-lookup"><span data-stu-id="b38de-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="b38de-134">في علامة التبويب **تحديد التدرج الهرمي**، في الحقل **نوع التدرج الهرمي:**، حدد **التدرج الهرمي الإداري**.</span><span class="sxs-lookup"><span data-stu-id="b38de-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="b38de-135">[![تحديد التدرج الهرمي الإداري](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="b38de-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="b38de-136">حدد **إغلاق**، حدد **سير العمل** في مسار تنقل اللوحة، ثم حدد **حفظ وإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="b38de-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="b38de-137">لمزيد من المعلومات حول إنشاء مهام سير العمل، راجع [نظرة عامة حول نظام سير العمل](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json)</span><span class="sxs-lookup"><span data-stu-id="b38de-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="b38de-138">إدخال مهارات لعامل</span><span class="sxs-lookup"><span data-stu-id="b38de-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="b38de-139">حدد عاملاً.</span><span class="sxs-lookup"><span data-stu-id="b38de-139">Select a worker.</span></span>

2. <span data-ttu-id="b38de-140">في شريط الإجراءات الخاص بالصفحة **العامل**، حدد **شخص**، ثم حدد **المهارات**.</span><span class="sxs-lookup"><span data-stu-id="b38de-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="b38de-141">في الصفحة **المهارات**، أكمل الحقول التالية لكل مهارة:</span><span class="sxs-lookup"><span data-stu-id="b38de-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="b38de-142">**المهارة**: حدد مهارة.</span><span class="sxs-lookup"><span data-stu-id="b38de-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="b38de-143">**نوع المستوى**: حدد **فعلي** للمهارة التي يمتلكها العامل، أو حدد **هدف** للمهارة التي يحاول العامل اكتسابها.</span><span class="sxs-lookup"><span data-stu-id="b38de-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="b38de-144">**المستوى**: حدد مستوى لمهارة العامل.</span><span class="sxs-lookup"><span data-stu-id="b38de-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="b38de-145">**تاريخ المستوى**: حدد تاريخًا في أداة التقويم.</span><span class="sxs-lookup"><span data-stu-id="b38de-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="b38de-146">**مسؤول اختبار**: إذا كانت ذلك مناسبًا، حدد مسؤول اختبار من القائمة.</span><span class="sxs-lookup"><span data-stu-id="b38de-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="b38de-147">يمكنك تصفية البحث الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b38de-147">You can filter your search.</span></span>
   - <span data-ttu-id="b38de-148">**سنوات الخبرة**: أدخل سنوات الخبرة.</span><span class="sxs-lookup"><span data-stu-id="b38de-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="b38de-149">**تم التحقق من الصحة**: إذا تم التحقق من صحة المهارة، حدد المربع.</span><span class="sxs-lookup"><span data-stu-id="b38de-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="b38de-150">**تم التحقق بواسطة**: أدخل اسم أداة التحقق.</span><span class="sxs-lookup"><span data-stu-id="b38de-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="b38de-151">عند الانتهاء من إدخال المهارات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b38de-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b38de-152">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b38de-152">See also</span></span>

[<span data-ttu-id="b38de-153">تكوين المهارات</span><span class="sxs-lookup"><span data-stu-id="b38de-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="b38de-154">تعيين المهارات</span><span class="sxs-lookup"><span data-stu-id="b38de-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]