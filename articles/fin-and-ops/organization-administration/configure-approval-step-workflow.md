---
title: "تكوين خطوة اعتماد في سير عمل"
description: "يوضح هذا الموضوع كيفية تكوين خصائص خطوة اعتماد."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b403a6f01a6c7ba95c2dd1cfd3bae8e58f0c6879
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="configure-an-approval-step-in-a-workflow"></a><span data-ttu-id="6a849-103">تكوين خطوة اعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="6a849-103">Configure an approval step in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6a849-104">يوضح هذا الموضوع كيفية تكوين خصائص خطوة اعتماد.</span><span class="sxs-lookup"><span data-stu-id="6a849-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="6a849-105">لتكوين خطوة اعتماد في محرر سير العمل، انقر بزر الماوس الأيمن فوق خطوة الاعتماد، وثم انقر فوق **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="6a849-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="6a849-106">ثم استخدم الإجراءات التالية لتكوين خصائص خطوة الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="6a849-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="6a849-107">تسمية الخطوة</span><span class="sxs-lookup"><span data-stu-id="6a849-107">Name the step</span></span>
<span data-ttu-id="6a849-108">اتبع الخطوات التالية لإدخال اسم لخطوة الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="6a849-108">Follow these steps to enter a name for the approval step.</span></span>

1.  <span data-ttu-id="6a849-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="6a849-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6a849-110">في حقل **الاسم**، أدخل اسمًا فريدًا لخطوة الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="6a849-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="6a849-111">أدخل سطر الموضوع والإرشادات</span><span class="sxs-lookup"><span data-stu-id="6a849-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="6a849-112">يجب توفير سطر موضوع وتعليمات للمستخدمين الذين تم تعيينهم إلى خطوة الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="6a849-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="6a849-113">على سبيل المثال، إذا كنت تقوم بتكوين خطوة اعتماد لطلبات الشراء، يرى المستخدم الذي تم تعيينه إلى الخطوة سطر الموضوع والتعليمات على صفحة **طلبات الشراء**.</span><span class="sxs-lookup"><span data-stu-id="6a849-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="6a849-114">يظهر سطر الموضوع في شريط الرسائل على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a849-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="6a849-115">وسيتمكن المستخدم عندئذٍ من النقر فوق الأيقونة في شريط الرسائل لرؤية التعليمات.</span><span class="sxs-lookup"><span data-stu-id="6a849-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="6a849-116">اتبع الخطوات التالية لإدخال سطر موضوع وتعليمات.</span><span class="sxs-lookup"><span data-stu-id="6a849-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="6a849-117">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="6a849-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6a849-118">في حقل **موضوع عنصر العمل**، أدخل سطر الموضوع.</span><span class="sxs-lookup"><span data-stu-id="6a849-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="6a849-119">لتخصيص سطر الموضوع، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="6a849-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="6a849-120">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر سطر الموضوع للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="6a849-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="6a849-121">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="6a849-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6a849-122">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="6a849-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6a849-123">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="6a849-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6a849-124">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="6a849-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6a849-125">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="6a849-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="6a849-126">لإضافة ترجمات سطر الموضوع، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a849-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="6a849-127">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="6a849-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6a849-128">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="6a849-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6a849-129">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="6a849-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6a849-130">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="6a849-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6a849-131">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="6a849-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="6a849-132">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="6a849-132">Click **Close**.</span></span>

