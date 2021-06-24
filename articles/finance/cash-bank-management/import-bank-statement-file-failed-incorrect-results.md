---
title: استكشاف أخطاء استيراد ملفات كشوفات الحسابات البنكية وإصلاحها
description: من الضروري أن يتطابق ملف كشف الحساب البنكي من البنك مع التخطيط الذي يدعمه Microsoft Dynamics 365 Finance. بسبب المعايير الصارمة الموضوعة على كشوفات الحسابات البنكية، ستعمل معظم عمليات الدمج بشكل صحيح. ومع ذلك، يتعذر أحيانًا استيراد ملف كشف الحساب أو تكون نتائجه غير صحيحة. بشكل عام، تحدث هذه المشاكل بسبب اختلافات طفيفة في ملف كشف الحساب البنكي. توضح هذه المقالة كيفية حل هذه الاختلافات وحل المشكلات.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188548"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="ca325-107">استكشاف أخطاء استيراد ملفات كشوفات الحسابات البنكية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="ca325-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca325-108">من الضروري أن يتطابق ملف كشف الحساب البنكي من البنك مع التخطيط الذي يدعمه Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ca325-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="ca325-109">بسبب المعايير الصارمة الموضوعة على كشوفات الحسابات البنكية، ستعمل معظم عمليات الدمج بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="ca325-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="ca325-110">ومع ذلك، يتعذر أحيانًا استيراد ملف كشف الحساب أو تكون نتائجه غير صحيحة.</span><span class="sxs-lookup"><span data-stu-id="ca325-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="ca325-111">بشكل عام، تحدث هذه المشاكل بسبب اختلافات طفيفة في ملف كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="ca325-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="ca325-112">توضح هذه المقالة كيفية حل هذه الاختلافات وحل المشكلات.</span><span class="sxs-lookup"><span data-stu-id="ca325-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="ca325-113">ما هو الخطأ؟</span><span class="sxs-lookup"><span data-stu-id="ca325-113">What is the error?</span></span>

<span data-ttu-id="ca325-114">بعد أن تحاول استيراد ملف كشف حساب بنكي، انتقل إلى محفوظات مهمة إدارة البيانات وتفاصيل التنفيذ الخاصة بها للعثور على الخطأ.</span><span class="sxs-lookup"><span data-stu-id="ca325-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="ca325-115">بإمكان الخطأ أن يكون مساعدًا عن طريق التأشير إلى كشف الحساب البنكي أو الرصيد أو بند في الكشف.</span><span class="sxs-lookup"><span data-stu-id="ca325-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="ca325-116">ومع ذلك، من غير المحتمل توفير ما يكفي من المعلومات لمساعدتك في تحديد الحقل أو العنصر الذي تسبب في حدوث المشكلة.</span><span class="sxs-lookup"><span data-stu-id="ca325-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="ca325-117">يمكن أن تتداخل كشوف الحسابات المصرفية المستوردة لفترة زمنية واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="ca325-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="ca325-118">على سبيل المثال ، إذا انتهى البيان في الساعة 12:00 صباحًا في 1 كانون الثاني (يناير) 2021 ، فيمكن أن يكون تاريخ البدء للبيان التالي هو 12:00 صباحًا في 1 كانون الثاني (يناير) 2021 12:00:00 صباحًا.</span><span class="sxs-lookup"><span data-stu-id="ca325-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="ca325-119">ما هي الاختلافات؟</span><span class="sxs-lookup"><span data-stu-id="ca325-119">What are the differences?</span></span>
<span data-ttu-id="ca325-120">قارن تعريف تخطيط الملف البنكي بتعريف استيراد Finance، ودوّن أي اختلافات في الحقول والعناصر.</span><span class="sxs-lookup"><span data-stu-id="ca325-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="ca325-121">‏قارن ملف كشف الحساب البنكي بملف Finance النموذجي ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="ca325-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="ca325-122">في ملفات ISO20022، يجب أن يكون من السهل رؤية الاختلافات.‬</span><span class="sxs-lookup"><span data-stu-id="ca325-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="ca325-123">فروق المنطقة الزمنية على كشوف الحسابات البنكية المستوردة</span><span class="sxs-lookup"><span data-stu-id="ca325-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="ca325-124">بإمكان قيم التاريخ والوقت في ملف الاستيراد أن تختلف عن قيم التاريخ والوقت التي تظهر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca325-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="ca325-125">لمنع حدوث هذا الاختلاف، ادخل تفضيل المنطقة الزمنية في الصفحة **تكوين مصادر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="ca325-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="ca325-126">لمزيد من المعلومات حول إدخال تفضيل المنطقة الزمنية، راجع [إعداد عملية استيراد التسوية البنكية المتقدمة](set-up-advanced-bank-reconciliation-import-process.md)</span><span class="sxs-lookup"><span data-stu-id="ca325-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="ca325-127">التحويلات</span><span class="sxs-lookup"><span data-stu-id="ca325-127">Transformations</span></span>
<span data-ttu-id="ca325-128">بشكل عام، يجب إجراء التغيير في أحد التحويلات الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="ca325-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="ca325-129">تتم كتابة كل تحويل لمعيار محدد.</span><span class="sxs-lookup"><span data-stu-id="ca325-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="ca325-130">اسم المورد</span><span class="sxs-lookup"><span data-stu-id="ca325-130">Resource name</span></span>                                         | <span data-ttu-id="ca325-131">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="ca325-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="ca325-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="ca325-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="ca325-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="ca325-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="ca325-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="ca325-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="ca325-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="ca325-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="ca325-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="ca325-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="ca325-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="ca325-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="ca325-138">تحويلات التصحيح</span><span class="sxs-lookup"><span data-stu-id="ca325-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="ca325-139">تعديل الملفات BAI2 وMT940</span><span class="sxs-lookup"><span data-stu-id="ca325-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="ca325-140">إن الملفات BAI2 وMT940 عبارة عن ملفات نصية وتتطلب تعديلاً لتمكين تصحيح تحويلات لغة صفحات الأنماط الموسعة (XSLT).</span><span class="sxs-lookup"><span data-stu-id="ca325-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="ca325-141">يقوم البرنامج بإجراء هذا التعديل عند استيراد ملف.</span><span class="sxs-lookup"><span data-stu-id="ca325-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="ca325-142">أنشئ ملف XML وانسخ النص التالي فيه.</span><span class="sxs-lookup"><span data-stu-id="ca325-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="ca325-143">انسخ محتويات ملف كشف الحساب البنكي، والصقها في ملف XML لكي تحل محل **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="ca325-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="ca325-144">تصحيح XSLT</span><span class="sxs-lookup"><span data-stu-id="ca325-144">Debug the XSLT</span></span>

