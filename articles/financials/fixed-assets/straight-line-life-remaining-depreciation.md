---
title: "إهلاك المتبقي من مدة خدمة القسط الثابت"
description: "تقدم هذه المقالة نظرة عامة على أسلوب إهلاك المتبقي من مدة خدمة القسط الثابت‬."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4ad82f3177e4abb7b9cb575b910aabc69901f475
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="bf961-103">إهلاك المتبقي من مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="bf961-103">Straight line life remaining depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bf961-104">تقدم هذه المقالة نظرة عامة على أسلوب إهلاك المتبقي من مدة خدمة القسط الثابت‬.</span><span class="sxs-lookup"><span data-stu-id="bf961-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="bf961-105">عند إعداد ملف تعريف إهلاك أصل ثابت وتحديد **المتبقي من مدة خدمة القسط الثابت‬** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يستند إهلاك الأصول الثابتة التي يتم تعيينها لملف تعريف الإهلاك إلى عمر الخدمة المتبقي للأصل.</span><span class="sxs-lookup"><span data-stu-id="bf961-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="bf961-106">ويُمثل مبلغ الإهلاك عمومًا نفس الشيء في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="bf961-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="bf961-107">ولإعداد إهلاك المتبقي من مدة خدمة القسط الثابت‬، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="bf961-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="bf961-108">وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة المحددة في حقل **سنة الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="bf961-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="bf961-109">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="bf961-109">Select a depreciation year</span></span>
<span data-ttu-id="bf961-110">ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="bf961-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="bf961-111">القيمة الافتراضية هي **تقويم**.</span><span class="sxs-lookup"><span data-stu-id="bf961-111">The default value is **Calendar**.</span></span> <span data-ttu-id="bf961-112">ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="bf961-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="bf961-113">ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="bf961-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="bf961-114">التقويم</span><span class="sxs-lookup"><span data-stu-id="bf961-114">Calendar</span></span>

<span data-ttu-id="bf961-115">في حالة تحديد **التقويم** في حقل  ***سنة الإهلاك***، يتم افتراض سنة من 1 يناير حتى 31 ديسمبر، حتى إذا كنت قد قمت بتحديد التقويم المالي بشكل مختلف.</span><span class="sxs-lookup"><span data-stu-id="bf961-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="bf961-116">ويقوم خيار **التقويم** بتحديث أساس الإهلاك في 1 كانون الثاني/يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="bf961-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="bf961-117">وبشكل عام، يعتبر أساس الإهلاك صافي القيمة الدفترية ناقص القيمة الباقية.</span><span class="sxs-lookup"><span data-stu-id="bf961-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="bf961-118">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود العمليات الحسابية.</span><span class="sxs-lookup"><span data-stu-id="bf961-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="bf961-119">وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="bf961-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="bf961-120">**السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="bf961-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="bf961-121">**شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="bf961-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="bf961-122">**ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="bf961-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="bf961-123">**نصف سنوي** ترحيل المبلغ نصف السنوي في نهاية كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="bf961-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="bf961-124">**يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="bf961-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="bf961-125">على سبيل المثال، إذا قمت بتحديد **سنوي**، يتم ترحيل الإهلاك السنوي مرة واحدة فقط في 31 ديسمبر من كل عام.</span><span class="sxs-lookup"><span data-stu-id="bf961-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="bf961-126">أما إذا حددت **شهري**، فإنه يتم ترحيل الإهلاك الشهري في كل شهر بمعدل 1/12 من قيمة المبلغ الإجمالي السنوي.</span><span class="sxs-lookup"><span data-stu-id="bf961-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="bf961-127">مالي</span><span class="sxs-lookup"><span data-stu-id="bf961-127">Fiscal</span></span>

