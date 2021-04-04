---
title: إنشاء تنبؤ أساسي
description: بإمكان مخطط الإنتاج إنشاء تنبؤ أساسي عن طريق استخدام نماذج تنبؤ التسلسل الزمني أو نسخ الطلب التاريخي.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f18da9563421e7e092869451376e53a450abdf7e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246707"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="b5ec3-103">إنشاء تنبؤ أساسي</span><span class="sxs-lookup"><span data-stu-id="b5ec3-103">Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5ec3-104">بإمكان مخطط الإنتاج إنشاء تنبؤ أساسي عن طريق استخدام نماذج تنبؤ التسلسل الزمني أو نسخ الطلب التاريخي.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="b5ec3-105">يوضح هذا الإجراء كيفية نسخ الطلب التاريخي لإنشاء تنبؤ أساسي لكافة المنتجات باستخدام مفتاح توزيع صنف واحد.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="b5ec3-106">إعداد مفتاح توزيع صنف</span><span class="sxs-lookup"><span data-stu-id="b5ec3-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="b5ec3-107">انتقل إلى التخطيط الرئيسي‬ > إعداد > مجموعات التخطيط بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="b5ec3-108">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b5ec3-109">على سبيل المثال، قم بإجراء التصفية على حقل الاسم بقيمة '10'.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="b5ec3-110">يتم تشغيل التنبؤ بالطلب عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="b5ec3-111">ولهذا السبب تحتاج إلى إعداد كافة الشركات التي تريد إنشاء تنبؤات لها في مجموعة تخطيط بين الشركات الشقيقة‬.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="b5ec3-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b5ec3-113">انقر فوق "مفاتيح توزيع الأصناف".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="b5ec3-114">حدد كافة مفاتيح توزيع الأصناف التي تريد إنشاء تنبؤات لها.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="b5ec3-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b5ec3-116">حدد مفتاح توزيع الصنف D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="b5ec3-117">انقر فوق >.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-117">Click >.</span></span>
7. <span data-ttu-id="b5ec3-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-118">Close the page.</span></span>
8. <span data-ttu-id="b5ec3-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="b5ec3-120">إعداد معلمات التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="b5ec3-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="b5ec3-121">انتقل إلى ‏‫التخطيط الرئيسي > إعداد > التنبؤ بالطلب‬ > محددات التنبؤ بالطلب‬.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="b5ec3-122">قم بتوسيع المقطع "محددات خوارزمية التنبؤ‬".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="b5ec3-123">في الحقل "إستراتيجية إنشاء ‏‫التنبؤ‬"، حدد "نسخ فوق الطلب التاريخي‬".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="b5ec3-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="b5ec3-125">إنشاء تنبؤ أساسي</span><span class="sxs-lookup"><span data-stu-id="b5ec3-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="b5ec3-126">انتقل إلى ‏‫التخطيط الرئيسي > تنبؤ‬ > التنبؤ بالطلب > إنشاء التنبؤ الأساسي الإحصائي‬.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="b5ec3-127">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="b5ec3-128">إذا كان لديك أوامر مبيعات بدءًا من 1 كانون الثاني/يناير 2015، فأدخل هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="b5ec3-129">إذا لم تكن موجودة، فأدخل أبكر تاريخ لأوامر المبيعات لديك.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="b5ec3-130">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="b5ec3-131">أدخل آخر تاريخ لأوامر المبيعات لديك، على سبيل المثال "31-03-2015.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="b5ec3-132">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="b5ec3-133">أدخل "01-04-2015".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="b5ec3-134">سيتم حساب هذا التاريخ تلقائيًا كتاريخ البدء التالي للفترة الزمنية‬ للتنبؤ‬‬.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="b5ec3-135">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="b5ec3-136">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-136">Click Filter.</span></span>
7. <span data-ttu-id="b5ec3-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b5ec3-138">ضع علامة على الصف حيث الحقل = مجموعة التخطيط بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="b5ec3-139">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b5ec3-140">اكتب مجموعة التخطيط بين الشركات الشقيقة، على سبيل المثال، 10، التي استخدمتها في المهمة الأولى.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="b5ec3-141">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b5ec3-142">حدد الصف حيث الحقل = مفتاح توزيع الصنف.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="b5ec3-143">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="b5ec3-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-144">Click OK.</span></span>
12. <span data-ttu-id="b5ec3-145">وسّع المقطع "المحددات المتقدمة‬".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="b5ec3-146">في حقل "الفترة الزمنية‬ للتنبؤ‬‬، حدد "شهر".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="b5ec3-147">في الحقل "أفق التنبؤ‬"، أدخل "3".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="b5ec3-148">في الحقل "الحد الزمني للتجمد‬‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="b5ec3-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="b5ec3-150">تصوّر التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="b5ec3-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="b5ec3-151">انتقل إلى ‏‫التخطيط الرئيسي > تنبؤ‬ > التنبؤ بالطلب > ‏‫‏‫التنبؤ بالطلب‬ الذي تمت تسويته‬.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="b5ec3-152">في جدول طريقة العرض المجمعة، حدد الخلية في الصف 1، العمود 2.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="b5ec3-153">هذا هو الشهر الثاني الذي قمت بإنشاء تنبؤ له.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="b5ec3-154">عيّن QtyCell إلى "400".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="b5ec3-155">في الخلية، أدخل رقمًا مختلفًا عن الرقم الذي تم توقعه، على سبيل المثال، 400.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="b5ec3-156">لقد قمت بإجراء تسوية يدوية للتنبؤ.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="b5ec3-157">لاحظ المؤشر الرسومي في الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="b5ec3-158">انقر فوق "تفاصيل بنود التنبؤ".</span><span class="sxs-lookup"><span data-stu-id="b5ec3-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="b5ec3-159">في هذه الصفحة، يمكنك مشاهدة قيم الدقة والطلب التاريخية والتنبؤ.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="b5ec3-160">يمكنك أيضً إدخال تغييرات على التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="b5ec3-160">You can make changes to the forecast as well.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]