---
title: عمليات اقتران الجودة
description: يصف هذا الموضوع كيفيه استخدام عمليات اقتران الجودة في Microsoft Dynamics 365 Supply Chain Management لإنشاء أوامر الجودة المرتبطة بعمليات المبيعات والشراء والإنتاج تلقائيا.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022314"
---
# <a name="quality-associations"></a><span data-ttu-id="20965-103">عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="20965-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20965-104">يصف هذا الموضوع كيفيه استخدام عمليات اقتران الجودة في Microsoft Dynamics 365 Supply Chain Management لإنشاء أوامر الجودة المرتبطة بعمليات المبيعات والشراء والإنتاج تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="20965-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="20965-105">يحدد اقتران الجودة كافة المعلومات التالية لأمر جودة يتم إنشاؤه:</span><span class="sxs-lookup"><span data-stu-id="20965-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="20965-106">حدث الحركة</span><span class="sxs-lookup"><span data-stu-id="20965-106">The transaction event</span></span>
- <span data-ttu-id="20965-107">مجموعة الاختبارات التي يجب إجراؤها على الأصناف</span><span class="sxs-lookup"><span data-stu-id="20965-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="20965-108">مستوى الجودة المقبول (AQL)</span><span class="sxs-lookup"><span data-stu-id="20965-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="20965-109">خطة أخذ العينات</span><span class="sxs-lookup"><span data-stu-id="20965-109">The sampling plan</span></span>

<span data-ttu-id="20965-110">يجب عليك تحديد اقتران جودة لكل فرق في العملية التجارية التي تتطلب إنشاء تلقائي لأوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="20965-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="20965-111">على سبيل المثال، يمكن إنشاء أمر الجودة في عمليات الأعمال لأوامر الشراء، وأوامر العزل، وأوامر المبيعات، وأوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="20965-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="20965-112">العمل مع عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="20965-112">Working with quality associations</span></span>

