--- 
title: "توزيع الاستبيانات باستخدام الجدولة"
description: "تتيح لك جدولة الاستبيان إمكانية تخطيط وتوزيع استبيانات على عدة مستجيبين."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6795c5ed48ef1d716ddec5cca1a2f6414bb318ce
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="389d0-103">توزيع الاستبيانات باستخدام الجدولة</span><span class="sxs-lookup"><span data-stu-id="389d0-103">Distribute questionnaires using scheduling</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="389d0-104">تتيح لك جدولة الاستبيان إمكانية تخطيط وتوزيع استبيانات على عدة مستجيبين.</span><span class="sxs-lookup"><span data-stu-id="389d0-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="389d0-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="389d0-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="389d0-106">إنشاء جدول استبيان</span><span class="sxs-lookup"><span data-stu-id="389d0-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="389d0-107">انتقل إلى الاستبيان > توزيع > جداول الاستبيانات.</span><span class="sxs-lookup"><span data-stu-id="389d0-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="389d0-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="389d0-108">Click New.</span></span>
3. <span data-ttu-id="389d0-109">في حقل الجدولة، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="389d0-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="389d0-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="389d0-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="389d0-111">قم بتعيين الجدولة إلى مجهول إذا كان يجب تسجيل الاستجابات دون أسماء مقترنة بالاستجابة.</span><span class="sxs-lookup"><span data-stu-id="389d0-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="389d0-112">يجب إعداد السماح بالنتائج المجهولة‬ في محددات الموارد البشرية أولاً.</span><span class="sxs-lookup"><span data-stu-id="389d0-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="389d0-113">في حقل النوع، حدد نوع التخطيط.</span><span class="sxs-lookup"><span data-stu-id="389d0-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="389d0-114">في هذا المثال سوف نستخدم النوع "رضا".</span><span class="sxs-lookup"><span data-stu-id="389d0-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="389d0-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="389d0-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="389d0-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="389d0-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="389d0-117">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="389d0-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="389d0-118">قم بتوسيع المقطع "بريد إلكتروني لخدمة الموظف الذاتية‬".</span><span class="sxs-lookup"><span data-stu-id="389d0-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="389d0-119">في الحقل "الموضوع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="389d0-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="389d0-120">على سبيل المثال: الاستبيان المتوفر</span><span class="sxs-lookup"><span data-stu-id="389d0-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="389d0-121">في حقل "النص"، اكتب النص الأساسي لرسالة البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="389d0-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="389d0-122">تجدر الإشارة إلى أنه يمكن استخدام المتغير لكي يحل محل القيم في النظام.</span><span class="sxs-lookup"><span data-stu-id="389d0-122">Note, the variable can be used to substitute values in the system.</span></span>
    * <span data-ttu-id="389d0-123">على سبيل المثال:   عزيزي % P %، الرجاء تسجيل الدخول إلى ‏‫خدمة الموظف الذاتية‬ لإكمال الاستبيان "صحة القوى العاملة".</span><span class="sxs-lookup"><span data-stu-id="389d0-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="389d0-124">شركة الرشيدي</span><span class="sxs-lookup"><span data-stu-id="389d0-124">Contoso</span></span>  
