---
title: التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 3 - استخدام العمليات الحسابية لإنشاء المخرجات)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "347067"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="82b0d-103">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 3: استخدام العمليات الحسابية لإنشاء المخرجات)</span><span class="sxs-lookup"><span data-stu-id="82b0d-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82b0d-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="82b0d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="82b0d-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="82b0d-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 2: العمليات الحسابية)".</span><span class="sxs-lookup"><span data-stu-id="82b0d-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="82b0d-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="82b0d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="82b0d-108">تكوين هذا التقرير لاستخدام معلومات الجرد والتجميع</span><span class="sxs-lookup"><span data-stu-id="82b0d-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="82b0d-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="82b0d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="82b0d-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="82b0d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="82b0d-111">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="82b0d-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="82b0d-112">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="82b0d-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="82b0d-113">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="82b0d-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="82b0d-114">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="82b0d-114">Click Designer.</span></span>
7. <span data-ttu-id="82b0d-115">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="82b0d-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="82b0d-116">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="82b0d-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="82b0d-117">أضف مصدر بيانات جديدًا للحصول على قائمة الكتل المحفوظة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="82b0d-118">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="82b0d-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="82b0d-119">في حقل "الاسم"، اكتب "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="82b0d-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="82b0d-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="82b0d-120">$BlocksList</span></span>  
11. <span data-ttu-id="82b0d-121">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-121">Click Edit formula.</span></span>
12. <span data-ttu-id="82b0d-122">في الشجرة، حدد "وظائف تجميع البيانات\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="82b0d-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="82b0d-123">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-123">Click Add function.</span></span>
14. <span data-ttu-id="82b0d-124">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="82b0d-124">Click Add data source.</span></span>
15. <span data-ttu-id="82b0d-125">في حقل "المعادلة"، أدخل 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="82b0d-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="82b0d-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="82b0d-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="82b0d-127">في حقل "المعادلة"، أدخل 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="82b0d-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="82b0d-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="82b0d-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="82b0d-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="82b0d-129">Click Save.</span></span>
    * <span data-ttu-id="82b0d-130">يعني النمط "\*" أنه سيتم تضمين جميع الكتل لهذا السجل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="82b0d-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-131">Close the page.</span></span>
19. <span data-ttu-id="82b0d-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-132">Click OK.</span></span>
20. <span data-ttu-id="82b0d-133">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-133">Click the Format tab.</span></span>
21. <span data-ttu-id="82b0d-134">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات".</span><span class="sxs-lookup"><span data-stu-id="82b0d-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="82b0d-135">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="82b0d-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="82b0d-136">في الشجرة، حدد "النص\التسلسل".</span><span class="sxs-lookup"><span data-stu-id="82b0d-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="82b0d-137">في الحقل "الاسم"، اكتب "الإجماليات بكتل‬‬".‬</span><span class="sxs-lookup"><span data-stu-id="82b0d-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="82b0d-138">الإجماليات بكتل‬</span><span class="sxs-lookup"><span data-stu-id="82b0d-138">Totals by blocks</span></span>  
25. <span data-ttu-id="82b0d-139">في الحقل "أحرف خاصة‬"، حدد "سطر جديد - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="82b0d-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="82b0d-140">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="82b0d-140">Click OK.</span></span>
27. <span data-ttu-id="82b0d-141">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬".</span><span class="sxs-lookup"><span data-stu-id="82b0d-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="82b0d-142">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="82b0d-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="82b0d-143">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="82b0d-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="82b0d-144">في حقل "الاسم"، اكتب "كود الكتلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="82b0d-145">كود الكتلة</span><span class="sxs-lookup"><span data-stu-id="82b0d-145">Block code</span></span>  
31. <span data-ttu-id="82b0d-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-146">Click OK.</span></span>
32. <span data-ttu-id="82b0d-147">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-147">Click Add String.</span></span>
33. <span data-ttu-id="82b0d-148">في الحقل "الاسم"، اكتب "تعداد البنود‬".</span><span class="sxs-lookup"><span data-stu-id="82b0d-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="82b0d-149">تعداد البنود</span><span class="sxs-lookup"><span data-stu-id="82b0d-149">Lines counting</span></span>  
34. <span data-ttu-id="82b0d-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-150">Click OK.</span></span>
35. <span data-ttu-id="82b0d-151">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-151">Click Add String.</span></span>
36. <span data-ttu-id="82b0d-152">في الحقل "الاسم"، اكتب "المبلغ الإجمالي".</span><span class="sxs-lookup"><span data-stu-id="82b0d-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="82b0d-153">المبلغ الإجمالي</span><span class="sxs-lookup"><span data-stu-id="82b0d-153">Total amount</span></span>  
37. <span data-ttu-id="82b0d-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-154">Click OK.</span></span>
38. <span data-ttu-id="82b0d-155">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="82b0d-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="82b0d-156">في الشجرة، حدد "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="82b0d-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="82b0d-157">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="82b0d-157">Click Bind.</span></span>
    * <span data-ttu-id="82b0d-158">أنشئ بند تلخيص لكل كتلة محفوظة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="82b0d-159">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-159">Click the Format tab.</span></span>
