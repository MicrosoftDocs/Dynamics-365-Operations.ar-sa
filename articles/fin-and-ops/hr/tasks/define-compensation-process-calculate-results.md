--- 
title: "تحديد عملية التعويض وحساب النتائج"
description: "تستخدم عمليات التعويض لتحديد مبالغ التعويضات الجديدة والمكافآت للموظفين المسجلين في خطط التعويض الثابتة والمتغيرة."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 9cc66eccec146c9f8f562b5d4e4d21bb6b7c6457
ms.contentlocale: ar-sa
ms.lasthandoff: 02/02/2018

---
# <a name="define-compensation-process-and-calculate-results"></a><span data-ttu-id="09ba0-103">تحديد عملية التعويض وحساب النتائج</span><span class="sxs-lookup"><span data-stu-id="09ba0-103">Define compensation process and calculate results</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09ba0-104">تستخدم عمليات التعويض لتحديد مبالغ التعويضات الجديدة والمكافآت للموظفين المسجلين في خطط التعويض الثابتة والمتغيرة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-104">Compensation processes are used to determine new compensation amounts and awards for employees enrolled in fixed and variable compensation plans.</span></span> <span data-ttu-id="09ba0-105">يمكن تشغيل عمليات التعويض عدة مرات للقيام بتحليل "ماذا لو"، للتحقق من صحة كافة التغييرات والإعدادات.</span><span class="sxs-lookup"><span data-stu-id="09ba0-105">Compensation processes can be run multiple times to perform "what-if" analysis, to verify all changes and settings are correct.</span></span> <span data-ttu-id="09ba0-106">يقوم هذا الإجراء بإنشاء عملية تعويض، وتشغيل العملية وعرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="09ba0-106">This procedure will create a compensation process, run the process, and view the results.</span></span> <span data-ttu-id="09ba0-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="09ba0-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-compensation-process"></a><span data-ttu-id="09ba0-108">إنشاء عملية تعويض</span><span class="sxs-lookup"><span data-stu-id="09ba0-108">Create a compensation process</span></span>
1. <span data-ttu-id="09ba0-109">انتقل إلى الموارد البشرية > التعويض > المعالجة > عمليات التعويض.</span><span class="sxs-lookup"><span data-stu-id="09ba0-109">Go to Human resources > Compensation > Process > Compensation processes.</span></span>
2. <span data-ttu-id="09ba0-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="09ba0-110">Click New.</span></span>
3. <span data-ttu-id="09ba0-111">في حقل "العملية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-111">In the Process field, type a value.</span></span>
4. <span data-ttu-id="09ba0-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09ba0-113">في حقل "نوع العملية"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-113">In the Process type field, select an option.</span></span>
    * <span data-ttu-id="09ba0-114">تحدد الدورة الفترة الزمنية التي تم تقييمها لتحديد التعويض.</span><span class="sxs-lookup"><span data-stu-id="09ba0-114">A cycle specifies the time period evaluated to determine compensation.</span></span> <span data-ttu-id="09ba0-115">ويشمل التقييم المناصب التي يشغلها الموظفون وتقييمات الأداء المطلوب تضمينها وحساب النسبة المئوية للوقت الذي كان الموظف يعمل فيه أثناء الدورة، والمزيد.</span><span class="sxs-lookup"><span data-stu-id="09ba0-115">The evaluation considers which positions were held by employees, which performance ratings to include, calculation of the percentage of time the employee was employed during the cycle, and more.</span></span> <span data-ttu-id="09ba0-116">قد يكون أحد الأمثلة لتاريخ بدء دورة هو اليوم الأول من السنة المالية الماضية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-116">An example of a cycle start date might be the first day of the past fiscal year.</span></span>  
6. <span data-ttu-id="09ba0-117">في حقل "بداية الدورة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-117">In the Cycle start field, enter a date.</span></span>
    * <span data-ttu-id="09ba0-118">إن تاريخ نهاية الدورة مهم لأنه التاريخ المستخدم لتحديد الموظفين العاملين والمسجلين بشكل فعال في واحدة أو أكثر من خطط التعويض.</span><span class="sxs-lookup"><span data-stu-id="09ba0-118">The cycle end date is  important because it is the date used to determine which employees were actively employed and enrolled in one or more compensation plans.</span></span>  
7. <span data-ttu-id="09ba0-119">في حقل "نهاية الدورة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-119">In the Cycle end field, enter a date.</span></span>
    * <span data-ttu-id="09ba0-120">إن تاريخ التفعيل للحركة هو التاريخ الذي ينبغي أن تدخل فيه معدلات التعويض الجديدة حيز التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="09ba0-120">The transaction active date is the date the new compensation rates should take effect.</span></span> <span data-ttu-id="09ba0-121">تضع العديد من الشركات بضعة أشهر بين نهاية دورة وتوقيت دخول معدلات التعويض جديدة حيز التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="09ba0-121">Many companies include a few months between their end of a cycle and the time the new compensation rates go into effect.</span></span> <span data-ttu-id="09ba0-122">يتم استخدام وقت إضافي لمعالجة ومراجعة التعويضات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-122">The additional time is used for processing and reviewing the new compensation.</span></span>  
