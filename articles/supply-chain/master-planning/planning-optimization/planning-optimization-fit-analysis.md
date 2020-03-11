---
title: تحليل ملاءمة تحسين التخطيط
description: يشرح هذا الموضوع كيفيه التحقق من صحة الاعداد والبيانات الحالية في مقابل قدرات وظيفة تحسين التخطيط.
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
ms.openlocfilehash: 25f3b39d0e6e88eb3f042ab93773e9724528ab0f
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076168"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="e5a8b-103">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="e5a8b-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5a8b-104">لمعرفه مدى توافق الاعداد والبيانات الحالية مع وظيفة تحسين التخطيط، انتقل إلى **التخطيط الرئيسي**\> **الإعداد** \>**تحليل ملائمة تحسين التخطيط**، ثم حدد **تشغيل التحليل**.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="e5a8b-105">إذا عثر التحليل علي إيه حالات عدم اتساق ، سيتم ادراجها في نفس الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="e5a8b-106">(قد تستغرق عمليه التحليل بضع دقائق ليتم تشغيلها.)</span><span class="sxs-lookup"><span data-stu-id="e5a8b-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="e5a8b-107">إذا تم العثور علي حالات عدم تناسق ، فلا يزال بإمكانك استخدام تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="e5a8b-108">تعرض نتائج تحليل الملائمة فقط الأماكن التي لا تقوم فيها خدمه التخطيط بالسماح بعمليه الاعداد الحالية.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="e5a8b-109">بمعني آخر ، تعرض الأماكن التي قد يتم فيها تجاهل بعض العمليات أو عدم اعتمادها.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="e5a8b-110">نتائج التحليل: مثال 1</span><span class="sxs-lookup"><span data-stu-id="e5a8b-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="e5a8b-111">**الميزة:** الإنتاج</span><span class="sxs-lookup"><span data-stu-id="e5a8b-111">**Feature:** Production</span></span>
- <span data-ttu-id="e5a8b-112">**المشكلة:** الأصناف التي بها مستوى قائمة مكونات أصناف أكبر من الصفر: 56</span><span class="sxs-lookup"><span data-stu-id="e5a8b-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="e5a8b-113">**التوضيح:** عثر التحليل الملائم على 56 عنصرًا يحتوي على إعداد قائمة مكونات الصنف (BOM) للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="e5a8b-114">ونظرا لان الإصدار الحالي من تحسين التخطيط لا يدعم الإنتاج ، سيقوم تحسين التخطيط بإنشاء أوامر شراء مخططه بدلا من أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="e5a8b-115">سيعرض أيضًا تحذيرًا يسرد العناصر المتأثره.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="e5a8b-116">نتائج التحليل: مثال 2</span><span class="sxs-lookup"><span data-stu-id="e5a8b-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="e5a8b-117">**الميزة:** الإجراءات</span><span class="sxs-lookup"><span data-stu-id="e5a8b-117">**Feature:** Actions</span></span>
- <span data-ttu-id="e5a8b-118">**المشكلة:** مجموعات التغطية مع تمكين حساب الإجراءات: 6</span><span class="sxs-lookup"><span data-stu-id="e5a8b-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="e5a8b-119">**التوضيح:** عثر تحليل الملائمة على ست مجموعات تغطيه حيث يتم تشغيل حساب الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="e5a8b-120">ونظرا لان الإصدار الحالي من تحسين التخطيط لا يدعم الإجراءات ، فلن يتم إنشاء إيه إجراءات اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="e5a8b-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e5a8b-121">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="e5a8b-121">Related resources</span></span>

[<span data-ttu-id="e5a8b-122">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="e5a8b-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e5a8b-123">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="e5a8b-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="e5a8b-124">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="e5a8b-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e5a8b-125">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="e5a8b-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e5a8b-126">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="e5a8b-126">Cancel a planning job</span></span>](cancel-planning-job.md)
