---
title: وضع على الحائط - وضع في المتجر
description: يوفر هذا الموضوع معلومات حول وظيفة وضع على الحائط - وضع في المتجر. تتيح لك هذه الوظيفة معالجة السيناريوهات التي يجب فيها تجميع منتج في منطقة مرحلية للتحزيم المسبق، استنادًا إلى معايير يمكن تكوينها. وساعد على تقليل وقت الانتقاء نظرًا لإتاحة الانتقاء إلى لوحة ترخيص هدف واحدة كما يمكنها استخدام المزيد من أماكن الوضع أكثر من انتقاء نظام المجموعة.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cf34a61d0b3f784b5a424473588d05bf8703635c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823277"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="24aa3-105">وضع على الحائط - وضع في المتجر</span><span class="sxs-lookup"><span data-stu-id="24aa3-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24aa3-106">تتيح لك الوظيفة *وضع على الحائط - وضع في المتجر* معالجة السيناريوهات التي يجب فيها تجميع منتج في منطقة مرحلية للتحزيم المسبق، استنادًا إلى معايير يمكن تكوينها.</span><span class="sxs-lookup"><span data-stu-id="24aa3-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="24aa3-107">ونظرًا لأن هذه الوظيفة تتيح الانتقاء إلى لوحة ترخيص هدف واحدة ويمكنكها استخدام المزيد من أماكن الوضع أكثر من انتقاء نظام المجموعة، فإن الشركات التي تقوم بالشحن إلى المتاجر أو تتعامل مع أصناف صغيرة ستستفيد من خفض وقت الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="24aa3-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="24aa3-108">يوجه سير عمل هذه الوظيفة المنتج المنتقى إلى موقع فرز لتوزيعه في أنواع مختلفة من الحاويات.</span><span class="sxs-lookup"><span data-stu-id="24aa3-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="24aa3-109">وبشكل عام، يتضمن كل موقع من مواقع الفرز عدة مواضع للفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="24aa3-110">يتم تعيين كل موضع فرز وفقًا للمعايير التي تعينها إجراءات العمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="24aa3-111">المعايير النموذجية هي الوجهة الأخيرة أو الشحنة أو الحمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="24aa3-112">بعد وصول منتج، يتم توزيعه لكل موضع فرز استنادًا إلى الكمية المقترنة بالأمر أو الوجهة أو الشحنة أو الحمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="24aa3-113">عندما تكون الحاوية كامله أو مكتملة، يتم نقلها إلى موقع مرحلي أو موقع شحن لإجراء مزيد من المعالجات، وذلك وفقًا لإجراءات العمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="24aa3-114">يُشار إلى وظيفة التخزين هذه أيضًا بواسطة أسماء أخرى، مثل الفتح من "التجزئة" و "الفصل".</span><span class="sxs-lookup"><span data-stu-id="24aa3-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="24aa3-115">تشغيل ميزة الفرز الخارجي</span><span class="sxs-lookup"><span data-stu-id="24aa3-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="24aa3-116">قبل أن تتمكن من استخدام الوظيفة *وضع على الحائط - وضع في المتجر*، يجب تشغيل ميزة *الفرز الخارجي* في النظام لديك.</span><span class="sxs-lookup"><span data-stu-id="24aa3-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="24aa3-117">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="24aa3-118">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="24aa3-119">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="24aa3-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="24aa3-120">**اسم الميزة:** *الفرز الخارجي*</span><span class="sxs-lookup"><span data-stu-id="24aa3-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="24aa3-121">يمكن استخدام ميزة *الفرز الخارجي* جنبًا إلى جنب مع الميزة *كود خطوة الموجة على مستوى المؤسسة* إذا كانت قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="24aa3-122">يجب أيضًا تشغيل هذه الميزة إذا كنت ستستخدم الأكواد المحددة مسبقًا والتي تم إعدادها في أكواد خطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="24aa3-123">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="24aa3-124">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="24aa3-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="24aa3-125">**اسم الموجة:** *كود خطوة الموجة على مستوى المؤسسة*</span><span class="sxs-lookup"><span data-stu-id="24aa3-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="24aa3-126">الإعداد</span><span class="sxs-lookup"><span data-stu-id="24aa3-126">Setup</span></span>

<span data-ttu-id="24aa3-127">بالنسبة لهذا العرض التوضيحي، يتم استخدام بيانات Contoso القياسية والمستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="24aa3-128">كما يتم أيضًا استخدام بعض الإضافات الموضحة لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="24aa3-129">نوع الموقع</span><span class="sxs-lookup"><span data-stu-id="24aa3-129">Location type</span></span>

1. <span data-ttu-id="24aa3-130">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> أنواع المواقع**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="24aa3-131">في جزء الإجراءات، حدد **جديد** لإنشاء نوع موقع للفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="24aa3-132">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-132">Set the following values:</span></span>

    - <span data-ttu-id="24aa3-133">**نوع الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="24aa3-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="24aa3-134">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="24aa3-135">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="24aa3-136">محددات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="24aa3-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="24aa3-137">انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="24aa3-138">في علامة التبويب **عام**، في علامة التبويب السريعة **أنواع المواقع**، في الحقل **نوع موقع الفرز**، أدخل *SORT*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="24aa3-139">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="24aa3-140">ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="24aa3-140">Location profile</span></span>

1. <span data-ttu-id="24aa3-141">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="24aa3-142">في جزء الإجراءات، حدد **جديد** لإنشاء ملف تعريف موقع لموقع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="24aa3-143">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="24aa3-144">**معرف ملف تعريف الموقع:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-145">**الاسم:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="24aa3-146">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="24aa3-147">**تنسيق الموقع:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="24aa3-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="24aa3-148">**نوع الموقع:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="24aa3-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="24aa3-149">**استخدام تعقب لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="24aa3-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="24aa3-150">**السماح بالأصناف المختلطة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="24aa3-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="24aa3-151">**السماح بحالات المخزون المختلطة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="24aa3-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="24aa3-152">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="24aa3-153">المواقع</span><span class="sxs-lookup"><span data-stu-id="24aa3-153">Locations</span></span>

