---
title: إعداد وظيفة كانبان عملية عندما لا تتوفر المواد لخلية العمل
description: يركز هذا الإجراء على إعداد وظيفة كانبان للمعالجة عندما لا تتوفر بعض المواد لخلية العمل، ولذلك من الضروري انتقاء المواد من المستودع.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d57df6188aacc2f8a56a7ba91c4ab50a90901a7e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421065"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="3a0fd-103">إعداد وظيفة كانبان عملية عندما لا تتوفر المواد لخلية العمل</span><span class="sxs-lookup"><span data-stu-id="3a0fd-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a0fd-104">يركز هذا الإجراء على إعداد وظيفة كانبان للمعالجة عندما لا تتوفر بعض المواد لخلية العمل، ولذلك من الضروري انتقاء المواد من المستودع.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="3a0fd-105">يُعد الإجراء "إعداد وظيفة كانبان للمعالجة عندما تتوفر المواد‬" شرطًا أساسيًا لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="3a0fd-106">هذا الإجراء مخصص لعامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="3a0fd-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3a0fd-108">انتقل إلى التحكم بالإنتاج‬ > كانبان > لوحة كانبان لوظائف المعالجة‬.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="3a0fd-109">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3a0fd-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3a0fd-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="3a0fd-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a0fd-113">حدد كانبان 000356.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="3a0fd-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a0fd-115">في القائمة، قم بإلغاء تحديد الصف 4.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-115">In the list, deselect row 4.</span></span> <span data-ttu-id="3a0fd-116">أو حدد الصف 4 إذا لم تكن قد أكملت المهمة "إعداد وظيفة كانبان للمعالجة عندما تتوفر المواد‬".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="3a0fd-117">بدّل توسيع المقطع قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="3a0fd-118">تشير أيقونة عدم وجود إدخال في حالة التوريد إلى فقدان 48 لكل صنف P0002 لخلية العمل.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="3a0fd-119">نقل المواد إلى خلية العمل</span><span class="sxs-lookup"><span data-stu-id="3a0fd-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="3a0fd-120">بدّل توسيع المقطع "وظائف النقل‬".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="3a0fd-121">استخدام عامل التصفية السريع لتصفية حقل رقم الصنف باستخدام القيمة "P0002".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="3a0fd-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3a0fd-123">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-123">Click Start.</span></span>
    * <span data-ttu-id="3a0fd-124">جارٍ تنفيذ عملية النقل.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="3a0fd-125">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-125">Click Complete.</span></span>
    * <span data-ttu-id="3a0fd-126">يتوفر الآن الصنف P0002 في قائمة الانتقاء لوظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="3a0fd-127">وهذا يعني أنه يمكننا تحضير الكانبان مع جميع المواد المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="3a0fd-128">انقر فوق "تحضير‬".</span><span class="sxs-lookup"><span data-stu-id="3a0fd-128">Click Prepare.</span></span>
    * <span data-ttu-id="3a0fd-129">لاحظ أن الأيقونة في حالة الوظيفة تشير إلى أن الوظيفة جاهزة الآن.</span><span class="sxs-lookup"><span data-stu-id="3a0fd-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

