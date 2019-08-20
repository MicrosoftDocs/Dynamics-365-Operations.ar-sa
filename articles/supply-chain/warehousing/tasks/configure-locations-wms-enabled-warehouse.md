---
title: تكوين المواقع في مستودع يدعم نظام إدارة المستودعات‬ (WMS)
description: يوضح هذا الدليل كيفية تكوين إعداد الموقع لمستودع جديد يدعم نظام إدارة المستودعات (WMS) (مستودع يستخدم عمليات إدارة مستودعات متقدمة).
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5df88f9ae7b07835db2911d55fae87f282826243
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847365"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="2ebb4-103">تكوين المواقع في مستودع يدعم نظام إدارة المستودعات‬ (WMS)</span><span class="sxs-lookup"><span data-stu-id="2ebb4-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ebb4-104">يوضح هذا الدليل كيفية تكوين إعداد الموقع لمستودع جديد يدعم نظام إدارة المستودعات (WMS) (مستودع يستخدم عمليات إدارة مستودعات متقدمة).</span><span class="sxs-lookup"><span data-stu-id="2ebb4-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="2ebb4-105">عادة ما يتم تنفيذ هذه العملية عن طريق مدير المستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="2ebb4-106">ويمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="2ebb4-107">يجب توفر موقع واحد على الأقل تم تكوينه كشرط مسبق.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="2ebb4-108">إنشاء مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="2ebb4-108">Create a new warehouse</span></span>
1. <span data-ttu-id="2ebb4-109">انتقل إلى المستودعات.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="2ebb4-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-110">Click New.</span></span>
3. <span data-ttu-id="2ebb4-111">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-113">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="2ebb4-114">قم بتوسيع أو طي قسم المستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="2ebb4-115">قم بتعيين الخيار "استخدام عمليات إدارة المستودعات" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="2ebb4-116">يتيح لك هذا الإعداد تشغيل عمليات التخزين المتقدمة باستخدام عمل المستودع والأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="2ebb4-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="2ebb4-118">تحديد تنسيق للموقع</span><span class="sxs-lookup"><span data-stu-id="2ebb4-118">Define a location format</span></span>
1. <span data-ttu-id="2ebb4-119">انتقل إلى تنسيقات الموقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-119">Go to Location formats.</span></span>
    * <span data-ttu-id="2ebb4-120">تمثل تنسيقات الموقع نظام تسمية يُستخدم لإنشاء أسماء فريدة ومتناسقة لمواضع صناديق المواقع المختلفة المستخدمة داخل مستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="2ebb4-121">وقد يكون من المفيد استخدام الفواصل كجزء من تنسيق الموقع لتسهيل التعرف على مكونات الموقع مثل رقم الممر.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="2ebb4-122">في هذا المثال، سنقوم بإنشاء اسم باستخدام أربعة مكونات.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="2ebb4-123">على سبيل المثال، قد تكون هذه المكونات هي الممر والحامل والرف والصندوق.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="2ebb4-124">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-124">Click New.</span></span>
3. <span data-ttu-id="2ebb4-125">في الحقل "تنسيق الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-126">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-127">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="2ebb4-128">ويصف هذا ما يمثله المكون الأول من اسم الموقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="2ebb4-129">على سبيل المثال، قد يكون المكون الأول هو الممر.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="2ebb4-130">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="2ebb4-131">ويحدد هذا عدد الأحرف التي يجب أن يتكون منها هذا الجزء من اسم الموقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="2ebb4-132">لاحظ أنه لا يمكن أن يتجاوز إجمالي عدد جميع المكونات في الاسم، بما في ذلك الفواصل، 10 حروف.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="2ebb4-133">في الحقل "الفاصل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="2ebb4-134">ويحدد هذا الحرف أو الرمز الذي سيُستخدم من بين مكونات الاسم الأول والثاني.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="2ebb4-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-135">Click New.</span></span>
9. <span data-ttu-id="2ebb4-136">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="2ebb4-137">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="2ebb4-138">في الحقل "الفاصل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="2ebb4-139">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-139">Click New.</span></span>
13. <span data-ttu-id="2ebb4-140">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="2ebb4-141">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="2ebb4-142">في الحقل "الفاصل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="2ebb4-143">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-143">Click New.</span></span>
17. <span data-ttu-id="2ebb4-144">في الحقل "وصف المقطع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="2ebb4-145">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="2ebb4-146">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-146">Click Save.</span></span>
20. <span data-ttu-id="2ebb4-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="2ebb4-148">تحديد أنواع الموقع</span><span class="sxs-lookup"><span data-stu-id="2ebb4-148">Define location types</span></span>
1. <span data-ttu-id="2ebb4-149">انتقل إلى أنواع المواقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-149">Go to Location types.</span></span>
    * <span data-ttu-id="2ebb4-150">يمكن استخدام أنواع المواقع كخيارات تصفية للتحكم في عمليات الإدارة المختلفة للمستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="2ebb4-151">وكحد أدنى، تحتاج إلى إنشاء أنواع مواقع الشحن مرحلية ونهائية لتحديد عملية إدارة المستودع الخارجي.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="2ebb4-152">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-152">Click New.</span></span>
