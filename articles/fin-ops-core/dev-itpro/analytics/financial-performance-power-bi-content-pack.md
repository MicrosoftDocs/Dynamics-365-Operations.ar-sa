---
title: حل محتوى PowerBI.com للأداء المالي
description: يصف هذا الموضوع حل PowerBI.com للأداء المالي.
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cbecf178d0588c51b831fbd55b536d3e4e41c27
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771109"
---
# <a name="financial-performance-powerbicom-solution"></a><span data-ttu-id="32624-103">حل محتوى PowerBI.com للأداء المالي</span><span class="sxs-lookup"><span data-stu-id="32624-103">Financial performance PowerBI.com solution</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="32624-104">تم إهمال حل PowerBI.com هذا كما هو موثق في [الميزات التي تمت ازالتها أو إهمالها لـ Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span><span class="sxs-lookup"><span data-stu-id="32624-104">This PowerBI.com solution has been deprecated as documented in [Removed or deprecated features for Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span></span>

<span data-ttu-id="32624-105">يصف هذا الموضوع حل PowerBI.com **للأداء المالي** </span><span class="sxs-lookup"><span data-stu-id="32624-105">This topic describes the **Financial performance** PowerBI.com solution.</span></span> <span data-ttu-id="32624-106">إنه يصف لوحة المعلومات والتقارير التي تم تضمينها في حزمة المحتوى، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء الحل.</span><span class="sxs-lookup"><span data-stu-id="32624-106">It describes the dashboard and reports that are included, and provides information about the data model and entities that were used to build the solution.</span></span>

## <a name="main-account-setup"></a><span data-ttu-id="32624-107">إعداد الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="32624-107">Main account setup</span></span>
<span data-ttu-id="32624-108">لأن المؤسسات تريد أن تظهر التزاماتها ومبالغ الإيراد كمبالغ موجبة في التقارير، يُعد إعداد الحسابات الرئيسية أمرًا بالغ الأهمية.</span><span class="sxs-lookup"><span data-stu-id="32624-108">Because organizations want liabilities and revenue amounts to appear as positive amounts on reports, the setup of the main accounts is important.</span></span> <span data-ttu-id="32624-109">بالنسبة لهذه الحسابات الرئيسية لتظهر كمبالغ موجبه، يجب تعيين نوع الحساب الرئيسي على **الالتزام** أو **الإيراد**.</span><span class="sxs-lookup"><span data-stu-id="32624-109">For these main accounts to appear as positive amounts, the main account type must be set to **Liability** or **Revenue**.</span></span> <span data-ttu-id="32624-110">عند استخدام أنواع الحسابات هذه، سوف يقوم الإبلاغ من خلال Power BI بعكس العلامات، وإظهار المبالغ كمبالغ موجبة.</span><span class="sxs-lookup"><span data-stu-id="32624-110">When these account types are used, reporting through Power BI will reverse the signs and show the amounts as positive.</span></span>

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a><span data-ttu-id="32624-111">لوحة المعلومات والتقارير المضمنة في حل PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="32624-111">Dashboard and reports that are included in the PowerBI.com solution</span></span>
<span data-ttu-id="32624-112">تحتوي لوحة المعلومات على إطارات متجانبة ملخصة للبيانات تستند إلى التقارير الأساسية.</span><span class="sxs-lookup"><span data-stu-id="32624-112">The dashboard contains summarized tiles of data that are based on underlying reports.</span></span> <span data-ttu-id="32624-113">ويحتوي كل إطار متجانب على معلومات ملخصة للسنة الحالية في كافة الشركات في مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="32624-113">Each tile contains summarized information for the current year across all companies in an organization.</span></span> <span data-ttu-id="32624-114">فيما يلي بعض التجانبات:</span><span class="sxs-lookup"><span data-stu-id="32624-114">Here are some of the tiles:</span></span>

