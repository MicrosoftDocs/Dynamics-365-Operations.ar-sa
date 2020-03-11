---
title: " تطوير طلبات الموظفين وفتحها "
description: مشاريع التعيين تساعد في إدارة عملية التعيين.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88be0205e04bf66833621049c2daf03bca4d9ed0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007995"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="6b0b0-103"> تطوير طلبات الموظفين وفتحها </span><span class="sxs-lookup"><span data-stu-id="6b0b0-103">Develop and open job requisition</span></span>



<span data-ttu-id="6b0b0-104">مشاريع التعيين تساعد في إدارة عملية التعيين.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="6b0b0-105">لكل مشروع تعيين، يمكنك إعداد معلومات، مثل الوظيفة التي يتم تعيين موظفين لها واسم مسؤول التعيين‬ وحالة المشروع والقسم الذي توجد الوظيفة فيه.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="6b0b0-106">بعد إنشاء مشروع تعيين، يمكنك كتابة إعلان عن وظيفة للمشروع، ونشر الإعلان على صفحات الخدمة الذاتية للموظف، وربط طلبات التوظيف بالمشروع، وتعقب أنشطة هذا المشروع.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="6b0b0-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6b0b0-108">لبدء الإجراء، انتقل إلى الموارد البشرية > التعيين > مشاريع التعيين > مشاريع التعيين</span><span class="sxs-lookup"><span data-stu-id="6b0b0-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="6b0b0-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-109">Click New.</span></span>
2. <span data-ttu-id="6b0b0-110">في الحقل "مشروع التعيين"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="6b0b0-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="6b0b0-112">في الحقل "مسؤول التعيين"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6b0b0-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="6b0b0-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6b0b0-115">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-115">Click Select.</span></span>
8. <span data-ttu-id="6b0b0-116">في الحقل "القسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6b0b0-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6b0b0-118">في الحقل "الوظيفة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6b0b0-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6b0b0-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6b0b0-121">في الحقل "عدد فرص العمل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="6b0b0-122">في الحقل "مدير التوظيف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="6b0b0-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="6b0b0-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="6b0b0-125">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-125">Click Select.</span></span>
18. <span data-ttu-id="6b0b0-126">في الحقل "الموعد النهائي لاستمارات التقديم‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="6b0b0-127">انقر فوق "الوسائط‬".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-127">Click Media.</span></span>
    * <span data-ttu-id="6b0b0-128">تتضمن مشاريع التعيين خيارًا لتحديد المنافذ الإعلامية لاستخدامها للإعلان عن مناصب مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="6b0b0-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-129">Click New.</span></span>
21. <span data-ttu-id="6b0b0-130">في الحقل "الوسائط"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="6b0b0-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="6b0b0-132">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="6b0b0-133">في الحقل "تاريخ الانتهاء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="6b0b0-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-134">Click Save.</span></span>
26. <span data-ttu-id="6b0b0-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-135">Close the page.</span></span>
27. <span data-ttu-id="6b0b0-136">انقر فوق "إعلانات الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-136">Click Job ads.</span></span>
28. <span data-ttu-id="6b0b0-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-137">Click Save.</span></span>
29. <span data-ttu-id="6b0b0-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-138">Close the page.</span></span>
30. <span data-ttu-id="6b0b0-139">حدد خانة الاختيار "العرض على خدمة الموظف الذاتية‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="6b0b0-140">حدد خانة الاختيار "العرض على خدمة الموظف الذاتية‬" لجعل مشروع التعيين مرئيًا للموظفين في صفحات خدمة الموظف الذاتية‬.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="6b0b0-141">انقر فوق حالة "مشروع التعيين".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="6b0b0-142">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-142">Click Start.</span></span>
    * <span data-ttu-id="6b0b0-143">تعني حالة البدء أن المشروع جاهز لتلقي الطلبات.</span><span class="sxs-lookup"><span data-stu-id="6b0b0-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="6b0b0-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6b0b0-144">Click OK.</span></span>
