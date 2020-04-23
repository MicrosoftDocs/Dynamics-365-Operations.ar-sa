---
title: جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف
description: يركز هذا الموضوع على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a69339bc678de8343dbf2646a4d6fe0ace9964c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210469"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="42841-103">جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف</span><span class="sxs-lookup"><span data-stu-id="42841-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42841-104">يركز هذا الموضوع على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="42841-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="42841-105">لا يتم إنشاء أي وظائف بواسطة جدولة العمليات، بينما يتم إنشاء الوظائف بواسطة جدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="42841-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="42841-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="42841-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="42841-107">تم تخصيص هذا الإجراء لمدير الإنتاج أو مخطط الإنتاج أو المشرف على صالة الإنتاج‬ في بيئة تصنيع منفصلة.</span><span class="sxs-lookup"><span data-stu-id="42841-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="42841-108">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="42841-108">Create a production order</span></span>
1. <span data-ttu-id="42841-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > ‏‫التحكم بالإنتاج‬ > أوامر الإنتاج > جميع أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="42841-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="42841-110">حدد **أمر إنتاج جديد**.</span><span class="sxs-lookup"><span data-stu-id="42841-110">Select **New production order**.</span></span>
3. <span data-ttu-id="42841-111">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42841-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="42841-112">حدد رقم الصنف **D0001**.</span><span class="sxs-lookup"><span data-stu-id="42841-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="42841-113">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="42841-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="42841-114">جدولة العمليات لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="42841-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="42841-115">ضع علامة على الصف الذي تم إنشاؤه حديثًا.</span><span class="sxs-lookup"><span data-stu-id="42841-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="42841-116">في جزء الإجراءات، حدد **جدول**.</span><span class="sxs-lookup"><span data-stu-id="42841-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="42841-117">حدد **جدولة العمليات**.</span><span class="sxs-lookup"><span data-stu-id="42841-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="42841-118">في الحقل **اتجاه الجدولة**، حدد **بدءًا من تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="42841-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="42841-119">أدخل تاريخًا في حقل **تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="42841-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="42841-120">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="42841-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="42841-121">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="42841-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="42841-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="42841-122">Select **OK**.</span></span>
7. <span data-ttu-id="42841-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="42841-123">In the list, mark the selected row.</span></span> <span data-ttu-id="42841-124">لاحظ أن الحالة تغيّرت إلى **مجدول**.</span><span class="sxs-lookup"><span data-stu-id="42841-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="42841-125">حدد **كل الوظائف‬**.</span><span class="sxs-lookup"><span data-stu-id="42841-125">Select **All jobs**.</span></span> <span data-ttu-id="42841-126">لاحظ أنه لم يتم إنشاء أي وظائف بواسطة جدولة العمليات.</span><span class="sxs-lookup"><span data-stu-id="42841-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="42841-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="42841-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="42841-128">جدولة المهام لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="42841-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="42841-129">في جزء الإجراءات، حدد **جدول**.</span><span class="sxs-lookup"><span data-stu-id="42841-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="42841-130">حدد **جدولة الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="42841-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="42841-131">في الحقل **اتجاه الجدولة**، حدد **بدءًا من تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="42841-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="42841-132">أدخل تاريخًا في حقل **تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="42841-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="42841-133">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="42841-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="42841-134">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="42841-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="42841-135">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="42841-135">Select **OK**.</span></span>
6. <span data-ttu-id="42841-136">في جزء الإجراءات، حدد **أمر إنتاج**.</span><span class="sxs-lookup"><span data-stu-id="42841-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="42841-137">حدد **كل الوظائف‬**.</span><span class="sxs-lookup"><span data-stu-id="42841-137">Select **All jobs**.</span></span> <span data-ttu-id="42841-138">لاحظ أنه تم إنشاء 5 وظائف بواسطة جدولة الوظائف على المسار النشط.</span><span class="sxs-lookup"><span data-stu-id="42841-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

