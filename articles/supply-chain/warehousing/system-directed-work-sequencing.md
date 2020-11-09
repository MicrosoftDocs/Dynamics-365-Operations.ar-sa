---
title: تسلسل العمل الموجه بواسطة النظام
description: يوفر هذا الموضوع معلومات حول تسلسل العمل الموجه بواسطة النظام. تتيح لك هذه الوظيفة فرز وتصفية أوامر العمل التي يقدمها النظام للمستخدمين ليتم تنفيذها. وهي مفيدو في السيناريوهات التي يُطلب فيها معايير إضافية لتوجيه عملية الانتقاء من المستودع.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017013"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="e1072-105">تسلسل العمل الموجه بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="e1072-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1072-106">يتيح لك تسلسل العمل الموجه من النظام فرز وتصفية أوامر العمل التي يقدمها النظام للمستخدمين ليتم تنفيذها.</span><span class="sxs-lookup"><span data-stu-id="e1072-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="e1072-107">وهي مفيدة في السيناريوهات التي تتطلب معايير إضافية (مثل وقت الشحن، أو منطقة الانتقاء، أو ملف تعريف الموقع، أو مجموعة من المعايير المتعددة) لتوجيه عملية الانتقاء من المستودع.</span><span class="sxs-lookup"><span data-stu-id="e1072-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="e1072-108">تقوم هذه الوظيفة بتوسيع وظيفة الانتقاء الموجه من النظام الحالية عن طريق إضافة أمر استعلام موجه من النظام؛ حيث يمكن للمستخدمين إعداد تسلسل واستعلام واحد أو أكثر والذي سيقوم بتقييم كافة أوامر العمل التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="e1072-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="e1072-109">لن يتم التقاط وتقديم إلا أوامر العمل التي تفي بالمعايير المحددة في إعداد عنصر قائمة جهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="e1072-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="e1072-110">لذلك، تتيح هذه الوظيفة تحسينًا إضافيًا لعمليات الانتقاء من المستودع حيث تحدد أوامر العمل التي تطابق المعايير المحددة، وتعيينها إلى عنصر قائمة الأجهزة المحمولة الصحيح، ثم تقدمها للعامل، استنادًا إلى مجموعة محددة من المهارات أو معدات انتقاء أو متطلبات أخرى.</span><span class="sxs-lookup"><span data-stu-id="e1072-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="e1072-111">في حالة الحاجة إلى معايير مختلفة، يجب استخدام عدة عناصر لقائمة الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="e1072-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="e1072-112">تشغيل ميزة تسلسل العمل الموجه بواسطة النظام على مستوى المؤسسة</span><span class="sxs-lookup"><span data-stu-id="e1072-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="e1072-113">قبل أن تتمكن من استخدام ميزة تسلسل العمل الموجه بواسطة النظام، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e1072-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="e1072-114">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e1072-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e1072-115">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e1072-116">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="e1072-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e1072-117">**اسم الميزة:** *تسلسل العمل الموجه بواسطة النظام على مستوى المؤسسة*</span><span class="sxs-lookup"><span data-stu-id="e1072-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="e1072-118">الإعداد</span><span class="sxs-lookup"><span data-stu-id="e1072-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e1072-119">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="e1072-119">Make demo data available</span></span>

