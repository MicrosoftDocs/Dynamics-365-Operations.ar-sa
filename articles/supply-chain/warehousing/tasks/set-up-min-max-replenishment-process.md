---
title: إعداد الحد الأدنى والحد الأقصى لعملية التزويد
description: يوضح هذا الإجراء كيفية إعداد عملية تزويد جديدة تستخدم استراتيجية الحد الأدنى/الحد الأقصى لعملية التزويد.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5fc03e0cf0ceb27a5cc406860bf5bd877e95460c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546607"
---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="3a843-103">إعداد الحد الأدنى والحد الأقصى لعملية التزويد</span><span class="sxs-lookup"><span data-stu-id="3a843-103">Set up a min-max replenishment process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a843-104">يوضح هذا الإجراء كيفية إعداد عملية تزويد جديدة تستخدم استراتيجية الحد الأدنى/الحد الأقصى لعملية التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="3a843-105">عندما يصبح المخزون أقل من الحد الأدنى، سيتم إنشاء العمل لتزويد الموقع.</span><span class="sxs-lookup"><span data-stu-id="3a843-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="3a843-106">يوضح الإجراء أيضًا كيفية استخدام مواقع انتقاء ثابتة للسماح بإعادة التخزين إذا كان المخزون أقل من مستوى الحد الأدنى، وكيفية تمكين عملية التزويد للتشغيل بانتظام باستخدام وظيفة مجموعة.</span><span class="sxs-lookup"><span data-stu-id="3a843-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="3a843-107">وعادة ما تُنفذ هذه المهام عن طريق مدير مستودع.</span><span class="sxs-lookup"><span data-stu-id="3a843-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="3a843-108">يمكنك تشغيل هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام قيم المثال في الملاحظات أو يمكن تشغيله على البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3a843-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="3a843-109">إذا كنت تستخدم البيانات الخاصة بك، فتأكد من حصولك على مستودع يتم تمكينه لعمليات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="3a843-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="3a843-110">إنشاء موقع انتقاء ثابت</span><span class="sxs-lookup"><span data-stu-id="3a843-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="3a843-111">انتقل إلى إدارة المستودعات > إعداد > المستودع > المواقع الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3a843-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="3a843-112">هذه مهمة اختيارية للحد الأدنى والحد الأقصى لعملية التزويد‬، ولكن إذا كنت تستخدم موقع انتقاء ثابت، فهذا يسمح بتزويد المخزون حتى إذا كان أقل من مستوى الحد الأدنى، لأن النظام يمكنه تحديد الأصناف التي بحاجة إلى التزويد، حتى إذا لم يكن هناك أي أصناف متبقية.</span><span class="sxs-lookup"><span data-stu-id="3a843-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="3a843-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-113">Click New.</span></span>
3. <span data-ttu-id="3a843-114">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-115">إذا كنت تستخدم USMF، يمكنك تحديد الصنف A0001.</span><span class="sxs-lookup"><span data-stu-id="3a843-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="3a843-116">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-117">إذا كنت تستخدم USMF، يمكنك تحديد "الموقع 2".</span><span class="sxs-lookup"><span data-stu-id="3a843-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="3a843-118">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-119">إذا كنت تستخدم الصنف، فيمكنك تحديد المستودع 24.</span><span class="sxs-lookup"><span data-stu-id="3a843-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="3a843-120">في الحقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-121">إذا كنت تستخدم USMF، فإنه يمكنك تحديد "CP-003".</span><span class="sxs-lookup"><span data-stu-id="3a843-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="3a843-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3a843-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="3a843-123">إنشاء توجيه موقع التزويد</span><span class="sxs-lookup"><span data-stu-id="3a843-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="3a843-124">انتقل إلى إدارة المستودعات > إعداد > توجيهات الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="3a843-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="3a843-125">يتم استخدام توجيهات الموقع لتحديد المكان الذي ينبغي أن يتم انتقاء الأصناف منه في عملية التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="3a843-126">في الحقل "نوع أمر العمل‬"، حدد "تزويد".</span><span class="sxs-lookup"><span data-stu-id="3a843-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="3a843-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-127">Click New.</span></span>
4. <span data-ttu-id="3a843-128">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3a843-129">في الحقل "نوع العمل"، حدد "انتقاء".</span><span class="sxs-lookup"><span data-stu-id="3a843-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="3a843-130">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-131">إذا كنت تستخدم USMF، يمكنك تحديد "الموقع 2".</span><span class="sxs-lookup"><span data-stu-id="3a843-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="3a843-132">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-133">إذا كنت تستخدم الصنف، فيمكنك تحديد المستودع 24.</span><span class="sxs-lookup"><span data-stu-id="3a843-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="3a843-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a843-134">Click Save.</span></span>
9. <span data-ttu-id="3a843-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-135">Click New.</span></span>
10. <span data-ttu-id="3a843-136">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a843-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3a843-137">في الحقل "إلى الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3a843-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="3a843-138">على سبيل المثال، يمكنك تعيينه على 9999.</span><span class="sxs-lookup"><span data-stu-id="3a843-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="3a843-139">حدد خانة الاختيار "السماح بالتقسيم".</span><span class="sxs-lookup"><span data-stu-id="3a843-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="3a843-140">إذا قمت بتحديد هذا الخيار، فستسمح عملية إنشاء العمل بعمل كميات بنود ليتم تقسيمها خلال مواقع متعددة.</span><span class="sxs-lookup"><span data-stu-id="3a843-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="3a843-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a843-141">Click Save.</span></span>
14. <span data-ttu-id="3a843-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-142">Click New.</span></span>
15. <span data-ttu-id="3a843-143">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a843-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="3a843-144">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="3a843-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a843-145">Click Save.</span></span>
18. <span data-ttu-id="3a843-146">انقر فوق "تحرير استعلام".</span><span class="sxs-lookup"><span data-stu-id="3a843-146">Click Edit query.</span></span>
    * <span data-ttu-id="3a843-147">يمكنك تحرير هذا الاستعلام لإضافة قيود حيث يمكن تحديد المخزون في عملية التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="3a843-148">على سبيل المثال، قد يكون هذا المخزون يجب استخدامه فقط من المنطقة الكبيرة من المستودع.</span><span class="sxs-lookup"><span data-stu-id="3a843-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="3a843-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3a843-149">Click OK.</span></span>