- <span data-ttu-id="32624-115">نقدي</span><span class="sxs-lookup"><span data-stu-id="32624-115">Cash</span></span>
- <span data-ttu-id="32624-116">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="32624-116">Total Revenue this year</span></span>
- <span data-ttu-id="32624-117">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="32624-117">Total Expenses this year</span></span>
- <span data-ttu-id="32624-118">صافي الدخل هذه السنة</span><span class="sxs-lookup"><span data-stu-id="32624-118">Net Income this year</span></span>
- <span data-ttu-id="32624-119">النسبة السريعة</span><span class="sxs-lookup"><span data-stu-id="32624-119">Quick Ratio</span></span>
- <span data-ttu-id="32624-120">إجمالي المصروفات هذه السنة حسب فئة الحساب</span><span class="sxs-lookup"><span data-stu-id="32624-120">Total Expenses this year by account category</span></span>
- <span data-ttu-id="32624-121">النسبة الحالية</span><span class="sxs-lookup"><span data-stu-id="32624-121">Current Ratio</span></span>
- <span data-ttu-id="32624-122">‏‏دين إجمالي الأصول</span><span class="sxs-lookup"><span data-stu-id="32624-122">Debt to Total Assets</span></span>
- <span data-ttu-id="32624-123">الإيراد الفعلي مقابل الإيراد المتوقع</span><span class="sxs-lookup"><span data-stu-id="32624-123">Actual vs Forecasted Revenue</span></span>
- <span data-ttu-id="32624-124">الإيراد المفوتر هذه السنة</span><span class="sxs-lookup"><span data-stu-id="32624-124">Billed Revenue this Year</span></span>
- <span data-ttu-id="32624-125">نسبة مصروفات التشغيل هذه السنة</span><span class="sxs-lookup"><span data-stu-id="32624-125">Operating expenses Ratio this year</span></span>
- <span data-ttu-id="32624-126">هامش الربح هذه السنة</span><span class="sxs-lookup"><span data-stu-id="32624-126">Profit Margin this year</span></span>
- <span data-ttu-id="32624-127">المصروفات الفعلية في مقابل مصروفات الميزانية – كافة الشركات</span><span class="sxs-lookup"><span data-stu-id="32624-127">Actual vs Budget Expenses – All companies</span></span>

<span data-ttu-id="32624-128">يتم دعم كل تجاب من هذه التجانبات من خلال تقرير داعم.</span><span class="sxs-lookup"><span data-stu-id="32624-128">Each tile is backed by a supporting report.</span></span> <span data-ttu-id="32624-129">تحتوي هذه التقارير على مخططات وجداول توفر المزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="32624-129">These reports contain both charts and tables that provide more information.</span></span> <span data-ttu-id="32624-130">يصف الجدول التالي التقارير.</span><span class="sxs-lookup"><span data-stu-id="32624-130">The following table describes the reports.</span></span>

