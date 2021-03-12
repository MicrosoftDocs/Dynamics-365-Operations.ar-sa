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
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3811486a31d079cac7f7c27ea6323f16de4478d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970196"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="ffb70-105">تسلسل العمل الموجه بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="ffb70-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffb70-106">يتيح لك تسلسل العمل الموجه من النظام فرز وتصفية أوامر العمل التي يقدمها النظام للمستخدمين ليتم تنفيذها.</span><span class="sxs-lookup"><span data-stu-id="ffb70-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="ffb70-107">وهي مفيدة في السيناريوهات التي تتطلب معايير إضافية (مثل وقت الشحن، أو منطقة الانتقاء، أو ملف تعريف الموقع، أو مجموعة من المعايير المتعددة) لتوجيه عملية الانتقاء من المستودع.</span><span class="sxs-lookup"><span data-stu-id="ffb70-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="ffb70-108">تقوم هذه الوظيفة بتوسيع وظيفة الانتقاء الموجه من النظام الحالية عن طريق إضافة أمر استعلام موجه من النظام؛ حيث يمكن للمستخدمين إعداد تسلسل واستعلام واحد أو أكثر والذي سيقوم بتقييم كافة أوامر العمل التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ffb70-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="ffb70-109">لن يتم التقاط وتقديم إلا أوامر العمل التي تفي بالمعايير المحددة في إعداد عنصر قائمة جهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="ffb70-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="ffb70-110">لذلك، تتيح هذه الوظيفة تحسينًا إضافيًا لعمليات الانتقاء من المستودع حيث تحدد أوامر العمل التي تطابق المعايير المحددة، وتعيينها إلى عنصر قائمة الأجهزة المحمولة الصحيح، ثم تقدمها للعامل، استنادًا إلى مجموعة محددة من المهارات أو معدات انتقاء أو متطلبات أخرى.</span><span class="sxs-lookup"><span data-stu-id="ffb70-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb70-111">في حالة الحاجة إلى معايير مختلفة، يجب استخدام عدة عناصر لقائمة الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="ffb70-112">تشغيل ميزة تسلسل العمل الموجه بواسطة النظام على مستوى المؤسسة</span><span class="sxs-lookup"><span data-stu-id="ffb70-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="ffb70-113">قبل أن تتمكن من استخدام ميزة تسلسل العمل الموجه بواسطة النظام، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ffb70-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="ffb70-114">بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ffb70-115">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ffb70-116">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="ffb70-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ffb70-117">**اسم الميزة:** *تسلسل العمل الموجه بواسطة النظام على مستوى المؤسسة*</span><span class="sxs-lookup"><span data-stu-id="ffb70-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="ffb70-118">الإعداد</span><span class="sxs-lookup"><span data-stu-id="ffb70-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ffb70-119">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="ffb70-119">Make demo data available</span></span>

<span data-ttu-id="ffb70-120">للعمل في السيناريو باستخدام القيم المقدمة في هذا الموضوع يجب أن تعمل على نظام تم تثبيت البيانات القياسية التوضيحية عليه.</span><span class="sxs-lookup"><span data-stu-id="ffb70-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="ffb70-121">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="ffb70-122">يستخدم السيناريو المستودع *51* من البيانات التوضيحية.</span><span class="sxs-lookup"><span data-stu-id="ffb70-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffb70-123">قبل أن تقوم بإصدار الأوامر إلى المستودع، تأكد من أن مواقع الانتقاء لديها مخزون كاف لكافة الأصناف الموجودة على كافة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="ffb70-124">يجب أن تدعم بيانات USMF الافتراضية هذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="ffb70-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="ffb70-125">إذا كنت تستخدم البيانات التوضيحية، فراجع إعداد **توجيه الموقع** لمعرفة ما هي مواقع الانتقاء التي يتم استخدامها لانتقاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="ffb70-126">إذا كان من الضروري تسوية المخزون، فيمكنك إنشاء حركات يدوية أو استخدام تزويد أو استخدام أي سير عمل آخر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="ffb70-127">إعداد عنصر قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ffb70-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="ffb70-128">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ffb70-129">في قائمة عناصر قائمة الجهاز المحمول، حدد **انتقاء المبيعات - النظام**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="ffb70-130">يجب أن يكون عنصر القائمة المطلوب موجودًا بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="ffb70-131">أكد الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="ffb70-132">في علامة التبويب السريعة **عام**، يجب تعيين الحقل **موجه بواسطة** إلى *النظام الذي تم التوجيه إليه*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="ffb70-133">يجب أن تعرض علامة التبويب السريعة **فئات العمل** الإعدادات التالية.</span><span class="sxs-lookup"><span data-stu-id="ffb70-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="ffb70-134">معرف فئة العمل</span><span class="sxs-lookup"><span data-stu-id="ffb70-134">Work class ID</span></span> | <span data-ttu-id="ffb70-135">نوع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="ffb70-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="ffb70-136">مبيعات</span><span class="sxs-lookup"><span data-stu-id="ffb70-136">Sales</span></span> | <span data-ttu-id="ffb70-137">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ffb70-137">Sales orders</span></span> |
        | <span data-ttu-id="ffb70-138">انتقاء SO</span><span class="sxs-lookup"><span data-stu-id="ffb70-138">SO Pick</span></span> | <span data-ttu-id="ffb70-139">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ffb70-139">Sales orders</span></span> |

