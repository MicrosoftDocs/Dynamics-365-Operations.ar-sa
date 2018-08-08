--- 
title: "تكوين المواقع في مستودع يدعم نظام إدارة المستودعات‬ (WMS)"
description: "يوضح هذا الدليل كيفية تكوين إعداد الموقع لمستودع جديد يدعم نظام إدارة المستودعات (WMS) (مستودع يستخدم عمليات إدارة مستودعات متقدمة)."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1b08cadc26f459bc197393e3794cb67bce6516d6
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="e8248-103">تكوين المواقع في مستودع يدعم نظام إدارة المستودعات‬ (WMS)</span><span class="sxs-lookup"><span data-stu-id="e8248-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8248-104">يوضح هذا الدليل كيفية تكوين إعداد الموقع لمستودع جديد يدعم نظام إدارة المستودعات (WMS) (مستودع يستخدم عمليات إدارة مستودعات متقدمة).</span><span class="sxs-lookup"><span data-stu-id="e8248-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="e8248-105">عادة ما يتم تنفيذ هذه العملية عن طريق مدير المستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="e8248-106">ويمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e8248-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e8248-107">يجب توفر موقع واحد على الأقل تم تكوينه كشرط مسبق.</span><span class="sxs-lookup"><span data-stu-id="e8248-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="e8248-108">إنشاء مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="e8248-108">Create a new warehouse</span></span>
1. <span data-ttu-id="e8248-109">انتقل إلى المستودعات.</span><span class="sxs-lookup"><span data-stu-id="e8248-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="e8248-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-110">Click New.</span></span>
3. <span data-ttu-id="e8248-111">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="e8248-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e8248-113">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="e8248-114">قم بتوسيع أو طي قسم المستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="e8248-115">قم بتعيين الخيار "استخدام عمليات إدارة المستودعات" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="e8248-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="e8248-116">يتيح لك هذا الإعداد تشغيل عمليات التخزين المتقدمة باستخدام عمل المستودع والأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="e8248-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="e8248-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="e8248-118">تحديد تنسيق للموقع</span><span class="sxs-lookup"><span data-stu-id="e8248-118">Define a location format</span></span>
1. <span data-ttu-id="e8248-119">انتقل إلى تنسيقات الموقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-119">Go to Location formats.</span></span>
    * <span data-ttu-id="e8248-120">تمثل تنسيقات الموقع نظام تسمية يُستخدم لإنشاء أسماء فريدة ومتناسقة لمواضع صناديق المواقع المختلفة المستخدمة داخل مستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="e8248-121">وقد يكون من المفيد استخدام الفواصل كجزء من تنسيق الموقع لتسهيل التعرف على مكونات الموقع مثل رقم الممر.</span><span class="sxs-lookup"><span data-stu-id="e8248-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="e8248-122">في هذا المثال، سنقوم بإنشاء اسم باستخدام أربعة مكونات.</span><span class="sxs-lookup"><span data-stu-id="e8248-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="e8248-123">على سبيل المثال، قد تكون هذه المكونات هي الممر والحامل والرف والصندوق.</span><span class="sxs-lookup"><span data-stu-id="e8248-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="e8248-124">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-124">Click New.</span></span>
