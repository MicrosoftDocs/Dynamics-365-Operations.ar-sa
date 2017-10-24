--- 
title: " تحديد برامج الولاء"
description: "يوضح هذا الإجراء كيفية إعداد برنامج ولاء بطبقتين ولاء."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a949d5cb4f01518b46bc4b1769de34196109050
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-programs"></a><span data-ttu-id="f4ddd-103"> تحديد برامج الولاء</span><span class="sxs-lookup"><span data-stu-id="f4ddd-103">Define loyalty programs</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f4ddd-104">يوضح هذا الإجراء كيفية إعداد برنامج ولاء بطبقتين ولاء.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="f4ddd-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="f4ddd-106">انتقل إلى البيع بالتجزئة والتجارة > ..</span><span class="sxs-lookup"><span data-stu-id="f4ddd-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="f4ddd-107">> برامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="f4ddd-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-108">Click New.</span></span>
3. <span data-ttu-id="f4ddd-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f4ddd-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f4ddd-111">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-111">Click Add line.</span></span>
6. <span data-ttu-id="f4ddd-112">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="f4ddd-113">في حقل "الطبقة‬"، أدخل اسمًا لطبقة الولاء.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="f4ddd-114">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f4ddd-115">في حقل "‏‫فترة التاريخ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4ddd-116">ينبغي أن تمتد ‏‫فترة التاريخ هذه في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-116">This date interval should extend into the future.</span></span> <span data-ttu-id="f4ddd-117">على سبيل المثال، إذا كانت فترة التاريخ المحددة للطبقة الذهبية مدتها سنة واحدة، فيمكن لأي عميل مؤهل للطبقة الذهبية تلقي المكافآت التي تم تعيينها إلى الطبقة الذهبية لمدة سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="f4ddd-118">وإذا أعاد العميل تأهله للطبقة الذهبية أثناء وجوده في هذه الطبقة، يتم تمديد التاريخ الذي تنتهي فيه صلاحية الطبقة بسنة أخرى من تاريخ إعادة تأهله.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="f4ddd-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f4ddd-120">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-120">Click Add line.</span></span>
12. <span data-ttu-id="f4ddd-121">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="f4ddd-122">في حقل "الطبقة‬"، أدخل اسمًا لطبقة الولاء.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="f4ddd-123">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="f4ddd-124">في حقل "‏‫فترة التاريخ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f4ddd-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f4ddd-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-126">Click Save.</span></span>
18. <span data-ttu-id="f4ddd-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f4ddd-128">تحدد قواعد الطبقة الحد الأدنى لعدد نقاط المكافأة المطلوب اكتسابها خلال فترة زمنية للتأهل لهذه الطبقة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="f4ddd-129">قم بتبديل توسيع الجزء "قواعد الطبقات".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="f4ddd-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-130">Click New.</span></span>
    * <span data-ttu-id="f4ddd-131">يمكنك تحديد أكثر من قاعدة طبقة واحدة لكل طبقة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="f4ddd-132">على سبيل المثال، يمكن أن يكون لديك ثلاثة معايير مختلفة لاكتساب طبقة؛ من خلال إنفاق 500 دولار أمريكي في شهر واحد، وإنفاق 1000 دولار أمريكي خلال سنة واحدة، وبوجود 20 حركة في سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="f4ddd-133">وللقيام بذلك، ستحتاج إلى إنشاء ثلاثة قواعد طبقات.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="f4ddd-134">في حقل "‏‫نقطة المكافأة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4ddd-135">ينبغي أن يكون هذا نقطة مكافأة ولاء غير قابلة للاسترداد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="f4ddd-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="f4ddd-137">في حقل "‏‫الحد الأدنى للنقاط التي تم إصدارها"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="f4ddd-138">بالنسبة لأدنى مستوى من الطبقات، إذا كان العملاء مؤهلين ببساطة من خلال المشاركة في البرنامج، فأدخل "0".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="f4ddd-139">في حقل "‏‫‏‫فترة تاريخ التقييم‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4ddd-140">ينبغي أن تمتد ‏‫فترة التاريخ هذه في الماضي.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-140">This date interval should extend into the past.</span></span> <span data-ttu-id="f4ddd-141">ولن يتم احتساب نقاط إلا المكتسبة خلال هذه الفترة للوصول إلى الحد الأدنى من قيمة النقاط التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="f4ddd-142">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="f4ddd-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-143">Click Save.</span></span>
27. <span data-ttu-id="f4ddd-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="f4ddd-145">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-145">Click New.</span></span>
29. <span data-ttu-id="f4ddd-146">في حقل "‏‫نقطة المكافأة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="f4ddd-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="f4ddd-148">في حقل "‏‫الحد الأدنى للنقاط التي تم إصدارها"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="f4ddd-149">في حقل "‏‫‏‫فترة تاريخ التقييم‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4ddd-150">ينبغي أن تمتد ‏‫فترة التاريخ هذه في الماضي.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="f4ddd-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="f4ddd-152">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-152">Click Save.</span></span>
35. <span data-ttu-id="f4ddd-153">انقر فوق "مجموعات الأسعار".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-153">Click Price groups.</span></span>
    * <span data-ttu-id="f4ddd-154">إذا أردت إعطاء خصومات للعملاء ذوي الولاء.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="f4ddd-155">سوف تحتاج إلى تعيين مجموعة أسعار أو أكثر إلى برنامج الولاء وتعيين مجموعات الأسعار إلى الخصومات.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="f4ddd-156">من المستحسن عدم خلط مجموعات الأسعار في أنواع مختلفة من كيانات الخصومات.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-156">It is a best practise to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="f4ddd-157">على سبيل المثال، لا تستخدم نفس مجموعة الأسعار للحصول على خصم الولاء وخصم القناة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="f4ddd-158">في حقل "مجموعة الأسعار"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4ddd-159">يوجد ارتباط مجموعات الأسعار في أعلى الصفحة لبرنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="f4ddd-160">بينما يوجد ارتباط مجموعات الأسعار في علامة التبويب السريعة "طبقات البرنامج" لطبقة ولاء معينة فقط.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="f4ddd-161">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="f4ddd-162">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-162">Click Save.</span></span>
39. <span data-ttu-id="f4ddd-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-163">Close the page.</span></span>
40. <span data-ttu-id="f4ddd-164">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f4ddd-164">Click Save.</span></span>


