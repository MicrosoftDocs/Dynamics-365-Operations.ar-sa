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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844551"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="dce01-103">إنشاء المسارات (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="dce01-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dce01-104">تركز هذه المهمة على إنشاء مسارات الإنتاج لمنتج نهائي ومنتج غير نهائي.</span><span class="sxs-lookup"><span data-stu-id="dce01-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="dce01-105">إنها المهمة الخامسة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="dce01-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="dce01-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="dce01-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="dce01-107">إنشاء مسار لمنتج غير نهائي</span><span class="sxs-lookup"><span data-stu-id="dce01-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="dce01-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="dce01-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="dce01-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dce01-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dce01-110">حدد رقم الصنف BOM_2.</span><span class="sxs-lookup"><span data-stu-id="dce01-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="dce01-111">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="dce01-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="dce01-112">انقر فوق "المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-112">Click Route.</span></span>
5. <span data-ttu-id="dce01-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="dce01-113">Click New.</span></span>
6. <span data-ttu-id="dce01-114">انقر فوق "مسار" و"إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-114">Click Route and route version.</span></span>
7. <span data-ttu-id="dce01-115">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dce01-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dce01-116">على سبيل المثال، اكتب ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="dce01-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="dce01-117">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-118">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="dce01-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="dce01-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dce01-119">Click OK.</span></span>
10. <span data-ttu-id="dce01-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="dce01-120">Click New.</span></span>
11. <span data-ttu-id="dce01-121">في الحقل "العملية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-122">بالنسبة إلى هذا المثال، حدد "التجميع‬".</span><span class="sxs-lookup"><span data-stu-id="dce01-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="dce01-123">في الحقل "وقت التشغيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="dce01-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="dce01-124">على سبيل المثال، اكتب "1".</span><span class="sxs-lookup"><span data-stu-id="dce01-124">For example, type 1.</span></span> <span data-ttu-id="dce01-125">تشكّل أوقات التشغيل في أغلب الأحيان جزءًا من السعر المحسوب لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="dce01-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="dce01-126">في الحقل "مجموعة المسارات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-127">بالنسبة إلى هذا المثال، حدد "قياسي".</span><span class="sxs-lookup"><span data-stu-id="dce01-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="dce01-128">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="dce01-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="dce01-129">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-130">بالنسبة إلى هذا المثال، حدد "التجميع‬".</span><span class="sxs-lookup"><span data-stu-id="dce01-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="dce01-131">انقر فوق علامة التبويب "الأوقات".</span><span class="sxs-lookup"><span data-stu-id="dce01-131">Click the Times tab.</span></span>
17. <span data-ttu-id="dce01-132">في الحقل "وقت الإعداد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="dce01-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="dce01-133">بالنسبة إلى هذا المثال، اكتب 1.</span><span class="sxs-lookup"><span data-stu-id="dce01-133">For this example, type 1.</span></span> <span data-ttu-id="dce01-134">تشكّل أوقات الإعداد في أغلب الأحيان جزءًا من السعر المحسوب لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="dce01-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="dce01-135">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="dce01-136">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="dce01-136">Click Approve.</span></span>
20. <span data-ttu-id="dce01-137">حدد "نعم" في الحقل "هل تريد أيضًا الموافقة على المسار؟ .</span><span class="sxs-lookup"><span data-stu-id="dce01-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="dce01-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dce01-138">Click OK.</span></span>
22. <span data-ttu-id="dce01-139">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="dce01-140">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="dce01-140">Click Activate.</span></span>
24. <span data-ttu-id="dce01-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dce01-141">Close the page.</span></span>
25. <span data-ttu-id="dce01-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dce01-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="dce01-143">إنشاء مسار لمنتج نهائي</span><span class="sxs-lookup"><span data-stu-id="dce01-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="dce01-144">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dce01-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dce01-145">حدد رقم الصنف BOM_1.</span><span class="sxs-lookup"><span data-stu-id="dce01-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="dce01-146">في جزء الإجراءات، انقر فوق "المهندس".</span><span class="sxs-lookup"><span data-stu-id="dce01-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="dce01-147">انقر فوق "المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-147">Click Route.</span></span>
4. <span data-ttu-id="dce01-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="dce01-148">Click New.</span></span>
5. <span data-ttu-id="dce01-149">انقر فوق "مسار" و"إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-149">Click Route and route version.</span></span>
6. <span data-ttu-id="dce01-150">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dce01-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dce01-151">بالنسبة إلى هذا المثال، اكتب ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="dce01-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="dce01-152">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-153">بالنسبة إلى هذا المثال، أدخل أو حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="dce01-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="dce01-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dce01-154">Click OK.</span></span>
9. <span data-ttu-id="dce01-155">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="dce01-155">Click New.</span></span>
10. <span data-ttu-id="dce01-156">في الحقل "العملية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-157">بالنسبة إلى هذا المثال، حدد "التعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="dce01-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="dce01-158">في الحقل "وقت التشغيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="dce01-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="dce01-159">بالنسبة إلى هذا المثال، اكتب 1.</span><span class="sxs-lookup"><span data-stu-id="dce01-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="dce01-160">في الحقل "مجموعة المسارات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-161">بالنسبة إلى هذا المثال، حدد "قياسي".</span><span class="sxs-lookup"><span data-stu-id="dce01-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="dce01-162">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="dce01-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="dce01-163">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dce01-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="dce01-164">بالنسبة إلى هذا المثال، حدد "التعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="dce01-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="dce01-165">انقر فوق علامة التبويب "الأوقات".</span><span class="sxs-lookup"><span data-stu-id="dce01-165">Click the Times tab.</span></span>
16. <span data-ttu-id="dce01-166">في الحقل "وقت الإعداد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="dce01-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="dce01-167">بالنسبة إلى هذا المثال، اكتب 1.</span><span class="sxs-lookup"><span data-stu-id="dce01-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="dce01-168">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="dce01-169">انقر فوق "‏‫موافقة".</span><span class="sxs-lookup"><span data-stu-id="dce01-169">Click Approve.</span></span>
19. <span data-ttu-id="dce01-170">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dce01-170">Click OK.</span></span>
20. <span data-ttu-id="dce01-171">في جزء "الإجراءات"، انقر فوق "إصدار المسار".</span><span class="sxs-lookup"><span data-stu-id="dce01-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="dce01-172">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="dce01-172">Click Activate.</span></span>
22. <span data-ttu-id="dce01-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dce01-173">Close the page.</span></span>
23. <span data-ttu-id="dce01-174">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dce01-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="dce01-175">تمكين الاستهلاك التلقائي لوقت الإعداد</span><span class="sxs-lookup"><span data-stu-id="dce01-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="dce01-176">انتقل إلى التحكم بالإنتاج > الإعداد > المسارات > مجموعات المسارات‬.</span><span class="sxs-lookup"><span data-stu-id="dce01-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="dce01-177">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="dce01-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dce01-178">حدد "قياسي" من القائمة.</span><span class="sxs-lookup"><span data-stu-id="dce01-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="dce01-179">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="dce01-179">Click Edit.</span></span>
4. <span data-ttu-id="dce01-180">حدد "نعم" في الحقل "وقت الإعداد".</span><span class="sxs-lookup"><span data-stu-id="dce01-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="dce01-181">تشكّل أوقات الإعداد في أغلب الأحيان جزءًا من السعر المحسوب لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="dce01-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="dce01-182">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="dce01-182">Click Save.</span></span>
6. <span data-ttu-id="dce01-183">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dce01-183">Close the page.</span></span>

