---
title: استحقاق خطط الإجازة والغياب
description: يمكنك تسجيل الإجازات والغياب في Dynamics 365 Human Resources للعديد من الموظفين أو لفرد واحد.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 86ca63b1703faa6f57ed2e5591c89a5e84363481
ms.sourcegitcommit: 318e406b84d43381d450272eb83c5eea9c5cf1c0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059463"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="ac3d0-103">استحقاق خطط الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="ac3d0-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ac3d0-104">يمكنك تسجيل الإجازات والغياب في Dynamics 365 Human Resources للعديد من الموظفين أو لفرد واحد.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="ac3d0-105">تسجيل الإجازات والغياب لموظفين متعددين</span><span class="sxs-lookup"><span data-stu-id="ac3d0-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="ac3d0-106">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ac3d0-107">ضمن **إدارة الإجازة**، حدد **تسجيل خطط الإجازات والغياب**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="ac3d0-108">يظهر مربع الحوار **استحقاق خطط الإجازة والغياب‬**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="ac3d0-109">في **استحقاق اعتبارًا من**، حدد **تاريخ اليوم** أو **تاريخ مخصص** وأدخل تاريخًا مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="ac3d0-110">إذا كنت ترغب في تشغيل الاستحقاقات لجميع الشركات، حدد **كافة الشركات**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="ac3d0-111">إذا كنت تريد معالجة الاستحقاقات لخطة إجازة واحدة، حدد **لا** لـ **جميع الخطط** ، ثم حدد **خطة إجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="ac3d0-112">إذا قمت بتحديد كافة الشركات، فلا يُمكنك تحديد خطة إجازة فردية.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="ac3d0-113">إذا كنت ترغب في تشغيل عملية التسجيل في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ac3d0-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="ac3d0-114">أدخل معلومات لعملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="ac3d0-115">لإعداد مهمة متكررة، حدد **التكرار**، وأدخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="ac3d0-116">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="ac3d0-117">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-117">Select **OK**.</span></span> <span data-ttu-id="ac3d0-118">سيتم تشغيل عملية التسجيل باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="ac3d0-119">تسجيل الإجازة والغياب لموظف</span><span class="sxs-lookup"><span data-stu-id="ac3d0-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="ac3d0-120">في سجل الموظف، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="ac3d0-121">حدد **تسجيل الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="ac3d0-122">يظهر مربع الحوار **استحقاق خطط الإجازة والغياب‬**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="ac3d0-123">في **استحقاق اعتبارًا من**، حدد **تاريخ اليوم** أو **تاريخ مخصص** وأدخل تاريخًا مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="ac3d0-124">إذا كنت ترغب في تشغيل الاستحقاقات لجميع الشركات، حدد **كافة الشركات**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="ac3d0-125">إذا كنت تريد معالجة الاستحقاقات لخطة إجازة واحدة، حدد **لا** لـ **جميع الخطط** ، ثم حدد **خطة إجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="ac3d0-126">إذا قمت بتحديد كافة الشركات، فلا يُمكنك تحديد خطة إجازة فردية.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="ac3d0-127">إذا كنت ترغب في تشغيل عملية التسجيل في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ac3d0-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="ac3d0-128">أدخل معلومات لعملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="ac3d0-129">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="ac3d0-130">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="ac3d0-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-131">Select **OK**.</span></span> <span data-ttu-id="ac3d0-132">سيتم تشغيل عملية التسجيل باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="ac3d0-133">حذف استحقاقات الإجازة والغياب لموظفين متعددين</span><span class="sxs-lookup"><span data-stu-id="ac3d0-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="ac3d0-134">حذف سجلات الاستحقاق الخاصة بخطة محدده ونطاق تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="ac3d0-135">يجب أن تكون تواريخ الاستحقاق في تاريخ اليوم أو في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="ac3d0-136">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ac3d0-137">ضمن **إدارة الإجازة**، حدد **حذف استحقاقات خطط الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="ac3d0-138">في مربع الحوار **حذف استحقاقات خطط الإجازة والغياب**، حدد **خطة الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="ac3d0-139">اختر **حذف تسويات الأرصدة**، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="ac3d0-140">أدخل **تاريخ استحقاق الاجازة** أو حدده.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="ac3d0-141">يجب أن يكون هذا التاريخ تاريخ اليوم أو تاريخًا في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="ac3d0-142">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-142">Select **OK**.</span></span> <span data-ttu-id="ac3d0-143">ستقوم عملية الاستحقاق بحذف الاستحقاقات مع المعلمات التي تعينها.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="ac3d0-144">حذف استحقاقات الإجازة والغياب لموظف واحد</span><span class="sxs-lookup"><span data-stu-id="ac3d0-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="ac3d0-145">في سجل الموظف، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="ac3d0-146">حدد **حذف خطط استحقاقات الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="ac3d0-147">في مربع الحوار **حذف استحقاقات خطط الإجازة والغياب**، حدد **خطة الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="ac3d0-148">اختر **حذف تسويات الأرصدة**، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="ac3d0-149">أدخل **تاريخ استحقاق الاجازة** أو حدده.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="ac3d0-150">يجب أن يكون هذا التاريخ تاريخ اليوم أو تاريخًا في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="ac3d0-151">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-151">Select **OK**.</span></span> <span data-ttu-id="ac3d0-152">ستقوم عملية الاستحقاق بحذف الاستحقاقات مع المعلمات التي تعينها.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="ac3d0-153">مراجعة استحقاقات الإجازات وعمليات الحذف</span><span class="sxs-lookup"><span data-stu-id="ac3d0-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="ac3d0-154">يظهر الخيار **تدقيق استحقاق الإجازة** في كل مره تقوم فيها بتشغيل أو حذف استحقاق لموظف أو لعدة موظفين.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="ac3d0-155">يظهر أيضًا التاريخ والشخص الذي قام بتنفيذ الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="ac3d0-156">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ac3d0-157">ضمن **إدارة الإجازة**، حدد **حذف تدقيق استحقاق الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="preview-leave-accrual-transaction-auditing"></a><span data-ttu-id="ac3d0-158">(معاينة) تدقيق حركة استحقاقات الإجازة</span><span class="sxs-lookup"><span data-stu-id="ac3d0-158">(Preview) Leave accrual transaction auditing</span></span>

