---
title: "إهلاك القسط المتناقص بنسبة 175 بالمائة"
description: "يقدم هذا الموضوع نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 175 بالمائة‬."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2a63293dbf24c27733f8013947aeab5792fa0db9
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="94a2e-103">إهلاك القسط المتناقص بنسبة 175 بالمائة</span><span class="sxs-lookup"><span data-stu-id="94a2e-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94a2e-104">يقدم هذا الموضوع نظرة عامة على أسلوب إهلاك الرصيد المتناقص بنسبة 175 بالمائة‬.</span><span class="sxs-lookup"><span data-stu-id="94a2e-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="94a2e-105">عند إعداد ملف تعريف إهلاك أصول ثابتة وتحديد **الرصيد المتناقص بنسبة 175%** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، يتم إهلاك الأصول الثابتة التي تم تعيين ملف تعريف الإهلاك لها بنفس النسبة المئوية في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="94a2e-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="94a2e-106">ولإعداد إهلاك الرصيد المتناقص بنسبة 175%، يجب عليك أيضًا تحديد الخيارات في حقل **سنة الإهلاك** وحقل **تكرار الفترة** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="94a2e-107">وتختلف الخيارات المتوفرة في حقل **تكرار الفترة** استناداً إلى القيمة المحددة في حقل **سنة الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="94a2e-108">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="94a2e-108">Select a depreciation year</span></span>
<span data-ttu-id="94a2e-109">ويمكنك تحديد **تقويم** أو **مالي** في حقل **سنة الإهلاك** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="94a2e-110">القيمة الافتراضية هي **تقويم**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="94a2e-111">ويعمل التحديد الذي قمت به على تحديد الخيارات المتوفرة في حقل **تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="94a2e-112">ويحدد هذا الحقل التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="94a2e-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="94a2e-113">التقويم</span><span class="sxs-lookup"><span data-stu-id="94a2e-113">Calendar</span></span>

<span data-ttu-id="94a2e-114">يمكنك اختيار الاحتفاظ بالقيمة الافتراضية في حقل **سنة الإهلاك**، **التقويم**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="94a2e-115">ويقوم خيار **التقويم** بتحديث أساس الإهلاك في 1 كانون الثاني/يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="94a2e-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="94a2e-116">وبشكل عام، يعتبر أساس الإهلاك صافي القيمة الدفترية ناقص قيمة الخردة.</span><span class="sxs-lookup"><span data-stu-id="94a2e-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="94a2e-117">في المثال الموضح أدناه في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب.</span><span class="sxs-lookup"><span data-stu-id="94a2e-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="94a2e-118">وإذا قمت بتحديد **التقويم** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="94a2e-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="94a2e-119">**السنوي** ترحيل مبلغ في 31 كانون الأول/ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="94a2e-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="94a2e-120">**شهري** ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="94a2e-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="94a2e-121">**ربع سنوي** مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="94a2e-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="94a2e-122">**نصف سنوي** ترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="94a2e-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="94a2e-123">**يومي** ترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="94a2e-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="94a2e-124">مالي</span><span class="sxs-lookup"><span data-stu-id="94a2e-124">Fiscal</span></span>

