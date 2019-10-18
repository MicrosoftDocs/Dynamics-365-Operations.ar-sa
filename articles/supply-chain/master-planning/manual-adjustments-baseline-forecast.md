---
title: القيام بتسويات يدوية في التنبؤ الأساسي
description: يشرح هذا الموضوع كيف يمكن إجراء التسويات اليدوية على تنبؤ خط أساسي وعرض تفاصيل التنبؤ.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9692dc168e9efb653b20c677cd6e3bb0bd8756
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250704"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="5b85b-103">القيام بتسويات يدوية في التنبؤ الأساسي</span><span class="sxs-lookup"><span data-stu-id="5b85b-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b85b-104">يشرح هذا الموضوع كيف يمكن إجراء التسويات اليدوية على تنبؤ خط أساسي وعرض تفاصيل التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5b85b-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="5b85b-105">قبل القيام بتسويات يدوية، من المهم أن تفهم بعض المفاهيم على صفحات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="5b85b-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="5b85b-106">الشبكة على صفحة التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="5b85b-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="5b85b-107">تتضمن صفحة **‏‫‏‫التنبؤ بالطلب‬ الذي تمت تسويته‬** الشبكة التي تحتوي على الهيكل التالي:</span><span class="sxs-lookup"><span data-stu-id="5b85b-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="5b85b-108">يعرض العمود الأول الأصناف ومفاتيح توزيع الأصناف والشركات وهكذا، بحيث تم إنشاء التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5b85b-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="5b85b-109">يوفر العنوان الفرعي للصفحة وصفًا لأبعاد التنبؤ الحالي التي تظهر في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="5b85b-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="5b85b-110">على سبيل المثال، إذا كان العنوان الفرعي للصفحة **الشركة/الموقع/مفتاح توزيع الصنف**، وأحد رؤوس الصفوف في الشبكة **USMF / 1 / D\_Alloc**، يظهر هذا الصف التنبؤ لشركة USMF، والموقع 1، ومفتاح توزيع الصنف **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="5b85b-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="5b85b-111">تمثل الأعمدة اللاحقة الفترات الزمنية للتنبؤ الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="5b85b-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="5b85b-112">يُعد رأس صفحة كل عمود هو أول تاريخ للفترة الزمنية للتنبؤ الذي يوضح العمود.</span><span class="sxs-lookup"><span data-stu-id="5b85b-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="5b85b-113">تمثل القيم الموجودة في الخلايا التنبؤ لصنف واحد ومفتاح توزيع الصنف وهكذا، للفترة الزمنية للتنبؤ المحدد.</span><span class="sxs-lookup"><span data-stu-id="5b85b-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="5b85b-114">تجميع التنبؤ وإزالة تجميعه</span><span class="sxs-lookup"><span data-stu-id="5b85b-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="5b85b-115">يظهر العنوان الفرعي للصفحة مستوى تجميع التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5b85b-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="5b85b-116">على سبيل المثال، إذا كان العنوان الفرعي للصفحة هو **الشركة / الموقع / مفتاح التوزيع / رقم الصنف / اللون / الحجم / التكوين / نمط**، لا يوجد تجميع تنبؤ ويظهر التنبؤ على مستوى العنصر وأبعاده.</span><span class="sxs-lookup"><span data-stu-id="5b85b-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="5b85b-117">لتغيير التجميع، استخدم صفحة**تغيير أبعاد التنبؤ**، التي يمكنك فتحها من قائمة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="5b85b-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="5b85b-118">لتعديل التنبؤ، انقر فوق أي من الخلايا المتوفرة، واكتب قيمة التنبؤ المعدل.</span><span class="sxs-lookup"><span data-stu-id="5b85b-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="5b85b-119">تصبح الخلية المحررة غامقة مباشرة للإشارة إلى أن التنبؤ الذي يظهر ليس التنبؤ الذي أنشأته خدمة التنبؤ بالطلب، ولكن تم تعديلها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="5b85b-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="5b85b-120">إذا قمت بتغيير التجميع لجعل الصفحة تظهر بيانات مجمعة بشكل أكبر، فإنه يمكنك استخدام الصفحة **بنود التنبؤ بالطلب** لعرض بنود التنبؤ الفردية التي تشكل التنبؤ المجمع.</span><span class="sxs-lookup"><span data-stu-id="5b85b-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="5b85b-121">على سبيل المثال، لقد قمت بإنشاء التنبؤ على مستوى الصنف، ولكنك تعلم أن الطلب على هذا الصنف سيزيد عبر كافة المواقع بسبب عرض ترويجي أو حدث مماثل آخر.</span><span class="sxs-lookup"><span data-stu-id="5b85b-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="5b85b-122">في هذه الحالة، يمكنك تعيين التجميع إلى **الشركة / مفتاح توزيع الصنف / الصنف** على الصفحة **تغيير أبعاد التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="5b85b-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="5b85b-123">يمكنك ضبط التنبؤ العمومي للصنف عبر كافة المواقع في الشبكة **توقعات الطلب المعدلة**.</span><span class="sxs-lookup"><span data-stu-id="5b85b-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="5b85b-124">لرؤية تأثير التغييرات عبر كافة المواقع، افتح الصفحة **بنود التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="5b85b-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="5b85b-125">في هذه الصفحة، سترى سطر واحد للصنف لكل موقع وكمية التنبؤ المعدل وكمية التنبؤ الأصلي.</span><span class="sxs-lookup"><span data-stu-id="5b85b-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="5b85b-126">عندما يتم القيام بتسوية الكمية المتوقعة على مستوى مجمع، يستخدم النظام التوزيع المرجح لتوزيع التغيير بين البنود التي تُنشئ التجميع.</span><span class="sxs-lookup"><span data-stu-id="5b85b-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="5b85b-127">يمكنك أيضًا جعل التعديلات اليدوية على صفحة **بنود التنبؤ بالطلب**، عن طريق تعديل إما قيمة **الكمية الإجمالية** أو خلايا **الكمية** في شبكة إلغاء التجميع.</span><span class="sxs-lookup"><span data-stu-id="5b85b-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="5b85b-128">عرض تفاصيل التنبؤ</span><span class="sxs-lookup"><span data-stu-id="5b85b-128">Viewing details of the forecast</span></span>
<span data-ttu-id="5b85b-129">يمكنك فتح صفحة **تفاصيل التنبؤ بالطلب** لعرض مزيد من المعلومات حول التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5b85b-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="5b85b-130">تظهر صفحة **تفاصيل التنبؤ بالطلب** المعلومات التالية في تنسيقات رسومية وجدولية:</span><span class="sxs-lookup"><span data-stu-id="5b85b-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="5b85b-131">الطلب التاريخية الذي يستند إليه توقعات التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5b85b-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="5b85b-132">التنبؤ الحالي الذي يستخدمه التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="5b85b-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="5b85b-133">قيم التنبؤ بالطلب والمبالغ التي تم تعديلها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="5b85b-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="5b85b-134">فاصل الثقة للقيم المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="5b85b-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="5b85b-135">نموذج التنبؤ الذي تم استخدامه لإنشاء التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5b85b-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="5b85b-136">إذا كنت تقوم بعرض البيانات المجمعة، سترى قائمة بكافة الأساليب التي تم استخدامها لكافة السلاسل الزمنية المجمعة.</span><span class="sxs-lookup"><span data-stu-id="5b85b-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="5b85b-137">دقة نموذج داخلي (‏‫متوسط الأخطاء النسبية المطلقة‬).</span><span class="sxs-lookup"><span data-stu-id="5b85b-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="5b85b-138">لمزيد من المعلومات حول دقة التنبؤ، راجع [مراقبة دقة التنبؤ](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="5b85b-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="5b85b-139">**ملاحظات:**</span><span class="sxs-lookup"><span data-stu-id="5b85b-139">**Notes:**</span></span>

-   <span data-ttu-id="5b85b-140">فاصل الثقة الذي يظهر في قسم **التنبؤ** من الصفحة يمثل الفرق بين الحد الأعلى لفاصل الثقة والحد الأدنى لفاصل الثقة.</span><span class="sxs-lookup"><span data-stu-id="5b85b-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="5b85b-141">لعرض القيم للحدود العليا والسفلية، قم بالمرور فوق التخطيط في القسم **‏‫التنبؤ والطلب التاريخي بشكل رسومي‬**.</span><span class="sxs-lookup"><span data-stu-id="5b85b-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="5b85b-142">إذا كنت تستخدم خدمة التعلم الآلي من Microsoft Azure للتنبؤ بالطلب، يمكنك تحديد النسبة المئوية لمستوى الثقة الذي ينبغي أن يتمتع به التنبؤ الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="5b85b-142">If you use the Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="5b85b-143">فاصل الثقة يتكون من مجموعة من القيم التي تعمل كتقديرات جيدة للتنبؤ بالطلب.</span><span class="sxs-lookup"><span data-stu-id="5b85b-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="5b85b-144">تشير النسبة المئوية لمستوى الثقة بنسبة 95% إلى وجود فرصة مخاطرة بنسبة 5% بخروج التنبؤ بالطلب من نطاق فاصل الثقة.</span><span class="sxs-lookup"><span data-stu-id="5b85b-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="5b85b-145">يمكن أيضًا إجراء التسويات اليدوية للتنبؤ على الصفحة **تفاصيل التنبؤ بالطلب** عن طريق تعديل القيم في الصف **التنبؤ** في القسم **التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="5b85b-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5b85b-146">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5b85b-146">Additional resources</span></span>
--------

[<span data-ttu-id="5b85b-147">مراقبة دقة التنبؤ</span><span class="sxs-lookup"><span data-stu-id="5b85b-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="5b85b-148">إنشاء التنبؤ الأساسي الإحصائي</span><span class="sxs-lookup"><span data-stu-id="5b85b-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