1. <span data-ttu-id="24aa3-154">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="24aa3-155">امسح خانة الاختيار **إنشاء أرقام شيكات للموقع**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="24aa3-156">في جزء الإجراءات، حدد **جديد**، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="24aa3-157">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="24aa3-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="24aa3-158">**الموقع:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-159">**معرف ملف تعريف الموقع:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="24aa3-160">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="24aa3-161">ملف تعريف التعبئة</span><span class="sxs-lookup"><span data-stu-id="24aa3-161">Packing profiles</span></span>

1. <span data-ttu-id="24aa3-162">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> ملفات تعريف التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="24aa3-163">في جزء الإجراءات، حدد **جديد**، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="24aa3-164">**معرف ملف تعريف التعبئة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-165">**الوصف:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-166">**سياسة تعبئة الحاوية:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="24aa3-167">**وضع معرف الحاوية:** *تلقائي*</span><span class="sxs-lookup"><span data-stu-id="24aa3-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="24aa3-168">**نوع الحاوية:** *PALLET 48X48*</span><span class="sxs-lookup"><span data-stu-id="24aa3-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="24aa3-169">**إنشاء حاوية تلقائيًا عند إغلاق الحاوية:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="24aa3-170">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="24aa3-171">رموز خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="24aa3-171">Wave step codes</span></span>

<span data-ttu-id="24aa3-172">عند تشغيل الميزة *كود خطوة الموجة على مستوى المؤسسة*، قم بإعداد الكود التالي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="24aa3-173">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> أكواد خطوة الموجة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="24aa3-174">في جزء الإجراءات، حدد **جديد**، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="24aa3-175">**كود خطوة الموجة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-176">**وصف خطوة الموجة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-177">**نوع خطوة الموجة:** *قالب فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="24aa3-178">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="24aa3-179">قالب الفرز الصادر</span><span class="sxs-lookup"><span data-stu-id="24aa3-179">Outbound sorting template</span></span>

