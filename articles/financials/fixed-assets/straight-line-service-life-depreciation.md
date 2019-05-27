---
title: إهلاك مدة خدمة القسط الثابت
description: تقدم هذه المقالة نظرة عامة على أسلوب إهلاك مدة خدمة القسط الثابت‬.
author: ShylaThompson
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b48cf3970379f8dd2ea529cd8a434c0bdc196a1e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560798"
---
# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="33ce3-103">إهلاك مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="33ce3-103">Straight line service life depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33ce3-104">تقدم هذه المقالة نظرة عامة على أسلوب إهلاك مدة خدمة القسط الثابت‬.</span><span class="sxs-lookup"><span data-stu-id="33ce3-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="33ce3-105">عند إعداد ملف تعريف إهلاك أصل ثابت وتحديد عمر خدمة القسط الثابت‬ في حقل الطريقة في صفحة ملفات تعريف الإهلاك، يتم إهلاك الأصول التي تم تعيين ملف تعريف الإهلاك هذا لها على أساس إجمالي عمر خدمة الأصل.</span><span class="sxs-lookup"><span data-stu-id="33ce3-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="33ce3-106">وهو يُمثل بصفة عامة مبلغ الإهلاك في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="33ce3-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="33ce3-107">ويكمن الاختلاف في مبلغ الإهلاك المحسوب بين المدة المتبقية لخدمة قسط ثابت ومدة خدمة القسط الثابت عند ترحيل تسوية إلى الأصل.</span><span class="sxs-lookup"><span data-stu-id="33ce3-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="33ce3-108">ولإعداد إهلاك عمر خدمة القسط الثابت‬، يجب عليك أيضًا تحديد الخيارات في حقلي سنة الإهلاك وحقل تكرار الفترة في صفحة ملفات تعريف الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="33ce3-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="33ce3-109">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="33ce3-109">Select a depreciation year</span></span>
<span data-ttu-id="33ce3-110">يمكنك تحديد "تقويم" أو "مالي" في حقل سنة الإهلاك في صفحة ملفات تعريف الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="33ce3-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="33ce3-111">ويعمل هذا التحديد على تحديد الخيارات المتوفرة في حقل تكرار الفترة.</span><span class="sxs-lookup"><span data-stu-id="33ce3-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="33ce3-112">والخيار الافتراضي هو "تقويم".</span><span class="sxs-lookup"><span data-stu-id="33ce3-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="33ce3-113">التقويم</span><span class="sxs-lookup"><span data-stu-id="33ce3-113">Calendar</span></span>

<span data-ttu-id="33ce3-114">عندما تقوم بتحديد تقويم، يتم افتراض سنة من 1 يناير حتى 31 ديسمبر، حتى إذا كنت قد قمت بتحديد التقويم المالي بشكل مختلف.</span><span class="sxs-lookup"><span data-stu-id="33ce3-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="33ce3-115">يقوم خيار التقويم بتحديث أساس الإهلاك، الذي عادةً ما يكون صافي القيمة الدفترية ناقص القيمة الباقية، في 1 يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="33ce3-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="33ce3-116">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب.</span><span class="sxs-lookup"><span data-stu-id="33ce3-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="33ce3-117">في حالة قيامك بتحديد "تقويم"، تتوفر الخيارات التالية في حقل "تكرار الفترة"، الذي يحدد التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم:</span><span class="sxs-lookup"><span data-stu-id="33ce3-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="33ce3-118">السنوي ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="33ce3-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="33ce3-119">شهري ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="33ce3-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="33ce3-120">ربع سنوي مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="33ce3-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="33ce3-121">نصف سنوي ترحيل المبلغ نصف السنوي في نهاية كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="33ce3-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="33ce3-122">يقوم خيار الترحيل اليومي بترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="33ce3-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="33ce3-123">على سبيل المثال، إذا قمت بتحديد "سنوي"، يتم ترحيل الإهلاك السنوي مرة واحدة فقط في 31 ديسمبر من كل عام.</span><span class="sxs-lookup"><span data-stu-id="33ce3-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="33ce3-124">أما إذا حددت "شهري"، فإنه يتم ترحيل الإهلاك الشهري في كل شهر بمعدل 1/12 من قيمة المبلغ الإجمالي السنوي.</span><span class="sxs-lookup"><span data-stu-id="33ce3-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="33ce3-125">مالي</span><span class="sxs-lookup"><span data-stu-id="33ce3-125">Fiscal</span></span>

