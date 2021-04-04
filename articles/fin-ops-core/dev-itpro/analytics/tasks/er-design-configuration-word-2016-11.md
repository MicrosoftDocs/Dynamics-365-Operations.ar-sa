---
title: إعادة استخدام التكوينات باستخدام قوالب Excel لإنشاء تقارير بتنسيقات Word
description: يصف هذا الموضوع كيف يمكن تكوين تنسيقات التقارير التي تم تصميمها لإنشاء تقارير كمصنفات Excel لإنشاء تقارير كمستندات Word.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 601896bad72b079759b1a07efba8717101e94362
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569301"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="5c018-103">إعادة استخدام التكوينات باستخدام قوالب Excel لإنشاء تقارير بتنسيقات Word</span><span class="sxs-lookup"><span data-stu-id="5c018-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c018-104">لإنشاء تقارير Microsoft Word كمستندات، يمكنك [تكوين](../er-design-configuration-word.md)[ تنسيق ](../general-electronic-reporting.md)[التقارير الإلكترونيه الجديد (ER)](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="5c018-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="5c018-105">بدلا من ذلك، يمكنك أعاده استخدام تنسيق ER الذي تم تصميمه في الأصل لإنشاء تقارير كمصنفات Excel.</span><span class="sxs-lookup"><span data-stu-id="5c018-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="5c018-106">في هذه الحالة، يجب استبدال قالب Excel بقالب Word.</span><span class="sxs-lookup"><span data-stu-id="5c018-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="5c018-107">تظهر الإجراءات التالية كيف يمكن لمستخدم ما في دور مسؤول النظام أو دور مطور التقارير الكترونيه تكوين تنسيق ER لإنشاء تقارير كملفات Word عن طريق أعاده استخدام تنسيق ER الذي تم تصميمه لإنشاء تقارير كملفات Excel.</span><span class="sxs-lookup"><span data-stu-id="5c018-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="5c018-108">يمكن إكمال هذه الإجراءات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="5c018-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5c018-109">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="5c018-109">Prerequisites</span></span>