8. <span data-ttu-id="09ba0-123">في حقل "‏‫تاريخ التفعيل للحركة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-123">In the Transaction active date field, enter a date.</span></span>
    * <span data-ttu-id="09ba0-124">يتم استخدام تاريخ النقطة الزمنية‬ لخطط التعويض المتغيرة التي تحدد مبلغ المكافأة الممنوح للموظف استنادًا إلى معدل التعويض في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="09ba0-124">The point-in-time date is used for variable compensation plans that determine an employee's award amount based on their compensation rate at this point in time.</span></span>  
    * <span data-ttu-id="09ba0-125">يتم استخدام ‏‫تاريخ التوظيف النسبي على أساس الدفع الثابت‬ مع خطط التعويض الثابت مع قاعدة التوظيف بالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-125">The fixed pay pro rated hire date is used with fixed compensation plans with a hire rule of Percent.</span></span>  <span data-ttu-id="09ba0-126">يحصل الموظفون الذين تم توظيفهم بين تاريخ بدء الدورة وتاريخ التوظيف النسبي على أساس الدفع الثابت على نسبة 100% من الزيادة المحسوبة في عملية التعويض، بدلاً من النسبة المئوية التناسبية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-126">Employees who are hired between the cycle start and the fixed pay pro rated hire date will receive 100% of their calculated compensation increase, instead of pro-rated percentage.</span></span>  
9. <span data-ttu-id="09ba0-127">في حقل "تاريخ التوظيف النسبي على أساس الدفع الثابت"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-127">In the Fixed pay pro rated hire date field, enter a date.</span></span>
    * <span data-ttu-id="09ba0-128">موعد انتهاء المراجعة هو التاريخ الذي ينبغي أن يتم قبله مراجعة جميع نتائج العملية بحيث يمكن تحميلها في سجل تعويضات الموظف قبل ‏‫تاريخ التفعيل للحركة‬.</span><span class="sxs-lookup"><span data-stu-id="09ba0-128">The review deadline is the date by which all process results should be reviewed so that they can be loaded into an employee's compensation record before the transaction active date.</span></span> <span data-ttu-id="09ba0-129">هذا الحقل للأغراض المعلوماتية فقط.</span><span class="sxs-lookup"><span data-stu-id="09ba0-129">This field is informational only.</span></span>  
10. <span data-ttu-id="09ba0-130">في حقل "الموعد النهائي للمراجعة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-130">In the Review deadline field, enter a date.</span></span>
11. <span data-ttu-id="09ba0-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="09ba0-131">Click Save.</span></span>

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a><span data-ttu-id="09ba0-132">إعداد خطط التعويض وإجراءات عملية التعويض</span><span class="sxs-lookup"><span data-stu-id="09ba0-132">Setup the compensation plans and actions for a compensation process</span></span>
1. <span data-ttu-id="09ba0-133">انقر فوق إعداد.</span><span class="sxs-lookup"><span data-stu-id="09ba0-133">Click Setup.</span></span>
    * <span data-ttu-id="09ba0-134">يتم استخدام إعداد الصفحة لتحديد أي خطط ستتم معالجتها كجزء من عملية التعويض هذه، بالإضافة إلى الإجراءات التي يجب اتخاذها ضد كل خطة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-134">The Setup page is used to select which plans to process as part of this compensation process, as well as which actions should be taken against each plan.</span></span>  
2. <span data-ttu-id="09ba0-135">في حقل "الخطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="09ba0-135">In the Plan field, enter or select a value.</span></span>
3. <span data-ttu-id="09ba0-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="09ba0-136">Click Save.</span></span>
4. <span data-ttu-id="09ba0-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-137">Click Add.</span></span>
5. <span data-ttu-id="09ba0-138">في حقل "الإجراءات"، حدد نوع الإجراء الخاص بحق الملكية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-138">In the Action field, select an Equity type of action.</span></span>
6. <span data-ttu-id="09ba0-139">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-139">Click Add.</span></span>
7. <span data-ttu-id="09ba0-140">في حقل "الإجراءات"، حدد نوع الإجراء الخاص بالاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="09ba0-140">In the Action field, select a Merit type of action.</span></span>
    * <span data-ttu-id="09ba0-141">يمكن "ربط" إجراءات التعويض معًا باستخدام حقل "استخدام النتيجة السابقة" للإشارة إلى ما إذا كان ينبغي على الإجراء المحدد استخدام الراتب الأساسي للموظفين أو نتيجة الإجراء السابق كنقطة انطلاق لحساب هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="09ba0-141">Compensation actions can be "chained" together using the Use previous result field to indicate whether the selected action should use the employees base pay or the result of the previous action as the starting point for this action's calculation.</span></span>  
