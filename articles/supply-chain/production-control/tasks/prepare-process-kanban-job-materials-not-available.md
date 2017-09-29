--- 
title: "إعداد وظيفة كانبان عملية عندما لا تتوفر المواد لخلية العمل"
description: "يركز هذا الإجراء على إعداد وظيفة كانبان للمعالجة عندما لا تتوفر بعض المواد لخلية العمل، ولذلك من الضروري انتقاء المواد من المستودع."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="50c6c-103">إعداد وظيفة كانبان عملية عندما لا تتوفر المواد لخلية العمل</span><span class="sxs-lookup"><span data-stu-id="50c6c-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50c6c-104">يركز هذا الإجراء على إعداد وظيفة كانبان للمعالجة عندما لا تتوفر بعض المواد لخلية العمل، ولذلك من الضروري انتقاء المواد من المستودع.</span><span class="sxs-lookup"><span data-stu-id="50c6c-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="50c6c-105">يُعد الإجراء "إعداد وظيفة كانبان للمعالجة عندما تتوفر المواد‬" شرطًا أساسيًا لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="50c6c-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="50c6c-106">هذا الإجراء مخصص لعامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="50c6c-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="50c6c-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="50c6c-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="50c6c-108">انتقل إلى التحكم بالإنتاج‬ > كانبان > لوحة كانبان لوظائف المعالجة‬.</span><span class="sxs-lookup"><span data-stu-id="50c6c-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="50c6c-109">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="50c6c-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="50c6c-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="50c6c-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="50c6c-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="50c6c-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="50c6c-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="50c6c-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50c6c-113">حدد كانبان 000356.</span><span class="sxs-lookup"><span data-stu-id="50c6c-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="50c6c-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="50c6c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50c6c-115">في القائمة، قم بإلغاء تحديد الصف 4.</span><span class="sxs-lookup"><span data-stu-id="50c6c-115">In the list, deselect row 4.</span></span> <span data-ttu-id="50c6c-116">أو حدد الصف 4 إذا لم تكن قد أكملت المهمة "إعداد وظيفة كانبان للمعالجة عندما تتوفر المواد‬".</span><span class="sxs-lookup"><span data-stu-id="50c6c-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="50c6c-117">بدّل توسيع المقطع قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="50c6c-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="50c6c-118">تشير أيقونة عدم وجود إدخال في حالة التوريد إلى فقدان 48 لكل صنف P0002 لخلية العمل.</span><span class="sxs-lookup"><span data-stu-id="50c6c-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="50c6c-119">نقل المواد إلى خلية العمل</span><span class="sxs-lookup"><span data-stu-id="50c6c-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="50c6c-120">بدّل توسيع المقطع "وظائف النقل‬".</span><span class="sxs-lookup"><span data-stu-id="50c6c-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="50c6c-121">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P0002".</span><span class="sxs-lookup"><span data-stu-id="50c6c-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="50c6c-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="50c6c-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="50c6c-123">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="50c6c-123">Click Start.</span></span>
    * <span data-ttu-id="50c6c-124">جارٍ تنفيذ عملية النقل.</span><span class="sxs-lookup"><span data-stu-id="50c6c-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="50c6c-125">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="50c6c-125">Click Complete.</span></span>
    * <span data-ttu-id="50c6c-126">يتوفر الآن الصنف P0002 في قائمة الانتقاء لوظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="50c6c-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="50c6c-127">وهذا يعني أنه يمكننا تحضير الكانبان مع جميع المواد المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="50c6c-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="50c6c-128">انقر فوق "تحضير‬".</span><span class="sxs-lookup"><span data-stu-id="50c6c-128">Click Prepare.</span></span>
    * <span data-ttu-id="50c6c-129">لاحظ أن الأيقونة في حالة الوظيفة تشير إلى أن الوظيفة جاهزة الآن.</span><span class="sxs-lookup"><span data-stu-id="50c6c-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


