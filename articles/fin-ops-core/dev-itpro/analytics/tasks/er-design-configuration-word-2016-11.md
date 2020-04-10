---
title: تصميم تكوينات التقارير الإلكترونية لإنشاء تقارير بتنسيق Word
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيقات التقارير الإلكترونية لإنشاء تقارير كملفات Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 208b1be20a8833afbf4929a7ceda706aeb5bda3b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142076"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="07037-103">تصميم تكوينات التقارير الإلكترونية لإنشاء تقارير بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="07037-103">Design ER configurations to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07037-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيقات التقارير الإلكترونية لإنشاء تقارير كملفات Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="07037-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="07037-105">يمكن تنفيذ هذه الخطوات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="07037-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="07037-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات الموضحة في دليل المهمة "إنشاء تكوين التقارير الإلكترونية لإنشاء التقارير بتنسيق OPENXML‬".</span><span class="sxs-lookup"><span data-stu-id="07037-106">To complete these steps, you must first complete the steps in the "Create an ER configuration for generating reports in OPENXML format" task guide.</span></span> <span data-ttu-id="07037-107">بشكل مسبق، يجب أيضًا تنزيل وحفظ القوالب التالية محليًا للتقرير النموذجي:</span><span class="sxs-lookup"><span data-stu-id="07037-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="07037-108">قالب تقرير الدفع</span><span class="sxs-lookup"><span data-stu-id="07037-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="07037-109">القالب المضمن لتقرير الدفع</span><span class="sxs-lookup"><span data-stu-id="07037-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="07037-110">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Microsoft Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="07037-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="07037-111">تحديد تكوين التقارير الإلكترونية الموجود</span><span class="sxs-lookup"><span data-stu-id="07037-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="07037-112">في **جزء التنقل، انتقل إلى الوحدات النمطية > إدارة المؤسسة > مساحات العمل > التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="07037-112">In the **Navigation pane, go to Modules > Organization administration > Workspaces > Electronic reporting**.</span></span> <span data-ttu-id="07037-113">تأكد من تحديد موفر التكوين ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="07037-113">Make sure that the configuration provider 'Litware, Inc.'</span></span> <span data-ttu-id="07037-114">كموفر نشط.</span><span class="sxs-lookup"><span data-stu-id="07037-114">is selected as active.</span></span>  
2. <span data-ttu-id="07037-115">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="07037-115">Click **Reporting configurations**.</span></span> <span data-ttu-id="07037-116">سوف نعيد استخدام تكوين التقارير الإلكترونية الموجود الذي تم تصميمه في الأصل لإنشاء مخرجات التقرير بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="07037-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="07037-117">في الشجرة، قم بتوسيع "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="07037-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="07037-118">في الشجرة، حدد "Payment model\Sample worksheet report".</span><span class="sxs-lookup"><span data-stu-id="07037-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="07037-119">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="07037-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="07037-120">استبدال قالب Excel بقالب Word</span><span class="sxs-lookup"><span data-stu-id="07037-120">Replace the Excel template with the Word template</span></span>

<span data-ttu-id="07037-121">في الوقت الحالي، يتم استخدام مستند Excel كقالب لإنشاء المخرجات بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="07037-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="07037-122">سوف نستورد قالب التقرير بتنسيق Word.</span><span class="sxs-lookup"><span data-stu-id="07037-122">We will import the report's template in Word format.</span></span>

