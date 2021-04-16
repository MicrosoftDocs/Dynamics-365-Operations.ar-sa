---
title: تجميع سطور الانتقاء
description: يوفر هذا الموضوع نظرة عامة على تجميع سطور الانتقاء.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828254"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="ca417-103">تجميع سطور الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ca417-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca417-104">في تجميع سطر الانتقاء، يمكن دمج أسطر عمل متعددة تحتوي على الصنف نفسه ويمكن دمج الموقع في سطر واحد يتم تقديمه إلى المستخدم على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="ca417-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="ca417-105">ولذلك، يمكن لعمال المستودع الحصول على التعليمات الأكثر فعالية الممكنة، ولكن يتم أيضًا الاحتفاظ بالفصل المطلوب لسطور العمل في النظام (للحاويات والأوامر المختلفة).</span><span class="sxs-lookup"><span data-stu-id="ca417-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="ca417-106">تشغيل ميزة تجميع بنود انتقاء العمل</span><span class="sxs-lookup"><span data-stu-id="ca417-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="ca417-107">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="ca417-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ca417-108">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ca417-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ca417-109">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="ca417-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ca417-110">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="ca417-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ca417-111">**اسم الميزة:** *انتقاء تجميع السطور*</span><span class="sxs-lookup"><span data-stu-id="ca417-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="ca417-112">إعداد تجميع سطور الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ca417-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="ca417-113">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="ca417-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="ca417-114">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ca417-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ca417-115">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ca417-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ca417-116">في الحقل **اسم عنصر القائمة**، أدخل *انتقاء بند مجموعة المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="ca417-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="ca417-117">في الحقل **العنوان**، أدخل *انتقاء بند مجموعة المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="ca417-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="ca417-118">سيظهر هذا العنوان في قائمه الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="ca417-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="ca417-119">في الحقل **الوضع**، حدد *العمل*.</span><span class="sxs-lookup"><span data-stu-id="ca417-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="ca417-120">قم بتعيين خيار **استخدام العمل الموجود** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ca417-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="ca417-121">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ca417-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ca417-122">في الحقل **موجه بواسطة**، حدد *المستخدم موجَّه*.</span><span class="sxs-lookup"><span data-stu-id="ca417-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="ca417-123">عيّن الخيار **إنشاء لوحة ترخيص** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ca417-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="ca417-124">عيّن الخيار **انتقاء المجموعة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ca417-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="ca417-125">اقبل القيم الافتراضية للخيارات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="ca417-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="ca417-126">اتبع هذه الخطوات لتكوين فئات العمل الصالحة لعنصر قائمة الجهاز المحمول:</span><span class="sxs-lookup"><span data-stu-id="ca417-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="ca417-127">في علامة التبويب السريعة **فئات العمل**، قم باختيار **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ca417-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="ca417-128">في الحقل **معرف فئة العمل**، يمكنك تحديد *المبيعات* أو *الانتقاء SO*، وفقًا للمستودع الذي ستستخدمه.</span><span class="sxs-lookup"><span data-stu-id="ca417-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="ca417-129">لهذا السيناريو ، حدد *انتقاء SO*.</span><span class="sxs-lookup"><span data-stu-id="ca417-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="ca417-130">يتم تعيين الحقل تلقائيًا **نوع أمر العمل** إلى *أوامر الشراء*.</span><span class="sxs-lookup"><span data-stu-id="ca417-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="ca417-131">إعداد قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ca417-131">Set up a mobile device menu</span></span>

<span data-ttu-id="ca417-132">اتبع الخطوات التالية لأضافه عنصر القائمة الذي قمت بإنشاءه للتو في القائمة **الصادر**.</span><span class="sxs-lookup"><span data-stu-id="ca417-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="ca417-133">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ca417-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ca417-134">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ca417-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ca417-135">يعرض جزء القائمة كافة قوائم الاجهزه المحمولة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="ca417-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="ca417-136">في القائمة، حدد *الصادر*.</span><span class="sxs-lookup"><span data-stu-id="ca417-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="ca417-137">في القائمة **القوائم المتوفرة وعناصر القائمة**، ابحث عن عنصر القائمة *انتقاء بند مجموعة المبيعات* الذي أنشأته وحدده.</span><span class="sxs-lookup"><span data-stu-id="ca417-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="ca417-138">حدد الزر سهم لليمين لنقل عنصر قائمة *انتقاء بند مجموعة المبيعات* إلى قائمة **بنية القائمة**.</span><span class="sxs-lookup"><span data-stu-id="ca417-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="ca417-139">استخدم أزرار السهم إلى الأعلى أو السهم إلى الأسفل لنقل عنصر القائمة إلى الموضع المطلوب في بنية القائمة.</span><span class="sxs-lookup"><span data-stu-id="ca417-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="ca417-140">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ca417-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="ca417-141">إعداد قالب عمل</span><span class="sxs-lookup"><span data-stu-id="ca417-141">Set up a work template</span></span>

