---
title: محتوى "تحليل إنفاق الشراء" في Power BI
description: يصف هذا الموضوع العناصر المضمنة في محتوى "تحليل إنفاق الشراء" في Power BI. وهو يوضح كيفية الوصول إلى التقارير التي تم تضمينها في المحتوى، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "313832"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="1d01b-104">محتوى "تحليل إنفاق الشراء" في Power BI</span><span class="sxs-lookup"><span data-stu-id="1d01b-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d01b-105">يصف هذا الموضوع ما هو مدرج في محتوى **تحليل إنفاق الشراء‬** في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="1d01b-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="1d01b-106">وهو يشرح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="1d01b-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="1d01b-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1d01b-107">Overview</span></span>

<span data-ttu-id="1d01b-108">تم تصميم محتوى **تحليل إنفاق الشراء** في Power BI لمساعدة مدراء المشتريات والمدراء المسؤولين عن الموازنة على مراقبة الإنفاق على الشراء.</span><span class="sxs-lookup"><span data-stu-id="1d01b-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="1d01b-109">باستطاعة المدراء تحليل الإنفاق على الشراء بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="1d01b-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="1d01b-110">الشراء للسنة حتى تاريخه (حسب مجموعة الموردين والموردين الفرديين، فئة التدبير والمنتجات الفردية، وموقع المورد)</span><span class="sxs-lookup"><span data-stu-id="1d01b-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="1d01b-111">تغيير الشراء عام بعد الآخر (حسب مجموعة الموردين وفئة التدبير)</span><span class="sxs-lookup"><span data-stu-id="1d01b-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="1d01b-112">يستخدم المحتوى البيانات الخاصة بحركة الشراء ويوفر طريقة عرض إجمالية لأرقام الشراء على مستوى الشركة، وتفاصيل تصنيف إنفاق الشراء بحسب المورد والمنتج.</span><span class="sxs-lookup"><span data-stu-id="1d01b-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="1d01b-113">تسلط التقارير الضوء على التغييرات في إنفاق الشراء على مدار الوقت.</span><span class="sxs-lookup"><span data-stu-id="1d01b-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="1d01b-114">وبالتالي، يمكن استخدام التقارير لتنبيه المديرين حول اتجاهات الإنفاق الإيجابية والسلبية لموردين فرديين وللمنتجات.</span><span class="sxs-lookup"><span data-stu-id="1d01b-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="1d01b-115">بالإضافة إلى ذلك، تُظهر المخططات إنفاق الشراء لفئات تدبير مختلفة ومجموعات موردين مختلفة.</span><span class="sxs-lookup"><span data-stu-id="1d01b-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="1d01b-116">وبالتالي، باستطاعة مدراء الفئات والمدراء الإقليميين استخدام المخططات للمساعدة في التعرف على التغييرات في سلوك الإنفاق.</span><span class="sxs-lookup"><span data-stu-id="1d01b-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="1d01b-117">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="1d01b-117">Accessing the Power BI content</span></span>
<span data-ttu-id="1d01b-118">يظهر محتوى **تحليل إنفاق الشراء** في Power BI في صفحة **تحليل الإنفاق والشراء** (**التدبير والتوريد** \> **الاستعلامات والتقارير** \> **تحليل أداء الشراء** \> **تحليل الإنفاق والشراء‬**).</span><span class="sxs-lookup"><span data-stu-id="1d01b-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="1d01b-119">المقاييس المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="1d01b-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="1d01b-120">يتضمن المحتوى **تحليل إنفاق الشراء** في Power BI تقريرًا يتكون من مجموعة من المقاييس.</span><span class="sxs-lookup"><span data-stu-id="1d01b-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="1d01b-121">هذه المقاييس مرئية مثل المخططات والتجانبات والجداول.</span><span class="sxs-lookup"><span data-stu-id="1d01b-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="1d01b-122">يوفر الجدول التالي نظرة عامة على الرسوم المرئية.</span><span class="sxs-lookup"><span data-stu-id="1d01b-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1d01b-123">صفحة التقرير</span><span class="sxs-lookup"><span data-stu-id="1d01b-123">Report page</span></span></th>
<th><span data-ttu-id="1d01b-124">مخططات</span><span class="sxs-lookup"><span data-stu-id="1d01b-124">Charts</span></span></th>
<th><span data-ttu-id="1d01b-125">إطارات متجانبة</span><span class="sxs-lookup"><span data-stu-id="1d01b-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d01b-126">الشراء حسب المورد</span><span class="sxs-lookup"><span data-stu-id="1d01b-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="1d01b-127">أفضل 10 موردين بحسب الشراء (مخطط شريطي مكدس)</span><span class="sxs-lookup"><span data-stu-id="1d01b-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="1d01b-128">إجمالي الشراء حسب مجموعة المورد/البلد/الاسم (دليل تخطيط دائري)</span><span class="sxs-lookup"><span data-stu-id="1d01b-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="1d01b-129">الشراء حسب مجموعة المورد/ البلد/ الاسم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="1d01b-130">متوسط الشراء حسب مجموعة المورد/ البلد/ الاسم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1d01b-131">إجمالي الشراء</span><span class="sxs-lookup"><span data-stu-id="1d01b-131">Total purchase</span></span></li>
<li><span data-ttu-id="1d01b-132">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="1d01b-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="1d01b-133">إجمالي عدد المورَّدين</span><span class="sxs-lookup"><span data-stu-id="1d01b-133">Total # vendors</span></span></li>
<li><span data-ttu-id="1d01b-134">إجمالي عدد الموردين النشطة</span><span class="sxs-lookup"><span data-stu-id="1d01b-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="1d01b-135">الشراء حسب المنتج</span><span class="sxs-lookup"><span data-stu-id="1d01b-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="1d01b-136">الشراء حسب فئة التدبير/اسم المنتج (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="1d01b-137">إجمالي الشراء حسب فئة التدبير/اسم المنتج (دليل تخطيط دائري)</span><span class="sxs-lookup"><span data-stu-id="1d01b-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="1d01b-138">أفضل 10 منتجات بحسب الشراء (مخطط شريطي مكدس)</span><span class="sxs-lookup"><span data-stu-id="1d01b-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1d01b-139">إجمالي عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="1d01b-139">Total # of products</span></span></li>
<li><span data-ttu-id="1d01b-140">إجمالي النسبة المئوية للمنتجات النشطة من إجمالي عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="1d01b-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="1d01b-141">رقم محاسبة المنتجات لـ 80% من الشراء</span><span class="sxs-lookup"><span data-stu-id="1d01b-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="1d01b-142">الشراء حسب الفترة\*</span><span class="sxs-lookup"><span data-stu-id="1d01b-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="1d01b-143">الشراء حسب الشهر/يوم (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="1d01b-144">فرق النسبة التراكمي للنسبة المئوية السنوية للشراء (مخطط انحداري)</span><span class="sxs-lookup"><span data-stu-id="1d01b-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="1d01b-145">إجمالي نمو النسبة المئوية السنوية للشراء (مخطط عمودي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="1d01b-146">كشف التدبير (مصفوفة)</span><span class="sxs-lookup"><span data-stu-id="1d01b-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1d01b-147">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="1d01b-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="1d01b-148">النسبة المئوية السنوية لنمو الشراء %</span><span class="sxs-lookup"><span data-stu-id="1d01b-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="1d01b-149">الشراء حسب موقع المورد</span><span class="sxs-lookup"><span data-stu-id="1d01b-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="1d01b-150">الشراء حسب المدينة</span><span class="sxs-lookup"><span data-stu-id="1d01b-150">Purchase by city</span></span></li>
<li><span data-ttu-id="1d01b-151">النسبة المئوية السنوية لنمو الشراء %</span><span class="sxs-lookup"><span data-stu-id="1d01b-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="1d01b-152">الشراء حسب البلد</span><span class="sxs-lookup"><span data-stu-id="1d01b-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="1d01b-153">تحليل إنفاق الشراء حسب الوقت</span><span class="sxs-lookup"><span data-stu-id="1d01b-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="1d01b-154">عام الشراء الحالي حسب الشهر/يوم (مخطط خطي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="1d01b-155">الشراء للعام الحالي والعام الماضي (تخطيط خطي وعمودي)</span><span class="sxs-lookup"><span data-stu-id="1d01b-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="1d01b-156">تحليل إنفاق الشراء حسب المورد</span><span class="sxs-lookup"><span data-stu-id="1d01b-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="1d01b-157">أفضل 10% موردين شراء لنسبة   %من الشراء (قمع)</span><span class="sxs-lookup"><span data-stu-id="1d01b-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="1d01b-158">أفضل 10 موردين باستخدام حساب الإنفاق المتزايد للنسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="1d01b-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="1d01b-159">أفضل 10 موردين باستخدام حساب الإنفاق المنخفض للنسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="1d01b-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1d01b-160">\* الشراء في العام الماضي وهذا العام، والنمو حسب فئة التدبير</span><span class="sxs-lookup"><span data-stu-id="1d01b-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="1d01b-161">نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="1d01b-161">Data model and entities</span></span>
<span data-ttu-id="1d01b-162">تُستخدم البيانات التالية لملء صفحات التقارير في محتوى **تحليل إنفاق الشراء** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="1d01b-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="1d01b-163">يتم تمثيل هذه البيانات كقياسات مجمعة تم تجهيزها في مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="1d01b-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="1d01b-164">مخزن الكيانات هو قاعدة بيانات Microsoft SQL Server تم تحسينها للتحليلات.</span><span class="sxs-lookup"><span data-stu-id="1d01b-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="1d01b-165">لمزيد من المعلومات، راجع [نظرة عامة عن تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="1d01b-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="1d01b-166">تُعد القياسات التجميعية في هذا المحتوي مجموعة فرعية من القياسات التجميعية التي كانت متوفرة في مكعب الشراء في Microsoft Dynamics AX 2012 وMicrosoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="1d01b-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="1d01b-167">للوصول إلى مرحلة قياسات المكعب التجميعية في متجر الكيان، يجب أن تجعلها قابلة للنشر.</span><span class="sxs-lookup"><span data-stu-id="1d01b-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="1d01b-168">لمزيد من المعلومات، انظر الإجراء للوصول إلى التشغيل المرحلي للقياسات التجميعية في مخزن الكيانات في [نظرة عامة على تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="1d01b-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="1d01b-169">تتوفر القياسات التجميعية الرئيسية التالية مباشرة من كيان بنود الفاتورة كأساس للمحتوى.</span><span class="sxs-lookup"><span data-stu-id="1d01b-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="1d01b-170">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d01b-170">Entity</span></span>        | <span data-ttu-id="1d01b-171">القياسات التجميعية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="1d01b-171">Key aggregate measurements</span></span> | <span data-ttu-id="1d01b-172">مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="1d01b-172">Data source</span></span>                                 | <span data-ttu-id="1d01b-173">الحقل</span><span class="sxs-lookup"><span data-stu-id="1d01b-173">Field</span></span>              | <span data-ttu-id="1d01b-174">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="1d01b-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="1d01b-175">سطور الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1d01b-175">Invoice lines</span></span> | <span data-ttu-id="1d01b-176">شراء</span><span class="sxs-lookup"><span data-stu-id="1d01b-176">Purchase</span></span>                   | <span data-ttu-id="1d01b-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="1d01b-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="1d01b-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="1d01b-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="1d01b-179">المبلغ بعملة عملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="1d01b-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="1d01b-180">يعرض الجدول التالي القياسات الرئيسية في المحتوى التي يتم حسابها من كيان بنود الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="1d01b-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="1d01b-181">المقياس</span><span class="sxs-lookup"><span data-stu-id="1d01b-181">Measure</span></span>               | <span data-ttu-id="1d01b-182">حساب</span><span class="sxs-lookup"><span data-stu-id="1d01b-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d01b-183">الشراء في العام الحالي</span><span class="sxs-lookup"><span data-stu-id="1d01b-183">Purchase current year</span></span> | <span data-ttu-id="1d01b-184">شراء السنة الحالية = SUM ('بنود الفاتورة'\[الشراء\])</span><span class="sxs-lookup"><span data-stu-id="1d01b-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="1d01b-185">شراء العام الماضي</span><span class="sxs-lookup"><span data-stu-id="1d01b-185">Purchase last year</span></span>    | <span data-ttu-id="1d01b-186">شراء العام الماضي = CALCULATE(SUM('Invoice lines'\[الشراء\]), SAMEPERIODLASTYEAR(التواريخ\[التاريخ\]))</span><span class="sxs-lookup"><span data-stu-id="1d01b-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="1d01b-187">النسبة المئوية السنوية لنمو الشراء</span><span class="sxs-lookup"><span data-stu-id="1d01b-187">YOY purchase growth</span></span>   | <span data-ttu-id="1d01b-188">النسبة المئوية السنوية لنمو الشراء = \[الشراء العام الحالي\] - \[الشراء العام الماضي\]</span><span class="sxs-lookup"><span data-stu-id="1d01b-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="1d01b-189">تستخدم الأبعاد الرئيسية التالية في حزمة المحتوى كعوامل تصفية لتقسيم القياسات التجميعية، لتتمكن من تحقيق مستوى أكثر دقة واكتساب معلومات تحليلية أعمق.</span><span class="sxs-lookup"><span data-stu-id="1d01b-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="1d01b-190">الكيان</span><span class="sxs-lookup"><span data-stu-id="1d01b-190">Entity</span></span>                 | <span data-ttu-id="1d01b-191">أمثلة لهذه السمات</span><span class="sxs-lookup"><span data-stu-id="1d01b-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="1d01b-192">الموردون</span><span class="sxs-lookup"><span data-stu-id="1d01b-192">Vendors</span></span>                | <span data-ttu-id="1d01b-193">مجموعات الموردين، أو بلد المورد، أو المناطق أو اسم المورد</span><span class="sxs-lookup"><span data-stu-id="1d01b-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="1d01b-194">المنتجات</span><span class="sxs-lookup"><span data-stu-id="1d01b-194">Products</span></span>               | <span data-ttu-id="1d01b-195">اسم المنتج، اسم المنتج، اسم مجموعات الصنف</span><span class="sxs-lookup"><span data-stu-id="1d01b-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="1d01b-196">فئات التدبير</span><span class="sxs-lookup"><span data-stu-id="1d01b-196">Procurement categories</span></span> | <span data-ttu-id="1d01b-197">فئة التدبير، أسماء فئات التدبير</span><span class="sxs-lookup"><span data-stu-id="1d01b-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="1d01b-198">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="1d01b-198">Legal entities</span></span>         | <span data-ttu-id="1d01b-199">اسم الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="1d01b-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="1d01b-200">التواريخ</span><span class="sxs-lookup"><span data-stu-id="1d01b-200">Dates</span></span>                  | <span data-ttu-id="1d01b-201">التواريخ، المقاصة الخاصة بالسنة</span><span class="sxs-lookup"><span data-stu-id="1d01b-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="1d01b-202">بشكل افتراضي، يعرض المحتوى البيانات للسنة التقويمية الجارية.</span><span class="sxs-lookup"><span data-stu-id="1d01b-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="1d01b-203">ولكن يمكنك تغيير عامل تصفية البيانات في قسم عوامل تصفية التقارير.</span><span class="sxs-lookup"><span data-stu-id="1d01b-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="1d01b-204">يمكنك أيضا تغيير عامل تصفية الشركة.</span><span class="sxs-lookup"><span data-stu-id="1d01b-204">You can also change the company filter.</span></span>
