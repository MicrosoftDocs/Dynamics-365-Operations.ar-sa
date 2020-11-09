---
title: موضع المجموعة ممتلئ
description: يوفر هذا الموضوع معلومات حول ميزة موضع المجموعة ممتلئ. تقدم هذه الميزة بديلاً لفرض قواعد أكثر صرامة لفصل العمل عند استخدام انتقاء المجموعة‬، لأنها تمكّن هامش خطأ أكبر في القيود الحجمية للحاويات أو العبوات.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3610725815b35609ee98b69b367db2945bbf166a
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016161"
---
# <a name="cluster-position-full"></a><span data-ttu-id="5a5b8-104">موضع المجموعة ممتلئ</span><span class="sxs-lookup"><span data-stu-id="5a5b8-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a5b8-105">تقدم ميزة *موضع المجموعة ممتلئ* بديلاً لفرض قواعد أكثر صرامة لفصل العمل عند استخدام انتقاء المجموعة‬، لأنها تمكّن هامش خطأ أكبر في القيود الحجمية للحاويات أو العبوات.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="5a5b8-106">في سيناريو شائع، لا يتم احتواء كافة العناصر الموجودة في أمر العمل في حاوية محددة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="5a5b8-107">هناك خيارات قليلة للعاملين في المستودع الذين ينتقون المجموعة في هذا السيناريو: عليهم إما التغيير إلى حجم حاوية أكبر أو العمل مع المشرف للوصول إلى حل مختلف.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="5a5b8-108">وتقدم هذه الميزة القدرة على تشغيل الزر **ممتلئ** على إحدى وحدات العمل في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="5a5b8-109">في الإصدارات الأقدم، كان هذا الخيار متاحًا فقط لانتقاء الأوامر المنتظمة، وليس لانتقاء المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="5a5b8-110">ومع ذلك، تختلف هذه الميزة عن الزر **ممتلئ** من ناحية أنها تلغي العمل المتبقي.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="5a5b8-111">إنها لا تقترح قيام المستخدم بإضافة صندوق آخر إلى المجموعة نفسها، ولا تقوم بإنشاء عمل جديد بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="5a5b8-112">تشغيل ميزة موضع المجموعة ممتلئ</span><span class="sxs-lookup"><span data-stu-id="5a5b8-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="5a5b8-113">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="5a5b8-114">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="5a5b8-115">في مساحة عمل **إدارة الميزات** ، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5a5b8-116">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5a5b8-117">**اسم الميزة:** *موضع المجموعة ممتلئ*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="5a5b8-118">الإعداد</span><span class="sxs-lookup"><span data-stu-id="5a5b8-118">Setup</span></span>

<span data-ttu-id="5a5b8-119">يوفر هذا القسم إرشادات ومثالاً يوضح كيفية إعداد الميزة *موضع المجموعة ممتلئ* واستخدامها‏‎.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="5a5b8-120">جعل بيانات العينة متاحة</span><span class="sxs-lookup"><span data-stu-id="5a5b8-120">Make sample data available</span></span>

