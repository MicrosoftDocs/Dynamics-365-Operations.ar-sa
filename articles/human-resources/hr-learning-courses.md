---
title: إعداد الدورات التدريبية
description: يمكن لمسؤولي ومديري الموارد البشرية استخدام ميزات الدورات التدريبية للاحتفاظ بمعلومات حول التدريب التي تم تقديمها للعمال.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 253f0d07679b6327a0ed1e3cc20ede66249750b8
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429326"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="b6e24-103">إعداد الدورات التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-103">Set up training courses</span></span>

<span data-ttu-id="b6e24-104">يمكن لمسؤولي ومديري الموارد البشرية استخدام ميزات الدورات التدريبية للاحتفاظ بمعلومات حول التدريب التي تم تقديمها للعمال.</span><span class="sxs-lookup"><span data-stu-id="b6e24-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="b6e24-105"> متطلبات الإعداد الأساسية</span><span class="sxs-lookup"><span data-stu-id="b6e24-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="b6e24-106">المعلومات التالية يلزم ويجب إعدادها قبل إنشاء دورات تدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="b6e24-107">**أنواع الدورات التدريبية**</span><span class="sxs-lookup"><span data-stu-id="b6e24-107">**Course types**</span></span>

<span data-ttu-id="b6e24-108">المعلومات التالية هي معلومات اختيارية يمكنك تحديدها للدورات التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="b6e24-109">إذا كنت تعرف أنك ستُدخل هذه المعلومات للدورات التدريبية، فيجب إعداد هذه المعلومات قبل إنشاء سجلات الدورات التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="b6e24-110">**مجموعات الفصول الدراسية**</span><span class="sxs-lookup"><span data-stu-id="b6e24-110">**Classroom groups**</span></span>
-   <span data-ttu-id="b6e24-111">**مجموعات الدورة التدريبية**</span><span class="sxs-lookup"><span data-stu-id="b6e24-111">**Course groups**</span></span>
-   <span data-ttu-id="b6e24-112">**مواقع الدورة التدريبية**</span><span class="sxs-lookup"><span data-stu-id="b6e24-112">**Course locations**</span></span>
-   <span data-ttu-id="b6e24-113">**الفصول الدراسية**</span><span class="sxs-lookup"><span data-stu-id="b6e24-113">**Classrooms**</span></span>
-   <span data-ttu-id="b6e24-114">**المعلمون**</span><span class="sxs-lookup"><span data-stu-id="b6e24-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="b6e24-115">أنواع الدورات التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-115">Course types</span></span>
<span data-ttu-id="b6e24-116">يمكنك استخدام أنواع الدورات التدريبية لتصنيفها وفقًا لبنية الدورة التدريبية أو محتواها.</span><span class="sxs-lookup"><span data-stu-id="b6e24-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="b6e24-117">يمكنك إنشاء أنواع الدورات التدريبية في صفحة **أنواع الدورات التدريبية**.</span><span class="sxs-lookup"><span data-stu-id="b6e24-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="b6e24-118">يجب تحديد نوع الدورة التدريبية عند إنشاء سجل دورات تدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="b6e24-119">نوع إعداد الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-119">Course setup type</span></span>
<span data-ttu-id="b6e24-120">يسرد الجدول التالي ثلاثة أنواع لإعدادات الدورات التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="b6e24-121">تحدد أنواع الإعداد بنية الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b6e24-122">نوع الإعداد</span><span class="sxs-lookup"><span data-stu-id="b6e24-122">Setup type</span></span></th>
<th><span data-ttu-id="b6e24-123">الوصف</span><span class="sxs-lookup"><span data-stu-id="b6e24-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6e24-124"><strong>قياسي</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="b6e24-125">حدد هذا النوع للدورات التدريبية التي لن يكون لها جدول أعمال يومي.</span><span class="sxs-lookup"><span data-stu-id="b6e24-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="b6e24-126">هذا هو نوع الإعداد الافتراضي عند إنشاء دورة تدريبية جديدة.</span><span class="sxs-lookup"><span data-stu-id="b6e24-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6e24-127"><strong>جدول الأعمال</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="b6e24-128">حدد هذا النوع لتخطيط تفاصيل كل يوم من الدورة التدريبية التي تجري على مدى عدة أيام.</span><span class="sxs-lookup"><span data-stu-id="b6e24-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6e24-129"><strong>جدول الأعمال + الجلسة</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="b6e24-130">حدد هذا النوع للدورات التدريبية الأكثر تعقيدًا.</span><span class="sxs-lookup"><span data-stu-id="b6e24-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="b6e24-131">على سبيل المثال، يمكنك تقسيم جدول الأعمال للدورة التدريبية إلى مسارات وجلسات عمل.</span><span class="sxs-lookup"><span data-stu-id="b6e24-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="b6e24-132"><strong>المسار</strong> – المسارات هي مجالات الموضوعات المحددة للدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="b6e24-133"><strong>الجلسات</strong> – تقوم جلسات العمل بتقسيم المسارات، وتساعد في تغطية عمليات أو تقنيات خاصة ذات صلة بكل مسار.</span><span class="sxs-lookup"><span data-stu-id="b6e24-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="b6e24-134">مهام الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-134">Course tasks</span></span>
<span data-ttu-id="b6e24-135">يمكنك أيضًا إكمال المهام التالية لكل دورة تدريبية:</span><span class="sxs-lookup"><span data-stu-id="b6e24-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="b6e24-136">تسجيل المشاركين</span><span class="sxs-lookup"><span data-stu-id="b6e24-136">Register participants</span></span>
- <span data-ttu-id="b6e24-137">تحديد آخر موعد للتسجيل</span><span class="sxs-lookup"><span data-stu-id="b6e24-137">Specify a registration deadline</span></span>
- <span data-ttu-id="b6e24-138">تعريف الحد الأدنى والحد الأقصى لعدد المشاركين</span><span class="sxs-lookup"><span data-stu-id="b6e24-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="b6e24-139">قم بتعيين موقع الدورة التدريبية والحجرة الدراسية</span><span class="sxs-lookup"><span data-stu-id="b6e24-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="b6e24-140">قم بتوصية الفنادق للمشاركين في الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="b6e24-141">إنشاء وصف للدورة التدريبية، حيث يمكنك الإعلان عنه على الخدمة الذاتية للموظف</span><span class="sxs-lookup"><span data-stu-id="b6e24-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="b6e24-142">**ملاحظة** يمكنك حذف دورة تدريبية فقط إذا لم يقم أي شخص بالتسجيل لها.</span><span class="sxs-lookup"><span data-stu-id="b6e24-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="b6e24-143">حالات الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-143">Course statuses</span></span>
<span data-ttu-id="b6e24-144">يسرد الجدول التالي حالات الدورة التدريبية المحتملة والإجراءات التي يمكنك إكمالها عندما يتم تحديد حالة معينة للدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b6e24-145">الحالة</span><span class="sxs-lookup"><span data-stu-id="b6e24-145">Status</span></span></th>
<th><span data-ttu-id="b6e24-146">إجراءات</span><span class="sxs-lookup"><span data-stu-id="b6e24-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6e24-147"><strong>تم إنشاؤه</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6e24-148">أدخل معلومات الدورة التدريبية وقم بتعديلها.</span><span class="sxs-lookup"><span data-stu-id="b6e24-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="b6e24-149">قم بتغيير حالة الدورة التدريبية إلى <strong>مفتوحة</strong> حتى يتمكن العاملين من التسجيل في الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6e24-150"><strong>فتح</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6e24-151">قم بتسجيل المشاركين في الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="b6e24-152">قم بإزالة المشاركين من الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="b6e24-153">قم بتأكيد المشاركين في الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="b6e24-154">قم بتغيير حالة الدورة التدريبية إلى<strong> مغلقة</strong> أو <strong>ملغاة</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6e24-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="b6e24-155">وضع خطة للاستبيانات الخاصة بالمشاركين الذين تم تعيين الحالة الخاصة بهم إلى الحالة <strong>مؤكدة</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6e24-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6e24-156"><strong>‏‏مغلق</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="b6e24-157">يمكنك إعادة فتح الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6e24-158"><strong>ملغى</strong></span><span class="sxs-lookup"><span data-stu-id="b6e24-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="b6e24-159">يمكنك إعادة فتح الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="b6e24-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="b6e24-160">المشاركون في الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="b6e24-160">Course participants</span></span>
<span data-ttu-id="b6e24-161">المشاركون في الدورة التدريبية هم العاملون المشاركون في دورة تدريبية أو حدث.</span><span class="sxs-lookup"><span data-stu-id="b6e24-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="b6e24-162">يمكنك فقط تسجيل المشاركين في الدورات التدريبية المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="b6e24-162">You can only register participants for open courses.</span></span> <span data-ttu-id="b6e24-163">يتم تحديد الحد الأقصى والأدنى لعدد المشاركين الذين يمكن تسجيلهم في دورة تدريبية في علامة التبويب **عام** في صفحة **الدورات التدربيبة**.</span><span class="sxs-lookup"><span data-stu-id="b6e24-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="b6e24-164">سير العمل</span><span class="sxs-lookup"><span data-stu-id="b6e24-164">Workflow</span></span>
--------

<span data-ttu-id="b6e24-165">‏‫يمكن للموظفين الذين يقومون بالتسجيل لدورة تدريبية من خلال صفحة **الخدمة الذاتية للموظف** توجيه تسجيلاتهم عن طريق سير العمل للموافقة.</span><span class="sxs-lookup"><span data-stu-id="b6e24-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="b6e24-166">يمكنك تعيين سير عمل إلى دورة تدريبية في علامة التبويب السريعة **عام** في صفحة **الدورات التدريبية‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="b6e24-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





