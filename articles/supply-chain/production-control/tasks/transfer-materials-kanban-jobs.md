--- 
title: "تحويل مواد مع وظائف كانبان"
description: "يركز هذا الإجراء على تنفيذ مهمة كانبان للسحب لتحويل المواد."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a2db7b9fb960beb5b4a851aabb9f28a0f9e3d3da
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="6b438-103">تحويل مواد مع وظائف كانبان</span><span class="sxs-lookup"><span data-stu-id="6b438-103">Transfer materials with kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b438-104">يركز هذا الإجراء على تنفيذ مهمة كانبان للسحب لتحويل المواد.</span><span class="sxs-lookup"><span data-stu-id="6b438-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="6b438-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="6b438-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6b438-106">هذا الإجراء مخصص لعامل المستودع.</span><span class="sxs-lookup"><span data-stu-id="6b438-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="6b438-107">عرض وظائف التحويل</span><span class="sxs-lookup"><span data-stu-id="6b438-107">Display transfer jobs</span></span>
1. <span data-ttu-id="6b438-108">انتقل إلى التحكم بالإنتاج > كانبان > لوحة كانبان لوظائف التحويل.</span><span class="sxs-lookup"><span data-stu-id="6b438-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="6b438-109">قم بتوسيع أو طي القسم عوامل التصفية .</span><span class="sxs-lookup"><span data-stu-id="6b438-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="6b438-110">في المقطع "عوامل التصفية"، يمكنك تحديد الوظائف التي تريد الاطلاع عليها عن طريق إجراء التصفية على تدفق الإنتاج واسم النشاط ومن المستودع والموقع، وإلى المستودع والموقع.</span><span class="sxs-lookup"><span data-stu-id="6b438-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="6b438-111">في الحقل "من المستودع"، اكتب "11".</span><span class="sxs-lookup"><span data-stu-id="6b438-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="6b438-112">في الحقل "إلى الموقع"، اكتب "12".</span><span class="sxs-lookup"><span data-stu-id="6b438-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="6b438-113">بدء مهمة تحويل</span><span class="sxs-lookup"><span data-stu-id="6b438-113">Start a transfer job</span></span>
1. <span data-ttu-id="6b438-114">في القائمة، قم بإلغاء تحديد الصف المحدد - إن وجد.</span><span class="sxs-lookup"><span data-stu-id="6b438-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="6b438-115">في القائمة، حدد الصف 4.</span><span class="sxs-lookup"><span data-stu-id="6b438-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="6b438-116">حدد الوظيفة الأولى مع الحالة "غير مخطط".</span><span class="sxs-lookup"><span data-stu-id="6b438-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="6b438-117">تأكد من تحديد هذه الوظيفة فقط.</span><span class="sxs-lookup"><span data-stu-id="6b438-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="6b438-118">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="6b438-118">Click Start.</span></span>
    * <span data-ttu-id="6b438-119">لاحظ أن ثمة أيقونة تشير إلى بدء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="6b438-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="6b438-120">تحديد وظيفة تحويل ثانية وتغيير الكمية</span><span class="sxs-lookup"><span data-stu-id="6b438-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="6b438-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b438-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b438-122">يمكنك تحديد وظائف متعددة، ولكن بالنسبة إلى الآن حدد الصف 5.</span><span class="sxs-lookup"><span data-stu-id="6b438-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="6b438-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b438-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b438-124">تأكد من أن المهمة في الخطوة السابقة هي وحدها محددة.</span><span class="sxs-lookup"><span data-stu-id="6b438-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="6b438-125">قم بإلغاء تحديد كافة الوظائف الأخرى.</span><span class="sxs-lookup"><span data-stu-id="6b438-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="6b438-126">دوّن القيمة الموجودة في الحقل "كمية الوظيفة‬" للرجوع إليها فيما بعد</span><span class="sxs-lookup"><span data-stu-id="6b438-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="6b438-127">عيّن "كمية الوظيفة" إلى "30".</span><span class="sxs-lookup"><span data-stu-id="6b438-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="6b438-128">لاحظ التحذير!</span><span class="sxs-lookup"><span data-stu-id="6b438-128">Notice the warning!</span></span> <span data-ttu-id="6b438-129">غير مسموح لك بتحويل 30.</span><span class="sxs-lookup"><span data-stu-id="6b438-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="6b438-130">وفقًا لإعداد قاعدة كانبان، يمكنك فقط تحويل الكمية الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6b438-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="6b438-131">استخدم القيمة التي تم تدوينها سابقًا في الحقل "كمية الوظيفة".</span><span class="sxs-lookup"><span data-stu-id="6b438-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="6b438-132">عيّن كمية الوظيفة إلى القيمة السابقة.</span><span class="sxs-lookup"><span data-stu-id="6b438-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="6b438-133">بدء وظيفة النقل الثانية</span><span class="sxs-lookup"><span data-stu-id="6b438-133">Start the second transfer job</span></span>
1. <span data-ttu-id="6b438-134">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="6b438-134">Click Start.</span></span>
    * <span data-ttu-id="6b438-135">سيؤدي ذلك إلى بدء تحويل الوظيفة في الصف 5.</span><span class="sxs-lookup"><span data-stu-id="6b438-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="6b438-136">إكمال وظيفتي التحويل</span><span class="sxs-lookup"><span data-stu-id="6b438-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="6b438-137">في القائمة، حدد الصف 4.</span><span class="sxs-lookup"><span data-stu-id="6b438-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="6b438-138">تم الآن تحديد وظيفتي تحويل في الصف 4 والصف 5.</span><span class="sxs-lookup"><span data-stu-id="6b438-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="6b438-139">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="6b438-139">Click Complete.</span></span>
    * <span data-ttu-id="6b438-140">سيؤدي ذلك إلى إكمال تحويل الوظيفتين.</span><span class="sxs-lookup"><span data-stu-id="6b438-140">This will complete the transfer of both jobs.</span></span>  


