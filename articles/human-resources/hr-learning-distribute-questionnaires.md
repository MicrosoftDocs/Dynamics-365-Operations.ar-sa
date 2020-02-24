---
title: توزيع الاستبيانات وجدولتها
description: توضح هذه المقالة كيفية توزيع الاستبيانات التي تقوم بتصميمها، بحيث تكون متوفرة لشخص أو مجموعة الأشخاص الذين سيقومون بإكمالها.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5372841c841e82d116381d7ce8fe48af8ddfb036
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007945"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="fad58-103">توزيع الاستبيانات وجدولتها</span><span class="sxs-lookup"><span data-stu-id="fad58-103">Distribute and schedule questionnaires</span></span>

<span data-ttu-id="fad58-104">توضح هذه المقالة كيفية توزيع الاستبيانات التي تقوم بتصميمها، بحيث تكون متوفرة لشخص أو مجموعة الأشخاص الذين سيقومون بإكمالها.</span><span class="sxs-lookup"><span data-stu-id="fad58-104">This article explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="fad58-105">هناك عدة طرق لتوزيع الاستبيان:</span><span class="sxs-lookup"><span data-stu-id="fad58-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="fad58-106">وضع علامة على الاستبيان كنشط.</span><span class="sxs-lookup"><span data-stu-id="fad58-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="fad58-107">بعد ذلك، يتوفر الاستبيان لكافة الموظفين، إلا إذا تم إعداد مجموعة استبيان لتقييد الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="fad58-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="fad58-108">تعيين حقوق إلى مجموعة استبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="fad58-109">يتوفر الاستبيان بعد ذلك لكافة أعضاء المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="fad58-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="fad58-110">إنشاء جلسات الإجابات المخططة.</span><span class="sxs-lookup"><span data-stu-id="fad58-110">Create planned answer sessions.</span></span> <span data-ttu-id="fad58-111">يتوفر الاستبيان بعد ذلك للشخص المعيَّن فقط.</span><span class="sxs-lookup"><span data-stu-id="fad58-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="fad58-112">إنشاء جدول.</span><span class="sxs-lookup"><span data-stu-id="fad58-112">Create a schedule.</span></span> <span data-ttu-id="fad58-113">قد يتوفر الاستبيان بعد ذلك لعدة أشخاص.</span><span class="sxs-lookup"><span data-stu-id="fad58-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="fad58-114">وضع علامة على الاستبيان كنشط</span><span class="sxs-lookup"><span data-stu-id="fad58-114">Marking a questionnaire as active</span></span>

<span data-ttu-id="fad58-115">‏‫من خلال تعيين الحقل **نشط‬‏‫** إلى **نعم‬‏‫** في صفحة **الاستبيانات‬‏‫**، يمكنك توفير الاستبيان لجميع الموظفين لإكماله.</span><span class="sxs-lookup"><span data-stu-id="fad58-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="fad58-116">ويمكن للمستجيبين إكمال الاستبيان عدة مرات.</span><span class="sxs-lookup"><span data-stu-id="fad58-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="fad58-117">وتفيد هذه الوظيفة إذا كنت تريد جمع التعليقات المستمرة طوال العام.‬</span><span class="sxs-lookup"><span data-stu-id="fad58-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="fad58-118">على سبيل المثال، يمكن إجراء استبيان يسخدمه الموظفون لتقديم بعض الملاحظات حول خدمة الغداء في الكافتيريا.</span><span class="sxs-lookup"><span data-stu-id="fad58-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="fad58-119">مجموعة استبيانات</span><span class="sxs-lookup"><span data-stu-id="fad58-119">Questionnaire groups</span></span>

