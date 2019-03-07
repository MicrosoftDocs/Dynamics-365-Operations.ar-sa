---
title: جدولة الاستبيانات وتوزيعها
description: يوضح هذا الموضوع كيفية توزيع الاستبيانات التي تقوم بتصميمها، بحيث تكون متوفرة لشخص أو مجموعة الأشخاص الذين سيقومون بإكمالها.
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eafcb047117eab73fddbd93c4c1d0aafb0023ebd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303063"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="71dcf-103">جدولة الاستبيانات وتوزيعها</span><span class="sxs-lookup"><span data-stu-id="71dcf-103">Distribute and schedule questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71dcf-104">يوضح هذا الموضوع كيفية توزيع الاستبيانات التي تقوم بتصميمها، بحيث تكون متوفرة لشخص أو مجموعة الأشخاص الذين سيقومون بإكمالها.</span><span class="sxs-lookup"><span data-stu-id="71dcf-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="71dcf-105">هناك عدة طرق لتوزيع الاستبيان:</span><span class="sxs-lookup"><span data-stu-id="71dcf-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="71dcf-106">وضع علامة على الاستبيان كنشط.</span><span class="sxs-lookup"><span data-stu-id="71dcf-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="71dcf-107">بعد ذلك، يتوفر الاستبيان لكافة الموظفين، إلا إذا تم إعداد مجموعة استبيان لتقييد الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="71dcf-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="71dcf-108">تعيين حقوق إلى مجموعة استبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="71dcf-109">يتوفر الاستبيان بعد ذلك لكافة أعضاء المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="71dcf-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="71dcf-110">إنشاء جلسات الإجابات المخططة.</span><span class="sxs-lookup"><span data-stu-id="71dcf-110">Create planned answer sessions.</span></span> <span data-ttu-id="71dcf-111">يتوفر الاستبيان بعد ذلك للشخص المعيَّن فقط.</span><span class="sxs-lookup"><span data-stu-id="71dcf-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="71dcf-112">إنشاء جدول.</span><span class="sxs-lookup"><span data-stu-id="71dcf-112">Create a schedule.</span></span> <span data-ttu-id="71dcf-113">قد يتوفر الاستبيان بعد ذلك لعدة أشخاص.</span><span class="sxs-lookup"><span data-stu-id="71dcf-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="71dcf-114">وضع علامة على الاستبيان كنشط</span><span class="sxs-lookup"><span data-stu-id="71dcf-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="71dcf-115">‏‫من خلال تعيين الحقل **نشط‬‏‫** إلى **نعم‬‏‫** في صفحة **الاستبيانات‬‏‫**، يمكنك توفير الاستبيان لجميع الموظفين لإكماله.</span><span class="sxs-lookup"><span data-stu-id="71dcf-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="71dcf-116">ويمكن للمستجيبين إكمال الاستبيان عدة مرات.</span><span class="sxs-lookup"><span data-stu-id="71dcf-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="71dcf-117">وتفيد هذه الوظيفة إذا كنت تريد جمع التعليقات المستمرة طوال العام.‬</span><span class="sxs-lookup"><span data-stu-id="71dcf-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="71dcf-118">على سبيل المثال، يمكن إجراء استبيان يسخدمه الموظفون لتقديم بعض الملاحظات حول خدمة الغداء في الكافتيريا.</span><span class="sxs-lookup"><span data-stu-id="71dcf-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="71dcf-119">مجموعة استبيانات</span><span class="sxs-lookup"><span data-stu-id="71dcf-119">Questionnaire groups</span></span>
<span data-ttu-id="71dcf-120">يمكنك إعداد مجموعات الاستبيان، ثم تضمين المستجيبين الذين يجب توزيع استبيان عليهم.</span><span class="sxs-lookup"><span data-stu-id="71dcf-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="71dcf-121">ويمكنك إنشاء صفحات الاستبيان من الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="71dcf-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="71dcf-122">**مجموعات الاستبيان**– فقط الأفراد في مجموعة استبيان يمكنهم إكمال استبيان محدد.</span><span class="sxs-lookup"><span data-stu-id="71dcf-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="71dcf-123">على سبيل المثال، جمهورك المستهدف هم المقاولون، حيث يمكنك إنشاء مجموعة استبيان خاصة بأولئك المستجيبين.</span><span class="sxs-lookup"><span data-stu-id="71dcf-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="71dcf-124">**أعضاء مجموعة الاستبيان** – يمكنك إضافة أشخاص إلى مجموعات الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="71dcf-125">‏‫لتعيين مجموعة استبيان إلى استبيان، في صفحة **الاستبيانات‬‏‫**‬‏‫، انقر فوق **حقوق المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="71dcf-126">وبعد حفظ الاستبيان كنشط، يمكن لأعضاء مجموعة الاستبيان إكماله.</span><span class="sxs-lookup"><span data-stu-id="71dcf-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="71dcf-127">وتفيد هذه الوظيفة إذا كنت تريد اختبار استبيان في مجموعة محددة من الأشخاص قبل أن يمكنك إخراجه لمجموعة أكبر، أو إذا كنت ترغب في توجيه استبيان إلى جمهور محدد جداً.‬</span><span class="sxs-lookup"><span data-stu-id="71dcf-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="71dcf-128">جلسات الإجابات المخططة في الاستبيان</span><span class="sxs-lookup"><span data-stu-id="71dcf-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="71dcf-129">جلسات الإجابات المخططة هي الاستبيانات التي قمت بتصميم وتحديد المستجيبين لها.</span><span class="sxs-lookup"><span data-stu-id="71dcf-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="71dcf-130">**ملاحظة:** قبل أن تتمكن من إعداد جلسات الإجابات المخططة، يجب عليك تصميم استبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="71dcf-131">في صفحة **جلسة الإجابة المخططة**، يُمكنك إنشاء جلسة إجابة مخططة لموظف واحد.</span><span class="sxs-lookup"><span data-stu-id="71dcf-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="71dcf-132">تعرض القائمة في الصفحة كافة الاستبيانات المخططة.</span><span class="sxs-lookup"><span data-stu-id="71dcf-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="71dcf-133">وتستخدم جلسات الإجابة المخططة أيضًا في صفحة **جداول الاستبيانات‬** حيث يُمكنك تخطيط استبيانات لعدة أشخاص وهم:</span><span class="sxs-lookup"><span data-stu-id="71dcf-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="71dcf-134">الموظفون</span><span class="sxs-lookup"><span data-stu-id="71dcf-134">Employees</span></span>
-   <span data-ttu-id="71dcf-135">المشاركون في الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="71dcf-135">Course participants</span></span>
-   <span data-ttu-id="71dcf-136">الوحدات المؤسسية</span><span class="sxs-lookup"><span data-stu-id="71dcf-136">Organizational units</span></span>