1. <span data-ttu-id="ffb70-140">في جزء الإجراءات، حدد **استعلامات تسلسل العمل الموجه بواسطة النظام**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="ffb70-141">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-141">Select **Edit**.</span></span>
1. <span data-ttu-id="ffb70-142">قم بحذف البند الموجود، ثم أكد الإجراء عن طريق تحديد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="ffb70-143">في جزء الإجراءات، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="ffb70-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="ffb70-144">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffb70-145">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="ffb70-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ffb70-146">**حقل الوصف:** *كمية العمل أقل من 20 وتنازلي*</span><span class="sxs-lookup"><span data-stu-id="ffb70-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="ffb70-147">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-147">Select **Save**.</span></span>
1. <span data-ttu-id="ffb70-148">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="ffb70-149">في علامة التبويب **صلات**، قم بتوسيع التسلسل الهرمي للصلات لإظهار جدول **بنود العمل**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="ffb70-150">حدد صلة جدول **بنود العمل**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="ffb70-151">حدد **إضافة انضمام جدول**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="ffb70-152">في القائمة التي تظهر، ابحث عن الصف الذي يحتوي على الإعدادات التالية وقم بتحديده:</span><span class="sxs-lookup"><span data-stu-id="ffb70-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="ffb70-153">**وضع الصلة:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="ffb70-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="ffb70-154">**العلاقة:** *المواقع (الموقع)*</span><span class="sxs-lookup"><span data-stu-id="ffb70-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="ffb70-155">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-155">Select **Select**.</span></span>

    <span data-ttu-id="ffb70-156">تتم إضافة المواقع إلى صلة الجدول.</span><span class="sxs-lookup"><span data-stu-id="ffb70-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="ffb70-157">في علامة التبويب **الفرز**، حدد **إضافة** لإضافة سطر جديد.</span><span class="sxs-lookup"><span data-stu-id="ffb70-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="ffb70-158">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffb70-159">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ffb70-160">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ffb70-161">**الحقل:** *كمية العمل* (في مربع الرسالة التي تظهر، حدد **نعم** لإضافة الفرز إلى هذا الحقل.)</span><span class="sxs-lookup"><span data-stu-id="ffb70-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="ffb70-162">**اتجاه البحث:** *تنازلي*</span><span class="sxs-lookup"><span data-stu-id="ffb70-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="ffb70-163">حدد علامة التبويب **النطاق**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="ffb70-164">إذا كان يجب تضمين معايير عمل محددة في التسلسل، فيمكنك تحديدها في علامة تبويب **النطاق**. في هذا المثال، تريد تضمين العمل فقط الذي تكون كميته أقل من 20 وحدة (أقل وحدة قياس).</span><span class="sxs-lookup"><span data-stu-id="ffb70-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="ffb70-165">لاحظ أن بعض البنود قد تم تضمينها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-165">Notice that some lines are already included.</span></span> <span data-ttu-id="ffb70-166">يجب عدم إزالة هذه البنود.</span><span class="sxs-lookup"><span data-stu-id="ffb70-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="ffb70-167">حدد **إضافة** لإضافة سطر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="ffb70-168">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffb70-169">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ffb70-170">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ffb70-171">**الحقل:** *كمية عمل المخزون*</span><span class="sxs-lookup"><span data-stu-id="ffb70-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="ffb70-172">**المعايير:** *\<20* (أقل من 20)</span><span class="sxs-lookup"><span data-stu-id="ffb70-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="ffb70-173">حدد **إضافة** لإضافة سطر آخر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="ffb70-174">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffb70-175">**الجدول:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ffb70-176">**الجدول المشتق:** *بنود العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ffb70-177">**الحقل:** *نوع العمل*</span><span class="sxs-lookup"><span data-stu-id="ffb70-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="ffb70-178">**المعايير:** *انتقاء*</span><span class="sxs-lookup"><span data-stu-id="ffb70-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="ffb70-179">حدد **إضافة** لإضافة سطر آخر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="ffb70-180">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffb70-181">**الجدول:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="ffb70-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ffb70-182">**الجدول المشتق:** *المواقع*</span><span class="sxs-lookup"><span data-stu-id="ffb70-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="ffb70-183">**الحقل:** *معرف ملف الموقع*</span><span class="sxs-lookup"><span data-stu-id="ffb70-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="ffb70-184">**المعايير:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="ffb70-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="ffb70-185">تأكد من تضمين علامة التعجب (*!*) أمام *STAGE*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="ffb70-186">حدد **موافق** لحفظ الاستعلام وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="ffb70-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="ffb70-187">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-187">Select **Save**.</span></span>