<span data-ttu-id="24aa3-180">يتحكم قالب الفرز فيما إذا كان سيتم إنشاء مواضع الفرز وتحديد المعايير المستخدمة والسمات الأخرى لعملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="24aa3-181">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> قالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="24aa3-182">في جزء الإجراءات، حدد **جديد** لإنشاء قالب فرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="24aa3-183">في رأس القالب الجديد، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="24aa3-184">**معرف قالب الفرز الخارجي:** *فرز الموجة*</span><span class="sxs-lookup"><span data-stu-id="24aa3-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="24aa3-185">**لوصف:** *فرز الموجة*</span><span class="sxs-lookup"><span data-stu-id="24aa3-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="24aa3-186">**نوع قالب الفرز:** *طلب الموجة*</span><span class="sxs-lookup"><span data-stu-id="24aa3-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="24aa3-187">يحدد هذا الحقل العملية التي يتم استخدام قالب الفرز لها.</span><span class="sxs-lookup"><span data-stu-id="24aa3-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="24aa3-188">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-188">The following values are available:</span></span>

        - <span data-ttu-id="24aa3-189">**طلب الموجة** – يتم استخدام قالب الفرز للعملية *وضع على الحائط*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="24aa3-190">يُستخدم نوع القاالب هذا لتجاوز محطة التعبئة ومعالجة المخزون الوارد من الموجة مباشرة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="24aa3-191">لا يمكن استخدام هذا النوع إلا في حالة تضمين طريقة معالجة موجة **الفرز** في قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="24aa3-192">**الحاوية** – يتم استخدام قالب الفرز لمعالجة *بناء البالتة بعد التعبئة*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="24aa3-193">يُستخدم هذا القالب لمعالجة الحاويات المغلقة في محطة التعبئة والتي يجب فرزها إلى بالتات.</span><span class="sxs-lookup"><span data-stu-id="24aa3-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="24aa3-194">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="24aa3-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="24aa3-195">**الموقع:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="24aa3-196">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="24aa3-197">**التحقق من الفرز:** *مسح الموضع*</span><span class="sxs-lookup"><span data-stu-id="24aa3-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="24aa3-198">يحدد هذا الحقل التحقق من الصحة المطلوب أثناء الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="24aa3-199">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-199">The following values are available:</span></span>

        - <span data-ttu-id="24aa3-200">بلا‬‬</span><span class="sxs-lookup"><span data-stu-id="24aa3-200">None</span></span>
        - <span data-ttu-id="24aa3-201">مسح لوحة الترخيص ضوئيًا</span><span class="sxs-lookup"><span data-stu-id="24aa3-201">License plate scan</span></span>
        - <span data-ttu-id="24aa3-202">مسح منصب</span><span class="sxs-lookup"><span data-stu-id="24aa3-202">Position scan</span></span>

    - <span data-ttu-id="24aa3-203">**إنشاء عمل عند إغلاق الموضع:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="24aa3-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="24aa3-204">عند تحديد هذا الخيار على القيمة *نعم*، سيتم إنشاء عمل عند إغلاق الموضع لنقل المخزون إلى موقع الشحن النهائي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="24aa3-205">وعند التعيين على القيمة *لا*، سيتم انتقاء المخزون إلى الأمر فورًا عند إغلاق الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="24aa3-206">**تعيين الموضع:** *يدويًا*</span><span class="sxs-lookup"><span data-stu-id="24aa3-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="24aa3-207">يحدد هذا الحقل نوع تعيين الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="24aa3-208">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-208">The following values are available:</span></span>

        - <span data-ttu-id="24aa3-209">**يدويًا** – يجب على المستخدم الإشارة دائمًا إلى الموضع الذي ينبغي فرز المخزون به.</span><span class="sxs-lookup"><span data-stu-id="24aa3-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="24aa3-210">**تلقائيًا** – سيرشد النظام المخزون تلقائيًا إلى موضع إذا أمكن، استنادًا إلى فواصل قالب الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="24aa3-211">**تعيين معايير موضع الفرز:** *استخدام الموضع الفارغ فقط*</span><span class="sxs-lookup"><span data-stu-id="24aa3-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="24aa3-212">يتحكم هذا الحقل فيما إذا كان ستتم مراعاة المخزون الموجود بالفعل في مواضع الفرز عند تعيين موضع للطلب.</span><span class="sxs-lookup"><span data-stu-id="24aa3-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="24aa3-213">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-213">The following values are available:</span></span>

        - <span data-ttu-id="24aa3-214">**استخدام الموضع الفارغ فقط** – ستتم مراعاة المواضع التي لديها بالفعل مخزون مقترن بها</span><span class="sxs-lookup"><span data-stu-id="24aa3-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="24aa3-215">**افتراض الموضع فارغ** – سيتم تجاهل أي مخزون موجود بالفعل في الموضع أثناء التعيين.</span><span class="sxs-lookup"><span data-stu-id="24aa3-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="24aa3-216">سيتم استخدام كافة المواضع المتاحة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-216">All available positions will be used.</span></span>

    - <span data-ttu-id="24aa3-217">**كود خطوة الموجة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="24aa3-218">إذا كانت الميزة *كود خطوة الموجة على مستوى المؤسسة* قيد التشغيل، يجب أيضًا إعداد كود خطوة موجة *الفرز* في أكواد خطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="24aa3-219">**الإغلاق التلقائي لموضع الفرز:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="24aa3-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="24aa3-220">عند تعيين هذا الخيار على *نعم*، يتم إغلاق موضع الفرز تلقائيًا عند اكتمال كافة الأعمال الواردة إلى الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="24aa3-221">**عدد مواضع الفرز:** *3*</span><span class="sxs-lookup"><span data-stu-id="24aa3-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="24aa3-222">يحدد هذا الحقل الحد الأقصى لعدد مواضع الفرز التي سينشئها النظام.</span><span class="sxs-lookup"><span data-stu-id="24aa3-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="24aa3-223">**بادئة موضع الفرز:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="24aa3-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="24aa3-224">يحدد هذا الحقل البادئة التي يعينها النظام قبل رقم الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="24aa3-225">**تعبئة موضع الفرز تلقائيًا:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="24aa3-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="24aa3-226">عند تعيين هذا الخيار على *نعم*، تتم تعبئة المخزون الموجود في موضع الفرز بإحدي الحاويات عند إغلاق الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="24aa3-227">**معرف ملف تعريف التعبئة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="24aa3-228">يحدد هذا الحقل ملف تعريف التعبئة الذي سيتم استخدامه عند تعبئة موضع الفرز في إحدي الحاويات.</span><span class="sxs-lookup"><span data-stu-id="24aa3-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="24aa3-229">في جزء الإجراءات، حدد **تحرير الاستعلام** لتحديد المعايير المستخدمة لقالب الفرز الحالي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="24aa3-230">في مربع حوار الاستعلام، ضمن علامة التبويب **الفرز**، حدد **جديد** لإضافة سطر، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="24aa3-231">**الجدول:** *تفاصيل الحمل*</span><span class="sxs-lookup"><span data-stu-id="24aa3-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="24aa3-232">**الجدول المشتق:** *تفاصيل الحمل*</span><span class="sxs-lookup"><span data-stu-id="24aa3-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="24aa3-233">**الحقل:** *معرف الشحنة*</span><span class="sxs-lookup"><span data-stu-id="24aa3-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="24aa3-234">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="24aa3-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="24aa3-235">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-235">Select **OK**.</span></span>
1. <span data-ttu-id="24aa3-236">قد تتلقى الرسالة التالية: "ستتم إعادة تعيين التجميع، هل تريد المتابعة؟"</span><span class="sxs-lookup"><span data-stu-id="24aa3-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="24aa3-237">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-237">Select **Yes**.</span></span>

    <span data-ttu-id="24aa3-238">يصبح الزر **فواصل قوالب الفرز الخارجي** في جزء الإجراءات متاحًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="24aa3-239">في جزء الإجراءات، حدد **فواصل قوالب الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="24aa3-240">حدد خانة الاختيار **تجميع حسب الحقل** للتجميع حسب معرفة الشحنة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="24aa3-241">يؤدي هذا الإعداد إلى إنشاء موضع فرز واحد لكل شحنة تمثل حاية في الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="24aa3-242">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="24aa3-243">طرق معالجة الموجة</span><span class="sxs-lookup"><span data-stu-id="24aa3-243">Wave process methods</span></span>

1. <span data-ttu-id="24aa3-244">انتقل إلى **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملي الموجة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="24aa3-245">في جزء الإجراءات، حدد **طرق إعادة الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="24aa3-246">يتم إضافة أسلوب **الفرز** إلى قائمة الأساليب المتوفرة، ويتم تحديد نوع قالب موجة *الشحن* له.</span><span class="sxs-lookup"><span data-stu-id="24aa3-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="24aa3-247">قوالب الموجة</span><span class="sxs-lookup"><span data-stu-id="24aa3-247">Wave templates</span></span>

