---
title: التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 3 - استخدام العمليات الحسابية لإنشاء المخرجات)
description: يصف هذا الموضوع كيفيه تكوين تنسيق التقارير الكتروني للقيام بالجرد والجمع استنادا إلى البيانات الخاصة بإخراج النص الذي تم إنشاؤه بالفعل. (جزء 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092962"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="cf5c3-104">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 3 - استخدام العمليات الحسابية لإنشاء المخرجات)</span><span class="sxs-lookup"><span data-stu-id="cf5c3-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf5c3-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="cf5c3-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="cf5c3-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 2: العمليات الحسابية)".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="cf5c3-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="cf5c3-109">تكوين هذا التقرير لاستخدام معلومات الجرد والتجميع</span><span class="sxs-lookup"><span data-stu-id="cf5c3-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="cf5c3-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cf5c3-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="cf5c3-112">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="cf5c3-113">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="cf5c3-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="cf5c3-114">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="cf5c3-115">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-115">Click Designer.</span></span>
7. <span data-ttu-id="cf5c3-116">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="cf5c3-117">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="cf5c3-118">أضف مصدر بيانات جديدًا للحصول على قائمة الكتل المحفوظة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="cf5c3-119">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="cf5c3-120">في حقل "الاسم"، اكتب "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="cf5c3-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="cf5c3-121">$BlocksList</span></span>  
11. <span data-ttu-id="cf5c3-122">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-122">Click Edit formula.</span></span>
12. <span data-ttu-id="cf5c3-123">في الشجرة، حدد "وظائف تجميع البيانات\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="cf5c3-124">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-124">Click Add function.</span></span>
14. <span data-ttu-id="cf5c3-125">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-125">Click Add data source.</span></span>
15. <span data-ttu-id="cf5c3-126">في حقل "المعادلة"، أدخل 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="cf5c3-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="cf5c3-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="cf5c3-128">في حقل "المعادلة"، أدخل 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="cf5c3-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="cf5c3-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="cf5c3-130">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-130">Click Save.</span></span>
    * <span data-ttu-id="cf5c3-131">يعني النمط "\*" أنه سيتم تضمين جميع الكتل لهذا السجل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="cf5c3-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-132">Close the page.</span></span>
19. <span data-ttu-id="cf5c3-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-133">Click OK.</span></span>
20. <span data-ttu-id="cf5c3-134">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-134">Click the Format tab.</span></span>
21. <span data-ttu-id="cf5c3-135">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="cf5c3-136">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="cf5c3-137">في الشجرة، حدد "النص\التسلسل".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="cf5c3-138">في الحقل "الاسم"، اكتب "الإجماليات بكتل‬‬".‬</span><span class="sxs-lookup"><span data-stu-id="cf5c3-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="cf5c3-139">الإجماليات بكتل‬</span><span class="sxs-lookup"><span data-stu-id="cf5c3-139">Totals by blocks</span></span>  
25. <span data-ttu-id="cf5c3-140">في الحقل "أحرف خاصة‬"، حدد "سطر جديد - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="cf5c3-141">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-141">Click OK.</span></span>
27. <span data-ttu-id="cf5c3-142">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="cf5c3-143">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="cf5c3-144">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="cf5c3-145">في حقل "الاسم"، اكتب "كود الكتلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="cf5c3-146">كود الكتلة</span><span class="sxs-lookup"><span data-stu-id="cf5c3-146">Block code</span></span>  
31. <span data-ttu-id="cf5c3-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-147">Click OK.</span></span>
32. <span data-ttu-id="cf5c3-148">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-148">Click Add String.</span></span>
33. <span data-ttu-id="cf5c3-149">في الحقل "الاسم"، اكتب "تعداد البنود‬".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="cf5c3-150">تعداد البنود</span><span class="sxs-lookup"><span data-stu-id="cf5c3-150">Lines counting</span></span>  
34. <span data-ttu-id="cf5c3-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-151">Click OK.</span></span>
35. <span data-ttu-id="cf5c3-152">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-152">Click Add String.</span></span>
36. <span data-ttu-id="cf5c3-153">في الحقل "الاسم"، اكتب "المبلغ الإجمالي".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="cf5c3-154">المبلغ الإجمالي</span><span class="sxs-lookup"><span data-stu-id="cf5c3-154">Total amount</span></span>  
37. <span data-ttu-id="cf5c3-155">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-155">Click OK.</span></span>
38. <span data-ttu-id="cf5c3-156">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="cf5c3-157">في الشجرة، حدد "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="cf5c3-158">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-158">Click Bind.</span></span>
    * <span data-ttu-id="cf5c3-159">أنشئ بند تلخيص لكل كتلة محفوظة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="cf5c3-160">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-160">Click the Format tab.</span></span>
