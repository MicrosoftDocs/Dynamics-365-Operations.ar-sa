---
title: تكوين المهام اليدوية في سير عمل
description: يوضح هذا الموضوع كيفية تكوين خصائص مهمة يدوية.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cae815bede98df7e5b937f6ffda99fa4ffed937
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698209"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="87093-103">تكوين المهام اليدوية في سير عمل</span><span class="sxs-lookup"><span data-stu-id="87093-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87093-104">يوضح هذا الموضوع كيفية تكوين خصائص مهمة يدوية.</span><span class="sxs-lookup"><span data-stu-id="87093-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="87093-105">لتكوين مهمة يدوية في محرر سير العمل، انقر بزر الماوس الأيمن فوق المهمة، وثم انقر فوق **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="87093-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="87093-106">ثم استخدم الإجراءات التالية لتكوين خصائص المهمة اليدوية.</span><span class="sxs-lookup"><span data-stu-id="87093-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="87093-107">تسمية المهمة</span><span class="sxs-lookup"><span data-stu-id="87093-107">Name the task</span></span>

<span data-ttu-id="87093-108">اتبع الخطوات التالية لإدخال اسم للمهمة اليدوية.</span><span class="sxs-lookup"><span data-stu-id="87093-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="87093-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="87093-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="87093-110">في حقل **الاسم**، أدخل اسمًا فريدًا للمهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="87093-111">أدخل سطر الموضوع والإرشادات</span><span class="sxs-lookup"><span data-stu-id="87093-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="87093-112">يجب توفير سطر موضوع وتعليمات للمستخدمين الذين تم تعيينهم للمهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="87093-113">على سبيل المثال، إذا كنت تقوم بتكوين مهمة لطلبات الشراء، يرى المستخدم الذي تم تعيينه للمهمة سطر الموضوع والتعليمات على صفحة **طلبات الشراء**.</span><span class="sxs-lookup"><span data-stu-id="87093-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="87093-114">يظهر سطر الموضوع في شريط الرسائل على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="87093-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="87093-115">وسيتمكن المستخدم عندئذٍ من النقر فوق الأيقونة في شريط الرسائل لعرض التعليمات.</span><span class="sxs-lookup"><span data-stu-id="87093-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="87093-116">اتبع الخطوات التالية لإدخال سطر موضوع وتعليمات.</span><span class="sxs-lookup"><span data-stu-id="87093-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="87093-117">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="87093-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="87093-118">في حقل **موضوع عنصر العمل**، أدخل سطر الموضوع.</span><span class="sxs-lookup"><span data-stu-id="87093-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="87093-119">لتخصيص سطر الموضوع، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="87093-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="87093-120">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر سطر الموضوع للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="87093-121">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="87093-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="87093-122">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="87093-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="87093-123">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="87093-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="87093-124">في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="87093-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="87093-125">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="87093-125">Click **Insert**.</span></span>

4. <span data-ttu-id="87093-126">لإضافة ترجمات سطر الموضوع، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="87093-127">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="87093-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="87093-128">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87093-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="87093-129">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="87093-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="87093-130">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="87093-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="87093-131">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="87093-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="87093-132">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="87093-132">Click **Close**.</span></span>

5. <span data-ttu-id="87093-133">في حقل **إرشادات عنصر العمل**، أدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="87093-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="87093-134">لتخصيص الإرشادات، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="87093-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="87093-135">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما تظهر الإرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="87093-136">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="87093-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="87093-137">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="87093-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="87093-138">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="87093-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="87093-139">في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="87093-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="87093-140">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="87093-140">Click **Insert**.</span></span>

7. <span data-ttu-id="87093-141">لإضافة ترجمات الإرشادات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="87093-142">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="87093-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="87093-143">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87093-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="87093-144">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="87093-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="87093-145">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="87093-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="87093-146">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 6.</span><span class="sxs-lookup"><span data-stu-id="87093-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="87093-147">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="87093-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="87093-148">تعيين المهمة</span><span class="sxs-lookup"><span data-stu-id="87093-148">Assign the task</span></span>

