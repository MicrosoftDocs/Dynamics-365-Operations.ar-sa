---
title: تطوير بنية التعويض
description: تنقلك هذه المقالة عبر عملية إنشاء خطة تعويض ثابت وتسجيل الموظفين بالخطة من خلال قواعد الأهلية.
author: andreabichsel
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75d1a05d4f94689581e2a67a13adeef6b14ac0cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800893"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="1e074-103">تطوير بنية التعويض</span><span class="sxs-lookup"><span data-stu-id="1e074-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1e074-104">تنقلك هذه المقالة عبر عملية إنشاء خطة تعويض ثابت وتسجيل الموظفين بالخطة من خلال قواعد الأهلية.</span><span class="sxs-lookup"><span data-stu-id="1e074-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="1e074-105">تستخدم هذه المقالة بيانات العرض التوضيحي USMF ويتم تطبيقها على مدراء التعويضات والميزات.</span><span class="sxs-lookup"><span data-stu-id="1e074-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="1e074-106">إنشاء خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="1e074-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="1e074-107">حدد **إدارة التعويض**.</span><span class="sxs-lookup"><span data-stu-id="1e074-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="1e074-108">حدد **خطط التعويض الثابت**.</span><span class="sxs-lookup"><span data-stu-id="1e074-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="1e074-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1e074-109">Select **New**.</span></span>