<span data-ttu-id="94a2e-125">إذا قمت بتحديد **مالية** في حقل **سنة الإهلاك**، يتم حساب إهلاك الرصيد المتناقص بنسبة 175% بحسب السنة المالية للتقويم المالي المحدد للدفتر، أو للتقويم المالي المحدد في صفحة **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="94a2e-126">ويتم إعداد التقويمات المالية في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="94a2e-127">ولمزيد من المعلومات، راجع [التقويمات المالية، والسنوات المالية، والفترات](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="94a2e-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="94a2e-128">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="94a2e-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="94a2e-129">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="94a2e-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="94a2e-130">وتتم تسوية الإهلاك تلقائيًا لكل فترة، ويتم تحديد طول السنة المالية التالية بواسطة إعداد الفترات في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="94a2e-131">وإذا قمت بتحديد **مالية** كسنة إهلاك، تتوفر الخيارات التالية في حقل **تكرار الفترة**:</span><span class="sxs-lookup"><span data-stu-id="94a2e-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="94a2e-132">**سنوي** ترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="94a2e-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="94a2e-133">تحسب **الفترة المالية** المبلغ الإجمالي للإهلاك للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="94a2e-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="94a2e-134">ويُستحق هذا المبلغ في الفترات المالية التي يتم تحديدها في صفحة **التقويمات المالية**.</span><span class="sxs-lookup"><span data-stu-id="94a2e-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="94a2e-135">مثال لإهلاك القسط المتناقص بنسبة 175%</span><span class="sxs-lookup"><span data-stu-id="94a2e-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="94a2e-136">تكلفة الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="94a2e-136">Acquisition cost</span></span>               | <span data-ttu-id="94a2e-137">11,000</span><span class="sxs-lookup"><span data-stu-id="94a2e-137">11,000</span></span> |
| <span data-ttu-id="94a2e-138">القيمة الباقية</span><span class="sxs-lookup"><span data-stu-id="94a2e-138">Salvage value</span></span>                  | <span data-ttu-id="94a2e-139">1,000</span><span class="sxs-lookup"><span data-stu-id="94a2e-139">1,000</span></span>  |
| <span data-ttu-id="94a2e-140">أساس الإهلاك</span><span class="sxs-lookup"><span data-stu-id="94a2e-140">Depreciation base</span></span>              | <span data-ttu-id="94a2e-141">10,000</span><span class="sxs-lookup"><span data-stu-id="94a2e-141">10,000</span></span> |
| <span data-ttu-id="94a2e-142">سنوات مدة الخدمة</span><span class="sxs-lookup"><span data-stu-id="94a2e-142">Service life years</span></span>             | <span data-ttu-id="94a2e-143">5</span><span class="sxs-lookup"><span data-stu-id="94a2e-143">5</span></span>      |
| <span data-ttu-id="94a2e-144">النسبة المئوية للإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="94a2e-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="94a2e-145">35%</span><span class="sxs-lookup"><span data-stu-id="94a2e-145">35%</span></span>    |

<span data-ttu-id="94a2e-146">تقسم طريقة إهلاك الرصيد المتناقص بنسبة 175 بالمائة على سنوات مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="94a2e-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="94a2e-147">وسيتم ضرب النسبة المئوية في صافي القيمة الدفترية للأصل لتحديد مبلغ الإهلاك في السنة.</span><span class="sxs-lookup"><span data-stu-id="94a2e-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="94a2e-148">الفترة</span><span class="sxs-lookup"><span data-stu-id="94a2e-148">Period</span></span> | <span data-ttu-id="94a2e-149">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="94a2e-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="94a2e-150">القيمة الدفترية</span><span class="sxs-lookup"><span data-stu-id="94a2e-150">Book value</span></span>                  | <span data-ttu-id="94a2e-151">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="94a2e-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="94a2e-152">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="94a2e-152">Year 1</span></span> | <span data-ttu-id="94a2e-153">(11,000 – 1,000) × 35% = 3,500</span><span class="sxs-lookup"><span data-stu-id="94a2e-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="94a2e-154">11,000 – 3,500 = 7,500</span><span class="sxs-lookup"><span data-stu-id="94a2e-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="94a2e-155">11,000 – 1,000 – 3,500 = 6,500</span><span class="sxs-lookup"><span data-stu-id="94a2e-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="94a2e-156">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="94a2e-156">Year 2</span></span> | <span data-ttu-id="94a2e-157">6,500 × 35% = 2,275</span><span class="sxs-lookup"><span data-stu-id="94a2e-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="94a2e-158">7,500 – 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="94a2e-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="94a2e-159">6,500 – 2,275 = 4,225</span><span class="sxs-lookup"><span data-stu-id="94a2e-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="94a2e-160">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="94a2e-160">Year 3</span></span> | <span data-ttu-id="94a2e-161">4,225 × 35% = 1,478.75</span><span class="sxs-lookup"><span data-stu-id="94a2e-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="94a2e-162">5,225 – 1,478.75 = 3,746.25</span><span class="sxs-lookup"><span data-stu-id="94a2e-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="94a2e-163">4,225 – 1,478.75 = 2,746.25</span><span class="sxs-lookup"><span data-stu-id="94a2e-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="94a2e-164">بشكل عام، عندما يصبح المبلغ الذي يتم حسابه باستخدام طريقة الإهلاك المتناقص بنسبة 175% أقل من المبلغ الذي يُحسب باستخدام طريقة القسط الثابت، يكون هناك تحويل لطريقة القسط الثابت للمدة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="94a2e-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




