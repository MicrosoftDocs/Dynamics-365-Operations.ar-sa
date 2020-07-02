---
title: أمثلة ومنطق تقرير تقادم المخزون
description: يقدم هذا الموضوع بعض الأمثله التي توضح كيفيه ترجمة نتائج تقرير تقادم المخزون.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484520"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="14aa6-103">أمثلة ومنطق تقرير تقادم المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14aa6-104">يقدم هذا الموضوع بعض الأمثله التي توضح كيفيه ترجمة نتائج تقرير **تقادم المخزون**.</span><span class="sxs-lookup"><span data-stu-id="14aa6-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="14aa6-105">ينظيم هذا التقرير القيم الفعية للكمية والمخزون لصنف أو مجموعه أصناف محددة في العديد من مستودعات الفترات.</span><span class="sxs-lookup"><span data-stu-id="14aa6-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="14aa6-106">يعرض هذا الموضوع أيضا المنطق الداخلي للتقرير.</span><span class="sxs-lookup"><span data-stu-id="14aa6-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="14aa6-107">توضح الامثله الواردة في هذا الموضوع النتائج التي يتم عرضها في تقرير **تقادم المخزون** القياسي.</span><span class="sxs-lookup"><span data-stu-id="14aa6-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="14aa6-108">ومع ذلك، نوصي باستخدام إصدار [تخزين تقرير تقادم المخزون](inventory-aging-report-storage.md) من هذا التقرير، وخاصه عندما يكون لديك العديد من الأصناف والمستودعات التي يجب معالجتها.</span><span class="sxs-lookup"><span data-stu-id="14aa6-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="14aa6-109">يعمل تخزين تقرير تقادم المخزون على حفظ كل تقرير تقوم بإنشاءه، ويظهر النتائج كصفحه تفاعليه وتخطيط، ويتيح تصدير اي تقرير محفوظ.</span><span class="sxs-lookup"><span data-stu-id="14aa6-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="14aa6-110">عينه البيانات المستخدمة في هذه الأمثلة</span><span class="sxs-lookup"><span data-stu-id="14aa6-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="14aa6-111">تستند الامثله الموجودة في هذا الموضوع إلى نموذج بيانات حركه المخزون الموضحة في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="14aa6-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="14aa6-112">إعداد أبعاد التخزين</span><span class="sxs-lookup"><span data-stu-id="14aa6-112">Storage dimension setup</span></span>

<span data-ttu-id="14aa6-113">يتضمن مثال النظام إعداد أبعاد التخزين التالي.</span><span class="sxs-lookup"><span data-stu-id="14aa6-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="14aa6-114">الاسم</span><span class="sxs-lookup"><span data-stu-id="14aa6-114">Name</span></span>      | <span data-ttu-id="14aa6-115">نشط(ة)</span><span class="sxs-lookup"><span data-stu-id="14aa6-115">Active</span></span> | <span data-ttu-id="14aa6-116">المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="14aa6-116">Physical inventory</span></span> | <span data-ttu-id="14aa6-117">المخزون المالي</span><span class="sxs-lookup"><span data-stu-id="14aa6-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="14aa6-118">الموقع</span><span class="sxs-lookup"><span data-stu-id="14aa6-118">Site</span></span>      | <span data-ttu-id="14aa6-119">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="14aa6-119">Yes</span></span>    | <span data-ttu-id="14aa6-120">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="14aa6-120">Yes</span></span>                | <span data-ttu-id="14aa6-121">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="14aa6-121">Yes</span></span>                 |
| <span data-ttu-id="14aa6-122">المستودع</span><span class="sxs-lookup"><span data-stu-id="14aa6-122">Warehouse</span></span> | <span data-ttu-id="14aa6-123">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="14aa6-123">Yes</span></span>    | <span data-ttu-id="14aa6-124">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="14aa6-124">Yes</span></span>                | <span data-ttu-id="14aa6-125">لا</span><span class="sxs-lookup"><span data-stu-id="14aa6-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="14aa6-126">نموذج المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-126">Inventory model</span></span>

