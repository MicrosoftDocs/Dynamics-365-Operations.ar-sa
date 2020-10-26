---
title: إدارة طلبات الإجازة في Teams
description: يوضح هذا الموضوع كيفية طلب إجازة في تطبيقات Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3929983"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="d89e7-103">إدارة طلبات الإجازة في Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d89e7-104">يتيح لك تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams طلب إجازة بسرعة وعرض معلومات رصيد إجازاتك مباشرة في Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d89e7-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="d89e7-105">يمكنك التفاعل مع الروبوت لطلب معلومات وبدء طلب إجازة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="d89e7-106">توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="d89e7-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="d89e7-107">علاوةً على ذلك، يمكنك إرسال معلومات الأشخاص حول وقت الإجازة القادم في الفرق والدردشات خارج تطبيق Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d89e7-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="d89e7-108">تثبيت التطبيق</span><span class="sxs-lookup"><span data-stu-id="d89e7-108">Install the app</span></span>

<span data-ttu-id="d89e7-109">يمكنك العثور على تطبيق Human Resources في متجر Teams.</span><span class="sxs-lookup"><span data-stu-id="d89e7-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="d89e7-110">في Microsoft Teams، حدد علامة القطع.</span><span class="sxs-lookup"><span data-stu-id="d89e7-110">In Microsoft Teams, select the ellipses.</span></span>

   ![علامة القطع لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="d89e7-112">ابحث عن Dynamics 365 Human Resources، ثم حدد تجانب **Human Resources** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![تجانب HR لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="d89e7-114">حدد زر **إضافة** لتثبيت التطبيق.</span><span class="sxs-lookup"><span data-stu-id="d89e7-114">Select the **Add** button to install the app.</span></span>

   ![تثبيت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="d89e7-116">إذا لم يقم التطبيق بتسجيل الدخول تلقائيًا، حدد علامة التبويب **إعدادات** لتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d89e7-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![علامة تبويب الإعدادات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="d89e7-118">إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="d89e7-119">إذا كان لديك حق الوصول إلى أكثر من مثيل واحد من Human Resources، فيمكنك تحديد البيئة التي ترغب في الاتصال بها في علامة تبويب **إعدادات** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="d89e7-120">يدعم التطبيق الآن دور أمان مسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="d89e7-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="d89e7-121">استخدام الروبوت</span><span class="sxs-lookup"><span data-stu-id="d89e7-121">Use the bot</span></span>

<span data-ttu-id="d89e7-122">بعد تثبيت التطبيق، تظهر رسالة ترحيب تسمح لك بمعرفة أنواع الإجراءات التي يمكن للروبوت القيام بها بالنيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="d89e7-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![رسالة الترحيب من روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="d89e7-124">عند التفاعل الأول مع الروبوت، قد تحتاج إلى تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d89e7-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="d89e7-125">إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="d89e7-126">يمكنك مطالبة الروبوت بما يلي:</span><span class="sxs-lookup"><span data-stu-id="d89e7-126">You can ask the bot to:</span></span>

- <span data-ttu-id="d89e7-127">إظهار معلومات رصيد الإجازات لكل نوع من أنواع الإجازات التي قمت بتسجيلها.</span><span class="sxs-lookup"><span data-stu-id="d89e7-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![إظهار الأرصدة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="d89e7-129">قم بعرض تفاصيل إضافية حول نوع إجازة معين.</span><span class="sxs-lookup"><span data-stu-id="d89e7-129">Show additional details about a specific leave type.</span></span>

   ![إظهار التفاصيل في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="d89e7-131">ابدأ طلب إجازة لك.</span><span class="sxs-lookup"><span data-stu-id="d89e7-131">Start a leave request for you.</span></span>

   ![طلب إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="d89e7-133">بعد بدء طلب إجازة، يمكنك ضبط الأيام داخل البطاقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![تحرير طلب في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="d89e7-135">عندما تنتهي من إدخال المعلومات، حدد **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="d89e7-136">يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d89e7-136">You can also select **Save as draft** to come back to it later.</span></span>

![تقديم طلب في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="d89e7-138">إدارة إجازتك في Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-138">Manage your leave in Teams</span></span>

<span data-ttu-id="d89e7-139">تتيح لك علامة التبويب **إجازة** عرض ما يلي:</span><span class="sxs-lookup"><span data-stu-id="d89e7-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="d89e7-140">معلومات الرصيد لكل نوع من أنواع الإجازات التي قمت بتسجيلها</span><span class="sxs-lookup"><span data-stu-id="d89e7-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="d89e7-141">طلبات الإجازة القادمة</span><span class="sxs-lookup"><span data-stu-id="d89e7-141">Upcoming leave requests</span></span>

- <span data-ttu-id="d89e7-142">طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="d89e7-142">Time-off requests</span></span>

- <span data-ttu-id="d89e7-143">مسودات طلبات الإجازات</span><span class="sxs-lookup"><span data-stu-id="d89e7-143">Draft leave requests</span></span>

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="d89e7-145">إنشاء طلب جديد</span><span class="sxs-lookup"><span data-stu-id="d89e7-145">Create a new request</span></span>

1. <span data-ttu-id="d89e7-146">لإنشاء طلب إجازة جديد، حدد **طلب جديد** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-146">To create a new leave request, select **New request** .</span></span>

   ![طلب جديد في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="d89e7-148">أدخل اليوم أو الأيام التي تريد أخذها إجازة، ثم حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-148">Enter the day or days you want to take off, and then select **Add** .</span></span>

   ![إضافة إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="d89e7-150">إن أمكن، أدخل رمز السبب.</span><span class="sxs-lookup"><span data-stu-id="d89e7-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="d89e7-151">وقم أيضا بإدخال أية تعليقات وإضافة أية مرفقات.</span><span class="sxs-lookup"><span data-stu-id="d89e7-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="d89e7-152">عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d89e7-153">يمكنك أيضًا كتابة **حفظ كمسودة** للعودة إليه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d89e7-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="d89e7-154">إدارة مسودات الطلبات</span><span class="sxs-lookup"><span data-stu-id="d89e7-154">Manage draft requests</span></span>

1. <span data-ttu-id="d89e7-155">حدد علامة التبويب **المسودات** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-155">Select the **Drafts** tab.</span></span>

   ![علامة تبويب المسودات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="d89e7-157">حدد القلم الرصاص لتحرير الطلب، أو حدد سلة المهملات لكي يمكنك حذف الطلب.</span><span class="sxs-lookup"><span data-stu-id="d89e7-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="d89e7-158">قم بإجراء أية تغييرات ضرورية.</span><span class="sxs-lookup"><span data-stu-id="d89e7-158">Make any necessary changes.</span></span> <span data-ttu-id="d89e7-159">عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d89e7-160">يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d89e7-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![تحرير مسودة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="d89e7-162">الاستجابة لإخطارات Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-162">Respond to Teams notifications</span></span>

<span data-ttu-id="d89e7-163">عندما تقوم أنت أو عامل أنت القائم بالموافقة بالنسبة له بإرسال طلب إجازة، ستتلقى إعلامًا في تطبيق Human Resources في Teams.</span><span class="sxs-lookup"><span data-stu-id="d89e7-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="d89e7-164">يمكنك تحديد الإعلام لعرضه.</span><span class="sxs-lookup"><span data-stu-id="d89e7-164">You can select the notification to view it.</span></span> <span data-ttu-id="d89e7-165">تظهر الإعلامات أيضًا في منطقة **الدردشة** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="d89e7-166">إذا كنت القائم بالموافقة، فيمكنك تحديد **موافقة** أو **رفض** في الإعلام.</span><span class="sxs-lookup"><span data-stu-id="d89e7-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="d89e7-167">يمكنك أيضًا توفير رسالة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="d89e7-167">You can also provide an optional message.</span></span>

![إعلام طلب إجازة في تطبيق Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="d89e7-169">إرسال معلومات وقت الإجازة القادم إلى الزملاء</span><span class="sxs-lookup"><span data-stu-id="d89e7-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="d89e7-170">بعد تثبيت تطبيق Human Resources لـ Teams، يمكنك بسهولة إرسال معلومات حول وقت الإجازة القادم إلى الزملاء في الفرق أو الدردشات.</span><span class="sxs-lookup"><span data-stu-id="d89e7-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="d89e7-171">في فريق أو دردشة في Teams، حدد الزر Human Resources أسفل نافذة الدردشة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![الزر Human Resources أسفل نافذة الدردشة](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="d89e7-173">حدد طلب الإجازة الذي ترغب في مشاركته.</span><span class="sxs-lookup"><span data-stu-id="d89e7-173">Select the leave request you want to share.</span></span> <span data-ttu-id="d89e7-174">إذا أردت مشاركة طلب إجازة تمهيدي، فحدد **المسودات** أولاً.</span><span class="sxs-lookup"><span data-stu-id="d89e7-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![تحديد طلب إجازة قادم لمشاركته](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="d89e7-176">سيظهر طلب إجازتك في الدردشة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-176">Your leave request will display in the chat.</span></span>

![بطاقة طلب إجازة في Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="d89e7-178">إذا كنت قد شاركت طلبًا تمهيديًا، فسيظهر كمسودة:</span><span class="sxs-lookup"><span data-stu-id="d89e7-178">If you shared a draft request, it will display as a draft:</span></span>

![بطاقة طلب إجازة تمهيدي في Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="d89e7-180">عرض تقويم الإجازات لفريقك</span><span class="sxs-lookup"><span data-stu-id="d89e7-180">View your team's leave calendar</span></span>

<span data-ttu-id="d89e7-181">إذا كنت مديرًا مسؤولاً عن مرؤوسين مباشرين، فيمكنك عرض إجازات الفريق الموافق عليها والمعلقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="d89e7-182">في تطبيق Human Resources في Teams، حدد **إجازة** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-182">In the Human Resources app in Teams, select **Time off** .</span></span>

2. <span data-ttu-id="d89e7-183">حدد **تقويم الفريق** .</span><span class="sxs-lookup"><span data-stu-id="d89e7-183">Select **Team calendar** .</span></span>

   ![عرض التقويم في تطبيق Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="d89e7-185">يعرض التقويم إجازات المرؤوسين المباشرين الموافق عليها والمعلقة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![تقويم الإجازات في تطبيق Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="d89e7-187">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="d89e7-187">Troubleshooting</span></span>

<span data-ttu-id="d89e7-188">إذا كنت تواجه مشكله في تسجيل الدخول أو باستخدام تطبيق فرق الموارد البشرية، حاول اتباع إرشادات استكشاف الأخطاء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="d89e7-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="d89e7-189">إذا كنت لا تزال تواجه مشاكل بعد استكشاف الأخطاء وإصلاحها، اتصل بالدعم.</span><span class="sxs-lookup"><span data-stu-id="d89e7-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="d89e7-190">لمزيد من المعلومات، راجع [الحصول على الدعم](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="d89e7-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="d89e7-191">لا يمكن التسجيل في تطبيق الموارد البشرية في الفرق</span><span class="sxs-lookup"><span data-stu-id="d89e7-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="d89e7-192">إذا لم تتمكن من تسجيل الدخول إلى التطبيق ، فمن الممكن ان يكون الحساب الذي تستخدمه لتسجيل الدخول إلى Microsoft Teams غير مقترن بسجل موظف في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d89e7-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d89e7-193">اتصل بمسؤول النظام لضمان ربط سجل الموظف بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="d89e7-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="d89e7-194">حدث خطا عند اعتماد طلبات المغادرة في تطبيق الموارد البشرية في الفرق</span><span class="sxs-lookup"><span data-stu-id="d89e7-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="d89e7-195">في حاله تلقي خطا اثناء محاولة الموافقة علي طلبات الإجازات في تطبيق الفرق ، قم باجراء خطوات استكشاف الأخطاء وإصلاحها التالية:</span><span class="sxs-lookup"><span data-stu-id="d89e7-195">If you receive an error when you're trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="d89e7-196">تحقق من ان الحساب الذي تستخدمه لتسجيل الدخول إلى Microsoft Teams هو نفس الحساب الذي تستخدمه للوصول اليه Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d89e7-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="d89e7-197">تحقق من انك أنت موافق صالح للطلب من خلال التحقق من إعدادات سير العمل للموافقة على المغادرة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="d89e7-198">لمزيد من المعلومات حول إنهاء مهام سير العمل، راجع [إنشاء سير عمل لطلب أجازه](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="d89e7-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="d89e7-199">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="d89e7-199">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="d89e7-200">خدمة الفهم الذكي للغة (LUIS) من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d89e7-200">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="d89e7-201">باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي.</span><span class="sxs-lookup"><span data-stu-id="d89e7-201">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="d89e7-202">يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS).</span><span class="sxs-lookup"><span data-stu-id="d89e7-202">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="d89e7-203">أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="d89e7-203">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="d89e7-204">تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso).</span><span class="sxs-lookup"><span data-stu-id="d89e7-204">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="d89e7-205">يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d89e7-205">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="d89e7-206">من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d89e7-206">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="d89e7-207">قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d89e7-207">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d89e7-208">في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure.</span><span class="sxs-lookup"><span data-stu-id="d89e7-208">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="d89e7-209">يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-209">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="d89e7-210">أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="d89e7-210">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="d89e7-211">لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="d89e7-211">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="d89e7-212">Microsoft Teams وشبكة أحداث Azure وAzure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d89e7-212">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="d89e7-213">عند استخدام تطبيق Dynamics 365 Human Resources في Microsoft Teams، قد تتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="d89e7-213">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="d89e7-214">يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-214">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="d89e7-215">قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة في شبكة أحداث Microsoft Azure وستتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d89e7-215">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="d89e7-216">لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="d89e7-216">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="d89e7-217">اثناء التحدث مع روبوت الدردشة في تطبيق Human Resources، قد يتم تخزين محتوى المحادثة في Azure Cosmos DB وإرساله إلى Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d89e7-217">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="d89e7-218">قد يتم تخزين هذه البيانات في Azure Cosmos DB لمدة 24 ساعة وقد تتم معالجتها خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="d89e7-218">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="d89e7-219">لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="d89e7-219">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="d89e7-220">لتقييد الوصول إلى تطبيق Human Resources في Microsoft Teams لمؤسستك أو المستخدمين في مؤسستك، راجع [إدارة سياسات أذونات التطبيق في Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="d89e7-220">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="d89e7-221">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d89e7-221">See also</span></span>

[<span data-ttu-id="d89e7-222">تنزيل وتثبيت Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-222">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="d89e7-223">مركز تعليمات Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-223">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="d89e7-224">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="d89e7-224">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
