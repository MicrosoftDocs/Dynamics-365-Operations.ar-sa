---
title: مجموعات التخزين
description: تقدم أنظمه مجموعات التخزين طريقه لانتقاء عده لوحات ترخيص في نفس الوقت ثم القيام بها للتخزين في مواقع مختلفه. ويمكن ان تكون مفيده جدا لاعمال البيع بالتجزئة ، حيث لا تعد لوحات الترخيص بالتات كامله من المخزون.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a330ddccbd17c92443232fc8488e36a59235773
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512320"
---
# <a name="putaway-clusters"></a><span data-ttu-id="a640f-104">مجموعات التخزين</span><span class="sxs-lookup"><span data-stu-id="a640f-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a640f-105">تقدم أنظمه مجموعات التخزين طريقه لانتقاء عده لوحات ترخيص في نفس الوقت ثم القيام بها للتخزين في مواقع مختلفه.</span><span class="sxs-lookup"><span data-stu-id="a640f-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="a640f-106">تشير إلى هذه العملية في أغلب الأحيان بالاسم *خط سير متكرر الوقفات*.</span><span class="sxs-lookup"><span data-stu-id="a640f-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="a640f-107">ويمكن ان تكون مجموعات التخزين مفيده جدا لاعمال البيع بالتجزئة ، حيث لا تعد لوحات الترخيص بالتات كامله من المخزون.</span><span class="sxs-lookup"><span data-stu-id="a640f-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="a640f-108">تشغيل ميزة تخزين المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="a640f-109">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="a640f-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a640f-110">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a640f-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a640f-111">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a640f-112">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="a640f-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a640f-113">**اسم الميزة:** *ميزه تخزين المجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="a640f-114">إعداد للسيناريو النموذجي</span><span class="sxs-lookup"><span data-stu-id="a640f-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="a640f-115">ملفات تعريف نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-115">Cluster profiles</span></span>

