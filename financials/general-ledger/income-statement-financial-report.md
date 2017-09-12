---
title: "التقرير المالي لكشف الدخل"
description: "توضح هذه المقالة التقرير الافتراضي لكشوف الدخل. كما تصف العناصر الأساسية التي تقترن بهذا التقرير."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="36230-104">التقرير المالي لكشف الدخل</span><span class="sxs-lookup"><span data-stu-id="36230-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="36230-105">توضح هذه المقالة التقرير الافتراضي لكشوف الدخل.</span><span class="sxs-lookup"><span data-stu-id="36230-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="36230-106">كما تصف العناصر الأساسية التي تقترن بهذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="36230-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="36230-107">تقرير كشف الدخل الافتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="36230-108">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-108">Default report</span></span>             | <span data-ttu-id="36230-109">مهامه</span><span class="sxs-lookup"><span data-stu-id="36230-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36230-110">بيان الدخل – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-110">Income Statement – Default</span></span> | <span data-ttu-id="36230-111">يوفر عرضًا لربحية المؤسسة للفترة الحالية وكذلك السنة حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="36230-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="36230-112">اللبنات الأساسية</span><span class="sxs-lookup"><span data-stu-id="36230-112">Building blocks</span></span>
<span data-ttu-id="36230-113">يستخدم التقرير المالي لكشف الدخل اللبنات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="36230-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="36230-114">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-114">Default report</span></span>             | <span data-ttu-id="36230-115">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="36230-115">Row definition</span></span>                     | <span data-ttu-id="36230-116">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="36230-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="36230-117">كشف الدخل – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-117">Income Statement - Default</span></span> | <span data-ttu-id="36230-118">كشف الدخل الافتراضي – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="36230-119">الدوري والسنة حتى تاريخه - افتراضي</span><span class="sxs-lookup"><span data-stu-id="36230-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="36230-120">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="36230-120">Row definition</span></span>

<span data-ttu-id="36230-121">يحتوي تعريف الصف، "كشف الدخل الملخص – الافتراضي"، على قسم لكل جزء من دخل الكشف التقليدي.</span><span class="sxs-lookup"><span data-stu-id="36230-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="36230-122">ويتم استخدام بُعد "فئة الحساب الرئيسي" لإنشاء تعريف الصف هذا.</span><span class="sxs-lookup"><span data-stu-id="36230-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="36230-123">ولذلك، يمكن لأي شخص إنشاء التقرير دون الحاجة إلى إجراء أي تعديلات.</span><span class="sxs-lookup"><span data-stu-id="36230-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="36230-124">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="36230-124">Column Definition</span></span>

<span data-ttu-id="36230-125">وتحتوي تعريفات الأعمدة هذه على أنواع مختلفة من الأعمدة لتوفير مستويات مختلفة من التفاصيل والبيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="36230-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="36230-126">**دوري والسنة حتى تاريخه – أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="36230-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="36230-127">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="36230-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="36230-128">**FD** – البيانات المالية للفترة الحالية</span><span class="sxs-lookup"><span data-stu-id="36230-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="36230-129">**FD** – البيانات المالية للسنة حتى تاريخه</span><span class="sxs-lookup"><span data-stu-id="36230-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="36230-130">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="36230-130">See also</span></span>
--------

[<span data-ttu-id="36230-131">التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="36230-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="36230-132">عرض التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="36230-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="36230-133">مدونة التقارير المالية في Dynamics</span><span class="sxs-lookup"><span data-stu-id="36230-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