1. <span data-ttu-id="07037-123">انقر فوق **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="07037-123">Click **Attachments**.</span></span> <span data-ttu-id="07037-124">استبدل قالب Excel الموجود بقالب Word الذي قمت بتنزيله في وقت سابق، SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="07037-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="07037-125">لاحظ أن هذا القالب يحتوي فقط على تخطيط المستند الذي نرغب في إنشائه كمخرجات تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="07037-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="07037-126">انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="07037-126">Click **Delete**.</span></span>
3. <span data-ttu-id="07037-127">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="07037-127">Click **Yes**.</span></span>
4. <span data-ttu-id="07037-128">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="07037-128">Click **New**.</span></span>
5. <span data-ttu-id="07037-129">انقر فوق **ملف**.</span><span class="sxs-lookup"><span data-stu-id="07037-129">Click **File**.</span></span>
6. <span data-ttu-id="07037-130">انقر فوق **استعراض**.</span><span class="sxs-lookup"><span data-stu-id="07037-130">Click **Browse**.</span></span> <span data-ttu-id="07037-131">انتقل إلى الملف SampleVendPaymDocReport.docx الذي قمت بتنزيله في وقت سابق وحدده.</span><span class="sxs-lookup"><span data-stu-id="07037-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="07037-132">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="07037-132">Click **OK**.</span></span> <span data-ttu-id="07037-133">حدد القالب الذي قمت بتنزيله في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="07037-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="07037-134">في حقل **القالب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="07037-134">In the **Template** field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="07037-135">توسيع قالب Word بإضافة جزء XML مخصص</span><span class="sxs-lookup"><span data-stu-id="07037-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="07037-136">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="07037-136">Click **Save**.</span></span> <span data-ttu-id="07037-137">بالإضافة إلى تخزين التغييرات على التكوين، يقوم إجراء الحفظ أيضًا بتحديث قالب Word المرفق.</span><span class="sxs-lookup"><span data-stu-id="07037-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="07037-138">يتم نقل بنية التنسيق المصمّم إلى مستند Word المرفق كجزء XML مخصص جديد باسم "التقرير".</span><span class="sxs-lookup"><span data-stu-id="07037-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name 'Report'.</span></span> <span data-ttu-id="07037-139">لاحظ أن قالب Word المرفق لا يحتوي على تخطيط المستند الذي نرغب في إنشائه كمخرجات تقارير إلكترونية فحسب، بل يحتوي أيضًا على بنية البيانات التي ستقوم التقارير الإلكترونية بتعبئتها في هذا القالب في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="07037-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="07037-140">انقر فوق **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="07037-140">Click **Attachments**.</span></span>
    + <span data-ttu-id="07037-141">الآن أنت بحاجة إلى ربط عناصر جزء XML المخصص "التقرير" بأجزاء مستند Word.</span><span class="sxs-lookup"><span data-stu-id="07037-141">Now you need to bind the elements of the custom XML part 'Report' to the Word document parts.</span></span>  
    + <span data-ttu-id="07037-142">إذا كنت ملمًا باستخدام مستندات Word التي يمكن تصميمها كنماذج تحتوي على عناصر تحكم بالمحتوى ترتباط بعناصر من أجزاء XML المخصصة – فيمكنك تشغيل كل الخطوات في المهمة الفرعية التالية لإنشاء مثل هذا المستند.</span><span class="sxs-lookup"><span data-stu-id="07037-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="07037-143">لمزيد من التفاصيل، راجع [إنشاء نماذج يقوم المستخدمون بإكمالها أو طباعتها في Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="07037-143">For more details, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span></span> <span data-ttu-id="07037-144">وإلا، فيمكنك تخطي كل الخطوات في المهمة الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="07037-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="07037-145">إحضار Word مع جزء XML مخصص للقيام بعمليات ربط البيانات</span><span class="sxs-lookup"><span data-stu-id="07037-145">Get Word with custom XML part to do data bindings</span></span>