<span data-ttu-id="a640f-116">يحدد ملف تعريف نظام مجموعه التخزين مكان انتقال أحد الأصناف ، استنادا إلى الموقع الذي تم تعيينه للصنف في وقت الاستلام.</span><span class="sxs-lookup"><span data-stu-id="a640f-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="a640f-117">في حالة طلب أنظمة مجموعة مختلفة، فإنه يجب إنشاء ملف تعريف نظام مجموعة مختلف للتخزين لكل صنف في قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="a640f-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="a640f-118">انتقل إلى **إدارة المستودعات \> الإعداد \> الجهاز المحمول \> ملفات تعريف نظام المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="a640f-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="a640f-119">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a640f-120">في **الرأس**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="a640f-121">**معرف ملف تعريف مجموعة التخزين:** *التخزين لنظام المجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a640f-122">**اسم معرف ملف تعريف نظام مجموعة التخزين:** *التخزين لنظام المجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a640f-123">**نوع نظام المجموعة:** *تخزين*</span><span class="sxs-lookup"><span data-stu-id="a640f-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="a640f-124">**الرقم التسلسلي:** قبول القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a640f-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="a640f-125">حدد **حفظ** لإتاحة الحقول المطلوبة في علامة التبويب السريعة **عام**.</span><span class="sxs-lookup"><span data-stu-id="a640f-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="a640f-126">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a640f-127">**توقيت تعيين نظام المجموعة:** *عند الاستلام*</span><span class="sxs-lookup"><span data-stu-id="a640f-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="a640f-128">ويحدد هذا الحقل ما إذا كان يجب تعيين نظام مجموعه التخزين فورا عند استلام المخزون ام لا أو فرزها فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="a640f-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="a640f-129">**قاعده تعيين نظام المجموعة:** *يدوية*</span><span class="sxs-lookup"><span data-stu-id="a640f-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="a640f-130">يحدد هذا الحقل ما إذا كان يجب تحديد تعيين نظام المجموعة تلقائيًا بواسطة النظام أم يدويًا بواسطة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="a640f-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="a640f-131">**كود التوجيه:** اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a640f-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="a640f-132">**تحديد موقع نظام مجموعة التخزين:** *الاستلام*</span><span class="sxs-lookup"><span data-stu-id="a640f-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="a640f-133">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-133">The following values are available:</span></span>

        - <span data-ttu-id="a640f-134">**الاستلام** - يتم العثور على الموقع مباشرة خلال الاستلام.</span><span class="sxs-lookup"><span data-stu-id="a640f-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="a640f-135">**إغلاق نظام المجموعة** - يتم العثور على الموقع عند إغلاق نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a640f-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="a640f-136">**موجه بواسطة المستخدم**- يتم العثور علي الموقع عند انتقاء لوح الترخيص من المجموعة للتخزين.</span><span class="sxs-lookup"><span data-stu-id="a640f-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="a640f-137">في هذه الحالة ، لا يتم تحديد اي موقع عند إنشاء العمل للتخزين.</span><span class="sxs-lookup"><span data-stu-id="a640f-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="a640f-138">خلال التخزين نفسه، يجب علي المستخدم تفحص لوح الترخيص أو معرف العمل لبدء الخطوة التي تم وضعها.</span><span class="sxs-lookup"><span data-stu-id="a640f-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="a640f-139">ثم يبحث النظام عن موقع المكان مره أخرى ويقوم باعلام المستخدم عن مكان وضع الكمية التي تم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="a640f-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="a640f-140">**نظام مجموعه التخزين لكل مستخدم:** *لا*</span><span class="sxs-lookup"><span data-stu-id="a640f-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="a640f-141">يحدد هذا الحقل ما إذا كان يجب ان يكون كل كتله فريدة لكل مستخدم عند تعيين نظام المجموعة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a640f-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="a640f-142">ويتوفر ذلك فقط عندما يتم تعيين حقل **قاعده تعيين نظام المجموعة** إلى *تلقائي*.</span><span class="sxs-lookup"><span data-stu-id="a640f-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="a640f-143">**قيد الوحدة:** اترك هذا الحقل فارغا.</span><span class="sxs-lookup"><span data-stu-id="a640f-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="a640f-144">يحدد هذا الحقل الوحدة التي يجب استلامها لملف التعريف ليكون صالحا.</span><span class="sxs-lookup"><span data-stu-id="a640f-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="a640f-145">في حالة تركها فارغة، تكون كافة الوحدات صالحة.</span><span class="sxs-lookup"><span data-stu-id="a640f-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="a640f-146">**فاصل وحده العمل:** *فردي*</span><span class="sxs-lookup"><span data-stu-id="a640f-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="a640f-147">يحدد هذا الحقل ما إذا كان يجب دمج كافة المخزون (باستخدام معرف نظام المجموعة ولوحه الترخيص) علي لوحه ترخيص واحده عند إغلاق نظام المجموعة، وما إذا كان يجب وضعها كلوحه ترخيص واحده أو بشكل منفصل علي لوحات الترخيص التي تم استلامها.</span><span class="sxs-lookup"><span data-stu-id="a640f-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="a640f-148">لا يتوفر هذا الحقل في حاله تعيين الحقل **تحديد موقع نظام المجموعة للتخزين** إلى *الاستلام*.</span><span class="sxs-lookup"><span data-stu-id="a640f-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="a640f-149">**استمرار نظام المجموعة كلوحة ترخيص رئيسية:** *لا*</span><span class="sxs-lookup"><span data-stu-id="a640f-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="a640f-150">في حاله تعيين هذا الخيار علي *نعم*، عند إتمام الخطوة "وضع"، سيصبح معرف نظام المجموعة للوحه ترخيص رئيسيه، سيتم ربط كافة العناصر الموجودة في معرف نظام مجموعة بلوحه الترخيص الرئيسية هذه.</span><span class="sxs-lookup"><span data-stu-id="a640f-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="a640f-151">في علامة التبويب السريعة **فرز نظام المجموعة**، يمكنك تحديد معايير فرز التخزين.</span><span class="sxs-lookup"><span data-stu-id="a640f-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="a640f-152">حدد **جديد** على شريط الأدوات لإضافة سطر، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="a640f-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="a640f-153">**الرقم التسلسلي:** قبول القيمة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a640f-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="a640f-154">**اسم الحقل:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="a640f-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="a640f-155">يحدد هذا الحقل الحقل الذي يجب ان يستخدمه هذا البند كمعيار فرز.</span><span class="sxs-lookup"><span data-stu-id="a640f-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="a640f-156">**الفرز:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="a640f-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="a640f-157">يحدد هذا الحقل ما إذا كان الفرز يتم بترتيب تصاعدي أم تنازلي.</span><span class="sxs-lookup"><span data-stu-id="a640f-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="a640f-158">في علامة التبويب السريعة **قالب عمل نظام المجموعة**، حدد **جديد** في شريط الأدوات لإضافة سطر، ثم عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="a640f-159">**نوع أمر العمل:** *أوامر الشراء*</span><span class="sxs-lookup"><span data-stu-id="a640f-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="a640f-160">**قالب العمل:** *أمر الشراء 61 مباشر*</span><span class="sxs-lookup"><span data-stu-id="a640f-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="a640f-161">في جزء الاجراء، حدد **حفظ**، ثم حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="a640f-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="a640f-162">في مربع حوار **التخزين لنظام المجموعة**، ضمن علامة التبويب **النطاق**، حدد **إضافة** لإضافة بند ثاني إلى الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a640f-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="a640f-163">ثم قم بتحديث بنود الاستعلام كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="a640f-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="a640f-164">الجدول</span><span class="sxs-lookup"><span data-stu-id="a640f-164">Table</span></span> | <span data-ttu-id="a640f-165">الجدول المشتق</span><span class="sxs-lookup"><span data-stu-id="a640f-165">Derived table</span></span> | <span data-ttu-id="a640f-166">الحقل</span><span class="sxs-lookup"><span data-stu-id="a640f-166">Field</span></span> | <span data-ttu-id="a640f-167">المعايير</span><span class="sxs-lookup"><span data-stu-id="a640f-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="a640f-168">العمل</span><span class="sxs-lookup"><span data-stu-id="a640f-168">Work</span></span> | <span data-ttu-id="a640f-169">العمل</span><span class="sxs-lookup"><span data-stu-id="a640f-169">Work</span></span> | <span data-ttu-id="a640f-170">المستودع</span><span class="sxs-lookup"><span data-stu-id="a640f-170">Warehouse</span></span> | <span data-ttu-id="a640f-171">*61*</span><span class="sxs-lookup"><span data-stu-id="a640f-171">*61*</span></span> |
    | <span data-ttu-id="a640f-172">العمل</span><span class="sxs-lookup"><span data-stu-id="a640f-172">Work</span></span> | <span data-ttu-id="a640f-173">العمل</span><span class="sxs-lookup"><span data-stu-id="a640f-173">Work</span></span> | <span data-ttu-id="a640f-174">معرف العمل</span><span class="sxs-lookup"><span data-stu-id="a640f-174">Work ID</span></span> | <span data-ttu-id="a640f-175">اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a640f-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="a640f-176">حدد **موافق** لحفظ الاستعلام وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="a640f-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="a640f-177">حدد **حفظ** في جزء الإجراءات وأغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a640f-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a640f-178">الحقول الموجودة في ملف تعريف الكتلة والتي تظهر معتمة عند **إنشاء معرف نظام المجموعة** يتم تعيينها إلى *نعم* غير متاحه ولن يتم اعتبارها عند استخدام هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="a640f-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a640f-179">أصناف قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="a640f-179">Mobile device menu items</span></span>

