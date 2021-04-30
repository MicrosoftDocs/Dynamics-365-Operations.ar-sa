---
title: إدارة طلبات الإجازة في Teams
description: يوضح هذا الموضوع كيفية طلب إجازة في تطبيقات Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 48bf6f7997d6159077419bcd05d27fd711c8fb4b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891020"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="aeb3f-103">إدارة طلبات الإجازة في Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aeb3f-104">يتيح لك تطبيق Dynamics 365 Human Resources في Microsoft Teams طلب إجازة بسرعة وعرض معلومات رصيد إجازاتك مباشرة في Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="aeb3f-105">يمكنك التفاعل مع الروبوت لطلب معلومات وبدء طلب إجازة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="aeb3f-106">توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="aeb3f-107">يمكنك أيضًا إرسال معلومات الأشخاص حول وقت الإجازة القادم في Teams والدردشات خارج تطبيق Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="aeb3f-108">تثبيت التطبيق</span><span class="sxs-lookup"><span data-stu-id="aeb3f-108">Install the app</span></span>

<span data-ttu-id="aeb3f-109">يمكنك العثور على تطبيق Dynamics 365 Human Resources في متجر Teams.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="aeb3f-110">في Microsoft Teams، حدد علامة القطع.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-110">In Microsoft Teams, select the ellipses.</span></span>

   ![علامة القطع لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="aeb3f-112">ابحث عن Dynamics 365 Human Resources، ثم حدد تجانب **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![تجانب HR لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="aeb3f-114">حدد زر **إضافة** لتثبيت التطبيق.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-114">Select the **Add** button to install the app.</span></span>

   ![تثبيت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="aeb3f-116">إذا لم يقم التطبيق بتسجيل الدخول تلقائيًا، حدد علامة التبويب **إعدادات** لتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![علامة تبويب الإعدادات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="aeb3f-118">إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="aeb3f-119">إذا كان لديك حق الوصول إلى أكثر من مثيل واحد من Human Resources، فيمكنك تحديد البيئة التي ترغب في الاتصال بها في علامة تبويب **إعدادات**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb3f-120">يدعم التطبيق الآن دور أمان مسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="aeb3f-121">استخدام الروبوت</span><span class="sxs-lookup"><span data-stu-id="aeb3f-121">Use the bot</span></span>

<span data-ttu-id="aeb3f-122">بعد تثبيت التطبيق، تظهر رسالة ترحيب تسمح لك بمعرفة أنواع الإجراءات التي يمكن للروبوت القيام بها بالنيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![رسالة الترحيب من روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="aeb3f-124">عند التفاعل الأول مع الروبوت، قد تحتاج إلى تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="aeb3f-125">إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="aeb3f-126">يمكنك مطالبة الروبوت بما يلي:</span><span class="sxs-lookup"><span data-stu-id="aeb3f-126">You can ask the bot to:</span></span>

- <span data-ttu-id="aeb3f-127">ابدأ طلب إجازة لك.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-127">Start a leave request for you.</span></span>

  ![بدء طلب إجازة في محادثة Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="aeb3f-129">سيقوم روبوت المحادثة بملء طلب الإجازة لك.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="aeb3f-130">حدد **طلب إجازة** وقم بتحرير التفاصيل الخاصة بطلبك.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-130">Select **Request time off** and edit the details for your request.</span></span>

  ![تحرير تفاصيل طلب الإجازة](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="aeb3f-132">عند الانتهاء من تحرير تفاصيل طلب الإجازة، حدد **إرسال** لإرساله للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![إرسال طلب الإجازة](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="aeb3f-134">إدارة إجازتك في Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-134">Manage your leave in Teams</span></span>

<span data-ttu-id="aeb3f-135">تتيح لك علامة التبويب **إجازة** عرض ما يلي:</span><span class="sxs-lookup"><span data-stu-id="aeb3f-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="aeb3f-136">معلومات الرصيد لكل نوع من أنواع الإجازات التي قمت بتسجيلها</span><span class="sxs-lookup"><span data-stu-id="aeb3f-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="aeb3f-137">طلبات الإجازة القادمة</span><span class="sxs-lookup"><span data-stu-id="aeb3f-137">Upcoming leave requests</span></span>

- <span data-ttu-id="aeb3f-138">طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="aeb3f-138">Time-off requests</span></span>

- <span data-ttu-id="aeb3f-139">مسودات طلبات الإجازات</span><span class="sxs-lookup"><span data-stu-id="aeb3f-139">Draft leave requests</span></span>

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="aeb3f-141">إنشاء طلب جديد</span><span class="sxs-lookup"><span data-stu-id="aeb3f-141">Create a new request</span></span>

1. <span data-ttu-id="aeb3f-142">لإنشاء طلب إجازة جديد، حدد **طلب جديد**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-142">To create a new leave request, select **New request**.</span></span>

   ![طلب جديد في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="aeb3f-144">أدخل اليوم أو الأيام التي تريد أخذها إجازة، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![إضافة إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="aeb3f-146">إن أمكن، أدخل رمز السبب.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="aeb3f-147">وقم أيضا بإدخال أية تعليقات وإضافة أية مرفقات.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="aeb3f-148">عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="aeb3f-149">يمكنك أيضًا كتابة **حفظ كمسودة** للعودة إليه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="aeb3f-150">إدارة مسودات الطلبات</span><span class="sxs-lookup"><span data-stu-id="aeb3f-150">Manage draft requests</span></span>

1. <span data-ttu-id="aeb3f-151">حدد علامة التبويب **المسودات**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-151">Select the **Drafts** tab.</span></span>

   ![علامة تبويب المسودات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="aeb3f-153">حدد القلم الرصاص لتحرير الطلب، أو حدد سلة المهملات لكي يمكنك حذف الطلب.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="aeb3f-154">قم بإجراء أية تغييرات ضرورية.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-154">Make any necessary changes.</span></span> <span data-ttu-id="aeb3f-155">عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="aeb3f-156">يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![تحرير مسودة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="aeb3f-158">الاستجابة لإخطارات Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-158">Respond to Teams notifications</span></span>

<span data-ttu-id="aeb3f-159">عندما تقوم أنت أو عامل أنت القائم بالموافقة بالنسبة له بإرسال طلب إجازة، ستتلقى إعلامًا في تطبيق Human Resources في Teams.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="aeb3f-160">يمكنك تحديد الإعلام لعرضه.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-160">You can select the notification to view it.</span></span> <span data-ttu-id="aeb3f-161">تظهر الإعلامات أيضًا في منطقة **الدردشة**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="aeb3f-162">إذا كنت القائم بالموافقة، فيمكنك تحديد **موافقة** أو **رفض** في الإعلام.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="aeb3f-163">يمكنك أيضًا توفير رسالة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-163">You can also provide an optional message.</span></span>

![إعلام طلب إجازة في تطبيق Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="aeb3f-165">إرسال معلومات وقت الإجازة القادم إلى الزملاء</span><span class="sxs-lookup"><span data-stu-id="aeb3f-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="aeb3f-166">بعد تثبيت تطبيق Human Resources لـ Teams، يمكنك بسهولة إرسال معلومات حول وقت الإجازة القادم إلى الزملاء في الفرق أو الدردشات.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="aeb3f-167">في فريق أو دردشة في Teams، حدد الزر Human Resources أسفل نافذة الدردشة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![الزر Human Resources أسفل نافذة الدردشة](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="aeb3f-169">حدد طلب الإجازة الذي ترغب في مشاركته.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-169">Select the leave request you want to share.</span></span> <span data-ttu-id="aeb3f-170">إذا أردت مشاركة طلب إجازة تمهيدي، فحدد **المسودات** أولاً.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![تحديد طلب إجازة قادم لمشاركته](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="aeb3f-172">سيظهر طلب إجازتك في الدردشة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-172">Your leave request will display in the chat.</span></span>

![بطاقة طلب إجازة في Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="aeb3f-174">إذا كنت قد شاركت طلبًا تمهيديًا، فسيظهر كمسودة:</span><span class="sxs-lookup"><span data-stu-id="aeb3f-174">If you shared a draft request, it will display as a draft:</span></span>

![بطاقة طلب إجازة تمهيدي في Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="aeb3f-176">عرض تقويم الإجازات لفريقك</span><span class="sxs-lookup"><span data-stu-id="aeb3f-176">View your team's leave calendar</span></span>

<span data-ttu-id="aeb3f-177">إذا كنت مديرًا مسؤولاً عن مرؤوسين مباشرين، فيمكنك عرض إجازات الفريق الموافق عليها والمعلقة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="aeb3f-178">في تطبيق Human Resources في Teams، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="aeb3f-179">حدد **تقويم الفريق**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-179">Select **Team calendar**.</span></span> <span data-ttu-id="aeb3f-180">يعرض التقويم إجازات المرؤوسين المباشرين الموافق عليها والمعلقة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![عرض التقويم في تطبيق Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="aeb3f-182">إذا لم تتمكن من رؤية تقويم الفريق، فاطلب من المسؤول تمكينه.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="aeb3f-183">لمزيد من المعلومات، راجع [التثبيت والإعداد](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="aeb3f-184">اللغات المدعومة</span><span class="sxs-lookup"><span data-stu-id="aeb3f-184">Supported languages</span></span>

<span data-ttu-id="aeb3f-185">يدعم التطبيق Dynamics 365 Human Resources الموجود في Teams اللغات التالية:</span><span class="sxs-lookup"><span data-stu-id="aeb3f-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="aeb3f-186">معرف الإعدادات المحلية</span><span class="sxs-lookup"><span data-stu-id="aeb3f-186">Locale ID</span></span> | <span data-ttu-id="aeb3f-187">اللغة</span><span class="sxs-lookup"><span data-stu-id="aeb3f-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="aeb3f-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="aeb3f-188">de-DE</span></span> | <span data-ttu-id="aeb3f-189">الألمانية (ألمانيا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-189">German (Germany)</span></span> |
| <span data-ttu-id="aeb3f-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="aeb3f-190">es-ES</span></span> | <span data-ttu-id="aeb3f-191">الأسبانية (أسبانيا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="aeb3f-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="aeb3f-192">es-MX</span></span> | <span data-ttu-id="aeb3f-193">الأسبانية (المكسيك)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="aeb3f-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="aeb3f-194">fr-CA</span></span> | <span data-ttu-id="aeb3f-195">الفرنسية (كندا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-195">French (Canada)</span></span> |
| <span data-ttu-id="aeb3f-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="aeb3f-196">fr-FR</span></span> | <span data-ttu-id="aeb3f-197">الفرنسية (فرنسا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-197">French (France)</span></span> |
| <span data-ttu-id="aeb3f-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="aeb3f-198">it-IT</span></span> | <span data-ttu-id="aeb3f-199">الإيطالية (إيطاليا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-199">Italian (Italy)</span></span> |
| <span data-ttu-id="aeb3f-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="aeb3f-200">nl-NL</span></span> | <span data-ttu-id="aeb3f-201">الهولندية (هولندا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="aeb3f-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="aeb3f-202">pt-BR</span></span> | <span data-ttu-id="aeb3f-203">البرتغالية (البرازيل)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="aeb3f-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="aeb3f-204">tr-TR</span></span> | <span data-ttu-id="aeb3f-205">التركية (تركيا)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="aeb3f-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="aeb3f-206">zh-CN</span></span> | <span data-ttu-id="aeb3f-207">الصينية (المبسطة)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="aeb3f-208">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="aeb3f-208">Troubleshooting</span></span>

<span data-ttu-id="aeb3f-209">في تسجيل الدخول أو باستخدام تطبيق Dynamics 365 Human Resources Teams، حاول اتباع إرشادات استكشاف الأخطاء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="aeb3f-210">إذا كنت لا تزال تواجه مشاكل بعد استكشاف الأخطاء وإصلاحها، اتصل بالدعم.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="aeb3f-211">لمزيد من المعلومات، راجع [الحصول على الدعم](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="aeb3f-212">لا يمكن التسجيل في تطبيق الموارد البشرية في الفرق</span><span class="sxs-lookup"><span data-stu-id="aeb3f-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="aeb3f-213">إذا لم تتمكن من تسجيل الدخول إلى التطبيق ، فمن الممكن ان يكون الحساب الذي تستخدمه لتسجيل الدخول إلى Microsoft Teams غير مقترن بسجل موظف في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="aeb3f-214">اتصل بمسؤول النظام لضمان ربط سجل الموظف بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="aeb3f-215">لا يتم عرض الترجمات بشكل صحيح</span><span class="sxs-lookup"><span data-stu-id="aeb3f-215">Translations don't display correctly</span></span>

<span data-ttu-id="aeb3f-216">إذا لم يتم عرض الترجمات على النحو المتوقع، فتأكد من أن اللغة التي تحددها في Teams تطابق اللغة المحددة في **خيارات المستخدم** لـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="aeb3f-217">في Teams، انظر إلى **لغة التطبيق** في **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-217">In Teams, look at **App language** in **Settings**.</span></span>

![إعدادات Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="aeb3f-219">في Human Resources، حدد **الإعدادات** ثم حدد **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="aeb3f-220">تحقق من أن الحقل **اللغة** يطابق الحقل **لغة التطبيق** في Teams.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![خيارات مستخدم Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="aeb3f-222">إذا كنت لا تزال تواجه مشاكل في الترجمة، فأعلمنا بذلك.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="aeb3f-223">للحصول على المعلومات، راجع [الحصول على الدعم لتطبيقات Finance and Operations أو Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="aeb3f-224">حدث خطا عند اعتماد طلبات المغادرة في تطبيق الموارد البشرية في الفرق</span><span class="sxs-lookup"><span data-stu-id="aeb3f-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="aeb3f-225">إذا تلقيت خطأً عندما تحاول الموافقة على طلبات الإجازة في تطبيق Teams، فجرّب خطوات استكشاف الأخطاء وإصلاحها التالية:</span><span class="sxs-lookup"><span data-stu-id="aeb3f-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="aeb3f-226">تحقق من ان الحساب الذي تستخدمه لتسجيل الدخول إلى Microsoft Teams هو نفس الحساب الذي تستخدمه للوصول اليه Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="aeb3f-227">تحقق من انك أنت موافق صالح للطلب من خلال التحقق من إعدادات سير العمل للموافقة على المغادرة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="aeb3f-228">لمزيد من المعلومات حول إنهاء مهام سير العمل، راجع [إنشاء سير عمل لطلب أجازه](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="aeb3f-229">مشكلات إمكانية الوصول المعروفة</span><span class="sxs-lookup"><span data-stu-id="aeb3f-229">Known accessibility issues</span></span>

<span data-ttu-id="aeb3f-230">يحتوي تطبيق Human Resources في Teams على مشكلات إمكانية الوصول التالية التي نعمل على إصلاحها في الإصدارات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="aeb3f-231">إصدار</span><span class="sxs-lookup"><span data-stu-id="aeb3f-231">Issue</span></span> | <span data-ttu-id="aeb3f-232">الحل أو التوضيح</span><span class="sxs-lookup"><span data-stu-id="aeb3f-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="aeb3f-233">يؤدي التكبير إلى 400٪ على سطح المكتب إلى إخفاء بعض أزرار الإجراءات عن العرض.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="aeb3f-234">نوصي باستخدام المكبر بدلاً من ذلك حتى نتمكن من دعم مستوى التكبير/التصغير هذا.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="aeb3f-235">في علامة التبويب **إجازة**، يعلن التعليق الصوتي عن إجراء زر أثناء قراءة رأس شبكة الإجازات.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="aeb3f-236">يتم تجميع الرأس والعناصر داخل الشبكة حسب السنة، وهي قابلة للطي.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="aeb3f-237">يفسر التعليق الصوتي هذا على أنه عنصر قابل للتنفيذ، لكنه ليس كذلك.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="aeb3f-238">في علامة التبويب **إجازة**، هناك إيماءة انتقاد إضافية عند الانتقال إلى **رمز السبب** في طلب جديد.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="aeb3f-239">لا يوجد عنصر تحكم خفي يحاول التنقل السريع الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="aeb3f-240">في علامة التبويب **إجازة**، إذا قمت بالتمرير أثناء فتح التقويم، فسوف ينتهي بك الأمر خارج نطاق التحكم بدلاً من أن تكون في الجزء العلوي في طلب جديد أو أثناء تحرير طلب.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="aeb3f-241">عند الوصول إلى **الوصول إلى اليوم**، ضع في اعتبارك أن هذا هو نهاية عنصر التحكم واسحب في الاتجاه العكسي للرجوع إلى الأعلى.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="aeb3f-242">في علامة التبويب **محادثة**، ينتقل التركيز إلى الأعلى عند إدخال تاريخ أثناء استخدام الأداة المساعدة أو التنقل باستخدام لوحة المفاتيح.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="aeb3f-243">اضغط حتى تصل إلى منطقة الإدخال مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="aeb3f-244">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="aeb3f-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="aeb3f-245">خدمة الفهم الذكي للغة (LUIS) من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="aeb3f-246">باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="aeb3f-247">يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="aeb3f-248">أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="aeb3f-249">تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="aeb3f-250">يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="aeb3f-251">من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="aeb3f-252">قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="aeb3f-253">في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="aeb3f-254">يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="aeb3f-255">أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="aeb3f-256">لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="aeb3f-257">Microsoft Teams وشبكة أحداث Azure وAzure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="aeb3f-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="aeb3f-258">عند استخدام تطبيق Dynamics 365 Human Resources في Microsoft Teams، قد تتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="aeb3f-259">يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="aeb3f-260">قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة في شبكة أحداث Microsoft Azure وستتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="aeb3f-261">لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="aeb3f-262">اثناء التحدث مع روبوت الدردشة في تطبيق Human Resources، قد يتم تخزين محتوى المحادثة في Azure Cosmos DB وإرساله إلى Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="aeb3f-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="aeb3f-263">قد يتم تخزين هذه البيانات في Azure Cosmos DB لمدة 24 ساعة وقد تتم معالجتها خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="aeb3f-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="aeb3f-264">لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="aeb3f-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="aeb3f-265">لتقييد الوصول إلى تطبيق Human Resources في Microsoft Teams لمؤسستك أو المستخدمين في مؤسستك، راجع [إدارة سياسات أذونات التطبيق في Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="aeb3f-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="aeb3f-266">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="aeb3f-266">See also</span></span>

[<span data-ttu-id="aeb3f-267">تنزيل وتثبيت Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="aeb3f-268">مركز تعليمات Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="aeb3f-269">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="aeb3f-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]