<span data-ttu-id="24aa3-248">تحرير قالب الموجة المستخدم لفرز طلب الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="24aa3-249">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="24aa3-250">في الحقل **نوع قالب الموجة**، حدد *الشحن*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="24aa3-251">حدد القالب **افتراضي الشحن 62** الموجود.</span><span class="sxs-lookup"><span data-stu-id="24aa3-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="24aa3-252">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="24aa3-253">في علامة التبويب السريعة **عام**، قم بإجراء التغييرات التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="24aa3-254">قم بتعيين الخيار **معالجة الموجة عند الإصدار إلى المستودع** إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="24aa3-255">عيّن الخيار **التعيين إلى الموجات المفتوحة** على *نعم*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="24aa3-256">في علامة التبويب السريعة **الأساليب**، قم بإعداد أسلوب **الفرز**:</span><span class="sxs-lookup"><span data-stu-id="24aa3-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="24aa3-257">في شبكة **الأساليب المتبقية**، حدد **الفرز**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="24aa3-258">حدد زر السهم الأيمن لنقل **الأسلوب** إلى شبكة **الأساليب المحددة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="24aa3-259">في شبكة **الأساليب المحددة**، حدد **الفرز**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="24aa3-260">عيِّن الحقل **رمز خطوة الموجة** على *الفرز*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="24aa3-261">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="24aa3-262">أصناف قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="24aa3-262">Mobile device menu items</span></span>

1. <span data-ttu-id="24aa3-263">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="24aa3-264">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24aa3-265">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="24aa3-266">**اسم عنصر القائمة:** *فرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-267">**العنوان:** *الفرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="24aa3-268">**الوضع:** *غير مباشر*</span><span class="sxs-lookup"><span data-stu-id="24aa3-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="24aa3-269">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="24aa3-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="24aa3-270">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="24aa3-271">**رمز النشاط:** *فرز خارجي*</span><span class="sxs-lookup"><span data-stu-id="24aa3-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="24aa3-272">**استخدام دليل المعالجة:** *نعم* (القيمة الافتراضية)</span><span class="sxs-lookup"><span data-stu-id="24aa3-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="24aa3-273">**معرف قالب الفرز الخارجي:** *فرز الموجة*</span><span class="sxs-lookup"><span data-stu-id="24aa3-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="24aa3-274">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="24aa3-275">قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="24aa3-275">Mobile device menu</span></span>

1. <span data-ttu-id="24aa3-276">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="24aa3-277">في قائمة القوائم، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="24aa3-278">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="24aa3-279">في شبكة **القوائم المتوفرة وعناصر القائمة**، ابحث عن عنصر القائمة **الفرز** الذي أنشأته وحدده.</span><span class="sxs-lookup"><span data-stu-id="24aa3-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="24aa3-280">حدد زر السهم الأيمن لنقل **الفرز** إلى شبكة **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="24aa3-281">بهذه الطريقة، تضيف عنصر القائمة الجديد إلى القائمة **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="24aa3-282">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="24aa3-283">توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="24aa3-283">Location directives</span></span>

<span data-ttu-id="24aa3-284">يجب إنشاء توجيهات الموقع لإرشاد العمل الذي يتم إنشاؤه بعد اكتمال الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="24aa3-285">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="24aa3-286">في الحقل **نوع أمر العمل**، حدد *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="24aa3-287">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24aa3-288">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="24aa3-289">**التسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="24aa3-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="24aa3-290">**الاسم:** *وضع على Baydoor*</span><span class="sxs-lookup"><span data-stu-id="24aa3-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="24aa3-291">في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="24aa3-292">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="24aa3-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="24aa3-293">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="24aa3-293">**Site:** *6*</span></span>
    - <span data-ttu-id="24aa3-294">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="24aa3-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="24aa3-295">**كود التوجيه:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="24aa3-296">**وحدة SKU متعددة:** *لا*</span><span class="sxs-lookup"><span data-stu-id="24aa3-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="24aa3-297">حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="24aa3-298">في علامة التبويب السريعة **السطور**، حدد **جديد**، ثم عيِّن القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="24aa3-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="24aa3-299">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="24aa3-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="24aa3-300">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="24aa3-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="24aa3-301">**من الكمية:** *0*</span><span class="sxs-lookup"><span data-stu-id="24aa3-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="24aa3-302">**إلى الكمية:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="24aa3-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="24aa3-303">حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="24aa3-304">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد**، ثم عيِّن القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="24aa3-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="24aa3-305">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="24aa3-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="24aa3-306">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="24aa3-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="24aa3-307">**الاسم:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="24aa3-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="24aa3-308">حدد **حفظ** لإتاحة الزر **تحرير الاستعلام** في علامة التبويب السريعة **إجراءات توجيه الموقع**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="24aa3-309">في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="24aa3-310">في مربع حوار الاستعلام، في علامة التبويب **النطاق**، ابحث عن الصف الذي يحتوي على حقل **المجال** المعين إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="24aa3-311">عيِّن حقل **المعايير** لهذا الصف على *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="24aa3-312">حدد **موافق** لتأكيد التحرير.</span><span class="sxs-lookup"><span data-stu-id="24aa3-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="24aa3-313">فئات العمل</span><span class="sxs-lookup"><span data-stu-id="24aa3-313">Work classes</span></span>

1. <span data-ttu-id="24aa3-314">انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="24aa3-315">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24aa3-316">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="24aa3-317">**معرف فئة العمل:** *الفرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="24aa3-318">**الوصف:** *الفرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="24aa3-319">**نوع أمر العمل:** *انتقاء المخزون الذي تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="24aa3-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="24aa3-320">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="24aa3-321">قوالب العمل</span><span class="sxs-lookup"><span data-stu-id="24aa3-321">Work templates</span></span>

