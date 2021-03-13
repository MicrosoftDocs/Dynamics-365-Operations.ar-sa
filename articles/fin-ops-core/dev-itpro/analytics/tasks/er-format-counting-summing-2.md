---
title: التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 2 - تكوين العمليات الحسابية)
description: يصف هذا الموضوع كيفيه تكوين تنسيق التقارير الكتروني للقيام بالجرد والجمع استنادا إلى البيانات الخاصة بإخراج النص الذي تم إنشاؤه بالفعل. (جزء 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6215fe1f32bcb4833bd009b7c33e09edbba17817
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092987"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="78e68-104">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 2 - تكوين العمليات الحسابية)</span><span class="sxs-lookup"><span data-stu-id="78e68-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78e68-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="78e68-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="78e68-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="78e68-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="78e68-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 1: إنشاء التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="78e68-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="78e68-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="78e68-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="78e68-109">إنشاء تكوين تنسيق لإضافة تفاصيل الجرد والتجميع‬</span><span class="sxs-lookup"><span data-stu-id="78e68-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="78e68-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="78e68-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="78e68-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="78e68-112">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="78e68-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="78e68-113">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="78e68-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="78e68-114">افترض أنك تحتاج إلى تخصيص تنسيق توفره Microsoft بإضافة بنود مع تفاصيل موجزة في نهاية تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="78e68-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="78e68-115">إنك تحتاج إلى القيام بذلك عن طريق اشتقاق مثيل خاص بك من تكوين نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي من مثيل Microsoft لإجراء التعديلات.</span><span class="sxs-lookup"><span data-stu-id="78e68-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="78e68-116">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="78e68-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="78e68-117">في الحقل "جديد"، أدخل "مشتق من اسم: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)، Microsoft".</span><span class="sxs-lookup"><span data-stu-id="78e68-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="78e68-118">في الحقل "الاسم"، اكتب "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="78e68-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="78e68-119">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="78e68-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="78e68-120">تكوين هذا التقرير للقيام بعمليات الجرد والتجميع‬ استنادًا إلى تفاصيل المخرجات</span><span class="sxs-lookup"><span data-stu-id="78e68-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="78e68-121">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="78e68-121">Click Designer.</span></span>
2. <span data-ttu-id="78e68-122">حدد "نعم" في حقل "تجميع تفاصيل المخرجات‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="78e68-123">ستقوم هذه العلامة في وقت التشغيل بتنشيط عملية تجميع تفاصيل المخرجات لإنشاء ملف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="78e68-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="78e68-124">إنك تحتاج إلى تنفيذ عملية جرد لمختلف اتجاهات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، ولذلك اعمل على إضافة تعداد نموذج مخصص إلى قائمة مصادر البيانات لتكوين التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="78e68-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="78e68-125">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="78e68-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="78e68-126">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="78e68-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="78e68-127">في الشجرة، حدد "نموذج البيانات\تعداد".</span><span class="sxs-lookup"><span data-stu-id="78e68-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="78e68-128">في حقل "الاسم"، اكتب "الاتجاه".</span><span class="sxs-lookup"><span data-stu-id="78e68-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="78e68-129">في الحقل "تعداد النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="78e68-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="78e68-130">حدد القيمة "الاتجاه".</span><span class="sxs-lookup"><span data-stu-id="78e68-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="78e68-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="78e68-131">Click OK.</span></span>
9. <span data-ttu-id="78e68-132">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="78e68-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="78e68-133">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="78e68-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="78e68-134">في حقل "الاسم"، اكتب "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="78e68-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="78e68-135">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="78e68-135">Click Edit formula.</span></span>
13. <span data-ttu-id="78e68-136">في حقل "المعادلة"، أدخل "الكتلة".</span><span class="sxs-lookup"><span data-stu-id="78e68-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="78e68-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-137">Click Save.</span></span>
15. <span data-ttu-id="78e68-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-138">Close the page.</span></span>
16. <span data-ttu-id="78e68-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="78e68-139">Click OK.</span></span>
17. <span data-ttu-id="78e68-140">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="78e68-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="78e68-141">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="78e68-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="78e68-142">في حقل "الاسم"، اكتب "$RecName".</span><span class="sxs-lookup"><span data-stu-id="78e68-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="78e68-143">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="78e68-143">Click Edit formula.</span></span>
21. <span data-ttu-id="78e68-144">في حقل "المعادلة"، أدخل "السجل".</span><span class="sxs-lookup"><span data-stu-id="78e68-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="78e68-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-145">Click Save.</span></span>
23. <span data-ttu-id="78e68-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-146">Close the page.</span></span>
24. <span data-ttu-id="78e68-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="78e68-147">Click OK.</span></span>
25. <span data-ttu-id="78e68-148">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="78e68-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="78e68-149">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="78e68-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="78e68-150">في حقل "الاسم"، اكتب "$InvName".</span><span class="sxs-lookup"><span data-stu-id="78e68-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="78e68-151">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="78e68-151">Click Edit formula.</span></span>
29. <span data-ttu-id="78e68-152">في حقل "المعادلة"، أدخل "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="78e68-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="78e68-153">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-153">Click Save.</span></span>
31. <span data-ttu-id="78e68-154">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-154">Close the page.</span></span>
32. <span data-ttu-id="78e68-155">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="78e68-155">Click OK.</span></span>
33. <span data-ttu-id="78e68-156">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات".</span><span class="sxs-lookup"><span data-stu-id="78e68-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="78e68-157">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬"</span><span class="sxs-lookup"><span data-stu-id="78e68-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="78e68-158">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="78e68-158">Click Add data source.</span></span>
    * <span data-ttu-id="78e68-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="78e68-159">$BlockName</span></span>  
36. <span data-ttu-id="78e68-160">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="78e68-160">Click Save.</span></span>
37. <span data-ttu-id="78e68-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-161">Close the page.</span></span>
38. <span data-ttu-id="78e68-162">انقر فوق الزر "تحرير" للحقل "قيمة مفتاح البيانات المجمعة‬‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="78e68-163">في حقل "المعادلة"، أدخل "r 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "استيراد"، "تصدير")'.</span><span class="sxs-lookup"><span data-stu-id="78e68-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="78e68-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "استيراد", "تصدير")</span><span class="sxs-lookup"><span data-stu-id="78e68-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="78e68-165">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-165">Click Save.</span></span>
41. <span data-ttu-id="78e68-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-166">Close the page.</span></span>
    * <span data-ttu-id="78e68-167">قم بعدّ الأسطر في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="78e68-167">Count the lines of this sequence.</span></span> <span data-ttu-id="78e68-168">سيتم استخدام النتائج مع الاسم "الكتلة" بشكل منفصل لاتجاهات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="78e68-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="78e68-169">سيتم استخدام القيمة "استيراد" لأية حركات تتعلق بعمليات الوصول لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="78e68-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="78e68-170">وسيتم استخدام القيمة "تصدير" لأية حركات تتعلق بعمليات إرسال لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="78e68-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="78e68-171">يمكنك اعتبار هذه النتائج وكأنها ورقة عمل Excel افتراضية.</span><span class="sxs-lookup"><span data-stu-id="78e68-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="78e68-172">بالنسبة إلى كل حركة، هناك صف حيث تتم تعبئة العمود الأول "الكتلة" بالقيم "استيراد" و"تصدير" وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="78e68-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="78e68-173">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل".</span><span class="sxs-lookup"><span data-stu-id="78e68-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="78e68-174">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الوصول؟".</span><span class="sxs-lookup"><span data-stu-id="78e68-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="78e68-175">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="78e68-176">قم بعدّ الأسطر في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="78e68-176">Count the lines of this sequence.</span></span> <span data-ttu-id="78e68-177">سوف تحفظ النتائج باستخدام الاسم "السجل".</span><span class="sxs-lookup"><span data-stu-id="78e68-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="78e68-178">في الشجرة، حدد "$RecName".</span><span class="sxs-lookup"><span data-stu-id="78e68-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="78e68-179">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="78e68-179">Click Add data source.</span></span>