1. <span data-ttu-id="ffb70-188">أغلق الصفحة للعودة إلى صفحة **عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="ffb70-189">يحدد هذا الإعداد المعايير التي سيتم استخدامها لتغذية العمل المؤهل بعنصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="ffb70-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="ffb70-190">إذا قمت بإضافة المزيد من بنود المعايير إلى الاستعلام، فسيقوم النظام باستخدام بند الاستعلام الذي له رقم التسلسل الأقل أولا.</span><span class="sxs-lookup"><span data-stu-id="ffb70-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="ffb70-191">بمعنى آخر، سيتم تقديم كافة الأعمال المؤهلة لرقم التسلسل 1 إلى المستخدم أولا، ثم كل أعمال رقم التسلسل 2.</span><span class="sxs-lookup"><span data-stu-id="ffb70-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="ffb70-192">بالتالي، إذا كان من الضروري استخدام نطاق فرز معين معًا، فيجب تحديدهما في نفس استعلام تسلسل العمل الموجه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="ffb70-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="ffb70-193">سيقوم هذا الإعداد بالتقاط أي عمل يحتوي على بند واحد على الأقل حيث تكون الكمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="ffb70-194">بالتالي، إذا كان العمل يحتوي على بند تكون فيه الكمية هي 20 وحدة بالضبط أو أكثر من 20 وحدة، فإنه سيكون صالحا، بشرط أن يحتوي أيضا على بند واحد على الأقل حيث تكون الكمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="ffb70-195">توجيهات الموقع</span><span class="sxs-lookup"><span data-stu-id="ffb70-195">Location directives</span></span>

<span data-ttu-id="ffb70-196">إذا كنت تستخدم بيانات شركة Contoso الافتراضية، فلن يتطلب الاستعلام عن الإجراء الموجة إلى الموقع القيام بأي تغييرات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="ffb70-197">مع ذلك، للتأكد من أن توجيهات المواقع ستقوم بالتقاط الأصناف الموجودة في أوامر المبيعات عند تطبيق الميزة في بيئة خلاف Contoso، قم بإنشاء توجيه موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="ffb70-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="ffb70-198">للتحقق من الإعدادات في بيئة العرض التوضيحي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ffb70-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="ffb70-199">انتقل إلى **إدارة المستودعات‬** \> **الإعداد** \> **موجهات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="ffb70-200">في الحقل **نوع أمر العمل**، حدد *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="ffb70-201">حدد التوجيه الخاص بالموقع الذي يسمى *51 الانتقاء*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="ffb70-202">في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد السطر الخاص بالإجراء **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="ffb70-203">حدد **تحرير استعلام** فوق الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="ffb70-204">راجع استعلام **النطاق**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="ffb70-205">ابحث عن البند الذي تم فيه تعيين حقل **الحقل** إلى *الموقع*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="ffb70-206">تأكد من أن حقل **المعايير** فارغ (أي أنه لا توجد قيود).</span><span class="sxs-lookup"><span data-stu-id="ffb70-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="ffb70-207">سيناريو</span><span class="sxs-lookup"><span data-stu-id="ffb70-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="ffb70-208">إنشاء عمل انتقاء لأمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ffb70-208">Create sales order picking work</span></span>