1. <span data-ttu-id="24aa3-322">انتقل إلى **إدارة المستودعات \> العمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="24aa3-323">في الحقل **نوع أمر العمل**، حدد *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="24aa3-324">في الشبكة، حدد قالب العمل **انتقاء 62 للتعبئة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="24aa3-325">في جزء الإجراءات، حدد **فواصل رأس العمل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="24aa3-326">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="24aa3-327">في السطر الذي يحتوي على الحقل **اسم الحقل** المعين على *معرف الشحنة*، امسح خانة الاختيار **تجميع حسب هذا الحقل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="24aa3-328">حدد **حفظ**، ثم اغلق مربع الحوار **فواصل رأس العمل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="24aa3-329">في الحقل **نوع أمر العمل**، حدد *انتقاء المخزون الذي تم فرزه*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="24aa3-330">حدد **جديد**، لإنشاء قالب عمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="24aa3-331">في القسم **نظرة عامة**، عيّن القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="24aa3-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="24aa3-332">اقبل القيم الافتراضية لكافة الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="24aa3-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="24aa3-333">**قالب العمل:** *انتقاء ما تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="24aa3-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="24aa3-334">**وصف قالب العمل:** *انتقاء ما تم فرزه*</span><span class="sxs-lookup"><span data-stu-id="24aa3-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="24aa3-335">حدد **حفظ** لإتاحة القسم **تفاصيل قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="24aa3-336">ستنشئ سطرين في القسم **تفاصيل قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="24aa3-337">حدد **جديد**، ثم عيِّن القيم التالية للسطر 1:</span><span class="sxs-lookup"><span data-stu-id="24aa3-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="24aa3-338">**نوع العمل:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="24aa3-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="24aa3-339">**إلزامي:** محدد (= *نعم*)</span><span class="sxs-lookup"><span data-stu-id="24aa3-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="24aa3-340">**معرف فئة العمل:** *الفرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="24aa3-341">حدد **جديد** مرة أخرى، ثم عيِّن القيم التالية للسطر 2:</span><span class="sxs-lookup"><span data-stu-id="24aa3-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="24aa3-342">**نوع العمل:** *إيداع*</span><span class="sxs-lookup"><span data-stu-id="24aa3-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="24aa3-343">**إلزامي:** محدد (= *نعم*)</span><span class="sxs-lookup"><span data-stu-id="24aa3-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="24aa3-344">**معرف فئة العمل:** *الفرز*</span><span class="sxs-lookup"><span data-stu-id="24aa3-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="24aa3-345">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="24aa3-346">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="24aa3-346">Example scenario</span></span>

<span data-ttu-id="24aa3-347">يحاكي هذا السيناريو موقفًا حيث يخزن المستودع الأصناف الصغيرة في المواقع ويجب حزمها في صناديق قبل شحنها، عندما تكون وظيفة محطة التعبئة غير مناسبة تمامًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="24aa3-348">يقوم العاملون بانتقاء الأوامر للعديد من العملاء والعناوين المختلفة في نفس الوقت لزيادة سرعة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="24aa3-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="24aa3-349">بعد اكتمال الانتقاءد، يصل العاملون إلى موقع الفرز، حيث يمكن فرز الأصناف المنتقاة في الصندوق الصحيح، استنادًا إلى المعايير المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="24aa3-350">في هذا المثال، سيتم استخدام معرف الشحنة لتحديد الصندوق الصحيح، نظرًا لأن كل شحنة لها عنوان مختلف.</span><span class="sxs-lookup"><span data-stu-id="24aa3-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="24aa3-351">بعد تعبئة كافة الأصناف من التحميل وفرزها حسب الشحنة، سيتم نقل الصناديق إلى المنطقة المرحلية وتحميلها في النهاية إلى الشاحنة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="24aa3-352">قبل بدء السيناريو، تأكد من إعداد كافة وظائف المستودع القياسية بشكل صحيح للمستودع لديك.</span><span class="sxs-lookup"><span data-stu-id="24aa3-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="24aa3-353">يستخدم مستودع Contoso القياسي *62* لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="24aa3-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="24aa3-354">لم يتم تغيير التكوينات القياسية، بالإضافة إلى ما هو موضح في الإعداد.</span><span class="sxs-lookup"><span data-stu-id="24aa3-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="24aa3-355">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="24aa3-355">Create demand</span></span>

<span data-ttu-id="24aa3-356">قبل التمكن من شرح الوظيفة، يجب إنشاء طلب.</span><span class="sxs-lookup"><span data-stu-id="24aa3-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="24aa3-357">بالنسبة لهذا السيناريو، ستقوم بإنشاء ثلاثه أوامر مبيعات لثلاثة عملاء مختلفين لمحاكاة عناوين تسليم مختلفة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="24aa3-358">وبهذه الطريقة ستنشئ ثلاث شحنات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="24aa3-359">قبل إنشاء أوامر المبيعات والشحنات، تأكد أن مواقع الانتقاء بها مخزون كاف لكافة الأصناف في الأوامر.</span><span class="sxs-lookup"><span data-stu-id="24aa3-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="24aa3-360">راجع إعدادات توجيه الموقع لتأكيد مواقع الانتقاء التي يتم استخدامها لانتقاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="24aa3-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="24aa3-361">إذا كان من الضروري تسوية المخزون، فيمكنك إنشاء حركات يدوية أو استخدام تزويد أو استخدام أي سير عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="24aa3-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="24aa3-362">ثم احجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="24aa3-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="24aa3-363">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="24aa3-364">حدد **جديد** لإنشاء أمر مبيعات للأمر 1.</span><span class="sxs-lookup"><span data-stu-id="24aa3-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="24aa3-365">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="24aa3-366">**العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="24aa3-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="24aa3-367">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="24aa3-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="24aa3-368">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-368">Select **OK**.</span></span>
1. <span data-ttu-id="24aa3-369">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="24aa3-370">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-370">Set the following values:</span></span>

    - <span data-ttu-id="24aa3-371">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="24aa3-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="24aa3-372">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="24aa3-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="24aa3-373">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="24aa3-374">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="24aa3-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="24aa3-375">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="24aa3-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="24aa3-376">كرر الخطوات التالية مع كل سطر مبيعات في الأمر لحجز المخزون له:</span><span class="sxs-lookup"><span data-stu-id="24aa3-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="24aa3-377">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="24aa3-378">في صفحة **الحجز**، حدد **حجز دفعة** ثم اغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="24aa3-379">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-379">Select **Save**.</span></span>

