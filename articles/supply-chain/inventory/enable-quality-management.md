---
title: نظرة عامة على إدارة الجودة
description: يصف هذا الموضوع كيفية استخدام إدارة الجودة في Dynamics 365 Supply Chain Management للمساعدة في تحسين جودة المنتج في سلسلة التوريد.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 711ce21d0e522a737e6307e7de1889c8badd5ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005217"
---
# <a name="quality-management-overview"></a><span data-ttu-id="1a885-103">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a885-104">يصف هذا الموضوع كيفية استخدام إدارة الجودة في Dynamics 365 Supply Chain Management للمساعدة في تحسين جودة المنتج في سلسلة التوريد.</span><span class="sxs-lookup"><span data-stu-id="1a885-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="1a885-105">ويمكن أن تساعدك إدارة الجودة في إدارة تنظيم أوقات الإنتاج عندما تتعامل مع المنتجات غير المتوافقة، بغض النظر عن نقطة الأصل.</span><span class="sxs-lookup"><span data-stu-id="1a885-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="1a885-106">ولأن أنواع التشخيص مرتبطة بالإبلاغ عن التصحيحات، بإمكان Supply Chain Management جدولة المهام لحل المشاكل ومنع تكرارها.</span><span class="sxs-lookup"><span data-stu-id="1a885-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="1a885-107">وبالإضافة إلى وظيفة إدارة عدم التوافق، تتضمن إدارة الجودة وظيفة تعقب المشكلات حسب نوع المشكلة (حتى المشكلات الداخلية،) ولتحديد الحلول قصيرة الأجل أو طويلة الأجل.</span><span class="sxs-lookup"><span data-stu-id="1a885-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="1a885-108">وتوفر إحصاءات مؤشرات الأداء الرئيسية (KPIs) رؤية في مشاكل عدم التوافق التي حدثت مسبقاً والحلول التي تم تطبيقها لتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="1a885-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="1a885-109">ويمكنك استخدام البيانات التاريخية للمساعدة على مراجعة فعالية تدابير الجودة التي تم اتخاذها سابقًا لتحديد التدابير المناسبة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="1a885-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="1a885-110">عند إعداد اقتران جودة، يمكن لتطبيق Supply Chain Management إنشاء أوامر الجودة لمختلف الأعمال والأحداث والشروط.</span><span class="sxs-lookup"><span data-stu-id="1a885-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="1a885-111">ويمكن لاقتران الجودة تغطية صنف محدد أو مجموعة محددة من الأصناف أو كافة الأصناف.</span><span class="sxs-lookup"><span data-stu-id="1a885-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="1a885-112">أمثلة على استخدام إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-112">Examples of the use of quality management</span></span>
<span data-ttu-id="1a885-113">تتسم إدارة الجودة بالمرونة ويمكن تنفيذها بطرق مختلفة للوفاء بمتطلبات مستويات محددة من عمليات سلاسل التوريد.</span><span class="sxs-lookup"><span data-stu-id="1a885-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="1a885-114">توضح الأمثلة التالية الاستخدامات المحتملة لهذه الميزات:</span><span class="sxs-lookup"><span data-stu-id="1a885-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="1a885-115">بدء عملية مراقبة الجودة، استناداً إلى معايير محددة مسبقاً (عند تسجيل المستودع لأمر شراء من مورد معين) تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="1a885-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="1a885-116">حظر المخزون أثناء الفحص لمنع استخدام المخزون غير المعتمد (الحظر الكامل لكميات أمر الشراء).</span><span class="sxs-lookup"><span data-stu-id="1a885-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="1a885-117">استخدام عينات الصنف كجزء من اقتران الجودة لتحديد كمية المخزون الفعلي الحالي الذي يجب فحصه.</span><span class="sxs-lookup"><span data-stu-id="1a885-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="1a885-118">يمكن أن يستند أخذ العينات إلى كميات ثابتة أو نسبة مئوية أو لوحة الترخيص الكاملة.</span><span class="sxs-lookup"><span data-stu-id="1a885-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="1a885-119">تعمل ميزة _إدارة الجودة لعمليات المستودع_ على توسيع قدرات إدارة الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="1a885-120">إذا كنت تستخدم هذه الميزة، فراجع [إدارة الجودة لعمليات المستودع](quality-management-for-warehouses-processes.md) للحصول على أمثلة حول كيفية عمل إدارة الجودة عند تمكينها.</span><span class="sxs-lookup"><span data-stu-id="1a885-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="1a885-121">إنشاء أوامر الجودة لإيصالات الاستلام الجزئية.</span><span class="sxs-lookup"><span data-stu-id="1a885-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="1a885-122">لإنشاء أمر جودة يستند إلى الكمية التي تم استلامها فعليًا مع أمر ما، يجب عليك تحديد خانة الاختيار **حسب الكمية المحدثة** في النموذج **أخذ عينات للصنف**.</span><span class="sxs-lookup"><span data-stu-id="1a885-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="1a885-123">إنشاء أنواع الاختبار التي تتضمن الحد الأدنى، والحد الأقصى، وقيم الاختبار المستهدفة، وإجراء اختبار النوعية مقابل الكمية الذي له نتائج تحقق محددة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1a885-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="1a885-124">تحديد مستوى جودة مقبول (AQL) للتحكم في تفاوتات قياس الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="1a885-125">تحديد الموارد التي تتطلب عملية فحص، مثل منطقة اختبار وأدوات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="1a885-126">العمل مع عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-126">Working with quality associations</span></span>
<span data-ttu-id="1a885-127">يمكن ربط عملية الأعمال التي تستخدم اقتران جودة بمستندات مصدر مختلفة، مثل أوامر الشراء أو أوامر المبيعات أو أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1a885-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="1a885-128">كما يقوم كل سجل من سجلات عمليات اقتران الجودة بتعريف مجموعة الاختبارات ومستوى الجودة المقبول (AQL) وعينة خطة تنطبق على أوامر الجودة التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="1a885-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="1a885-129">ويجب تحديد سجل اقتران جودة لكل فرق في عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="1a885-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="1a885-130">على سبيل المثال، يمكنك إعداد اقتران جودة يقوم بإنشاء أمر جودة عند تحديث إيصال استلام منتج أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="1a885-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="1a885-131">واستنادًا إلى إعداد خطة التنفيذ، يمكن حظر عملية التشغيل نفسها، بينما هناك أمر جودة مفتوح، أو يمكن خظر العمليات التالية، مثل فوترة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="1a885-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="1a885-132">**ملاحظة:** أثناء وجود أوامر الجودة المفتوحة، يتم حظر إصدار كميات المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="1a885-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="1a885-133">واستناداً إلى إعداد **الحظر الكامل** في صفحة **عينات الصنف**، تكون الكمية هي أما الكمية الموجودة في أمر الجودة أو الكمية الموجودة في بند المستند المصدر.</span><span class="sxs-lookup"><span data-stu-id="1a885-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="1a885-134">وفي عملية أعمال محددة، يحدد سجل اقتران الجودة الحدث والظروف التي يتم إنشاء أمر جودة لها.</span><span class="sxs-lookup"><span data-stu-id="1a885-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="1a885-135">ويمكن أن تكون الظروف خاصة بموقع أو كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="1a885-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="1a885-136">ويمكن إنشاء أمر الجودة الذي يتضمن اختبارات تحديد القدرة فقط عند توفر مخزون للحدث.</span><span class="sxs-lookup"><span data-stu-id="1a885-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="1a885-137">توضح الأمثلة التالية كيفية تعريف سجل اقتران الجودة بالنسبة للتباينات في كل عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="1a885-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="1a885-138">وتم أيضًا تلخيص الأمثلة في الرسم التخطيطي التالي من حيث الأحداث والشروط التي تم تعريفها عن طريق سجل اقتران الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1a885-139">نوع المرجع</span><span class="sxs-lookup"><span data-stu-id="1a885-139">Reference type</span></span></th>
<th><span data-ttu-id="1a885-140">نوع الحدث</span><span class="sxs-lookup"><span data-stu-id="1a885-140">Event type</span></span></th>
<th><span data-ttu-id="1a885-141">التنفيذ</span><span class="sxs-lookup"><span data-stu-id="1a885-141">Execution</span></span></th>
<th><span data-ttu-id="1a885-142">حظر الحدث</span><span class="sxs-lookup"><span data-stu-id="1a885-142">Event blocking</span></span></th>
<th><span data-ttu-id="1a885-143">مرجع المستند</span><span class="sxs-lookup"><span data-stu-id="1a885-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1a885-144">المخزون</span><span class="sxs-lookup"><span data-stu-id="1a885-144">Inventory</span></span></td>
<td><span data-ttu-id="1a885-145">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="1a885-145">Not applicable</span></span></td>
<td><span data-ttu-id="1a885-146">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="1a885-146">Not applicable</span></span></td>
<td><span data-ttu-id="1a885-147">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-147">None</span></span></td>
<td><span data-ttu-id="1a885-148">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="1a885-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="1a885-149">المبيعات</span><span class="sxs-lookup"><span data-stu-id="1a885-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="1a885-150">تمت جدولة عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="1a885-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="1a885-151">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-151">Before</span></span></td>
<td><span data-ttu-id="1a885-152">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="1a885-153">معرف محدد أو المجموعة أو الكل فقط</span><span class="sxs-lookup"><span data-stu-id="1a885-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-154">عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="1a885-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-155">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="1a885-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-156">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a885-157">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="1a885-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-158">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-158">Before</span></span></td>
<td><span data-ttu-id="1a885-159">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-160">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="1a885-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-161">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="1a885-162">شراء</span><span class="sxs-lookup"><span data-stu-id="1a885-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="1a885-163">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="1a885-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="1a885-164">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-164">Before</span></span></td>
<td><span data-ttu-id="1a885-165">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-166">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="1a885-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-167">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="1a885-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-168">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a885-169">بعد</span><span class="sxs-lookup"><span data-stu-id="1a885-169">After</span></span></td>
<td><span data-ttu-id="1a885-170">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-171">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="1a885-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-172">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a885-173">تسجيل</span><span class="sxs-lookup"><span data-stu-id="1a885-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-174">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="1a885-174">Not applicable</span></span></td>
<td><span data-ttu-id="1a885-175">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-176">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="1a885-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-177">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1a885-178">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="1a885-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-179">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-179">Before</span></span></td>
<td><span data-ttu-id="1a885-180">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-181">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="1a885-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-182">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a885-183">بعد</span><span class="sxs-lookup"><span data-stu-id="1a885-183">After</span></span></td>
<td><span data-ttu-id="1a885-184">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-185">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="1a885-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="1a885-186">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1a885-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-187">تسجيل</span><span class="sxs-lookup"><span data-stu-id="1a885-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-188">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="1a885-188">Not applicable</span></span></td>
<td><span data-ttu-id="1a885-189">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="1a885-190">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="1a885-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-191">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-192">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1a885-193">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-194">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-194">Before</span></span></td>
<td><span data-ttu-id="1a885-195">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-196">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-197">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a885-198">بعد</span><span class="sxs-lookup"><span data-stu-id="1a885-198">After</span></span></td>
<td><span data-ttu-id="1a885-199">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-200">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1a885-201">العزل</span><span class="sxs-lookup"><span data-stu-id="1a885-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-202">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1a885-203">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-203">Before</span></span></td>
<td><span data-ttu-id="1a885-204">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-205">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-206">بعد</span><span class="sxs-lookup"><span data-stu-id="1a885-206">After</span></span></td>
<td><span data-ttu-id="1a885-207">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-208">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-208">End</span></span></td>
<td><span data-ttu-id="1a885-209">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-209">Before</span></span></td>
<td><span data-ttu-id="1a885-210">نهاية</span><span class="sxs-lookup"><span data-stu-id="1a885-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a885-211">مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="1a885-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-212">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1a885-213">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-213">Before</span></span></td>
<td><span data-ttu-id="1a885-214">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-215">المعرف الخاص، والمجموعة، أو الكل، والمورد المحدد، أو المجموعة، أو الكل</span><span class="sxs-lookup"><span data-stu-id="1a885-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-216">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-217">بعد</span><span class="sxs-lookup"><span data-stu-id="1a885-217">After</span></span></td>
<td><span data-ttu-id="1a885-218">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1a885-219">إنتاج المنتج المساعد</span><span class="sxs-lookup"><span data-stu-id="1a885-219">Co-product production</span></span></td>
<td><span data-ttu-id="1a885-220">تسجيل</span><span class="sxs-lookup"><span data-stu-id="1a885-220">Registration</span></span></td>
<td><span data-ttu-id="1a885-221">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="1a885-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-222">بلا</span><span class="sxs-lookup"><span data-stu-id="1a885-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1a885-223">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="1a885-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1a885-224">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1a885-224">Report as finished</span></span></td>
<td><span data-ttu-id="1a885-225">قبل</span><span class="sxs-lookup"><span data-stu-id="1a885-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-226">بعد</span><span class="sxs-lookup"><span data-stu-id="1a885-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1a885-227">يوفر الجدول التالي مزيدًا من المعلومات حول كيفية إنشاء أوامر الجودة لأنواع معينة من العمليات.</span><span class="sxs-lookup"><span data-stu-id="1a885-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="1a885-228">نوع العملية</span><span class="sxs-lookup"><span data-stu-id="1a885-228">Type of process</span></span></th>
<th><span data-ttu-id="1a885-229">عند إمكانية إنشاء أوامر الجودة تلقائياً</span><span class="sxs-lookup"><span data-stu-id="1a885-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="1a885-230">وقت إمكانية إنشاء أوامر الجودة في حالة تطلب اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="1a885-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="1a885-231">معلومات الظروف</span><span class="sxs-lookup"><span data-stu-id="1a885-231">Condition information</span></span></th>
<th><span data-ttu-id="1a885-232">معلومات الإنشاء اليدوي</span><span class="sxs-lookup"><span data-stu-id="1a885-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1a885-233">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="1a885-233">Purchase order</span></span></td>
<td><span data-ttu-id="1a885-234">قبل أو بعد ترحيل قائمة عمليات الاستلام أو استلام المنتج للمادة التي تم استلامها</span><span class="sxs-lookup"><span data-stu-id="1a885-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="1a885-235">بعد ترحيل إيصال استلام المنتج للمواد التي تم استلامها، لأن المواد يجب أن تتوفر لإجراء اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="1a885-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="1a885-236">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="1a885-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1a885-237">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر شراء أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-238">أمر إدخال مخزن العزل</span><span class="sxs-lookup"><span data-stu-id="1a885-238">Quarantine order</span></span></td>
<td><span data-ttu-id="1a885-239">قبل أو بعد الإبلاغ عن أمر العزل كمنتهٍ أو مكتمل</span><span class="sxs-lookup"><span data-stu-id="1a885-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="1a885-240">لا يمكن إنشاء أوامر الجودة التي تتطلب إجراء اختبارات تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="1a885-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="1a885-241">ويُفترض أن تتولى وظيفة أمر العزل التخلص من المواد التي تم إتلافها.</span><span class="sxs-lookup"><span data-stu-id="1a885-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="1a885-242">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="1a885-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1a885-243">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر عزل أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-244">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="1a885-244">Sales order</span></span></td>
<td><span data-ttu-id="1a885-245">قبل تحديث عملية الانتقاء المجدولة أو إيصال التعبئة للأصناف التي يتم شحنها</span><span class="sxs-lookup"><span data-stu-id="1a885-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="1a885-246">في أي خطوة</span><span class="sxs-lookup"><span data-stu-id="1a885-246">At any step</span></span></td>
<td><span data-ttu-id="1a885-247">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو عميلاً بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="1a885-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1a885-248">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر مبيعات أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-249">أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1a885-249">Production order</span></span></td>
<td><span data-ttu-id="1a885-250">قبل أو بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1a885-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1a885-251">بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1a885-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1a885-252">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="1a885-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1a885-253">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر إنتاج أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-254">أمر الإنتاج الذي يشتمل على عملية مسار</span><span class="sxs-lookup"><span data-stu-id="1a885-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="1a885-255">قبل أو بعد انتهاء تقرير لعملية</span><span class="sxs-lookup"><span data-stu-id="1a885-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="1a885-256">بعد الإبلاغ عن انتهاء الإنتاج للعملية الأخيرة</span><span class="sxs-lookup"><span data-stu-id="1a885-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="1a885-257">وقد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو مورد عمليات أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="1a885-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1a885-258">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لعملية مسار أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a885-259">المخزون</span><span class="sxs-lookup"><span data-stu-id="1a885-259">Inventory</span></span></td>
<td><span data-ttu-id="1a885-260">لا يمكن إنشاء أمر الجودة تلقائيًا لإحدى الحركات الواردة في دفتر يومية المخزون أو لحركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="1a885-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1a885-261">يجب إنشاء أمر جودة يدويًا لكمية مخزون الصنف.</span><span class="sxs-lookup"><span data-stu-id="1a885-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="1a885-262">المخزون الفعلي المتوفر مطلوب.</span><span class="sxs-lookup"><span data-stu-id="1a885-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="1a885-263">أمثلة الإنشاء التلقائي لأمر الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="1a885-264">الشراء</span><span class="sxs-lookup"><span data-stu-id="1a885-264">Purchasing</span></span>

