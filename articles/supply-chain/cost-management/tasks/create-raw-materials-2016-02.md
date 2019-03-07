---
title: إنشاء المواد الخام (فبراير 2016 فقط)
description: تركز هذه المهمة على إنشاء مكونات منتجات نهائية وغير نهائية.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 869acddf6f7e9754bb4952176ded4b22c74eaffd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "327287"
---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="4f847-103">إنشاء المواد الخام (فبراير 2016 فقط)</span><span class="sxs-lookup"><span data-stu-id="4f847-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f847-104">تركز هذه المهمة على إنشاء مكونات منتجات نهائية وغير نهائية.</span><span class="sxs-lookup"><span data-stu-id="4f847-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="4f847-105">إنها المهمة الثالثة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="4f847-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="4f847-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="4f847-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="4f847-107">إنشاء المواد الأولى</span><span class="sxs-lookup"><span data-stu-id="4f847-107">Create the first material</span></span>
1. <span data-ttu-id="4f847-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="4f847-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4f847-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4f847-109">Click New.</span></span>
3. <span data-ttu-id="4f847-110">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4f847-111">بالنسبة إلى هذا المثال، أدخل ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="4f847-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="4f847-112">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-113">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="4f847-113">Select STD.</span></span> <span data-ttu-id="4f847-114">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4f847-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="4f847-115">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-116">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="4f847-116">For example, select Audio.</span></span> <span data-ttu-id="4f847-117">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4f847-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="4f847-118">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-119">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="4f847-119">Select SiteWH.</span></span> <span data-ttu-id="4f847-120">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="4f847-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="4f847-121">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-122">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="4f847-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="4f847-123">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="4f847-123">Select None.</span></span>  
8. <span data-ttu-id="4f847-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4f847-124">Click OK.</span></span>
9. <span data-ttu-id="4f847-125">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="4f847-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="4f847-126">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="4f847-126">Click Default order settings.</span></span>
11. <span data-ttu-id="4f847-127">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-128">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="4f847-129">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-130">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="4f847-131">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-132">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="4f847-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-133">Close the page.</span></span>
15. <span data-ttu-id="4f847-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-134">Close the page.</span></span>
16. <span data-ttu-id="4f847-135">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f847-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4f847-136">انقر فوق ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="4f847-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="4f847-137">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="4f847-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="4f847-138">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="4f847-139">بالنسبة إلى هذا المثال، اكتب M2.</span><span class="sxs-lookup"><span data-stu-id="4f847-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="4f847-140">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="4f847-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="4f847-141">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="4f847-141">Click Item price.</span></span>
21. <span data-ttu-id="4f847-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4f847-142">Click New.</span></span>
22. <span data-ttu-id="4f847-143">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-144">بالنسبة إلى هذا المثال، حدد 10، وهو نوع التكاليف − تكلفة معيارية.‬</span><span class="sxs-lookup"><span data-stu-id="4f847-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="4f847-145">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-146">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="4f847-147">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4f847-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="4f847-148">بالنسبة إلى هذا المثال، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="4f847-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="4f847-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4f847-149">Click Save.</span></span>
26. <span data-ttu-id="4f847-150">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="4f847-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="4f847-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-151">Close the page.</span></span>
28. <span data-ttu-id="4f847-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="4f847-153">إنشاء المواد الثانية</span><span class="sxs-lookup"><span data-stu-id="4f847-153">Create the second material</span></span>
1. <span data-ttu-id="4f847-154">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4f847-154">Click New.</span></span>
2. <span data-ttu-id="4f847-155">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4f847-156">بالنسبة إلى هذا المثال، اكتب ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="4f847-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="4f847-157">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-158">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="4f847-158">Select STD.</span></span> <span data-ttu-id="4f847-159">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4f847-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="4f847-160">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-161">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="4f847-161">For example, select Audio.</span></span> <span data-ttu-id="4f847-162">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4f847-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="4f847-163">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-164">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="4f847-164">Select SiteWH.</span></span> <span data-ttu-id="4f847-165">سيتم استخدام الموقع والمستودع فقط لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="4f847-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="4f847-166">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-167">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="4f847-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="4f847-168">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="4f847-168">Select None.</span></span>  
7. <span data-ttu-id="4f847-169">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4f847-169">Click OK.</span></span>
8. <span data-ttu-id="4f847-170">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="4f847-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="4f847-171">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="4f847-171">Click Default order settings.</span></span>
10. <span data-ttu-id="4f847-172">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-173">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="4f847-174">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-175">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="4f847-176">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-177">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="4f847-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-178">Close the page.</span></span>
14. <span data-ttu-id="4f847-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-179">Close the page.</span></span>
15. <span data-ttu-id="4f847-180">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f847-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4f847-181">انقر فوق ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="4f847-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="4f847-182">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="4f847-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="4f847-183">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="4f847-184">بالنسبة إلى هذا المثال، اكتب M2.</span><span class="sxs-lookup"><span data-stu-id="4f847-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="4f847-185">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="4f847-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="4f847-186">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="4f847-186">Click Item price.</span></span>
20. <span data-ttu-id="4f847-187">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4f847-187">Click New.</span></span>
21. <span data-ttu-id="4f847-188">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-189">بالنسبة إلى هذا المثال، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="4f847-189">For this example, select 10.</span></span> <span data-ttu-id="4f847-190">هذا هو نوع التكاليف − تكلفة معيارية.</span><span class="sxs-lookup"><span data-stu-id="4f847-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="4f847-191">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-192">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="4f847-193">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4f847-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="4f847-194">للعرض التوضيحي، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="4f847-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="4f847-195">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4f847-195">Click Save.</span></span>
25. <span data-ttu-id="4f847-196">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="4f847-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="4f847-197">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-197">Close the page.</span></span>
27. <span data-ttu-id="4f847-198">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="4f847-199">إنشاء المواد الثالثة</span><span class="sxs-lookup"><span data-stu-id="4f847-199">Create the third material</span></span>
1. <span data-ttu-id="4f847-200">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4f847-200">Click New.</span></span>
2. <span data-ttu-id="4f847-201">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4f847-202">للعرض التوضيحي، اكتب ITEM_C</span><span class="sxs-lookup"><span data-stu-id="4f847-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="4f847-203">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-204">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="4f847-204">Select STD.</span></span> <span data-ttu-id="4f847-205">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4f847-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="4f847-206">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-207">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="4f847-207">For example, select Audio.</span></span> <span data-ttu-id="4f847-208">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="4f847-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="4f847-209">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-210">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="4f847-210">Select SiteWH.</span></span> <span data-ttu-id="4f847-211">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="4f847-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="4f847-212">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-213">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="4f847-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="4f847-214">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="4f847-214">Select None.</span></span>  
7. <span data-ttu-id="4f847-215">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4f847-215">Click OK.</span></span>
8. <span data-ttu-id="4f847-216">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="4f847-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="4f847-217">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="4f847-217">Click Default order settings.</span></span>
10. <span data-ttu-id="4f847-218">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-219">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="4f847-220">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-221">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="4f847-222">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-223">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="4f847-224">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-224">Close the page.</span></span>
14. <span data-ttu-id="4f847-225">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-225">Close the page.</span></span>
15. <span data-ttu-id="4f847-226">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f847-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4f847-227">انقر فوق ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="4f847-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="4f847-228">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="4f847-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="4f847-229">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="4f847-230">بالنسبة إلى هذا المثال، اكتب M1.</span><span class="sxs-lookup"><span data-stu-id="4f847-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="4f847-231">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="4f847-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="4f847-232">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="4f847-232">Click Item price.</span></span>
20. <span data-ttu-id="4f847-233">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4f847-233">Click New.</span></span>
21. <span data-ttu-id="4f847-234">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="4f847-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-235">بالنسبة إلى هذا المثال، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="4f847-235">For this example, select 10.</span></span> <span data-ttu-id="4f847-236">هذا هو نوع التكاليف − تكلفة معيارية.</span><span class="sxs-lookup"><span data-stu-id="4f847-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="4f847-237">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4f847-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="4f847-238">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="4f847-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="4f847-239">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4f847-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="4f847-240">بالنسبة إلى هذا المثال، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="4f847-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="4f847-241">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4f847-241">Click Save.</span></span>
25. <span data-ttu-id="4f847-242">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="4f847-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="4f847-243">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-243">Close the page.</span></span>
27. <span data-ttu-id="4f847-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f847-244">Close the page.</span></span>