<span data-ttu-id="e1072-120">للعمل في السيناريو باستخدام القيم المقدمة في هذا الموضوع يجب أن تعمل على نظام تم تثبيت البيانات القياسية التوضيحية عليه.</span><span class="sxs-lookup"><span data-stu-id="e1072-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="e1072-121">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF**.</span><span class="sxs-lookup"><span data-stu-id="e1072-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="e1072-122">يستخدم السيناريو المستودع *51* من البيانات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="e1072-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1072-123">قبل أن تقوم بإصدار الأوامر إلى المستودع، تأكد من أن مواقع الانتقاء لديها مخزون كاف لكافة الأصناف الموجودة على كافة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="e1072-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="e1072-124">يجب أن تدعم بيانات USMF الافتراضية هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="e1072-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="e1072-125">إذا كنت تستخدم البيانات التوضيحية، فراجع إعداد **توجيه الموقع** لمعرفة ما هي مواقع الانتقاء التي يتم استخدامها لانتقاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="e1072-126">إذا كان من الضروري تسوية المخزون، فيمكنك إنشاء حركات يدوية أو استخدام تزويد أو استخدام أي سير عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="e1072-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="e1072-127">إعداد عنصر قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="e1072-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="e1072-128">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="e1072-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e1072-129">في قائمة عناصر قائمة الجهاز المحمول، حدد **انتقاء المبيعات - النظام**.</span><span class="sxs-lookup"><span data-stu-id="e1072-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="e1072-130">يجب أن يكون عنصر القائمة المطلوب موجودًا بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e1072-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="e1072-131">أكد الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="e1072-132">في علامة التبويب السريعة **عام** ، يجب تعيين الحقل **موجه بواسطة** إلى *النظام الذي تم التوجيه إليه*.</span><span class="sxs-lookup"><span data-stu-id="e1072-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="e1072-133">يجب أن تعرض علامة التبويب السريعة **فئات العمل** الإعدادات التالية.</span><span class="sxs-lookup"><span data-stu-id="e1072-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="e1072-134">معرف فئة العمل</span><span class="sxs-lookup"><span data-stu-id="e1072-134">Work class ID</span></span> | <span data-ttu-id="e1072-135">نوع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="e1072-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="e1072-136">مبيعات</span><span class="sxs-lookup"><span data-stu-id="e1072-136">Sales</span></span> | <span data-ttu-id="e1072-137">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="e1072-137">Sales orders</span></span> |
        | <span data-ttu-id="e1072-138">انتقاء SO</span><span class="sxs-lookup"><span data-stu-id="e1072-138">SO Pick</span></span> | <span data-ttu-id="e1072-139">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="e1072-139">Sales orders</span></span> |

