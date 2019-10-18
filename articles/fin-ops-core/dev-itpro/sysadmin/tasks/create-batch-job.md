---
title: إنشاء مهمة مجموعة
description: إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191375"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="bdbf2-103">إنشاء مهمة مجموعة</span><span class="sxs-lookup"><span data-stu-id="bdbf2-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdbf2-104">إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="bdbf2-105">ويتم تشغيل الوظائف الدفعية باستخدام بيانات اعتماد الأمان للمستخدم الذي قام بإنشاء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="bdbf2-106">استخدم الإجراء التالي لإنشاء وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="bdbf2-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="bdbf2-108">إنشاء الوظيفة الدفعية</span><span class="sxs-lookup"><span data-stu-id="bdbf2-108">Create the batch job</span></span>
1. <span data-ttu-id="bdbf2-109">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الاستعلامات > الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="bdbf2-110">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-110">Click **New**.</span></span>
3. <span data-ttu-id="bdbf2-111">في حقل **وصف الوظيفة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="bdbf2-112">في حقل **تاريخ/وقت البدء المجدول‬**، أدخل الوقت والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="bdbf2-113">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="bdbf2-114">إنشاء تكرار</span><span class="sxs-lookup"><span data-stu-id="bdbf2-114">Create a recurrence</span></span>
1. <span data-ttu-id="bdbf2-115">في جزء الإجراءات، انقر فوق **وظيفة دفعية**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="bdbf2-116">انقر فوق **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-116">Click **Recurrence**.</span></span> <span data-ttu-id="bdbf2-117">استخدم هذه الخيارات لإدخال نطاق ونمط للتكرار.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="bdbf2-118">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="bdbf2-119">إضافة تنبيهات</span><span class="sxs-lookup"><span data-stu-id="bdbf2-119">Add alerts</span></span>
1. <span data-ttu-id="bdbf2-120">في جزء الإجراءات، انقر فوق **وظيفة دفعية**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="bdbf2-121">انقر فوق **تنبيهات**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-121">Click **Alerts**.</span></span> <span data-ttu-id="bdbf2-122">حدد إن كنت تريد إرسال رسائل تنبيه عند انتهاء الوظيفة الدفعية‬، أو إذا احتوت الوظيفة الدفعية على خطأ أو إذا تم إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="bdbf2-123">ثم حدد إذا كنت تريد عرض التنبيهات كرسائل منبثقة.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="bdbf2-124">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="bdbf2-125">ضبط حالة الوظيفة الدفعية</span><span class="sxs-lookup"><span data-stu-id="bdbf2-125">Adjust batch job status</span></span>
1. <span data-ttu-id="bdbf2-126">انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="bdbf2-127">حدد الوظيفة الدفعية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="bdbf2-128">في جزء الإجراءات، انقر فوق **وظيفة دفعية > الوظائف > حالة التغيير**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="bdbf2-129">حدد الحالة المناسبة:</span><span class="sxs-lookup"><span data-stu-id="bdbf2-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="bdbf2-130">**اقتطاع**: تعيين وظيفة دفعية كـ **اقتطاع** لكي يتم اقتطاعها من جدوله وظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="bdbf2-131">يكافئ *إيقاف*.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="bdbf2-132">**انتظار**: تعيين وظيفة دفعية كـ **انتظار** بحيث تكون قيد انتظار الالتقاط بواسطة جدولة الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="bdbf2-133">يكافئ *انطلاق*.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="bdbf2-134">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bdbf2-134">Click **OK**.</span></span>
