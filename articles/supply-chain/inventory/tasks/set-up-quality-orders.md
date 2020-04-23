---
title: إعداد أوامر الجودة
description: يوضح هذا الإجراء كيفية تمكين عملية إدارة الجدة حيث يجب فحص المخزون الواردة مباشرة بعد تسجيل الوصول.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 679448255bd85aafb07270f4858d4b83d2fe643b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204023"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="11170-103">إعداد أوامر الجودة</span><span class="sxs-lookup"><span data-stu-id="11170-103">Set up quality orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11170-104">يوضح هذا الإجراء كيفية تمكين عملية إدارة الجدة حيث يجب فحص المخزون الواردة مباشرة بعد تسجيل الوصول.</span><span class="sxs-lookup"><span data-stu-id="11170-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="11170-105">سيتم عادة تنفيذ الإجراء من قبل مدير الجودة.</span><span class="sxs-lookup"><span data-stu-id="11170-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="11170-106">تتضمن العملية عادةً إنشاء مجموعة الجودة، لتحديد العناصر التي سيتم أخذ عينات مها واختبار مجموعة لتجميع الاختبارات التي يجب القيام بها على العناصر الموجودة في مجموعة الجودة.</span><span class="sxs-lookup"><span data-stu-id="11170-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="11170-107">يمكنك تشغيل هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="11170-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="11170-108">تمكين إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="11170-108">Enable quality management</span></span>
1. <span data-ttu-id="11170-109">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المخزون > الإعداد > محددات إدارة المستودعات والمخزون‬**.</span><span class="sxs-lookup"><span data-stu-id="11170-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="11170-110">انقر فوق علامة التبويب **إدارة الجودة**.</span><span class="sxs-lookup"><span data-stu-id="11170-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="11170-111">عيّن الخيار **استخدام إدارة الجودة** إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="11170-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="11170-112">انقر فوق **إعداد التقرير‬**.</span><span class="sxs-lookup"><span data-stu-id="11170-112">Click **Report setup**.</span></span> <span data-ttu-id="11170-113">في USMF، يتم تعريف إعداد تقرير إدارة الجودة بشكل مسبق.</span><span class="sxs-lookup"><span data-stu-id="11170-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="11170-114">إذا لم يتم ذلك، فستضيف بنودًا جديدة هنا لأنواع التقارير المختلفة وستحدد نوع المستند الذي يجب استخدامه لكل تقرير.</span><span class="sxs-lookup"><span data-stu-id="11170-114">If this wasn't done, you'd add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="11170-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-115">Close the page.</span></span>
6. <span data-ttu-id="11170-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="11170-117">إنشاء اختبار</span><span class="sxs-lookup"><span data-stu-id="11170-117">Create a test</span></span>
1. <span data-ttu-id="11170-118">انتقل إلى **إدارة المخزون > الإعداد > مراقبة الجودة > الاختبارات‬**.</span><span class="sxs-lookup"><span data-stu-id="11170-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="11170-119">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-119">Click **New**.</span></span>
3. <span data-ttu-id="11170-120">في الحقل **اختبار**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="11170-121">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11170-122">في حقل **النوع**، حدد "خيار".</span><span class="sxs-lookup"><span data-stu-id="11170-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="11170-123">في هذا المثال، سوف نحدد "خيار" مما يجعل من الممكن تعيين نتائج الاختبار استنادًا إلى قيم معرّفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="11170-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="11170-124">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-124">Click **Save**.</span></span>
7. <span data-ttu-id="11170-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="11170-126">إنشاء متغيرات الاختبار لتحديد الطريقة التي يتم بها تسجيل نتائج الاختبار</span><span class="sxs-lookup"><span data-stu-id="11170-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="11170-127">انتقل إلى **إدارة المخزون > الإعداد > مراقبة الجودة > متغيرات الاختبار**‬.</span><span class="sxs-lookup"><span data-stu-id="11170-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="11170-128">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-128">Click **New**.</span></span>
3. <span data-ttu-id="11170-129">في الحقل **المتغير‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="11170-130">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11170-131">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-131">Click **Save**.</span></span>
6. <span data-ttu-id="11170-132">انقر فوق **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="11170-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="11170-133">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-133">Click **New**.</span></span>
8. <span data-ttu-id="11170-134">في الحقل **النتيجة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="11170-135">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="11170-136">في الحقل **حالة الناتج**، حدد "نجاح‬".</span><span class="sxs-lookup"><span data-stu-id="11170-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="11170-137">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-137">Click **Save**.</span></span>
12. <span data-ttu-id="11170-138">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-138">Click **New**.</span></span>
13. <span data-ttu-id="11170-139">في الحقل **النتيجة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="11170-140">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="11170-141">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-141">Click **Save**.</span></span>
16. <span data-ttu-id="11170-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-142">Close the page.</span></span>
17. <span data-ttu-id="11170-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="11170-144">إعداد أخذ عينات الصنف‬</span><span class="sxs-lookup"><span data-stu-id="11170-144">Set up item sampling</span></span>
1. <span data-ttu-id="11170-145">انتقل إلى **إدارة المخزون > الإعداد > مراقبة الجودة > أخذ عينات للصنف**.</span><span class="sxs-lookup"><span data-stu-id="11170-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="11170-146">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-146">Click **New**.</span></span>
3. <span data-ttu-id="11170-147">في الحقل **أخذ عينات للصنف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="11170-148">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11170-149">في الحقل **القيمة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="11170-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="11170-150">تتعلق هذه القيمة بمواصفات الكمية‬ المحددة في الحقل المجاور.</span><span class="sxs-lookup"><span data-stu-id="11170-150">This value relates to the Quantity specification that's selected in the adjacent field.</span></span>  
6. <span data-ttu-id="11170-151">قم بتوسيع أو طي قسم **العملية**.</span><span class="sxs-lookup"><span data-stu-id="11170-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="11170-152">حدد خانة الاختيار **حظر كامل**  أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="11170-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="11170-153">إذا حددت هذا الخيار، فسيتم حظر الدفعة أو كمية بند الأمر بكاملها إذا فشل الاختبار.</span><span class="sxs-lookup"><span data-stu-id="11170-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="11170-154">إذا لم تحدد هذا الخيار، فسيتم حظر الأصناف في أمر الجودة فقط.</span><span class="sxs-lookup"><span data-stu-id="11170-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="11170-155">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-155">Click **Save**.</span></span>
9. <span data-ttu-id="11170-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="11170-157">إنشاء مجموعة جودة</span><span class="sxs-lookup"><span data-stu-id="11170-157">Create a quality group</span></span>
1. <span data-ttu-id="11170-158">انتقل إلى **إدارة المخزون > الإعداد > مراقبة الجودة > مجموعات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="11170-158">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="11170-159">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-159">Click **New**.</span></span>
3. <span data-ttu-id="11170-160">في الحقل **مجموعة الجودة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-160">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="11170-161">استخدم اسمًا وصفيًا للتعرف على نوع الأصناف التي ستحتوي عليها المجموعة معايير العينات).</span><span class="sxs-lookup"><span data-stu-id="11170-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="11170-162">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-162">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11170-163">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-163">Click **Save**.</span></span>
6. <span data-ttu-id="11170-164">انقر فوق **إضافة أصناف**.</span><span class="sxs-lookup"><span data-stu-id="11170-164">Click **Add items**.</span></span>
7. <span data-ttu-id="11170-165">حدد صف **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="11170-165">Select the **Item number** row.</span></span> <span data-ttu-id="11170-166">في هذا المثال، سيتم تشغيل التصفية استنادًا إلى رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="11170-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="11170-167">في الحقل **المعايير**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-167">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="11170-168">على سبيل المثال، اكتب T\* للتصفية حسب أرقام الأصناف التي تبدأ بالحرف T.</span><span class="sxs-lookup"><span data-stu-id="11170-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="11170-169">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="11170-169">Click **OK**.</span></span>
10. <span data-ttu-id="11170-170">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="11170-170">Click **OK**.</span></span>
11. <span data-ttu-id="11170-171">انقر فوق **مجموعات جودة الصنف**.</span><span class="sxs-lookup"><span data-stu-id="11170-171">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="11170-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-172">Close the page.</span></span>
13. <span data-ttu-id="11170-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="11170-174">إنشاء مجموعة اختبار</span><span class="sxs-lookup"><span data-stu-id="11170-174">Create a test group</span></span>
1. <span data-ttu-id="11170-175">انتقل إلى **إدارة المخزون > الإعداد > مراقبة الجودة‬ > مجموعات الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="11170-175">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="11170-176">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-176">Click **New**.</span></span>
3. <span data-ttu-id="11170-177">في الحقل **مجموعة الاختبار‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-177">In the **Test group** field, type a value.</span></span> <span data-ttu-id="11170-178">أدخل اسمًا **لمجموعة الاختبار** ليساعدك على تذكر أنواع الاختبارات الجاري تشغيلها، ومجموعة الجودة التي يجب إقرانها بها.</span><span class="sxs-lookup"><span data-stu-id="11170-178">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="11170-179">على سبيل المثال، يجب استخدامها مع مجموعة جودة تحدد الأصناف التي تبدأ بالحرف "T"، ويمكنك تسميتها "اختبارات أصناف T".</span><span class="sxs-lookup"><span data-stu-id="11170-179">For example, it it's to be used with a quality group that selects items starting with "T", you could call it "T-item tests".</span></span>  
4. <span data-ttu-id="11170-180">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11170-180">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11170-181">في الحقل **أخذ عينات للصنف**‬، حدد بند أخذ العينات للصنف‬ الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="11170-181">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="11170-182">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="11170-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11170-183">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="11170-183">Click **Add**.</span></span>
8. <span data-ttu-id="11170-184">الرقم التسلسلي **الرقم التسلسلي**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="11170-184">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="11170-185">في الحقل **اختبار**، حدد الاختبار الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="11170-185">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="11170-186">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="11170-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="11170-187">انقر فوق علامة التبويب **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="11170-187">Click the **Test** tab.</span></span>
12. <span data-ttu-id="11170-188">في الحقل **المتغير‬**، حدد متغير الاختبار الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="11170-188">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="11170-189">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="11170-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="11170-190">في الحقل **الناتج الافتراضي‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11170-190">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="11170-191">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11170-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="11170-192">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-192">Click **Save**.</span></span>
17. <span data-ttu-id="11170-193">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="11170-194">تعريف توقيت إنشاء أوامر الجودة</span><span class="sxs-lookup"><span data-stu-id="11170-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="11170-195">انتقل إلى **إدارة المخزون > الإعداد > مراقبة الجودة > عمليات اقتران الجودة**‬.</span><span class="sxs-lookup"><span data-stu-id="11170-195">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="11170-196">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="11170-196">Click **New**.</span></span>
3. <span data-ttu-id="11170-197">في الحقل **نوع المرجع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="11170-197">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="11170-198">في الحقل **كود الصنف**، حدد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="11170-198">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="11170-199">في هذا المثال، سنقوم بتحديد "مجموعة" وسنستخدم مجموعة الجودة التي أنشأناها في السابق.</span><span class="sxs-lookup"><span data-stu-id="11170-199">In this example, we'll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="11170-200">يمكن أيضا تعيين هذه القيمة إلى "جدول" لتحديد الأصناف يدويًا، أو تحديد "الكل" لإضافة كافة الأصناف لأمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="11170-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="11170-201">في الحقل **صنف‬**، حدد مجموعة الجودة التي أنشأتها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="11170-201">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="11170-202">تتوقف الخيارات المتوفرة في حقل "الصنف" على ما قمت بتعيينه في حقل "كود الصنف".</span><span class="sxs-lookup"><span data-stu-id="11170-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="11170-203">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="11170-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11170-204">قم بتوسيع قسم "العملية" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="11170-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="11170-205">في الحقل **نوع الحدث**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="11170-205">In the **Event type** field, select an option.</span></span> <span data-ttu-id="11170-206">هذا هو الحدث الذي سيقوم بتشغيل الاختبار.</span><span class="sxs-lookup"><span data-stu-id="11170-206">This is the event that triggers the test.</span></span> <span data-ttu-id="11170-207">تتوقف الخيارات المتاحة هنا على العملية التي حددتها في الحقل "نوع المرجع".</span><span class="sxs-lookup"><span data-stu-id="11170-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="11170-208">في الحقل **التنفيذ**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="11170-208">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="11170-209">قم بتوسيع قسم **معالجة أمر الجودة‬** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="11170-209">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="11170-210">في الحقل **حظر الحدث**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11170-210">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="11170-211">يظهر هذا الحقل قائمة العمليات التي يمكن حظرها إذا كان أمر الجودة ما زال مفتوحًا.</span><span class="sxs-lookup"><span data-stu-id="11170-211">This field shows the list of processes that it's possible to block if the quality order is still open.</span></span> <span data-ttu-id="11170-212">تتوقف الخيارات على ما حددته في الحقل "نوع الحدث".</span><span class="sxs-lookup"><span data-stu-id="11170-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="11170-213">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11170-213">In the list, click the link in the selected row.</span></span> <span data-ttu-id="11170-214">سيتوقف ذلك على القيم المحددة السابقة.</span><span class="sxs-lookup"><span data-stu-id="11170-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="11170-215">حدد ما إذا كان يجب حظر العمليات التالية أثناء ارتباط أوامر الجودة المفتوحة ببند المستند المصدر.</span><span class="sxs-lookup"><span data-stu-id="11170-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="11170-216">قم بتوسيع قسم **المواصفات** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="11170-216">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="11170-217">في الحقل **مجموعة الاختبار‬**، حدد مجموعة الاختبار‬ التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="11170-217">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="11170-218">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="11170-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="11170-219">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11170-219">Click **Save**.</span></span>
17. <span data-ttu-id="11170-220">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11170-220">Close the page.</span></span>