1. <span data-ttu-id="e1072-140">في جزء الإجراءات، حدد **استعلامات تسلسل العمل الموجه بواسطة النظام**.</span><span class="sxs-lookup"><span data-stu-id="e1072-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="e1072-141">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e1072-141">Select **Edit**.</span></span>
1. <span data-ttu-id="e1072-142">قم بحذف البند الموجود، ثم أكد الإجراء عن طريق تحديد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e1072-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="e1072-143">في جزء الإجراءات، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="e1072-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="e1072-144">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1072-145">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="e1072-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="e1072-146">**حقل الوصف:** *كمية العمل أقل من 20 وتنازلي*</span><span class="sxs-lookup"><span data-stu-id="e1072-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="e1072-147">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e1072-147">Select **Save**.</span></span>
1. <span data-ttu-id="e1072-148">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="e1072-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="e1072-149">في علامة التبويب **صلات** ، قم بتوسيع التسلسل الهرمي للصلات لإظهار جدول **بنود العمل**.</span><span class="sxs-lookup"><span data-stu-id="e1072-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="e1072-150">حدد صلة جدول **بنود العمل**.</span><span class="sxs-lookup"><span data-stu-id="e1072-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="e1072-151">حدد **إضافة انضمام جدول**.</span><span class="sxs-lookup"><span data-stu-id="e1072-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="e1072-152">في القائمة التي تظهر، ابحث عن الصف الذي يحتوي على الإعدادات التالية وقم بتحديده:</span><span class="sxs-lookup"><span data-stu-id="e1072-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="e1072-153">**وضع الصلة:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="e1072-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="e1072-154">**العلاقة:** *المواقع (الموقع)*</span><span class="sxs-lookup"><span data-stu-id="e1072-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="e1072-155">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="e1072-155">Select **Select**.</span></span>

    <span data-ttu-id="e1072-156">تتم إضافة المواقع إلى صلة الجدول.</span><span class="sxs-lookup"><span data-stu-id="e1072-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="e1072-157">في علامة التبويب **الفرز** ، حدد **إضافة** لإضافة سطر جديد.</span><span class="sxs-lookup"><span data-stu-id="e1072-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="e1072-158">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1072-159">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e1072-160">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e1072-161">**الحقل:** *كمية العمل* (في مربع الرسالة التي تظهر، حدد **نعم** لإضافة الفرز إلى هذا الحقل.)</span><span class="sxs-lookup"><span data-stu-id="e1072-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="e1072-162">**اتجاه البحث:** *تنازلي*</span><span class="sxs-lookup"><span data-stu-id="e1072-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="e1072-163">حدد علامة التبويب **النطاق**.</span><span class="sxs-lookup"><span data-stu-id="e1072-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="e1072-164">إذا كان يجب تضمين معايير عمل محددة في التسلسل، فيمكنك تحديدها في علامة تبويب **النطاق**. في هذا المثال، تريد تضمين العمل فقط الذي تكون كميته أقل من 20 وحدة (أقل وحدة قياس).</span><span class="sxs-lookup"><span data-stu-id="e1072-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="e1072-165">لاحظ أن بعض البنود قد تم تضمينها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e1072-165">Notice that some lines are already included.</span></span> <span data-ttu-id="e1072-166">يجب عدم إزالة هذه البنود.</span><span class="sxs-lookup"><span data-stu-id="e1072-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="e1072-167">حدد **إضافة** لإضافة سطر.</span><span class="sxs-lookup"><span data-stu-id="e1072-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="e1072-168">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1072-169">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e1072-170">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e1072-171">**الحقل:** *كمية عمل المخزون*</span><span class="sxs-lookup"><span data-stu-id="e1072-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="e1072-172">**المعايير:** *\<20* (أقل من 20)</span><span class="sxs-lookup"><span data-stu-id="e1072-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="e1072-173">حدد **إضافة** لإضافة سطر آخر.</span><span class="sxs-lookup"><span data-stu-id="e1072-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="e1072-174">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1072-175">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e1072-176">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e1072-177">**الحقل:** *نوع العمل*</span><span class="sxs-lookup"><span data-stu-id="e1072-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e1072-178">**المعايير:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="e1072-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="e1072-179">حدد **إضافة** لإضافة سطر آخر.</span><span class="sxs-lookup"><span data-stu-id="e1072-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="e1072-180">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1072-181">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="e1072-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="e1072-182">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="e1072-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="e1072-183">**الحقل:** *معرف ملف الموقع*</span><span class="sxs-lookup"><span data-stu-id="e1072-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="e1072-184">**المعايير:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="e1072-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="e1072-185">تأكد من تضمين علامة التعجب ( *!* ) أمام *STAGE*.</span><span class="sxs-lookup"><span data-stu-id="e1072-185">Be sure to include the exclamation point ( *!* ) in front of *STAGE*.</span></span>

1. <span data-ttu-id="e1072-186">حدد **موافق** لحفظ الاستعلام وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="e1072-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="e1072-187">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e1072-187">Select **Save**.</span></span>
1. <span data-ttu-id="e1072-188">أغلق الصفحة للعودة إلى صفحة **عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="e1072-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="e1072-189">يحدد هذا الإعداد المعايير التي سيتم استخدامها لتغذية العمل المؤهل بعنصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="e1072-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="e1072-190">إذا قمت بإضافة المزيد من بنود المعايير إلى الاستعلام، فسيقوم النظام باستخدام بند الاستعلام الذي له رقم التسلسل الأقل أولا.</span><span class="sxs-lookup"><span data-stu-id="e1072-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="e1072-191">بمعنى آخر، سيتم تقديم كافة الأعمال المؤهلة لرقم التسلسل 1 إلى المستخدم أولا، ثم كل أعمال رقم التسلسل 2.</span><span class="sxs-lookup"><span data-stu-id="e1072-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="e1072-192">بالتالي، إذا كان من الضروري استخدام نطاق فرز معين معًا، فيجب تحديدهما في نفس استعلام تسلسل العمل الموجه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="e1072-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="e1072-193">سيقوم هذا الإعداد بالتقاط أي عمل يحتوي على بند واحد على الأقل حيث تكون الكمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="e1072-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="e1072-194">بالتالي، إذا كان العمل يحتوي على بند تكون فيه الكمية هي 20 وحدة بالضبط أو أكثر من 20 وحدة، فإنه سيكون صالحا، بشرط أن يحتوي أيضا على بند واحد على الأقل حيث تكون الكمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="e1072-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="e1072-195">توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="e1072-195">Location directives</span></span>

