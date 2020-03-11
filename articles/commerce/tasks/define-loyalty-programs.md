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
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b178f1c6a71b34b70db4dbcd1765117215a4d2a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021471"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="f8d74-103"> تحديد برامج الولاء</span><span class="sxs-lookup"><span data-stu-id="f8d74-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f8d74-104">يوضح هذا الإجراء كيفية إعداد برنامج ولاء بطبقتين ولاء.</span><span class="sxs-lookup"><span data-stu-id="f8d74-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="f8d74-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="f8d74-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="f8d74-106">انتقل إلى البيع بالتجزئة والتجارة > ..</span><span class="sxs-lookup"><span data-stu-id="f8d74-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="f8d74-107">> برامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="f8d74-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="f8d74-108">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-108">Click New.</span></span>
3. <span data-ttu-id="f8d74-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f8d74-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f8d74-111">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="f8d74-111">Click Add line.</span></span>
6. <span data-ttu-id="f8d74-112">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f8d74-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="f8d74-113">في حقل "الطبقة‬"، أدخل اسمًا لطبقة الولاء.</span><span class="sxs-lookup"><span data-stu-id="f8d74-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="f8d74-114">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f8d74-115">في حقل "‏‫فترة التاريخ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8d74-116">ينبغي أن تمتد ‏‫فترة التاريخ هذه في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="f8d74-116">This date interval should extend into the future.</span></span> <span data-ttu-id="f8d74-117">على سبيل المثال، إذا كانت فترة التاريخ المحددة للطبقة الذهبية مدتها سنة واحدة، فيمكن لأي عميل مؤهل للطبقة الذهبية تلقي المكافآت التي تم تعيينها إلى الطبقة الذهبية لمدة سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="f8d74-118">وإذا أعاد العميل تأهله للطبقة الذهبية أثناء وجوده في هذه الطبقة، يتم تمديد التاريخ الذي تنتهي فيه صلاحية الطبقة بسنة أخرى من تاريخ إعادة تأهله.</span><span class="sxs-lookup"><span data-stu-id="f8d74-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="f8d74-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f8d74-120">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="f8d74-120">Click Add line.</span></span>
12. <span data-ttu-id="f8d74-121">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f8d74-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="f8d74-122">في حقل "الطبقة‬"، أدخل اسمًا لطبقة الولاء.</span><span class="sxs-lookup"><span data-stu-id="f8d74-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="f8d74-123">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="f8d74-124">في حقل "‏‫فترة التاريخ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f8d74-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f8d74-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f8d74-126">Click Save.</span></span>
18. <span data-ttu-id="f8d74-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f8d74-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f8d74-128">تحدد قواعد الطبقة الحد الأدنى لعدد نقاط المكافأة المطلوب اكتسابها خلال فترة زمنية للتأهل لهذه الطبقة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="f8d74-129">قم بتبديل توسيع الجزء "قواعد الطبقات".</span><span class="sxs-lookup"><span data-stu-id="f8d74-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="f8d74-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f8d74-130">Click New.</span></span>
    * <span data-ttu-id="f8d74-131">يمكنك تحديد أكثر من قاعدة طبقة واحدة لكل طبقة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="f8d74-132">على سبيل المثال، يمكن أن يكون لديك ثلاثة معايير مختلفة لاكتساب طبقة؛ من خلال إنفاق 500 دولار أمريكي في شهر واحد، وإنفاق 1000 دولار أمريكي خلال سنة واحدة، وبوجود 20 حركة في سنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="f8d74-133">وللقيام بذلك، ستحتاج إلى إنشاء ثلاثة قواعد طبقات.</span><span class="sxs-lookup"><span data-stu-id="f8d74-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="f8d74-134">في حقل "‏‫نقطة المكافأة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8d74-135">ينبغي أن يكون هذا نقطة مكافأة ولاء غير قابلة للاسترداد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="f8d74-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="f8d74-137">في حقل "‏‫الحد الأدنى للنقاط التي تم إصدارها"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f8d74-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="f8d74-138">بالنسبة لأدنى مستوى من الطبقات، إذا كان العملاء مؤهلين ببساطة من خلال المشاركة في البرنامج، فأدخل "0".</span><span class="sxs-lookup"><span data-stu-id="f8d74-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="f8d74-139">في حقل "‏‫‏‫فترة تاريخ التقييم‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8d74-140">ينبغي أن تمتد ‏‫فترة التاريخ هذه في الماضي.</span><span class="sxs-lookup"><span data-stu-id="f8d74-140">This date interval should extend into the past.</span></span> <span data-ttu-id="f8d74-141">ولن يتم احتساب نقاط إلا المكتسبة خلال هذه الفترة للوصول إلى الحد الأدنى من قيمة النقاط التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="f8d74-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="f8d74-142">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="f8d74-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f8d74-143">Click Save.</span></span>
27. <span data-ttu-id="f8d74-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f8d74-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="f8d74-145">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-145">Click New.</span></span>
29. <span data-ttu-id="f8d74-146">في حقل "‏‫نقطة المكافأة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="f8d74-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="f8d74-148">في حقل "‏‫الحد الأدنى للنقاط التي تم إصدارها"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f8d74-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="f8d74-149">في حقل "‏‫‏‫فترة تاريخ التقييم‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8d74-150">ينبغي أن تمتد ‏‫فترة التاريخ هذه في الماضي.</span><span class="sxs-lookup"><span data-stu-id="f8d74-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="f8d74-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="f8d74-152">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f8d74-152">Click Save.</span></span>
35. <span data-ttu-id="f8d74-153">انقر فوق "مجموعات الأسعار".</span><span class="sxs-lookup"><span data-stu-id="f8d74-153">Click Price groups.</span></span>
    * <span data-ttu-id="f8d74-154">إذا أردت إعطاء خصومات للعملاء ذوي الولاء.</span><span class="sxs-lookup"><span data-stu-id="f8d74-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="f8d74-155">سوف تحتاج إلى تعيين مجموعة أسعار أو أكثر إلى برنامج الولاء وتعيين مجموعات الأسعار إلى الخصومات.</span><span class="sxs-lookup"><span data-stu-id="f8d74-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="f8d74-156">إنها أفضل ممارسة لعدم خلط مجموعات الأسعار في أنواع مختلفة من كيانات الخصومات.</span><span class="sxs-lookup"><span data-stu-id="f8d74-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="f8d74-157">على سبيل المثال، لا تستخدم نفس مجموعة الأسعار للحصول على خصم الولاء وخصم القناة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="f8d74-158">في حقل "مجموعة الأسعار"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f8d74-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f8d74-159">يوجد ارتباط مجموعات الأسعار في أعلى الصفحة لبرنامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="f8d74-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="f8d74-160">بينما يوجد ارتباط مجموعات الأسعار في علامة التبويب السريعة "طبقات البرنامج" لطبقة ولاء معينة فقط.</span><span class="sxs-lookup"><span data-stu-id="f8d74-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="f8d74-161">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f8d74-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="f8d74-162">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f8d74-162">Click Save.</span></span>
39. <span data-ttu-id="f8d74-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f8d74-163">Close the page.</span></span>
40. <span data-ttu-id="f8d74-164">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f8d74-164">Click Save.</span></span>
