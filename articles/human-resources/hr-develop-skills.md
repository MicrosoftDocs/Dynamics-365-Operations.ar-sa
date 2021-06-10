---
title: تكوين المهارات
description: يمكنك تعقب مهارات العامل في Dynamics 365 Human Resources. يمكنك أيضًا تحديد المهارات المطلوبة لمهمة معينة.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076549"
---
# <a name="configure-skills"></a><span data-ttu-id="17829-104">تكوين المهارات</span><span class="sxs-lookup"><span data-stu-id="17829-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="17829-105">يمكنك تعقب مهارات العامل في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="17829-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="17829-106">يمكنك أيضًا تحديد المهارات المطلوبة لمهمة معينة.</span><span class="sxs-lookup"><span data-stu-id="17829-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="17829-107">تتضمن أمثلة المهارات التي يمكنك تعقبها:</span><span class="sxs-lookup"><span data-stu-id="17829-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="17829-108">الإشراف - القدرة على الإشراف على عمل الآخرين.</span><span class="sxs-lookup"><span data-stu-id="17829-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="17829-109">القيادة - القدرة على قيادة الموظفين ومجالات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="17829-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="17829-110">التخطيط – القدرة على التطلع للمستقبل، لتشكيل عبارات الرؤى وإدراك ما وراء هذه الرؤى.</span><span class="sxs-lookup"><span data-stu-id="17829-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="17829-111">HTML – القدرة على كتابة التعليمات البرمجية لـ HTML.</span><span class="sxs-lookup"><span data-stu-id="17829-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="17829-112">إذا لم تقم بالفعل بإعداد أنواع المهارات ونماذج التصنيف، ستحتاج إلى إضافة بعضها قبل إنشاء المهارات.</span><span class="sxs-lookup"><span data-stu-id="17829-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="17829-113">يمكن للأشخاص التاليين إدخال مهارات لعامل:</span><span class="sxs-lookup"><span data-stu-id="17829-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="17829-114">يمكن للعاملين إدخال المهارات لأنفسهم في خدمة الموظف الذاتية.</span><span class="sxs-lookup"><span data-stu-id="17829-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="17829-115">تتطلب هذه المهارات اعتماد المدير.</span><span class="sxs-lookup"><span data-stu-id="17829-115">These skills require manager approval.</span></span>
- <span data-ttu-id="17829-116">يمكن للمديرين إدخال مهارات للعاملين.</span><span class="sxs-lookup"><span data-stu-id="17829-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="17829-117">يمكنك إنشاء سير عمل يعتمد هذه المهارات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="17829-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="17829-118">إنشاء نوع مهارة</span><span class="sxs-lookup"><span data-stu-id="17829-118">Create a skill type</span></span>

<span data-ttu-id="17829-119">أنواع المهارات هي فئات تقع ضمنها مهارات فردية، مثل الإدارة أو المبيعات.</span><span class="sxs-lookup"><span data-stu-id="17829-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="17829-120">في مساحة العمل **تطوير الموظفين**، حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="17829-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="17829-121">ضمن **إعداد الاختصاص**، حدد **أنواع المهارات**.</span><span class="sxs-lookup"><span data-stu-id="17829-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="17829-122">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="17829-122">Select **New**.</span></span>

4. <span data-ttu-id="17829-123">أكمل الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="17829-123">Complete the following fields:</span></span>

   - <span data-ttu-id="17829-124">**نوع المهارة**، أدخل اسمًا لنوع المهارة.</span><span class="sxs-lookup"><span data-stu-id="17829-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="17829-125">**الوصف**، أدخل وصفًا لنوع المهارة.</span><span class="sxs-lookup"><span data-stu-id="17829-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="17829-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="17829-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="17829-127">إنشاء نموذج تقييم</span><span class="sxs-lookup"><span data-stu-id="17829-127">Create a rating model</span></span>

<span data-ttu-id="17829-128">تساعد أنظمة التقييم في تقييم مستوى المهارة الفعلي لشخص أو المستوى الذي يجب أن يصل إليه أو مستوى المهارة المطلوب لمهمة.</span><span class="sxs-lookup"><span data-stu-id="17829-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="17829-129">ويتم تعيين عامل لكل مستوى في نموذج التقييم.</span><span class="sxs-lookup"><span data-stu-id="17829-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="17829-130">في مساحة العمل **تطوير الموظفين**، حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="17829-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="17829-131">ضمن **إعداد الاختصاص**، حدد **نماذج التقييم**.</span><span class="sxs-lookup"><span data-stu-id="17829-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="17829-132">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="17829-132">Select **New**.</span></span>

