--- 
title: "تحديد ‬‏‫عملية الجرد الدوري الجزئي للمواقع‫ "
description: "عندما تستخدم خطط الجرد الدوري لإنشاء عمل الجرد، يمكنك إرشاد عمليات الجرد الفعلية عن طريق طلب إجراء عمليات جرد لمنتجات ومتغيرات منتجات معينة فقط بدلاً من جر كل المخزون الفعلي في الموقع."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 030f0f75d64c97f1109f36c9fd38283c2d1fa7b0
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="f7810-103">تحديد ‬‏‫عملية الجرد الدوري الجزئي للمواقع‫ </span><span class="sxs-lookup"><span data-stu-id="f7810-103">Define partial location cycle counting process</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7810-104">عندما تستخدم خطط الجرد الدوري لإنشاء عمل الجرد، يمكنك إرشاد عمليات الجرد الفعلية عن طريق طلب إجراء عمليات جرد لمنتجات ومتغيرات منتجات معينة فقط بدلاً من جر كل المخزون الفعلي في الموقع.</span><span class="sxs-lookup"><span data-stu-id="f7810-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="f7810-105">من خلال تصفية منتجات معينة، يستطيع مدير المستودع تقليل مصروفات المراجعة والمساعدة في أخطاء الدمج وتوفير الوقت.</span><span class="sxs-lookup"><span data-stu-id="f7810-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="f7810-106">يقوم مدير المستودع عادةً بتنفيذ مهام الإعداد هذه.</span><span class="sxs-lookup"><span data-stu-id="f7810-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="f7810-107">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في بياناتك.</span><span class="sxs-lookup"><span data-stu-id="f7810-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="f7810-108">إنشاء قالب عمل جرد دوري</span><span class="sxs-lookup"><span data-stu-id="f7810-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="f7810-109">انتقل إلى إدارة المستودعات > إعداد > العمل > قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="f7810-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="f7810-110">في الحقل "نوع أمر العمل‬"، حدد "جرد دوري".</span><span class="sxs-lookup"><span data-stu-id="f7810-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="f7810-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7810-111">Click New.</span></span>
4. <span data-ttu-id="f7810-112">في الحقل "الرقم التسلسلي"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f7810-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f7810-113">ترتيب الفرز هو من أصغر رقم إلى أكبر رقم.</span><span class="sxs-lookup"><span data-stu-id="f7810-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="f7810-114">يجب أن تكون القيمة أكبر من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="f7810-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="f7810-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f7810-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f7810-116">في الحقل "قالب العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7810-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="f7810-117">في الحقل "وصف قالب العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7810-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="f7810-118">في الحقل "معرف وعاء العمل‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f7810-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="f7810-119">في حقل "أولوية العمل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f7810-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="f7810-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f7810-120">Click Save.</span></span>
11. <span data-ttu-id="f7810-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7810-121">Click New.</span></span>
12. <span data-ttu-id="f7810-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f7810-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f7810-123">في الحقل "نوع العمل"، حدد "الجرد".</span><span class="sxs-lookup"><span data-stu-id="f7810-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="f7810-124">في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f7810-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="f7810-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f7810-125">Click Save.</span></span>
16. <span data-ttu-id="f7810-126">انقر فوق "فواصل بنود العمل".</span><span class="sxs-lookup"><span data-stu-id="f7810-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="f7810-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7810-127">Click New.</span></span>
18. <span data-ttu-id="f7810-128">في الحقل "الرقم التسلسلي"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f7810-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f7810-129">ترتيب الفرز هو من أصغر رقم إلى أكبر رقم.</span><span class="sxs-lookup"><span data-stu-id="f7810-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="f7810-130">يجب أن تكون القيمة أكبر من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="f7810-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="f7810-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f7810-131">Click Save.</span></span>
20. <span data-ttu-id="f7810-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f7810-132">Close the page.</span></span>
21. <span data-ttu-id="f7810-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f7810-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="f7810-134">إنشاء خطة جرد دوري</span><span class="sxs-lookup"><span data-stu-id="f7810-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="f7810-135">انتقل إلى إدارة المستودعات > إعداد > الجرد الدوري > خطط الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="f7810-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="f7810-136">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7810-136">Click New.</span></span>
3. <span data-ttu-id="f7810-137">في الحقل "معرف خطة الجرد الدوري"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7810-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="f7810-138">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7810-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7810-139">في الحقل "الحد الأقصى لعدد عمليات الجرد الدوري"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f7810-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="f7810-140">في الحقل "قالب العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f7810-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="f7810-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7810-141">Click New.</span></span>
8. <span data-ttu-id="f7810-142">في الحقل "الرقم التسلسلي"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f7810-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f7810-143">ترتيب الفرز هو من أصغر رقم إلى أكبر رقم.</span><span class="sxs-lookup"><span data-stu-id="f7810-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="f7810-144">يجب أن تكون القيمة أكبر من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="f7810-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="f7810-145">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7810-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f7810-146">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f7810-146">Click Save.</span></span>
11. <span data-ttu-id="f7810-147">انقر فوق "تحديد استعلام المنتج".</span><span class="sxs-lookup"><span data-stu-id="f7810-147">Click Define product query.</span></span>
12. <span data-ttu-id="f7810-148">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f7810-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f7810-149">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f7810-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="f7810-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f7810-150">Click OK.</span></span>
15. <span data-ttu-id="f7810-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f7810-151">Close the page.</span></span>


