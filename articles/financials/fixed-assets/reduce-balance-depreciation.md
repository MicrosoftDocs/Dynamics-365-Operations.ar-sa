---
title: "إهلاك القسط المتناقص"
description: "تقدم هذه المقالة نظرة عامة على أسلوب تقليل الرصيد للإهلاك."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29bc8cd02d98479197d7e5f5664b9859c03893b3
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="236ca-103">إهلاك القسط المتناقص</span><span class="sxs-lookup"><span data-stu-id="236ca-103">Reduce balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="236ca-104">تقدم هذه المقالة نظرة عامة على أسلوب تقليل الرصيد للإهلاك.</span><span class="sxs-lookup"><span data-stu-id="236ca-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="236ca-105">عند إعداد ملف تعريف إهلاك أصل ثابت وتحديد "الرصيد المتناقص" في الحقل "الطريقة" في صفحة "ملفات تعريف الإهلاك"، يتم إهلاك الأصول التي تم تخصيص ملف تعريف الإهلاك هذا لها، وذلك بنفس النسبة المئوية في كل فترة إهلاك.</span><span class="sxs-lookup"><span data-stu-id="236ca-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="236ca-106">ولإعداد إهلاك الرصيد المتناقص، يجب عليك أيضًا عمل تحديدات في بعض الحقول الموجودة في علامة التبويب السريع "عام" الموجودة في صفحة "ملفات تعريف الإهلاك".</span><span class="sxs-lookup"><span data-stu-id="236ca-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="236ca-107">أولاً، حدد سنة في حقل "سنة الإهلاك".</span><span class="sxs-lookup"><span data-stu-id="236ca-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="236ca-108">وبناءً على التحديد، تظهر خيارات مختلفة في الحقل "تكرار الفترة"، كما هو موضح في الأقسام التالية.</span><span class="sxs-lookup"><span data-stu-id="236ca-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="236ca-109">ويجب عليك أيضًا إدخال قيمة في الحقل "النسبة المئوية" لملف تعريف الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="236ca-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="236ca-110">وفي حالة تحديد الخيار "الإهلاك الكامل"، فسيتم تحصيل أساس الإهلاك المتبقي في فترة آخر إهلاك وقد يكون مبلغًا كبيرًا.</span><span class="sxs-lookup"><span data-stu-id="236ca-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="236ca-111">ولا تستخدم بعض البلاد/المناطق بديلاً لطريقة القسط الثابت.</span><span class="sxs-lookup"><span data-stu-id="236ca-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="236ca-112">ويتم استخدام البديل عندما يكون مبلغ الإهلاك البديل أكبر من أو مساويًا لمبلغ ملف تعريف الإهلاك الأساسي، فإن مبلغ الإهلاك المأخوذ يكون مبلغ الطريقة البديلة.</span><span class="sxs-lookup"><span data-stu-id="236ca-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="236ca-113">ولأنه لن يتم مطلقًا إهلاك الأصل بالكامل بناءً على حساب النسبة المئوية، فيجب عليك تحديد الخيار "الإهلاك الكامل" لإهلاك أصل بالكامل.</span><span class="sxs-lookup"><span data-stu-id="236ca-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="236ca-114">تحديد سنة الإهلاك</span><span class="sxs-lookup"><span data-stu-id="236ca-114">Select a depreciation year</span></span>
<span data-ttu-id="236ca-115">يمكنك تحديد "تقويم" أو "مالي" في حقل سنة الإهلاك في صفحة ملفات تعريف الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="236ca-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="236ca-116">ويعمل هذا التحديد على تحديد الخيارات المتوفرة في حقل تكرار الفترة.</span><span class="sxs-lookup"><span data-stu-id="236ca-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="236ca-117">والخيار الافتراضي هو "تقويم".</span><span class="sxs-lookup"><span data-stu-id="236ca-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="236ca-118">التقويم</span><span class="sxs-lookup"><span data-stu-id="236ca-118">Calendar</span></span>

<span data-ttu-id="236ca-119">يقوم خيار التقويم بتحديث أساس الإهلاك، الذي عادةً ما يكون صافي القيمة الدفترية ناقص قيمة الخردة، في 1 يناير من كل عام.</span><span class="sxs-lookup"><span data-stu-id="236ca-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="236ca-120">وفي مثال إهلاك الرصيد المتناقص الموضح لاحقًا في هذا الموضوع، يعتبر أساس الإهلاك هو البسط في التعبير الأول في عمود عمليات الحساب.</span><span class="sxs-lookup"><span data-stu-id="236ca-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="236ca-121">في حالة قيامك بتحديد "تقويم"، تتوفر الخيارات التالية في حقل "تكرار الفترة"، الذي يحدد التواريخ الخاصة بترحيل استحقاق الإهلاك بالإضافة إلى المبالغ خلال سنة التقويم:</span><span class="sxs-lookup"><span data-stu-id="236ca-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="236ca-122">الترحيلات السنوية في 31 ديسمبر.</span><span class="sxs-lookup"><span data-stu-id="236ca-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="236ca-123">شهري ترحيل مبلغ شهري في نهاية كل شهر في التقويم.</span><span class="sxs-lookup"><span data-stu-id="236ca-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="236ca-124">ربع سنوي مبلغ ربع سنوي في نهاية كل ربع عام بالتقويم (31 مارس و30 يونيو و30 سبتمبر و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="236ca-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="236ca-125">يقوم خيار الترحيل نصف السنوي بترحيل مبلغ نصف سنوي في كل نصف عام بالتقويم (30 يونيو و31 ديسمبر).</span><span class="sxs-lookup"><span data-stu-id="236ca-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="236ca-126">يقوم خيار الترحيل اليومي بترحيل مبلغ الإهلاك لطريقة الإهلاك اليومية باستخدام حركة واحدة لكل يوم.</span><span class="sxs-lookup"><span data-stu-id="236ca-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="236ca-127">على سبيل المثال، إذا قمت بتحديد "سنوي"، يتم ترحيل الإهلاك السنوي مرة واحدة فقط في 31 ديسمبر من كل عام.</span><span class="sxs-lookup"><span data-stu-id="236ca-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="236ca-128">أما إذا حددت "شهري"، فإنه يتم ترحيل الإهلاك الشهري في كل شهر بمعدل 1/12 من قيمة المبلغ الإجمالي السنوي.</span><span class="sxs-lookup"><span data-stu-id="236ca-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="236ca-129">مالي</span><span class="sxs-lookup"><span data-stu-id="236ca-129">Fiscal</span></span>

<span data-ttu-id="236ca-130">في حالة تحديد "مالي" في حقل سنة الإهلاك، فسيتم استخدام طريقة إهلاك القسط الثابت.</span><span class="sxs-lookup"><span data-stu-id="236ca-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="236ca-131">ويتم حساب ذلك على أساس السنة المالية، التي تم إعدادها في صفحة التقويمات المالية للتقويم المالي المحدد في صفحة دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="236ca-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="236ca-132">‏‫على سبيل المثال، بالنسبة للسنة المالية من 1 تموز/يوليو إلى 30 حزيران/يونيو، يبدأ حساب الإهلاك في 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="236ca-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="236ca-133">قد تطول مدة السنة المالية عن 12 شهرًا أو قد تقل عن ذلك.</span><span class="sxs-lookup"><span data-stu-id="236ca-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="236ca-134">وتتم تسوية الإهلاك لكل فترة مالية.</span><span class="sxs-lookup"><span data-stu-id="236ca-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="236ca-135">ويعتمد طول السنة المالية التالية على الفترات المالية التي تقوم بإعدادها عند قيامك بإنشاء سنة مالية جديدة في صفحة التقويمات المالية.</span><span class="sxs-lookup"><span data-stu-id="236ca-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="236ca-136">إذا قمت بتحديد "مالي"، تتوفر الخيارات التالية في حقل تكرار الفترة:</span><span class="sxs-lookup"><span data-stu-id="236ca-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="236ca-137">يقوم الخيار "سنوي" بترحيل إجمالي مبلغ الإهلاك المحسوب بالنسبة للسنة المالية كمبلغ واحد في آخر يوم في السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="236ca-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="236ca-138">تقوم الفترة المالية بترحيل المبلغ الإجمالي للإهلاك المحسوب للسنة المالية، والذي يتراكم في الفترات المالية التي تم تعريفها للتقويم المالي المحدد في صفحة "دفتر الأستاذ"، أو للتقويم المالي المحدد لدفتر أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="236ca-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="236ca-139">مثال لإهلاك القسط المتناقص</span><span class="sxs-lookup"><span data-stu-id="236ca-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="236ca-140">افترض أن سعر امتلاك الأصل الثابت هو 11000، وقيمة الخردة هي 1000، وعامل النسبة المئوية للإهلاك هو 30.</span><span class="sxs-lookup"><span data-stu-id="236ca-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="236ca-141">باستخدام طريقة "تقليل الرصيد‬"، سيتم حساب 30 بالمئة من أساس الإهلاك (صافي القيمة الدفترية ناقص قيمة الخردة) في نهاية فترة الإهلاك السابقة.</span><span class="sxs-lookup"><span data-stu-id="236ca-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="236ca-142">والإهلاك بالنسبة لأول ثلاث سنوات مبين في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="236ca-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="236ca-143">الفترة</span><span class="sxs-lookup"><span data-stu-id="236ca-143">Period</span></span> | <span data-ttu-id="236ca-144">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="236ca-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="236ca-145">صافي القيمة الدفترية في نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="236ca-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="236ca-146">السنة الأولى</span><span class="sxs-lookup"><span data-stu-id="236ca-146">Year 1</span></span> | <span data-ttu-id="236ca-147">(11000 - 1000) \* 30% =‏ 3000</span><span class="sxs-lookup"><span data-stu-id="236ca-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="236ca-148">(11000 - 1000) - 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="236ca-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="236ca-149">السنة الثانية</span><span class="sxs-lookup"><span data-stu-id="236ca-149">Year 2</span></span> | <span data-ttu-id="236ca-150">(7000 - 1000) \* 30% =‏ 1800</span><span class="sxs-lookup"><span data-stu-id="236ca-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="236ca-151">(7000 -1800) = 5200</span><span class="sxs-lookup"><span data-stu-id="236ca-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="236ca-152">السنة الثالثة</span><span class="sxs-lookup"><span data-stu-id="236ca-152">Year 3</span></span> | <span data-ttu-id="236ca-153">(5200 - 1000) \* 30% =‏ 1260</span><span class="sxs-lookup"><span data-stu-id="236ca-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="236ca-154">(5200 - 1260) = 3940</span><span class="sxs-lookup"><span data-stu-id="236ca-154">(5,200 - 1,260) = 3,940</span></span>               |

 
-