1. <span data-ttu-id="24aa3-380">حدد **جديد** لإنشاء أمر مبيعات للأمر 2.</span><span class="sxs-lookup"><span data-stu-id="24aa3-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="24aa3-381">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="24aa3-382">**العميل:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="24aa3-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="24aa3-383">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="24aa3-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="24aa3-384">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-384">Select **OK**.</span></span>
1. <span data-ttu-id="24aa3-385">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="24aa3-386">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-386">Set the following values:</span></span>

    - <span data-ttu-id="24aa3-387">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="24aa3-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="24aa3-388">**الكمية:** *7*</span><span class="sxs-lookup"><span data-stu-id="24aa3-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="24aa3-389">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="24aa3-390">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="24aa3-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="24aa3-391">**الكمية:** *3*</span><span class="sxs-lookup"><span data-stu-id="24aa3-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="24aa3-392">كرر الخطوات التالية مع كل سطر مبيعات في الأمر لحجز المخزون له:</span><span class="sxs-lookup"><span data-stu-id="24aa3-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="24aa3-393">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="24aa3-394">في صفحة **الحجز**، حدد **حجز دفعة** ثم اغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="24aa3-395">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-395">Select **Save**.</span></span>

1. <span data-ttu-id="24aa3-396">حدد **جديد** لإنشاء أمر مبيعات للأمر 3.</span><span class="sxs-lookup"><span data-stu-id="24aa3-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="24aa3-397">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="24aa3-398">**العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="24aa3-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="24aa3-399">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="24aa3-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="24aa3-400">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-400">Select **OK**.</span></span>
1. <span data-ttu-id="24aa3-401">تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="24aa3-402">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="24aa3-402">Set the following values:</span></span>

    - <span data-ttu-id="24aa3-403">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="24aa3-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="24aa3-404">**الكمية:** *8*</span><span class="sxs-lookup"><span data-stu-id="24aa3-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="24aa3-405">اتبع الخطوات التالية لحجز مخزون لسطر المبيعات:</span><span class="sxs-lookup"><span data-stu-id="24aa3-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="24aa3-406">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="24aa3-407">في صفحة **الحجز**، حدد **حجز دفعة** ثم اغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="24aa3-408">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-408">Select **Save**.</span></span>

<span data-ttu-id="24aa3-409">أكمل الإجراء التالي لإصدار كل أمر من أوامر المبيعات للمستودع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="24aa3-410">سيتم إنشاء ثلاث شحنات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-410">Three different shipments will be created.</span></span> <span data-ttu-id="24aa3-411">ستضيف بعدها الشحنات الثلاث إلى موجة واحدة جديدة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="24aa3-412">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="24aa3-413">حدد أول أمر مبيعات أنشأته في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="24aa3-414">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="24aa3-415">ستتلقى رسالة معلوماتية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="24aa3-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="24aa3-416">كرر الخطوات السابقة لإصدار أمري المبيعات 2 و 3 للمستودع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="24aa3-417">لاحظ أن الرسالة المعلوماتية التي تتلقاها تشير إلى أنه قد تمت إضافة شحنة إلى الموجة التي تم إنشاؤه عند إصدارك أمر المبيعات رقم 1.</span><span class="sxs-lookup"><span data-stu-id="24aa3-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="24aa3-418">انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="24aa3-419">حدد معرف الموجة الذي تم إنشاؤه من إصدار أوامر المبيعات لفتح صفحة **الموجات**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="24aa3-420">تعرض هذه الصفحة تفاصيل الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-420">This page shows the wave details.</span></span> <span data-ttu-id="24aa3-421">تعرض علامة التبويب السريعة **بنود الموجة** الشحنات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="24aa3-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="24aa3-422">يجب الآن إنشاء عمل لإحضار الأصناف من مواقع الانتقاء إلى موقع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="24aa3-423">في جزء الإجراءات، حدد **معالجة**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="24aa3-424">أثناء معالجة الموجة، سيستخدم أسلوب الفرز قالب الفرز لتعيين المخزون لمواضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="24aa3-425">عند اكتمال معالجة الموجة، تتلقى رسالة معلوماتية توضح أنه تم ترحيل الموجة وإنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="24aa3-426">في جزء الإجراءات، ضمن علامة التبويب **الموجة**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل** لعرض العمل الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="24aa3-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="24aa3-427">قم بتدوين ملاحظة بمُعرف العمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="24aa3-428">انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> تعيينات موضع الفرز الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="24aa3-429">في العمود الأيمن، يمكنك عرض موضع الفرز الخارجي الذي تم إنشاؤه لكل شحنة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="24aa3-430">في علامة التبويب السريعة **معايير موضع الفرز**، يمكنك عرض معرف الشحنة لهذا الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="24aa3-431">تم إنشاء معرف عمل واحد لإحضار المخزون من مواقع الانتقاء إلى موقع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="24aa3-432">لإكمال العمل، ستحتاج إلى معرف العمل الذي تم إنشاؤه أثناء معالجة الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="24aa3-433">انتقاء أمر المبيعات لموقع الفرز</span><span class="sxs-lookup"><span data-stu-id="24aa3-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="24aa3-434">سجِّل الدخول إلى تطبيق الأجهزة المحمولة كعامل في المستودع *62*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="24aa3-435">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="24aa3-436">من القائمة **خارجي**، حدد **انتقاء المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="24aa3-437">حدد الحقل **المعرف**، ثم أدخل معرف العمل من معالجة الموجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="24aa3-438">قم بتأكيد الإدخال.</span><span class="sxs-lookup"><span data-stu-id="24aa3-438">Confirm your entry.</span></span>

    <span data-ttu-id="24aa3-439">ستكون مطالبًا بعدها بإدخال لوحة الترخيص الهدف (LP).</span><span class="sxs-lookup"><span data-stu-id="24aa3-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="24aa3-440">لاحظ أن السطر 1 في أمر المبيعات 1 هو ما يجب انتقاؤه وإضافته إلى لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="24aa3-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="24aa3-441">يتم إظهار رقم الصنف والكمية ووصف الصنف وموقع الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="24aa3-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="24aa3-442">في الحقل **لوحة الترخيص الهدف**، أدخل رقم لوحة ترخيص.</span><span class="sxs-lookup"><span data-stu-id="24aa3-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="24aa3-443">ستنتقِ كافة السطور التي تم إنشاؤها من الموجة التي تمت معالجتها إلى نفس لوحة الترخيص الهدف.</span><span class="sxs-lookup"><span data-stu-id="24aa3-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="24aa3-444">قم بتأكيد الإدخال.</span><span class="sxs-lookup"><span data-stu-id="24aa3-444">Confirm your entry.</span></span>

    <span data-ttu-id="24aa3-445">يقدم تطبيق الأجهزة المحمولة الآن سلسلة من صفحات **الانتقاء** التي توجهك إلى موقع الانتقاء، والصنف والكمية التي يجب انتقاؤهما.</span><span class="sxs-lookup"><span data-stu-id="24aa3-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="24aa3-446">بعد إضافة الصنف المنتقى إلى لوحة الترخيص، ستقوم بتأكيد عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="24aa3-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="24aa3-447">ستكون الصفحة الأخيرة هي العمل لوضع العناصر المنتقاة في موقع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="24aa3-448">قم بتأكيد عمل الانتقاء الأول.</span><span class="sxs-lookup"><span data-stu-id="24aa3-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="24aa3-449">يتم عرض عمل الانتقاء التالي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-449">The next pick work is shown.</span></span> <span data-ttu-id="24aa3-450">قم بتأكيد الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="24aa3-450">Confirm the pick.</span></span>
