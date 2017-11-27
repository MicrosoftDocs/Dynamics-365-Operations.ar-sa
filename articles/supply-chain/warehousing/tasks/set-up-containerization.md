--- 
title: "إعداد التعبئة في حاويات"
description: "يصف هذا الإجراء كيفية جعل تعبئة الأحمال في إدارة المستودع عملية تلقائية."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: c5faf926071dec5d2ddc1c9e921a98ecd0754917
ms.contentlocale: ar-sa
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="029e2-103">إعداد التعبئة في حاويات</span><span class="sxs-lookup"><span data-stu-id="029e2-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="029e2-104">يصف هذا الإجراء كيفية جعل تعبئة الأحمال في إدارة المستودع عملية تلقائية.</span><span class="sxs-lookup"><span data-stu-id="029e2-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="029e2-105">تعمل التعبئة التلقائية في الحاويات على إنشاء الحاويات وانتقاء العمل للشحن عند معالجة موجة ويمكن تقسيم بنود العمل إلى الكميات التي تناسب الحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="029e2-106">يساعد ذلك العاملين في المستودع على انتقاء الأصناف مباشرة في الحاوية المختارة.</span><span class="sxs-lookup"><span data-stu-id="029e2-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="029e2-107">مقارنة بعملية التعبئة اليدوية، تتم أتمتة المهام مثل إنشاء حاويات وتعيين الأصناف وإغلاق الحاويات بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="029e2-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="029e2-108">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF ويتم التنفيذ من قبل مدير المستودع.</span><span class="sxs-lookup"><span data-stu-id="029e2-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="029e2-109">إعداد قالب موجة</span><span class="sxs-lookup"><span data-stu-id="029e2-109">Set up a wave template</span></span>
1. <span data-ttu-id="029e2-110">انتقل إلى إدارة المستودعات > إعداد > الموجات > قوالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="029e2-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="029e2-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-111">Click New.</span></span>
3. <span data-ttu-id="029e2-112">في الحقل "اسم قالب الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="029e2-113">في الحقل "وصف قالب الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="029e2-114">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="029e2-115">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="029e2-116">قم بتوسيع قسم "الأساليب".</span><span class="sxs-lookup"><span data-stu-id="029e2-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="029e2-117">يسرد جزء الأساليب المحددة أساليب لنوع قالب الموجة المحدد.</span><span class="sxs-lookup"><span data-stu-id="029e2-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="029e2-118">يجب أن يتضمن قالب الموجة أسلوب التعبئة في الحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="029e2-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="029e2-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="029e2-120">في حقل "كود خطوة الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="029e2-121">أدخل كود خطوة الموجة للأسلوب المضاف، الذي يمكن يكون أي كود.</span><span class="sxs-lookup"><span data-stu-id="029e2-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="029e2-122">من الممكن إضافة الأسلوب أكثر من مرة وتعيين أكواد خطوة موجة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="029e2-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="029e2-123">للقيام بذلك، حدد "قابل للتكرار" لهذا الأسلوب في صفحة أساليب معالجة الموجة.</span><span class="sxs-lookup"><span data-stu-id="029e2-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="029e2-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="029e2-124">Click Save.</span></span>
11. <span data-ttu-id="029e2-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="029e2-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="029e2-126">إعداد نوع حاوية</span><span class="sxs-lookup"><span data-stu-id="029e2-126">Set up a container type</span></span>
1. <span data-ttu-id="029e2-127">انتقل إلى إدارة المستودعات > إعداد > الحاويات > أنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="029e2-128">يمكنك تحديد الحاويات الخاصة بك في صفحة أنواع الحاوية.</span><span class="sxs-lookup"><span data-stu-id="029e2-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="029e2-129">يمكنك تكوين الأبعاد الفعلية للحاويات، بما في ذلك وزن الفارغ والحد الأقصى للوزن والحد الأقصى للحجم والطول والعرض والارتفاع.</span><span class="sxs-lookup"><span data-stu-id="029e2-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="029e2-130">في هذا المثال، لدينا ثلاثة أحجام مختلفة من الصناديق.</span><span class="sxs-lookup"><span data-stu-id="029e2-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="029e2-131">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-131">Click New.</span></span>
3. <span data-ttu-id="029e2-132">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="029e2-133">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="029e2-134">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="029e2-135">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="029e2-136">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="029e2-137">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="029e2-138">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="029e2-139">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="029e2-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="029e2-140">Click Save.</span></span>
12. <span data-ttu-id="029e2-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-141">Click New.</span></span>
13. <span data-ttu-id="029e2-142">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="029e2-143">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="029e2-144">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="029e2-145">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="029e2-146">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="029e2-147">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="029e2-148">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="029e2-149">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="029e2-150">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="029e2-150">Click Save.</span></span>
22. <span data-ttu-id="029e2-151">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-151">Click New.</span></span>
23. <span data-ttu-id="029e2-152">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="029e2-153">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="029e2-154">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="029e2-155">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="029e2-156">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="029e2-157">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="029e2-158">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="029e2-159">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="029e2-160">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="029e2-160">Click Save.</span></span>
32. <span data-ttu-id="029e2-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="029e2-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="029e2-162">إعداد مجموعة حاويات</span><span class="sxs-lookup"><span data-stu-id="029e2-162">Set up a container group</span></span>
1. <span data-ttu-id="029e2-163">انتقل إلى إدارة المستودعات > إعداد > الحاويات > مجموعات الحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="029e2-164">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-164">Click New.</span></span>
    * <span data-ttu-id="029e2-165">يمكنك إعداد مجموعات منطقية من أنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="029e2-166">لكل مجموعة، يمكنك تحديد التسلسل الذي يتم حزم الحاويات فيه، والنسبة المئوية للحاويات المراد تعبئتها.</span><span class="sxs-lookup"><span data-stu-id="029e2-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="029e2-167">تُستخدم أبعاد حجم الصنف لتحديد ما إذا كان سيتم احتواؤه في حاوية أم لا.</span><span class="sxs-lookup"><span data-stu-id="029e2-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="029e2-168">يتم استخدام الحاوية الأقرب إلى أبعاد حجم الصنف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="029e2-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="029e2-169">إذا كان لديك أنواع متعددة من الحاويات في مجموعة، نوصي بترتيب التسلسل حسب الحجم، حيث تكون الحاوية الأكبر أولاً، أي رقم 1 في التسلسل والحاوية الأصغر تكون الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="029e2-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="029e2-170">في الحقل "معرف مجموعة الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="029e2-171">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="029e2-172">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="029e2-172">Click New.</span></span>
