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
ms.openlocfilehash: fab0e9d5e550b1848c3483b3172836e258353ebb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249061"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="5d4ca-104">التقرير المالي لكشف الدخل</span><span class="sxs-lookup"><span data-stu-id="5d4ca-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d4ca-105">توضح هذه المقالة التقرير الافتراضي لكشوف الدخل.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="5d4ca-106">كما تصف العناصر الأساسية التي تقترن بهذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="5d4ca-107">تقرير كشف الدخل الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="5d4ca-108">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-108">Default report</span></span>             | <span data-ttu-id="5d4ca-109">مهامه</span><span class="sxs-lookup"><span data-stu-id="5d4ca-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4ca-110">بيان الدخل – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-110">Income Statement – Default</span></span> | <span data-ttu-id="5d4ca-111">يوفر عرضًا لربحية المؤسسة للفترة الحالية وكذلك السنة حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="5d4ca-112">اللبنات الأساسية</span><span class="sxs-lookup"><span data-stu-id="5d4ca-112">Building blocks</span></span>
<span data-ttu-id="5d4ca-113">يستخدم التقرير المالي لكشف الدخل اللبنات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="5d4ca-114">التقرير الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-114">Default report</span></span>             | <span data-ttu-id="5d4ca-115">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="5d4ca-115">Row definition</span></span>                     | <span data-ttu-id="5d4ca-116">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="5d4ca-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="5d4ca-117">كشف الدخل – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-117">Income Statement - Default</span></span> | <span data-ttu-id="5d4ca-118">كشف الدخل الافتراضي – الافتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="5d4ca-119">الدوري والسنة حتى تاريخه - افتراضي</span><span class="sxs-lookup"><span data-stu-id="5d4ca-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="5d4ca-120">تعريف الصف</span><span class="sxs-lookup"><span data-stu-id="5d4ca-120">Row definition</span></span>

<span data-ttu-id="5d4ca-121">يحتوي تعريف الصف، "كشف الدخل الملخص – الافتراضي"، على قسم لكل جزء من دخل الكشف التقليدي.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="5d4ca-122">ويتم استخدام بُعد "فئة الحساب الرئيسي" لإنشاء تعريف الصف هذا.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="5d4ca-123">ولذلك، يمكن لأي شخص إنشاء التقرير دون الحاجة إلى إجراء أي تعديلات.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="5d4ca-124">تعريف العمود</span><span class="sxs-lookup"><span data-stu-id="5d4ca-124">Column Definition</span></span>

<span data-ttu-id="5d4ca-125">وتحتوي تعريفات الأعمدة هذه على أنواع مختلفة من الأعمدة لتوفير مستويات مختلفة من التفاصيل والبيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="5d4ca-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="5d4ca-126">**دوري والسنة حتى تاريخه – أنواع الأعمدة الافتراضية:**</span><span class="sxs-lookup"><span data-stu-id="5d4ca-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="5d4ca-127">**DESC** – الوصف من كل تعريف صف</span><span class="sxs-lookup"><span data-stu-id="5d4ca-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="5d4ca-128">**FD** – البيانات المالية للفترة الحالية</span><span class="sxs-lookup"><span data-stu-id="5d4ca-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="5d4ca-129">**FD** – البيانات المالية للسنة حتى تاريخه</span><span class="sxs-lookup"><span data-stu-id="5d4ca-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="5d4ca-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5d4ca-130">Additional resources</span></span>
--------

[<span data-ttu-id="5d4ca-131">نظرة عامة على التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="5d4ca-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="5d4ca-132">عرض التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="5d4ca-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="5d4ca-133">مدونة التقارير المالية في Dynamics</span><span class="sxs-lookup"><span data-stu-id="5d4ca-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]