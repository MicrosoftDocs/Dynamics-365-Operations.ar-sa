---
title: إنشاء مهمة مجموعة
description: إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562871"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="51b10-103">إنشاء مهمة مجموعة</span><span class="sxs-lookup"><span data-stu-id="51b10-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51b10-104">إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="51b10-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="51b10-105">ويتم تشغيل الوظائف الدفعية باستخدام بيانات اعتماد الأمان للمستخدم الذي قام بإنشاء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="51b10-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="51b10-106">استخدم الإجراء التالي لإنشاء وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="51b10-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="51b10-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="51b10-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="51b10-108">إنشاء الوظيفة الدفعية</span><span class="sxs-lookup"><span data-stu-id="51b10-108">Create the batch job</span></span>
1. <span data-ttu-id="51b10-109">انتقل إلى إدارة النظام > الاستعلامات > الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="51b10-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="51b10-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="51b10-110">Click New.</span></span>
3. <span data-ttu-id="51b10-111">في حقل "وصف الوظيفة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="51b10-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="51b10-112">في الحقل "تاريخ/وقت البدء المجدول‬"، أدخل الوقت والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="51b10-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="51b10-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="51b10-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="51b10-114">إنشاء تكرار</span><span class="sxs-lookup"><span data-stu-id="51b10-114">Create a recurrence</span></span>
1. <span data-ttu-id="51b10-115">في جزء الإجراءات، انقر فوق "وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="51b10-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="51b10-116">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="51b10-116">Click Recurrence.</span></span>
    * <span data-ttu-id="51b10-117">استخدم هذه الخيارات لإدخال نطاق ونمط للتكرار.</span><span class="sxs-lookup"><span data-stu-id="51b10-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="51b10-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="51b10-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="51b10-119">إضافة تنبيهات</span><span class="sxs-lookup"><span data-stu-id="51b10-119">Add alerts</span></span>
1. <span data-ttu-id="51b10-120">في جزء الإجراءات، انقر فوق "وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="51b10-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="51b10-121">انقر فوق "تنبيهات".</span><span class="sxs-lookup"><span data-stu-id="51b10-121">Click Alerts.</span></span>
    * <span data-ttu-id="51b10-122">حدد إن كنت تريد إرسال رسائل تنبيه عند انتهاء الوظيفة الدفعية‬، أو إذا احتوت الوظيفة الدفعية على خطأ أو إذا تم إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="51b10-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="51b10-123">ثم حدد إذا كنت تريد عرض التنبيهات كرسائل منبثقة.</span><span class="sxs-lookup"><span data-stu-id="51b10-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="51b10-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="51b10-124">Click OK.</span></span>