5.  <span data-ttu-id="6a849-133">في حقل **إرشادات عنصر العمل**، أدخل الإرشادات.</span><span class="sxs-lookup"><span data-stu-id="6a849-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="6a849-134">لتخصيص الإرشادات، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="6a849-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="6a849-135">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما تظهر الإرشادات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="6a849-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="6a849-136">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="6a849-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6a849-137">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="6a849-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6a849-138">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="6a849-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6a849-139">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="6a849-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6a849-140">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="6a849-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="6a849-141">لإضافة ترجمات الإرشادات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a849-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="6a849-142">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="6a849-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6a849-143">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="6a849-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6a849-144">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="6a849-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6a849-145">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="6a849-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6a849-146">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 6.</span><span class="sxs-lookup"><span data-stu-id="6a849-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="6a849-147">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="6a849-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="6a849-148">تعيين خطوة الاعتماد</span><span class="sxs-lookup"><span data-stu-id="6a849-148">Assign the approval step</span></span>
<span data-ttu-id="6a849-149">اتبع الخطوات التالية لتحديد الشخص الذي ينبغي تعيين خطوة الاعتماد له.</span><span class="sxs-lookup"><span data-stu-id="6a849-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1.  <span data-ttu-id="6a849-150">في الجزء الأيمن، انقر فوق **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="6a849-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="6a849-151">على علامة التبويب **نوع التعيين**، حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="6a849-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6a849-152">خيار</span><span class="sxs-lookup"><span data-stu-id="6a849-152">Option</span></span></th>
    <th><span data-ttu-id="6a849-153">المستخدمون الذين تم تعيين خطوة الاعتماد‬ لهم</span><span class="sxs-lookup"><span data-stu-id="6a849-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="6a849-154">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a849-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6a849-155">المشارك</span><span class="sxs-lookup"><span data-stu-id="6a849-155">Participant</span></span></td>
    <td><span data-ttu-id="6a849-156">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="6a849-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6a849-157">بعد تحديد <strong>المشارك</strong>، على علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لتعيين الخطوة إليه.</span><span class="sxs-lookup"><span data-stu-id="6a849-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="6a849-158">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لتعيين الخطوة إليه.</span><span class="sxs-lookup"><span data-stu-id="6a849-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6a849-159">التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="6a849-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="6a849-160">المستخدمون في تدرج هرمي محدد للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="6a849-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6a849-161">بعد تحديد <strong>التدرج الهرمي</strong>، على علامة التبويب <strong>تحديد التدرج الهرمي</strong>، في قائمة <strong>نوع التدرج الهرمي</strong>، حدد نوع التدرج الهرمي لتعيين الخطوة إليه.</span><span class="sxs-lookup"><span data-stu-id="6a849-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="6a849-162">يجب أن يقوم النظام باسترداد نطاق أسماء المستخدمين من التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="6a849-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="6a849-163">تمثل هذه الأسماء المستخدمين الذين يمكن تعيين الخطوة لهم.</span><span class="sxs-lookup"><span data-stu-id="6a849-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="6a849-164">اتبع هذه الخطوات لتحديد نقطة البداية ونقطة الانتهاء في نطاق أسماء المستخدمين الذي يقوم النظام باسترداده.</span><span class="sxs-lookup"><span data-stu-id="6a849-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="6a849-165">لتحديد نقطة البداية، حدد شخصًا من القائمة <strong>البدء من</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="6a849-166">لتحديد نقطة النهاية، انقر فوق <strong>إضافة شرط‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="6a849-167">بعد ذلك، أدخل شرطًا يحدد المكان في التدرج الهرمي حيث يتوقف النظام عن استرداد الأسماء.</span><span class="sxs-lookup"><span data-stu-id="6a849-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6a849-168">على علامة التبويب <strong>خيارات التدرج الهرمي</strong>، حدد المستخدمين في النطاق الذين يجب تعيين الخطوة إليهم:</span><span class="sxs-lookup"><span data-stu-id="6a849-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="6a849-169"><strong>التعيين لكافة المستخدمين الذين تم استردادهم‬</strong> – يتم تعيين الخطوة لكافة المستخدمين الموجودين في النطاق.</span><span class="sxs-lookup"><span data-stu-id="6a849-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="6a849-170"><strong>التعيين لآخر مستخدم تم استرداده فقط</strong> – يتم تعيين الخطوة للمستخدم الأخير فقط الموجود في النطاق.</span><span class="sxs-lookup"><span data-stu-id="6a849-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="6a849-171"><strong>استبعاد المستخدمين الذين يستوفون الشرط التالي</strong> - لا يتم تعيين الخطوة لأي من المستخدمين في النطاق الذين يستوفون شرطًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="6a849-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="6a849-172">انقر فوق <strong>إضافة شرط</strong> لتحديد الشرط.</span><span class="sxs-lookup"><span data-stu-id="6a849-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6a849-173">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="6a849-173">Workflow user</span></span></td>
    <td><span data-ttu-id="6a849-174">المستخدمون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="6a849-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6a849-175">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a849-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6a849-176">المستخدم</span><span class="sxs-lookup"><span data-stu-id="6a849-176">User</span></span></td>
    <td><span data-ttu-id="6a849-177">‏‫مستخدمو Microsoft Dynamics 365 for Finance and Operations معينون‬</span><span class="sxs-lookup"><span data-stu-id="6a849-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6a849-178">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6a849-179">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع مستخدمي Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a849-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6a849-180">حدد المستخدمين المراد تعيين الخطوة لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="6a849-181">على علامة التبويب **الحد الزمني**، في حقل **المدة**، حدد فترة الوقت التي يمكن للمستخدم خلالها اتخاذ إجراء ما يتعلق بالمستندات التي تصل إلى خطوة الاعتماد أو الاستجابة لها.</span><span class="sxs-lookup"><span data-stu-id="6a849-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="6a849-182">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a849-182">Select one of the following options:</span></span>
    -   <span data-ttu-id="6a849-183">**الساعات** – أدخل عدد الساعات التي يجب أن يستجيب خلالها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6a849-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="6a849-184">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="6a849-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6a849-185">**الأيام** – أدخل عدد الأيام التي يجب أن يستجيب خلالها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6a849-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="6a849-186">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="6a849-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6a849-187">**الأسابيع** – أدخل عدد الأسابيع التي يجب أن يستجيب خلالها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6a849-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    -   <span data-ttu-id="6a849-188">**الأشهر** - حدد اليوم والأسبوع الذي يتعين على المستخدم الاستجابة خلالهما.</span><span class="sxs-lookup"><span data-stu-id="6a849-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="6a849-189">على سبيل المثال، قد ترغب في أن يستجيب المستخدم بحلول يوم الجمعة من الأسبوع الثالث من الشهر.</span><span class="sxs-lookup"><span data-stu-id="6a849-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6a849-190">**السنوات** - حدد اليوم والأسبوع والشهر الذي يتعين على المستخدم الاستجابة خلالها.</span><span class="sxs-lookup"><span data-stu-id="6a849-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="6a849-191">على سبيل المثال، قد ترغب في أن يستجيب المستخدم بحلول يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="6a849-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="6a849-192">إذا لم يتخذ المستخدم أي إجراء بشأن المستند في الوقت المحدد، فسيتم اعتبار المستند متأخرًا.‬</span><span class="sxs-lookup"><span data-stu-id="6a849-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="6a849-193">يتم تصعيد المستند المتأخر، استنادًا إلى الخيارات التي تحددها في ناحية **التصعيد** في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a849-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>
