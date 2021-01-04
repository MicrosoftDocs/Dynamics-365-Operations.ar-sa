---
title: محتوى "تحليل إنفاق الشراء" في Power BI
description: يصف هذا الموضوع العناصر المضمنة في محتوى "تحليل إنفاق الشراء" في Power BI. وهو يوضح كيفية الوصول إلى التقارير التي تم تضمينها في المحتوى، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3f556cf2e506c57e465c2a86485d2cdd4cf8b65e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680604"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="85325-104">محتوى "تحليل إنفاق الشراء" في Power BI</span><span class="sxs-lookup"><span data-stu-id="85325-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85325-105">يصف هذا الموضوع ما هو مدرج في محتوى **تحليل إنفاق الشراء‬** في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="85325-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="85325-106">وهو يشرح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="85325-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="85325-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="85325-107">Overview</span></span>

<span data-ttu-id="85325-108">تم تصميم محتوى **تحليل إنفاق الشراء** في Power BI لمساعدة مدراء المشتريات والمدراء المسؤولين عن الموازنة على تعقب الإنفاق على الشراء.</span><span class="sxs-lookup"><span data-stu-id="85325-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="85325-109">باستطاعة المدراء تحليل الإنفاق على الشراء بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="85325-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="85325-110">الشراء للسنة حتى تاريخه (حسب مجموعة الموردين والموردين الفرديين، فئة التدبير والمنتجات الفردية، وموقع المورد)</span><span class="sxs-lookup"><span data-stu-id="85325-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="85325-111">تغيير الشراء عام بعد الآخر (حسب مجموعة الموردين وفئة التدبير)</span><span class="sxs-lookup"><span data-stu-id="85325-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="85325-112">يستخدم المحتوى البيانات الخاصة بحركة الشراء ويوفر طريقة عرض إجمالية لأرقام الشراء على مستوى الشركة، وتفاصيل تصنيف إنفاق الشراء بحسب المورد والمنتج.</span><span class="sxs-lookup"><span data-stu-id="85325-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="85325-113">تسلط التقارير الضوء على التغييرات في إنفاق الشراء على مدار الوقت.</span><span class="sxs-lookup"><span data-stu-id="85325-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="85325-114">وبالتالي، يمكن استخدام التقارير لتنبيه المديرين حول اتجاهات الإنفاق الإيجابية والسلبية لموردين فرديين وللمنتجات.</span><span class="sxs-lookup"><span data-stu-id="85325-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="85325-115">بالإضافة إلى ذلك، تُظهر المخططات إنفاق الشراء لفئات تدبير مختلفة ومجموعات موردين مختلفة.</span><span class="sxs-lookup"><span data-stu-id="85325-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="85325-116">وبالتالي، باستطاعة مدراء الفئات والمدراء الإقليميين استخدام المخططات للمساعدة في التعرف على التغييرات في سلوك الإنفاق.</span><span class="sxs-lookup"><span data-stu-id="85325-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="85325-117">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="85325-117">Accessing the Power BI content</span></span>
<span data-ttu-id="85325-118">يظهر محتوى **تحليل إنفاق الشراء** في Power BI في صفحة **تحليل الإنفاق والشراء** (**التدبير والتوريد** \> **الاستعلامات والتقارير** \> **تحليل أداء الشراء** \> **تحليل الإنفاق والشراء‬**).</span><span class="sxs-lookup"><span data-stu-id="85325-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="85325-119">المقاييس المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="85325-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="85325-120">يتضمن المحتوى **تحليل إنفاق الشراء** في Power BI تقريرًا يتكون من مجموعة من المقاييس.</span><span class="sxs-lookup"><span data-stu-id="85325-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="85325-121">هذه المقاييس مرئية مثل المخططات والتجانبات والجداول.</span><span class="sxs-lookup"><span data-stu-id="85325-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="85325-122">توفر المقاطع التالية نظرة عامة على الرسوم المرئية.</span><span class="sxs-lookup"><span data-stu-id="85325-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="85325-123">صفحة تقرير الشراء حسب المورّد</span><span class="sxs-lookup"><span data-stu-id="85325-123">Purchase by vendor report page</span></span>
<span data-ttu-id="85325-124">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="85325-124">**Charts**</span></span>
- <span data-ttu-id="85325-125">أفضل 10 موردين بحسب الشراء (مخطط شريطي مكدس)</span><span class="sxs-lookup"><span data-stu-id="85325-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="85325-126">إجمالي الشراء حسب مجموعة المورد/البلد/الاسم (دليل تخطيط دائري)</span><span class="sxs-lookup"><span data-stu-id="85325-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="85325-127">الشراء حسب مجموعة المورد/ البلد/ الاسم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="85325-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="85325-128">متوسط الشراء حسب مجموعة المورد/ البلد/ الاسم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="85325-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="85325-129">**إطارات متجانبة**</span><span class="sxs-lookup"><span data-stu-id="85325-129">**Tiles**</span></span>
- <span data-ttu-id="85325-130">إجمالي الشراء</span><span class="sxs-lookup"><span data-stu-id="85325-130">Total purchase</span></span>
- <span data-ttu-id="85325-131">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="85325-131">YOY purchase growth</span></span>
- <span data-ttu-id="85325-132">إجمالي عدد المورَّدين</span><span class="sxs-lookup"><span data-stu-id="85325-132">Total # vendors</span></span>
- <span data-ttu-id="85325-133">إجمالي عدد الموردين النشطة</span><span class="sxs-lookup"><span data-stu-id="85325-133">Total # of active vendors</span></span>

