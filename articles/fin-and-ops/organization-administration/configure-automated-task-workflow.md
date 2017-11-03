---
title: "تكوين مهمة مؤتمتة في سير عمل"
description: "يوضح هذا الموضوع كيفية تكوين خصائص مهمة تلقائية."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e8189f8d16e9b6dcbc339a23c1af5402c0316ce3
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="0a115-103">تكوين مهمة مؤتمتة في سير عمل</span><span class="sxs-lookup"><span data-stu-id="0a115-103">Configure an automated task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0a115-104">يوضح هذا الموضوع كيفية تكوين خصائص مهمة تلقائية.</span><span class="sxs-lookup"><span data-stu-id="0a115-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="0a115-105">لتكوين مهمة تلقائية في محرر سير العمل، انقر بزر الماوس الأيمن فوق المهمة، وثم انقر فوق **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="0a115-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="0a115-106">ثم استخدم الإجراءات التالية لتكوين خصائص المهمة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="0a115-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="0a115-107">تسمية المهمة</span><span class="sxs-lookup"><span data-stu-id="0a115-107">Name the task</span></span>
<span data-ttu-id="0a115-108">اتبع الخطوات التالية لإدخال اسم للمهمة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="0a115-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="0a115-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="0a115-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="0a115-110">في حقل **الاسم**، أدخل اسمًا فريدًا للمهمة.</span><span class="sxs-lookup"><span data-stu-id="0a115-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="0a115-111">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="0a115-111">Specify when notifications are sent</span></span>
<span data-ttu-id="0a115-112">يمكنك إرسال الإخطارات إلى الأشخاص عند تشغيل مهمة تلقائية أو إلغائها.</span><span class="sxs-lookup"><span data-stu-id="0a115-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="0a115-113">اتبع هذه الخطوات لتحديد الوقت الذي يتم فيه ارسال الإخطارات، والأشخاص الذين يتم إرسال الإخطارات إليهم.</span><span class="sxs-lookup"><span data-stu-id="0a115-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="0a115-114">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="0a115-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="0a115-115">حدد خانة الاختيار إلى جانب الأحداث التي يجب إرسال الإخطارات بشأنها:</span><span class="sxs-lookup"><span data-stu-id="0a115-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="0a115-116">**التنفيذ** – يتم إرسال الإخطارات عند تشغيل المهمة.</span><span class="sxs-lookup"><span data-stu-id="0a115-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="0a115-117">**مُلغى‬** – يتم إرسال الإخطارات عند إلغاء المهمة.</span><span class="sxs-lookup"><span data-stu-id="0a115-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="0a115-118">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="0a115-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="0a115-119">على علامة التبويب **نص الإخطار‬**، في مربع النص، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="0a115-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="0a115-120">لتخصيص الإخطار، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="0a115-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="0a115-121">يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر الإخطار للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="0a115-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="0a115-122">اتبع هذه الخطوات لإدراج عنصر نائب:</span><span class="sxs-lookup"><span data-stu-id="0a115-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="0a115-123">في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="0a115-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="0a115-124">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="0a115-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="0a115-125">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="0a115-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="0a115-126">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="0a115-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="0a115-127">لإضافة ترجمات الإخطارات، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a115-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="0a115-128">انقر فوق **الترجمات**.</span><span class="sxs-lookup"><span data-stu-id="0a115-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="0a115-129">في الصفحة التي تظهر، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0a115-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="0a115-130">في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="0a115-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="0a115-131">في حقل **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="0a115-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="0a115-132">لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 5.</span><span class="sxs-lookup"><span data-stu-id="0a115-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="0a115-133">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="0a115-133">Click **Close**.</span></span>

7.  <span data-ttu-id="0a115-134">على علامة تبويب **المستلم**، حدد الشخص الذي يتم إرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="0a115-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="0a115-135">حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="0a115-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="0a115-136">خيار</span><span class="sxs-lookup"><span data-stu-id="0a115-136">Option</span></span></th>
    <th><span data-ttu-id="0a115-137">مستلمو الإخطارات</span><span class="sxs-lookup"><span data-stu-id="0a115-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="0a115-138">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="0a115-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="0a115-139">المشارك</span><span class="sxs-lookup"><span data-stu-id="0a115-139">Participant</span></span></td>
    <td><span data-ttu-id="0a115-140">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="0a115-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="0a115-141">بعد تحديد <strong>المشارك</strong>، على علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="0a115-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="0a115-142">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="0a115-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="0a115-143">مستخدم سير العمل</span><span class="sxs-lookup"><span data-stu-id="0a115-143">Workflow user</span></span></td>
    <td><span data-ttu-id="0a115-144">المستخدمون المشاركون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="0a115-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="0a115-145">بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="0a115-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="0a115-146">المستخدم</span><span class="sxs-lookup"><span data-stu-id="0a115-146">User</span></span></td>
    <td><span data-ttu-id="0a115-147">‏‫مستخدمو Microsoft Dynamics 365 for Finance and Operations معينون‬</span><span class="sxs-lookup"><span data-stu-id="0a115-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="0a115-148">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a115-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="0a115-149">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع مستخدمي Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a115-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="0a115-150">حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a115-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="0a115-151">كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="0a115-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





