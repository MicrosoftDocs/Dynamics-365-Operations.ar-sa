--- 
title: "إعداد التعبئة في حاويات"
description: "يصف هذا الإجراء كيفية جعل تعبئة الأحمال في إدارة المستودع عملية تلقائية."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="bc266-103">إعداد التعبئة في حاويات</span><span class="sxs-lookup"><span data-stu-id="bc266-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc266-104">يصف هذا الإجراء كيفية جعل تعبئة الأحمال في إدارة المستودع عملية تلقائية.</span><span class="sxs-lookup"><span data-stu-id="bc266-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="bc266-105">تعمل التعبئة التلقائية في الحاويات على إنشاء الحاويات وانتقاء العمل للشحن عند معالجة موجة ويمكن تقسيم بنود العمل إلى الكميات التي تناسب الحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="bc266-106">يساعد ذلك العاملين في المستودع على انتقاء الأصناف مباشرة في الحاوية المختارة.</span><span class="sxs-lookup"><span data-stu-id="bc266-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="bc266-107">مقارنة بعملية التعبئة اليدوية، تتم أتمتة المهام مثل إنشاء حاويات وتعيين الأصناف وإغلاق الحاويات بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="bc266-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="bc266-108">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF ويتم التنفيذ من قبل مدير المستودع.</span><span class="sxs-lookup"><span data-stu-id="bc266-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="bc266-109">إعداد قالب موجة</span><span class="sxs-lookup"><span data-stu-id="bc266-109">Set up a wave template</span></span>
1. <span data-ttu-id="bc266-110">انتقل إلى إدارة المستودعات > إعداد > الموجات > قوالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="bc266-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="bc266-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-111">Click New.</span></span>
3. <span data-ttu-id="bc266-112">في الحقل "اسم قالب الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="bc266-113">في الحقل "وصف قالب الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="bc266-114">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="bc266-115">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="bc266-116">قم بتوسيع قسم "الأساليب".</span><span class="sxs-lookup"><span data-stu-id="bc266-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="bc266-117">يسرد جزء الأساليب المحددة أساليب لنوع قالب الموجة المحدد.</span><span class="sxs-lookup"><span data-stu-id="bc266-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="bc266-118">يجب أن يتضمن قالب الموجة أسلوب التعبئة في الحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="bc266-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bc266-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="bc266-120">في حقل "كود خطوة الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="bc266-121">أدخل كود خطوة الموجة للأسلوب المضاف، الذي يمكن يكون أي كود.</span><span class="sxs-lookup"><span data-stu-id="bc266-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="bc266-122">من الممكن إضافة الأسلوب أكثر من مرة وتعيين أكواد خطوة موجة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="bc266-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="bc266-123">للقيام بذلك، حدد "قابل للتكرار" لهذا الأسلوب في صفحة أساليب معالجة الموجة.</span><span class="sxs-lookup"><span data-stu-id="bc266-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="bc266-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bc266-124">Click Save.</span></span>
11. <span data-ttu-id="bc266-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc266-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="bc266-126">إعداد نوع حاوية</span><span class="sxs-lookup"><span data-stu-id="bc266-126">Set up a container type</span></span>
1. <span data-ttu-id="bc266-127">انتقل إلى إدارة المستودعات > إعداد > الحاويات > أنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="bc266-128">يمكنك تحديد الحاويات الخاصة بك في صفحة أنواع الحاوية.</span><span class="sxs-lookup"><span data-stu-id="bc266-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="bc266-129">يمكنك تكوين الأبعاد الفعلية للحاويات، بما في ذلك وزن الفارغ والحد الأقصى للوزن والحد الأقصى للحجم والطول والعرض والارتفاع.</span><span class="sxs-lookup"><span data-stu-id="bc266-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="bc266-130">في هذا المثال، لدينا ثلاثة أحجام مختلفة من الصناديق.</span><span class="sxs-lookup"><span data-stu-id="bc266-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="bc266-131">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-131">Click New.</span></span>
3. <span data-ttu-id="bc266-132">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="bc266-133">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="bc266-134">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="bc266-135">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="bc266-136">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="bc266-137">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="bc266-138">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="bc266-139">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="bc266-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bc266-140">Click Save.</span></span>
12. <span data-ttu-id="bc266-141">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-141">Click New.</span></span>
13. <span data-ttu-id="bc266-142">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="bc266-143">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="bc266-144">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="bc266-145">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="bc266-146">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="bc266-147">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="bc266-148">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="bc266-149">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="bc266-150">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bc266-150">Click Save.</span></span>
22. <span data-ttu-id="bc266-151">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-151">Click New.</span></span>
23. <span data-ttu-id="bc266-152">في حقل "كود نوع الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="bc266-153">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="bc266-154">في الحقل "وزن الفارغ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="bc266-155">في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="bc266-156">في الحقل "الحجم‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="bc266-157">في الحقل "الطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="bc266-158">في الحقل "العرض"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="bc266-159">في الحقل "الارتفاع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="bc266-160">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bc266-160">Click Save.</span></span>
32. <span data-ttu-id="bc266-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc266-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="bc266-162">إعداد مجموعة حاويات</span><span class="sxs-lookup"><span data-stu-id="bc266-162">Set up a container group</span></span>
1. <span data-ttu-id="bc266-163">انتقل إلى إدارة المستودعات > إعداد > الحاويات > مجموعات الحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="bc266-164">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-164">Click New.</span></span>
    * <span data-ttu-id="bc266-165">يمكنك إعداد مجموعات منطقية من أنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="bc266-166">لكل مجموعة، يمكنك تحديد التسلسل لحزم الحاويات به والنسبة المئوية لتعبئة الحاويات. تستخدم أبعاد حجم الصنف لتحديد ما إذا كانت مناسبة للحاوية أم لا.</span><span class="sxs-lookup"><span data-stu-id="bc266-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="bc266-167">يتم استخدام الحاوية الأقرب إلى أبعاد حجم الصنف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="bc266-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="bc266-168">إذا كان لديك أنواع متعددة من الحاويات في مجموعة، نوصي بترتيب التسلسل حسب الحجم، حيث تكون الحاوية الأكبر أولاً، أي رقم 1 في التسلسل والحاوية الأصغر تكون الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="bc266-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="bc266-169">في الحقل "معرف مجموعة الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="bc266-170">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bc266-171">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="bc266-171">Click New.</span></span>
