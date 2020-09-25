---
title: تطبيق Human Resources في Teams
description: يقدم لك هذا الموضوع تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776298"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="1f9e9-103">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1f9e9-104">يتيح تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams للموظفين طلب إجازة بسرعة وعرض معلومات رصيد إجازاتهم في Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="1f9e9-105">ويمكن للموظفين التفاعل مع روبوت لطلب المعلومات.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="1f9e9-106">توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-106">The **Time off** tab provides more detailed information.</span></span>

![روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-admin-teams-leave-app-bot.png)

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="1f9e9-109">التثبيت والإعداد</span><span class="sxs-lookup"><span data-stu-id="1f9e9-109">Install and setup</span></span>

<span data-ttu-id="1f9e9-110">يمكنك العثور على تطبيق Human Resources في متجر Teams.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="1f9e9-111">للحصول على معلومات حول تثبيت تطبيق Teams، راجع [إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="1f9e9-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="1f9e9-112">للحصول على معلومات حول إدارة أذونات التطبيق في Teams، راجع [إدارة نهج أذونات التطبيق في Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="1f9e9-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="1f9e9-113">تمكين الإعلامات لتطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="1f9e9-114">إذا أردت أن يتلقى المستخدمون إعلامات تتعلق بطلبات الإجازات في تطبيق Teams، يجب عليك تمكين الإعلامات في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="1f9e9-115">وحدهم المستخدمون الذين سجلوا دخولهم إلى Teams ويستخدمون تطبيق Human Resources سيتلقون إعلامات.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="1f9e9-116">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="1f9e9-117">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-117">Select **Links**.</span></span>

3. <span data-ttu-id="1f9e9-118">ضمن **الإعداد**، حدد **معلمات النظام**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="1f9e9-119">من علامة التبويب **عام**، قم بتعيين الخيار **تمكين الاعلامات لتطبيق Teams** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![تمكين إعلامات تطبيق Teams في معلمات النظام](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="1f9e9-121">لتشغيل إعلامات Teams لجميع المستخدمين، حدد **نعم** عند المطالبة.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![تمكين إعلامات Teams لجميع المستخدمين](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="1f9e9-123">تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين</span><span class="sxs-lookup"><span data-stu-id="1f9e9-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="1f9e9-124">بعد تمكين الإعلامات لتطبيق Human Resources Teams، يمكنك تشغيل الإعلامات أو إيقاف تشغيلها لمستخدمين فرديين.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="1f9e9-125">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="1f9e9-126">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-126">Select **Links**.</span></span>

3. <span data-ttu-id="1f9e9-127">ضمن **المستخدمون**، حدد **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="1f9e9-128">حدد علامة التبويب **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="1f9e9-129">عيّن الخيار **تمكين الإعلامات لتطبيق Teams** إلى **نعم** لتمكين الإعلامات للمستخدم أو إلى **لا** لتعطيل الإعلامات للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![تمكين إعلامات تطبيق Teams في خيارات المستخدم على علامة تبويب سير العمل](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="1f9e9-131">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="1f9e9-132">مشكلات معروفة</span><span class="sxs-lookup"><span data-stu-id="1f9e9-132">Known issues</span></span>

| <span data-ttu-id="1f9e9-133">إصدار</span><span class="sxs-lookup"><span data-stu-id="1f9e9-133">Issue</span></span> | <span data-ttu-id="1f9e9-134">الحالة</span><span class="sxs-lookup"><span data-stu-id="1f9e9-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="1f9e9-135">التمرير الأفقي لا يعمل على هواتف Android</span><span class="sxs-lookup"><span data-stu-id="1f9e9-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="1f9e9-136">التمرير الأفقي ليس بمشكلة على أجهزة iOS أو أجهزه سطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="1f9e9-137">نحن نعمل علي إصلاح هذه المشكلة في Android.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="1f9e9-138">خطأ: توجد مشكلة في العثور على بيئة للاتصال بها.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="1f9e9-139">قد تتلقى رسالة الخطأ هذه حتى لو تأكدت من أنه باستطاعة المستخدم الوصول إلى بيئة واحدة أو أكثر من بيئات Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="1f9e9-140">علاوةً على ذلك، قد لا ترى كافة البيئات التي تتوقعها.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="1f9e9-141">وحتى نقوم بإصلاح هذه المشكلة، يمكنك حذف المستخدم ثم استيراده مرة أخرى لحل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="1f9e9-142">يصبح الرصيد غير صحيح عند إرسال إجازة لتاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="1f9e9-143">التنبؤ غير متوفر بعد.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="1f9e9-144">يتم عرض الرصيد للتاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="1f9e9-145">تعذر إلغاء طلب **قيد المراجعة**.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="1f9e9-146">هذه الوظيفة غير مدعومة في الوقت الحالي وستتم إضافتها في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="1f9e9-147">يتم حساب معلومات الرصيد اعتبارًا من اليوم.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="1f9e9-148">لا يعرض النظام حاليًا الأرصدة اعتبارًا من فترة الاستحقاق، حتى إذا تم تكوينه في معلمات الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="1f9e9-149">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="1f9e9-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="1f9e9-150">خدمة الفهم الذكي للغة (LUIS) من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="1f9e9-151">باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="1f9e9-152">يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS).</span><span class="sxs-lookup"><span data-stu-id="1f9e9-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="1f9e9-153">أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="1f9e9-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="1f9e9-154">تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso).</span><span class="sxs-lookup"><span data-stu-id="1f9e9-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="1f9e9-155">يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="1f9e9-156">من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="1f9e9-157">قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1f9e9-158">في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="1f9e9-159">يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="1f9e9-160">أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="1f9e9-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="1f9e9-161">لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="1f9e9-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="1f9e9-162">شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="1f9e9-163">عند استخدام ميزة الإعلامات لتطبيق Dynamics 365 Human Resources في Teams، ستتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="1f9e9-164">يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="1f9e9-165">قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة وتتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f9e9-166">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="1f9e9-166">See also</span></span> 

[<span data-ttu-id="1f9e9-167">تنزيل وتثبيت Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="1f9e9-168">مركز تعليمات Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="1f9e9-169">إدارة طلبات الإجازة في Teams</span><span class="sxs-lookup"><span data-stu-id="1f9e9-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

