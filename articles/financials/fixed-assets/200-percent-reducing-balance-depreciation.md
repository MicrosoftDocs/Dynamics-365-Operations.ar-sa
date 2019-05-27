---
title: إهلاك الرصيد المتناقص بنسبة 200 بالمائة
description: تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 200 بالمائة‬.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec51f9e12e31e81c56fab9e82d0fc18d45beb5e6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569303"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="acee1-103">إهلاك الرصيد المتناقص بنسبة 200 بالمائة</span><span class="sxs-lookup"><span data-stu-id="acee1-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acee1-104">تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 200 بالمائة‬.</span><span class="sxs-lookup"><span data-stu-id="acee1-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="acee1-105">عند إعداد ملف تعريف إهلاك أصول ثابتة وتحديد **الرصيد المتناقص بنسبة 200%** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يتم إهلاك الأصول الثابتة التي تم تعيين ملف تعريف الإهلاك لها بنفس النسبة المئوية في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="acee1-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="acee1-106">حيث يتم حساب هذه النسبة المئوية بناءً على مدة الخدمة للأصل.</span><span class="sxs-lookup"><span data-stu-id="acee1-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="acee1-107">على سبيل المثال، إذا كانت مدة خدمة الأصل خمس سنوات، فإنه يتم حساب النسبة المئوية بنسبة 40% (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="acee1-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="acee1-108">تعرف هذه الطريقة أيضًا بالرصيد المتناقض المزدوج.</span><span class="sxs-lookup"><span data-stu-id="acee1-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="acee1-109">ولإعداد إهلاك الرصيد المتناقص بنسبة 200%، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="acee1-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="acee1-110">وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة التي تحددها في حقل **سنة الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="acee1-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="acee1-111">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="acee1-111">Select a depreciation year</span></span>
<span data-ttu-id="acee1-112">ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="acee1-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="acee1-113">القيمة الافتراضية هي **تقويم**.</span><span class="sxs-lookup"><span data-stu-id="acee1-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="acee1-114">ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="acee1-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="acee1-115">ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="acee1-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="acee1-116">التقويم</span><span class="sxs-lookup"><span data-stu-id="acee1-116">Calendar</span></span>

<span data-ttu-id="acee1-117">يمكنك اختيار الاحتفاظ بالقيمة الافتراضية في حقل **سنة الإهلاك**، **التقويم**.</span><span class="sxs-lookup"><span data-stu-id="acee1-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="acee1-118">ويقوم خيار **التقويم** بتحديث أساس الإهلاك في 1 كانون الثاني/يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="acee1-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="acee1-119">بشكل عام، يعتبر الإهلاك صافي القيمة الدفترية ناقص قيمة الخردة.</span><span class="sxs-lookup"><span data-stu-id="acee1-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="acee1-120">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب.</span><span class="sxs-lookup"><span data-stu-id="acee1-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="acee1-121">وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="acee1-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="acee1-122">**السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="acee1-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="acee1-123">**شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="acee1-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="acee1-124">**ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="acee1-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="acee1-125">**نصف سنوي** ترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="acee1-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="acee1-126">**يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="acee1-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="acee1-127">مالي</span><span class="sxs-lookup"><span data-stu-id="acee1-127">Fiscal</span></span>

<span data-ttu-id="acee1-128">إذا قمت بتحديد **مالية** في حقل سنة **الإهلاك**، يتم حساب إهلاك الرصيد المتناقص بنسبة 200% بحسب السنة المالية للتقويم المالي المحدد للدفتر، أو للتقويم المالي المحدد في صفحة **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="acee1-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="acee1-129">ويتم إعداد التقويمات المالية في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="acee1-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="acee1-130">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="acee1-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="acee1-131">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="acee1-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="acee1-132">وتتم تسوية الإهلاك لكل فترة.</span><span class="sxs-lookup"><span data-stu-id="acee1-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="acee1-133">ويتم تحديد طول السنة المالية التالية بإعداد الفترات في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="acee1-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="acee1-134">وعند تحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="acee1-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="acee1-135">يقوم الخيار **سنوي** بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="acee1-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="acee1-136">تقوم **الفترة المالية** بترحيل المبلغ الإجمالي للإهلاك للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="acee1-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="acee1-137">ويُستحق هذا المبلغ في الفترات المالية التي يتم تحديدها في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="acee1-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="acee1-138">مثال لإهلاك الرصيد المتناقص بنسبة 200%</span><span class="sxs-lookup"><span data-stu-id="acee1-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="acee1-139">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="acee1-139">Acquisition cost</span></span>               | <span data-ttu-id="acee1-140">11,000</span><span class="sxs-lookup"><span data-stu-id="acee1-140">11,000</span></span> |
| <span data-ttu-id="acee1-141">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="acee1-141">Salvage value</span></span>                  | <span data-ttu-id="acee1-142">1, 000</span><span class="sxs-lookup"><span data-stu-id="acee1-142">1, 000</span></span> |
| <span data-ttu-id="acee1-143">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="acee1-143">Depreciation base</span></span>              | <span data-ttu-id="acee1-144">10,000</span><span class="sxs-lookup"><span data-stu-id="acee1-144">10,000</span></span> |
| <span data-ttu-id="acee1-145">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="acee1-145">Service life years</span></span>             | <span data-ttu-id="acee1-146">5</span><span class="sxs-lookup"><span data-stu-id="acee1-146">5</span></span>      |
| <span data-ttu-id="acee1-147">النسبة المئوية للإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="acee1-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="acee1-148">40%</span><span class="sxs-lookup"><span data-stu-id="acee1-148">40%</span></span>    |

<span data-ttu-id="acee1-149">تقسم طريقة الرصيد المتناقص بنسبة 200% هذه النسبة على سنوات مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="acee1-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="acee1-150">وسيتم ضرب النسبة المئوية في صافي القيمة الدفترية للأصل لتحديد مبلغ الإهلاك في السنة.</span><span class="sxs-lookup"><span data-stu-id="acee1-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="acee1-151">الفترة</span><span class="sxs-lookup"><span data-stu-id="acee1-151">Period</span></span> | <span data-ttu-id="acee1-152">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="acee1-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="acee1-153">القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="acee1-153">Book value</span></span>             | <span data-ttu-id="acee1-154">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="acee1-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="acee1-155">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="acee1-155">Year 1</span></span> | <span data-ttu-id="acee1-156">(11,000 – 1,000) × 40% = 4,000</span><span class="sxs-lookup"><span data-stu-id="acee1-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="acee1-157">11,000 – 4,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="acee1-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="acee1-158">11,000 – 1,000 – 4,000 = 6,000</span><span class="sxs-lookup"><span data-stu-id="acee1-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="acee1-159">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="acee1-159">Year 2</span></span> | <span data-ttu-id="acee1-160">6,000 × 40% = 2,400</span><span class="sxs-lookup"><span data-stu-id="acee1-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="acee1-161">7,000 – 2,400 = 4,600</span><span class="sxs-lookup"><span data-stu-id="acee1-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="acee1-162">6,000 – 2,400 = 3,600</span><span class="sxs-lookup"><span data-stu-id="acee1-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="acee1-163">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="acee1-163">Year 3</span></span> | <span data-ttu-id="acee1-164">3,600 × 40% = 1,440</span><span class="sxs-lookup"><span data-stu-id="acee1-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="acee1-165">4,600 – 1,440 = 3,160</span><span class="sxs-lookup"><span data-stu-id="acee1-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="acee1-166">3,600 – 1,440 = 2,160</span><span class="sxs-lookup"><span data-stu-id="acee1-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="acee1-167">بشكل عام، عندما يصبح المبلغ الذي يتم حسابه باستخدام طريقة الإهلاك المتناقص بنسبة 200% أقل من المبلغ الذي يُحسب باستخدام طريقة القسط الثابت، يكون هناك تحويل لطريقة القسط الثابت للمدة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="acee1-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



