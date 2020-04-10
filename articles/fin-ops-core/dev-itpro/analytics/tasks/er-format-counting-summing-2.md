---
title: التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 2 - تكوين العمليات الحسابية)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20188438a4ca623fc926e6c373fb002f148c3df4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142468"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="842c7-103">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 2 - تكوين العمليات الحسابية)</span><span class="sxs-lookup"><span data-stu-id="842c7-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="842c7-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="842c7-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="842c7-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="842c7-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="842c7-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 1: إنشاء التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="842c7-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="842c7-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="842c7-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="842c7-108">إنشاء تكوين تنسيق لإضافة تفاصيل الجرد والتجميع‬</span><span class="sxs-lookup"><span data-stu-id="842c7-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="842c7-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="842c7-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="842c7-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="842c7-111">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="842c7-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="842c7-112">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="842c7-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="842c7-113">افترض أنك تحتاج إلى تخصيص تنسيق توفره Microsoft بإضافة بنود مع تفاصيل موجزة في نهاية تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="842c7-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="842c7-114">إنك تحتاج إلى القيام بذلك عن طريق اشتقاق مثيل خاص بك من تكوين نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي من مثيل Microsoft لإجراء التعديلات.</span><span class="sxs-lookup"><span data-stu-id="842c7-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="842c7-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="842c7-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="842c7-116">في الحقل "جديد"، أدخل "مشتق من اسم: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)، Microsoft".</span><span class="sxs-lookup"><span data-stu-id="842c7-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="842c7-117">في الحقل "الاسم"، اكتب "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="842c7-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="842c7-118">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="842c7-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="842c7-119">تكوين هذا التقرير للقيام بعمليات الجرد والتجميع‬ استنادًا إلى تفاصيل المخرجات</span><span class="sxs-lookup"><span data-stu-id="842c7-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="842c7-120">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="842c7-120">Click Designer.</span></span>
2. <span data-ttu-id="842c7-121">حدد "نعم" في حقل "تجميع تفاصيل المخرجات‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="842c7-122">ستقوم هذه العلامة في وقت التشغيل بتنشيط عملية تجميع تفاصيل المخرجات لإنشاء ملف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="842c7-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="842c7-123">إنك تحتاج إلى تنفيذ عملية جرد لمختلف اتجاهات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، ولذلك اعمل على إضافة تعداد نموذج مخصص إلى قائمة مصادر البيانات لتكوين التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="842c7-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="842c7-124">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="842c7-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="842c7-125">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="842c7-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="842c7-126">في الشجرة، حدد "نموذج البيانات\تعداد".</span><span class="sxs-lookup"><span data-stu-id="842c7-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="842c7-127">في حقل "الاسم"، اكتب "الاتجاه".</span><span class="sxs-lookup"><span data-stu-id="842c7-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="842c7-128">في الحقل "تعداد النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="842c7-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="842c7-129">حدد القيمة "الاتجاه".</span><span class="sxs-lookup"><span data-stu-id="842c7-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="842c7-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="842c7-130">Click OK.</span></span>
9. <span data-ttu-id="842c7-131">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="842c7-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="842c7-132">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="842c7-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="842c7-133">في حقل "الاسم"، اكتب "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="842c7-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="842c7-134">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="842c7-134">Click Edit formula.</span></span>
13. <span data-ttu-id="842c7-135">في حقل "المعادلة"، أدخل "الكتلة".</span><span class="sxs-lookup"><span data-stu-id="842c7-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="842c7-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-136">Click Save.</span></span>
15. <span data-ttu-id="842c7-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-137">Close the page.</span></span>
16. <span data-ttu-id="842c7-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="842c7-138">Click OK.</span></span>
17. <span data-ttu-id="842c7-139">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="842c7-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="842c7-140">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="842c7-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="842c7-141">في حقل "الاسم"، اكتب "$RecName".</span><span class="sxs-lookup"><span data-stu-id="842c7-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="842c7-142">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="842c7-142">Click Edit formula.</span></span>
21. <span data-ttu-id="842c7-143">في حقل "المعادلة"، أدخل "السجل".</span><span class="sxs-lookup"><span data-stu-id="842c7-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="842c7-144">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-144">Click Save.</span></span>
23. <span data-ttu-id="842c7-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-145">Close the page.</span></span>
24. <span data-ttu-id="842c7-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="842c7-146">Click OK.</span></span>
25. <span data-ttu-id="842c7-147">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="842c7-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="842c7-148">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="842c7-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="842c7-149">في حقل "الاسم"، اكتب "$InvName".</span><span class="sxs-lookup"><span data-stu-id="842c7-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="842c7-150">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="842c7-150">Click Edit formula.</span></span>
29. <span data-ttu-id="842c7-151">في حقل "المعادلة"، أدخل "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="842c7-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="842c7-152">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-152">Click Save.</span></span>
31. <span data-ttu-id="842c7-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-153">Close the page.</span></span>
32. <span data-ttu-id="842c7-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="842c7-154">Click OK.</span></span>
33. <span data-ttu-id="842c7-155">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات".</span><span class="sxs-lookup"><span data-stu-id="842c7-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="842c7-156">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬"</span><span class="sxs-lookup"><span data-stu-id="842c7-156">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="842c7-157">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="842c7-157">Click Add data source.</span></span>
    * <span data-ttu-id="842c7-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="842c7-158">$BlockName</span></span>  
