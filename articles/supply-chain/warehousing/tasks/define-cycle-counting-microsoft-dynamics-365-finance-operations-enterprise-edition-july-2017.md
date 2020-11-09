---
title: تحديد الجرد الدوري
description: الجرد الدوري هو معالجة المستودع التي يمكنك استخدامها للتدقيق في أصناف المخزون الفعلي.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8b7f39fc9a91d9fe219445e409d000266e24775
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016138"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="b0980-103">تحديد الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="b0980-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0980-104">الجرد الدوري هو معالجة المستودع التي يمكنك استخدامها للتدقيق في أصناف المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="b0980-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="b0980-105">يظهر تسجيل هذه المهمة كيفية إعداد الأولوية الافتراضية لعمل الجرد وتمكين عنصر قائمة جهاز محمول لمعالجة علميات الانتقاء والجرد على حد سواء وتمكين مشغل عتبة جرد عندما يصبح الموقع فارغًا وتمكين خطة جرد دوري لصنف محدد داخل مستودع محدد.</span><span class="sxs-lookup"><span data-stu-id="b0980-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="b0980-106">يقوم مدير المستودع عادةً بتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="b0980-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="b0980-107">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في بياناتك.</span><span class="sxs-lookup"><span data-stu-id="b0980-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="b0980-108">تعيين أولوية عمل الجرد</span><span class="sxs-lookup"><span data-stu-id="b0980-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="b0980-109">في **جزء التنقل** ، انتقل إلى **الوحدات النمطية > إدارة المخزون > الإعداد > محددات إدارة المستودعات** ‬.</span><span class="sxs-lookup"><span data-stu-id="b0980-109">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="b0980-110">انقر فوق علامة التبويب **الجرد الدوري**.</span><span class="sxs-lookup"><span data-stu-id="b0980-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="b0980-111">في الحقل **أولوية عمل الجرد الدوري** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b0980-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="b0980-112">تقوم هذه الخطوة بتغيير أولوية عمل الجرد الدوري مقارنة بأنواع العمل الأخرى في المستودع.</span><span class="sxs-lookup"><span data-stu-id="b0980-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="b0980-113">من خلال إدخال رقم أقل من رقم أنواع العمل الأخرى، ستقوم برفع الأولوية لعمل الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="b0980-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="b0980-114">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-114">Click **Save**.</span></span>
5. <span data-ttu-id="b0980-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0980-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="b0980-116">تمكين الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="b0980-116">Enable the mobile device</span></span>
1. <span data-ttu-id="b0980-117">في **جزء التنقل** ، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="b0980-117">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="b0980-118">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b0980-118">Click **New**.</span></span>
3. <span data-ttu-id="b0980-119">في الحقل **اسم عنصر القائمة‬** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="b0980-120">في الحقل **العنوان** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="b0980-121">في الحقل **الوضع** ، حدد "العمل".</span><span class="sxs-lookup"><span data-stu-id="b0980-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="b0980-122">قم بتعيين الخيار **استخدام العمل الموجود** إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="b0980-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="b0980-123">عند تعيين هذا الخيار إلى "نعم"، سيبحث النظام عن العمل الموجود عند استخدام عنصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="b0980-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="b0980-124">في الحقل **موجه بواسطة** ، حدد "موجه بواسطة النظام".</span><span class="sxs-lookup"><span data-stu-id="b0980-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="b0980-125">عند تحديد "توجيه النظام"، سيتم توجيه عامل المستودع لفتح العمل الموجود في فئات العمل المحددة.</span><span class="sxs-lookup"><span data-stu-id="b0980-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="b0980-126">(سنقوم بعد ذلك بإنشاء فئات العمل هذه.)</span><span class="sxs-lookup"><span data-stu-id="b0980-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="b0980-127">وسّع علامة التبويب السريعة **فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="b0980-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="b0980-128">بعد ذلك، سنقوم بإنشاء فئتي عمل سيتم استخدامهما مع عنصر قائمة الجهاز المحمول هذا.</span><span class="sxs-lookup"><span data-stu-id="b0980-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="b0980-129">عند استخدام عنصر القائمة، سيتم الاستعلام عن فئات العمل هذه، وسيتم إظهار العمل ذي الأولوية العليا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="b0980-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="b0980-130">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b0980-130">Click **New**.</span></span>
10. <span data-ttu-id="b0980-131">حدد قيمة في حقل **معرف فئة العمل**.</span><span class="sxs-lookup"><span data-stu-id="b0980-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="b0980-132">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b0980-132">Click **New**.</span></span>
12. <span data-ttu-id="b0980-133">حدد قيمة في حقل **معرف فئة العمل**.</span><span class="sxs-lookup"><span data-stu-id="b0980-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="b0980-134">في **جزء الإجراءات** ، انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-134">In the **Action Pane** , click **Save**.</span></span>
14. <span data-ttu-id="b0980-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0980-135">Close the page.</span></span>
15. <span data-ttu-id="b0980-136">في **جزء التنقل** ، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > الجهاز المحمول > عنصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="b0980-136">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="b0980-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b0980-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b0980-138">في الشجرة، حدد "عنصر القائمة الذي قمت بإنشائه للتو".</span><span class="sxs-lookup"><span data-stu-id="b0980-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="b0980-139">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b0980-139">Click **Edit**.</span></span>
19. <span data-ttu-id="b0980-140">انقر فوق السهم لإضافة عنصر القائمة إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="b0980-141">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="b0980-142">إنشاء عتبة جرد</span><span class="sxs-lookup"><span data-stu-id="b0980-142">Create a counting threshold</span></span>
1. <span data-ttu-id="b0980-143">في **جزء التنقل** ، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > جرد دوري > حدود الجرد الدوري**.</span><span class="sxs-lookup"><span data-stu-id="b0980-143">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="b0980-144">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b0980-144">Click **New**.</span></span>
3. <span data-ttu-id="b0980-145">في الحقل **معرف حدود الجرد الدوري** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="b0980-146">قم بتعيين الخيار **معالجة الجرد الدوري فورًا‬** إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="b0980-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="b0980-147">في حقل **الوصف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b0980-148">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-148">Click **Save**.</span></span>
7. <span data-ttu-id="b0980-149">انقر فوق **تحديد المواقع**.</span><span class="sxs-lookup"><span data-stu-id="b0980-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="b0980-150">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b0980-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b0980-151">في الحقل **المعايير** ، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="b0980-152">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b0980-152">Click **OK**.</span></span>
11. <span data-ttu-id="b0980-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0980-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="b0980-154">إنشاء خطة جرد دوري</span><span class="sxs-lookup"><span data-stu-id="b0980-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="b0980-155">في **جزء التنقل** ، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > جرد دوري > خطط الجرد الدوري**.</span><span class="sxs-lookup"><span data-stu-id="b0980-155">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="b0980-156">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b0980-156">Click **New**.</span></span>
3. <span data-ttu-id="b0980-157">في الحقل **معرف خطة الجرد الدوري** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="b0980-158">في حقل **الوصف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b0980-159">في الحقل **الحد الأقصى لعدد عمليات الجرد الدوري** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b0980-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="b0980-160">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-160">Click **Save**.</span></span>
7. <span data-ttu-id="b0980-161">انقر فوق **تحديد المواقع**.</span><span class="sxs-lookup"><span data-stu-id="b0980-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="b0980-162">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b0980-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b0980-163">في الحقل **المعايير** ، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="b0980-164">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b0980-164">Click **OK**.</span></span>
11. <span data-ttu-id="b0980-165">في الحقل **الأيام الفاصلة بين عمليات الجرد الدوري** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b0980-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="b0980-166">على سبيل المثال، إذا تم تعيين الحقل **الأيام الفاصلة بين الجرد الدوري** إلى 5، سيتم إنشاء عمل الجرد الدوري كل خمسة أيام.</span><span class="sxs-lookup"><span data-stu-id="b0980-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="b0980-167">ومع ذلك، إذا تمت معالجة عمل الجرد الدوري في اليوم الثالث، فسيتم إنشاء عمل الجرد الدوري التالي خمسة أيام بعد معالجة آخر جرد دوري، في اليوم الثامن.</span><span class="sxs-lookup"><span data-stu-id="b0980-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="b0980-168">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-168">Click **Save**.</span></span>
13. <span data-ttu-id="b0980-169">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b0980-169">Click **New**.</span></span>
14. <span data-ttu-id="b0980-170">الرقم التسلسلي **الرقم التسلسلي** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b0980-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="b0980-171">الفرز هو من أصغر رقم إلى أكبر رقم.</span><span class="sxs-lookup"><span data-stu-id="b0980-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="b0980-172">يجب أن تكون القيمة أكبر من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="b0980-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="b0980-173">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b0980-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="b0980-174">في حقل **الوصف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0980-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="b0980-175">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0980-175">Click **Save**.</span></span>
18. <span data-ttu-id="b0980-176">انقر فوق استعلام **تعريف المنتج**.</span><span class="sxs-lookup"><span data-stu-id="b0980-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="b0980-177">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b0980-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b0980-178">في الحقل **المعايير‬** ، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b0980-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="b0980-179">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b0980-179">Click **OK**.</span></span>
22. <span data-ttu-id="b0980-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0980-180">Close the page.</span></span>

