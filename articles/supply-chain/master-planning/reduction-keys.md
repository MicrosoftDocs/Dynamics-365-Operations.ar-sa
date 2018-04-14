---
title: "مفاتيح الخفض"
description: "توفر هذه المقالات أمثلة تعرض كيفية إعداد طريقة الخفض. وهي تتضمن معلومات حول مختلف إعدادات طريقة الخفض ونتائج كل إعداد. يمكنك استخدام طريقة الخفض لتعريف كيفية خفض متطلبات التنبؤ."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6ca65d3c12abd64bef23954b45f73af1bf62f9f3
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="reduction-keys"></a><span data-ttu-id="f84eb-105">مفاتيح الخفض</span><span class="sxs-lookup"><span data-stu-id="f84eb-105">Reduction keys</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f84eb-106">توفر هذه المقالات أمثلة تعرض كيفية إعداد طريقة الخفض.</span><span class="sxs-lookup"><span data-stu-id="f84eb-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="f84eb-107">وهي تتضمن معلومات حول مختلف إعدادات طريقة الخفض ونتائج كل إعداد.</span><span class="sxs-lookup"><span data-stu-id="f84eb-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="f84eb-108">يمكنك استخدام طريقة الخفض لتعريف كيفية خفض متطلبات التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="f84eb-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="f84eb-109">مثال 1: النسبة المئوية - قاعدة خفض التنبؤ بطريقة الخفض</span><span class="sxs-lookup"><span data-stu-id="f84eb-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="f84eb-110">يوضح هذا المثال إلى أي مدى تقلل طريقة خفض من متطلبات التنبؤ بالطلب وفقًا للنسب المئوية والفترات الزمنية التي تم تحديدها باستخدام طريقة الخفض.</span><span class="sxs-lookup"><span data-stu-id="f84eb-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="f84eb-111">في صفحة **طرق الخفض**، قم بإعداد البنود التالية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="f84eb-112">الباقي</span><span class="sxs-lookup"><span data-stu-id="f84eb-112">Change</span></span> | <span data-ttu-id="f84eb-113">الوحدة</span><span class="sxs-lookup"><span data-stu-id="f84eb-113">Unit</span></span>  | <span data-ttu-id="f84eb-114">النسبة</span><span class="sxs-lookup"><span data-stu-id="f84eb-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="f84eb-115">1</span><span class="sxs-lookup"><span data-stu-id="f84eb-115">1</span></span>    | <span data-ttu-id="f84eb-116">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-116">Month</span></span> |   <span data-ttu-id="f84eb-117">100</span><span class="sxs-lookup"><span data-stu-id="f84eb-117">100</span></span>   |
   |   <span data-ttu-id="f84eb-118">2</span><span class="sxs-lookup"><span data-stu-id="f84eb-118">2</span></span>    | <span data-ttu-id="f84eb-119">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-119">Month</span></span> |   <span data-ttu-id="f84eb-120">75</span><span class="sxs-lookup"><span data-stu-id="f84eb-120">75</span></span>    |
   |   <span data-ttu-id="f84eb-121">3</span><span class="sxs-lookup"><span data-stu-id="f84eb-121">3</span></span>    | <span data-ttu-id="f84eb-122">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-122">Month</span></span> |   <span data-ttu-id="f84eb-123">50</span><span class="sxs-lookup"><span data-stu-id="f84eb-123">50</span></span>    |
   |   <span data-ttu-id="f84eb-124">4</span><span class="sxs-lookup"><span data-stu-id="f84eb-124">4</span></span>    | <span data-ttu-id="f84eb-125">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-125">Month</span></span> |   <span data-ttu-id="f84eb-126">25</span><span class="sxs-lookup"><span data-stu-id="f84eb-126">25</span></span>    |


