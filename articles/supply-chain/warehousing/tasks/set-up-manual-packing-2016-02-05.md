--- 
title: "إعداد التعبئة اليدوية (فبراير ومايو 2016 فقط)"
description: "تسمح لك عملية التعبئة بالتحقق من المنتجات داخل الحاويات وتعبئتها."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 714fd4762ae54f8f6638e81dd19fdd636091b88e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="15cfc-103">إعداد التعبئة اليدوية (فبراير ومايو 2016 فقط)</span><span class="sxs-lookup"><span data-stu-id="15cfc-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15cfc-104">تسمح لك عملية التعبئة بالتحقق من المنتجات داخل الحاويات وتعبئتها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="15cfc-105">في هذه العملية، يعمل عمال المستودع على انتقاء المنتجات من مواقع التخزين ونقلها إلى محطة تعبئة حيث يتحققون من كميات الأصناف وأنواعها ووضعها في حاويات مناسبة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="15cfc-106">عند وجود حاوية معبأة تمامًا، فإنه يمكنك إغلاقها ونقلها إلى مساحات خارجية وتكون المنتجات جاهزة للشحن.</span><span class="sxs-lookup"><span data-stu-id="15cfc-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="15cfc-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="15cfc-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="15cfc-108">إعداد ملفات تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="15cfc-108">Set up location profiles</span></span>
1. <span data-ttu-id="15cfc-109">انتقل إلى إدارة المستودعات‬ > إعداد > المستودع > ملفات تعريف الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="15cfc-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="15cfc-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="15cfc-110">Click New.</span></span>
    * <span data-ttu-id="15cfc-111">يتم استخدام ملف تعريف الموقع لمحطات التعبئة ويحتوي على معلومات وقواعد لموقع ما.</span><span class="sxs-lookup"><span data-stu-id="15cfc-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="15cfc-112">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="15cfc-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="15cfc-114">في الحقل "تنسيق الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="15cfc-115">في الحقل "نوع الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="15cfc-116">حدد "نعم" في حقل "‏‫‏‫السماح بالأصناف المختلطة".</span><span class="sxs-lookup"><span data-stu-id="15cfc-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="15cfc-117">حدد "نعم" في حقل "‏‫‏‫السماح بحالات المخزون المختلطة".</span><span class="sxs-lookup"><span data-stu-id="15cfc-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="15cfc-118">حدد "نعم" في حقل "تجاوز قواعد أيام الدفعة".</span><span class="sxs-lookup"><span data-stu-id="15cfc-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="15cfc-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="15cfc-120">قم بإعداد معلمات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="15cfc-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="15cfc-121">انتقل إلى إدارة المستودعات > إعداد‬ > محددات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="15cfc-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="15cfc-122">انقر فوق علامة التبويب "التعبئة".</span><span class="sxs-lookup"><span data-stu-id="15cfc-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="15cfc-123">في حقل "‏‫معرف ملف تعريف لموقع تعبئة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="15cfc-124">حدد ملف تعريف الموقع الذي تريد استخدامه للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="15cfc-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="15cfc-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="15cfc-126">إعداد أنواع الحاويات</span><span class="sxs-lookup"><span data-stu-id="15cfc-126">Set up container types</span></span>
1. <span data-ttu-id="15cfc-127">انتقل إلى إدارة المستودعات > إعداد > الحاويات > أنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="15cfc-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="15cfc-128">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="15cfc-128">Click New.</span></span>
    * <span data-ttu-id="15cfc-129">يمكنك تحديد أنواع حاويات لاستخدامها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-129">You can define the types of containers to use.</span></span> <span data-ttu-id="15cfc-130">يمكنك تحديد الأبعاد الفعلية للحاوية، بما في ذلك وزن الفارغ والحد الأقصى للوزن والحد الأقصى للحجم والطول والعرض والوزن.</span><span class="sxs-lookup"><span data-stu-id="15cfc-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="15cfc-131">تُعد السمات حقول مخصصة تسمح لك بإضافة أبعاد إضافية على نوع الحاوية.</span><span class="sxs-lookup"><span data-stu-id="15cfc-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="15cfc-132">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="15cfc-133">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="15cfc-134">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="15cfc-135">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="15cfc-136">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="15cfc-137">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="15cfc-138">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="15cfc-139">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="15cfc-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="15cfc-140">Click Save.</span></span>