36. <span data-ttu-id="842c7-159">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="842c7-159">Click Save.</span></span>
37. <span data-ttu-id="842c7-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-160">Close the page.</span></span>
38. <span data-ttu-id="842c7-161">انقر فوق الزر "تحرير" للحقل "قيمة مفتاح البيانات المجمعة‬‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="842c7-162">في حقل "المعادلة"، أدخل "r 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "استيراد"، "تصدير")'.</span><span class="sxs-lookup"><span data-stu-id="842c7-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="842c7-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "استيراد", "تصدير")</span><span class="sxs-lookup"><span data-stu-id="842c7-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="842c7-164">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-164">Click Save.</span></span>
41. <span data-ttu-id="842c7-165">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-165">Close the page.</span></span>
    * <span data-ttu-id="842c7-166">قم بعدّ الأسطر في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="842c7-166">Count the lines of this sequence.</span></span> <span data-ttu-id="842c7-167">سيتم استخدام النتائج مع الاسم "الكتلة" بشكل منفصل لاتجاهات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="842c7-167">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="842c7-168">سيتم استخدام القيمة "استيراد" لأية حركات تتعلق بعمليات الوصول لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="842c7-168">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="842c7-169">وسيتم استخدام القيمة "تصدير" لأية حركات تتعلق بعمليات إرسال لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="842c7-169">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="842c7-170">يمكنك اعتبار هذه النتائج وكأنها ورقة عمل Excel افتراضية.</span><span class="sxs-lookup"><span data-stu-id="842c7-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="842c7-171">بالنسبة إلى كل حركة، هناك صف حيث تتم تعبئة العمود الأول "الكتلة" بالقيم "استيراد" و"تصدير" وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="842c7-171">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="842c7-172">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل".</span><span class="sxs-lookup"><span data-stu-id="842c7-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="842c7-173">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الوصول؟".</span><span class="sxs-lookup"><span data-stu-id="842c7-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="842c7-174">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-174">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="842c7-175">قم بعدّ الأسطر في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="842c7-175">Count the lines of this sequence.</span></span> <span data-ttu-id="842c7-176">سوف تحفظ النتائج باستخدام الاسم "السجل".</span><span class="sxs-lookup"><span data-stu-id="842c7-176">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="842c7-177">في الشجرة، حدد "$RecName".</span><span class="sxs-lookup"><span data-stu-id="842c7-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="842c7-178">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="842c7-178">Click Add data source.</span></span>
47. <span data-ttu-id="842c7-179">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="842c7-179">Click Save.</span></span>
48. <span data-ttu-id="842c7-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-180">Close the page.</span></span>
49. <span data-ttu-id="842c7-181">انقر فوق الزر "تحرير" للحقل "قيمة مفتاح البيانات المجمعة‬‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-181">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="842c7-182">في حقل المعادلة، أدخل "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="842c7-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="842c7-183">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-183">Click Save.</span></span>
52. <span data-ttu-id="842c7-184">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-184">Close the page.</span></span>
    * <span data-ttu-id="842c7-185">قم بعدّ الأسطر في هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="842c7-185">Count the lines of this sequence.</span></span> <span data-ttu-id="842c7-186">سيتم استخدام النتائج مع الاسم "السجل" بشكل منفصل لأكواد السلع.</span><span class="sxs-lookup"><span data-stu-id="842c7-186">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="842c7-187">يمكنك اعتبار هذه النتائج وكأنها ورقة عمل Excel افتراضية.</span><span class="sxs-lookup"><span data-stu-id="842c7-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="842c7-188">بالنسبة إلى كل حركة، هناك صف حيث تتم تعبئة العمود الأول "الكتلة" بالقيم "استيراد" و"تصدير" وفقًا لذلك، وتتم تعبئة الكتلة الثانية "السجل" بواسطة قيمة كود السلعة.</span><span class="sxs-lookup"><span data-stu-id="842c7-188">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="842c7-189">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الإرسال؟".</span><span class="sxs-lookup"><span data-stu-id="842c7-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="842c7-190">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬"</span><span class="sxs-lookup"><span data-stu-id="842c7-190">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="842c7-191">في الشجرة، حدد "$RecName".</span><span class="sxs-lookup"><span data-stu-id="842c7-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="842c7-192">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="842c7-192">Click Add data source.</span></span>
