---
title: "مهام الخدمة"
description: "استخدم مهام الخدمة لوصف المهمة المراد إكمالها خلال أمر الخدمة. يستطيع كل من الفنيين والعملاء رؤية هذه المعلومات."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: de180a1258bbfb95acbfd0985cb91c88efc320f2
ms.contentlocale: ar-sa
ms.lasthandoff: 02/21/2018

---

# <a name="service-tasks"></a><span data-ttu-id="ddcfe-104">مهام الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-104">Service tasks</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ddcfe-105">استخدم مهام الخدمة لوصف المهمة المراد إكمالها خلال أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="ddcfe-106">يستطيع كل من الفنيين والعملاء رؤية هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="ddcfe-107">يمكنك إنشاء مهام الخدمة في صفحة **مهام الخدمة**، ويمكنك إقران مهام الخدمة باتفاقية خدمة أو أمر خدمة محدد وذلك بواسطة إنشاء علاقات مهمة خدمة.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="ddcfe-108">وفي كل مرة تقوم فيها بإنشاء علاقة مهمة خدمة، يمكنك إنشاء ما يلي:</span><span class="sxs-lookup"><span data-stu-id="ddcfe-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="ddcfe-109">ملاحظات داخلية للمهمة، مثل طلبات فنية مفصلة للمهمة التي ينبغي أن يعرفها الفني.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="ddcfe-110">ملاحظات خارجية يمكن للعميل الاطلاع عليها.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-110">External notes that the customer can see.</span></span> <span data-ttu-id="ddcfe-111">وقد توفر هذه الملاحظات شرحًا فنيًا أقل للمهمة التي يتم إكمالها وفقًا للاتفاقية المبرمة بين العميل والشركة الموفرة للخدمة.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="ddcfe-112">عندما تقوم بإعداد علاقة مهمة الخدمة بين مهمة الخدمة وأمر الخدمة أو اتفاقية الخدمة، يمكنك تحديد مهمة الخدمة هذه عند إنشاء بنود أمر الخدمة أو بنود اتفاقية الخدمة لأمر الخدمة أو اتفاقية الخدمة الحالية.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="ddcfe-113">عند إنشاء أوامر خدمة من اتفاقية خدمة، يمكنك استخدام مهام الخدمة المعينة لكل بند اتفاقية خدمة لتجميع بنود أمر الخدمة في أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="ddcfe-114">إنشاء مهمة خدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-114">Create a service task</span></span>

1. <span data-ttu-id="ddcfe-115">انقر فوق **إدارة الخدمة‬** \> **الإعداد** \> **مهام الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="ddcfe-116">قم بإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-116">Create a new line.</span></span>
3. <span data-ttu-id="ddcfe-117">أدخل معرف الخدمة ووصفًا لها.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="ddcfe-118">مثال</span><span class="sxs-lookup"><span data-stu-id="ddcfe-118">Example</span></span>

<span data-ttu-id="ddcfe-119">يجب على الفني إكمال وظيفتين على علبة التروس (كائن الخدمة GB-1234) في موقع العميل.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="ddcfe-120">ويتم إنشاء اتفاقية الخدمة للعميل، ويتم إقران العديد من الحركات بالوظائف.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="ddcfe-121">اتفاقية الخدمة وبنود اتفاقية الخدمة للوظيفتين هي على الشكل التالي:</span><span class="sxs-lookup"><span data-stu-id="ddcfe-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="ddcfe-122">اتفاقية الخدمات</span><span class="sxs-lookup"><span data-stu-id="ddcfe-122">Service agreement</span></span>

| <span data-ttu-id="ddcfe-123">Project</span><span class="sxs-lookup"><span data-stu-id="ddcfe-123">Project</span></span> | <span data-ttu-id="ddcfe-124">اتفاقية الخدمات</span><span class="sxs-lookup"><span data-stu-id="ddcfe-124">Service agreement</span></span> | <span data-ttu-id="ddcfe-125">الوصف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-125">Description</span></span>                                  | <span data-ttu-id="ddcfe-126">مجموعة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="ddcfe-127">9012</span><span class="sxs-lookup"><span data-stu-id="ddcfe-127">9012</span></span>    | <span data-ttu-id="ddcfe-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="ddcfe-128">000008\_001</span></span>       | <span data-ttu-id="ddcfe-129">فحص واستبدال روتيني – GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="ddcfe-130">المكافأة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="ddcfe-131">حدود اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-131">Service agreement lines</span></span>

