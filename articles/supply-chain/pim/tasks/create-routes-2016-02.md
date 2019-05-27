---
title: إنشاء المسارات (فبراير 2016)
description: تركز هذه المهمة على إنشاء مسارات الإنتاج لمنتج نهائي ومنتج غير نهائي.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567808"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="35941-103">إنشاء المسارات (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="35941-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35941-104">تركز هذه المهمة على إنشاء مسارات الإنتاج لمنتج نهائي ومنتج غير نهائي.</span><span class="sxs-lookup"><span data-stu-id="35941-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="35941-105">إنها المهمة الخامسة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="35941-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="35941-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="35941-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="35941-107">إنشاء مسار لمنتج غير نهائي</span><span class="sxs-lookup"><span data-stu-id="35941-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="35941-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="35941-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="35941-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="35941-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="35941-110">حدد رقم الصنف BOM_2.</span><span class="sxs-lookup"><span data-stu-id="35941-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="35941-111">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="35941-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="35941-112">انقر فوق "المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-112">Click Route.</span></span>
5. <span data-ttu-id="35941-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="35941-113">Click New.</span></span>
6. <span data-ttu-id="35941-114">انقر فوق "مسار" و"إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-114">Click Route and route version.</span></span>
7. <span data-ttu-id="35941-115">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="35941-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="35941-116">على سبيل المثال، اكتب ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="35941-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="35941-117">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-118">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="35941-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="35941-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="35941-119">Click OK.</span></span>
10. <span data-ttu-id="35941-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="35941-120">Click New.</span></span>
11. <span data-ttu-id="35941-121">في الحقل "العملية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-122">بالنسبة إلى هذا المثال، حدد "التجميع‬".</span><span class="sxs-lookup"><span data-stu-id="35941-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="35941-123">في الحقل "وقت التشغيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="35941-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="35941-124">على سبيل المثال، اكتب "1".</span><span class="sxs-lookup"><span data-stu-id="35941-124">For example, type 1.</span></span> <span data-ttu-id="35941-125">تشكّل أوقات التشغيل في أغلب الأحيان جزءًا من السعر المحسوب لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="35941-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="35941-126">في الحقل "مجموعة المسارات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-127">بالنسبة إلى هذا المثال، حدد "قياسي".</span><span class="sxs-lookup"><span data-stu-id="35941-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="35941-128">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="35941-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="35941-129">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-130">بالنسبة إلى هذا المثال، حدد "التجميع‬".</span><span class="sxs-lookup"><span data-stu-id="35941-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="35941-131">انقر فوق علامة التبويب "الأوقات".</span><span class="sxs-lookup"><span data-stu-id="35941-131">Click the Times tab.</span></span>
17. <span data-ttu-id="35941-132">في الحقل "وقت الإعداد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="35941-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="35941-133">بالنسبة إلى هذا المثال، اكتب 1.</span><span class="sxs-lookup"><span data-stu-id="35941-133">For this example, type 1.</span></span> <span data-ttu-id="35941-134">تشكّل أوقات الإعداد في أغلب الأحيان جزءًا من السعر المحسوب لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="35941-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="35941-135">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="35941-136">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="35941-136">Click Approve.</span></span>
20. <span data-ttu-id="35941-137">حدد "نعم" في الحقل "هل تريد أيضًا الموافقة على المسار؟ .</span><span class="sxs-lookup"><span data-stu-id="35941-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="35941-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="35941-138">Click OK.</span></span>
22. <span data-ttu-id="35941-139">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="35941-140">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="35941-140">Click Activate.</span></span>
24. <span data-ttu-id="35941-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35941-141">Close the page.</span></span>
25. <span data-ttu-id="35941-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35941-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="35941-143">إنشاء مسار لمنتج نهائي</span><span class="sxs-lookup"><span data-stu-id="35941-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="35941-144">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="35941-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="35941-145">حدد رقم الصنف BOM_1.</span><span class="sxs-lookup"><span data-stu-id="35941-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="35941-146">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="35941-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="35941-147">انقر فوق "المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-147">Click Route.</span></span>
4. <span data-ttu-id="35941-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="35941-148">Click New.</span></span>
5. <span data-ttu-id="35941-149">انقر فوق "مسار" و"إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-149">Click Route and route version.</span></span>
6. <span data-ttu-id="35941-150">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="35941-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="35941-151">بالنسبة إلى هذا المثال، اكتب ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="35941-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="35941-152">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-153">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="35941-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="35941-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="35941-154">Click OK.</span></span>
9. <span data-ttu-id="35941-155">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="35941-155">Click New.</span></span>
10. <span data-ttu-id="35941-156">في الحقل "العملية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-157">بالنسبة إلى هذا المثال، حدد "التعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="35941-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="35941-158">في الحقل "وقت التشغيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="35941-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="35941-159">بالنسبة إلى هذا المثال، اكتب 1.</span><span class="sxs-lookup"><span data-stu-id="35941-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="35941-160">في الحقل "مجموعة المسارات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-161">بالنسبة إلى هذا المثال، حدد "قياسي".</span><span class="sxs-lookup"><span data-stu-id="35941-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="35941-162">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="35941-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="35941-163">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="35941-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="35941-164">بالنسبة إلى هذا المثال، حدد "التعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="35941-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="35941-165">انقر فوق علامة التبويب "الأوقات".</span><span class="sxs-lookup"><span data-stu-id="35941-165">Click the Times tab.</span></span>
16. <span data-ttu-id="35941-166">في الحقل "وقت الإعداد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="35941-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="35941-167">بالنسبة إلى هذا المثال، اكتب 1.</span><span class="sxs-lookup"><span data-stu-id="35941-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="35941-168">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="35941-169">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="35941-169">Click Approve.</span></span>
19. <span data-ttu-id="35941-170">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="35941-170">Click OK.</span></span>
20. <span data-ttu-id="35941-171">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="35941-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="35941-172">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="35941-172">Click Activate.</span></span>
22. <span data-ttu-id="35941-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35941-173">Close the page.</span></span>
23. <span data-ttu-id="35941-174">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35941-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="35941-175">تمكين الاستهلاك التلقائي لوقت الإعداد</span><span class="sxs-lookup"><span data-stu-id="35941-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="35941-176">انتقل إلى التحكم بالإنتاج > الإعداد > المسارات > مجموعات المسارات‬.</span><span class="sxs-lookup"><span data-stu-id="35941-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="35941-177">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="35941-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="35941-178">حدد "قياسي" من القائمة.</span><span class="sxs-lookup"><span data-stu-id="35941-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="35941-179">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="35941-179">Click Edit.</span></span>
4. <span data-ttu-id="35941-180">حدد "نعم" في الحقل "وقت الإعداد".</span><span class="sxs-lookup"><span data-stu-id="35941-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="35941-181">تشكّل أوقات الإعداد في أغلب الأحيان جزءًا من السعر المحسوب لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="35941-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="35941-182">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="35941-182">Click Save.</span></span>
6. <span data-ttu-id="35941-183">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35941-183">Close the page.</span></span>

