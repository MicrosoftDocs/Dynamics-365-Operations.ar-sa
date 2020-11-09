---
title: دمج الأصناف - استخدام الموقع
description: يوفر هذا الموضوع معلومات حول الوظيفة التي تسهل على مديري المستودعات عرض الاستخدام الحجمي للمواقع عبر المستودع وتصفيته. يمكن للمديرين تحديد المواقع وإنشاء عمل حركة المخزون مباشرة من صفحة دمج الأصناف لدمج الأصناف وبالتالي استخدام مساحة المستودع بشكل أفضل.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017174"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="5aadf-104">دمج الأصناف - استخدام الموقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aadf-105">يوفر هذا الموضوع معلومات حول الوظيفة التي تسهل على مديري المستودعات عرض الاستخدام الحجمي للمواقع عبر المستودع وتصفيته.</span><span class="sxs-lookup"><span data-stu-id="5aadf-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="5aadf-106">يمكن للمديرين تحديد المواقع وإنشاء عمل حركة المخزون مباشرة من صفحة **دمج الأصناف** لدمج الأصناف وبالتالي استخدام مساحة المستودع بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="5aadf-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="5aadf-107">تشغيل الميزات</span><span class="sxs-lookup"><span data-stu-id="5aadf-107">Turn on the features</span></span>

<span data-ttu-id="5aadf-108">قبل أن تتمكن من استخدام الميزات الموضحة في هذا الموضوع، يجب تشغيلها في النظام لديك.</span><span class="sxs-lookup"><span data-stu-id="5aadf-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="5aadf-109">يمكن للمسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزات وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="5aadf-110">شغَّل كل من الميزتين التاليتين بترتيب إدراجهما.</span><span class="sxs-lookup"><span data-stu-id="5aadf-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="5aadf-111">(كلتا الميزتان مخصصتان للوحدة النمطية **لإدارة المستودعات**.)</span><span class="sxs-lookup"><span data-stu-id="5aadf-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="5aadf-112">حالة موقع المستودع</span><span class="sxs-lookup"><span data-stu-id="5aadf-112">Warehouse location status</span></span>
2. <span data-ttu-id="5aadf-113">استخدام موقع دمج الأصناف</span><span class="sxs-lookup"><span data-stu-id="5aadf-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="5aadf-114">حالة موقع المستودع</span><span class="sxs-lookup"><span data-stu-id="5aadf-114">Warehouse location status</span></span>

<span data-ttu-id="5aadf-115">تضيف الميزة *حالة موقع المستودع* أربعة حقول جديدة إلى صفحة **المواقع** لتعقب المعلومات الإضافية حول حالة الموقع الحالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="5aadf-116">**رقم الصنف** – الصنف الموجود حاليًا في الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="5aadf-117">إذا كان الموقع يحتوي على عدة أصناف، فسيكون هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="5aadf-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="5aadf-118">**تاريخ ووقت النشاط الأخير** – الطابع الزمني لحركة المستودع التي تم إجراؤها مقابل الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="5aadf-119">**تاريخ التقادم** – التاريخ الذي تم فيه إحضار المخزون من الموقع إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="5aadf-120">يتم حساب هذا التاريخ استنادًا إلى تاريخ تقادم لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5aadf-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="5aadf-121">وعلى الرغم من دقة هذا التاريخ بالنسبة للمواقع التي يتم فيها تعقب لوحة الترخيص، فقد لا يكون دقيقًا للمواقع التي لا يتم فيها تعقب لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5aadf-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="5aadf-122">**حالة الموقع** – الحالة الخاصة بالموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="5aadf-123">القيم الأربع المتوفرة هي:</span><span class="sxs-lookup"><span data-stu-id="5aadf-123">Four values are available:</span></span>

    - <span data-ttu-id="5aadf-124">**غير محدد** – لا يتعقب ملف تعريف الموقع الحالة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="5aadf-125">بالتالي، تكون الحالة الحالية غير معروفة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="5aadf-126">**فارغ** – لا يوجد مخزون حاليًا في الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="5aadf-127">**انتقاء** – تم تنفيذ الحركات الصادرة مقابل الموقع بعد أن كان فارغًا آخر مرة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="5aadf-128">**التخزين** – تم تنفيذ الحركات الواردة فقط منذ أن كان الموقع فارغًا آخر مرة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="5aadf-129">تتيح هذه الحقول لمديري المستودعات الحصول على نظرة عامة أفضل حول حالة المواقع في المستودعات.</span><span class="sxs-lookup"><span data-stu-id="5aadf-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="5aadf-130">وهي أيضًا تسمح بالمزيد من إعداد التقارير والتصفية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="5aadf-131">إعداد دمج الأصناف واستخدام الموقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="5aadf-132">يوضح هذا القسم كيفية تجهيز النظام لاستخدام دمج الأصناف واستخدام الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="5aadf-133">تستخدم الإجراءات نماذج القيم من البيانات التجريبية القياسية.</span><span class="sxs-lookup"><span data-stu-id="5aadf-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="5aadf-134">إذا كنت تخطط للعمل من خلال سيناريو المثال المتوفر لاحقًا في هذا الموضوع، فحدد كيان **USMF** القانوني (الذي يحتوي على بيانات العرض التوضيحي القياسي)، وقم بإنشاء كل سجل موضح في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="5aadf-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="5aadf-135">إذا كنت لا تخطط للعمل في سيناريو المثال، فإنه يمكن اعتبار القيم المتوفرة هنا أمثلة لأنواع الإعداد التي يجب إكمالها لاستخدام الميزات.</span><span class="sxs-lookup"><span data-stu-id="5aadf-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="5aadf-136">المنتج الذي تم إصداره</span><span class="sxs-lookup"><span data-stu-id="5aadf-136">Released product</span></span>