<span data-ttu-id="fad58-120">يمكنك إعداد مجموعات الاستبيان، ثم تضمين المستجيبين الذين يجب توزيع استبيان عليهم.</span><span class="sxs-lookup"><span data-stu-id="fad58-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="fad58-121">ويمكنك إنشاء صفحات الاستبيان من الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="fad58-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="fad58-122">**مجموعات الاستبيان**– فقط الأفراد في مجموعة استبيان يمكنهم إكمال استبيان محدد.</span><span class="sxs-lookup"><span data-stu-id="fad58-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="fad58-123">على سبيل المثال، جمهورك المستهدف هم المقاولون، حيث يمكنك إنشاء مجموعة استبيان خاصة بأولئك المستجيبين.</span><span class="sxs-lookup"><span data-stu-id="fad58-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="fad58-124">**أعضاء مجموعة الاستبيان** – يمكنك إضافة أشخاص إلى مجموعات الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="fad58-125">‏‫لتعيين مجموعة استبيان إلى استبيان، في صفحة **الاستبيانات‬‏‫**‬‏‫، انقر فوق **حقوق المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="fad58-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="fad58-126">وبعد حفظ الاستبيان كنشط، يمكن لأعضاء مجموعة الاستبيان إكماله.</span><span class="sxs-lookup"><span data-stu-id="fad58-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="fad58-127">وتفيد هذه الوظيفة إذا كنت تريد اختبار استبيان في مجموعة محددة من الأشخاص قبل أن يمكنك إخراجه لمجموعة أكبر، أو إذا كنت ترغب في توجيه استبيان إلى جمهور محدد جداً.‬</span><span class="sxs-lookup"><span data-stu-id="fad58-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="fad58-128">جلسات الإجابات المخططة في الاستبيان</span><span class="sxs-lookup"><span data-stu-id="fad58-128">Planned answer sessions in a questionnaire</span></span>

<span data-ttu-id="fad58-129">جلسات الإجابات المخططة هي الاستبيانات التي قمت بتصميم وتحديد المستجيبين لها.</span><span class="sxs-lookup"><span data-stu-id="fad58-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
> <span data-ttu-id="fad58-130">قبل أن تتمكن من إعداد جلسات الإجابات المخططة، يجب عليك تصميم استبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="fad58-131">في صفحة **جلسة الإجابة المخططة**، يُمكنك إنشاء جلسة إجابة مخططة لموظف واحد.</span><span class="sxs-lookup"><span data-stu-id="fad58-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="fad58-132">تعرض القائمة في الصفحة كافة الاستبيانات المخططة.</span><span class="sxs-lookup"><span data-stu-id="fad58-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="fad58-133">وتستخدم جلسات الإجابة المخططة أيضًا في صفحة **جداول الاستبيانات‬** حيث يُمكنك تخطيط استبيانات لعدة أشخاص وهم:</span><span class="sxs-lookup"><span data-stu-id="fad58-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="fad58-134">الموظفون</span><span class="sxs-lookup"><span data-stu-id="fad58-134">Employees</span></span>
-   <span data-ttu-id="fad58-135">المشاركون في الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="fad58-135">Course participants</span></span>
-   <span data-ttu-id="fad58-136">الوحدات المؤسسية</span><span class="sxs-lookup"><span data-stu-id="fad58-136">Organizational units</span></span>

<span data-ttu-id="fad58-137">يمكن لكل شخص الإجابة عن الاستبيان مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="fad58-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="fad58-138">جدولة استبيان</span><span class="sxs-lookup"><span data-stu-id="fad58-138">Scheduling a questionnaire</span></span>

<span data-ttu-id="fad58-139">يمكنك جدولة استبيان لعدة مستجيبين اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="fad58-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="fad58-140">أنواع التخطيط</span><span class="sxs-lookup"><span data-stu-id="fad58-140">Planning types</span></span>

<span data-ttu-id="fad58-141">أنواع التخطيط مطلوبة إذا كنت تريد جدولة جلسات الإجابات المخططة لعدة مستجيبين.</span><span class="sxs-lookup"><span data-stu-id="fad58-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="fad58-142">ويتم استخدام أنواع التخطيط لتصنيف جداول الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="fad58-143">على سبيل المثال، يمكنك جدولة استبيانات الجداول للأغراض التالية:</span><span class="sxs-lookup"><span data-stu-id="fad58-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="fad58-144">التقييم</span><span class="sxs-lookup"><span data-stu-id="fad58-144">Evaluation</span></span>
-   <span data-ttu-id="fad58-145">استقصاء</span><span class="sxs-lookup"><span data-stu-id="fad58-145">Survey</span></span>
-   <span data-ttu-id="fad58-146">الاختبار</span><span class="sxs-lookup"><span data-stu-id="fad58-146">Testing</span></span>