57. <span data-ttu-id="842c7-193">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="842c7-193">Click Save.</span></span>
58. <span data-ttu-id="842c7-194">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-194">Close the page.</span></span>
59. <span data-ttu-id="842c7-195">انقر فوق الزر "تحرير" للحقل "قيمة مفتاح البيانات المجمعة‬‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-195">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="842c7-196">في حقل المعادلة، أدخل "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="842c7-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="842c7-197">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="842c7-197">Click Save.</span></span>
62. <span data-ttu-id="842c7-198">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-198">Close the page.</span></span>
63. <span data-ttu-id="842c7-199">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الإرسال: التسلسل؟".</span><span class="sxs-lookup"><span data-stu-id="842c7-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="842c7-200">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات: التسلسل\حركات الإرسال: التسلسل?\السجل = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="842c7-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="842c7-201">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="842c7-201">Click the Format tab.</span></span>
66. <span data-ttu-id="842c7-202">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الإرسال\السجل\مبلغ الفاتورة EUR".</span><span class="sxs-lookup"><span data-stu-id="842c7-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="842c7-203">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="842c7-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="842c7-204">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-204">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="842c7-205">في الشجرة، حدد "$InvName'".</span><span class="sxs-lookup"><span data-stu-id="842c7-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="842c7-206">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="842c7-206">Click Add data source.</span></span>
71. <span data-ttu-id="842c7-207">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-207">Click Save.</span></span>
72. <span data-ttu-id="842c7-208">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-208">Close the page.</span></span>
    * <span data-ttu-id="842c7-209">قم بتلخيص قيم المبلغ المفوتر لبنود هذا التسلسل.</span><span class="sxs-lookup"><span data-stu-id="842c7-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="842c7-210">سيتم استخدام النتائج مع الاسم "InvoicedAmountEUR" بشكل منفصل لاتجاهات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي وأكواد السلع.</span><span class="sxs-lookup"><span data-stu-id="842c7-210">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="842c7-211">يمكنك اعتبار هذه النتائج وكأنها عبارة عن عملية إنشاء افتراضية في ورقة عمل Excel.</span><span class="sxs-lookup"><span data-stu-id="842c7-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="842c7-212">بالنسبة إلى كل حركة، هناك صف حيث تتم تعبئة العمود الأول "الكتلة" بالقيم "استيراد" و"تصدير" وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="842c7-212">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="842c7-213">تتم تعبئة الكتلة الثانية "السجل" بقيمة كود السلعة، وتتم تعبئة العمود الثالث "InvoicedAmountEUR" بقيمة مبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="842c7-213">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="842c7-214">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الوصول?".</span><span class="sxs-lookup"><span data-stu-id="842c7-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="842c7-215">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الوصول?\السجل = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="842c7-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="842c7-216">انقر فوق علامة التبويب "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="842c7-216">Click the Format tab.</span></span>
76. <span data-ttu-id="842c7-217">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\البيانات\حركات الإرسال\السجل\مبلغ الفاتورة EUR".</span><span class="sxs-lookup"><span data-stu-id="842c7-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="842c7-218">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="842c7-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="842c7-219">انقر فوق الزر "تحرير" للحقل "اسم مفتاح البيانات المجمعة‬".</span><span class="sxs-lookup"><span data-stu-id="842c7-219">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="842c7-220">في الشجرة، حدد "$InvName'".</span><span class="sxs-lookup"><span data-stu-id="842c7-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="842c7-221">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="842c7-221">Click Add data source.</span></span>
81. <span data-ttu-id="842c7-222">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-222">Click Save.</span></span>
82. <span data-ttu-id="842c7-223">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-223">Close the page.</span></span>
83. <span data-ttu-id="842c7-224">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="842c7-224">Click Save.</span></span>
84. <span data-ttu-id="842c7-225">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="842c7-225">Close the page.</span></span>