1. <span data-ttu-id="ca417-142">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="ca417-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ca417-143">في الحقل **نوع أمر العمل**، حدد *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="ca417-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="ca417-144">في شبكه **النظرة العامة**، ابحث عن وحدد قالب العمل الذي يجب استخدامه مع هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="ca417-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="ca417-145">بالنسبة لهذا السيناريو ، حدد قالب *51 انتقاء إلى المرحلة*.</span><span class="sxs-lookup"><span data-stu-id="ca417-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="ca417-146">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="ca417-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ca417-147">في مربع حوار محرر الاستعلام، ضمن علامة التبويب **الفرز**، حدد **إضافة** لتعيين قيم السطر الجديد:</span><span class="sxs-lookup"><span data-stu-id="ca417-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ca417-148">في عمود **الجدول**، حدد *حركات العمل المؤقتة*.</span><span class="sxs-lookup"><span data-stu-id="ca417-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="ca417-149">في حقل **الجدول المشتق**، حدد *حركات العمل المؤقتة*.</span><span class="sxs-lookup"><span data-stu-id="ca417-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="ca417-150">في عمود **الحقل**، حدد *رقم الصنف*.</span><span class="sxs-lookup"><span data-stu-id="ca417-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="ca417-151">في العمود **اتجاه البحث**، حدد *تصاعدي*.</span><span class="sxs-lookup"><span data-stu-id="ca417-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="ca417-152">حدد **موافق** لحفظ اختيارك وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="ca417-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="ca417-153">تتلقى الرسالة التالية: "ستتم إعادة تعيين التجميع، هل تريد المتابعة؟"</span><span class="sxs-lookup"><span data-stu-id="ca417-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="ca417-154">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ca417-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca417-155">بالنسبة لوظيفة تجميع سطور الانتقاء للعمل، فإنه يجب أن يتم فرز بنود العمل حسب معرف الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca417-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="ca417-156">إذا لم تكن السطور التي تحتوي على الأصناف نفسها متسلسلة واحدة تلو الأخرى، فإنه لن يتم تجميعها.</span><span class="sxs-lookup"><span data-stu-id="ca417-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="ca417-157">مثال</span><span class="sxs-lookup"><span data-stu-id="ca417-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="ca417-158">إنشاء عمل انتقاء</span><span class="sxs-lookup"><span data-stu-id="ca417-158">Create picking work</span></span>