| <span data-ttu-id="32624-131">التقرير</span><span class="sxs-lookup"><span data-stu-id="32624-131">Report</span></span>                      | <span data-ttu-id="32624-132">المعلومات التي يحتوي عليها التقرير</span><span class="sxs-lookup"><span data-stu-id="32624-132">Information that the report contains</span></span> |
|-----------------------------|--------------------------------------|
| <span data-ttu-id="32624-133">التحليل النقدي</span><span class="sxs-lookup"><span data-stu-id="32624-133">Cash Analysis</span></span>               | <span data-ttu-id="32624-134">النقدية حسب الكيان القانوني والنقدية حسب ربع السنة وإجمالي النقدية والنقدية حسب الحساب</span><span class="sxs-lookup"><span data-stu-id="32624-134">Cash by legal entity, cash by quarter, total cash, and cash by account</span></span><blockquote>[!NOTE] <span data-ttu-id="32624-135">لا تتضمن معلومات النقدية حسب ربع السنة أرصدة البداية في الإجمالي الخاص بالربع الأول.</span><span class="sxs-lookup"><span data-stu-id="32624-135">The cash by quarter information doesn't include beginning balances in the total for the first quarter.</span></span> <span data-ttu-id="32624-136">فهو يعرض إجمالي الحركات الجديدة المُرحلة في كل ربع سنة.</span><span class="sxs-lookup"><span data-stu-id="32624-136">It shows the total of new transactions that are posted in each quarter.</span></span></blockquote> |
| <span data-ttu-id="32624-137">تحليل النسبة الحالية</span><span class="sxs-lookup"><span data-stu-id="32624-137">Current Ratio Analysis</span></span>      | <span data-ttu-id="32624-138">النسبة الحالية حسب الكيان القانوني والنسبة الحالية حسب ربع السنة وأرصدة الأصول الحالية والالتزامات الحالية</span><span class="sxs-lookup"><span data-stu-id="32624-138">Current ratio by legal entity, current ratio by quarter, and balances for current assets and current liabilities</span></span> |
| <span data-ttu-id="32624-139">تحليل النسبة السريعة</span><span class="sxs-lookup"><span data-stu-id="32624-139">Quick Ratio Analysis</span></span>        | <span data-ttu-id="32624-140">النسبة السريعة حسب الكيان القانوني والنسبة السريعة حسب ربع السنة وأرصدة النقدية والحسابات المدينة والالتزامات الحالية</span><span class="sxs-lookup"><span data-stu-id="32624-140">Quick ratio by legal entity, quick ratio by quarter, and balances for cash, accounts receivable, and current liabilities</span></span> |
| <span data-ttu-id="32624-141">تحليل تكلفة البضائع المبيعة</span><span class="sxs-lookup"><span data-stu-id="32624-141">Cost of Goods Sold Analysis</span></span> | <span data-ttu-id="32624-142">تكلفة البضائع المبيعة حسب الكيان القانوني، وتكلفة البضائع المبيعة هذه السنة والسنة الماضية حسب ربع السنة، وتكلفة البضائع المبيعة إلى المبيعات حسب الكيان القانوني، وإجمالي تكلفة البضائع المبيعة، ونسبة تكلفة البضائع المبيعة إلى المبيعات</span><span class="sxs-lookup"><span data-stu-id="32624-142">Cost of goods sold (COGS) by legal entity, COGS this year and last year by quarter, COGS to sales by legal entity, total COGS, and COGS to sales percentage</span></span> |
| <span data-ttu-id="32624-143">تحليل رأس المال العامل</span><span class="sxs-lookup"><span data-stu-id="32624-143">Working Capital Analysis</span></span>    | <span data-ttu-id="32624-144">رأس المال العامل حسب الكيان القانوني، ورأس المال العامل حسب ربع السنة، والأصول الحالية، والالتزامات الحالية، وإجمالي رأس المال العامل</span><span class="sxs-lookup"><span data-stu-id="32624-144">Working capital by legal entity, working capital by quarter, current assets, current liabilities, and total working capital</span></span> |
| <span data-ttu-id="32624-145">تحليل الأصول والديون</span><span class="sxs-lookup"><span data-stu-id="32624-145">Asset and Debt Analysis</span></span>     | <span data-ttu-id="32624-146">العائد على إجمالي الأصول والديون إلى إجمالي الأصول حسب الكيان القانوني، ونسبة الدين إلى إجمالي الأصول والعائد على ربع سنة إجمالي الأصول إلى التاريخ والأصول والالتزامات</span><span class="sxs-lookup"><span data-stu-id="32624-146">Return on total assets and debt to total assets by legal entity, debt to total assets and return on total assets quarter to date, assets, and liabilities</span></span> |
| <span data-ttu-id="32624-147">تحليل هامش الربح</span><span class="sxs-lookup"><span data-stu-id="32624-147">Profit Margin Analysis</span></span>      | <span data-ttu-id="32624-148">هامش الربح الفعلي وهامش ربح الموازنة حسب الكيان القانوني، وتمييز الأرباح حسب ربع السنة، ونسبة هامش الربح وهامش الربح</span><span class="sxs-lookup"><span data-stu-id="32624-148">Actual and budget profit margin by legal entity, profit marking by quarter, profit margin percentage, and profit margin</span></span> |
| <span data-ttu-id="32624-149">تحليل صافي الدخل</span><span class="sxs-lookup"><span data-stu-id="32624-149">Net Income Analysis</span></span>         | <span data-ttu-id="32624-150">صافي الدخل الفعلي وصافي الدخل على الموازنة حسب الكيان القانوني، وصافي الدخل هذا العام وفي العام الماضي، ونسبة المصروفات إلى صافي الدخل</span><span class="sxs-lookup"><span data-stu-id="32624-150">Actual and budget net income by legal entity, net income this year and last year, and expenses to net income percentage</span></span> |
| <span data-ttu-id="32624-151">تحليل الأرباح</span><span class="sxs-lookup"><span data-stu-id="32624-151">Earnings Analysis</span></span>           | <span data-ttu-id="32624-152">الأرباح الفعلية وأرباح الموازنة قبل الفوائد والضرائب (EBIT) حسب الكيان القانوني، وأرباح الفوائد والضرائب هذا العام وفي العام الماضي، ونسبة المصروفات إلى الإيرادات، ونسبة المصروفات الفعلية ومصروفات الموازنة إلى الإيرادات</span><span class="sxs-lookup"><span data-stu-id="32624-152">Actual and budget earnings before interest and taxes (EBIT) by legal entity, EBIT this year and last year, expenses to revenue percentage, and actual and budget expenses to revenue</span></span> |
| <span data-ttu-id="32624-153">تحليل الإيرادات</span><span class="sxs-lookup"><span data-stu-id="32624-153">Revenue Analysis</span></span>            | <span data-ttu-id="32624-154">إجمالي الإيرادات الفعلية وإجمالي إيرادات الموازنة حسب الكيان القانوني، وإجمالي الإيرادات هذا العام وفي العام الماضي، وفرق موازنة الإيرادات حسب الكيان القانوني، وإجمالي إيرادات هذه الفترة والفترة الأخيرة</span><span class="sxs-lookup"><span data-stu-id="32624-154">Total revenue, actual and budget total revenue by legal entity, total revenue this year and last year, revenue budget variance by legal entity, and total revenue this period and last period</span></span> |
| <span data-ttu-id="32624-155">تحليل المصروفات</span><span class="sxs-lookup"><span data-stu-id="32624-155">Expense Analysis</span></span>            | <span data-ttu-id="32624-156">إجمالي المصروفات، الفعلية إلى إجمالي مصروفات الموازنة حسب الكيان القانوني، وإجمالي المصروفات الفعلية وإجمالي مصروفات الموازنة حسب ربع السنة، وإجمالي المصروفات حسب فئة الحساب ونسبة مصروفات التشغيل</span><span class="sxs-lookup"><span data-stu-id="32624-156">Total expenses, actual to budget total expenses by legal entity, actual and budget total expense by quarter, total expenses by account category, and operating expenses ratio</span></span> |
| <span data-ttu-id="32624-157">تحليل الإيرادات المفوترة</span><span class="sxs-lookup"><span data-stu-id="32624-157">Billed Revenue Analysis</span></span>     | <span data-ttu-id="32624-158">إجمالي الحسابات المدينة، وإجمالي الحسابات المدينة حسب الكيان القانوني، وإجمالي الحسابات المدينة حسب ربع السنة، وأرصدة الحسابات للحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="32624-158">Total accounts receivable, total accounts receivable by legal entity, total accounts receivable by quarter, and balances for accounts receivable accounts</span></span><blockquote>[!NOTE] <span data-ttu-id="32624-159">لا تتضمن المعلومات أرصدة البداية لحسابات دفتر الأستاذ للحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="32624-159">The information doesn't include beginning balances for the accounts receivable ledger accounts.</span></span> <span data-ttu-id="32624-160">إنها تظهر إجمالي الحركات الجديدة المُرحلة إلى الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="32624-160">It shows the total of new transactions that are posted to Accounts receivable.</span></span></blockquote> |

