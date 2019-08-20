---
title: إهلاك العامل
description: توفر هذه المقالة نظرة عامة على أسلوب الإهلاك بالمعامل.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840519"
---
# <a name="factor-depreciation"></a><span data-ttu-id="2d183-103">إهلاك العامل</span><span class="sxs-lookup"><span data-stu-id="2d183-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d183-104">توفر هذه المقالة نظرة عامة على أسلوب الإهلاك بالمعامل.</span><span class="sxs-lookup"><span data-stu-id="2d183-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="2d183-105">العوامل هي النسب المئوية المُستخدمة في إهلاك الأصول.</span><span class="sxs-lookup"><span data-stu-id="2d183-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="2d183-106">فعند إعداد ملف تعريف إهلاك الأصل الثابت وتحديد **المعامل** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يمكنك إعداد إهلاك القسط الثابت أو التقدمي أو غير التقدمي.</span><span class="sxs-lookup"><span data-stu-id="2d183-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="2d183-107">إذا قمت بتحديد الإهلاك التقدمي، فسيزيد مبلغ الإهلاك مع كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="2d183-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="2d183-108">وفي الإهلاك غير التقدمي، سينخفض مبلغ الإهلاك لكل فترة بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="2d183-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="2d183-109">في إهلاك القسط الثابت، يكون الإهلاك نفس الشيء في كل فترة.</span><span class="sxs-lookup"><span data-stu-id="2d183-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="2d183-110">تشير القواعد والأمثلة أدناه إلى كيفية إعداد عوامل لكل نوع إهلاك.</span><span class="sxs-lookup"><span data-stu-id="2d183-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="2d183-111">عندما تحدد **المعامل** في حقل **الطريقة**، يتم عرض حقل **المعامل** وحقل **الفترة**.</span><span class="sxs-lookup"><span data-stu-id="2d183-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="2d183-112">الإهلاك المتتالي</span><span class="sxs-lookup"><span data-stu-id="2d183-112">Progressive depreciation</span></span>
<span data-ttu-id="2d183-113">القيمة في حقل **المعامل** أكبر من **50**.</span><span class="sxs-lookup"><span data-stu-id="2d183-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2d183-114">مثال</span><span class="sxs-lookup"><span data-stu-id="2d183-114">Example</span></span>

<span data-ttu-id="2d183-115">يساوي مبلغ الاستحواذ 100000، والمعامل هو 70، ومدة الخدمة 10 سنوات، ويبدأ الإهلاك في 1 يناير.</span><span class="sxs-lookup"><span data-stu-id="2d183-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2d183-116">ويتم عرض مبالغ الإهلاك ومبالغ القيم الدفترية الصافية فقط لست سنوات من مدة الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="2d183-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2d183-117">سنة</span><span class="sxs-lookup"><span data-stu-id="2d183-117">Year</span></span> | <span data-ttu-id="2d183-118">الفترة</span><span class="sxs-lookup"><span data-stu-id="2d183-118">Period</span></span>      | <span data-ttu-id="2d183-119">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="2d183-119">Depreciation amount</span></span> | <span data-ttu-id="2d183-120">مبلغ صافي القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="2d183-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2d183-121">1</span><span class="sxs-lookup"><span data-stu-id="2d183-121">1</span></span>    | <span data-ttu-id="2d183-122">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-122">December 31</span></span> | <span data-ttu-id="2d183-123">307.69</span><span class="sxs-lookup"><span data-stu-id="2d183-123">307.69</span></span>              | <span data-ttu-id="2d183-124">99692.31</span><span class="sxs-lookup"><span data-stu-id="2d183-124">99,692.31</span></span>             |
| <span data-ttu-id="2d183-125">2</span><span class="sxs-lookup"><span data-stu-id="2d183-125">2</span></span>    | <span data-ttu-id="2d183-126">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-126">December 31</span></span> | <span data-ttu-id="2d183-127">1447.21</span><span class="sxs-lookup"><span data-stu-id="2d183-127">1,447.21</span></span>            | <span data-ttu-id="2d183-128">98245.10</span><span class="sxs-lookup"><span data-stu-id="2d183-128">98,245.10</span></span>             |
| <span data-ttu-id="2d183-129">3</span><span class="sxs-lookup"><span data-stu-id="2d183-129">3</span></span>    | <span data-ttu-id="2d183-130">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-130">December 31</span></span> | <span data-ttu-id="2d183-131">3104.50</span><span class="sxs-lookup"><span data-stu-id="2d183-131">3,104.50</span></span>            | <span data-ttu-id="2d183-132">95140.60</span><span class="sxs-lookup"><span data-stu-id="2d183-132">95,140.60</span></span>             |
| <span data-ttu-id="2d183-133">4</span><span class="sxs-lookup"><span data-stu-id="2d183-133">4</span></span>    | <span data-ttu-id="2d183-134">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-134">December 31</span></span> | <span data-ttu-id="2d183-135">5150.21</span><span class="sxs-lookup"><span data-stu-id="2d183-135">5,150.21</span></span>            | <span data-ttu-id="2d183-136">89990.39</span><span class="sxs-lookup"><span data-stu-id="2d183-136">89,990.39</span></span>             |
| <span data-ttu-id="2d183-137">5</span><span class="sxs-lookup"><span data-stu-id="2d183-137">5</span></span>    | <span data-ttu-id="2d183-138">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-138">December 31</span></span> | <span data-ttu-id="2d183-139">7522.95</span><span class="sxs-lookup"><span data-stu-id="2d183-139">7,522.95</span></span>            | <span data-ttu-id="2d183-140">82467.44</span><span class="sxs-lookup"><span data-stu-id="2d183-140">82,467.44</span></span>             |
| <span data-ttu-id="2d183-141">6</span><span class="sxs-lookup"><span data-stu-id="2d183-141">6</span></span>    | <span data-ttu-id="2d183-142">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-142">December 31</span></span> | <span data-ttu-id="2d183-143">10184.06</span><span class="sxs-lookup"><span data-stu-id="2d183-143">10,184.06</span></span>           | <span data-ttu-id="2d183-144">72283.38</span><span class="sxs-lookup"><span data-stu-id="2d183-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="2d183-145">الإهلاك الاستطرادي</span><span class="sxs-lookup"><span data-stu-id="2d183-145">Digressive depreciation</span></span>
<span data-ttu-id="2d183-146">القيمة في حقل **المعامل** أقل من **50**.</span><span class="sxs-lookup"><span data-stu-id="2d183-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2d183-147">مثال</span><span class="sxs-lookup"><span data-stu-id="2d183-147">Example</span></span>