<span data-ttu-id="fad58-147">يمكنك تحديد أنواع التخطيط لجدول استبيان في صفحة **جداول الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="fad58-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="fad58-148">أنواع المراجع للاستبيان</span><span class="sxs-lookup"><span data-stu-id="fad58-148">Reference types for questionnaire</span></span>

<span data-ttu-id="fad58-149">يمكنك استخدام أنواع المرجع لإدخال معايير للمستجيبين الذين قد تحددهم عندما تقوم بجدولة استبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="fad58-150">واستخدام صفحة **أنواع المراجع** لإعداد أنواع المرجع لاستبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="fad58-151">يتوافق كل نوع مرجع مع جدول في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fad58-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="fad58-152">وعند إنشاء جداول الاستبيان، يمكنك تحديد السجلات الفردية في الجدول أو مجموعة السجلات التي سيتم إقران الاستبيان بها.</span><span class="sxs-lookup"><span data-stu-id="fad58-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="fad58-153">على سبيل المثال، إذا قمت بتحديد جدول الدورات التدريبية، يمكنك أن تقرر أي دورات تدريبية معينة سيُخصص الاستبيان لها.</span><span class="sxs-lookup"><span data-stu-id="fad58-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="fad58-154">وعند إعداد مرجع لجدول الدورات، تتوفر بعض الحقول والأزرار في صفحة **الدورات**.</span><span class="sxs-lookup"><span data-stu-id="fad58-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="fad58-155">جداول الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="fad58-155">Questionnaire schedules</span></span>

<span data-ttu-id="fad58-156">‏‫يمكنك استخدام جداول الاستبيان لإنشاء عدة جلسات إجابات مخططة لمجموعة من المستخدمين، استناداً إلى نوع مرجع.</span><span class="sxs-lookup"><span data-stu-id="fad58-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="fad58-157">قم بإنشاء جدول في صفحة **جداول الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="fad58-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="fad58-158">وحدد نوع تخطيط لتصنيف الجدول، وحدد أيضًا نوع المرجع الذي يجب استخدامه للاستعلام عن النظام لمستخدمين محددين.</span><span class="sxs-lookup"><span data-stu-id="fad58-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="fad58-159">على سبيل المثال، إذا قمت بتعيين نوع المرجع إلى جدول الدورات التدريبية، يمكنك تحديد مسار محدد في حقل **المرجع**.</span><span class="sxs-lookup"><span data-stu-id="fad58-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="fad58-160">وانقر فوق **تفاصيل الإعداد** لتحديد الاستبيان والمعايير الأخرى.</span><span class="sxs-lookup"><span data-stu-id="fad58-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="fad58-161">على سبيل المثال، حدد اسم المعلم كمعيار إذا كان الاستبيان تقييمًا للمعلم.</span><span class="sxs-lookup"><span data-stu-id="fad58-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="fad58-162">وبعد الانتهاء من إدخال تفاصيل الإعداد، يقوم النظام بإنشاء جلسات إجابات مخططة للمستخدمين الذين سيتم تضمينهم في الاستعلام.‬</span><span class="sxs-lookup"><span data-stu-id="fad58-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="fad58-163">وانقر فوق **جلسات الإجابات المخططة** لعرض جلسات الإجابات للجدول.</span><span class="sxs-lookup"><span data-stu-id="fad58-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="fad58-164">ويمكنك بعد ذلك يدوياً إنشاء جلسات إجابات مخططة إضافية أو حذف جلسات الإجابات المخططة التي لم يتم الرد عليها.</span><span class="sxs-lookup"><span data-stu-id="fad58-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="fad58-165">انقر فوق **المهام** &gt; **البدء‬** لتوفير الاستبيان للمستخدمين في جلسات الإجابات المخططة ذات الصلة.‬</span><span class="sxs-lookup"><span data-stu-id="fad58-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="fad58-166">وانقر فوق **إجابات** لعرض الإجابات المكتملة للاستبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="fad58-167">ويمكنك بشكل اختياري نسخ إعدادات جدولة الاستبيان، وجلسات الإجابات المخططة، والإجابات على جدول استبيان جديد.</span><span class="sxs-lookup"><span data-stu-id="fad58-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="fad58-168">إخطار المستجيبين بالاستبيانات المتوفرة لهم</span><span class="sxs-lookup"><span data-stu-id="fad58-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="fad58-169">عندما تقوم بتوزيع استبيان، فإنه يُطلب منك إخطار المشاركين بأن الاستبيانات متاحة لهم.</span><span class="sxs-lookup"><span data-stu-id="fad58-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="fad58-170">إخطار المستجيبين بجلسة إجابة مخططة</span><span class="sxs-lookup"><span data-stu-id="fad58-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="fad58-171">إذا كنت تستخدم جلسة إجابة مخططة، يجب عليك إخطار الشخص مباشرةً، مثل بواسطة الهاتف أو البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="fad58-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="fad58-172">إخطار المستجيبين بجدولة</span><span class="sxs-lookup"><span data-stu-id="fad58-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="fad58-173">استخدم صفحة **جداول الاستبيانات** لإعداد رسالة بريد إلكتروني وإرسالها إلى جميع المشاركين الذين تم تعيينهم للاستبيان.</span><span class="sxs-lookup"><span data-stu-id="fad58-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="fad58-174">أدخل نص البريد الإلكتروني على علامة تبويب **بريد إلكتروني لخدمة الموظف الذاتية‬‬‏‫**. بعد بدء الجدول، انقر فوق **الوظائف** &gt; **إرسال بريد إلكتروني** لإنشاء البريد الإلكتروني وإرساله للمستجيبين.</span><span class="sxs-lookup"><span data-stu-id="fad58-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="fad58-175">ويمكن للمستجيبين فيما بعد تسجيل الدخول إلى موقع الويب وإكمال الاستبيان.‬</span><span class="sxs-lookup"><span data-stu-id="fad58-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="fad58-176">قبل استخدام وظيفة البريد الإلكتروني، يجب على مسؤول تكنولوجيا المعلومات إدخال إعدادات البريد الإلكتروني في صفحة **معلمات البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="fad58-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="fad58-177">إنهاء استبيان مجدول</span><span class="sxs-lookup"><span data-stu-id="fad58-177">Ending a scheduled questionnaire</span></span>

