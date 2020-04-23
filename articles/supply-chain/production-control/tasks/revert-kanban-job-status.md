---
title: عكس حالة وظيفة الكانبان
description: يركز هذا الإجراء على عكس حالة وظيفة كانبان غير الصحيحة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adf65175669d4cd5ec4cb431a7e1436ea3da83ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210492"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="d1109-103">عكس حالة وظيفة الكانبان</span><span class="sxs-lookup"><span data-stu-id="d1109-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1109-104">يركز هذا الإجراء على عكس حالة وظيفة كانبان غير الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="d1109-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="d1109-105">ويكون هذا مفيدًا في حالة قيام مشغل الجهاز بتحديث الوظيفة الخاطئة، أو تعيين الحالة الخاطئة عن طريق الخطأ.</span><span class="sxs-lookup"><span data-stu-id="d1109-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="d1109-106">وفي هذا الإجراء، يتم تسجيل وظيفة كانبان كما تم إعدادها عن طريق الخطأ، ويتم عكس الحالة.</span><span class="sxs-lookup"><span data-stu-id="d1109-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="d1109-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="d1109-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d1109-108">ويُعد هذا الإجراء مخصصًا إلى مشرف المتجر أو عامل تشغيل الجهاز الذي يعمل في شركة lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="d1109-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="d1109-109">افتح لوحة عملية لخلية العمل</span><span class="sxs-lookup"><span data-stu-id="d1109-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="d1109-110">انتقل إلى "‏‫لوحة كانبان لوظائف المعالجة‬".</span><span class="sxs-lookup"><span data-stu-id="d1109-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="d1109-111">في حقل "خلية العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d1109-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="d1109-112">حدد خلية العمل 1260.</span><span class="sxs-lookup"><span data-stu-id="d1109-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="d1109-113">إعداد وظيفة كانبان</span><span class="sxs-lookup"><span data-stu-id="d1109-113">Prepare kanban job</span></span>
1. <span data-ttu-id="d1109-114">انقر فوق "تحضير‬".</span><span class="sxs-lookup"><span data-stu-id="d1109-114">Click Prepare.</span></span>
    * <span data-ttu-id="d1109-115">إذا تعذر النقر فوق "التحضير" لأن اللون رمادي، فتأكد من أن وظيفة كانبان المحددة لها حالة مخططة، ويشار إليها بالرمز قيمة كانبان فارغة.</span><span class="sxs-lookup"><span data-stu-id="d1109-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="d1109-116">إذا فشل "التحضير"، فتأكد من توفر جميع المواد الموجودة في قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="d1109-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="d1109-117">في القائمة، حدد الوظيفة المُعدة.</span><span class="sxs-lookup"><span data-stu-id="d1109-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="d1109-118">حدد الوظيفة الأولى التي أعددتها للتو.</span><span class="sxs-lookup"><span data-stu-id="d1109-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="d1109-119">لاحظ أنه يتم إعداد حالة الوظائف، والتي يشار إليها بمثلث داخل رمز كانبان.</span><span class="sxs-lookup"><span data-stu-id="d1109-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="d1109-120">عكس حالة وظيفة كانبان المُعدة</span><span class="sxs-lookup"><span data-stu-id="d1109-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="d1109-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d1109-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d1109-122">حدد الوظيفة الأولى التي تم إعدادها.</span><span class="sxs-lookup"><span data-stu-id="d1109-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="d1109-123">في جزء "الإجراءات"، انقر فوق "تصنيع".</span><span class="sxs-lookup"><span data-stu-id="d1109-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="d1109-124">انقر فوق "عكس الحالة".</span><span class="sxs-lookup"><span data-stu-id="d1109-124">Click Revert status.</span></span>
    * <span data-ttu-id="d1109-125">يمكنك استخدام قاعدة كانبان بديلة إذا تحققت الشروط التالية:  - استراتيجية التزويد هي نفسها لكل من القاعدتين.</span><span class="sxs-lookup"><span data-stu-id="d1109-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="d1109-126">- إصدار تدفق الإنتاج هو نفسه لكل من القاعدتين.</span><span class="sxs-lookup"><span data-stu-id="d1109-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="d1109-127">- المنتج الذي تم توفيره هو نفسه لكل من القاعدتين.</span><span class="sxs-lookup"><span data-stu-id="d1109-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="d1109-128">- يجب أن تكون أي أنشطة المراحل النهائية التي تم تكوينها للنشاط الأخير من قواعد كانبان هي نفسها لكل من القاعدتين.</span><span class="sxs-lookup"><span data-stu-id="d1109-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="d1109-129">- يجب تكوين نفس أبعاد المخزون المتوفر لكل من القاعدتين.</span><span class="sxs-lookup"><span data-stu-id="d1109-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="d1109-130">- يجب عدم تعيين حالة وحدة معالجة المواد.</span><span class="sxs-lookup"><span data-stu-id="d1109-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="d1109-131">- يجب أن يكون تكوين كانبان للحدث هو نفسه.</span><span class="sxs-lookup"><span data-stu-id="d1109-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="d1109-132">تأكد من أنه تم تخطيط الحالة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="d1109-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="d1109-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d1109-133">Click OK.</span></span>
5. <span data-ttu-id="d1109-134">في القائمة، قم بإلغاء علامة الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d1109-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="d1109-135">حدد الوظيفة نفسها.</span><span class="sxs-lookup"><span data-stu-id="d1109-135">Select the same job.</span></span>  
    * <span data-ttu-id="d1109-136">لاحظ أنه تم عكس حالة الوظيفة لوظيفة كانبان إلى مخططة، ويشار إليها بالرمز قيمة كانبان فارغة.</span><span class="sxs-lookup"><span data-stu-id="d1109-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