1. <span data-ttu-id="5aadf-137">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5aadf-138">في الحقل **رقم الصنف** ، حدد *M9201* ثم افتح صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="5aadf-138">In the **Item number** field, select *M9201* , and open the details page.</span></span>
1. <span data-ttu-id="5aadf-139">في جزء الإجراءات، في علامة التبويب **إدارة المخزون** ، في مجموعة **المستودعات** ، حدد **الأبعاد الفعلية**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="5aadf-140">في صفحة **الأبعاد الفعلية** ، في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="5aadf-141">تتم إضافة سطر جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-141">A new line is added to the grid.</span></span> <span data-ttu-id="5aadf-142">ويتم تعيين الحقل **رقم الصنف** مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="5aadf-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="5aadf-143">في حقل **الوحدة** ، حدد *ea*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="5aadf-144">يتم تعيين الحقول المتبقية في السطر تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="5aadf-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="5aadf-145">حدد **حفظ** ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-145">Select **Save** , and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="5aadf-146">ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-146">Location profile</span></span>

1. <span data-ttu-id="5aadf-147">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="5aadf-148">في قائمه ملفات تعريف المواقع، حدد **FLOOR-05**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="5aadf-149">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5aadf-150">في علامة التبويب السريعة **عام** ، تأكد من تعيين كلا الخيارين التاليين على القيمة *نعم* :</span><span class="sxs-lookup"><span data-stu-id="5aadf-150">On the **General** FastTab, make sure that both the following options are set to *Yes* :</span></span>

    - <span data-ttu-id="5aadf-151">تمكين العنصر في الموقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-151">Enable item in location</span></span>
    - <span data-ttu-id="5aadf-152">تمكين حالة الموقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-152">Enable location status</span></span>