<span data-ttu-id="87093-149">اتبع الخطوات التالية لتحديد الشخص الذي ينبغي تعيين المهمة اليدوية له.</span><span class="sxs-lookup"><span data-stu-id="87093-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="87093-150">في الجزء الأيمن، انقر فوق **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="87093-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="87093-151">على علامة التبويب **نوع التعيين**، حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="87093-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="87093-152">خيار</span><span class="sxs-lookup"><span data-stu-id="87093-152">Option</span></span></th>
    <th><span data-ttu-id="87093-153">المستخدمون الذين تم تعيين المهمة‬ لهم</span><span class="sxs-lookup"><span data-stu-id="87093-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="87093-154">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="87093-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="87093-155">المشارك</span><span class="sxs-lookup"><span data-stu-id="87093-155">Participant</span></span></td>
    <td><span data-ttu-id="87093-156">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="87093-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-157">بعد تحديد <strong>المشارك</strong>، على علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لتعيين المهمة إليه.</span><span class="sxs-lookup"><span data-stu-id="87093-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="87093-158">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لتعيين المهمة إليه.</span><span class="sxs-lookup"><span data-stu-id="87093-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-159">التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="87093-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="87093-160">المستخدمون في تدرج هرمي محدد للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="87093-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-161">بعد تحديد <strong>التدرج الهرمي</strong>، على علامة التبويب <strong>تحديد التدرج الهرمي</strong>، في قائمة <strong>نوع التدرج الهرمي</strong>، حدد نوع التدرج الهرمي لتعيين المهمة له.</span><span class="sxs-lookup"><span data-stu-id="87093-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="87093-162">يجب أن يقوم النظام باسترداد نطاق أسماء المستخدمين من التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="87093-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="87093-163">تمثل هذه الأسماء المستخدمين الذين يمكن تعيين المهمة لهم.</span><span class="sxs-lookup"><span data-stu-id="87093-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="87093-164">اتبع هذه الخطوات لتحديد نقطة البداية ونقطة الانتهاء في نطاق أسماء المستخدمين الذي يقوم النظام باسترداده.</span><span class="sxs-lookup"><span data-stu-id="87093-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="87093-165">لتحديد نقطة البداية، حدد شخصًا من القائمة <strong>البدء من</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="87093-166">لتحديد نقطة النهاية، انقر فوق <strong>إضافة شرط‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="87093-167">بعد ذلك، أدخل شرطًا يحدد المكان في التدرج الهرمي حيث يتوقف النظام عن استرداد الأسماء.</span><span class="sxs-lookup"><span data-stu-id="87093-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="87093-168">على علامة التبويب <strong>خيارات التدرج الهرمي</strong>، حدد المستخدمين في النطاق الذين يجب تعيين المهمة إليهم:</span><span class="sxs-lookup"><span data-stu-id="87093-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="87093-169"><strong>التعيين لكافة المستخدمين الذين تم استردادهم‬</strong> – يتم تعيين المهمة لكافة المستخدمين الموجودين في النطاق.</span><span class="sxs-lookup"><span data-stu-id="87093-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="87093-170"><strong>التعيين لآخر مستخدم تم استرداده فقط</strong> – يتم تعيين المهمة للمستخدم الأخير فقط الموجود في النطاق.</span><span class="sxs-lookup"><span data-stu-id="87093-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="87093-171"><strong>استبعاد المستخدمين الذين يستوفون الشرط التالي</strong> - لا يتم تعيين المهمة للمستخدمين في النطاق الذين يستوفون شرطًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="87093-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="87093-172">انقر فوق <strong>إضافة شرط</strong> لتحديد الشرط.</span><span class="sxs-lookup"><span data-stu-id="87093-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-173">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="87093-173">Workflow user</span></span></td>
    <td><span data-ttu-id="87093-174">المستخدمون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="87093-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="87093-175">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="87093-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-176">المستخدم</span><span class="sxs-lookup"><span data-stu-id="87093-176">User</span></span></td>
    <td><span data-ttu-id="87093-177">مستخدمون محددون</span><span class="sxs-lookup"><span data-stu-id="87093-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-178">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="87093-179">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="87093-180">حدد المستخدمين المراد تعيين المهمة لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-181">قائمة الانتظار</span><span class="sxs-lookup"><span data-stu-id="87093-181">Queue</span></span></td>
    <td><span data-ttu-id="87093-182">قائمة انتظار عناصر العمل</span><span class="sxs-lookup"><span data-stu-id="87093-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-183">بعد تحديد <strong>قائمة انتظار</strong>، انقر فوق علامة التبويب <strong>مستند إلى قائمة الانتظار</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="87093-184">لتعيين المهمة إلى قائمة انتظار معينة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="87093-185">في قائمة <strong>نوع قائمة الانتظار</strong>، حدد <strong>قوائم انتظار عناصر العمل‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="87093-186">في قائمة <strong>اسم قائمة الانتظار</strong>، حدد قائمة الانتظار.</span><span class="sxs-lookup"><span data-stu-id="87093-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="87093-187">إذا كان يتعين تحديد قائمة الانتظار التي يجب تعيين المهمة لها بواسطة شرط محدد، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="87093-188">في قائمة <strong>نوع قائمة الانتظار</strong>، حدد <strong>قوائم انتظار عناصر عمل شرطية‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="87093-189">في قائمة <strong>اسم قائمة الانتظار</strong>، حدد <strong>قائمة انتظار شرطية</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="87093-190">يتم استخدام هذا الخيار لبعض مهام سير العمل فقط، مثل إدارة الحالات‬.</span><span class="sxs-lookup"><span data-stu-id="87093-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="87093-191">على علامة التبويب **الحد الزمني**، في حقل **المدة**، حدد فترة الوقت التي يمكن للمستخدم خلالها إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="87093-192">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-192">Select one of the following options:</span></span>

    - <span data-ttu-id="87093-193">**الساعات** – أدخل عدد الساعات التي يجب أن يقوم المستخدم خلالها بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="87093-194">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="87093-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="87093-195">**الأيام** – أدخل عدد الأيام التي يجب أن يقوم المستخدم خلالها بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="87093-196">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="87093-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="87093-197">**الأسابيع** – أدخل عدد الأسابيع التي يجب أن يقوم المستخدم خلالها بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="87093-198">**الأشهر** - حدد اليوم والأسبوع الذي يتعين على المستخدم إكمال المهمة خلالهما.</span><span class="sxs-lookup"><span data-stu-id="87093-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="87093-199">على سبيل المثال، قد ترغب في أن يقوم المستخدم بإكمال المهمة بحلول يوم الجمعة من الأسبوع الثالث من الشهر.</span><span class="sxs-lookup"><span data-stu-id="87093-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="87093-200">**السنوات** - حدد اليوم والأسبوع والشهر الذي يتعين على المستخدم إكمال المهمة خلالها.</span><span class="sxs-lookup"><span data-stu-id="87093-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="87093-201">على سبيل المثال، قد ترغب في أن يقوم المستخدم بإكمال المهمة بحلول يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="87093-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="87093-202">إذا لم يتمكن المستخدم من إكمال المهمة في الوقت المحدد، فسيتم اعتبار المهمة متأخرة.‬</span><span class="sxs-lookup"><span data-stu-id="87093-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="87093-203">يمكن تصعيد المهمة المتأخرة، استنادًا إلى الخيارات التي تحددها في ناحية **التصعيد** في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="87093-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="87093-204">تحديد ما يحدث عندما تكون المهمة متأخرة</span><span class="sxs-lookup"><span data-stu-id="87093-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="87093-205">إذا لم يتمكن المستخدم من إكمال المهمة اليدوية في الوقت المحدد، فسيتم اعتبار المهمة متأخرة.‬</span><span class="sxs-lookup"><span data-stu-id="87093-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="87093-206">يمكن تصعيد المهمة المتأخرة، أو يمكن تعيينها تلقائيًا إلى مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="87093-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="87093-207">اتبع هذه الخطوات لتصعيد المهمة إذا كانت متأخرة.</span><span class="sxs-lookup"><span data-stu-id="87093-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="87093-208">في الجزء الأيمن، انقر فوق **التصعيد**.</span><span class="sxs-lookup"><span data-stu-id="87093-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="87093-209">حدد خانة الاختيار **استخدام مسار التصعيد** لإنشاء مسار تصعيد.</span><span class="sxs-lookup"><span data-stu-id="87093-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="87093-210">سيقوم النظام تلقائيًا بتعيين المهمة للمستخدمين المذكورين في مسار التصعيد.</span><span class="sxs-lookup"><span data-stu-id="87093-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="87093-211">على سبيل المثال، يمثل الجدول التالي مسار تصعيد.</span><span class="sxs-lookup"><span data-stu-id="87093-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="87093-212">التسلسل</span><span class="sxs-lookup"><span data-stu-id="87093-212">Sequence</span></span> | <span data-ttu-id="87093-213">مسار التصعيد</span><span class="sxs-lookup"><span data-stu-id="87093-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="87093-214">1</span><span class="sxs-lookup"><span data-stu-id="87093-214">1</span></span>        | <span data-ttu-id="87093-215">تعيين إلى: دنيا</span><span class="sxs-lookup"><span data-stu-id="87093-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="87093-216">2</span><span class="sxs-lookup"><span data-stu-id="87093-216">2</span></span>        | <span data-ttu-id="87093-217">تعيين إلى: ليلى</span><span class="sxs-lookup"><span data-stu-id="87093-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="87093-218">3</span><span class="sxs-lookup"><span data-stu-id="87093-218">3</span></span>        | <span data-ttu-id="87093-219">الإجراء الأخير: رفض</span><span class="sxs-lookup"><span data-stu-id="87093-219">Final action: Reject</span></span> |

    <span data-ttu-id="87093-220">في هذا المثال، سيقوم النظام بتعيين المهمة المتأخرة إلى دنيا.</span><span class="sxs-lookup"><span data-stu-id="87093-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="87093-221">إذا لم تتمكن دنيا من إكمال المهمة في الوقت المخصص، فسيقوم النظام بتعيين المهمة لنادية.</span><span class="sxs-lookup"><span data-stu-id="87093-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="87093-222">إذا لم تتمكن نادية من إكمال المهمة في الوقت المخصص، فسيرفض النظام المستند الذي تم إرساله للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="87093-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="87093-223">لإضافة مستخدم إلى مسار التصعيد، انقر **إضافة تصعيد**.</span><span class="sxs-lookup"><span data-stu-id="87093-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="87093-224">على علامة التبويب **نوع التعيين**، حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 4.</span><span class="sxs-lookup"><span data-stu-id="87093-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="87093-225">خيار</span><span class="sxs-lookup"><span data-stu-id="87093-225">Option</span></span></th>
    <th><span data-ttu-id="87093-226">المستخدمون الذين تم تصعيد المهمة‬ إليهم</span><span class="sxs-lookup"><span data-stu-id="87093-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="87093-227">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="87093-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="87093-228">التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="87093-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="87093-229">المستخدمون في تدرج هرمي محدد للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="87093-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-230">بعد تحديد <strong>التدرج الهرمي</strong>، على علامة التبويب <strong>تحديد التدرج الهرمي</strong>، في قائمة <strong>نوع التدرج الهرمي</strong>، حدد نوع التدرج الهرمي لتصعيد المهمة إليه.</span><span class="sxs-lookup"><span data-stu-id="87093-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="87093-231">يجب أن يقوم النظام باسترداد نطاق أسماء المستخدمين من التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="87093-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="87093-232">تمثل هذه الأسماء المستخدمين الذين يمكن تصعيد المهمة إليهم.</span><span class="sxs-lookup"><span data-stu-id="87093-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="87093-233">اتبع هذه الخطوات لتحديد نقطة البداية ونقطة الانتهاء في نطاق أسماء المستخدمين الذي يقوم النظام باسترداده.</span><span class="sxs-lookup"><span data-stu-id="87093-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="87093-234">لتحديد نقطة البداية، حدد شخصًا من القائمة <strong>البدء من</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="87093-235">لتحديد نقطة النهاية، انقر فوق <strong>إضافة شرط‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="87093-236">بعد ذلك، أدخل شرطًا يحدد المكان في التدرج الهرمي حيث يتوقف النظام عن استرداد الأسماء.</span><span class="sxs-lookup"><span data-stu-id="87093-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="87093-237">على علامة التبويب <strong>خيارات التدرج الهرمي</strong>، حدد المستخدمين في النطاق الذين يجب تصعيد المهمة إليهم:</span><span class="sxs-lookup"><span data-stu-id="87093-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="87093-238"><strong>التعيين لكافة المستخدمين الذين تم استردادهم‬</strong> – يتم تصعيد المهمة إلى كافة المستخدمين الموجودين في النطاق.</span><span class="sxs-lookup"><span data-stu-id="87093-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="87093-239"><strong>التعيين لآخر مستخدم تم استرداده فقط</strong> – يتم تصعيد المهمة إلى المستخدم الأخير فقط الموجود في النطاق.</span><span class="sxs-lookup"><span data-stu-id="87093-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="87093-240"><strong>استبعاد المستخدمين الذين يستوفون الشرط التالي</strong> - لا يتم تصعيد المهمة إلى المستخدمين في النطاق الذين يستوفون شرطًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="87093-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="87093-241">انقر فوق <strong>إضافة شرط</strong> لتحديد الشرط.</span><span class="sxs-lookup"><span data-stu-id="87093-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-242">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="87093-242">Workflow user</span></span></td>
    <td><span data-ttu-id="87093-243">المستخدمون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="87093-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="87093-244">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="87093-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-245">المستخدم</span><span class="sxs-lookup"><span data-stu-id="87093-245">User</span></span></td>
    <td><span data-ttu-id="87093-246">مستخدمون محددون</span><span class="sxs-lookup"><span data-stu-id="87093-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-247">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="87093-248">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="87093-249">حدد المستخدمين المراد تصعيد المهمة إليهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="87093-250">على علامة التبويب **الحد الزمني**، في حقل **المدة**، حدد فترة الوقت التي يمكن للمستخدم خلالها إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="87093-251">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-251">Select one of the following options:</span></span>

    - <span data-ttu-id="87093-252">**الساعات** – أدخل عدد الساعات التي يجب أن يقوم المستخدم خلالها بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="87093-253">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="87093-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="87093-254">**الأيام** – أدخل عدد الأيام التي يجب أن يقوم المستخدم خلالها بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="87093-255">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="87093-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="87093-256">**الأسابيع** – أدخل عدد الأسابيع التي يجب أن يقوم المستخدم خلالها بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="87093-257">**الأشهر** - حدد اليوم والأسبوع الذي يتعين على المستخدم إكمال المهمة خلالهما.</span><span class="sxs-lookup"><span data-stu-id="87093-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="87093-258">على سبيل المثال، قد ترغب في أن يقوم المستخدم بإكمال المهمة بحلول يوم الجمعة من الأسبوع الثالث من الشهر.</span><span class="sxs-lookup"><span data-stu-id="87093-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="87093-259">**السنوات** - حدد اليوم والأسبوع والشهر الذي يتعين على المستخدم إكمال المهمة خلالها.</span><span class="sxs-lookup"><span data-stu-id="87093-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="87093-260">على سبيل المثال، قد ترغب في أن يقوم المستخدم بإكمال المهمة بحلول يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="87093-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="87093-261">كرر الخطوتين 3 و4 لكل مستخدم يجب إضافته إلى مسار التصعيد.</span><span class="sxs-lookup"><span data-stu-id="87093-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="87093-262">يمكنك تغيير ترتيب المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="87093-263">إذا لم يتمكن المستخدمون في مسار التصعيد من إكمال المهمة في الوقت المخصص، فسيقوم النظام تلقائيًا باتخاذ الإجراء المناسب على المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="87093-264">لتحديد الإجراء الذي يتخذه النظام، حدد الصف **إجراء**، ثم، على علامة التبويب **إجراء الإنهاء‬**، حدد أحد الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="87093-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="87093-265">تحديد الوقت الذي يعمل فيه النظام تلقائيًا على المهمة</span><span class="sxs-lookup"><span data-stu-id="87093-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="87093-266">يمكنك تكوين النظام بحيث يتخذ الإجراء المناسب على المهمة اليدوية عند استيفاء شروط محددة.</span><span class="sxs-lookup"><span data-stu-id="87093-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="87093-267">على سبيل المثال، تتطلب إحدى المهام أن يقوم أحد أعضاء قسم تقارير المصروفات بمراجعة الإيصالات التي تم إرسالها إلى جانب تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="87093-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="87093-268">‏‫وفقًا لسياسة الشركة، يجب تنفيذ هذه المهمة إذا كان المبلغ الإجمالي لتقرير المصروفات أكثر من 100 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="87093-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="87093-269">في هذا السيناريو، يمكنك تكوين النظام ليتم تلقائيًا وضع علامة على المهمة على أنها **مكتملة** عندما يكون المبلغ الإجمالي أقل من 100.</span><span class="sxs-lookup"><span data-stu-id="87093-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="87093-270">اتبع هذه الخطوات لتحديد الوقت الذي يقوم فيه النظام باتخاذ إجراء ما على المهمة اليدوية.</span><span class="sxs-lookup"><span data-stu-id="87093-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="87093-271">في الجزء الأيمن، انقر فوق **إجراءات تلقائية‬**.</span><span class="sxs-lookup"><span data-stu-id="87093-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="87093-272">حدد خانة الاختيار **تمكين الإجراءات التلقائية**.</span><span class="sxs-lookup"><span data-stu-id="87093-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="87093-273">انقر فوق **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="87093-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="87093-274">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="87093-274">Enter a condition.</span></span>