2. <span data-ttu-id="f84eb-127">ربط طريقة الخفض بمجموعة تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="f84eb-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="f84eb-128">في صفحة **الخطط الرئيسية** ، في حقل **قاعدة الخفض** حدد **النسبة المئوية - طريقة الخفض**.</span><span class="sxs-lookup"><span data-stu-id="f84eb-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="f84eb-129">نشاء تنبؤ بطلب بمقدار 1,000 قطعة لكل شهر.</span><span class="sxs-lookup"><span data-stu-id="f84eb-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="f84eb-130">إذا قمت بتشغيل جدولة التنبؤ في 1 يناير، يتم استهلاك متطلبات التنبؤ بالطلب وفقًا للنسب المئوية التي تقوم بإعدادها في صفحة **طرق الخفض**.</span><span class="sxs-lookup"><span data-stu-id="f84eb-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="f84eb-131">يتم تحويل كميات المتطلبات التالية إلى الخطة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="f84eb-132">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-132">Month</span></span>                | <span data-ttu-id="f84eb-133">عدد القطع المطلوبة</span><span class="sxs-lookup"><span data-stu-id="f84eb-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="f84eb-134">يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-134">January</span></span>              | <span data-ttu-id="f84eb-135">0</span><span class="sxs-lookup"><span data-stu-id="f84eb-135">0</span></span>                         |
| <span data-ttu-id="f84eb-136">فبراير</span><span class="sxs-lookup"><span data-stu-id="f84eb-136">February</span></span>             | <span data-ttu-id="f84eb-137">250</span><span class="sxs-lookup"><span data-stu-id="f84eb-137">250</span></span>                       |
| <span data-ttu-id="f84eb-138">مارس</span><span class="sxs-lookup"><span data-stu-id="f84eb-138">March</span></span>                | <span data-ttu-id="f84eb-139">500</span><span class="sxs-lookup"><span data-stu-id="f84eb-139">500</span></span>                       |
| <span data-ttu-id="f84eb-140">أبريل</span><span class="sxs-lookup"><span data-stu-id="f84eb-140">April</span></span>                | <span data-ttu-id="f84eb-141">750</span><span class="sxs-lookup"><span data-stu-id="f84eb-141">750</span></span>                       |
| <span data-ttu-id="f84eb-142">من مايو حتى ديسمبر</span><span class="sxs-lookup"><span data-stu-id="f84eb-142">May through December</span></span> | <span data-ttu-id="f84eb-143">1,000</span><span class="sxs-lookup"><span data-stu-id="f84eb-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="f84eb-144">مثال 2: الحركات - قاعدة خفض التنبؤ بطريقة الخفض</span><span class="sxs-lookup"><span data-stu-id="f84eb-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="f84eb-145">يوضح هذا المثال إلى أي مدى تقلل الأوامر الفعلية التي تحدث أثناء الفترات المحددة بواسطة طريقة الخفض من متطلبات التنبؤ بالطللب.</span><span class="sxs-lookup"><span data-stu-id="f84eb-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="f84eb-146">في صفحة **الخطط الرئيسية** ، في حقل **قاعدة الخفض**، حدد **الحركات - طريقة الخفض**.</span><span class="sxs-lookup"><span data-stu-id="f84eb-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="f84eb-147">توجد أوامر المبيعات التالية في 1 يناير.</span><span class="sxs-lookup"><span data-stu-id="f84eb-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="f84eb-148">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-148">Month</span></span>    | <span data-ttu-id="f84eb-149">عدد القطع المطلوبة</span><span class="sxs-lookup"><span data-stu-id="f84eb-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="f84eb-150">يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-150">January</span></span>  | <span data-ttu-id="f84eb-151">956</span><span class="sxs-lookup"><span data-stu-id="f84eb-151">956</span></span>                      |
| <span data-ttu-id="f84eb-152">فبراير</span><span class="sxs-lookup"><span data-stu-id="f84eb-152">February</span></span> | <span data-ttu-id="f84eb-153">1,176</span><span class="sxs-lookup"><span data-stu-id="f84eb-153">1,176</span></span>                    |
| <span data-ttu-id="f84eb-154">مارس</span><span class="sxs-lookup"><span data-stu-id="f84eb-154">March</span></span>    | <span data-ttu-id="f84eb-155">451</span><span class="sxs-lookup"><span data-stu-id="f84eb-155">451</span></span>                      |
| <span data-ttu-id="f84eb-156">أبريل</span><span class="sxs-lookup"><span data-stu-id="f84eb-156">April</span></span>    | <span data-ttu-id="f84eb-157">119</span><span class="sxs-lookup"><span data-stu-id="f84eb-157">119</span></span>                      |