<span data-ttu-id="e1072-196">إذا كنت تستخدم بيانات شركة Contoso الافتراضية، فلن يتطلب الاستعلام عن الإجراء الموجة إلى الموقع القيام بأي تغييرات.</span><span class="sxs-lookup"><span data-stu-id="e1072-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="e1072-197">مع ذلك، للتأكد من أن توجيهات المواقع ستقوم بالتقاط الأصناف الموجودة في أوامر المبيعات عند تطبيق الميزة في بيئة خلاف Contoso، قم بإنشاء توجيه موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="e1072-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="e1072-198">للتحقق من الإعدادات في بيئة العرض التوضيحي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e1072-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="e1072-199">انتقل إلى **إدارة المستودعات‬** \> **الإعداد** \> **موجهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="e1072-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="e1072-200">في الحقل **نوع أمر العمل** ، حدد *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="e1072-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="e1072-201">حدد التوجيه الخاص بالموقع الذي يسمى *51 الانتقاء*.</span><span class="sxs-lookup"><span data-stu-id="e1072-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="e1072-202">في علامة التبويب السريعة **إجراءات توجيه الموقع** ، حدد السطر الخاص بالإجراء **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="e1072-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="e1072-203">حدد **تحرير استعلام** فوق الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e1072-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="e1072-204">راجع استعلام **النطاق**.</span><span class="sxs-lookup"><span data-stu-id="e1072-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="e1072-205">ابحث عن البند الذي تم فيه تعيين حقل **الحقل** إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="e1072-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="e1072-206">تأكد من أن حقل **المعايير** فارغ (أي أنه لا توجد قيود).</span><span class="sxs-lookup"><span data-stu-id="e1072-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="e1072-207">سيناريو</span><span class="sxs-lookup"><span data-stu-id="e1072-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="e1072-208">إنشاء عمل انتقاء لأمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="e1072-208">Create sales order picking work</span></span>

<span data-ttu-id="e1072-209">قبل تشغيل الانتقاء الموجه بواسطة النظام، يجب إنشاء بعض العمل الصادر.</span><span class="sxs-lookup"><span data-stu-id="e1072-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="e1072-210">في هذا السيناريو، ستقوم بإنشاء أربعة أوامر مبيعات تستند إلى استعلامات محددة لتسلسل العمل الموجه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="e1072-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="e1072-211">عليك حجز كميات مخزون لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="e1072-212">بالتالي، لا يمكن سحب المخزون المحجوز من المستودع لأوامر أخرى إلا إذا تم إلغاء حجز المخزون أو جزء منه.</span><span class="sxs-lookup"><span data-stu-id="e1072-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="e1072-213">ستقوم بعد ذلك بإصدار كل أمر مبيعات للمستودع لإنشاء العمل الصادر.</span><span class="sxs-lookup"><span data-stu-id="e1072-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="e1072-214">أمر المبيعات 1</span><span class="sxs-lookup"><span data-stu-id="e1072-214">Sales order 1</span></span>

1. <span data-ttu-id="e1072-215">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="e1072-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e1072-216">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="e1072-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="e1072-217">في مربع الحوار **إنشاء أمر المبيعات** ، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e1072-218">في قسم **العميل** ، قم بتعيين حقل **حساب العميل** إلى *US-004*.</span><span class="sxs-lookup"><span data-stu-id="e1072-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="e1072-219">في القسم **عام** ، قم بتعيين حقل **المستودع** إلى *51*.</span><span class="sxs-lookup"><span data-stu-id="e1072-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="e1072-220">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="e1072-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="e1072-221">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e1072-222">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="e1072-223">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="e1072-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="e1072-224">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="e1072-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="e1072-225">في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="e1072-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e1072-226">في صفحة **الحجز** ، حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="e1072-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="e1072-227">أغلق صفحة **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="e1072-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="e1072-228">في جزء الإجراءات، ضمن علامة التبويب **المستودع** ، حدد **إصدار إلى المستودع‬** لإنشاء عمل للمستودع.</span><span class="sxs-lookup"><span data-stu-id="e1072-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="e1072-229">سوف تستلم رسائل معلوماتية تعرض معرف الموجة ومعرفات الشحنة التي تم إنشاؤها لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="e1072-230">أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="e1072-230">Sales order 2</span></span>

1. <span data-ttu-id="e1072-231">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="e1072-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="e1072-232">في مربع الحوار **إنشاء أمر المبيعات** ، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e1072-233">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e1072-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e1072-234">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="e1072-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="e1072-235">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="e1072-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="e1072-236">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e1072-237">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="e1072-238">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="e1072-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="e1072-239">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="e1072-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="e1072-240">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="e1072-241">**رقم الصنف:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="e1072-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="e1072-242">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="e1072-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e1072-243">احجز المخزون لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="e1072-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="e1072-244">قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="e1072-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="e1072-245">أمر المبيعات 3</span><span class="sxs-lookup"><span data-stu-id="e1072-245">Sales order 3</span></span>

1. <span data-ttu-id="e1072-246">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 3.</span><span class="sxs-lookup"><span data-stu-id="e1072-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="e1072-247">في مربع الحوار **إنشاء أمر المبيعات** ، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e1072-248">**حساب العميل:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="e1072-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="e1072-249">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="e1072-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="e1072-250">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="e1072-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="e1072-251">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e1072-252">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="e1072-253">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="e1072-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="e1072-254">**الكمية:** *7*</span><span class="sxs-lookup"><span data-stu-id="e1072-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="e1072-255">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="e1072-256">**رقم الصنف:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="e1072-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="e1072-257">**الكمية:** *8*</span><span class="sxs-lookup"><span data-stu-id="e1072-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="e1072-258">احجز المخزون لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="e1072-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="e1072-259">قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="e1072-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="e1072-260">أمر المبيعات 4</span><span class="sxs-lookup"><span data-stu-id="e1072-260">Sales order 4</span></span>