<span data-ttu-id="14aa6-127">بالنسبة لمثال النظام، يكون نموذج المخزون للمنتجات التي تم إصدارها هو *FIFO* ويكون إعداد **سعر التكلفة** لنموذج المخزون هو *‏‫تضمين القيمة الفعلية‬*.</span><span class="sxs-lookup"><span data-stu-id="14aa6-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="14aa6-128">حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-128">Inventory transactions</span></span>

<span data-ttu-id="14aa6-129">يتضمن مثال النظام حركات المخزون التالية لمنتج تم إصداره والذي يحتوي علي رقم الصنف *1000*.</span><span class="sxs-lookup"><span data-stu-id="14aa6-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="14aa6-130">المرجع</span><span class="sxs-lookup"><span data-stu-id="14aa6-130">Reference</span></span>      | <span data-ttu-id="14aa6-131">الموقع</span><span class="sxs-lookup"><span data-stu-id="14aa6-131">Site</span></span> | <span data-ttu-id="14aa6-132">المستودع</span><span class="sxs-lookup"><span data-stu-id="14aa6-132">Warehouse</span></span> | <span data-ttu-id="14aa6-133">إيصال</span><span class="sxs-lookup"><span data-stu-id="14aa6-133">Receipt</span></span>   | <span data-ttu-id="14aa6-134">المشكلة</span><span class="sxs-lookup"><span data-stu-id="14aa6-134">Issue</span></span> | <span data-ttu-id="14aa6-135">التاريخ الفعلي</span><span class="sxs-lookup"><span data-stu-id="14aa6-135">Physical date</span></span> | <span data-ttu-id="14aa6-136">التاريخ المالي</span><span class="sxs-lookup"><span data-stu-id="14aa6-136">Financial date</span></span> | <span data-ttu-id="14aa6-137">الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-137">Quantity</span></span> | <span data-ttu-id="14aa6-138">مبلغ التكلفة</span><span class="sxs-lookup"><span data-stu-id="14aa6-138">Cost amount</span></span> | <span data-ttu-id="14aa6-139">مبلغ تكلفة المخزون الفعلية</span><span class="sxs-lookup"><span data-stu-id="14aa6-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="14aa6-140">أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="14aa6-140">Purchase order</span></span> | <span data-ttu-id="14aa6-141">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-141">1</span></span>    | <span data-ttu-id="14aa6-142">11</span><span class="sxs-lookup"><span data-stu-id="14aa6-142">11</span></span>        | <span data-ttu-id="14aa6-143">المشترى</span><span class="sxs-lookup"><span data-stu-id="14aa6-143">Purchased</span></span> |       | <span data-ttu-id="14aa6-144">15 مارس</span><span class="sxs-lookup"><span data-stu-id="14aa6-144">March 15</span></span>      | <span data-ttu-id="14aa6-145">15 مارس</span><span class="sxs-lookup"><span data-stu-id="14aa6-145">March 15</span></span>       | <span data-ttu-id="14aa6-146">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-146">10</span></span>       | <span data-ttu-id="14aa6-147">1,000</span><span class="sxs-lookup"><span data-stu-id="14aa6-147">1,000</span></span>       | <span data-ttu-id="14aa6-148">1,000</span><span class="sxs-lookup"><span data-stu-id="14aa6-148">1,000</span></span>                |
| <span data-ttu-id="14aa6-149">أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="14aa6-149">Purchase order</span></span> | <span data-ttu-id="14aa6-150">2</span><span class="sxs-lookup"><span data-stu-id="14aa6-150">2</span></span>    | <span data-ttu-id="14aa6-151">21</span><span class="sxs-lookup"><span data-stu-id="14aa6-151">21</span></span>        | <span data-ttu-id="14aa6-152">المشترى</span><span class="sxs-lookup"><span data-stu-id="14aa6-152">Purchased</span></span> |       | <span data-ttu-id="14aa6-153">15 مارس</span><span class="sxs-lookup"><span data-stu-id="14aa6-153">March 15</span></span>      | <span data-ttu-id="14aa6-154">15 مارس</span><span class="sxs-lookup"><span data-stu-id="14aa6-154">March 15</span></span>       | <span data-ttu-id="14aa6-155">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-155">10</span></span>       | <span data-ttu-id="14aa6-156">2,000</span><span class="sxs-lookup"><span data-stu-id="14aa6-156">2,000</span></span>       | <span data-ttu-id="14aa6-157">2,000</span><span class="sxs-lookup"><span data-stu-id="14aa6-157">2,000</span></span>                |
| <span data-ttu-id="14aa6-158">أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="14aa6-158">Purchase order</span></span> | <span data-ttu-id="14aa6-159">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-159">1</span></span>    | <span data-ttu-id="14aa6-160">11</span><span class="sxs-lookup"><span data-stu-id="14aa6-160">11</span></span>        | <span data-ttu-id="14aa6-161">تم الاستلام</span><span class="sxs-lookup"><span data-stu-id="14aa6-161">Received</span></span>  |       | <span data-ttu-id="14aa6-162">15 أبريل</span><span class="sxs-lookup"><span data-stu-id="14aa6-162">April 15</span></span>      |                | <span data-ttu-id="14aa6-163">5</span><span class="sxs-lookup"><span data-stu-id="14aa6-163">5</span></span>        |             | <span data-ttu-id="14aa6-164">375</span><span class="sxs-lookup"><span data-stu-id="14aa6-164">375</span></span>                  |
| <span data-ttu-id="14aa6-165">أمر التحويل</span><span class="sxs-lookup"><span data-stu-id="14aa6-165">Transfer order</span></span> | <span data-ttu-id="14aa6-166">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-166">1</span></span>    | <span data-ttu-id="14aa6-167">11</span><span class="sxs-lookup"><span data-stu-id="14aa6-167">11</span></span>        |           | <span data-ttu-id="14aa6-168">تم البيع</span><span class="sxs-lookup"><span data-stu-id="14aa6-168">Sold</span></span>  | <span data-ttu-id="14aa6-169">2 مايو</span><span class="sxs-lookup"><span data-stu-id="14aa6-169">May 2</span></span>         | <span data-ttu-id="14aa6-170">2 مايو</span><span class="sxs-lookup"><span data-stu-id="14aa6-170">May 2</span></span>          | <span data-ttu-id="14aa6-171">-5</span><span class="sxs-lookup"><span data-stu-id="14aa6-171">-5</span></span>       | <span data-ttu-id="14aa6-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-172">-458.33</span></span>     | <span data-ttu-id="14aa6-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-173">-458.33</span></span>              |
| <span data-ttu-id="14aa6-174">أمر التحويل</span><span class="sxs-lookup"><span data-stu-id="14aa6-174">Transfer order</span></span> | <span data-ttu-id="14aa6-175">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-175">1</span></span>    | <span data-ttu-id="14aa6-176">12</span><span class="sxs-lookup"><span data-stu-id="14aa6-176">12</span></span>        | <span data-ttu-id="14aa6-177">المشترى</span><span class="sxs-lookup"><span data-stu-id="14aa6-177">Purchased</span></span> |       | <span data-ttu-id="14aa6-178">2 مايو</span><span class="sxs-lookup"><span data-stu-id="14aa6-178">May 2</span></span>         | <span data-ttu-id="14aa6-179">2 مايو</span><span class="sxs-lookup"><span data-stu-id="14aa6-179">May 2</span></span>          | <span data-ttu-id="14aa6-180">5</span><span class="sxs-lookup"><span data-stu-id="14aa6-180">5</span></span>        | <span data-ttu-id="14aa6-181">458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-181">458.33</span></span>      | <span data-ttu-id="14aa6-182">458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-182">458.33</span></span>               |
| <span data-ttu-id="14aa6-183">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="14aa6-183">Sales order</span></span>    | <span data-ttu-id="14aa6-184">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-184">1</span></span>    | <span data-ttu-id="14aa6-185">12</span><span class="sxs-lookup"><span data-stu-id="14aa6-185">12</span></span>        |           | <span data-ttu-id="14aa6-186">تم البيع</span><span class="sxs-lookup"><span data-stu-id="14aa6-186">Sold</span></span>  | <span data-ttu-id="14aa6-187">3 مايو</span><span class="sxs-lookup"><span data-stu-id="14aa6-187">May 3</span></span>         | <span data-ttu-id="14aa6-188">3 مايو</span><span class="sxs-lookup"><span data-stu-id="14aa6-188">May 3</span></span>          | <span data-ttu-id="14aa6-189">1-</span><span class="sxs-lookup"><span data-stu-id="14aa6-189">-1</span></span>       | <span data-ttu-id="14aa6-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-190">-91.67</span></span>      | <span data-ttu-id="14aa6-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="14aa6-192">طريقة حساب الكميات والمبالغ الموجودة في كل دلو فترى</span><span class="sxs-lookup"><span data-stu-id="14aa6-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="14aa6-193">باستخدام نموذج البيانات الموضح في الأقسام السابقة، يمكنك تشغيل تقرير **تقادم المخزون** الذي يضم الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="14aa6-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="14aa6-194">**‏‫اعتبارًا من تاريخ‬:** *9 مايو، 2020*</span><span class="sxs-lookup"><span data-stu-id="14aa6-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="14aa6-195">**الموقع:** *عرض*</span><span class="sxs-lookup"><span data-stu-id="14aa6-195">**Site:** *View*</span></span>
- <span data-ttu-id="14aa6-196">**المستودع:** *رقم*</span><span class="sxs-lookup"><span data-stu-id="14aa6-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="14aa6-197">**رقم الصنف:** *الإجمالي*</span><span class="sxs-lookup"><span data-stu-id="14aa6-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="14aa6-198">**فتره التقادم:** قم بتعيين هذا الحقل ليتم إنشاء المستودعات الشهرية.</span><span class="sxs-lookup"><span data-stu-id="14aa6-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="14aa6-199">في هذه الحالة، سيكون محتوي التقرير الذي تم إنشاؤه مشابها للمثال التالي.</span><span class="sxs-lookup"><span data-stu-id="14aa6-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="14aa6-200">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="14aa6-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-201">الموقع</span><span class="sxs-lookup"><span data-stu-id="14aa6-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-202">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="14aa6-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-203">قيمة المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="14aa6-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-204">كمية قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-205">قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-206">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="14aa6-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="14aa6-210">P1:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-211">P1:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="14aa6-212">P2:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-213">P2:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="14aa6-214">P3:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-215">P3:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="14aa6-216">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-216">1000</span></span></td>
    <td><span data-ttu-id="14aa6-217">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-217">1</span></span></td>
    <td><span data-ttu-id="14aa6-218">14</span><span class="sxs-lookup"><span data-stu-id="14aa6-218">14</span></span></td>
    <td><span data-ttu-id="14aa6-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-219">1,283.33</span></span></td>
    <td><span data-ttu-id="14aa6-220">14</span><span class="sxs-lookup"><span data-stu-id="14aa6-220">14</span></span></td>
    <td><span data-ttu-id="14aa6-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-221">1,283.33</span></span></td>
    <td><span data-ttu-id="14aa6-222">91.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-223">5.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-223">5.00</span></span></td>
    <td><span data-ttu-id="14aa6-224">458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-224">458.33</span></span></td>
    <td><span data-ttu-id="14aa6-225">9.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-225">9.00</span></span></td>
    <td><span data-ttu-id="14aa6-226">825.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="14aa6-227">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-227">1000</span></span></td>
    <td><span data-ttu-id="14aa6-228">2</span><span class="sxs-lookup"><span data-stu-id="14aa6-228">2</span></span></td>
    <td><span data-ttu-id="14aa6-229">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-229">10</span></span></td>
    <td><span data-ttu-id="14aa6-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-230">2,000.00</span></span></td>
    <td><span data-ttu-id="14aa6-231">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-231">10</span></span></td>
    <td><span data-ttu-id="14aa6-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-232">2,000.00</span></span></td>
    <td><span data-ttu-id="14aa6-233">200.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-234">10.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-234">10.00</span></span></td>
    <td><span data-ttu-id="14aa6-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="14aa6-236"><strong>إجمالي 1000</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="14aa6-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="14aa6-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="14aa6-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="14aa6-243">لاحظ التفاصيل التالية في التقرير التالي:</span><span class="sxs-lookup"><span data-stu-id="14aa6-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="14aa6-244">القيم **كمية قيمة المخزون** و **قيمة المخزون** و **متوسط تكلفة الوحدة** التي تظهر في التقرير هي قيم لبعد المخزون المالي (**الموقع**، في هذه الحالة).</span><span class="sxs-lookup"><span data-stu-id="14aa6-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="14aa6-245">علي سبيل المثال، بالنسبة للموقع 1، يعرض التقرير المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="14aa6-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="14aa6-246">قيمة **كمية قيمةالمخزون** هي *14* (= 10 + 5-5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="14aa6-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="14aa6-247">قيمة **قيمةالمخزون** هي *1,283.33* (= 1,000 + 375-458.33 + 458.33 – 91.67).</span><span class="sxs-lookup"><span data-stu-id="14aa6-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="14aa6-248">قيمة **متوسط تكلفة الوحدة** هي *91.67*.</span><span class="sxs-lookup"><span data-stu-id="14aa6-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="14aa6-249">يتم حساب قيمة **‏‫قيمة المخزون الفعلي‬** وقيمة **المبلغ** في كل دلو فترة باستخدام قيمة **متوسط تكلفة الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="14aa6-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="14aa6-250">يحدد التقرير الكمية الفعلية لكل دلو فتره عن طريق تلخيص إجمالي كميه المخزون المستلمة لكل دلو فترة.</span><span class="sxs-lookup"><span data-stu-id="14aa6-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="14aa6-251">ثم يقوم بتطبيق مبدأ ما يرد أولاً يصرف أولاً (FIFO)‬ لخصم إجمالي الكمية الصادرة، بغض النظر عن نموذج المخزون الذي تستخدمه الأصناف.</span><span class="sxs-lookup"><span data-stu-id="14aa6-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="14aa6-252">إذا قمت بتشغيل نفس التقرير مره أخرى، ولكنك هذه المرة قمت بتعيين حقلي **الموقع** و **المستودوع** على *عرض* فان التقرير الجديد سيبدو كالمثال التالي.</span><span class="sxs-lookup"><span data-stu-id="14aa6-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="14aa6-253">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="14aa6-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-254">الموقع</span><span class="sxs-lookup"><span data-stu-id="14aa6-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-255">المستودع</span><span class="sxs-lookup"><span data-stu-id="14aa6-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-256">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="14aa6-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-257">قيمة المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="14aa6-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-258">كمية قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-259">قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-260">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="14aa6-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="14aa6-264">P1:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-265">P1:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="14aa6-266">P2:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-267">P2:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="14aa6-268">P3:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-269">P3:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="14aa6-270">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-270">1000</span></span></td>
    <td><span data-ttu-id="14aa6-271">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-271">1</span></span></td>
    <td><span data-ttu-id="14aa6-272">11</span><span class="sxs-lookup"><span data-stu-id="14aa6-272">11</span></span></td>
    <td><span data-ttu-id="14aa6-273">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-273">10</span></span></td>
    <td><span data-ttu-id="14aa6-274">916.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-274">916.67</span></span></td>
    <td><span data-ttu-id="14aa6-275">14</span><span class="sxs-lookup"><span data-stu-id="14aa6-275">14</span></span></td>
    <td><span data-ttu-id="14aa6-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-276">1,283.33</span></span></td>
    <td><span data-ttu-id="14aa6-277">91.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-278">5.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-278">5.00</span></span></td>
    <td><span data-ttu-id="14aa6-279">458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-279">458.33</span></span></td>
    <td><span data-ttu-id="14aa6-280">5.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-280">5.00</span></span></td>
    <td><span data-ttu-id="14aa6-281">458.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="14aa6-282">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-282">1000</span></span></td>
    <td><span data-ttu-id="14aa6-283">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-283">1</span></span></td>
    <td><span data-ttu-id="14aa6-284">12</span><span class="sxs-lookup"><span data-stu-id="14aa6-284">12</span></span></td>
    <td><span data-ttu-id="14aa6-285">4</span><span class="sxs-lookup"><span data-stu-id="14aa6-285">4</span></span></td>
    <td><span data-ttu-id="14aa6-286">366.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-286">366.67</span></span></td>
    <td><span data-ttu-id="14aa6-287">14</span><span class="sxs-lookup"><span data-stu-id="14aa6-287">14</span></span></td>
    <td><span data-ttu-id="14aa6-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="14aa6-288">1,283.33</span></span></td>
    <td><span data-ttu-id="14aa6-289">91.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-289">91.67</span></span></td>
    <td><span data-ttu-id="14aa6-290">4.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-290">4.00</span></span></td>
    <td><span data-ttu-id="14aa6-291">366.67</span><span class="sxs-lookup"><span data-stu-id="14aa6-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="14aa6-292">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-292">1000</span></span></td>
    <td><span data-ttu-id="14aa6-293">2</span><span class="sxs-lookup"><span data-stu-id="14aa6-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="14aa6-294">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-294">10</span></span></td>
    <td><span data-ttu-id="14aa6-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-295">2,000.00</span></span></td>
    <td><span data-ttu-id="14aa6-296">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-296">10</span></span></td>
    <td><span data-ttu-id="14aa6-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-297">2,000.00</span></span></td>
    <td><span data-ttu-id="14aa6-298">200.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-299">10.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-299">10.00</span></span></td>
    <td><span data-ttu-id="14aa6-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="14aa6-301"><strong>إجمالي 1000</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="14aa6-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="14aa6-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="14aa6-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="14aa6-310">في هذه المرة، يتم تقسيم الموقع 1 إلى صفين، صف للمستودع 11 وصف للمستودع 12.</span><span class="sxs-lookup"><span data-stu-id="14aa6-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="14aa6-311">ومع ذلك، تبقى القيم **كمية قيمة المخزون** و **قيمة المخزون** و **متوسط تكلفة الوحدة** كما هي لأن **المستودع** ليس بعدًا مالي لمخزون.</span><span class="sxs-lookup"><span data-stu-id="14aa6-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="14aa6-312">بالاضافه إلى ذلك، لاحظ ان توزيع الكمية للموقع 1 مختلف.</span><span class="sxs-lookup"><span data-stu-id="14aa6-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="14aa6-313">في التقرير الأول الذي قمت بتشغيله، تجاهل النظام أمر التحويل الذي حدث في نفس الموقع ويقوم بخصم كميه فاتورة المبيعات من دلو فترة **3/31/2020 - 3/1/2020** في الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="14aa6-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="14aa6-314">علي الرغم من ذلك، في التقرير الجديد، يقوم النظام بخصم كمية فاتورة المبيعات من دلو فترة **5/8/2020 - 5/1/2020** في المستودع 12.</span><span class="sxs-lookup"><span data-stu-id="14aa6-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="14aa6-315">تأثيرات إغلاق المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-315">Effects of inventory closing</span></span>