<span data-ttu-id="ffb70-209">قبل تشغيل الانتقاء الموجه بواسطة النظام، يجب إنشاء بعض العمل الصادر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="ffb70-210">في هذا السيناريو، ستقوم بإنشاء أربعة أوامر مبيعات تستند إلى استعلامات محددة لتسلسل العمل الموجه بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="ffb70-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="ffb70-211">عليك حجز كميات مخزون لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="ffb70-212">بالتالي، لا يمكن سحب المخزون المحجوز من المستودع لأوامر أخرى إلا إذا تم إلغاء حجز المخزون أو جزء منه.</span><span class="sxs-lookup"><span data-stu-id="ffb70-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="ffb70-213">ستقوم بعد ذلك بإصدار كل أمر مبيعات للمستودع لإنشاء العمل الصادر.</span><span class="sxs-lookup"><span data-stu-id="ffb70-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="ffb70-214">أمر المبيعات 1</span><span class="sxs-lookup"><span data-stu-id="ffb70-214">Sales order 1</span></span>

1. <span data-ttu-id="ffb70-215">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ffb70-216">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 1.</span><span class="sxs-lookup"><span data-stu-id="ffb70-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="ffb70-217">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffb70-218">في قسم **العميل**، قم بتعيين حقل **حساب العميل** إلى *US-004*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="ffb70-219">في القسم **عام**، قم بتعيين حقل **المستودع** إلى *51*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="ffb70-220">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ffb70-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffb70-221">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffb70-222">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-223">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffb70-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffb70-224">**الكمية:** *20*</span><span class="sxs-lookup"><span data-stu-id="ffb70-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="ffb70-225">في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="ffb70-226">في صفحة **الحجز**، حدد **حجز لوط** لحجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="ffb70-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="ffb70-227">أغلق صفحة **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="ffb70-228">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬** لإنشاء عمل للمستودع.</span><span class="sxs-lookup"><span data-stu-id="ffb70-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="ffb70-229">سوف تستلم رسائل معلوماتية تعرض معرف الموجة ومعرفات الشحنة التي تم إنشاؤها لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="ffb70-230">أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="ffb70-230">Sales order 2</span></span>

1. <span data-ttu-id="ffb70-231">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 2.</span><span class="sxs-lookup"><span data-stu-id="ffb70-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="ffb70-232">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffb70-233">**حساب العميل:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="ffb70-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="ffb70-234">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="ffb70-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ffb70-235">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ffb70-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffb70-236">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffb70-237">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-238">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffb70-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffb70-239">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="ffb70-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="ffb70-240">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-241">**رقم الصنف:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="ffb70-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="ffb70-242">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="ffb70-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="ffb70-243">احجز المخزون لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="ffb70-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="ffb70-244">قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="ffb70-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="ffb70-245">أمر المبيعات 3</span><span class="sxs-lookup"><span data-stu-id="ffb70-245">Sales order 3</span></span>

1. <span data-ttu-id="ffb70-246">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 3.</span><span class="sxs-lookup"><span data-stu-id="ffb70-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="ffb70-247">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffb70-248">**حساب العميل:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="ffb70-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="ffb70-249">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="ffb70-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ffb70-250">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ffb70-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffb70-251">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffb70-252">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-253">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffb70-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffb70-254">**الكمية:** *7*</span><span class="sxs-lookup"><span data-stu-id="ffb70-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="ffb70-255">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-256">**رقم الصنف:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="ffb70-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="ffb70-257">**الكمية:** *8*</span><span class="sxs-lookup"><span data-stu-id="ffb70-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="ffb70-258">احجز المخزون لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="ffb70-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="ffb70-259">قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="ffb70-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="ffb70-260">أمر المبيعات 4</span><span class="sxs-lookup"><span data-stu-id="ffb70-260">Sales order 4</span></span>

