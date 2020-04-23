---
title: إنشاء خطة مادية للمنتجات المساعدة
description: يعمل مخطط الإنتاج على التخطيط للمتطلبات المادية للأصناف التي تعتبر منتجات مساعدة للمعادلة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209664"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="30c63-103">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="30c63-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30c63-104">يعمل مخطط الإنتاج على التخطيط للمتطلبات المادية للأصناف التي تعتبر منتجات مساعدة للمعادلة.</span><span class="sxs-lookup"><span data-stu-id="30c63-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="30c63-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USP2.</span><span class="sxs-lookup"><span data-stu-id="30c63-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="30c63-106">إنشاء متطلبات منتج مساعد</span><span class="sxs-lookup"><span data-stu-id="30c63-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="30c63-107">انتقل إلى لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="30c63-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="30c63-108">انقر فوق "الاستعلام عن أمر المبيعات ومعالجته‬".</span><span class="sxs-lookup"><span data-stu-id="30c63-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="30c63-109">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="30c63-109">Click New.</span></span>
4. <span data-ttu-id="30c63-110">انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="30c63-110">Click Sales order.</span></span>
5. <span data-ttu-id="30c63-111">في الحقل "حساب العميل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30c63-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="30c63-112">على سبيل المثال: US-001</span><span class="sxs-lookup"><span data-stu-id="30c63-112">Example: US-001</span></span>  
6. <span data-ttu-id="30c63-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30c63-113">Click OK.</span></span>
7. <span data-ttu-id="30c63-114">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30c63-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="30c63-115">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="30c63-115">Example: P6003</span></span>  
8. <span data-ttu-id="30c63-116">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="30c63-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="30c63-117">على سبيل المثال: 50000</span><span class="sxs-lookup"><span data-stu-id="30c63-117">Example: 50000</span></span>  
9. <span data-ttu-id="30c63-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="30c63-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="30c63-119">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="30c63-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="30c63-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30c63-120">Close the page.</span></span>
2. <span data-ttu-id="30c63-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30c63-121">Close the page.</span></span>
3. <span data-ttu-id="30c63-122">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="30c63-122">Click Master planning.</span></span>
4. <span data-ttu-id="30c63-123">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="30c63-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="30c63-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30c63-125">على سبيل المثال: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="30c63-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="30c63-126">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="30c63-126">Click Run.</span></span>
7. <span data-ttu-id="30c63-127">قم بتوسيع المقطع "السجلات المطلوب تضمينها‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="30c63-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="30c63-128">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="30c63-128">Click Filter.</span></span>
9. <span data-ttu-id="30c63-129">في القائمة، حدد الصف للحقل = رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="30c63-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="30c63-130">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30c63-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="30c63-131">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="30c63-131">Example: P6003</span></span>  
11. <span data-ttu-id="30c63-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30c63-132">Click OK.</span></span>
12. <span data-ttu-id="30c63-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30c63-133">Click OK.</span></span>
13. <span data-ttu-id="30c63-134">انقر فوق "الأوامر المخططة".</span><span class="sxs-lookup"><span data-stu-id="30c63-134">Click Planned orders.</span></span>
14. <span data-ttu-id="30c63-135">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="30c63-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="30c63-136">على سبيل المثال، قم بإجراء التصفية على الحقل "رقم الصنف" باستخدام القيمة "P6000".</span><span class="sxs-lookup"><span data-stu-id="30c63-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="30c63-137">قم بإجراء التصفية حسب بند المعادلة الذي لديه منتج مساعد للصنف الذي أنشأت أمر المبيعات له.</span><span class="sxs-lookup"><span data-stu-id="30c63-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="30c63-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="30c63-139">حدد أي واحد من الصفوف التي أرجعها عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="30c63-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="30c63-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="30c63-141">قم بتوسيع المقطع "تثبيت السعر" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="30c63-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="30c63-142">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30c63-143">يتم تثبيت الأمر المخطط لأمر المبيعات الخاص بالمنتج المساعد.</span><span class="sxs-lookup"><span data-stu-id="30c63-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="30c63-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30c63-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="30c63-145">إنشاء متطلبات منتج مساعد</span><span class="sxs-lookup"><span data-stu-id="30c63-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="30c63-146">انتقل إلى لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="30c63-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="30c63-147">انقر فوق "الاستعلام عن أمر المبيعات ومعالجته‬".</span><span class="sxs-lookup"><span data-stu-id="30c63-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="30c63-148">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="30c63-148">Click New.</span></span>
4. <span data-ttu-id="30c63-149">انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="30c63-149">Click Sales order.</span></span>
5. <span data-ttu-id="30c63-150">في الحقل "حساب العميل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30c63-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="30c63-151">على سبيل المثال: US-001</span><span class="sxs-lookup"><span data-stu-id="30c63-151">Example: US-001</span></span>  
6. <span data-ttu-id="30c63-152">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30c63-152">Click OK.</span></span>
7. <span data-ttu-id="30c63-153">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30c63-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="30c63-154">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="30c63-154">Example: P6003</span></span>  
8. <span data-ttu-id="30c63-155">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="30c63-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="30c63-156">على سبيل المثال: 50000</span><span class="sxs-lookup"><span data-stu-id="30c63-156">Example: 50000</span></span>  
9. <span data-ttu-id="30c63-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="30c63-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="30c63-158">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="30c63-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="30c63-159">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="30c63-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="30c63-160">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30c63-161">على سبيل المثال: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="30c63-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="30c63-162">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="30c63-162">Click Run.</span></span>
4. <span data-ttu-id="30c63-163">قم بتوسيع المقطع "السجلات المطلوب تضمينها‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="30c63-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="30c63-164">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="30c63-164">Click Filter.</span></span>
6. <span data-ttu-id="30c63-165">في القائمة، حدد الصف للحقل = رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="30c63-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="30c63-166">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30c63-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="30c63-167">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="30c63-167">Example: P6003</span></span>  
8. <span data-ttu-id="30c63-168">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30c63-168">Click OK.</span></span>
9. <span data-ttu-id="30c63-169">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30c63-169">Click OK.</span></span>
10. <span data-ttu-id="30c63-170">انقر فوق "الأوامر المخططة".</span><span class="sxs-lookup"><span data-stu-id="30c63-170">Click Planned orders.</span></span>
11. <span data-ttu-id="30c63-171">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="30c63-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="30c63-172">على سبيل المثال، قم بإجراء التصفية على الحقل "رقم الصنف" باستخدام القيمة "P6000".</span><span class="sxs-lookup"><span data-stu-id="30c63-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="30c63-173">قم بإجراء التصفية حسب بند المعادلة الذي لديه منتج مساعد للصنف الذي أنشأت أمر المبيعات له.</span><span class="sxs-lookup"><span data-stu-id="30c63-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="30c63-174">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="30c63-175">حدد أي واحد من الصفوف التي أرجعها عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="30c63-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="30c63-176">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="30c63-177">قم بتوسيع المقطع "تثبيت السعر" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="30c63-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="30c63-178">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="30c63-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30c63-179">يتم تثبيت الأمر المخطط لأمر المبيعات الخاص بالمنتج المساعد.</span><span class="sxs-lookup"><span data-stu-id="30c63-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="30c63-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30c63-180">Close the page.</span></span>
17. <span data-ttu-id="30c63-181">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="30c63-181">Click Master planning.</span></span>
18. <span data-ttu-id="30c63-182">انتقل إلى التخطيط الرئيسي > إعداد > مُحددات التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="30c63-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="30c63-183">حدد لا في حقل تعطيل كافة عمليات التخطيط.</span><span class="sxs-lookup"><span data-stu-id="30c63-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="30c63-184">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30c63-184">Close the page.</span></span>