42. <span data-ttu-id="82b0d-160">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬\كود الكتلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="82b0d-161">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="82b0d-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="82b0d-162">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-162">Click Edit formula.</span></span>
45. <span data-ttu-id="82b0d-163">في حقل "المعادلة"، أدخل '"معرف الكتلة: " & '.</span><span class="sxs-lookup"><span data-stu-id="82b0d-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="82b0d-164">"معرف الكتلة: " &</span><span class="sxs-lookup"><span data-stu-id="82b0d-164">"Block id: " &</span></span>  
46. <span data-ttu-id="82b0d-165">في الشجرة، قم بتوسيع "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="82b0d-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="82b0d-166">في الشجرة، حدد "$BlocksList\Value".</span><span class="sxs-lookup"><span data-stu-id="82b0d-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="82b0d-167">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="82b0d-167">Click Add data source.</span></span>
49. <span data-ttu-id="82b0d-168">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="82b0d-168">Click Save.</span></span>
50. <span data-ttu-id="82b0d-169">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-169">Close the page.</span></span>
51. <span data-ttu-id="82b0d-170">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-170">Click the Format tab.</span></span>
52. <span data-ttu-id="82b0d-171">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬\تعداد البنود".</span><span class="sxs-lookup"><span data-stu-id="82b0d-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="82b0d-172">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="82b0d-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="82b0d-173">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-173">Click Edit formula.</span></span>
    * <span data-ttu-id="82b0d-174">أنشئ مخرجات لعدد البنود لكل كتلة واردة في هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="82b0d-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="82b0d-175">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & '.</span><span class="sxs-lookup"><span data-stu-id="82b0d-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="82b0d-176">"عدد البنود في هذه الكتلة: " &</span><span class="sxs-lookup"><span data-stu-id="82b0d-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="82b0d-177">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="82b0d-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="82b0d-178">"عدد البنود في هذه الكتلة: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="82b0d-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="82b0d-179">في الشجرة، حدد "وظائف تجميع البيانات\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="82b0d-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="82b0d-180">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-180">Click Add function.</span></span>
59. <span data-ttu-id="82b0d-181">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="82b0d-181">Click Add data source.</span></span>
60. <span data-ttu-id="82b0d-182">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="82b0d-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="82b0d-183">"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="82b0d-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="82b0d-184">في الشجرة، قم بتوسيع "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="82b0d-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="82b0d-185">في الشجرة، حدد "$BlocksList\Value".</span><span class="sxs-lookup"><span data-stu-id="82b0d-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="82b0d-186">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="82b0d-186">Click Add data source.</span></span>
64. <span data-ttu-id="82b0d-187">في حقل "المعادلة"، أدخل '"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="82b0d-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="82b0d-188">"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="82b0d-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="82b0d-189">في الشجرة، حدد "$RecName".</span><span class="sxs-lookup"><span data-stu-id="82b0d-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="82b0d-190">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="82b0d-190">Click Add data source.</span></span>
67. <span data-ttu-id="82b0d-191">في حقل "المعادلة، أدخل '"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="82b0d-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="82b0d-192">"عدد البنود في هذه الكتلة: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="82b0d-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="82b0d-193">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="82b0d-193">Click Save.</span></span>
69. <span data-ttu-id="82b0d-194">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-194">Close the page.</span></span>
70. <span data-ttu-id="82b0d-195">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="82b0d-195">Click the Format tab.</span></span>
71. <span data-ttu-id="82b0d-196">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\الإجماليات بكتل‬‬\المبلغ الإجمالي".</span><span class="sxs-lookup"><span data-stu-id="82b0d-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="82b0d-197">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="82b0d-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="82b0d-198">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="82b0d-198">Click Edit formula.</span></span>
    * <span data-ttu-id="82b0d-199">أنشئ مخرجات ستكون إجمالي المبلغ المفوتر لكل كتلة واردة في هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="82b0d-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="82b0d-200">في حقل "المعادلة"، أدخل '"مجموع المبلغ المفوتر: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="82b0d-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="82b0d-201">"مجموع المبلغ المفوتر: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="82b0d-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="82b0d-202">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="82b0d-202">Click Save.</span></span>
76. <span data-ttu-id="82b0d-203">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-203">Close the page.</span></span>
77. <span data-ttu-id="82b0d-204">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="82b0d-204">Click Save.</span></span>
78. <span data-ttu-id="82b0d-205">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b0d-205">Close the page.</span></span>