<span data-ttu-id="5c018-110">لإكمال الخطوات في هذا الإجراء، يجب أولاً إكمال الخطوات في دليل مهام [تصميم تكوين لإنشاء التقارير بتنسيق OPENXML](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5c018-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="5c018-111">يجب أيضًا تنزيل وحفظ القوالب التالية محليًا للتقرير النموذجي:</span><span class="sxs-lookup"><span data-stu-id="5c018-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="5c018-112">قالب تقرير الدفع (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="5c018-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="5c018-113">القالب المرتبط لتقرير الدفع (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="5c018-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="5c018-114">وتكون هذه الإجراءات لميزه تمت اضافتها في Dynamics 365 for Operations الإصدار 1611 (نوفمبر 2016).</span><span class="sxs-lookup"><span data-stu-id="5c018-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="5c018-115">تحديد تكوين التقارير الإلكترونية الموجود</span><span class="sxs-lookup"><span data-stu-id="5c018-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="5c018-116">في Dynamics 365 Finance، انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5c018-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="5c018-117">تأكد من تحديد موفر التكوين **Litware, Inc.** بالقيمة **نشط**.</span><span class="sxs-lookup"><span data-stu-id="5c018-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="5c018-118">وإذا لم تكن كذلك، فاتبع الخطوات الموجودة في [إنشاء موفري تكوين وقم بوضع علامة عليها علي انها نشط في دليل المهام](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5c018-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="5c018-119">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="5c018-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="5c018-120">سوف تعيد استخدام تكوين التقارير الإلكترونية الموجود الذي تم تصميمه لإنشاء مخرجات التقرير بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="5c018-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="5c018-121">في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، وسَّع **نموذج الدفع**، ثم حدد **عينة تقرير ورقة العمل**.</span><span class="sxs-lookup"><span data-stu-id="5c018-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c018-122">على علامة التبويب السريعة **إصدارات**، يمكن تحرير مسودة الإصدار من تنسيق ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="5c018-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="5c018-123">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="5c018-123">Select **Designer**.</span></span>
6. <span data-ttu-id="5c018-124">في الصفحة **مصمم التنسيق**، لاحظ ان عنوان عنصر التنسيق الجذر يشير إلى ان قالب Excel مستخدم حاليا.</span><span class="sxs-lookup"><span data-stu-id="5c018-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![تحديد التكوين الموجود](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="5c018-126">مراجعه قالب Word الذي تم تنزيله</span><span class="sxs-lookup"><span data-stu-id="5c018-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="5c018-127">في تطبيق Word desktop، قم بفتح ملف القالب **SampleVendPaymDocReport.docx** الذي قمت بتنزيله سابقا.</span><span class="sxs-lookup"><span data-stu-id="5c018-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="5c018-128">تحقق من أن القالب يحتوي فقط على تخطيط المستند الذي ترغب في إنشائه كمخرجات تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5c018-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![تخطيط قالب Word الموجود في تطبيق سطح المكتب](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="5c018-130">استبدال قالب Excel بقالب Word وأضافه جزء XML مخصص</span><span class="sxs-lookup"><span data-stu-id="5c018-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="5c018-131">في الوقت الحالي، يتم استخدام مستند Excel كقالب لإنشاء المخرجات بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="5c018-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="5c018-132">سوف تستبدل هذ القالب بملف قالب Word الذي قمت بتنزيله في وقت سابق، SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="5c018-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="5c018-133">سوف تقوم توسيع قالب Word بإضافة جزء XML مخصص.</span><span class="sxs-lookup"><span data-stu-id="5c018-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="5c018-134">في Finance، في صفحة **مصمم التنسيق**، وفي علامة التبويب **التنسيق**، حدد **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="5c018-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="5c018-135">في الصفحة **المرفقات**، حدد **حذف** لأزاله قالب Excel الموجود.</span><span class="sxs-lookup"><span data-stu-id="5c018-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="5c018-136">حدد **نعم** لتأكيد التغيير.</span><span class="sxs-lookup"><span data-stu-id="5c018-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="5c018-137">حدد **جديد** \> **ملف**.</span><span class="sxs-lookup"><span data-stu-id="5c018-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c018-138">يجب أن تقوم بتحديد نوع المستند الذي تم [تكوينه](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) في معلمات التقارير الإلكترونية لتحديد تخزين قوالب تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5c018-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="5c018-139">حدد **استعراض**، ثم قم بالاستعراض بحثا عن الملف **SampleVendPaymDocReport.docx** الذي قمت بتنزيله سابقا وحدده.</span><span class="sxs-lookup"><span data-stu-id="5c018-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="5c018-140">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c018-140">Select **OK**.</span></span>
6. <span data-ttu-id="5c018-141">أغلق صفحة **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="5c018-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="5c018-142">في الصفحة **مصمم التنسيق**، في الحقل **القالب**، ادخل أو حدد الملف **SampleVendPaymDocReport.docx** لاستخدام قالب Word بدلا من قالب Excel الذي تم استخدامه مسبقا.</span><span class="sxs-lookup"><span data-stu-id="5c018-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="5c018-143">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5c018-143">Select **Save**.</span></span>

    <span data-ttu-id="5c018-144">بالإضافة إلى تخزين التغييرات على التكوين، يقوم إجراء **الحفظ** بتحديث قالب Word المرفق.</span><span class="sxs-lookup"><span data-stu-id="5c018-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="5c018-145">تتم إضافة بنية التنسيق المصمّم إلى مستند Word المرفق كجزء XML مخصص جديد باسم **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="5c018-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="5c018-146">لاحظ أن قالب Word المرفق لا يحتوي على تخطيط المستند الذي نرغب في إنشائه كمخرجات تقارير إلكترونية فحسب، بل يحتوي أيضًا على بنية البيانات التي ستقوم التقارير الإلكترونية بتعبئتها في هذا القالب في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="5c018-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="5c018-147">لاحظ ان عنوان عنصر التنسيق الجذر يشير إلى ان قالب Word مستخدم حاليا.</span><span class="sxs-lookup"><span data-stu-id="5c018-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![استبدال قالب Excel بقالب Word وأضافه جزء XML مخصص](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="5c018-149">ضمن علامة التبويب **تنسيق**، حدد **مرفقات**.</span><span class="sxs-lookup"><span data-stu-id="5c018-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="5c018-150">نفّذ تعيين العناصر في جزء XML المخصص المحدد **التقرير** وعناصر التحكم بالمحتوى في مستند Word.</span><span class="sxs-lookup"><span data-stu-id="5c018-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="5c018-151">إذا كنت ملمًا باستخدام مستندات Word التي يمكن تصميمها كنماذج تحتوي على [عناصر تحكم](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) بالمحتوى ترتباط بعناصر من [أجزاء XML المخصصة](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019)، فيمكنك تشغيل كل الخطوات في المهمة الفرعية التالية لإنشاء مثل هذا المستند.</span><span class="sxs-lookup"><span data-stu-id="5c018-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="5c018-152">لمزيد من المعلومات، راجع [إنشاء نماذج يقوم المستخدمون بإكمالها أو طباعتها في Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="5c018-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="5c018-153">وإلا، فيمكنك تخطي الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="5c018-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="5c018-154">الحصول علي مستند Word يحتوي علي جزء XML مخصص وتعيين البيانات</span><span class="sxs-lookup"><span data-stu-id="5c018-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="5c018-155">في Finance، في الصفحة **المرفقات**، حدد **فتح** لتنزيل القالب المحدد من المالية وتخزينه محليا كمستند Word.</span><span class="sxs-lookup"><span data-stu-id="5c018-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="5c018-156">في تطبيق Word desktop، افتح المستند الذي قمت بتنزيله الآن.</span><span class="sxs-lookup"><span data-stu-id="5c018-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="5c018-157">في علامة تبويب **المطور**، حدد **جزء تخطيط XML**.</span><span class="sxs-lookup"><span data-stu-id="5c018-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c018-158">في حاله عدم ظهور علامة التبويب **المطور** علي الشريط، قم بتخصيص الشريط لأضافه.</span><span class="sxs-lookup"><span data-stu-id="5c018-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="5c018-159">في **جزء تعيين xml**، في الحقل **جزء xml مخصص**، حدد جزء xml المخصص **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="5c018-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="5c018-160">نفّذ تعيين العناصر في جزء XML المخصص المحدد **التقرير** وعناصر التحكم بالمحتوى في مستند Word.</span><span class="sxs-lookup"><span data-stu-id="5c018-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="5c018-161">قم بحفظ مستند Word المحدث محليا باسم **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="5c018-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="5c018-162">مراجعه قالب Word الذي يتم فيه تعيين جزء XML المخصص إلى عناصر تحكم المحتوي</span><span class="sxs-lookup"><span data-stu-id="5c018-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="5c018-163">في تطبيق Word desktop، قم بفتح ملف القالب **SampleVendPaymDocReportBounded.docx** الذي قمت بتنزيله سابقا.</span><span class="sxs-lookup"><span data-stu-id="5c018-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="5c018-164">تحقق من أن القالب يحتوي على تخطيط المستند الذي ترغب في إنشائه كمخرجات تقارير إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5c018-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="5c018-165">تعتمد عناصر تحكم المحتوي التي يتم استخدامها كعناصر نائبه للبيانات التي يقوم ER بإدخالها في هذا القالب في وقت التشغيل علي التعيينات التي تم تكوينها بين عناصر جزء XML المخصص **التقرير** وعناصر تحكم المحتوي الخاصة بمستند Word.</span><span class="sxs-lookup"><span data-stu-id="5c018-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![معاينة قالب Word الموجود في تطبيق سطح المكتب](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="5c018-167">تحميل قالب Word الذي يتم فيه تعيين جزء XML المخصص إلى عناصر تحكم المحتوي</span><span class="sxs-lookup"><span data-stu-id="5c018-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="5c018-168">في Finance، في الصفحة **المرفقات**، حدد **حذف** لأزاله قالب Word الذي لا يوجد به تعيينات بين عناصر جزء XML المخصص **التقرير** وعناصر تحكم المحتوي.</span><span class="sxs-lookup"><span data-stu-id="5c018-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="5c018-169">حدد **نعم** لتأكيد التغيير.</span><span class="sxs-lookup"><span data-stu-id="5c018-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="5c018-170">حدد **جديد** \> **ملف** لأضافه ملف قالب جديد يحتوي علي التعيينات بين عناصر جزء XML المخصص **التقرير** وعناصر تحكم المحتوي.</span><span class="sxs-lookup"><span data-stu-id="5c018-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c018-171">يجب أن تقوم بتحديد نوع المستند الذي تم [تكوينه](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) في معلمات التقارير الإلكترونية لتحديد تخزين قوالب تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5c018-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="5c018-172">حدد **استعراض**، ثم استعرض بحثا عن الملف **SampleVendPaymDocReportBounded.docx** الذي قمت بتنزيله أو تحضيره من خلال إكمال الاجراء في [الحصول علي كلمه تحتوي علي جزء XML مخصص للقيام بتعيين البيانات](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="5c018-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="5c018-173">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c018-173">Select **OK**.</span></span>
5. <span data-ttu-id="5c018-174">أغلق صفحة **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="5c018-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="5c018-175">في الصفحة **مصمم التنسيق**، في الحقل **القالب**، حدد المستند الذي قمت بتنزيله الآن.</span><span class="sxs-lookup"><span data-stu-id="5c018-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="5c018-176">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5c018-176">Select **Save**.</span></span>
8. <span data-ttu-id="5c018-177">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="5c018-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="5c018-178">وضع علامة علي التنسيق المكون كقابل للتشغيل</span><span class="sxs-lookup"><span data-stu-id="5c018-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="5c018-179">لتشغيل الإصدار التمهيدي من التنسيق القابل للتحرير ، يجب ان تجعله [كقابل للتشغيل](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="5c018-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="5c018-180">في Finance، في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="5c018-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="5c018-181">في مربع الحوار **معلمات المستخدم**، قم بتعيين خيارات **إعدادات التشغيل** إلى **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c018-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="5c018-182">حدد **تحرير** لتجعل الصفحة الحالية قابلة للتحرير، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="5c018-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="5c018-183">بالنسبة للنموذج المحدد حاليا لتكوين **تقرير ورقه العمل**، قم بتعيين الخيار **تشغيل مسودة**  إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="5c018-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="5c018-184">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5c018-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="5c018-185">تشغيل التنسيق لإنشاء إخراج بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="5c018-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="5c018-186">في Finance، انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات‬**.</span><span class="sxs-lookup"><span data-stu-id="5c018-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="5c018-187">في دفتر يوميه المدفوعات الذي قمت بإدخاله في السابق ، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="5c018-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="5c018-188">في **مدفوعات المورد**، حدد كافة الصفوف الموجودة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="5c018-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="5c018-189">تحديد **حاله الدفع**\>**بلا**.</span><span class="sxs-lookup"><span data-stu-id="5c018-189">Select **Payment status** \> **None**.</span></span>

    ![المدفوعات للمعالجة في صفحة مدفوعات المورد](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="5c018-191">في جزء الإجراءات، حدد **إنشاء مدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="5c018-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="5c018-192">في مربع الحوار الذي يظهر، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5c018-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="5c018-193">في حقل **طريقة الدفع** حدد **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="5c018-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="5c018-194">في الحقل **حساب البنك** حدد **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="5c018-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="5c018-195">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c018-195">Select **OK**.</span></span>

7. <span data-ttu-id="5c018-196">في مربع الحوار **معلمات التقارير الإلكترونية** حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c018-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="5c018-197">يتم عرض الإخراج الذي تم إنشاؤه بتنسيق Word وهي تحتوي على تفاصيل المدفوعات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="5c018-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="5c018-198">مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="5c018-198">Analyze the generated output.</span></span>

    ![الإخراج الناتج بتنسيق Word](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="5c018-200">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5c018-200">Additional resources</span></span>

- [<span data-ttu-id="5c018-201">تصميم تكوين ER جديد لإنشاء تقارير بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="5c018-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="5c018-202">تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5c018-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]