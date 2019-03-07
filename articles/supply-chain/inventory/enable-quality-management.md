---
title: نظرة عامة على إدارة الجودة
description: يصف هذا الموضوع كيفية استخدام إدارة الجودة في Microsoft Dynamics 365 for Finance and Operations للمساعدة في تحسين جودة المنتج في سلسلة التوريد.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "338304"
---
# <a name="quality-management-overview"></a><span data-ttu-id="a1526-103">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="a1526-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1526-104">يصف هذا الموضوع كيفية استخدام إدارة الجودة في Microsoft Dynamics 365 for Finance and Operations للمساعدة في تحسين جودة المنتج في سلسلة التوريد.</span><span class="sxs-lookup"><span data-stu-id="a1526-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="a1526-105">ويمكن أن تساعدك إدارة الجودة في إدارة تنظيم أوقات الإنتاج عندما تتعامل مع المنتجات غير المتوافقة، بغض النظر عن نقطة الأصل.</span><span class="sxs-lookup"><span data-stu-id="a1526-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="a1526-106">ولأن أنواع التشخيص مرتبطة بالإبلاغ عن التصحيحات، بإمكان Microsoft Dynamics 365 for Finance and Operations جدولة المهام لحل المشاكل ومنع تكرارها.</span><span class="sxs-lookup"><span data-stu-id="a1526-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="a1526-107">وبالإضافة إلى وظيفة إدارة عدم التوافق، تتضمن إدارة الجودة وظيفة تعقب المشكلات حسب نوع المشكلة (حتى المشكلات الداخلية، ولتحديد الحلول قصيرة الأجل أو طويلة الأجل.</span><span class="sxs-lookup"><span data-stu-id="a1526-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="a1526-108">وتوفر إحصاءات مؤشرات الأداء الرئيسية (KPIs) رؤية في مشاكل عدم التوافق التي حدثت مسبقاً والحلول التي تم تطبيقها لتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="a1526-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="a1526-109">ويمكنك استخدام البيانات التاريخية للمساعدة على مراجعة فعالية تدابير الجودة التي تم اتخاذها سابقًا لتحديد التدابير المناسبة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="a1526-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="a1526-110">عند إعداد اقتران جودة، يمكن لتطبيق Finance and Operations إنشاء أوامر الجودة لمختلف الأعمال والأحداث والشروط.</span><span class="sxs-lookup"><span data-stu-id="a1526-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="a1526-111">ويمكن لاقتران الجودة تغطية صنف محدد أو مجموعة محددة من الأصناف أو كافة الأصناف.</span><span class="sxs-lookup"><span data-stu-id="a1526-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="a1526-112">أمثلة على استخدام إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="a1526-112">Examples of the use of quality management</span></span>
<span data-ttu-id="a1526-113">تتسم إدارة الجودة بالمرونة ويمكن تنفيذها بطرق مختلفة للوفاء بمتطلبات مستويات محددة من عمليات سلاسل التوريد.</span><span class="sxs-lookup"><span data-stu-id="a1526-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="a1526-114">توضح الأمثلة التالية الاستخدامات المحتملة لهذه الميزات:</span><span class="sxs-lookup"><span data-stu-id="a1526-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="a1526-115">بدء عملية مراقبة الجودة، استناداً إلى معايير محددة مسبقاً (عند تسجيل المستودع لأمر شراء من مورد معين) تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="a1526-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="a1526-116">حظر المخزون أثناء الفحص لمنع استخدام المخزون غير المعتمد (الحظر الكامل لكميات أمر الشراء).</span><span class="sxs-lookup"><span data-stu-id="a1526-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="a1526-117">استخدام عينات الصنف كجزء من اقتران الجودة لتحديد كمية المخزون الفعلي الحالي الذي يجب فحصه.</span><span class="sxs-lookup"><span data-stu-id="a1526-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="a1526-118">يمكن لأخذ العينات الاستناد إلى نسبة مئوية أو كميات ثابتة.</span><span class="sxs-lookup"><span data-stu-id="a1526-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="a1526-119">إنشاء أوامر الجودة لإيصالات الاستلام الجزئية.</span><span class="sxs-lookup"><span data-stu-id="a1526-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="a1526-120">لإنشاء أمر جودة يستند إلى الكمية التي تم استلامها فعليًا مع أمر ما، يجب عليك تحديد خانة الاختيار **حسب الكمية المحدثة** في النموذج **أخذ عينات للصنف**.</span><span class="sxs-lookup"><span data-stu-id="a1526-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="a1526-121">إنشاء أنواع الاختبار التي تتضمن الحد الأدنى، والحد الأقصى، وقيم الاختبار المستهدفة، وإجراء اختبار النوعية مقابل الكمية الذي له نتائج تحقق محددة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="a1526-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="a1526-122">تحديد مستوى جودة مقبول (AQL) للتحكم في تفاوتات قياس الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="a1526-123">تحديد الموارد التي تتطلب عملية فحص، مثل منطقة اختبار وأدوات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="a1526-124">العمل مع عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="a1526-124">Working with quality associations</span></span>
<span data-ttu-id="a1526-125">يمكن ربط عملية الأعمال التي تستخدم اقتران جودة بمستندات مصدر مختلفة، مثل أوامر الشراء أو أوامر المبيعات أو أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a1526-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="a1526-126">كما يقوم كل سجل من سجلات عمليات اقتران الجودة بتعريف مجموعة الاختبارات ومستوى الجودة المقبول (AQL) وعينة خطة تنطبق على أوامر الجودة التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="a1526-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="a1526-127">ويجب تحديد سجل اقتران جودة لكل فرق في عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="a1526-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="a1526-128">على سبيل المثال، يمكنك إعداد اقتران جودة يقوم بإنشاء أمر جودة عند تحديث إيصال استلام منتج أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="a1526-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="a1526-129">واستنادًا إلى إعداد خطة التنفيذ، يمكن حظر عملية التشغيل نفسها، بينما هناك أمر جودة مفتوح، أو يمكن خظر العمليات التالية، مثل فوترة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a1526-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="a1526-130">**ملاحظة:** أثناء وجود أوامر الجودة المفتوحة، يتم حظر إصدار كميات المخزون تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="a1526-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="a1526-131">واستناداً إلى إعداد **الحظر الكامل** في صفحة **عينات الصنف**، تكون الكمية هي أما الكمية الموجودة في أمر الجودة أو الكمية الموجودة في بند المستند المصدر.</span><span class="sxs-lookup"><span data-stu-id="a1526-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="a1526-132">وفي عملية أعمال محددة، يحدد سجل اقتران الجودة الحدث والظروف التي يتم إنشاء أمر جودة لها.</span><span class="sxs-lookup"><span data-stu-id="a1526-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="a1526-133">ويمكن أن تكون الظروف خاصة بموقع أو كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="a1526-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="a1526-134">ويمكن إنشاء أمر الجودة الذي يتضمن اختبارات تحديد القدرة فقط عند توفر مخزون للحدث.</span><span class="sxs-lookup"><span data-stu-id="a1526-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="a1526-135">توضح الأمثلة التالية كيفية تعريف سجل اقتران الجودة بالنسبة للتباينات في كل عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="a1526-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="a1526-136">وتم أيضًا تلخيص الأمثلة في الرسم التخطيطي التالي من حيث الأحداث والشروط التي تم تعريفها عن طريق سجل اقتران الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="a1526-137">نوع المرجع</span><span class="sxs-lookup"><span data-stu-id="a1526-137">Reference type</span></span></th>
<th><span data-ttu-id="a1526-138">نوع الحدث</span><span class="sxs-lookup"><span data-stu-id="a1526-138">Event type</span></span></th>
<th><span data-ttu-id="a1526-139">التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a1526-139">Execution</span></span></th>
<th><span data-ttu-id="a1526-140">حظر الحدث</span><span class="sxs-lookup"><span data-stu-id="a1526-140">Event blocking</span></span></th>
<th><span data-ttu-id="a1526-141">مرجع المستند</span><span class="sxs-lookup"><span data-stu-id="a1526-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a1526-142">المخزون</span><span class="sxs-lookup"><span data-stu-id="a1526-142">Inventory</span></span></td>
<td><span data-ttu-id="a1526-143">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="a1526-143">Not applicable</span></span></td>
<td><span data-ttu-id="a1526-144">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="a1526-144">Not applicable</span></span></td>
<td><span data-ttu-id="a1526-145">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-145">None</span></span></td>
<td><span data-ttu-id="a1526-146">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="a1526-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="a1526-147">المبيعات</span><span class="sxs-lookup"><span data-stu-id="a1526-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="a1526-148">تمت جدولة عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="a1526-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="a1526-149">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-149">Before</span></span></td>
<td><span data-ttu-id="a1526-150">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="a1526-151">معرف محدد أو المجموعة أو الكل فقط</span><span class="sxs-lookup"><span data-stu-id="a1526-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-152">عملية الانتقاء</span><span class="sxs-lookup"><span data-stu-id="a1526-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-153">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1526-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-154">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1526-155">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1526-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-156">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-156">Before</span></span></td>
<td><span data-ttu-id="a1526-157">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-158">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="a1526-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-159">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="a1526-160">شراء</span><span class="sxs-lookup"><span data-stu-id="a1526-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="a1526-161">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="a1526-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="a1526-162">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-162">Before</span></span></td>
<td><span data-ttu-id="a1526-163">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-164">قائمة إيصالات الاستلام</span><span class="sxs-lookup"><span data-stu-id="a1526-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-165">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="a1526-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-166">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1526-167">بعد</span><span class="sxs-lookup"><span data-stu-id="a1526-167">After</span></span></td>
<td><span data-ttu-id="a1526-168">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-169">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="a1526-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-170">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1526-171">تسجيل</span><span class="sxs-lookup"><span data-stu-id="a1526-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-172">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="a1526-172">Not applicable</span></span></td>
<td><span data-ttu-id="a1526-173">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-174">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="a1526-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-175">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a1526-176">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="a1526-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-177">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-177">Before</span></span></td>
<td><span data-ttu-id="a1526-178">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-179">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="a1526-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-180">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1526-181">بعد</span><span class="sxs-lookup"><span data-stu-id="a1526-181">After</span></span></td>
<td><span data-ttu-id="a1526-182">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-183">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="a1526-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="a1526-184">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a1526-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-185">تسجيل</span><span class="sxs-lookup"><span data-stu-id="a1526-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-186">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="a1526-186">Not applicable</span></span></td>
<td><span data-ttu-id="a1526-187">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="a1526-188">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="a1526-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-189">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-190">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a1526-191">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-192">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-192">Before</span></span></td>
<td><span data-ttu-id="a1526-193">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-194">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-195">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1526-196">بعد</span><span class="sxs-lookup"><span data-stu-id="a1526-196">After</span></span></td>
<td><span data-ttu-id="a1526-197">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-198">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a1526-199">العزل</span><span class="sxs-lookup"><span data-stu-id="a1526-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-200">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="a1526-201">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-201">Before</span></span></td>
<td><span data-ttu-id="a1526-202">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-203">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-204">بعد</span><span class="sxs-lookup"><span data-stu-id="a1526-204">After</span></span></td>
<td><span data-ttu-id="a1526-205">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-206">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-206">End</span></span></td>
<td><span data-ttu-id="a1526-207">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-207">Before</span></span></td>
<td><span data-ttu-id="a1526-208">نهاية</span><span class="sxs-lookup"><span data-stu-id="a1526-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1526-209">مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="a1526-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-210">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="a1526-211">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-211">Before</span></span></td>
<td><span data-ttu-id="a1526-212">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-213">المعرف الخاص، والمجموعة، أو الكل، والمورد المحدد، أو المجموعة، أو الكل</span><span class="sxs-lookup"><span data-stu-id="a1526-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-214">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-215">بعد</span><span class="sxs-lookup"><span data-stu-id="a1526-215">After</span></span></td>
<td><span data-ttu-id="a1526-216">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1526-217">إنتاج المنتج المساعد</span><span class="sxs-lookup"><span data-stu-id="a1526-217">Co-product production</span></span></td>
<td><span data-ttu-id="a1526-218">تسجيل</span><span class="sxs-lookup"><span data-stu-id="a1526-218">Registration</span></span></td>
<td><span data-ttu-id="a1526-219">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="a1526-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-220">بلا</span><span class="sxs-lookup"><span data-stu-id="a1526-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="a1526-221">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="a1526-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1526-222">الإبلاغ كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="a1526-222">Report as finished</span></span></td>
<td><span data-ttu-id="a1526-223">قبل</span><span class="sxs-lookup"><span data-stu-id="a1526-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-224">بعد</span><span class="sxs-lookup"><span data-stu-id="a1526-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1526-225">يوفر الجدول التالي مزيدًا من المعلومات حول كيفية إنشاء أوامر الجودة لأنواع معينة من العمليات.</span><span class="sxs-lookup"><span data-stu-id="a1526-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="a1526-226">نوع العملية</span><span class="sxs-lookup"><span data-stu-id="a1526-226">Type of process</span></span></th>
<th><span data-ttu-id="a1526-227">عند إمكانية إنشاء أوامر الجودة تلقائياً</span><span class="sxs-lookup"><span data-stu-id="a1526-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="a1526-228">وقت إمكانية إنشاء أوامر الجودة في حالة تطلب اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="a1526-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="a1526-229">معلومات الظروف</span><span class="sxs-lookup"><span data-stu-id="a1526-229">Condition information</span></span></th>
<th><span data-ttu-id="a1526-230">معلومات الإنشاء اليدوي</span><span class="sxs-lookup"><span data-stu-id="a1526-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a1526-231">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="a1526-231">Purchase order</span></span></td>
<td><span data-ttu-id="a1526-232">قبل أو بعد ترحيل قائمة عمليات الاستلام أو استلام المنتج للمادة التي تم استلامها</span><span class="sxs-lookup"><span data-stu-id="a1526-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="a1526-233">بعد ترحيل إيصال استلام المنتج للمواد التي تم استلامها، لأن المواد يجب أن تتوفر لإجراء اختبار تحديد القدرات</span><span class="sxs-lookup"><span data-stu-id="a1526-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="a1526-234">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="a1526-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a1526-235">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر شراء أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-236">أمر إدخال مخزن العزل</span><span class="sxs-lookup"><span data-stu-id="a1526-236">Quarantine order</span></span></td>
<td><span data-ttu-id="a1526-237">قبل أو بعد الإبلاغ عن أمر العزل كمنتهٍ أو مكتمل</span><span class="sxs-lookup"><span data-stu-id="a1526-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="a1526-238">لا يمكن إنشاء أوامر الجودة التي تتطلب إجراء اختبارات تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="a1526-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="a1526-239">ويُفترض أن تتولى وظيفة أمر العزل التخلص من المواد التي تم إتلافها.</span><span class="sxs-lookup"><span data-stu-id="a1526-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="a1526-240">وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="a1526-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a1526-241">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر عزل أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-242">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="a1526-242">Sales order</span></span></td>
<td><span data-ttu-id="a1526-243">قبل تحديث عملية الانتقاء المجدولة أو إيصال التعبئة للأصناف التي يتم شحنها</span><span class="sxs-lookup"><span data-stu-id="a1526-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="a1526-244">في أي خطوة</span><span class="sxs-lookup"><span data-stu-id="a1526-244">At any step</span></span></td>
<td><span data-ttu-id="a1526-245">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو عميلاً بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="a1526-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a1526-246">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر مبيعات أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-247">أمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a1526-247">Production order</span></span></td>
<td><span data-ttu-id="a1526-248">قبل أو بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a1526-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="a1526-249">بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="a1526-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="a1526-250">قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا بعينه أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="a1526-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a1526-251">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر إنتاج أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-252">أمر الإنتاج الذي يشتمل على عملية مسار</span><span class="sxs-lookup"><span data-stu-id="a1526-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="a1526-253">قبل أو بعد انتهاء تقرير لعملية</span><span class="sxs-lookup"><span data-stu-id="a1526-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="a1526-254">بعد الإبلاغ عن انتهاء الإنتاج للعملية الأخيرة</span><span class="sxs-lookup"><span data-stu-id="a1526-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="a1526-255">وقد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو مورد عمليات أو مجموعة من هذه الشروط.</span><span class="sxs-lookup"><span data-stu-id="a1526-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="a1526-256">ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لعملية مسار أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1526-257">المخزون</span><span class="sxs-lookup"><span data-stu-id="a1526-257">Inventory</span></span></td>
<td><span data-ttu-id="a1526-258">لا يمكن إنشاء أمر الجودة تلقائيًا لإحدى الحركات الواردة في دفتر يومية المخزون أو لحركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="a1526-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a1526-259">يجب إنشاء أمر جودة يدويًا لكمية مخزون الصنف.</span><span class="sxs-lookup"><span data-stu-id="a1526-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="a1526-260">المخزون الفعلي المتوفر مطلوب.</span><span class="sxs-lookup"><span data-stu-id="a1526-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="a1526-261">صفحات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="a1526-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1526-262">الصفحة</span><span class="sxs-lookup"><span data-stu-id="a1526-262">Page</span></span></th>
<th><span data-ttu-id="a1526-263">الوصف</span><span class="sxs-lookup"><span data-stu-id="a1526-263">Description</span></span></th>
<th><span data-ttu-id="a1526-264">مثال</span><span class="sxs-lookup"><span data-stu-id="a1526-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1526-265">عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="a1526-265">Quality associations</span></span></td>
<td><span data-ttu-id="a1526-266">راجع الأقسام السابقة في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="a1526-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="a1526-267">يحدد اقتران الجودة كافة المعلومات التالية لأمر جودة يتم إنشاؤه:</span><span class="sxs-lookup"><span data-stu-id="a1526-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="a1526-268">حدث الحركة</span><span class="sxs-lookup"><span data-stu-id="a1526-268">The transaction event</span></span></li>
<li><span data-ttu-id="a1526-269">مجموعة الاختبارات التي يجب إجراؤها على الأصناف</span><span class="sxs-lookup"><span data-stu-id="a1526-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="a1526-270">مستوى الجودة المقبول (AQL)</span><span class="sxs-lookup"><span data-stu-id="a1526-270">The AQL</span></span></li>
<li><span data-ttu-id="a1526-271">خطة أخذ العينات</span><span class="sxs-lookup"><span data-stu-id="a1526-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="a1526-272">يجب عليك تحديد اقتران جودة لكل فرق في العملية التجارية التي تتطلب إنشاء تلقائي لأوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="a1526-273">على سبيل المثال، يمكن إنشاء أمر الجودة في عمليات الأعمال لأوامر الشراء، وأوامر العزل، وأوامر المبيعات، وأوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a1526-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1526-274">الاختبارات</span><span class="sxs-lookup"><span data-stu-id="a1526-274">Tests</span></span></td>
<td><span data-ttu-id="a1526-275">استخدم هذه الصفحة لتحديد الاختبارات الفردية وعرضها والتي تحدد ما إذا كانت منتجاتك تفي بمواصفات الجودة أم لا.</span><span class="sxs-lookup"><span data-stu-id="a1526-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="a1526-276">ويمكنك تعيين واحد أو أكثر من الاختبارات الفردية لمجموعة اختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="a1526-277">وفي هذه الحالة، يمكنك أيضًا تحديد المعلومات الخاصة بالاختبار، مثل قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="a1526-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="a1526-278">يتم استخدام قيم القياس للاختبارات الكمية، ويتم استخدام متغيرات الاختبار لاختبارات الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="a1526-279">يشتمل الاختبار الكمي على نوع اختبار <strong>عدد صحيح</strong> أو <strong>كسر</strong>، ويشتمل أيضًا على وحدة قياس معيَّنة.</span><span class="sxs-lookup"><span data-stu-id="a1526-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="a1526-280">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات كأرقام.</span><span class="sxs-lookup"><span data-stu-id="a1526-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="a1526-281">يشتمل الاختبار النوعي على نوع اختبار <strong>الخيار</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1526-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="a1526-282">وتتطلب الاختبارات النوعية معلومات إضافية حول متغير الاختبار الذي يتم قياسه وخياراته العديدة.</span><span class="sxs-lookup"><span data-stu-id="a1526-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="a1526-283">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات حسب النتيجة.</span><span class="sxs-lookup"><span data-stu-id="a1526-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="a1526-284">تقوم إحدى شركات التصنيع بإجراء اختبارين على المادة التي تم شراؤها وهما اختبار كمي حول جودة المادة واختبار نوعي حول حدوث تلف في التعبئة.</span><span class="sxs-lookup"><span data-stu-id="a1526-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="a1526-285">وتحدد الشركة معلومات إضافية حول الاختبار النوعي لتحديد متغير الاختبار (التعبئة التالفة) ونتائجه.</span><span class="sxs-lookup"><span data-stu-id="a1526-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="a1526-286">تستخدم الشركة صفحة <strong>مجموعات الاختبار</strong> لتعيين الاختبارين لمجموعة اختبارات وتحديد المعلومات الخاصة بالاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="a1526-287">يتم تعيين مجموعة الاختبار إلى أمر الجودة بحيث يمكن للشركة تقديم تقرير بنتائج الاختبار لكلا الاختبارين.</span><span class="sxs-lookup"><span data-stu-id="a1526-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1526-288">مجموعات الاختبار</span><span class="sxs-lookup"><span data-stu-id="a1526-288">Test groups</span></span></td>
<td><span data-ttu-id="a1526-289">استخدم هذه الصفحة لإعداد مجموعات الاختبار والاختبارات الفردية، والتي يتم تعيينها إلى مجموعة اختبار، وتحريرها وعرضها.</span><span class="sxs-lookup"><span data-stu-id="a1526-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="a1526-290">يعرض الجزء العلوي مجموعات الاختبار، ويعرض الجزء السفلي الاختبارات التي يتم تعيينها إلى مجموعة اختبار محددة.</span><span class="sxs-lookup"><span data-stu-id="a1526-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="a1526-291">تقوم بتعيين نُهج متعددة إلى مجموعة اختبار، بما في ذلك خطة أخذ عينات و"مستوى الجودة المقبول "(AQL) ومتطلب لاختبار تحديد القدرة.</span><span class="sxs-lookup"><span data-stu-id="a1526-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="a1526-292">وعند تعيين اختبار فردي إلى مجموعة اختبار، يمكنك تحديد معلومات إضافية، مثل التسلسل والوثائق وتواريخ الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="a1526-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="a1526-293">وفي الاختبار الكمي، تتضمن المعلومات التي تحددها قيم القياس المقبولة أيضًا.</span><span class="sxs-lookup"><span data-stu-id="a1526-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="a1526-294">أما في الاختبار النوعي، تتضمن المعلومات متغير الاختبار والنتيجة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a1526-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="a1526-295">وتحدد مجموعة الاختبار التي تم تعيينها لأمر جودة مجموعة الاختبارات الافتراضية التي يجب إجراؤها على الصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a1526-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="a1526-296">ومع ذلك، يمكن إضافة أو حذف أو تغيير الاختبارات في أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="a1526-297">يتم الإعلام عن نتائج كل اختبار في أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="a1526-298">تقوم شركة تصنيع بتعريف مجموعة اختبار لكل تباين في إرشادات الجودة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="a1526-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="a1526-299">تعكس مجموعات الاختبار المتنوعة فروقًا في خطط أخذ العينات ومجموعات الاختبارات التي تحتاج لإجرائها معًا ومستوى الجودة المقبول (AQL) والعوامل الأخرى.</span><span class="sxs-lookup"><span data-stu-id="a1526-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="a1526-300">وفي الاختبارات الكمية، هناك أيضًا اختلافات في قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="a1526-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="a1526-301">ولفرض إرشادات الجودة الخاصة بها، تقوم الشركة بتعيين مجموعة اختبار لكل قاعدة لإنشاء أوامر الجودة تلقائياً في صفحة <strong>عمليات اقتران الجودة</strong>، وتقوم أيضًا بتعيين مجموعة اختبار لأوامر الجودة التي يتم إنشاؤها يدوياً.</span><span class="sxs-lookup"><span data-stu-id="a1526-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1526-302">مجموعات جودة الصنف</span><span class="sxs-lookup"><span data-stu-id="a1526-302">Item quality groups</span></span></td>
<td><span data-ttu-id="a1526-303">استخدم هذه الصفحة لإعداد وتحرير وعرض الأصناف المخصصة لمجموعة الجودة أو مجموعات الجودة المخصصة للصنف.</span><span class="sxs-lookup"><span data-stu-id="a1526-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="a1526-304">تمثل مجموعة الجودة متطلبات الاختبار الشائعة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="a1526-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="a1526-305">وبعد تحديد متطلبات الاختبار في صفحة <strong>مجموعات الاختبار</strong>، يمكنك تحديد القواعد لإنشاء أوامر الجودة تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="a1526-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="a1526-306">ولتبسيط العملية، لا يلزمك تحديد قواعد للأصناف الفردية.</span><span class="sxs-lookup"><span data-stu-id="a1526-306">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="a1526-307">وبدلاً من ذلك، يمكنك تحديد قواعد لمجموعة جودة، من خلال استخدام صفحة <strong>عمليات اقتران الجودة</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1526-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="a1526-308">ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لمجموعة جودة محددة لتعيين الأصناف ذات الصلة لهذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a1526-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="a1526-309">ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لصنف محدد لتعيين مجموعات الجودة ذات الصلة لهذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="a1526-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="a1526-310">تقوم الشركة المصنعة بشراء العديد من المواد الخام المتعددة التي لها نفس متطلبات الاختبار الخاصة بالفحص الوارد.</span><span class="sxs-lookup"><span data-stu-id="a1526-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="a1526-311">وتحدد الشركة مجموعة الجودة، ثم تقوم بتعيين أرقام الأصناف المرتبطة بالمواد الخام إلى تلك المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a1526-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="a1526-312">ولاحقاً، تشتري الشركة نوعًا جديدًا من المواد الخام له نفس متطلبات الاختبارات.</span><span class="sxs-lookup"><span data-stu-id="a1526-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="a1526-313">وبدلاً من إعداد متطلبات الاختبار الجديدة للمواد الجديدة، تضيف الشركة رقم الصنف للمواد الجديدة إلى مجموعة الجودة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="a1526-314">كما تنتج نفس شركة التصنيع الأصناف التي تشتمل على نفس متطلبات اختبارات الإنتاج وتقوم بشحن الأصناف التي تشتمل على نفس متطلبات اختبارات ما قبل الشحن.</span><span class="sxs-lookup"><span data-stu-id="a1526-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="a1526-315">وتحدد الشركة مجموعتي جودة إضافيتين، ثم تقوم بتعيين أرقام الأصناف ذات الصلة لكل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="a1526-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1526-316">متغيرات الاختبار</span><span class="sxs-lookup"><span data-stu-id="a1526-316">Test variables</span></span></td>
<td><span data-ttu-id="a1526-317">استخدم هذه الصفحة لتحديد وعرض المتغيرات المرتبطة باختبار جودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="a1526-318">وبالنسبة لكل متغير، تقوم بتحديد النتائج العديدة التي تمثل الخيارات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="a1526-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="a1526-319">ويمكنك تحديد الاختبارات في صفحة <strong>الاختبارات</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1526-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="a1526-320">وبالنسبة لاختبارات الجودة، يجب عليك تعيين نوع الاختبار إلى <strong>الخيار</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1526-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="a1526-321">واستخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار لكل اختبار فردي.</span><span class="sxs-lookup"><span data-stu-id="a1526-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="a1526-322">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="a1526-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="a1526-323">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="a1526-323">This inspection test has several variables.</span></span> <span data-ttu-id="a1526-324">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="a1526-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="a1526-325">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="a1526-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1526-326">نتائج متغير الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1526-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="a1526-327">استخدم هذه الصفحة لإعداد نتائج الاختبار الممكنة وتحريرها وعرضها لأحد متغيرات الاختبار المرتبطة باختبار الجودة.</span><span class="sxs-lookup"><span data-stu-id="a1526-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="a1526-328">وللحصول على كل نتيجة، تقوم بتعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1526-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="a1526-329">يجب تعريف المتغير ونتائجه الخاصة بكل اختبار جودة الذي يتم تحديده في صفحة <strong>الاختبارات</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1526-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="a1526-330">(بالنسبة لاختبارات الجودة، يتم تعيين نوع الاختبار إلى <strong>الخيار</strong> في صفحة <strong>الاختبارات‬‏‫</strong>.) ‏‫استخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار والنتيجة الافتراضية لاختبار جودة فردي.‬</span><span class="sxs-lookup"><span data-stu-id="a1526-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="a1526-331">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="a1526-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="a1526-332">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="a1526-332">This inspection test has of several variables.</span></span> <span data-ttu-id="a1526-333">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="a1526-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="a1526-334">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="a1526-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="a1526-335">ويتم تعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong> لكل نتيجة.</span><span class="sxs-lookup"><span data-stu-id="a1526-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="a1526-336">أثناء اختبار الفحص الخاص بكل متغير، يقوم المفتش بالإعلام عن نتيجة الاختبار عن طريق تحديد إحدى النتائج.</span><span class="sxs-lookup"><span data-stu-id="a1526-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="a1526-337">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a1526-337">Additional resources</span></span>
--------

[<span data-ttu-id="a1526-338">عمليات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="a1526-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="a1526-339">تمكين إدارة عدم التوافق</span><span class="sxs-lookup"><span data-stu-id="a1526-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