<span data-ttu-id="fad58-178">يمكن إنهاء استبيان مجدول بعد قيام كل المستجيبين بإكمال جلسات الإجابة المخصصة لهم.</span><span class="sxs-lookup"><span data-stu-id="fad58-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="fad58-179">وبعد إنهاء استبيان مجدول، لا يمكنك نسخ إعداداته إلى جدول جديد.</span><span class="sxs-lookup"><span data-stu-id="fad58-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="fad58-180">في حالة عدم إكمال الاستبيان من قبل مستجيب واحد أو أكثر، ولكنك مع ذلك تريد إنهاء الجدولة، فيجب عليك أولاً حذف أولئك المستجيبين من القائمة في صفحة **جلسة الإجابة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="fad58-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="fad58-181">ويمكنك حينئذٍ إنهاء الجدولة.</span><span class="sxs-lookup"><span data-stu-id="fad58-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="fad58-182">استكمال الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="fad58-182">Completing questionnaires</span></span>

<span data-ttu-id="fad58-183">بعد قيامك تصميم وتوزيع استبيان، يمكن إكمال الاستبيان بواسطة المستجيبين المحددة.</span><span class="sxs-lookup"><span data-stu-id="fad58-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="fad58-184">يمكن إكمال الاستبيانات المتاحة لك من موقعين:</span><span class="sxs-lookup"><span data-stu-id="fad58-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="fad58-185">في جزء التنقل، انقر فوق **الاستبيانات‬** &gt; **توزيع** &gt; **‎إكمال استبيان**.</span><span class="sxs-lookup"><span data-stu-id="fad58-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="fad58-186">في الخدمة الذاتية للموظف، انقر فوق **الاستبيانات المراد إكمالها**.</span><span class="sxs-lookup"><span data-stu-id="fad58-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="fad58-187">يمكن توفير الاستبيانات لمستخدمين أو مجموعات مستخدمين محددة أو لجميع الموظفين في شبكة.</span><span class="sxs-lookup"><span data-stu-id="fad58-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>


