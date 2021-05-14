---
title: إنشاء حالات عدم المطابقة ومعالجتها
description: يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956196"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="294fb-103">إنشاء حالات عدم المطابقة ومعالجتها</span><span class="sxs-lookup"><span data-stu-id="294fb-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="294fb-104">يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.</span><span class="sxs-lookup"><span data-stu-id="294fb-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="294fb-105">عادةً ما يتم إدارة عدم المطابقة بواسطة موظف الجودة.</span><span class="sxs-lookup"><span data-stu-id="294fb-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="294fb-106">كشرط أساسي، يجب أن يكون لديك أمر جودة متاح.</span><span class="sxs-lookup"><span data-stu-id="294fb-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="294fb-107">(للحصول على معلومات حول كيفية إنشاء أمر الجودة، راجع [فحص جودة البضائع](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="294fb-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="294fb-108">قبل أن يتمكن المستخدم من معالجة الموافقة على عدم المطابقة، يجب تعيين عامل لهم في حقل **الشخص** في صفحة **المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="294fb-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="294fb-109">بالإضافة إلى ذلك، قبل أن يتمكن المستخدم من استخدام ملاحظات المستند، فإنه يجب تعيين خيار **تمكين معالجة المستندات** إلى *نعم* في خيارات المستخدم الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="294fb-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="294fb-110">إنشاء عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-110">Create a nonconformance</span></span>

