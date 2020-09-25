---
title: إدارة طلبات الإجازة في Teams
description: يوضح هذا الموضوع كيفية طلب إجازة في تطبيقات Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766750"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="d0621-103">إدارة طلبات الإجازة في Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d0621-104">يتيح لك تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams طلب إجازة بسرعة وعرض معلومات رصيد إجازاتك مباشرة في Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d0621-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="d0621-105">ويمكنك التفاعل مع روبوت لطلب المعلومات.</span><span class="sxs-lookup"><span data-stu-id="d0621-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="d0621-106">توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="d0621-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="d0621-107">تثبيت التطبيق</span><span class="sxs-lookup"><span data-stu-id="d0621-107">Install the app</span></span>

<span data-ttu-id="d0621-108">يمكنك العثور على تطبيق Human Resources في متجر Teams.</span><span class="sxs-lookup"><span data-stu-id="d0621-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="d0621-109">في Microsoft Teams، حدد علامة القطع.</span><span class="sxs-lookup"><span data-stu-id="d0621-109">In Microsoft Teams, select the ellipses.</span></span>

   ![علامة القطع لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="d0621-111">ابحث عن Dynamics 365 Human Resources، ثم حدد تجانب **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="d0621-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![تجانب HR لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="d0621-113">حدد زر **إضافة** لتثبيت التطبيق.</span><span class="sxs-lookup"><span data-stu-id="d0621-113">Select the **Add** button to install the app.</span></span>

   ![تثبيت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="d0621-115">إذا لم يقم التطبيق بتسجيل الدخول تلقائيًا، حدد علامة التبويب **إعدادات** لتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d0621-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![علامة تبويب الإعدادات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="d0621-117">إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="d0621-118">إذا كان لديك حق الوصول إلى أكثر من مثيل واحد من Human Resources، فيمكنك تحديد البيئة التي ترغب في الاتصال بها في علامة تبويب **إعدادات**.</span><span class="sxs-lookup"><span data-stu-id="d0621-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="d0621-119">لا يدعم التطبيق حاليًا دور أمان مسؤول النظام، وسيعرض رسالة خطأ إذا قمت بتسجيل الدخول باستخدام حساب مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="d0621-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="d0621-120">لتسجيل الدخول باستخدام حساب مختلف، في علامة تبويب **الإعدادات**، حدد زر **تبديل الحسابات**، ثم قم بتسجيل الدخول باستخدام حساب مستخدم ليس لديه امتيازات مسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="d0621-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="d0621-121">استخدام الروبوت</span><span class="sxs-lookup"><span data-stu-id="d0621-121">Use the bot</span></span>

<span data-ttu-id="d0621-122">بعد تثبيت التطبيق، تظهر رسالة ترحيب تسمح لك بمعرفة أنواع الإجراءات التي يمكن للروبوت القيام بها بالنيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="d0621-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![رسالة الترحيب من روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="d0621-124">عند التفاعل الأول مع الروبوت، قد تحتاج إلى تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d0621-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="d0621-125">إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="d0621-126">يمكنك مطالبة الروبوت بما يلي:</span><span class="sxs-lookup"><span data-stu-id="d0621-126">You can ask the bot to:</span></span>

- <span data-ttu-id="d0621-127">إظهار معلومات رصيد الإجازات لكل نوع من أنواع الإجازات التي قمت بتسجيلها.</span><span class="sxs-lookup"><span data-stu-id="d0621-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![إظهار الأرصدة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="d0621-129">قم بعرض تفاصيل إضافية حول نوع إجازة معين.</span><span class="sxs-lookup"><span data-stu-id="d0621-129">Show additional details about a specific leave type.</span></span>

   ![إظهار التفاصيل في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="d0621-131">ابدأ طلب إجازة لك.</span><span class="sxs-lookup"><span data-stu-id="d0621-131">Start a leave request for you.</span></span>

   ![طلب إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="d0621-133">بعد بدء طلب إجازة، يمكنك ضبط الأيام داخل البطاقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![تحرير طلب في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="d0621-135">عندما تنتهي من إدخال المعلومات، حدد **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="d0621-136">يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d0621-136">You can also select **Save as draft** to come back to it later.</span></span>

![تقديم طلب في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="d0621-138">إدارة إجازتك في Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-138">Manage your leave in Teams</span></span>

<span data-ttu-id="d0621-139">تتيح لك علامة التبويب **إجازة** عرض ما يلي:</span><span class="sxs-lookup"><span data-stu-id="d0621-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="d0621-140">معلومات الرصيد لكل نوع من أنواع الإجازات التي قمت بتسجيلها</span><span class="sxs-lookup"><span data-stu-id="d0621-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="d0621-141">طلبات الإجازة القادمة</span><span class="sxs-lookup"><span data-stu-id="d0621-141">Upcoming leave requests</span></span>

- <span data-ttu-id="d0621-142">طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="d0621-142">Time-off requests</span></span>

- <span data-ttu-id="d0621-143">مسودات طلبات الإجازات</span><span class="sxs-lookup"><span data-stu-id="d0621-143">Draft leave requests</span></span>

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="d0621-145">إنشاء طلب جديد</span><span class="sxs-lookup"><span data-stu-id="d0621-145">Create a new request</span></span>

1. <span data-ttu-id="d0621-146">لإنشاء طلب إجازة جديد، حدد **طلب جديد**.</span><span class="sxs-lookup"><span data-stu-id="d0621-146">To create a new leave request, select **New request**.</span></span>

   ![طلب جديد في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="d0621-148">أدخل اليوم أو الأيام التي تريد أخذها إجازة، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d0621-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![إضافة إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="d0621-150">إن أمكن، أدخل رمز السبب.</span><span class="sxs-lookup"><span data-stu-id="d0621-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="d0621-151">وقم أيضا بإدخال أية تعليقات وإضافة أية مرفقات.</span><span class="sxs-lookup"><span data-stu-id="d0621-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="d0621-152">عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d0621-153">يمكنك أيضًا كتابة **حفظ كمسودة** للعودة إليه لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d0621-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="d0621-154">إدارة مسودات الطلبات</span><span class="sxs-lookup"><span data-stu-id="d0621-154">Manage draft requests</span></span>

1. <span data-ttu-id="d0621-155">حدد علامة التبويب **المسودات**.</span><span class="sxs-lookup"><span data-stu-id="d0621-155">Select the **Drafts** tab.</span></span>

   ![علامة تبويب المسودات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="d0621-157">حدد القلم الرصاص لتحرير الطلب، أو حدد سلة المهملات لكي يمكنك حذف الطلب.</span><span class="sxs-lookup"><span data-stu-id="d0621-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="d0621-158">قم بإجراء أية تغييرات ضرورية.</span><span class="sxs-lookup"><span data-stu-id="d0621-158">Make any necessary changes.</span></span> <span data-ttu-id="d0621-159">عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d0621-160">يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d0621-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![تحرير مسودة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="d0621-162">إعلامات Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-162">Teams notifications</span></span>

<span data-ttu-id="d0621-163">عندما تقوم أنت أو عامل أنت القائم بالموافقة بالنسبة له بإرسال طلب إجازة، ستتلقى إعلامًا في تطبيق Human Resources في Teams.</span><span class="sxs-lookup"><span data-stu-id="d0621-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="d0621-164">يمكنك تحديد الإعلام لعرضه.</span><span class="sxs-lookup"><span data-stu-id="d0621-164">You can select the notification to view it.</span></span> <span data-ttu-id="d0621-165">تظهر الإعلامات أيضًا في منطقة **الدردشة**.</span><span class="sxs-lookup"><span data-stu-id="d0621-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="d0621-166">إذا كنت القائم بالموافقة، فيمكنك تحديد **موافقة** أو **رفض** في الإعلام.</span><span class="sxs-lookup"><span data-stu-id="d0621-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="d0621-167">يمكنك أيضًا توفير رسالة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="d0621-167">You can also provide an optional message.</span></span>

![إعلام طلب إجازة في تطبيق Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="d0621-169">عرض تقويم الإجازات لفريقك</span><span class="sxs-lookup"><span data-stu-id="d0621-169">View your team's leave calendar</span></span>

<span data-ttu-id="d0621-170">إذا كنت مديرًا مسؤولاً عن مرؤوسين مباشرين، فيمكنك عرض إجازات الفريق الموافق عليها والمعلقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="d0621-171">في تطبيق Human Resources في Teams، حدد **إجازة**.</span><span class="sxs-lookup"><span data-stu-id="d0621-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="d0621-172">حدد **تقويم الفريق**.</span><span class="sxs-lookup"><span data-stu-id="d0621-172">Select **Team calendar**.</span></span>

   ![عرض التقويم في تطبيق Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="d0621-174">يعرض التقويم إجازات المرؤوسين المباشرين الموافق عليها والمعلقة.</span><span class="sxs-lookup"><span data-stu-id="d0621-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![تقويم الإجازات في تطبيق Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="d0621-176">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="d0621-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="d0621-177">خدمة الفهم الذكي للغة (LUIS) من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d0621-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="d0621-178">باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي.</span><span class="sxs-lookup"><span data-stu-id="d0621-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="d0621-179">يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS).</span><span class="sxs-lookup"><span data-stu-id="d0621-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="d0621-180">أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="d0621-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="d0621-181">تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso).</span><span class="sxs-lookup"><span data-stu-id="d0621-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="d0621-182">يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d0621-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="d0621-183">من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d0621-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="d0621-184">قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d0621-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d0621-185">في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure.</span><span class="sxs-lookup"><span data-stu-id="d0621-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="d0621-186">يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d0621-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="d0621-187">أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="d0621-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="d0621-188">لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="d0621-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="d0621-189">شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="d0621-190">عند استخدام ميزة الإعلامات لتطبيق Dynamics 365 Human Resources في Teams، ستتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="d0621-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="d0621-191">يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="d0621-192">قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة وتتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d0621-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0621-193">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d0621-193">See also</span></span>

[<span data-ttu-id="d0621-194">تنزيل وتثبيت Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="d0621-195">مركز تعليمات Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="d0621-196">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="d0621-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
