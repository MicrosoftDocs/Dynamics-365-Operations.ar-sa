---
title: إعداد عنصر قائمة جهاز محمول لإكمال عمل من النوع "أمر الشراء"
description: يوضح هذا الإجراء كيفية إعداد عنصر قائمة جهاز محمول.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545869"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="72cf4-103">إعداد عنصر قائمة جهاز محمول لإكمال عمل من النوع "أمر الشراء"</span><span class="sxs-lookup"><span data-stu-id="72cf4-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72cf4-104">يوضح هذا الإجراء كيفية إعداد عنصر قائمة جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="72cf4-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="72cf4-105">في هذا المثال، يتم استخدام عنصر القائمة لتنفيذ عمل من النوع "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="72cf4-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="72cf4-106">تحدد فئة العمل المرتبطة بعنصر القائمة العمل الصالح.</span><span class="sxs-lookup"><span data-stu-id="72cf4-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="72cf4-107">ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="72cf4-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="72cf4-108">يقوم مدير المستودع عادةً بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="72cf4-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="72cf4-109">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="72cf4-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="72cf4-110">انتقل إلى عناصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="72cf4-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="72cf4-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="72cf4-111">Click New.</span></span>
3. <span data-ttu-id="72cf4-112">في الحقل "اسم عنصر القائمة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="72cf4-113">أدخل قيمة فريدة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-113">Enter a unique value.</span></span> <span data-ttu-id="72cf4-114">على سبيل المثال، يمكنك كتابة نقل أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="72cf4-114">For example, you could type POMove.</span></span> <span data-ttu-id="72cf4-115">تذكر القيمة، إذ ستحتاجها في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="72cf4-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="72cf4-116">في الحقل "المسمى الوظيفي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="72cf4-117">هذا هو المسمى الوظيفي الذي سيُعرض على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="72cf4-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="72cf4-118">على سبيل المثال، يمكنك كتابة نقل أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="72cf4-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="72cf4-119">في الحقل "الوضع"، حدد "العمل".</span><span class="sxs-lookup"><span data-stu-id="72cf4-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="72cf4-120">حدد "نعم" في الحقل "استخدام العمل الموجود‬".</span><span class="sxs-lookup"><span data-stu-id="72cf4-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="72cf4-121">يتم استخدام عنصر قائمة الجهاز المحمول هذا لتنفيذ العمل الموجود.</span><span class="sxs-lookup"><span data-stu-id="72cf4-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="72cf4-122">لذلك يجب تعيين هذه القيمة إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="72cf4-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="72cf4-123">يحدد حقل "عرض حالة المخزون‬" ما إذا كانت حالة المخزون للمخزون الفعلي ستظهر للعامل في المستودع على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="72cf4-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="72cf4-124">في الحقل "موجه بواسطة"، حدد "تجميع النظام".</span><span class="sxs-lookup"><span data-stu-id="72cf4-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="72cf4-125">عند تحديد شيء في الحقل "موجه بواسطة‬"، تظهر حقول إضافية في المقطع "عام" في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="72cf4-126">تتوقف الحقول التي تظهر على ما قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="72cf4-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="72cf4-127">عندما تحدد "تجميع النظام‬"، يُضاف حقلان جديدان.</span><span class="sxs-lookup"><span data-stu-id="72cf4-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="72cf4-128">سيرد شرح هذان الحقلان أدناه.</span><span class="sxs-lookup"><span data-stu-id="72cf4-128">These are explained below.</span></span>  
8. <span data-ttu-id="72cf4-129">في حقل "تجميع النظام"، اكتب "WorkPoolId".</span><span class="sxs-lookup"><span data-stu-id="72cf4-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="72cf4-130">عند قيام العاملين في المستودع بفتح عنصر القائمة هذا، ستتم مطالبتهم بفحص معرف وعاء العمل‬.</span><span class="sxs-lookup"><span data-stu-id="72cf4-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="72cf4-131">سيتم دفع كافة أوامر العمل التي لديها معرف وعاء العمل هذا وبنود أوامر العمل المفتوحة مع إحدى فئات العمل المضافة إلى عنصر القائمة هذا إلى المستخدم.</span><span class="sxs-lookup"><span data-stu-id="72cf4-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="72cf4-132">في الحقل "تسمية تجميع النظام"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="72cf4-133">هذا هو النص الذي سيتم عرضه للمستخدم على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="72cf4-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="72cf4-134">على سبيل المثال، يمكنك كتابة وعاء العمل.</span><span class="sxs-lookup"><span data-stu-id="72cf4-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="72cf4-135">حدد "نعم" في الحقل "تجاوز لوحة الترخيص‬ أثناء التخزين".</span><span class="sxs-lookup"><span data-stu-id="72cf4-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="72cf4-136">يسمح هذا الخيار للعاملين في المستودع تجاوز لوحة الترخيص الهدف عندما يتم وضع الأصناف على موقع تتحكم به لوحة ترخيص.</span><span class="sxs-lookup"><span data-stu-id="72cf4-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="72cf4-137">حدد نعم في الحقل "تخزين المجموعة".</span><span class="sxs-lookup"><span data-stu-id="72cf4-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="72cf4-138">إذا كانت كافة بنود الوضع في أمر العمل تشارك الموقع نفسه، فسيتلقى المستخدم إرشادات وضع مدمجة لكافة البنود.</span><span class="sxs-lookup"><span data-stu-id="72cf4-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="72cf4-139">معرف قالب التدقيق: يسمح لك معرف قالب التدقيق بتحديد وجوب مقاطعة عملية العمل لعنصر قائمة بحيث يمكن تنفيذ عملية أخرى.</span><span class="sxs-lookup"><span data-stu-id="72cf4-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="72cf4-140">على سبيل المثال، إذا كان عنصر القائمة هذا للعمل الوارد، فقد يتطلب قالب التدقيق أن يتحقق العامل من درجة الحرارة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="72cf4-141">تم تحديد النقطة التي تمت عندها مقاطعة العملية على قالب التدقيق ويمكن أن تكون، على سبيل المثال، عند بدء العمل أو إكماله أو عند تغيير حالته.</span><span class="sxs-lookup"><span data-stu-id="72cf4-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="72cf4-142">وسّع مقطع "فئات العمل".</span><span class="sxs-lookup"><span data-stu-id="72cf4-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="72cf4-143">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="72cf4-143">Click New.</span></span>
14. <span data-ttu-id="72cf4-144">في الحقل "معرف فئة العمل"، اكتب "شراء".</span><span class="sxs-lookup"><span data-stu-id="72cf4-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="72cf4-145">يقوم وعاء العمل بتقييد العمل الذي يمكن استخدام عنصر القائمة له.</span><span class="sxs-lookup"><span data-stu-id="72cf4-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="72cf4-146">في هذه الحالة سيتم استخدامه لبنود أمر العمل المفتوح التي لديها معرف فئة العمل "شراء".</span><span class="sxs-lookup"><span data-stu-id="72cf4-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="72cf4-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="72cf4-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="72cf4-148">إعداد تأكيد العمل</span><span class="sxs-lookup"><span data-stu-id="72cf4-148">Set up work confirmation</span></span>
1. <span data-ttu-id="72cf4-149">انقر فوق "إعداد تأكيد العمل".</span><span class="sxs-lookup"><span data-stu-id="72cf4-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="72cf4-150">في الحقل "نوع العمل"، حدد "انتقاء".</span><span class="sxs-lookup"><span data-stu-id="72cf4-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="72cf4-151">حدد خانة الاختيار "التأكيد التلقائي".</span><span class="sxs-lookup"><span data-stu-id="72cf4-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="72cf4-152">سيتم تأكيد إرشادات العمل ذات نوع العمل "انتقاء" بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="72cf4-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="72cf4-153">لن يتم تقديم هذه الإرشادات للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="72cf4-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="72cf4-154">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="72cf4-154">Click New.</span></span>
5. <span data-ttu-id="72cf4-155">في الحقل "نوع العمل"، حدد "تم وضعه".</span><span class="sxs-lookup"><span data-stu-id="72cf4-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="72cf4-156">حدد خانة الاختيار "تأكيد الموقع".</span><span class="sxs-lookup"><span data-stu-id="72cf4-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="72cf4-157">ستتم مطالبة العامل في المستودع بإجراء فحص تأكيد للموقع، عندما يتم وضع الصنف.</span><span class="sxs-lookup"><span data-stu-id="72cf4-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="72cf4-158">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="72cf4-158">Click Save.</span></span>
8. <span data-ttu-id="72cf4-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-159">Close the page.</span></span>
9. <span data-ttu-id="72cf4-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="72cf4-161">إضافة عنصر القائمة إلى قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="72cf4-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="72cf4-162">انتقل إلى قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="72cf4-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="72cf4-163">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="72cf4-163">Click Edit.</span></span>
3. <span data-ttu-id="72cf4-164">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="72cf4-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="72cf4-165">على سبيل المثال، قم بإجراء التصفية بالحقل "الاسم" باستخدام القيمة "الوارد".</span><span class="sxs-lookup"><span data-stu-id="72cf4-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="72cf4-166">إنك تريد العثور على القائمة التي تستخدمها لعناصر القائمة الواردة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="72cf4-167">في USMF، يسمى ذلك "الوارد‬".</span><span class="sxs-lookup"><span data-stu-id="72cf4-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="72cf4-168">في الشجرة، حدد "قيمة".</span><span class="sxs-lookup"><span data-stu-id="72cf4-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="72cf4-169">انقر فوق المتجه لليمين.</span><span class="sxs-lookup"><span data-stu-id="72cf4-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="72cf4-170">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="72cf4-170">Click Save.</span></span>
7. <span data-ttu-id="72cf4-171">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="72cf4-171">Close the page.</span></span>