20. <span data-ttu-id="3a843-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3a843-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="3a843-151">إنشاء قالب عمل التزويد</span><span class="sxs-lookup"><span data-stu-id="3a843-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="3a843-152">انتقل إلى إدارة المستودعات > إعداد > العمل > قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="3a843-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="3a843-153">يتم استخدام قالب العمل لتوجيه النظام إلى كيفية إنشاء الحد الأدنى/الحد الأقصى لعملية التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="3a843-154">وكحد أدنى، يجب أن يكون هناك بند قالب عمل للانتقاء والوضع.</span><span class="sxs-lookup"><span data-stu-id="3a843-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="3a843-155">سيخبر قالب العمل أنه غير صالح حتى يتم كتابة جميع المعلومات اللازمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="3a843-156">في الحقل "نوع أمر العمل‬"، حدد "تزويد".</span><span class="sxs-lookup"><span data-stu-id="3a843-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="3a843-157">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-157">Click New.</span></span>
4. <span data-ttu-id="3a843-158">في الحقل "قالب العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="3a843-159">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a843-159">Click Save.</span></span>
6. <span data-ttu-id="3a843-160">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-160">Click New.</span></span>
7. <span data-ttu-id="3a843-161">في الحقل "نوع العمل"، حدد "انتقاء".</span><span class="sxs-lookup"><span data-stu-id="3a843-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="3a843-162">في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-163">ينبغي أن تكون فئة العمل المتعلقة بالتزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="3a843-164">إذا كنت تستخدم USMF، فحدد "تزويد".</span><span class="sxs-lookup"><span data-stu-id="3a843-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="3a843-165">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-165">Click New.</span></span>
10. <span data-ttu-id="3a843-166">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a843-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3a843-167">في الحقل "نوع العمل"، حدد "تم وضعه".</span><span class="sxs-lookup"><span data-stu-id="3a843-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="3a843-168">في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="3a843-169">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a843-169">Click Save.</span></span>
14. <span data-ttu-id="3a843-170">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3a843-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="3a843-171">إنشاء قالب تزويد جديد</span><span class="sxs-lookup"><span data-stu-id="3a843-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="3a843-172">انتقل إلى إدارة المستودعات > إعداد > التزويد > قوالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="3a843-173">يتم استخدام قالب التزويد لتحديد الأصناف والكميات والموقع للتزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="3a843-174">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-174">Click New.</span></span>
3. <span data-ttu-id="3a843-175">في الحقل "قالب التزويد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="3a843-176">أطلق اسمًا على القالب للإشارة إلى أنه يخص الحد الأدنى/الحد الأقصى لعملية التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="3a843-177">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3a843-178">حدد خانة الاختيار "السماح لطلب الموجة باستخدام الكميات غير المحجوزة".</span><span class="sxs-lookup"><span data-stu-id="3a843-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="3a843-179">بتحديد هذا الخيار، يتم تمكين تزويد طلب الموجة لاستهلاك الكميات المتعلقة بالحد الأدنى/الحد الأقصى لعملية التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="3a843-180">على سبيل المثال، قد يكون ذلك مفيدًا إذا لم تتم معالجة الحد الأدنى/الحد الأقصى لعملية التزويد على الفور، لتجنب إنشاء عمل التزويد الطلب غير الضروري.</span><span class="sxs-lookup"><span data-stu-id="3a843-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="3a843-181">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a843-181">Click New.</span></span>
7. <span data-ttu-id="3a843-182">في الحقل "الرقم التسلسلي"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3a843-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="3a843-183">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="3a843-184">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a843-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="3a843-185">في الحقل "وحدة التزويد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-186">على سبيل المثال، حدد "أجزاء".</span><span class="sxs-lookup"><span data-stu-id="3a843-186">For example, select pcs.</span></span> <span data-ttu-id="3a843-187">هذا الإعداد إلزامي.</span><span class="sxs-lookup"><span data-stu-id="3a843-187">This setting is mandatory.</span></span> <span data-ttu-id="3a843-188">يسمح لك بتحديد وحدة قياس مختلفة لعمل التزويد مقارنة بالوحدة المحددة لمستويات الحد الأدنى والحد الأقصى للمخزون في هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="3a843-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="3a843-189">في الحقل "قالب العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-190">اختر قالب العمل الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="3a843-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="3a843-191">في الحقل "الحد الأدنى للكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3a843-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="3a843-192">حدد الحد الأدنى للكمية الذي يمكنه تشغل التزويد.</span><span class="sxs-lookup"><span data-stu-id="3a843-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="3a843-193">على سبيل المثال، قم بتعيين هذا على 50.</span><span class="sxs-lookup"><span data-stu-id="3a843-193">For example, set this to 50.</span></span> <span data-ttu-id="3a843-194">من الممكن ترك هذه المجموعة على صفر، إذا كنت تقوم بتزويد موقع ثابت وتعيين خيار "تزويد المواقع الثابتة الفارغة" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="3a843-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="3a843-195">كما نوصي بتحديد الخيار "تزويد المواقع الثابتة فقط" لأسباب تتعلق بالأداء.</span><span class="sxs-lookup"><span data-stu-id="3a843-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="3a843-196">في الحقل "الحد الأقصى للكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3a843-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="3a843-197">على سبيل المثال، قم بتعيين هذا على 100.</span><span class="sxs-lookup"><span data-stu-id="3a843-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="3a843-198">في الحقل "وحدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="3a843-199">قم بتعيين الوحدة الخاصة بالحد الأدنى والحد الأقصى للكميات.</span><span class="sxs-lookup"><span data-stu-id="3a843-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="3a843-200">على سبيل المثال، قم بتعيين هذا على "أجزاء".</span><span class="sxs-lookup"><span data-stu-id="3a843-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="3a843-201">حدد خانة الاختيار "تزويد المواقع الثابتة الفارغة".</span><span class="sxs-lookup"><span data-stu-id="3a843-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="3a843-202">حدد خانة الاختيار هذه لتزويد المواقع الثابتة عندما تكون فارغة.</span><span class="sxs-lookup"><span data-stu-id="3a843-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="3a843-203">وإلا، فقط سيتم تزويد المواقع التي يوجد بها كميات فعلية.</span><span class="sxs-lookup"><span data-stu-id="3a843-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="3a843-204">حدد خانة الاختيار "تزويد المواقع الثابتة فقط".</span><span class="sxs-lookup"><span data-stu-id="3a843-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="3a843-205">انقر فوق "تحديد المنتجات".</span><span class="sxs-lookup"><span data-stu-id="3a843-205">Click Select products.</span></span>
    * <span data-ttu-id="3a843-206">هذا هو المكان حيث يتم تحديد المنتجات التي ينبغي تزويدها.</span><span class="sxs-lookup"><span data-stu-id="3a843-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="3a843-207">إذا تم تحديد الخيار "مواقع الانتقاء الثابتة"، فإنك تحتاج أيضًا إلى تحديد المواقع في هذا الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="3a843-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="3a843-208">تتوافر الاستعلامات الخاصة بمتغير بالإضافة إلى الاستعلامات الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="3a843-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="3a843-209">حدد صف الأصناف.</span><span class="sxs-lookup"><span data-stu-id="3a843-209">Select the Items row.</span></span>
