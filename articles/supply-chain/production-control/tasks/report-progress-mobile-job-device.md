---
title: الإبلاغ عن مدى تقدم في جهاز وظيفة محمول
description: هذا الإجراء يوضح لك كيفية البدء والإبلاغ عن التقدم المحرز في وظيفة إنتاج في نموذج تسجيل جهاز الوظيفة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm, JmgRegistrationTouchReportProgress, JmgFeedbackWizard, JmgJobBundleProdFeedback
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34067902f05546b5c420feca633f77f16033ed2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421352"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="fba7a-103">الإبلاغ عن مدى تقدم في جهاز وظيفة محمول</span><span class="sxs-lookup"><span data-stu-id="fba7a-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fba7a-104">هذا الإجراء يوضح لك كيفية البدء والإبلاغ عن التقدم المحرز في وظيفة إنتاج في نموذج تسجيل جهاز الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="fba7a-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="fba7a-105">لتتمكن من تشغيل هذا الإجراء يجب أن يكون لديك دور مسؤول النظام أو دور "عامل تشغيل الجهاز" الذي يقترن بحساب المستخدم.</span><span class="sxs-lookup"><span data-stu-id="fba7a-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="fba7a-106">انتقل إلى التحكم بالإنتاج > ‏‫التنفيذ التصنيعي > جهاز بطاقة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="fba7a-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="fba7a-107">في حقل WorkerTextField، أدخل شارة العامل.</span><span class="sxs-lookup"><span data-stu-id="fba7a-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="fba7a-108">في نوع بيانات العرض التوضيحي USMF، اكتب '123' لكريستينا بوترا..</span><span class="sxs-lookup"><span data-stu-id="fba7a-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="fba7a-109">انقر فوق تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="fba7a-109">Click Log in.</span></span>
4. <span data-ttu-id="fba7a-110">انقر فوق زر عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="fba7a-110">Click the Filter button.</span></span>
5. <span data-ttu-id="fba7a-111">حدد مربع الاختيار ‏‫تطبيق عامل تصفية التكوين أو قم بإلغاء تحديده.</span><span class="sxs-lookup"><span data-stu-id="fba7a-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="fba7a-112">إذا قمت بتعيين عامل تصفية، فيمكنك استخدام وحدة إنتاج 110 في USMF.</span><span class="sxs-lookup"><span data-stu-id="fba7a-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="fba7a-113">في حقل وحدة الإنتاج، حدد مجموعة الموارد لوظائف الإنتاج التي يمكن أن يعمل عليها العامل.</span><span class="sxs-lookup"><span data-stu-id="fba7a-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="fba7a-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fba7a-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fba7a-115">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fba7a-115">Click OK.</span></span>
9. <span data-ttu-id="fba7a-116">انقر فوق زر "ابدأ الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="fba7a-116">Click the Start job button.</span></span>
10. <span data-ttu-id="fba7a-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fba7a-117">Click OK.</span></span>
11. <span data-ttu-id="fba7a-118">انقر فوق زر "‏‫الإبلاغ عن مدى التقدم".</span><span class="sxs-lookup"><span data-stu-id="fba7a-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="fba7a-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fba7a-119">Click OK.</span></span>
13. <span data-ttu-id="fba7a-120">انقر فوق زر "الوظيفة التالية".</span><span class="sxs-lookup"><span data-stu-id="fba7a-120">Click the Next job button.</span></span>
14. <span data-ttu-id="fba7a-121">انقر فوق معيّن لإلقاء نظرة عامة على زر كل وظائف الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="fba7a-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="fba7a-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fba7a-122">Close the page.</span></span>
16. <span data-ttu-id="fba7a-123">انقر فوق زر "فاصل".</span><span class="sxs-lookup"><span data-stu-id="fba7a-123">Click the Break button.</span></span>
17. <span data-ttu-id="fba7a-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fba7a-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="fba7a-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fba7a-125">Click OK.</span></span>
19. <span data-ttu-id="fba7a-126">انقر فوق زر "مغادرة".</span><span class="sxs-lookup"><span data-stu-id="fba7a-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="fba7a-127">حدد هذا الخيار لتسجيل الخروج.</span><span class="sxs-lookup"><span data-stu-id="fba7a-127">Select to log out.</span></span>
21. <span data-ttu-id="fba7a-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fba7a-128">Click OK.</span></span>
22. <span data-ttu-id="fba7a-129">تسجيل الدخول مرة أخرى في حقل WorkerTextField.</span><span class="sxs-lookup"><span data-stu-id="fba7a-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="fba7a-130">يمكنك تحديد العامل "123" في بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="fba7a-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="fba7a-131">انقر فوق تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="fba7a-131">Click Log in.</span></span>
24. <span data-ttu-id="fba7a-132">انقر فوق "‏‫إيقاف فترة الراحة‬".</span><span class="sxs-lookup"><span data-stu-id="fba7a-132">Click Stop break.</span></span>
25. <span data-ttu-id="fba7a-133">انقر فوق زر "النشاط".</span><span class="sxs-lookup"><span data-stu-id="fba7a-133">Click the Activity button.</span></span>
26. <span data-ttu-id="fba7a-134">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="fba7a-134">Click Cancel.</span></span>
27. <span data-ttu-id="fba7a-135">انقر فوق زر "مغادرة".</span><span class="sxs-lookup"><span data-stu-id="fba7a-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="fba7a-136">حدد هذا الخيار لتسجيل الانصراف.</span><span class="sxs-lookup"><span data-stu-id="fba7a-136">Select to clock out.</span></span>
29. <span data-ttu-id="fba7a-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fba7a-137">Click OK.</span></span>
30. <span data-ttu-id="fba7a-138">حدد سببا تسجيل الانصراف مبكرًا.</span><span class="sxs-lookup"><span data-stu-id="fba7a-138">Select a reason why you are clocking out early.</span></span>