<span data-ttu-id="5a5b8-121">للعمل عبر [السيناريو المثال](#example-scenario) باستخدام عينات البيانات والسجلات المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="5a5b8-122">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="5a5b8-123">يمكنك أيضًا استخدام السيناريو المثال كإرشادات لاستخدام هذه الميزة في نظام إنتاج.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="5a5b8-124">ولكن، وفي هذه الحالة، يجب استبدال قيمك بالإعدادات التي ورد وصفها هنا.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="5a5b8-125">ملفات تعريف نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="5a5b8-125">Cluster profiles</span></span>

<span data-ttu-id="5a5b8-126">يجب تحديد ما إذا كان سيتم إنشاء معرفات المجموعات بشكل تلقائي، وعدد المواضع التي يتم استخدامها، ومتى يتم فصل المجموعات، وكيف تتم سلسلة عملي التسليم والتحقق منه.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="5a5b8-127">انتقل إلى **إدارة المستودعات \> الإعداد \> الجهاز المحمول \> ملفات تعريف نظام المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="5a5b8-128">في جزء القائمة، حدد السجل **إنشاء مجموعة**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="5a5b8-129">في علامة التبويب السريعة **عام** ، تحقق من القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="5a5b8-130">**إنشاء معرف المجموعة:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="5a5b8-131">**تنشيط المواضع:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="5a5b8-132">**عدد المواضع:** *2*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="5a5b8-133">**اسم الموضع:** *رقمي*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="5a5b8-134">**فصل المجموعة عند:** - حدد *التخزين*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="5a5b8-135">**نوع التحقق من الفرز:** *مسح الموضع*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="5a5b8-136">على علامة التبويب السريعة **فرز المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="5a5b8-137">يجب أن تكون الشبكة فارغة (أي، يجب ألا تحتوي على خطوط).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="5a5b8-138">قوالب العمل</span><span class="sxs-lookup"><span data-stu-id="5a5b8-138">Work templates</span></span>

<span data-ttu-id="5a5b8-139">يجب عليك تحديد كيفية عمل الانتقاء لإنشاء انتقاء المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="5a5b8-140">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="5a5b8-141">في أعلى الصفحة، قم بتعيين حقل **نوع أمر العمل** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="5a5b8-142">تأكد من إدراج قوالب العمل التالية من بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="5a5b8-143">إذا لم تكن متوفرة، فلن تتمكن من إكمال السيناريو.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="5a5b8-144">61 مرحلة SO</span><span class="sxs-lookup"><span data-stu-id="5a5b8-144">61 SO Stage</span></span>
    - <span data-ttu-id="5a5b8-145">61 انتقاء مجموعة SO</span><span class="sxs-lookup"><span data-stu-id="5a5b8-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="5a5b8-146">توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="5a5b8-146">Location directives</span></span>

<span data-ttu-id="5a5b8-147">يجب تحديد مكان انتقاء الأصناف ومكان تخزينها.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="5a5b8-148">انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="5a5b8-149">في رأس القائمة، قم بتعيين الحقل **نوع أمر العمل** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="5a5b8-150">تأكد من إدراج توجيهات أمر المبيعات التالية من بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="5a5b8-151">إذا لم تكن متوفرة، فلن تتمكن من إكمال السيناريو.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="5a5b8-152">61 انتقاء مجموعة</span><span class="sxs-lookup"><span data-stu-id="5a5b8-152">61 Cluster pick</span></span>
    - <span data-ttu-id="5a5b8-153">61 انتقاء أمر SO</span><span class="sxs-lookup"><span data-stu-id="5a5b8-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="5a5b8-154">أصناف قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="5a5b8-154">Mobile device menu items</span></span>

<span data-ttu-id="5a5b8-155">يجب تكوين عنصر قائمة للجهاز المحمول لاستخدام العمل الموجود الذي يتم توجيهه بواسطة انتقاء المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="5a5b8-156">في عنصر قائمة الجهاز المحمول لانتقاء المجموعة، يجب أن تكون المعلمة **السماح بتقسيم العمل** قيد التشغيل، ويجب إضافة فئة العمل *انتقاء SO*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="5a5b8-157">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5a5b8-158">في جزء القائمة، حدد السجل **إنشاء انتقاء مجموعة**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="5a5b8-159">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="5a5b8-160">في علامة التبويب السريعة **عام** ، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5a5b8-161">**موجّه بواسطة:** *انتقاء المجموعة*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="5a5b8-162">**إنشاء لوحة الترخيص:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="5a5b8-163">**السماح بتقسيم العمل:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="5a5b8-164">**معرف ملف تعريف المجموعة:** *إنشاء مجموعة*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="5a5b8-165">اقبل القيم الافتراضية لجميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="5a5b8-166">على علامة التبويب السريعة **فئات العمل** ، أضف السطرين التاليين حسب الحاجة:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="5a5b8-167">السطر 1 (موجود عادةً في بيانات العرض التوضيحي):</span><span class="sxs-lookup"><span data-stu-id="5a5b8-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="5a5b8-168">**معرف فئة العمل:** *المبيعات*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="5a5b8-169">**نوع أمر العمل:** *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="5a5b8-170">السطر 2 (غير موجود على الأرجح في بيانات العرض التوضيحي):</span><span class="sxs-lookup"><span data-stu-id="5a5b8-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="5a5b8-171">**معرف فئة العمل:** *انتقاء SO*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="5a5b8-172">**نوع أمر العمل:** *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="5a5b8-173">انتقل إلى **إعداد تأكيد العمل** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="5a5b8-174">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-174">Select **Edit**.</span></span>
1. <span data-ttu-id="5a5b8-175">أدخل القيم التالية على السطر في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="5a5b8-176">**نوع العمل** - *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="5a5b8-177">**تأكيد المنتج** - *حدد خانة الاختيار*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="5a5b8-178">حدد **حفظ** في جزء الإجراءات وأغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="5a5b8-179">إنشاء عمل انتقاء</span><span class="sxs-lookup"><span data-stu-id="5a5b8-179">Create picking work</span></span>

<span data-ttu-id="5a5b8-180">قبل أن تتمكن من بدء تشغيل انتقاء المجموعة، يجب إنشاء بعض العمل الصادر.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="5a5b8-181">يحدد ملف تعريف نظام المجموعة الذي قمت بإنشائه سابقًا منصبين في نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="5a5b8-182">ولذلك، يجب إنشاء معرفي عمل على الأقل لانتقاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="5a5b8-183">بالنسبة لهذا السيناريو، ستحدث الحركات في المستودع *61* ، وستستخدم الأصناف *L0101* و *T0100*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-183">For this scenario, transactions will occur in warehouse *61* , and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="5a5b8-184">يلزم وجود مخزون فعلي كافٍ لهذه الأصناف في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="5a5b8-185">تأكد من وجود مخزون كافٍ لإكمال الحركات.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="5a5b8-186">إنشاء أمر مبيعات 1</span><span class="sxs-lookup"><span data-stu-id="5a5b8-186">Create sales order 1</span></span>

1. <span data-ttu-id="5a5b8-187">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5a5b8-188">حدد **جديد** لإنشاء أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="5a5b8-189">في مربع الحوار **إنشاء أمر المبيعات** ، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5a5b8-190">**حساب العميل:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="5a5b8-191">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="5a5b8-192">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-192">Select **OK**.</span></span>
1. <span data-ttu-id="5a5b8-193">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-193">The new sales order is opened.</span></span> <span data-ttu-id="5a5b8-194">على علامة التبويب السريعة **بنود أمر المبيعات** ، أضف بندًا لديه الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="5a5b8-195">**رقم الصنف:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="5a5b8-196">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="5a5b8-197">على علامة التبويب السريعة **تفاصيل البند** على علامة التبويب **تسليم** ، عيّن الحقل **تاريخ الشحن المؤكد** إلى تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="5a5b8-198">على علامة التبويب السريعة **بنود أمر المبيعات** ، أضف بندًا ثانيًا لديه الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="5a5b8-199">**رقم الصنف:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="5a5b8-200">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="5a5b8-201">على علامة التبويب السريعة **تفاصيل البند** على علامة التبويب **تسليم** ، عيّن الحقل **تاريخ الشحن المؤكد** إلى تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="5a5b8-202">بالنسبة لكل بند قمت بإضافته، اتبع الخطوات التالية لحجز المخزون:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="5a5b8-203">حدد البند المراد حجزه.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="5a5b8-204">على علامة التبويب السريعة **بنود أمر المبيعات** ، حدد **المخزون‏‎ \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="5a5b8-205">في صفحة **الحجز** ، في جزء الإجراءات حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="5a5b8-206">أغلق صفحة **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="5a5b8-207">في جزء الإجراءات، ضمن علامة التبويب **المستودع** ، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5a5b8-208">عند اكتمال الإصدار، سوف تستلم رسائل معلوماتية تعرض معرف الموجة ومعرف حمل العمل اللذين تم إنشاؤهما.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="5a5b8-209">إنشاء أمر مبيعات 2</span><span class="sxs-lookup"><span data-stu-id="5a5b8-209">Create sales order 2</span></span>

1. <span data-ttu-id="5a5b8-210">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5a5b8-211">حدد **جديد** لإنشاء أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="5a5b8-212">في مربع الحوار **إنشاء أمر المبيعات** ، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5a5b8-213">**حساب العميل:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="5a5b8-214">**المستودع:** *61*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="5a5b8-215">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-215">Select **OK**.</span></span>
1. <span data-ttu-id="5a5b8-216">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-216">The new sales order is opened.</span></span> <span data-ttu-id="5a5b8-217">على علامة التبويب السريعة **بنود أمر المبيعات** ، أضف بندًا لديه الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="5a5b8-218">**رقم الصنف:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="5a5b8-219">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="5a5b8-220">على علامة التبويب السريعة **تفاصيل البند** على علامة التبويب **تسليم** ، عيّن الحقل **تاريخ الشحن المؤكد** إلى تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="5a5b8-221">على علامة التبويب السريعة **بنود أمر المبيعات** ، أضف بندًا ثانيًا لديه الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="5a5b8-222">**رقم الصنف:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="5a5b8-223">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="5a5b8-224">على علامة التبويب السريعة **تفاصيل البند** على علامة التبويب **تسليم** ، عيّن الحقل **تاريخ الشحن المؤكد** إلى تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="5a5b8-225">بالنسبة لكل بند قمت بإضافته، اتبع الخطوات التالية لحجز المخزون:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="5a5b8-226">حدد البند المراد حجزه.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="5a5b8-227">على علامة التبويب السريعة **بنود أمر المبيعات** ، حدد **المخزون‏‎ \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="5a5b8-228">في صفحة **الحجز** ، في جزء الإجراءات حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="5a5b8-229">أغلق صفحة **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="5a5b8-230">في جزء الإجراءات، ضمن علامة التبويب **المستودع** ، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5a5b8-231">عند اكتمال الإصدار، سوف تستلم رسائل معلوماتية تعرض معرف الموجة ومعرف حمل العمل اللذين تم إنشاؤهما.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="5a5b8-232">الحصول على معرفات العمل وأرقام لوحات الترخيص</span><span class="sxs-lookup"><span data-stu-id="5a5b8-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="5a5b8-233">من المفترض أن يكون قد تم إنشاء معرفين للعمل، مع وجود بندي انتقاء لكل واحد منهما.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="5a5b8-234">اتبع الخطوات التالية للعثور على معرفات العمل وتعيينات لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="5a5b8-235">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="5a5b8-236">في شبكة **النظرة العامة** ، ابحث عن العمود **رقم الأمر** لأمري المبيعات اللذين قمت بإنشائهما.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="5a5b8-237">لكل أمر مبيعات، يمكنك تدوين معرف العمل المناظر.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="5a5b8-238">حدد الصف الخاص بكل أمر عمل لإظهار المعلومات المرتبطة به في شبكة **البنود**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="5a5b8-239">دوّن الموقع الذي سيتم انتقاء كل صنف منه.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="5a5b8-240">انتقل إلى **إدارة المخزون \> الاستعلامات والتقارير \> قائمة المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="5a5b8-241">في جزء الإجراءات، حدد **الأبعاد** لفتح مربع حوار **عرض البُعد**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="5a5b8-242">تأكد من تحديد خانات الاختيار **لوحة الترخيص** و **المستودع** و **رقم الصنف** ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-242">Make sure that the **License plate** , **Warehouse** , and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="5a5b8-243">في جزء **التصفية** ، قم بتعيين عوامل التصفية التالية:</span><span class="sxs-lookup"><span data-stu-id="5a5b8-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="5a5b8-244">**رقم الصنف** – **هو واحد من** – *L0101* و *T100*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="5a5b8-245">**المستودع** – **يبدأ بـ** – *61*</span><span class="sxs-lookup"><span data-stu-id="5a5b8-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="5a5b8-246">دوّن قيم **لوحة الترخيص** التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="5a5b8-247">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="5a5b8-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="5a5b8-248">تنفيذ سير مهام الجهاز المحمول - إعداد تأكيد العمل للمنتج</span><span class="sxs-lookup"><span data-stu-id="5a5b8-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="5a5b8-249">سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *61*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="5a5b8-250">انتقل إلى **الصادر \> إنشاء انتقاء مجموعة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="5a5b8-251">تظهر الصفحة **المهمة: تعيين العمل إلى المجموعة** .</span><span class="sxs-lookup"><span data-stu-id="5a5b8-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="5a5b8-252">أدخل معرف العمل لأمر المبيعات 1 لتعيينه إلى موضع المجموعة 1.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="5a5b8-253">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-254">أدخل معرف العمل لأمر المبيعات 2 لتعيينه إلى موضع المجموعة 2.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="5a5b8-255">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="5a5b8-256">تظهر الصفحة **المهمة: إنشاء انتقاء مجموعة‬‏‫: انتقاء** وتعرض *الصنف L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="5a5b8-257">لأن ملف تعريف المجموعة عيّن عدد المواضع إلى 2، يوجهك النظام بشكل تلقائي إلى الانتقاء المدمج الأول: 2 بالتات للصنف *L0101*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="5a5b8-258">في أي وقت خلال الخطوات التالية، يمكنك تحديد علامة التبويب **التفاصيل** لعرض معلومات إضافية حول المهمة، مثل موقع الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="5a5b8-259">عيِّن الحقل **الصنف** إلى *L0101*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="5a5b8-260">وهذا يؤكد على رقم الصنف المطلوب لعنصر القائمة هذا (قمت بتكوينه في وقت سابق من خلال تحديد **إعداد تأكيد العمل** من صفحة **عنصر قائمة الجهاز المحمول** عندما أنشأت عنصر القائمة هذا).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="5a5b8-261">أدخل رقم لوحة الترخيص المرتبط بالصنف في الموقع الذي يجري الانتقاء منه.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="5a5b8-262">ستنتقي إثنتين من البالتات.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="5a5b8-263">عيّن الحقل **LP** إلى *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="5a5b8-264">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="5a5b8-265">تظهر صفحة **المهمة: فرز: إنشاء انتقاء مجموعة** ‬‏‫ .</span><span class="sxs-lookup"><span data-stu-id="5a5b8-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="5a5b8-266">هنا، هنا يتم فرز البالتات الإثنتين اللتين تم انتقاؤهما في موضع الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="5a5b8-267">قد يكون هذا الموضع عبارة عن صندوق أو حاوية يتم استخدامها لفصل المخزون المستلم حسب أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="5a5b8-268">استعرض التفاصيل التي تظهر للصنف ( *L0101* ) والكمية ( *20* ea) التي سيتم فرزها في الموضع 1 (لأمر المبيعات 1).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-268">View the details that are shown for the item ( *L0101* ) and quantity ( *20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="5a5b8-269">عيّن الحقل **POSITION NA** إلى *1*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="5a5b8-270">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-271">استعرض التفاصيل التي تظهر للصنف ( *L0101* ) والكمية ( *20* ea) التي سيتم فرزها في الموضع 2 (لأمر المبيعات 2).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-271">View the details that are shown for the item ( *L0101* ) and quantity ( *20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="5a5b8-272">عيّن الحقل **POSITION NA** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="5a5b8-273">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="5a5b8-274">تظهر الصفحة **المهمة: إنشاء انتقاء مجموعة‬‏‫: انتقاء** وتعرض *الصنف T0100 7 ea*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="5a5b8-275">في هذا السيناريو، لا يمكن للموضع 1 قبول الكمية الكاملة للأصناف التي يجب انتقاؤها لتنفيذ أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="5a5b8-276">يجب وضع علامة ممتلئ على الموضع.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-276">A position must be marked as full.</span></span> <span data-ttu-id="5a5b8-277">في هذا السيناريو، ستقوم بانتقاء جزئي للصنف الثاني.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="5a5b8-278">سيتم انتقاء الصنف الثاني جزئيًا للموضع 1، وسيتم إنشاء عمل جديد لانتقاء الكمية المتبقية لتنفيذ الأمر.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="5a5b8-279">حدد زر القائمة (أحيانًا يُشار إليه بهامبورجير أو الزر هامبورجير)، ثم حدد **الموضع ممتلئ**.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="5a5b8-280">حدد الموضع الممتلئ، وحدد *1*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="5a5b8-281">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-282">أدخل كمية الانتقاء والكمية التي لا زال من الممكن انتقاؤها في الموضع 1.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="5a5b8-283">يمكن للنظام تحديد رقم الصنف الذي يتم انتقاؤه.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="5a5b8-284">أدخل *2*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-284">Enter *2*.</span></span>
1. <span data-ttu-id="5a5b8-285">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-286">قم بتأكيد رقم الصنف لإكمال انتقاء الصنف المتبقي إلى الموضع 2.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="5a5b8-287">عيِّن الحقل **الصنف** إلى *T0100*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="5a5b8-288">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-289">أدخل لوحة الترخيص التي يجري انتقاء الصنف منها عن طريق تعيين الحقل **LP** إلى *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="5a5b8-290">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-291">استعرض التفاصيل التي تظهر للصنف ( *T0100* ) والكمية ( *2* ea) التي سيتم فرزها في الموضع 2 (لأمر المبيعات 2).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-291">View the details that are shown for the item ( *T0100* ) and quantity ( *2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="5a5b8-292">عيّن الحقل **POSITION NA** إلى *2*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="5a5b8-293">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="5a5b8-294">استعرض التفاصيل التي تظهر للصنف ( *T0100* ) والكمية ( *2* ea) التي سيتم فرزها في الموضع 1 (لأمر المبيعات 1).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-294">View the details that are shown for the item ( *T0100* ) and quantity ( *2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="5a5b8-295">عيّن الحقل **POSITION NA** إلى *1*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="5a5b8-296">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="5a5b8-297">تظهر صفحة **المهمة: إنشاء انتقاء مجموعة: تخزين** ‬‏‫ .</span><span class="sxs-lookup"><span data-stu-id="5a5b8-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="5a5b8-298">في هذا السيناريو، تم إكمال انتقاء المجموعة، ويتم توجيه المستخدم لتخزين الأصناف المنتقاة من الموضع 1 والموضع 2 في موقع مرحلي *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="5a5b8-299">راجع المعلومات الموجودة في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-299">Review the information on the page.</span></span> <span data-ttu-id="5a5b8-300">توضح هذه المعلومات أنه سيتم تخزين الكمية الإجمالية *44* في موقع مرحلي.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="5a5b8-301">حدد **موافق** (رمز علامة الاختيار).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="5a5b8-302">سوف تستلم رسالة "اكتمل التجميع".</span><span class="sxs-lookup"><span data-stu-id="5a5b8-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="5a5b8-303">يمكنك الآن استخدام عنصر قائمة **انتقاء المبيعات** لانتقاء الكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="5a5b8-304">يمكنك بعدئذٍ استخدام عنصر قائمة **تحميل المبيعات** لنقل الأصناف من الموقع المرحلي إلى رصيف التحميل.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
