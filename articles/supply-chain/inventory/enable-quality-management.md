---
title: نظرة عامة على إدارة الجودة
description: يصف هذا الموضوع كيفية استخدام إدارة الجودة في Dynamics 365 Supply Chain Management للمساعدة في تحسين جودة المنتج في سلسلة التوريد.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814388"
---
# <a name="quality-management-overview"></a><span data-ttu-id="ca9f3-103">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca9f3-104">يصف هذا الموضوع كيفية استخدام إدارة الجودة في Dynamics 365 Supply Chain Management للمساعدة في تحسين جودة المنتج في سلسلة التوريد.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="ca9f3-105">ويمكن أن تساعدك إدارة الجودة في إدارة تنظيم أوقات الإنتاج عندما تتعامل مع المنتجات غير المتوافقة، بغض النظر عن نقطة الأصل.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="ca9f3-106">ولأن أنواع التشخيص مرتبطة بالإبلاغ عن التصحيحات، بإمكان Supply Chain Management جدولة المهام لحل المشاكل ومنع تكرارها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="ca9f3-107">وبالإضافة إلى وظيفة إدارة عدم التوافق، تتضمن إدارة الجودة وظيفة تعقب المشكلات حسب نوع المشكلة (حتى المشكلات الداخلية، ولتحديد الحلول قصيرة الأجل أو طويلة الأجل.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="ca9f3-108">وتوفر إحصاءات مؤشرات الأداء الرئيسية (KPIs) رؤية في مشاكل عدم التوافق التي حدثت مسبقاً والحلول التي تم تطبيقها لتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="ca9f3-109">ويمكنك استخدام البيانات التاريخية للمساعدة على مراجعة فعالية تدابير الجودة التي تم اتخاذها سابقًا لتحديد التدابير المناسبة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="ca9f3-110">عند إعداد اقتران جودة، يمكن لتطبيق Supply Chain Management إنشاء أوامر الجودة لمختلف الأعمال والأحداث والشروط.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="ca9f3-111">ويمكن لاقتران الجودة تغطية صنف محدد أو مجموعة محددة من الأصناف أو كافة الأصناف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="ca9f3-112">أمثلة على استخدام إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-112">Examples of the use of quality management</span></span>
<span data-ttu-id="ca9f3-113">تتسم إدارة الجودة بالمرونة ويمكن تنفيذها بطرق مختلفة للوفاء بمتطلبات مستويات محددة من عمليات سلاسل التوريد.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="ca9f3-114">توضح الأمثلة التالية الاستخدامات المحتملة لهذه الميزات:</span><span class="sxs-lookup"><span data-stu-id="ca9f3-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="ca9f3-115">بدء عملية مراقبة الجودة، استناداً إلى معايير محددة مسبقاً (عند تسجيل المستودع لأمر شراء من مورد معين) تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="ca9f3-116">حظر المخزون أثناء الفحص لمنع استخدام المخزون غير المعتمد (الحظر الكامل لكميات أمر الشراء).</span><span class="sxs-lookup"><span data-stu-id="ca9f3-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="ca9f3-117">استخدام عينات الصنف كجزء من اقتران الجودة لتحديد كمية المخزون الفعلي الحالي الذي يجب فحصه.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="ca9f3-118">يمكن لأخذ العينات الاستناد إلى نسبة مئوية أو كميات ثابتة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="ca9f3-119">إنشاء أوامر الجودة لإيصالات الاستلام الجزئية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="ca9f3-120">لإنشاء أمر جودة يستند إلى الكمية التي تم استلامها فعليًا مع أمر ما، يجب عليك تحديد خانة الاختيار **حسب الكمية المحدثة** في النموذج **أخذ عينات للصنف**.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="ca9f3-121">إنشاء أنواع الاختبار التي تتضمن الحد الأدنى، والحد الأقصى، وقيم الاختبار المستهدفة، وإجراء اختبار النوعية مقابل الكمية الذي له نتائج تحقق محددة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="ca9f3-122">تحديد مستوى جودة مقبول (AQL) للتحكم في تفاوتات قياس الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="ca9f3-123">تحديد الموارد التي تتطلب عملية فحص، مثل منطقة اختبار وأدوات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="ca9f3-124">العمل مع عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-124">Working with quality associations</span></span>
<span data-ttu-id="ca9f3-125">يمكن ربط عملية الأعمال التي تستخدم اقتران جودة بمستندات مصدر مختلفة، مثل أوامر الشراء أو أوامر المبيعات أو أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="ca9f3-126">كما يقوم كل سجل من سجلات عمليات اقتران الجودة بتعريف مجموعة الاختبارات ومستوى الجودة المقبول (AQL) وعينة خطة تنطبق على أوامر الجودة التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="ca9f3-127">ويجب تحديد سجل اقتران جودة لكل فرق في عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="ca9f3-128">على سبيل المثال، يمكنك إعداد اقتران جودة يقوم بإنشاء أمر جودة عند تحديث إيصال استلام منتج أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="ca9f3-129">واستنادًا إلى إعداد خطة التنفيذ، يمكن حظر عملية التشغيل نفسها، بينما هناك أمر جودة مفتوح، أو يمكن خظر العمليات التالية، مثل فوترة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="ca9f3-130">**ملاحظة:** أثناء وجود أوامر الجودة المفتوحة، يتم حظر إصدار كميات المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="ca9f3-131">واستناداً إلى إعداد **الحظر الكامل** في صفحة **عينات الصنف**، تكون الكمية هي أما الكمية الموجودة في أمر الجودة أو الكمية الموجودة في بند المستند المصدر.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="ca9f3-132">وفي عملية أعمال محددة، يحدد سجل اقتران الجودة الحدث والظروف التي يتم إنشاء أمر جودة لها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="ca9f3-133">ويمكن أن تكون الظروف خاصة بموقع أو كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="ca9f3-134">ويمكن إنشاء أمر الجودة الذي يتضمن اختبارات تحديد القدرة فقط عند توفر مخزون للحدث.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="ca9f3-135">توضح الأمثلة التالية كيفية تعريف سجل اقتران الجودة بالنسبة للتباينات في كل عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="ca9f3-136">وتم أيضًا تلخيص الأمثلة في الرسم التخطيطي التالي من حيث الأحداث والشروط التي تم تعريفها عن طريق سجل اقتران الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="ca9f3-137">نوع المرجع</span><span class="sxs-lookup"><span data-stu-id="ca9f3-137">Reference type</span></span></th>
<th><span data-ttu-id="ca9f3-138">نوع الحدث</span><span class="sxs-lookup"><span data-stu-id="ca9f3-138">Event type</span></span></th>
<th><span data-ttu-id="ca9f3-139">التنفيذ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-139">Execution</span></span></th>
<th><span data-ttu-id="ca9f3-140">حظر الحدث</span><span class="sxs-lookup"><span data-stu-id="ca9f3-140">Event blocking</span></span></th>
<th><span data-ttu-id="ca9f3-141">مرجع المستند</span><span class="sxs-lookup"><span data-stu-id="ca9f3-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-142">المخزون</span><span class="sxs-lookup"><span data-stu-id="ca9f3-142">Inventory</span></span></td>
<td><span data-ttu-id="ca9f3-143">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="ca9f3-143">Not applicable</span></span></td>
<td><span data-ttu-id="ca9f3-144">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="ca9f3-144">Not applicable</span></span></td>
<td><span data-ttu-id="ca9f3-145">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-145">None</span></span></td>
<td><span data-ttu-id="ca9f3-146">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="ca9f3-147">المبيعات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="ca9f3-148">تمت جدولة عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ca9f3-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="ca9f3-149">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-149">Before</span></span></td>
<td><span data-ttu-id="ca9f3-150">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="ca9f3-151">معرف محدد أو المجموعة أو الكل فقط</span><span class="sxs-lookup"><span data-stu-id="ca9f3-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-152">عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ca9f3-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-153">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-154">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9f3-155">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-156">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-156">Before</span></span></td>
<td><span data-ttu-id="ca9f3-157">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-158">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-159">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="ca9f3-160">شراء</span><span class="sxs-lookup"><span data-stu-id="ca9f3-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="ca9f3-161">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="ca9f3-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="ca9f3-162">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-162">Before</span></span></td>
<td><span data-ttu-id="ca9f3-163">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-164">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="ca9f3-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-165">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-166">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9f3-167">بعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-167">After</span></span></td>
<td><span data-ttu-id="ca9f3-168">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-169">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-170">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9f3-171">تسجيل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-172">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="ca9f3-172">Not applicable</span></span></td>
<td><span data-ttu-id="ca9f3-173">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-174">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-175">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ca9f3-176">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-177">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-177">Before</span></span></td>
<td><span data-ttu-id="ca9f3-178">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-179">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-180">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ca9f3-181">بعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-181">After</span></span></td>
<td><span data-ttu-id="ca9f3-182">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-183">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="ca9f3-184">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ca9f3-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-185">تسجيل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-186">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="ca9f3-186">Not applicable</span></span></td>
<td><span data-ttu-id="ca9f3-187">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="ca9f3-188">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-189">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-190">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ca9f3-191">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-192">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-192">Before</span></span></td>
<td><span data-ttu-id="ca9f3-193">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-194">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-195">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ca9f3-196">بعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-196">After</span></span></td>
<td><span data-ttu-id="ca9f3-197">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-198">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ca9f3-199">العزل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-200">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="ca9f3-201">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-201">Before</span></span></td>
<td><span data-ttu-id="ca9f3-202">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-203">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-204">بعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-204">After</span></span></td>
<td><span data-ttu-id="ca9f3-205">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-206">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-206">End</span></span></td>
<td><span data-ttu-id="ca9f3-207">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-207">Before</span></span></td>
<td><span data-ttu-id="ca9f3-208">نهاية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9f3-209">مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-210">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="ca9f3-211">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-211">Before</span></span></td>
<td><span data-ttu-id="ca9f3-212">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-213">المعرف الخاص، والمجموعة، أو الكل، والمورد المحدد، أو المجموعة، أو الكل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-214">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-215">بعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-215">After</span></span></td>
<td><span data-ttu-id="ca9f3-216">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9f3-217">إنتاج المنتج المساعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-217">Co-product production</span></span></td>
<td><span data-ttu-id="ca9f3-218">تسجيل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-218">Registration</span></span></td>
<td><span data-ttu-id="ca9f3-219">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="ca9f3-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-220">بلا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9f3-221">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ca9f3-222">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="ca9f3-222">Report as finished</span></span></td>
<td><span data-ttu-id="ca9f3-223">قبل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-224">بعد</span><span class="sxs-lookup"><span data-stu-id="ca9f3-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ca9f3-225">يوفر الجدول التالي مزيدًا من المعلومات حول كيفية إنشاء أوامر الجودة لأنواع معينة من العمليات.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="ca9f3-226">نوع العملية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-226">Type of process</span></span></th>
<th><span data-ttu-id="ca9f3-227">عند إمكانية إنشاء أوامر الجودة تلقائياً</span><span class="sxs-lookup"><span data-stu-id="ca9f3-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="ca9f3-228">وقت إمكانية إنشاء أوامر الجودة في حالة تطلب اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="ca9f3-229">معلومات الظروف</span><span class="sxs-lookup"><span data-stu-id="ca9f3-229">Condition information</span></span></th>
<th><span data-ttu-id="ca9f3-230">معلومات الإنشاء اليدوي</span><span class="sxs-lookup"><span data-stu-id="ca9f3-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-231">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="ca9f3-231">Purchase order</span></span></td>
<td><span data-ttu-id="ca9f3-232">قبل أو بعد ترحيل قائمة عمليات الاستلام أو استلام المنتج للمادة التي تم استلامها</span><span class="sxs-lookup"><span data-stu-id="ca9f3-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="ca9f3-233">بعد ترحيل إيصال استلام المنتج للمواد التي تم استلامها، لأن المواد يجب أن تتوفر لإجراء اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="ca9f3-234">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9f3-235">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر شراء أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-236">أمر إدخال مخزن العزل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-236">Quarantine order</span></span></td>
<td><span data-ttu-id="ca9f3-237">قبل أو بعد الإبلاغ عن أمر العزل كمنتهٍ أو مكتمل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="ca9f3-238">لا يمكن إنشاء أوامر الجودة التي تتطلب إجراء اختبارات تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="ca9f3-239">ويُفترض أن تتولى وظيفة أمر العزل التخلص من المواد التي تم إتلافها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="ca9f3-240">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9f3-241">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر عزل أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-242">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-242">Sales order</span></span></td>
<td><span data-ttu-id="ca9f3-243">قبل تحديث عملية الانتقاء المجدولة أو إيصال التعبئة للأصناف التي يتم شحنها</span><span class="sxs-lookup"><span data-stu-id="ca9f3-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="ca9f3-244">في أي خطوة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-244">At any step</span></span></td>
<td><span data-ttu-id="ca9f3-245">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو عميلاً بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9f3-246">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر مبيعات أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-247">أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ca9f3-247">Production order</span></span></td>
<td><span data-ttu-id="ca9f3-248">قبل أو بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ca9f3-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="ca9f3-249">بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ca9f3-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="ca9f3-250">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9f3-251">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر إنتاج أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-252">أمر الإنتاج الذي يشتمل على عملية مسار</span><span class="sxs-lookup"><span data-stu-id="ca9f3-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="ca9f3-253">قبل أو بعد انتهاء تقرير لعملية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="ca9f3-254">بعد الإبلاغ عن انتهاء الإنتاج للعملية الأخيرة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="ca9f3-255">وقد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو مورد عمليات أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9f3-256">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لعملية مسار أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-257">المخزون</span><span class="sxs-lookup"><span data-stu-id="ca9f3-257">Inventory</span></span></td>
<td><span data-ttu-id="ca9f3-258">لا يمكن إنشاء أمر الجودة تلقائيًا لإحدى الحركات الواردة في دفتر يومية المخزون أو لحركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ca9f3-259">يجب إنشاء أمر جودة يدويًا لكمية مخزون الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="ca9f3-260">المخزون الفعلي المتوفر مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="ca9f3-261">أمثلة الإنشاء التلقائي لأمر الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="ca9f3-262">الشراء</span><span class="sxs-lookup"><span data-stu-id="ca9f3-262">Purchasing</span></span>

