---
title: الإهلاك اليدوي
description: توفر هذه المقالة نظرة عامة على أسلوب الإهلاك اليدوي.
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
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187212"
---
# <a name="manual-depreciation"></a><span data-ttu-id="32a82-103">الإهلاك اليدوي</span><span class="sxs-lookup"><span data-stu-id="32a82-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32a82-104">توفر هذه المقالة نظرة عامة على أسلوب الإهلاك اليدوي.</span><span class="sxs-lookup"><span data-stu-id="32a82-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="32a82-105">عند تحديد ملف تعريف إهلاك أصول ثابتة ثم تحديد **يدوي** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، فإنه يتم تحديد إهلاك الأصول الثابتة المعينة لملف تعريف الإهلاك هذا بالنسبة المئوية التي يتم إدخالها لكل فترة زمنية في سنة التقويم.</span><span class="sxs-lookup"><span data-stu-id="32a82-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="32a82-106">ويتم ترحيل الفترات الزمنية التي تقوم بإعداد النسب المئوية لها وفقًا للقيمة التي تحددها في حقل **تكرار الفترة** في علامة التبويب السريع **عام** في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="32a82-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="32a82-107">وفيما يلي القيم التي يمكن تحديدها:</span><span class="sxs-lookup"><span data-stu-id="32a82-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="32a82-108">سنويًا</span><span class="sxs-lookup"><span data-stu-id="32a82-108">Yearly</span></span>
-   <span data-ttu-id="32a82-109">شهريًا</span><span class="sxs-lookup"><span data-stu-id="32a82-109">Monthly</span></span>
-   <span data-ttu-id="32a82-110">ربع سنوي</span><span class="sxs-lookup"><span data-stu-id="32a82-110">Quarterly</span></span>
-   <span data-ttu-id="32a82-111">نصف سنوي</span><span class="sxs-lookup"><span data-stu-id="32a82-111">Half-Yearly</span></span>
-   <span data-ttu-id="32a82-112">يوميًا</span><span class="sxs-lookup"><span data-stu-id="32a82-112">Daily</span></span>

<span data-ttu-id="32a82-113">بعد تحديد تكرار الفترة، انقر فوق **الجداول اليدوية**، وقم بإعداد نسب مئوية لكل فترة زمنية منفصلة للترحيل.</span><span class="sxs-lookup"><span data-stu-id="32a82-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="32a82-114">وتحدد الجداول اليدوية بالاشتراك مع فترات الترحيل مبلغ الإهلاك، كما هو موضح في الأمثلة الواردة لاحقًا في هذا المقال.</span><span class="sxs-lookup"><span data-stu-id="32a82-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="32a82-115">ويتم حساب الإهلاك اليدوي دومًا كنسبة مئوية من سعر الاستحواذ.</span><span class="sxs-lookup"><span data-stu-id="32a82-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="32a82-116">وبالنسبة للإهلاك اليدوي، يجب ألا تبلغ النسب المئوية المدخلة في الفترات الزمنية للإهلاك 100 بالمائة.</span><span class="sxs-lookup"><span data-stu-id="32a82-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="32a82-117">الإهلاك اليدوي عبارة عن طريقة إهلاك مرنة وعادةً ما تُستخدم لتحديد ملف تعريف إهلاك استثنائي في صفحة **الدفاتر**، مثل الإهلاك غير الدوري لأغراض خاصة (على سبيل المثال، الضرائب).</span><span class="sxs-lookup"><span data-stu-id="32a82-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="32a82-118">أمثلة</span><span class="sxs-lookup"><span data-stu-id="32a82-118">Examples</span></span>
<span data-ttu-id="32a82-119">سعر الاستحواذ: 11,000.00 قيمة الخردة المتوقعة: 1,000.00 يعرض الجدول التالي الفترات الزمنية والنسبة المئوية التي تقوم بإعدادها في صفحة **جداول ملف تعريف إهلاك الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="32a82-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="32a82-120">رقم الفترة</span><span class="sxs-lookup"><span data-stu-id="32a82-120">Interval number</span></span> | <span data-ttu-id="32a82-121">النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="32a82-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="32a82-122">1</span><span class="sxs-lookup"><span data-stu-id="32a82-122">1</span></span>               | <span data-ttu-id="32a82-123">10.00</span><span class="sxs-lookup"><span data-stu-id="32a82-123">10.00</span></span>      |
| <span data-ttu-id="32a82-124">2</span><span class="sxs-lookup"><span data-stu-id="32a82-124">2</span></span>               | <span data-ttu-id="32a82-125">50.00</span><span class="sxs-lookup"><span data-stu-id="32a82-125">50.00</span></span>      |
| <span data-ttu-id="32a82-126">3</span><span class="sxs-lookup"><span data-stu-id="32a82-126">3</span></span>               | <span data-ttu-id="32a82-127">8.00</span><span class="sxs-lookup"><span data-stu-id="32a82-127">8.00</span></span>       |