<span data-ttu-id="85325-134">**مثال**</span><span class="sxs-lookup"><span data-stu-id="85325-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="85325-135">صفحة تقرير الشراء حسب المنتج</span><span class="sxs-lookup"><span data-stu-id="85325-135">Purchase by product report page</span></span>

<span data-ttu-id="85325-136">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="85325-136">**Charts**</span></span>
- <span data-ttu-id="85325-137">الشراء حسب فئة التدبير/اسم المنتج (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="85325-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="85325-138">إجمالي الشراء حسب فئة التدبير/اسم المنتج (دليل تخطيط دائري)</span><span class="sxs-lookup"><span data-stu-id="85325-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="85325-139">أفضل 10 منتجات بحسب الشراء (مخطط شريطي مكدس)</span><span class="sxs-lookup"><span data-stu-id="85325-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="85325-140">**إطارات متجانبة**</span><span class="sxs-lookup"><span data-stu-id="85325-140">**Tiles**</span></span>
- <span data-ttu-id="85325-141">إجمالي عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="85325-141">Total # of products</span></span></li>
- <span data-ttu-id="85325-142">إجمالي النسبة المئوية للمنتجات النشطة من إجمالي عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="85325-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="85325-143">رقم محاسبة المنتجات لـ 80% من الشراء</span><span class="sxs-lookup"><span data-stu-id="85325-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="85325-144">**مثال**</span><span class="sxs-lookup"><span data-stu-id="85325-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="85325-145">صفحة تقرير الشراء حسب الفترة</span><span class="sxs-lookup"><span data-stu-id="85325-145">Purchase by period report page</span></span>
<span data-ttu-id="85325-146">تعرض هذه الصفحة المشتريات في العام الماضي وهذا العام، والنمو حسب فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="85325-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="85325-147">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="85325-147">**Charts**</span></span> 
- <span data-ttu-id="85325-148">الشراء حسب الشهر/يوم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="85325-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="85325-149">فرق النسبة التراكمي للنسبة المئوية السنوية للشراء (مخطط انحداري)</span><span class="sxs-lookup"><span data-stu-id="85325-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="85325-150">إجمالي نمو النسبة المئوية السنوية للشراء (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="85325-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="85325-151">كشف التدبير (مصفوفة)</span><span class="sxs-lookup"><span data-stu-id="85325-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="85325-152">**إطارات متجانبة**</span><span class="sxs-lookup"><span data-stu-id="85325-152">**Tiles**</span></span>
- <span data-ttu-id="85325-153">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="85325-153">YOY purchase growth</span></span>
- <span data-ttu-id="85325-154">النسبة المئوية السنوية لنمو الشراء %</span><span class="sxs-lookup"><span data-stu-id="85325-154">YOY purchase growth %</span></span>

<span data-ttu-id="85325-155">**مثال**</span><span class="sxs-lookup"><span data-stu-id="85325-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="85325-156">صفحة تقرير الشراء حسب موقع المورّد</span><span class="sxs-lookup"><span data-stu-id="85325-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="85325-157">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="85325-157">**Charts**</span></span>
- <span data-ttu-id="85325-158">الشراء حسب المدينة</span><span class="sxs-lookup"><span data-stu-id="85325-158">Purchase by city</span></span>
- <span data-ttu-id="85325-159">النسبة المئوية السنوية لنمو الشراء %</span><span class="sxs-lookup"><span data-stu-id="85325-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="85325-160">الشراء حسب البلد</span><span class="sxs-lookup"><span data-stu-id="85325-160">Purchase by country</span></span>

<span data-ttu-id="85325-161">**مثال**</span><span class="sxs-lookup"><span data-stu-id="85325-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="85325-162">صفحة تقرير تحليل إنفاق الشراء حسب الوقت</span><span class="sxs-lookup"><span data-stu-id="85325-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="85325-163">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="85325-163">**Charts**</span></span> 
- <span data-ttu-id="85325-164">عام الشراء الحالي حسب الشهر/يوم (مخطط خطي)</span><span class="sxs-lookup"><span data-stu-id="85325-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="85325-165">الشراء للعام الحالي والعام الماضي (تخطيط خطي وعمودي)</span><span class="sxs-lookup"><span data-stu-id="85325-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="85325-166">**مثال**</span><span class="sxs-lookup"><span data-stu-id="85325-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="85325-167">صفحة تقرير تحليل إنفاق الشراء حسب المورّد</span><span class="sxs-lookup"><span data-stu-id="85325-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="85325-168">**مخططات**</span><span class="sxs-lookup"><span data-stu-id="85325-168">**Charts**</span></span> 
- <span data-ttu-id="85325-169">أفضل 10% موردين شراء لنسبة   %من الشراء (قمع)</span><span class="sxs-lookup"><span data-stu-id="85325-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="85325-170">أفضل 10 موردين باستخدام حساب الإنفاق المتزايد للنسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="85325-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="85325-171">أفضل 10 موردين باستخدام حساب الإنفاق المنخفض للنسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="85325-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="85325-172">**مثال‏‎** 
</span><span class="sxs-lookup"><span data-stu-id="85325-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="85325-173">نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="85325-173">Data model and entities</span></span>
<span data-ttu-id="85325-174">تُستخدم البيانات التالية لملء صفحات التقارير في محتوى **تحليل إنفاق الشراء** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="85325-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="85325-175">يتم تمثيل هذه البيانات كقياسات مجمعة تم تجهيزها في مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="85325-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="85325-176">مخزن الكيانات هو قاعدة بيانات Microsoft SQL Server تم تحسينها للتحليلات.</span><span class="sxs-lookup"><span data-stu-id="85325-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="85325-177">لمزيد من المعلومات، راجع [تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="85325-177">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="85325-178">تُعد القياسات التجميعية في هذا المحتوي مجموعة فرعية من القياسات التجميعية التي كانت متوفرة في مكعب الشراء في Microsoft Dynamics AX 2012 وMicrosoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="85325-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="85325-179">للوصول إلى مرحلة قياسات المكعب التجميعية في متجر الكيان، يجب أن تجعلها قابلة للنشر.</span><span class="sxs-lookup"><span data-stu-id="85325-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="85325-180">لمزيد من المعلومات، انظر الإجراء للوصول إلى التشغيل المرحلي للقياسات التجميعية في مخزن الكيانات في[تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="85325-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="85325-181">تتوفر القياسات التجميعية الرئيسية التالية مباشرة من كيان بنود الفاتورة كأساس للمحتوى.</span><span class="sxs-lookup"><span data-stu-id="85325-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="85325-182">الكيان</span><span class="sxs-lookup"><span data-stu-id="85325-182">Entity</span></span>        | <span data-ttu-id="85325-183">القياسات التجميعية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="85325-183">Key aggregate measurements</span></span> | <span data-ttu-id="85325-184">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="85325-184">Data source</span></span>                                 | <span data-ttu-id="85325-185">الحقل</span><span class="sxs-lookup"><span data-stu-id="85325-185">Field</span></span>              | <span data-ttu-id="85325-186">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="85325-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="85325-187">سطور الفاتورة</span><span class="sxs-lookup"><span data-stu-id="85325-187">Invoice lines</span></span> | <span data-ttu-id="85325-188">شراء</span><span class="sxs-lookup"><span data-stu-id="85325-188">Purchase</span></span>                   | <span data-ttu-id="85325-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="85325-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="85325-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="85325-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="85325-191">المبلغ بعملة عملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="85325-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="85325-192">يعرض الجدول التالي القياسات الرئيسية في المحتوى التي يتم حسابها من كيان بنود الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="85325-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="85325-193">المقياس</span><span class="sxs-lookup"><span data-stu-id="85325-193">Measure</span></span>               | <span data-ttu-id="85325-194">حساب</span><span class="sxs-lookup"><span data-stu-id="85325-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85325-195">الشراء في العام الحالي</span><span class="sxs-lookup"><span data-stu-id="85325-195">Purchase current year</span></span> | <span data-ttu-id="85325-196">شراء السنة الحالية = SUM ('بنود الفاتورة'\[الشراء\])</span><span class="sxs-lookup"><span data-stu-id="85325-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="85325-197">شراء العام الماضي</span><span class="sxs-lookup"><span data-stu-id="85325-197">Purchase last year</span></span>    | <span data-ttu-id="85325-198">شراء العام الماضي = CALCULATE(SUM('Invoice lines'\[الشراء\]), SAMEPERIODLASTYEAR(التواريخ\[التاريخ\]))</span><span class="sxs-lookup"><span data-stu-id="85325-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="85325-199">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="85325-199">YOY purchase growth</span></span>   | <span data-ttu-id="85325-200">النسبة المئوية السنوية لنمو الشراء = \[الشراء العام الحالي\] - \[الشراء العام الماضي\]</span><span class="sxs-lookup"><span data-stu-id="85325-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="85325-201">تستخدم الأبعاد الرئيسية التالية في حزمة المحتوى كعوامل تصفية لتقسيم القياسات التجميعية، لتتمكن من تحقيق مستوى أكثر دقة واكتساب معلومات تحليلية أعمق.</span><span class="sxs-lookup"><span data-stu-id="85325-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="85325-202">الكيان</span><span class="sxs-lookup"><span data-stu-id="85325-202">Entity</span></span>                 | <span data-ttu-id="85325-203">أمثلة لهذه السمات</span><span class="sxs-lookup"><span data-stu-id="85325-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="85325-204">الموردون</span><span class="sxs-lookup"><span data-stu-id="85325-204">Vendors</span></span>                | <span data-ttu-id="85325-205">مجموعات الموردين، أو بلد المورد، أو المناطق أو اسم المورد</span><span class="sxs-lookup"><span data-stu-id="85325-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="85325-206">المنتجات</span><span class="sxs-lookup"><span data-stu-id="85325-206">Products</span></span>               | <span data-ttu-id="85325-207">اسم المنتج، اسم المنتج، اسم مجموعات الصنف</span><span class="sxs-lookup"><span data-stu-id="85325-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="85325-208">فئات التدبير</span><span class="sxs-lookup"><span data-stu-id="85325-208">Procurement categories</span></span> | <span data-ttu-id="85325-209">فئة التدبير، أسماء فئات التدبير</span><span class="sxs-lookup"><span data-stu-id="85325-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="85325-210">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="85325-210">Legal entities</span></span>         | <span data-ttu-id="85325-211">اسم الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="85325-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="85325-212">التواريخ</span><span class="sxs-lookup"><span data-stu-id="85325-212">Dates</span></span>                  | <span data-ttu-id="85325-213">التواريخ، المقاصة الخاصة بالسنة</span><span class="sxs-lookup"><span data-stu-id="85325-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="85325-214">بشكل افتراضي، يعرض المحتوى البيانات للسنة التقويمية الجارية.</span><span class="sxs-lookup"><span data-stu-id="85325-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="85325-215">ولكن يمكنك تغيير عامل تصفية البيانات في قسم عوامل تصفية التقارير.</span><span class="sxs-lookup"><span data-stu-id="85325-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="85325-216">يمكنك أيضا تغيير عامل تصفية الشركة.</span><span class="sxs-lookup"><span data-stu-id="85325-216">You can also change the company filter.</span></span>