19. <span data-ttu-id="3a843-210">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a843-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3a843-211">حدد الأصناف التي يجب تزويدها في المواقع الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3a843-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="3a843-212">على سبيل المثال، اكتب أ\* لتحديد كل أرقام الأصناف التي تبدأ بحرف أ.</span><span class="sxs-lookup"><span data-stu-id="3a843-212">For example, type A\* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="3a843-213">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3a843-213">Click Add.</span></span>
    * <span data-ttu-id="3a843-214">أضف كيان الموقع (إلا إذا كان موجودًا بالفعل) حتى تكون قادرًا على تقييد عمل التزويد إلى مواقع انتقاء ثابتة داخل منطقة معينة من المستودع.</span><span class="sxs-lookup"><span data-stu-id="3a843-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="3a843-215">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a843-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="3a843-216">قم بتعيين الحقل "الجدول" على ''المواقع".</span><span class="sxs-lookup"><span data-stu-id="3a843-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="3a843-217">في الحقل "الحقل"، حدد "معرف ملف تعريف الموقع".</span><span class="sxs-lookup"><span data-stu-id="3a843-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="3a843-218">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="3a843-219">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3a843-219">Click OK.</span></span>
26. <span data-ttu-id="3a843-220">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3a843-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="3a843-221">تعيين عملية التزويد للتشغيل كوظيفة دفعية</span><span class="sxs-lookup"><span data-stu-id="3a843-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="3a843-222">انتقل إلى إدارة المستودعات > التزويد > عمليات التزويد‬.</span><span class="sxs-lookup"><span data-stu-id="3a843-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="3a843-223">تسمح لك صفحة التزويد بإعداد التزويد لتشغيله كوظيفة دفعية أو تتطلب أن يتم بدء التشغيل يدويًا.</span><span class="sxs-lookup"><span data-stu-id="3a843-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="3a843-224">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="3a843-224">Click Filter.</span></span>
3. <span data-ttu-id="3a843-225">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a843-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3a843-226">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a843-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="3a843-227">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="3a843-227">Click OK.</span></span>
6. <span data-ttu-id="3a843-228">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="3a843-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="3a843-229">قم بتعيين خيار "معالجة الدفعة" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="3a843-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="3a843-230">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="3a843-230">Click Recurrence.</span></span>
9. <span data-ttu-id="3a843-231">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="3a843-231">Select the No end date option.</span></span>
10. <span data-ttu-id="3a843-232">قم بتعيين نمط التكرار.</span><span class="sxs-lookup"><span data-stu-id="3a843-232">Set the Recurrance pattern.</span></span>
    * <span data-ttu-id="3a843-233">على سبيل المثال: حدد "أيام".</span><span class="sxs-lookup"><span data-stu-id="3a843-233">For example, select Days.</span></span>  
11. <span data-ttu-id="3a843-234">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3a843-234">Click OK.</span></span>
12. <span data-ttu-id="3a843-235">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3a843-235">Click OK.</span></span>

