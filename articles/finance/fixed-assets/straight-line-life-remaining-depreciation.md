---
title: إهلاك المتبقي من مدة خدمة القسط الثابت
description: تقدم هذه المقالة نظرة عامة على أسلوب إهلاك المتبقي من مدة خدمة القسط الثابت‬.
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 823b2569670adfbf04038abca656e34f0199fce1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210085"
---
# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="44b11-103">إهلاك المتبقي من مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="44b11-103">Straight line life remaining depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44b11-104">تقدم هذه المقالة نظرة عامة على أسلوب إهلاك المتبقي من مدة خدمة القسط الثابت‬.</span><span class="sxs-lookup"><span data-stu-id="44b11-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="44b11-105">عند إعداد ملف تعريف إهلاك أصل ثابت وتحديد **المتبقي من مدة خدمة القسط الثابت‬** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يستند إهلاك الأصول الثابتة التي يتم تعيينها لملف تعريف الإهلاك إلى عمر الخدمة المتبقي للأصل.</span><span class="sxs-lookup"><span data-stu-id="44b11-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="44b11-106">ويُمثل مبلغ الإهلاك عمومًا نفس الشيء في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="44b11-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="44b11-107">ولإعداد إهلاك المتبقي من مدة خدمة القسط الثابت‬، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="44b11-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="44b11-108">وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة المحددة في حقل **سنة الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="44b11-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="44b11-109">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="44b11-109">Select a depreciation year</span></span>
<span data-ttu-id="44b11-110">ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="44b11-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="44b11-111">القيمة الافتراضية هي **تقويم**.</span><span class="sxs-lookup"><span data-stu-id="44b11-111">The default value is **Calendar**.</span></span> <span data-ttu-id="44b11-112">ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="44b11-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="44b11-113">ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="44b11-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="44b11-114">التقويم</span><span class="sxs-lookup"><span data-stu-id="44b11-114">Calendar</span></span>

<span data-ttu-id="44b11-115">إذا قمت بتحديد **التقويم** في حقل **_سنة الإهلاك_*، يتم افتراض السنة من 1 يناير حتى 31 ديسمبر، حتى وإن كنت قمت بتحديد التقويم المالي بشكل مختلف. يقوم الخيار _\* التقويم*\* بتحديث أساس الإهلاك في 1 يناير من كل سنة.</span><span class="sxs-lookup"><span data-stu-id="44b11-115">If you select **Calendar** in the **_Depreciation year_*_ field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently. The _\* Calendar*\* option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="44b11-116">وبشكل عام، يعتبر أساس الإهلاك صافي القيمة الدفترية ناقص القيمة الباقية.</span><span class="sxs-lookup"><span data-stu-id="44b11-116">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="44b11-117">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود العمليات الحسابية.</span><span class="sxs-lookup"><span data-stu-id="44b11-117">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="44b11-118">وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="44b11-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="44b11-119">**السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="44b11-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="44b11-120">**شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="44b11-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="44b11-121">**ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="44b11-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="44b11-122">**نصف سنوي** ترحيل المبلغ نصف السنوي في نهاية كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="44b11-122">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="44b11-123">**يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="44b11-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="44b11-124">على سبيل المثال، إذا قمت بتحديد **سنوي**، يتم ترحيل الإهلاك السنوي مرة واحدة فقط في 31 ديسمبر من كل عام.</span><span class="sxs-lookup"><span data-stu-id="44b11-124">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="44b11-125">أما إذا حددت **شهري**، فإنه يتم ترحيل الإهلاك الشهري في كل شهر بمعدل 1/12 من قيمة المبلغ الإجمالي السنوي.</span><span class="sxs-lookup"><span data-stu-id="44b11-125">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="44b11-126">مالي</span><span class="sxs-lookup"><span data-stu-id="44b11-126">Fiscal</span></span>