8. <span data-ttu-id="09ba0-142">حدد "نعم" في حقل "استخدام النتيجة السابقة".</span><span class="sxs-lookup"><span data-stu-id="09ba0-142">Select Yes in the Use previous result field.</span></span>
9. <span data-ttu-id="09ba0-143">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-143">Click Add.</span></span>
10. <span data-ttu-id="09ba0-144">في حقل "الإجراءات"، حدد نوع الإجراء العام.</span><span class="sxs-lookup"><span data-stu-id="09ba0-144">In the Action field, select a General type of Action.</span></span>
    * <span data-ttu-id="09ba0-145">تؤدي أنواع إجراءات التعويض المختلفة إلى تمكين حقول مختلفة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-145">Different compensation action types enable different fields.</span></span> <span data-ttu-id="09ba0-146">بالنسبة لنوع إجراء التعويض العام، يمكن تحديد نسبة الزيادة أو مبلغ الزيادة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-146">For a General compensation action type, an increase percent or increase amount can be specified.</span></span>  
11. <span data-ttu-id="09ba0-147">حدد خيار "‏‫تحديد مبلغ الزيادة‬".</span><span class="sxs-lookup"><span data-stu-id="09ba0-147">Select the Select increase amount option.</span></span>
12. <span data-ttu-id="09ba0-148">في حقل "مبلغ الزيادة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-148">In the Increase amount field, enter a number.</span></span>
13. <span data-ttu-id="09ba0-149">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-149">Click Add.</span></span>
14. <span data-ttu-id="09ba0-150">في حقل "الإجراءات"، حدد نوع إجراء الترقية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-150">In the Action field, select a Promotion type of Action.</span></span>
    * <span data-ttu-id="09ba0-151">تؤدي الترقية وأنواع إجراء التغيير على مستوي آخر إلى تمكين المستخدمين من إجراء تعديلات يدوية لتعويض الموظف.</span><span class="sxs-lookup"><span data-stu-id="09ba0-151">Promotion and Other level change action types enable users to make manual adjustments to employee compensation.</span></span> <span data-ttu-id="09ba0-152">يمكن تمكين التوصيات لهذه الأنواع من الإجراءات، بالإضافة إلى أنواع الإجراءات الأخرى لكي تتمكن من إدخال قيمة التعويض الجديدة الموصى بدفعها للموظف.</span><span class="sxs-lookup"><span data-stu-id="09ba0-152">Recommendations can be enabled for these action types, as well as other action types to enable you to enter a new recommended compensation value for an employee.</span></span>  
15. <span data-ttu-id="09ba0-153">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-153">Click Add.</span></span>
16. <span data-ttu-id="09ba0-154">في الحقل "النوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-154">In the Type field, select an option.</span></span>
    * <span data-ttu-id="09ba0-155">يمكن تشغيل خطط التعويض الثابتة والمتغيرة في نفس عملية التعويض.</span><span class="sxs-lookup"><span data-stu-id="09ba0-155">Fixed and variable compensation plans can be run in the same compensation process.</span></span>  
17. <span data-ttu-id="09ba0-156">في حقل "الخطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="09ba0-156">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="09ba0-157">استخدم خانة الاختيار "تمكين الدفع مقابل الأداء" لتحديد ما إذا كان ينبغي تعديل مبالغ التعويض الثابتة والمتغيرة استنادًا إلى تقييم أداء الموظف.</span><span class="sxs-lookup"><span data-stu-id="09ba0-157">Use the Enable pay for performance check box to determine whether fixed and variable compensation amounts should be adjusted based on the employee's performance rating.</span></span>  
    * <span data-ttu-id="09ba0-158">يمكن تجاوز الزيادة في خطط التعويض المتغيرة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-158">Leverage can be overridden on variable compensation plans.</span></span>  
18. <span data-ttu-id="09ba0-159">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="09ba0-159">Click Save.</span></span>
19. <span data-ttu-id="09ba0-160">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-160">Click Add.</span></span>
20. <span data-ttu-id="09ba0-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-161">Close the page.</span></span>

