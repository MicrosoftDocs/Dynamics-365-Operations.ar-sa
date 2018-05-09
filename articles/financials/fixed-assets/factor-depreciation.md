---
title: "إهلاك العامل"
description: "توفر هذه المقالة نظرة عامة على أسلوب الإهلاك بالمعامل."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d56386db5f1223dd03764d0f515aca6409f2c8a7
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="factor-depreciation"></a><span data-ttu-id="4762d-103">إهلاك العامل</span><span class="sxs-lookup"><span data-stu-id="4762d-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4762d-104">توفر هذه المقالة نظرة عامة على أسلوب الإهلاك بالمعامل.</span><span class="sxs-lookup"><span data-stu-id="4762d-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="4762d-105">العوامل هي النسب المئوية المُستخدمة في إهلاك الأصول.</span><span class="sxs-lookup"><span data-stu-id="4762d-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="4762d-106">فعند إعداد ملف تعريف إهلاك الأصل الثابت وتحديد **المعامل** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يمكنك إعداد إهلاك القسط الثابت أو التقدمي أو غير التقدمي.</span><span class="sxs-lookup"><span data-stu-id="4762d-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="4762d-107">إذا قمت بتحديد الإهلاك التقدمي، فسيزيد مبلغ الإهلاك مع كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="4762d-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="4762d-108">وفي الإهلاك غير التقدمي، سينخفض مبلغ الإهلاك لكل فترة بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="4762d-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="4762d-109">في إهلاك القسط الثابت، يكون الإهلاك نفس الشيء في كل فترة.</span><span class="sxs-lookup"><span data-stu-id="4762d-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="4762d-110">تشير القواعد والأمثلة أدناه إلى كيفية إعداد عوامل لكل نوع إهلاك.</span><span class="sxs-lookup"><span data-stu-id="4762d-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="4762d-111">عندما تحدد **المعامل** في حقل **الطريقة**، يتم عرض حقل **المعامل** وحقل **الفترة**.</span><span class="sxs-lookup"><span data-stu-id="4762d-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="4762d-112">الإهلاك المتتالي</span><span class="sxs-lookup"><span data-stu-id="4762d-112">Progressive depreciation</span></span>
<span data-ttu-id="4762d-113">القيمة في حقل **المعامل** أكبر من **50**.</span><span class="sxs-lookup"><span data-stu-id="4762d-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="4762d-114">مثال</span><span class="sxs-lookup"><span data-stu-id="4762d-114">Example</span></span>

<span data-ttu-id="4762d-115">يساوي مبلغ الاستحواذ 100000، والمعامل هو 70، ومدة الخدمة 10 سنوات، ويبدأ الإهلاك في 1 يناير.</span><span class="sxs-lookup"><span data-stu-id="4762d-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="4762d-116">ويتم عرض مبالغ الإهلاك ومبالغ القيم الدفترية الصافية فقط لست سنوات من مدة الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="4762d-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="4762d-117">سنة</span><span class="sxs-lookup"><span data-stu-id="4762d-117">Year</span></span> | <span data-ttu-id="4762d-118">الفترة</span><span class="sxs-lookup"><span data-stu-id="4762d-118">Period</span></span>      | <span data-ttu-id="4762d-119">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4762d-119">Depreciation amount</span></span> | <span data-ttu-id="4762d-120">مبلغ صافي القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="4762d-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="4762d-121">1</span><span class="sxs-lookup"><span data-stu-id="4762d-121">1</span></span>    | <span data-ttu-id="4762d-122">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-122">December 31</span></span> | <span data-ttu-id="4762d-123">307.69</span><span class="sxs-lookup"><span data-stu-id="4762d-123">307.69</span></span>              | <span data-ttu-id="4762d-124">99692.31</span><span class="sxs-lookup"><span data-stu-id="4762d-124">99,692.31</span></span>             |
| <span data-ttu-id="4762d-125">2</span><span class="sxs-lookup"><span data-stu-id="4762d-125">2</span></span>    | <span data-ttu-id="4762d-126">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-126">December 31</span></span> | <span data-ttu-id="4762d-127">1447.21</span><span class="sxs-lookup"><span data-stu-id="4762d-127">1,447.21</span></span>            | <span data-ttu-id="4762d-128">98245.10</span><span class="sxs-lookup"><span data-stu-id="4762d-128">98,245.10</span></span>             |
| <span data-ttu-id="4762d-129">3</span><span class="sxs-lookup"><span data-stu-id="4762d-129">3</span></span>    | <span data-ttu-id="4762d-130">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-130">December 31</span></span> | <span data-ttu-id="4762d-131">3104.50</span><span class="sxs-lookup"><span data-stu-id="4762d-131">3,104.50</span></span>            | <span data-ttu-id="4762d-132">95140.60</span><span class="sxs-lookup"><span data-stu-id="4762d-132">95,140.60</span></span>             |
| <span data-ttu-id="4762d-133">4</span><span class="sxs-lookup"><span data-stu-id="4762d-133">4</span></span>    | <span data-ttu-id="4762d-134">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-134">December 31</span></span> | <span data-ttu-id="4762d-135">5150.21</span><span class="sxs-lookup"><span data-stu-id="4762d-135">5,150.21</span></span>            | <span data-ttu-id="4762d-136">89990.39</span><span class="sxs-lookup"><span data-stu-id="4762d-136">89,990.39</span></span>             |
| <span data-ttu-id="4762d-137">5</span><span class="sxs-lookup"><span data-stu-id="4762d-137">5</span></span>    | <span data-ttu-id="4762d-138">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-138">December 31</span></span> | <span data-ttu-id="4762d-139">7522.95</span><span class="sxs-lookup"><span data-stu-id="4762d-139">7,522.95</span></span>            | <span data-ttu-id="4762d-140">82467.44</span><span class="sxs-lookup"><span data-stu-id="4762d-140">82,467.44</span></span>             |
| <span data-ttu-id="4762d-141">6</span><span class="sxs-lookup"><span data-stu-id="4762d-141">6</span></span>    | <span data-ttu-id="4762d-142">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-142">December 31</span></span> | <span data-ttu-id="4762d-143">10184.06</span><span class="sxs-lookup"><span data-stu-id="4762d-143">10,184.06</span></span>           | <span data-ttu-id="4762d-144">72283.38</span><span class="sxs-lookup"><span data-stu-id="4762d-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="4762d-145">الإهلاك الاستطرادي</span><span class="sxs-lookup"><span data-stu-id="4762d-145">Digressive depreciation</span></span>
<span data-ttu-id="4762d-146">القيمة في حقل **المعامل** أقل من **50**.</span><span class="sxs-lookup"><span data-stu-id="4762d-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="4762d-147">مثال</span><span class="sxs-lookup"><span data-stu-id="4762d-147">Example</span></span>

