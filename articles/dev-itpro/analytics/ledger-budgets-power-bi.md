---
title: "محتوى Power BI القيمة الفعلية مقابل الموازنة"
description: "يصف هذا الموضوع محتوى Power BI \"القيمة الفعلية مقابل الموازنة‬\". وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: db79d594e67a0e163cabbd3a5f7b7b1452c2ae9e
ms.openlocfilehash: a395f29aa8a1ed58f4d8681c4d874ee8b8b0a860
ms.contentlocale: ar-sa
ms.lasthandoff: 01/09/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="50132-104">محتوى Power BI القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="50132-105">يصف هذا الموضوع محتوى Microsoft Power BI **القيمة الفعلية مقابل الموازنة‬**.</span><span class="sxs-lookup"><span data-stu-id="50132-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="50132-106">فهو يوضح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="50132-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="50132-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="50132-107">Overview</span></span>

<span data-ttu-id="50132-108">تم إنشاء محتوى Power BI **القيمة الفعلية مقابل الموازنة** للأفراد المسؤولين عن مراقبة القيمة الفعلية في مقابل أداء الموازنة في مؤسستهم.</span><span class="sxs-lookup"><span data-stu-id="50132-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="50132-109">يوفر محتوى Power BI **القيمة الفعلية مقابل الموازنة** إمكانية رؤية تباينات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="50132-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="50132-110">يمكنك تحليل الموازنة للسنة الحالية حسب فئة الحساب أو كود الموازنة أو الحساب الرئيسي أو أوصاف الحساب الرئيسي أو الفترة المالية للحصول على فهم أفضل لسبب التباينات.</span><span class="sxs-lookup"><span data-stu-id="50132-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="50132-111">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="50132-111">Accessing the Power BI content</span></span>
<span data-ttu-id="50132-112">يتم عرض تقارير من محتوى Power BI **الفعلي مقابل الموازنة** في مساحتي عمل **موازنة دفتر الأستاذ والتنبؤات** و**المدير المالي**.</span><span class="sxs-lookup"><span data-stu-id="50132-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="50132-113">التقارير المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="50132-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="50132-114">يوفر الجدول التالي تفاصيل حول المقاييس التي يتم العثور عليها في كل صفحة من صفحات التقرير في محتوى Power BI **القيمة الفعلية مقابل الموازنة‬**.</span><span class="sxs-lookup"><span data-stu-id="50132-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="50132-115">تقرير</span><span class="sxs-lookup"><span data-stu-id="50132-115">Report</span></span>                      | <span data-ttu-id="50132-116">المقاييس</span><span class="sxs-lookup"><span data-stu-id="50132-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="50132-117">المصروفات- ‏‫القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="50132-118">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-118">Total expenses this year</span></span></li><li><span data-ttu-id="50132-119">إجمالي مصروفات الموازنة هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="50132-120">الإيراد- ‏‫القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="50132-121">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-121">Total revenue this year</span></span></li><li><span data-ttu-id="50132-122">إجمالي إيراد الموازنة هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="50132-123">المصروفات</span><span class="sxs-lookup"><span data-stu-id="50132-123">Expense</span></span>                     | <ul><li><span data-ttu-id="50132-124">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-124">Total expenses this year</span></span></li><li><span data-ttu-id="50132-125">هدف للمصروفات استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="50132-126">الإيراد</span><span class="sxs-lookup"><span data-stu-id="50132-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="50132-127">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-127">Total revenue this year</span></span></li><li><span data-ttu-id="50132-128">هدف للإيراد استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="50132-129">صافي الدخل</span><span class="sxs-lookup"><span data-stu-id="50132-129">Net income</span></span>                  | <ul><li><span data-ttu-id="50132-130">صافي الدخل هذه السنة</span><span class="sxs-lookup"><span data-stu-id="50132-130">Net income this year</span></span></li><li><span data-ttu-id="50132-131">هدف لصافي الدخل استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-131">Goal for net income based on budget</span></span> </li><ul> |


# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="50132-132">فهم نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="50132-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="50132-133">الكيان</span><span class="sxs-lookup"><span data-stu-id="50132-133">Entity</span></span>                    | <span data-ttu-id="50132-134">المحتويات</span><span class="sxs-lookup"><span data-stu-id="50132-134">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="50132-135">أنشطة دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="50132-135">General Ledger Activities</span></span> | <span data-ttu-id="50132-136">مبالغ الحركات لدفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="50132-136">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="50132-137">أنشطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-137">Budget Activities</span></span>         | <span data-ttu-id="50132-138">مبالغ الحركات لسجل الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-138">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="50132-139">الحسابات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="50132-139">Main Accounts</span></span>             | <span data-ttu-id="50132-140">الحسابات الرئيسية لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="50132-140">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="50132-141">التقويمات المالية</span><span class="sxs-lookup"><span data-stu-id="50132-141">Fiscal Calendars</span></span>          | <span data-ttu-id="50132-142">التقويمات المالية لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="50132-142">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="50132-143">دفاتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="50132-143">Ledgers</span></span>                   | <span data-ttu-id="50132-144">دفاتر الأستاذ التي يمكن استخدامها لتصفية التقرير إلى دفتر الأستاذ الحالي</span><span class="sxs-lookup"><span data-stu-id="50132-144">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="50132-145">أكواد الموازنة</span><span class="sxs-lookup"><span data-stu-id="50132-145">Budget Codes</span></span>              | <span data-ttu-id="50132-146">أكواد الموازنة لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="50132-146">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="50132-147">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="50132-147">Legal Entities</span></span>            | <span data-ttu-id="50132-148">الكيانات القانونية التي يمكن استخدامها لتصفية التقرير إلى الكيان القانوني الحالي</span><span class="sxs-lookup"><span data-stu-id="50132-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |

