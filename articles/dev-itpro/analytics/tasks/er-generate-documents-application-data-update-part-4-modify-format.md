--- 
title: "تعديل التنسيق لإنشاء مستندات بواسطة بيانات التطبيق"
description: "لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، \"التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 3 - تعديل النموذج والتعيين)‬\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7923c958b3a1063c505e5bd263ec042d86165f07
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="modify-format-to-generate-documents-with-application-data"></a><span data-ttu-id="5dac5-103">تعديل التنسيق لإنشاء مستندات بواسطة بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="5dac5-103">Modify format to generate documents with application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dac5-104">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 3: تعديل النموذج والتعيين)‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 3: Modify model and mapping)".</span></span>

<span data-ttu-id="5dac5-105">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="5dac5-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="5dac5-106">في هذا الإجراء، ستقوم بتعديل تكوينات التقارير الإلكترونية ليس فقط لاستخدامها لإنشاء المستندات الإلكترونية، بل أيضًا لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="5dac5-106">In this procedure, you will modify the ER configurations to not just use them to generate electronic documents, but also to update application data.</span></span> <span data-ttu-id="5dac5-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5dac5-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="5dac5-108">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="5dac5-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-format-to-collect-details-of-reporting"></a><span data-ttu-id="5dac5-109">تعديل التنسيق لجمع تفاصيل إعداد التقارير</span><span class="sxs-lookup"><span data-stu-id="5dac5-109">Modify format to collect details of reporting</span></span>
1. <span data-ttu-id="5dac5-110">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="5dac5-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5dac5-111">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-111">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="5dac5-112">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تنسيق)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-112">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="5dac5-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="5dac5-113">Click Designer.</span></span>
5. <span data-ttu-id="5dac5-114">في الشجرة، قم بتوسيع "ملف"</span><span class="sxs-lookup"><span data-stu-id="5dac5-114">In the tree, expand 'File'.</span></span>
6. <span data-ttu-id="5dac5-115">في الشجرة، قم بتوسيع "ملف\إقرار".</span><span class="sxs-lookup"><span data-stu-id="5dac5-115">In the tree, expand 'File\Declaration'.</span></span>
7. <span data-ttu-id="5dac5-116">في الشجرة، حدد "ملف\إقرار\بيانات".</span><span class="sxs-lookup"><span data-stu-id="5dac5-116">In the tree, select 'File\Declaration\Data'.</span></span>
8. <span data-ttu-id="5dac5-117">في حقل "التعدد"، حدد "واحد كثير‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-117">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="5dac5-118">قم بتكوين عنصر التنسيق هذا لأرشفة التفاصيل الخاصة بعملية إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="5dac5-118">Configure this format element to archive details of the Intrastat reporting process.</span></span> <span data-ttu-id="5dac5-119">يمثل هذا العنصر سجل رأس الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="5dac5-119">This item represents the archive’s header record.</span></span>  
9. <span data-ttu-id="5dac5-120">في الشجرة، قم بتوسيع "ملف\إقرار\بيانات".</span><span class="sxs-lookup"><span data-stu-id="5dac5-120">In the tree, expand 'File\Declaration\Data'.</span></span>
10. <span data-ttu-id="5dac5-121">في الشجرة، حدد "ملف\إقرار\بيانات\صنف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-121">In the tree, select 'File\Declaration\Data\Item'.</span></span>
11. <span data-ttu-id="5dac5-122">في حقل "التعدد"، حدد "صفر كثير‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-122">In the Multiplicity field, select 'Zero many'.</span></span>
    * <span data-ttu-id="5dac5-123">قم بتكوين عنصر التنسيق هذا لأرشفة التفاصيل الخاصة بعملية إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="5dac5-123">Configure this format element to archive details of the Intrastat reporting process.</span></span> <span data-ttu-id="5dac5-124">سيمثل هذا العنصر قائمة بالبنود المؤرشفة.</span><span class="sxs-lookup"><span data-stu-id="5dac5-124">This item will represent the list of archived lines.</span></span>  
