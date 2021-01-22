---
title: محتوى "أداء الربحية والمبيعات" في Power BI
description: يصف هذا الموضوع العناصر المضمنة في محتوى "أداء الربحية والمبيعات" في Power BI. وهو يشرح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 490a4f6d1bd9f3bdb0af09bd4e6f7f8fb2c92a1b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984264"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a><span data-ttu-id="510f4-104">محتوى "أداء الربحية والمبيعات" في Power BI</span><span class="sxs-lookup"><span data-stu-id="510f4-104">Sales and profitability performance Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="510f4-105">يصف هذا الموضوع العناصر المضمنة في محتوى **أداء الربحية والمبيعات** في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="510f4-105">This topic describes what is included in the **Sales and profitability performance** Microsoft Power BI content.</span></span> <span data-ttu-id="510f4-106">وهو يشرح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="510f4-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="510f4-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="510f4-107">Overview</span></span>

<span data-ttu-id="510f4-108">تم إنشاء محتوى **أداء الربحية والمبيعات** في Power BI لتمكين مدراء المبيعات من مراقبة مقاييس المبيعات الرئيسية للإيراد وإجمالي الربح وهوامش الربح.</span><span class="sxs-lookup"><span data-stu-id="510f4-108">The **Sales and profitability performance** Power BI content was created so that sales managers can monitor the key sales metrics of revenue, gross profit, and profit margins.</span></span> <span data-ttu-id="510f4-109">إنه يستخدم البيانات الخاصة بحركة الشراء، ويوفر طريقة عرض إجمالية لأرقام المبيعات على مستوى الشركة، وتفاصيل أداء المبيعات للعملاء والمنتجات.</span><span class="sxs-lookup"><span data-stu-id="510f4-109">It uses sales transactional data, and provides both an aggregate view of the company-wide sales figures and a breakdown of sales performance for customers and products.</span></span>

<span data-ttu-id="510f4-110">تقوم التقارير بتمييز التغييرات في نمو الإيراد والربح مع مرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="510f4-110">Reports highlight changes in revenue and profit growth over time.</span></span> <span data-ttu-id="510f4-111">وبالتالي، يمكن استخدام التقارير لتنبيه المديرين حول اتجاهات الإنفاق الإيجابية والسلبية لعملاء فرديين ومنتجات فردية.</span><span class="sxs-lookup"><span data-stu-id="510f4-111">Therefore, the reports can be used to alert managers about positive and negative trends for individual customers and products.</span></span> <span data-ttu-id="510f4-112">بالإضافة إلى ذلك، تقارن المخططات الإيراد والربحية لفئات منتجات ومجموعات عملاء مختلفة ببعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="510f4-112">Additionally, charts compare the revenue and profitability of different product categories and customer groups to each other.</span></span> <span data-ttu-id="510f4-113">لذلك، باستطاعة مدراء الفئات والمدراء الإقليميين تحديد الأسهم ذات الأداء الضعيف والأخرى ذات الأداء الجيد.</span><span class="sxs-lookup"><span data-stu-id="510f4-113">Therefore, category and regional managers can identify laggards and leaders.</span></span> <span data-ttu-id="510f4-114">وأخيراً، يرسم تقرير شامل إيراد عميل واحد في مقابل هامش الربح.</span><span class="sxs-lookup"><span data-stu-id="510f4-114">Finally, a comprehensive report plots an individual customer's revenue versus profit margin.</span></span> <span data-ttu-id="510f4-115">ونتيجة لذلك، يتوفر لدى مدراء الحسابات أساسًا تدعمه البيانات، يمكنهم استخدامه لضبط جهودهم من ناحية المبيعات والتسويق حسب ملف كل عميل.</span><span class="sxs-lookup"><span data-stu-id="510f4-115">Therefore, account managers have a data-backed foundation that they can use to tune their sales and marketing efforts to each customer's profile.</span></span>

<span data-ttu-id="510f4-116">يسمح محتوى **أداء الربحية والمبيعات** لمدراء المبيعات تحليل أداء المبيعات من خلال الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="510f4-116">The **Sales and profitability performance** content lets sales managers analyze sales performance in the following ways:</span></span>

