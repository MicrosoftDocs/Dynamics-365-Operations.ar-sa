---
title: نقل وظائف كانبان المجدولة
description: يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2526c2bd106e35c736e930b5b5114d019718dc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836230"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="eed7b-103">نقل وظائف كانبان المجدولة</span><span class="sxs-lookup"><span data-stu-id="eed7b-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eed7b-104">يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى.</span><span class="sxs-lookup"><span data-stu-id="eed7b-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="eed7b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="eed7b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eed7b-106">هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬ الذي يعمل مع كانبان.</span><span class="sxs-lookup"><span data-stu-id="eed7b-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="eed7b-107">حدد وظائف كانبان المُجدولة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="eed7b-108">انتقل إلى **التحكم بالإنتاج > كانبان > جدولة وظيفة كانبان**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="eed7b-109">في حقل **خلية العمل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="eed7b-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="eed7b-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="eed7b-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="eed7b-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="eed7b-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="eed7b-112">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-112">Click **Select**.</span></span> 

5. <span data-ttu-id="eed7b-113">في حقل **عرض حالة الوظيفة**، حدد **تمت الجدولة**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="eed7b-114">يؤدي ذلك إلى تصفية قائمة الوظائف‬ لعرض وظائف كانبان المجدولة فقط.</span><span class="sxs-lookup"><span data-stu-id="eed7b-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="eed7b-115">نقل وظائف كانبان إلى فترة أخرى.</span><span class="sxs-lookup"><span data-stu-id="eed7b-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="eed7b-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="eed7b-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="eed7b-117">حدد وظيفة حالتها **مهمة مخططة**، على سبيل المثال، وظيفة مجدولة في 20 ديسمبر 2012 في حقل **الفترة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="eed7b-118">ثم انقل الوظيفة إلى الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="eed7b-119">انقر فوق **الفترة السابقة**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="eed7b-120">انقر **الإنهاء** لنقل الوظيفة إلى نهاية قائمة الوظائف كالوظيفة الأخيرة في الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="eed7b-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="eed7b-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="eed7b-122">حدد وظيفة حالتها **مهمة مخططة**، على سبيل المثال، وظيفة مجدولة في 18 ديسمبر 2012 في حقل **الفترة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="eed7b-123">ثم انقل الوظيفة إلى الفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="eed7b-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="eed7b-124">انقر فوق **الفترة التالية**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="eed7b-125">انقر **البدء** لنقل الوظيفة إلى بداية قائمة الوظائف كالوظيفة الأولى في الفترة السابقة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="eed7b-126">نقل وظيفة ضمن فترة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="eed7b-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="eed7b-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="eed7b-128">حدد وظيفة حالتها مهمة مخططة، على سبيل المثال، الوظيفة الثانية المجدولة في 19 كانون الأول/ديسمبر 2012، في حقل **الفترة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="eed7b-129">ثم انقل الوظيفة ضمن الفترة المخططة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="eed7b-130">انقر فوق **التالي**</span><span class="sxs-lookup"><span data-stu-id="eed7b-130">Click **Forward**.</span></span> <span data-ttu-id="eed7b-131">لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأسفل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="eed7b-132">انقر فوق **انتقال للخلف**.</span><span class="sxs-lookup"><span data-stu-id="eed7b-132">Click **Backward**.</span></span> <span data-ttu-id="eed7b-133">لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأعلى في القائمة.</span><span class="sxs-lookup"><span data-stu-id="eed7b-133">Notice that the job is moved one line up on the list.</span></span>
