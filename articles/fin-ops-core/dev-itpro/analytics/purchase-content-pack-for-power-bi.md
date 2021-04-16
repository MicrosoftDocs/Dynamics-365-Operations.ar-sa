---
title: محتوى "تحليل إنفاق الشراء" في Power BI
description: يصف هذا الموضوع العناصر المضمنة في محتوى "تحليل إنفاق الشراء" في Power BI.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749359"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="4cbd2-103">محتوى "تحليل إنفاق الشراء" في Power BI</span><span class="sxs-lookup"><span data-stu-id="4cbd2-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cbd2-104">يصف هذا الموضوع العناصر المضمنة في محتوى **تحليل إنفاق الشراء** في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="4cbd2-105">وهو يشرح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="4cbd2-106">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="4cbd2-106">Overview</span></span>

<span data-ttu-id="4cbd2-107">تم تصميم محتوى **تحليل إنفاق الشراء** في Power BI لمساعدة مدراء المشتريات والمدراء المسؤولين عن الموازنة على تعقب الإنفاق على الشراء.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="4cbd2-108">باستطاعة المدراء تحليل الإنفاق على الشراء بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="4cbd2-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="4cbd2-109">الشراء للسنة حتى تاريخه (حسب مجموعة الموردين والموردين الفرديين، فئة التدبير والمنتجات الفردية، وموقع المورد)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="4cbd2-110">تغيير الشراء عام بعد الآخر (حسب مجموعة الموردين وفئة التدبير)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="4cbd2-111">يستخدم المحتوى البيانات الخاصة بحركة الشراء ويوفر طريقة عرض إجمالية لأرقام الشراء على مستوى الشركة، وتفاصيل تصنيف إنفاق الشراء بحسب المورد والمنتج.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="4cbd2-112">تسلط التقارير الضوء على التغييرات في إنفاق الشراء على مدار الوقت.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="4cbd2-113">وبالتالي، يمكن استخدام التقارير لتنبيه المديرين حول اتجاهات الإنفاق الإيجابية والسلبية لموردين فرديين وللمنتجات.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="4cbd2-114">بالإضافة إلى ذلك، تُظهر المخططات إنفاق الشراء لفئات تدبير مختلفة ومجموعات موردين مختلفة.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="4cbd2-115">وبالتالي، باستطاعة مدراء الفئات والمدراء الإقليميين استخدام المخططات للمساعدة في التعرف على التغييرات في سلوك الإنفاق.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="4cbd2-116">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="4cbd2-116">Accessing the Power BI content</span></span>
<span data-ttu-id="4cbd2-117">يظهر محتوى **تحليل إنفاق الشراء** في Power BI في صفحة **تحليل الإنفاق والشراء** (**التدبير والتوريد** \> **الاستعلامات والتقارير** \> **تحليل أداء الشراء** \> **تحليل الإنفاق والشراء‬**).</span><span class="sxs-lookup"><span data-stu-id="4cbd2-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="4cbd2-118">المقاييس المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="4cbd2-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="4cbd2-119">يتضمن المحتوى **تحليل إنفاق الشراء** في Power BI تقريرًا يتكون من مجموعة من المقاييس.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="4cbd2-120">هذه المقاييس مرئية مثل المخططات والتجانبات والجداول.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="4cbd2-121">توفر المقاطع التالية نظرة عامة على الرسوم المرئية.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="4cbd2-122">صفحة تقرير الشراء حسب المورّد</span><span class="sxs-lookup"><span data-stu-id="4cbd2-122">Purchase by vendor report page</span></span>
<span data-ttu-id="4cbd2-123">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-123">**Charts**</span></span>
- <span data-ttu-id="4cbd2-124">أفضل 10 موردين بحسب الشراء (مخطط شريطي مكدس)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="4cbd2-125">إجمالي الشراء حسب مجموعة المورد/البلد/الاسم (دليل تخطيط دائري)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="4cbd2-126">الشراء حسب مجموعة المورد/ البلد/ الاسم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="4cbd2-127">متوسط الشراء حسب مجموعة المورد/ البلد/ الاسم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="4cbd2-128">**إطارات متجانبة**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-128">**Tiles**</span></span>
- <span data-ttu-id="4cbd2-129">إجمالي الشراء</span><span class="sxs-lookup"><span data-stu-id="4cbd2-129">Total purchase</span></span>
- <span data-ttu-id="4cbd2-130">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="4cbd2-130">YOY purchase growth</span></span>
- <span data-ttu-id="4cbd2-131">إجمالي عدد المورَّدين</span><span class="sxs-lookup"><span data-stu-id="4cbd2-131">Total # vendors</span></span>
- <span data-ttu-id="4cbd2-132">إجمالي عدد الموردين النشطة</span><span class="sxs-lookup"><span data-stu-id="4cbd2-132">Total # of active vendors</span></span>