<span data-ttu-id="bf961-128">في حالة تحديد **مالي** في حقل **سنة الإهلاك**، فإنه يتم استخدام إهلاك المتبقي من مدة خدمة القسط الثابت‬.</span><span class="sxs-lookup"><span data-stu-id="bf961-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="bf961-129">ويتم حساب الإهلاك استناداً إلى السنوات المالية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="bf961-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="bf961-130">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو 2015 حتى 30 حزيران/يونيو 2016، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="bf961-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="bf961-131">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="bf961-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="bf961-132">وتتم تسوية الإهلاك لكل فترة مالية.</span><span class="sxs-lookup"><span data-stu-id="bf961-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="bf961-133">ويتم تحديد طول السنة المالية التالية حسب الفترات المالية التي يتم إعدادها في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="bf961-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="bf961-134">وإذا قمت بتحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="bf961-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="bf961-135">يقوم الخيار **سنوي** بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="bf961-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="bf961-136">تحسب **الفترة المالية** المبلغ الإجمالي للإهلاك للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="bf961-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="bf961-137">يتراكم هذا المبلغ فيما بعد في الفترات المالية المحددة في صفحة **التقويمات المالية** للتقويم المالي المحدد للدفتر.</span><span class="sxs-lookup"><span data-stu-id="bf961-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="bf961-138">مثال على إهلاك القسط الثابت لأصل ثابت لم يتم تغييره</span><span class="sxs-lookup"><span data-stu-id="bf961-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="bf961-139">يشتمل الأصل الثابت على الخصائص التالية.</span><span class="sxs-lookup"><span data-stu-id="bf961-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="bf961-140">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="bf961-140">Acquisition cost</span></span>    | <span data-ttu-id="bf961-141">11,000</span><span class="sxs-lookup"><span data-stu-id="bf961-141">11,000</span></span> |
| <span data-ttu-id="bf961-142">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="bf961-142">Salvage value</span></span>       | <span data-ttu-id="bf961-143">1,000</span><span class="sxs-lookup"><span data-stu-id="bf961-143">1,000</span></span>  |
| <span data-ttu-id="bf961-144">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="bf961-144">Depreciation base</span></span>   | <span data-ttu-id="bf961-145">10,000</span><span class="sxs-lookup"><span data-stu-id="bf961-145">10,000</span></span> |
| <span data-ttu-id="bf961-146">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="bf961-146">Service life years</span></span>  | <span data-ttu-id="bf961-147">5</span><span class="sxs-lookup"><span data-stu-id="bf961-147">5</span></span>      |
| <span data-ttu-id="bf961-148">الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="bf961-148">Yearly depreciation</span></span> | <span data-ttu-id="bf961-149">2,000</span><span class="sxs-lookup"><span data-stu-id="bf961-149">2,000</span></span>  |

<span data-ttu-id="bf961-150">مبلغ الإهلاك هو نفسه كل سنة: (تكلفة الاستحواذ - قيمة الخردة) ÷ سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="bf961-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="bf961-151">الفترة</span><span class="sxs-lookup"><span data-stu-id="bf961-151">Period</span></span> | <span data-ttu-id="bf961-152">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="bf961-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="bf961-153">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="bf961-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="bf961-154">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="bf961-154">Year 1</span></span> | <span data-ttu-id="bf961-155">(11,000 – 1,000) ÷ 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="bf961-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="bf961-156">9,000</span><span class="sxs-lookup"><span data-stu-id="bf961-156">9,000</span></span>                                 |
| <span data-ttu-id="bf961-157">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="bf961-157">Year 2</span></span> | <span data-ttu-id="bf961-158">(9,000 – 1,000) ÷ 4 = 2,000</span><span class="sxs-lookup"><span data-stu-id="bf961-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="bf961-159">7,000</span><span class="sxs-lookup"><span data-stu-id="bf961-159">7,000</span></span>                                 |
| <span data-ttu-id="bf961-160">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="bf961-160">Year 3</span></span> | <span data-ttu-id="bf961-161">(7,000 – 1,000) ÷ 3 = 2,000</span><span class="sxs-lookup"><span data-stu-id="bf961-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="bf961-162">5,000</span><span class="sxs-lookup"><span data-stu-id="bf961-162">5,000</span></span>                                 |
| <span data-ttu-id="bf961-163">السنة الرابعة</span><span class="sxs-lookup"><span data-stu-id="bf961-163">Year 4</span></span> | <span data-ttu-id="bf961-164">(5,000 – 1,000) ÷ 2 = 2,000</span><span class="sxs-lookup"><span data-stu-id="bf961-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="bf961-165">3,000</span><span class="sxs-lookup"><span data-stu-id="bf961-165">3,000</span></span>                                 |
| <span data-ttu-id="bf961-166">السنة الخامسة</span><span class="sxs-lookup"><span data-stu-id="bf961-166">Year 5</span></span> | <span data-ttu-id="bf961-167">(3,000 – 1,000) ÷ 1 = 2,000</span><span class="sxs-lookup"><span data-stu-id="bf961-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="bf961-168">1,000</span><span class="sxs-lookup"><span data-stu-id="bf961-168">1,000</span></span>                                 |






