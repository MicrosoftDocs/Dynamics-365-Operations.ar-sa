--- 
title: "إعداد شبكات التعويض"
description: "تُستخدم شبكات التعويض لتحديد بنيات الدفع المحافظة عليها لخطط التعويض الثابتة."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d507224004bdf319f9bf13ba07ed07ef29cc85dc
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="08794-103">إعداد شبكات التعويض</span><span class="sxs-lookup"><span data-stu-id="08794-103">Set up compensation grids</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08794-104">تُستخدم شبكات التعويض لتحديد بنيات الدفع المحافظة عليها لخطط التعويض الثابتة.</span><span class="sxs-lookup"><span data-stu-id="08794-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="08794-105">يمكن مشاركة شبكات تعويض بين خطط متعددة أو منسوخة عند إنشاء خطة تعويض جديدة.</span><span class="sxs-lookup"><span data-stu-id="08794-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="08794-106">قبل إنشاء شبكة تعويض، يجب إعداد المستويات والنقاط المرجعية.</span><span class="sxs-lookup"><span data-stu-id="08794-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="08794-107">سينشئ هذا المثال نوعًا جديدًا للدرجة خاص بشبكة التعويض باستخدام بيانات العرض التوضيحي للمستويات والنقاط المرجعية.</span><span class="sxs-lookup"><span data-stu-id="08794-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="08794-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="08794-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="08794-109">إعداد معلومات عن شبكة التعويض</span><span class="sxs-lookup"><span data-stu-id="08794-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="08794-110">انتقل إلى الموارد البشرية > التعويض > التعويض الثابت > شبكات التعويض.</span><span class="sxs-lookup"><span data-stu-id="08794-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="08794-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="08794-111">Click New.</span></span>
3. <span data-ttu-id="08794-112">في الحقل "الشبكة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08794-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="08794-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08794-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="08794-114">في الحقل "النوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="08794-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="08794-115">في الحقل "إعداد مرجع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="08794-116">في الحقل "العملة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="08794-117">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08794-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="08794-118">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="08794-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="08794-119">إضافة مستويات لبنية التعويض</span><span class="sxs-lookup"><span data-stu-id="08794-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="08794-120">انقر فوق "بنية التعويض".</span><span class="sxs-lookup"><span data-stu-id="08794-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="08794-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="08794-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="08794-122">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="08794-123">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="08794-123">Click New.</span></span>
5. <span data-ttu-id="08794-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="08794-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="08794-125">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="08794-126">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="08794-126">Click New.</span></span>
8. <span data-ttu-id="08794-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="08794-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="08794-128">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="08794-129">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="08794-129">Click New.</span></span>
11. <span data-ttu-id="08794-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="08794-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="08794-131">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="08794-132">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="08794-132">Click New.</span></span>
14. <span data-ttu-id="08794-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="08794-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="08794-134">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="08794-135">تعبئة بنية التعويض بالقيم</span><span class="sxs-lookup"><span data-stu-id="08794-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="08794-136">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="08794-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="08794-137">عند هذه النقطة، يمكن إدخال قيم التعويض يدوياً في كل حقل في الجدول، أو يمكن استخدام وظيفة التغيير الجماعي لملء حقول متعددة وتنفيذ العمليات الحسابية الأساسية بسهولة.</span><span class="sxs-lookup"><span data-stu-id="08794-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="08794-138">انقر فوق "تغيير شامل".</span><span class="sxs-lookup"><span data-stu-id="08794-138">Click Mass change.</span></span>
    * <span data-ttu-id="08794-139">بالنسبة لهذه الشبكة، سنقوم أولاً بتطبيق قيمة نقطة الوسط في المستوى الأول على جميع الحقول الموجودة في الجدول.</span><span class="sxs-lookup"><span data-stu-id="08794-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="08794-140">سيكون هذا هو أساس مصفوفة التعويض.</span><span class="sxs-lookup"><span data-stu-id="08794-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="08794-141">في الحقل "نوع التعديل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="08794-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="08794-142">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="08794-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="08794-143">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="08794-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="08794-144">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="08794-145">والآن سنستخدم وظيفة التغيير الجماعي لزيادة المبالغ الموجودة في كل مستوى لاحق بنسبة مئوية أو مبلغ معين.</span><span class="sxs-lookup"><span data-stu-id="08794-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="08794-146">في هذا المثال، سيكون لكل درجة حيزًا مقداره 12.5% بين نقاط الوسط الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="08794-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="08794-147">في الحقل "نوع التعديل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="08794-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="08794-148">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="08794-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="08794-149">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="08794-150">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="08794-151">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="08794-152">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="08794-153">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="08794-154">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="08794-155">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="08794-156">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="08794-157">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="08794-158">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="08794-159">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="08794-160">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="08794-161">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="08794-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="08794-162">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="08794-163">والآن سنستخدم وظيفة التغيير الجماعي لضبط الحدين الأدنى والحد الأقصى للنقاط المرجعية لكل مستوى.</span><span class="sxs-lookup"><span data-stu-id="08794-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="08794-164">سيستخدم هذا المثال حيزًا قدره 50% بحيث يتم تعديل الحد الأدنى للنقطة المرجعية- وهي 20% ويتم تعديل الحد الأقصى وهو+20%.</span><span class="sxs-lookup"><span data-stu-id="08794-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="08794-165">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="08794-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="08794-166">في الحقل "النقطة المرجعية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="08794-167">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="08794-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="08794-168">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="08794-169">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="08794-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="08794-170">في الحقل "النقطة المرجعية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="08794-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="08794-171">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="08794-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="08794-172">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="08794-172">Click Apply to grid.</span></span>


