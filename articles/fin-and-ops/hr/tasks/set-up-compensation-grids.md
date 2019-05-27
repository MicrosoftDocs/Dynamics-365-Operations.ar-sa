---
title: إعداد شبكات التعويض
description: تُستخدم شبكات التعويض لتحديد بنيات الدفع المحافظة عليها لخطط التعويض الثابتة.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0caebb2dfbff12545610aa6438dccbec84db3f9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509718"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="3dca4-103">إعداد شبكات التعويض</span><span class="sxs-lookup"><span data-stu-id="3dca4-103">Set up compensation grids</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3dca4-104">تُستخدم شبكات التعويض لتحديد بنيات الدفع المحافظة عليها لخطط التعويض الثابتة.</span><span class="sxs-lookup"><span data-stu-id="3dca4-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="3dca4-105">يمكن مشاركة شبكات تعويض بين خطط متعددة أو منسوخة عند إنشاء خطة تعويض جديدة.</span><span class="sxs-lookup"><span data-stu-id="3dca4-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="3dca4-106">قبل إنشاء شبكة تعويض، يجب إعداد المستويات والنقاط المرجعية.</span><span class="sxs-lookup"><span data-stu-id="3dca4-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="3dca4-107">سينشئ هذا المثال نوعًا جديدًا للدرجة خاص بشبكة التعويض باستخدام بيانات العرض التوضيحي للمستويات والنقاط المرجعية.</span><span class="sxs-lookup"><span data-stu-id="3dca4-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="3dca4-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="3dca4-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="3dca4-109">إعداد معلومات عن شبكة التعويض</span><span class="sxs-lookup"><span data-stu-id="3dca4-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="3dca4-110">انتقل إلى الموارد البشرية > التعويض > التعويض الثابت > شبكات التعويض.</span><span class="sxs-lookup"><span data-stu-id="3dca4-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="3dca4-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3dca4-111">Click New.</span></span>
3. <span data-ttu-id="3dca4-112">في الحقل "الشبكة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3dca4-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="3dca4-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3dca4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3dca4-114">في الحقل "النوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="3dca4-115">في الحقل "إعداد مرجع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="3dca4-116">في الحقل "العملة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="3dca4-117">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3dca4-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="3dca4-118">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="3dca4-119">إضافة مستويات لبنية التعويض</span><span class="sxs-lookup"><span data-stu-id="3dca4-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="3dca4-120">انقر فوق "بنية التعويض".</span><span class="sxs-lookup"><span data-stu-id="3dca4-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="3dca4-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3dca4-122">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="3dca4-123">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-123">Click New.</span></span>
5. <span data-ttu-id="3dca4-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="3dca4-125">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="3dca4-126">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-126">Click New.</span></span>
8. <span data-ttu-id="3dca4-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3dca4-128">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="3dca4-129">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-129">Click New.</span></span>
11. <span data-ttu-id="3dca4-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="3dca4-131">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="3dca4-132">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-132">Click New.</span></span>
14. <span data-ttu-id="3dca4-133">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="3dca4-134">في الحقل "المستوى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="3dca4-135">تعبئة بنية التعويض بالقيم</span><span class="sxs-lookup"><span data-stu-id="3dca4-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="3dca4-136">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3dca4-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3dca4-137">عند هذه النقطة، يمكن إدخال قيم التعويض يدوياً في كل حقل في الجدول، أو يمكن استخدام وظيفة التغيير الجماعي لملء حقول متعددة وتنفيذ العمليات الحسابية الأساسية بسهولة.</span><span class="sxs-lookup"><span data-stu-id="3dca4-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="3dca4-138">انقر فوق "تغيير شامل".</span><span class="sxs-lookup"><span data-stu-id="3dca4-138">Click Mass change.</span></span>
    * <span data-ttu-id="3dca4-139">بالنسبة لهذه الشبكة، سنقوم أولاً بتطبيق قيمة نقطة الوسط في المستوى الأول على جميع الحقول الموجودة في الجدول.</span><span class="sxs-lookup"><span data-stu-id="3dca4-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="3dca4-140">سيكون هذا هو أساس مصفوفة التعويض.</span><span class="sxs-lookup"><span data-stu-id="3dca4-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="3dca4-141">في الحقل "نوع التعديل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="3dca4-142">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="3dca4-143">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="3dca4-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="3dca4-144">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="3dca4-145">والآن سنستخدم وظيفة التغيير الجماعي لزيادة المبالغ الموجودة في كل مستوى لاحق بنسبة مئوية أو مبلغ معين.</span><span class="sxs-lookup"><span data-stu-id="3dca4-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="3dca4-146">في هذا المثال، سيكون لكل درجة حيزًا مقداره 12.5% بين نقاط الوسط الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="3dca4-147">في الحقل "نوع التعديل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="3dca4-148">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="3dca4-149">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="3dca4-150">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="3dca4-151">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="3dca4-152">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="3dca4-153">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="3dca4-154">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="3dca4-155">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="3dca4-156">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="3dca4-157">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="3dca4-158">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="3dca4-159">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="3dca4-160">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="3dca4-161">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3dca4-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="3dca4-162">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="3dca4-163">والآن سنستخدم وظيفة التغيير الجماعي لضبط الحدين الأدنى والحد الأقصى للنقاط المرجعية لكل مستوى.</span><span class="sxs-lookup"><span data-stu-id="3dca4-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="3dca4-164">سيستخدم هذا المثال حيزًا قدره 50% بحيث يتم تعديل الحد الأدنى للنقطة المرجعية- وهي 20% ويتم تعديل الحد الأقصى وهو+20%.</span><span class="sxs-lookup"><span data-stu-id="3dca4-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="3dca4-165">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="3dca4-166">في الحقل "النقطة المرجعية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="3dca4-167">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="3dca4-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="3dca4-168">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="3dca4-169">في حقل "مبلغ التسوية‬"‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3dca4-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="3dca4-170">في الحقل "النقطة المرجعية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3dca4-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="3dca4-171">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="3dca4-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="3dca4-172">انقر فوق "تطبيق على الشبكة".</span><span class="sxs-lookup"><span data-stu-id="3dca4-172">Click Apply to grid.</span></span>