4.  <span data-ttu-id="6a849-194">إذا قمت بتعيين خطوة الاعتماد لعدة مستخدمين أو مجموعة مستخدمين، على علامة التبويب **سياسة الإكمال**، حدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a849-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>
    -   <span data-ttu-id="6a849-195">**معتمد واحد** – سيتم تحديد الإجراء المطبَّق على المستند من قِبل أول شخص مستجيب.</span><span class="sxs-lookup"><span data-stu-id="6a849-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="6a849-196">على سبيل المثال، قام سامي بتقديم تقرير مصروفات بمبلغ 15,000 دولار.</span><span class="sxs-lookup"><span data-stu-id="6a849-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6a849-197">تم تعيين تقرير المصروفات حاليًا لكل من سمر وهبة وهاني.</span><span class="sxs-lookup"><span data-stu-id="6a849-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="6a849-198">فإذا كانت سمر أول شخص يستجيب للمستند، فسيتم تطبيق الإجراء الذي تتخذه على المستند.</span><span class="sxs-lookup"><span data-stu-id="6a849-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="6a849-199">أما إذا قامت سمر برفض المستند، فسيتم رفضه وإرجاعه إلى سامي.</span><span class="sxs-lookup"><span data-stu-id="6a849-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="6a849-200">وبعد أن تعتمد سمر المستند، يتم إرساله إلى أمل لاعتماده.</span><span class="sxs-lookup"><span data-stu-id="6a849-200">If Sue approves the document, it's sent to Ann for approval.</span></span> 
    
    ![سير عمل لديه عملية اعتماد](./media/workflow_multipleusersinstep.gif)
    
    -   <span data-ttu-id="6a849-202">**أغلبية المعتمدين‬** – سيتم تحديد الإجراء المطبَّق على المستند عند استجابة أغلبية المعتمدين.</span><span class="sxs-lookup"><span data-stu-id="6a849-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="6a849-203">على سبيل المثال، قام سامي بتقديم تقرير مصروفات بمبلغ 15,000 دولار.</span><span class="sxs-lookup"><span data-stu-id="6a849-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6a849-204">تم تعيين تقرير المصروفات حاليًا لكل من سمر وهبة وهاني.</span><span class="sxs-lookup"><span data-stu-id="6a849-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="6a849-205">إذا كان كل من سمر وهبة أول شخصين مستجيبين، فسيتم تطبيق الإجراء المتخذ من قِبلهما على المستند.</span><span class="sxs-lookup"><span data-stu-id="6a849-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>
        -   <span data-ttu-id="6a849-206">إذا تم اعتماد المستند من قِبل سمر ولكن هبة رفضته، فسيتم رفض المستند وإرجاعه إلى سامي.</span><span class="sxs-lookup"><span data-stu-id="6a849-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        -   <span data-ttu-id="6a849-207">إذا تم اعتماد المستند من قِبل كل من سمر وهبة، فسيتم إرساله إلى أمل لاعتماده.</span><span class="sxs-lookup"><span data-stu-id="6a849-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>
    -   <span data-ttu-id="6a849-208">**نسبة المعتمدين** – يتم تحديد الإجراء المطبَّق على المستند عند استجابة نسبة معينة من المعتمدين.</span><span class="sxs-lookup"><span data-stu-id="6a849-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="6a849-209">على سبيل المثال، قام سامي بتقديم تقرير مصروفات بمبلغ 15,000 دولار.</span><span class="sxs-lookup"><span data-stu-id="6a849-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6a849-210">تم تعيين تقرير المصروفات حاليًا إلى كل من سمر وهبة وهاني، وقمت بإدخال **50** كالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="6a849-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="6a849-211">إذا كان كل من سمر وهبة أول شخصين مستجيبين من المعتمدين، فسيتم تطبيق الإجراء المتخذ من قِبلهما على المستند، لأنهما يلبيان المطلب المتعلق بنسبة 50 في المائة من المعتمدين.</span><span class="sxs-lookup"><span data-stu-id="6a849-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>
        -   <span data-ttu-id="6a849-212">إذا تم اعتماد المستند من قِبل سمر ولكن هبة رفضته، فسيتم رفض المستند وإرجاعه إلى سامي.</span><span class="sxs-lookup"><span data-stu-id="6a849-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        -   <span data-ttu-id="6a849-213">إذا تم اعتماد المستند من قِبل كل من سمر وهبة، فسيتم إرساله إلى أمل لاعتماده.</span><span class="sxs-lookup"><span data-stu-id="6a849-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>
    -   <span data-ttu-id="6a849-214">**كافة المعتمدين** – يجب على كافة المعتمدين الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="6a849-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="6a849-215">وإلا، لا يمكن متابعة سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a849-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="6a849-216">على سبيل المثال، قام سامي بتقديم تقرير مصروفات بمبلغ 15,000 دولار.</span><span class="sxs-lookup"><span data-stu-id="6a849-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6a849-217">تم تعيين تقرير المصروفات حاليًا لكل من سمر وهبة وهاني.</span><span class="sxs-lookup"><span data-stu-id="6a849-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="6a849-218">إذا تم اعتماد المستند من قِبل سمر وهبة، ولكن هاني رفضه، فسيتم رفض المستند وإرجاعه إلى سامي.</span><span class="sxs-lookup"><span data-stu-id="6a849-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="6a849-219">إذا تم اعتماد المستند من قِبل كل من سمر وهبة وهاني، فسيتم إرسال المستند إلى أمل لاعتماده.</span><span class="sxs-lookup"><span data-stu-id="6a849-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="6a849-220">تحديد الوقت الذي تكون فيه خطوة الاعتماد مطلوبة</span><span class="sxs-lookup"><span data-stu-id="6a849-220">Specify when the approval step is required</span></span>
