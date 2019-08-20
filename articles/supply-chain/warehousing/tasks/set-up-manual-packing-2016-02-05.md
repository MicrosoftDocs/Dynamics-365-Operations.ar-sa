---
title: إعداد التعبئة اليدوية (فبراير 2016 & مايو 2016)
description: تسمح لك عملية التعبئة بالتحقق من المنتجات داخل الحاويات وتعبئتها.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30bbb404e624c33e047c5505c5b21565ed8cce10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847173"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="76780-103">إعداد التعبئة اليدوية (فبراير 2016 & مايو 2016)</span><span class="sxs-lookup"><span data-stu-id="76780-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76780-104">تسمح لك عملية التعبئة بالتحقق من المنتجات داخل الحاويات وتعبئتها.</span><span class="sxs-lookup"><span data-stu-id="76780-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="76780-105">في هذه العملية، يعمل عمال المستودع على انتقاء المنتجات من مواقع التخزين ونقلها إلى محطة تعبئة حيث يتحققون من كميات الأصناف وأنواعها ووضعها في حاويات مناسبة.</span><span class="sxs-lookup"><span data-stu-id="76780-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="76780-106">عند وجود حاوية معبأة تمامًا، فإنه يمكنك إغلاقها ونقلها إلى مساحات خارجية وتكون المنتجات جاهزة للشحن.</span><span class="sxs-lookup"><span data-stu-id="76780-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="76780-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="76780-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="76780-108">يتم استخدام هذا الإجراء لإصدارات فبراير 2016 ومايو 2016 من Dynamics 365 for Operations فقط.</span><span class="sxs-lookup"><span data-stu-id="76780-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="76780-109">إعداد ملفات تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="76780-109">Set up location profiles</span></span>
1. <span data-ttu-id="76780-110">انتقل إلى إدارة المستودعات‬ > إعداد > المستودع > ملفات تعريف الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="76780-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="76780-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="76780-111">Click New.</span></span>
    * <span data-ttu-id="76780-112">يتم استخدام ملف تعريف الموقع لمحطات التعبئة ويحتوي على معلومات وقواعد لموقع ما.</span><span class="sxs-lookup"><span data-stu-id="76780-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="76780-113">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="76780-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="76780-115">في الحقل "تنسيق الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="76780-116">في الحقل "نوع الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="76780-117">حدد "نعم" في حقل "‏‫‏‫السماح بالأصناف المختلطة".</span><span class="sxs-lookup"><span data-stu-id="76780-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="76780-118">حدد "نعم" في حقل "‏‫‏‫السماح بحالات المخزون المختلطة".</span><span class="sxs-lookup"><span data-stu-id="76780-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="76780-119">حدد "نعم" في حقل "تجاوز قواعد أيام الدفعة".</span><span class="sxs-lookup"><span data-stu-id="76780-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="76780-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="76780-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="76780-121">قم بإعداد معلمات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="76780-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="76780-122">انتقل إلى إدارة المستودعات > إعداد‬ > محددات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="76780-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="76780-123">انقر فوق علامة التبويب "التعبئة".</span><span class="sxs-lookup"><span data-stu-id="76780-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="76780-124">في حقل "‏‫معرف ملف تعريف لموقع تعبئة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="76780-125">حدد ملف تعريف الموقع الذي تريد استخدامه للانتقاء.</span><span class="sxs-lookup"><span data-stu-id="76780-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="76780-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="76780-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="76780-127">إعداد أنواع الحاويات</span><span class="sxs-lookup"><span data-stu-id="76780-127">Set up container types</span></span>
1. <span data-ttu-id="76780-128">انتقل إلى إدارة المستودعات > إعداد > الحاويات > أنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="76780-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="76780-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="76780-129">Click New.</span></span>
    * <span data-ttu-id="76780-130">يمكنك تحديد أنواع حاويات لاستخدامها.</span><span class="sxs-lookup"><span data-stu-id="76780-130">You can define the types of containers to use.</span></span> <span data-ttu-id="76780-131">يمكنك تحديد الأبعاد الفعلية للحاوية، بما في ذلك وزن الفارغ والحد الأقصى للوزن والحد الأقصى للحجم والطول والعرض والوزن.</span><span class="sxs-lookup"><span data-stu-id="76780-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="76780-132">تُعد السمات حقول مخصصة تسمح لك بإضافة أبعاد إضافية على نوع الحاوية.</span><span class="sxs-lookup"><span data-stu-id="76780-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="76780-133">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="76780-134">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76780-135">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="76780-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="76780-136">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="76780-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="76780-137">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="76780-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="76780-138">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="76780-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="76780-139">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="76780-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="76780-140">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="76780-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="76780-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="76780-141">Click Save.</span></span>