| <span data-ttu-id="ddcfe-132">الوصف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-132">Description</span></span>             | <span data-ttu-id="ddcfe-133">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-133">Transaction type</span></span> | <span data-ttu-id="ddcfe-134">كائن الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-134">Service object</span></span> | <span data-ttu-id="ddcfe-135">مهمة الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="ddcfe-136">الفحص والتنظيف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-136">Inspection and cleaning</span></span> | <span data-ttu-id="ddcfe-137">ساعة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-137">Hour</span></span>             | <span data-ttu-id="ddcfe-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-138">GB-1234</span></span>        | <span data-ttu-id="ddcfe-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-139">I/C - GB1234</span></span> |
| <span data-ttu-id="ddcfe-140">سفر</span><span class="sxs-lookup"><span data-stu-id="ddcfe-140">Travel</span></span>                  | <span data-ttu-id="ddcfe-141">المصروفات</span><span class="sxs-lookup"><span data-stu-id="ddcfe-141">Expense</span></span>          | <span data-ttu-id="ddcfe-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-142">GB-1234</span></span>        | <span data-ttu-id="ddcfe-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-143">I/C - GB1234</span></span> |
| <span data-ttu-id="ddcfe-144">المواد</span><span class="sxs-lookup"><span data-stu-id="ddcfe-144">Materials</span></span>               | <span data-ttu-id="ddcfe-145">الصنف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-145">Item</span></span>             | <span data-ttu-id="ddcfe-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-146">GB-1234</span></span>        | <span data-ttu-id="ddcfe-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-147">I/C - GB1234</span></span> |
| <span data-ttu-id="ddcfe-148">استبدال روتيني</span><span class="sxs-lookup"><span data-stu-id="ddcfe-148">Routine replacement</span></span>     | <span data-ttu-id="ddcfe-149">ساعة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-149">Hour</span></span>             | <span data-ttu-id="ddcfe-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-150">GB-1234</span></span>        | <span data-ttu-id="ddcfe-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-151">RR - GB1234</span></span>  |
| <span data-ttu-id="ddcfe-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="ddcfe-152">GR-1</span></span>                    | <span data-ttu-id="ddcfe-153">الصنف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-153">Item</span></span>             | <span data-ttu-id="ddcfe-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-154">GB-1234</span></span>        | <span data-ttu-id="ddcfe-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-155">RR - GB1234</span></span>  |
| <span data-ttu-id="ddcfe-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="ddcfe-156">GR-5</span></span>                    | <span data-ttu-id="ddcfe-157">الصنف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-157">Item</span></span>             | <span data-ttu-id="ddcfe-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-158">GB-1234</span></span>        | <span data-ttu-id="ddcfe-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-159">RR - GB1234</span></span>  |

<span data-ttu-id="ddcfe-160">تحتوي بنود اتفاقية الخدمة للوظيفتين على مهمتي خدمة مرفقتين بها.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="ddcfe-161">وتحدد مهمة الخدمة الحركات التي تنتمي إلى كل وظيفة.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="ddcfe-162">في الحالة الأولى، تقوم مهمة الخدمة I/C - GB1234 بتحديد كافة بنود اتفاقية الخدمة المشاركة في فحص الكائن GB-1234 وتنظيفه.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="ddcfe-163">وفي الحالة الثانية، تقوم مهمة الخدمة RR - GB1234 بتحديد كافة بنود اتفاقية الخدمة المشاركة في إكمال وظيفة الاستبدال الروتيني.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="ddcfe-164">علاقات مهمة الخدمة التي تربط بين مهام الخدمة واتفاقية محددة هي كالتالي:</span><span class="sxs-lookup"><span data-stu-id="ddcfe-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="ddcfe-165">مهام الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-165">Service tasks</span></span>

| <span data-ttu-id="ddcfe-166">مهمة الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-166">Service task</span></span> | <span data-ttu-id="ddcfe-167">الوصف</span><span class="sxs-lookup"><span data-stu-id="ddcfe-167">Description</span></span>                             | <span data-ttu-id="ddcfe-168">ملاحظة داخلية</span><span class="sxs-lookup"><span data-stu-id="ddcfe-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="ddcfe-169">ملاحظة خارجية</span><span class="sxs-lookup"><span data-stu-id="ddcfe-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="ddcfe-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-170">I/C - GB1234</span></span> | <span data-ttu-id="ddcfe-171">فحص علبة التروس GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="ddcfe-172">الفحص البصري والآلي وتنظيف علبة التروس GB-1234.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="ddcfe-173">فحص روتيني لعلبة التروس</span><span class="sxs-lookup"><span data-stu-id="ddcfe-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="ddcfe-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-174">RR - GB1234</span></span>  | <span data-ttu-id="ddcfe-175">استبدال روتيني لأجزاء GB-1234</span><span class="sxs-lookup"><span data-stu-id="ddcfe-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="ddcfe-176">استبدال خدمة روتيني لمكونات GR-1 وGR-5 (لعلب التروس التي تمت صناعتها قبل 2002، وكذلك استبدال مكونات GR-2)</span><span class="sxs-lookup"><span data-stu-id="ddcfe-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="ddcfe-177">استبدال أجزاء روتيني</span><span class="sxs-lookup"><span data-stu-id="ddcfe-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="ddcfe-178">تجميع أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="ddcfe-178">Group service orders</span></span>

<span data-ttu-id="ddcfe-179">عندما تقوم بإنشاء أوامر الخدمة تلقائيًا، يمكنك استخدام مهام الخدمة كمعيار تجميع.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="ddcfe-180">ولتجميع أوامر الخدمة حسب مهام الخدمة، يجب أن تحدد في اتفاقية الخدمة أن أوامر الخدمة التي تستند إلى اتفاقية الخدمة يجب أن يتم تجميعها حسب معرّف مهمة الخدمة كمعيار التجميع الأولي الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="ddcfe-181">**تجميع حسب مهمة الخدمة**</span><span class="sxs-lookup"><span data-stu-id="ddcfe-181">**Group by service task**</span></span>

1. <span data-ttu-id="ddcfe-182">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="ddcfe-183">على علامة تبويب **الإعداد**، حدد **حسب مهمة الخدمة‬** في الحقل **تجميع أوامر الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


