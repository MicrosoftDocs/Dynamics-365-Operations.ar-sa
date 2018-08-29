---
title: "تكوين عمليات الاعتماد في سير عمل"
description: "استخدم الإجراء التالي لتكوين خصائص عملية الاعتماد."
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
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 212e9c32c7bb22b0ee0450e04b4090c540df7b54
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="f2c02-103">تكوين عمليات الاعتماد في سير عمل</span><span class="sxs-lookup"><span data-stu-id="f2c02-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2c02-104">استخدم الإجراء التالي لتكوين خصائص عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="f2c02-105">لتكوين عملية اعتماد في محرر سير العمل، انقر بزر الماوس الأيمن فوق عنصر الاعتماد، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="f2c02-106">تسمية عملية الاعتماد</span><span class="sxs-lookup"><span data-stu-id="f2c02-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="f2c02-107">اتباع الخطوات التالية لإدخال اسم لعملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="f2c02-108">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f2c02-109">في حقل **الاسم**، أدخل اسمًا فريدًا لعملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="f2c02-110">تحديد الوقت الذي يجب أن يقوم خلاله النظام بشكل تلقائي باتخاذ الإجراء المناسب على المستند</span><span class="sxs-lookup"><span data-stu-id="f2c02-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="f2c02-111">يمكنك تكوين النظام بحيث يتخذ الإجراء المناسب على المستند بشكل تلقائي إذا تمت تلبية شروط معينة.</span><span class="sxs-lookup"><span data-stu-id="f2c02-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="f2c02-112">على سبيل المثال، باستطاعة النظام اعتماد تقارير المصروفات ذات مبالغ إجمالية أقل من 100 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="f2c02-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="f2c02-113">اتبع هذه الخطوات لتحديد الوقت الذي يجب أن يتخذ النظام خلاله الإجراء المناسب على المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="f2c02-114">في الجزء الأيمن، انقر فوق **إجراءات تلقائية‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="f2c02-115">حدد خانة الاختيار **تمكين الإجراءات التلقائية**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="f2c02-116">انقر فوق **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="f2c02-117">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="f2c02-117">Enter a condition.</span></span>
5.  <span data-ttu-id="f2c02-118">أدخل شروطًا إضافية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="f2c02-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="f2c02-119">للتأكد من تكوين الشروط التي قمت بإدخالها بشكل صحيح، أكمل الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f2c02-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="f2c02-120">انقر فوق **اختبار** لفتح النموذج **اختبار حالة سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="f2c02-121">حدد سجلاً في المنطقة **‏‏التحقق من الشرط** من النموذج.</span><span class="sxs-lookup"><span data-stu-id="f2c02-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="f2c02-122">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-122">Click **Test**.</span></span> <span data-ttu-id="f2c02-123">سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.</span><span class="sxs-lookup"><span data-stu-id="f2c02-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="f2c02-124">انقر فوق **موافق** أو **إلغاء الأمر** للعودة إلى النموذج **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="f2c02-125">من القائمة **إجراء الإكمال التلقائي**، حدد الإجراء الذي يجب أن يتخذه النظام على المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f2c02-126">تحديد وقت إرسال الإخطارات</span><span class="sxs-lookup"><span data-stu-id="f2c02-126">Specify when notifications are sent</span></span>
<span data-ttu-id="f2c02-127">يمكن إرسال الإخطارات إلى الأشخاص عند الموافقة على مستند أو رفضه أو تفويضه أو تصعيده، أو عند طلب إجراء تغيير.</span><span class="sxs-lookup"><span data-stu-id="f2c02-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="f2c02-128">اتبع هذه الخطوات لتحديد الوقت الذي يتم فيه ارسال الإخطارات، والأشخاص الذين يتم إرسال الإخطارات إليهم.</span><span class="sxs-lookup"><span data-stu-id="f2c02-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="f2c02-129">في الجزء الأيمن، انقر فوق **الإخطارات‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="f2c02-130">حدد خانة الاختيار إلى جانب الأحداث التي يجب إرسال الإخطارات بشأنها:</span><span class="sxs-lookup"><span data-stu-id="f2c02-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="f2c02-131">**تفويض** – عند تعيين المستند إلى مستخدم آخر للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="f2c02-132">**تصعيد** – عندما لا ينفذ المستخدم أي إجراء على المستند في الوقت المخصص لذلك.</span><span class="sxs-lookup"><span data-stu-id="f2c02-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="f2c02-133">**موافقة** – عند الموافقة على مستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="f2c02-134">**رفض** – عند رفض مستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="f2c02-135">**طلب تغيير** – عندما يطالب المستخدم المعين بإجراء تغيير على المستند الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="f2c02-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="f2c02-136">حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="f2c02-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="f2c02-137">انقر فوق علامة التبويب **نص الإخطار‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="f2c02-138">في مربع النص ، أدخل نص الإخطار‬.</span><span class="sxs-lookup"><span data-stu-id="f2c02-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="f2c02-139">لإضفاء طابع شخصي على النص، يمكنك إدراج عناصر نائبة، يتم استبدالها بالبيانات المناسبة عند عرضها للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f2c02-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="f2c02-140">لإدراج عنصر نائب، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="f2c02-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="f2c02-141">انقر داخل مربع النص في المكان الذي يجب أن يظهر فيه العنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="f2c02-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="f2c02-142">انقر فوق **إدراج عنصر نائب**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="f2c02-143">في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.</span><span class="sxs-lookup"><span data-stu-id="f2c02-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="f2c02-144">انقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="f2c02-145">لإضافة ترجمات الإخطارات، انقر فوق **ترجمات**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="f2c02-146">في النموذج الذي يظهر، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f2c02-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="f2c02-147">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="f2c02-148">في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.</span><span class="sxs-lookup"><span data-stu-id="f2c02-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="f2c02-149">في مربع النص **النص المترجم‬**، أدخل النص.</span><span class="sxs-lookup"><span data-stu-id="f2c02-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="f2c02-150">لتخصيص النص، يمكنك إدراج عناصر نائبة.</span><span class="sxs-lookup"><span data-stu-id="f2c02-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="f2c02-151">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-151">Click **Close**.</span></span>

