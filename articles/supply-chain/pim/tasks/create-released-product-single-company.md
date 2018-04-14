--- 
title: "إنشاء منتج تم إصداره لشركة واحدة"
description: "ينقلك هذا الإجراء عبر عملية إنشاء منتج واحد تم إصداره في سياق وحدة قانونية واحدة."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ced48377f8f6cfdf416bcaf5e2b5e6473998ea91
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="79e42-103">إنشاء منتج تم إصداره لشركة واحدة</span><span class="sxs-lookup"><span data-stu-id="79e42-103">Create a released product for a single company</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79e42-104">ينقلك هذا الإجراء عبر عملية إنشاء منتج واحد تم إصداره في سياق وحدة قانونية واحدة.</span><span class="sxs-lookup"><span data-stu-id="79e42-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="79e42-105">بعد إنشاء المنتج الذي تم إصداره، سيكون متوفرًا على الفور في هذه الوحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="79e42-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="79e42-106">يمكنك التنقل عبر هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="79e42-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="79e42-107">عادة ما يتم تنفيذ هذه المهمة من قبل مصمم منتجات.</span><span class="sxs-lookup"><span data-stu-id="79e42-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="79e42-108">إنشاء منتج تم إصداره</span><span class="sxs-lookup"><span data-stu-id="79e42-108">Create a released product</span></span>
1. <span data-ttu-id="79e42-109">انتقل إلى "المنتجات الصادرة‬".</span><span class="sxs-lookup"><span data-stu-id="79e42-109">Go to Released products.</span></span>
2. <span data-ttu-id="79e42-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="79e42-110">Click New.</span></span>
3. <span data-ttu-id="79e42-111">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="79e42-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="79e42-112">إذا لم يتم إدخال رقم منتج في حقل "رقم المنتج" تلقائيًا، فاكتب رقم منتج فريد.</span><span class="sxs-lookup"><span data-stu-id="79e42-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="79e42-113">يلزم هذه الخطوة فقط إذا لم يتم تعيين تسلسل رقمي الأرقام المنتج.</span><span class="sxs-lookup"><span data-stu-id="79e42-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="79e42-114">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="79e42-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="79e42-115">يتم وضع اسم المنتج الافتراضي تبعًا لاسم البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="79e42-116">إذا لزم الأمر، يمكنك تحديد تغيير اسم البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="79e42-117">في الحقل "مجموعة نماذج الصنف‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-118">وتحتوي مجموعات نموذج الصنف على الإعدادات التي تحدد كيفية التحكم في الأصناف ومعالجتها في إيصالات الأصناف وإصداراتها.</span><span class="sxs-lookup"><span data-stu-id="79e42-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="79e42-119">تحدد الإعدادات أيضًا كيف يتم حساب استهلاك الأصناف.</span><span class="sxs-lookup"><span data-stu-id="79e42-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="79e42-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="79e42-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="79e42-122">في الحقل "مجموعة الأصناف‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-123">تستخدم مجموعات الأصناف لإدارة المخزون بتقسيم أصناف المخزون إلى مجموعات بناءً على خصائص الصنف.</span><span class="sxs-lookup"><span data-stu-id="79e42-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="79e42-124">على سبيل المثال، لإدارة كيفية ترحيل المعلومات للحسابات الرئيسية، يمكنك إنشاء سلسلة من مجموعات أصناف مختلفة مرتبطة بالحسابات الرئيسية المحددة.</span><span class="sxs-lookup"><span data-stu-id="79e42-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="79e42-125">يتيح لك هذا الأمر إمكانية تعقب قيمة المخزون للأصناف بمراحل مختلفة.</span><span class="sxs-lookup"><span data-stu-id="79e42-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="79e42-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="79e42-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="79e42-128">في الحقل "مجموعة أبعاد التخزين‬‬‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-129">تساعدك أبعاد التخزين على التحكم في كيفية تخزين الأصناف وأخذها من المخزون.</span><span class="sxs-lookup"><span data-stu-id="79e42-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="79e42-130">على سبيل المثال، قد يكون الموقع والمستودع عبارة عن بُعد تخزين.</span><span class="sxs-lookup"><span data-stu-id="79e42-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="79e42-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="79e42-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="79e42-133">في الحقل "مجموعة أبعاد التعقب‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-134">تحدد مجموعة بُعد التعقب أبعاد التعقب التي يمكنك إضافتها إلى منتج.</span><span class="sxs-lookup"><span data-stu-id="79e42-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="79e42-135">على سبيل المثال، يُستخدم رقم الدفعة والرقم المسلسل لتعقب أصناف المخزون.</span><span class="sxs-lookup"><span data-stu-id="79e42-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="79e42-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="79e42-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="79e42-138">في الحقل "وحدة المخزون‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-139">يحدد وحدة المخزون كيفية تحديد كمية المنتج عند تخزينه في المخزون.</span><span class="sxs-lookup"><span data-stu-id="79e42-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="79e42-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="79e42-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="79e42-142">في الحقل "وحدة الشراء‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-143">تحدد وحدة الشراء كيف يتم تحديد كمية المنتج عندما يتم شراؤها من مورد.</span><span class="sxs-lookup"><span data-stu-id="79e42-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="79e42-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="79e42-145">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="79e42-146">في الحقل "وحدة المبيعات‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-147">تحدد وحدة المبيعات كيف يتم تحديد كمية المنتج عند بيعه إلى عميل.</span><span class="sxs-lookup"><span data-stu-id="79e42-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="79e42-148">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="79e42-149">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="79e42-150">في الحقل "وحدة قائمة مكونات الصنف‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-151">تحدد وحدة قائمة مكونات الصنف كيف يتم تحديد كمية المنتج عند إدراجه في قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="79e42-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="79e42-152">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="79e42-153">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="79e42-154">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-155">تحدد مجموعة ضريبة مبيعات الصنف في مجموعة ضرائب المبيعات كيف يتم حساب ضريبة المبيعات لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="79e42-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="79e42-156">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="79e42-157">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="79e42-158">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="79e42-159">تحدد مجموعة ضريبة مبيعات الصنف في مجموعة ضرائب الشراء كيف يتم حساب ضريبة الشراء لكل صنف.</span><span class="sxs-lookup"><span data-stu-id="79e42-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="79e42-160">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="79e42-161">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="79e42-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="79e42-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="79e42-163">إضافة خصائص المنتج</span><span class="sxs-lookup"><span data-stu-id="79e42-163">Add product characteristics</span></span>
1. <span data-ttu-id="79e42-164">قم بتوسيع أو طي قسم إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="79e42-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="79e42-165">في الحقل "الوزن الصافي‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79e42-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="79e42-166">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79e42-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="79e42-167">في الحقل "إجمالي العمق‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79e42-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="79e42-168">في الحقل "إجمالي العرض‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79e42-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="79e42-169">في الحقل "إجمالي الارتفاع‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79e42-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="79e42-170">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="79e42-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="79e42-171">إضافة الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="79e42-171">Add financial dimensions</span></span>
1. <span data-ttu-id="79e42-172">قم بتوسيع القسم "الأبعاد المالية" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="79e42-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="79e42-173">في الحقل "BusinessUnit‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="79e42-174">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="79e42-175">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="79e42-176">في الحقل "CostCenter"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="79e42-177">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="79e42-178">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="79e42-179">في الحقل "القسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="79e42-180">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="79e42-181">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="79e42-182">في الحقل "ItemGroup"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="79e42-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="79e42-183">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="79e42-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="79e42-184">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="79e42-184">In the list, click the link in the selected row.</span></span>


