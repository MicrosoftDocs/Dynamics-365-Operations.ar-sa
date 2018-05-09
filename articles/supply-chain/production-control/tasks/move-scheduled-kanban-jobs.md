--- 
title: "نقل وظائف كانبان المجدولة"
description: "يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ae6ea66f0e0ce03008882e59140ad7a0d89f0e30
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="cbeda-103">نقل وظائف كانبان المجدولة</span><span class="sxs-lookup"><span data-stu-id="cbeda-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbeda-104">يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى.</span><span class="sxs-lookup"><span data-stu-id="cbeda-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="cbeda-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cbeda-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cbeda-106">هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬ الذي يعمل مع كانبان.</span><span class="sxs-lookup"><span data-stu-id="cbeda-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="cbeda-107">حدد "وظائف كانبان المجدولة".</span><span class="sxs-lookup"><span data-stu-id="cbeda-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="cbeda-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="cbeda-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="cbeda-109">!MtCMR!في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cbeda-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="cbeda-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="cbeda-110">áçêìõý !</span></span>
3. <span data-ttu-id="cbeda-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cbeda-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="cbeda-112">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="cbeda-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="cbeda-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="cbeda-113">Klik på Select.</span></span>
5. <span data-ttu-id="cbeda-114">Vælg 'Planlagt' i feltet عرض حالة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="cbeda-115">يؤدي ذلك إلى تصفية قائمة الوظائف‬ لعرض وظائف كانبان المجدولة فقط.</span><span class="sxs-lookup"><span data-stu-id="cbeda-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="cbeda-116">نقل وظائف كانبان إلى فترة أخرى</span><span class="sxs-lookup"><span data-stu-id="cbeda-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="cbeda-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cbeda-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="cbeda-118">حدد وظيفة حالتها "مخطط‬"، على سبيل المثال، وظيفة مجدولة في 20 كانون الأول/ديسمبر 2012 في الحقل "الفترة المخططة".</span><span class="sxs-lookup"><span data-stu-id="cbeda-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="cbeda-119">ثم انقل الوظيفة إلى الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="cbeda-120">Klik på الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="cbeda-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="cbeda-121">Klik på End.</span></span>
    * <span data-ttu-id="cbeda-122">سيؤدي ذلك إلى نقل الوظيفة إلى نهاية قائمة الوظائف كالوظيفة الأخيرة في الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="cbeda-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cbeda-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="cbeda-124">حدد وظيفة حالتها "مخطط‬"، على سبيل المثال، وظيفة مجدولة في 18 كانون الأول/ديسمبر 2012 في الحقل "الفترة المخططة".</span><span class="sxs-lookup"><span data-stu-id="cbeda-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="cbeda-125">ثم انقل الوظيفة إلى الفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="cbeda-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="cbeda-126">Klik på الفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="cbeda-126">Klik på Next period.</span></span>
6. <span data-ttu-id="cbeda-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="cbeda-127">Klik på Start.</span></span>
    * <span data-ttu-id="cbeda-128">سيؤدي ذلك إلى نقل الوظيفة إلى بداية قائمة الوظائف كالوظيفة الأولى في الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="cbeda-129">المهمة: نقل وظيفة ضمن فترة</span><span class="sxs-lookup"><span data-stu-id="cbeda-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="cbeda-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cbeda-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="cbeda-131">حدد وظيفة حالتها "مخطط‬"، على سبيل المثال، الوظيفة الثانية المجدولة في 19 كانون الأول/ديسمبر 2012 في الحقل "الفترة المخططة".</span><span class="sxs-lookup"><span data-stu-id="cbeda-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="cbeda-132">ثم انقل الوظيفة ضمن الفترة المخططة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="cbeda-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="cbeda-133">Klik på Forward.</span></span>
    * <span data-ttu-id="cbeda-134">لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأسفل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="cbeda-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="cbeda-135">Klik på Backward.</span></span>
    * <span data-ttu-id="cbeda-136">لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأعلى في القائمة.</span><span class="sxs-lookup"><span data-stu-id="cbeda-136">Notice that the job is moved one line up on the list.</span></span>  


