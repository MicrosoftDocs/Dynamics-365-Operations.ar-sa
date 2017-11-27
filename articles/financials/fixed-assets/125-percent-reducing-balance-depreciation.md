---
title: "إهلاك الرصيد المتناقص بنسبة 125 بالمائة"
description: "تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 125 بالمائة‬."
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
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="29730-103">إهلاك الرصيد المتناقص بنسبة 125 بالمائة</span><span class="sxs-lookup"><span data-stu-id="29730-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="29730-104">تقدم هذه المقالة نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 125 بالمائة‬.</span><span class="sxs-lookup"><span data-stu-id="29730-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="29730-105">عند إعداد ملف تعريف إهلاك أصول ثابتة وتحديد **الرصيد المتناقص بنسبة 125%** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يتم إهلاك الأصول الثابتة التي تم تعيين ملف تعريف الإهلاك لها بنفس النسبة المئوية في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="29730-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="29730-106">حيث يتم حساب هذه النسبة المئوية بناءً على مدة الخدمة للأصل.</span><span class="sxs-lookup"><span data-stu-id="29730-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="29730-107">على سبيل المثال، إذا كانت مدة خدمة الأصل خمس سنوات، فإنه يتم حساب النسبة المئوية بنسبة 25% (125% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="29730-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="29730-108">ولإعداد إهلاك الرصيد المتناقص بنسبة 125%، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="29730-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="29730-109">وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة المحددة في حقل **سنة الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="29730-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="29730-110">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="29730-110">Select a depreciation year</span></span>
<span data-ttu-id="29730-111">ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="29730-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="29730-112">القيمة الافتراضية هي **تقويم**.</span><span class="sxs-lookup"><span data-stu-id="29730-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="29730-113">ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="29730-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="29730-114">ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="29730-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="29730-115">التقويم</span><span class="sxs-lookup"><span data-stu-id="29730-115">Calendar</span></span>

<span data-ttu-id="29730-116">يمكنك اختيار الاحتفاظ بالقيمة الافتراضية في حقل **سنة الإهلاك**، **التقويم**.</span><span class="sxs-lookup"><span data-stu-id="29730-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="29730-117">ويقوم خيار **التقويم** بتحديث أساس الإهلاك في 1 كانون الثاني/يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="29730-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="29730-118">وبشكل عام، يعتبر أساس الإهلاك صافي القيمة الدفترية ناقص قيمة الخردة.</span><span class="sxs-lookup"><span data-stu-id="29730-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="29730-119">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب.</span><span class="sxs-lookup"><span data-stu-id="29730-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="29730-120">وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="29730-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="29730-121">**السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="29730-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="29730-122">**شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="29730-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="29730-123">**ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="29730-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="29730-124">**نصف سنوي** ترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="29730-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="29730-125">**يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="29730-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="29730-126">مالي</span><span class="sxs-lookup"><span data-stu-id="29730-126">Fiscal</span></span>

<span data-ttu-id="29730-127">إذا قمت بتحديد **مالية** في حقل **سنة الإهلاك**، يتم حساب الإهلاك المتناقص بنسبة 125% بحسب السنة المالية للتقويم المالي المحدد للدفتر، أو للتقويم المالي المحدد في صفحة **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="29730-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="29730-128">ويتم إعداد التقويمات المالية في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="29730-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="29730-129">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="29730-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="29730-130">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="29730-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="29730-131">وتتم تسوية الإهلاك تلقائيًا لكل فترة، ويتم تحديد طول السنة المالية التالية بواسطة إعداد الفترات في صفحة **القوائم المالية**.</span><span class="sxs-lookup"><span data-stu-id="29730-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="29730-132">وإذا قمت بتحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="29730-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="29730-133">يقوم الخيار **سنوي** بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="29730-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="29730-134">تقوم **الفترة المالية** بترحيل المبلغ الإجمالي للإهلاك للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="29730-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="29730-135">ويُستحق هذا المبلغ في الفترات المالية التي يتم تحديدها في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="29730-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="29730-136">مثال لإهلاك الرصيد المتناقص بنسبة 125%</span><span class="sxs-lookup"><span data-stu-id="29730-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="29730-137">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="29730-137">Acquisition cost</span></span>               | <span data-ttu-id="29730-138">11,000</span><span class="sxs-lookup"><span data-stu-id="29730-138">11,000</span></span> |
| <span data-ttu-id="29730-139">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="29730-139">Salvage value</span></span>                  | <span data-ttu-id="29730-140">1,000</span><span class="sxs-lookup"><span data-stu-id="29730-140">1,000</span></span>  |
| <span data-ttu-id="29730-141">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="29730-141">Depreciation base</span></span>              | <span data-ttu-id="29730-142">10,000</span><span class="sxs-lookup"><span data-stu-id="29730-142">10,000</span></span> |
| <span data-ttu-id="29730-143">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="29730-143">Service life years</span></span>             | <span data-ttu-id="29730-144">5</span><span class="sxs-lookup"><span data-stu-id="29730-144">5</span></span>      |
| <span data-ttu-id="29730-145">النسبة المئوية للإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="29730-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="29730-146">25%</span><span class="sxs-lookup"><span data-stu-id="29730-146">25%</span></span>    |

<span data-ttu-id="29730-147">تقسم طريقة الرصيد المتناقص بنسبة 125% على سنوات مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="29730-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="29730-148">وسيتم ضرب النسبة المئوية في صافي القيمة الدفترية للأصل لتحديد مبلغ الإهلاك في السنة.</span><span class="sxs-lookup"><span data-stu-id="29730-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="29730-149">الفترة</span><span class="sxs-lookup"><span data-stu-id="29730-149">Period</span></span> | <span data-ttu-id="29730-150">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="29730-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="29730-151">القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="29730-151">Book value</span></span>                    | <span data-ttu-id="29730-152">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="29730-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="29730-153">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="29730-153">Year 1</span></span> | <span data-ttu-id="29730-154">(11,000 – 1,000) × 25% = 2,500</span><span class="sxs-lookup"><span data-stu-id="29730-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="29730-155">(11,000 – 2,500) = 8,500</span><span class="sxs-lookup"><span data-stu-id="29730-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="29730-156">(11,000 – 1,000 – 2,500) = 7,500</span><span class="sxs-lookup"><span data-stu-id="29730-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="29730-157">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="29730-157">Year 2</span></span> | <span data-ttu-id="29730-158">7,500 × 25% = 1,875</span><span class="sxs-lookup"><span data-stu-id="29730-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="29730-159">(8,500 – 1,875) = 6,625</span><span class="sxs-lookup"><span data-stu-id="29730-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="29730-160">(7,500 – 1,875) = 5,625</span><span class="sxs-lookup"><span data-stu-id="29730-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="29730-161">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="29730-161">Year 3</span></span> | <span data-ttu-id="29730-162">5,625 × 25% = 1,406.25</span><span class="sxs-lookup"><span data-stu-id="29730-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="29730-163">(6,625 – 1,406.25) = 5,218.75</span><span class="sxs-lookup"><span data-stu-id="29730-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="29730-164">(5,625 – 1,406.25) = 4,218.75</span><span class="sxs-lookup"><span data-stu-id="29730-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="29730-165">بشكل عام، عندما يصبح المبلغ الذي يتم حسابه باستخدام طريقة الإهلاك المتناقص بنسبة 125% أقل من المبلغ الذي يُحسب باستخدام طريقة القسط الثابت، يكون هناك تحويل لطريقة القسط الثابت للمدة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="29730-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




