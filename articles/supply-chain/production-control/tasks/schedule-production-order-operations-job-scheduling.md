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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4932cfa472c34a16249b226aa4a07b8e5f528053
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838477"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="af940-103">جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف</span><span class="sxs-lookup"><span data-stu-id="af940-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af940-104">يركز هذا الإجراء على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="af940-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="af940-105">لا يتم إنشاء أي وظائف بواسطة جدولة العمليات، بينما يتم إنشاء الوظائف بواسطة جدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="af940-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="af940-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="af940-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="af940-107">تم تخصيص هذا الإجراء لمدير الإنتاج أو مخطط الإنتاج أو المشرف على صالة الإنتاج‬ في بيئة تصنيع منفصلة.</span><span class="sxs-lookup"><span data-stu-id="af940-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="af940-108">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="af940-108">Create a production order</span></span>
1. <span data-ttu-id="af940-109">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="af940-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="af940-110">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="af940-110">Click New production order.</span></span>
3. <span data-ttu-id="af940-111">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="af940-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="af940-112">حدد رقم الصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="af940-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="af940-113">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="af940-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="af940-114">جدولة العمليات لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="af940-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="af940-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="af940-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="af940-116">حدد أمر الإنتاج الذي قمت بإنشائه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="af940-116">Select the production order that you have just created.</span></span> <span data-ttu-id="af940-117">يجب أن يكون في أعلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="af940-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="af940-118">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="af940-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="af940-119">انقر فوق "جدولة العمليات".</span><span class="sxs-lookup"><span data-stu-id="af940-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="af940-120">في الحقل "اتجاه الجدولة"، حدد "التقدم من تاريخ الجدولة‬".</span><span class="sxs-lookup"><span data-stu-id="af940-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="af940-121">في حقل "تاريخ الجدولة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="af940-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="af940-122">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="af940-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="af940-123">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="af940-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="af940-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="af940-124">Click OK.</span></span>
7. <span data-ttu-id="af940-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="af940-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="af940-126">لاحظ أن الحالة تغيّرت إلى "مجدولة".</span><span class="sxs-lookup"><span data-stu-id="af940-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="af940-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="af940-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="af940-128">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="af940-128">Click All jobs.</span></span>
    * <span data-ttu-id="af940-129">لاحظ أنه لم يتم إنشاء أي وظائف بواسطة جدولة العمليات.</span><span class="sxs-lookup"><span data-stu-id="af940-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="af940-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="af940-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="af940-131">جدولة المهام لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="af940-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="af940-132">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="af940-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="af940-133">انقر فوق "جدولة الوظائف".</span><span class="sxs-lookup"><span data-stu-id="af940-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="af940-134">في الحقل "اتجاه الجدولة"، حدد "التقدم من تاريخ الجدولة‬".</span><span class="sxs-lookup"><span data-stu-id="af940-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="af940-135">في حقل "تاريخ الجدولة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="af940-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="af940-136">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="af940-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="af940-137">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="af940-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="af940-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="af940-138">Click OK.</span></span>
6. <span data-ttu-id="af940-139">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="af940-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="af940-140">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="af940-140">Click All jobs.</span></span>
    * <span data-ttu-id="af940-141">لاحظ أنه تم إنشاء 5 وظائف بواسطة جدولة الوظائف على المسار النشط.</span><span class="sxs-lookup"><span data-stu-id="af940-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

