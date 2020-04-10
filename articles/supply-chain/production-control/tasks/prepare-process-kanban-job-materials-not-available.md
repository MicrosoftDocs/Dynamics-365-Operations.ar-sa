---
title: إعداد وظيفة كانبان عملية عندما لا تتوفر المواد لخلية العمل
description: يركز هذا الإجراء على إعداد وظيفة كانبان للمعالجة عندما لا تتوفر بعض المواد لخلية العمل، ولذلك من الضروري انتقاء المواد من المستودع.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f779db14a866cc9a401d15e0666883ba3a828548
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146688"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="f796b-103">إعداد وظيفة كانبان عملية عندما لا تتوفر المواد لخلية العمل</span><span class="sxs-lookup"><span data-stu-id="f796b-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f796b-104">يركز هذا الإجراء على إعداد وظيفة كانبان للمعالجة عندما لا تتوفر بعض المواد لخلية العمل، ولذلك من الضروري انتقاء المواد من المستودع.</span><span class="sxs-lookup"><span data-stu-id="f796b-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="f796b-105">يُعد الإجراء "إعداد وظيفة كانبان للمعالجة عندما تتوفر المواد‬" شرطًا أساسيًا لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="f796b-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="f796b-106">هذا الإجراء مخصص لعامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="f796b-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="f796b-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="f796b-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f796b-108">انتقل إلى التحكم بالإنتاج‬ > كانبان > لوحة كانبان لوظائف المعالجة‬.</span><span class="sxs-lookup"><span data-stu-id="f796b-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="f796b-109">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f796b-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f796b-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f796b-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f796b-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="f796b-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="f796b-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f796b-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f796b-113">حدد كانبان 000356.</span><span class="sxs-lookup"><span data-stu-id="f796b-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="f796b-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f796b-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f796b-115">في القائمة، قم بإلغاء تحديد الصف 4.</span><span class="sxs-lookup"><span data-stu-id="f796b-115">In the list, deselect row 4.</span></span> <span data-ttu-id="f796b-116">أو حدد الصف 4 إذا لم تكن قد أكملت المهمة "إعداد وظيفة كانبان للمعالجة عندما تتوفر المواد‬".</span><span class="sxs-lookup"><span data-stu-id="f796b-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="f796b-117">بدّل توسيع المقطع قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="f796b-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="f796b-118">تشير أيقونة عدم وجود إدخال في حالة التوريد إلى فقدان 48 لكل صنف P0002 لخلية العمل.</span><span class="sxs-lookup"><span data-stu-id="f796b-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="f796b-119">نقل المواد إلى خلية العمل</span><span class="sxs-lookup"><span data-stu-id="f796b-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="f796b-120">بدّل توسيع المقطع "وظائف النقل‬".</span><span class="sxs-lookup"><span data-stu-id="f796b-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="f796b-121">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P0002".</span><span class="sxs-lookup"><span data-stu-id="f796b-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="f796b-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f796b-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f796b-123">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="f796b-123">Click Start.</span></span>
    * <span data-ttu-id="f796b-124">جارٍ تنفيذ عملية النقل.</span><span class="sxs-lookup"><span data-stu-id="f796b-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="f796b-125">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="f796b-125">Click Complete.</span></span>
    * <span data-ttu-id="f796b-126">يتوفر الآن الصنف P0002 في قائمة الانتقاء لوظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="f796b-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="f796b-127">وهذا يعني أنه يمكننا تحضير الكانبان مع جميع المواد المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="f796b-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="f796b-128">انقر فوق "تحضير‬".</span><span class="sxs-lookup"><span data-stu-id="f796b-128">Click Prepare.</span></span>
    * <span data-ttu-id="f796b-129">لاحظ أن الأيقونة في حالة الوظيفة تشير إلى أن الوظيفة جاهزة الآن.</span><span class="sxs-lookup"><span data-stu-id="f796b-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