3. <span data-ttu-id="2ebb4-153">في الحقل "نوع الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-154">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="2ebb4-156">تحديد ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="2ebb4-156">Define location profile</span></span>
1. <span data-ttu-id="2ebb4-157">انتقل إلى "ملفات تعريف المواقع".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="2ebb4-158">يُعد تعريف ملفات تعريف الموقع مهم جداً.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="2ebb4-159">يمكن هنا التحكم في قدرة المواقع المجمعة بالإضافة عن السياسات المتعلقة بالمخزون الذي يتم تخزينه وكيفية تخزينه.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="2ebb4-160">يمكن استخدام ملفات تعريف المواقع كخيارات تصفية للتحكم في عمليات الإدارة المختلفة للمستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="2ebb4-161">وكحد أدنى، يجب إنشاء ملف تعريف موقع مستخدم لتمكين عمليات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="2ebb4-162">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-162">Click New.</span></span>
3. <span data-ttu-id="2ebb4-163">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-164">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-165">في الحقل "تنسيق الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2ebb4-166">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2ebb4-167">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2ebb4-168">في الحقل "نوع الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2ebb4-169">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2ebb4-170">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2ebb4-171">قم بتحديد خانة الاختيار "السماح بحالات المخزون المختلطة" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="2ebb4-172">قم بتمكين هذا الخيار إذا كنت تريد السماح بقيم حالة المخزون في المواقع التي سيتم تجميعها حسب ملف تعريف الموقع هذا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="2ebb4-173">قم بتحديد خانة الاختيار "تجاوز قواعد تحديد أيام الدفعة" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="2ebb4-174">قم بتمكين هذا الخيار لتجاوز القاعدة التي تحدد عدد الأيام التي قد تتفاوت فيها تواريخ انتهاء صلاحية دفعات المخزون، للسماح بخلط دفعات المخزون التي لا تمتثل لهذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="2ebb4-175">قم بتحديد أو إلغاء تحديد خانة الاختيار ‏‫السماح بالجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="2ebb4-176">قم بتمكين هذا الخيار للسماح بمعالجة الجرد الدوري في جميع المواقع التي سيتم تجميعها حسب ملف تعريف الموقع هذا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="2ebb4-177">قم بتوسيع أو طي قسم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="2ebb4-178">تتيح لك علامة التبويب "الأبعاد" تحديد المعلمات والأساليب لتمكين إجراء حسابات دقيقة لقدرة الحمل في كل موقع من المواقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="2ebb4-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="2ebb4-180">تمكين معلمات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="2ebb4-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="2ebb4-181">انتقل إلى معلمات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="2ebb4-182">ولتتمكن من معالجة عمل المستودع، ستحتاج إلى تعيين المعلمات لملف تعريف موقع المستخدم ونوع موقع التخزين المؤقت ونوع موقع الشحن النهائي. وبمجرد انتهاء عملية الصادر في موقع الشحن النهائي الذي تحدده، سيتم تحديث الحركات الصادرة ذات الصلة إلى الحالة "منتقاة".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="2ebb4-183">قم بتوسيع أو طي قسم ملفات تعريف المواقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="2ebb4-184">في الحقل "موقع المستخدم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2ebb4-185">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2ebb4-186">قم بتوسيع أو طي قسم أنواع المواقع‬.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="2ebb4-187">في الحقل "نوع موقع التخزين المؤقت"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2ebb4-188">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2ebb4-189">في الحقل "نوع موقع الشحن النهائي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2ebb4-190">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2ebb4-191">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="2ebb4-192">تحديد مجموعات مناطق المستودعات</span><span class="sxs-lookup"><span data-stu-id="2ebb4-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="2ebb4-193">انتقل إلى مجموعات مناطق المستودعات.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="2ebb4-194">يمكن استخدام مناطق المستودعات كعوامل تصفية لخيارات التحكم في عمليات الإدارة المختلفة للمستودعات.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="2ebb4-195">تحتاجُ إلى إنشاء مجموعة مناطق قبل تحديد منطقة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="2ebb4-196">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-196">Click New.</span></span>
3. <span data-ttu-id="2ebb4-197">في الحقل "معرف مجموعة المناطق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-198">في الحقل "اسم مجموعة المناطق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-199">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="2ebb4-200">تحديد مناطق المستودعات</span><span class="sxs-lookup"><span data-stu-id="2ebb4-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="2ebb4-201">انتقل إلى المناطق.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-201">Go to Zones.</span></span>
2. <span data-ttu-id="2ebb4-202">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-202">Click New.</span></span>
3. <span data-ttu-id="2ebb4-203">في الحقل "معرف المنطقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-204">في الحقل "اسم المنطقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-205">في الحقل "معرف مجموعة المناطق"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2ebb4-206">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2ebb4-207">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2ebb4-208">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="2ebb4-209">إنشاء المواقع باستخدام معالج إعداد المواقع</span><span class="sxs-lookup"><span data-stu-id="2ebb4-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="2ebb4-210">انتقل إلى معالج إعداد المواقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="2ebb4-211">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2ebb4-212">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2ebb4-213">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2ebb4-214">في الحقل "معرف المنطقة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2ebb4-215">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2ebb4-216">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2ebb4-217">في الحقل "معرف ملف تعريف الموقع، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2ebb4-218">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2ebb4-219">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2ebb4-220">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="2ebb4-221">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="2ebb4-222">يحدد الحقلان "من الرقم" و"إلى الرقم" عدد المواقع التي سيتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="2ebb4-223">على سبيل المثال، إذا قمت بتعيين الحقل "من الرقم 1" و"إلى الرقم 3" لجميع البنود الأربعة في تنسيق الموقع، سيتم إنشاء 81 موقع (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="2ebb4-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="2ebb4-224">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="2ebb4-225">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2ebb4-226">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="2ebb4-227">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="2ebb4-228">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="2ebb4-229">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="2ebb4-230">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="2ebb4-231">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="2ebb4-232">في الحقل "من الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="2ebb4-233">في الحقل "إلى الرقم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="2ebb4-234">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="2ebb4-235">إنشاء المواقع يدويًا</span><span class="sxs-lookup"><span data-stu-id="2ebb4-235">Create locations manually</span></span>
1. <span data-ttu-id="2ebb4-236">انتقل إلى المواقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-236">Go to Locations.</span></span>
    * <span data-ttu-id="2ebb4-237">ويمكن إنشاء المواقع يدويًا داخل المستودعات بسهولة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="2ebb4-238">يُعد كل من "اسم الموقع" و"معرف ملف تعريف الموقع" حقلا إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="2ebb4-239">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-239">Click New.</span></span>
