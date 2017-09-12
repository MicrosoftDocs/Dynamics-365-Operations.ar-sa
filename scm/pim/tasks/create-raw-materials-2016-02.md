--- 
title: "إنشاء المواد الخام (فبراير 2016 فقط)"
description: "تركز هذه المهمة على إنشاء مكونات منتجات نهائية وغير نهائية."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1c10e0f8275d928c1455cd99105aece8780e7f0
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="f9aae-103">إنشاء المواد الخام (فبراير 2016 فقط)</span><span class="sxs-lookup"><span data-stu-id="f9aae-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9aae-104">تركز هذه المهمة على إنشاء مكونات منتجات نهائية وغير نهائية.</span><span class="sxs-lookup"><span data-stu-id="f9aae-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="f9aae-105">إنها المهمة الثالثة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="f9aae-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="f9aae-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="f9aae-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="f9aae-107">إنشاء المواد الأولى</span><span class="sxs-lookup"><span data-stu-id="f9aae-107">Create the first material</span></span>
1. <span data-ttu-id="f9aae-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f9aae-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f9aae-109">Click New.</span></span>
3. <span data-ttu-id="f9aae-110">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f9aae-111">بالنسبة إلى هذا المثال، أدخل ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f9aae-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="f9aae-112">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-113">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="f9aae-113">Select STD.</span></span> <span data-ttu-id="f9aae-114">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f9aae-115">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-116">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="f9aae-116">For example, select Audio.</span></span> <span data-ttu-id="f9aae-117">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f9aae-118">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-119">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f9aae-119">Select SiteWH.</span></span> <span data-ttu-id="f9aae-120">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="f9aae-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="f9aae-121">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-122">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="f9aae-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f9aae-123">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="f9aae-123">Select None.</span></span>  
8. <span data-ttu-id="f9aae-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f9aae-124">Click OK.</span></span>
9. <span data-ttu-id="f9aae-125">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="f9aae-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f9aae-126">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="f9aae-126">Click Default order settings.</span></span>
11. <span data-ttu-id="f9aae-127">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-128">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f9aae-129">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-130">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f9aae-131">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-132">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f9aae-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-133">Close the page.</span></span>
15. <span data-ttu-id="f9aae-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-134">Close the page.</span></span>
16. <span data-ttu-id="f9aae-135">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f9aae-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f9aae-136">انقر فوق ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f9aae-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="f9aae-137">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="f9aae-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="f9aae-138">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f9aae-139">بالنسبة إلى هذا المثال، اكتب M2.</span><span class="sxs-lookup"><span data-stu-id="f9aae-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="f9aae-140">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="f9aae-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="f9aae-141">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="f9aae-141">Click Item price.</span></span>
21. <span data-ttu-id="f9aae-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f9aae-142">Click New.</span></span>
22. <span data-ttu-id="f9aae-143">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-144">بالنسبة إلى هذا المثال، حدد 10، وهو نوع التكاليف − تكلفة معيارية.‬</span><span class="sxs-lookup"><span data-stu-id="f9aae-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="f9aae-145">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-146">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="f9aae-147">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f9aae-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f9aae-148">بالنسبة إلى هذا المثال، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="f9aae-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="f9aae-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f9aae-149">Click Save.</span></span>
26. <span data-ttu-id="f9aae-150">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="f9aae-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="f9aae-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-151">Close the page.</span></span>
28. <span data-ttu-id="f9aae-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="f9aae-153">إنشاء المواد الثانية</span><span class="sxs-lookup"><span data-stu-id="f9aae-153">Create the second material</span></span>
1. <span data-ttu-id="f9aae-154">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f9aae-154">Click New.</span></span>
2. <span data-ttu-id="f9aae-155">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f9aae-156">بالنسبة إلى هذا المثال، اكتب ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f9aae-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="f9aae-157">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-158">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="f9aae-158">Select STD.</span></span> <span data-ttu-id="f9aae-159">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f9aae-160">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-161">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="f9aae-161">For example, select Audio.</span></span> <span data-ttu-id="f9aae-162">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f9aae-163">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-164">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f9aae-164">Select SiteWH.</span></span> <span data-ttu-id="f9aae-165">سيتم استخدام الموقع والمستودع فقط لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="f9aae-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="f9aae-166">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-167">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="f9aae-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f9aae-168">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="f9aae-168">Select None.</span></span>  
7. <span data-ttu-id="f9aae-169">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f9aae-169">Click OK.</span></span>
8. <span data-ttu-id="f9aae-170">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="f9aae-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f9aae-171">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="f9aae-171">Click Default order settings.</span></span>
10. <span data-ttu-id="f9aae-172">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-173">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f9aae-174">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-175">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f9aae-176">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-177">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f9aae-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-178">Close the page.</span></span>
14. <span data-ttu-id="f9aae-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-179">Close the page.</span></span>
15. <span data-ttu-id="f9aae-180">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f9aae-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f9aae-181">انقر فوق ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f9aae-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="f9aae-182">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="f9aae-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f9aae-183">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f9aae-184">بالنسبة إلى هذا المثال، اكتب M2.</span><span class="sxs-lookup"><span data-stu-id="f9aae-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="f9aae-185">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="f9aae-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f9aae-186">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="f9aae-186">Click Item price.</span></span>
20. <span data-ttu-id="f9aae-187">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f9aae-187">Click New.</span></span>
21. <span data-ttu-id="f9aae-188">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-189">بالنسبة إلى هذا المثال، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="f9aae-189">For this example, select 10.</span></span> <span data-ttu-id="f9aae-190">هذا هو نوع التكاليف − تكلفة معيارية.</span><span class="sxs-lookup"><span data-stu-id="f9aae-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f9aae-191">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-192">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f9aae-193">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f9aae-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f9aae-194">للعرض التوضيحي، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="f9aae-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="f9aae-195">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f9aae-195">Click Save.</span></span>
25. <span data-ttu-id="f9aae-196">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="f9aae-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f9aae-197">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-197">Close the page.</span></span>
27. <span data-ttu-id="f9aae-198">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="f9aae-199">إنشاء المواد الثالثة</span><span class="sxs-lookup"><span data-stu-id="f9aae-199">Create the third material</span></span>
1. <span data-ttu-id="f9aae-200">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f9aae-200">Click New.</span></span>
2. <span data-ttu-id="f9aae-201">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f9aae-202">للعرض التوضيحي، اكتب ITEM_C</span><span class="sxs-lookup"><span data-stu-id="f9aae-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="f9aae-203">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-204">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="f9aae-204">Select STD.</span></span> <span data-ttu-id="f9aae-205">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f9aae-206">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-207">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="f9aae-207">For example, select Audio.</span></span> <span data-ttu-id="f9aae-208">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f9aae-209">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-210">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f9aae-210">Select SiteWH.</span></span> <span data-ttu-id="f9aae-211">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="f9aae-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="f9aae-212">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-213">لن يتم استخدام أبعاد التعقب لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="f9aae-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f9aae-214">حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="f9aae-214">Select None.</span></span>  
7. <span data-ttu-id="f9aae-215">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f9aae-215">Click OK.</span></span>
8. <span data-ttu-id="f9aae-216">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="f9aae-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f9aae-217">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="f9aae-217">Click Default order settings.</span></span>
10. <span data-ttu-id="f9aae-218">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-219">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f9aae-220">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-221">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f9aae-222">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-223">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f9aae-224">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-224">Close the page.</span></span>
14. <span data-ttu-id="f9aae-225">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-225">Close the page.</span></span>
15. <span data-ttu-id="f9aae-226">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f9aae-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f9aae-227">انقر فوق ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="f9aae-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="f9aae-228">قم بتوسيع القسم "إدارة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="f9aae-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f9aae-229">في الحقل "مجموعة التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f9aae-230">بالنسبة إلى هذا المثال، اكتب M1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="f9aae-231">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="f9aae-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f9aae-232">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="f9aae-232">Click Item price.</span></span>
20. <span data-ttu-id="f9aae-233">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f9aae-233">Click New.</span></span>
21. <span data-ttu-id="f9aae-234">في حقل "الإصدار"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-235">بالنسبة إلى هذا المثال، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="f9aae-235">For this example, select 10.</span></span> <span data-ttu-id="f9aae-236">هذا هو نوع التكاليف − تكلفة معيارية.</span><span class="sxs-lookup"><span data-stu-id="f9aae-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f9aae-237">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f9aae-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f9aae-238">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f9aae-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f9aae-239">في حقل "السعر"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f9aae-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f9aae-240">بالنسبة إلى هذا المثال، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="f9aae-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="f9aae-241">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f9aae-241">Click Save.</span></span>
25. <span data-ttu-id="f9aae-242">انقر فوق "تنشيط السعر (الأسعار) المعلقة".</span><span class="sxs-lookup"><span data-stu-id="f9aae-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f9aae-243">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-243">Close the page.</span></span>
27. <span data-ttu-id="f9aae-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f9aae-244">Close the page.</span></span>