[!include [Preview feature](includes/preview-feature.md)]

<span data-ttu-id="ac3d0-159">تساعد ميزة المعاينة هذه على فهم مديري الإجازات والغياب لحركات الإجازات والغياب المستحقة المرتبطة بأرصدة إجازات الموظف لنوع إجازة معين.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-159">This preview feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="ac3d0-160">لعرض تفاصيل الحركة:</span><span class="sxs-lookup"><span data-stu-id="ac3d0-160">To view transaction details:</span></span>

1. <span data-ttu-id="ac3d0-161">في سجل الموظف، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="ac3d0-162">حدد **عرض الإجازة**، ثم حدد علامة التبويب **أرصدة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="ac3d0-163">لعرض حركات الاستحقاق المرتبطة بنوع إجازة معين، حدد القيمة الرقمية في العمود **الرصيد الحالي**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="ac3d0-164">لعرض تفاصيل الحركة لمبلغ استحقاق معين، حدد صف استحقاق، وافتح لوحة **المعلومات المرتبطة** على اليمين، ثم افتح القسم **تفاصيل الحركة**.</span><span class="sxs-lookup"><span data-stu-id="ac3d0-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="ac3d0-165">يعرض قسم تفاصيل الحركة:</span><span class="sxs-lookup"><span data-stu-id="ac3d0-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="ac3d0-166">التغييرات التي تم إجراؤها على رصيد نوع إجازة الموظف</span><span class="sxs-lookup"><span data-stu-id="ac3d0-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="ac3d0-167">تفاصيل التوظيف لفترة الاستحقاق المحددة</span><span class="sxs-lookup"><span data-stu-id="ac3d0-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="ac3d0-168">تفاصيل حول فترة ومعدلات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="ac3d0-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="ac3d0-169">أية تغييرات يتم إجراؤها لتكوينات خطة الإجازة</span><span class="sxs-lookup"><span data-stu-id="ac3d0-169">Any changes made to leave plan configurations</span></span>

![عرض تدقيق حركة استحقاقات الإجازة](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="ac3d0-171">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="ac3d0-171">See also</span></span>

[<span data-ttu-id="ac3d0-172">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="ac3d0-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="ac3d0-173">إنشاء خطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="ac3d0-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