<span data-ttu-id="a640f-180">تتوفر عناصر القائمة الجديدة للجهاز المحمول لهذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="a640f-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="a640f-181">يتم استخدام عنصر القائمة **نظام مجموعة الفرز والاستلام** لفرز المخزون الذي تم استلامه في نظام مجموعه المخزون عند الاستلام.</span><span class="sxs-lookup"><span data-stu-id="a640f-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="a640f-182">يتم استخدام عنصر القائمة **التخزين لنظام المجموعة** لنظام المجموعة لتخزين نظام المجموعة بعد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="a640f-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="a640f-183">الاستلام والفرز في نظام مجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-183">Receive and sort cluster</span></span>

<span data-ttu-id="a640f-184">قم بإنشاء عنصر قائمه جهاز محمول جديد لاستلام المخزون والفرز في نظام مجموعه.</span><span class="sxs-lookup"><span data-stu-id="a640f-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="a640f-185">سيقوم عنصر القائمة هذا بإنشاء العمل الوارد بعد استلام المخزون ، والذي يشير إلى انه سيتم استخدام عنصر القائمة المتلقية في مجموعات التخزين.</span><span class="sxs-lookup"><span data-stu-id="a640f-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="a640f-186">يمكن استخدام عنصر قائمه **الاستلام والفرز في نظام المجموعة** مع عناصر قائمه الاستلام التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="a640f-187">استلام بند أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="a640f-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="a640f-188">استلام صنف أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="a640f-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="a640f-189">استلام صنف الحمل</span><span class="sxs-lookup"><span data-stu-id="a640f-189">Load item receiving</span></span>

