--- 
title: "إنشاء قاعدة كانبان لأنشطة متعددة"
description: "يوضح هذا الإجراء كيفية إنشاء قاعدة كانبان تتضمن أنشطة متعددة من تدفق إنتاج."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.openlocfilehash: d6d0c50da3124553124b65f6ba0e1c5ed35e8613
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="ee51b-103">إنشاء قاعدة كانبان لأنشطة متعددة</span><span class="sxs-lookup"><span data-stu-id="ee51b-103">Create a kanban rule for multiple activities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee51b-104">يوضح هذا الإجراء كيفية إنشاء قاعدة كانبان تتضمن أنشطة متعددة من تدفق إنتاج.</span><span class="sxs-lookup"><span data-stu-id="ee51b-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="ee51b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="ee51b-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ee51b-106">هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند قيامه بتحضير عملية إنتاج منتج جديد أو معدل في بيئة محدودة.</span><span class="sxs-lookup"><span data-stu-id="ee51b-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ee51b-107">إنشاء قاعدة كانبان جديدة</span><span class="sxs-lookup"><span data-stu-id="ee51b-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="ee51b-108">انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.</span><span class="sxs-lookup"><span data-stu-id="ee51b-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="ee51b-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ee51b-109">Click New.</span></span>
3. <span data-ttu-id="ee51b-110">في حقل "استراتيجية التزويد"، حدد "مجدول".</span><span class="sxs-lookup"><span data-stu-id="ee51b-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="ee51b-111">في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ee51b-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ee51b-112">حدد SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="ee51b-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="ee51b-113">حدد خانة الاختيار "أنشطة متعددة".</span><span class="sxs-lookup"><span data-stu-id="ee51b-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="ee51b-114">الغرض هو تضمين أكثر من نشاط واحد في قاعدة كانبان.</span><span class="sxs-lookup"><span data-stu-id="ee51b-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="ee51b-115">ستختار مسارًا في تدفق الإنتاج عند تحديد نشاط الخطة الأخير.</span><span class="sxs-lookup"><span data-stu-id="ee51b-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="ee51b-116">في الحقل "نشاط الخطة الأخير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ee51b-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ee51b-117">حدد SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="ee51b-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="ee51b-118">بعد تحديد القيمة، تفتح صفحة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="ee51b-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="ee51b-119">حدد تدفق كانبان SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="ee51b-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="ee51b-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ee51b-120">Click OK.</span></span>  
7. <span data-ttu-id="ee51b-121">قم بتوسيع القسم "التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="ee51b-121">Expand the Details section.</span></span>
8. <span data-ttu-id="ee51b-122">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ee51b-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ee51b-123">حدد الصنف L0006.</span><span class="sxs-lookup"><span data-stu-id="ee51b-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="ee51b-124">إنشاء كانبان وعرض الوظائف</span><span class="sxs-lookup"><span data-stu-id="ee51b-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="ee51b-125">قم بتوسيع القسم "كانبان".</span><span class="sxs-lookup"><span data-stu-id="ee51b-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="ee51b-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ee51b-126">Click Add.</span></span>
3. <span data-ttu-id="ee51b-127">في الحقل "عدد بطاقات كانبان الجديدة‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="ee51b-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="ee51b-128">سيؤدي هذا إلى إنشاء كانبان.</span><span class="sxs-lookup"><span data-stu-id="ee51b-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="ee51b-129">عيّن كمية المنتجات إلى "3".</span><span class="sxs-lookup"><span data-stu-id="ee51b-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="ee51b-130">سيعالج كانبان 3 منتجات.</span><span class="sxs-lookup"><span data-stu-id="ee51b-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="ee51b-131">في الحقل "‏‫تاريخ/وقت الاستحقاق‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="ee51b-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="ee51b-132">يمكنك إدخال "اليوم".</span><span class="sxs-lookup"><span data-stu-id="ee51b-132">You can enter Today.</span></span>  
6. <span data-ttu-id="ee51b-133">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="ee51b-133">Click Create.</span></span>
7. <span data-ttu-id="ee51b-134">انقر فوق "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="ee51b-134">Click Details.</span></span>
    * <span data-ttu-id="ee51b-135">لاحظ وجود وظيفتي معالجة لكانبان من تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ee51b-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="ee51b-136">الوظيفة الأولى هي SpeakerAssemblyAndPolish، والثانية هي SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="ee51b-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="ee51b-137">هذه هي الخطوة الأخيرة!</span><span class="sxs-lookup"><span data-stu-id="ee51b-137">This is the last step!</span></span>  