1. <span data-ttu-id="24aa3-451">استمر في تأكيد عمل الانتقاء المتبقي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="24aa3-452">الخطوة الأخيرة هي إكمال عمل الوضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-452">The last step is to complete the put work.</span></span> <span data-ttu-id="24aa3-453">قم بتأكيد الاحتفاظ في موقع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="24aa3-454">ستتلقى رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="24aa3-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="24aa3-455">انهِ **انتقاء المبيعات** على تطبيق الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="24aa3-456">الفرز/وضع على الحائط</span><span class="sxs-lookup"><span data-stu-id="24aa3-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="24aa3-457">الآن وبعد وضع كل المخزون في موقع الفرز، يجب فرزه في موضع الفرز الصحيح.</span><span class="sxs-lookup"><span data-stu-id="24aa3-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="24aa3-458">سجِّل الدخول إلى تطبيق الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="24aa3-459">من القائمة الرئيسية، حدد **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="24aa3-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="24aa3-460">في القائمة **خارجي**، حدد **فرز** للبدء في فرز العناصر.</span><span class="sxs-lookup"><span data-stu-id="24aa3-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="24aa3-461">في الحقل **لوحة الترخيص/الحاوية**، أدخل لوحة الترخيص الهدف لعمل أمر المبيعات الذي تم انتقاؤه.</span><span class="sxs-lookup"><span data-stu-id="24aa3-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="24aa3-462">قم بتأكيد الإدخال.</span><span class="sxs-lookup"><span data-stu-id="24aa3-462">Confirm your entry.</span></span>
1. <span data-ttu-id="24aa3-463">أدخل رقم الصنف المراد فرزه أولاً.</span><span class="sxs-lookup"><span data-stu-id="24aa3-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="24aa3-464">يحدد النظام موضع الفرز الأول الذي ينبغي إظهاره.</span><span class="sxs-lookup"><span data-stu-id="24aa3-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="24aa3-465">قم بتأكيد موضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="24aa3-466">أنت مطالب بتعيين لوحة ترخيص إلى موضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="24aa3-467">حدد الحقل **لوحة الترخيص**، وأدخل رقم لوحة الترخيص، ثم قم بأاكيد الإدخال.</span><span class="sxs-lookup"><span data-stu-id="24aa3-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="24aa3-468">نظرًا لارتباط موضع الفرز بمعرف الشحنة، ستقوم بفرز الأصناف المنتقاة في لوحة ترخيص خاصة بالشحنة الخارجية وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="24aa3-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="24aa3-469">تعرض الصفحة التالية معرف الصنف والكمية ومعرف موضع الفرز ومعرفات لوحات ترخيص "من" (الانتقاء) و "إلى" (الفرز).</span><span class="sxs-lookup"><span data-stu-id="24aa3-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="24aa3-470">وترشدك المعلومات الموجودة في هذه الصفحة إلى فرز الأصناف والكميات المحددة من لوحة ترخيص الانتقاء إلى لوحة ترخيص الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="24aa3-471">قم بتأكيد موضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="24aa3-472">افرز العناصر الموجودة في موضع الفرز الأول.</span><span class="sxs-lookup"><span data-stu-id="24aa3-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="24aa3-473">وعند الانتهاء من ذلك، يوجهك النظام إلى موضع الفرز التالي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="24aa3-474">كرر هذه العملية لكافة السطور المنتقاة في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="24aa3-475">وينبغي لك أيضًا استخدام هذه العملية عند وجود سطور انتقاء متعددة لها نفس رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="24aa3-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="24aa3-476">بتكرار هذه العملية لكافة الأصناف، يقيِّم النظام المعايير من الصنف التالي الممسوح ضوئيًا (سطر العمل) ويحدد موضع الفرز الذي ينبغي وضعه فيه.</span><span class="sxs-lookup"><span data-stu-id="24aa3-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="24aa3-477">يتم توجيهك تلقائيًا لوضع العنصر في موضع الفرز الصحيح.</span><span class="sxs-lookup"><span data-stu-id="24aa3-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="24aa3-478">وفقًا لإعداد التأكيد، يتم أيضًا توجيهك لتأكيد هذا الإجراء عن طريق إدخال رقم الموضع أو معرف لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="24aa3-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="24aa3-479">في حالة تشغيل الفرز التلقائي، لا يتوفر التخطي اليدوي.</span><span class="sxs-lookup"><span data-stu-id="24aa3-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="24aa3-480">عند الانتهاء من ذلك، في Microsoft Dynamics 365 Supply Chain Management، افتح صفحة **تعيينات موضع الفرز الخارجي** لمراجعة حالة المواضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="24aa3-481">إذا كانت المواضع مغلقة تلقائيًا، فحدد **إظهار المغلق** لإظهار المواضع المغلقة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="24aa3-482">لاحظ أنه يتم عرض حركات موضع الفرز.</span><span class="sxs-lookup"><span data-stu-id="24aa3-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="24aa3-483">يتم إظهار الصنف والكمية التي تمت معالجتها في الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="24aa3-484">عند إعداد قالب الفرز الخارجي، عيِّن الخيار **إغلاق موضع الفرز تلقائيًا** على *نعم*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="24aa3-485">وبالتالي يتم إغلاق الموضع تلقائيًا بعد وضع آخر مخزون متوقع به.</span><span class="sxs-lookup"><span data-stu-id="24aa3-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="24aa3-486">تكون مواضع الفرز بالحالة **مغلق**، وقد تم إنشاء العمل لنقل المخزون الذي تم فرزه إلى موقع *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="24aa3-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="24aa3-487">أكمل عمل انتقاء المخزون الذي تم فرزه لنقل المخزون إلى موقع الشحن.</span><span class="sxs-lookup"><span data-stu-id="24aa3-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="24aa3-488">عندما يكون المخزون جاهزًا قم بتأكيد شحنه.</span><span class="sxs-lookup"><span data-stu-id="24aa3-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="24aa3-489">لكي تتم معالجة عمل انتقاء المخزون الذي تم فرزه بشكل صحيح، ينبغي استخدام عنصر قائمة الأجهزة المحمولة الذي يحتوي على معرف فئة عمل يكون الحقل **نوع أمر العمل** فيه معينًا على *انتقاء المخزون الذي تم فرزه* لعملية التحميل والحركة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="24aa3-490">إغلاق موضع يدويًا (اختياري)</span><span class="sxs-lookup"><span data-stu-id="24aa3-490">Manually close a position (optional)</span></span>