<span data-ttu-id="32624-161">يمكنك تصفية المخططات والإطارات المتجانبة الموجودة على كافة هذه التقارير وتثبيتها بلوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="32624-161">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="32624-162">لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span><span class="sxs-lookup"><span data-stu-id="32624-162">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="32624-163">فهم نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="32624-163">Understanding the data model and entities</span></span>
<span data-ttu-id="32624-164">تم استخدام الكيانات التالية كأساس لحل PowerBI.com **للأداء المالي**</span><span class="sxs-lookup"><span data-stu-id="32624-164">The following entities were used as the basis of the **Financial performance** PowerBI.com solution:</span></span>

<span data-ttu-id="32624-165">**كيانات البيانات المجمّعة**</span><span class="sxs-lookup"><span data-stu-id="32624-165">**Aggregate data entities**</span></span>

- <span data-ttu-id="32624-166">**GeneralLedgerActivities** – يجمع هذا الكيان أرصدة دفتر الأستاذ العام بحسب فئة الحساب.</span><span class="sxs-lookup"><span data-stu-id="32624-166">**GeneralLedgerActivities** – This entity aggregates general ledger balances by account category.</span></span>
- <span data-ttu-id="32624-167">**BudgetActivities** – يجمع هذا الكيان أرصدة الموازنة بحسب فئة الحساب.</span><span class="sxs-lookup"><span data-stu-id="32624-167">**BudgetActivities** – This entity aggregates budget balances by account category.</span></span>

