---
title: التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 4 - تشغيل التنسيق)
description: يصف هذا الموضوع كيفيه تكوين تنسيق التقارير الكتروني للقيام بالجرد والجمع استنادا إلى البيانات الخاصة بإخراج النص الذي تم إنشاؤه بالفعل. (جزء 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5792505de78aad458bd8745630915cf58f05f73f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748963"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="a6ff9-104">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 4 - تشغيل التنسيق)</span><span class="sxs-lookup"><span data-stu-id="a6ff9-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6ff9-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a6ff9-106">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a6ff9-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 3: استخدام العمليات الحسابية لإنشاء المخرجات)".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="a6ff9-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="a6ff9-109">اختبار هذا التكوين لإنشاء تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="a6ff9-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="a6ff9-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a6ff9-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a6ff9-112">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="a6ff9-113">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="a6ff9-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="a6ff9-114">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="a6ff9-115">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="a6ff9-116">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-116">Click User parameters.</span></span>
8. <span data-ttu-id="a6ff9-117">حدد "نعم" في حقل "تشغيل الإعدادات".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="a6ff9-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-118">Click OK.</span></span>
10. <span data-ttu-id="a6ff9-119">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-119">Click Edit.</span></span>
11. <span data-ttu-id="a6ff9-120">حدد "نعم" في حقل "تشغيل المسودة‬".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="a6ff9-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-121">Click Save.</span></span>
13. <span data-ttu-id="a6ff9-122">انتقل إلى الضريبة > الإعداد > التجارة الخارجية > معلمات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="a6ff9-123">قم بتوسيع القسم "إعداد التقارير الإلكترونية".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="a6ff9-124">حدد التكوين "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والجمع".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="a6ff9-125">حدد التكوين "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والجمع".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="a6ff9-126">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-126">Click Save.</span></span>
18. <span data-ttu-id="a6ff9-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-127">Close the page.</span></span>
19. <span data-ttu-id="a6ff9-128">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="a6ff9-129">انقر فوق "الإخراج".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-129">Click Output.</span></span>
21. <span data-ttu-id="a6ff9-130">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-130">Click Report.</span></span>
    * <span data-ttu-id="a6ff9-131">شغّل عملية إنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="a6ff9-132">في الحقل "من تاريخ"، قم بتعيين التاريخ على "2000/01/01".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="a6ff9-133">حدد تاريخي البدء والانتهاء لفترة إعداد التقارير التي تشتمل على تلك الموجودة على حركات النموذج.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="a6ff9-134">في الحقل "إلى تاريخ"، قم بتعيين التاريخ على "2022/12/31".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="a6ff9-135">حدد تاريخي البدء والانتهاء لفترة إعداد التقارير التي تشتمل على تلك الموجودة على حركات النموذج.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="a6ff9-136">في الحقل "اتجاه"، حدد "حركات الوصول".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="a6ff9-137">حدد "نعم" في الحقل "إنشاء ملف".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="a6ff9-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-138">Click OK.</span></span>
    * <span data-ttu-id="a6ff9-139">راجع المخرجات المُنشأة مع بنود الملخص في النهاية.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="a6ff9-140">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-140">Click New.</span></span>
28. <span data-ttu-id="a6ff9-141">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="a6ff9-142">في الحقل "اتجاه"، حدد "حركات الإرسال".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="a6ff9-143">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="a6ff9-144">في الحقل "السلعة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="a6ff9-145">عيّن "الوزن" إلى"10".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="a6ff9-146">عيّن "مبلغ الفاتورة" إلى "10000".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="a6ff9-147">عيّن "المبلغ الإحصائي‬" إلى "10000".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="a6ff9-148">انقر فوق "الإخراج".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-148">Click Output.</span></span>
36. <span data-ttu-id="a6ff9-149">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-149">Click Report.</span></span>
37. <span data-ttu-id="a6ff9-150">في الحقل "اتجاه"، حدد "حركات الإرسال".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="a6ff9-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-151">Click OK.</span></span>
    * <span data-ttu-id="a6ff9-152">راجع المخرجات المُنشأة مع بنود الملخص في النهاية.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="a6ff9-153">لاحظ أنه تم تغييرها بالمقارنة مع التشغيل الأول.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="a6ff9-154">تشغيل هذا التكوين في وضع التصحيح لمراجعة بيانات الجرد والجمع المجمّعة</span><span class="sxs-lookup"><span data-stu-id="a6ff9-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="a6ff9-155">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a6ff9-156">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="a6ff9-157">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="a6ff9-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="a6ff9-158">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="a6ff9-159">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="a6ff9-160">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-160">Click User parameters.</span></span>
7. <span data-ttu-id="a6ff9-161">حدد "نعم" في الحقل "تشغيل في وضع التصحيح‬".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="a6ff9-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-162">Click OK.</span></span>
9. <span data-ttu-id="a6ff9-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-163">Close the page.</span></span>
10. <span data-ttu-id="a6ff9-164">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="a6ff9-165">انقر فوق "الإخراج".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-165">Click Output.</span></span>
12. <span data-ttu-id="a6ff9-166">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-166">Click Report.</span></span>
13. <span data-ttu-id="a6ff9-167">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-167">Click OK.</span></span>
14. <span data-ttu-id="a6ff9-168">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-168">Close the page.</span></span>
15. <span data-ttu-id="a6ff9-169">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="a6ff9-170">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="a6ff9-171">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="a6ff9-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="a6ff9-172">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="a6ff9-173">انقر فوق "سجلات التصحيح‬".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-173">Click Debug logs.</span></span>
    * <span data-ttu-id="a6ff9-174">لاحظ أنه قد تم إنشاء سجل تصحيح لعملية تنفيذ التكوين الذي تم تحديده.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="a6ff9-175">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-175">Click Attach.</span></span>
21. <span data-ttu-id="a6ff9-176">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="a6ff9-176">Click Open.</span></span>
    * <span data-ttu-id="a6ff9-177">راجع ملف XML المُنشأ الذي يحتوي على تفاصيل الجرد والتجميع التي تم جمعها أثناء تنفيذ التكوين الذي تم تحديده.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]