8.  <span data-ttu-id="f2c02-152">انقر فوق علامة تبويب **المستلم**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="f2c02-153">حدد الأشخاص الذين ستُرسل الإخطارات إليهم.</span><span class="sxs-lookup"><span data-stu-id="f2c02-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="f2c02-154">حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية للخيار قبل الانتقال إلى الخطوة 10.</span><span class="sxs-lookup"><span data-stu-id="f2c02-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f2c02-155">الخيار</span><span class="sxs-lookup"><span data-stu-id="f2c02-155">Option</span></span></th>
    <th><span data-ttu-id="f2c02-156">مستلمو الإخطارات</span><span class="sxs-lookup"><span data-stu-id="f2c02-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="f2c02-157">الخطوات الإضافية</span><span class="sxs-lookup"><span data-stu-id="f2c02-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f2c02-158"><strong>المشارك</strong></span><span class="sxs-lookup"><span data-stu-id="f2c02-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="f2c02-159">المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</span><span class="sxs-lookup"><span data-stu-id="f2c02-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f2c02-160">بعد تحديد <strong>المشارك</strong>، انقر فوق علامة التبويب <strong>مستند إلى الدور‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2c02-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="f2c02-161">في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</span><span class="sxs-lookup"><span data-stu-id="f2c02-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f2c02-162">في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</span><span class="sxs-lookup"><span data-stu-id="f2c02-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f2c02-163"><strong>مستخدم سير العمل</strong></span><span class="sxs-lookup"><span data-stu-id="f2c02-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="f2c02-164">المستخدمون المشاركون في سير العمل الحالي</span><span class="sxs-lookup"><span data-stu-id="f2c02-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f2c02-165">بعد تحديد <strong>مستخدم سير العمل</strong>، انقر فوق علامة تبويب <strong>سير العمل</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2c02-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="f2c02-166">في قائمة <strong>مستخدم سير العمل</strong>، حدد مستخدمًا يشارك في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="f2c02-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f2c02-167"><strong>المستخدم</strong></span><span class="sxs-lookup"><span data-stu-id="f2c02-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="f2c02-168">‏‫مستخدمو Microsoft Dynamics 365 for Finance and Operations معينون‬</span><span class="sxs-lookup"><span data-stu-id="f2c02-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f2c02-169">بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</span><span class="sxs-lookup"><span data-stu-id="f2c02-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f2c02-170">تتضمن قائمة <strong>المستخدمون المتاحون</strong> جميع مستخدمي Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2c02-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="f2c02-171">حدد المستخدمين لإرسال الإخطارات إليهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>:.</span><span class="sxs-lookup"><span data-stu-id="f2c02-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="f2c02-172">كرر الخطوات من 3 إلى 9 لكل الأحداث التي قمت بتحديدها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="f2c02-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="f2c02-173"> تحديد معتمد نهائي</span><span class="sxs-lookup"><span data-stu-id="f2c02-173">Specify a final approver</span></span>
<span data-ttu-id="f2c02-174">قد تحتاج إلى تعيين معتمد نهائي للسيناريوهات حيث يكون المعتمد الشخص الذي قام بإرسال المستند للموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="f2c02-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="f2c02-175">اتبع الخطوات التالية لتحديد المعتمد النهائي.</span><span class="sxs-lookup"><span data-stu-id="f2c02-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="f2c02-176">في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f2c02-177">حدد خانة الاختيار **استخدام المعتمد النهائي**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="f2c02-178">من القائمة، حدد المستخدم الذي سيكون المعتمد النهائي.</span><span class="sxs-lookup"><span data-stu-id="f2c02-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="f2c02-179">قم بتعيين حد زمني</span><span class="sxs-lookup"><span data-stu-id="f2c02-179">Set a time limit</span></span>
<span data-ttu-id="f2c02-180">اتبع الخطوات التالية إذا كان يجب إكمال عملية الاعتماد في وقت معين.</span><span class="sxs-lookup"><span data-stu-id="f2c02-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