1. <span data-ttu-id="e1072-261">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 4.</span><span class="sxs-lookup"><span data-stu-id="e1072-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="e1072-262">في مربع الحوار **إنشاء أمر المبيعات** ، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e1072-263">**حساب العميل:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="e1072-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="e1072-264">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="e1072-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="e1072-265">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="e1072-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="e1072-266">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e1072-267">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="e1072-268">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="e1072-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="e1072-269">**الكمية:** *25*</span><span class="sxs-lookup"><span data-stu-id="e1072-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="e1072-270">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e1072-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="e1072-271">**رقم الصنف:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="e1072-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="e1072-272">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="e1072-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="e1072-273">احجز المخزون لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="e1072-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="e1072-274">قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="e1072-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="e1072-275">الحصول على معرفات العمل للعمل الذي تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="e1072-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="e1072-276">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="e1072-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="e1072-277">قم بالتصفية حسب حقل **المستودع** بحيث يتم عرض العمل الخاص بالمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="e1072-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="e1072-278">ينبغي أن يتم إنشاء أربع معرفات عمل.</span><span class="sxs-lookup"><span data-stu-id="e1072-278">Four work IDs should have been created.</span></span> <span data-ttu-id="e1072-279">قم بتدوين معرف العمل لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1072-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="e1072-280">مُعرف أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="e1072-280">Sales order ID</span></span> | <span data-ttu-id="e1072-281">معرف العمل</span><span class="sxs-lookup"><span data-stu-id="e1072-281">Work ID</span></span> | <span data-ttu-id="e1072-282">كمية العمل</span><span class="sxs-lookup"><span data-stu-id="e1072-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="e1072-283">أمر المبيعات 1</span><span class="sxs-lookup"><span data-stu-id="e1072-283">Sales Order 1</span></span> | <span data-ttu-id="e1072-284">معرف العمل 1</span><span class="sxs-lookup"><span data-stu-id="e1072-284">Work ID 1</span></span> | <span data-ttu-id="e1072-285">20 وحدة</span><span class="sxs-lookup"><span data-stu-id="e1072-285">20 ea</span></span> |
    | <span data-ttu-id="e1072-286">أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="e1072-286">Sales Order 2</span></span> | <span data-ttu-id="e1072-287">معرف العمل 2</span><span class="sxs-lookup"><span data-stu-id="e1072-287">Work ID 2</span></span> | <span data-ttu-id="e1072-288">6 وحدات (مجموع كلا السطرين)</span><span class="sxs-lookup"><span data-stu-id="e1072-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="e1072-289">أمر المبيعات 3</span><span class="sxs-lookup"><span data-stu-id="e1072-289">Sales Order 3</span></span> | <span data-ttu-id="e1072-290">معرف العمل 3</span><span class="sxs-lookup"><span data-stu-id="e1072-290">Work ID 3</span></span> | <span data-ttu-id="e1072-291">15 وحدة (مجموع كلا السطرين)</span><span class="sxs-lookup"><span data-stu-id="e1072-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="e1072-292">أمر المبيعات 4</span><span class="sxs-lookup"><span data-stu-id="e1072-292">Sales Order 4</span></span> | <span data-ttu-id="e1072-293">معرف العمل 4</span><span class="sxs-lookup"><span data-stu-id="e1072-293">Work ID 4</span></span> | <span data-ttu-id="e1072-294">35 وحدة (مجموع كلا السطرين)</span><span class="sxs-lookup"><span data-stu-id="e1072-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="e1072-295">قبل تشغيل سير العمل على الجهاز المحمول، تأكد من أن العمل الذي قمت بإنشائه للتو بالحالة *مفتوح* للمستودع *51* ونوع أمر العمل *أمر مبيعات*.</span><span class="sxs-lookup"><span data-stu-id="e1072-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="e1072-296">خلاف ذلك، قد تختلف نتائج الاختبار، لأن الانتقاء المباشر من النظام سيتضمن كافة العمل المؤهل.</span><span class="sxs-lookup"><span data-stu-id="e1072-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="e1072-297">الانتقال إلى **إدارة المستودعات \> العمل \> الصادر \> عمل المبيعات المفتوح**.</span><span class="sxs-lookup"><span data-stu-id="e1072-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="e1072-298">في شبكة **عمل المبيعات المفتوح** ، بالتصفية حسب حقل **المستودع** بحيث يتم فقط عرض العمل الخاص بالمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="e1072-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="e1072-299">تأكد من أنه تم عرض معرفات العمل الأربع التي قمت بإنشائها مسبقا فقط.</span><span class="sxs-lookup"><span data-stu-id="e1072-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="e1072-300">أغلق صفحة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="e1072-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="e1072-301">تنفيذ سير عمل الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="e1072-301">Mobile device flow execution</span></span>

<span data-ttu-id="e1072-302">واستنادا إلى الإعداد، سيقوم النظام بتغذيه عمل المستخدم الذي تم فرزه من أعلى كمية لبند العمل إلى الأقل.</span><span class="sxs-lookup"><span data-stu-id="e1072-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="e1072-303">ستكون الكمية في كل بند أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="e1072-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="e1072-304">تذكر أن هذا الإعداد سوف يلتقط أي عمل يحتوي على بند واحد على الأقل حيث تكون الكمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="e1072-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="e1072-305">بالتالي، إذا كان العمل يحتوي على بند آخر حيث تكون الكمية 20 وحدة بالضبط أو أكثر من 20 وحدة، فسيكون صالحًا أيضًا.</span><span class="sxs-lookup"><span data-stu-id="e1072-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="e1072-306">تطبيق الجوال</span><span class="sxs-lookup"><span data-stu-id="e1072-306">Mobile app</span></span>

