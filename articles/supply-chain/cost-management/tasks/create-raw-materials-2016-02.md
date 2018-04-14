--- 
title: "إنشاء المواد الخام (فبراير 2016 فقط)"
description: "تركز هذه المهمة على إنشاء مكونات منتجات نهائية وغير نهائية."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5a31ceacb7037164d35e38fb70a013b33d670d94
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="cdc79-103">إنشاء المواد الخام (فبراير 2016 فقط)</span><span class="sxs-lookup"><span data-stu-id="cdc79-103">Create raw materials (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cdc79-104">تركز هذه المهمة على إنشاء مكونات منتجات نهائية وغير نهائية.</span><span class="sxs-lookup"><span data-stu-id="cdc79-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="cdc79-105">إنها المهمة الثالثة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="cdc79-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="cdc79-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="cdc79-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="cdc79-107">إنشاء المواد الأولى</span><span class="sxs-lookup"><span data-stu-id="cdc79-107">Create the first material</span></span>
1. <span data-ttu-id="cdc79-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="cdc79-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cdc79-109">Click New.</span></span>
3. <span data-ttu-id="cdc79-110">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdc79-111">بالنسبة إلى هذا المثال، أدخل ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="cdc79-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="cdc79-112">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-113">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="cdc79-113">Select STD.</span></span> <span data-ttu-id="cdc79-114">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="cdc79-115">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-116">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="cdc79-116">For example, select Audio.</span></span> <span data-ttu-id="cdc79-117">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="cdc79-118">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-119">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="cdc79-119">Select SiteWH.</span></span> <span data-ttu-id="cdc79-120">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="cdc79-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="cdc79-121">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-122">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="cdc79-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="cdc79-123">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="cdc79-123">Select None.</span></span>  
8. <span data-ttu-id="cdc79-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cdc79-124">Click OK.</span></span>
9. <span data-ttu-id="cdc79-125">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="cdc79-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="cdc79-126">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="cdc79-126">Click Default order settings.</span></span>
11. <span data-ttu-id="cdc79-127">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-128">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="cdc79-129">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-130">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="cdc79-131">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-132">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="cdc79-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-133">Close the page.</span></span>
15. <span data-ttu-id="cdc79-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-134">Close the page.</span></span>
16. <span data-ttu-id="cdc79-135">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cdc79-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdc79-136">انقر فوق ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="cdc79-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="cdc79-137">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="cdc79-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="cdc79-138">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="cdc79-139">بالنسبة إلى هذا المثال، اكتب M2.</span><span class="sxs-lookup"><span data-stu-id="cdc79-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="cdc79-140">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="cdc79-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="cdc79-141">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="cdc79-141">Click Item price.</span></span>
21. <span data-ttu-id="cdc79-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cdc79-142">Click New.</span></span>
22. <span data-ttu-id="cdc79-143">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-144">بالنسبة إلى هذا المثال، حدد 10، وهو نوع التكاليف − تكلفة معيارية.‬</span><span class="sxs-lookup"><span data-stu-id="cdc79-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="cdc79-145">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-146">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="cdc79-147">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cdc79-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="cdc79-148">بالنسبة إلى هذا المثال، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="cdc79-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="cdc79-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cdc79-149">Click Save.</span></span>
26. <span data-ttu-id="cdc79-150">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="cdc79-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="cdc79-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-151">Close the page.</span></span>
28. <span data-ttu-id="cdc79-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="cdc79-153">إنشاء المواد الثانية</span><span class="sxs-lookup"><span data-stu-id="cdc79-153">Create the second material</span></span>
1. <span data-ttu-id="cdc79-154">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cdc79-154">Click New.</span></span>
2. <span data-ttu-id="cdc79-155">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdc79-156">بالنسبة إلى هذا المثال، اكتب ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="cdc79-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="cdc79-157">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-158">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="cdc79-158">Select STD.</span></span> <span data-ttu-id="cdc79-159">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="cdc79-160">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-161">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="cdc79-161">For example, select Audio.</span></span> <span data-ttu-id="cdc79-162">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="cdc79-163">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-164">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="cdc79-164">Select SiteWH.</span></span> <span data-ttu-id="cdc79-165">سيتم استخدام الموقع والمستودع فقط لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="cdc79-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="cdc79-166">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-167">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="cdc79-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="cdc79-168">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="cdc79-168">Select None.</span></span>  
7. <span data-ttu-id="cdc79-169">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cdc79-169">Click OK.</span></span>
8. <span data-ttu-id="cdc79-170">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="cdc79-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="cdc79-171">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="cdc79-171">Click Default order settings.</span></span>
10. <span data-ttu-id="cdc79-172">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-173">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="cdc79-174">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-175">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="cdc79-176">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-177">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="cdc79-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-178">Close the page.</span></span>
14. <span data-ttu-id="cdc79-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-179">Close the page.</span></span>
15. <span data-ttu-id="cdc79-180">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cdc79-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdc79-181">انقر فوق ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="cdc79-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="cdc79-182">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="cdc79-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="cdc79-183">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="cdc79-184">بالنسبة إلى هذا المثال، اكتب M2.</span><span class="sxs-lookup"><span data-stu-id="cdc79-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="cdc79-185">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="cdc79-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="cdc79-186">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="cdc79-186">Click Item price.</span></span>
20. <span data-ttu-id="cdc79-187">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cdc79-187">Click New.</span></span>
21. <span data-ttu-id="cdc79-188">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-189">بالنسبة إلى هذا المثال، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="cdc79-189">For this example, select 10.</span></span> <span data-ttu-id="cdc79-190">هذا هو نوع التكاليف − تكلفة معيارية.</span><span class="sxs-lookup"><span data-stu-id="cdc79-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="cdc79-191">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-192">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="cdc79-193">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cdc79-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="cdc79-194">للعرض التوضيحي، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="cdc79-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="cdc79-195">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cdc79-195">Click Save.</span></span>
25. <span data-ttu-id="cdc79-196">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="cdc79-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="cdc79-197">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-197">Close the page.</span></span>
27. <span data-ttu-id="cdc79-198">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="cdc79-199">إنشاء المواد الثالثة</span><span class="sxs-lookup"><span data-stu-id="cdc79-199">Create the third material</span></span>
1. <span data-ttu-id="cdc79-200">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cdc79-200">Click New.</span></span>
2. <span data-ttu-id="cdc79-201">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdc79-202">للعرض التوضيحي، اكتب ITEM_C</span><span class="sxs-lookup"><span data-stu-id="cdc79-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="cdc79-203">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-204">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="cdc79-204">Select STD.</span></span> <span data-ttu-id="cdc79-205">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="cdc79-206">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-207">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="cdc79-207">For example, select Audio.</span></span> <span data-ttu-id="cdc79-208">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="cdc79-209">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-210">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="cdc79-210">Select SiteWH.</span></span> <span data-ttu-id="cdc79-211">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="cdc79-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="cdc79-212">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-213">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="cdc79-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="cdc79-214">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="cdc79-214">Select None.</span></span>  
7. <span data-ttu-id="cdc79-215">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cdc79-215">Click OK.</span></span>
8. <span data-ttu-id="cdc79-216">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="cdc79-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="cdc79-217">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="cdc79-217">Click Default order settings.</span></span>
10. <span data-ttu-id="cdc79-218">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-219">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="cdc79-220">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-221">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="cdc79-222">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-223">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="cdc79-224">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-224">Close the page.</span></span>
14. <span data-ttu-id="cdc79-225">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-225">Close the page.</span></span>
15. <span data-ttu-id="cdc79-226">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cdc79-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdc79-227">انقر فوق ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="cdc79-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="cdc79-228">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="cdc79-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="cdc79-229">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="cdc79-230">بالنسبة إلى هذا المثال، اكتب M1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="cdc79-231">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="cdc79-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="cdc79-232">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="cdc79-232">Click Item price.</span></span>
20. <span data-ttu-id="cdc79-233">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cdc79-233">Click New.</span></span>
21. <span data-ttu-id="cdc79-234">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-235">بالنسبة إلى هذا المثال، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="cdc79-235">For this example, select 10.</span></span> <span data-ttu-id="cdc79-236">هذا هو نوع التكاليف − تكلفة معيارية.</span><span class="sxs-lookup"><span data-stu-id="cdc79-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="cdc79-237">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cdc79-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdc79-238">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="cdc79-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="cdc79-239">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cdc79-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="cdc79-240">بالنسبة إلى هذا المثال، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="cdc79-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="cdc79-241">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cdc79-241">Click Save.</span></span>
25. <span data-ttu-id="cdc79-242">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="cdc79-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="cdc79-243">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-243">Close the page.</span></span>
27. <span data-ttu-id="cdc79-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cdc79-244">Close the page.</span></span>


