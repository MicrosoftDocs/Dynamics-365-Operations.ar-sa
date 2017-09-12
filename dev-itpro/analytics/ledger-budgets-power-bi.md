---
title: "محتوى Power BI القيمة الفعلية مقابل الموازنة"
description: "يصف هذا الموضوع محتوى Power BI \"القيمة الفعلية مقابل الموازنة‬\". وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 6e675ccd610561668dec4f5c7410530edaa122b8
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="e21b7-104">محتوى Power BI القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e21b7-105">يصف هذا الموضوع محتوى Microsoft Power BI **القيمة الفعلية مقابل الموازنة‬**.</span><span class="sxs-lookup"><span data-stu-id="e21b7-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="e21b7-106">فهو يوضح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.</span><span class="sxs-lookup"><span data-stu-id="e21b7-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="e21b7-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e21b7-107">Overview</span></span>

<span data-ttu-id="e21b7-108">تم إنشاء محتوى Power BI **القيمة الفعلية مقابل الموازنة** للأفراد المسؤولين عن مراقبة القيمة الفعلية في مقابل أداء الموازنة في مؤسستهم.</span><span class="sxs-lookup"><span data-stu-id="e21b7-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="e21b7-109">يوفر محتوى Power BI **القيمة الفعلية مقابل الموازنة** إمكانية رؤية تباينات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="e21b7-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="e21b7-110">يمكنك تحليل الموازنة للسنة الحالية حسب فئة الحساب أو كود الموازنة أو الحساب الرئيسي أو أوصاف الحساب الرئيسي أو الفترة المالية للحصول على فهم أفضل لسبب التباينات.</span><span class="sxs-lookup"><span data-stu-id="e21b7-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="e21b7-111">الوصول إلى محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="e21b7-111">Accessing the Power BI content</span></span>
<span data-ttu-id="e21b7-112">إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، تحديث يوليو 2017، فستظهر تقارير من محتوى Power BI **القيمة الفعلية مقابل الموازنة** في مساحتي العمل **تنبؤات وموازنات دفتر الأستاذ** و**المدير المالي**.</span><span class="sxs-lookup"><span data-stu-id="e21b7-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="e21b7-113">التقارير المضمنة في محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="e21b7-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="e21b7-114">يوفر الجدول التالي تفاصيل حول المقاييس التي يتم العثور عليها في كل صفحة من صفحات التقرير في محتوى Power BI **القيمة الفعلية مقابل الموازنة‬**.</span><span class="sxs-lookup"><span data-stu-id="e21b7-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="e21b7-115">تقرير</span><span class="sxs-lookup"><span data-stu-id="e21b7-115">Report</span></span>                      | <span data-ttu-id="e21b7-116">المقاييس</span><span class="sxs-lookup"><span data-stu-id="e21b7-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="e21b7-117">المصروفات- ‏‫القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="e21b7-118">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-118">Total expenses this year</span></span></li><li><span data-ttu-id="e21b7-119">إجمالي مصروفات الموازنة هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="e21b7-120">الإيراد- ‏‫القيمة الفعلية مقابل الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="e21b7-121">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-121">Total revenue this year</span></span></li><li><span data-ttu-id="e21b7-122">إجمالي إيراد الموازنة هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="e21b7-123">المصروفات</span><span class="sxs-lookup"><span data-stu-id="e21b7-123">Expense</span></span>                     | <ul><li><span data-ttu-id="e21b7-124">إجمالي المصروفات هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-124">Total expenses this year</span></span></li><li><span data-ttu-id="e21b7-125">هدف للمصروفات استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="e21b7-126">الإيراد</span><span class="sxs-lookup"><span data-stu-id="e21b7-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="e21b7-127">إجمالي الإيراد هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-127">Total revenue this year</span></span></li><li><span data-ttu-id="e21b7-128">هدف للإيراد استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="e21b7-129">صافي الدخل</span><span class="sxs-lookup"><span data-stu-id="e21b7-129">Net income</span></span>                  | <ul><li><span data-ttu-id="e21b7-130">صافي الدخل هذه السنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-130">Net income this year</span></span></li><li><span data-ttu-id="e21b7-131">هدف لصافي الدخل استنادًا إلى الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="e21b7-132">توسيع محتوى Power BI</span><span class="sxs-lookup"><span data-stu-id="e21b7-132">Extending the Power BI content</span></span>
<span data-ttu-id="e21b7-133">باستخدام حزم المحتوى المتاحة في Microsoft Dynamics Lifecycle Services (LCS)، يمكنك تقديم تحليلات رائعة للأشخاص الذين لم يقوموا بتسجيل الدخول إلى Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e21b7-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="e21b7-134">يمكنك تعديل حزم المحتوى هذه بحيث تتضمن تقارير أخرى أو رسوم مرئية، ثم قم بنشر حزم المحتوى لمستأجر Power BI.com الخاص بك لتحليلها.</span><span class="sxs-lookup"><span data-stu-id="e21b7-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="e21b7-135">يمكنك العثور على محتوى Power BI **القيمة الفعلية مقابل الموازنة** في مكتبة الأصول المشتركة في LCS.</span><span class="sxs-lookup"><span data-stu-id="e21b7-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="e21b7-136">للمزيد من المعلومات حول كيفية تنزيل المحتوى وتطبيقه في مؤسستك، راجع [محتوى Power BI في LCS من Microsoft والشركاء‬‏‫](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="e21b7-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="e21b7-137">لمشاهدة عرض توضيحي يعرض كيفية تطبيق محتوى Power BI، راجع [محتوى Power BI من Microsoft والشركاء في Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w)Office Mix.</span><span class="sxs-lookup"><span data-stu-id="e21b7-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="e21b7-138">فهم نموذج البيانات والكيانات</span><span class="sxs-lookup"><span data-stu-id="e21b7-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="e21b7-139">الكيان</span><span class="sxs-lookup"><span data-stu-id="e21b7-139">Entity</span></span>                    | <span data-ttu-id="e21b7-140">المحتويات</span><span class="sxs-lookup"><span data-stu-id="e21b7-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="e21b7-141">أنشطة دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="e21b7-141">General Ledger Activities</span></span> | <span data-ttu-id="e21b7-142">مبالغ الحركات لدفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="e21b7-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="e21b7-143">أنشطة الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-143">Budget Activities</span></span>         | <span data-ttu-id="e21b7-144">مبالغ الحركات لسجل الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="e21b7-145">الحسابات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="e21b7-145">Main Accounts</span></span>             | <span data-ttu-id="e21b7-146">الحسابات الرئيسية لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="e21b7-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="e21b7-147">التقويمات المالية</span><span class="sxs-lookup"><span data-stu-id="e21b7-147">Fiscal Calendars</span></span>          | <span data-ttu-id="e21b7-148">التقويمات المالية لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="e21b7-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="e21b7-149">دفاتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e21b7-149">Ledgers</span></span>                   | <span data-ttu-id="e21b7-150">دفاتر الأستاذ التي يمكن استخدامها لتصفية التقرير إلى دفتر الأستاذ الحالي</span><span class="sxs-lookup"><span data-stu-id="e21b7-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="e21b7-151">أكواد الموازنة</span><span class="sxs-lookup"><span data-stu-id="e21b7-151">Budget Codes</span></span>              | <span data-ttu-id="e21b7-152">أكواد الموازنة لاستخدامها لتصفية التقارير</span><span class="sxs-lookup"><span data-stu-id="e21b7-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="e21b7-153">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="e21b7-153">Legal Entities</span></span>            | <span data-ttu-id="e21b7-154">الكيانات القانونية التي يمكن استخدامها لتصفية التقرير إلى الكيان القانوني الحالي</span><span class="sxs-lookup"><span data-stu-id="e21b7-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