<span data-ttu-id="32a82-128">يتم حساب الإهلاك حسب الفترة كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="32a82-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="32a82-129">رقم الفترة</span><span class="sxs-lookup"><span data-stu-id="32a82-129">Interval number</span></span> | <span data-ttu-id="32a82-130">حساب مبلغ الإهلاك السنوي</span><span class="sxs-lookup"><span data-stu-id="32a82-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="32a82-131">صافي القيمة الدفترية بنهاية الفترة</span><span class="sxs-lookup"><span data-stu-id="32a82-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="32a82-132">1</span><span class="sxs-lookup"><span data-stu-id="32a82-132">1</span></span>                | <span data-ttu-id="32a82-133">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="32a82-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="32a82-134">10,000 (11,000 – 1,000)</span><span class="sxs-lookup"><span data-stu-id="32a82-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="32a82-135">2</span><span class="sxs-lookup"><span data-stu-id="32a82-135">2</span></span>                | <span data-ttu-id="32a82-136">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="32a82-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="32a82-137">5,000 (10,000 – 5,000)</span><span class="sxs-lookup"><span data-stu-id="32a82-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="32a82-138">3</span><span class="sxs-lookup"><span data-stu-id="32a82-138">3</span></span>                | <span data-ttu-id="32a82-139">(11,000 – 1,000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="32a82-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="32a82-140">4,200 (5,000 – 800)</span><span class="sxs-lookup"><span data-stu-id="32a82-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="32a82-141">إذا قمت بتحديد **شهري** في حقل **تكرار الفترة**، فقد قمت بإعداد 12 فترة زمنية لجدول يدوي.</span><span class="sxs-lookup"><span data-stu-id="32a82-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="32a82-142">يبين الجدول التالي مبالغ الإهلاك للفترتين الأولى.</span><span class="sxs-lookup"><span data-stu-id="32a82-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="32a82-143">الفاصل الزمني</span><span class="sxs-lookup"><span data-stu-id="32a82-143">Interval</span></span> | <span data-ttu-id="32a82-144">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="32a82-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="32a82-145">يناير</span><span class="sxs-lookup"><span data-stu-id="32a82-145">January</span></span>  | <span data-ttu-id="32a82-146">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="32a82-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="32a82-147">فبراير</span><span class="sxs-lookup"><span data-stu-id="32a82-147">February</span></span> | <span data-ttu-id="32a82-148">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="32a82-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="32a82-149">إذا قمت بتحديد <strong>نصف سنوي</strong> في حقل *<strong><em>تكرارة الفترة</em>*</strong>، فإنك تقوم بإعداد فترتين لجدول يدوي.</span><span class="sxs-lookup"><span data-stu-id="32a82-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="32a82-150">يبين الجدول التالي مبالغ الإهلاك للفترتين الأولتين.</span><span class="sxs-lookup"><span data-stu-id="32a82-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="32a82-151">الفاصل الزمني</span><span class="sxs-lookup"><span data-stu-id="32a82-151">Interval</span></span>    | <span data-ttu-id="32a82-152">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="32a82-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="32a82-153">30 يونيو</span><span class="sxs-lookup"><span data-stu-id="32a82-153">June 30</span></span>     | <span data-ttu-id="32a82-154">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="32a82-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="32a82-155">31 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="32a82-155">December 31</span></span> | <span data-ttu-id="32a82-156">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="32a82-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="32a82-157">ولا ينبغي أن يكون مجموع النسب المئوية لكافة الفترات الزمنية 100.</span><span class="sxs-lookup"><span data-stu-id="32a82-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="32a82-158">ومع ذلك، تتلقى رسالة، إذا لم تكن القيمة في حقل **‬‏‫النسبة المئوية التراكمية** في صفحة **جداول ملف تعريف إهلاك الأصول الثابتة‬‏‫** **100**.</span><span class="sxs-lookup"><span data-stu-id="32a82-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>


