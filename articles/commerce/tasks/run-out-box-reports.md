---
title: إنشاء وتشغيل من التقارير الجاهزة
description: استخدم دليل المهام هذا لتشغيل التقارير الجاهزة‬ في المقر الرئيسي من مساحات عمل مختلفة واستعلامات وتقارير المبيعات ضمن Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3dd941eb4e682e61c8b3d10ef0ccd14239f090c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232703"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="981a9-103">إنشاء وتشغيل من التقارير الجاهزة</span><span class="sxs-lookup"><span data-stu-id="981a9-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="981a9-104">استخدم دليل المهام هذا لتشغيل التقارير الجاهزة‬ في المقر الرئيسي من مساحات عمل مختلفة واستعلامات وتقارير المبيعات ضمن Commerce.</span><span class="sxs-lookup"><span data-stu-id="981a9-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="981a9-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا التسجيل هي USRT.</span><span class="sxs-lookup"><span data-stu-id="981a9-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="981a9-106">ويُعد هذا السجل مخصصًا لدور ‏‫مسؤول النظام‬.</span><span class="sxs-lookup"><span data-stu-id="981a9-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="981a9-107">إصدار التقارير من مساحات العمل</span><span class="sxs-lookup"><span data-stu-id="981a9-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="981a9-108">انتقل إلى Retail and Commerce > المنتجات والفئات > إدارة الفئات والمنتجات.</span><span class="sxs-lookup"><span data-stu-id="981a9-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="981a9-109">‏‫انقر فوق السهم لتوسيع قسم "التقارير" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="981a9-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="981a9-110">انقر فوق تقرير أهم المنتجات.</span><span class="sxs-lookup"><span data-stu-id="981a9-110">Click Top products report.</span></span>
4. <span data-ttu-id="981a9-111">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="981a9-112">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="981a9-113">في حقل "القناة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="981a9-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="981a9-114">في الشجرة، حدد "Contoso Retail\Contoso Retail USA\Central\Houston".</span><span class="sxs-lookup"><span data-stu-id="981a9-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="981a9-115">يوضح ذلك التدرج الهرمي الافتراضي لمؤسسات Commerce لأغراض إعداد ‏‫تقارير البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="981a9-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="981a9-116">انتقل إلى ‏‫إدارة المؤسسة > المؤسسات >‬ ‏‫أغراض التدرج الهرمي للمؤسسات‬ واختر ‏‫"تقارير Commerce"‬، وضمن ‏‫"التدرجات الهرمية المعينة"‬، حدد ‏‫اسم التدرج الهرمي الذي سيتم تحديد العمود الافتراضي له.</span><span class="sxs-lookup"><span data-stu-id="981a9-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="981a9-117">كجزء من بيانات العرض التوضيحي‬ (المستخدمة لتسجيل هذه المهمة) ستلاحظ أن "المتاجر حسب المنطقة" هو التدرج الهرمي الافتراضي للمؤسسات لأغراض إعداد ‏‫التقارير.</span><span class="sxs-lookup"><span data-stu-id="981a9-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="981a9-118">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="981a9-118">Click OK.</span></span>
9. <span data-ttu-id="981a9-119">في حقل "عرض"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="981a9-120">في حقل "بواسطة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="981a9-121">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="981a9-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="981a9-122">بدء تشغيل التقارير من تقارير الاستعلامات والاستعلامات</span><span class="sxs-lookup"><span data-stu-id="981a9-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="981a9-123">انتقل إلى Retail and Commerce > ‏‫الاستعلامات والتقارير‬ > تقارير المبيعات > ‏‫تقرير مبيعات الفئة‬.</span><span class="sxs-lookup"><span data-stu-id="981a9-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="981a9-124">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="981a9-125">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="981a9-126">في حقل "القناة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="981a9-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="981a9-127">في الشجرة، حدد "Contoso Retail\Contoso Retail USA\West\Seattle".</span><span class="sxs-lookup"><span data-stu-id="981a9-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="981a9-128">يوضح ذلك التدرج الهرمي الافتراضي لمؤسسات Commerce لأغراض إعداد ‏‫تقارير البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="981a9-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="981a9-129">انتقل إلى ‏‫إدارة المؤسسة > المؤسسات >‬ ‏‫أغراض التدرج الهرمي للمؤسسات‬ واختر ‏‫"تقارير Commerce"‬، وضمن ‏‫"التدرجات الهرمية المعينة"‬، حدد ‏‫اسم التدرج الهرمي الذي سيتم تحديد العمود الافتراضي له.</span><span class="sxs-lookup"><span data-stu-id="981a9-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="981a9-130">كجزء من بيانات العرض التوضيحي‬ (المستخدمة لتسجيل هذه المهمة) ستلاحظ أن "المتاجر حسب المنطقة" هو التدرج الهرمي الافتراضي للمؤسسات لأغراض إعداد ‏‫التقارير.</span><span class="sxs-lookup"><span data-stu-id="981a9-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="981a9-131">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="981a9-131">Click OK.</span></span>
7. <span data-ttu-id="981a9-132">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="981a9-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="981a9-133">تصدير تقارير HQ</span><span class="sxs-lookup"><span data-stu-id="981a9-133">Export an HQ reports</span></span>
1. <span data-ttu-id="981a9-134">انتقل إلى Retail and Commerce > ‏‫الاستعلامات والتقارير‬ > تقارير المبيعات > ‏‫تقرير مبيعات المؤسسة‬.</span><span class="sxs-lookup"><span data-stu-id="981a9-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="981a9-135">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="981a9-136">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="981a9-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="981a9-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="981a9-137">Click OK.</span></span>
5. <span data-ttu-id="981a9-138">انقر فوق "تصدير".</span><span class="sxs-lookup"><span data-stu-id="981a9-138">Click Export.</span></span>
6. <span data-ttu-id="981a9-139">انقر فوق "ملف PDF‬".</span><span class="sxs-lookup"><span data-stu-id="981a9-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]