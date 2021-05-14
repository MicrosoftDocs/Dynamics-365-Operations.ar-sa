---
title: إنشاء خطة مادية للمنتجات المساعدة
description: يعمل مخطط الإنتاج على التخطيط للمتطلبات المادية للأصناف التي تعتبر منتجات مساعدة للمعادلة.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920719"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="44d8d-103">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="44d8d-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44d8d-104">يعمل مخطط الإنتاج على التخطيط للمتطلبات المادية للأصناف التي تعتبر منتجات مساعدة للمعادلة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="44d8d-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USP2.</span><span class="sxs-lookup"><span data-stu-id="44d8d-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="44d8d-106">إنشاء متطلبات منتج مساعد</span><span class="sxs-lookup"><span data-stu-id="44d8d-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="44d8d-107">انتقل إلى **المبيعات والتسويق \> مساحات العمل \> معالجة أوامر المبيعات والاستعلام عنها**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="44d8d-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-108">Select **New**.</span></span>
1. <span data-ttu-id="44d8d-109">حدد **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="44d8d-110">في الحقل **حساب العميل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="44d8d-111">على سبيل المثال: US-001</span><span class="sxs-lookup"><span data-stu-id="44d8d-111">Example: US-001</span></span>  
1. <span data-ttu-id="44d8d-112">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-112">Select **OK**.</span></span>
1. <span data-ttu-id="44d8d-113">في حقل **رقم الصنف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="44d8d-114">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="44d8d-114">Example: P6003</span></span>  
1. <span data-ttu-id="44d8d-115">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="44d8d-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="44d8d-116">على سبيل المثال: 50000</span><span class="sxs-lookup"><span data-stu-id="44d8d-116">Example: 50000</span></span>  
1. <span data-ttu-id="44d8d-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="44d8d-118">إنشاء خطة مادية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="44d8d-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="44d8d-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-119">Close the page.</span></span>
1. <span data-ttu-id="44d8d-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-120">Close the page.</span></span>
1. <span data-ttu-id="44d8d-121">حدد **التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="44d8d-122">في الحقل **الخطة**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="44d8d-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="44d8d-123">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="44d8d-124">على سبيل المثال: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="44d8d-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="44d8d-125">حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-125">Select **Run**.</span></span>
1. <span data-ttu-id="44d8d-126">قم بتوسيع قسم **السجلات المطلوب تضمينها** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="44d8d-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="44d8d-127">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-127">Select **Filter**.</span></span>
1. <span data-ttu-id="44d8d-128">في القائمة، حدد الصف لـ **الحقل** = *رقم الصنف*.</span><span class="sxs-lookup"><span data-stu-id="44d8d-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="44d8d-129">في الحقل **المعايير**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="44d8d-130">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="44d8d-130">Example: P6003</span></span>  
1. <span data-ttu-id="44d8d-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-131">Select **OK**.</span></span>
1. <span data-ttu-id="44d8d-132">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-132">Select **OK**.</span></span>
1. <span data-ttu-id="44d8d-133">حدد **الأوامر المخططة‬**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="44d8d-134">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="44d8d-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="44d8d-135">على سبيل المثال، قم بإجراء التصفية في حقل **رقم الصنف** باستخدام القيمة "P6000".</span><span class="sxs-lookup"><span data-stu-id="44d8d-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="44d8d-136">قم بإجراء التصفية حسب بند المعادلة الذي لديه منتج مساعد للصنف الذي أنشأت أمر المبيعات له.</span><span class="sxs-lookup"><span data-stu-id="44d8d-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="44d8d-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="44d8d-138">حدد أي واحد من الصفوف التي أرجعها عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="44d8d-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="44d8d-139">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="44d8d-140">قم بتوسيع قسم  **تثبيت السعر**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="44d8d-141">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="44d8d-142">يتم تثبيت الأمر المخطط لأمر المبيعات الخاص بالمنتج المساعد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="44d8d-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="44d8d-144">إنشاء متطلبات ثاني لمنتج مساعد</span><span class="sxs-lookup"><span data-stu-id="44d8d-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="44d8d-145">انتقل إلى **المبيعات والتسويق \> مساحات العمل \> معالجة أوامر المبيعات والاستعلام عنها**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="44d8d-146">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-146">Select **New**.</span></span>
1. <span data-ttu-id="44d8d-147">حدد **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="44d8d-148">في الحقل **حساب العميل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="44d8d-149">على سبيل المثال: US-001</span><span class="sxs-lookup"><span data-stu-id="44d8d-149">Example: US-001</span></span>  
1. <span data-ttu-id="44d8d-150">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-150">Select **OK**.</span></span>
1. <span data-ttu-id="44d8d-151">في حقل **رقم الصنف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="44d8d-152">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="44d8d-152">Example: P6003</span></span>  
1. <span data-ttu-id="44d8d-153">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="44d8d-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="44d8d-154">على سبيل المثال: 50000</span><span class="sxs-lookup"><span data-stu-id="44d8d-154">Example: 50000</span></span>  
1. <span data-ttu-id="44d8d-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="44d8d-156">إنشاء خطة مادية ثانية للمنتجات المساعدة</span><span class="sxs-lookup"><span data-stu-id="44d8d-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="44d8d-157">في الحقل **الخطة**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="44d8d-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="44d8d-158">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="44d8d-159">على سبيل المثال: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="44d8d-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="44d8d-160">حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-160">Select **Run**.</span></span>
4. <span data-ttu-id="44d8d-161">قم بتوسيع قسم **السجلات المطلوب تضمينها** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="44d8d-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="44d8d-162">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-162">Select **Filter**.</span></span>
6. <span data-ttu-id="44d8d-163">في القائمة، حدد الصف لـ **الحقل** = *رقم الصنف*.</span><span class="sxs-lookup"><span data-stu-id="44d8d-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="44d8d-164">في الحقل *المعايير*، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="44d8d-165">على سبيل المثال: P6003</span><span class="sxs-lookup"><span data-stu-id="44d8d-165">Example: P6003</span></span>  
8. <span data-ttu-id="44d8d-166">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-166">Select **OK**.</span></span>
9. <span data-ttu-id="44d8d-167">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-167">Select **OK**.</span></span>
10. <span data-ttu-id="44d8d-168">حدد **الأوامر المخططة‬**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="44d8d-169">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="44d8d-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="44d8d-170">على سبيل المثال، قم بإجراء التصفية في حقل **رقم الصنف** باستخدام القيمة "P6000".</span><span class="sxs-lookup"><span data-stu-id="44d8d-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="44d8d-171">قم بإجراء التصفية حسب بند المعادلة الذي لديه منتج مساعد للصنف الذي أنشأت أمر المبيعات له.</span><span class="sxs-lookup"><span data-stu-id="44d8d-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="44d8d-172">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="44d8d-173">حدد أي واحد من الصفوف التي أرجعها عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="44d8d-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="44d8d-174">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="44d8d-175">قم بتوسيع قسم **تثبيت السعر** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="44d8d-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="44d8d-176">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="44d8d-177">يتم تثبيت الأمر المخطط لأمر المبيعات الخاص بالمنتج المساعد.</span><span class="sxs-lookup"><span data-stu-id="44d8d-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="44d8d-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-178">Close the page.</span></span>
17. <span data-ttu-id="44d8d-179">حدد **التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="44d8d-180">انتقل إلى **التخطيط الرئيسي \> إعداد \> محددات التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="44d8d-181">حدد *لا* في حقل **تعطيل كل عمليات التخطيط**.</span><span class="sxs-lookup"><span data-stu-id="44d8d-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="44d8d-182">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="44d8d-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]