<span data-ttu-id="33ce3-126">في حالة تحديد مالي في حقل سنة الإهلاك، فإنه يتم استخدام إهلاك عمر خدمة القسط الثابت‬.</span><span class="sxs-lookup"><span data-stu-id="33ce3-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="33ce3-127">ويتم حسابه بالاستناد إلى السنة المالية، التي يتم تحديدها بالتقويم المالي المحدد للدفتر أو التقويم المالي المحدد في صفحة دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="33ce3-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="33ce3-128">ويتم إعداد التقويمات المالية في صفحة التقويمات المالية.</span><span class="sxs-lookup"><span data-stu-id="33ce3-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="33ce3-129">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="33ce3-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="33ce3-130">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="33ce3-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="33ce3-131">وتتم تسوية الإهلاك تلقائيًا لكل فترة مالية.</span><span class="sxs-lookup"><span data-stu-id="33ce3-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="33ce3-132">ويعتمد طول السنة المالية التالية على الفترات المالية التي تقوم بإعدادها عند قيامك بإنشاء سنة مالية جديدة في نموذج التقويمات المالية.</span><span class="sxs-lookup"><span data-stu-id="33ce3-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="33ce3-133">إذا قمت بتحديد "مالي"، تتوفر الخيارات التالية في حقل تكرار الفترة:</span><span class="sxs-lookup"><span data-stu-id="33ce3-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="33ce3-134">يقوم الخيار سنوي بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="33ce3-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="33ce3-135">تحسب الفترة المالية إجمالي مبلغ الإهلاك بالنسبة للسنة المالية، الذي يستحق في فترات السنة المالية التي تم تحديدها في نموذج التقويمات المالية للتقويم المالي.</span><span class="sxs-lookup"><span data-stu-id="33ce3-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="33ce3-136">مثال: إهلاك القسط الثابت لأصل ثابت لم يتم تغييره</span><span class="sxs-lookup"><span data-stu-id="33ce3-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="33ce3-137">تخيل أن الأصل الثابت يحتوي على الخصائص التالية.</span><span class="sxs-lookup"><span data-stu-id="33ce3-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="33ce3-138">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="33ce3-138">Acquisition cost</span></span>    | <span data-ttu-id="33ce3-139">11,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-139">11,000</span></span> |
| <span data-ttu-id="33ce3-140">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="33ce3-140">Salvage value</span></span>       | <span data-ttu-id="33ce3-141">1,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-141">1,000</span></span>  |
| <span data-ttu-id="33ce3-142">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="33ce3-142">Depreciation base</span></span>   | <span data-ttu-id="33ce3-143">10,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-143">10,000</span></span> |
| <span data-ttu-id="33ce3-144">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="33ce3-144">Service life years</span></span>  | <span data-ttu-id="33ce3-145">5</span><span class="sxs-lookup"><span data-stu-id="33ce3-145">5</span></span>      |
| <span data-ttu-id="33ce3-146">الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="33ce3-146">Yearly depreciation</span></span> | <span data-ttu-id="33ce3-147">2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-147">2,000</span></span>  |

