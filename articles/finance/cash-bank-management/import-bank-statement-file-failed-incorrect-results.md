---
title: استكشاف أخطاء استيراد ملفات كشوفات الحسابات البنكية وإصلاحها
description: من الضروري أن يتطابق ملف كشف الحساب البنكي من البنك مع التخطيط الذي يدعمه Microsoft Dynamics 365 Finance. بسبب المعايير الصارمة الموضوعة على كشوفات الحسابات البنكية، ستعمل معظم عمليات الدمج بشكل صحيح. ومع ذلك، يتعذر أحيانًا استيراد ملف كشف الحساب أو تكون نتائجه غير صحيحة. بشكل عام، تحدث هذه المشاكل بسبب اختلافات طفيفة في ملف كشف الحساب البنكي. توضح هذه المقالة كيفية حل هذه الاختلافات وحل المشكلات.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adea87b6341860a9aa1625811270274e02a88b26
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978929"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="523d8-107">استكشاف أخطاء استيراد ملفات كشوفات الحسابات البنكية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="523d8-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="523d8-108">من الضروري أن يتطابق ملف كشف الحساب البنكي من البنك مع التخطيط الذي يدعمه Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="523d8-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="523d8-109">بسبب المعايير الصارمة الموضوعة على كشوفات الحسابات البنكية، ستعمل معظم عمليات الدمج بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="523d8-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="523d8-110">ومع ذلك، يتعذر أحيانًا استيراد ملف كشف الحساب أو تكون نتائجه غير صحيحة.</span><span class="sxs-lookup"><span data-stu-id="523d8-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="523d8-111">بشكل عام، تحدث هذه المشاكل بسبب اختلافات طفيفة في ملف كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="523d8-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="523d8-112">توضح هذه المقالة كيفية حل هذه الاختلافات وحل المشكلات.</span><span class="sxs-lookup"><span data-stu-id="523d8-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="523d8-113">ما هو الخطأ؟</span><span class="sxs-lookup"><span data-stu-id="523d8-113">What is the error?</span></span>
------------------

<span data-ttu-id="523d8-114">بعد أن تحاول استيراد ملف كشف حساب بنكي، انتقل إلى محفوظات مهمة إدارة البيانات وتفاصيل التنفيذ الخاصة بها للعثور على الخطأ.</span><span class="sxs-lookup"><span data-stu-id="523d8-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="523d8-115">بإمكان الخطأ أن يكون مساعدًا عن طريق التأشير إلى كشف الحساب البنكي أو الرصيد أو بند في الكشف.</span><span class="sxs-lookup"><span data-stu-id="523d8-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="523d8-116">ومع ذلك، من غير المحتمل توفير ما يكفي من المعلومات لمساعدتك في تحديد الحقل أو العنصر الذي تسبب في حدوث المشكلة.</span><span class="sxs-lookup"><span data-stu-id="523d8-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="523d8-117">ما هي الاختلافات؟</span><span class="sxs-lookup"><span data-stu-id="523d8-117">What are the differences?</span></span>
<span data-ttu-id="523d8-118">قارن تعريف تخطيط الملف البنكي بتعريف استيراد Finance، ودوّن أي اختلافات في الحقول والعناصر.</span><span class="sxs-lookup"><span data-stu-id="523d8-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="523d8-119">‏قارن ملف كشف الحساب البنكي بملف Finance النموذجي ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="523d8-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="523d8-120">في ملفات ISO20022، يجب أن يكون من السهل رؤية الاختلافات.‬</span><span class="sxs-lookup"><span data-stu-id="523d8-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="523d8-121">فروق المنطقة الزمنية على كشوف الحسابات البنكية المستوردة</span><span class="sxs-lookup"><span data-stu-id="523d8-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="523d8-122">بإمكان قيم التاريخ والوقت في ملف الاستيراد أن تختلف عن قيم التاريخ والوقت التي تظهر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="523d8-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="523d8-123">لمنع حدوث هذا الاختلاف، ادخل تفضيل المنطقة الزمنية في الصفحة **تكوين مصادر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="523d8-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="523d8-124">راجع [إعداد عملية استيراد التسوية البنكية المتقدمة](set-up-advanced-bank-reconciliation-import-process.md) لمزيد من المعلومات حول إدخال تفضيل المنطقة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="523d8-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="523d8-125">التحويلات</span><span class="sxs-lookup"><span data-stu-id="523d8-125">Transformations</span></span>
<span data-ttu-id="523d8-126">بشكل عام، يجب إجراء التغيير في أحد التحويلات الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="523d8-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="523d8-127">تتم كتابة كل تحويل لمعيار محدد.</span><span class="sxs-lookup"><span data-stu-id="523d8-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="523d8-128">اسم المورد</span><span class="sxs-lookup"><span data-stu-id="523d8-128">Resource name</span></span>                                         | <span data-ttu-id="523d8-129">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="523d8-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="523d8-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="523d8-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="523d8-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="523d8-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="523d8-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="523d8-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="523d8-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="523d8-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="523d8-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="523d8-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="523d8-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="523d8-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="523d8-136">تحويلات التصحيح</span><span class="sxs-lookup"><span data-stu-id="523d8-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="523d8-137">تعديل الملفات BAI2 وMT940</span><span class="sxs-lookup"><span data-stu-id="523d8-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="523d8-138">إن الملفات BAI2 وMT940 عبارة عن ملفات نصية وتتطلب تعديلاً لتمكين تصحيح تحويلات لغة صفحات الأنماط الموسعة (XSLT).</span><span class="sxs-lookup"><span data-stu-id="523d8-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="523d8-139">يقوم البرنامج بإجراء هذا التعديل عند استيراد ملف.</span><span class="sxs-lookup"><span data-stu-id="523d8-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="523d8-140">أنشئ ملف XML وانسخ النص التالي فيه.</span><span class="sxs-lookup"><span data-stu-id="523d8-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="523d8-141">انسخ محتويات ملف كشف الحساب البنكي، والصقها في ملف XML لكي تحل محل **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="523d8-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="523d8-142">تصحيح XSLT</span><span class="sxs-lookup"><span data-stu-id="523d8-142">Debug the XSLT</span></span>

