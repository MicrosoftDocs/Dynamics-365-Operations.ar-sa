--- 
title: "جدولة وظائف كانبان"
description: "يركز هذا الإجراء على جدولة وظائف كانبان للمعالجة لخلية عمل معينة."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 692a867eae15ac02f7042c69b9dde4f1fcbd0d54
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="951a0-103">جدولة وظائف كانبان</span><span class="sxs-lookup"><span data-stu-id="951a0-103">Schedule kanban jobs</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="951a0-104">يركز هذا الإجراء على جدولة وظائف كانبان للمعالجة لخلية عمل معينة.</span><span class="sxs-lookup"><span data-stu-id="951a0-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="951a0-105">يُعد الإجراء "إعداد وظيفة كانبان للمعالجة عندما لا تتوفر المواد" شرطًا أساسيًا لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="951a0-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="951a0-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="951a0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="951a0-107">هذه المهمة مخصصة للمشرف على صالة الإنتاج‬ ومخطط الإنتاج‬ اللذين يعملان مع كانبان.</span><span class="sxs-lookup"><span data-stu-id="951a0-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="951a0-108">تحديد وظائف كانبان لخلية عمل</span><span class="sxs-lookup"><span data-stu-id="951a0-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="951a0-109">انتقل إلى التحكم بالإنتاج‬ > كانبان > جدولة وظيفة كانبان‬.</span><span class="sxs-lookup"><span data-stu-id="951a0-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="951a0-110">وسّع مربع الحقائق "قدرة الفترة‬".</span><span class="sxs-lookup"><span data-stu-id="951a0-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="951a0-111">وسّع مربع الحقائق "كانبان".</span><span class="sxs-lookup"><span data-stu-id="951a0-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="951a0-112">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="951a0-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="951a0-113">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="951a0-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="951a0-114">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="951a0-114">Select work cell 1250.</span></span> <span data-ttu-id="951a0-115">سيؤدي ذلك إلى تصفية طريقة العرض لعرض فقط وظائف خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="951a0-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="951a0-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="951a0-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="951a0-117">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="951a0-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="951a0-118">جدولة وظيفة كانبان في الفترة الأولى المتوفرة</span><span class="sxs-lookup"><span data-stu-id="951a0-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="951a0-119">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="951a0-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="951a0-120">حدد الصف الأول في القائمة التي تحتوي على الحالة "غير مخطط‬".</span><span class="sxs-lookup"><span data-stu-id="951a0-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="951a0-121">تشير الأيقونة المنقطة في حقل "حالة الوظيفة" إلى أن الوظيفة غير مخططة.</span><span class="sxs-lookup"><span data-stu-id="951a0-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="951a0-122">انقر فوق "الجدول‬".</span><span class="sxs-lookup"><span data-stu-id="951a0-122">Click Schedule.</span></span>
    * <span data-ttu-id="951a0-123">سيؤدي ذلك إلى جدولة وظيفة كانبان في الفترة الأولى المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="951a0-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="951a0-124">لاحظ نقل وظيفة كانبان إلى نهاية القائمة بسبب إضافتها إلى لفترة التي تبدأ من اليوم.</span><span class="sxs-lookup"><span data-stu-id="951a0-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="951a0-125">إذا كانت الفترة اعتبارًا من اليوم محجوزة بالكامل، سيتم نقل الوظيفة إلى الفترة الأولى المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="951a0-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="951a0-126">جدولة وظيفتي كانبان ليوم معين</span><span class="sxs-lookup"><span data-stu-id="951a0-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="951a0-127">في القائمة، حدد الصف 1.</span><span class="sxs-lookup"><span data-stu-id="951a0-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="951a0-128">سترى أن الصف الأول يحتوي على الحالة "غير مخطط" في الحقل "حالة الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="951a0-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="951a0-129">في القائمة، حدد الصف 2.</span><span class="sxs-lookup"><span data-stu-id="951a0-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="951a0-130">وسترى أن الصف الثاني يحتوي على الحالة "غير مخطط" في الحقل "حالة الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="951a0-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="951a0-131">تم الآن تحديد الوظيفتين الأولى والثانية.</span><span class="sxs-lookup"><span data-stu-id="951a0-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="951a0-132">انقر فوق "جدولة تاريخ البداية‬" لفتح نموذج مربع حوار الإسقاط‬</span><span class="sxs-lookup"><span data-stu-id="951a0-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="951a0-133">حدد المربع "تجاوز الاستجابة للعجز في السعة‬" أو قم بإلغاء تحديده.</span><span class="sxs-lookup"><span data-stu-id="951a0-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="951a0-134">يسمح لك هذا الخيار بتجاوز الاستجابة الافتراضية للعجز في السعة‬.</span><span class="sxs-lookup"><span data-stu-id="951a0-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="951a0-135">في الحقل "الاستجابة للعجز في القدرة الإنتاجية‬"، حدد "إضافة إلى الفترة المطلوبة".</span><span class="sxs-lookup"><span data-stu-id="951a0-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="951a0-136">يضمن هذا الخيار إضافة الوظيفة إلى الفترة المطلوبة، بغض النظر عن إمكانية وجود حمل زائد في خلية العمل.</span><span class="sxs-lookup"><span data-stu-id="951a0-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="951a0-137">انقر فوق "الجدول‬".</span><span class="sxs-lookup"><span data-stu-id="951a0-137">Click Schedule.</span></span>
    * <span data-ttu-id="951a0-138">لاحظ أنه قد تم إضافة الوظيفتين إلى الفترة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="951a0-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="951a0-139">في المقطع "قدرة الفترة‬"، يمكنك مشاهدة حمل العمل لكل فترة.</span><span class="sxs-lookup"><span data-stu-id="951a0-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="951a0-140">يظهر الاستهلاك المجدول في هذه الفترة في الحقل "الاستهلاك".</span><span class="sxs-lookup"><span data-stu-id="951a0-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="951a0-141">إذا كان الاستهلاك المجدول أعلى من القدرة المتاحة في هذه الفترة، فسيتم تحديد الاستهلاك المحمل بشكل زائد.</span><span class="sxs-lookup"><span data-stu-id="951a0-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  


