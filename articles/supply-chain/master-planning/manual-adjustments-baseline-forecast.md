---
title: "القيام بتسويات يدوية في التنبؤ الأساسي"
description: "يشرح هذا المقال كيف يمكن إجراء التسويات اليدوية على تنبؤ خط أساسي وعرض تفاصيل التنبؤ."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 218374cdb6b5588648422d97c04fb60f26e47ac7
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="c4c86-103">القيام بتسويات يدوية في التنبؤ الأساسي</span><span class="sxs-lookup"><span data-stu-id="c4c86-103">Make manual adjustments to the baseline forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c4c86-104">يشرح هذا المقال كيف يمكن إجراء التسويات اليدوية على تنبؤ خط أساسي وعرض تفاصيل التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c4c86-104">This article explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="c4c86-105">قبل القيام بتسويات يدوية، من المهم أن تفهم بعض المفاهيم على صفحات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="c4c86-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="c4c86-106">الشبكة على صفحة التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="c4c86-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="c4c86-107">تتضمن صفحة **‏‫‏‫التنبؤ بالطلب‬ الذي تمت تسويته‬** الشبكة التي تحتوي على الهيكل التالي:</span><span class="sxs-lookup"><span data-stu-id="c4c86-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="c4c86-108">يعرض العمود الأول الأصناف ومفاتيح توزيع الأصناف والشركات وهكذا، بحيث تم إنشاء التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c4c86-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="c4c86-109">يوفر العنوان الفرعي للصفحة وصفًا لأبعاد التنبؤ الحالي التي تظهر في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="c4c86-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="c4c86-110">على سبيل المثال، إذا كان العنوان الفرعي للصفحة **الشركة/الموقع/مفتاح توزيع الصنف**، وأحد رؤوس الصفوف في الشبكة **USMF / 1 / D\_Alloc**، يظهر هذا الصف التنبؤ لشركة USMF، والموقع 1، ومفتاح توزيع الصنف **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="c4c86-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="c4c86-111">تمثل الأعمدة اللاحقة الفترات الزمنية للتنبؤ الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="c4c86-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="c4c86-112">يُعد رأس صفحة كل عمود هو أول تاريخ للفترة الزمنية للتنبؤ الذي يوضح العمود.</span><span class="sxs-lookup"><span data-stu-id="c4c86-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="c4c86-113">تمثل القيم الموجودة في الخلايا التنبؤ لصنف واحد ومفتاح توزيع الصنف وهكذا، للفترة الزمنية للتنبؤ المحدد.</span><span class="sxs-lookup"><span data-stu-id="c4c86-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-deaggregation"></a><span data-ttu-id="c4c86-114">تجميع التنبؤ وإزالة تجميعه</span><span class="sxs-lookup"><span data-stu-id="c4c86-114">Forecast aggregation and deaggregation</span></span>
<span data-ttu-id="c4c86-115">يظهر العنوان الفرعي للصفحة مستوى تجميع التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c4c86-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="c4c86-116">على سبيل المثال، إذا كان العنوان الفرعي للصفحة هو **الشركة / الموقع / مفتاح التوزيع / رقم الصنف / اللون / الحجم / التكوين / نمط**، لا يوجد تجميع تنبؤ ويظهر التنبؤ على مستوى العنصر وأبعاده.</span><span class="sxs-lookup"><span data-stu-id="c4c86-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="c4c86-117">لتغيير التجميع، استخدم صفحة**تغيير أبعاد التنبؤ**، التي يمكنك فتحها من قائمة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="c4c86-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="c4c86-118">لتعديل التنبؤ، انقر فوق أي من الخلايا المتوفرة، واكتب قيمة التنبؤ المعدل.</span><span class="sxs-lookup"><span data-stu-id="c4c86-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="c4c86-119">تصبح الخلية المحررة غامقة مباشرة للإشارة إلى أن التنبؤ الذي يظهر ليس التنبؤ الذي أنشأته خدمة التنبؤ بالطلب، ولكن تم تعديلها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="c4c86-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="c4c86-120">إذا قمت بتغيير التجميع لجعل الصفحة تظهر بيانات مجمعة بشكل أكبر، فإنه يمكنك استخدام الصفحة **بنود التنبؤ بالطلب** لعرض بنود التنبؤ الفردية التي تشكل التنبؤ المجمع.</span><span class="sxs-lookup"><span data-stu-id="c4c86-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="c4c86-121">على سبيل المثال، لقد قمت بإنشاء التنبؤ على مستوى الصنف، ولكنك تعلم أن الطلب على هذا الصنف سيزيد عبر كافة المواقع بسبب عرض ترويجي أو حدث مماثل آخر.</span><span class="sxs-lookup"><span data-stu-id="c4c86-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="c4c86-122">في هذه الحالة، يمكنك تعيين التجميع إلى **الشركة / مفتاح توزيع الصنف / الصنف** على الصفحة **تغيير أبعاد التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="c4c86-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="c4c86-123">يمكنك ضبط التنبؤ العمومي للصنف عبر كافة المواقع في الشبكة **توقعات الطلب المعدلة**.</span><span class="sxs-lookup"><span data-stu-id="c4c86-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="c4c86-124">لرؤية تأثير التغييرات عبر كافة المواقع، افتح الصفحة **بنود التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="c4c86-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="c4c86-125">في هذه الصفحة، سترى سطر واحد للصنف لكل موقع وكمية التنبؤ المعدل وكمية التنبؤ الأصلي.</span><span class="sxs-lookup"><span data-stu-id="c4c86-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="c4c86-126">عندما يتم القيام بتسوية الكمية المتوقعة على مستوى مجمع، يستخدم النظام التوزيع المرجح لتوزيع التغيير بين البنود التي تُنشئ التجميع.</span><span class="sxs-lookup"><span data-stu-id="c4c86-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="c4c86-127">يمكنك أيضًا جعل التعديلات اليدوية على صفحة **بنود التنبؤ بالطلب**، عن طريق تعديل إما قيمة **الكمية الإجمالية** أو خلايا **الكمية** في شبكة إلغاء التجميع.</span><span class="sxs-lookup"><span data-stu-id="c4c86-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="c4c86-128">عرض تفاصيل التنبؤ</span><span class="sxs-lookup"><span data-stu-id="c4c86-128">Viewing details of the forecast</span></span>
<span data-ttu-id="c4c86-129">يمكنك فتح صفحة **تفاصيل التنبؤ بالطلب** لعرض مزيد من المعلومات حول التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c4c86-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="c4c86-130">تظهر صفحة **تفاصيل التنبؤ بالطلب** المعلومات التالية في تنسيقات رسومية وجدولية:</span><span class="sxs-lookup"><span data-stu-id="c4c86-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="c4c86-131">الطلب التاريخية الذي يستند إليه توقعات التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c4c86-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="c4c86-132">التنبؤ الحالي الذي يستخدمه التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c4c86-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="c4c86-133">قيم التنبؤ بالطلب والمبالغ التي تم تعديلها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="c4c86-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="c4c86-134">فاصل الثقة للقيم المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="c4c86-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="c4c86-135">نموذج التنبؤ الذي تم استخدامه لإنشاء التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c4c86-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="c4c86-136">إذا كنت تقوم بعرض البيانات المجمعة، سترى قائمة بكافة الأساليب التي تم استخدامها لكافة السلاسل الزمنية المجمعة.</span><span class="sxs-lookup"><span data-stu-id="c4c86-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="c4c86-137">دقة نموذج داخلي (‏‫متوسط الأخطاء النسبية المطلقة‬).</span><span class="sxs-lookup"><span data-stu-id="c4c86-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="c4c86-138">لمزيد من المعلومات حول دقة التنبؤ، راجع [مراقبة دقة التنبؤ](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="c4c86-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="c4c86-139">**ملاحظات:**</span><span class="sxs-lookup"><span data-stu-id="c4c86-139">**Notes:**</span></span>