3. <span data-ttu-id="e8248-125">في الحقل "تنسيق الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="e8248-126">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e8248-127">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="e8248-128">ويصف هذا ما يمثله المكون الأول من اسم الموقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="e8248-129">على سبيل المثال، قد يكون المكون الأول هو الممر.</span><span class="sxs-lookup"><span data-stu-id="e8248-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="e8248-130">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="e8248-131">ويحدد هذا عدد الأحرف التي يجب أن يتكون منها هذا الجزء من اسم الموقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="e8248-132">لاحظ أنه لا يمكن أن يتجاوز إجمالي عدد جميع المكونات في الاسم، بما في ذلك الفواصل، 10 حروف.</span><span class="sxs-lookup"><span data-stu-id="e8248-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="e8248-133">في الحقل "الفاصل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="e8248-134">ويحدد هذا الحرف أو الرمز الذي سيُستخدم من بين مكونات الاسم الأول والثاني.</span><span class="sxs-lookup"><span data-stu-id="e8248-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="e8248-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-135">Click New.</span></span>
9. <span data-ttu-id="e8248-136">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="e8248-137">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="e8248-138">في الحقل "الفاصل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="e8248-139">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="e8248-139">Click New.</span></span>
13. <span data-ttu-id="e8248-140">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="e8248-141">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="e8248-142">في الحقل "الفاصل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="e8248-143">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="e8248-143">Click New.</span></span>
17. <span data-ttu-id="e8248-144">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="e8248-145">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="e8248-146">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e8248-146">Click Save.</span></span>
20. <span data-ttu-id="e8248-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="e8248-148">تحديد أنواع الموقع</span><span class="sxs-lookup"><span data-stu-id="e8248-148">Define location types</span></span>
1. <span data-ttu-id="e8248-149">انتقل إلى أنواع المواقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-149">Go to Location types.</span></span>
    * <span data-ttu-id="e8248-150">يمكن استخدام أنواع المواقع كخيارات تصفية للتحكم في عمليات الإدارة المختلفة للمستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="e8248-151">وكحد أدنى، تحتاج إلى إنشاء أنواع مواقع الشحن مرحلية ونهائية لتحديد عملية إدارة المستودع الخارجي.</span><span class="sxs-lookup"><span data-stu-id="e8248-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="e8248-152">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-152">Click New.</span></span>