1. <span data-ttu-id="5aadf-153">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5aadf-154">في حالة تعيين الخيارين **تمكين العنصر في الموقع** و **تمكين حالة الموقع** بالفعل على *نعم* ، تخطى للأمام وصولاً إلى إرشادات إعداد علامة التبويب السريعة **الأبعاد** في الخطوة 10.</span><span class="sxs-lookup"><span data-stu-id="5aadf-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes* , skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="5aadf-155">في حالة عدم تعيين الخيارات بالفعل على القيمة *نعم* ، يجب تشغيل تدقيق التناسق لوحدة **إدارة المستودعات** النمطية بعد تعيين الخيارات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="5aadf-155">If the options weren't already set to *Yes* , you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="5aadf-156">انتقل في هذه الحالة إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="5aadf-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="5aadf-157">لتشغيل تدقيق التناسق، انتقل إلى **إدارة النظام \> المهام الدورية \> قاعدة البيانات \> تدقيق التناسق**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="5aadf-158">في مربع الحوار **تدقيق التناسق** ، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5aadf-159">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="5aadf-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="5aadf-160">**فحص/إصلاح:** *فحص*</span><span class="sxs-lookup"><span data-stu-id="5aadf-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="5aadf-161">**من تاريخ** – اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="5aadf-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="5aadf-162">**تدقيق تناسق حالة موقع المستودع:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="5aadf-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="5aadf-163">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="5aadf-164">ستتلقى إخطارًا عند اكتمال تدقيق التناسق.</span><span class="sxs-lookup"><span data-stu-id="5aadf-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="5aadf-165">افتح [مركز الإجراءات](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) لعرض الرسالة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="5aadf-166">حدد **تفاصيل الرسالة** لعرض التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="5aadf-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="5aadf-167">إذا كانت رسالة تدقيق التناسق هي، "تم العثور على معلومات حالة موقع غير صحيحة للموقع XXXX في المستودع XX"، يجب تشغيل تدقيق التناسق مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="5aadf-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="5aadf-168">في هذه المرة، عيِّن الحقل **تحقق/إصلاح** على *إصلاح الخطأ*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="5aadf-169">اعرض الرسائل للتأكد من عدم وجود أخطاء.</span><span class="sxs-lookup"><span data-stu-id="5aadf-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="5aadf-170">يجب الآن إنهاء إعداد ملف تعريف الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="5aadf-171">ارجع إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف المواقع** ، حدد ملف تعريف الموقع **FLOOR-05** ، ثم حدد في جزء الإجراءات **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles** , select location profile **FLOOR-05** , and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5aadf-172">في علامة التبويب السريعة **الأبعاد** ، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5aadf-173">**النسبة المئوية لاستخدام الحجم:** *100*</span><span class="sxs-lookup"><span data-stu-id="5aadf-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="5aadf-174">**‏‫الأسلوب الحجمي المستخدم لموقع المخزون:** *استخدام حجم الموقع*</span><span class="sxs-lookup"><span data-stu-id="5aadf-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="5aadf-175">**ارتفاع الموقع الفعلي:** *10*</span><span class="sxs-lookup"><span data-stu-id="5aadf-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="5aadf-176">**عرض الموقع الفعلي:** *10*</span><span class="sxs-lookup"><span data-stu-id="5aadf-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="5aadf-177">**عمق الموقع الفعلي:** *10*</span><span class="sxs-lookup"><span data-stu-id="5aadf-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="5aadf-178">**الحد الأقصى للوزن:** *100*</span><span class="sxs-lookup"><span data-stu-id="5aadf-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="5aadf-179">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="5aadf-180">أصناف قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="5aadf-180">Mobile device menu items</span></span>

1. <span data-ttu-id="5aadf-181">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5aadf-182">في جزء الإجراءات، حدد **جديد** لإنشاء عنصر قائمة للفرز.</span><span class="sxs-lookup"><span data-stu-id="5aadf-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="5aadf-183">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="5aadf-184">**اسم عنصر القائمة:** *تعديل في*</span><span class="sxs-lookup"><span data-stu-id="5aadf-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="5aadf-185">**العنوان:** *تعديل في*</span><span class="sxs-lookup"><span data-stu-id="5aadf-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="5aadf-186">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="5aadf-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="5aadf-187">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="5aadf-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="5aadf-188">في علامة التبويب السريعة **عام** ، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5aadf-189">**عملية إنشاء العمل:** *تعديل في*</span><span class="sxs-lookup"><span data-stu-id="5aadf-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="5aadf-190">**أنواع تعديل المخزون:** *تعديل في*</span><span class="sxs-lookup"><span data-stu-id="5aadf-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="5aadf-191">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="5aadf-192">قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="5aadf-192">Mobile device menu</span></span>