<span data-ttu-id="1a885-265">في الشراء، إذا قمت بتعيين حقل **نوع الحدث** إلى **إيصال استلام المنتجات** وحقل **التنفيذ** إلى **بعد** في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="1a885-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="1a885-266">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **نعم**، يتم إنشاء أمر الجودة لكل إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة والإعدادات الموجودة في أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1a885-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="1a885-267">في كل مرة يتم فيها استلام كمية مقابل أمر الشراء، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المستلمة حديثًا.</span><span class="sxs-lookup"><span data-stu-id="1a885-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="1a885-268">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **لا**، يتم إنشاء أمر الجودة لأول إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة.</span><span class="sxs-lookup"><span data-stu-id="1a885-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="1a885-269">بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب.</span><span class="sxs-lookup"><span data-stu-id="1a885-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="1a885-270">لا يتم إنشاء أوامر الجودة لعمليات الاستلام اللاحقة مقابل أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="1a885-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="1a885-271">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1a885-271">Production</span></span>

<span data-ttu-id="1a885-272">في الإنتاج، إذا قمت بتعيين حقل **نوع الحدث** إلى **الإبلاغ كمنته** وحقل **التنفيذ** إلى **بعد** في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:</span><span class="sxs-lookup"><span data-stu-id="1a885-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="1a885-273">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **نعم**، يتم إنشاء أمر الجودة بناءً على كل كمية منتهية والإعدادات الموجودة في أخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1a885-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="1a885-274">في كل مرة يتم فيها الإبلاغ عن كمية كمنتهي مقابل أمر الإنتاج، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المنتهية حديثًا.</span><span class="sxs-lookup"><span data-stu-id="1a885-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="1a885-275">يتناسق منطق الإنشاء هذا مع الشراء.</span><span class="sxs-lookup"><span data-stu-id="1a885-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="1a885-276">إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **لا**، يتم إنشاء أمر الجودة في أول مرة يتم الإبلاغ فيها عن منتج كمنتهي، بناءً على الكمية المنتهية.</span><span class="sxs-lookup"><span data-stu-id="1a885-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="1a885-277">بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب لأخذ عينات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1a885-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="1a885-278">لا يتم إنشاء أوامر الجودة للكميات المنتهية اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="1a885-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1a885-279">مواصفات الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-279">Quality specification</span></span></th>
<th><span data-ttu-id="1a885-280">حسب الكمية المحدثة</span><span class="sxs-lookup"><span data-stu-id="1a885-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="1a885-281">حسب بُعد التعقب</span><span class="sxs-lookup"><span data-stu-id="1a885-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="1a885-282">النتيجة</span><span class="sxs-lookup"><span data-stu-id="1a885-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1a885-283">النسبة: 10%</span><span class="sxs-lookup"><span data-stu-id="1a885-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="1a885-284">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="1a885-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="1a885-285">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="1a885-285">Batch number: No</span></span></p>
<p><span data-ttu-id="1a885-286">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="1a885-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="1a885-287">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="1a885-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="1a885-288">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="1a885-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1a885-289">أمر الجودة رقم 1 من 3 (10% من 30%)</span><span class="sxs-lookup"><span data-stu-id="1a885-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1a885-290">الإبلاغ كمنته لنسبة 70</span><span class="sxs-lookup"><span data-stu-id="1a885-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="1a885-291">أمر الجودة رقم 2 لـ 7 (10%من كمية الأمر المتبقية، والتي تساوي 70 في هذه الحالة)</span><span class="sxs-lookup"><span data-stu-id="1a885-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a885-292">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="1a885-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1a885-293">لا</span><span class="sxs-lookup"><span data-stu-id="1a885-293">No</span></span></td>
<td>
<p><span data-ttu-id="1a885-294">رقم الدُفعة: لا</span><span class="sxs-lookup"><span data-stu-id="1a885-294">Batch number: No</span></span></p>
<p><span data-ttu-id="1a885-295">الرقم التسلسلي: لا</span><span class="sxs-lookup"><span data-stu-id="1a885-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="1a885-296">كمية الطلب: 100</span><span class="sxs-lookup"><span data-stu-id="1a885-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="1a885-297">الإبلاغ كمنته لنسبة 30</span><span class="sxs-lookup"><span data-stu-id="1a885-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1a885-298">أمر الجودة رقم 1 لـ 1 (للكمية الأولى التي تم الإبلاغ عنها كمنتهِ، والتي لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="1a885-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="1a885-299">أمر الجودة رقم 2 لـ 1 (للكمية الأولى المتبقية، والتي لا يزال لها قيمة ثابتة 1).</span><span class="sxs-lookup"><span data-stu-id="1a885-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1a885-300">الإبلاغ كمنته لـ 10</span><span class="sxs-lookup"><span data-stu-id="1a885-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="1a885-301">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1a885-302">الإبلاغ كمنته لـ 60</span><span class="sxs-lookup"><span data-stu-id="1a885-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="1a885-303">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a885-304">كمية ثابتة: 1</span><span class="sxs-lookup"><span data-stu-id="1a885-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1a885-305">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="1a885-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="1a885-306">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="1a885-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1a885-307">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="1a885-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1a885-308">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="1a885-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1a885-309">الإبلاغ كمنته لـ 3: 1 للدفعة b1، مسلسل s1؛ 1 للدفعة b2، مسلسل s2؛ و1 للدفعة b3 والمسلسل s3</span><span class="sxs-lookup"><span data-stu-id="1a885-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="1a885-310">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="1a885-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1a885-311">أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</span><span class="sxs-lookup"><span data-stu-id="1a885-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1a885-312">أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</span><span class="sxs-lookup"><span data-stu-id="1a885-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1a885-313">الإبلاغ كمنتهِ لـ 2: 1 للدفعة b4 والمسلسل s4 و1 للدفعة b5 والمسلسل s5</span><span class="sxs-lookup"><span data-stu-id="1a885-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="1a885-314">أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</span><span class="sxs-lookup"><span data-stu-id="1a885-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="1a885-315">أمر الجودة رقم 5 لـ1 من الدفعة رقم b5، مسلسل s5</span><span class="sxs-lookup"><span data-stu-id="1a885-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="1a885-316"><strong>ملاحظة:</strong> يُمكن إعادة استخدام الدفعة.</span><span class="sxs-lookup"><span data-stu-id="1a885-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a885-317">كمية ثابتة: 2</span><span class="sxs-lookup"><span data-stu-id="1a885-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="1a885-318">لا</span><span class="sxs-lookup"><span data-stu-id="1a885-318">No</span></span></td>
<td>
<p><span data-ttu-id="1a885-319">رقم الدفعة: نعم</span><span class="sxs-lookup"><span data-stu-id="1a885-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1a885-320">الرقم التسلسلي: نعم</span><span class="sxs-lookup"><span data-stu-id="1a885-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1a885-321">كمية الطلب: 10</span><span class="sxs-lookup"><span data-stu-id="1a885-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1a885-322">الإبلاغ كمنته لـ 4: 1 للدفعة b1، المسلسل s1؛ 1 للدفعة b2، المسلسل s2؛ 1 للدفعة b3 والمسلسل s3 و1 للدفعة b4 والمسلسل s4</span><span class="sxs-lookup"><span data-stu-id="1a885-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="1a885-323">أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</span><span class="sxs-lookup"><span data-stu-id="1a885-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1a885-324">أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</span><span class="sxs-lookup"><span data-stu-id="1a885-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1a885-325">أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</span><span class="sxs-lookup"><span data-stu-id="1a885-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="1a885-326">أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</span><span class="sxs-lookup"><span data-stu-id="1a885-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="1a885-327">أمر الجودة رقم 5 لـ 2، دون الإشارة إلى دفعة ورقم مسلسل</span><span class="sxs-lookup"><span data-stu-id="1a885-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1a885-328">الإبلاغ كمنتهِ لـ 6: 1 للدفعة b5 ومسلسل s5؛ 1 للدفعة b6 ومسلسل s6؛ 1 للدفعة b7 ومسلسل s7؛ و1 للدفعة b8 ومسلسل 8s؛ و1 للدفعة b9 ومسلسل s9؛ و1 للدفعة b10 ومسلسل s10</span><span class="sxs-lookup"><span data-stu-id="1a885-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="1a885-329">لم يتم إنشاء أوامر جودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1a885-330">تضيف ميزة *إدارة الجودة لعمليات المستودع* إمكانيات معالجة أمر الجودة مع تعيين الإنتاج من **نوع الحدث** إلى *الإبلاغ كمنته* وتعيين **التنفيذ** إلى *بعد*، وتعيين عمليات الشراء من **نوع الحدث** إلى *التسجيل*.</span><span class="sxs-lookup"><span data-stu-id="1a885-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="1a885-331">لمزيد من التفاصيل، راجع [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="1a885-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="1a885-332">صفحات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a885-333">الصفحة</span><span class="sxs-lookup"><span data-stu-id="1a885-333">Page</span></span></th>
<th><span data-ttu-id="1a885-334">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="1a885-334">Description</span></span></th>
<th><span data-ttu-id="1a885-335">مثال</span><span class="sxs-lookup"><span data-stu-id="1a885-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a885-336">عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-336">Quality associations</span></span></td>
<td><span data-ttu-id="1a885-337">راجع الأقسام السابقة في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="1a885-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="1a885-338">يحدد اقتران الجودة كافة المعلومات التالية لأمر جودة يتم إنشاؤه:</span><span class="sxs-lookup"><span data-stu-id="1a885-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="1a885-339">حدث الحركة</span><span class="sxs-lookup"><span data-stu-id="1a885-339">The transaction event</span></span></li>
<li><span data-ttu-id="1a885-340">مجموعة الاختبارات التي يجب إجراؤها على الأصناف</span><span class="sxs-lookup"><span data-stu-id="1a885-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="1a885-341">مستوى الجودة المقبول (AQL)</span><span class="sxs-lookup"><span data-stu-id="1a885-341">The AQL</span></span></li>
<li><span data-ttu-id="1a885-342">خطة أخذ العينات</span><span class="sxs-lookup"><span data-stu-id="1a885-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="1a885-343">يجب عليك تحديد اقتران جودة لكل فرق في العملية التجارية التي تتطلب إنشاء تلقائي لأوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="1a885-344">على سبيل المثال، يمكن إنشاء أمر الجودة في عمليات الأعمال لأوامر الشراء، وأوامر العزل، وأوامر المبيعات، وأوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1a885-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a885-345">الاختبارات</span><span class="sxs-lookup"><span data-stu-id="1a885-345">Tests</span></span></td>
<td><span data-ttu-id="1a885-346">استخدم هذه الصفحة لتحديد الاختبارات الفردية وعرضها والتي تحدد ما إذا كانت منتجاتك تفي بمواصفات الجودة أم لا.</span><span class="sxs-lookup"><span data-stu-id="1a885-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="1a885-347">ويمكنك تعيين واحد أو أكثر من الاختبارات الفردية لمجموعة اختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="1a885-348">وفي هذه الحالة، يمكنك أيضًا تحديد المعلومات الخاصة بالاختبار، مثل قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="1a885-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="1a885-349">يتم استخدام قيم القياس للاختبارات الكمية، ويتم استخدام متغيرات الاختبار لاختبارات الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="1a885-350">يشتمل الاختبار الكمي على نوع اختبار <strong>عدد صحيح</strong> أو <strong>كسر</strong>، ويشتمل أيضًا على وحدة قياس معيَّنة.</span><span class="sxs-lookup"><span data-stu-id="1a885-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="1a885-351">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات كأرقام.</span><span class="sxs-lookup"><span data-stu-id="1a885-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="1a885-352">يشتمل الاختبار النوعي على نوع اختبار <strong>الخيار</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a885-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="1a885-353">وتتطلب الاختبارات النوعية معلومات إضافية حول متغير الاختبار الذي يتم قياسه وخياراته العديدة.</span><span class="sxs-lookup"><span data-stu-id="1a885-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="1a885-354">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات حسب النتيجة.</span><span class="sxs-lookup"><span data-stu-id="1a885-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="1a885-355">تقوم إحدى شركات التصنيع بإجراء اختبارين على المادة التي تم شراؤها وهما اختبار كمي حول جودة المادة واختبار نوعي حول حدوث تلف في التعبئة.</span><span class="sxs-lookup"><span data-stu-id="1a885-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="1a885-356">وتحدد الشركة معلومات إضافية حول الاختبار النوعي لتحديد متغير الاختبار (التعبئة التالفة) ونتائجه.</span><span class="sxs-lookup"><span data-stu-id="1a885-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="1a885-357">تستخدم الشركة صفحة <strong>مجموعات الاختبار</strong> لتعيين الاختبارين لمجموعة اختبارات وتحديد المعلومات الخاصة بالاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="1a885-358">يتم تعيين مجموعة الاختبار إلى أمر الجودة بحيث يمكن للشركة تقديم تقرير بنتائج الاختبار لكلا الاختبارين.</span><span class="sxs-lookup"><span data-stu-id="1a885-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a885-359">مجموعات الاختبار</span><span class="sxs-lookup"><span data-stu-id="1a885-359">Test groups</span></span></td>
<td><span data-ttu-id="1a885-360">استخدم هذه الصفحة لإعداد مجموعات الاختبار والاختبارات الفردية، والتي يتم تعيينها إلى مجموعة اختبار، وتحريرها وعرضها.</span><span class="sxs-lookup"><span data-stu-id="1a885-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="1a885-361">يعرض الجزء العلوي مجموعات الاختبار، ويعرض الجزء السفلي الاختبارات التي يتم تعيينها إلى مجموعة اختبار محددة.</span><span class="sxs-lookup"><span data-stu-id="1a885-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="1a885-362">تقوم بتعيين نُهج متعددة إلى مجموعة اختبار، بما في ذلك خطة أخذ عينات و"مستوى الجودة المقبول "(AQL) ومتطلب لاختبار تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="1a885-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="1a885-363">وعند تعيين اختبار فردي إلى مجموعة اختبار، يمكنك تحديد معلومات إضافية، مثل التسلسل والوثائق وتواريخ الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="1a885-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="1a885-364">وفي الاختبار الكمي، تتضمن المعلومات التي تحددها قيم القياس المقبولة أيضًا.</span><span class="sxs-lookup"><span data-stu-id="1a885-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="1a885-365">أما في الاختبار النوعي، تتضمن المعلومات متغير الاختبار والنتيجة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="1a885-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="1a885-366">وتحدد مجموعة الاختبار التي تم تعيينها لأمر جودة مجموعة الاختبارات الافتراضية التي يجب إجراؤها على الصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1a885-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="1a885-367">ومع ذلك، يمكن إضافة أو حذف أو تغيير الاختبارات في أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="1a885-368">يتم الإعلام عن نتائج كل اختبار في أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="1a885-369">تقوم شركة تصنيع بتعريف مجموعة اختبار لكل تباين في إرشادات الجودة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="1a885-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="1a885-370">تعكس مجموعات الاختبار المتنوعة فروقًا في خطط أخذ العينات ومجموعات الاختبارات التي تحتاج لإجرائها معًا ومستوى الجودة المقبول (AQL) والعوامل الأخرى.</span><span class="sxs-lookup"><span data-stu-id="1a885-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="1a885-371">وفي الاختبارات الكمية، هناك أيضًا اختلافات في قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="1a885-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="1a885-372">ولفرض إرشادات الجودة الخاصة بها، تقوم الشركة بتعيين مجموعة اختبار لكل قاعدة لإنشاء أوامر الجودة تلقائياً في صفحة <strong>عمليات اقتران الجودة</strong>، وتقوم أيضًا بتعيين مجموعة اختبار لأوامر الجودة التي يتم إنشاؤها يدوياً.</span><span class="sxs-lookup"><span data-stu-id="1a885-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a885-373">مجموعات جودة الصنف</span><span class="sxs-lookup"><span data-stu-id="1a885-373">Item quality groups</span></span></td>
<td><span data-ttu-id="1a885-374">استخدم هذه الصفحة لإعداد وتحرير وعرض الأصناف المخصصة لمجموعة الجودة أو مجموعات الجودة المخصصة للصنف.</span><span class="sxs-lookup"><span data-stu-id="1a885-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="1a885-375">تمثل مجموعة الجودة متطلبات الاختبار الشائعة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="1a885-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="1a885-376">وبعد تحديد متطلبات الاختبار في صفحة <strong>مجموعات الاختبار</strong>، يمكنك تحديد القواعد لإنشاء أوامر الجودة تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="1a885-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="1a885-377">ولتبسيط العملية، لا يلزمك تحديد قواعد للأصناف الفردية.</span><span class="sxs-lookup"><span data-stu-id="1a885-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="1a885-378">وبدلاً من ذلك، يمكنك تحديد قواعد لمجموعة جودة، من خلال استخدام صفحة <strong>عمليات اقتران الجودة</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a885-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="1a885-379">ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لمجموعة جودة محددة لتعيين الأصناف ذات الصلة لهذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="1a885-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="1a885-380">ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لصنف محدد لتعيين مجموعات الجودة ذات الصلة لهذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="1a885-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="1a885-381">تقوم الشركة المصنعة بشراء العديد من المواد الخام المتعددة التي لها نفس متطلبات الاختبار الخاصة بالفحص الوارد.</span><span class="sxs-lookup"><span data-stu-id="1a885-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="1a885-382">وتحدد الشركة مجموعة الجودة، ثم تقوم بتعيين أرقام الأصناف المرتبطة بالمواد الخام إلى تلك المجموعة.</span><span class="sxs-lookup"><span data-stu-id="1a885-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="1a885-383">ولاحقاً، تشتري الشركة نوعًا جديدًا من المواد الخام له نفس متطلبات الاختبارات.</span><span class="sxs-lookup"><span data-stu-id="1a885-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="1a885-384">وبدلاً من إعداد متطلبات الاختبار الجديدة للمواد الجديدة، تضيف الشركة رقم الصنف للمواد الجديدة إلى مجموعة الجودة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="1a885-385">كما تنتج نفس شركة التصنيع الأصناف التي تشتمل على نفس متطلبات اختبارات الإنتاج وتقوم بشحن الأصناف التي تشتمل على نفس متطلبات اختبارات ما قبل الشحن.</span><span class="sxs-lookup"><span data-stu-id="1a885-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="1a885-386">وتحدد الشركة مجموعتي جودة إضافيتين، ثم تقوم بتعيين أرقام الأصناف ذات الصلة لكل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="1a885-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a885-387">متغيرات الاختبار</span><span class="sxs-lookup"><span data-stu-id="1a885-387">Test variables</span></span></td>
<td><span data-ttu-id="1a885-388">استخدم هذه الصفحة لتحديد وعرض المتغيرات المرتبطة باختبار جودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="1a885-389">وبالنسبة لكل متغير، تقوم بتحديد النتائج العديدة التي تمثل الخيارات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="1a885-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="1a885-390">ويمكنك تحديد الاختبارات في صفحة <strong>الاختبارات</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a885-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1a885-391">وبالنسبة لاختبارات الجودة، يجب عليك تعيين نوع الاختبار إلى <strong>الخيار</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a885-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="1a885-392">واستخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار لكل اختبار فردي.</span><span class="sxs-lookup"><span data-stu-id="1a885-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="1a885-393">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="1a885-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1a885-394">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="1a885-394">This inspection test has several variables.</span></span> <span data-ttu-id="1a885-395">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="1a885-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1a885-396">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="1a885-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a885-397">نتائج متغير الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1a885-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="1a885-398">استخدم هذه الصفحة لإعداد نتائج الاختبار الممكنة وتحريرها وعرضها لأحد متغيرات الاختبار المرتبطة باختبار الجودة.</span><span class="sxs-lookup"><span data-stu-id="1a885-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="1a885-399">وللحصول على كل نتيجة، تقوم بتعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a885-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="1a885-400">يجب تعريف المتغير ونتائجه الخاصة بكل اختبار جودة الذي يتم تحديده في صفحة <strong>الاختبارات</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a885-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1a885-401">(بالنسبة لاختبارات الجودة، يتم تعيين نوع الاختبار إلى <strong>الخيار</strong> في صفحة <strong>الاختبارات‬‏‫</strong>.) ‏‫استخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار والنتيجة الافتراضية لاختبار جودة فردي.‬</span><span class="sxs-lookup"><span data-stu-id="1a885-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="1a885-402">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="1a885-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1a885-403">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="1a885-403">This inspection test has of several variables.</span></span> <span data-ttu-id="1a885-404">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="1a885-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1a885-405">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="1a885-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="1a885-406">ويتم تعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong> لكل نتيجة.</span><span class="sxs-lookup"><span data-stu-id="1a885-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="1a885-407">أثناء اختبار الفحص الخاص بكل متغير، يقوم المفتش بالإعلام عن نتيجة الاختبار عن طريق تحديد إحدى النتائج.</span><span class="sxs-lookup"><span data-stu-id="1a885-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="1a885-408">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1a885-408">Additional resources</span></span>
--------

[<span data-ttu-id="1a885-409">عمليات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1a885-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="1a885-410">إدارة عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="1a885-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="1a885-411">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="1a885-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