12. <span data-ttu-id="389d0-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="389d0-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="389d0-126">استخدم تفاصيل الإعداد لتحديد الاستبيان (الاستبيانات) الذي تتعين الإجابة عليه بالإضافة إلى أية استعلامات لاستخدامها في تحديد المستجيبين.</span><span class="sxs-lookup"><span data-stu-id="389d0-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="389d0-127">انقر فوق تفاصيل الإعداد.</span><span class="sxs-lookup"><span data-stu-id="389d0-127">Click Setup details.</span></span>
2. <span data-ttu-id="389d0-128">في القائمة، حدد استعلامًا لاستخدامه للبحث في النظام عن المستجيبين للاستبيان.</span><span class="sxs-lookup"><span data-stu-id="389d0-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="389d0-129">مثال: العاملون‬</span><span class="sxs-lookup"><span data-stu-id="389d0-129">Example: Workers</span></span>  
3. <span data-ttu-id="389d0-130">انقر فوق عرض أو تعديل الاستعلام لتحديد أشخاص معينين أو تعديل الاستعلام للبحث عن الأشخاص الذين يتطابقون مع معايير معينة.</span><span class="sxs-lookup"><span data-stu-id="389d0-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="389d0-131">لاحظ أن جميع المستجيبين يجب أن يكونوا مستخدمين في النظام.</span><span class="sxs-lookup"><span data-stu-id="389d0-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="389d0-132">في القائمة، ضع علامة على صف "الشخص".</span><span class="sxs-lookup"><span data-stu-id="389d0-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="389d0-133">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="389d0-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="389d0-134">حدد جوليا فونديربورك</span><span class="sxs-lookup"><span data-stu-id="389d0-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="389d0-135">في القائمة، حدد جوليا فونديربورك‬</span><span class="sxs-lookup"><span data-stu-id="389d0-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="389d0-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="389d0-136">Click OK.</span></span>
8. <span data-ttu-id="389d0-137">انقر فوق علامة التبويب الاستبيانات.</span><span class="sxs-lookup"><span data-stu-id="389d0-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="389d0-138">في الشجرة، قم بتوسيع "عقدة نوع الاستبيان استقصاء‬ الرضا".</span><span class="sxs-lookup"><span data-stu-id="389d0-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="389d0-139">في الشجرة، حدد "تقييم صحة العاملين".</span><span class="sxs-lookup"><span data-stu-id="389d0-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="389d0-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="389d0-140">Click OK.</span></span>
12. <span data-ttu-id="389d0-141">انقر فوق جلسة إجابة مخططة.</span><span class="sxs-lookup"><span data-stu-id="389d0-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="389d0-142">لاحظ أنه تم إنشاء جلسات الإجابة المخططة لكل مستخدم تم تحديده/الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="389d0-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="389d0-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="389d0-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="389d0-144">ابدأ جدولة الاستبيان لتوفير الاستبيان للمستجيبين لإكماله.</span><span class="sxs-lookup"><span data-stu-id="389d0-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="389d0-145">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="389d0-145">Click Functions.</span></span>
2. <span data-ttu-id="389d0-146">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="389d0-146">Click Start.</span></span>
3. <span data-ttu-id="389d0-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="389d0-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="389d0-148">أرسل رسالة بريد إلكتروني لإعلام المستجيبين بالاستبيان المتوفر.</span><span class="sxs-lookup"><span data-stu-id="389d0-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="389d0-149">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="389d0-149">Click Functions.</span></span>
2. <span data-ttu-id="389d0-150">انقر فوق "إرسال بريد الإلكتروني".</span><span class="sxs-lookup"><span data-stu-id="389d0-150">Click Send email.</span></span>
3. <span data-ttu-id="389d0-151">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="389d0-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="389d0-152">استخدم جلسات الإجابة المخططة لمراقبة من يحتاج إلى إكمال الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="389d0-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="389d0-153">انقر فوق جلسة إجابة مخططة.</span><span class="sxs-lookup"><span data-stu-id="389d0-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="389d0-154">احذف أي جلسة إجابة مخططة متبقية عندما تصبح جاهزاً لإنهاء الجلسة المجدولة.</span><span class="sxs-lookup"><span data-stu-id="389d0-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="389d0-155">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="389d0-155">Click Delete.</span></span>
3. <span data-ttu-id="389d0-156">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="389d0-156">Click Yes.</span></span>
4. <span data-ttu-id="389d0-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="389d0-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="389d0-158">قم بإنهاء الجدول عند قيام جميع المستجيبين بإكمال الاستبيان و/أو عند حذف كل جلسات الإجابات المخططة.</span><span class="sxs-lookup"><span data-stu-id="389d0-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="389d0-159">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="389d0-159">Click Functions.</span></span>
2. <span data-ttu-id="389d0-160">انقر فوق "إنهاء".</span><span class="sxs-lookup"><span data-stu-id="389d0-160">Click End.</span></span>
3. <span data-ttu-id="389d0-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="389d0-161">Click OK.</span></span>