6. <span data-ttu-id="bc266-172">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bc266-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="bc266-173">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="bc266-174">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="bc266-174">Click New.</span></span>
9. <span data-ttu-id="bc266-175">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bc266-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="bc266-176">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="bc266-177">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="bc266-177">Click New.</span></span>
12. <span data-ttu-id="bc266-178">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bc266-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bc266-179">في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="bc266-180">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bc266-180">Click Save.</span></span>
15. <span data-ttu-id="bc266-181">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc266-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="bc266-182">إعداد قالب إنشاء الحاوية</span><span class="sxs-lookup"><span data-stu-id="bc266-182">Set up a container build template</span></span>
1. <span data-ttu-id="bc266-183">انتقل إلى إدارة المستودعات > إعداد > الحاويات > قوالب إنشاء الحاوية‬.</span><span class="sxs-lookup"><span data-stu-id="bc266-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="bc266-184">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-184">Click New.</span></span>
    * <span data-ttu-id="bc266-185">يعتمد قالب بناء الحاوية على عمليات التعبئة في الحاويات التي يتم إجراؤها.</span><span class="sxs-lookup"><span data-stu-id="bc266-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="bc266-186">يعرف قالب بناء كل حاوية عملية النقل بالحاويات التي سيتم استخدامها بواسطة قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="bc266-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="bc266-187">يسمح لك خيار تحرير الاستعلام بتحديد الشروط التي ستتم معالجة القالب المحدد بموجبها.</span><span class="sxs-lookup"><span data-stu-id="bc266-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="bc266-188">على سبيل المثال، قد تريد تشغيل النقل بالحاويات فقط لعملاء معينين أو المنتجات أو المستودعات أو يمكنك إضافة نطاقي استعلام مقابلين إلى القالب.</span><span class="sxs-lookup"><span data-stu-id="bc266-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="bc266-189">ويحدد حقل كود خطوة الموجة كيفية ارتباط قالب بناء حاوية بالخطوات في قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="bc266-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="bc266-190">عند تنفيذ موجة، فإنه يحدد أي قالب (قوالب) بناء الحاويات يتم استخدامه لبدء النقل بالحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="bc266-191">يحدد الحقل "نوع الاستعلام الأساسي" ما يتم حزمه وما الذي يستند إليه استعلام عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="bc266-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="bc266-192">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bc266-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bc266-193">في الحقل "معرف قالب الحاوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="bc266-194">في الحقل "معرف مجموعة الحاوية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="bc266-195">في حقل "كود خطوة الموجة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bc266-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="bc266-196">حدد خانة الاختيار "السماح بتقسيم الانتقاءات".</span><span class="sxs-lookup"><span data-stu-id="bc266-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="bc266-197">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bc266-197">Click Save.</span></span>
9. <span data-ttu-id="bc266-198">انقر فوق قيود خلط الحاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="bc266-199">تسمح لك فواصل منطق الخلط بإعداد قواعد لتعبئة بنود التوزيع في حاويات.</span><span class="sxs-lookup"><span data-stu-id="bc266-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="bc266-200">على سبيل المثال، إذا قمت بإضافة حقل رقم الصنف، عندما يتم تعيين الأصناف إلى الحاويات، فإنه سيتم إنشاء حاوية جديدة عند وجود رقم صنف جديد.</span><span class="sxs-lookup"><span data-stu-id="bc266-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="bc266-201">وهذا سيمنع العمال من تعبئة بنود التوزيعات لعميلين مختلفين في الحاوية نفسها.</span><span class="sxs-lookup"><span data-stu-id="bc266-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="bc266-202">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bc266-202">Click New.</span></span>
11. <span data-ttu-id="bc266-203">في الحقل "جدول"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="bc266-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="bc266-204">في حقل "تحديد الحقل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc266-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="bc266-205">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bc266-205">Click OK.</span></span>


