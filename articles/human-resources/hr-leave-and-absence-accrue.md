---
title: استحقاق خطط الإجازة والغياب
description: يمكنك تسجيل الإجازات والغياب في Dynamics 365 Human Resources للعديد من الموظفين أو لفرد واحد.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
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
ms.openlocfilehash: 348c8e5336854eb2a1c04a1f98a97a2c9dba7176
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464900"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="06332-103">استحقاق خطط الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="06332-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="06332-104">يمكنك تسجيل الإجازات والغياب في Dynamics 365 Human Resources للعديد من الموظفين أو لفرد واحد.</span><span class="sxs-lookup"><span data-stu-id="06332-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="06332-105">تسجيل الإجازات والغياب لموظفين متعددين</span><span class="sxs-lookup"><span data-stu-id="06332-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="06332-106">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="06332-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="06332-107">ضمن **إدارة الإجازة**، حدد **تسجيل خطط الإجازات والغياب**.</span><span class="sxs-lookup"><span data-stu-id="06332-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="06332-108">يظهر مربع الحوار **استحقاق خطط الإجازة والغياب‬**.</span><span class="sxs-lookup"><span data-stu-id="06332-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="06332-109">في **استحقاق اعتبارًا من**، حدد **تاريخ اليوم** أو **تاريخ مخصص** وأدخل تاريخًا مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="06332-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="06332-110">إذا كنت ترغب في تشغيل الاستحقاقات لجميع الشركات، حدد **كافة الشركات**.</span><span class="sxs-lookup"><span data-stu-id="06332-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="06332-111">إذا كنت تريد معالجة الاستحقاقات لخطة إجازة واحدة، حدد **لا** لـ **جميع الخطط** ، ثم حدد **خطة إجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="06332-112">إذا قمت بتحديد كافة الشركات، فلا يُمكنك تحديد خطة إجازة فردية.</span><span class="sxs-lookup"><span data-stu-id="06332-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="06332-113">إذا كنت ترغب في تشغيل عملية التسجيل في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="06332-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="06332-114">أدخل معلومات لعملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="06332-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="06332-115">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="06332-116">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="06332-117">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-117">Select **OK**.</span></span> <span data-ttu-id="06332-118">سيتم تشغيل عملية التسجيل باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="06332-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="06332-119">تسجيل الإجازة والغياب لموظف</span><span class="sxs-lookup"><span data-stu-id="06332-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="06332-120">في سجل الموظف، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="06332-121">حدد **تسجيل الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="06332-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="06332-122">يظهر مربع الحوار **استحقاق خطط الإجازة والغياب‬**.</span><span class="sxs-lookup"><span data-stu-id="06332-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="06332-123">في **استحقاق اعتبارًا من**، حدد **تاريخ اليوم** أو **تاريخ مخصص** وأدخل تاريخًا مخصصًا.</span><span class="sxs-lookup"><span data-stu-id="06332-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="06332-124">إذا كنت ترغب في تشغيل الاستحقاقات لجميع الشركات، حدد **كافة الشركات**.</span><span class="sxs-lookup"><span data-stu-id="06332-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="06332-125">إذا كنت تريد معالجة الاستحقاقات لخطة إجازة واحدة، حدد **لا** لـ **جميع الخطط** ، ثم حدد **خطة إجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="06332-126">إذا قمت بتحديد كافة الشركات، فلا يُمكنك تحديد خطة إجازة فردية.</span><span class="sxs-lookup"><span data-stu-id="06332-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="06332-127">إذا كنت ترغب في تشغيل عملية التسجيل في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="06332-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="06332-128">أدخل معلومات لعملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="06332-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="06332-129">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="06332-130">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="06332-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-131">Select **OK**.</span></span> <span data-ttu-id="06332-132">سيتم تشغيل عملية التسجيل باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="06332-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="06332-133">حذف استحقاقات الإجازة والغياب لموظفين متعددين</span><span class="sxs-lookup"><span data-stu-id="06332-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="06332-134">حذف سجلات الاستحقاق الخاصة بخطة محدده ونطاق تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="06332-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="06332-135">يجب أن تكون تواريخ الاستحقاق في تاريخ اليوم أو في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="06332-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="06332-136">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="06332-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="06332-137">ضمن **إدارة الإجازة**، حدد **حذف استحقاقات خطط الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="06332-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="06332-138">في مربع الحوار **حذف استحقاقات خطط الإجازة والغياب**، حدد **خطة الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="06332-139">اختر **حذف تسويات الأرصدة**، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="06332-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="06332-140">أدخل **تاريخ استحقاق الاجازة** أو حدده.</span><span class="sxs-lookup"><span data-stu-id="06332-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="06332-141">يجب أن يكون هذا التاريخ تاريخ اليوم أو تاريخًا في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="06332-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="06332-142">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-142">Select **OK**.</span></span> <span data-ttu-id="06332-143">ستقوم عملية الاستحقاق بحذف الاستحقاقات مع المعلمات التي تعينها.</span><span class="sxs-lookup"><span data-stu-id="06332-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="06332-144">حذف استحقاقات الإجازة والغياب لموظف واحد</span><span class="sxs-lookup"><span data-stu-id="06332-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="06332-145">في سجل الموظف، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="06332-146">حدد **حذف خطط استحقاقات الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="06332-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="06332-147">في مربع الحوار **حذف استحقاقات خطط الإجازة والغياب**، حدد **خطة الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="06332-148">اختر **حذف تسويات الأرصدة**، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="06332-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="06332-149">أدخل **تاريخ استحقاق الاجازة** أو حدده.</span><span class="sxs-lookup"><span data-stu-id="06332-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="06332-150">يجب أن يكون هذا التاريخ تاريخ اليوم أو تاريخًا في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="06332-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="06332-151">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="06332-151">Select **OK**.</span></span> <span data-ttu-id="06332-152">ستقوم عملية الاستحقاق بحذف الاستحقاقات مع المعلمات التي تعينها.</span><span class="sxs-lookup"><span data-stu-id="06332-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="06332-153">مراجعة استحقاقات الإجازات وعمليات الحذف</span><span class="sxs-lookup"><span data-stu-id="06332-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="06332-154">يظهر الخيار **تدقيق استحقاق الإجازة** في كل مره تقوم فيها بتشغيل أو حذف استحقاق لموظف أو لعدة موظفين.</span><span class="sxs-lookup"><span data-stu-id="06332-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="06332-155">يظهر أيضًا التاريخ والشخص الذي قام بتنفيذ الإجراء.</span><span class="sxs-lookup"><span data-stu-id="06332-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="06332-156">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="06332-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="06332-157">ضمن **إدارة الإجازة**، حدد **حذف تدقيق استحقاق الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="06332-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="06332-158">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="06332-158">See also</span></span>

[<span data-ttu-id="06332-159">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="06332-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="06332-160">إنشاء خطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="06332-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]