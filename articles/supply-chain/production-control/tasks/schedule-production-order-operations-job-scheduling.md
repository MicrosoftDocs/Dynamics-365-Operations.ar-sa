---
title: جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف
description: يركز هذا الإجراء على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2019
ms.locfileid: "352449"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="0e28f-103">جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف</span><span class="sxs-lookup"><span data-stu-id="0e28f-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e28f-104">يركز هذا الإجراء على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="0e28f-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="0e28f-105">لا يتم إنشاء أي وظائف بواسطة جدولة العمليات، بينما يتم إنشاء الوظائف بواسطة جدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="0e28f-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="0e28f-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="0e28f-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="0e28f-107">تم تخصيص هذا الإجراء لمدير الإنتاج أو مخطط الإنتاج أو المشرف على صالة الإنتاج‬ في بيئة تصنيع منفصلة.</span><span class="sxs-lookup"><span data-stu-id="0e28f-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="0e28f-108">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="0e28f-108">Create a production order</span></span>
1. <span data-ttu-id="0e28f-109">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="0e28f-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="0e28f-110">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="0e28f-110">Click New production order.</span></span>
3. <span data-ttu-id="0e28f-111">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0e28f-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="0e28f-112">حدد رقم الصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="0e28f-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="0e28f-113">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="0e28f-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="0e28f-114">جدولة العمليات لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="0e28f-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="0e28f-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e28f-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0e28f-116">حدد أمر الإنتاج الذي قمت بإنشائه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="0e28f-116">Select the production order that you have just created.</span></span> <span data-ttu-id="0e28f-117">يجب أن يكون في أعلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="0e28f-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="0e28f-118">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="0e28f-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="0e28f-119">انقر فوق "جدولة العمليات".</span><span class="sxs-lookup"><span data-stu-id="0e28f-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="0e28f-120">في الحقل "اتجاه الجدولة"، حدد "التقدم من تاريخ الجدولة‬".</span><span class="sxs-lookup"><span data-stu-id="0e28f-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="0e28f-121">في حقل "تاريخ الجدولة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0e28f-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="0e28f-122">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="0e28f-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="0e28f-123">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="0e28f-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="0e28f-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0e28f-124">Click OK.</span></span>
7. <span data-ttu-id="0e28f-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e28f-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0e28f-126">لاحظ أن الحالة تغيّرت إلى "مجدولة".</span><span class="sxs-lookup"><span data-stu-id="0e28f-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="0e28f-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e28f-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0e28f-128">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="0e28f-128">Click All jobs.</span></span>
    * <span data-ttu-id="0e28f-129">لاحظ أنه لم يتم إنشاء أي وظائف بواسطة جدولة العمليات.</span><span class="sxs-lookup"><span data-stu-id="0e28f-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="0e28f-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0e28f-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="0e28f-131">جدولة المهام لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="0e28f-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="0e28f-132">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="0e28f-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="0e28f-133">انقر فوق "جدولة الوظائف".</span><span class="sxs-lookup"><span data-stu-id="0e28f-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="0e28f-134">في الحقل "اتجاه الجدولة"، حدد "التقدم من تاريخ الجدولة‬".</span><span class="sxs-lookup"><span data-stu-id="0e28f-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="0e28f-135">في حقل "تاريخ الجدولة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0e28f-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="0e28f-136">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="0e28f-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="0e28f-137">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="0e28f-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="0e28f-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0e28f-138">Click OK.</span></span>
6. <span data-ttu-id="0e28f-139">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="0e28f-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="0e28f-140">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="0e28f-140">Click All jobs.</span></span>
    * <span data-ttu-id="0e28f-141">لاحظ أنه تم إنشاء 5 وظائف بواسطة جدولة الوظائف على المسار النشط.</span><span class="sxs-lookup"><span data-stu-id="0e28f-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