<span data-ttu-id="f84eb-158">إذا استخدمت نفس التنبؤ بالطلب لعدد 1,000 قطعة لكل شهر، سيتم تحويل كميات المتطلبات التالية إلى الخطة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="f84eb-159">شهر</span><span class="sxs-lookup"><span data-stu-id="f84eb-159">Month</span></span>                | <span data-ttu-id="f84eb-160">عدد القطع المطلوبة</span><span class="sxs-lookup"><span data-stu-id="f84eb-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="f84eb-161">يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-161">January</span></span>              | <span data-ttu-id="f84eb-162">44</span><span class="sxs-lookup"><span data-stu-id="f84eb-162">44</span></span>                        |
| <span data-ttu-id="f84eb-163">فبراير</span><span class="sxs-lookup"><span data-stu-id="f84eb-163">February</span></span>             | <span data-ttu-id="f84eb-164">0</span><span class="sxs-lookup"><span data-stu-id="f84eb-164">0</span></span>                         |
| <span data-ttu-id="f84eb-165">مارس</span><span class="sxs-lookup"><span data-stu-id="f84eb-165">March</span></span>                | <span data-ttu-id="f84eb-166">549</span><span class="sxs-lookup"><span data-stu-id="f84eb-166">549</span></span>                       |
| <span data-ttu-id="f84eb-167">أبريل</span><span class="sxs-lookup"><span data-stu-id="f84eb-167">April</span></span>                | <span data-ttu-id="f84eb-168">881</span><span class="sxs-lookup"><span data-stu-id="f84eb-168">881</span></span>                       |
| <span data-ttu-id="f84eb-169">من مايو حتى ديسمبر</span><span class="sxs-lookup"><span data-stu-id="f84eb-169">May through December</span></span> | <span data-ttu-id="f84eb-170">1,000</span><span class="sxs-lookup"><span data-stu-id="f84eb-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="f84eb-171">مثال 3: الحركات - قاعدة خفض التنبؤ بالفترة الديناميكية</span><span class="sxs-lookup"><span data-stu-id="f84eb-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="f84eb-172">في معظم الحالات، يتم إعداد الأنظمة بحيث تقلل الحركات من التنبؤ بالطلب خلال فترات تنبؤ محددة: الأسابيع، والشهور، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="f84eb-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="f84eb-173">ويتم تحديد هذه الفترات في طريقة الخفض.</span><span class="sxs-lookup"><span data-stu-id="f84eb-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="f84eb-174">ومع ذلك، قد*يعني* الوقت بين بندي التنؤ بالطلب فترة كذلك.</span><span class="sxs-lookup"><span data-stu-id="f84eb-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="f84eb-175">إنشاء طلب تنبؤ للتواريخ والكميات التالية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="f84eb-176">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f84eb-176">Date</span></span>       | <span data-ttu-id="f84eb-177">التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="f84eb-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="f84eb-178">1 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-178">January 1</span></span>  | <span data-ttu-id="f84eb-179">1,000</span><span class="sxs-lookup"><span data-stu-id="f84eb-179">1,000</span></span>           |
   | <span data-ttu-id="f84eb-180">5 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-180">January 5</span></span>  | <span data-ttu-id="f84eb-181">500</span><span class="sxs-lookup"><span data-stu-id="f84eb-181">500</span></span>             |
   | <span data-ttu-id="f84eb-182">12 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-182">January 12</span></span> | <span data-ttu-id="f84eb-183">1,000</span><span class="sxs-lookup"><span data-stu-id="f84eb-183">1,000</span></span>           |

   <span data-ttu-id="f84eb-184">في هذا التنبؤ، لا توجد فترة زمنية واضحة بين تواريخ التنبؤ: هناك فترة أربعة أيام بين التاريخين الأول والثاني، وهناك فترة سبعة أيام بين التاريخ الثاني والثالث.</span><span class="sxs-lookup"><span data-stu-id="f84eb-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="f84eb-185">هذه النطاقات المختلفة هي الفترات الحيوية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="f84eb-186">قم بإنشاء بنود أمر مبيعات على النحو التالي.</span><span class="sxs-lookup"><span data-stu-id="f84eb-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="f84eb-187">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f84eb-187">Date</span></span>                             | <span data-ttu-id="f84eb-188">كمية أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="f84eb-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="f84eb-189">15 كانون الأول/ديسمبر في السنة السابقة</span><span class="sxs-lookup"><span data-stu-id="f84eb-189">December 15 in the previous year</span></span> | <span data-ttu-id="f84eb-190">500</span><span class="sxs-lookup"><span data-stu-id="f84eb-190">500</span></span>                  |
   | <span data-ttu-id="f84eb-191">3 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-191">January 3</span></span>                        | <span data-ttu-id="f84eb-192">100</span><span class="sxs-lookup"><span data-stu-id="f84eb-192">100</span></span>                  |
   | <span data-ttu-id="f84eb-193">10 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-193">January 10</span></span>                       | <span data-ttu-id="f84eb-194">200</span><span class="sxs-lookup"><span data-stu-id="f84eb-194">200</span></span>                  |