- <span data-ttu-id="510f4-117">الإيرادات، للسنة حتى تاريخه (حسب مجموعة العميل والعملاء الفرديين وفئات المبيعات والمنتجات الفردية والمناطق الجغرافية)</span><span class="sxs-lookup"><span data-stu-id="510f4-117">Revenue, year-to-date (by customer group and individual customers, sales categories, and individual products and geographies)</span></span>
- <span data-ttu-id="510f4-118">التغير في الإيراد، عام تلو الآخر (حسب مناطق العملاء وفئات المبيعات)</span><span class="sxs-lookup"><span data-stu-id="510f4-118">Revenue change, year-over-year (by customer regions and sales categories)</span></span>

<span data-ttu-id="510f4-119">يتم تحليل الربحية بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="510f4-119">Profitability can be analyzed in these ways:</span></span>

- <span data-ttu-id="510f4-120">الربح الإجمالي وهامش الربح (حسب مجموعات العملاء وفئات مبيعات المنتج)</span><span class="sxs-lookup"><span data-stu-id="510f4-120">Gross profit and profit margin (by customer groups and product sales categories)</span></span>
- <span data-ttu-id="510f4-121">تغير إجمالي الربح، عام بعد الآخر</span><span class="sxs-lookup"><span data-stu-id="510f4-121">Gross profit change, year-over-year</span></span>
- <span data-ttu-id="510f4-122">ربحية العميل (حسب الإيرادات مقابل إجمالي هامش الربح)</span><span class="sxs-lookup"><span data-stu-id="510f4-122">Customer profitability (by revenue versus gross margin)</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="510f4-123">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="510f4-123">Accessing the Power BI content</span></span>
<span data-ttu-id="510f4-124">يظهر محتوى **أداء المبيعات والربحية** في Power BI في صفحة **أداء المبيعات والربحية** ( **المبيعات والتسويق** \> **الاستعلامات والتقارير** \> **تحليل أداء المبيعات** \> **أداء المبيعات والربحية** ).</span><span class="sxs-lookup"><span data-stu-id="510f4-124">The **Sales and profitability performance** Power BI content is shown on the **Sales and profitability performance** page ( **Sales and marketing** \> **Inquiries and reports** \> **Sales performance analysis** \> **Sales and profitability performance** ).</span></span>

## <a name="metricsthat-are-included-in-the-power-bi-content"></a><span data-ttu-id="510f4-125">المقاييس المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="510f4-125">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="510f4-126">يتضمن محتوى **أداء الربحية والمبيعات** في Power BI تقريرًا يتكون من مجموعة من المقاييس.</span><span class="sxs-lookup"><span data-stu-id="510f4-126">The **Sales and profitability performance** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="510f4-127">هذه المقاييس مرئية مثل المخططات والتجانبات والجداول.</span><span class="sxs-lookup"><span data-stu-id="510f4-127">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="510f4-128">يوفر الجدول التالي نظرة عامة حول مجموعة الرسوم المرئية في المحتوى.</span><span class="sxs-lookup"><span data-stu-id="510f4-128">The following table provides an overview of the visualizations in the content.</span></span>