1. <span data-ttu-id="ffb70-261">في جزء الإجراءات، حدد **جديد** لإنشاء أمر المبيعات 4.</span><span class="sxs-lookup"><span data-stu-id="ffb70-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="ffb70-262">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffb70-263">**حساب العميل:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="ffb70-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="ffb70-264">**المستودع:** *51*</span><span class="sxs-lookup"><span data-stu-id="ffb70-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ffb70-265">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ffb70-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffb70-266">قم بتدوين رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffb70-267">أضف سطرًا إلى أمر المبيعات الجديد، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-268">**رقم الصنف:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffb70-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffb70-269">**الكمية:** *25*</span><span class="sxs-lookup"><span data-stu-id="ffb70-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="ffb70-270">حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ffb70-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="ffb70-271">**رقم الصنف:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="ffb70-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="ffb70-272">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="ffb70-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="ffb70-273">احجز المخزون لكل من البندين.</span><span class="sxs-lookup"><span data-stu-id="ffb70-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="ffb70-274">قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="ffb70-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="ffb70-275">الحصول على معرفات العمل للعمل الذي تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="ffb70-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="ffb70-276">انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ffb70-277">قم بالتصفية حسب حقل **المستودع** بحيث يتم عرض العمل الخاص بالمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="ffb70-278">ينبغي أن يتم إنشاء أربع معرفات عمل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-278">Four work IDs should have been created.</span></span> <span data-ttu-id="ffb70-279">قم بتدوين معرف العمل لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="ffb70-280">مُعرف أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ffb70-280">Sales order ID</span></span> | <span data-ttu-id="ffb70-281">معرف العمل</span><span class="sxs-lookup"><span data-stu-id="ffb70-281">Work ID</span></span> | <span data-ttu-id="ffb70-282">كمية العمل</span><span class="sxs-lookup"><span data-stu-id="ffb70-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="ffb70-283">أمر المبيعات 1</span><span class="sxs-lookup"><span data-stu-id="ffb70-283">Sales Order 1</span></span> | <span data-ttu-id="ffb70-284">معرف العمل 1</span><span class="sxs-lookup"><span data-stu-id="ffb70-284">Work ID 1</span></span> | <span data-ttu-id="ffb70-285">20 وحدة</span><span class="sxs-lookup"><span data-stu-id="ffb70-285">20 ea</span></span> |
    | <span data-ttu-id="ffb70-286">أمر المبيعات 2</span><span class="sxs-lookup"><span data-stu-id="ffb70-286">Sales Order 2</span></span> | <span data-ttu-id="ffb70-287">معرف العمل 2</span><span class="sxs-lookup"><span data-stu-id="ffb70-287">Work ID 2</span></span> | <span data-ttu-id="ffb70-288">6 وحدات (مجموع كلا السطرين)</span><span class="sxs-lookup"><span data-stu-id="ffb70-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="ffb70-289">أمر المبيعات 3</span><span class="sxs-lookup"><span data-stu-id="ffb70-289">Sales Order 3</span></span> | <span data-ttu-id="ffb70-290">معرف العمل 3</span><span class="sxs-lookup"><span data-stu-id="ffb70-290">Work ID 3</span></span> | <span data-ttu-id="ffb70-291">15 وحدة (مجموع كلا السطرين)</span><span class="sxs-lookup"><span data-stu-id="ffb70-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="ffb70-292">أمر المبيعات 4</span><span class="sxs-lookup"><span data-stu-id="ffb70-292">Sales Order 4</span></span> | <span data-ttu-id="ffb70-293">معرف العمل 4</span><span class="sxs-lookup"><span data-stu-id="ffb70-293">Work ID 4</span></span> | <span data-ttu-id="ffb70-294">35 وحدة (مجموع كلا السطرين)</span><span class="sxs-lookup"><span data-stu-id="ffb70-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="ffb70-295">قبل تشغيل سير العمل على الجهاز المحمول، تأكد من أن العمل الذي قمت بإنشائه للتو بالحالة *مفتوح* للمستودع *51* ونوع أمر العمل *أمر مبيعات*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="ffb70-296">خلاف ذلك، قد تختلف نتائج الاختبار، لأن الانتقاء المباشر من النظام سيتضمن كافة العمل المؤهل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="ffb70-297">الانتقال إلى **إدارة المستودعات \> العمل \> الصادر \> عمل المبيعات المفتوح**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="ffb70-298">في شبكة **عمل المبيعات المفتوح**، بالتصفية حسب حقل **المستودع** بحيث يتم فقط عرض العمل الخاص بالمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="ffb70-299">تأكد من أنه تم عرض معرفات العمل الأربع التي قمت بإنشائها مسبقا فقط.</span><span class="sxs-lookup"><span data-stu-id="ffb70-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="ffb70-300">أغلق صفحة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="ffb70-301">تنفيذ سير عمل الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ffb70-301">Mobile device flow execution</span></span>