<span data-ttu-id="ca325-145">لمزيد من المعلومات، راجع <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="ca325-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="ca325-146">ابدأ تشغيل Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca325-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="ca325-147">أنشئ تطبيق وحدة تحكم.</span><span class="sxs-lookup"><span data-stu-id="ca325-147">Create a console application.</span></span>
3.  <span data-ttu-id="ca325-148">افتح XSLT المناسب.</span><span class="sxs-lookup"><span data-stu-id="ca325-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="ca325-149">انقر فوق XLST وصفحة خصائصه.</span><span class="sxs-lookup"><span data-stu-id="ca325-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="ca325-150">عيّن الإدخال إلى موقع ملف كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="ca325-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="ca325-151">حدد موقعًا واسم ملف للإخراج.</span><span class="sxs-lookup"><span data-stu-id="ca325-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="ca325-152">عيّن نقاط التوقف المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ca325-152">Set the required break points.</span></span>
8.  <span data-ttu-id="ca325-153">في القائمة، انقر فوق **XML** &gt; **بدء تصحيح XSLT**.</span><span class="sxs-lookup"><span data-stu-id="ca325-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="ca325-154">تنسيق إخراج XSLT</span><span class="sxs-lookup"><span data-stu-id="ca325-154">Format the XSLT output</span></span>

<span data-ttu-id="ca325-155">تقوم عملية التحويل عند تشغيلها بإنشاء ملف إخراج يمكنك عرضه في Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca325-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="ca325-156">استخدم Ctrl + A وCtrl + K وCtrl + D لتنسيق ملف الإخراج بسرعة.</span><span class="sxs-lookup"><span data-stu-id="ca325-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="ca325-157">ضبط التحويل</span><span class="sxs-lookup"><span data-stu-id="ca325-157">Adjust the transformation</span></span>

<span data-ttu-id="ca325-158">اضبط التحويل للحصول على العنصر أو الحقل الملائم في ملف كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="ca325-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="ca325-159">ثم عيّن هذا الحقل أو العنصر إلى عنصر Finance المناسب.</span><span class="sxs-lookup"><span data-stu-id="ca325-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="ca325-160">مؤشر الديون/الائتمانات</span><span class="sxs-lookup"><span data-stu-id="ca325-160">Debit/credit indicator</span></span>

<span data-ttu-id="ca325-161">في بعض الأحيان، قد يتم استيراد الديون كائتمانات، وقد يتم استيراد الائتمانات كديون.</span><span class="sxs-lookup"><span data-stu-id="ca325-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="ca325-162">لحل هذه المشكلة، يجب تغيير XSLT المناسب.</span><span class="sxs-lookup"><span data-stu-id="ca325-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="ca325-163">إذا كانت كشوف الحسابات البنكية تأتي من بنوك متعددة، فتأكد من أنها كلها تستخدم منهج الديون/الائتمانات نفسه أو أنشئ تحويلات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="ca325-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="ca325-164">قالب BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="ca325-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="ca325-165">قالب ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="ca325-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="ca325-166">قالب MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="ca325-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="ca325-167">أمثلة عن تنسيقات كشوف الحسابات البنكية والتخطيطات التقنية</span><span class="sxs-lookup"><span data-stu-id="ca325-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="ca325-168">يسرد الجدول التالي أمثلة على تعريفات التخطيط التقني لملفات استيراد التسوية البنكية المتقدمة وثلاثة ملفات أمثلة عن كشوفات الحسابات البنكية ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="ca325-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="ca325-169">يمكنك تنزيل أمثلة الملفات والتخطيطات الفنية هنا: [استيراد أمثلة الملفات](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="ca325-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="ca325-170">تعريف التخطيط التقني</span><span class="sxs-lookup"><span data-stu-id="ca325-170">Technical layout definition</span></span>                             | <span data-ttu-id="ca325-171">ملف مثال عن كشف الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="ca325-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="ca325-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="ca325-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="ca325-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="ca325-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="ca325-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="ca325-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="ca325-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="ca325-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="ca325-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="ca325-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="ca325-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="ca325-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