-   <span data-ttu-id="c4c86-140">فاصل الثقة الذي يظهر في قسم **التنبؤ** من الصفحة يمثل الفرق بين الحد الأعلى لفاصل الثقة والحد الأدنى لفاصل الثقة.</span><span class="sxs-lookup"><span data-stu-id="c4c86-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="c4c86-141">لعرض القيم للحدود العليا والسفلية، قم بالمرور فوق التخطيط في القسم **‏‫التنبؤ والطلب التاريخي بشكل رسومي‬**.</span><span class="sxs-lookup"><span data-stu-id="c4c86-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="c4c86-142">إذا كنت تستخدم التنبؤ بالطلب في تطبيق Finance and Operations لخدمة التعلم الآلي من Microsoft Azure، يمكنك تحديد نسبة مئوية لمستوى الثقة الذي ينبغي أن يتمتع به التنبؤ الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="c4c86-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="c4c86-143">فاصل الثقة يتكون من مجموعة من القيم التي تعمل كتقديرات جيدة للتنبؤ بالطلب.</span><span class="sxs-lookup"><span data-stu-id="c4c86-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="c4c86-144">تشير النسبة المئوية لمستوى الثقة بنسبة 95% إلى وجود فرصة مخاطرة بنسبة 5% بخروج التنبؤ بالطلب من نطاق فاصل الثقة.</span><span class="sxs-lookup"><span data-stu-id="c4c86-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="c4c86-145">يمكن أيضًا إجراء التسويات اليدوية للتنبؤ على الصفحة **تفاصيل التنبؤ بالطلب** عن طريق تعديل القيم في الصف **التنبؤ** في القسم **التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="c4c86-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="see-also"></a><span data-ttu-id="c4c86-146">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="c4c86-146">See also</span></span>
--------

[<span data-ttu-id="c4c86-147">مراقبة دقة التنبؤ</span><span class="sxs-lookup"><span data-stu-id="c4c86-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="c4c86-148">إنشاء التنبؤ الأساسي الإحصائي</span><span class="sxs-lookup"><span data-stu-id="c4c86-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)




