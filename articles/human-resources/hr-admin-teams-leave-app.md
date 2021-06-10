---
title: تطبيق Human Resources في Teams
description: يقدم لك هذا الموضوع تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1cceb15d64215cb8d5c996df792e863d466f87d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053553"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="b8413-103">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="b8413-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b8413-104">يتيح تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams للموظفين طلب إجازة بسرعة وعرض معلومات رصيد إجازاتهم في Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b8413-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="b8413-105">ويمكن للموظفين التفاعل مع روبوت لطلب المعلومات.</span><span class="sxs-lookup"><span data-stu-id="b8413-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="b8413-106">توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="b8413-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="b8413-107">علاوةً على ذلك، يمكنهم إرسال معلومات الأشخاص حول وقت الإجازة القادم في الفرق والدردشات خارج تطبيق Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b8413-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot.png)

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![بطاقة طلب إجازة في Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="b8413-111">التثبيت والإعداد</span><span class="sxs-lookup"><span data-stu-id="b8413-111">Install and setup</span></span>

<span data-ttu-id="b8413-112">يمكنك العثور على تطبيق Dynamics 365 Human Resources في متجر Teams.</span><span class="sxs-lookup"><span data-stu-id="b8413-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="b8413-113">للحصول على معلومات حول تثبيت تطبيق Teams، راجع [إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="b8413-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="b8413-114">للحصول على معلومات حول إدارة أذونات التطبيق في Teams، راجع [إدارة نهج أذونات التطبيق في Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="b8413-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="b8413-115">إذا كنت ترغب أن يقوم المستخدمون بعرض تقويم الإجازة والغياب في التطبيق، فستحتاج إلى تمكين **‏‫تقويم الإجازة والغياب في Teams** في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="b8413-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="b8413-116">لمزيد من المعلومات حول تمكين الميزات، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="b8413-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="b8413-117">تمكين الإعلامات لتطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="b8413-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="b8413-118">إذا أردت أن يتلقى المستخدمون إعلامات تتعلق بطلبات الإجازات في تطبيق Teams، يجب عليك تمكين الإعلامات في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b8413-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="b8413-119">وحدهم المستخدمون الذين سجلوا دخولهم إلى Teams ويستخدمون تطبيق Dynamics 365 Human Resources سيتلقون إعلامات.</span><span class="sxs-lookup"><span data-stu-id="b8413-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="b8413-120">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="b8413-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="b8413-121">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="b8413-121">Select **Links**.</span></span>

3. <span data-ttu-id="b8413-122">ضمن **الإعداد**، حدد **معلمات النظام**.</span><span class="sxs-lookup"><span data-stu-id="b8413-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="b8413-123">من علامة التبويب **عام**، قم بتعيين الخيار **تمكين الاعلامات لتطبيق Teams** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b8413-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![تمكين إعلامات تطبيق Teams في معلمات النظام](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="b8413-125">لتشغيل إعلامات Teams لجميع المستخدمين، حدد **نعم** عند المطالبة.</span><span class="sxs-lookup"><span data-stu-id="b8413-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![تمكين إعلامات Teams لجميع المستخدمين](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="b8413-127">تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين</span><span class="sxs-lookup"><span data-stu-id="b8413-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="b8413-128">بعد تمكين الإعلامات لتطبيق Dynamics 365 Human Resources Teams، يمكنك تشغيل الإعلامات أو إيقاف تشغيلها لمستخدمين فرديين.</span><span class="sxs-lookup"><span data-stu-id="b8413-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="b8413-129">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="b8413-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="b8413-130">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="b8413-130">Select **Links**.</span></span>

3. <span data-ttu-id="b8413-131">ضمن **المستخدمون**، حدد **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="b8413-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="b8413-132">حدد علامة التبويب **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="b8413-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="b8413-133">عيّن الخيار **تمكين الإعلامات لتطبيق Teams** إلى **نعم** لتمكين الإعلامات للمستخدم أو إلى **لا** لتعطيل الإعلامات للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="b8413-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![تمكين إعلامات تطبيق Teams في خيارات المستخدم على علامة تبويب سير العمل](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="b8413-135">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b8413-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="b8413-136">اللغات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b8413-136">Supported languages</span></span>

<span data-ttu-id="b8413-137">يدعم التطبيق Dynamics 365 Human Resources الموجود في Teams اللغات التالية:</span><span class="sxs-lookup"><span data-stu-id="b8413-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="b8413-138">معرف الإعدادات المحلية</span><span class="sxs-lookup"><span data-stu-id="b8413-138">Locale ID</span></span> | <span data-ttu-id="b8413-139">اللغة</span><span class="sxs-lookup"><span data-stu-id="b8413-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="b8413-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="b8413-140">de-DE</span></span> | <span data-ttu-id="b8413-141">الألمانية (ألمانيا)</span><span class="sxs-lookup"><span data-stu-id="b8413-141">German (Germany)</span></span> |
| <span data-ttu-id="b8413-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="b8413-142">es-ES</span></span> | <span data-ttu-id="b8413-143">الأسبانية (أسبانيا)</span><span class="sxs-lookup"><span data-stu-id="b8413-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="b8413-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="b8413-144">es-MX</span></span> | <span data-ttu-id="b8413-145">الأسبانية (المكسيك)</span><span class="sxs-lookup"><span data-stu-id="b8413-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="b8413-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="b8413-146">fr-CA</span></span> | <span data-ttu-id="b8413-147">الفرنسية (كندا)</span><span class="sxs-lookup"><span data-stu-id="b8413-147">French (Canada)</span></span> |
| <span data-ttu-id="b8413-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="b8413-148">fr-FR</span></span> | <span data-ttu-id="b8413-149">الفرنسية (فرنسا)</span><span class="sxs-lookup"><span data-stu-id="b8413-149">French (France)</span></span> |
| <span data-ttu-id="b8413-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="b8413-150">it-IT</span></span> | <span data-ttu-id="b8413-151">الإيطالية (إيطاليا)</span><span class="sxs-lookup"><span data-stu-id="b8413-151">Italian (Italy)</span></span> |
| <span data-ttu-id="b8413-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="b8413-152">nl-NL</span></span> | <span data-ttu-id="b8413-153">الهولندية (هولندا)</span><span class="sxs-lookup"><span data-stu-id="b8413-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="b8413-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="b8413-154">pt-BR</span></span> | <span data-ttu-id="b8413-155">البرتغالية (البرازيل)</span><span class="sxs-lookup"><span data-stu-id="b8413-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="b8413-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="b8413-156">tr-TR</span></span> | <span data-ttu-id="b8413-157">التركية (تركيا)</span><span class="sxs-lookup"><span data-stu-id="b8413-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="b8413-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="b8413-158">zh-CN</span></span> | <span data-ttu-id="b8413-159">الصينية (المبسطة)</span><span class="sxs-lookup"><span data-stu-id="b8413-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="b8413-160">الملاحظات</span><span class="sxs-lookup"><span data-stu-id="b8413-160">Notes</span></span>

<span data-ttu-id="b8413-161">يتم تحديد عناصر العمل التالية للإصدارات المستقبلية:</span><span class="sxs-lookup"><span data-stu-id="b8413-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="b8413-162">عنصر العمل</span><span class="sxs-lookup"><span data-stu-id="b8413-162">Work item</span></span> | <span data-ttu-id="b8413-163">الحالة</span><span class="sxs-lookup"><span data-stu-id="b8413-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="b8413-164">يصبح الرصيد غير صحيح عند إرسال إجازة لتاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="b8413-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="b8413-165">التنبؤ غير متوفر بعد.</span><span class="sxs-lookup"><span data-stu-id="b8413-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="b8413-166">يتم عرض الرصيد للتاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="b8413-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="b8413-167">تعذر إلغاء طلب **قيد المراجعة**.</span><span class="sxs-lookup"><span data-stu-id="b8413-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="b8413-168">هذه الوظيفة غير مدعومة في الوقت الحالي وستتم إضافتها في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="b8413-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="b8413-169">يتم حساب معلومات الرصيد اعتبارًا من اليوم.</span><span class="sxs-lookup"><span data-stu-id="b8413-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="b8413-170">لا يعرض النظام حاليًا الأرصدة اعتبارًا من فترة الاستحقاق، حتى إذا تم تكوينه في معلمات الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="b8413-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="b8413-171">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="b8413-171">Troubleshooting</span></span>

<span data-ttu-id="b8413-172">إذا كان المستخدم يواجه مشكله في تسجيل الدخول أو باستخدام تطبيق فرق الموارد البشرية، حاول اتباع إرشادات استكشاف الأخطاء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="b8413-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="b8413-173">إذا كنت لا تزال تواجه مشاكل بعد استكشاف الأخطاء وإصلاحها، اتصل بالدعم.</span><span class="sxs-lookup"><span data-stu-id="b8413-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="b8413-174">لمزيد من المعلومات، راجع [الحصول على الدعم](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="b8413-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="b8413-175">لا يمكن التسجيل في تطبيق الموارد البشرية في الفرق</span><span class="sxs-lookup"><span data-stu-id="b8413-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="b8413-176">إذا قام مستخدم بالاتصال بك لأنه لا يمكنه تسجيل الدخول إلى التطبيق، تحقق من أن المستخدم لديه سجل موظف مقترن في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="b8413-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="b8413-177">حدث خطا عند اعتماد طلبات المغادرة في تطبيق الموارد البشرية في الفرق</span><span class="sxs-lookup"><span data-stu-id="b8413-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="b8413-178">في حاله تلقي المستخدم خطأ أثناء محاولة الموافقة علي طلبات الإجازات في تطبيق Teams، قم بإجراء خطوات استكشاف الأخطاء وإصلاحها التالية:</span><span class="sxs-lookup"><span data-stu-id="b8413-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="b8413-179">تحقق من ان حساب الفرق الخاص بهم هو نفسه الذي يستخدم للوصول إلى الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="b8413-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="b8413-180">تحقق من انهم موافقون صالحون للطلب من خلال التحقق من إعدادات سير العمل للموافقة على المغادرة.</span><span class="sxs-lookup"><span data-stu-id="b8413-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="b8413-181">لمزيد من المعلومات حول إنهاء مهام سير العمل، راجع [إنشاء سير عمل لطلب أجازه](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b8413-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="b8413-182">لا يتلقى معتمدون الإجازات رسائل دردشة Teams للموافقة على طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="b8413-182">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="b8413-183">تأكد من تمكين الإعلامات للبيئة والمستخدم.</span><span class="sxs-lookup"><span data-stu-id="b8413-183">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="b8413-184">لمزيد من المعلومات، راجع [تمكين الإعلامات لتطبيق الموارد البشرية في Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) و[تشغيل إعلامات Teams أو إيقاف تشغيلها للمستخدمين الفرديين](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="b8413-184">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="b8413-185">تأكد من تسجيل المستخدمين الدخول إلى علامة التبويب **الدردشة** بنفس بيانات الاعتماد التي يستخدمونها للموافقة على طلبات الإجازة.</span><span class="sxs-lookup"><span data-stu-id="b8413-185">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="b8413-186">استخدم رسائل "تسجيل الخروج" ثم "تسجيل الدخول" لتسجيل الدخول باستخدام بيانات الاعتماد الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="b8413-186">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="b8413-187">إذا استمرت المشكلة، فتحقق من حالة الوظيفة الدفعية لنظام أحداث الأعمال كمسؤول عن النظام.</span><span class="sxs-lookup"><span data-stu-id="b8413-187">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="b8413-188">إذا كان في مرحلة انتظار أو تنفيذ، تحقق مرة أخرى في غضون بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="b8413-188">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="b8413-189">إذا ظلت الحالة دون تغيير، فقم بتسجيل بطاقة دعم حتى يتمكن فريقنا من المساعدة في حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="b8413-189">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b8413-190">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="b8413-190">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="b8413-191">خدمة الفهم الذكي للغة (LUIS) من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8413-191">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="b8413-192">باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي.</span><span class="sxs-lookup"><span data-stu-id="b8413-192">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="b8413-193">يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS).</span><span class="sxs-lookup"><span data-stu-id="b8413-193">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="b8413-194">أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="b8413-194">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="b8413-195">تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso).</span><span class="sxs-lookup"><span data-stu-id="b8413-195">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="b8413-196">يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b8413-196">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span>

<span data-ttu-id="b8413-197">من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b8413-197">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="b8413-198">قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b8413-198">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b8413-199">في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure.</span><span class="sxs-lookup"><span data-stu-id="b8413-199">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="b8413-200">يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b8413-200">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="b8413-201">أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="b8413-201">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="b8413-202">لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="b8413-202">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="b8413-203">Microsoft Teams وشبكة أحداث Azure وAzure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b8413-203">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="b8413-204">عند استخدام تطبيق Dynamics 365 Human Resources في Microsoft Teams، قد تتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="b8413-204">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="b8413-205">يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="b8413-205">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="b8413-206">قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة في شبكة أحداث Microsoft Azure وستتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b8413-206">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="b8413-207">لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="b8413-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="b8413-208">اثناء التحدث مع روبوت الدردشة في تطبيق Human Resources، قد يتم تخزين محتوى المحادثة في Azure Cosmos DB وإرساله إلى Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b8413-208">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="b8413-209">قد يتم تخزين هذه البيانات في Azure Cosmos DB لمدة 24 ساعة وقد تتم معالجتها خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="b8413-209">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="b8413-210">لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="b8413-210">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="b8413-211">لتقييد الوصول إلى تطبيق Human Resources في Microsoft Teams لمؤسستك أو المستخدمين في مؤسستك، راجع [إدارة سياسات أذونات التطبيق في Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="b8413-211">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="b8413-212">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b8413-212">See also</span></span> 

[<span data-ttu-id="b8413-213">تنزيل وتثبيت Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b8413-213">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="b8413-214">مركز تعليمات Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b8413-214">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="b8413-215">إدارة طلبات الإجازة في Teams</span><span class="sxs-lookup"><span data-stu-id="b8413-215">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]