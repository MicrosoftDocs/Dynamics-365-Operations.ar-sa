--- 
title: "إنشاء مهمة مجموعة"
description: "إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-batch-job"></a><span data-ttu-id="6bdc5-103">إنشاء مهمة مجموعة</span><span class="sxs-lookup"><span data-stu-id="6bdc5-103">Create a batch job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6bdc5-104">إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="6bdc5-105">ويتم تشغيل الوظائف الدفعية باستخدام بيانات اعتماد الأمان للمستخدم الذي قام بإنشاء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="6bdc5-106">استخدم الإجراء التالي لإنشاء وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="6bdc5-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="6bdc5-108">إنشاء الوظيفة الدفعية</span><span class="sxs-lookup"><span data-stu-id="6bdc5-108">Create the batch job</span></span>
1. <span data-ttu-id="6bdc5-109">انتقل إلى إدارة النظام > الاستعلامات > الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="6bdc5-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-110">Click New.</span></span>
3. <span data-ttu-id="6bdc5-111">في حقل "وصف الوظيفة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="6bdc5-112">في الحقل "تاريخ/وقت البدء المجدول‬"، أدخل الوقت والتاريخ.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="6bdc5-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="6bdc5-114">إنشاء تكرار</span><span class="sxs-lookup"><span data-stu-id="6bdc5-114">Create a recurrence</span></span>
1. <span data-ttu-id="6bdc5-115">في جزء الإجراءات، انقر فوق "وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="6bdc5-116">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-116">Click Recurrence.</span></span>
    * <span data-ttu-id="6bdc5-117">استخدم هذه الخيارات لإدخال نطاق ونمط للتكرار.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="6bdc5-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="6bdc5-119">إضافة تنبيهات</span><span class="sxs-lookup"><span data-stu-id="6bdc5-119">Add alerts</span></span>
1. <span data-ttu-id="6bdc5-120">في جزء الإجراءات، انقر فوق "وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="6bdc5-121">انقر فوق "تنبيهات".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-121">Click Alerts.</span></span>
    * <span data-ttu-id="6bdc5-122">حدد إن كنت تريد إرسال رسائل تنبيه عند انتهاء الوظيفة الدفعية‬، أو إذا احتوت الوظيفة الدفعية على خطأ أو إذا تم إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="6bdc5-123">ثم حدد إذا كنت تريد عرض التنبيهات كرسائل منبثقة.</span><span class="sxs-lookup"><span data-stu-id="6bdc5-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="6bdc5-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6bdc5-124">Click OK.</span></span>


