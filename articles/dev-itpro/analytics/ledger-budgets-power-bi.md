---
title: محتوى "الفعلي مقابل الموازنة‬" في Power BI
description: يصف هذا الموضوع محتوى "الفعلي مقابل الموازنة‬" في Power BI. وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c801544e9e37a528203f5a1730aa8cb526d63dbf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553728"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="fbdf7-104">محتوى "الفعلي مقابل الموازنة‬" في Power BI</span><span class="sxs-lookup"><span data-stu-id="fbdf7-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbdf7-105">يصف هذا الموضوع محتوى **الفعلي مقابل الموازنة** في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="fbdf7-106">وهو يوضح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="fbdf7-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-107">Overview</span></span>

<span data-ttu-id="fbdf7-108">تم إنشاء محتوى **الفعلي مقابل الموازنة** في Power BI للأفراد المسؤولين عن مراقبة أداء القيم الفعلية في مقابل أداء الموازنة في مؤسستهم.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="fbdf7-109">يوفر محتوى **الفعلي مقابل الموازنة** في Power BI إمكانية رؤية تباينات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="fbdf7-110">يمكنك تحليل الموازنة للسنة الحالية حسب فئة الحساب أو كود الموازنة أو الحساب الرئيسي أو أوصاف الحساب الرئيسي أو الفترة المالية للحصول على فهم أفضل لسبب التباينات.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="fbdf7-111">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="fbdf7-111">Accessing the Power BI content</span></span>
<span data-ttu-id="fbdf7-112">تظهر تقارير محتوى **الفعلي مقابل الموازنة** في Power BI في مساحتي عمل **موازنة دفتر الأستاذ والتنبؤات** و**المدير المالي**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="fbdf7-113">التقارير المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="fbdf7-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="fbdf7-114">يوفر الجدول التالي تفاصيل حول المقاييس التي يتم العثور عليها في كل صفحة من صفحات التقرير في محتوى **الفعلي مقابل الموازنة‬** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="fbdf7-115">تقرير</span><span class="sxs-lookup"><span data-stu-id="fbdf7-115">Report</span></span>                      | <span data-ttu-id="fbdf7-116">المقاييس</span><span class="sxs-lookup"><span data-stu-id="fbdf7-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fbdf7-117">المصروفات- ‏‫القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="fbdf7-118">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-118">Total expenses this year</span></span></li><li><span data-ttu-id="fbdf7-119">إجمالي مصروفات الموازنة هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="fbdf7-120">الإيراد- ‏‫القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="fbdf7-121">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-121">Total revenue this year</span></span></li><li><span data-ttu-id="fbdf7-122">إجمالي إيراد الموازنة هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="fbdf7-123">المصروفات</span><span class="sxs-lookup"><span data-stu-id="fbdf7-123">Expense</span></span>                     | <ul><li><span data-ttu-id="fbdf7-124">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-124">Total expenses this year</span></span></li><li><span data-ttu-id="fbdf7-125">هدف للمصروفات استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="fbdf7-126">الإيراد</span><span class="sxs-lookup"><span data-stu-id="fbdf7-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="fbdf7-127">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-127">Total revenue this year</span></span></li><li><span data-ttu-id="fbdf7-128">هدف للإيراد استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="fbdf7-129">صافي الدخل</span><span class="sxs-lookup"><span data-stu-id="fbdf7-129">Net income</span></span>                  | <ul><li><span data-ttu-id="fbdf7-130">صافي الدخل هذه السنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-130">Net income this year</span></span></li><li><span data-ttu-id="fbdf7-131">هدف لصافي الدخل استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="fbdf7-132">فهم نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="fbdf7-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="fbdf7-133">الكيان</span><span class="sxs-lookup"><span data-stu-id="fbdf7-133">Entity</span></span>                    | <span data-ttu-id="fbdf7-134">المحتويات</span><span class="sxs-lookup"><span data-stu-id="fbdf7-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fbdf7-135">أنشطة دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="fbdf7-135">General Ledger Activities</span></span> | <span data-ttu-id="fbdf7-136">مبالغ الحركات لدفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="fbdf7-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="fbdf7-137">أنشطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-137">Budget Activities</span></span>         | <span data-ttu-id="fbdf7-138">مبالغ الحركات لسجل الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="fbdf7-139">الحسابات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="fbdf7-139">Main Accounts</span></span>             | <span data-ttu-id="fbdf7-140">الحسابات الرئيسية لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="fbdf7-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="fbdf7-141">التقويمات المالية</span><span class="sxs-lookup"><span data-stu-id="fbdf7-141">Fiscal Calendars</span></span>          | <span data-ttu-id="fbdf7-142">التقويمات المالية لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="fbdf7-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="fbdf7-143">دفاتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="fbdf7-143">Ledgers</span></span>                   | <span data-ttu-id="fbdf7-144">دفاتر الأستاذ التي يمكن استخدامها لتصفية التقرير إلى دفتر الأستاذ الحالي</span><span class="sxs-lookup"><span data-stu-id="fbdf7-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="fbdf7-145">أكواد الموازنة</span><span class="sxs-lookup"><span data-stu-id="fbdf7-145">Budget Codes</span></span>              | <span data-ttu-id="fbdf7-146">أكواد الموازنة لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="fbdf7-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="fbdf7-147">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="fbdf7-147">Legal Entities</span></span>            | <span data-ttu-id="fbdf7-148">الكيانات القانونية التي يمكن استخدامها لتصفية التقرير إلى الكيان القانوني الحالي</span><span class="sxs-lookup"><span data-stu-id="fbdf7-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
