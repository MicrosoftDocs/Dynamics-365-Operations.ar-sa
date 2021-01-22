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
ms.openlocfilehash: 55260a4d25f41bc649f5e1f1f8c950c6b438ecfb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144031"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="488d8-103"> تطوير طلبات الموظفين وفتحها </span><span class="sxs-lookup"><span data-stu-id="488d8-103">Develop and open job requisition</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="488d8-104">مشاريع التعيين تساعد في إدارة عملية التعيين.</span><span class="sxs-lookup"><span data-stu-id="488d8-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="488d8-105">لكل مشروع تعيين، يمكنك إعداد معلومات، مثل الوظيفة التي يتم تعيين موظفين لها واسم مسؤول التعيين‬ وحالة المشروع والقسم الذي توجد الوظيفة فيه.</span><span class="sxs-lookup"><span data-stu-id="488d8-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="488d8-106">بعد إنشاء مشروع تعيين، يمكنك كتابة إعلان عن وظيفة للمشروع، ونشر الإعلان على صفحات الخدمة الذاتية للموظف، وربط طلبات التوظيف بالمشروع، وتعقب أنشطة هذا المشروع.</span><span class="sxs-lookup"><span data-stu-id="488d8-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="488d8-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="488d8-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="488d8-108">لبدء الإجراء، انتقل إلى الموارد البشرية > التعيين > مشاريع التعيين > مشاريع التعيين</span><span class="sxs-lookup"><span data-stu-id="488d8-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="488d8-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="488d8-109">Click New.</span></span>
2. <span data-ttu-id="488d8-110">في الحقل "مشروع التعيين"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="488d8-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="488d8-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="488d8-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="488d8-112">في الحقل "مسؤول التعيين"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="488d8-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="488d8-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="488d8-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="488d8-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="488d8-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="488d8-115">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="488d8-115">Click Select.</span></span>
8. <span data-ttu-id="488d8-116">في الحقل "القسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="488d8-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="488d8-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="488d8-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="488d8-118">في الحقل "الوظيفة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="488d8-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="488d8-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="488d8-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="488d8-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="488d8-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="488d8-121">في الحقل "عدد فرص العمل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="488d8-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="488d8-122">في الحقل "مدير التوظيف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="488d8-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="488d8-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="488d8-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="488d8-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="488d8-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="488d8-125">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="488d8-125">Click Select.</span></span>
18. <span data-ttu-id="488d8-126">في الحقل "الموعد النهائي لاستمارات التقديم‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="488d8-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="488d8-127">انقر فوق "الوسائط‬".</span><span class="sxs-lookup"><span data-stu-id="488d8-127">Click Media.</span></span>
    * <span data-ttu-id="488d8-128">تتضمن مشاريع التعيين خيارًا لتحديد المنافذ الإعلامية لاستخدامها للإعلان عن مناصب مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="488d8-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="488d8-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="488d8-129">Click New.</span></span>
21. <span data-ttu-id="488d8-130">في الحقل "الوسائط"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="488d8-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="488d8-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="488d8-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="488d8-132">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="488d8-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="488d8-133">في الحقل "تاريخ الانتهاء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="488d8-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="488d8-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="488d8-134">Click Save.</span></span>
26. <span data-ttu-id="488d8-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="488d8-135">Close the page.</span></span>
27. <span data-ttu-id="488d8-136">انقر فوق "إعلانات الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="488d8-136">Click Job ads.</span></span>
28. <span data-ttu-id="488d8-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="488d8-137">Click Save.</span></span>
29. <span data-ttu-id="488d8-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="488d8-138">Close the page.</span></span>
30. <span data-ttu-id="488d8-139">حدد خانة الاختيار "العرض على خدمة الموظف الذاتية‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="488d8-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="488d8-140">حدد خانة الاختيار "العرض على خدمة الموظف الذاتية‬" لجعل مشروع التعيين مرئيًا للموظفين في صفحات خدمة الموظف الذاتية‬.</span><span class="sxs-lookup"><span data-stu-id="488d8-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="488d8-141">انقر فوق حالة "مشروع التعيين".</span><span class="sxs-lookup"><span data-stu-id="488d8-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="488d8-142">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="488d8-142">Click Start.</span></span>
    * <span data-ttu-id="488d8-143">تعني حالة البدء أن المشروع جاهز لتلقي الطلبات.</span><span class="sxs-lookup"><span data-stu-id="488d8-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="488d8-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="488d8-144">Click OK.</span></span>