<span data-ttu-id="33ce3-148">تحصل على نفس مبلغ الإهلاك كل سنة.</span><span class="sxs-lookup"><span data-stu-id="33ce3-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="33ce3-149">(تكلفة الامتلاك - القيمة الباقية) / سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="33ce3-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="33ce3-150">الفترة</span><span class="sxs-lookup"><span data-stu-id="33ce3-150">Period</span></span> | <span data-ttu-id="33ce3-151">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="33ce3-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="33ce3-152">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="33ce3-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="33ce3-153">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="33ce3-153">Year 1</span></span> | <span data-ttu-id="33ce3-154">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="33ce3-155">9,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-155">9,000</span></span>                                 |
| <span data-ttu-id="33ce3-156">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="33ce3-156">Year 2</span></span> | <span data-ttu-id="33ce3-157">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="33ce3-158">7,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-158">7,000</span></span>                                 |
| <span data-ttu-id="33ce3-159">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="33ce3-159">Year 3</span></span> | <span data-ttu-id="33ce3-160">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="33ce3-161">5,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-161">5,000</span></span>                                 |
| <span data-ttu-id="33ce3-162">السنة الرابعة</span><span class="sxs-lookup"><span data-stu-id="33ce3-162">Year 4</span></span> | <span data-ttu-id="33ce3-163">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="33ce3-164">3,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-164">3,000</span></span>                                 |
| <span data-ttu-id="33ce3-165">السنة الخامسة</span><span class="sxs-lookup"><span data-stu-id="33ce3-165">Year 5</span></span> | <span data-ttu-id="33ce3-166">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="33ce3-167">1,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="33ce3-168"> مثال: إهلاك قسط ثابت لأصل ثابت تم تعديله</span><span class="sxs-lookup"><span data-stu-id="33ce3-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="33ce3-169">افترض الآن أنك قمت بإضافة تسوية امتلاك تصل إلى 4000 في السنة الثانية إلى نفس الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="33ce3-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="33ce3-170">تكون مدة الخدمة لتسوية الامتلاك هي نفس مدة الخدمة للأصل الثابت وتبدأ منذ وقت امتلاكه.</span><span class="sxs-lookup"><span data-stu-id="33ce3-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="33ce3-171">يبقى صافي القيمة الدفترية في نهاية السنة الخامسة، مطابقًا لصافي القيمة الدفترية الخاصة بتسوية الامتلاك.</span><span class="sxs-lookup"><span data-stu-id="33ce3-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="33ce3-172">يتم حساب الإهلاك حسب الفترة كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="33ce3-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="33ce3-173">الفترة</span><span class="sxs-lookup"><span data-stu-id="33ce3-173">Period</span></span> | <span data-ttu-id="33ce3-174">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="33ce3-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="33ce3-175">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="33ce3-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="33ce3-176">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="33ce3-176">Year 1</span></span> | <span data-ttu-id="33ce3-177">10,000 / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="33ce3-178">11,000 - 2,000 = 9,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="33ce3-179">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="33ce3-179">Year 2</span></span> | <span data-ttu-id="33ce3-180">4,000 (تسوية الاستحواذ)</span><span class="sxs-lookup"><span data-stu-id="33ce3-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="33ce3-181">9,000 + 4,000 =13,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="33ce3-182">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="33ce3-182">Year 2</span></span> | <span data-ttu-id="33ce3-183">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="33ce3-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="33ce3-184">13,000 - 2,800 = 10,200</span><span class="sxs-lookup"><span data-stu-id="33ce3-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="33ce3-185">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="33ce3-185">Year 3</span></span> | <span data-ttu-id="33ce3-186">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="33ce3-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="33ce3-187">10,200 - 2,800 = 7,400</span><span class="sxs-lookup"><span data-stu-id="33ce3-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="33ce3-188">السنة الرابعة</span><span class="sxs-lookup"><span data-stu-id="33ce3-188">Year 4</span></span> | <span data-ttu-id="33ce3-189">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="33ce3-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="33ce3-190">7,400 - 2,800 = 4,600</span><span class="sxs-lookup"><span data-stu-id="33ce3-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="33ce3-191">السنة الخامسة</span><span class="sxs-lookup"><span data-stu-id="33ce3-191">Year 5</span></span> | <span data-ttu-id="33ce3-192">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="33ce3-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="33ce3-193">4,600 - 2,800 = 1,800</span><span class="sxs-lookup"><span data-stu-id="33ce3-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="33ce3-194">السنة السادسة</span><span class="sxs-lookup"><span data-stu-id="33ce3-194">Year 6</span></span> | <span data-ttu-id="33ce3-195">المتبقي 800\*</span><span class="sxs-lookup"><span data-stu-id="33ce3-195">Remaining 800\*</span></span>                           | <span data-ttu-id="33ce3-196">1,800 – 800 = 1,000</span><span class="sxs-lookup"><span data-stu-id="33ce3-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="33ce3-197">\*نظرًا لأن الكمية المتبقية أقل من مبلغ الإهلاك، فسيتم فقط أخذ الكمية المتبقية ناقص القيمة الباقية.</span><span class="sxs-lookup"><span data-stu-id="33ce3-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>