<span data-ttu-id="2d183-148">‏‫يساوي مبلغ الاستحواذ 100000، والمعامل هو 20، ومدة الخدمة 10 سنوات، ويبدأ الإهلاك في 1 يناير.</span><span class="sxs-lookup"><span data-stu-id="2d183-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2d183-149">ويتم عرض مبالغ الإهلاك ومبالغ القيم الدفترية الصافية فقط لست سنوات من مدة الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="2d183-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2d183-150">سنة</span><span class="sxs-lookup"><span data-stu-id="2d183-150">Year</span></span> | <span data-ttu-id="2d183-151">الفترة</span><span class="sxs-lookup"><span data-stu-id="2d183-151">Period</span></span>      | <span data-ttu-id="2d183-152">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="2d183-152">Depreciation amount</span></span> | <span data-ttu-id="2d183-153">مبلغ صافي القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="2d183-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2d183-154">1</span><span class="sxs-lookup"><span data-stu-id="2d183-154">1</span></span>    | <span data-ttu-id="2d183-155">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-155">December 31</span></span> | <span data-ttu-id="2d183-156">56080.43</span><span class="sxs-lookup"><span data-stu-id="2d183-156">56,080.43</span></span>           | <span data-ttu-id="2d183-157">43919.57</span><span class="sxs-lookup"><span data-stu-id="2d183-157">43,919.57</span></span>             |
| <span data-ttu-id="2d183-158">2</span><span class="sxs-lookup"><span data-stu-id="2d183-158">2</span></span>    | <span data-ttu-id="2d183-159">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-159">December 31</span></span> | <span data-ttu-id="2d183-160">10665.70</span><span class="sxs-lookup"><span data-stu-id="2d183-160">10,665.70</span></span>           | <span data-ttu-id="2d183-161">33253.87</span><span class="sxs-lookup"><span data-stu-id="2d183-161">33,253.87</span></span>             |
| <span data-ttu-id="2d183-162">3</span><span class="sxs-lookup"><span data-stu-id="2d183-162">3</span></span>    | <span data-ttu-id="2d183-163">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-163">December 31</span></span> | <span data-ttu-id="2d183-164">7156.22</span><span class="sxs-lookup"><span data-stu-id="2d183-164">7,156.22</span></span>            | <span data-ttu-id="2d183-165">26097.65</span><span class="sxs-lookup"><span data-stu-id="2d183-165">26,097.65</span></span>             |
| <span data-ttu-id="2d183-166">4</span><span class="sxs-lookup"><span data-stu-id="2d183-166">4</span></span>    | <span data-ttu-id="2d183-167">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-167">December 31</span></span> | <span data-ttu-id="2d183-168">5538.06</span><span class="sxs-lookup"><span data-stu-id="2d183-168">5,538.06</span></span>            | <span data-ttu-id="2d183-169">20559.59</span><span class="sxs-lookup"><span data-stu-id="2d183-169">20,559.59</span></span>             |
| <span data-ttu-id="2d183-170">5</span><span class="sxs-lookup"><span data-stu-id="2d183-170">5</span></span>    | <span data-ttu-id="2d183-171">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-171">December 31</span></span> | <span data-ttu-id="2d183-172">4579.89</span><span class="sxs-lookup"><span data-stu-id="2d183-172">4,579.89</span></span>            | <span data-ttu-id="2d183-173">15979.70</span><span class="sxs-lookup"><span data-stu-id="2d183-173">15,979.70</span></span>             |
| <span data-ttu-id="2d183-174">6</span><span class="sxs-lookup"><span data-stu-id="2d183-174">6</span></span>    | <span data-ttu-id="2d183-175">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="2d183-175">December 31</span></span> | <span data-ttu-id="2d183-176">3937.36</span><span class="sxs-lookup"><span data-stu-id="2d183-176">3,937.36</span></span>            | <span data-ttu-id="2d183-177">12042.34</span><span class="sxs-lookup"><span data-stu-id="2d183-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="2d183-178">إهلاك القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="2d183-178">Straight line depreciation</span></span>
<span data-ttu-id="2d183-179">القيمة في حقل **المعامل** تساوي **50**.</span><span class="sxs-lookup"><span data-stu-id="2d183-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="2d183-180">في هذه الحالة، يكون الإهلاك نفس الشيء في كل فترة، ويجب أن تأخذ في الاعتبار آثار القيم التي حددتها في حقول أخرى، كما هو موضح في [إهلاك مدة خدمة القسط الثابت‬](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="2d183-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



