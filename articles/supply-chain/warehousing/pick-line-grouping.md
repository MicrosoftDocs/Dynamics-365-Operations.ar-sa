---
title: تجميع سطور الانتقاء
description: يوفر هذا الموضوع نظرة عامة على تجميع سطور الانتقاء.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906258"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="ddb9e-103">تجميع سطور الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ddb9e-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddb9e-104">في تجميع سطر الانتقاء، يمكن دمج أسطر عمل متعددة تحتوي على الصنف نفسه ويمكن دمج الموقع في سطر واحد يتم تقديمه إلى المستخدم على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="ddb9e-105">ولذلك، يمكن لعمال المستودع الحصول على التعليمات الأكثر فعالية الممكنة، ولكن يتم أيضًا الاحتفاظ بالفصل المطلوب لسطور العمل في النظام (على سبيل المثال، للحاويات والأوامر المختلفة).</span><span class="sxs-lookup"><span data-stu-id="ddb9e-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="ddb9e-106">إعداد تجميع سطور الانتقاء</span><span class="sxs-lookup"><span data-stu-id="ddb9e-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="ddb9e-107">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="ddb9e-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="ddb9e-108">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> أصناف قائمة الجهاز المحمول**، وقم بإنشاء صنف قائمة جديدة باسم **انتقاء صنف مجموعة المبيعات – المستخدم موجَّه**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="ddb9e-109">ضمن **أصناف قائمة الجهاز المحمول**، قم بضبط القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="ddb9e-110">في الحقل **اسم عنصر القائمة**، أدخل **انتقاء المبيعات - بند المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="ddb9e-111">في الحقل **العنوان**، أدخل **انتقاء المبيعات - بند المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="ddb9e-112">في الحقل **الوضع**، حدد **العمل**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="ddb9e-113">قم بتعيين خيار **استخدام العمل الموجود** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="ddb9e-114">في علامة التبويب السريعة **عام**، يمكنك تعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="ddb9e-115">في الحقل **موجه بواسطة**، حدد **المستخدم موجَّه**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="ddb9e-116">عيّن الخيار **إنشاء لوحة ترخيص** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="ddb9e-117">عيّن الخيار **انتقاء المجموعة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="ddb9e-118">ضمن علامة التبويب السريعة **فئات العمل**، اتبع هذه الخطوات لتكوين فئات العمل الصالحة لعنصر قائمة الجهاز المحمول:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="ddb9e-119">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-119">Select **New**.</span></span>
    2. <span data-ttu-id="ddb9e-120">في الحقل **معرف فئة العمل**، حدد **المبيعات** أو **الانتقاء SO**، وفقًا للمستودع الذي ستستخدمه.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="ddb9e-121">في الحقل **نوع أمر العمل**، حدد **أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="ddb9e-122">إعداد قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ddb9e-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="ddb9e-123">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="ddb9e-124">أضف عنصر القائمة الذي قمت بإنشائه للتو إلى القائمة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="ddb9e-125">إعداد قالب عمل</span><span class="sxs-lookup"><span data-stu-id="ddb9e-125">Set up a work template</span></span>

1. <span data-ttu-id="ddb9e-126">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ddb9e-127">ابحث عن قالب العمل الذي يجب استخدامه مع هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="ddb9e-128">على سبيل المثال، حدد المعيار **51 انتقاء لمرحلة** قالب عمل Contoso.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="ddb9e-129">من القائمة، حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="ddb9e-130">في علامة التبويب **فرز**، حدد **إضافة**، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="ddb9e-131">في حقل **الجدول**، حدد **حركات العمل المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="ddb9e-132">في حقل **الجدول**، حدد **حركات العمل المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="ddb9e-133">في الحقل **الحقل**، حدد **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="ddb9e-134">في الحقل **اتجاه البحث**، حدد **تصاعدي**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="ddb9e-135">بالنسبة لوظيفة تجميع سطور الانتقاء للعمل، فإنه يجب أن يتم فرز بنود العمل حسب معرف الصنف.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="ddb9e-136">إذا لم تكن السطور التي تحتوي على الأصناف نفسها متسلسلة واحدة تلو الأخرى، فإنه لن يتم تجميعها.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="ddb9e-137">مثال</span><span class="sxs-lookup"><span data-stu-id="ddb9e-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="ddb9e-138">إنشاء عمل انتقاء</span><span class="sxs-lookup"><span data-stu-id="ddb9e-138">Create picking work</span></span>