12. <span data-ttu-id="5dac5-125">في الشجرة، قم بتوسيع "ملف\إقرار\بيانات\صنف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-125">In the tree, expand 'File\Declaration\Data\Item'.</span></span>
13. <span data-ttu-id="5dac5-126">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim1".</span><span class="sxs-lookup"><span data-stu-id="5dac5-126">In the tree, select 'File\Declaration\Data\Item\Dim1'.</span></span>
14. <span data-ttu-id="5dac5-127">حدد "نعم" في الحقل "مستبعد‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-127">Select Yes in the Excluded field.</span></span>
    * <span data-ttu-id="5dac5-128">لن تقوم بأرشفة هذه البيانات، لذا يمكنك استبعاد عنصر التنسيق هذا من مصدر البيانات الخاص بتفاصيل إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="5dac5-128">You will not archive this data, so you can exclude this format element from the data source of Intrastat reporting details.</span></span>  
15. <span data-ttu-id="5dac5-129">في الشجرة، قم بتوسيع "ملف\إقرار\بيانات\صنف\Dim1".</span><span class="sxs-lookup"><span data-stu-id="5dac5-129">In the tree, expand 'File\Declaration\Data\Item\Dim1'.</span></span>
16. <span data-ttu-id="5dac5-130">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim1\خاصية".</span><span class="sxs-lookup"><span data-stu-id="5dac5-130">In the tree, select 'File\Declaration\Data\Item\Dim1\property'.</span></span>
17. <span data-ttu-id="5dac5-131">حدد "نعم" في الحقل "مستبعد‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-131">Select Yes in the Excluded field.</span></span>
18. <span data-ttu-id="5dac5-132">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim1\تاريخ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-132">In the tree, select 'File\Declaration\Data\Item\Dim1\date'.</span></span>
19. <span data-ttu-id="5dac5-133">حدد "نعم" في الحقل "مستبعد‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-133">Select Yes in the Excluded field.</span></span>
20. <span data-ttu-id="5dac5-134">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim2".</span><span class="sxs-lookup"><span data-stu-id="5dac5-134">In the tree, select 'File\Declaration\Data\Item\Dim2'.</span></span>
21. <span data-ttu-id="5dac5-135">حدد "نعم" في الحقل "مستبعد‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-135">Select Yes in the Excluded field.</span></span>
22. <span data-ttu-id="5dac5-136">في الشجرة، قم بتوسيع "ملف\إقرار\بيانات\صنف\Dim2".</span><span class="sxs-lookup"><span data-stu-id="5dac5-136">In the tree, expand 'File\Declaration\Data\Item\Dim2'.</span></span>
23. <span data-ttu-id="5dac5-137">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim2\خاصية".</span><span class="sxs-lookup"><span data-stu-id="5dac5-137">In the tree, select 'File\Declaration\Data\Item\Dim2\property'.</span></span>
24. <span data-ttu-id="5dac5-138">حدد "نعم" في الحقل "مستبعد‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-138">Select Yes in the Excluded field.</span></span>
25. <span data-ttu-id="5dac5-139">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim2\كود".</span><span class="sxs-lookup"><span data-stu-id="5dac5-139">In the tree, select 'File\Declaration\Data\Item\Dim2\code'.</span></span>
26. <span data-ttu-id="5dac5-140">حدد "نعم" في الحقل "مستبعد‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-140">Select Yes in the Excluded field.</span></span>
27. <span data-ttu-id="5dac5-141">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim3".</span><span class="sxs-lookup"><span data-stu-id="5dac5-141">In the tree, select 'File\Declaration\Data\Item\Dim3'.</span></span>
    * <span data-ttu-id="5dac5-142">باستطاعة عناصر تنسيق متعددة أن تحمل نفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="5dac5-142">Several format elements can have the same name.</span></span> <span data-ttu-id="5dac5-143">على سبيل المثال، Dim.‬ لا يمكنك أن تتعرف عليها بشكل صريح عند استخدام هذا التنسيق كمصدر بيانات لأرشفة تفاصيل إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، وبالتالي يجب تحديد الأسماء البديلة لعناصر التنسيق هذه.</span><span class="sxs-lookup"><span data-stu-id="5dac5-143">For example, Dim. You cannot explicitly recognize them when you use this format as a data source for archiving Intrastat reporting details, so you need to define the alternative names for these format elements.</span></span>   