1. <span data-ttu-id="5aadf-193">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="5aadf-194">في قائمة القوائم، حدد **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="5aadf-195">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5aadf-196">في قائمة **القوائم المتوفرة وعناصر القائمة** ، ابحث عن عنصر القائمة **تعديل في** وحدده.</span><span class="sxs-lookup"><span data-stu-id="5aadf-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="5aadf-197">حدد زر السهم الأيمن لنقل **تعديل في** إلى قائمة **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="5aadf-198">بهذه الطريقة، تضيف عنصر القائمة الجديد إلى القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="5aadf-199">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="5aadf-200">أنواع الحركات</span><span class="sxs-lookup"><span data-stu-id="5aadf-200">Movement types</span></span>

1. <span data-ttu-id="5aadf-201">انتقل إلى **إدارة المخزون \> الإعداد \> المخزون \> أنواع الحركات‬**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="5aadf-202">في جزء الإجراءات، حدد **جديد** ، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-202">On the Action Pane, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="5aadf-203">**رمز نوع الحركة:** *دمج*</span><span class="sxs-lookup"><span data-stu-id="5aadf-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="5aadf-204">**الوصف:** *دمج المواقع*</span><span class="sxs-lookup"><span data-stu-id="5aadf-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="5aadf-205">**معرف فئة العمل:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="5aadf-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="5aadf-206">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="5aadf-207">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="5aadf-207">Example scenario</span></span>

<span data-ttu-id="5aadf-208">يستخدم السيناريو التالي تطبيق المستودع على جهاز محمول لإجراء *تعديل في* المخزون في موقعين بالمستودع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="5aadf-209">إضافة المخزون للمواقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-209">Add inventory to locations</span></span>

1. <span data-ttu-id="5aadf-210">سجل الدخول إلى الجهاز المحمول كمستخدم معين للمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="5aadf-211">انتقل إلى **المخزون \> تعديل في**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="5aadf-212">ستقوم الآن بإدخال تعديل الموقع الأول.</span><span class="sxs-lookup"><span data-stu-id="5aadf-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="5aadf-213">في مهمة **التعديل في** ، حدد الموقع المطلوب إجراء تعديلات في المخزون له.</span><span class="sxs-lookup"><span data-stu-id="5aadf-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="5aadf-214">في الحقل **LOC** ، حدد *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="5aadf-215">قم بتأكيد الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-215">Confirm the location.</span></span>
1. <span data-ttu-id="5aadf-216">انشئ معرف لوح الترخيص للصنف الذي ستتم إضافته إلى الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="5aadf-217">في الحقل **LP** ، أدخل *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="5aadf-218">قم بتأكيد لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5aadf-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="5aadf-219">أدخل الصنف الذي ستتم إضافته إلى لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5aadf-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="5aadf-220">في حقل **ITEM** ، أدخل *M9201*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="5aadf-221">قم بتأكيد الصنف.</span><span class="sxs-lookup"><span data-stu-id="5aadf-221">Confirm the item.</span></span>
1. <span data-ttu-id="5aadf-222">أدخل كمية الصنف الذي ستتم إضافته.</span><span class="sxs-lookup"><span data-stu-id="5aadf-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="5aadf-223">في الحقل **الكمية** ، أدخل *10*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="5aadf-224">قم بتأكيد الكمية.</span><span class="sxs-lookup"><span data-stu-id="5aadf-224">Confirm the quantity.</span></span>

    <span data-ttu-id="5aadf-225">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="5aadf-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="5aadf-226">ستقوم الآن بإدخال تعديل الموقع الثاني.</span><span class="sxs-lookup"><span data-stu-id="5aadf-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="5aadf-227">في مهمة **التعديل في** ، حدد الموقع المطلوب إجراء تعديلات في المخزون له.</span><span class="sxs-lookup"><span data-stu-id="5aadf-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="5aadf-228">في الحقل **LOC** ، حدد *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="5aadf-229">قم بتأكيد الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-229">Confirm the location.</span></span>