12. <span data-ttu-id="76780-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="76780-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="76780-143">إعداد ملفات تعريف التعبئة</span><span class="sxs-lookup"><span data-stu-id="76780-143">Set up packing profiles</span></span>
1. <span data-ttu-id="76780-144">انتقل إلى إدارة المستودعات > إعداد > التعبئة > ملفات تعريف التعبئة.</span><span class="sxs-lookup"><span data-stu-id="76780-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="76780-145">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="76780-145">Click New.</span></span>
3. <span data-ttu-id="76780-146">في الحقل "معرف ملف تعريف التعبئة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="76780-147">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76780-148">في الحقل "‏‫معرف ملف تعريف إقفال الحاوية "، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="76780-149">يُعد معرف ملف تعريف إقفال حاوية اختيارياً وملف تعريف الحاوية للإغلاق الافتراضي لملف تعريف التعبئة هذا.</span><span class="sxs-lookup"><span data-stu-id="76780-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="76780-150">في الحقل "وضع معرف الحاوية"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="76780-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="76780-151">يحدد هذا الخيار ما إذا كان معرف الحاوية سيتم إنشاءه تلقائيًا أم يدويًا.</span><span class="sxs-lookup"><span data-stu-id="76780-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="76780-152">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="76780-153">سيتم استخدام نوع الحاوية بشكل افتراضي عند إنشاء حاوية جديدة.</span><span class="sxs-lookup"><span data-stu-id="76780-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="76780-154">حدد إنشاء تلقائي لحاوية في خانة اختيار إغلاق حاوية.</span><span class="sxs-lookup"><span data-stu-id="76780-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="76780-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="76780-155">Click Save.</span></span>
10. <span data-ttu-id="76780-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="76780-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="76780-157">إعداد ملفات تعريف إقفال الحاوية</span><span class="sxs-lookup"><span data-stu-id="76780-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="76780-158">انتقل إلى إدارة المستودعات > إعداد > الحاويات > ملفات تعريف إقفال الحاوية‬.</span><span class="sxs-lookup"><span data-stu-id="76780-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="76780-159">تحدد ملفات تعريف إغلاق الحاوية الذي يحدث عند إغلاق حاوية.</span><span class="sxs-lookup"><span data-stu-id="76780-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="76780-160">يمكنك إعداد ملفات تعريف حاوية إغلاق متعددة.</span><span class="sxs-lookup"><span data-stu-id="76780-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="76780-161">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="76780-161">Click New.</span></span>
3. <span data-ttu-id="76780-162">في الحقل "‏‫معرف ملف تعريف إقفال الحاوية "، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="76780-163">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="76780-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76780-164">في الحقل "البيان"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="76780-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="76780-165">حدد ما إذا كان البيان سيحدث عند إغلاق الحاويات أو عند التأكد من الشحن.</span><span class="sxs-lookup"><span data-stu-id="76780-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="76780-166">لاحظ أن البيان يتطلب إدارة النقل.</span><span class="sxs-lookup"><span data-stu-id="76780-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="76780-167">يجب تنفذ البيان بمحركات النقل من أجل العمل.</span><span class="sxs-lookup"><span data-stu-id="76780-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="76780-168">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="76780-169">في حقل "‏‫‏‫الموقع الافتراضي للشحنة النهائية‬" أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="76780-170">سيكون هذا هو الموقع الذي سيتم نقل المنتجات بعد إغلاق الحاويات إليه.</span><span class="sxs-lookup"><span data-stu-id="76780-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="76780-171">يجب أن يحتوي هذا الموقع على ملف تعريف موقع محدد في معلمات المستودع.</span><span class="sxs-lookup"><span data-stu-id="76780-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="76780-172">في الحقل "وحدة الوزن"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="76780-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="76780-173">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="76780-173">Click Save.</span></span>