<span data-ttu-id="14aa6-316">إذا قمت بتشغيل إغلاق المخزون لشهر مايو، وقمت بتشغيل التقرير السابق مره أخرى، ولكنك قمت بتعيين الحقل **اعتبارًا من تاريخ** إلى *31 مايو 2020*، فستلاحظ النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="14aa6-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="14aa6-317">يتم تحديث **قيمة المخزون** وقيم **متوسط تكلفة الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="14aa6-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="14aa6-318">يتم تحديث قيمة **‏‫قيمة المخزون الفعلي‬** وجيمع قيم **المبلغ** في كل دلو فتره وفقا لذلك.</span><span class="sxs-lookup"><span data-stu-id="14aa6-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="14aa6-319">يشبه التقرير الجديد المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="14aa6-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="14aa6-320">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="14aa6-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-321">الموقع</span><span class="sxs-lookup"><span data-stu-id="14aa6-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-322">المستودع</span><span class="sxs-lookup"><span data-stu-id="14aa6-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-323">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="14aa6-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-324">قيمة المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="14aa6-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-325">كمية قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-326">قيمة المخزون</span><span class="sxs-lookup"><span data-stu-id="14aa6-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="14aa6-327">متوسط تكلفة الوحدة</span><span class="sxs-lookup"><span data-stu-id="14aa6-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="14aa6-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="14aa6-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="14aa6-331">P1:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-332">P1:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="14aa6-333">P2:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-334">P2:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="14aa6-335">P3:الكمية</span><span class="sxs-lookup"><span data-stu-id="14aa6-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="14aa6-336">P3:المبلغ</span><span class="sxs-lookup"><span data-stu-id="14aa6-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="14aa6-337">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-337">1000</span></span></td>
    <td><span data-ttu-id="14aa6-338">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-338">1</span></span></td>
    <td><span data-ttu-id="14aa6-339">11</span><span class="sxs-lookup"><span data-stu-id="14aa6-339">11</span></span></td>
    <td><span data-ttu-id="14aa6-340">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-340">10</span></span></td>
    <td><span data-ttu-id="14aa6-341">910.70</span><span class="sxs-lookup"><span data-stu-id="14aa6-341">910.70</span></span></td>
    <td><span data-ttu-id="14aa6-342">14</span><span class="sxs-lookup"><span data-stu-id="14aa6-342">14</span></span></td>
    <td><span data-ttu-id="14aa6-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-343">1,275.00</span></span></td>
    <td><span data-ttu-id="14aa6-344">91.07</span><span class="sxs-lookup"><span data-stu-id="14aa6-344">91.07</span></span></td>
    <td><span data-ttu-id="14aa6-345">0.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="14aa6-346">5.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-346">5.00</span></span></td>
    <td><span data-ttu-id="14aa6-347">455.36</span><span class="sxs-lookup"><span data-stu-id="14aa6-347">455.36</span></span></td>
    <td><span data-ttu-id="14aa6-348">5.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-348">5.00</span></span></td>
    <td><span data-ttu-id="14aa6-349">455.36</span><span class="sxs-lookup"><span data-stu-id="14aa6-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="14aa6-350">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-350">1000</span></span></td>
    <td><span data-ttu-id="14aa6-351">1</span><span class="sxs-lookup"><span data-stu-id="14aa6-351">1</span></span></td>
    <td><span data-ttu-id="14aa6-352">12</span><span class="sxs-lookup"><span data-stu-id="14aa6-352">12</span></span></td>
    <td><span data-ttu-id="14aa6-353">4</span><span class="sxs-lookup"><span data-stu-id="14aa6-353">4</span></span></td>
    <td><span data-ttu-id="14aa6-354">364.29</span><span class="sxs-lookup"><span data-stu-id="14aa6-354">364.29</span></span></td>
    <td><span data-ttu-id="14aa6-355">14</span><span class="sxs-lookup"><span data-stu-id="14aa6-355">14</span></span></td>
    <td><span data-ttu-id="14aa6-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-356">1,275.00</span></span></td>
    <td><span data-ttu-id="14aa6-357">91.07</span><span class="sxs-lookup"><span data-stu-id="14aa6-357">91.07</span></span></td>
    <td><span data-ttu-id="14aa6-358">4.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-358">4.00</span></span></td>
    <td><span data-ttu-id="14aa6-359">364.29</span><span class="sxs-lookup"><span data-stu-id="14aa6-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="14aa6-360">1000</span><span class="sxs-lookup"><span data-stu-id="14aa6-360">1000</span></span></td>
    <td><span data-ttu-id="14aa6-361">2</span><span class="sxs-lookup"><span data-stu-id="14aa6-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="14aa6-362">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-362">10</span></span></td>
    <td><span data-ttu-id="14aa6-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-363">2,000.00</span></span></td>
    <td><span data-ttu-id="14aa6-364">10</span><span class="sxs-lookup"><span data-stu-id="14aa6-364">10</span></span></td>
    <td><span data-ttu-id="14aa6-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-365">2,000.00</span></span></td>
    <td><span data-ttu-id="14aa6-366">200.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-367">10.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-367">10.00</span></span></td>
    <td><span data-ttu-id="14aa6-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="14aa6-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="14aa6-369"><strong>إجمالي 1000</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="14aa6-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="14aa6-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="14aa6-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="14aa6-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="14aa6-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="14aa6-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
