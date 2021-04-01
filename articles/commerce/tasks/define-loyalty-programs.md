---
title: " تحديد برامج الولاء"
description: يوضح هذا الإجراء كيفية إعداد برنامج ولاء بطبقتين ولاء.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69424cdaae84ffe5ca8157f061ba5876b9eeeff9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256891"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="e66b1-103"> تحديد برامج الولاء</span><span class="sxs-lookup"><span data-stu-id="e66b1-103">Define loyalty programs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e66b1-104">يوضح هذا الإجراء كيفية إعداد برنامج ولاء بطبقتين ولاء.</span><span class="sxs-lookup"><span data-stu-id="e66b1-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="e66b1-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="e66b1-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="e66b1-106">انتقل إلى البيع بالتجزئة والتجارة > ..</span><span class="sxs-lookup"><span data-stu-id="e66b1-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="e66b1-107">> برامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="e66b1-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="e66b1-108">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-108">Click New.</span></span>
3. <span data-ttu-id="e66b1-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e66b1-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e66b1-111">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="e66b1-111">Click Add line.</span></span>
6. <span data-ttu-id="e66b1-112">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e66b1-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="e66b1-113">في حقل "الطبقة‬"، أدخل اسمًا لطبقة الولاء.</span><span class="sxs-lookup"><span data-stu-id="e66b1-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="e66b1-114">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="e66b1-115">في حقل "‏‫فترة التاريخ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e66b1-116">ينبغي أن تمتد ‏‫فترة التاريخ هذه في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="e66b1-116">This date interval should extend into the future.</span></span> <span data-ttu-id="e66b1-117">على سبيل المثال، إذا كانت فترة التاريخ المحددة للطبقة الذهبية مدتها سنة واحدة، فيمكن لأي عميل مؤهل للطبقة الذهبية تلقي المكافآت التي تم تعيينها إلى الطبقة الذهبية لمدة سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="e66b1-118">وإذا أعاد العميل تأهله للطبقة الذهبية أثناء وجوده في هذه الطبقة، يتم تمديد التاريخ الذي تنتهي فيه صلاحية الطبقة بسنة أخرى من تاريخ إعادة تأهله.</span><span class="sxs-lookup"><span data-stu-id="e66b1-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="e66b1-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e66b1-120">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="e66b1-120">Click Add line.</span></span>
12. <span data-ttu-id="e66b1-121">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e66b1-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="e66b1-122">في حقل "الطبقة‬"، أدخل اسمًا لطبقة الولاء.</span><span class="sxs-lookup"><span data-stu-id="e66b1-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="e66b1-123">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="e66b1-124">في حقل "‏‫فترة التاريخ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e66b1-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e66b1-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e66b1-126">Click Save.</span></span>
18. <span data-ttu-id="e66b1-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e66b1-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e66b1-128">تحدد قواعد الطبقة الحد الأدنى لعدد نقاط المكافأة المطلوب اكتسابها خلال فترة زمنية للتأهل لهذه الطبقة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="e66b1-129">قم بتبديل توسيع الجزء "قواعد الطبقات".</span><span class="sxs-lookup"><span data-stu-id="e66b1-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="e66b1-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e66b1-130">Click New.</span></span>
    * <span data-ttu-id="e66b1-131">يمكنك تحديد أكثر من قاعدة طبقة واحدة لكل طبقة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="e66b1-132">على سبيل المثال، يمكن أن يكون لديك ثلاثة معايير مختلفة لاكتساب طبقة؛ من خلال إنفاق 500 دولار أمريكي في شهر واحد، وإنفاق 1000 دولار أمريكي خلال سنة واحدة، وبوجود 20 حركة في سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="e66b1-133">وللقيام بذلك، ستحتاج إلى إنشاء ثلاثة قواعد طبقات.</span><span class="sxs-lookup"><span data-stu-id="e66b1-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="e66b1-134">في حقل "‏‫نقطة المكافأة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e66b1-135">ينبغي أن يكون هذا نقطة مكافأة ولاء غير قابلة للاسترداد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="e66b1-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="e66b1-137">في حقل "‏‫الحد الأدنى للنقاط التي تم إصدارها"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e66b1-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="e66b1-138">بالنسبة لأدنى مستوى من الطبقات، إذا كان العملاء مؤهلين ببساطة من خلال المشاركة في البرنامج، فأدخل "0".</span><span class="sxs-lookup"><span data-stu-id="e66b1-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="e66b1-139">في حقل "‏‫‏‫فترة تاريخ التقييم‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e66b1-140">ينبغي أن تمتد ‏‫فترة التاريخ هذه في الماضي.</span><span class="sxs-lookup"><span data-stu-id="e66b1-140">This date interval should extend into the past.</span></span> <span data-ttu-id="e66b1-141">ولن يتم احتساب نقاط إلا المكتسبة خلال هذه الفترة للوصول إلى الحد الأدنى من قيمة النقاط التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="e66b1-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="e66b1-142">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="e66b1-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e66b1-143">Click Save.</span></span>
27. <span data-ttu-id="e66b1-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e66b1-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="e66b1-145">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-145">Click New.</span></span>
29. <span data-ttu-id="e66b1-146">في حقل "‏‫نقطة المكافأة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="e66b1-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="e66b1-148">في حقل "‏‫الحد الأدنى للنقاط التي تم إصدارها"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e66b1-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="e66b1-149">في حقل "‏‫‏‫فترة تاريخ التقييم‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e66b1-150">ينبغي أن تمتد ‏‫فترة التاريخ هذه في الماضي.</span><span class="sxs-lookup"><span data-stu-id="e66b1-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="e66b1-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="e66b1-152">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e66b1-152">Click Save.</span></span>
35. <span data-ttu-id="e66b1-153">انقر فوق "مجموعات الأسعار".</span><span class="sxs-lookup"><span data-stu-id="e66b1-153">Click Price groups.</span></span>
    * <span data-ttu-id="e66b1-154">إذا أردت إعطاء خصومات للعملاء ذوي الولاء.</span><span class="sxs-lookup"><span data-stu-id="e66b1-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="e66b1-155">سوف تحتاج إلى تعيين مجموعة أسعار أو أكثر إلى برنامج الولاء وتعيين مجموعات الأسعار إلى الخصومات.</span><span class="sxs-lookup"><span data-stu-id="e66b1-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="e66b1-156">إنها أفضل ممارسة لعدم خلط مجموعات الأسعار في أنواع مختلفة من كيانات الخصومات.</span><span class="sxs-lookup"><span data-stu-id="e66b1-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="e66b1-157">على سبيل المثال، لا تستخدم نفس مجموعة الأسعار للحصول على خصم الولاء وخصم القناة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="e66b1-158">في حقل "مجموعة الأسعار"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e66b1-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e66b1-159">يوجد ارتباط مجموعات الأسعار في أعلى الصفحة لبرنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="e66b1-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="e66b1-160">بينما يوجد ارتباط مجموعات الأسعار في علامة التبويب السريعة "طبقات البرنامج" لطبقة ولاء معينة فقط.</span><span class="sxs-lookup"><span data-stu-id="e66b1-160">The Price groups link in the Program tiers FastTab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="e66b1-161">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66b1-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="e66b1-162">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e66b1-162">Click Save.</span></span>
39. <span data-ttu-id="e66b1-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e66b1-163">Close the page.</span></span>
40. <span data-ttu-id="e66b1-164">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e66b1-164">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]