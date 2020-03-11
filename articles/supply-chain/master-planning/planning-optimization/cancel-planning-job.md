---
title: إلغاء وظيفة تخطيط
description: يوضح هذا الموضوع كيفية إلغاء وظيفة تخطيط نشطة تستخدم وظيفة تحسين التخطيط.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 18c5c7b8030fc6adbc548dab750e4f454aebc867
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076330"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="1b44e-103">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="1b44e-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1b44e-104">في Microsoft Dynamics 365 Supply Chain Management، يمكنك إلغاء وظيفة تخطيط نشطة تستخدم وظيفة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1b44e-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="1b44e-105">عندما تقوم بتحديد **إلغاء** في مربع الحوار عند تشغيل مهمة تحسين التخطيط مباشرة من واجهة المستخدم (غير موجودة في الخلفية)، فلن يؤدي ذلك إلى إلغاء مهمة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1b44e-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="1b44e-106">حتى إذا تلقيت تحذيرًا مثل "تم إلغاء العملية"، فإنك ستظل بحاجة إلى استخدام الخطوات التالية لإلغاء مهمة تخطيط بتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1b44e-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="1b44e-107">لإلغاء وظيفة تخطيط نشطة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1b44e-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="1b44e-108">يمكن إلغاء الوظائف النشطة فقط.</span><span class="sxs-lookup"><span data-stu-id="1b44e-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="1b44e-109">انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط**.</span><span class="sxs-lookup"><span data-stu-id="1b44e-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="1b44e-110">حدد خطة مناسبة لتشغيل التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1b44e-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="1b44e-111">حدد **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="1b44e-111">Select **History**.</span></span>
4. <span data-ttu-id="1b44e-112">حدد وظيفة التخطيط المراد إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="1b44e-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="1b44e-113">حدد **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="1b44e-113">Select **Cancel**.</span></span>

<span data-ttu-id="1b44e-114">ستكون حالة الوظيفة **قيد الإلغاء** حتى تؤكد خدمة تحسين التخطيط أنه تم إلغاء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1b44e-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="1b44e-115">سيتم تغيير الحالة بعد ذلك إلى **تم الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="1b44e-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="1b44e-116">لرؤية تغييرات الحالة، يجب تحديث الصفحة بتحديد الزر **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="1b44e-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b44e-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1b44e-117">Additional resources</span></span>

[<span data-ttu-id="1b44e-118">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="1b44e-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1b44e-119">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1b44e-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1b44e-120">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="1b44e-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1b44e-121">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="1b44e-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1b44e-122">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="1b44e-122">Apply filters to a plan</span></span>](plan-filters.md)