<span data-ttu-id="6a849-221">يمكنك تحديد الوقت الذي تكون فيه خطوة الاعتماد مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a849-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="6a849-222">قد تكون خطوة الاعتماد مطلوبة في كل الأوقات، أو قد تكون مطلوبة فقط في حال تلبية شروط معينة.</span><span class="sxs-lookup"><span data-stu-id="6a849-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="6a849-223">خطوة الاعتماد مطلوبة دائمًا</span><span class="sxs-lookup"><span data-stu-id="6a849-223">The approval step is always required</span></span>

<span data-ttu-id="6a849-224">اتبع الخطوات التالية إذا كانت خطوة الاعتماد مطلوبة دائمًا.</span><span class="sxs-lookup"><span data-stu-id="6a849-224">Follow these steps if the approval step is always required.</span></span>

1.  <span data-ttu-id="6a849-225">في الجزء الأيمن، انقر فوق **الشرط**.</span><span class="sxs-lookup"><span data-stu-id="6a849-225">In the left pane, click **Condition**.</span></span>
2.  <span data-ttu-id="6a849-226">حدد خيار **تشغيل هذه الخطوة دائمًا**.</span><span class="sxs-lookup"><span data-stu-id="6a849-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="6a849-227">خطوة الاعتماد مطلوبة عند تلبية شروط معينة</span><span class="sxs-lookup"><span data-stu-id="6a849-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="6a849-228">قد تكون خطوة الاعتماد التي تقوم بتكوينها مطلوبة فقط عند تلبية شروط معينة.</span><span class="sxs-lookup"><span data-stu-id="6a849-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="6a849-229">على سبيل المثال، إذا كنت تقوم بتكوين خطوة اعتماد لسير عمل طلب شراء، قد تحتاج إلى حدوث خطوة الاعتماد فقط إذا كان مبلغ طلب الشراء أكثر من 10,000 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="6a849-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="6a849-230">اتبع الخطوات التالية لتحديد الوقت الذي تكون فيه خطوة الاعتماد مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a849-230">Follow these steps to specify when the approval step is required.</span></span>