4. <span data-ttu-id="17829-133">أكمل الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="17829-133">Complete the following fields:</span></span>

   - <span data-ttu-id="17829-134">**التقييم**: أدخل اسمًا لنموذج التقييم، مثل **المهارات**.</span><span class="sxs-lookup"><span data-stu-id="17829-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="17829-135">**الوصف**: أدخل وصفًا لنظام التقييم، مثل **تقييمات المهارات**.</span><span class="sxs-lookup"><span data-stu-id="17829-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="17829-136">في القسم **مستويات**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="17829-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="17829-137">بالنسبة لكل مستوى تريد إضافته، أكمل الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="17829-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="17829-138">**المستوى**: أدخل اسمًا للمستوى.</span><span class="sxs-lookup"><span data-stu-id="17829-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="17829-139">**الوصف**: أدخل وصفًا للمستوى.</span><span class="sxs-lookup"><span data-stu-id="17829-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="17829-140">**العامل**: أدخل قيمة عامل من 0 إلى 9.</span><span class="sxs-lookup"><span data-stu-id="17829-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="17829-141">تساعد العوامل في تسوية نتائج المهارات التي تستخدم نماذج تقييم مختلفة.</span><span class="sxs-lookup"><span data-stu-id="17829-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="17829-142">يجب أن يكون لكل مستوى عامل فريد.</span><span class="sxs-lookup"><span data-stu-id="17829-142">Each level must have a unique factor.</span></span> <span data-ttu-id="17829-143">تؤثر المستويات التي لها قيم عوامل أعلى بشكل أكبر في نموذج تقييم.</span><span class="sxs-lookup"><span data-stu-id="17829-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="17829-144">استمر في إضافة المستويات حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="17829-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="17829-145">يمكنك إدخال حتى 10 مستويات لكل نموذج تقييم.</span><span class="sxs-lookup"><span data-stu-id="17829-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="17829-146">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="17829-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="17829-147">إنشاء مهارة</span><span class="sxs-lookup"><span data-stu-id="17829-147">Create a skill</span></span>

<span data-ttu-id="17829-148">قبل أن تتمكن من تعيين مهارة لشخص ، أو القيام بإنشاء بحث تعيين مهارات أو ملف تعريف مهارات، فإنه يجب إدخال معلومات حول المهارات في صفحة **المهارات**.</span><span class="sxs-lookup"><span data-stu-id="17829-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="17829-149">لكل مهارة، يمكنك تحديد نوع مهارة ونظام تقييم.</span><span class="sxs-lookup"><span data-stu-id="17829-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="17829-150">في مساحة العمل **تطوير الموظفين**، حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="17829-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="17829-151">ضمن **إعداد الاختصاص**، حدد **المهارات**.</span><span class="sxs-lookup"><span data-stu-id="17829-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="17829-152">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="17829-152">Select **New**.</span></span>

4. <span data-ttu-id="17829-153">أكمل الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="17829-153">Complete the following fields:</span></span>

   - <span data-ttu-id="17829-154">**المهارة**، أدخل اسمًا للمهارة.</span><span class="sxs-lookup"><span data-stu-id="17829-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="17829-155">**الوصف**، أدخل وصفًا للمهارة.</span><span class="sxs-lookup"><span data-stu-id="17829-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="17829-156">**التقييم**: حدد نموذج التقييم الذي ترغب في استخدامه لهذه المهارة.</span><span class="sxs-lookup"><span data-stu-id="17829-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="17829-157">**نوع المهارة**: حدد من قائمة أنواع المهارات.</span><span class="sxs-lookup"><span data-stu-id="17829-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="17829-158">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="17829-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="17829-159">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="17829-159">See also</span></span>

[<span data-ttu-id="17829-160">إدخال المهارات</span><span class="sxs-lookup"><span data-stu-id="17829-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="17829-161">تعيين المهارات</span><span class="sxs-lookup"><span data-stu-id="17829-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]