<span data-ttu-id="523d8-143">لمزيد من المعلومات، راجع <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="523d8-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="523d8-144">ابدأ تشغيل Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="523d8-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="523d8-145">أنشئ تطبيق وحدة تحكم.</span><span class="sxs-lookup"><span data-stu-id="523d8-145">Create a console application.</span></span>
3.  <span data-ttu-id="523d8-146">افتح XSLT المناسب.</span><span class="sxs-lookup"><span data-stu-id="523d8-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="523d8-147">انقر فوق XLST وصفحة خصائصه.</span><span class="sxs-lookup"><span data-stu-id="523d8-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="523d8-148">عيّن الإدخال إلى موقع ملف كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="523d8-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="523d8-149">حدد موقعًا واسم ملف للإخراج.</span><span class="sxs-lookup"><span data-stu-id="523d8-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="523d8-150">عيّن نقاط التوقف المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="523d8-150">Set the required break points.</span></span>
8.  <span data-ttu-id="523d8-151">في القائمة، انقر فوق **XML** &gt; **بدء تصحيح XSLT**.</span><span class="sxs-lookup"><span data-stu-id="523d8-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="523d8-152">تنسيق إخراج XSLT</span><span class="sxs-lookup"><span data-stu-id="523d8-152">Format the XSLT output</span></span>

<span data-ttu-id="523d8-153">تقوم عملية التحويل عند تشغيلها بإنشاء ملف إخراج يمكنك عرضه في Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="523d8-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="523d8-154">استخدم Ctrl + A وCtrl + K وCtrl + D لتنسيق ملف الإخراج بسرعة.</span><span class="sxs-lookup"><span data-stu-id="523d8-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="523d8-155">ضبط التحويل</span><span class="sxs-lookup"><span data-stu-id="523d8-155">Adjust the transformation</span></span>

<span data-ttu-id="523d8-156">اضبط التحويل للحصول على العنصر أو الحقل الملائم في ملف كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="523d8-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="523d8-157">ثم عيّن هذا الحقل أو العنصر إلى عنصر Finance المناسب.</span><span class="sxs-lookup"><span data-stu-id="523d8-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="523d8-158">مؤشر الديون/الائتمانات</span><span class="sxs-lookup"><span data-stu-id="523d8-158">Debit/credit indicator</span></span>

<span data-ttu-id="523d8-159">في بعض الأحيان، قد يتم استيراد الديون كائتمانات، وقد يتم استيراد الائتمانات كديون.</span><span class="sxs-lookup"><span data-stu-id="523d8-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="523d8-160">لحل هذه المشكلة، يجب تغيير XSLT المناسب.</span><span class="sxs-lookup"><span data-stu-id="523d8-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="523d8-161">إذا كانت كشوف الحسابات البنكية تأتي من بنوك متعددة، فتأكد من أنها كلها تستخدم منهج الديون/الائتمانات نفسه أو أنشئ تحويلات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="523d8-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="523d8-162">قالب BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="523d8-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="523d8-163">قالب ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="523d8-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="523d8-164">قالب MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="523d8-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="523d8-165">أمثلة عن تنسيقات كشوف الحسابات البنكية والتخطيطات التقنية</span><span class="sxs-lookup"><span data-stu-id="523d8-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="523d8-166">يسرد الجدول التالي أمثلة على تعريفات التخطيط التقني لملفات استيراد التسوية البنكية المتقدمة وثلاثة ملفات أمثلة عن كشوفات الحسابات البنكية ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="523d8-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="523d8-167">يمكنك تنزيل أمثلة الملفات والتخطيطات الفنية هنا:https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="523d8-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="523d8-168">تعريف التخطيط التقني</span><span class="sxs-lookup"><span data-stu-id="523d8-168">Technical layout definition</span></span>                             | <span data-ttu-id="523d8-169">ملف مثال عن كشف الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="523d8-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="523d8-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="523d8-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="523d8-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="523d8-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="523d8-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="523d8-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="523d8-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="523d8-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="523d8-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="523d8-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="523d8-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="523d8-175">BAI2StatementExample</span></span>                 |