12. <span data-ttu-id="15cfc-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="15cfc-142">إعداد ملفات تعريف التعبئة</span><span class="sxs-lookup"><span data-stu-id="15cfc-142">Set up packing profiles</span></span>
1. <span data-ttu-id="15cfc-143">انتقل إلى إدارة المستودعات > إعداد > التعبئة > ملفات تعريف التعبئة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="15cfc-144">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="15cfc-144">Click New.</span></span>
3. <span data-ttu-id="15cfc-145">في الحقل "معرف ملف تعريف التعبئة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="15cfc-146">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="15cfc-147">في الحقل "‏‫معرف ملف تعريف إقفال الحاوية "، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="15cfc-148">يُعد معرف ملف تعريف إقفال حاوية اختيارياً وملف تعريف الحاوية للإغلاق الافتراضي لملف تعريف التعبئة هذا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="15cfc-149">في الحقل "وضع معرف الحاوية"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="15cfc-150">يحدد هذا الخيار ما إذا كان معرف الحاوية سيتم إنشاءه تلقائيًا أم يدويًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="15cfc-151">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="15cfc-152">سيتم استخدام نوع الحاوية بشكل افتراضي عند إنشاء حاوية جديدة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="15cfc-153">حدد إنشاء تلقائي لحاوية في خانة اختيار إغلاق حاوية.</span><span class="sxs-lookup"><span data-stu-id="15cfc-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="15cfc-154">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="15cfc-154">Click Save.</span></span>
10. <span data-ttu-id="15cfc-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="15cfc-156">إعداد ملفات تعريف إقفال الحاوية</span><span class="sxs-lookup"><span data-stu-id="15cfc-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="15cfc-157">انتقل إلى إدارة المستودعات > إعداد > الحاويات > ملفات تعريف إقفال الحاوية‬.</span><span class="sxs-lookup"><span data-stu-id="15cfc-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="15cfc-158">تحدد ملفات تعريف إغلاق الحاوية الذي يحدث عند إغلاق حاوية.</span><span class="sxs-lookup"><span data-stu-id="15cfc-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="15cfc-159">يمكنك إعداد ملفات تعريف حاوية إغلاق متعددة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="15cfc-160">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="15cfc-160">Click New.</span></span>
3. <span data-ttu-id="15cfc-161">في الحقل "‏‫معرف ملف تعريف إقفال الحاوية "، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="15cfc-162">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="15cfc-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="15cfc-163">في الحقل "البيان"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="15cfc-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="15cfc-164">حدد ما إذا كان البيان سيحدث عند إغلاق الحاويات أو عند التأكد من الشحن.</span><span class="sxs-lookup"><span data-stu-id="15cfc-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="15cfc-165">لاحظ أن البيان يتطلب إدارة النقل.</span><span class="sxs-lookup"><span data-stu-id="15cfc-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="15cfc-166">يجب تنفذ البيان بمحركات النقل من أجل العمل.</span><span class="sxs-lookup"><span data-stu-id="15cfc-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="15cfc-167">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="15cfc-168">في حقل "‏‫‏‫الموقع الافتراضي للشحنة النهائية‬" أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="15cfc-169">سيكون هذا هو الموقع الذي سيتم نقل المنتجات بعد إغلاق الحاويات إليه.</span><span class="sxs-lookup"><span data-stu-id="15cfc-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="15cfc-170">يجب أن يحتوي هذا الموقع على ملف تعريف موقع محدد في معلمات المستودع.</span><span class="sxs-lookup"><span data-stu-id="15cfc-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="15cfc-171">في الحقل "وحدة الوزن"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15cfc-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="15cfc-172">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="15cfc-172">Click Save.</span></span>