47. <span data-ttu-id="78e68-180">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="78e68-180">Click Save.</span></span>
48. <span data-ttu-id="78e68-181">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-181">Close the page.</span></span>
49. <span data-ttu-id="78e68-182">انقر فوق الزر "تحرير" للحقل "قيمة مفتاح البيانات المجمعة‬‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="78e68-183">في حقل المعادلة، أدخل "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="78e68-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="78e68-184">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-184">Click Save.</span></span>
52. <span data-ttu-id="78e68-185">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-185">Close the page.</span></span>
    * <span data-ttu-id="78e68-186">قم بعدّ الأسطر في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="78e68-186">Count the lines of this sequence.</span></span> <span data-ttu-id="78e68-187">سيتم استخدام النتائج مع الاسم "السجل" بشكل منفصل لأكواد السلع.</span><span class="sxs-lookup"><span data-stu-id="78e68-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="78e68-188">يمكنك اعتبار هذه النتائج وكأنها ورقة عمل Excel افتراضية.</span><span class="sxs-lookup"><span data-stu-id="78e68-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="78e68-189">بالنسبة إلى كل حركة، هناك صف حيث تتم تعبئة العمود الأول "الكتلة" بالقيم "استيراد" و"تصدير" وفقًا لذلك، وتتم تعبئة الكتلة الثانية "السجل" بواسطة قيمة كود السلعة.</span><span class="sxs-lookup"><span data-stu-id="78e68-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="78e68-190">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الإرسال؟".</span><span class="sxs-lookup"><span data-stu-id="78e68-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="78e68-191">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬"</span><span class="sxs-lookup"><span data-stu-id="78e68-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="78e68-192">في الشجرة، حدد "$RecName".</span><span class="sxs-lookup"><span data-stu-id="78e68-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="78e68-193">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="78e68-193">Click Add data source.</span></span>