3. <span data-ttu-id="2ebb4-240">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-241">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="2ebb4-242">لاحظ أنك تقوم هنا بإنشاء موقع جديد، ولذلك تحتاجُ إلى اسم فريد جديد، بدلاً من تحديد اسم موجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="2ebb4-243">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="2ebb4-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="2ebb4-245">تحديد فئات حجم العبوة</span><span class="sxs-lookup"><span data-stu-id="2ebb4-245">Define Pack size categories</span></span>
1. <span data-ttu-id="2ebb4-246">انتقل إلى فئات حجم العبوة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="2ebb4-247">يمكن استخدام فئات أحجام العبوات لتجميع العناصر التي لها أحجام عبوات مادية متشابهة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="2ebb4-248">في هذا المثال يمكن استخدام فئة حجم العبوة للتحكم في القدرة في مواقع الانتقاء داخل منطقة معينة من المستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="2ebb4-249">يُرجى ملاحظة أنه يجب تعيين معرف فئة حجم العبوة إلى كيان المنتج الذي تم إصداره ليتم استخدامه كجزء من معالجة حدود المخزون.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="2ebb4-250">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-250">Click New.</span></span>
3. <span data-ttu-id="2ebb4-251">في الحقل "معرف فئة حجم العبوة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-252">في الحقل "اسم فئة حجم العبوة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-253">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="2ebb4-254">قم بتحديد حدود مخزون الموقع</span><span class="sxs-lookup"><span data-stu-id="2ebb4-254">Define location stocking limits</span></span>
1. <span data-ttu-id="2ebb4-255">انتقل إلى حدود المخزون للموقع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="2ebb4-256">تساعد حدود المخزون في الموقع على التأكد من عدم إنشاء العمل لطلب وضع ذلك المخزون في موقع الذي لا يملك القدرة المادية المطلوبة لحمل المخزون.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="2ebb4-257">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-257">Click New.</span></span>
3. <span data-ttu-id="2ebb4-258">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-259">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-260">في الحقل "معرف فئة حجم العبوة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="2ebb4-261">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="2ebb4-262">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-262">Click Save.</span></span>
8. <span data-ttu-id="2ebb4-263">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="2ebb4-264">تحديد مواقع الانتقاء الثابتة</span><span class="sxs-lookup"><span data-stu-id="2ebb4-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="2ebb4-265">انتقل إلى المواقع الثابتة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="2ebb4-266">يمكنك تحديد المواقع التي سيتم استخدامها حسب المنتج أو حسب متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="2ebb4-267">من الممكن إنشاء مواقع ثابتة متعددة لنفس المنتج داخل نفس المستودع.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="2ebb4-268">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ebb4-268">Click New.</span></span>
3. <span data-ttu-id="2ebb4-269">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="2ebb4-270">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="2ebb4-271">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2ebb4-272">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2ebb4-273">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2ebb4-273">Close the page.</span></span>

