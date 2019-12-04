---
title: تطبيق عوامل تصفية على خطة
description: يشرح هذا الموضوع كيفية استخدام عوامل التصفية في خطة عند استخدام وظيفة "تحسين التخطيط".
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
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
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773895"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="b5ac6-103">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="b5ac6-103">Apply filters to a plan</span></span>

<span data-ttu-id="b5ac6-104">عند استخدام وظيفة تحسين التخطيط ، يمكنك تطبيق عامل تصفيه علي أحدي الخطط.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="b5ac6-105">سيتم دائما تطبيق عامل تصفيه الخطة اثناء تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="b5ac6-106">يكون عامل تصفيه الخطة مفيدا عندما تريد تحديد الخطة لمجموعه معينه من الأصناف والتاكد من عدم تضمين إيه أصناف أخرى كجزء من التخطيط الرئيسي الناتج.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="b5ac6-107">في حاله تطبيق عامل تصفيه الخطة ، وتطبيق عامل تصفيه وقت التشغيل أيضا اثناء تشغيل التخطيط الرئيسي ، يتم تضمين تقاطع عاملي التصفية في تشغيل التخطيط.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b5ac6-108">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="b5ac6-108">Example scenario</span></span>

<span data-ttu-id="b5ac6-109">يتم إعداد مرشح الخطة الذي يتضمن العناصر A و B و C. ثم يتم تشغيل عمليات التخطيط الرئيسية لنفس الخطة ، ولكن يتم تطبيق عوامل تصفية مختلفة لوقت التشغيل:</span><span class="sxs-lookup"><span data-stu-id="b5ac6-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="b5ac6-110">**عامل تصفيه وقت التشغيل الذي يتضمن العنصر D:** لا يتم تخطيط إيه أصناف لأنه لا يوجد تقاطع بين عامل تصفيه الخطة وعامل تصفيه وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="b5ac6-111">**عامل تصفيه وقت التشغيل الذي يتضمن العنصر A وD:** فقط يتم تضمين الصنف A في تشغيل التخطيط ، نظرا لان الصنف D ليس جزءا من عامل تصفيه الخطة.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="b5ac6-112">**عامل تصفيه وقت التشغيل الذي يتضمن العنصر B:** يتم تضمين العنصر B فقط في تشغيل التخطيط ، ويتم الاحتفاظ بإخراج التخطيط السابق للعنصر A.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="b5ac6-113">**عامل التصفية وقت التشغيل الذي يتضمن كافة الأصناف (عامل التصفية الفارغ):** يتم تضمين الأصناف A و B و C في تشغيل التخطيط ، وتتم الكتابة فوق الإخراج السابق للتخطيط الخاص بالأصناف A و B.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="b5ac6-114">وينبغي تجنب اعداد عامل تصفيه الخطة علي الخطة المحددة كـ **خطة رئيسيه ديناميكية حاليه** في صفحه **معلمات التخطيط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="b5ac6-115">وبخلاف ذلك ، سيتم تحديد وظيفة الخطة الرئيسية الديناميكية للأصناف التي تمت تصفيتها.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="b5ac6-116">علي سبيل المثال ، إذا تم تحديث صافي المتطلبات لصنف ليس جزءا من عامل تصفيه الخطة ، فلن يتم إنشاء إيه نتيجة.</span><span class="sxs-lookup"><span data-stu-id="b5ac6-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b5ac6-117">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="b5ac6-117">Related resources</span></span>

[<span data-ttu-id="b5ac6-118">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="b5ac6-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="b5ac6-119">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="b5ac6-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="b5ac6-120">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="b5ac6-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b5ac6-121">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="b5ac6-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b5ac6-122">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="b5ac6-122">Cancel a planning job</span></span>](cancel-planning-job.md)