| <span data-ttu-id="510f4-129">صفحة التقرير</span><span class="sxs-lookup"><span data-stu-id="510f4-129">Report page</span></span>            | <span data-ttu-id="510f4-130">مخططات</span><span class="sxs-lookup"><span data-stu-id="510f4-130">Charts</span></span>                                     | <span data-ttu-id="510f4-131">إطارات متجانبة</span><span class="sxs-lookup"><span data-stu-id="510f4-131">Tiles</span></span>                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="510f4-132">الإيراد حسب العميل</span><span class="sxs-lookup"><span data-stu-id="510f4-132">Revenue by customer</span></span>    | <span data-ttu-id="510f4-133">أفضل 10 عملاء حسب الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-133">Top 10 customers by revenue</span></span>                | <span data-ttu-id="510f4-134">إجمالي الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-134">Total revenue</span></span>                                           |
|                        | <span data-ttu-id="510f4-135">إجمالي الإيرادات حسب مجموعة العملاء</span><span class="sxs-lookup"><span data-stu-id="510f4-135">Total revenue by customer group</span></span>            | <span data-ttu-id="510f4-136">النسبة المئوية السنوية لنمو الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-136">YOY revenue growth</span></span>                                      |
|                        | <span data-ttu-id="510f4-137">متوسط إيراد العميل حسب مجموعة العميل</span><span class="sxs-lookup"><span data-stu-id="510f4-137">Average customer revenue by customer group</span></span> | <span data-ttu-id="510f4-138">إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="510f4-138">Gross margin</span></span>                                            |
|                        | <span data-ttu-id="510f4-139">الإيراد وإجمالي الربح حسب مجموعة العملاء</span><span class="sxs-lookup"><span data-stu-id="510f4-139">Revenue & gross profit by customer group</span></span>   |                                                         |
| <span data-ttu-id="510f4-140">الإيراد حسب المنتج</span><span class="sxs-lookup"><span data-stu-id="510f4-140">Revenue by product</span></span>     | <span data-ttu-id="510f4-141">الإيراد وإجمالي الربح حسب فئة المبيعات</span><span class="sxs-lookup"><span data-stu-id="510f4-141">Revenue & gross profit by sales category</span></span>   | <span data-ttu-id="510f4-142">إجمالي \# عدد المنتجات</span><span class="sxs-lookup"><span data-stu-id="510f4-142">Total \# of products</span></span>                                    |
|                        | <span data-ttu-id="510f4-143">أفضل 10 منتجات حسب الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-143">Top 10 products by revenue</span></span>                 | <span data-ttu-id="510f4-144">إجمالي عدد المنتجات النشطة والنسبة المئوية للإجمالي</span><span class="sxs-lookup"><span data-stu-id="510f4-144">Total number of active products and percentage of total</span></span> |
|                        | <span data-ttu-id="510f4-145">إجمالي الإيراد حسب فئة المبيعات</span><span class="sxs-lookup"><span data-stu-id="510f4-145">Total revenue by sales category</span></span>            | <span data-ttu-id="510f4-146">رقم محاسبة المنتجات لـ 80% من الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-146">Number of products accounting for 80% revenue</span></span>           |
| <span data-ttu-id="510f4-147">الإيراد حسب الفترة\*</span><span class="sxs-lookup"><span data-stu-id="510f4-147">Revenue by period\*</span></span>    | <span data-ttu-id="510f4-148">الإيراد حسب الشهر</span><span class="sxs-lookup"><span data-stu-id="510f4-148">Revenue by month</span></span>                           | <span data-ttu-id="510f4-149">النسبة المئوية السنوية لنمو الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-149">YOY revenue growth</span></span>                                      |
|                        | <span data-ttu-id="510f4-150">نسبة فرق الإيراد اللاحق، النسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="510f4-150">Trailing revenue variance, YOY</span></span>             | <span data-ttu-id="510f4-151">النسبة المئوية السنوية لنمو الإيراد %</span><span class="sxs-lookup"><span data-stu-id="510f4-151">YOY revenue growth %</span></span>                                    |
|                        | <span data-ttu-id="510f4-152">إجمالي نسبة فرق المبيعات حسب منطقة العميل</span><span class="sxs-lookup"><span data-stu-id="510f4-152">Total sales variance by customer region</span></span>    |                                                         |
| <span data-ttu-id="510f4-153">الإيراد حسب الموقع</span><span class="sxs-lookup"><span data-stu-id="510f4-153">Revenue by location</span></span>    | <span data-ttu-id="510f4-154">إيرادات المبيعات حسب المدينة</span><span class="sxs-lookup"><span data-stu-id="510f4-154">Sales revenue by city</span></span>                      |                                                         |
|                        | <span data-ttu-id="510f4-155">النسبة المئوية السنوية لنمو الإيراد %</span><span class="sxs-lookup"><span data-stu-id="510f4-155">YOY revenue growth %</span></span>                       |                                                         |
|                        | <span data-ttu-id="510f4-156">إيراد المبيعات حسب المنطقة</span><span class="sxs-lookup"><span data-stu-id="510f4-156">Sales revenue by region</span></span>                    |                                                         |
| <span data-ttu-id="510f4-157">ربحية العميل</span><span class="sxs-lookup"><span data-stu-id="510f4-157">Customer profitability</span></span> | <span data-ttu-id="510f4-158">إجمالي هامش الربح في مقابل الإيراد، حسب العميل</span><span class="sxs-lookup"><span data-stu-id="510f4-158">Gross margin versus revenue, by customer</span></span>   | <span data-ttu-id="510f4-159">إجمالي الربح وإجمالي هامش الربح، والنسبة المئوية السنوية لنمو الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-159">Gross profit, gross margin, YOY revenue growth</span></span>          |
| <span data-ttu-id="510f4-160">تحليل الربحية</span><span class="sxs-lookup"><span data-stu-id="510f4-160">Profitability analysis</span></span> | <span data-ttu-id="510f4-161">الإيراد وإجمالي الربح حسب الشهر</span><span class="sxs-lookup"><span data-stu-id="510f4-161">Revenue and gross profit by month</span></span>          |                                                         |
|                        | <span data-ttu-id="510f4-162">أفضل 15 عميل حسب إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="510f4-162">Top 15 customers by gross margin</span></span>           |                                                         |
|                        | <span data-ttu-id="510f4-163">إجمالي الربح حسب الشهر، النسبة المئوية السنوية</span><span class="sxs-lookup"><span data-stu-id="510f4-163">Gross profit by month, YOY</span></span>                 |                                                         |