| <span data-ttu-id="f2c02-181">**ملاحظة**</span><span class="sxs-lookup"><span data-stu-id="f2c02-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c02-182">ستقوم الخيارات التي تحددها هنا بإبطال الخيارات التي حددتها في الناحيتين  **تعيين** و**تصعيد** لكل خطوة اعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="f2c02-183">في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f2c02-184">حدد خانة الاختيار **تعيين حد زمني** **لعنصر سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="f2c02-185">في حقل **المدة** ، حدد الوقت الذي يجب خلاله إكمال عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="f2c02-186">وحدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="f2c02-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="f2c02-187">**ساعات** - أدخل عدد الساعات التي يجب خلالها إكمال عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="f2c02-188">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="f2c02-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f2c02-189">**أيام** - أدخل عدد الأيام التي يجب خلالها إكمال عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="f2c02-190">ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="f2c02-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="f2c02-191">**أسابيع** - أدخل عدد الأسابيع التي يجب خلالها إكمال عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="f2c02-192">**أشهر** - حدد اليوم والأسبوع الذي يجب أن تكون فيه عملية الاعتماد مكتملة.</span><span class="sxs-lookup"><span data-stu-id="f2c02-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="f2c02-193">على سبيل المثال، ربما تريد إكمال عملية الاعتماد في يوم الجمعة من الأسبوع الثالث من الشهر.</span><span class="sxs-lookup"><span data-stu-id="f2c02-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="f2c02-194">**سنوات** - حدد اليوم والأسبوع والشهر الذي يجب أن تكون فيه عملية الاعتماد مكتملة.</span><span class="sxs-lookup"><span data-stu-id="f2c02-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="f2c02-195">على سبيل المثال، ربما تريد إكمال عملية الاعتماد في يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="f2c02-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="f2c02-196">إذا تم تجاوز الحد الزمني فسيقوم النظام باتخاذ الإجراء المناسب على المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="f2c02-197">من القائمة **إجراء**، حدد الإجراء الذي يجب أن يقوم النظام باتخاذه.</span><span class="sxs-lookup"><span data-stu-id="f2c02-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="f2c02-198">تحديد الإجراءات المتاحة للمستخدم</span><span class="sxs-lookup"><span data-stu-id="f2c02-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="f2c02-199">عند تعيين مستند إلى مستخدم للاعتماد، يجب أن يقوم المستخدم بإجراء في المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="f2c02-200">اتبع هذه الخطوات لتحديد الإجراءات التي يمكن للمستخدم اتخاذها على المستند الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="f2c02-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="f2c02-201">في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="f2c02-202">حدد خانة الاختيار **موافقة** إذا كان باستطاعة المستخدم الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="f2c02-203">حدد خانة الاختيار **رفض** إذا كان باستطاعة المستخدم رفض المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="f2c02-204">حدد خانة الاختيار **طلب التغيير** لكي يتمكن المستخدم من طلب إدخال تغييرات على المستند.</span><span class="sxs-lookup"><span data-stu-id="f2c02-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="f2c02-205">حدد خانة الاختيار **تفويض** إذا كان باستطاعة المستخدم تعيين المستند إلى مستخدم آخر للموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="f2c02-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="f2c02-206">**ملاحظة**: توقف العمل بخانة الاختيار **تمكين الإجراءات من قائمة العمل في مدخل الشركة على الإنترنت‬**.</span><span class="sxs-lookup"><span data-stu-id="f2c02-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="f2c02-207"> تكوين خطوات الاعتماد</span><span class="sxs-lookup"><span data-stu-id="f2c02-207">Configure the approval steps</span></span>
<span data-ttu-id="f2c02-208">تتكون عملية الاعتماد من خطوات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="f2c02-209">أكمل الإجراء التالي لإضافة خطوات عملية الاعتماد وتكوين الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f2c02-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="f2c02-210">في محرر سير العمل، انقر نقرًا مزدوجًا فوق عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="f2c02-211">يعرض محرر سير العمل خطوات عملية الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="f2c02-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="f2c02-212">لإضافة خطوة اعتماد، اسحب الخطوة من ناحية **عناصر سير العمل** إلى لوحة الرسم.</span><span class="sxs-lookup"><span data-stu-id="f2c02-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="f2c02-213">لتكوين خطوة اعتماد، انظر [تكوين خطوة اعتماد](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f2c02-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






