---
title: إنشاء تقارير القناة عبر الإنترنت
description: يوضح هذا الموضوع كيفيه إنشاء تقارير للقناة عبر الإنترنت في Microsoft Dynamics 365 Retail.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698040"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="b83d0-103">إنشاء تقارير القناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="b83d0-103">Generate online channel reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b83d0-104">يوضح هذا الموضوع كيفيه إنشاء تقارير للقناة عبر الإنترنت في Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="b83d0-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="b83d0-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="b83d0-105">Overview</span></span>

<span data-ttu-id="b83d0-106">يمكن إنشاء العديد من التقارير وعرضها في Retail لمعرفة كيفية أداء القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-106">You can generate and view several reports in Retail to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="b83d0-107">تقرير ملخص القناة</span><span class="sxs-lookup"><span data-stu-id="b83d0-107">Channel summary report</span></span>

<span data-ttu-id="b83d0-108">يعرض تقرير **‏‫ملخص قناة‬** ملخصًا بالحركات التالية للقناة المحددة:</span><span class="sxs-lookup"><span data-stu-id="b83d0-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="b83d0-109">حركات المبيعات</span><span class="sxs-lookup"><span data-stu-id="b83d0-109">Sales transactions</span></span>
- <span data-ttu-id="b83d0-110">حركات الدفع</span><span class="sxs-lookup"><span data-stu-id="b83d0-110">Payment transactions</span></span>
- <span data-ttu-id="b83d0-111">حركات الضريبة</span><span class="sxs-lookup"><span data-stu-id="b83d0-111">Tax transactions</span></span>
- <span data-ttu-id="b83d0-112">الحركات المخصومة</span><span class="sxs-lookup"><span data-stu-id="b83d0-112">Discounted transactions</span></span>

<span data-ttu-id="b83d0-113">لإنشاء تقرير **ملخص قناة**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-114">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> ‏‫تقارير المبيعات‬ \> ‏‫تقرير ملخص القناة‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-114">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="b83d0-115">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-116">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-117">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="b83d0-119">تقرير قناة المبيعات حسب السنة</span><span class="sxs-lookup"><span data-stu-id="b83d0-119">Channel sales by year report</span></span> 

<span data-ttu-id="b83d0-120">يعرض تقرير **قناة المبيعات حسب السنة‬** مقارنة للمبيعات كل سنة لمتجر معين.</span><span class="sxs-lookup"><span data-stu-id="b83d0-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="b83d0-121">قم بتحديد السنة لمقارنه المبيعات مقابلها، ويقوم التقرير بمقارنة المبيعات للسنة المحددة مع مبيعات السنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="b83d0-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="b83d0-122">لإنشاء تقرير **قناة المبيعات حسب السنة‬**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-123">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> ‏‫تقارير المبيعات‬ \> ‏‫تقرير قناة المبيعات حسب السنة‬‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-123">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="b83d0-124">أدخل سنة في الحقل **‏‫من سنة التقويم‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="b83d0-125">أدخل سنة في الحقل **إلى سنة التقويم‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="b83d0-126">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="b83d0-128">تقرير قناة المبيعات حسب الساعة</span><span class="sxs-lookup"><span data-stu-id="b83d0-128">Channel sales by hour report</span></span>

<span data-ttu-id="b83d0-129">يعرض تقرير **قناة المبيعات حسب الساعة‬** مقاييس المبيعات في الساعة لقناة محددة أو وحدة تشغيل محددة.</span><span class="sxs-lookup"><span data-stu-id="b83d0-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="b83d0-130">لإنشاء تقرير **قناة المبيعات حسب الساعة‬**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-131">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> ‏‫تقارير المبيعات‬ \> ‏‫‏‫تقرير قناة المبيعات حسب الساعة‬‬‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-131">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="b83d0-132">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-133">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-134">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-135">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="b83d0-136">تقرير أهم العملاء</span><span class="sxs-lookup"><span data-stu-id="b83d0-136">Top customers report</span></span>