6. <span data-ttu-id="029e2-173">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="029e2-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="029e2-174">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="029e2-175">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="029e2-175">Click New.</span></span>
9. <span data-ttu-id="029e2-176">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="029e2-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="029e2-177">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="029e2-178">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="029e2-178">Click New.</span></span>
12. <span data-ttu-id="029e2-179">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="029e2-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="029e2-180">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="029e2-181">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="029e2-181">Click Save.</span></span>
15. <span data-ttu-id="029e2-182">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="029e2-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="029e2-183">إعداد قالب إنشاء الحاوية</span><span class="sxs-lookup"><span data-stu-id="029e2-183">Set up a container build template</span></span>
1. <span data-ttu-id="029e2-184">انتقل إلى إدارة المستودعات > إعداد > الحاويات > قوالب إنشاء الحاوية‬.</span><span class="sxs-lookup"><span data-stu-id="029e2-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="029e2-185">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-185">Click New.</span></span>
    * <span data-ttu-id="029e2-186">يعتمد قالب بناء الحاوية على عمليات التعبئة في الحاويات التي يتم إجراؤها.</span><span class="sxs-lookup"><span data-stu-id="029e2-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="029e2-187">يعرف قالب بناء كل حاوية عملية النقل بالحاويات التي سيتم استخدامها بواسطة قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="029e2-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="029e2-188">يسمح لك خيار تحرير الاستعلام بتحديد الشروط التي ستتم معالجة القالب المحدد بموجبها.</span><span class="sxs-lookup"><span data-stu-id="029e2-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="029e2-189">على سبيل المثال، قد تريد تشغيل النقل بالحاويات فقط لعملاء معينين أو المنتجات أو المستودعات أو يمكنك إضافة نطاقي استعلام مقابلين إلى القالب.</span><span class="sxs-lookup"><span data-stu-id="029e2-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="029e2-190">ويحدد حقل كود خطوة الموجة كيفية ارتباط قالب بناء حاوية بالخطوات في قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="029e2-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="029e2-191">عند تنفيذ موجة، فإنه يحدد أي قالب (قوالب) بناء الحاويات يتم استخدامه لبدء النقل بالحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="029e2-192">يحدد الحقل "نوع الاستعلام الأساسي" ما يتم حزمه وما الذي يستند إليه استعلام عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="029e2-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="029e2-193">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="029e2-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="029e2-194">في الحقل "معرف قالب الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="029e2-195">في الحقل "معرف مجموعة الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="029e2-196">في حقل "كود خطوة الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="029e2-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="029e2-197">حدد خانة الاختيار "السماح بتقسيم الانتقاءات".</span><span class="sxs-lookup"><span data-stu-id="029e2-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="029e2-198">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="029e2-198">Click Save.</span></span>
9. <span data-ttu-id="029e2-199">انقر فوق قيود خلط الحاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="029e2-200">تسمح لك فواصل منطق الخلط بإعداد قواعد لتعبئة بنود التوزيع في حاويات.</span><span class="sxs-lookup"><span data-stu-id="029e2-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="029e2-201">على سبيل المثال، إذا قمت بإضافة حقل رقم الصنف، عندما يتم تعيين الأصناف إلى الحاويات، فإنه سيتم إنشاء حاوية جديدة عند وجود رقم صنف جديد.</span><span class="sxs-lookup"><span data-stu-id="029e2-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="029e2-202">وهذا سيمنع العمال من تعبئة بنود التوزيعات لعميلين مختلفين في الحاوية نفسها.</span><span class="sxs-lookup"><span data-stu-id="029e2-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="029e2-203">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="029e2-203">Click New.</span></span>
11. <span data-ttu-id="029e2-204">في الحقل "جدول"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="029e2-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="029e2-205">في حقل "تحديد الحقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="029e2-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="029e2-206">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="029e2-206">Click OK.</span></span>