<span data-ttu-id="510f4-164">\* الإيراد في هذا العام وفي العام الماضي، والنمو حسب فئة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="510f4-164">\* Revenue this and last year, and growth by sales category.</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="510f4-165">فهم نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="510f4-165">Understanding the data model and entities</span></span>
<span data-ttu-id="510f4-166">تُستخدم البيانات التالية لملء صفحات التقارير في محتوى **أداء الربحية والمبيعات** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="510f4-166">The following data is used to fill the report in the **Sales and profitability performance** Power BI content.</span></span> <span data-ttu-id="510f4-167">يتم تمثيل هذه البيانات كقياسات مجمعة تم تجهيزها في مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="510f4-167">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="510f4-168">مخزن الكيانات هو قاعدة بيانات Microsoft SQL Server تم تحسينها للتحليلات.</span><span class="sxs-lookup"><span data-stu-id="510f4-168">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="510f4-169">لمزيد من المعلومات، راجع [تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="510f4-169">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="510f4-170">تُعد القياسات التجميعية في هذا المحتوي مجموعة فرعية من القياسات التجميعية التي كانت متوفرة في مكعب المبيعات في Microsoft Dynamics AX 2012 وMicrosoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="510f4-170">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Sales Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="510f4-171">للوصول إلى مرحلة قياسات المكعب التجميعية في متجر الكيان، يجب أن تجعلها قابلة للنشر.</span><span class="sxs-lookup"><span data-stu-id="510f4-171">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="510f4-172">لمزيد من المعلومات، راجع الإجراء المتعلق بالوصول إلى التشغيل المرحلي للقياسات التجميعية في مخزن الكيانات في [ تكامل Power BI مع مخن الكيانات في Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog post.</span><span class="sxs-lookup"><span data-stu-id="510f4-172">For more information, see the procedure for staging aggregate measurements in the Entity store in the [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog post.</span></span>

<span data-ttu-id="510f4-173">تستخدم القياسات التجميعية الرئيسية التالية لكيان سطور فاتورة كأساس للمحتوى.</span><span class="sxs-lookup"><span data-stu-id="510f4-173">The following key aggregate measurements of the Invoice lines entity are used as the basis of the content.</span></span>

| <span data-ttu-id="510f4-174">الكيان</span><span class="sxs-lookup"><span data-stu-id="510f4-174">Entity</span></span>        | <span data-ttu-id="510f4-175">القياسات التجميعية الرئيسية</span><span class="sxs-lookup"><span data-stu-id="510f4-175">Key aggregate measurements</span></span>                   | <span data-ttu-id="510f4-176">مصدر البيانات لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="510f4-176">Data source for Dynamics 365</span></span> | <span data-ttu-id="510f4-177">الحقل</span><span class="sxs-lookup"><span data-stu-id="510f4-177">Field</span></span>                                        | <span data-ttu-id="510f4-178">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="510f4-178">Description</span></span>                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="510f4-179">سطور الفاتورة</span><span class="sxs-lookup"><span data-stu-id="510f4-179">Invoice lines</span></span> | <span data-ttu-id="510f4-180">الإيراد</span><span class="sxs-lookup"><span data-stu-id="510f4-180">Revenue</span></span>                                      | <span data-ttu-id="510f4-181">CustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="510f4-181">CustInvoiceTrans</span></span>             | <span data-ttu-id="510f4-182">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="510f4-182">SUM(LineAmountMST)</span></span>                           | <span data-ttu-id="510f4-183">المبلغ بعملة عملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="510f4-183">The amount in the accounting currency.</span></span>            |
|               | <span data-ttu-id="510f4-184">تكلفة البضائع المبيعة</span><span class="sxs-lookup"><span data-stu-id="510f4-184">Cost of goods sold</span></span>                           | <span data-ttu-id="510f4-185">InventTrans</span><span class="sxs-lookup"><span data-stu-id="510f4-185">InventTrans</span></span>                  | <span data-ttu-id="510f4-186">SUM(CostAmountPosted + CostAmountAdjustment)</span><span class="sxs-lookup"><span data-stu-id="510f4-186">SUM(CostAmountPosted + CostAmountAdjustment)</span></span> | <span data-ttu-id="510f4-187">مجموع مبلغ التكلفة والتسوية.</span><span class="sxs-lookup"><span data-stu-id="510f4-187">The sum of the cost amount and the adjustment.</span></span>    |
|               | <span data-ttu-id="510f4-188">مبلغ سطر العمولة - عملة المحاسبة</span><span class="sxs-lookup"><span data-stu-id="510f4-188">Commission line amount – accounting currency</span></span> | <span data-ttu-id="510f4-189">CustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="510f4-189">CustInvoiceTrans</span></span>             | <span data-ttu-id="510f4-190">SUM(CommissAmountMST)</span><span class="sxs-lookup"><span data-stu-id="510f4-190">SUM(CommissAmountMST)</span></span>                        | <span data-ttu-id="510f4-191">مبلغ العمولة بعملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="510f4-191">The commission amount in the accounting currency.</span></span> |

<span data-ttu-id="510f4-192">يوضح الجدول التالي القياسات التجميعية الرئيسية لكيان بنود الفاتورة المستخدمة لإنشاء العديد من القياسات المحسوبة في قاعدة بيانات المحتوى.</span><span class="sxs-lookup"><span data-stu-id="510f4-192">The following table shows the key aggregate measurements of the Invoice lines entity that are used to create several calculated measures in the content's dataset.</span></span>

| <span data-ttu-id="510f4-193">المقياس</span><span class="sxs-lookup"><span data-stu-id="510f4-193">Measure</span></span>           | <span data-ttu-id="510f4-194">حساب</span><span class="sxs-lookup"><span data-stu-id="510f4-194">Calculation</span></span>                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="510f4-195">إجمالي الربح</span><span class="sxs-lookup"><span data-stu-id="510f4-195">Gross profit</span></span>      | <span data-ttu-id="510f4-196">SUM(الإيراد – تكلفة البضائع المبيعة – العمولة – ضريبة المبيعات (مضمنة في مبلغ بند فاتورة العميل))</span><span class="sxs-lookup"><span data-stu-id="510f4-196">SUM(Revenue – COGS – Commission – Sales tax (included in customer invoice line amount))</span></span>          |
| <span data-ttu-id="510f4-197">إجمالي هامش الربح</span><span class="sxs-lookup"><span data-stu-id="510f4-197">Gross margin</span></span>      | <span data-ttu-id="510f4-198">SUM(إجمالي الربح/ (الإيراد – ضريبة المبيعات (مضمنة في مبلغ بند فاتورة العميل)))</span><span class="sxs-lookup"><span data-stu-id="510f4-198">SUM(Gross profit / (Revenue - Sales tax (included in customer invoice line amount)))</span></span>             |
| <span data-ttu-id="510f4-199">إيراد العام الماضي</span><span class="sxs-lookup"><span data-stu-id="510f4-199">Revenue last year</span></span> | <span data-ttu-id="510f4-200">إيراد العام الماضي = CALCULATE(SUM('بنود الفاتورة'\[الإيراد\]), SAMEPERIODLASTYEAR(التواريخ\[التاريخ\])</span><span class="sxs-lookup"><span data-stu-id="510f4-200">Revenue last year = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\])</span></span> |

<span data-ttu-id="510f4-201">يُظهر الجدول التالي الأبعاد الرئيسية في مكعب المبيعات المستخدمة كعوامل تصفية لتقسيم القياسات التجميعية، لتتمكن من تحقيق مستوى أكبر من الدقة وتوفير نظرة تحليلية أعمق.</span><span class="sxs-lookup"><span data-stu-id="510f4-201">The following key dimensions in the Sales Cube are used as filters to slice the aggregate measurements, so that you can achieve greater granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="510f4-202">الكيان</span><span class="sxs-lookup"><span data-stu-id="510f4-202">Entity</span></span>           | <span data-ttu-id="510f4-203">أمثلة لهذه السمات</span><span class="sxs-lookup"><span data-stu-id="510f4-203">Examples of attributes</span></span>                               |
|------------------|------------------------------------------------------|
| <span data-ttu-id="510f4-204">العملاء</span><span class="sxs-lookup"><span data-stu-id="510f4-204">Customers</span></span>        | <span data-ttu-id="510f4-205">مجموعات العملاء ومناطق العملاء والعنوان والصناعة</span><span class="sxs-lookup"><span data-stu-id="510f4-205">Customer groups, Customer regions, Address, Industry</span></span> |
| <span data-ttu-id="510f4-206">المنتجات</span><span class="sxs-lookup"><span data-stu-id="510f4-206">Products</span></span>         | <span data-ttu-id="510f4-207">اسم المنتج، اسم المنتج، اسم مجموعات الصنف</span><span class="sxs-lookup"><span data-stu-id="510f4-207">Product number, Product name, Item groups name</span></span>       |
| <span data-ttu-id="510f4-208">فئات المبيعات</span><span class="sxs-lookup"><span data-stu-id="510f4-208">Sales categories</span></span> | <span data-ttu-id="510f4-209">أسماء فئات المبيعات</span><span class="sxs-lookup"><span data-stu-id="510f4-209">Sales category names</span></span>                                 |
| <span data-ttu-id="510f4-210">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="510f4-210">Legal entities</span></span>   | <span data-ttu-id="510f4-211">أسماء الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="510f4-211">Legal entity names</span></span>                                   |
| <span data-ttu-id="510f4-212">التواريخ</span><span class="sxs-lookup"><span data-stu-id="510f4-212">Dates</span></span>            | <span data-ttu-id="510f4-213">التواريخ</span><span class="sxs-lookup"><span data-stu-id="510f4-213">Dates</span></span>                                                |

<span data-ttu-id="510f4-214">بشكل افتراضي، يعرض المحتوى البيانات للسنة التقويمية الجارية.</span><span class="sxs-lookup"><span data-stu-id="510f4-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="510f4-215">ولكن يمكنك تغيير عامل تصفية البيانات في قسم عوامل تصفية التقارير.</span><span class="sxs-lookup"><span data-stu-id="510f4-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="510f4-216">يمكنك أيضا تغيير عامل تصفية الشركة.</span><span class="sxs-lookup"><span data-stu-id="510f4-216">You can also change the company filter.</span></span>