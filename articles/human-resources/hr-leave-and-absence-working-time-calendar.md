---
title: إنشاء تقويم مواعيد العمل
description: تحديد تقويم وقت العمل وأيام العطل وأوقات عدم العمل في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bedbe65f146c4159c2a809de8f683815fd4a01f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417090"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="721ed-103">إنشاء تقويم مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="721ed-103">Create a working time calendar</span></span>

<span data-ttu-id="721ed-104">يعرض تقويم مواعيد العمل في Dynamics 365 Human Resources الأيام والساعات التي يعمل بها الموظفون في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="721ed-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="721ed-105">عندما يقوم أحد الموظفين بإرسال طلب المهلة، فليس من الضروري القلق بالعطلات والإغلاق.</span><span class="sxs-lookup"><span data-stu-id="721ed-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="721ed-106">لتبسيط طلبات المهلة، قم بتكوين هذه العناصر للمؤسسة الخاصة بك:</span><span class="sxs-lookup"><span data-stu-id="721ed-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="721ed-107">تقويم خاص بمواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="721ed-107">Working time calendar</span></span>
- <span data-ttu-id="721ed-108">العطلات والإغلاق</span><span class="sxs-lookup"><span data-stu-id="721ed-108">Holidays and closures</span></span>
- <span data-ttu-id="721ed-109">وقت غير العمل</span><span class="sxs-lookup"><span data-stu-id="721ed-109">Non-work time</span></span>

<span data-ttu-id="721ed-110">يمكنك أضافه آخر صنفين مع إعداد تقويم زمني للعمل.</span><span class="sxs-lookup"><span data-stu-id="721ed-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="721ed-111">ويمكنك أيضا تكوينها أو تحديثها بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="721ed-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="721ed-112">إعداد تقويم وقت العمل</span><span class="sxs-lookup"><span data-stu-id="721ed-112">Set up a working time calendar</span></span>

<span data-ttu-id="721ed-113">قم بإعداد تقويم وقت عمل واحد علي الأقل يوضح أيام العمل وساعتاته.</span><span class="sxs-lookup"><span data-stu-id="721ed-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="721ed-114">إذا كانت لديك مواقع في العديد من البلدان والمناطق، فقد ترغب في إعداد تقويم زمني للعمل لكل منطقه.</span><span class="sxs-lookup"><span data-stu-id="721ed-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="721ed-115">على صفحة **"إدارة المؤسسة"**، حدد **التقويمات**.</span><span class="sxs-lookup"><span data-stu-id="721ed-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="721ed-116">حدد **جديد**، وأدخل اسمًا ووصفًا لتقويمك.</span><span class="sxs-lookup"><span data-stu-id="721ed-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="721ed-117">ضمن **خيارات الإنشاء**، حدد أيام العمل للمؤسسة وادخل أوقات العمل.</span><span class="sxs-lookup"><span data-stu-id="721ed-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="721ed-118">لأضافه عطله أو إغلاق، حدد الزر **إضافة** بجوار **العطلات والإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="721ed-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="721ed-119">لأضافه وقت غير العمل، مثل مواعيد الغداء أو الفواصل الزمنية، حدد **إضافة** ضمن **وقت غير العمل** وادخل الاسم ونطاق الوقت.</span><span class="sxs-lookup"><span data-stu-id="721ed-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="721ed-120">ضمن علامة التبويب **الأيام**، حدد **إنشاء** لإنشاء الأيام في التقويم الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="721ed-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="721ed-121">ادخل نطاق التاريخ للتقويم الخاص بك ثم حدد **إنشاء أيام**.</span><span class="sxs-lookup"><span data-stu-id="721ed-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="721ed-122">لأضافه جداول عمل، ضمن **جدول العمل**، حدد **إضافة**، ثم ادخل الأوقات لكل جدول من جداول العمل.</span><span class="sxs-lookup"><span data-stu-id="721ed-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="721ed-123">تكوين العطلات والإغلاق</span><span class="sxs-lookup"><span data-stu-id="721ed-123">Configure holidays and closures</span></span>

<span data-ttu-id="721ed-124">ويمكنك أضافه أيام العطل أو تغييرها وإغلاقها بشكل منفصل من تقويم وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="721ed-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="721ed-125">على صفحة **"إدارة المؤسسة"**، حدد **العطلات والإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="721ed-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="721ed-126">حدد **جديد**، وأدخل اسمًا وتاريخًا للعطلة أو الإغلاق.</span><span class="sxs-lookup"><span data-stu-id="721ed-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="721ed-127">تكوين وقت غير العمل</span><span class="sxs-lookup"><span data-stu-id="721ed-127">Configure non-work time</span></span>

<span data-ttu-id="721ed-128">يمكنك أضافه أوقات غير العمل أو تغييرها وإغلاقها بشكل منفصل من تقويم وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="721ed-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="721ed-129">على صفحة **"إدارة المؤسسة"**، حدد **وقت غير العمل**.</span><span class="sxs-lookup"><span data-stu-id="721ed-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="721ed-130">حدد **جديد**، وأدخل اسمًا ونطاق الوقت لوقت غير العمل.</span><span class="sxs-lookup"><span data-stu-id="721ed-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="721ed-131">إذا قمت بتمكين ميزه معاينه تصحيحات أيام الإجازات والإجازات البنكية للغياب، تستخدم Human Resources تواريخ العطل والإغلاق لتحديد عدد الأيام التي يجب تعديلها للموظفين المسجلين في التقويم.</span><span class="sxs-lookup"><span data-stu-id="721ed-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="721ed-132">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="721ed-132">See also</span></span>

- [<span data-ttu-id="721ed-133">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="721ed-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="721ed-134">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="721ed-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