28. <span data-ttu-id="5dac5-144">في الحقل "الاسم"، اكتب "المبلغ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-144">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="5dac5-145">المبلغ</span><span class="sxs-lookup"><span data-stu-id="5dac5-145">Amount</span></span>  
29. <span data-ttu-id="5dac5-146">في حقل "التعدد"، حدد "واحد فقط‬‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-146">In the Multiplicity field, select 'Exactly one'.</span></span>
30. <span data-ttu-id="5dac5-147">في الشجرة، حدد "ملف\إقرار\بيانات\صنف\Dim4".</span><span class="sxs-lookup"><span data-stu-id="5dac5-147">In the tree, select 'File\Declaration\Data\Item\Dim4'.</span></span>
31. <span data-ttu-id="5dac5-148">في الحقل "الاسم" اكتب "الصنف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-148">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="5dac5-149">الصنف</span><span class="sxs-lookup"><span data-stu-id="5dac5-149">Item</span></span>  
32. <span data-ttu-id="5dac5-150">في حقل "التعدد"، حدد "واحد فقط‬‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-150">In the Multiplicity field, select 'Exactly one'.</span></span>
    * <span data-ttu-id="5dac5-151">بالإضافة إلى تصميم عناصر التنسيق، يجب أن تتم أرشفة التفاصيل التالية لإعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي: تعريف سجل فريد لكل صنف سلعة تم الإبلاغ عنه واسم الملف الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="5dac5-151">In addition to the design format elements, the following Intrastat reporting details must be archived: unique record identification of each reported commodity item and name of the generated file.</span></span> <span data-ttu-id="5dac5-152">نظراً لعدم تعبئة هذه البيانات في تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، يجب عليك إضافة التنسيق المتعلق بعناصر التفاصيل هذه كعناصر مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="5dac5-152">Because this data will not be populated in the Intrastat report, you need to add the format that is related to these detail elements as data source items.</span></span>  
33. <span data-ttu-id="5dac5-153">في الشجرة، حدد "ملف\إقرار\بيانات".</span><span class="sxs-lookup"><span data-stu-id="5dac5-153">In the tree, select 'File\Declaration\Data'.</span></span>
34. <span data-ttu-id="5dac5-154">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="5dac5-154">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="5dac5-155">في الشجرة، حدد "مصدر بيانات\صنف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-155">In the tree, select 'Data source\Item'.</span></span>
36. <span data-ttu-id="5dac5-156">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-156">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="5dac5-157">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="5dac5-157">File name</span></span>  
37. <span data-ttu-id="5dac5-158">في الحقل "نوع البيانات"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="5dac5-158">In the Data type field, select 'String'.</span></span>
38. <span data-ttu-id="5dac5-159">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="5dac5-159">Click OK.</span></span>
39. <span data-ttu-id="5dac5-160">في الشجرة، حدد "ملف\إقرار\بيانات\صنف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-160">In the tree, select 'File\Declaration\Data\Item'.</span></span>
40. <span data-ttu-id="5dac5-161">انقر فوق "إضافة صنف‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-161">Click Add Item.</span></span>
41. <span data-ttu-id="5dac5-162">في حقل "الاسم"، اكتب "معرف سجل السلع".</span><span class="sxs-lookup"><span data-stu-id="5dac5-162">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="5dac5-163">معرف سجل السلع</span><span class="sxs-lookup"><span data-stu-id="5dac5-163">Commodity rec id</span></span>  
42. <span data-ttu-id="5dac5-164">في الحقل "نوع البيانات"، حدد "Int64".</span><span class="sxs-lookup"><span data-stu-id="5dac5-164">In the Data type field, select 'Int64'.</span></span>
43. <span data-ttu-id="5dac5-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="5dac5-165">Click OK.</span></span>
44. <span data-ttu-id="5dac5-166">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="5dac5-166">Click the Mapping tab.</span></span>
45. <span data-ttu-id="5dac5-167">في الشجرة، حدد "ملف\إقرار\بيانات\اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-167">In the tree, select 'File\Declaration\Data\File name'.</span></span>
46. <span data-ttu-id="5dac5-168">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-168">Click Bind.</span></span>
47. <span data-ttu-id="5dac5-169">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="5dac5-169">In the tree, expand 'model'.</span></span>
48. <span data-ttu-id="5dac5-170">في الشجرة، قم بتوسيع "نموذج\حركات".</span><span class="sxs-lookup"><span data-stu-id="5dac5-170">In the tree, expand 'model\Transactions'.</span></span>
49. <span data-ttu-id="5dac5-171">في الشجرة، حدد "ملف\إقرار\بيانات\صنف= model.Transactions\معرف سجل السلع‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-171">In the tree, select 'File\Declaration\Data\Item =  model.Transactions\Commodity rec id'.</span></span>
50. <span data-ttu-id="5dac5-172">في الشجرة، حدد "نموذج\حركات\معرف سجل السلع‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-172">In the tree, select 'model\Transactions\Commodity rec id'.</span></span>
51. <span data-ttu-id="5dac5-173">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-173">Click Bind.</span></span>
52. <span data-ttu-id="5dac5-174">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-174">Click Save.</span></span>