5. <span data-ttu-id="87093-275">أدخل أية شروط إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="87093-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="87093-276">للتأكد من تكوين الشروط التي قمت بإدخالها بشكل صحيح، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="87093-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="87093-277">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="87093-277">Click **Test**.</span></span>
    2. <span data-ttu-id="87093-278">في صفحة **اختبار حالة سير العمل**، في الناحية **التحقق من صحة الشرط‬**، حدد سجلاً.</span><span class="sxs-lookup"><span data-stu-id="87093-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="87093-279">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="87093-279">Click **Test**.</span></span> <span data-ttu-id="87093-280">سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.</span><span class="sxs-lookup"><span data-stu-id="87093-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="87093-281">انقر فوق **موافق** أو **إلغاء الأمر** للرجوع إلى الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="87093-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="87093-282">من القائمة **إجراء الإكمال التلقائي**، حدد الإجراء الذي يجب أن يتخذه النظام على المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="87093-283">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="87093-283">Specify when notifications are sent</span></span>

<span data-ttu-id="87093-284">يمكن إرسال الإخطارات إلى الأشخاص عند اكتمال مهمة يدوية تم تفويضها أو تصعيدها أو رفضها، أو عند طلب إجراء تغيير.</span><span class="sxs-lookup"><span data-stu-id="87093-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="87093-285">اتبع هذه الخطوات لتحديد الوقت الذي يتم فيه ارسال الإخطارات، والأشخاص الذين يتم إرسال الإخطارات إليهم.</span><span class="sxs-lookup"><span data-stu-id="87093-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="87093-286">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="87093-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="87093-287">حدد خانة الاختيار إلى جانب الأحداث التي يجب إرسال الإخطارات بشأنها:</span><span class="sxs-lookup"><span data-stu-id="87093-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="87093-288">**التفويض** – تم تعيين المهمة إلى مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="87093-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="87093-289">**التصعيد** – لم يتمكن المستخدم المعين من إكمال المهمة في الوقت المخصص لها.</span><span class="sxs-lookup"><span data-stu-id="87093-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="87093-290">**إكمال‬** – قام المستخدم المعين بإكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="87093-291">**رفض** – قام المستخدم المعين برفض المستند الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="87093-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="87093-292">**طلب تغيير** – طالب المستخدم المعين بإجراء تغيير على المستند الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="87093-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="87093-293">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="87093-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="87093-294">على علامة التبويب **نص الإخطار‬**، في مربع النص، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="87093-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="87093-295">لتخصيص الإخطار، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="87093-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="87093-296">يتم استبدال العناصر النائبة بالمعلومات المناسبة عندما يظهر الإخطار للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="87093-297">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="87093-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="87093-298">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="87093-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="87093-299">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="87093-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="87093-300">في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="87093-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="87093-301">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="87093-301">Click **Insert**.</span></span>

