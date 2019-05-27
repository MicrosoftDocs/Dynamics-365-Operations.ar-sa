---
title: إدخال الجداول الزمنية للمشروع‬
description: يمكنك هذا الإجراء من إنشاء جدول زمني باستخدام نموذج جدول زمني فارغ.
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510372"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="46994-103">إدخال الجداول الزمنية للمشروع‬</span><span class="sxs-lookup"><span data-stu-id="46994-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46994-104">يمكنك هذا الإجراء من إنشاء جدول زمني باستخدام نموذج جدول زمني فارغ.</span><span class="sxs-lookup"><span data-stu-id="46994-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="46994-105">ويمكن أن يستند الجدول الزمني الجديد على معلومات من جدول زمني سابق، أو من مشروع وتعيينات أنشطة في صفحة "‏‫المفضلة‬".</span><span class="sxs-lookup"><span data-stu-id="46994-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="46994-106">وبشكل افتراضي، تعرض صفحة قائمة "كل الجداول الزمنية" كل جداولك الزمنية الخاصة بالفترة الحالية.</span><span class="sxs-lookup"><span data-stu-id="46994-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="46994-107">يمكنك استخدام القائمة المنسدلة لحقل "إظهار" في صفحة الجداول الزمنية لتصفية قائمة الجداول الزمنية حسب الفترة الزمنية أو المشروع، أو لعرض الجداول الزمنية التي تم إنشاؤها باسم العمال الآخرين.</span><span class="sxs-lookup"><span data-stu-id="46994-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="46994-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USSI.</span><span class="sxs-lookup"><span data-stu-id="46994-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="46994-109">لبدء هذا الإجراء، انتقل إلى إدارة المشاريع والمحاسبة > الجداول الزمنية > الجداول الزمنية الخاصة بي</span><span class="sxs-lookup"><span data-stu-id="46994-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="46994-110">لإدخال جدول زمني جديد، انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="46994-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="46994-111">تعرض القائمة المنسدلة "الموارد" العامل المعين للمستخدم الحالي، بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="46994-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="46994-112">إذا تم تعيين المستخدم كمفوض، فهذا سيقوم بسرد الأسماء بحيث يمكن للمستخدم إدخال جدول زمني بالنيابة عنه.</span><span class="sxs-lookup"><span data-stu-id="46994-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="46994-113">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="46994-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="46994-114">إذا تم تحديد هذا الخيار، فسيتم إنشاء بنود جدول زمني جديد باستخدام إعدادات الجداول الزمنية التي تم تكوينها كمفضلة.</span><span class="sxs-lookup"><span data-stu-id="46994-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="46994-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="46994-115">Click OK.</span></span>
4. <span data-ttu-id="46994-116">انقر فوق "بند جديد".</span><span class="sxs-lookup"><span data-stu-id="46994-116">Click New line.</span></span>
5. <span data-ttu-id="46994-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="46994-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="46994-118">يعرض حقل "الكيان القانوني" الكيان القانوني الحالي بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="46994-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="46994-119">في حقل "المشروع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="46994-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="46994-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="46994-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="46994-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="46994-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="46994-122">في الحقل "النشاط"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="46994-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="46994-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="46994-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="46994-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="46994-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="46994-125">في حقل "الفئة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="46994-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="46994-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="46994-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="46994-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="46994-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="46994-128">أدخل عدد ساعات العمل كل يوم.</span><span class="sxs-lookup"><span data-stu-id="46994-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="46994-129">يجب إدخال الساعات بتنسيق عشري.</span><span class="sxs-lookup"><span data-stu-id="46994-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="46994-130">على سبيل المثال، إذا قمت بالعمل لمدة ساعتين وخمس عشرة دقيقة، أدخل 2:15.</span><span class="sxs-lookup"><span data-stu-id="46994-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="46994-131">أدخل عدد ساعات العمل كل يوم.</span><span class="sxs-lookup"><span data-stu-id="46994-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="46994-132">يجب إدخال الساعات بتنسيق عشري.</span><span class="sxs-lookup"><span data-stu-id="46994-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="46994-133">على سبيل المثال، إذا قمت بالعمل لمدة ساعتين وخمس عشرة دقيقة، أدخل 2:15.</span><span class="sxs-lookup"><span data-stu-id="46994-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="46994-134">أدخل عدد ساعات العمل كل يوم.</span><span class="sxs-lookup"><span data-stu-id="46994-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="46994-135">يجب إدخال الساعات بتنسيق عشري.</span><span class="sxs-lookup"><span data-stu-id="46994-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="46994-136">على سبيل المثال، إذا قمت بالعمل لمدة ساعتين وخمس عشرة دقيقة، أدخل 2:15.</span><span class="sxs-lookup"><span data-stu-id="46994-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="46994-137">أدخل عدد ساعات العمل كل يوم.</span><span class="sxs-lookup"><span data-stu-id="46994-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="46994-138">يجب إدخال الساعات بتنسيق عشري.</span><span class="sxs-lookup"><span data-stu-id="46994-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="46994-139">على سبيل المثال، إذا قمت بالعمل لمدة ساعتين وخمس عشرة دقيقة، أدخل 2:15.</span><span class="sxs-lookup"><span data-stu-id="46994-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="46994-140">أدخل عدد ساعات العمل كل يوم.</span><span class="sxs-lookup"><span data-stu-id="46994-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="46994-141">يجب إدخال الساعات بتنسيق عشري.</span><span class="sxs-lookup"><span data-stu-id="46994-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="46994-142">على سبيل المثال، إذا قمت بالعمل لمدة ساعتين وخمس عشرة دقيقة، أدخل 2:15.</span><span class="sxs-lookup"><span data-stu-id="46994-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="46994-143">في تفاصيل البنود‬، تتوفر الخيارات التالية:  o  إضافة معلومات حول الأبعاد المالية والضرائب.</span><span class="sxs-lookup"><span data-stu-id="46994-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="46994-144">o    إضافة تعليقات حول بند الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="46994-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="46994-145">انقر فوق "سير العمل" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="46994-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="46994-146">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="46994-146">Click Submit.</span></span>
22. <span data-ttu-id="46994-147">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="46994-147">Click Submit.</span></span>