1. <span data-ttu-id="5aadf-230">انشئ معرف لوح الترخيص للصنف الذي ستتم إضافته إلى الموقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="5aadf-231">في الحقل **LP** ، أدخل *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="5aadf-232">قم بتأكيد لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5aadf-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="5aadf-233">أدخل الصنف الذي ستتم إضافته إلى لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5aadf-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="5aadf-234">في حقل **ITEM** ، أدخل *M9201*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="5aadf-235">قم بتأكيد الصنف.</span><span class="sxs-lookup"><span data-stu-id="5aadf-235">Confirm the item.</span></span>
1. <span data-ttu-id="5aadf-236">أدخل كمية الصنف الذي ستتم إضافته.</span><span class="sxs-lookup"><span data-stu-id="5aadf-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="5aadf-237">في الحقل **الكمية** ، أدخل *15*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="5aadf-238">قم بتأكيد الكمية.</span><span class="sxs-lookup"><span data-stu-id="5aadf-238">Confirm the quantity.</span></span>

    <span data-ttu-id="5aadf-239">سوف تستلم رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="5aadf-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="5aadf-240">حدد زر القائمة (أحيانًا يُشار إليه بهامبورجير أو الزر هامبورجير)، ثم حدد **إلغاء** لإنهاء مهمة **التعديل في**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="5aadf-241">دمج المواقع</span><span class="sxs-lookup"><span data-stu-id="5aadf-241">Consolidate locations</span></span>

1. <span data-ttu-id="5aadf-242">انتقل إلى **إدارة المستودعات \> المهام الدورية \> دمج الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="5aadf-243">في الرأس، حدد مستودعًا لإجراء الدمج به.</span><span class="sxs-lookup"><span data-stu-id="5aadf-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="5aadf-244">في حقل **المستودع** ، أدخل *51*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="5aadf-245">يظهر سجل لكل موقع يتم فيه تعديل الصنف *M9201*.</span><span class="sxs-lookup"><span data-stu-id="5aadf-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="5aadf-246">يُظهر عمود **النسبة المئوية للاستخدام** الاستخدام الحجمي لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="5aadf-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="5aadf-247">لدمج المخزون، حدد كافة المواقع التي يجب دمجها، ثم في جزء الإجراء، حدد **دمج المخزون**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="5aadf-248">في مربع الحوار **دمج المخزون** ، حدد الموقع ونوع الحركة التي يجب استخدامهما لإنشاء العمل لحركة المخزون.</span><span class="sxs-lookup"><span data-stu-id="5aadf-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="5aadf-249">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5aadf-249">Set the following values:</span></span>

    - <span data-ttu-id="5aadf-250">**الموقع:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="5aadf-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="5aadf-251">**رمز نوع الحركة:** *دمج*</span><span class="sxs-lookup"><span data-stu-id="5aadf-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="5aadf-252">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-252">Select **OK**.</span></span>
1. <span data-ttu-id="5aadf-253">تتلقى رسالة معلوماتية توضح عمل الحركة الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="5aadf-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="5aadf-254">دوِّن ملاحظة بمُعرف عمل الحركة.</span><span class="sxs-lookup"><span data-stu-id="5aadf-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="5aadf-255">عرض عمل الحركة</span><span class="sxs-lookup"><span data-stu-id="5aadf-255">View movement work</span></span>

1. <span data-ttu-id="5aadf-256">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="5aadf-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="5aadf-257">يعرض العمل الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="5aadf-257">View the work that was created.</span></span> <span data-ttu-id="5aadf-258">استخدم معرف عمل الحركة من دمج المخزون للتصفية أو البحث في شبكة العمل.</span><span class="sxs-lookup"><span data-stu-id="5aadf-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="5aadf-259">في هذا السيناريو، تم استخدام موقع موجود يحتوي على مخزون كموقع دمج المخزون.</span><span class="sxs-lookup"><span data-stu-id="5aadf-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="5aadf-260">لذا تم إنشاء معرف عمل واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="5aadf-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="5aadf-261">ينشئ النظام معرف عمل واحد لكل حركة يجب إكمالها.</span><span class="sxs-lookup"><span data-stu-id="5aadf-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="5aadf-262">بتحديد موقع يحتوي بالفعل على مخزون، يتم إنشاء معرف عمل واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="5aadf-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="5aadf-263">بتحديد موقع جديد، يتم إنشاء معرفي عمل.</span><span class="sxs-lookup"><span data-stu-id="5aadf-263">If you specify a new location, two work IDs are created.</span></span>