<span data-ttu-id="32624-168">**كيانات البيانات**</span><span class="sxs-lookup"><span data-stu-id="32624-168">**Data entities**</span></span>

- <span data-ttu-id="32624-169">FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="32624-169">FiscalCalendars</span></span>
- <span data-ttu-id="32624-170">MainAccounts</span><span class="sxs-lookup"><span data-stu-id="32624-170">MainAccounts</span></span>
- <span data-ttu-id="32624-171">LegalEntities</span><span class="sxs-lookup"><span data-stu-id="32624-171">LegalEntities</span></span>
- <span data-ttu-id="32624-172">دفاتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="32624-172">Ledgers</span></span>
- <span data-ttu-id="32624-173">ChartofAccounts</span><span class="sxs-lookup"><span data-stu-id="32624-173">ChartofAccounts</span></span>

<span data-ttu-id="32624-174">استخدمت هذه الكيانات لإنشاء القياسات المحسوبة في نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="32624-174">These entities were used to create calculated measures in the data model.</span></span> <span data-ttu-id="32624-175">تُستخدم القياسات المحسوبة لإنشاء مؤشرات الأداء الرئيسية والتقارير المستخدمة في المحتوى.</span><span class="sxs-lookup"><span data-stu-id="32624-175">The calculated measures are used to calculate the key performance indicators (KPIs) and reports that are used in the content.</span></span> <span data-ttu-id="32624-176">بشكل افتراضي، يحضر المحتوى بيانات للسنوات الثلاث الماضية وسنة واحدة مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="32624-176">By default, the content brings in data for the last three years and one future year.</span></span> <span data-ttu-id="32624-177">لتضمين عمليات حسابية إضافية على لوحة المعلومات والتقارير، يمكنك تعديل [مصنف Microsoft Excel](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span><span class="sxs-lookup"><span data-stu-id="32624-177">To include additional calculations on your reports and dashboard, you can modify the [Microsoft Excel workbook](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span></span> <span data-ttu-id="32624-178">هذا المصنف هو نموذج البيانات الافتراضي الذي تم استخدامه لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="32624-178">This workbook is the default data model that was used to create the content.</span></span>