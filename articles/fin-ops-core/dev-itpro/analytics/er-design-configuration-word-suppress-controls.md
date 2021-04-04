---
title: منع عناصر تحكم محتوى Word في التقارير التي تم إنشاؤها
description: يشرح هذا الموضوع كيفيه تكوين تنسيق التقارير الإلكترونية (ER) لإنشاء التقارير كملفات Microsoft Word حيث يتم منع عناصر تحكم المحتويات.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562108"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="b68d6-103">منع عناصر تحكم محتوى Word في التقارير التي تم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="b68d6-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b68d6-104">لإنشاء تقارير كمستندات Microsoft Word، يجب تصميم قالب للتقارير كمستند Word.</span><span class="sxs-lookup"><span data-stu-id="b68d6-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="b68d6-105">يجب أن يحتوي هذا القالب على عناصر تحكم محتوى Word كعناصر نائبة للبيانات التي سيتم ملؤها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="b68d6-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="b68d6-106">لاستخدام مستند Word الذي تم إنشائه كقالب لتقاريرك، يمكنك [تكوين](er-design-configuration-word.md) حل [تقارير إلكترونية (ER)](general-electronic-reporting.md) [جديد](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="b68d6-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="b68d6-107">يجب أن يتضمن الحل [تكوين ER](general-electronic-reporting.md#Configuration) الذي يحتوي على مكون [تنسيق ER](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="b68d6-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="b68d6-108">يجب تكوين تنسيق ER هذا لاستخدام القالب الذي تم تصميمه لإنشاء التقارير.</span><span class="sxs-lookup"><span data-stu-id="b68d6-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="b68d6-109">في الإصدار 10.0.6 والإصدارات الأحدث من Dynamics 365 Finance، يمكنك تكوين الصيغ في تنسيق ER لمنع بعض عناصر تحكم محتوى Word في المستندات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b68d6-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="b68d6-110">توضح الخطوات التالية كيفية قيام المستخدم الذي تم تعيينه في دور مسؤول النظام أو مستشار وظيفي للتقارير الإلكترونية بتكوين تنسيق ER الذي يقوم بإنشاء تقارير كملفات Word ومنع بعض عناصر تحكم المحتوى في التقارير التي تم إنشاؤها والتي تم تكوينها باستخدام قالب Word.</span><span class="sxs-lookup"><span data-stu-id="b68d6-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="b68d6-111">يمكن تنفيذ هذه الخطوات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="b68d6-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b68d6-112">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="b68d6-112">Prerequisites</span></span>

<span data-ttu-id="b68d6-113">لإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوط في دلائل المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="b68d6-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="b68d6-114">تصميم تكوين لإنشاء التقارير بتنسيق OPENXML</span><span class="sxs-lookup"><span data-stu-id="b68d6-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="b68d6-115">إعادة استخدام تكوينات ER باستخدام قوالب Excel لإنشاء التقارير بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="b68d6-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="b68d6-116">عند إكمال الخطوات لدلائل المهام هذه، يتم إعداد العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="b68d6-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="b68d6-117">تنسيق ER **لعينة تقرير ورقة عمل** الذي تم تكوينه لإنشاء مستند بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="b68d6-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="b68d6-118">إصدار [مسودة](general-electronic-reporting.md#component-versioning) من تنسيق ER **لعينة تقرير ورقة العمل** الذي تم تعليمه كـ **قابل للتشغيل**</span><span class="sxs-lookup"><span data-stu-id="b68d6-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="b68d6-119">طريقة دفع **إلكترونية** تم تكوينها لاستخدام تنسيق ER **لعينة تقرير ورقة العمل** لمعالجة مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="b68d6-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="b68d6-120">يجب أيضًا تنزيل وحفظ القالب التالي لعينة التقرير:</span><span class="sxs-lookup"><span data-stu-id="b68d6-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="b68d6-121">القالب المرتبط 2 لتقرير الدفع (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="b68d6-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="b68d6-122">مراجعه قالب Word الذي تم تنزيله</span><span class="sxs-lookup"><span data-stu-id="b68d6-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="b68d6-123">في تطبيق سطح مكتب Word، قم بفتح ملف القالب **SampleVendPaymDocReportBounded2.docx** الذي قمت بتنزيله سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b68d6-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="b68d6-124">تحقق من احتواء ملف القالب على قسم ملخص يعرض إجمالي مبالغ الدفع الخاصة بكل كود عملة تم استيفاؤه في المدفوعات المعالجة.</span><span class="sxs-lookup"><span data-stu-id="b68d6-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="b68d6-125">يوجد قسم الملخص في جدول منفصل من مستند Word.</span><span class="sxs-lookup"><span data-stu-id="b68d6-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="b68d6-126">يحتوي الصف الأول من هذا الجدول على عناوين أعمدة الجدول كرأس للقسم.</span><span class="sxs-lookup"><span data-stu-id="b68d6-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="b68d6-127">يحتوي الصف الثاني من هذا الجدول على عنصر تحكم المحتوى المكرر كتفاصيل للقسم.</span><span class="sxs-lookup"><span data-stu-id="b68d6-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="b68d6-128">يتم تعيين عنصر تحكم المحتوى هذا إلى حقل **SummaryLines** في جزء XML المخصص لـ **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="b68d6-129">واستنادًا إلى هذا التعيين، يتم ربط عنصر تحكم المحتوى بعنصر **SummaryLines** لتنسيق ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="b68d6-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b68d6-130">يتم وضع علامة على عنصر تحكم المحتوي المتكرر بواسطة مفتاح **SummaryLines** الذي يتطابق مع الحقل الخاص بجزء XML المخصص الذي تم تعيينه إليه.</span><span class="sxs-lookup"><span data-stu-id="b68d6-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![تخطيط قالب Word](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="b68d6-132">تحديد تكوين التقارير الإلكترونية الموجود</span><span class="sxs-lookup"><span data-stu-id="b68d6-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="b68d6-133">بالنسبة للخطوات التالية، ستقوم بإعادة استخدام تكوين ER الموجود الذي قمت بتكوينه عند إكمال الخطوات في دلائل المهام المذكورة سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b68d6-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="b68d6-134">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b68d6-135">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b68d6-136">في صفحة **التكوينات**، في شجرة التكوينات، وسَّع **نموذج الدفع**، ثم حدد **عينة تقرير ورقة العمل**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="b68d6-137">حدد **المصمم** لتحرير إصدار المسودة لتنسيق ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="b68d6-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="b68d6-138">استبدال القالب الحالي بالقالب الجديد</span><span class="sxs-lookup"><span data-stu-id="b68d6-138">Replace the current template with the new template</span></span>

<span data-ttu-id="b68d6-139">في الوقت الحالي، يتم استخدام ملف SampleVendPaymDocReportBounded.docx كقالب لإنشاء المخرجات بتنسيق Word.</span><span class="sxs-lookup"><span data-stu-id="b68d6-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="b68d6-140">في الخطوات التالية، سوف تستبدل قالب Word هذا بقالب Word، SampleVendPaymDocReportBounded2.docx، الذي قمت بتنزيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="b68d6-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="b68d6-141">في صفحة **مصمم التنسيق**، حدد **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="b68d6-142">في الصفحة **المرفقات**، حدد **حذف** لإزالة القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="b68d6-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="b68d6-143">حدد **نعم** لتأكيد الحذف.</span><span class="sxs-lookup"><span data-stu-id="b68d6-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="b68d6-144">حدد **جديد** \> **ملف**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="b68d6-145">حدد **استعراض**، واستعرض بحثا عن الملف **SampleVendPaymDocReportBounded2.docx** الذي قمت بتنزيله سابقًا وحدده.</span><span class="sxs-lookup"><span data-stu-id="b68d6-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="b68d6-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-146">Select **OK**.</span></span>
7. <span data-ttu-id="b68d6-147">أغلق صفحة **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="b68d6-148">في صفحة **مصمم التنسيق**، في حقل **القالب**، أدخل أو حدد الملف **SampleVendPaymDocReportBounded2.docx**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="b68d6-149">تشغيل التنسيق لإنشاء مخرجات Word</span><span class="sxs-lookup"><span data-stu-id="b68d6-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="b68d6-150">انتقل إلى **الحسابات الدائنة** \> **المدفوعات‬** \> **دفتر يومية المدفوعات‬**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="b68d6-151">في صفحة **مدفوعات المورد**، من علامة تبويب **القائمة**، حدد كافة المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="b68d6-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="b68d6-152">تحديد **حاله الدفع**\>**بلا**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="b68d6-153">حدد **إنشاء المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="b68d6-154">في حقل **طريقة الدفع** حدد **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="b68d6-155">في الحقل **حساب البنك** حدد **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="b68d6-156">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-156">Select **OK**.</span></span>
8. <span data-ttu-id="b68d6-157">في مربع الحوار **معلمات التقرير الإلكتروني** ، حدد **موافق**، وقم بتحليل المخرجات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b68d6-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![المدفوعات للمعالجة في صفحة مدفوعات المورد](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="b68d6-159">يتم تقديم الإخراج بتنسيق Word ويحتوي على قسم الملخص.</span><span class="sxs-lookup"><span data-stu-id="b68d6-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="b68d6-160">تكوين التنسيق القابل للتحرير لمنع قسم الملخص</span><span class="sxs-lookup"><span data-stu-id="b68d6-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="b68d6-161">إذا أردت منع قسم الملخص في مستند تم إنشاؤه، استنادا إلى طلب المستخدم الذي يقوم بتشغيل تنسيق ER هذا، فيجب تعديل تنسيق ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="b68d6-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="b68d6-162">انتقل إلى **إدارة المؤسسات**\> **مساحات العمل** \> **التقارير الإلكترونية**، وافتح إصدار المسودة لتنسيق ER للتحرير.</span><span class="sxs-lookup"><span data-stu-id="b68d6-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="b68d6-163">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="b68d6-164">في صفحة **التكوينات**، في شجرة التكوينات، قم بتوسيع **نموذج الدفع** \> **عينة تقرير ورقة العمل**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="b68d6-165">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-165">Select **Designer**.</span></span>
5. <span data-ttu-id="b68d6-166">في صفحة **مصمم التنسيق** ، قم بتوسيع **Word**، وحدد **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="b68d6-167">في علامة التبويب **التعيين**، قم بإضافة مصدر بيانات جديد لسؤال المستخدم، في وقت التشغيل، عن ما إذا كان يجب منع قسم الملخص أم لا:</span><span class="sxs-lookup"><span data-stu-id="b68d6-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="b68d6-168">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="b68d6-169">في مربع الحوار **إضافة مصدر بيانات**، حدد **معلمة إدخال عام/إدخال المستخدم** لفتح مربع الحوار **خصائص مصدر البيانات 'معلمة إدخال المستخدم'**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="b68d6-170">في الحقل **الاسم** ، أدخل **‏uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="b68d6-171">في حقل **التسمية**، أدخل **منح قسم الملخص**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="b68d6-172">في حقل **اسم نوع بيانات العمليات** ، حدد أو أدخل **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="b68d6-173">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-173">Select **OK**.</span></span>

7. <span data-ttu-id="b68d6-174">أضف مصدر بيانات جديد لنوع تكرار التطبيق **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="b68d6-175">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="b68d6-176">في مربع الحوار **إضافة مصدر بيانات** حدد **Dynamics 365 for Operations\تعداد** لفتح مربع الحوار **خصائص مصدر البيانات 'تعداد'**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="b68d6-177">في الحقل **الاسم**، أدخل **‏enumNoYes**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="b68d6-178">في حقل **التسمية**، أدخل **خيارات المنع**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="b68d6-179">في حقل **اسم نوع بيانات العمليات** ، حدد أو أدخل **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="b68d6-180">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-180">Select **OK**.</span></span>

8. <span data-ttu-id="b68d6-181">بالنسبة لعنصر التنسيق **SummaryLines** المحدد، قم بتكوين المعادلة لتحديد متى يتم منع عنصر تحكم محتوى Word المقترن بعنصر التنسيق المحدد:</span><span class="sxs-lookup"><span data-stu-id="b68d6-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="b68d6-182">ضمن علامة التبويب **تعيين**، في قسم **تمت الإزالة**، حدد **تحرير** لفتح صفحة **[مصمم المعادلة](general-electronic-reporting-formula-designer.md)**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="b68d6-183">في حقل **المعادلة**، أدخل المعادلة `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="b68d6-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="b68d6-184">حدد **حفظ** وأغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b68d6-185">سيتم تطبيق هذه المعادلة على مستند تم إنشاؤه **بعد تشغيل كافة عناصر التنسيق الأخرى**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="b68d6-186">لتطبيق هذه المعادلة، يوجد عنصر تحكم محتوى Word الذي تم تعليمه كعنصر تنسيق تم تكوين الصيغة لـ (**SummaryLines** في هذه الحالة) في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="b68d6-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="b68d6-187">يتم بعد ذلك إزالة عنصر تحكم المحتوى هذا بشكل كامل، مع الصف الموجود في جدول Word الذي يحمل هذا العنصر.</span><span class="sxs-lookup"><span data-stu-id="b68d6-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="b68d6-188">وتتم إزالة صف التفاصيل الخاص بقسم الملخص من المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="b68d6-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="b68d6-189">في وقت التصميم، قد تقوم بتكوين المعادلة **تمت الإزالة** لعنصر التنسيق، بالرغم من عدم وجود عنصر تحكم محتويات في قالب Word الذي تستخدمه يحتوي على علامة تطابق اسم عنصر التنسيق الذي تم تكوين خاصية **تمت الإزالة** له.</span><span class="sxs-lookup"><span data-stu-id="b68d6-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="b68d6-190">عند التحقق من صحة التنسيق في وقت التصميم، فإنك تتلقي [تحذيرا](er-components-inspections.md#i14) حول عدم التوافق هذا.</span><span class="sxs-lookup"><span data-stu-id="b68d6-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="b68d6-191">في وقت التشغيل، يتم عرض استثناء في حالة عدم وجود عنصر تحكم المحتوى في قالب Word الذي تستخدمه يحتوي على علامة تطابق اسم عنصر التنسيق الذي تم تكوين خاصية **تمت الإزالة** له.</span><span class="sxs-lookup"><span data-stu-id="b68d6-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="b68d6-192">ضمن علامة التبويب **تعيين** في قسم **تمت الإزالة**، قم بتعيين خيار **مع الأصل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b68d6-193">يجب تعيين هذا الخيار على **نعم** لإزالة جدول Word بأكمله مثل الكائن الأصلي للصف الذي يحتوي على تفاصيل قسم الملخص.</span><span class="sxs-lookup"><span data-stu-id="b68d6-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="b68d6-194">إذا قمت بتعيين هذا الخيار إلى **لا**، سيبقي صف رأس القسم في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="b68d6-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="b68d6-195">حدد **حفظ** لحفظ تغييراتك على التنسيق القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="b68d6-195">Select **Save** to save your changes to the editable format.</span></span>

    ![الإخراج الناتج بتنسيق Word](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="b68d6-197">تشغيل التنسيق المعدل لإنشاء مخرجات Word</span><span class="sxs-lookup"><span data-stu-id="b68d6-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="b68d6-198">انتقل إلى **الحسابات الدائنة** \> **المدفوعات‬** \> **دفتر يومية المدفوعات‬**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="b68d6-199">حدد دفترة يومية الدفع الذي أنشأته، ثم حدد **السطور**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="b68d6-200">في صفحة **مدفوعات المورد**، حدد كافة الصفوف، ثم حدد **حالة الدفع** \> **بلا**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="b68d6-201">حدد **إنشاء المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="b68d6-202">في حقل **طريقة الدفع** حدد **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="b68d6-203">في الحقل **حساب البنك** حدد **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="b68d6-204">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-204">Select **OK**.</span></span>
8. <span data-ttu-id="b68d6-205">في مربع الحوار **معلمات التقارير الإلكترونية**، في حقل **منع قسم الملخص**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b68d6-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="b68d6-206">حدد **موافق**، وقم بتحليل المخرجات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="b68d6-206">Select **OK**, and analyze the generated output.</span></span>

    ![الإخراج الناتج بتنسيق Word](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="b68d6-208">لاحظ أن الإخراج لا يحتوي على قسم الملخص، لأنه تم منعه.</span><span class="sxs-lookup"><span data-stu-id="b68d6-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b68d6-209">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b68d6-209">Additional resources</span></span>

- [<span data-ttu-id="b68d6-210">تصميم تكوين لإنشاء التقارير بتنسيق OPENXML</span><span class="sxs-lookup"><span data-stu-id="b68d6-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="b68d6-211">تصميم تكوين ER جديد لإنشاء التقارير بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="b68d6-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="b68d6-212">إعادة استخدام تكوينات ER باستخدام قوالب Excel لإنشاء التقارير بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="b68d6-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="b68d6-213">فحص مكون التقارير الإلكترونية الذي تم تكوينه لمنع مشكلات وقت التشغيل</span><span class="sxs-lookup"><span data-stu-id="b68d6-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]