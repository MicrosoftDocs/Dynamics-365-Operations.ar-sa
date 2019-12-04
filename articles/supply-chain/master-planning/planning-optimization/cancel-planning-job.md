---
title: إلغاء وظيفة تخطيط
description: يوضح هذا الموضوع كيفية إلغاء وظيفة تخطيط نشطة تستخدم وظيفة تحسين التخطيط.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773896"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="224db-103">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="224db-103">Cancel a planning job</span></span>

<span data-ttu-id="224db-104">في Microsoft Dynamics 365 Supply Chain Management، يمكنك إلغاء وظيفة تخطيط نشطة تستخدم وظيفة تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="224db-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="224db-105">لإلغاء وظيفة تخطيط نشطة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="224db-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="224db-106">يمكن إلغاء الوظائف النشطة فقط.</span><span class="sxs-lookup"><span data-stu-id="224db-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="224db-107">انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط**.</span><span class="sxs-lookup"><span data-stu-id="224db-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="224db-108">حدد خطة مناسبة لتشغيل التخطيط.</span><span class="sxs-lookup"><span data-stu-id="224db-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="224db-109">حدد **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="224db-109">Select **History**.</span></span>
4. <span data-ttu-id="224db-110">حدد وظيفة التخطيط المراد إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="224db-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="224db-111">حدد **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="224db-111">Select **Cancel**.</span></span>

<span data-ttu-id="224db-112">ستكون حالة الوظيفة **قيد الإلغاء** حتى تؤكد خدمة تحسين التخطيط أنه تم إلغاء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="224db-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="224db-113">سيتم تغيير الحالة بعد ذلك إلى **تم الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="224db-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="224db-114">لرؤية تغييرات الحالة، يجب تحديث الصفحة بتحديد الزر **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="224db-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="224db-115">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="224db-115">Related resources</span></span>

[<span data-ttu-id="224db-116">نظرة عامة على تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="224db-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="224db-117">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="224db-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="224db-118">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="224db-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="224db-119">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="224db-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="224db-120">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="224db-120">Apply filters to a plan</span></span>](plan-filters.md)