<span data-ttu-id="07037-146">افتح هذا المستند في Word وقم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="07037-146">Open this document in Word and do the following:</span></span>  
1. <span data-ttu-id="07037-147">افتح علامة تبويب المطور في Word (يمكنك تخصيص الشريط إذا لم يكن ممكّنًا حتى الآن).‬</span><span class="sxs-lookup"><span data-stu-id="07037-147">Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>
2. <span data-ttu-id="07037-148">حدد جزء تعيين XML.</span><span class="sxs-lookup"><span data-stu-id="07037-148">Select XML mapping pane.</span></span>
3. <span data-ttu-id="07037-149">حدد جزء XML المخصص "التقرير" في البحث.</span><span class="sxs-lookup"><span data-stu-id="07037-149">Select the 'Report' custom XML part in the lookup.</span></span>
4. <span data-ttu-id="07037-150">نفّذ تعيين العناصر في جزء XML المخصص المحدد وعناصر التحكم بالمحتوى في مستند Word.</span><span class="sxs-lookup"><span data-stu-id="07037-150">Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="07037-151">5.</span><span class="sxs-lookup"><span data-stu-id="07037-151">5.</span></span> <span data-ttu-id="07037-152">احفظ مستند Word المحدث على محرك أقراص محلي.</span><span class="sxs-lookup"><span data-stu-id="07037-152">Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="07037-153">تحميل قالب Word مع جزء XML المخصص المرتبط بعناصر التحكم بالمحتوى</span><span class="sxs-lookup"><span data-stu-id="07037-153">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="07037-154">انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="07037-154">Click **Delete**.</span></span>
2. <span data-ttu-id="07037-155">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="07037-155">Click **Yes**.</span></span> <span data-ttu-id="07037-156">إضافة قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="07037-156">Add a new template.</span></span> <span data-ttu-id="07037-157">إذا أكملت الخطوات في المهمة الفرعية السابقة، فحدد مستند Word الذي قمت بإعداده وحفظه محليًا.</span><span class="sxs-lookup"><span data-stu-id="07037-157">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="07037-158">وإلا، فحدد قالب SampleVendPaymDocReportBounded.docx MS Word الذي قمت بتنزيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="07037-158">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="07037-159">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="07037-159">Click **New**.</span></span>
4. <span data-ttu-id="07037-160">انقر فوق **ملف**.</span><span class="sxs-lookup"><span data-stu-id="07037-160">Click **File**.</span></span>
5. <span data-ttu-id="07037-161">انقر فوق **استعراض**.</span><span class="sxs-lookup"><span data-stu-id="07037-161">Click **Browse**.</span></span> <span data-ttu-id="07037-162">انتقل إلى الملف SampleVendPaymDocReportBounded.docx الذي قمت بتنزيله في وقت سابق وحدده.</span><span class="sxs-lookup"><span data-stu-id="07037-162">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="07037-163">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="07037-163">Click **OK**.</span></span>
6. <span data-ttu-id="07037-164">في حقل **القالب**، حدد القالب الذي قمت بتنزيله في الخطوة السابقة.</span><span class="sxs-lookup"><span data-stu-id="07037-164">In the **Template** field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="07037-165">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="07037-165">Click **Save**.</span></span>
8. <span data-ttu-id="07037-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="07037-166">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="07037-167">تنفيذ التنسيق لإنشاء مخرجات Word</span><span class="sxs-lookup"><span data-stu-id="07037-167">Execute the format to create Word output</span></span>
1. <span data-ttu-id="07037-168">في **جزء الإجراءات**، انقر فوق **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="07037-168">On the **Action Pane**, click **Configurations**.</span></span>
2. <span data-ttu-id="07037-169">انقر فوق **محددات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="07037-169">Click **User parameters**.</span></span>
3. <span data-ttu-id="07037-170">حدد "نعم" في حقل **تشغيل الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="07037-170">Select Yes in the **Run settings** field.</span></span>
4. <span data-ttu-id="07037-171">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="07037-171">Click **OK**.</span></span>
5. <span data-ttu-id="07037-172">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="07037-172">Click **Edit**.</span></span>
6. <span data-ttu-id="07037-173">حدد "نعم" في حقل **تشغيل المسودة‬**.</span><span class="sxs-lookup"><span data-stu-id="07037-173">Select Yes in the **Run Draft** field.</span></span>
7. <span data-ttu-id="07037-174">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="07037-174">Click **Save**.</span></span>
8. <span data-ttu-id="07037-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="07037-175">Close the page.</span></span>
9. <span data-ttu-id="07037-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="07037-176">Close the page.</span></span>
10. <span data-ttu-id="07037-177">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > المدفوعات > دفتر يومية المدفوعات**‬.</span><span class="sxs-lookup"><span data-stu-id="07037-177">In the **Navigation pane**, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
11. <span data-ttu-id="07037-178">انقر فوق **البنود**.</span><span class="sxs-lookup"><span data-stu-id="07037-178">Click **Lines**.</span></span>
12. <span data-ttu-id="07037-179">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="07037-179">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="07037-180">انقر فوق **حالة الدفع**.</span><span class="sxs-lookup"><span data-stu-id="07037-180">Click **Payment status**.</span></span>
14. <span data-ttu-id="07037-181">انقر فوق **بلا**.</span><span class="sxs-lookup"><span data-stu-id="07037-181">Click **None**.</span></span>
15. <span data-ttu-id="07037-182">انقر فوق **إنشاء مدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="07037-182">Click **Generate payments**.</span></span>
16. <span data-ttu-id="07037-183">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="07037-183">Click **OK**.</span></span>
17. <span data-ttu-id="07037-184">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="07037-184">Click **OK**.</span></span> <span data-ttu-id="07037-185">مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="07037-185">Analyze the generated output.</span></span> <span data-ttu-id="07037-186">لاحظ أن تقديم المخرجات المنشأة يتم بتنسيق Word وهي تحتوي على تفاصيل المدفوعات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="07037-186">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

