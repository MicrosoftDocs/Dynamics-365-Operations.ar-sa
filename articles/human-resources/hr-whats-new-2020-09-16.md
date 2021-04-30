---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (16 سبتمبر 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 16 سبتمبر 2020.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b07bfb27bbe5e546dac9d72666b3225cc202670
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890689"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="44729-103">ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (16 سبتمبر 2020)</span><span class="sxs-lookup"><span data-stu-id="44729-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="44729-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="44729-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="44729-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="44729-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="44729-106">تشير الأرقام الموجودة بين أقواس إلى جانب بعض العناوين إلى أرقام دعم كمرجع في Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="44729-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="44729-107">الميزات المضمنة في هذا الإصدار</span><span class="sxs-lookup"><span data-stu-id="44729-107">Included in this release</span></span>

-  [<span data-ttu-id="44729-108">طرق العرض المحفوظة - التوفر العام</span><span class="sxs-lookup"><span data-stu-id="44729-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="44729-109">- لمزيد من المعلومات، راجع [طرق العرض المحفوظة](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="44729-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="44729-110">يتضمن النموذج **إجراءات المنصب** شبكة أبعاد محدّثة بالإضافة إلى مربع حوار جديد (469495).</span><span class="sxs-lookup"><span data-stu-id="44729-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="44729-111">إذا قمت بتعيين الخيار **تقييد الوصول إلى معلومات العامل** إلى "نعم" في **الوصول المتقدم** في  **المعلمات المشتركة لـ Human resources**‬، تعرض الآن نماذج المزايا العاملين المناسبين فقط (393384).</span><span class="sxs-lookup"><span data-stu-id="44729-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="44729-112">خيارات جديدة لإنشاء التقويم في كيان **WorkCalendar** ‏(477055):</span><span class="sxs-lookup"><span data-stu-id="44729-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="44729-113">- وقت الانتهاء الافتراضي</span><span class="sxs-lookup"><span data-stu-id="44729-113">- Default ending time</span></span><br><span data-ttu-id="44729-114">- وقت البدء الافتراضي</span><span class="sxs-lookup"><span data-stu-id="44729-114">-    Default starting time</span></span><br><span data-ttu-id="44729-115">- هل يوم الجمعة يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-115">-  Is Friday working day</span></span><br><span data-ttu-id="44729-116">- هل يوم الإثنين يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-116">-  Is Monday working day</span></span><br><span data-ttu-id="44729-117">- هل يوم السبت يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-117">-  Is Saturday working day</span></span><br><span data-ttu-id="44729-118">- هل يوم الأحد يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-118">- Is Sunday working day</span></span><br><span data-ttu-id="44729-119">- هل يوم الخميس يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-119">- Is Thursday working day</span></span><br><span data-ttu-id="44729-120">- هل يوم الثلاثاء يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-120">- Is Tuesday working day</span></span><br><span data-ttu-id="44729-121">- هل يوم الأربعاء يوم عمل</span><span class="sxs-lookup"><span data-stu-id="44729-121">- Is Wednesday working day</span></span><br><span data-ttu-id="44729-122">- معرف إجازة تقويم العمل</span><span class="sxs-lookup"><span data-stu-id="44729-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="44729-123">يتضمن الآن الكيان **LeaveBankTransactionV1** كود السبب (477823).</span><span class="sxs-lookup"><span data-stu-id="44729-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="44729-124">يمكنك الآن حفظ تسجيلات المهمة (492923).</span><span class="sxs-lookup"><span data-stu-id="44729-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="44729-125">يتم الآن نشر البيانات بنجاح من **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="44729-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="44729-126">تظهر الآن علامة التبويب السريعة **التعويض** لنوع العامل المقاول في النموذج **إجراءات العامل** (482494).</span><span class="sxs-lookup"><span data-stu-id="44729-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="44729-127">الحقلان **المستوى** و **الخطة** إلزاميان الآن إذا قمت بتعيين **التعويض الثابت**.</span><span class="sxs-lookup"><span data-stu-id="44729-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="44729-128">تظهر رسالة خطأ إذا تركت هذه الحقول فارغة (482497).</span><span class="sxs-lookup"><span data-stu-id="44729-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="44729-129">الحقل **نوع الخطة** في **المزايا** هو الآن قائمة منسدلة (488768).</span><span class="sxs-lookup"><span data-stu-id="44729-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="44729-130">يتلقى مسؤولو النظام الآن إعلامًا إذا تم حذف حقل مخصص من Human Resources (481408).</span><span class="sxs-lookup"><span data-stu-id="44729-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="44729-131">أثناء عملية إنهاء خدمات الموظف، يتصرف Human Resources كما هو متوقع، ولا يغيّر الشركة المحددة بعد أن يبدو وكأنه تم تأمينه (479877).</span><span class="sxs-lookup"><span data-stu-id="44729-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="44729-132">لم يعد بإمكان المدراء إضافة عمود رقمي من خلال التخصيص (485317).</span><span class="sxs-lookup"><span data-stu-id="44729-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="44729-133">لن يعد بإمكان المدراء إزالة عامل تصفية نطاق البيانات من أرقام التعريف التي ستنتهي صلاحيتها (485321).</span><span class="sxs-lookup"><span data-stu-id="44729-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="44729-134">عندما يكون الحقل **مسؤول أمام** فارغًا، تستمر تفاصيل المنصب في الظهور عند تمرير الماوس فوق المنصب (433328).</span><span class="sxs-lookup"><span data-stu-id="44729-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="44729-135">بإمكان الموظفين الآن عرض معلومات خطة المزايا في خدمة الموظف الذاتية (481676).</span><span class="sxs-lookup"><span data-stu-id="44729-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="44729-136">بإمكان الموظفين الآن رؤية كافة الدورات التدريبية المسجلة (429048).</span><span class="sxs-lookup"><span data-stu-id="44729-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="44729-137">يمكنك الآن تقييد خيارات العرض لصفحة **الشهادات المهنية**.</span><span class="sxs-lookup"><span data-stu-id="44729-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="44729-138">يمكنك تقييد خيارات العرض للكيان القانوني الحالي حسب  حالة العامل ونوع العامل (451501).</span><span class="sxs-lookup"><span data-stu-id="44729-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="44729-139">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="44729-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="44729-140">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="44729-140">Human Resources app in Teams</span></span>

<span data-ttu-id="44729-141">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="44729-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="44729-142">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="44729-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="44729-143">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="44729-143">For more information, see:</span></span>

- <span data-ttu-id="44729-144">[تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬</span><span class="sxs-lookup"><span data-stu-id="44729-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="44729-145">[تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="44729-146">تطبيق Human Resources في ميزات المعاينة لـ Teams</span><span class="sxs-lookup"><span data-stu-id="44729-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="44729-147">**الإخطارات**: سوف يتم إعلام المُرسلين والمعتمدين لطلبات الإجازات في تطبيق Human Resources في Teams.</span><span class="sxs-lookup"><span data-stu-id="44729-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="44729-148">بإمكان الموافقين الموافقة على طلبات الإجازة أو رفضها.</span><span class="sxs-lookup"><span data-stu-id="44729-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="44729-149">سيتم اعلام مقدمي الطلبات ما إذا تمت الموافقة على طلبهم أم رفضه.</span><span class="sxs-lookup"><span data-stu-id="44729-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="44729-150">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="44729-150">For more information, see:</span></span>
   - <span data-ttu-id="44729-151">[تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬</span><span class="sxs-lookup"><span data-stu-id="44729-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="44729-152">[تمكين الإعلامات لتطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="44729-153">[تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="44729-154">[إعلامات Teams](./hr-teams-leave-app.md#respond-to-teams-notifications) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="44729-155">[عرض تقويم إجازة الفريق](./hr-teams-leave-app.md#view-your-teams-leave-calendar) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="44729-156">**تقويم إجازة المُدير**: بإمكان المدراء رؤية الإجازات الموافق عليها والمعلقة لمرؤوسيهم المباشرين في طريقة عرض التقويم.</span><span class="sxs-lookup"><span data-stu-id="44729-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="44729-157">توفر طريقة العرض هذه طريقة سهلة في الفهم عند انقطاع أعضاء فريقهم عن العمل.</span><span class="sxs-lookup"><span data-stu-id="44729-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="44729-158">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="44729-158">For more information, see:</span></span>
   - <span data-ttu-id="44729-159">[تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬</span><span class="sxs-lookup"><span data-stu-id="44729-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="44729-160">[عرض تقويم إجازة الفريق](./hr-teams-leave-app.md#view-your-teams-leave-calendar) في وثائق Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="44729-161">خيار التكوين لوضع عناصر العمل المعينة لي في قائمة (477004)</span><span class="sxs-lookup"><span data-stu-id="44729-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="44729-162">يتوفر الآن خيار جديد الآن لوضع قائمة **عناصر العمل التي تم تعيينها لي** في العمود الأيسر في لوحه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="44729-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="44729-163">مع هذا التغيير، تظهر كافة عناصر العمل وقوائم المهام في نفس الناحية.</span><span class="sxs-lookup"><span data-stu-id="44729-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="44729-164">يمكنك تمكين هذه الوظيفة عن طريق تشغيل **المعاينة - تحسينات تجربة سير العمل** في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="44729-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="44729-165">للحصول على مزيد من المعلومات حول تشغيل ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="44729-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="44729-166">تقوم هذه الميزة أيضًا بترقية خيارات سير العمل التي تظهر في نماذج إجراءات العاملين.</span><span class="sxs-lookup"><span data-stu-id="44729-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="44729-167">تظهر خيارات سير العمل أيضًا أعلى علامة التبويب السريعة للإجراءات لتمكين الوصول السريع إليها.</span><span class="sxs-lookup"><span data-stu-id="44729-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="44729-168">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="44729-168">For more information, see:</span></span> 

- <span data-ttu-id="44729-169">[تحسينات في تجربة سير عمل إدارة المؤسسة والموظفين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬</span><span class="sxs-lookup"><span data-stu-id="44729-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![عناصر عمل تم تعيينها إلي](./media/hr-workflow-work-items-assigned-to-me.png)

![الوصول السريع إلى عناصر سير العمل](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="44729-172">تقويم الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="44729-172">Leave and absence calendar</span></span>

<span data-ttu-id="44729-173">يتضمن هذا الإصدار خيارات تقويم إضافية لتقويمات الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="44729-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="44729-174">لمزيد من المعلومات، راجع [عرض تقويمات الفريق والشركة](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="44729-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="44729-175">قريبًا</span><span class="sxs-lookup"><span data-stu-id="44729-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="44729-176">تضمين كيانات قائمة الاختيار في Dataverse</span><span class="sxs-lookup"><span data-stu-id="44729-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="44729-177">ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="44729-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="44729-178">أكواد سبب إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="44729-178">Benefits management reason codes</span></span>

<span data-ttu-id="44729-179">سيتم دمج أكواد سبب إدارة الميزات في وقت قريب مع أكواد السبب الموجودة في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="44729-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="44729-180">إذا قمت بإنشاء أكواد أسباب في إدارة الميزات تزيد عن 15 حرفًا، فيجب تغيير اسم كود السبب في نموذج **أكواد السبب** في إدارة الميزات بحيث تتكون من 15 حرفًا أو أقل.</span><span class="sxs-lookup"><span data-stu-id="44729-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="44729-181">بعد تحديث الاسم، سيظهر كود السبب ضمن نموذج كود السبب في إدارة العاملين.</span><span class="sxs-lookup"><span data-stu-id="44729-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="44729-182">سيتوفر هذا التغيير في المستقبل ولن يؤثر على الوظيفة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="44729-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="44729-183">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="44729-183">See also</span></span>

[<span data-ttu-id="44729-184">الميزات الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="44729-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="44729-185">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="44729-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="44729-186">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="44729-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="44729-187">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="44729-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