<span data-ttu-id="71dcf-137">يمكن لكل شخص الإجابة عن الاستبيان مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="71dcf-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="71dcf-138">جدولة استبيان</span><span class="sxs-lookup"><span data-stu-id="71dcf-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="71dcf-139">يمكنك جدولة استبيان لعدة مستجيبين اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="71dcf-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="71dcf-140">أنواع التخطيط</span><span class="sxs-lookup"><span data-stu-id="71dcf-140">Planning types</span></span>

<span data-ttu-id="71dcf-141">أنواع التخطيط مطلوبة إذا كنت تريد جدولة جلسات الإجابات المخططة لعدة مستجيبين.</span><span class="sxs-lookup"><span data-stu-id="71dcf-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="71dcf-142">ويتم استخدام أنواع التخطيط لتصنيف جداول الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="71dcf-143">على سبيل المثال، يمكنك جدولة استبيانات الجداول للأغراض التالية:</span><span class="sxs-lookup"><span data-stu-id="71dcf-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="71dcf-144">التقييم</span><span class="sxs-lookup"><span data-stu-id="71dcf-144">Evaluation</span></span>
-   <span data-ttu-id="71dcf-145">استقصاء</span><span class="sxs-lookup"><span data-stu-id="71dcf-145">Survey</span></span>
-   <span data-ttu-id="71dcf-146">الاختبار</span><span class="sxs-lookup"><span data-stu-id="71dcf-146">Testing</span></span>

<span data-ttu-id="71dcf-147">يمكنك تحديد أنواع التخطيط لجدول استبيان في صفحة **جداول الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="71dcf-148">أنواع المراجع للاستبيان</span><span class="sxs-lookup"><span data-stu-id="71dcf-148">Reference types for questionnaire</span></span>