1. <span data-ttu-id="a640f-190">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="a640f-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a640f-191">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a640f-192">في **الرأس**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="a640f-193">**اسم عنصر القائمة:** *الاستلام والفرز في نظام المجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="a640f-194">**العنوان:** *الاستلام والفرز في نظام مجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="a640f-195">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="a640f-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a640f-196">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="a640f-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="a640f-197">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a640f-198">**عملية إنشاء العمل:** *استلام صنف أمر الشراء*</span><span class="sxs-lookup"><span data-stu-id="a640f-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="a640f-199">**إنشاء لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="a640f-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="a640f-200">**تعيين مجموعه نظام التخزين:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="a640f-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="a640f-201">يتوفر خيار **تعيين نظام المجموعة للتخزين** فقط لنشاط *عمليه إنشاء عمل* من خطوه واحده للاستلام.</span><span class="sxs-lookup"><span data-stu-id="a640f-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="a640f-202">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="a640f-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="a640f-203">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a640f-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="a640f-204">تخزين نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-204">Cluster putaway</span></span>

<span data-ttu-id="a640f-205">قم بإنشاء عنصر قائمه جهاز محمول جديد لوضع نظام المجموعة بعيدا بعد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="a640f-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="a640f-206">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="a640f-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a640f-207">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a640f-208">في **الرأس**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="a640f-209">**اسم عنصر القائمة:** *التخزين لنظام المجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a640f-210">**اللقب:** *التخزين لنظام المجموعة*</span><span class="sxs-lookup"><span data-stu-id="a640f-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a640f-211">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="a640f-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a640f-212">**استخدام العمل الموجود:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="a640f-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="a640f-213">في علامة التبويب السريعة **عام**، عيِّن الحقل **موجه بواسطة** على *التخزين لنظام المجموعة*.</span><span class="sxs-lookup"><span data-stu-id="a640f-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="a640f-214">اقبل القيم الافتراضية للحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="a640f-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="a640f-215">في علامة التبويب السريعة **فئات العمل**، قم باعداد فئة العمل الصالحة لعنصر قائمه جهاز المحمول هذا:</span><span class="sxs-lookup"><span data-stu-id="a640f-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="a640f-216">**معرف فئة العمل:** *شراء*</span><span class="sxs-lookup"><span data-stu-id="a640f-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="a640f-217">**نوع أمر العمل:** *أوامر الشراء*</span><span class="sxs-lookup"><span data-stu-id="a640f-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="a640f-218">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a640f-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="a640f-219">قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="a640f-219">Mobile device menu</span></span>