<span data-ttu-id="f84eb-195">سيتم تقليل التنبؤ كما يلي:</span><span class="sxs-lookup"><span data-stu-id="f84eb-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="f84eb-196">لا يوجد أمر المبيعات الأول خلال أي فترة، لذا لن يخفض أي تنبؤ.</span><span class="sxs-lookup"><span data-stu-id="f84eb-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="f84eb-197">أمر المبيعات الثاني موجود في الفترة بين 1 كانون الثاني/يناير و5 كانون الثاني/يناير، لذا سيخفض التنبؤ بتاريخ 1 كانون الثاني/يناير بـ 100.</span><span class="sxs-lookup"><span data-stu-id="f84eb-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="f84eb-198">أمر المبيعات الثالث موجود في الفترة بين 5 كانون الثاني/يناير و12 كانون الثاني/يناير، لذا سيخفض التنبؤ لتاريخ 5 كانون الثاني/يناير بـ 200.</span><span class="sxs-lookup"><span data-stu-id="f84eb-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="f84eb-199">سيتم إنشاء الأمر المخطط التالي للوفاء بالتنبؤ.</span><span class="sxs-lookup"><span data-stu-id="f84eb-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="f84eb-200">تاريخ التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="f84eb-200">Demand forecast date</span></span> | <span data-ttu-id="f84eb-201">الكمية المخفضة</span><span class="sxs-lookup"><span data-stu-id="f84eb-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="f84eb-202">1 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-202">January 1</span></span>            | <span data-ttu-id="f84eb-203">900</span><span class="sxs-lookup"><span data-stu-id="f84eb-203">900</span></span>              |
| <span data-ttu-id="f84eb-204">5 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-204">January 5</span></span>            | <span data-ttu-id="f84eb-205">300</span><span class="sxs-lookup"><span data-stu-id="f84eb-205">300</span></span>              |
| <span data-ttu-id="f84eb-206">12 يناير</span><span class="sxs-lookup"><span data-stu-id="f84eb-206">January 12</span></span>           | <span data-ttu-id="f84eb-207">1,000</span><span class="sxs-lookup"><span data-stu-id="f84eb-207">1,000</span></span>            |

<span data-ttu-id="f84eb-208">فيما يلي ملخص لتخفيض **الحركات - الفترة الديناميكية**:</span><span class="sxs-lookup"><span data-stu-id="f84eb-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="f84eb-209">يتم تخفيض متطلبات التنبؤ بحركات الأمر الفعلية التي تحدث خلال الفترة الديناميكية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="f84eb-210">تغطي الفترة الديناميكية تواريخ التنبؤ الحالية وتنتهي عند بداية التنبؤ التالي.</span><span class="sxs-lookup"><span data-stu-id="f84eb-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="f84eb-211">لا تستخدم هذه الطريقة أو تتطلب طريقة خفض.</span><span class="sxs-lookup"><span data-stu-id="f84eb-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="f84eb-212">عند استخدام هذا الخيار، يحدث السلوك التالي:</span><span class="sxs-lookup"><span data-stu-id="f84eb-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="f84eb-213">إذا قل التنبؤ تمامًا، تصبح متطلبات التنبؤ للتنبؤ الحالي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="f84eb-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="f84eb-214">إذا لم يكن هناك أي تنبؤ مستقبلي، يتم تخفيض طلبات التنبؤ من التنبؤ الأخيرة الذي تم إدخاله.</span><span class="sxs-lookup"><span data-stu-id="f84eb-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="f84eb-215">يتم تضمين الحدود الزمنية في عملية حساب خفض التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="f84eb-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="f84eb-216">يتم تضمين الأيام الموجبة في عملية حساب خفض التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="f84eb-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="f84eb-217">إذا تجاوزت حركات الأوامر الفعلية المتطلبات التي تم التنبؤ بها، لا يتم توجيه الحركات المتبقية إلى فترة التنبؤ التالية.</span><span class="sxs-lookup"><span data-stu-id="f84eb-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="f84eb-218">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f84eb-218">See also</span></span>
--------

[<span data-ttu-id="f84eb-219">الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="f84eb-219">Master plans</span></span>](master-plans.md)




