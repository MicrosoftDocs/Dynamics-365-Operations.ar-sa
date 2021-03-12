---
title: التقرير المالي لكشف الدخل
description: توضح هذه المقالة التقرير الافتراضي لكشوف الدخل. كما تصف العناصر الأساسية التي تقترن بهذا التقرير.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146d4b9946c1b29105cff637fa9d8803db3d0c0f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988767"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="edf47-104">التقرير المالي لكشف الدخل</span><span class="sxs-lookup"><span data-stu-id="edf47-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edf47-105">توضح هذه المقالة التقرير الافتراضي لكشوف الدخل.</span><span class="sxs-lookup"><span data-stu-id="edf47-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="edf47-106">كما تصف العناصر الأساسية التي تقترن بهذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="edf47-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="edf47-107">تقرير كشف الدخل الافتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="edf47-108">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-108">Default report</span></span>             | <span data-ttu-id="edf47-109">مهامه</span><span class="sxs-lookup"><span data-stu-id="edf47-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edf47-110">بيان الدخل – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-110">Income Statement – Default</span></span> | <span data-ttu-id="edf47-111">يوفر عرضًا لربحية المؤسسة للفترة الحالية وكذلك السنة حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="edf47-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="edf47-112">اللبنات الأساسية</span><span class="sxs-lookup"><span data-stu-id="edf47-112">Building blocks</span></span>
<span data-ttu-id="edf47-113">يستخدم التقرير المالي لكشف الدخل اللبنات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="edf47-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="edf47-114">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-114">Default report</span></span>             | <span data-ttu-id="edf47-115">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="edf47-115">Row definition</span></span>                     | <span data-ttu-id="edf47-116">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="edf47-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="edf47-117">كشف الدخل – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-117">Income Statement - Default</span></span> | <span data-ttu-id="edf47-118">كشف الدخل الافتراضي – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="edf47-119">الدوري والسنة حتى تاريخه - افتراضي</span><span class="sxs-lookup"><span data-stu-id="edf47-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="edf47-120">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="edf47-120">Row definition</span></span>

<span data-ttu-id="edf47-121">يحتوي تعريف الصف، "كشف الدخل الملخص – الافتراضي"، على قسم لكل جزء من دخل الكشف التقليدي.</span><span class="sxs-lookup"><span data-stu-id="edf47-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="edf47-122">ويتم استخدام بُعد "فئة الحساب الرئيسي" لإنشاء تعريف الصف هذا.</span><span class="sxs-lookup"><span data-stu-id="edf47-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="edf47-123">ولذلك، يمكن لأي شخص إنشاء التقرير دون الحاجة إلى إجراء أي تعديلات.</span><span class="sxs-lookup"><span data-stu-id="edf47-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="edf47-124">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="edf47-124">Column Definition</span></span>

<span data-ttu-id="edf47-125">وتحتوي تعريفات الأعمدة هذه على أنواع مختلفة من الأعمدة لتوفير مستويات مختلفة من التفاصيل والبيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="edf47-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="edf47-126">**دوري والسنة حتى تاريخه – أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="edf47-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="edf47-127">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="edf47-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="edf47-128">**FD** – البيانات المالية للفترة الحالية</span><span class="sxs-lookup"><span data-stu-id="edf47-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="edf47-129">**FD** – البيانات المالية للسنة حتى تاريخه</span><span class="sxs-lookup"><span data-stu-id="edf47-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="edf47-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="edf47-130">Additional resources</span></span>
--------

[<span data-ttu-id="edf47-131">نظرة عامة على التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="edf47-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="edf47-132">عرض التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="edf47-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="edf47-133">مدونة التقارير المالية في Dynamics</span><span class="sxs-lookup"><span data-stu-id="edf47-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