4. <span data-ttu-id="1e074-110">في الحقل **خطة**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e074-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="1e074-111">في حقل **الوصف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e074-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="1e074-112">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="1e074-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="1e074-113">في الحقل **النوع**، حدد ما إذا كانت خطة التعويض الثابت عبارة عن خطة **نطاق** أو **درجة** أو **خطوة**.</span><span class="sxs-lookup"><span data-stu-id="1e074-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="1e074-114">تعمل خانة الاختيار **التوصيات المسموحة** بمثابة قيمة افتراضية لأي إجراءات تتم إضافتها إلى هذه الخطة في حدث عملية.</span><span class="sxs-lookup"><span data-stu-id="1e074-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="1e074-115">تمكّنك خانة الاختيار "التوصيات المسموحة" من تجاوز مبلغ الإرشاد المحسوب عند معالجة التعويض.</span><span class="sxs-lookup"><span data-stu-id="1e074-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="1e074-116">يسمح لك **التفاوت الخارج عن النطاق** بتحديد كيفية التعامل مع مبالغ التعويض التي تقع خارج نطاق بنية التعويض المحددة للمستوى المعين.</span><span class="sxs-lookup"><span data-stu-id="1e074-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="1e074-117">يتيح لك تعيين الحقل **‏‫التفاوت الخارج عن النطاق‬** إلى **لا شيء** لاستخدام أي مبلغ تعويض.</span><span class="sxs-lookup"><span data-stu-id="1e074-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="1e074-118">سيقوم **التفاوت الناعم** بتحذير المستخدم إذا كان مبلغ التعويض أقل من الحد الأدنى أو أكبر الحد الأقصى لمبالغ النقطة المرجعية لهذا المستوى.</span><span class="sxs-lookup"><span data-stu-id="1e074-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="1e074-119">يمكن للمستخدمين تجاهل التحذير والمتابعة.</span><span class="sxs-lookup"><span data-stu-id="1e074-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="1e074-120">سيؤدي **التفاوت الثابت** إلى توليد رسالة خطأ إذا كان تعويض الموظف خارج الحد الأدنى والحد الأقصى للنقاط لمرجعية للمستوى، وسيقوم بشكل تلقائي بضبط تعويض الموظف لكي يقع ضمن النطاق.</span><span class="sxs-lookup"><span data-stu-id="1e074-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="1e074-121">يقوم الحقل **قاعدة التوظيف** بحساب تعويض الموظف أثناء حدث العملية.</span><span class="sxs-lookup"><span data-stu-id="1e074-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="1e074-122">تحسب **قاعدة التوظيف** بـ **النسبة المئوية** الزيادة التي تم حساب تناسبها لفترة الوقت التي تم خلالها توظيف العامل في الدورة.</span><span class="sxs-lookup"><span data-stu-id="1e074-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="1e074-123">في الحقل **العملة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e074-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="1e074-124">في الحقل **تحويل معدل الدفع**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1e074-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="1e074-125">قم بتوسيع القسم **مصفوفة مقياس معدل استخدام النطاق**.</span><span class="sxs-lookup"><span data-stu-id="1e074-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="1e074-126">بشكل اختياري، يمكنك إضافة سجلات استخدام النطاق لتمكين الموظفين من الوصول إلى نقطة الوسط الخاصة بهم بشكل أسرع وإبطاء وصولهم إلى الحد الأقصى للنطاق.</span><span class="sxs-lookup"><span data-stu-id="1e074-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="1e074-127">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1e074-127">Select **Save**.</span></span> <span data-ttu-id="1e074-128">وهذا يمكن الزر **إعداد التعويض** ويستمر في تعريف بنية التعويض للخطة.</span><span class="sxs-lookup"><span data-stu-id="1e074-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="1e074-129">حدد **إعداد التعويض**.</span><span class="sxs-lookup"><span data-stu-id="1e074-129">Select **Set up compensation**.</span></span> <span data-ttu-id="1e074-130">يمكنك إنشاء بنية التعويض باستخدام أحد الأساليب الثلاثة هذه:</span><span class="sxs-lookup"><span data-stu-id="1e074-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="1e074-131">إنشاء هيكل جديد تمامًا عن طريق تحديد مجموعة من النقاط المرجعية وإضافة المستويات اللازمة لإنشاء الهيكل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1e074-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="1e074-132">نسخ بنية تعويض من إحدى الخطط الموجودة كنقطة انطلاق وتعديلها للخطة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1e074-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="1e074-133">تحديد شبكة تعويض موجودة.</span><span class="sxs-lookup"><span data-stu-id="1e074-133">Select an existing compensation grid.</span></span> <span data-ttu-id="1e074-134">إذا كانت خطة أخرى تستخدم شبكة التعويض بالفعل، فستعمل الخطة الأخرى كذلك على عكس أية تغييرات تقوم بإدخالها على الشبكة.</span><span class="sxs-lookup"><span data-stu-id="1e074-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="1e074-135">حدد **إنشاء مصفوفة جديدة من مصفوفة تعويض موجودة**.</span><span class="sxs-lookup"><span data-stu-id="1e074-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="1e074-136">في الحقل **نسخ من الشبكة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1e074-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="1e074-137">بشكل اختياري، يمكنك تغيير اسم شبكة التعويض الجديدة التي ستقوم بإنشائها عن طريق نسخ الشبكة المحددة.</span><span class="sxs-lookup"><span data-stu-id="1e074-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="1e074-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1e074-138">Select **OK**.</span></span>

