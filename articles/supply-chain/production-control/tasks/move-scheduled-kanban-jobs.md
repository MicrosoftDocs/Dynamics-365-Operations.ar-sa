---
title: نقل وظائف كانبان المجدولة
description: يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2769a7d519e12613796025b658db0b08cdfc4fde
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961630"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="7d3af-103">نقل وظائف كانبان المجدولة</span><span class="sxs-lookup"><span data-stu-id="7d3af-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d3af-104">يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى.</span><span class="sxs-lookup"><span data-stu-id="7d3af-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="7d3af-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="7d3af-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7d3af-106">هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬ الذي يعمل مع كانبان.</span><span class="sxs-lookup"><span data-stu-id="7d3af-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="7d3af-107">حدد وظائف كانبان المُجدولة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="7d3af-108">انتقل إلى **التحكم بالإنتاج > كانبان > جدولة وظيفة كانبان**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="7d3af-109">في حقل **خلية العمل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7d3af-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="7d3af-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7d3af-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="7d3af-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="7d3af-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="7d3af-112">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-112">Click **Select**.</span></span> 

5. <span data-ttu-id="7d3af-113">في حقل **عرض حالة الوظيفة**، حدد **تمت الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="7d3af-114">يؤدي ذلك إلى تصفية قائمة الوظائف‬ لعرض وظائف كانبان المجدولة فقط.</span><span class="sxs-lookup"><span data-stu-id="7d3af-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="7d3af-115">نقل وظائف كانبان إلى فترة أخرى.</span><span class="sxs-lookup"><span data-stu-id="7d3af-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="7d3af-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7d3af-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="7d3af-117">حدد وظيفة حالتها **مهمة مخططة**، على سبيل المثال، وظيفة مجدولة في 20 ديسمبر 2012 في حقل **الفترة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="7d3af-118">ثم انقل الوظيفة إلى الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="7d3af-119">انقر فوق **الفترة السابقة**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="7d3af-120">انقر **الإنهاء** لنقل الوظيفة إلى نهاية قائمة الوظائف كالوظيفة الأخيرة في الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="7d3af-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7d3af-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="7d3af-122">حدد وظيفة حالتها **مهمة مخططة**، على سبيل المثال، وظيفة مجدولة في 18 ديسمبر 2012 في حقل **الفترة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="7d3af-123">ثم انقل الوظيفة إلى الفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="7d3af-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="7d3af-124">انقر فوق **الفترة التالية**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="7d3af-125">انقر **البدء** لنقل الوظيفة إلى بداية قائمة الوظائف كالوظيفة الأولى في الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="7d3af-126">نقل وظيفة ضمن فترة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="7d3af-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7d3af-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="7d3af-128">حدد وظيفة حالتها مهمة مخططة، على سبيل المثال، الوظيفة الثانية المجدولة في 19 كانون الأول/ديسمبر 2012، في حقل **الفترة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="7d3af-129">ثم انقل الوظيفة ضمن الفترة المخططة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="7d3af-130">انقر فوق **التالي**</span><span class="sxs-lookup"><span data-stu-id="7d3af-130">Click **Forward**.</span></span> <span data-ttu-id="7d3af-131">لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأسفل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="7d3af-132">انقر فوق **انتقال للخلف**.</span><span class="sxs-lookup"><span data-stu-id="7d3af-132">Click **Backward**.</span></span> <span data-ttu-id="7d3af-133">لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأعلى في القائمة.</span><span class="sxs-lookup"><span data-stu-id="7d3af-133">Notice that the job is moved one line up on the list.</span></span>
