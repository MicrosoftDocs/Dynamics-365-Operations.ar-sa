---
title: "إهلاك الرصيد المتناقص بنسبة 150 بالمائة"
description: "تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 150 بالمائة‬."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 20572163bd32d059323cbb80e606ae344d70b7be
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="09d45-103">إهلاك الرصيد المتناقص بنسبة 150 بالمائة</span><span class="sxs-lookup"><span data-stu-id="09d45-103">150 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="09d45-104">تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 150 بالمائة‬.</span><span class="sxs-lookup"><span data-stu-id="09d45-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="09d45-105">عند إعداد ملف تعريف إهلاك أصول ثابتة وتحديد **الرصيد المتناقص بنسبة 150%** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يتم إهلاك الأصول الثابتة التي تم تعيين ملف تعريف الإهلاك لها بنفس النسبة المئوية في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="09d45-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="09d45-106">حيث يتم حساب هذه النسبة المئوية بناءً على مدة الخدمة للأصل.</span><span class="sxs-lookup"><span data-stu-id="09d45-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="09d45-107">على سبيل المثال، إذا كانت مدة خدمة الأصل خمس سنوات، فإنه يتم حساب النسبة المئوية بنسبة 30% (150% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="09d45-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="09d45-108">ولإعداد إهلاك الرصيد المتناقص بنسبة 150%، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="09d45-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="09d45-109">وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة المحددة في حقل **سنة الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="09d45-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="09d45-110">حدد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="09d45-110">Selection of depreciation year</span></span>
<span data-ttu-id="09d45-111">ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="09d45-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="09d45-112">القيمة الافتراضية هي **تقويم**.</span><span class="sxs-lookup"><span data-stu-id="09d45-112">The default value is **Calendar**.</span></span> <span data-ttu-id="09d45-113">ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="09d45-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="09d45-114">ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="09d45-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="09d45-115">التقويم</span><span class="sxs-lookup"><span data-stu-id="09d45-115">Calendar</span></span>

<span data-ttu-id="09d45-116">يمكنك اختيار الاحتفاظ بالقيمة الافتراضية في حقل **سنة الإهلاك**، **التقويم**.</span><span class="sxs-lookup"><span data-stu-id="09d45-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="09d45-117">ويقوم خيار **التقويم** بتحديث أساس الإهلاك في 1 كانون الثاني/يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="09d45-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="09d45-118">وبشكل عام، يعتبر أساس الإهلاك صافي القيمة الدفترية ناقص قيمة الخردة.</span><span class="sxs-lookup"><span data-stu-id="09d45-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="09d45-119">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب.</span><span class="sxs-lookup"><span data-stu-id="09d45-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="09d45-120">وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="09d45-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="09d45-121">**السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="09d45-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="09d45-122">**شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="09d45-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="09d45-123">**ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="09d45-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="09d45-124">**نصف سنوي** ترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="09d45-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="09d45-125">**يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="09d45-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="09d45-126">مالي</span><span class="sxs-lookup"><span data-stu-id="09d45-126">Fiscal</span></span>

<span data-ttu-id="09d45-127">إذا قمت بتحديد **مالية** في حقل **سنة الإهلاك**، يتم حساب إهلاك الرصيد المتناقص بنسبة 150% بحسب السنة المالية للتقويم المالي المحدد للدفتر، أو للتقويم المالي المحدد في صفحة **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="09d45-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="09d45-128">ويتم إعداد التقويمات المالية في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="09d45-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="09d45-129">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="09d45-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="09d45-130">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="09d45-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="09d45-131">وتتم تسوية الإهلاك لكل فترة.</span><span class="sxs-lookup"><span data-stu-id="09d45-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="09d45-132">ويتم تحديد طول السنة المالية التالية بإعداد الفترات في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="09d45-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="09d45-133">وإذا قمت بتحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="09d45-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="09d45-134">**سنوي** ترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="09d45-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="09d45-135">تقوم **الفترة المالية** بترحيل المبلغ الإجمالي للإهلاك للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="09d45-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="09d45-136">ويُستحق هذا المبلغ في الفترات المالية التي يتم تحديدها في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="09d45-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="09d45-137">مثال على إهلاك القسط المتناقص بسبة 150 في المائة</span><span class="sxs-lookup"><span data-stu-id="09d45-137">Example of 150% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="09d45-138">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="09d45-138">Acquisition cost</span></span>               | <span data-ttu-id="09d45-139">11,000</span><span class="sxs-lookup"><span data-stu-id="09d45-139">11,000</span></span> |
| <span data-ttu-id="09d45-140">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="09d45-140">Salvage value</span></span>                  | <span data-ttu-id="09d45-141">1,000</span><span class="sxs-lookup"><span data-stu-id="09d45-141">1,000</span></span>  |
| <span data-ttu-id="09d45-142">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="09d45-142">Depreciation base</span></span>              | <span data-ttu-id="09d45-143">10,000</span><span class="sxs-lookup"><span data-stu-id="09d45-143">10,000</span></span> |
| <span data-ttu-id="09d45-144">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="09d45-144">Service life years</span></span>             | <span data-ttu-id="09d45-145">5</span><span class="sxs-lookup"><span data-stu-id="09d45-145">5</span></span>      |
| <span data-ttu-id="09d45-146">النسبة المئوية للإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="09d45-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="09d45-147">30%</span><span class="sxs-lookup"><span data-stu-id="09d45-147">30%</span></span>    |

<span data-ttu-id="09d45-148">تقسم طريقة الرصيد المتناقص بنسبة 150 بالمائة على سنوات مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="09d45-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="09d45-149">وسيتم ضرب النسبة المئوية في صافي القيمة الدفترية للأصل لتحديد مبلغ الإهلاك في السنة.</span><span class="sxs-lookup"><span data-stu-id="09d45-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="09d45-150">الفترة</span><span class="sxs-lookup"><span data-stu-id="09d45-150">Period</span></span> | <span data-ttu-id="09d45-151">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="09d45-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="09d45-152">القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="09d45-152">Book value</span></span>             | <span data-ttu-id="09d45-153">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="09d45-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="09d45-154">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="09d45-154">Year 1</span></span> | <span data-ttu-id="09d45-155">(11,000 – 1,000) × 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="09d45-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="09d45-156">11,000 – 3,000 = 8,000</span><span class="sxs-lookup"><span data-stu-id="09d45-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="09d45-157">11,000 – 1,000 – 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="09d45-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="09d45-158">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="09d45-158">Year 2</span></span> | <span data-ttu-id="09d45-159">7,000 × 30% = 2,100</span><span class="sxs-lookup"><span data-stu-id="09d45-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="09d45-160">8,000 – 2,100 = 5,900</span><span class="sxs-lookup"><span data-stu-id="09d45-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="09d45-161">7,000 – 2,100 = 4,900</span><span class="sxs-lookup"><span data-stu-id="09d45-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="09d45-162">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="09d45-162">Year 3</span></span> | <span data-ttu-id="09d45-163">4,900 × 30% = 1,470</span><span class="sxs-lookup"><span data-stu-id="09d45-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="09d45-164">5,900 – 1,470 = 4,430</span><span class="sxs-lookup"><span data-stu-id="09d45-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="09d45-165">4,900 – 1,470 = 3,430</span><span class="sxs-lookup"><span data-stu-id="09d45-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="09d45-166">بشكل عام، عندما يصبح المبلغ الذي يتم حسابه باستخدام طريقة الإهلاك المتناقص بنسبة 150% أقل من المبلغ الذي يُحسب باستخدام طريقة القسط الثابت، يكون هناك تحويل لطريقة القسط الثابت للمدة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="09d45-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




