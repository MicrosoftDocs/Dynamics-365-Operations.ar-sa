--- 
title: "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 4 - تشغيل التنسيق)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a><span data-ttu-id="61278-103">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 4: تشغيل التنسيق)</span><span class="sxs-lookup"><span data-stu-id="61278-103">ER Configure format to do counting and summing (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61278-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="61278-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="61278-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="61278-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="61278-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 3: استخدام العمليات الحسابية لإنشاء المخرجات)".</span><span class="sxs-lookup"><span data-stu-id="61278-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="61278-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="61278-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="61278-108">اختبار هذا التكوين لإنشاء تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="61278-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="61278-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="61278-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="61278-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="61278-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="61278-111">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="61278-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="61278-112">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="61278-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="61278-113">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="61278-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="61278-114">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="61278-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="61278-115">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="61278-115">Click User parameters.</span></span>
8. <span data-ttu-id="61278-116">حدد "نعم" في حقل "تشغيل الإعدادات".</span><span class="sxs-lookup"><span data-stu-id="61278-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="61278-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="61278-117">Click OK.</span></span>
10. <span data-ttu-id="61278-118">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="61278-118">Click Edit.</span></span>
11. <span data-ttu-id="61278-119">حدد "نعم" في حقل "تشغيل المسودة‬".</span><span class="sxs-lookup"><span data-stu-id="61278-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="61278-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="61278-120">Click Save.</span></span>
13. <span data-ttu-id="61278-121">انتقل إلى الضريبة > الإعداد > التجارة الخارجية > معلمات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="61278-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="61278-122">قم بتوسيع القسم "إعداد التقارير الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="61278-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="61278-123">حدد التكوين "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والجمع".</span><span class="sxs-lookup"><span data-stu-id="61278-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="61278-124">حدد التكوين "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والجمع".</span><span class="sxs-lookup"><span data-stu-id="61278-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="61278-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="61278-125">Click Save.</span></span>
18. <span data-ttu-id="61278-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="61278-126">Close the page.</span></span>
19. <span data-ttu-id="61278-127">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="61278-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="61278-128">انقر فوق "الإخراج".</span><span class="sxs-lookup"><span data-stu-id="61278-128">Click Output.</span></span>
21. <span data-ttu-id="61278-129">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="61278-129">Click Report.</span></span>
    * <span data-ttu-id="61278-130">شغّل عملية إنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="61278-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="61278-131">في الحقل "من تاريخ"، قم بتعيين التاريخ على "2000/01/01".</span><span class="sxs-lookup"><span data-stu-id="61278-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="61278-132">حدد تاريخي البدء والانتهاء لفترة إعداد التقارير التي تشتمل على تلك الموجودة على حركات النموذج.</span><span class="sxs-lookup"><span data-stu-id="61278-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="61278-133">في الحقل "إلى تاريخ"، قم بتعيين التاريخ على "2022/12/31".</span><span class="sxs-lookup"><span data-stu-id="61278-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="61278-134">حدد تاريخي البدء والانتهاء لفترة إعداد التقارير التي تشتمل على تلك الموجودة على حركات النموذج.</span><span class="sxs-lookup"><span data-stu-id="61278-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="61278-135">في الحقل "اتجاه"، حدد "حركات الوصول".</span><span class="sxs-lookup"><span data-stu-id="61278-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="61278-136">حدد "نعم" في الحقل "إنشاء ملف".</span><span class="sxs-lookup"><span data-stu-id="61278-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="61278-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="61278-137">Click OK.</span></span>
    * <span data-ttu-id="61278-138">راجع المخرجات المُنشأة مع بنود الملخص في النهاية.</span><span class="sxs-lookup"><span data-stu-id="61278-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="61278-139">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="61278-139">Click New.</span></span>
28. <span data-ttu-id="61278-140">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="61278-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="61278-141">في الحقل "اتجاه"، حدد "حركات الإرسال".</span><span class="sxs-lookup"><span data-stu-id="61278-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="61278-142">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="61278-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="61278-143">في الحقل "السلعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="61278-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="61278-144">عيّن "الوزن" إلى"10".</span><span class="sxs-lookup"><span data-stu-id="61278-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="61278-145">عيّن "مبلغ الفاتورة" إلى "10000".</span><span class="sxs-lookup"><span data-stu-id="61278-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="61278-146">عيّن "المبلغ الإحصائي‬" إلى "10000".</span><span class="sxs-lookup"><span data-stu-id="61278-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="61278-147">انقر فوق "الإخراج".</span><span class="sxs-lookup"><span data-stu-id="61278-147">Click Output.</span></span>
36. <span data-ttu-id="61278-148">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="61278-148">Click Report.</span></span>
37. <span data-ttu-id="61278-149">في الحقل "اتجاه"، حدد "حركات الإرسال".</span><span class="sxs-lookup"><span data-stu-id="61278-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="61278-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="61278-150">Click OK.</span></span>
    * <span data-ttu-id="61278-151">راجع المخرجات المُنشأة مع بنود الملخص في النهاية.</span><span class="sxs-lookup"><span data-stu-id="61278-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="61278-152">لاحظ أنه تم تغييرها بالمقارنة مع التشغيل الأول.</span><span class="sxs-lookup"><span data-stu-id="61278-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="61278-153">تشغيل هذا التكوين في وضع التصحيح لمراجعة بيانات الجرد والجمع المجمّعة</span><span class="sxs-lookup"><span data-stu-id="61278-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="61278-154">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="61278-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="61278-155">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="61278-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="61278-156">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="61278-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="61278-157">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="61278-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="61278-158">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="61278-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="61278-159">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="61278-159">Click User parameters.</span></span>
7. <span data-ttu-id="61278-160">حدد "نعم" في الحقل "تشغيل في وضع التصحيح‬".</span><span class="sxs-lookup"><span data-stu-id="61278-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="61278-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="61278-161">Click OK.</span></span>
9. <span data-ttu-id="61278-162">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="61278-162">Close the page.</span></span>
10. <span data-ttu-id="61278-163">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="61278-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="61278-164">انقر فوق "الإخراج".</span><span class="sxs-lookup"><span data-stu-id="61278-164">Click Output.</span></span>
12. <span data-ttu-id="61278-165">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="61278-165">Click Report.</span></span>
13. <span data-ttu-id="61278-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="61278-166">Click OK.</span></span>
14. <span data-ttu-id="61278-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="61278-167">Close the page.</span></span>
15. <span data-ttu-id="61278-168">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="61278-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="61278-169">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="61278-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="61278-170">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="61278-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="61278-171">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="61278-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="61278-172">انقر فوق "سجلات التصحيح‬".</span><span class="sxs-lookup"><span data-stu-id="61278-172">Click Debug logs.</span></span>
    * <span data-ttu-id="61278-173">لاحظ أنه قد تم إنشاء سجل تصحيح لعملية تنفيذ التكوين الذي تم تحديده.</span><span class="sxs-lookup"><span data-stu-id="61278-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="61278-174">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="61278-174">Click Attach.</span></span>
21. <span data-ttu-id="61278-175">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="61278-175">Click Open.</span></span>
    * <span data-ttu-id="61278-176">راجع ملف XML المُنشأ الذي يحتوي على تفاصيل الجرد والتجميع التي تم جمعها أثناء تنفيذ التكوين الذي تم تحديده.</span><span class="sxs-lookup"><span data-stu-id="61278-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