1.  <span data-ttu-id="6a849-231">في الجزء الأيمن، انقر فوق **الشرط**.</span><span class="sxs-lookup"><span data-stu-id="6a849-231">In the left pane, click **Condition**.</span></span>
2.  <span data-ttu-id="6a849-232">حدد خيار **تشغيل هذه الخطوة فقط عند الوفاء بالشرط التالي**.</span><span class="sxs-lookup"><span data-stu-id="6a849-232">Select the **Run this step only when the following condition is met** option.</span></span>
3.  <span data-ttu-id="6a849-233">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="6a849-233">Enter a condition.</span></span>
4.  <span data-ttu-id="6a849-234">أدخل أية شروط إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a849-234">Enter any additional conditions that are required.</span></span>
5.  <span data-ttu-id="6a849-235">للتأكد من تكوين الشروط التي قمت بإدخالها بشكل صحيح، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="6a849-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="6a849-236">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="6a849-236">Click **Test**.</span></span>
    2.  <span data-ttu-id="6a849-237">في صفحة **اختبار حالة سير العمل**، في الناحية **التحقق من صحة الشرط‬**، حدد سجلاً.</span><span class="sxs-lookup"><span data-stu-id="6a849-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="6a849-238">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="6a849-238">Click **Test**.</span></span> <span data-ttu-id="6a849-239">سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.</span><span class="sxs-lookup"><span data-stu-id="6a849-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="6a849-240">انقر فوق **موافق** أو **إلغاء الأمر** للرجوع إلى الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="6a849-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="6a849-241">تحديد ما سيحدث عندما يكون المستند متأخرًا</span><span class="sxs-lookup"><span data-stu-id="6a849-241">Specify what happens when the document is overdue</span></span>
<span data-ttu-id="6a849-242">إذا لم يتخذ المستخدم أي إجراء بشأن مستند ما في الوقت المحدد، فسيتم اعتبار المستند متأخرًا.‬</span><span class="sxs-lookup"><span data-stu-id="6a849-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="6a849-243">يمكن تصعيد المستند المتأخر، أو يمكن تعيينه تلقائيًا إلى مستخدم آخر لاعتماده.</span><span class="sxs-lookup"><span data-stu-id="6a849-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="6a849-244">اتبع هذه الخطوات لتصعيد المستند إذا كان متأخرًا.</span><span class="sxs-lookup"><span data-stu-id="6a849-244">Follow these steps to escalate the document if it's overdue.</span></span>