<span data-ttu-id="ca9f3-263">في الشراء، إذا قمت بتعيين حقل **نوع الحدث** إلى **إيصال استلام المنتجات** وحقل **التنفيذ** إلى **بعد** في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="ca9f3-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="ca9f3-264">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **نعم**، يتم إنشاء أمر الجودة لكل إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة والإعدادات الموجودة في أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="ca9f3-265">في كل مرة يتم فيها استلام كمية مقابل أمر الشراء، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المستلمة حديثًا.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="ca9f3-266">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **لا**، يتم إنشاء أمر الجودة لأول إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="ca9f3-267">بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="ca9f3-268">لا يتم إنشاء أوامر الجودة لعمليات الاستلام اللاحقة مقابل أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="ca9f3-269">مواصفات الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-269">Quality specification</span></span></th>
<th><span data-ttu-id="ca9f3-270">حسب الكمية المحدثة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="ca9f3-271">حسب بُعد التعقب</span><span class="sxs-lookup"><span data-stu-id="ca9f3-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="ca9f3-272">النتيجة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-273">النسبة: 10%</span><span class="sxs-lookup"><span data-stu-id="ca9f3-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="ca9f3-274">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-275">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-275">Batch number: No</span></span></p>
<p><span data-ttu-id="ca9f3-276">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9f3-277">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="ca9f3-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="ca9f3-278">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="ca9f3-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ca9f3-279">أمر الجودة رقم 1 من 3 (10% من 30%)</span><span class="sxs-lookup"><span data-stu-id="ca9f3-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-280">الإبلاغ كمنته لنسبة 70</span><span class="sxs-lookup"><span data-stu-id="ca9f3-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="ca9f3-281">أمر الجودة رقم 2 لـ 7 (10%من كمية الأمر المتبقية، والتي تساوي 70 في هذه الحالة)</span><span class="sxs-lookup"><span data-stu-id="ca9f3-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-282">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ca9f3-283">لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-283">No</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-284">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-284">Batch number: No</span></span></p>
<p><span data-ttu-id="ca9f3-285">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="ca9f3-286">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="ca9f3-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="ca9f3-287">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="ca9f3-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ca9f3-288">يتم إنشاء #1 أمر الجودة لـ 1 (للكمية الأولى التي تم الإبلاغ عنها كمنتهِ، والتي لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="ca9f3-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="ca9f3-289">لا يتم إنشاء المزيد من أوامر الجودة مقابل الكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-290">الإبلاغ كمنته لـ 10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="ca9f3-291">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-292">الإبلاغ كمنته لـ 60</span><span class="sxs-lookup"><span data-stu-id="ca9f3-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="ca9f3-293">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-294">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ca9f3-295">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-296">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ca9f3-297">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9f3-298">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ca9f3-299">الإبلاغ كمنته لنسبة 3</span><span class="sxs-lookup"><span data-stu-id="ca9f3-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="ca9f3-300">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="ca9f3-301">أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</span><span class="sxs-lookup"><span data-stu-id="ca9f3-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="ca9f3-302">أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</span><span class="sxs-lookup"><span data-stu-id="ca9f3-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-303">الإبلاغ كمنته لنسبة 2</span><span class="sxs-lookup"><span data-stu-id="ca9f3-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="ca9f3-304">أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</span><span class="sxs-lookup"><span data-stu-id="ca9f3-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="ca9f3-305">أمر الجودة رقم 5 لـ1 من الدفعة رقم b5، مسلسل s5</span><span class="sxs-lookup"><span data-stu-id="ca9f3-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="ca9f3-306"><strong>ملاحظة:</strong> يُمكن إعادة استخدام الدفعة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-307">كمية ثابتة: 2</span><span class="sxs-lookup"><span data-stu-id="ca9f3-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="ca9f3-308">لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-308">No</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-309">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ca9f3-310">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9f3-311">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ca9f3-312">الإبلاغ كمنته لنسبة 4</span><span class="sxs-lookup"><span data-stu-id="ca9f3-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="ca9f3-313">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="ca9f3-314">أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="ca9f3-315">أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="ca9f3-316">أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="ca9f3-317">لا يتم إنشاء المزيد من أوامر الجودة مقابل الكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-318">الإبلاغ كمنته لنسبة 6</span><span class="sxs-lookup"><span data-stu-id="ca9f3-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="ca9f3-319">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="ca9f3-320">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="ca9f3-320">Production</span></span>

