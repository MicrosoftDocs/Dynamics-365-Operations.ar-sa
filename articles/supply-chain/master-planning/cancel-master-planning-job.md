---
title: إلغاء وظيفة التخطيط الرئيسي
description: يشرح هذا الموضوع كيفية إلغاء وظيفة تخطيط نشطة تستخدم وظيفة التخطيط المُضمن.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f5ce460cc2915d1d4d9b5699723a62ed7f94599
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421617"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="4e1a1-103">إلغاء وظيفة التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="4e1a1-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e1a1-104">في Microsoft Dynamics 365 Supply Chain Management، هناك اختيارات متعددة لإلغاء وظيفة التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="4e1a1-105">على سبيل المثال، قد ترغب في إلغاء وظيفة تخطيط رئيسيه إذا تم تشغيلها عن طريق الخطأ أو انها تعمل لفتره أطول من المتوقع وتريد إنهائها.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="4e1a1-106">أفضل طريقة لإلغاء وظيفة التخطيط هي من صفحة **عمليات التخطيط غير المكتملة** .</span><span class="sxs-lookup"><span data-stu-id="4e1a1-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="4e1a1-107">تُستخدم اختيارات بديلة من صفحات **الوظائف الدفعية‬** و **الوظائف الدفعية‬ المحسّنة** فقط في حالة عدم اكتمال إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** في غضون بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="4e1a1-108">خيار الإلغاء المفضل</span><span class="sxs-lookup"><span data-stu-id="4e1a1-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="4e1a1-109">إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** .</span><span class="sxs-lookup"><span data-stu-id="4e1a1-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="4e1a1-110">انتقل إلى **التخطيط الرئيسي‬ > الاستعلامات والتقارير‬ > التخطيط الرئيسي‬ > عمليات التخطيط غير المكتملة**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="4e1a1-111">حدد سطر عملية التخطيط التي تريد إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="4e1a1-112">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="4e1a1-113">خيارات إلغاء إضافية</span><span class="sxs-lookup"><span data-stu-id="4e1a1-113">Additional cancel options</span></span>
<span data-ttu-id="4e1a1-114">تُستخدم هذه فقط إذا لم يكتمل إلغاء وظيفة التخطيط الرئيسي من صفحة **عمليات التخطيط غير المكتملة** في غضون بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="4e1a1-115">حذف وظيفة التخطيط الرئيسي من صفحة **الوظائف الدفعية** .</span><span class="sxs-lookup"><span data-stu-id="4e1a1-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="4e1a1-116">انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="4e1a1-117">حدد سطر وظيفة التخطيط التي تريد إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="4e1a1-118">انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="4e1a1-119">حذف وظيفة التخطيط الرئيسية من صفحة **الوظائف الدفعية المُحسنة** .</span><span class="sxs-lookup"><span data-stu-id="4e1a1-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="4e1a1-120">انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="4e1a1-121">إذا لم يتم عرض معرف الوظيفة في القائمة، فانقر فوق **التبديل إلى النموذج المحسّن**، وإلا فتابع الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="4e1a1-122">فتح الوظيفة الدفعية</span><span class="sxs-lookup"><span data-stu-id="4e1a1-122">Open the batch job.</span></span> <span data-ttu-id="4e1a1-123">انقر فوق **معرف الوظيفة** للوظيفة الدفعية مع المهام التي تريد إنهائها.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="4e1a1-124">في **الوظائف الدفعية**، حدد المهام المطلوب إنهاؤها.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="4e1a1-125">انقر فوق **تغيير الحالة**، واختر **إلغاء التحديد** ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="4e1a1-126">في علامة التبويب السريعة **مهام الدُفعة** ، انقر فوق **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="4e1a1-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