6. <span data-ttu-id="87093-302">لإضافة ترجمات الإخطارات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="87093-303">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="87093-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="87093-304">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87093-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="87093-305">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="87093-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="87093-306">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="87093-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="87093-307">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 5.</span><span class="sxs-lookup"><span data-stu-id="87093-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="87093-308">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="87093-308">Click **Close**.</span></span>

7. <span data-ttu-id="87093-309">على علامة تبويب **المستلم**، حدد الشخص الذي يتم إرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="87093-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="87093-310">حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="87093-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="87093-311">خيار</span><span class="sxs-lookup"><span data-stu-id="87093-311">Option</span></span></th>
    <th><span data-ttu-id="87093-312">مستلمو الإخطارات</span><span class="sxs-lookup"><span data-stu-id="87093-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="87093-313">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="87093-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="87093-314">المشارك</span><span class="sxs-lookup"><span data-stu-id="87093-314">Participant</span></span></td>
    <td><span data-ttu-id="87093-315">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="87093-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-316">بعد تحديد <strong>المشارك</strong>، على علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="87093-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="87093-317">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="87093-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-318">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="87093-318">Workflow user</span></span></td>
    <td><span data-ttu-id="87093-319">المستخدمون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="87093-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="87093-320">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="87093-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="87093-321">المستخدم</span><span class="sxs-lookup"><span data-stu-id="87093-321">User</span></span></td>
    <td><span data-ttu-id="87093-322">مستخدمون محددون</span><span class="sxs-lookup"><span data-stu-id="87093-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="87093-323">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="87093-324">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="87093-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="87093-325">حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="87093-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="87093-326">كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="87093-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="87093-327">قم بتعيين حد زمني</span><span class="sxs-lookup"><span data-stu-id="87093-327">Set a time limit</span></span>