<span data-ttu-id="ca9f3-321">في الإنتاج، إذا قمت بتعيين حقل **نوع الحدث** إلى **الإبلاغ كمنته** وحقل **التنفيذ** إلى **بعد** في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="ca9f3-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="ca9f3-322">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **نعم**، يتم إنشاء أمر الجودة بناءً على كل كمية منتهية والإعدادات الموجودة في أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="ca9f3-323">في كل مرة يتم فيها الإبلاغ عن كمية كمنتهي مقابل أمر الإنتاج، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المنتهية حديثًا.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="ca9f3-324">يتناسق منطق الإنشاء هذا مع الشراء.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="ca9f3-325">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **لا**، يتم إنشاء أمر الجودة في أول مرة يتم الإبلاغ فيها عن منتج كمنتهي، بناءً على الكمية المنتهية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="ca9f3-326">بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب لأخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="ca9f3-327">لا يتم إنشاء أوامر الجودة للكميات المنتهية اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="ca9f3-328">مواصفات الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-328">Quality specification</span></span></th>
<th><span data-ttu-id="ca9f3-329">حسب الكمية المحدثة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="ca9f3-330">حسب بُعد التعقب</span><span class="sxs-lookup"><span data-stu-id="ca9f3-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="ca9f3-331">النتيجة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-332">النسبة: 10%</span><span class="sxs-lookup"><span data-stu-id="ca9f3-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="ca9f3-333">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-334">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-334">Batch number: No</span></span></p>
<p><span data-ttu-id="ca9f3-335">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9f3-336">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="ca9f3-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="ca9f3-337">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="ca9f3-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ca9f3-338">أمر الجودة رقم 1 من 3 (10% من 30%)</span><span class="sxs-lookup"><span data-stu-id="ca9f3-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-339">الإبلاغ كمنته لنسبة 70</span><span class="sxs-lookup"><span data-stu-id="ca9f3-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="ca9f3-340">أمر الجودة رقم 2 لـ 7 (10%من كمية الأمر المتبقية، والتي تساوي 70 في هذه الحالة)</span><span class="sxs-lookup"><span data-stu-id="ca9f3-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-341">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ca9f3-342">لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-342">No</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-343">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-343">Batch number: No</span></span></p>
<p><span data-ttu-id="ca9f3-344">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="ca9f3-345">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="ca9f3-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="ca9f3-346">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="ca9f3-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ca9f3-347">أمر الجودة رقم 1 لـ 1 (للكمية الأولى التي تم الإبلاغ عنها كمنتهِ، والتي لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="ca9f3-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="ca9f3-348">أمر الجودة رقم 2 لـ 1 (للكمية الأولى المتبقية، والتي لا يزال لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="ca9f3-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-349">الإبلاغ كمنته لـ 10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="ca9f3-350">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-351">الإبلاغ كمنته لـ 60</span><span class="sxs-lookup"><span data-stu-id="ca9f3-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="ca9f3-352">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-353">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ca9f3-354">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-355">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ca9f3-356">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9f3-357">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ca9f3-358">الإبلاغ كمنته لـ 3: 1 للدفعة b1، مسلسل s1؛ 1 للدفعة b2، مسلسل s2؛ و1 للدفعة b3 والمسلسل s3</span><span class="sxs-lookup"><span data-stu-id="ca9f3-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="ca9f3-359">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="ca9f3-360">أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</span><span class="sxs-lookup"><span data-stu-id="ca9f3-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="ca9f3-361">أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</span><span class="sxs-lookup"><span data-stu-id="ca9f3-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-362">الإبلاغ كمنتهِ لـ 2: 1 للدفعة b4 والمسلسل s4 و1 للدفعة b5 والمسلسل s5</span><span class="sxs-lookup"><span data-stu-id="ca9f3-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="ca9f3-363">أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</span><span class="sxs-lookup"><span data-stu-id="ca9f3-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="ca9f3-364">أمر الجودة رقم 5 لـ1 من الدفعة رقم b5، مسلسل s5</span><span class="sxs-lookup"><span data-stu-id="ca9f3-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="ca9f3-365"><strong>ملاحظة:</strong> يُمكن إعادة استخدام الدفعة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9f3-366">كمية ثابتة: 2</span><span class="sxs-lookup"><span data-stu-id="ca9f3-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="ca9f3-367">لا</span><span class="sxs-lookup"><span data-stu-id="ca9f3-367">No</span></span></td>
<td>
<p><span data-ttu-id="ca9f3-368">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ca9f3-369">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="ca9f3-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9f3-370">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ca9f3-371">الإبلاغ كمنته لـ 4: 1 للدفعة b1، المسلسل s1؛ 1 للدفعة b2، المسلسل s2؛ 1 للدفعة b3 والمسلسل s3 و1 للدفعة b4 والمسلسل s4</span><span class="sxs-lookup"><span data-stu-id="ca9f3-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="ca9f3-372">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="ca9f3-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="ca9f3-373">أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</span><span class="sxs-lookup"><span data-stu-id="ca9f3-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="ca9f3-374">أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</span><span class="sxs-lookup"><span data-stu-id="ca9f3-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="ca9f3-375">أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</span><span class="sxs-lookup"><span data-stu-id="ca9f3-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="ca9f3-376">أمر الجودة رقم 5 لـ 2، دون الإشارة إلى دفعة ورقم مسلسل</span><span class="sxs-lookup"><span data-stu-id="ca9f3-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9f3-377">الإبلاغ كمنتهِ لـ 6: 1 للدفعة b5 ومسلسل s5؛ 1 للدفعة b6 ومسلسل s6؛ 1 للدفعة b7 ومسلسل s7؛ و1 للدفعة b8 ومسلسل 8s؛ و1 للدفعة b9 ومسلسل s9؛ و1 للدفعة b10 ومسلسل s10</span><span class="sxs-lookup"><span data-stu-id="ca9f3-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="ca9f3-378">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="ca9f3-379">صفحات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca9f3-380">الصفحة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-380">Page</span></span></th>
<th><span data-ttu-id="ca9f3-381">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="ca9f3-381">Description</span></span></th>
<th><span data-ttu-id="ca9f3-382">مثال</span><span class="sxs-lookup"><span data-stu-id="ca9f3-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca9f3-383">عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-383">Quality associations</span></span></td>
<td><span data-ttu-id="ca9f3-384">راجع الأقسام السابقة في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="ca9f3-385">يحدد اقتران الجودة كافة المعلومات التالية لأمر جودة يتم إنشاؤه:</span><span class="sxs-lookup"><span data-stu-id="ca9f3-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="ca9f3-386">حدث الحركة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-386">The transaction event</span></span></li>
<li><span data-ttu-id="ca9f3-387">مجموعة الاختبارات التي يجب إجراؤها على الأصناف</span><span class="sxs-lookup"><span data-stu-id="ca9f3-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="ca9f3-388">مستوى الجودة المقبول (AQL)</span><span class="sxs-lookup"><span data-stu-id="ca9f3-388">The AQL</span></span></li>
<li><span data-ttu-id="ca9f3-389">خطة أخذ العينات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="ca9f3-390">يجب عليك تحديد اقتران جودة لكل فرق في العملية التجارية التي تتطلب إنشاء تلقائي لأوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="ca9f3-391">على سبيل المثال، يمكن إنشاء أمر الجودة في عمليات الأعمال لأوامر الشراء، وأوامر العزل، وأوامر المبيعات، وأوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca9f3-392">الاختبارات</span><span class="sxs-lookup"><span data-stu-id="ca9f3-392">Tests</span></span></td>
<td><span data-ttu-id="ca9f3-393">استخدم هذه الصفحة لتحديد الاختبارات الفردية وعرضها والتي تحدد ما إذا كانت منتجاتك تفي بمواصفات الجودة أم لا.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="ca9f3-394">ويمكنك تعيين واحد أو أكثر من الاختبارات الفردية لمجموعة اختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="ca9f3-395">وفي هذه الحالة، يمكنك أيضًا تحديد المعلومات الخاصة بالاختبار، مثل قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="ca9f3-396">يتم استخدام قيم القياس للاختبارات الكمية، ويتم استخدام متغيرات الاختبار لاختبارات الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="ca9f3-397">يشتمل الاختبار الكمي على نوع اختبار <strong>عدد صحيح</strong> أو <strong>كسر</strong>، ويشتمل أيضًا على وحدة قياس معيَّنة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="ca9f3-398">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات كأرقام.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="ca9f3-399">يشتمل الاختبار النوعي على نوع اختبار <strong>الخيار</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="ca9f3-400">وتتطلب الاختبارات النوعية معلومات إضافية حول متغير الاختبار الذي يتم قياسه وخياراته العديدة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="ca9f3-401">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات حسب النتيجة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="ca9f3-402">تقوم إحدى شركات التصنيع بإجراء اختبارين على المادة التي تم شراؤها وهما اختبار كمي حول جودة المادة واختبار نوعي حول حدوث تلف في التعبئة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="ca9f3-403">وتحدد الشركة معلومات إضافية حول الاختبار النوعي لتحديد متغير الاختبار (التعبئة التالفة) ونتائجه.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="ca9f3-404">تستخدم الشركة صفحة <strong>مجموعات الاختبار</strong> لتعيين الاختبارين لمجموعة اختبارات وتحديد المعلومات الخاصة بالاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="ca9f3-405">يتم تعيين مجموعة الاختبار إلى أمر الجودة بحيث يمكن للشركة تقديم تقرير بنتائج الاختبار لكلا الاختبارين.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca9f3-406">مجموعات الاختبار</span><span class="sxs-lookup"><span data-stu-id="ca9f3-406">Test groups</span></span></td>
<td><span data-ttu-id="ca9f3-407">استخدم هذه الصفحة لإعداد مجموعات الاختبار والاختبارات الفردية، والتي يتم تعيينها إلى مجموعة اختبار، وتحريرها وعرضها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="ca9f3-408">يعرض الجزء العلوي مجموعات الاختبار، ويعرض الجزء السفلي الاختبارات التي يتم تعيينها إلى مجموعة اختبار محددة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="ca9f3-409">تقوم بتعيين نُهج متعددة إلى مجموعة اختبار، بما في ذلك خطة أخذ عينات و"مستوى الجودة المقبول "(AQL) ومتطلب لاختبار تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="ca9f3-410">وعند تعيين اختبار فردي إلى مجموعة اختبار، يمكنك تحديد معلومات إضافية، مثل التسلسل والوثائق وتواريخ الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="ca9f3-411">وفي الاختبار الكمي، تتضمن المعلومات التي تحددها قيم القياس المقبولة أيضًا.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="ca9f3-412">أما في الاختبار النوعي، تتضمن المعلومات متغير الاختبار والنتيجة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="ca9f3-413">وتحدد مجموعة الاختبار التي تم تعيينها لأمر جودة مجموعة الاختبارات الافتراضية التي يجب إجراؤها على الصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="ca9f3-414">ومع ذلك، يمكن إضافة أو حذف أو تغيير الاختبارات في أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="ca9f3-415">يتم الإعلام عن نتائج كل اختبار في أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="ca9f3-416">تقوم شركة تصنيع بتعريف مجموعة اختبار لكل تباين في إرشادات الجودة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="ca9f3-417">تعكس مجموعات الاختبار المتنوعة فروقًا في خطط أخذ العينات ومجموعات الاختبارات التي تحتاج لإجرائها معًا ومستوى الجودة المقبول (AQL) والعوامل الأخرى.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="ca9f3-418">وفي الاختبارات الكمية، هناك أيضًا اختلافات في قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="ca9f3-419">ولفرض إرشادات الجودة الخاصة بها، تقوم الشركة بتعيين مجموعة اختبار لكل قاعدة لإنشاء أوامر الجودة تلقائياً في صفحة <strong>عمليات اقتران الجودة</strong>، وتقوم أيضًا بتعيين مجموعة اختبار لأوامر الجودة التي يتم إنشاؤها يدوياً.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca9f3-420">مجموعات جودة الصنف</span><span class="sxs-lookup"><span data-stu-id="ca9f3-420">Item quality groups</span></span></td>
<td><span data-ttu-id="ca9f3-421">استخدم هذه الصفحة لإعداد وتحرير وعرض الأصناف المخصصة لمجموعة الجودة أو مجموعات الجودة المخصصة للصنف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="ca9f3-422">تمثل مجموعة الجودة متطلبات الاختبار الشائعة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="ca9f3-423">وبعد تحديد متطلبات الاختبار في صفحة <strong>مجموعات الاختبار</strong>، يمكنك تحديد القواعد لإنشاء أوامر الجودة تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="ca9f3-424">ولتبسيط العملية، لا يلزمك تحديد قواعد للأصناف الفردية.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="ca9f3-425">وبدلاً من ذلك، يمكنك تحديد قواعد لمجموعة جودة، من خلال استخدام صفحة <strong>عمليات اقتران الجودة</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="ca9f3-426">ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لمجموعة جودة محددة لتعيين الأصناف ذات الصلة لهذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="ca9f3-427">ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لصنف محدد لتعيين مجموعات الجودة ذات الصلة لهذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="ca9f3-428">تقوم الشركة المصنعة بشراء العديد من المواد الخام المتعددة التي لها نفس متطلبات الاختبار الخاصة بالفحص الوارد.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="ca9f3-429">وتحدد الشركة مجموعة الجودة، ثم تقوم بتعيين أرقام الأصناف المرتبطة بالمواد الخام إلى تلك المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="ca9f3-430">ولاحقاً، تشتري الشركة نوعًا جديدًا من المواد الخام له نفس متطلبات الاختبارات.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="ca9f3-431">وبدلاً من إعداد متطلبات الاختبار الجديدة للمواد الجديدة، تضيف الشركة رقم الصنف للمواد الجديدة إلى مجموعة الجودة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="ca9f3-432">كما تنتج نفس شركة التصنيع الأصناف التي تشتمل على نفس متطلبات اختبارات الإنتاج وتقوم بشحن الأصناف التي تشتمل على نفس متطلبات اختبارات ما قبل الشحن.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="ca9f3-433">وتحدد الشركة مجموعتي جودة إضافيتين، ثم تقوم بتعيين أرقام الأصناف ذات الصلة لكل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca9f3-434">متغيرات الاختبار</span><span class="sxs-lookup"><span data-stu-id="ca9f3-434">Test variables</span></span></td>
<td><span data-ttu-id="ca9f3-435">استخدم هذه الصفحة لتحديد وعرض المتغيرات المرتبطة باختبار جودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="ca9f3-436">وبالنسبة لكل متغير، تقوم بتحديد النتائج العديدة التي تمثل الخيارات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="ca9f3-437">ويمكنك تحديد الاختبارات في صفحة <strong>الاختبارات</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="ca9f3-438">وبالنسبة لاختبارات الجودة، يجب عليك تعيين نوع الاختبار إلى <strong>الخيار</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="ca9f3-439">واستخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار لكل اختبار فردي.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="ca9f3-440">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="ca9f3-441">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-441">This inspection test has several variables.</span></span> <span data-ttu-id="ca9f3-442">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="ca9f3-443">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca9f3-444">نتائج متغير الاختبار.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="ca9f3-445">استخدم هذه الصفحة لإعداد نتائج الاختبار الممكنة وتحريرها وعرضها لأحد متغيرات الاختبار المرتبطة باختبار الجودة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="ca9f3-446">وللحصول على كل نتيجة، تقوم بتعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="ca9f3-447">يجب تعريف المتغير ونتائجه الخاصة بكل اختبار جودة الذي يتم تحديده في صفحة <strong>الاختبارات</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="ca9f3-448">(بالنسبة لاختبارات الجودة، يتم تعيين نوع الاختبار إلى <strong>الخيار</strong> في صفحة <strong>الاختبارات‬‏‫</strong>.) ‏‫استخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار والنتيجة الافتراضية لاختبار جودة فردي.‬</span><span class="sxs-lookup"><span data-stu-id="ca9f3-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="ca9f3-449">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="ca9f3-450">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-450">This inspection test has of several variables.</span></span> <span data-ttu-id="ca9f3-451">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="ca9f3-452">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="ca9f3-453">ويتم تعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong> لكل نتيجة.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="ca9f3-454">أثناء اختبار الفحص الخاص بكل متغير، يقوم المفتش بالإعلام عن نتيجة الاختبار عن طريق تحديد إحدى النتائج.</span><span class="sxs-lookup"><span data-stu-id="ca9f3-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="ca9f3-455">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ca9f3-455">Additional resources</span></span>
--------

[<span data-ttu-id="ca9f3-456">عمليات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="ca9f3-457">إدارة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="ca9f3-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
