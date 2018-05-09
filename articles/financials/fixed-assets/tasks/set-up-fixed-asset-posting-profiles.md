--- 
title: "إعداد ملفات تعريف ترحيل الأصول الثابتة"
description: "سيقوم دليل المهمة هذا بإعداد ملفات تعريف ترحيل الأصول الثابتة."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d07df2c2779833485bd70240c47bb569622800f8
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="c8526-103">إعداد ملفات تعريف ترحيل الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="c8526-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8526-104">سيقوم دليل المهمة هذا بإعداد ملفات تعريف ترحيل الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c8526-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="c8526-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="c8526-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="c8526-106">تتعلق الأمثلة الواردة في دليل المهمة بملف تعريف ترحيل أساسي، على الرغم من ضرورة إنشاء ملفات تعريف ترحيل خاصة بمتطلبات معينة لدليل الحسابات‬ والتقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="c8526-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="c8526-107">انتقل إلى الأصول الثابتة > إعداد > ملفات تعريف ترحيل الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="c8526-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="c8526-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c8526-108">Click New.</span></span>
3. <span data-ttu-id="c8526-109">في الحقل "ملف تعريف ترحيل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8526-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="c8526-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8526-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c8526-111">ستحتاج إلى إنشاء ملف تعريف ترحيل لكل نوع من أنواع حركات الأصول الثابتة التي ستستخدمها عند التعامل مع الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c8526-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="c8526-112">سيبدأ دليل المهمة هذا بنوع حركة الاستحواذ.</span><span class="sxs-lookup"><span data-stu-id="c8526-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="c8526-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-113">Click Add.</span></span>
6. <span data-ttu-id="c8526-114">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="c8526-115">يسمح لك الحقل "عمليات التجميع‬" بتحديد ملف تعريف الترحيل في "الجدول" (إعداد حساب واحد لكل أصل ثابت) أو "المجموعة" (حساب واحد لكل مجموعة أصول ثابتة).</span><span class="sxs-lookup"><span data-stu-id="c8526-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="c8526-116">بالنسبة إلى دليل المهمة هذا، سوف اترك القيمة معينة إلى "الكل" لتطبيقها على كافة الأصول الثابتة باستخدام الدفتر المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8526-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="c8526-117">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c8526-118">بالنسبة إلى عمليات الاستحواذ، يمكنك إدخال حساب مقابل أو تركه فارغًا لكي تتم تعبئته للحركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c8526-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="c8526-119">في الحقل "نوع الحركة"، حدد "تسوية الاستحواذ".</span><span class="sxs-lookup"><span data-stu-id="c8526-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="c8526-120">بالنسبة إلى حركات تسوية الاستحواذ، سوف نستخدم نفس الحسابات التي تم استخدامها لحركات الاستحواذ.</span><span class="sxs-lookup"><span data-stu-id="c8526-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="c8526-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-121">Click Add.</span></span>
10. <span data-ttu-id="c8526-122">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="c8526-123">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c8526-124">بالنسبة إلى عمليات تسوية الاستحواذ، يمكنك إدخال حساب مقابل أو تركه فارغًا لكي تتم تعبئته للحركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c8526-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="c8526-125">في الحقل "نوع الحركة"، حدد "إهلاك".</span><span class="sxs-lookup"><span data-stu-id="c8526-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="c8526-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-126">Click Add.</span></span>
14. <span data-ttu-id="c8526-127">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="c8526-128">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="c8526-129">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="c8526-130">في الحقل "نوع الحركة"، حدد "تسوية الإهلاك".</span><span class="sxs-lookup"><span data-stu-id="c8526-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="c8526-131">بالنسبة إلى حركات تسوية الإهلاك، سوف نستخدم نفس الحسابات التي تم استخدامها لحركات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="c8526-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="c8526-132">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-132">Click Add.</span></span>
19. <span data-ttu-id="c8526-133">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="c8526-134">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="c8526-135">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="c8526-136">في الحقل "نوع الحركة"، حدد "التخلص - البيع‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="c8526-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-137">Click Add.</span></span>
24. <span data-ttu-id="c8526-138">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="c8526-139">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c8526-140">بالنسبة إلى عمليات التخلص، يمكنك إدخال حساب مقابل أو تركه فارغًا لكي تتم تعبئته للحركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c8526-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="c8526-141">في الحقل "نوع الحركة"، حدد "التخلص - الخردة‬‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="c8526-142">سوف نستخدم الحسابات نفسها للتخلص عن طريق البيع والتخلص عن طريق التخريد.</span><span class="sxs-lookup"><span data-stu-id="c8526-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="c8526-143">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-143">Click Add.</span></span>
28. <span data-ttu-id="c8526-144">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="c8526-145">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c8526-146">بالنسبة إلى عمليات التخلص، يمكنك إدخال حساب مقابل أو تركه فارغًا لكي تتم تعبئته للحركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c8526-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="c8526-147">قم بتوسيع قسم "التخلص‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="c8526-148">يجب إعداد ملفات تعريف ترحيل التخلص لكل من البيع والخردة.</span><span class="sxs-lookup"><span data-stu-id="c8526-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="c8526-149">سنبدأ بالحركات الخاصة بالتخلص عن طريق البيع.</span><span class="sxs-lookup"><span data-stu-id="c8526-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="c8526-150">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-150">Click Add.</span></span>
32. <span data-ttu-id="c8526-151">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="c8526-152">في الحقل "ترحيل القيمة‬"، حدد "قيمة الاستحواذ‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="c8526-153">ستأخذ قيمة الاستحواذ في الاعتبار الاستحواذ وقيم تسوية الاستحواذ لكل السنوات.</span><span class="sxs-lookup"><span data-stu-id="c8526-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="c8526-154">يمكنك أيضًا تعريف حسابات لأنواع هذه الحركات بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="c8526-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="c8526-155">يمكنك تعيين عملية التخلص لاستخدام حسابات مختلفة بالاستناد إلى ما إذا كانت نتائج التخلص تؤدي إلى ربح أو خسارة.</span><span class="sxs-lookup"><span data-stu-id="c8526-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="c8526-156">سأقوم بتعيين نوع قيمة المبيعات إلى "الكل" لاستخدام نفس الحسابات لجميع أنواع عمليات التخلص.</span><span class="sxs-lookup"><span data-stu-id="c8526-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="c8526-157">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="c8526-158">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="c8526-159">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-159">Click Add.</span></span>
37. <span data-ttu-id="c8526-160">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="c8526-161">في الحقل "ترحيل القيمة‬"، حدد "الإهلاك (سنوات سابقة)".</span><span class="sxs-lookup"><span data-stu-id="c8526-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="c8526-162">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="c8526-163">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="c8526-164">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-164">Click Add.</span></span>
41. <span data-ttu-id="c8526-165">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="c8526-166">في الحقل "ترحيل القيمة‬"، حدد "الإهلاك (هذه السنة)".</span><span class="sxs-lookup"><span data-stu-id="c8526-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="c8526-167">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="c8526-168">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="c8526-169">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-169">Click Add.</span></span>
46. <span data-ttu-id="c8526-170">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="c8526-171">في الحقل "ترحيل القيمة‬"، حدد "تسويات الإهلاك (سنوات سابقة)‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="c8526-172">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="c8526-173">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="c8526-174">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-174">Click Add.</span></span>
51. <span data-ttu-id="c8526-175">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="c8526-176">في الحقل "ترحيل القيمة‬"، حدد "تسويات الإهلاك (هذه السنة)".</span><span class="sxs-lookup"><span data-stu-id="c8526-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="c8526-177">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="c8526-178">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="c8526-179">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-179">Click Add.</span></span>
56. <span data-ttu-id="c8526-180">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="c8526-181">في الحقل "ترحيل القيمة‬"، حدد "صافي القيمة الدفترية‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="c8526-182">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="c8526-183">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="c8526-184">في الحقل "بيع أو تخريد‬"، حدد "خردة‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="c8526-185">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-185">Click Add.</span></span>
62. <span data-ttu-id="c8526-186">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="c8526-187">في الحقل "ترحيل القيمة‬"، حدد "قيمة الاستحواذ‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="c8526-188">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="c8526-189">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="c8526-190">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-190">Click Add.</span></span>
67. <span data-ttu-id="c8526-191">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="c8526-192">في الحقل "ترحيل القيمة‬"، حدد "الإهلاك (سنوات سابقة)".</span><span class="sxs-lookup"><span data-stu-id="c8526-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="c8526-193">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="c8526-194">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="c8526-195">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-195">Click Add.</span></span>
71. <span data-ttu-id="c8526-196">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="c8526-197">في الحقل "ترحيل القيمة‬"، حدد "الإهلاك (هذه السنة)".</span><span class="sxs-lookup"><span data-stu-id="c8526-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="c8526-198">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="c8526-199">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="c8526-200">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-200">Click Add.</span></span>
76. <span data-ttu-id="c8526-201">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="c8526-202">في الحقل "ترحيل القيمة‬"، حدد "تسويات الإهلاك (سنوات سابقة)‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="c8526-203">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="c8526-204">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="c8526-205">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-205">Click Add.</span></span>
81. <span data-ttu-id="c8526-206">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="c8526-207">في الحقل "ترحيل القيمة‬"، حدد "تسويات الإهلاك (هذه السنة)".</span><span class="sxs-lookup"><span data-stu-id="c8526-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="c8526-208">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="c8526-209">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="c8526-210">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="c8526-210">Click Add.</span></span>
86. <span data-ttu-id="c8526-211">في الحقل "الدفتر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8526-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="c8526-212">في الحقل "ترحيل القيمة‬"، حدد "صافي القيمة الدفترية‬".</span><span class="sxs-lookup"><span data-stu-id="c8526-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="c8526-213">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="c8526-214">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8526-214">In the Offset account field, specify the desired values.</span></span>