<span data-ttu-id="71dcf-149">يمكنك استخدام أنواع المرجع لإدخال معايير للمستجيبين الذين قد تحددهم عندما تقوم بجدولة استبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="71dcf-150">واستخدام صفحة **أنواع المراجع** لإعداد أنواع المرجع لاستبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="71dcf-151">يتوافق كل نوع مرجع مع جدول في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="71dcf-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="71dcf-152">وعند إنشاء جداول الاستبيان، يمكنك تحديد السجلات الفردية في الجدول أو مجموعة السجلات التي سيتم إقران الاستبيان بها.</span><span class="sxs-lookup"><span data-stu-id="71dcf-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="71dcf-153">على سبيل المثال، إذا قمت بتحديد جدول الدورات التدريبية، يمكنك أن تقرر أي دورات تدريبية معينة سيُخصص الاستبيان لها.</span><span class="sxs-lookup"><span data-stu-id="71dcf-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="71dcf-154">وعند إعداد مرجع لجدول الدورات، تتوفر بعض الحقول والأزرار في صفحة **الدورات**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="71dcf-155">جداول الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="71dcf-155">Questionnaire schedules</span></span>

<span data-ttu-id="71dcf-156">‏‫يمكنك استخدام جداول الاستبيان لإنشاء عدة جلسات إجابات مخططة لمجموعة من المستخدمين، استناداً إلى نوع مرجع.</span><span class="sxs-lookup"><span data-stu-id="71dcf-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="71dcf-157">قم بإنشاء جدول في صفحة **جداول الاستبيان**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="71dcf-158">وحدد نوع تخطيط لتصنيف الجدول، وحدد أيضًا نوع المرجع الذي يجب استخدامه للاستعلام عن النظام لمستخدمين محددين.</span><span class="sxs-lookup"><span data-stu-id="71dcf-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="71dcf-159">على سبيل المثال، إذا قمت بتعيين نوع المرجع إلى جدول الدورات التدريبية، يمكنك تحديد مسار محدد في حقل **المرجع**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="71dcf-160">وانقر فوق **تفاصيل الإعداد** لتحديد الاستبيان والمعايير الأخرى.</span><span class="sxs-lookup"><span data-stu-id="71dcf-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="71dcf-161">على سبيل المثال، حدد اسم المعلم كمعيار إذا كان الاستبيان تقييمًا للمعلم.</span><span class="sxs-lookup"><span data-stu-id="71dcf-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="71dcf-162">وبعد الانتهاء من إدخال تفاصيل الإعداد، يقوم النظام بإنشاء جلسات إجابات مخططة للمستخدمين الذين سيتم تضمينهم في الاستعلام.‬</span><span class="sxs-lookup"><span data-stu-id="71dcf-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="71dcf-163">وانقر فوق **جلسات الإجابات المخططة** لعرض جلسات الإجابات للجدول.</span><span class="sxs-lookup"><span data-stu-id="71dcf-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="71dcf-164">ويمكنك بعد ذلك يدوياً إنشاء جلسات إجابات مخططة إضافية أو حذف جلسات الإجابات المخططة التي لم يتم الرد عليها.</span><span class="sxs-lookup"><span data-stu-id="71dcf-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="71dcf-165">انقر فوق **المهام** &gt; **البدء‬** لتوفير الاستبيان للمستخدمين في جلسات الإجابات المخططة ذات الصلة.‬</span><span class="sxs-lookup"><span data-stu-id="71dcf-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="71dcf-166">وانقر فوق **إجابات** لعرض الإجابات المكتملة للاستبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="71dcf-167">ويمكنك بشكل اختياري نسخ إعدادات جدولة الاستبيان، وجلسات الإجابات المخططة، والإجابات على جدول استبيان جديد.</span><span class="sxs-lookup"><span data-stu-id="71dcf-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="71dcf-168">إخطار المستجيبين بالاستبيانات المتوفرة لهم</span><span class="sxs-lookup"><span data-stu-id="71dcf-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="71dcf-169">عندما تقوم بتوزيع استبيان، فإنه يُطلب منك إخطار المشاركين بأن الاستبيانات متاحة لهم.</span><span class="sxs-lookup"><span data-stu-id="71dcf-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="71dcf-170">إخطار المستجيبين بجلسة إجابة مخططة</span><span class="sxs-lookup"><span data-stu-id="71dcf-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="71dcf-171">إذا كنت تستخدم جلسة إجابة مخططة، يجب عليك إخطار الشخص مباشرةً، مثل بواسطة الهاتف أو البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="71dcf-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="71dcf-172">إخطار المستجيبين بجدولة</span><span class="sxs-lookup"><span data-stu-id="71dcf-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="71dcf-173">استخدم صفحة **جداول الاستبيانات** لإعداد رسالة بريد إلكتروني وإرسالها إلى جميع المشاركين الذين تم تعيينهم للاستبيان.</span><span class="sxs-lookup"><span data-stu-id="71dcf-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="71dcf-174">أدخل نص البريد الإلكتروني على علامة تبويب **بريد إلكتروني لخدمة الموظف الذاتية‬‬‏‫**. بعد بدء الجدول، انقر فوق **الوظائف** &gt; **إرسال بريد إلكتروني** لإنشاء البريد الإلكتروني وإرساله للمستجيبين.</span><span class="sxs-lookup"><span data-stu-id="71dcf-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="71dcf-175">ويمكن للمستجيبين فيما بعد تسجيل الدخول إلى موقع الويب وإكمال الاستبيان.‬</span><span class="sxs-lookup"><span data-stu-id="71dcf-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="71dcf-176">**ملاحظة:** قبل استخدام وظيفة البريد الإلكتروني، يجب على مسؤول تكنولوجيا المعلومات إدخال إعدادات البريد الإلكتروني في صفحة **معلمات البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="71dcf-177">إنهاء استبيان مجدول</span><span class="sxs-lookup"><span data-stu-id="71dcf-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="71dcf-178">يمكن إنهاء استبيان مجدول بعد قيام كل المستجيبين بإكمال جلسات الإجابة المخصصة لهم.</span><span class="sxs-lookup"><span data-stu-id="71dcf-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="71dcf-179">وبعد إنهاء استبيان مجدول، لا يمكنك نسخ إعداداته إلى جدول جديد.</span><span class="sxs-lookup"><span data-stu-id="71dcf-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="71dcf-180">**ملاحظة** في حالة عدم إكمال الاستبيان من قبل مستجيب واحد أو أكثر، ولكنك مع ذلك تريد إنهاء الجدولة، فيجب عليك أولاً حذف أولئك المستجيبين من القائمة في صفحة **جلسة الإجابة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="71dcf-181">ويمكنك حينئذٍ إنهاء الجدولة.</span><span class="sxs-lookup"><span data-stu-id="71dcf-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="71dcf-182">استكمال الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="71dcf-182">Completing questionnaires</span></span>
<span data-ttu-id="71dcf-183">بعد قيامك تصميم وتوزيع استبيان، يمكن إكمال الاستبيان بواسطة المستجيبين المحددة.</span><span class="sxs-lookup"><span data-stu-id="71dcf-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="71dcf-184">يمكن إكمال الاستبيانات المتاحة لك من موقعين:</span><span class="sxs-lookup"><span data-stu-id="71dcf-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="71dcf-185">في جزء التنقل، انقر فوق **الاستبيانات‬** &gt; **توزيع** &gt; **‎إكمال استبيان**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="71dcf-186">في الخدمة الذاتية للموظف، انقر فوق **الاستبيانات المراد إكمالها**.</span><span class="sxs-lookup"><span data-stu-id="71dcf-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="71dcf-187">يمكن توفير الاستبيانات لمستخدمين أو مجموعات مستخدمين محددة أو لجميع الموظفين في شبكة.</span><span class="sxs-lookup"><span data-stu-id="71dcf-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="additional-resources"></a><span data-ttu-id="71dcf-188">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="71dcf-188">Additional resources</span></span>
--------

[<span data-ttu-id="71dcf-189">تصميم الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="71dcf-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="71dcf-190">استخدام الاستبيانات</span><span class="sxs-lookup"><span data-stu-id="71dcf-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="71dcf-191">عرض نتائج الاستبيان وتقييمها</span><span class="sxs-lookup"><span data-stu-id="71dcf-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