19. <span data-ttu-id="1e074-139">حدد **تغيير شامل**.</span><span class="sxs-lookup"><span data-stu-id="1e074-139">Select **Mass change**.</span></span> <span data-ttu-id="1e074-140">يسمح لك **التغيير الشامل** بالاحتفاظ بمبالغ مصفوفة التعويض عن طريق تطبيق زيادة في النسبة المئوية أو المبلغ الأساسي إلى واحد أو أكثر من المستويات أو النقاط المرجعية.</span><span class="sxs-lookup"><span data-stu-id="1e074-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="1e074-141">في الحقل **مبلغ التسوية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1e074-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="1e074-142">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="1e074-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="1e074-143">انقر فوق **تطبيق على الشبكة**.</span><span class="sxs-lookup"><span data-stu-id="1e074-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="1e074-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1e074-144">Close the page.</span></span> <span data-ttu-id="1e074-145">بمجرد أن تقوم بإنشاء بنية تعويض، فإنه يمكنك تحديد النقاط المرجعية التي يجب استخدامها كنقطة التحكم لخطة التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="1e074-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="1e074-146">يتم استخدام نقطة التحكم لحساب نسبة التعويض للموظف.</span><span class="sxs-lookup"><span data-stu-id="1e074-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="1e074-147">في الحقل **نقطة التحكم**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1e074-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="1e074-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1e074-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="1e074-149">إنشاء قاعدة أهلية لخطة التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="1e074-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="1e074-150">يتعذر عليك تعيين خطة التعويض الثابت الجديدة إلى موظف حتى تقوم بتعريف قواعد الأهلية للخطة.</span><span class="sxs-lookup"><span data-stu-id="1e074-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="1e074-151">حدد **قواعد الأهلية**.</span><span class="sxs-lookup"><span data-stu-id="1e074-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="1e074-152">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1e074-152">Select **New**.</span></span>

3. <span data-ttu-id="1e074-153">في الحقل **الأهلية**، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e074-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="1e074-154">في حقل **الوصف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e074-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="1e074-155">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="1e074-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="1e074-156">تستخدم كلاً من خطط التعويض الثابت والمتغير قواعد الأهلية.</span><span class="sxs-lookup"><span data-stu-id="1e074-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="1e074-157">في الحقل **النوع**، حدد نوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="1e074-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="1e074-158">في حقل **الخطة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1e074-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="1e074-159">حدد المعايير التي يجب أن يفي بها الموظف لكي يتأهل لخطة التعويض.</span><span class="sxs-lookup"><span data-stu-id="1e074-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="1e074-160">يمكن أن تتضمن المعايير ما يلي:</span><span class="sxs-lookup"><span data-stu-id="1e074-160">Criteria can include:</span></span>

    - <span data-ttu-id="1e074-161">**قسم**</span><span class="sxs-lookup"><span data-stu-id="1e074-161">**Department**</span></span>
    - <span data-ttu-id="1e074-162">**اتحاد العمال**</span><span class="sxs-lookup"><span data-stu-id="1e074-162">**Labor union**</span></span>
    - <span data-ttu-id="1e074-163">**الموقع** (**منطقة التعويض**)</span><span class="sxs-lookup"><span data-stu-id="1e074-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="1e074-164">**الوظيفة**</span><span class="sxs-lookup"><span data-stu-id="1e074-164">**Job**</span></span>
    - <span data-ttu-id="1e074-165">**الوظيفة**</span><span class="sxs-lookup"><span data-stu-id="1e074-165">**Function**</span></span>
    - <span data-ttu-id="1e074-166">**نوع الوظيفة**</span><span class="sxs-lookup"><span data-stu-id="1e074-166">**Job type**</span></span>
    - <span data-ttu-id="1e074-167">**مستوى التعويض**</span><span class="sxs-lookup"><span data-stu-id="1e074-167">**Compensation level**</span></span>
    
    <span data-ttu-id="1e074-168">يجب أن يفي الموظف بكل المعايير المحددة لكي يتأهل لخطة التعويض.</span><span class="sxs-lookup"><span data-stu-id="1e074-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="1e074-169">إذا لم تقم بتحديد أية معايير، فسيتأهل جميع الموظفين لخطة التعويض.</span><span class="sxs-lookup"><span data-stu-id="1e074-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="1e074-170">إذا لم يتمكن الموظف من استيفاء المعايير المحددة في قاعدة الأهلية، أو لم يتم تحديد قاعدة أهلية لخطة تعويض، فلن تظهر خطة التعويض في البحث عندما تقوم بإنشاء سجل تعويض ثابت لموظف.</span><span class="sxs-lookup"><span data-stu-id="1e074-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="1e074-171">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1e074-171">Close the page.</span></span>

8. <span data-ttu-id="1e074-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1e074-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]