<span data-ttu-id="a640f-220">قم باضافه عناصر القائمة التي قمت بإنشائها للتو إلى قائمه الوارد الخاصة بتطبيق الاجهزه المحمولة.</span><span class="sxs-lookup"><span data-stu-id="a640f-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="a640f-221">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="a640f-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="a640f-222">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a640f-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a640f-223">في قائمة القوائم، حدد **وارد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="a640f-224">في قائمة **عناصر القوائم المتوفرة وعناصر القائمة**، ابحث عن عنصر القائمة **استلام وفرز نظام المجموعة** وحدده.</span><span class="sxs-lookup"><span data-stu-id="a640f-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="a640f-225">حدد الزر سهم لليمين لنقل عنصر قائمة المحدد إلى قائمة **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="a640f-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="a640f-226">استخدم زر السهم إلى الأعلى أو السهم إلى الأسفل لنقل عنصر القائمة إلى الموضع المطلوب في القائمة</span><span class="sxs-lookup"><span data-stu-id="a640f-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="a640f-227">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a640f-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a640f-228">كرر الخطوات من 4 إلى 7 لإضافة مزيد من عناصر القائمة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="a640f-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="a640f-229">تعيين نظام المجموعه</span><span class="sxs-lookup"><span data-stu-id="a640f-229">Assign cluster</span></span>
    - <span data-ttu-id="a640f-230">تخزين نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a640f-231">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="a640f-231">Example scenario</span></span>

<span data-ttu-id="a640f-232">يحاكي هذا السيناريو معالجه نظام مجموعه التخزين.</span><span class="sxs-lookup"><span data-stu-id="a640f-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="a640f-233">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="a640f-233">Create a purchase order</span></span>

