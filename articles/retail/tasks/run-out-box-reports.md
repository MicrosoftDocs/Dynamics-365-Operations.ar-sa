--- 
title: " إنشاء وتشغيل من التقارير الجاهزة"
description: "استخدم دليل المهام هذا لتشغيل التقارير الجاهزة‬ في المقر الرئيسي من مساحات عمل مختلفة واستعلامات وتقارير المبيعات ضمن \"التجارة والبيع بالتجزئة\"."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a298ff9689b460bec0a4dcf53b3ca7de8e05fb10
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="acc5f-103"> إنشاء وتشغيل من التقارير الجاهزة</span><span class="sxs-lookup"><span data-stu-id="acc5f-103">Generate and run out-of-box reports</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="acc5f-104">استخدم دليل المهام هذا لتشغيل التقارير الجاهزة‬ في المقر الرئيسي من مساحات عمل مختلفة واستعلامات وتقارير المبيعات ضمن "التجارة والبيع بالتجزئة".</span><span class="sxs-lookup"><span data-stu-id="acc5f-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="acc5f-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا التسجيل هي USRT.</span><span class="sxs-lookup"><span data-stu-id="acc5f-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="acc5f-106">ويُعد هذا السجل مخصصًا لدور ‏‫مسؤول النظام‬.</span><span class="sxs-lookup"><span data-stu-id="acc5f-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="acc5f-107">إصدار التقارير من مساحات العمل</span><span class="sxs-lookup"><span data-stu-id="acc5f-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="acc5f-108">انتقل إلى البيع بالتجزئة والتجارة > المنتجات والفئات > إدارة الفئات والمنتجات.</span><span class="sxs-lookup"><span data-stu-id="acc5f-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="acc5f-109">‏‫انقر فوق السهم لتوسيع قسم "التقارير" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="acc5f-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="acc5f-110">انقر فوق تقرير أهم المنتجات.</span><span class="sxs-lookup"><span data-stu-id="acc5f-110">Click Top products report.</span></span>
4. <span data-ttu-id="acc5f-111">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="acc5f-112">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="acc5f-113">في حقل "القناة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="acc5f-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="acc5f-114">في الشجرة، حدد "Contoso Retail\Contoso Retail USA\Central\Houston".</span><span class="sxs-lookup"><span data-stu-id="acc5f-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="acc5f-115">يوضح ذلك التدرج الهرمي الافتراضي لمؤسسات البيع بالتجزئة لأغراض إعداد ‏‫تقارير البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="acc5f-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="acc5f-116">انتقل إلى ‏‫إدارة المؤسسة > المؤسسات >‬ ‏‫أغراض التدرج الهرمي للمؤسسات‬ واختر ‏‫"تقارير البيع بالتجزئة"‬، وضمن ‏‫"التدرجات الهرمية المعينة"‬، حدد ‏‫اسم التدرج الهرمي الذي سيتم تحديد العمود الافتراضي له.</span><span class="sxs-lookup"><span data-stu-id="acc5f-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="acc5f-117">كجزء من بيانات العرض التوضيحي‬ (المستخدمة لتسجيل هذه المهمة) ستلاحظ أن "متاجر البيع بالتجزئة حسب المنطقة" هو التدرج الهرمي الافتراضي للمؤسسات لأغراض إعداد ‏‫تقارير البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="acc5f-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="acc5f-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acc5f-118">Click OK.</span></span>
9. <span data-ttu-id="acc5f-119">في حقل "عرض"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="acc5f-120">في حقل "بواسطة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="acc5f-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acc5f-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="acc5f-122">ابدأ تشغيل التقارير من الاستعلامات وتقارير المبيعات تحت ارتباط تطبيق "البيع بالتجزئة والتجارة".</span><span class="sxs-lookup"><span data-stu-id="acc5f-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="acc5f-123">انتقل إلى البيع بالتجزئة والتجارة > ‏‫الاستعلامات والتقارير‬ > تقارير المبيعات > ‏‫تقرير مبيعات الفئة‬.</span><span class="sxs-lookup"><span data-stu-id="acc5f-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="acc5f-124">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="acc5f-125">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="acc5f-126">في حقل "القناة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="acc5f-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="acc5f-127">في الشجرة، حدد "Contoso Retail\Contoso Retail USA\West\Seattle".</span><span class="sxs-lookup"><span data-stu-id="acc5f-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="acc5f-128">يوضح ذلك التدرج الهرمي الافتراضي لمؤسسات البيع بالتجزئة لأغراض إعداد ‏‫تقارير البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="acc5f-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="acc5f-129">انتقل إلى ‏‫إدارة المؤسسة > المؤسسات >‬ ‏‫أغراض التدرج الهرمي للمؤسسات‬ واختر ‏‫"تقارير البيع بالتجزئة"‬، وضمن ‏‫"التدرجات الهرمية المعينة"‬، حدد ‏‫اسم التدرج الهرمي الذي سيتم تحديد العمود الافتراضي له.</span><span class="sxs-lookup"><span data-stu-id="acc5f-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="acc5f-130">كجزء من بيانات العرض التوضيحي‬ (المستخدمة لتسجيل هذه المهمة) ستلاحظ أن "متاجر البيع بالتجزئة حسب المنطقة" هو التدرج الهرمي الافتراضي للمؤسسات لأغراض إعداد ‏‫تقارير البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="acc5f-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="acc5f-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acc5f-131">Click OK.</span></span>
7. <span data-ttu-id="acc5f-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acc5f-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="acc5f-133">تصدير تقارير HQ</span><span class="sxs-lookup"><span data-stu-id="acc5f-133">Export an HQ reports</span></span>
1. <span data-ttu-id="acc5f-134">انتقل إلى البيع بالتجزئة والتجارة > ‏‫الاستعلامات والتقارير‬ > تقارير المبيعات > ‏‫تقرير مبيعات المؤسسة‬.</span><span class="sxs-lookup"><span data-stu-id="acc5f-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="acc5f-135">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="acc5f-136">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="acc5f-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="acc5f-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acc5f-137">Click OK.</span></span>
5. <span data-ttu-id="acc5f-138">انقر فوق "تصدير".</span><span class="sxs-lookup"><span data-stu-id="acc5f-138">Click Export.</span></span>
6. <span data-ttu-id="acc5f-139">انقر فوق "ملف PDF‬".</span><span class="sxs-lookup"><span data-stu-id="acc5f-139">Click PDF.</span></span>