3. <span data-ttu-id="e8248-153">في الحقل "نوع الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="e8248-154">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e8248-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="e8248-156">تحديد ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="e8248-156">Define location profile</span></span>
1. <span data-ttu-id="e8248-157">انتقل إلى "ملفات تعريف المواقع".</span><span class="sxs-lookup"><span data-stu-id="e8248-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="e8248-158">يُعد تعريف ملفات تعريف الموقع مهم جداً.</span><span class="sxs-lookup"><span data-stu-id="e8248-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="e8248-159">يمكن هنا التحكم في قدرة المواقع المجمعة بالإضافة عن السياسات المتعلقة بالمخزون الذي يتم تخزينه وكيفية تخزينه.</span><span class="sxs-lookup"><span data-stu-id="e8248-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="e8248-160">يمكن استخدام ملفات تعريف المواقع كخيارات تصفية للتحكم في عمليات الإدارة المختلفة للمستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="e8248-161">وكحد أدنى، يجب إنشاء ملف تعريف موقع مستخدم لتمكين عمليات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="e8248-162">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-162">Click New.</span></span>
3. <span data-ttu-id="e8248-163">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="e8248-164">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e8248-165">في الحقل "تنسيق الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e8248-166">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e8248-167">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e8248-168">في الحقل "نوع الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e8248-169">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e8248-170">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e8248-171">قم بتحديد خانة الاختيار "السماح بحالات المخزون المختلطة" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="e8248-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="e8248-172">قم بتمكين هذا الخيار إذا كنت تريد السماح بقيم حالة المخزون في المواقع التي سيتم تجميعها حسب ملف تعريف الموقع هذا.</span><span class="sxs-lookup"><span data-stu-id="e8248-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="e8248-173">قم بتحديد خانة الاختيار "تجاوز قواعد تحديد أيام الدفعة" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="e8248-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="e8248-174">قم بتمكين هذا الخيار لتجاوز القاعدة التي تحدد عدد الأيام التي قد تتفاوت فيها تواريخ انتهاء صلاحية دفعات المخزون، للسماح بخلط دفعات المخزون التي لا تمتثل لهذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="e8248-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="e8248-175">قم بتحديد أو إلغاء تحديد خانة الاختيار ‏‫السماح بالجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="e8248-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="e8248-176">قم بتمكين هذا الخيار للسماح بمعالجة الجرد الدوري في جميع المواقع التي سيتم تجميعها حسب ملف تعريف الموقع هذا.</span><span class="sxs-lookup"><span data-stu-id="e8248-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="e8248-177">قم بتوسيع أو طي قسم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="e8248-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="e8248-178">تتيح لك علامة التبويب "الأبعاد" تحديد المعلمات والأساليب لتمكين إجراء حسابات دقيقة لقدرة الحمل في كل موقع من المواقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="e8248-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="e8248-180">تمكين معلمات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="e8248-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="e8248-181">انتقل إلى معلمات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="e8248-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="e8248-182">ولتتمكن من معالجة عمل المستودع، ستحتاج إلى تعيين المعلمات لملف تعريف موقع المستخدم ونوع موقع التخزين المؤقت ونوع موقع الشحن النهائي. وبمجرد انتهاء عملية الصادر في موقع الشحن النهائي الذي تحدده، سيتم تحديث الحركات الصادرة ذات الصلة إلى الحالة "منتقاة".</span><span class="sxs-lookup"><span data-stu-id="e8248-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="e8248-183">قم بتوسيع أو طي قسم ملفات تعريف المواقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="e8248-184">في الحقل "موقع المستخدم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e8248-185">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e8248-186">قم بتوسيع أو طي قسم أنواع المواقع‬.</span><span class="sxs-lookup"><span data-stu-id="e8248-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="e8248-187">في الحقل "نوع موقع التخزين المؤقت"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e8248-188">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e8248-189">في الحقل "نوع موقع الشحن النهائي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e8248-190">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e8248-191">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="e8248-192">تحديد مجموعات مناطق المستودعات</span><span class="sxs-lookup"><span data-stu-id="e8248-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="e8248-193">انتقل إلى مجموعات مناطق المستودعات.</span><span class="sxs-lookup"><span data-stu-id="e8248-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="e8248-194">يمكن استخدام مناطق المستودعات كعوامل تصفية لخيارات التحكم في عمليات الإدارة المختلفة للمستودعات.</span><span class="sxs-lookup"><span data-stu-id="e8248-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="e8248-195">تحتاجُ إلى إنشاء مجموعة مناطق قبل تحديد منطقة.</span><span class="sxs-lookup"><span data-stu-id="e8248-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="e8248-196">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-196">Click New.</span></span>
3. <span data-ttu-id="e8248-197">في الحقل "معرف مجموعة المناطق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="e8248-198">في الحقل "اسم مجموعة المناطق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="e8248-199">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="e8248-200">تحديد مناطق المستودعات</span><span class="sxs-lookup"><span data-stu-id="e8248-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="e8248-201">انتقل إلى المناطق.</span><span class="sxs-lookup"><span data-stu-id="e8248-201">Go to Zones.</span></span>
2. <span data-ttu-id="e8248-202">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-202">Click New.</span></span>
3. <span data-ttu-id="e8248-203">في الحقل "معرف المنطقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="e8248-204">في الحقل "اسم المنطقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="e8248-205">في الحقل "معرف مجموعة المناطق"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e8248-206">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e8248-207">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e8248-208">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="e8248-209">إنشاء المواقع باستخدام معالج إعداد المواقع</span><span class="sxs-lookup"><span data-stu-id="e8248-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="e8248-210">انتقل إلى معالج إعداد المواقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="e8248-211">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e8248-212">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e8248-213">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e8248-214">في الحقل "معرف المنطقة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e8248-215">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e8248-216">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e8248-217">في الحقل "معرف ملف تعريف الموقع، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e8248-218">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e8248-219">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e8248-220">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="e8248-221">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="e8248-222">يحدد الحقلان "من الرقم" و"إلى الرقم" عدد المواقع التي سيتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="e8248-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="e8248-223">على سبيل المثال، إذا قمت بتعيين الحقل "من الرقم 1" و"إلى الرقم 3" لجميع البنود الأربعة في تنسيق الموقع، سيتم إنشاء 81 موقع (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="e8248-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="e8248-224">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="e8248-225">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="e8248-226">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="e8248-227">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="e8248-228">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="e8248-229">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="e8248-230">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="e8248-231">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e8248-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="e8248-232">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="e8248-233">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="e8248-234">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="e8248-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="e8248-235">إنشاء المواقع يدويًا</span><span class="sxs-lookup"><span data-stu-id="e8248-235">Create locations manually</span></span>
1. <span data-ttu-id="e8248-236">انتقل إلى المواقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-236">Go to Locations.</span></span>
    * <span data-ttu-id="e8248-237">ويمكن إنشاء المواقع يدويًا داخل المستودعات بسهولة.</span><span class="sxs-lookup"><span data-stu-id="e8248-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="e8248-238">يُعد كل من "اسم الموقع" و"معرف ملف تعريف الموقع" حقلا إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="e8248-239">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-239">Click New.</span></span>
3. <span data-ttu-id="e8248-240">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="e8248-241">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="e8248-242">لاحظ أنك تقوم هنا بإنشاء موقع جديد، ولذلك تحتاجُ إلى اسم فريد جديد، بدلاً من تحديد اسم موجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e8248-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="e8248-243">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="e8248-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="e8248-245">تحديد فئات حجم العبوة</span><span class="sxs-lookup"><span data-stu-id="e8248-245">Define Pack size categories</span></span>
1. <span data-ttu-id="e8248-246">انتقل إلى فئات حجم العبوة.</span><span class="sxs-lookup"><span data-stu-id="e8248-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="e8248-247">يمكن استخدام فئات أحجام العبوات لتجميع العناصر التي لها أحجام عبوات مادية متشابهة.</span><span class="sxs-lookup"><span data-stu-id="e8248-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="e8248-248">في هذا المثال يمكن استخدام فئة حجم العبوة للتحكم في القدرة في مواقع الانتقاء داخل منطقة معينة من المستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="e8248-249">يُرجى ملاحظة أنه يجب تعيين معرف فئة حجم العبوة إلى كيان المنتج الذي تم إصداره ليتم استخدامه كجزء من معالجة حدود المخزون.</span><span class="sxs-lookup"><span data-stu-id="e8248-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="e8248-250">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-250">Click New.</span></span>
3. <span data-ttu-id="e8248-251">في الحقل "معرف فئة حجم العبوة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="e8248-252">في الحقل "اسم فئة حجم العبوة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="e8248-253">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="e8248-254">قم بتحديد حدود مخزون الموقع</span><span class="sxs-lookup"><span data-stu-id="e8248-254">Define location stocking limits</span></span>
1. <span data-ttu-id="e8248-255">انتقل إلى حدود المخزون للموقع.</span><span class="sxs-lookup"><span data-stu-id="e8248-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="e8248-256">تساعد حدود المخزون في الموقع على التأكد من عدم إنشاء العمل لطلب وضع ذلك المخزون في موقع الذي لا يملك القدرة المادية المطلوبة لحمل المخزون.</span><span class="sxs-lookup"><span data-stu-id="e8248-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="e8248-257">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-257">Click New.</span></span>
3. <span data-ttu-id="e8248-258">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="e8248-259">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="e8248-260">في الحقل "معرف فئة حجم العبوة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="e8248-261">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e8248-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="e8248-262">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e8248-262">Click Save.</span></span>
8. <span data-ttu-id="e8248-263">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="e8248-264">تحديد مواقع الانتقاء الثابتة</span><span class="sxs-lookup"><span data-stu-id="e8248-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="e8248-265">انتقل إلى المواقع الثابتة.</span><span class="sxs-lookup"><span data-stu-id="e8248-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="e8248-266">يمكنك تحديد المواقع التي سيتم استخدامها حسب المنتج أو حسب متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="e8248-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="e8248-267">من الممكن إنشاء مواقع ثابتة متعددة لنفس المنتج داخل نفس المستودع.</span><span class="sxs-lookup"><span data-stu-id="e8248-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="e8248-268">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e8248-268">Click New.</span></span>
3. <span data-ttu-id="e8248-269">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="e8248-270">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8248-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="e8248-271">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e8248-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e8248-272">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8248-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e8248-273">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8248-273">Close the page.</span></span>