<span data-ttu-id="ddb9e-139">قبل أن تتمكن من إعداد تجميع سطور الانتقاء، فإنه يجب عليك إنشاء بعض الأعمال الصادرة المؤهلة.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="ddb9e-140">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="ddb9e-141">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="ddb9e-142">في الحقل **حساب العميل**، حدد أي عميل.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="ddb9e-143">من علامة التبويب السريعة **عام**، في الحقل **المستودع**، حدد **51**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="ddb9e-144">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-144">Then select **OK**.</span></span>
5. <span data-ttu-id="ddb9e-145">ضمن **سطور أمر المبيعات**، أضف الأسطر الستة التالية:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="ddb9e-146">**السطر 1:** في الحقل **رقم الصنف**، حدد **M9200**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="ddb9e-147">في حقل **كمية** ، أدخل **3**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="ddb9e-148">**السطر 2:** في الحقل **رقم الصنف**، حدد **M9201**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="ddb9e-149">في حقل **كمية** ، أدخل **3**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="ddb9e-150">**السطر 3:** في الحقل **رقم الصنف**، حدد **M9202**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="ddb9e-151">في حقل **كمية** ، أدخل **2**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="ddb9e-152">**السطر 4:** في الحقل **رقم الصنف**، حدد **M9200**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="ddb9e-153">في حقل **كمية** ، أدخل **1**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="ddb9e-154">**السطر 5:** في الحقل **رقم الصنف**، حدد **M9200**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="ddb9e-155">في حقل **كمية** ، أدخل **3**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="ddb9e-156">**السطر 6:** في الحقل **رقم الصنف**، حدد **M9202**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="ddb9e-157">في حقل **كمية** ، أدخل **7**.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="ddb9e-158">وفيما يلي ملخص للكميات الإجمالية لكل صنف:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="ddb9e-159">**الصنف M9200:** عدد 7</span><span class="sxs-lookup"><span data-stu-id="ddb9e-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="ddb9e-160">**الصنف M9201:** عدد 3</span><span class="sxs-lookup"><span data-stu-id="ddb9e-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="ddb9e-161">**الصنف M9202:** عدد 9</span><span class="sxs-lookup"><span data-stu-id="ddb9e-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="ddb9e-162">قبل أن تقوم بإصدار الأوامر إلى المستودع، فإنه يجب عليك التأكد من أن مواقع الانتقاء لديها مخزون كاف لكافة الأصناف الموجودة على كافة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="ddb9e-163">راجع إعداد **توجيه الموقع** لتحديد مواقع الانتقاء التي يتم استخدامها لانتقاء أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="ddb9e-164">احجز المخزون، وقم بالإفراج عنه في المستودع.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="ddb9e-165">يتم إنشاء معرف العمل الذي يحتوي على ستة أسطر.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="ddb9e-166">يتم فرز الأسطر حسب رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="ddb9e-167">تشغيل تدفق الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="ddb9e-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="ddb9e-168">على الجهاز المحمول، حدد القائمة التي تتضمن صنف قائمة الجهاز المحمول الجديد.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="ddb9e-169">حدد صنف القائمة **انتقاء المبيعات – بند المجموعة**، وقم ببدء الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="ddb9e-170">بعد أن تقوم بتحديد القائمة وإدخال معرف العمل، فإنك سترى خطوة الانتقاء حيث يتم تجميع كافة بنود الانتقاء الخاصة بالصنف M9200.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="ddb9e-171">إنك تتلقى تعليمات لانتقاء 7 من الصنف M9200.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="ddb9e-172">قم بتأكيد خطوة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="ddb9e-173">انتقل إلى شاشة العميل للعمل قيد التنفيذ، ولاحظ أنه تم إغلاق كافة بنود الانتقاء الثلاثة للصنف M9200 في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="ddb9e-174">يتم عرض بند العمل رقم 4.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="ddb9e-175">قم بتأكيد خطوة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-175">Confirm the pick step.</span></span>

    <span data-ttu-id="ddb9e-176">تعمل الخطوة الأخيرة للانتقاء في الجهاز المحمول على تجميع بندين الانتقاء الأخيرين من أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="ddb9e-177">قم بإكمال خطوة الانتقاء لـ 9 من كل صنف M9202.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="ddb9e-178">قم بتأكيد خطوة الوضع وأي زوج انتقاء/وضع إضافي لإكمال العمل.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="ddb9e-179">يمكن تجميع خطوط العمل فقط إذا كانت في تسلسل.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="ddb9e-180">الوظيفة التالية غير مدعومة:</span><span class="sxs-lookup"><span data-stu-id="ddb9e-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="ddb9e-181">أصناف وزن التعبئة.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-181">Catch-weight items.</span></span> <span data-ttu-id="ddb9e-182">إذا كان هناك أية أصناف وزن التعبئة في العمل، فإنك تتلقى رسالة خطأ قبل البدء في الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="ddb9e-183">انتقاء الأجزاء.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-183">Piece picking.</span></span>
>    - <span data-ttu-id="ddb9e-184">خطوط العمل التي تحتوي على عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="ddb9e-185">انتقاء زائد.</span><span class="sxs-lookup"><span data-stu-id="ddb9e-185">Over-picking.</span></span>
