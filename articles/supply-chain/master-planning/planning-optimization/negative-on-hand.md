---
title: التخطيط بالكميات الحالية السالبة
description: يوضح هذا الموضوع كيفية معالجة الكمية الحالية السالبة عند استخدام تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983456"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="23833-103">التخطيط بالكميات الحالية السالبة</span><span class="sxs-lookup"><span data-stu-id="23833-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23833-104">إذا أظهر النظام كمية حالية مجمعة سالبة، يتعامل مشغل التخطيط مع الكمية على القيمة 0 (صفر) للمساعدة على تجنب التوريد الزائد.</span><span class="sxs-lookup"><span data-stu-id="23833-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="23833-105">فيما يلي كيفية عمل هذه الوظيفة:</span><span class="sxs-lookup"><span data-stu-id="23833-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="23833-106">تعمل ميزة تحسين التخطيط على تجميع الكميات الفعلية بأقل مستوى من أبعاد التغطية.</span><span class="sxs-lookup"><span data-stu-id="23833-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="23833-107">(على سبيل المثال، إذا لم يقم *الموقع* بتغطية البُعد، يعمل تجميع تحسين التخطيط على تجميع كميات حالية على مستوى *المستودع*).</span><span class="sxs-lookup"><span data-stu-id="23833-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="23833-108">إذا كانت الكمية الفعلية المجمعة بأدنى مستوى من أبعاد التغطية سالبة، فإن النظام الذي يفترض أن الكمية الحالية هي 0 (صفر) بالفعل.</span><span class="sxs-lookup"><span data-stu-id="23833-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23833-109">يمكن أن يكون نظام التخطيط دقيقًا لبيانات الإدخال فقط.</span><span class="sxs-lookup"><span data-stu-id="23833-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="23833-110">إذا كانت بيانات الإدخال غير دقيقة، فستشير السجلات الحالية السالبة إلى أن معلومات المخزون في Microsoft Dynamics 365 Supply Chain Management تكون غير متزامنة مع العالم الحقيقي.</span><span class="sxs-lookup"><span data-stu-id="23833-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="23833-111">لذلك، ستكون نتيجة التخطيط خاطئة.</span><span class="sxs-lookup"><span data-stu-id="23833-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="23833-112">للحصول على نتيجة تخطيط دقيقة، فإنه ينبغي عليك تقليل عدد السجلات التي تعرض كمية حالية سالبة.</span><span class="sxs-lookup"><span data-stu-id="23833-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="23833-113">مثال1</span><span class="sxs-lookup"><span data-stu-id="23833-113">Example 1</span></span>

<span data-ttu-id="23833-114">يتم تكوين المستودع 13 بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="23833-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="23833-115">**كود التغطية:** الحد الأدنى/الحد الأقصى.</span><span class="sxs-lookup"><span data-stu-id="23833-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="23833-116">**الحد الأدنى:** 15 قطعة (أجهزة كمبيوتر)</span><span class="sxs-lookup"><span data-stu-id="23833-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="23833-117">**الحد الأقصى:** 25 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="23833-118">أقل مستوى من أبعاد التغطية هو *المستودع*، ويتم تسجيل الكميات الحالية التالية على مستوى *الموقع*:</span><span class="sxs-lookup"><span data-stu-id="23833-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="23833-119">**الموقع 1، المستودع 13، الموقع 1:** 20 من أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="23833-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="23833-120">**الموقع 1، المستودع 13، الموقع 2:** &minus;8 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="23833-121">وبالتالي، فإن الكمية الحالية التجميعية للمستودع 13 هي 12 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="23833-122">(= 20 من أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="23833-122">(= 20 pcs.</span></span> <span data-ttu-id="23833-123">&minus; 8 من أجهزة الكمبيوتر).</span><span class="sxs-lookup"><span data-stu-id="23833-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="23833-124">في هذه الحالة، يستخدم محرك التخطيط كمية التجميع الحالية التي تبلغ 12 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="23833-125">للمستودع 13.</span><span class="sxs-lookup"><span data-stu-id="23833-125">for warehouse 13.</span></span>

<span data-ttu-id="23833-126">تكون النتيجة هي الأمر المخطط الذي يبلغ 13 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="23833-127">(= 25 من أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="23833-127">(= 25 pcs.</span></span> <span data-ttu-id="23833-128">&minus; 12 جهاز من أجهزة الكمبيوتر.) لإعادة ملء المستودع 13 من 12 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="23833-129">إلى 25 من أجهزة كمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="23833-130">مثال2</span><span class="sxs-lookup"><span data-stu-id="23833-130">Example 2</span></span>

<span data-ttu-id="23833-131">يتم تكوين المستودع 13 بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="23833-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="23833-132">**كود التغطية:** الحد الأدنى/الحد الأقصى.</span><span class="sxs-lookup"><span data-stu-id="23833-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="23833-133">**الحد الأدنى** 15 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="23833-134">**الحد الأقصى:** 25 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="23833-135">أقل مستوى من أبعاد التغطية هو *المستودع*، ويتم تسجيل الكميات الحالية التالية على مستوى *الموقع*:</span><span class="sxs-lookup"><span data-stu-id="23833-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="23833-136">**الموقع 1، المستودع 13، الموقع 1:** 4 من أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="23833-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="23833-137">**الموقع 1، المستودع 13، الموقع 2:** &minus;8 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="23833-138">وبالتالي، فإن الكمية الحالية التجميعية للمستودع 13 &minus;4 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="23833-139">(= 4 من أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="23833-139">(= 4 pcs.</span></span> <span data-ttu-id="23833-140">&minus; 8 من أجهزة الكمبيوتر).</span><span class="sxs-lookup"><span data-stu-id="23833-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="23833-141">وبعبارة أخرى، إنها أقل من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="23833-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="23833-142">وفي هذه الحالة، يفترض مشغل التخطيط أن الكمية الحالية للمستودع 13 هي 0 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="23833-143">بدلاً من &minus;4 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="23833-144">تكون النتيجة هي الأمر المخطط الذي يبلغ 25 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="23833-145">(= 25 من أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="23833-145">(= 25 pcs.</span></span> <span data-ttu-id="23833-146">&minus; 0 جهاز من أجهزة الكمبيوتر.) لإعادة ملء المستودع 13 من 0 من أجهزة الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="23833-147">إلى 25 من أجهزة كمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="23833-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="23833-148">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="23833-148">Related resources</span></span>

[<span data-ttu-id="23833-149">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="23833-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="23833-150">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="23833-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="23833-151">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="23833-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="23833-152">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="23833-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="23833-153">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="23833-153">Cancel a planning job</span></span>](cancel-planning-job.md)