57. <span data-ttu-id="78e68-194">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="78e68-194">Click Save.</span></span>
58. <span data-ttu-id="78e68-195">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-195">Close the page.</span></span>
59. <span data-ttu-id="78e68-196">انقر فوق الزر "تحرير" للحقل "قيمة مفتاح البيانات المجمعة‬‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="78e68-197">في حقل المعادلة، أدخل "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="78e68-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="78e68-198">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="78e68-198">Click Save.</span></span>
62. <span data-ttu-id="78e68-199">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-199">Close the page.</span></span>
63. <span data-ttu-id="78e68-200">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الإرسال: التسلسل؟".</span><span class="sxs-lookup"><span data-stu-id="78e68-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="78e68-201">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الإرسال: التسلسل?\السجل = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="78e68-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="78e68-202">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="78e68-202">Click the Format tab.</span></span>
66. <span data-ttu-id="78e68-203">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الإرسال\السجل\مبلغ الفاتورة EUR".</span><span class="sxs-lookup"><span data-stu-id="78e68-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="78e68-204">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="78e68-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="78e68-205">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="78e68-206">في الشجرة، حدد "$InvName'".</span><span class="sxs-lookup"><span data-stu-id="78e68-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="78e68-207">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="78e68-207">Click Add data source.</span></span>
71. <span data-ttu-id="78e68-208">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-208">Click Save.</span></span>
72. <span data-ttu-id="78e68-209">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-209">Close the page.</span></span>
    * <span data-ttu-id="78e68-210">قم بتلخيص قيم المبلغ المفوتر لبنود هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="78e68-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="78e68-211">سيتم استخدام النتائج مع الاسم "InvoicedAmountEUR" بشكل منفصل لاتجاهات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي وأكواد السلع.</span><span class="sxs-lookup"><span data-stu-id="78e68-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="78e68-212">يمكنك اعتبار هذه النتائج وكأنها عبارة عن عملية إنشاء افتراضية في ورقة عمل Excel.</span><span class="sxs-lookup"><span data-stu-id="78e68-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="78e68-213">بالنسبة إلى كل حركة، هناك صف حيث تتم تعبئة العمود الأول "الكتلة" بالقيم "استيراد" و"تصدير" وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="78e68-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="78e68-214">تتم تعبئة الكتلة الثانية "السجل" بقيمة كود السلعة، وتتم تعبئة العمود الثالث "InvoicedAmountEUR" بقيمة مبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="78e68-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="78e68-215">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الوصول?".</span><span class="sxs-lookup"><span data-stu-id="78e68-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="78e68-216">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الوصول?\السجل = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="78e68-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="78e68-217">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="78e68-217">Click the Format tab.</span></span>
76. <span data-ttu-id="78e68-218">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الإرسال\السجل\مبلغ الفاتورة EUR".</span><span class="sxs-lookup"><span data-stu-id="78e68-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="78e68-219">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="78e68-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="78e68-220">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬".</span><span class="sxs-lookup"><span data-stu-id="78e68-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="78e68-221">في الشجرة، حدد "$InvName'".</span><span class="sxs-lookup"><span data-stu-id="78e68-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="78e68-222">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="78e68-222">Click Add data source.</span></span>
81. <span data-ttu-id="78e68-223">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-223">Click Save.</span></span>
82. <span data-ttu-id="78e68-224">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-224">Close the page.</span></span>
83. <span data-ttu-id="78e68-225">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="78e68-225">Click Save.</span></span>
84. <span data-ttu-id="78e68-226">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="78e68-226">Close the page.</span></span>