1.  <span data-ttu-id="6a849-245">في الجزء الأيمن، انقر فوق **التصعيد**.</span><span class="sxs-lookup"><span data-stu-id="6a849-245">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="6a849-246">حدد خانة الاختيار **استخدام مسار التصعيد** لإنشاء مسار تصعيد.</span><span class="sxs-lookup"><span data-stu-id="6a849-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="6a849-247">سيقوم النظام تلقائيًا بتعيين المستند للمستخدمين المذكورين في مسار التصعيد.</span><span class="sxs-lookup"><span data-stu-id="6a849-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="6a849-248">على سبيل المثال، يمثل الجدول التالي مسار تصعيد.</span><span class="sxs-lookup"><span data-stu-id="6a849-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="6a849-249">التسلسل</span><span class="sxs-lookup"><span data-stu-id="6a849-249">Sequence</span></span> | <span data-ttu-id="6a849-250">مسار التصعيد</span><span class="sxs-lookup"><span data-stu-id="6a849-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="6a849-251">1</span><span class="sxs-lookup"><span data-stu-id="6a849-251">1</span></span>        | <span data-ttu-id="6a849-252">تعيين إلى: دنيا</span><span class="sxs-lookup"><span data-stu-id="6a849-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="6a849-253">2</span><span class="sxs-lookup"><span data-stu-id="6a849-253">2</span></span>        | <span data-ttu-id="6a849-254">تعيين إلى: ليلى</span><span class="sxs-lookup"><span data-stu-id="6a849-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="6a849-255">3</span><span class="sxs-lookup"><span data-stu-id="6a849-255">3</span></span>        | <span data-ttu-id="6a849-256">الإجراء الأخير: رفض</span><span class="sxs-lookup"><span data-stu-id="6a849-256">Final action: Reject</span></span> |

    <span data-ttu-id="6a849-257">في هذا المثال، سيقوم النظام بتعيين المستند المتأخر إلى دنيا.</span><span class="sxs-lookup"><span data-stu-id="6a849-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="6a849-258">إذا لم تستجب دنيا في الوقت المحدد، فسيعيّن النظام المستند إلى ليلى.</span><span class="sxs-lookup"><span data-stu-id="6a849-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="6a849-259">إذا لم تستجب ليلى في الوقت المحدد، فسيرفض النظام المستند.</span><span class="sxs-lookup"><span data-stu-id="6a849-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>