<span data-ttu-id="87093-328">اتبع الخطوات التالية إذا كان يجب إكمال المهمة اليدوية في وقت معين.</span><span class="sxs-lookup"><span data-stu-id="87093-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="87093-329">ستقوم الخيارات التي تحددها هنا بتجاوز الخيارات التي حددتها في ناحيتي **التعيين** و**التصعيد** على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="87093-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="87093-330">في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="87093-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="87093-331">حدد خانة الاختيار **تعيين حد زمني لعنصر سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="87093-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="87093-332">في حقل **المدة**، حدد الوقت الذي يجب خلاله إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="87093-333">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="87093-333">Select one of the following options:</span></span>

    - <span data-ttu-id="87093-334">**الساعات** – أدخل عدد الساعات التي يجب خلالها إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="87093-335">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="87093-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="87093-336">**الأيام** – أدخل عدد الأيام التي يجب خلالها إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="87093-337">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="87093-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="87093-338">**الأسابيع** – أدخل عدد الأسابيع التي يجب خلالها إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="87093-339">**الأشهر** - حدد اليوم والأسبوع الذي يتعين إكمال المهمة خلالهما.</span><span class="sxs-lookup"><span data-stu-id="87093-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="87093-340">على سبيل المثال، قد ترغب في أن يتم إكمال المهمة بحلول يوم الجمعة من الأسبوع الثالث من الشهر.</span><span class="sxs-lookup"><span data-stu-id="87093-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="87093-341">**السنوات** - حدد اليوم والأسبوع والشهر الذي يتعين إكمال المهمة خلالها.</span><span class="sxs-lookup"><span data-stu-id="87093-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="87093-342">على سبيل المثال، قد ترغب في أن يتم إكمال المهمة بحلول يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="87093-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="87093-343">إذا تم تجاوز الحد الزمني فسيقوم النظام باتخاذ الإجراء المناسب على المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="87093-344">من القائمة **إجراء**، حدد الإجراء الذي يجب أن يقوم النظام باتخاذه.</span><span class="sxs-lookup"><span data-stu-id="87093-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="87093-345">تحديد الإجراءات المتاحة للمستخدم</span><span class="sxs-lookup"><span data-stu-id="87093-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="87093-346">عند تعيين مهمة يدوية إلى المستخدم، يجب على هذا المستخدم اتخاذ الإجراء المناسب على المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="87093-347">اتبع هذه الخطوات لتحديد الإجراءات التي يمكن للمستخدم اتخاذها على المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="87093-348">تختلف الإجراءات المتاحة استنادًا إلى تصميم المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="87093-349">في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="87093-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="87093-350">حدد خانة الاختيار **إكمال** إذا كان من المفترض أن يكون المستخدم قادرًا على وضع علامة على المهمة على أنها **مكتملة**.</span><span class="sxs-lookup"><span data-stu-id="87093-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="87093-351">حدد خانة الاختيار **رفض** إذا كان من المفترض أن يكون المستخدم قادرًا على رفض المستند الذي تم تقديمه.</span><span class="sxs-lookup"><span data-stu-id="87093-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="87093-352">حدد خانة الاختيار **طلب تغيير** إذا كان من المفترض أن يكون المستخدم قادرًا على طلب إجراء تغييرات في المستند الذي تم تقديمه.</span><span class="sxs-lookup"><span data-stu-id="87093-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="87093-353">حدد خانة الاختيار **تفويض** إذا كان من المفترض أن يكون المستخدم قادرًا على تعيين المهمة إلى مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="87093-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="87093-354">حدد خانة الاختيار **إعادة تعيين** إذا كان من المفترض أن يكون المستخدم قادرًا على إعادة تعيين المهمة إلى مستخدم آخر في قائمة انتظار عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="87093-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="87093-355">حدد خانة الاختيار **تحرير** إذا كان من المفترض أن يكون المستخدم قادرًا على إعادة تعيين المهمة في قائمة انتظار عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="87093-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="87093-356">عندئذٍ، سيكون باستطاعة مستخدم آخر إكمال المهمة.</span><span class="sxs-lookup"><span data-stu-id="87093-356">Another user can then complete the task.</span></span>