<span data-ttu-id="44b11-127">في حالة تحديد **مالي** في حقل **سنة الإهلاك**، فإنه يتم استخدام إهلاك المتبقي من مدة خدمة القسط الثابت‬.</span><span class="sxs-lookup"><span data-stu-id="44b11-127">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="44b11-128">ويتم حساب الإهلاك استناداً إلى السنوات المالية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="44b11-128">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="44b11-129">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو 2015 حتى 30 حزيران/يونيو 2016، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="44b11-129">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="44b11-130">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="44b11-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="44b11-131">وتتم تسوية الإهلاك لكل فترة مالية.</span><span class="sxs-lookup"><span data-stu-id="44b11-131">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="44b11-132">ويتم تحديد طول السنة المالية التالية حسب الفترات المالية التي يتم إعدادها في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="44b11-132">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="44b11-133">وإذا قمت بتحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="44b11-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="44b11-134">يقوم الخيار **سنوي** بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="44b11-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="44b11-135">تحسب **الفترة المالية** المبلغ الإجمالي للإهلاك للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="44b11-135">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="44b11-136">يتراكم هذا المبلغ فيما بعد في الفترات المالية المحددة في صفحة **التقويمات المالية** للتقويم المالي المحدد للدفتر.</span><span class="sxs-lookup"><span data-stu-id="44b11-136">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="44b11-137">مثال على إهلاك القسط الثابت لأصل ثابت لم يتم تغييره</span><span class="sxs-lookup"><span data-stu-id="44b11-137">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="44b11-138">يشتمل الأصل الثابت على الخصائص التالية.</span><span class="sxs-lookup"><span data-stu-id="44b11-138">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="44b11-139">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="44b11-139">Acquisition cost</span></span>    | <span data-ttu-id="44b11-140">11,000</span><span class="sxs-lookup"><span data-stu-id="44b11-140">11,000</span></span> |
| <span data-ttu-id="44b11-141">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="44b11-141">Salvage value</span></span>       | <span data-ttu-id="44b11-142">1,000</span><span class="sxs-lookup"><span data-stu-id="44b11-142">1,000</span></span>  |
| <span data-ttu-id="44b11-143">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="44b11-143">Depreciation base</span></span>   | <span data-ttu-id="44b11-144">10,000</span><span class="sxs-lookup"><span data-stu-id="44b11-144">10,000</span></span> |
| <span data-ttu-id="44b11-145">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="44b11-145">Service life years</span></span>  | <span data-ttu-id="44b11-146">5</span><span class="sxs-lookup"><span data-stu-id="44b11-146">5</span></span>      |
| <span data-ttu-id="44b11-147">الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="44b11-147">Yearly depreciation</span></span> | <span data-ttu-id="44b11-148">2,000</span><span class="sxs-lookup"><span data-stu-id="44b11-148">2,000</span></span>  |

<span data-ttu-id="44b11-149">مبلغ الإهلاك هو نفسه كل سنة: (تكلفة الاستحواذ - قيمة الخردة) ÷ سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="44b11-149">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="44b11-150">الفترة</span><span class="sxs-lookup"><span data-stu-id="44b11-150">Period</span></span> | <span data-ttu-id="44b11-151">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="44b11-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="44b11-152">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="44b11-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="44b11-153">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="44b11-153">Year 1</span></span> | <span data-ttu-id="44b11-154">(11,000 – 1,000) ÷ 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44b11-154">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="44b11-155">9,000</span><span class="sxs-lookup"><span data-stu-id="44b11-155">9,000</span></span>                                 |
| <span data-ttu-id="44b11-156">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="44b11-156">Year 2</span></span> | <span data-ttu-id="44b11-157">(9,000 – 1,000) ÷ 4 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44b11-157">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="44b11-158">7,000</span><span class="sxs-lookup"><span data-stu-id="44b11-158">7,000</span></span>                                 |
| <span data-ttu-id="44b11-159">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="44b11-159">Year 3</span></span> | <span data-ttu-id="44b11-160">(7,000 – 1,000) ÷ 3 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44b11-160">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="44b11-161">5,000</span><span class="sxs-lookup"><span data-stu-id="44b11-161">5,000</span></span>                                 |
| <span data-ttu-id="44b11-162">السنة الرابعة</span><span class="sxs-lookup"><span data-stu-id="44b11-162">Year 4</span></span> | <span data-ttu-id="44b11-163">(5,000 – 1,000) ÷ 2 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44b11-163">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="44b11-164">3,000</span><span class="sxs-lookup"><span data-stu-id="44b11-164">3,000</span></span>                                 |
| <span data-ttu-id="44b11-165">السنة الخامسة</span><span class="sxs-lookup"><span data-stu-id="44b11-165">Year 5</span></span> | <span data-ttu-id="44b11-166">(3,000 – 1,000) ÷ 1 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44b11-166">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="44b11-167">1,000</span><span class="sxs-lookup"><span data-stu-id="44b11-167">1,000</span></span>                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]