<span data-ttu-id="24aa3-491">إذا كان ينبغي إغلاق مواضع الفرز يدويًا، يجب تعيين الخيار **إغلاق موضع الفرز تلقائيًا** لقالب الفرز الخارجي على *لا*، ويجب إجراء الإغلاق قبل إمكانية نقل المخزون إلى منطقه باب المرسى.</span><span class="sxs-lookup"><span data-stu-id="24aa3-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="24aa3-492">يمكن إغلاق المواضع بعدة طرق:</span><span class="sxs-lookup"><span data-stu-id="24aa3-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="24aa3-493">عبر تطبيق إدارة المستودع للأجهزة المحمولة:</span><span class="sxs-lookup"><span data-stu-id="24aa3-493">Via the Warehouse Management mobile app:</span></span>

    - <span data-ttu-id="24aa3-494">يمكن للمستخدم إجراء المسح الضوئي لأحد الأصناف الموجودة بالفعل في الموضع ثم تحديد **إغلاق** لإغلاق الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="24aa3-495">إذا قام المستخدم بالمسح الوئي لحاوية تم فرزها بالفعل، تظهر رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="24aa3-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="24aa3-496">ولكن لا يزال بإمكان المستخدم الاستمرار في إغلاق الموضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="24aa3-497">من صفحة **تعيينات موضع الفرز الخارجي** في Microsoft Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="24aa3-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="24aa3-498">يمكن للمستخدم تحديد سجل موضع الفرز الخارجي ثم تحديد **إغلاق الوضع** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="24aa3-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="24aa3-499">تلميحات</span><span class="sxs-lookup"><span data-stu-id="24aa3-499">Tips</span></span>

- <span data-ttu-id="24aa3-500">لا يمكن نقل الأصناف بين المواضع بعد تعيينها إلى موضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="24aa3-501">يقيِّم النظام عدد العناصر التي ينبغي نقلها إلى موضع معين.</span><span class="sxs-lookup"><span data-stu-id="24aa3-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="24aa3-502">يمكن تكوين قالب الفرز لإنشاء الحاويات تلقائيًا عند إغلاق المواضع.</span><span class="sxs-lookup"><span data-stu-id="24aa3-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="24aa3-503">سيؤدي هذا الأسلوب إلى إنشاء بنية معرف حاوية قياسية استنادًا إلى ملف تعريف التعبئة المحدد.</span><span class="sxs-lookup"><span data-stu-id="24aa3-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24aa3-504">بعد إنشاء عمل الحركة من موقع الفرز، يجب ألا يتم إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="24aa3-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="24aa3-505">وبخلاف ذلك، سيتم حذف الموضع والحاويات الموجودة فيه من النظام ولن تكون متوفرة لإجراء مزيد من المعالجة.</span><span class="sxs-lookup"><span data-stu-id="24aa3-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="24aa3-506">ستتم إزالة المخزون أيضًا.</span><span class="sxs-lookup"><span data-stu-id="24aa3-506">The inventory will also be removed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]