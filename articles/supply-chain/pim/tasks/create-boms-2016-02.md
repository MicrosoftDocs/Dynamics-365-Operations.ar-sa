---
title: إنشاء قوائم مكونات الأصناف (فبراير 2016)
description: تركز هذه المهمة على إنشاء بنية قائمة مكونات الصنف لمنتج نهائي ومنتج غير نهائي.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "333198"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="eb489-103">إنشاء قوائم مكونات الأصناف (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="eb489-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb489-104">تركز هذه المهمة على إنشاء بنية قائمة مكونات الصنف لمنتج نهائي ومنتج غير نهائي.</span><span class="sxs-lookup"><span data-stu-id="eb489-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="eb489-105">إنها المهمة الرابعة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="eb489-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="eb489-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="eb489-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="eb489-107">إنشاء قائمة مكونات الصنف لمنتج غير نهائي</span><span class="sxs-lookup"><span data-stu-id="eb489-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="eb489-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="eb489-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="eb489-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="eb489-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="eb489-110">حدد رقم الصنف BOM_2.</span><span class="sxs-lookup"><span data-stu-id="eb489-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="eb489-111">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="eb489-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="eb489-112">انقر فوق "إصدارات قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="eb489-112">Click BOM versions.</span></span>
5. <span data-ttu-id="eb489-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="eb489-113">Click New.</span></span>
6. <span data-ttu-id="eb489-114">انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="eb489-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="eb489-115">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="eb489-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eb489-116">على سبيل المثال، اكتب "BOM_2".</span><span class="sxs-lookup"><span data-stu-id="eb489-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="eb489-117">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="eb489-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="eb489-118">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="eb489-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="eb489-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="eb489-119">Click OK.</span></span>
10. <span data-ttu-id="eb489-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="eb489-120">Click New.</span></span>
11. <span data-ttu-id="eb489-121">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="eb489-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="eb489-122">بالنسبة إلى هذا المثال، اكتب ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="eb489-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="eb489-123">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="eb489-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="eb489-124">بالنسبة إلى هذا المثال، أدخل أو حدد 11.</span><span class="sxs-lookup"><span data-stu-id="eb489-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="eb489-125">انقر فوق "الرأس".</span><span class="sxs-lookup"><span data-stu-id="eb489-125">Click Header.</span></span>
14. <span data-ttu-id="eb489-126">انقر فوق "موافقة" للموافقة على قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="eb489-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="eb489-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="eb489-127">Click OK.</span></span>
16. <span data-ttu-id="eb489-128">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="eb489-128">Click Approve.</span></span>
    * <span data-ttu-id="eb489-129">يقع الزر "موافقة" على شريط الأدوات في مقطع "إصدارات قائمة مكونات الصنف"‬.</span><span class="sxs-lookup"><span data-stu-id="eb489-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="eb489-130">إذا لم يكن مرئيًا، فانقر فوق "الرأس" في الجزء العلوي الأيسر من صفحة "قائمة مكونات الصنف" لعرض "موافقة".</span><span class="sxs-lookup"><span data-stu-id="eb489-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="eb489-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="eb489-131">Click OK.</span></span>
18. <span data-ttu-id="eb489-132">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="eb489-132">Click Activate.</span></span>
19. <span data-ttu-id="eb489-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="eb489-133">Close the page.</span></span>
20. <span data-ttu-id="eb489-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="eb489-134">Close the page.</span></span>
21. <span data-ttu-id="eb489-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="eb489-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="eb489-136">إنشاء قائمة مكونات الصنف لمنتج نهائي</span><span class="sxs-lookup"><span data-stu-id="eb489-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="eb489-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="eb489-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="eb489-138">حدد رقم الصنف BOM_1.</span><span class="sxs-lookup"><span data-stu-id="eb489-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="eb489-139">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="eb489-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="eb489-140">انقر فوق "إصدارات قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="eb489-140">Click BOM versions.</span></span>
4. <span data-ttu-id="eb489-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="eb489-141">Click New.</span></span>
5. <span data-ttu-id="eb489-142">انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="eb489-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="eb489-143">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="eb489-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eb489-144">على سبيل المثال، اكتب "BOM_1".</span><span class="sxs-lookup"><span data-stu-id="eb489-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="eb489-145">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="eb489-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="eb489-146">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="eb489-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="eb489-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="eb489-147">Click OK.</span></span>
9. <span data-ttu-id="eb489-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="eb489-148">Click New.</span></span>
10. <span data-ttu-id="eb489-149">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="eb489-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="eb489-150">بالنسبة إلى هذا المثال، اكتب ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="eb489-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="eb489-151">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="eb489-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="eb489-152">بالنسبة إلى هذا المثال، حدد 11.</span><span class="sxs-lookup"><span data-stu-id="eb489-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="eb489-153">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="eb489-153">Click New.</span></span>
13. <span data-ttu-id="eb489-154">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="eb489-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="eb489-155">بالنسبة إلى هذا المثال، اكتب ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="eb489-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="eb489-156">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="eb489-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="eb489-157">بالنسبة إلى هذا المثال، أدخل أو حدد 11.</span><span class="sxs-lookup"><span data-stu-id="eb489-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="eb489-158">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="eb489-158">Click New.</span></span>
16. <span data-ttu-id="eb489-159">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="eb489-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="eb489-160">بالنسبة إلى هذا المثال، اكتب BOM_2.</span><span class="sxs-lookup"><span data-stu-id="eb489-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="eb489-161">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="eb489-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="eb489-162">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="eb489-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="eb489-163">بالنسبة إلى هذا المثال، أدخل أو حدد المستودع 11.</span><span class="sxs-lookup"><span data-stu-id="eb489-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="eb489-164">انقر فوق "الرأس".</span><span class="sxs-lookup"><span data-stu-id="eb489-164">Click Header.</span></span>
20. <span data-ttu-id="eb489-165">انقر فوق "موافقة" للموافقة على قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="eb489-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="eb489-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="eb489-166">Click OK.</span></span>
22. <span data-ttu-id="eb489-167">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="eb489-167">Click Approve.</span></span>
    * <span data-ttu-id="eb489-168">يقع الزر "موافقة" على شريط الأدوات في مقطع "إصدارات قائمة مكونات الصنف"‬.</span><span class="sxs-lookup"><span data-stu-id="eb489-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="eb489-169">إذا لم يكن مرئيًا، فانقر فوق "الرأس" في الجزء العلوي الأيسر من صفحة "قائمة مكونات الصنف" لعرض "موافقة".</span><span class="sxs-lookup"><span data-stu-id="eb489-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="eb489-170">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="eb489-170">Click OK.</span></span>
24. <span data-ttu-id="eb489-171">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="eb489-171">Click Activate.</span></span>
25. <span data-ttu-id="eb489-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="eb489-172">Close the page.</span></span>
26. <span data-ttu-id="eb489-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="eb489-173">Close the page.</span></span>
27. <span data-ttu-id="eb489-174">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="eb489-174">Close the page.</span></span>