42. <span data-ttu-id="cf5c3-161">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬\كود الكتلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="cf5c3-162">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="cf5c3-163">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-163">Click Edit formula.</span></span>
45. <span data-ttu-id="cf5c3-164">في حقل "المعادلة"، أدخل '"معرف الكتلة: " & '.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="cf5c3-165">"معرف الكتلة: " &</span><span class="sxs-lookup"><span data-stu-id="cf5c3-165">"Block id: " &</span></span>  
46. <span data-ttu-id="cf5c3-166">في الشجرة، قم بتوسيع "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="cf5c3-167">في الشجرة، حدد "$BlocksList\Value".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="cf5c3-168">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-168">Click Add data source.</span></span>
49. <span data-ttu-id="cf5c3-169">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-169">Click Save.</span></span>
50. <span data-ttu-id="cf5c3-170">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-170">Close the page.</span></span>
51. <span data-ttu-id="cf5c3-171">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-171">Click the Format tab.</span></span>
52. <span data-ttu-id="cf5c3-172">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬\تعداد البنود".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="cf5c3-173">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="cf5c3-174">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-174">Click Edit formula.</span></span>
    * <span data-ttu-id="cf5c3-175">أنشئ مخرجات لعدد البنود لكل كتلة واردة في هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="cf5c3-176">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & '.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="cf5c3-177">"عدد البنود في هذه الكتلة: " &</span><span class="sxs-lookup"><span data-stu-id="cf5c3-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="cf5c3-178">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="cf5c3-179">"عدد البنود في هذه الكتلة: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="cf5c3-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="cf5c3-180">في الشجرة، حدد "وظائف تجميع البيانات\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="cf5c3-181">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-181">Click Add function.</span></span>
59. <span data-ttu-id="cf5c3-182">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-182">Click Add data source.</span></span>
60. <span data-ttu-id="cf5c3-183">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="cf5c3-184">"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="cf5c3-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="cf5c3-185">في الشجرة، قم بتوسيع "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="cf5c3-186">في الشجرة، حدد "$BlocksList\Value".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="cf5c3-187">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-187">Click Add data source.</span></span>
64. <span data-ttu-id="cf5c3-188">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="cf5c3-189">"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="cf5c3-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="cf5c3-190">في الشجرة، حدد "$RecName".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="cf5c3-191">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-191">Click Add data source.</span></span>
67. <span data-ttu-id="cf5c3-192">في حقل "المعادلة، أدخل '"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="cf5c3-193">"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="cf5c3-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="cf5c3-194">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-194">Click Save.</span></span>
69. <span data-ttu-id="cf5c3-195">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-195">Close the page.</span></span>
70. <span data-ttu-id="cf5c3-196">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-196">Click the Format tab.</span></span>
71. <span data-ttu-id="cf5c3-197">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬\المبلغ الإجمالي".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="cf5c3-198">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="cf5c3-199">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-199">Click Edit formula.</span></span>
    * <span data-ttu-id="cf5c3-200">أنشئ مخرجات ستكون إجمالي المبلغ المفوتر لكل كتلة واردة في هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="cf5c3-201">في حقل "المعادلة"، أدخل '"مجموع المبلغ المفوتر: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="cf5c3-202">"مجموع المبلغ المفوتر: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="cf5c3-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="cf5c3-203">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-203">Click Save.</span></span>
76. <span data-ttu-id="cf5c3-204">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-204">Close the page.</span></span>
77. <span data-ttu-id="cf5c3-205">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cf5c3-205">Click Save.</span></span>
78. <span data-ttu-id="cf5c3-206">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cf5c3-206">Close the page.</span></span>

