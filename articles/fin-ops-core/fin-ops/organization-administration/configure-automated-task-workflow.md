---
title: تكوين المهام المؤتمتة في سير عمل
description: يوضح هذا الموضوع كيفية تكوين خصائص مهمة تلقائية.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ca46e6c69b8e823be15f3e039408017e6463406
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698257"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="d4a39-103">تكوين المهام المؤتمتة في سير عمل</span><span class="sxs-lookup"><span data-stu-id="d4a39-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4a39-104">يوضح هذا الموضوع كيفية تكوين خصائص مهمة تلقائية.</span><span class="sxs-lookup"><span data-stu-id="d4a39-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="d4a39-105">لتكوين مهمة تلقائية في محرر سير العمل، انقر بزر الماوس الأيمن فوق المهمة، وثم انقر فوق **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="d4a39-106">ثم استخدم الإجراءات التالية لتكوين خصائص المهمة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="d4a39-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="d4a39-107">تسمية المهمة</span><span class="sxs-lookup"><span data-stu-id="d4a39-107">Name the task</span></span>

<span data-ttu-id="d4a39-108">اتبع الخطوات التالية لإدخال اسم للمهمة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="d4a39-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="d4a39-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="d4a39-110">في حقل **الاسم**، أدخل اسمًا فريدًا للمهمة.</span><span class="sxs-lookup"><span data-stu-id="d4a39-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="d4a39-111">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="d4a39-111">Specify when notifications are sent</span></span>

<span data-ttu-id="d4a39-112">يمكنك إرسال الإخطارات إلى الأشخاص عند تشغيل مهمة تلقائية أو إلغائها.</span><span class="sxs-lookup"><span data-stu-id="d4a39-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="d4a39-113">اتبع هذه الخطوات لتحديد الوقت الذي يتم فيه ارسال الإخطارات، والأشخاص الذين يتم إرسال الإخطارات إليهم.</span><span class="sxs-lookup"><span data-stu-id="d4a39-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="d4a39-114">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="d4a39-115">حدد خانة الاختيار إلى جانب الأحداث التي يجب إرسال الإخطارات بشأنها:</span><span class="sxs-lookup"><span data-stu-id="d4a39-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="d4a39-116">**التنفيذ** – يتم إرسال الإخطارات عند تشغيل المهمة.</span><span class="sxs-lookup"><span data-stu-id="d4a39-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="d4a39-117">**مُلغى‬** – يتم إرسال الإخطارات عند إلغاء المهمة.</span><span class="sxs-lookup"><span data-stu-id="d4a39-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="d4a39-118">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="d4a39-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="d4a39-119">على علامة التبويب **نص الإخطار‬**، في مربع النص، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="d4a39-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="d4a39-120">لتخصيص الإخطار، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="d4a39-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="d4a39-121">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر الإخطار للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="d4a39-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="d4a39-122">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="d4a39-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="d4a39-123">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="d4a39-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="d4a39-124">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="d4a39-125">في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="d4a39-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="d4a39-126">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-126">Click **Insert**.</span></span>

6. <span data-ttu-id="d4a39-127">لإضافة ترجمات الإخطارات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="d4a39-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="d4a39-128">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="d4a39-129">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="d4a39-130">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="d4a39-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="d4a39-131">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="d4a39-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="d4a39-132">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 5.</span><span class="sxs-lookup"><span data-stu-id="d4a39-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="d4a39-133">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="d4a39-133">Click **Close**.</span></span>

7. <span data-ttu-id="d4a39-134">على علامة تبويب **المستلم**، حدد الشخص الذي يتم إرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="d4a39-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="d4a39-135">حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="d4a39-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="d4a39-136">خيار</span><span class="sxs-lookup"><span data-stu-id="d4a39-136">Option</span></span></th>
    <th><span data-ttu-id="d4a39-137">مستلمو الإخطارات</span><span class="sxs-lookup"><span data-stu-id="d4a39-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="d4a39-138">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="d4a39-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="d4a39-139">المشارك</span><span class="sxs-lookup"><span data-stu-id="d4a39-139">Participant</span></span></td>
    <td><span data-ttu-id="d4a39-140">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="d4a39-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="d4a39-141">بعد تحديد <strong>المشارك</strong>، على علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="d4a39-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="d4a39-142">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="d4a39-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="d4a39-143">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="d4a39-143">Workflow user</span></span></td>
    <td><span data-ttu-id="d4a39-144">المستخدمون المشاركون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="d4a39-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="d4a39-145">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="d4a39-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="d4a39-146">المستخدم</span><span class="sxs-lookup"><span data-stu-id="d4a39-146">User</span></span></td>
    <td><span data-ttu-id="d4a39-147">مستخدمون محددون</span><span class="sxs-lookup"><span data-stu-id="d4a39-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="d4a39-148">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4a39-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="d4a39-149">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="d4a39-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="d4a39-150">حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4a39-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="d4a39-151">كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="d4a39-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>