## <a name="modify-format-to-memorize-details-of-reporting"></a><span data-ttu-id="5dac5-175">تعديل التنسيق لحفظ تفاصيل إعداد التقارير</span><span class="sxs-lookup"><span data-stu-id="5dac5-175">Modify format to memorize details of reporting</span></span>
1. <span data-ttu-id="5dac5-176">انقر فوق "تعيين تنسيق لنموذج‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-176">Click Map format to model.</span></span>
2. <span data-ttu-id="5dac5-177">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5dac5-177">Click New.</span></span>
3. <span data-ttu-id="5dac5-178">في حقل "التعريف"، أدخل أو حدد عنصر الجذر "لتحديث بيانات التطبيق".</span><span class="sxs-lookup"><span data-stu-id="5dac5-178">In the Definition field, enter or select the ‘For application data update’ root item.</span></span>
    * <span data-ttu-id="5dac5-179">لتحديث بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="5dac5-179">For application data update</span></span>  
4. <span data-ttu-id="5dac5-180">في حقل "الاسم"، اكتب "تعيين لتحديث البيانات‬".</span><span class="sxs-lookup"><span data-stu-id="5dac5-180">In the Name field, type 'Mapping to update data'.</span></span>
    * <span data-ttu-id="5dac5-181">تعيين لتحديث البيانات</span><span class="sxs-lookup"><span data-stu-id="5dac5-181">Mapping to update data</span></span>  
5. <span data-ttu-id="5dac5-182">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-182">Click Save.</span></span>
    * <span data-ttu-id="5dac5-183">يحدد هذا التعيين كيف يتم جمع تفاصيل إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي في نموذج البيانات، والذي يتم تحديد بنيته بالعنصر الجذر المحدد 'لتحديث بيانات التطبيق'.</span><span class="sxs-lookup"><span data-stu-id="5dac5-183">This mapping defines how the details of the Intrastat report are collected in the data model, the structure of which is specified by the selected root item ‘For application data update’.</span></span> <span data-ttu-id="5dac5-184">سيتم استخدام هذه التفاصيل وتعيين النموذج مع عنصر الجذر نفسه 'لتحديث بيانات التطبيق' والاتجاه 'إلى الوجهة‬' لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="5dac5-184">These details, the model mapping with same root item ‘For application data update’, and the direction ‘To destination’ will be used for the application data update.</span></span> <span data-ttu-id="5dac5-185">يبدأ تحديث بيانات التطبيق مباشرة بعد إنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="5dac5-185">The application data update starts immediately after the outgoing Intrastat report is generated.</span></span> <span data-ttu-id="5dac5-186">لاحظ أنه يمكن تخطي تحديث بيانات التطبيق في وقت التشغيل، ولكن يجب أن يكون نموذج البيانات فارغًا (يحتوي على قائمة سجلات فارغة).</span><span class="sxs-lookup"><span data-stu-id="5dac5-186">Note that the application data update can be skipped at run-time, but the data model must be empty (containing empty record list).</span></span>   
