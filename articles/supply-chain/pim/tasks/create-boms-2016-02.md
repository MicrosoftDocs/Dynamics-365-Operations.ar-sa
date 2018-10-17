--- 
title: "إنشاء قوائم مكونات الأصناف (فبراير 2016)"
description: "تركز هذه المهمة على إنشاء بنية قائمة مكونات الصنف لمنتج نهائي ومنتج غير نهائي."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="ba08c-103">إنشاء قوائم مكونات الأصناف (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="ba08c-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba08c-104">تركز هذه المهمة على إنشاء بنية قائمة مكونات الصنف لمنتج نهائي ومنتج غير نهائي.</span><span class="sxs-lookup"><span data-stu-id="ba08c-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="ba08c-105">إنها المهمة الرابعة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ba08c-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="ba08c-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="ba08c-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="ba08c-107">إنشاء قائمة مكونات الصنف لمنتج غير نهائي</span><span class="sxs-lookup"><span data-stu-id="ba08c-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="ba08c-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ba08c-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ba08c-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ba08c-110">حدد رقم الصنف BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ba08c-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="ba08c-111">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="ba08c-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="ba08c-112">انقر فوق "إصدارات قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="ba08c-112">Click BOM versions.</span></span>
5. <span data-ttu-id="ba08c-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ba08c-113">Click New.</span></span>
6. <span data-ttu-id="ba08c-114">انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ba08c-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="ba08c-115">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ba08c-116">على سبيل المثال، اكتب "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="ba08c-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="ba08c-117">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ba08c-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ba08c-118">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="ba08c-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="ba08c-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ba08c-119">Click OK.</span></span>
10. <span data-ttu-id="ba08c-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ba08c-120">Click New.</span></span>
11. <span data-ttu-id="ba08c-121">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ba08c-122">بالنسبة إلى هذا المثال، اكتب ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="ba08c-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="ba08c-123">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ba08c-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ba08c-124">بالنسبة إلى هذا المثال، أدخل أو حدد 11.</span><span class="sxs-lookup"><span data-stu-id="ba08c-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="ba08c-125">انقر فوق "الرأس".</span><span class="sxs-lookup"><span data-stu-id="ba08c-125">Click Header.</span></span>
14. <span data-ttu-id="ba08c-126">انقر فوق "موافقة" للموافقة على قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ba08c-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="ba08c-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ba08c-127">Click OK.</span></span>
16. <span data-ttu-id="ba08c-128">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="ba08c-128">Click Approve.</span></span>
    * <span data-ttu-id="ba08c-129">يقع الزر "موافقة" على شريط الأدوات في مقطع "إصدارات قائمة مكونات الصنف"‬.</span><span class="sxs-lookup"><span data-stu-id="ba08c-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="ba08c-130">إذا لم يكن مرئيًا، فانقر فوق "الرأس" في الجزء العلوي الأيسر من صفحة "قائمة مكونات الصنف" لعرض "موافقة".</span><span class="sxs-lookup"><span data-stu-id="ba08c-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="ba08c-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ba08c-131">Click OK.</span></span>
18. <span data-ttu-id="ba08c-132">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="ba08c-132">Click Activate.</span></span>
19. <span data-ttu-id="ba08c-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-133">Close the page.</span></span>
20. <span data-ttu-id="ba08c-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-134">Close the page.</span></span>
21. <span data-ttu-id="ba08c-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="ba08c-136">إنشاء قائمة مكونات الصنف لمنتج نهائي</span><span class="sxs-lookup"><span data-stu-id="ba08c-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="ba08c-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ba08c-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ba08c-138">حدد رقم الصنف BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ba08c-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="ba08c-139">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="ba08c-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="ba08c-140">انقر فوق "إصدارات قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="ba08c-140">Click BOM versions.</span></span>
4. <span data-ttu-id="ba08c-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ba08c-141">Click New.</span></span>
5. <span data-ttu-id="ba08c-142">انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ba08c-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="ba08c-143">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ba08c-144">على سبيل المثال، اكتب "BOM_1".</span><span class="sxs-lookup"><span data-stu-id="ba08c-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="ba08c-145">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ba08c-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ba08c-146">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="ba08c-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="ba08c-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ba08c-147">Click OK.</span></span>
9. <span data-ttu-id="ba08c-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ba08c-148">Click New.</span></span>
10. <span data-ttu-id="ba08c-149">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ba08c-150">بالنسبة إلى هذا المثال، اكتب ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="ba08c-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="ba08c-151">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ba08c-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ba08c-152">بالنسبة إلى هذا المثال، حدد 11.</span><span class="sxs-lookup"><span data-stu-id="ba08c-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="ba08c-153">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ba08c-153">Click New.</span></span>
13. <span data-ttu-id="ba08c-154">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ba08c-155">بالنسبة إلى هذا المثال، اكتب ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="ba08c-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="ba08c-156">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ba08c-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ba08c-157">بالنسبة إلى هذا المثال، أدخل أو حدد 11.</span><span class="sxs-lookup"><span data-stu-id="ba08c-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="ba08c-158">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ba08c-158">Click New.</span></span>
16. <span data-ttu-id="ba08c-159">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ba08c-160">بالنسبة إلى هذا المثال، اكتب BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ba08c-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="ba08c-161">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ba08c-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="ba08c-162">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ba08c-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ba08c-163">بالنسبة إلى هذا المثال، أدخل أو حدد المستودع 11.</span><span class="sxs-lookup"><span data-stu-id="ba08c-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="ba08c-164">انقر فوق "الرأس".</span><span class="sxs-lookup"><span data-stu-id="ba08c-164">Click Header.</span></span>
20. <span data-ttu-id="ba08c-165">انقر فوق "موافقة" للموافقة على قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ba08c-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="ba08c-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ba08c-166">Click OK.</span></span>
22. <span data-ttu-id="ba08c-167">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="ba08c-167">Click Approve.</span></span>
    * <span data-ttu-id="ba08c-168">يقع الزر "موافقة" على شريط الأدوات في مقطع "إصدارات قائمة مكونات الصنف"‬.</span><span class="sxs-lookup"><span data-stu-id="ba08c-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="ba08c-169">إذا لم يكن مرئيًا، فانقر فوق "الرأس" في الجزء العلوي الأيسر من صفحة "قائمة مكونات الصنف" لعرض "موافقة".</span><span class="sxs-lookup"><span data-stu-id="ba08c-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="ba08c-170">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ba08c-170">Click OK.</span></span>
24. <span data-ttu-id="ba08c-171">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="ba08c-171">Click Activate.</span></span>
25. <span data-ttu-id="ba08c-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-172">Close the page.</span></span>
26. <span data-ttu-id="ba08c-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-173">Close the page.</span></span>
27. <span data-ttu-id="ba08c-174">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba08c-174">Close the page.</span></span>