<span data-ttu-id="ca417-159">قبل أن تتمكن من إعداد تجميع سطور الانتقاء، فإنه يجب عليك إنشاء بعض الأعمال الصادرة المؤهلة.</span><span class="sxs-lookup"><span data-stu-id="ca417-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="ca417-160">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="ca417-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ca417-161">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ca417-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="ca417-162">في حقل **حساب العميل**، حدد *US-004*.</span><span class="sxs-lookup"><span data-stu-id="ca417-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="ca417-163">من علامة التبويب السريعة **عام**، في الحقل **المستودع**، حدد *51*.</span><span class="sxs-lookup"><span data-stu-id="ca417-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="ca417-164">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ca417-164">Select **OK**.</span></span>
1. <span data-ttu-id="ca417-165">في علامة التبويب السريعة **سطور أمر المبيعات**، أضف الأسطر الستة التالية:</span><span class="sxs-lookup"><span data-stu-id="ca417-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="ca417-166">**السطر 1:** في الحقل **رقم الصنف**، حدد *M9200*.</span><span class="sxs-lookup"><span data-stu-id="ca417-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="ca417-167">في حقل **كمية** ، أدخل *3*.</span><span class="sxs-lookup"><span data-stu-id="ca417-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="ca417-168">**السطر 2:** في الحقل **رقم الصنف**، حدد *M9201*.</span><span class="sxs-lookup"><span data-stu-id="ca417-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="ca417-169">في حقل **كمية** ، أدخل *3*.</span><span class="sxs-lookup"><span data-stu-id="ca417-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="ca417-170">**السطر 3:** في الحقل **رقم الصنف**، حدد *M9202*.</span><span class="sxs-lookup"><span data-stu-id="ca417-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="ca417-171">في حقل **كمية** ، أدخل *2*.</span><span class="sxs-lookup"><span data-stu-id="ca417-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="ca417-172">**السطر 4:** في الحقل **رقم الصنف**، حدد *M9200*.</span><span class="sxs-lookup"><span data-stu-id="ca417-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="ca417-173">في حقل **كمية** ، أدخل *1*.</span><span class="sxs-lookup"><span data-stu-id="ca417-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="ca417-174">**السطر 5:** في الحقل **رقم الصنف**، حدد *M9200*.</span><span class="sxs-lookup"><span data-stu-id="ca417-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="ca417-175">في حقل **كمية** ، أدخل *3*.</span><span class="sxs-lookup"><span data-stu-id="ca417-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="ca417-176">**السطر 6:** في الحقل **رقم الصنف**، حدد *M9202*.</span><span class="sxs-lookup"><span data-stu-id="ca417-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="ca417-177">في حقل **كمية** ، أدخل *7*.</span><span class="sxs-lookup"><span data-stu-id="ca417-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="ca417-178">وفيما يلي ملخص للكميات الإجمالية لكل صنف:</span><span class="sxs-lookup"><span data-stu-id="ca417-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="ca417-179">**الصنف M9200:** *7* لكل واحد</span><span class="sxs-lookup"><span data-stu-id="ca417-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="ca417-180">**الصنف M9201:** *3* لكل واحد</span><span class="sxs-lookup"><span data-stu-id="ca417-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="ca417-181">**الصنف M9202:** *9* لكل واحد</span><span class="sxs-lookup"><span data-stu-id="ca417-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="ca417-182">قبل أن تقوم بإصدار الأوامر إلى المستودع، فإنه يجب عليك التأكد من أن مواقع الانتقاء لديها مخزون كاف لكافة الأصناف الموجودة على كافة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ca417-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="ca417-183">راجع إعداد **توجيه الموقع** لتحديد مواقع الانتقاء التي يتم استخدامها لانتقاء أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="ca417-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="ca417-184">إذا كنت تستخدم بيئة بيانات الشركة التجريبية للمستودع *51*، فقم بالتاكيد علي وجود مخزون متاح.</span><span class="sxs-lookup"><span data-stu-id="ca417-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="ca417-185">يجب الآن حجز المخزون لكل بند.</span><span class="sxs-lookup"><span data-stu-id="ca417-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="ca417-186">في علامة التبويب السريعة **بنود أمر التوريد**، حدد أحد البنود التي يجب حجزها.</span><span class="sxs-lookup"><span data-stu-id="ca417-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="ca417-187">في قائمة **المخزون** أعلى الشبكة، حدد **حجز**.</span><span class="sxs-lookup"><span data-stu-id="ca417-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="ca417-188">في صفحة **الحجز**، في جزء الإجراءات حدد **حجز لوط** للحجز.</span><span class="sxs-lookup"><span data-stu-id="ca417-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="ca417-189">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ca417-189">Then close the page.</span></span>
1. <span data-ttu-id="ca417-190">كرر الخطوات من 8 إلى 10 للبنود المتبقية التي يجب حجزها.</span><span class="sxs-lookup"><span data-stu-id="ca417-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="ca417-191">يجب عليك الآن إصدار أمر المبيعات إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="ca417-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="ca417-192">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="ca417-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ca417-193">وتظهر رسالة توضح انه تم إنشاء شحنه وموجه، وانه قد تم إرسال الموجه ليتم تشغيله في مجموعه.</span><span class="sxs-lookup"><span data-stu-id="ca417-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="ca417-194">عند اكتمال الموجه والوظائف التي تم إكمالها في الجانب الآخر، يتم إنشاء معرف عمل للعمل الذي يحتوي علي سته بنود.</span><span class="sxs-lookup"><span data-stu-id="ca417-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="ca417-195">يتم فرز الأسطر حسب رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="ca417-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="ca417-196">انتقل إلى **إدارة المستودع\> العمل \> كل العمل** لعرض العمل الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="ca417-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="ca417-197">دوّن قيمة **معرف العمل**، بحيث يمكنك استخدامه في الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="ca417-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="ca417-198">بدء الانتقاء من الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ca417-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="ca417-199">سجل الدخول إلى الجهاز المحمول كمستخدم معين للمستودع *51*.</span><span class="sxs-lookup"><span data-stu-id="ca417-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="ca417-200">على الجهاز المحمول، حدد القائمة التي تتضمن صنف قائمة الجهاز المحمول الجديد.</span><span class="sxs-lookup"><span data-stu-id="ca417-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="ca417-201">لهذا السيناريو ، حدد **صادر**.</span><span class="sxs-lookup"><span data-stu-id="ca417-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="ca417-202">حدد صنف القائمة **انتقاء بند مجموعة المبيعات**، وقم ببدء الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ca417-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="ca417-203">ادخل قيمه **معرف العمل** التي قمت بإنشاءها في الاجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="ca417-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="ca417-204">يجب ان تشاهد خطوه انتقاء حيث يتم تجميع كافة بنود الانتقاء الخاصة بـ *M9200* للأصناف، ويجب ان تتلقي تعليمه لانتقاء *7* كل صنف من *M9200*.</span><span class="sxs-lookup"><span data-stu-id="ca417-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ca417-205">علي الجهاز المحمول ، يتم تجميع العمل المنتقي لبنود عمل الانتقاء الثلاثة في خطوه انتقاء واحده للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="ca417-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="ca417-206">قم بتأكيد خطوة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ca417-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="ca417-207">انتقل إلى صفحة العمل لمعرف العمل، ولاحظ أنه تم إغلاق كافة بنود الانتقاء الثلاثة للصنف *M9200* في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="ca417-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="ca417-208">ارجع إلى الجهاز المحمول واستمر في الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ca417-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="ca417-209">يجب تقديم سطر العمل 4 للصنف *M9201*.</span><span class="sxs-lookup"><span data-stu-id="ca417-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="ca417-210">وبسبب وجود سطر عمل واحد فقط في الأمر ، فلا يوجد شيء لتجميعه.</span><span class="sxs-lookup"><span data-stu-id="ca417-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="ca417-211">قم بتأكيد خطوة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ca417-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="ca417-212">تعمل الخطوة الأخيرة للانتقاء في الجهاز المحمول على تجميع بندين الانتقاء الأخيرين من أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="ca417-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="ca417-213">قم بإكمال خطوة الانتقاء لـ *9* من كل صنف *M9202*.</span><span class="sxs-lookup"><span data-stu-id="ca417-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="ca417-214">قم بتأكيد خطوة الوضع وأي زوج انتقاء/وضع إضافي لإكمال العمل.</span><span class="sxs-lookup"><span data-stu-id="ca417-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="ca417-215">يمكن تجميع خطوط العمل فقط إذا كانت في تسلسل.</span><span class="sxs-lookup"><span data-stu-id="ca417-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="ca417-216">الوظيفة التالية غير مدعومة:</span><span class="sxs-lookup"><span data-stu-id="ca417-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="ca417-217">أصناف وزن التعبئة</span><span class="sxs-lookup"><span data-stu-id="ca417-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="ca417-218">إذا كان هناك أية أصناف وزن التعبئة في العمل، فإنك تتلقى رسالة خطأ قبل البدء في الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ca417-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="ca417-219">انتقاء الأجزاء</span><span class="sxs-lookup"><span data-stu-id="ca417-219">Piece picking</span></span>
>   - <span data-ttu-id="ca417-220">خطوط العمل التي تحتوي على عمل التزويد</span><span class="sxs-lookup"><span data-stu-id="ca417-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="ca417-221">انتقاء زائد</span><span class="sxs-lookup"><span data-stu-id="ca417-221">Over-picking</span></span>
>   - <span data-ttu-id="ca417-222">إعادة توزيع الأصناف للانتقاء القصير</span><span class="sxs-lookup"><span data-stu-id="ca417-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]