1. <span data-ttu-id="e1072-307">سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="e1072-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="e1072-308">انتقل إلى **الصادر \> انتقاء المبيعات - النظام**.</span><span class="sxs-lookup"><span data-stu-id="e1072-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="e1072-309">يتم تقديم خطوة الانتقاء لمعرف العمل *4*.</span><span class="sxs-lookup"><span data-stu-id="e1072-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="e1072-310">يتم تقديم معرف العمل هذا أولا بسبب إعداد أمر الاستعلام الموجه بواسطة النظام، حيث حددت أن يجب عمل تسلسل للعمل استنادًا إلى كمية بند العمل التنازلية.</span><span class="sxs-lookup"><span data-stu-id="e1072-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="e1072-311">أكمل الانتقاء والوضع المطلوب لإغلاق معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="e1072-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="e1072-312">بعد ذلك، يتم تقديم معرف العمل *3*.</span><span class="sxs-lookup"><span data-stu-id="e1072-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="e1072-313">ويكون أحد بنود العمل الخاصة به تاليًا في التسلسل، استنادًا إلى كمية بند العمل.</span><span class="sxs-lookup"><span data-stu-id="e1072-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="e1072-314">أكمل الانتقاء والوضع لإغلاق معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="e1072-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="e1072-315">بعد ذلك، يتم تقديم معرف العمل *2*.</span><span class="sxs-lookup"><span data-stu-id="e1072-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="e1072-316">يكون بند انتقاء العمل هذا تاليًا في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="e1072-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="e1072-317">أكمل الانتقاء والوضع لإغلاق معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="e1072-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="e1072-318">ولا تظهر لك أي أعمال إضافية.</span><span class="sxs-lookup"><span data-stu-id="e1072-318">No further work should be presented to you.</span></span> <span data-ttu-id="e1072-319">معرف العمل *1* ليس مؤهلا لعنصر قائمة الجهاز المحمول هذا، نظرا لأن الاستعلام يحدد أن رؤوس العمل تعتبر فقط إذا كانت الكمية الموجودة في بنود العمل أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="e1072-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="e1072-320">تلميحات</span><span class="sxs-lookup"><span data-stu-id="e1072-320">Tips</span></span>

<span data-ttu-id="e1072-321">تكون استعلامات تسلسل العمل الموجه بواسطة النظام *شمولية*.</span><span class="sxs-lookup"><span data-stu-id="e1072-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="e1072-322">ومن المهم أن تتذكر هذه الحقيقة لبعض الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="e1072-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="e1072-323">على سبيل المثال، عندما تريد فقط أن يعالج عنصر قائمة معين العمل الذي بالوحدة *وحدة* ، وقمت بتحديد هذا القيد في علامة تبويب **النطاق** الخاص بالاستعلام.</span><span class="sxs-lookup"><span data-stu-id="e1072-323">For example, you want a specific menu item to process only work where the work unit is *ea* , and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="e1072-324">في هذه الحالة، سيتم تغذية كل العمل الذي يحتوي بند عمل واحد على الأقل فيه على وحد العمل *الوحدة* للعامل.</span><span class="sxs-lookup"><span data-stu-id="e1072-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="e1072-325">بالتالي، قد يتضمن هذا العمل أيضا العمل الذي تحتوي بنود العمل به على وحدة عمل خلاف *الوحدة* (مثل *صندوق* أو *بالتة* ).</span><span class="sxs-lookup"><span data-stu-id="e1072-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet* ).</span></span> <span data-ttu-id="e1072-326">سيقوم الاستعلام باستبعاد فقط العمل الذي لم يتم تعيين وحدة العمل لأي بند عمل به على *الوحدة*.</span><span class="sxs-lookup"><span data-stu-id="e1072-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="e1072-327">بالتالي، في المثال من هذا السيناريو، يتم أيضًا التقاط معرف العمل *4* بواسطة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="e1072-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="e1072-328">وعندما تم إنشاؤه، تمت إضافة بندين: واحد لـ 25 وحدة وآخر لـ 10 وحدات.</span><span class="sxs-lookup"><span data-stu-id="e1072-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="e1072-329">ما يزال العمل مقدمًا إلى المستخدم، نظرا لأن بند عمل واحد الأقل يتضمن كمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="e1072-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="e1072-330">استنادا إلى السيناريو، يمكنك منع هذا السلوك باستخدام فواصل العمل.</span><span class="sxs-lookup"><span data-stu-id="e1072-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
