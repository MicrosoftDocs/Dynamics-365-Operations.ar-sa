---
title: جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف
description: يركز هذا الموضوع على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 3023d6a6fe09c84b47839a2c4b78c37907754ded
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914874"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="5c885-103">جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف</span><span class="sxs-lookup"><span data-stu-id="5c885-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c885-104">يركز هذا الموضوع على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="5c885-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="5c885-105">لا يتم إنشاء أي وظائف بواسطة جدولة العمليات، بينما يتم إنشاء الوظائف بواسطة جدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="5c885-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="5c885-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="5c885-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="5c885-107">تم تخصيص هذا الإجراء لمدير الإنتاج أو مخطط الإنتاج أو المشرف على صالة الإنتاج‬ في بيئة تصنيع منفصلة.</span><span class="sxs-lookup"><span data-stu-id="5c885-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="5c885-108">إنشاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="5c885-108">Create a production order</span></span>
1. <span data-ttu-id="5c885-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > ‏‫التحكم بالإنتاج‬ > أوامر الإنتاج > جميع أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="5c885-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="5c885-110">حدد **أمر إنتاج جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c885-110">Select **New production order**.</span></span>
3. <span data-ttu-id="5c885-111">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5c885-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="5c885-112">حدد رقم الصنف **D0001**.</span><span class="sxs-lookup"><span data-stu-id="5c885-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="5c885-113">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="5c885-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="5c885-114">جدولة العمليات لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="5c885-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="5c885-115">ضع علامة على الصف الذي تم إنشاؤه حديثًا.</span><span class="sxs-lookup"><span data-stu-id="5c885-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="5c885-116">في جزء الإجراءات، حدد **جدول**.</span><span class="sxs-lookup"><span data-stu-id="5c885-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="5c885-117">حدد **جدولة العمليات**.</span><span class="sxs-lookup"><span data-stu-id="5c885-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="5c885-118">في الحقل **اتجاه الجدولة**، حدد **بدءًا من تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="5c885-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="5c885-119">أدخل تاريخًا في حقل **تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="5c885-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="5c885-120">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="5c885-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="5c885-121">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="5c885-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="5c885-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c885-122">Select **OK**.</span></span>
7. <span data-ttu-id="5c885-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5c885-123">In the list, mark the selected row.</span></span> <span data-ttu-id="5c885-124">لاحظ أن الحالة تغيّرت إلى **مجدول**.</span><span class="sxs-lookup"><span data-stu-id="5c885-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="5c885-125">حدد **كل الوظائف‬**.</span><span class="sxs-lookup"><span data-stu-id="5c885-125">Select **All jobs**.</span></span> <span data-ttu-id="5c885-126">لاحظ أنه لم يتم إنشاء أي وظائف بواسطة جدولة العمليات.</span><span class="sxs-lookup"><span data-stu-id="5c885-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="5c885-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5c885-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="5c885-128">جدولة المهام لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="5c885-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="5c885-129">في جزء الإجراءات، حدد **جدول**.</span><span class="sxs-lookup"><span data-stu-id="5c885-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="5c885-130">حدد **جدولة الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="5c885-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="5c885-131">في الحقل **اتجاه الجدولة**، حدد **بدءًا من تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="5c885-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="5c885-132">أدخل تاريخًا في حقل **تاريخ الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="5c885-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="5c885-133">حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="5c885-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="5c885-134">مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="5c885-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="5c885-135">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c885-135">Select **OK**.</span></span>
6. <span data-ttu-id="5c885-136">في جزء الإجراءات، حدد **أمر إنتاج**.</span><span class="sxs-lookup"><span data-stu-id="5c885-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="5c885-137">حدد **كل الوظائف‬**.</span><span class="sxs-lookup"><span data-stu-id="5c885-137">Select **All jobs**.</span></span> <span data-ttu-id="5c885-138">لاحظ أنه تم إنشاء 5 وظائف بواسطة جدولة الوظائف على المسار النشط.</span><span class="sxs-lookup"><span data-stu-id="5c885-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