<span data-ttu-id="4762d-148">‏‫يساوي مبلغ الاستحواذ 100000، والمعامل هو 20، ومدة الخدمة 10 سنوات، ويبدأ الإهلاك في 1 يناير.</span><span class="sxs-lookup"><span data-stu-id="4762d-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="4762d-149">ويتم عرض مبالغ الإهلاك ومبالغ القيم الدفترية الصافية فقط لست سنوات من مدة الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="4762d-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="4762d-150">سنة</span><span class="sxs-lookup"><span data-stu-id="4762d-150">Year</span></span> | <span data-ttu-id="4762d-151">الفترة</span><span class="sxs-lookup"><span data-stu-id="4762d-151">Period</span></span>      | <span data-ttu-id="4762d-152">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="4762d-152">Depreciation amount</span></span> | <span data-ttu-id="4762d-153">مبلغ صافي القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="4762d-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="4762d-154">1</span><span class="sxs-lookup"><span data-stu-id="4762d-154">1</span></span>    | <span data-ttu-id="4762d-155">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-155">December 31</span></span> | <span data-ttu-id="4762d-156">56080.43</span><span class="sxs-lookup"><span data-stu-id="4762d-156">56,080.43</span></span>           | <span data-ttu-id="4762d-157">43919.57</span><span class="sxs-lookup"><span data-stu-id="4762d-157">43,919.57</span></span>             |
| <span data-ttu-id="4762d-158">2</span><span class="sxs-lookup"><span data-stu-id="4762d-158">2</span></span>    | <span data-ttu-id="4762d-159">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-159">December 31</span></span> | <span data-ttu-id="4762d-160">10665.70</span><span class="sxs-lookup"><span data-stu-id="4762d-160">10,665.70</span></span>           | <span data-ttu-id="4762d-161">33253.87</span><span class="sxs-lookup"><span data-stu-id="4762d-161">33,253.87</span></span>             |
| <span data-ttu-id="4762d-162">3</span><span class="sxs-lookup"><span data-stu-id="4762d-162">3</span></span>    | <span data-ttu-id="4762d-163">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-163">December 31</span></span> | <span data-ttu-id="4762d-164">7156.22</span><span class="sxs-lookup"><span data-stu-id="4762d-164">7,156.22</span></span>            | <span data-ttu-id="4762d-165">26097.65</span><span class="sxs-lookup"><span data-stu-id="4762d-165">26,097.65</span></span>             |
| <span data-ttu-id="4762d-166">4</span><span class="sxs-lookup"><span data-stu-id="4762d-166">4</span></span>    | <span data-ttu-id="4762d-167">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-167">December 31</span></span> | <span data-ttu-id="4762d-168">5538.06</span><span class="sxs-lookup"><span data-stu-id="4762d-168">5,538.06</span></span>            | <span data-ttu-id="4762d-169">20559.59</span><span class="sxs-lookup"><span data-stu-id="4762d-169">20,559.59</span></span>             |
| <span data-ttu-id="4762d-170">5</span><span class="sxs-lookup"><span data-stu-id="4762d-170">5</span></span>    | <span data-ttu-id="4762d-171">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-171">December 31</span></span> | <span data-ttu-id="4762d-172">4579.89</span><span class="sxs-lookup"><span data-stu-id="4762d-172">4,579.89</span></span>            | <span data-ttu-id="4762d-173">15979.70</span><span class="sxs-lookup"><span data-stu-id="4762d-173">15,979.70</span></span>             |
| <span data-ttu-id="4762d-174">6</span><span class="sxs-lookup"><span data-stu-id="4762d-174">6</span></span>    | <span data-ttu-id="4762d-175">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="4762d-175">December 31</span></span> | <span data-ttu-id="4762d-176">3937.36</span><span class="sxs-lookup"><span data-stu-id="4762d-176">3,937.36</span></span>            | <span data-ttu-id="4762d-177">12042.34</span><span class="sxs-lookup"><span data-stu-id="4762d-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="4762d-178">إهلاك القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="4762d-178">Straight line depreciation</span></span>
<span data-ttu-id="4762d-179">القيمة في حقل **المعامل** تساوي **50**.</span><span class="sxs-lookup"><span data-stu-id="4762d-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="4762d-180">في هذه الحالة، يكون الإهلاك نفس الشيء في كل فترة، ويجب أن تأخذ في الاعتبار آثار القيم التي حددتها في حقول أخرى، كما هو موضح في [إهلاك مدة خدمة القسط الثابت‬](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="4762d-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