## <a name="run-the-compensation-process"></a><span data-ttu-id="09ba0-162">تشغيل عملية التعويض</span><span class="sxs-lookup"><span data-stu-id="09ba0-162">Run the compensation process</span></span>
1. <span data-ttu-id="09ba0-163">انقر فوق "‏‫تشغيل العملية".</span><span class="sxs-lookup"><span data-stu-id="09ba0-163">Click Run process.</span></span>
    * <span data-ttu-id="09ba0-164">يتيح لك "التحكم في عرض نتائج المعالجة" عرض رسائل المعالجة لعملية التعويض الكاملة عند انتهاء معالجة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-164">The Show processing results control lets you view processing messages for the complete compensation process when processing has finished.</span></span>  
2. <span data-ttu-id="09ba0-165">حدد "نعم" في حقل "إظهار نتائج المعالجة.</span><span class="sxs-lookup"><span data-stu-id="09ba0-165">Select Yes in the Show processing results field.</span></span>
3. <span data-ttu-id="09ba0-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="09ba0-166">Click OK.</span></span>

## <a name="view-the-results"></a><span data-ttu-id="09ba0-167">عرض النتائج</span><span class="sxs-lookup"><span data-stu-id="09ba0-167">View the results</span></span>
1. <span data-ttu-id="09ba0-168">انقر فوق "نتائج العملية".</span><span class="sxs-lookup"><span data-stu-id="09ba0-168">Click Process results.</span></span>
2. <span data-ttu-id="09ba0-169">انقر فوق "نتائج الموظف".</span><span class="sxs-lookup"><span data-stu-id="09ba0-169">Click Employee results.</span></span>
3. <span data-ttu-id="09ba0-170">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="09ba0-170">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="09ba0-171">قم بتوسيع مقطع "التعويض الثابت".</span><span class="sxs-lookup"><span data-stu-id="09ba0-171">Expand the Fixed compensation section.</span></span>
    * <span data-ttu-id="09ba0-172">قم بتوسيع علامات التبويب السريعة لعرض نتائج العملية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-172">Expand the FastTabs to view the results of the process.</span></span> <span data-ttu-id="09ba0-173">إذا تم وضع علامة على تمكين التوصيات لإجراء تعويض، فسيتم تمكين حقول التوصية المتعلقة بهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="09ba0-173">If Enable recommendations was marked for a compensation action, the Recommendation fields will be enabled for that action.</span></span>  
5. <span data-ttu-id="09ba0-174">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="09ba0-174">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="09ba0-175">يمكن عرض النتائج لموظف واحد بالنقر على زر "عرض النتائج".</span><span class="sxs-lookup"><span data-stu-id="09ba0-175">The results for a single employee can be viewed by clicking the View results button.</span></span>  
    * <span data-ttu-id="09ba0-176">يمكنك استبدال مبلغ التعويض المحسوب عن طريق تعديل النسبة المئوية أو مبلغ الزيادة في حقول التوصية.</span><span class="sxs-lookup"><span data-stu-id="09ba0-176">You can overwrite the calculated compensation amount by adjusting the percent or the increase amount in the Recommendation fields.</span></span>  
6. <span data-ttu-id="09ba0-177">في حقل النسبة المئوية الموصى بها‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-177">In the percent recommended field, enter a number.</span></span>
7. <span data-ttu-id="09ba0-178">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="09ba0-178">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="09ba0-179">في حقل النسبة المئوية الموصى بها‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="09ba0-179">In the percent recommended field, enter a number.</span></span>
    * <span data-ttu-id="09ba0-180">يمكن استخدام إعادة الحساب لتجاهل أية تغييرات طرأت على السجل الحالي وإنشاء نتيجة تعويض جديدة للموظف المحدد.</span><span class="sxs-lookup"><span data-stu-id="09ba0-180">Recalculate can be used to ignore any changes made to the existing record and generate a new compensation result for the selected employee.</span></span>  
    * <span data-ttu-id="09ba0-181">عند إتمام كافة التغييرات لأحد الموظفين، قم بتغيير الحالة إلى "‏‫معتمد".</span><span class="sxs-lookup"><span data-stu-id="09ba0-181">When all changes are complete for an employee, change the status to Approved.</span></span>  
9. <span data-ttu-id="09ba0-182">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="09ba0-182">Click Change status.</span></span>
10. <span data-ttu-id="09ba0-183">انقر فوق "‏‫معتمد".</span><span class="sxs-lookup"><span data-stu-id="09ba0-183">Click Approved.</span></span>
    * <span data-ttu-id="09ba0-184">بعد اعتماد السجل، يمكن تحميله إلى سجل التعويض الرسمي للموظف.</span><span class="sxs-lookup"><span data-stu-id="09ba0-184">After the record has been approved it can be loaded to the employee's official compensation record.</span></span> <span data-ttu-id="09ba0-185">سيكون التعويض الجديد ساري المفعول اعتبارًا من تاريخ الحركة المحدد على عملية التعويض.</span><span class="sxs-lookup"><span data-stu-id="09ba0-185">The new compensation will be effective as of the transaction date set on the compensation process.</span></span>  