6. <span data-ttu-id="5dac5-187">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="5dac5-187">Click Designer.</span></span>
    * <span data-ttu-id="5dac5-188">لاحظ أن تنسيق تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي يضاف بشكل افتراضي كمصدر بيانات لتعيين النموذج هذا.</span><span class="sxs-lookup"><span data-stu-id="5dac5-188">Note that the outgoing Intrastat report format is added by default as a data source for this model mapping.</span></span>  
    * <span data-ttu-id="5dac5-189">اربط عناصر التقرير المصمم (المعروض كمصدر بيانات) بعناصر نموذج البيانات، الذي تمت تصفيته استنادًا إلى العنصر الجذر للنموذج المحدد.</span><span class="sxs-lookup"><span data-stu-id="5dac5-189">Bind elements of the designed report (presented as data source) to elements of the data model, which is filtered based on the selected model’s root item.</span></span>  
7. <span data-ttu-id="5dac5-190">في الشجرة ، قم بتوسيع "رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-190">In the tree, expand 'Archive header'.</span></span>
8. <span data-ttu-id="5dac5-191">في الشجرة، قم بتوسيع "رأس الأرشيف\بنود الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-191">In the tree, expand 'Archive header\Archive lines'.</span></span>
9. <span data-ttu-id="5dac5-192">في الشجرة، قم بتوسيع "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="5dac5-192">In the tree, expand 'format'.</span></span>
10. <span data-ttu-id="5dac5-193">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-193">In the tree, expand 'format\Declaration: XML Element(Declaration)'.</span></span>
11. <span data-ttu-id="5dac5-194">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..\* (بيانات)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-194">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..\* (Data)'.</span></span>
12. <span data-ttu-id="5dac5-195">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-195">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
13. <span data-ttu-id="5dac5-196">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)\Dim3: عنصر XML 1..1 (المبلغ)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-196">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)'.</span></span>
14. <span data-ttu-id="5dac5-197">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)\Dim4: عنصر XML 1..1 (الصنف)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-197">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)'.</span></span>
15. <span data-ttu-id="5dac5-198">في الشجرة، حدد "رأس الأرشيف\عدد البنود".</span><span class="sxs-lookup"><span data-stu-id="5dac5-198">In the tree, select 'Archive header\Number of lines'.</span></span>
16. <span data-ttu-id="5dac5-199">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="5dac5-199">Click Edit.</span></span>
17. <span data-ttu-id="5dac5-200">في الشجرة، حدد "قائمة\COUNT".</span><span class="sxs-lookup"><span data-stu-id="5dac5-200">In the tree, select 'List\COUNT'.</span></span>
18. <span data-ttu-id="5dac5-201">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="5dac5-201">Click Add function.</span></span>
19. <span data-ttu-id="5dac5-202">في الشجرة، قم بتوسيع "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="5dac5-202">In the tree, expand 'format'.</span></span>
20. <span data-ttu-id="5dac5-203">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-203">In the tree, expand 'format\Declaration: XML Element(Declaration)'.</span></span>
21. <span data-ttu-id="5dac5-204">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..\* (بيانات)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-204">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..\* (Data)'.</span></span>
22. <span data-ttu-id="5dac5-205">في الشجرة، حدد "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-205">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
23. <span data-ttu-id="5dac5-206">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="5dac5-206">Click Add data source.</span></span>
24. <span data-ttu-id="5dac5-207">في حقل المعادلة، أدخل "COUNT(format.Declaration.Data.Item)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-207">In the Formula field, enter 'COUNT(format.Declaration.Data.Item)'.</span></span>
    * <span data-ttu-id="5dac5-208">COUNT(format.Declaration.Data.Item)</span><span class="sxs-lookup"><span data-stu-id="5dac5-208">COUNT(format.Declaration.Data.Item)</span></span>  