1. <span data-ttu-id="a640f-234">انتقل إلى **الحسابات الدائنة \> أوامر الشراء \> جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="a640f-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="a640f-235">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a640f-236">في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a640f-237">**حساب المورّد:** *1001*</span><span class="sxs-lookup"><span data-stu-id="a640f-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="a640f-238">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="a640f-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a640f-239">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a640f-239">Select **OK**.</span></span>

    <span data-ttu-id="a640f-240">تظهر صفحة **جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="a640f-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="a640f-241">في الصفحة **كافة أوامر الشراء**، في علامة التبويب السريعة **بنود أمر الشراء**، استخدم الزر **أضافه بند** لأضافه البنود التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="a640f-242">سطر أمر الشراء 1:</span><span class="sxs-lookup"><span data-stu-id="a640f-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="a640f-243">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a640f-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="a640f-244">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="a640f-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="a640f-245">سطر أمر الشراء 2:</span><span class="sxs-lookup"><span data-stu-id="a640f-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="a640f-246">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a640f-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="a640f-247">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="a640f-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="a640f-248">سطر أمر الشراء 3:</span><span class="sxs-lookup"><span data-stu-id="a640f-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="a640f-249">**رقم الصنف:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="a640f-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="a640f-250">**الكمية:** *30*</span><span class="sxs-lookup"><span data-stu-id="a640f-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="a640f-251">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a640f-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a640f-252">تدوين ملاحظة برقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a640f-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="a640f-253">استلام المخزون ووضعه بعيدا عن الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="a640f-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="a640f-254">استلام المخزون وفرزه في نظام مجموعه</span><span class="sxs-lookup"><span data-stu-id="a640f-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="a640f-255">سجل الدخول إلى تطبيق المستودع كمستخدم تم إعداده للمستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="a640f-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="a640f-256">من القائمة الرئيسية، حدد **وارد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="a640f-257">في القائمة **وارد**، حدد **استلام نظام المجموعة وفرزها**.</span><span class="sxs-lookup"><span data-stu-id="a640f-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="a640f-258">في حقل **‎Ponum**، أدخل رقم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a640f-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="a640f-259">حدد الزر **موافق** (زر علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="a640f-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="a640f-260">حدد حقل **الصنف**، وأدخل *A0001* كرقم صنف، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a640f-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="a640f-261">حدد حقل **الكمية**، وادخل *10* باستخدام لوحه الأرقام ، ثم حدد زر علامة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="a640f-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="a640f-262">في الصفحة مهمة **الكمية**، حدد **موافق** (الزر علامة الاختيار) لتاكيد الكمية التي قمت بإدخالها.</span><span class="sxs-lookup"><span data-stu-id="a640f-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="a640f-263">في صفحة مهمة **الصنف**، حدد **موافق** للتاكد من انه تم إدخال *A0001* للصنف.</span><span class="sxs-lookup"><span data-stu-id="a640f-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="a640f-264">حدد حقل **معرف نظام المجموعة**، وادخل قيمه لتعيين معرف نظام المجموعة التي تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="a640f-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="a640f-265">سيتم استخدام المعرف الذي تقوم بإدخاله هنا عند استلام الصنفين المتبقيين في أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a640f-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="a640f-266">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a640f-266">Select **OK**.</span></span>

    <span data-ttu-id="a640f-267">تظهر صفحة مهمة **Ponum** وتظهر رسالة "اكتمل العمل".</span><span class="sxs-lookup"><span data-stu-id="a640f-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="a640f-268">تم استلام الصنف *A0001* الآن في موقع *RECV* ويتم تعيينه إلى معرف نظام المجموعة الذي قمت بإدخاله في الخطوة 10.</span><span class="sxs-lookup"><span data-stu-id="a640f-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="a640f-269">كرر الخطوات من 4 إلى 11 لاستلام الصنفين الباقيين من أمر الشراء وتعيينهما إلى معرف نظام المجموعة:</span><span class="sxs-lookup"><span data-stu-id="a640f-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="a640f-270">الكمية *20* للصنف *A0002*.</span><span class="sxs-lookup"><span data-stu-id="a640f-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="a640f-271">الكمية *30* للصنف *M9215*.</span><span class="sxs-lookup"><span data-stu-id="a640f-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="a640f-272">اغلق نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-272">Close the cluster</span></span>

<span data-ttu-id="a640f-273">قبل ان تصبح العناصر الموجودة في المجموعة بعيده ، يجب إغلاق نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a640f-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="a640f-274">في Supply Chain Management، انتقل إلى **أداره المستودعات \> العمل \> الصادر \>مجموعات نظام العمل**.</span><span class="sxs-lookup"><span data-stu-id="a640f-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="a640f-275">في الصفحة **أنظمة مجموعات العمل**، في قسم **نظام مجموعه العمل**، ابحث عن الحقل **معرف نظام المجموعة** لمعرف نظام المجموعة الذي قمت بإدخاله سابقا.</span><span class="sxs-lookup"><span data-stu-id="a640f-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="a640f-276">إذا لم يتم عرض نظام المجموعة، قد يكون تم إغلاقه مسبقا.</span><span class="sxs-lookup"><span data-stu-id="a640f-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="a640f-277">لتحديد ما إذا كان النظام مغلقا ام لا ، حدد خانه الاختيار **إظهار العمل المغلق**، وابحث عن معرف نظام المجموعة الذي قمت بإدخاله سابقا.</span><span class="sxs-lookup"><span data-stu-id="a640f-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="a640f-278">ثم اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="a640f-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="a640f-279">إذا كان قد تم إغلاق نظام المجموعة، فقم بتخطي الخطوات المتبقية لهذا الاجراء ، والانتقال إلى الاجراء التالي، [تخزين نظام المجموعة](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="a640f-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="a640f-280">إذا لم يتم إغلاق نظام المجموعة ، اتبع الخطوات المتبقية من هذا الاجراء لإغلاق نظام المجموعة يدويا.</span><span class="sxs-lookup"><span data-stu-id="a640f-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="a640f-281">بعد ذلك، انتقل إلى الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="a640f-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="a640f-282">في قسم **نظام مجموعة العمل**، حدد معرف مجموعة النظام الذي قمت بإدخاله سابقا.</span><span class="sxs-lookup"><span data-stu-id="a640f-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="a640f-283">في جزء الإجراءات، حدد **إغلاق نظام المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="a640f-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="a640f-284">بعد إغلاق نظام المجموعة، لن يعود ظاهرا في قسم **نظام المجموعة للعمل** (الا إذا تم تحديد خانه الاختيار **إظهار العمل المغلق**).</span><span class="sxs-lookup"><span data-stu-id="a640f-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="a640f-285">تخزين نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-285">Put the cluster away</span></span>