<span data-ttu-id="294fb-111">لإنشاء حالة عدم مطابقة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="294fb-112">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-113">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="294fb-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="294fb-114">في مربع الحوار **إنشاء عدم المطابقة** في حقل **نوع المشكلة**، حدد نوع المشكلة التي تم العثور عليها أثناء عملية الفحص.</span><span class="sxs-lookup"><span data-stu-id="294fb-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="294fb-115">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="294fb-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="294fb-116">الموافقة على أو رفض عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="294fb-117">للموافقة على عدم المطابقة أو رفضه، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="294fb-118">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-119">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-120">يمكنك إضافة تصحيح فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-121">في جزء الإجراء، حدد **الوظائف \> الموافقة على عدم المطابقة** للموافقة على عدم المطابقة أو **الوظائف \> رفض عدم المطابقة** لرفضها.</span><span class="sxs-lookup"><span data-stu-id="294fb-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="294fb-122">يمكنك ربط حالات عدم المطابقة التي تمت الموافقة عليها بـ [العمليات ذات الصلة](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="294fb-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="294fb-123">بهذه الطريقة، يمكنك تسجيل العمل الذي تم إجراؤه كجزء من معالجة عدم المطابقة ومعالجة عملية التصحيح.</span><span class="sxs-lookup"><span data-stu-id="294fb-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="294fb-124">يُطلب منك تأكيد اختيارك.</span><span class="sxs-lookup"><span data-stu-id="294fb-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="294fb-125">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="294fb-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="294fb-126">إضافة العمليات والتفاصيل الأخرى إلى حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="294fb-127">بعد إنشاء حالة عدم المطابقة، يمكنك البدء في إضافة العمليات ذات الصلة وتحديد معلومات إضافية حول تلك العمليات.</span><span class="sxs-lookup"><span data-stu-id="294fb-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="294fb-128">يمكنك إضافة العمليات ذات الصلة فقط إلى حالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="294fb-129">بالإضافة إلى المعلومات الأساسية، يمكنك إضافة التفاصيل التالية إلى العملية:</span><span class="sxs-lookup"><span data-stu-id="294fb-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="294fb-130">**العناصر** – يمكنك إنشاء قائمة بالعناصر المستهلكة لإجراء التصحيح.</span><span class="sxs-lookup"><span data-stu-id="294fb-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="294fb-131">على سبيل المثال، قد تكون العناصر عبارة عن منتجات مطلوبة لإصلاح المعدات أو المكونات المطلوبة لإعادة صياغة منتج نهائي.</span><span class="sxs-lookup"><span data-stu-id="294fb-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="294fb-132">**رسوم الجودة** – يمكنك إنشاء قائمة بالرسوم التي يتم تكبدها أو إصدار فواتير بها إلى مصادر خارجية.</span><span class="sxs-lookup"><span data-stu-id="294fb-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="294fb-133">**جدول زمني** – يمكنك إنشاء سجل للوقت الذي يقضيه كل عامل في العملية.</span><span class="sxs-lookup"><span data-stu-id="294fb-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="294fb-134">الإعدادات المتبقية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="294fb-134">The remaining settings are optional.</span></span> <span data-ttu-id="294fb-135">يتم تجميع تكلفة كل عنصر ورسوم الجودة والجدول الزمني وعرضها في العملية.</span><span class="sxs-lookup"><span data-stu-id="294fb-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="294fb-136">لا يمكنك تحرير حقل **التكلفة** في العملية مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="294fb-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="294fb-137">إنشاء عملية لعدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="294fb-138">لإنشاء عملية لحالة عدم مطابقة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="294fb-139">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-140">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-141">يمكنك إضافة أو تحديث العمليات فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-142">في جزء الإجراءات، حدد **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="294fb-143">في صفحة **العمليات ذات الصلة**، في جزء الإجراء، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="294fb-144">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="294fb-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="294fb-145">**العملية** – حدد كود العملية التي سيتم إجراؤها لعدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="294fb-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="294fb-146">**السبب** – أدخل وصفا مفصلا يوضح لماذا تكون العملية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="294fb-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="294fb-147">**أمر المبيعات** – إذا كان كود العملية المحدد مرتبطًا بنوع أمر المبيعات، فحدد أمر المبيعات الذي تربط العملية به.</span><span class="sxs-lookup"><span data-stu-id="294fb-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="294fb-148">**أمر الشراء** – إذا كان رمز العملية المحدد مرتبطًا بنوع أمر الشراء، فحدد أمر الشراء الذي تربط العملية به.</span><span class="sxs-lookup"><span data-stu-id="294fb-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="294fb-149">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="294fb-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="294fb-150">إضافة عناصر إلى عملية</span><span class="sxs-lookup"><span data-stu-id="294fb-150">Add items to an operation</span></span>

<span data-ttu-id="294fb-151">لإضافة عناصر إلى عملية ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="294fb-152">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-153">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-154">يمكنك إضافة أو تحديث العمليات فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-155">في جزء الإجراءات، حدد **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="294fb-156">في صفحة **العمليات ذات الصلة**، حدد العملية التي تريد إضافة عناصر إليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="294fb-157">في جزء الإجراءات، حدد **الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="294fb-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="294fb-158">في صفحة **العمليات ذات الصلة**، في جزء الإجراء، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="294fb-159">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="294fb-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="294fb-160">**رقم العنصر** – حدد المنتج الذي سيتم استهلاكه كجزء من العملية المحددة.</span><span class="sxs-lookup"><span data-stu-id="294fb-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="294fb-161">**الكمية** – أدخل عدد العناصر التي سيتم استهلاكها.</span><span class="sxs-lookup"><span data-stu-id="294fb-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-162">يمكنك عرض تكلفة العنصر في حقل **التكلفة** في علامة التبويب **عام**. تأتي التكلفة المعروضة هناك من التكلفة التي تم إعدادها في صفحة **المنتج الصادر**.</span><span class="sxs-lookup"><span data-stu-id="294fb-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="294fb-163">لا يمكن تحديث التكلفة مباشرةً في صفحة **عنصر العملية ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="294fb-164">تتم إضافة تكلفة جميع العناصر التي تمت إضافتها إلى صفحة **عناصر العملية ذات الصلة** إلى حقل **التكلفة** في صفحة **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="294fb-165">كرر الخطوة السابقة لكل عنصر إضافي يجب عليك إضافته.</span><span class="sxs-lookup"><span data-stu-id="294fb-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="294fb-166">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="294fb-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="294fb-167">إضافة رسوم الجودة إلى العملية</span><span class="sxs-lookup"><span data-stu-id="294fb-167">Add quality charges to an operation</span></span>

<span data-ttu-id="294fb-168">لإضافة رسوم الجودة إلى عملية ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="294fb-169">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-170">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-171">يمكنك إضافة أو تحديث العمليات فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-172">في جزء الإجراءات، حدد **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="294fb-173">في صفحة **العمليات ذات الصلة**، حدد العملية التي تريد إضافة رسوم الجودة إليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="294fb-174">في جزء الإجراءات، حدد **رسوم الجودة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="294fb-175">في صفحة **رسوم العمليات ذات الصلة**، في جزء الإجراء، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="294fb-176">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="294fb-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="294fb-177">**كود المصاريف** – حدد رسوم الجودة التي ترغب في إضافتها.</span><span class="sxs-lookup"><span data-stu-id="294fb-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="294fb-178">**الوصف** - أدخل وصفًا مفصلاً للمصاريف.</span><span class="sxs-lookup"><span data-stu-id="294fb-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="294fb-179">**قيمة المصاريف** – أدخل مبلغ المصاريف.</span><span class="sxs-lookup"><span data-stu-id="294fb-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="294fb-180">كرر الخطوة السابقة لكل تكلفة إضافية يجب عليك إضافتها.</span><span class="sxs-lookup"><span data-stu-id="294fb-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="294fb-181">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="294fb-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="294fb-182">يتم جمع المبلغ الموجود في حقل **قيمة المصاريف** تلقائيًا لجميع مصاريف الجودة وتتم إضافته إلى أي مبالغ أخرى في حقل **التكلفة** في صفحة **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="294fb-183">إنشاء جدول زمني لعملية</span><span class="sxs-lookup"><span data-stu-id="294fb-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="294fb-184">لإضافة جدول زمني إلى عملية ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="294fb-185">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-186">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-187">يمكنك إضافة أو تحديث العمليات فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-188">في جزء الإجراءات، حدد **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="294fb-189">في صفحة **العمليات ذات الصلة**، حدد العملية التي تريد إضافة جدول زمني إليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="294fb-190">في جزء الإجراءات، حدد **الجدول الزمني**.</span><span class="sxs-lookup"><span data-stu-id="294fb-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="294fb-191">في صفحة **الجداول الزمنية لرسوم العمليات ذات الصلة**، في جزء الإجراء، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="294fb-192">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="294fb-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="294fb-193">**التاريخ** - حدد التاريخ الذي تم فيه تنفيذ العمل.</span><span class="sxs-lookup"><span data-stu-id="294fb-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="294fb-194">بشكل افتراضي، يتم تعيين هذا الحقل إلى التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="294fb-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="294fb-195">**العامل** – حدد العامل الذي قام بالعمل.</span><span class="sxs-lookup"><span data-stu-id="294fb-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="294fb-196">بشكل افتراضي، يتم تعيين هذا الحقل للعامل الذي تم تعيينه للمستخدم الحالي.</span><span class="sxs-lookup"><span data-stu-id="294fb-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="294fb-197">**ساعات العملية** – أدخل عدد الساعات التي تم العمل بها في العملية المحددة.</span><span class="sxs-lookup"><span data-stu-id="294fb-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="294fb-198">**مفوتر** – حدد خانة الاختيار هذه إذا تم خصم الوقت من العميل أو المورد في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="294fb-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-199">يمكنك عرض التكلفة في حقل **التكلفة** في علامة التبويب **عام**. يتم حساب التكلفة باستخدام السعر الذي تحدده في صفحة **معلمات إدارة المخزون**.</span><span class="sxs-lookup"><span data-stu-id="294fb-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="294fb-200">كرر الخطوة السابقة لكل بند جدول زمني إضافي يجب إضافته.</span><span class="sxs-lookup"><span data-stu-id="294fb-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="294fb-201">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="294fb-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="294fb-202">يتم جمع المبلغ الموجود في حقل **التكلفة** لجميع بنود الجدول الزمني وتتم إضافته إلى أي مبالغ أخرى في حقل **التكلفة** في صفحة **العمليات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="294fb-203">إضافة تصحيح إلى عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="294fb-204">لإضافة تصحيح إلى عدم مطابقة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="294fb-205">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-206">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-207">يمكنك إضافة تصحيح فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-208">في جزء الإجراءات، حدد **التصحيحات**.</span><span class="sxs-lookup"><span data-stu-id="294fb-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="294fb-209">في صفحة **التصحيحات**، في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="294fb-210">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="294fb-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="294fb-211">**تشخيص** – حدد نوع التشخيص الذي يحدد نوع التصحيح الذي تقوم بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="294fb-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="294fb-212">**العامل** – حدد الشخص المسؤول عن التصحيح.</span><span class="sxs-lookup"><span data-stu-id="294fb-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="294fb-213">**أولوية التصحيح** – حدد خيارًا للإشارة إلى كيفية إعطاء الأولوية للتصحيح (*منخفضة* أو *عادية* أو *عالية*).</span><span class="sxs-lookup"><span data-stu-id="294fb-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="294fb-214">**التاريخ المطلوب** – أدخل التاريخ الذي تم فيه طلب إجراء التصحيح.</span><span class="sxs-lookup"><span data-stu-id="294fb-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="294fb-215">**التاريخ المخطط** – أدخل التاريخ الذي يتوقع فيه إكمال التصحيح.</span><span class="sxs-lookup"><span data-stu-id="294fb-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="294fb-216">**حل قصير الأجل** – حدد خانه الاختيار هذه إذا كان إجراء التصحيح يصحح عدم المطابقة فقط لوقت قصير.</span><span class="sxs-lookup"><span data-stu-id="294fb-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="294fb-217">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="294fb-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="294fb-218">وضع علامة على التصحيح كمكتمل</span><span class="sxs-lookup"><span data-stu-id="294fb-218">Mark a correction as completed</span></span>

<span data-ttu-id="294fb-219">لوضع علامة مكتمل على تصحيح عدم المطابقة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="294fb-220">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-221">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="294fb-222">يمكنك إضافة تصحيح فقط لحالات عدم المطابقة التي تمت الموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="294fb-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="294fb-223">في جزء الإجراءات، حدد **التصحيحات**.</span><span class="sxs-lookup"><span data-stu-id="294fb-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="294fb-224">في صفحة **التصحيحات**، في الشبكة، حدد التصحيح الذي تريد وضع علامة مكتمل عليه.</span><span class="sxs-lookup"><span data-stu-id="294fb-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="294fb-225">في جزء الإجراءات، حدد **وضع علامة مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="294fb-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="294fb-226">يُطلب منك تأكيد اختيارك.</span><span class="sxs-lookup"><span data-stu-id="294fb-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="294fb-227">حدد **موافق** للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="294fb-227">Select **OK** to continue.</span></span> <span data-ttu-id="294fb-228">يتم تعيين حقل **تاريخ ووقت الإكمال** إلى التاريخ والوقت الحاليين، ويتم تحديد خانة الاختيار **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="294fb-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="294fb-229">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="294fb-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="294fb-230">إعادة فتح تصحيح مكتمل</span><span class="sxs-lookup"><span data-stu-id="294fb-230">Reopen a completed correction</span></span>

<span data-ttu-id="294fb-231">لإعادة فتح تصحيح مكتمل، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="294fb-232">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-233">في القائمة، حدد عدم المطابقة الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="294fb-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="294fb-234">في جزء الإجراءات، حدد **التصحيحات**.</span><span class="sxs-lookup"><span data-stu-id="294fb-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="294fb-235">في صفحة **التصحيحات**، في الشبكة، حدد التصحيح الذي تريد إعادة فتحه.</span><span class="sxs-lookup"><span data-stu-id="294fb-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="294fb-236">في "جزء الإجراءات"، حدد **إعادة فتح**.</span><span class="sxs-lookup"><span data-stu-id="294fb-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="294fb-237">يُطلب منك تأكيد اختيارك.</span><span class="sxs-lookup"><span data-stu-id="294fb-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="294fb-238">حدد **موافق** للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="294fb-238">Select **OK** to continue.</span></span> <span data-ttu-id="294fb-239">ويتم مسح القيمة من حقل **تاريخ ووقت الاكتمال**، ويتم مسح خانة الاختيار **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="294fb-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="294fb-240">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="294fb-240">Close the page.</span></span>

<span data-ttu-id="294fb-241">يمكنك الآن إجراء تعديلات أو تحديثات إضافية على التصحيح.</span><span class="sxs-lookup"><span data-stu-id="294fb-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="294fb-242">عند الانتهاء، يمكنك وضع علامة على التصحيح على أنه مكتمل مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="294fb-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="294fb-243">إغلاق حالة عدم مطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-243">Close a nonconformance</span></span>

<span data-ttu-id="294fb-244">لإغلاق حالة عدم مطابقة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="294fb-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="294fb-245">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="294fb-246">حدد أمر الجودة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="294fb-247">في جزء الإجراءات، حدد **الاستعلامات \> حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="294fb-248">في صفحة **حالات عدم المطابقة**، حدد حالة عدم المطابقة الهدف في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="294fb-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="294fb-249">في جزء الإجراءات، حدد **الوظائف \> إغلاق حالة عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="294fb-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="294fb-250">يُطلب منك تأكيد اختيارك.</span><span class="sxs-lookup"><span data-stu-id="294fb-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="294fb-251">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="294fb-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="294fb-252">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="294fb-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="294fb-253">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="294fb-253">Additional resources</span></span>

- [<span data-ttu-id="294fb-254">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="294fb-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="294fb-255">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="294fb-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="294fb-256">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="294fb-257">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="294fb-258">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="294fb-259">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="294fb-260">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="294fb-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="294fb-261">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="294fb-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