25. <span data-ttu-id="5dac5-209">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-209">Click Save.</span></span>
26. <span data-ttu-id="5dac5-210">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5dac5-210">Close the page.</span></span>
27. <span data-ttu-id="5dac5-211">في الشجرة، حدد "رأس الأرشيف\اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-211">In the tree, select 'Archive header\File name'.</span></span>
28. <span data-ttu-id="5dac5-212">في الشجرة، حدد "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..\* (بيانات)\اسم الملف: سلسلة أصناف(اسم الملف)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-212">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..\* (Data)\File name: Item String(File name)'.</span></span>
29. <span data-ttu-id="5dac5-213">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-213">Click Bind.</span></span>
30. <span data-ttu-id="5dac5-214">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)\Dim4: عنصر XML 1..1 (صنف)\رقم: سلسلة(رقم)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-214">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)'.</span></span>
31. <span data-ttu-id="5dac5-215">في الشجرة، حدد "رأس الأرشيف\بنود الأرشيف\رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-215">In the tree, select 'Archive header\Archive lines\Item number'.</span></span>
32. <span data-ttu-id="5dac5-216">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-216">Click Bind.</span></span>
33. <span data-ttu-id="5dac5-217">في الشجرة، قم بتوسيع "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)\Dim3: عنصر XML 1..1 (مبلغ)\قيمة: رقمية حقيقية(قيمة)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-217">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)'.</span></span>
34. <span data-ttu-id="5dac5-218">في الشجرة، حدد "رأس الأرشيف\بنود الأرشيف\مبلغ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-218">In the tree, select 'Archive header\Archive lines\Amount'.</span></span>
35. <span data-ttu-id="5dac5-219">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-219">Click Bind.</span></span>
36. <span data-ttu-id="5dac5-220">في الشجرة، حدد "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)\معرف سجل السلع: صنف Int64(معرف سجل السلع)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-220">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec id: Item Int64(Commodity rec id)'.</span></span>
37. <span data-ttu-id="5dac5-221">في الشجرة، حدد "رأس الأرشيف\بنود الأرشيف\معرف سجل السلع".</span><span class="sxs-lookup"><span data-stu-id="5dac5-221">In the tree, select 'Archive header\Archive lines\Commodity rec id'.</span></span>
38. <span data-ttu-id="5dac5-222">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-222">Click Bind.</span></span>
39. <span data-ttu-id="5dac5-223">في الشجرة، حدد "رأس الأرشيف\بنود الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-223">In the tree, select 'Archive header\Archive lines'.</span></span>
40. <span data-ttu-id="5dac5-224">في الشجرة، حدد "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..* (بيانات)\صنف: عنصر XML 0..* (صنف)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-224">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
41. <span data-ttu-id="5dac5-225">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-225">Click Bind.</span></span>
42. <span data-ttu-id="5dac5-226">في الشجرة ، حدد "رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="5dac5-226">In the tree, select 'Archive header'.</span></span>
43. <span data-ttu-id="5dac5-227">في الشجرة، حدد "تنسيق\إقرار: عنصر XML(إقرار)\بيانات: عنصر XML 1..\* (بيانات)".</span><span class="sxs-lookup"><span data-stu-id="5dac5-227">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..\* (Data)'.</span></span>
44. <span data-ttu-id="5dac5-228">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="5dac5-228">Click Bind.</span></span>
45. <span data-ttu-id="5dac5-229">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5dac5-229">Click Save.</span></span>
46. <span data-ttu-id="5dac5-230">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5dac5-230">Close the page.</span></span>
47. <span data-ttu-id="5dac5-231">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5dac5-231">Close the page.</span></span>
48. <span data-ttu-id="5dac5-232">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5dac5-232">Close the page.</span></span>