<span data-ttu-id="20965-113">يمكن ربط عملية الأعمال التي تستخدم اقتران جودة بمستندات مصدر مختلفة، مثل أوامر الشراء أو أوامر المبيعات أو أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="20965-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="20965-114">كما يقوم كل سجل من سجلات عمليات اقتران الجودة بتعريف مجموعة الاختبارات ومستوى الجودة المقبول (AQL) وعينة خطة تنطبق على أوامر الجودة التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="20965-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="20965-115">ويجب تحديد سجل اقتران جودة لكل فرق في عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="20965-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="20965-116">على سبيل المثال، يمكنك إعداد اقتران جودة يقوم بإنشاء أمر جودة عند تحديث إيصال استلام منتج أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="20965-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="20965-117">ووفقا لاعداد خطه التنفيذ، فانه يمكن تامين العملية الجارية ذاتها في حين يكون هناك أمر جوده مفتوح.</span><span class="sxs-lookup"><span data-stu-id="20965-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="20965-118">وبدلا من ذلك، يمكن حظر العمليات اللاحقة، مثل فوتره أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="20965-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="20965-119">أثناء وجود أوامر الجودة المفتوحة، يتم حظر إصدار كميات المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="20965-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="20965-120">واستناداً إلى إعداد حقل **الحظر الكامل** في صفحة **عينات الصنف**، تكون الكمية هي أما الكمية الموجودة في أمر الجودة أو الكمية الموجودة في بند المستند المصدر.</span><span class="sxs-lookup"><span data-stu-id="20965-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="20965-121">لمزيد من المعلومات، راجع [أخذ عينات عناصر إدارة الجودة](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="20965-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="20965-122">وفي عملية أعمال محددة، يحدد سجل اقتران الجودة الحدث والظروف التي يتم إنشاء أمر جودة لها.</span><span class="sxs-lookup"><span data-stu-id="20965-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="20965-123">ويمكن أن تكون الظروف خاصة بموقع أو كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="20965-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="20965-124">ويمكن إنشاء أمر الجودة الذي يتضمن اختبارات تحديد القدرة فقط عند توفر مخزون للحدث.</span><span class="sxs-lookup"><span data-stu-id="20965-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="20965-125">للعمل مع عمليات اقتران الجودة، انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> اقترانات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="20965-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="20965-126">توضح الأمثلة التالية كيفية تعريف سجل اقتران الجودة بالنسبة للتباينات في كل عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="20965-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="20965-127">وتم أيضًا تلخيص الأمثلة في الرسم التخطيطي التالي من حيث الأحداث والشروط التي تم تعريفها عن طريق سجل اقتران الجودة.</span><span class="sxs-lookup"><span data-stu-id="20965-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="20965-128">نوع المرجع</span><span class="sxs-lookup"><span data-stu-id="20965-128">Reference type</span></span></th>
<th><span data-ttu-id="20965-129">نوع الحدث</span><span class="sxs-lookup"><span data-stu-id="20965-129">Event type</span></span></th>
<th><span data-ttu-id="20965-130">التنفيذ</span><span class="sxs-lookup"><span data-stu-id="20965-130">Execution</span></span></th>
<th><span data-ttu-id="20965-131">حظر الحدث</span><span class="sxs-lookup"><span data-stu-id="20965-131">Event blocking</span></span></th>
<th><span data-ttu-id="20965-132">مرجع المستند</span><span class="sxs-lookup"><span data-stu-id="20965-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="20965-133">المخزون</span><span class="sxs-lookup"><span data-stu-id="20965-133">Inventory</span></span></td>
<td><span data-ttu-id="20965-134">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="20965-134">Not applicable</span></span></td>
<td><span data-ttu-id="20965-135">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="20965-135">Not applicable</span></span></td>
<td><span data-ttu-id="20965-136">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-136">None</span></span></td>
<td><span data-ttu-id="20965-137">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="20965-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="20965-138">المبيعات</span><span class="sxs-lookup"><span data-stu-id="20965-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="20965-139">تمت جدولة عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="20965-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="20965-140">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-140">Before</span></span></td>
<td><span data-ttu-id="20965-141">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="20965-142">معرف محدد أو المجموعة أو الكل فقط</span><span class="sxs-lookup"><span data-stu-id="20965-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-143">عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="20965-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-144">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="20965-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-145">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="20965-146">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="20965-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-147">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-147">Before</span></span></td>
<td><span data-ttu-id="20965-148">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-149">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="20965-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-150">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="20965-151">شراء</span><span class="sxs-lookup"><span data-stu-id="20965-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="20965-152">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="20965-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="20965-153">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-153">Before</span></span></td>
<td><span data-ttu-id="20965-154">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-155">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="20965-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-156">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="20965-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-157">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="20965-158">بعد</span><span class="sxs-lookup"><span data-stu-id="20965-158">After</span></span></td>
<td><span data-ttu-id="20965-159">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-160">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="20965-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-161">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="20965-162">تسجيل</span><span class="sxs-lookup"><span data-stu-id="20965-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-163">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="20965-163">Not applicable</span></span></td>
<td><span data-ttu-id="20965-164">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-165">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="20965-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-166">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="20965-167">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="20965-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-168">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-168">Before</span></span></td>
<td><span data-ttu-id="20965-169">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-170">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="20965-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-171">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="20965-172">بعد</span><span class="sxs-lookup"><span data-stu-id="20965-172">After</span></span></td>
<td><span data-ttu-id="20965-173">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-174">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="20965-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="20965-175">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="20965-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-176">تسجيل</span><span class="sxs-lookup"><span data-stu-id="20965-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-177">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="20965-177">Not applicable</span></span></td>
<td><span data-ttu-id="20965-178">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="20965-179">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="20965-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-180">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="20965-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-181">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="20965-182">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="20965-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-183">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-183">Before</span></span></td>
<td><span data-ttu-id="20965-184">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-185">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="20965-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-186">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="20965-187">بعد</span><span class="sxs-lookup"><span data-stu-id="20965-187">After</span></span></td>
<td><span data-ttu-id="20965-188">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-189">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="20965-190">العزل</span><span class="sxs-lookup"><span data-stu-id="20965-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-191">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="20965-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="20965-192">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-192">Before</span></span></td>
<td><span data-ttu-id="20965-193">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="20965-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-194">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-195">بعد</span><span class="sxs-lookup"><span data-stu-id="20965-195">After</span></span></td>
<td><span data-ttu-id="20965-196">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-197">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-197">End</span></span></td>
<td><span data-ttu-id="20965-198">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-198">Before</span></span></td>
<td><span data-ttu-id="20965-199">نهاية</span><span class="sxs-lookup"><span data-stu-id="20965-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="20965-200">مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="20965-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-201">الإبلاغ كمنته</span><span class="sxs-lookup"><span data-stu-id="20965-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="20965-202">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-202">Before</span></span></td>
<td><span data-ttu-id="20965-203">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-204">المعرف الخاص، والمجموعة، أو الكل، والمورد المحدد، أو المجموعة، أو الكل</span><span class="sxs-lookup"><span data-stu-id="20965-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-205">الإبلاغ كمنته</span><span class="sxs-lookup"><span data-stu-id="20965-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-206">بعد</span><span class="sxs-lookup"><span data-stu-id="20965-206">After</span></span></td>
<td><span data-ttu-id="20965-207">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="20965-208">إنتاج المنتج المساعد</span><span class="sxs-lookup"><span data-stu-id="20965-208">Co-product production</span></span></td>
<td><span data-ttu-id="20965-209">تسجيل</span><span class="sxs-lookup"><span data-stu-id="20965-209">Registration</span></span></td>
<td><span data-ttu-id="20965-210">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="20965-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-211">بلا</span><span class="sxs-lookup"><span data-stu-id="20965-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="20965-212">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="20965-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="20965-213">الإبلاغ كمنته</span><span class="sxs-lookup"><span data-stu-id="20965-213">Report as finished</span></span></td>
<td><span data-ttu-id="20965-214">قبل</span><span class="sxs-lookup"><span data-stu-id="20965-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-215">بعد</span><span class="sxs-lookup"><span data-stu-id="20965-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="20965-216">تضيف ميزة *إدارة الجودة لعمليات المستودع* إمكانيات معالجة أمر الجودة مع تعيين الإنتاج من حقل **نوع الحدث** إلى *الإبلاغ كمنته* وتعيين حقل **التنفيذ** إلى *بعد*، وتعيين عمليات الشراء من **نوع الحدث** إلى *التسجيل*.</span><span class="sxs-lookup"><span data-stu-id="20965-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="20965-217">لمزيد من المعلومات، راجع [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="20965-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="20965-218">يوفر الجدول التالي مزيدًا من المعلومات حول كيفية إنشاء أوامر الجودة لأنواع معينة من العمليات.</span><span class="sxs-lookup"><span data-stu-id="20965-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="20965-219">نوع العملية</span><span class="sxs-lookup"><span data-stu-id="20965-219">Type of process</span></span></th>
<th><span data-ttu-id="20965-220">عند إمكانية إنشاء أوامر الجودة تلقائياً</span><span class="sxs-lookup"><span data-stu-id="20965-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="20965-221">وقت إمكانية إنشاء أوامر الجودة في حالة تطلب اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="20965-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="20965-222">معلومات الظروف</span><span class="sxs-lookup"><span data-stu-id="20965-222">Condition information</span></span></th>
<th><span data-ttu-id="20965-223">معلومات الإنشاء اليدوي</span><span class="sxs-lookup"><span data-stu-id="20965-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="20965-224">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="20965-224">Purchase order</span></span></td>
<td><span data-ttu-id="20965-225">قبل أو بعد ترحيل قائمة عمليات الاستلام أو استلام المنتج للمادة التي تم استلامها</span><span class="sxs-lookup"><span data-stu-id="20965-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="20965-226">بعد ترحيل إيصال استلام المنتج للمواد التي تم استلامها، لأن المواد يجب أن تتوفر لإجراء اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="20965-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="20965-227">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="20965-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="20965-228">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر شراء أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="20965-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-229">أمر إدخال مخزن العزل</span><span class="sxs-lookup"><span data-stu-id="20965-229">Quarantine order</span></span></td>
<td><span data-ttu-id="20965-230">قبل أو بعد الإبلاغ عن أمر العزل كمنتهٍ أو مكتمل</span><span class="sxs-lookup"><span data-stu-id="20965-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="20965-231">لا يمكن إنشاء أوامر الجودة التي تتطلب إجراء اختبارات تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="20965-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="20965-232">ويُفترض أن تتولى وظيفة أمر العزل التخلص من المواد التي تم إتلافها.</span><span class="sxs-lookup"><span data-stu-id="20965-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="20965-233">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="20965-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="20965-234">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر عزل أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="20965-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-235">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="20965-235">Sales order</span></span></td>
<td><span data-ttu-id="20965-236">قبل تحديث عملية الانتقاء المجدولة أو إيصال التعبئة للأصناف التي يتم شحنها</span><span class="sxs-lookup"><span data-stu-id="20965-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="20965-237">في أي خطوة</span><span class="sxs-lookup"><span data-stu-id="20965-237">At any step</span></span></td>
<td><span data-ttu-id="20965-238">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو عميلاً بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="20965-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="20965-239">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر مبيعات أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="20965-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-240">أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="20965-240">Production order</span></span></td>
<td><span data-ttu-id="20965-241">قبل أو بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="20965-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="20965-242">بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="20965-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="20965-243">يمكن أن تعكس متطلبات أمر الجودة موقعًا أو عنصرًا معينًا، أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="20965-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="20965-244">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر إنتاج أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="20965-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-245">أمر الإنتاج الذي يشتمل على عملية مسار</span><span class="sxs-lookup"><span data-stu-id="20965-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="20965-246">قبل أو بعد انتهاء تقرير لعملية</span><span class="sxs-lookup"><span data-stu-id="20965-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="20965-247">بعد الإبلاغ عن انتهاء الإنتاج للعملية الأخيرة</span><span class="sxs-lookup"><span data-stu-id="20965-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="20965-248">وقد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو مورد عمليات أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="20965-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="20965-249">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لعملية مسار أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="20965-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="20965-250">المخزون</span><span class="sxs-lookup"><span data-stu-id="20965-250">Inventory</span></span></td>
<td><span data-ttu-id="20965-251">لا يمكن إنشاء أمر الجودة تلقائيًا لإحدى الحركات الواردة في دفتر يومية المخزون أو لحركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="20965-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="20965-252">يجب إنشاء أمر جودة يدويًا لكمية مخزون الصنف.</span><span class="sxs-lookup"><span data-stu-id="20965-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="20965-253">المخزون الفعلي المتوفر مطلوب.</span><span class="sxs-lookup"><span data-stu-id="20965-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="20965-254">أمثلة حول الإنشاء التلقائي لأوامر الجودة</span><span class="sxs-lookup"><span data-stu-id="20965-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="20965-255">الشراء</span><span class="sxs-lookup"><span data-stu-id="20965-255">Purchasing</span></span>

<span data-ttu-id="20965-256">في الشراء، إذا قمت بتعيين حقل **نوع الحدث** إلى *إيصال استلام المنتجات* وحقل **التنفيذ** إلى *بعد* في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="20965-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="20965-257">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى *نعم*، يتم إنشاء أمر الجودة لكل إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة والإعدادات الموجودة في أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="20965-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="20965-258">في كل مرة يتم فيها استلام كمية مقابل أمر الشراء، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المستلمة حديثًا.</span><span class="sxs-lookup"><span data-stu-id="20965-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="20965-259">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى *لا*، يتم إنشاء أمر الجودة لأول إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة.</span><span class="sxs-lookup"><span data-stu-id="20965-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="20965-260">بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب.</span><span class="sxs-lookup"><span data-stu-id="20965-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="20965-261">لا يتم إنشاء أوامر الجودة لعمليات الاستلام اللاحقة مقابل أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="20965-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="20965-262">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="20965-262">Production</span></span>

<span data-ttu-id="20965-263">في الإنتاج، إذا قمت بتعيين حقل **نوع الحدث** إلى *الإبلاغ كمنته* وحقل **التنفيذ** إلى *بعد* في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="20965-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="20965-264">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى *نعم*، يتم إنشاء أمر الجودة بناءً على كل كمية منتهية والإعدادات الموجودة في أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="20965-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="20965-265">في كل مرة يتم فيها الإبلاغ عن كمية كمنتهي مقابل أمر الإنتاج، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المنتهية حديثًا.</span><span class="sxs-lookup"><span data-stu-id="20965-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="20965-266">يتناسق منطق الإنشاء هذا مع الشراء.</span><span class="sxs-lookup"><span data-stu-id="20965-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="20965-267">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى *لا*، يتم إنشاء أمر الجودة في أول مرة يتم الإبلاغ فيها عن منتج كمنتهي، بناءً على الكمية المنتهية.</span><span class="sxs-lookup"><span data-stu-id="20965-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="20965-268">بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب لأخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="20965-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="20965-269">لا يتم إنشاء أوامر الجودة للكميات المنتهية اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="20965-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="20965-270">مواصفات الجودة</span><span class="sxs-lookup"><span data-stu-id="20965-270">Quality specification</span></span></th>
<th><span data-ttu-id="20965-271">حسب الكمية المحدثة</span><span class="sxs-lookup"><span data-stu-id="20965-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="20965-272">حسب بُعد التعقب</span><span class="sxs-lookup"><span data-stu-id="20965-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="20965-273">النتيجة</span><span class="sxs-lookup"><span data-stu-id="20965-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="20965-274">النسبة: 10%</span><span class="sxs-lookup"><span data-stu-id="20965-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="20965-275">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="20965-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="20965-276">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="20965-276">Batch number: No</span></span></p>
<p><span data-ttu-id="20965-277">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="20965-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="20965-278">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="20965-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="20965-279">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="20965-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="20965-280">أمر الجودة رقم 1 من 3 (10% من 30)</span><span class="sxs-lookup"><span data-stu-id="20965-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="20965-281">الإبلاغ كمنته لنسبة 70</span><span class="sxs-lookup"><span data-stu-id="20965-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="20965-282">أمر الجودة رقم 2 لـ 7 (10%من كمية الأمر المتبقية، والتي تساوي 70 في هذه الحالة)</span><span class="sxs-lookup"><span data-stu-id="20965-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="20965-283">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="20965-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="20965-284">لا</span><span class="sxs-lookup"><span data-stu-id="20965-284">No</span></span></td>
<td>
<p><span data-ttu-id="20965-285">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="20965-285">Batch number: No</span></span></p>
<p><span data-ttu-id="20965-286">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="20965-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="20965-287">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="20965-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="20965-288">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="20965-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="20965-289">أمر الجودة رقم 1 لـ 1 (للكمية الأولى التي تم الإبلاغ عنها كمنتهِ، والتي لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="20965-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="20965-290">أمر الجودة رقم 2 لـ 1 (للكمية الأولى المتبقية، والتي لا يزال لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="20965-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="20965-291">الإبلاغ كمنته لـ 10</span><span class="sxs-lookup"><span data-stu-id="20965-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="20965-292">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="20965-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="20965-293">الإبلاغ كمنته لـ 60</span><span class="sxs-lookup"><span data-stu-id="20965-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="20965-294">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="20965-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="20965-295">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="20965-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="20965-296">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="20965-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="20965-297">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="20965-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="20965-298">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="20965-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="20965-299">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="20965-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="20965-300">الإبلاغ عن الانتهاء 3:1 بالنسبة لرقم المجموعة b1، الرقم التسلسلي s1؛ 1 بالنسبة لرقم المجموعة b2، الرقم التسلسلي s2; و 1 لرقم المجموعة b3، الرقم التسلسلي s3</span><span class="sxs-lookup"><span data-stu-id="20965-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="20965-301">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="20965-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="20965-302">أمر الجودة رقم 2 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="20965-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="20965-303">أمر الجودة 3 لـ 1 من رقم الدُفعة b3، الرقم التسلسلي s3</span><span class="sxs-lookup"><span data-stu-id="20965-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="20965-304">الإبلاغ كمنته لـ 2: 1 لرقم الدُفعة b4، الرقم التسلسلي s4؛ و 1 لرقم الدُفعة b5، الرقم التسلسلي s5</span><span class="sxs-lookup"><span data-stu-id="20965-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="20965-305">أمر الجودة 4 لـ 1 من رقم الدُفعة b4، الرقم التسلسلي s4</span><span class="sxs-lookup"><span data-stu-id="20965-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="20965-306">أمر الجودة 5 لـ 1 من رقم الدُفعة b5، الرقم التسلسلي s5</span><span class="sxs-lookup"><span data-stu-id="20965-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="20965-307"><strong>ملاحظة:</strong> يُمكن إعادة استخدام الدفعة.</span><span class="sxs-lookup"><span data-stu-id="20965-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="20965-308">كمية ثابتة: 2</span><span class="sxs-lookup"><span data-stu-id="20965-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="20965-309">لا</span><span class="sxs-lookup"><span data-stu-id="20965-309">No</span></span></td>
<td>
<p><span data-ttu-id="20965-310">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="20965-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="20965-311">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="20965-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="20965-312">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="20965-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="20965-313">الإبلاغ كمنته لـ 4: 1 لرقم الدُفعة b1، الرقم التسلسلي s1؛ 1 لرقم الدُفعة b2، الرقم التسلسلي s2؛ 1 لرقم الدُفعة b3، الرقم التسلسلي s3؛ و 1 لرقم الدُفعة b4، الرقم التسلسلي s4</span><span class="sxs-lookup"><span data-stu-id="20965-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="20965-314">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="20965-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="20965-315">أمر الجودة رقم 2 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="20965-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="20965-316">أمر الجودة 3 لـ 1 من رقم الدُفعة b3، الرقم التسلسلي s3</span><span class="sxs-lookup"><span data-stu-id="20965-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="20965-317">أمر الجودة 4 لـ 1 من رقم الدُفعة b4، الرقم التسلسلي s4</span><span class="sxs-lookup"><span data-stu-id="20965-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="20965-318">أمر الجودة 5 لـ 2، بدون إشارة إلى رقم الدُفعة والرقم التسلسلي</span><span class="sxs-lookup"><span data-stu-id="20965-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="20965-319">تقرير كمنته لـ 6: 1 لرقم الدُفعة b5، الرقم التسلسلي s5؛ 1 لرقم الدُفعة b6، الرقم التسلسلي s6؛ 1 لرقم الدُفعة b7، الرقم التسلسلي s7؛ 1 لرقم الدُفعة b8، الرقم التسلسلي s8؛ 1 لرقم الدُفعة b9، الرقم التسلسلي s9؛ و 1 لرقم الدُفعة b10، الرقم التسلسلي s10</span><span class="sxs-lookup"><span data-stu-id="20965-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="20965-320">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="20965-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="20965-321">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="20965-321">Additional resources</span></span>

- [<span data-ttu-id="20965-322">عمليات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="20965-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="20965-323">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="20965-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="20965-324">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="20965-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