<span data-ttu-id="ffb70-302">واستنادا إلى الإعداد، سيقوم النظام بتغذيه عمل المستخدم الذي تم فرزه من أعلى كمية لبند العمل إلى الأقل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="ffb70-303">ستكون الكمية في كل بند أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="ffb70-304">تذكر أن هذا الإعداد سوف يلتقط أي عمل يحتوي على بند واحد على الأقل حيث تكون الكمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="ffb70-305">بالتالي، إذا كان العمل يحتوي على بند آخر حيث تكون الكمية 20 وحدة بالضبط أو أكثر من 20 وحدة، فسيكون صالحًا أيضًا.</span><span class="sxs-lookup"><span data-stu-id="ffb70-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="ffb70-306">تطبيق الجوال</span><span class="sxs-lookup"><span data-stu-id="ffb70-306">Mobile app</span></span>

1. <span data-ttu-id="ffb70-307">سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="ffb70-308">انتقل إلى **الصادر \> انتقاء المبيعات - النظام**.</span><span class="sxs-lookup"><span data-stu-id="ffb70-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="ffb70-309">يتم تقديم خطوة الانتقاء لمعرف العمل *4*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="ffb70-310">يتم تقديم معرف العمل هذا أولا بسبب إعداد أمر الاستعلام الموجه بواسطة النظام، حيث حددت أن يجب عمل تسلسل للعمل استنادًا إلى كمية بند العمل التنازلية.</span><span class="sxs-lookup"><span data-stu-id="ffb70-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="ffb70-311">أكمل الانتقاء والوضع المطلوب لإغلاق معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="ffb70-312">بعد ذلك، يتم تقديم معرف العمل *3*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="ffb70-313">ويكون أحد بنود العمل الخاصة به تاليًا في التسلسل، استنادًا إلى كمية بند العمل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="ffb70-314">أكمل الانتقاء والوضع لإغلاق معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="ffb70-315">بعد ذلك، يتم تقديم معرف العمل *2*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="ffb70-316">يكون بند انتقاء العمل هذا تاليًا في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="ffb70-317">أكمل الانتقاء والوضع لإغلاق معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="ffb70-318">ولا تظهر لك أي أعمال إضافية.</span><span class="sxs-lookup"><span data-stu-id="ffb70-318">No further work should be presented to you.</span></span> <span data-ttu-id="ffb70-319">معرف العمل *1* ليس مؤهلا لعنصر قائمة الجهاز المحمول هذا، نظرا لأن الاستعلام يحدد أن رؤوس العمل تعتبر فقط إذا كانت الكمية الموجودة في بنود العمل أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="ffb70-320">تلميحات</span><span class="sxs-lookup"><span data-stu-id="ffb70-320">Tips</span></span>

<span data-ttu-id="ffb70-321">تكون استعلامات تسلسل العمل الموجه بواسطة النظام *شمولية*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="ffb70-322">ومن المهم أن تتذكر هذه الحقيقة لبعض الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="ffb70-323">على سبيل المثال، عندما تريد فقط أن يعالج عنصر قائمة معين العمل الذي بالوحدة *وحدة*، وقمت بتحديد هذا القيد في علامة تبويب **النطاق** الخاص بالاستعلام.</span><span class="sxs-lookup"><span data-stu-id="ffb70-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="ffb70-324">في هذه الحالة، سيتم تغذية كل العمل الذي يحتوي بند عمل واحد على الأقل فيه على وحد العمل *الوحدة* للعامل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="ffb70-325">بالتالي، قد يتضمن هذا العمل أيضا العمل الذي تحتوي بنود العمل به على وحدة عمل خلاف *الوحدة* (مثل *صندوق* أو *بالتة*).</span><span class="sxs-lookup"><span data-stu-id="ffb70-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="ffb70-326">سيقوم الاستعلام باستبعاد فقط العمل الذي لم يتم تعيين وحدة العمل لأي بند عمل به على *الوحدة*.</span><span class="sxs-lookup"><span data-stu-id="ffb70-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="ffb70-327">بالتالي، في المثال من هذا السيناريو، يتم أيضًا التقاط معرف العمل *4* بواسطة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="ffb70-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="ffb70-328">وعندما تم إنشاؤه، تمت إضافة بندين: واحد لـ 25 وحدة وآخر لـ 10 وحدات.</span><span class="sxs-lookup"><span data-stu-id="ffb70-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="ffb70-329">ما يزال العمل مقدمًا إلى المستخدم، نظرا لأن بند عمل واحد الأقل يتضمن كمية أقل من 20 وحدة.</span><span class="sxs-lookup"><span data-stu-id="ffb70-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="ffb70-330">استنادا إلى السيناريو، يمكنك منع هذا السلوك باستخدام فواصل العمل.</span><span class="sxs-lookup"><span data-stu-id="ffb70-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