3.  <span data-ttu-id="6a849-260">لإضافة مستخدم إلى مسار التصعيد، انقر **إضافة تصعيد**.</span><span class="sxs-lookup"><span data-stu-id="6a849-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="6a849-261">على علامة التبويب **نوع التعيين**، حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 4.</span><span class="sxs-lookup"><span data-stu-id="6a849-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6a849-262">خيار</span><span class="sxs-lookup"><span data-stu-id="6a849-262">Option</span></span></th>
    <th><span data-ttu-id="6a849-263">المستخدمون الذين يتم تصعيد المستند إليهم</span><span class="sxs-lookup"><span data-stu-id="6a849-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="6a849-264">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a849-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6a849-265">التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="6a849-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="6a849-266">المستخدمون في تدرج هرمي محدد للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="6a849-266">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6a849-267">بعد تحديد <strong>التدرج الهرمي</strong>، على علامة التبويب <strong>تحديد التدرج الهرمي</strong>، في قائمة <strong>نوع التدرج الهرمي</strong>، حدد نوع التدرج الهرمي لتصعيد المستند إليه.</span><span class="sxs-lookup"><span data-stu-id="6a849-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="6a849-268">يجب أن يقوم النظام باسترداد نطاق أسماء المستخدمين من التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="6a849-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="6a849-269">تمثل هذه الأسماء المستخدمين الذين يمكن تصعيد المستند إليهم.</span><span class="sxs-lookup"><span data-stu-id="6a849-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="6a849-270">اتبع هذه الخطوات لتحديد نقطة البداية ونقطة الانتهاء في نطاق أسماء المستخدمين الذي يقوم النظام باسترداده.</span><span class="sxs-lookup"><span data-stu-id="6a849-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="6a849-271">لتحديد نقطة البداية، حدد شخصًا من القائمة <strong>البدء من</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="6a849-272">لتحديد نقطة النهاية، انقر فوق <strong>إضافة شرط‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="6a849-273">بعد ذلك، أدخل شرطًا يحدد المكان في التدرج الهرمي حيث يتوقف النظام عن استرداد الأسماء.</span><span class="sxs-lookup"><span data-stu-id="6a849-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6a849-274">على علامة التبويب <strong>خيارات التدرج الهرمي</strong>، حدد المستخدمين في النطاق الذين يجب تصعيد المستند إليهم:</span><span class="sxs-lookup"><span data-stu-id="6a849-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="6a849-275"><strong>التعيين لكافة المستخدمين الذين تم استردادهم‬</strong> – يتم تصعيد المستند لكافة المستخدمين الموجودين في النطاق.</span><span class="sxs-lookup"><span data-stu-id="6a849-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="6a849-276"><strong>التعيين لآخر مستخدم تم استرداده فقط</strong> – يتم تصعيد المستند إلى المستخدم الأخير فقط الموجود في النطاق.</span><span class="sxs-lookup"><span data-stu-id="6a849-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="6a849-277"><strong>استبعاد المستخدمين الذين يستوفون الشرط التالي</strong> - لا يتم تصعيد المستند إلى أي من المستخدمين في النطاق الذين يستوفون شرطًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="6a849-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="6a849-278">انقر فوق <strong>إضافة شرط</strong> لتحديد الشرط.</span><span class="sxs-lookup"><span data-stu-id="6a849-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6a849-279">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="6a849-279">Workflow user</span></span></td>
    <td><span data-ttu-id="6a849-280">المستخدمون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="6a849-280">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6a849-281">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a849-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6a849-282">المستخدم</span><span class="sxs-lookup"><span data-stu-id="6a849-282">User</span></span></td>
    <td><span data-ttu-id="6a849-283">مستخدمو Finance and Operations معينون</span><span class="sxs-lookup"><span data-stu-id="6a849-283">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6a849-284">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6a849-285">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع مستخدمي Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a849-285">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6a849-286">حدد المستخدمين المراد تصعيد المستند إليهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a849-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="6a849-287">على علامة التبويب **الحد الزمني**، في حقل **المدة**، حدد فترة الوقت التي يمكن للمستخدم خلالها اتخاذ إجراء ما يتعلق بالمستندات أو الاستجابة لها.</span><span class="sxs-lookup"><span data-stu-id="6a849-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="6a849-288">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a849-288">Select one of the following options:</span></span>
    -   <span data-ttu-id="6a849-289">**الساعات** – أدخل عدد الساعات التي يجب أن يستجيب خلالها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6a849-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="6a849-290">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="6a849-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6a849-291">**الأيام** – أدخل عدد الأيام التي يجب أن يستجيب خلالها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6a849-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="6a849-292">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="6a849-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6a849-293">**الأسابيع** – أدخل عدد الأسابيع التي يجب أن يستجيب خلالها المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6a849-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    -   <span data-ttu-id="6a849-294">**الأشهر** - حدد اليوم والأسبوع الذي يتعين على المستخدم الاستجابة خلالهما.</span><span class="sxs-lookup"><span data-stu-id="6a849-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="6a849-295">على سبيل المثال، قد ترغب في أن يستجيب المستخدم بحلول يوم الجمعة من الأسبوع الثالث من الشهر.</span><span class="sxs-lookup"><span data-stu-id="6a849-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6a849-296">**السنوات** - حدد اليوم والأسبوع والشهر الذي يتعين على المستخدم الاستجابة خلالها.</span><span class="sxs-lookup"><span data-stu-id="6a849-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="6a849-297">على سبيل المثال، قد ترغب في أن يستجيب المستخدم بحلول يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="6a849-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="6a849-298">كرر الخطوتين 3 و4 لكل مستخدم يجب إضافته إلى مسار التصعيد.</span><span class="sxs-lookup"><span data-stu-id="6a849-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="6a849-299">يمكنك تغيير ترتيب المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="6a849-299">You can change the order of the users.</span></span>
6.  <span data-ttu-id="6a849-300">إذا لم يستجب المستخدمون في مسار التصعيد في الوقت المخصص، فسيقوم النظام تلقائيًا باتخاذ الإجراء المناسب على المستند.</span><span class="sxs-lookup"><span data-stu-id="6a849-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="6a849-301">لتحديد الإجراء الذي يتخذه النظام، حدد الصف **إجراء**، ثم، على علامة التبويب **إجراء الإنهاء‬**، حدد أحد الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="6a849-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>