<span data-ttu-id="b83d0-137">يعرض تقرير **‏‫أهم العملاء‬** مقاييس المبيعات لأهم عملاء *N* لقناة محددة أو وحدة تشغيل.</span><span class="sxs-lookup"><span data-stu-id="b83d0-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="b83d0-138">القيمة *N* هي رقم من 10 إلى 100 ومستندة إلى مقياس تجميع محدد من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b83d0-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="b83d0-139">لإنشاء تقرير **أهم العملاء**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-140">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> ‏‫تقارير المبيعات‬ \> ‏‫تقرير أهم العملاء**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-140">Go to **Retail \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="b83d0-141">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-142">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-143">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-144">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="b83d0-145">تقرير أعلى خصومات</span><span class="sxs-lookup"><span data-stu-id="b83d0-145">Top discounts report</span></span>

<span data-ttu-id="b83d0-146">يعرض تقرير **‏‫‏‫أعلى خصومات‬** مقاييس المبيعات لأعلى خصومات *N* لقناة محددة أو وحدة تشغيل.</span><span class="sxs-lookup"><span data-stu-id="b83d0-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="b83d0-147">القيمة *N* هي رقم من 10 إلى 100 ومستندة إلى مقياس تجميع محدد من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b83d0-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="b83d0-148">لإنشاء تقرير **أعلى خصومات**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-149">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> ‏‫تقارير المبيعات‬ \> ‏‫تقرير أعلى خصومات**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-149">Go to **Retail \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="b83d0-150">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-151">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-152">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="b83d0-154">تقرير أهم المنتجات</span><span class="sxs-lookup"><span data-stu-id="b83d0-154">Top products report</span></span>

<span data-ttu-id="b83d0-155">يعرض تقرير **‏‫‏‫‏‫أهم المنتجات‬** مقاييس المبيعات لأهم منتجات *N* لقناة محددة أو وحدة تشغيل.</span><span class="sxs-lookup"><span data-stu-id="b83d0-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="b83d0-156">القيمة *N* هي رقم من 10 إلى 100 ومستندة إلى مقياس تجميع محدد من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b83d0-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="b83d0-157">لإنشاء تقرير **أهم المنتجات**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-158">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> ‏‫تقارير المبيعات‬ \> ‏‫تقرير أهم المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-158">Go to **Retail \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="b83d0-159">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-160">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-161">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-162">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="b83d0-163">تقرير مبيعات الفئة</span><span class="sxs-lookup"><span data-stu-id="b83d0-163">Category sales report</span></span>

<span data-ttu-id="b83d0-164">يعرض تقرير **مبيعات الفئة** مقاييس المبيعات عبر فتره محددة لكل عقدة في تدرج هرمي للفئات لقناة محددة أو وحدة تشغيل محددة.</span><span class="sxs-lookup"><span data-stu-id="b83d0-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="b83d0-165">لإنشاء تقرير **مبيعات الفئة**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-166">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> تقارير المبيعات \> ‏‫تقرير مبيعات الفئة‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-166">Go to **Retail \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="b83d0-167">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-168">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-169">في حقل **القناة**، حدد القناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b83d0-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b83d0-170">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="b83d0-171">تقرير مبيعات المؤسسة</span><span class="sxs-lookup"><span data-stu-id="b83d0-171">Organization sales report</span></span>

<span data-ttu-id="b83d0-172">يعرض تقرير **مبيعات المؤسسة‬** أداء متاجر البيع بالتجزئة بواسطة وحدة المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="b83d0-172">The **Organization sales** report shows the performance of your retail stores by organization unit.</span></span> <span data-ttu-id="b83d0-173">يتضمن هذا التقرير كمية المبيعات والمبلغ حسب المتجر وهامش الربح لكل متجر.</span><span class="sxs-lookup"><span data-stu-id="b83d0-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="b83d0-174">تعتمد وحدة المؤسسة على التدرج الهرمي للتقارير الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="b83d0-175">لإنشاء تقرير **مبيعات المؤسسة**، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b83d0-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="b83d0-176">انتقل إلى **Retail \> ‏‫الاستعلامات والتقارير‬ \> تقارير المبيعات \> ‏‫تقرير مبيعات المؤسسة‬**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-176">Go to **Retail \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="b83d0-177">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-178">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83d0-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b83d0-179">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b83d0-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b83d0-180">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b83d0-180">Additional resources</span></span>

- [<span data-ttu-id="b83d0-181">موارد تعليمات لـ Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="b83d0-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