<span data-ttu-id="4cbd2-133">**مثال**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="4cbd2-134">صفحة تقرير الشراء حسب المنتج</span><span class="sxs-lookup"><span data-stu-id="4cbd2-134">Purchase by product report page</span></span>

<span data-ttu-id="4cbd2-135">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-135">**Charts**</span></span>
- <span data-ttu-id="4cbd2-136">الشراء حسب فئة التدبير/اسم المنتج (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="4cbd2-137">إجمالي الشراء حسب فئة التدبير/اسم المنتج (دليل تخطيط دائري)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="4cbd2-138">أفضل 10 منتجات بحسب الشراء (مخطط شريطي مكدس)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="4cbd2-139">**إطارات متجانبة**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-139">**Tiles**</span></span>
- <span data-ttu-id="4cbd2-140">إجمالي عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="4cbd2-140">Total # of products</span></span></li>
- <span data-ttu-id="4cbd2-141">إجمالي النسبة المئوية للمنتجات النشطة من إجمالي عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="4cbd2-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="4cbd2-142">رقم محاسبة المنتجات لـ 80% من الشراء</span><span class="sxs-lookup"><span data-stu-id="4cbd2-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="4cbd2-143">**مثال**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="4cbd2-144">صفحة تقرير الشراء حسب الفترة</span><span class="sxs-lookup"><span data-stu-id="4cbd2-144">Purchase by period report page</span></span>
<span data-ttu-id="4cbd2-145">تعرض هذه الصفحة المشتريات في العام الماضي وهذا العام، والنمو حسب فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="4cbd2-146">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-146">**Charts**</span></span> 
- <span data-ttu-id="4cbd2-147">الشراء حسب الشهر/يوم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="4cbd2-148">فرق النسبة التراكمي للنسبة المئوية السنوية للشراء (مخطط انحداري)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="4cbd2-149">إجمالي نمو النسبة المئوية السنوية للشراء (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="4cbd2-150">كشف التدبير (مصفوفة)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="4cbd2-151">**إطارات متجانبة**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-151">**Tiles**</span></span>
- <span data-ttu-id="4cbd2-152">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="4cbd2-152">YOY purchase growth</span></span>
- <span data-ttu-id="4cbd2-153">النسبة المئوية السنوية لنمو الشراء %</span><span class="sxs-lookup"><span data-stu-id="4cbd2-153">YOY purchase growth %</span></span>

<span data-ttu-id="4cbd2-154">**مثال**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="4cbd2-155">صفحة تقرير الشراء حسب موقع المورّد</span><span class="sxs-lookup"><span data-stu-id="4cbd2-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="4cbd2-156">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-156">**Charts**</span></span>
- <span data-ttu-id="4cbd2-157">الشراء حسب المدينة</span><span class="sxs-lookup"><span data-stu-id="4cbd2-157">Purchase by city</span></span>
- <span data-ttu-id="4cbd2-158">النسبة المئوية السنوية لنمو الشراء %</span><span class="sxs-lookup"><span data-stu-id="4cbd2-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="4cbd2-159">الشراء حسب البلد</span><span class="sxs-lookup"><span data-stu-id="4cbd2-159">Purchase by country</span></span>

<span data-ttu-id="4cbd2-160">**مثال**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="4cbd2-161">صفحة تقرير تحليل إنفاق الشراء حسب الوقت</span><span class="sxs-lookup"><span data-stu-id="4cbd2-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="4cbd2-162">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-162">**Charts**</span></span> 
- <span data-ttu-id="4cbd2-163">عام الشراء الحالي حسب الشهر/يوم (مخطط خطي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="4cbd2-164">الشراء للعام الحالي والعام الماضي (تخطيط خطي وعمودي)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="4cbd2-165">**مثال**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="4cbd2-166">صفحة تقرير تحليل إنفاق الشراء حسب المورّد</span><span class="sxs-lookup"><span data-stu-id="4cbd2-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="4cbd2-167">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="4cbd2-167">**Charts**</span></span> 
- <span data-ttu-id="4cbd2-168">أفضل 10% موردين شراء لنسبة   %من الشراء (قمع)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="4cbd2-169">أفضل 10 موردين باستخدام حساب الإنفاق المتزايد للنسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="4cbd2-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="4cbd2-170">أفضل 10 موردين باستخدام حساب الإنفاق المنخفض للنسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="4cbd2-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="4cbd2-171">**مثال‏‎** 
</span><span class="sxs-lookup"><span data-stu-id="4cbd2-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="4cbd2-172">نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="4cbd2-172">Data model and entities</span></span>
<span data-ttu-id="4cbd2-173">تُستخدم البيانات التالية لملء صفحات التقارير في محتوى **تحليل إنفاق الشراء** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="4cbd2-174">يتم تمثيل هذه البيانات كقياسات مجمعة تم تجهيزها في مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="4cbd2-175">مخزن الكيانات هو قاعدة بيانات Microsoft SQL Server تم تحسينها للتحليلات.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="4cbd2-176">لمزيد من المعلومات، راجع [تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="4cbd2-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="4cbd2-177">تُعد القياسات التجميعية في هذا المحتوي مجموعة فرعية من القياسات التجميعية التي كانت متوفرة في مكعب الشراء في Microsoft Dynamics AX 2012 وMicrosoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="4cbd2-178">للوصول إلى مرحلة قياسات المكعب التجميعية في متجر الكيان، يجب أن تجعلها قابلة للنشر.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="4cbd2-179">لمزيد من المعلومات، انظر الإجراء للوصول إلى التشغيل المرحلي للقياسات التجميعية في مخزن الكيانات في[تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="4cbd2-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="4cbd2-180">تتوفر القياسات التجميعية الرئيسية التالية مباشرة من كيان بنود الفاتورة كأساس للمحتوى.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="4cbd2-181">الكيان</span><span class="sxs-lookup"><span data-stu-id="4cbd2-181">Entity</span></span>        | <span data-ttu-id="4cbd2-182">القياسات التجميعية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="4cbd2-182">Key aggregate measurements</span></span> | <span data-ttu-id="4cbd2-183">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="4cbd2-183">Data source</span></span>                                 | <span data-ttu-id="4cbd2-184">الحقل</span><span class="sxs-lookup"><span data-stu-id="4cbd2-184">Field</span></span>              | <span data-ttu-id="4cbd2-185">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4cbd2-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="4cbd2-186">سطور الفاتورة</span><span class="sxs-lookup"><span data-stu-id="4cbd2-186">Invoice lines</span></span> | <span data-ttu-id="4cbd2-187">شراء</span><span class="sxs-lookup"><span data-stu-id="4cbd2-187">Purchase</span></span>                   | <span data-ttu-id="4cbd2-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="4cbd2-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="4cbd2-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="4cbd2-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="4cbd2-190">المبلغ بعملة عملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="4cbd2-191">يعرض الجدول التالي القياسات الرئيسية في المحتوى التي يتم حسابها من كيان بنود الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="4cbd2-192">المقياس</span><span class="sxs-lookup"><span data-stu-id="4cbd2-192">Measure</span></span>               | <span data-ttu-id="4cbd2-193">حساب</span><span class="sxs-lookup"><span data-stu-id="4cbd2-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbd2-194">الشراء في العام الحالي</span><span class="sxs-lookup"><span data-stu-id="4cbd2-194">Purchase current year</span></span> | <span data-ttu-id="4cbd2-195">شراء السنة الحالية = SUM ('بنود الفاتورة'\[الشراء\])</span><span class="sxs-lookup"><span data-stu-id="4cbd2-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="4cbd2-196">شراء العام الماضي</span><span class="sxs-lookup"><span data-stu-id="4cbd2-196">Purchase last year</span></span>    | <span data-ttu-id="4cbd2-197">شراء العام الماضي = CALCULATE(SUM('Invoice lines'\[الشراء\]), SAMEPERIODLASTYEAR(التواريخ\[التاريخ\]))</span><span class="sxs-lookup"><span data-stu-id="4cbd2-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="4cbd2-198">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="4cbd2-198">YOY purchase growth</span></span>   | <span data-ttu-id="4cbd2-199">النسبة المئوية السنوية لنمو الشراء = \[الشراء العام الحالي\] - \[الشراء العام الماضي\]</span><span class="sxs-lookup"><span data-stu-id="4cbd2-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="4cbd2-200">تستخدم الأبعاد الرئيسية التالية في حزمة المحتوى كعوامل تصفية لتقسيم القياسات التجميعية، لتتمكن من تحقيق مستوى أكثر دقة واكتساب معلومات تحليلية أعمق.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="4cbd2-201">الكيان</span><span class="sxs-lookup"><span data-stu-id="4cbd2-201">Entity</span></span>                 | <span data-ttu-id="4cbd2-202">أمثلة لهذه السمات</span><span class="sxs-lookup"><span data-stu-id="4cbd2-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="4cbd2-203">الموردون</span><span class="sxs-lookup"><span data-stu-id="4cbd2-203">Vendors</span></span>                | <span data-ttu-id="4cbd2-204">مجموعات الموردين، أو بلد المورد، أو المناطق أو اسم المورد</span><span class="sxs-lookup"><span data-stu-id="4cbd2-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="4cbd2-205">المنتجات</span><span class="sxs-lookup"><span data-stu-id="4cbd2-205">Products</span></span>               | <span data-ttu-id="4cbd2-206">اسم المنتج، اسم المنتج، اسم مجموعات الصنف</span><span class="sxs-lookup"><span data-stu-id="4cbd2-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="4cbd2-207">فئات التدبير</span><span class="sxs-lookup"><span data-stu-id="4cbd2-207">Procurement categories</span></span> | <span data-ttu-id="4cbd2-208">فئة التدبير، أسماء فئات التدبير</span><span class="sxs-lookup"><span data-stu-id="4cbd2-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="4cbd2-209">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="4cbd2-209">Legal entities</span></span>         | <span data-ttu-id="4cbd2-210">اسم الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="4cbd2-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="4cbd2-211">التواريخ</span><span class="sxs-lookup"><span data-stu-id="4cbd2-211">Dates</span></span>                  | <span data-ttu-id="4cbd2-212">التواريخ، المقاصة الخاصة بالسنة</span><span class="sxs-lookup"><span data-stu-id="4cbd2-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="4cbd2-213">بشكل افتراضي، يعرض المحتوى البيانات للسنة التقويمية الجارية.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="4cbd2-214">ولكن يمكنك تغيير عامل تصفية البيانات في قسم عوامل تصفية التقارير.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="4cbd2-215">يمكنك أيضا تغيير عامل تصفية الشركة.</span><span class="sxs-lookup"><span data-stu-id="4cbd2-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]