1. <span data-ttu-id="a640f-286">سجل الدخول إلى تطبيق المستودع كمستخدم تم إعداده للمستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="a640f-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="a640f-287">من القائمة الرئيسية، حدد **وارد**.</span><span class="sxs-lookup"><span data-stu-id="a640f-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="a640f-288">من القائمة **الوارد**، حدد **تخزين نظام المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="a640f-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="a640f-289">حدد **معرف نظام المجموعة**، وادخل معرف نظام المجموعة الذي قمت بإدخاله سابقا لنظام المجموعة المغلق.</span><span class="sxs-lookup"><span data-stu-id="a640f-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="a640f-290">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a640f-290">Select **OK**.</span></span>

    <span data-ttu-id="a640f-291">تظهر صفحة **تخزين نظام المجموعة: الانتقاء**‬‏‫ .</span><span class="sxs-lookup"><span data-stu-id="a640f-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="a640f-292">ويعرض معرف الكتلة ، وموقع الانتقاء ، والأصناف (القيمة *مضاعفة* التي سيتم عرضها) ، وإجمالي الكمية في المجموعة التي يجب انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="a640f-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="a640f-293">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a640f-293">Select **OK**.</span></span>

    <span data-ttu-id="a640f-294">تظهر صفحة **تخزين نظام المجموعة: التخزين**‬‏‫ .</span><span class="sxs-lookup"><span data-stu-id="a640f-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="a640f-295">تقوم إرشادات **التخزين** بتعريف معرف نظام المجموعة وموقع التخزين والأصناف وإجمالي الكمية ومعرفات لوحة الترخيص للأصناف التي تم استلامها في نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a640f-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="a640f-296">لديك الخيارات القياسية لتجاوز هذه الخطوة أو المرور فيها.</span><span class="sxs-lookup"><span data-stu-id="a640f-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="a640f-297">![تخزين نظام المجموعة: صفحة التخزين](media/Cluster_putaway-Put.png "تخزين نظام المجموعة: صفحة التخزين")</span><span class="sxs-lookup"><span data-stu-id="a640f-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="a640f-298">حدد **موافق** لتأكيد تخزين نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="a640f-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="a640f-299">تظهر رسالة "اكتمل نظام المجموعة".</span><span class="sxs-lookup"><span data-stu-id="a640f-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="a640f-300">ملاحظات وتلميحات</span><span class="sxs-lookup"><span data-stu-id="a640f-300">Notes and tips</span></span>

<span data-ttu-id="a640f-301">بالنسبة للحالات التي يصبح فيها معرف نظام المجموعة هو لوحه الترخيص الرئيسية لبالته متداخلة ، يتم تعيين موضع التخزين تلقائيا عند فحص معرف نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a640f-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="a640f-302">لا يجب مسح لوحة الترخيص الأخرى ، حتى إذا تم تعيين إنشاء لوحه الترخيص علي يدوي.</span><span class="sxs-lookup"><span data-stu-id="a640f-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>