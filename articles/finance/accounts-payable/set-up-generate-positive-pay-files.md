---
title: إعداد ملفات الدفع الإيجابي وإنشاؤها
description: يشرح هذا الموضوع كيفية إعداد الدفع الإيجابي وإنشاء ملفات الدفع الإيجابي.
author: panolte
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0984710220171f36a520e471c6c55bf12d97675b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971999"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="b7464-103">إعداد ملفات الدفع الإيجابي وإنشاؤها</span><span class="sxs-lookup"><span data-stu-id="b7464-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7464-104">يشرح هذا الموضوع كيفية إعداد الدفع الإيجابي وإنشاء ملفات الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="b7464-105">إعداد الدفع الإيجابي لإنشاء قائمة إلكترونية بالشيكات التي يتم توفيرها للبنك.</span><span class="sxs-lookup"><span data-stu-id="b7464-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="b7464-106">بعد ذلك، عندما يتم تقديم الشيك إلى البنك، يقارنه البنك بقائمة الشيكات.</span><span class="sxs-lookup"><span data-stu-id="b7464-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="b7464-107">إذا تطابق الشيك مع شيك آخر في القائمة، فسيقوم البنك بمخالصته.</span><span class="sxs-lookup"><span data-stu-id="b7464-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="b7464-108">أما إذا لم يتطابق الشيك لم تطابق مع أي شيك آخر في القائمة، فسيحتفظ البنك به لمراجعته.</span><span class="sxs-lookup"><span data-stu-id="b7464-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="b7464-109">الأمان لملفات الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-109">Security for positive pay files</span></span>
<span data-ttu-id="b7464-110">يمكن أن تحتوي ملفات الدفع الإيجابي على معلومات هامة حول المستفيدين ومبالغ الشيكات.</span><span class="sxs-lookup"><span data-stu-id="b7464-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="b7464-111">لذلك، تأكد من استخدام تدابير أمنية مناسبة اعتبارًا من وقت إنشاء الملفات وحى استلام البنك لها.</span><span class="sxs-lookup"><span data-stu-id="b7464-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="b7464-112">يتم تنزيل ملفات الدفع الإيجابي إلى الموقع المحدد بواسطة مستعرض ويب.</span><span class="sxs-lookup"><span data-stu-id="b7464-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="b7464-113">ونظرًا لإمكانية احتواء ملفات الدفع الإيجابي على معلومات حساسة، من الضروري أن يقتصر حق الوصول لإنشاء وعرض هذه المعلومات في Microsoft Dynamics 365 Finance على المستخدمين المخوّلين فقط.</span><span class="sxs-lookup"><span data-stu-id="b7464-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="b7464-114">استخدم الجدول التالي للمساعدة في تحديد الامتيازات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b7464-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7464-115">المهمة</span><span class="sxs-lookup"><span data-stu-id="b7464-115">Task</span></span></th>
<th><span data-ttu-id="b7464-116">الامتياز</span><span class="sxs-lookup"><span data-stu-id="b7464-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7464-117">إنشاء ملفات الدفع الإيجابي من صفحة قائمة <strong>الحسابات البنكية</strong> أو صفحة <strong>الحسابات البنكية</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7464-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7464-118"><strong>الاحتفاظ بمعلومات الدفع الإيجابي البنكي</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="b7464-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="b7464-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="b7464-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7464-120">إنشاء ملفات دفع إيجابي لعدة كيانات قانونية وحسابات بنكية من صفحة <strong>إنشاء ملف دفع إيجابي‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7464-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7464-121"><strong>الاحتفاظ بمعلومات الدفع الإيجابي البنكي</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="b7464-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="b7464-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="b7464-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7464-123">عرض ملفات الدفع الإيجابي في صفحة <strong>ملخص ملف الدفع الإيجابي</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7464-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="b7464-124"><strong>عرض معلومات الدفع الإيجابي البنكي لكيانات قانونية متعددة</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="b7464-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7464-125">تأكيد ملف الدفع الإيجابي في صفحة <strong>ملخص ملف الدفع الإيجابي</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7464-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="b7464-126"><strong>تأكيد ملف الدفع الإيجابي</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="b7464-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7464-127">استدعاء ملف الدفع الإيجابي في صفحة <strong>ملخص ملف الدفع الإيجابي</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7464-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="b7464-128"><strong>استدعاء ملف دفع إيجابي</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="b7464-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="b7464-129">إعداد تنسيق الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-129">Set up a positive pay format</span></span>
<span data-ttu-id="b7464-130">يتم إنشاء ملفات الدفع الإيجابي باستخدام كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="b7464-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="b7464-131">قبل إنشاء ملف الدفع الإيجابي، يجب إعداد تنسيق إدخال التحويل الذي سيتم استخدامه لترجمة معلومات الشيك إلى تنسيق يمكنه التواصل مع البنك.</span><span class="sxs-lookup"><span data-stu-id="b7464-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="b7464-132">في صفحة **تنسيق الدفع الإيجابي**، يمكنك إنشاء معرف تنسيق الملف ووصف لهذا التنسيق.</span><span class="sxs-lookup"><span data-stu-id="b7464-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="b7464-133">يجب أن يكون تنسيق إدخال التحويل عبارة عن ملف من نوع XML.</span><span class="sxs-lookup"><span data-stu-id="b7464-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="b7464-134">يتوقف التنسيق المحدد على ملف التحويل الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="b7464-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="b7464-135">على سبيل المثال، يستخدم ملف تحويل لغة صفحات الأنماط الموسعة (XSLT) النموذجي الذي تم توفيره تنسيق **XML-Element**.</span><span class="sxs-lookup"><span data-stu-id="b7464-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="b7464-136">استخدم الإجراء **تحميل الملف المستخدم في التحويل‬** لتحديد موقع ملف التحويل للتنسيق الذي يتطلبه البنك الذي تتعامل معه.</span><span class="sxs-lookup"><span data-stu-id="b7464-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="b7464-137">على سبيل المثال: ملف XSLT لملف الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="b7464-138">تعيين تنسيق الدفع الإيجابي لحساب بنكي</span><span class="sxs-lookup"><span data-stu-id="b7464-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="b7464-139">لكل حساب بنكي تريد إنشاء معلومات دفع إيجابي له، يجب تعيين تنسيق الدفع الإيجابي الذي حددته في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="b7464-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="b7464-140">في صفحة **الحسابات البنكية**، حدد تنسيق الدفع الإيجابي الذي يتوافق مع الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="b7464-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="b7464-141">في الحقل **تاريخ بدء الدفع الإيجابي‬**  التاريخ الأول لإنشاء ملفات الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="b7464-142">من الضروري إدخال تاريخ في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="b7464-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="b7464-143">خلاف ذلك، سيتضمن ملف الدفع الإيجابي الأول الذي تقوم بإنشائه كل الشيكات التي تم إنشاؤها لهذا الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="b7464-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="b7464-144">تعيين تسلسل رقمي لملفات الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="b7464-145">يجب أن يكون لكل ملف دفع إيجابي رقم فريد.</span><span class="sxs-lookup"><span data-stu-id="b7464-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="b7464-146">استخدم علامة التبويب **التسلسلات الرقمية‬** في صفحة **محددات إدارة البنك والنقد‬** لإنشاء تسلسل رقمي لملفات الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="b7464-147">إنشاء ملف دفع إيجابي لحساب بنكي واحد</span><span class="sxs-lookup"><span data-stu-id="b7464-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="b7464-148">يمكنك إنشاء ملف دفع إيجابي لكيان قانوني واحد وحساب بنكي واحد.</span><span class="sxs-lookup"><span data-stu-id="b7464-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="b7464-149">للحصول على معلومات حول كيفية إنشاء ملفات الدفع الإيجابي لكيانات قانونية وحسابات بنكية متعددة في نفس الوقت، راجع القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="b7464-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="b7464-150">لإنشاء ملف دفع إيجابي لكيان قانوني واحد وحساب بنكي واحد، افتح مربع الحوار **إنشاء ملف دفع إيجابي** من صفحة **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="b7464-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="b7464-151">في حقل **تاريخ الانقطاع‬**، أدخل تاريخ الشيك الأخير لتضمينه في ملف الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="b7464-152">يتم تضمين كافة الشيكات غير المضمنة في ملف دفع إيجابي بنهاية تاريخ الشيك هذا في الملف.</span><span class="sxs-lookup"><span data-stu-id="b7464-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="b7464-153">إنشاء ملف دفع إيجابي لحسابات بنكية متعددة</span><span class="sxs-lookup"><span data-stu-id="b7464-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="b7464-154">لإنشاء ملف دفع إيجابي لحسابات بنكية متعددة، استخدم المهمة الدورية **إنشاء ملف دفع إيجابي**.</span><span class="sxs-lookup"><span data-stu-id="b7464-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="b7464-155">حدد تنسيق ملف الدفع الإيجابي، وحدد إذا كنت تريد إنشاء ملف الدفع الإيجابي لجميع الكيانات القانونية أو لكيان قانوني محدد.</span><span class="sxs-lookup"><span data-stu-id="b7464-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="b7464-156">يمكنك أيضًا إنشاء ملف الدفع الإيجابي لجميع الحسابات البنكية التي تستخدم تنسيق الدفع الإيجابي المحدد أو لحساب بنكي محدد.</span><span class="sxs-lookup"><span data-stu-id="b7464-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="b7464-157">في حقل **تاريخ الانقطاع‬**، أدخل تاريخ الشيك الأخير لتضمينه في ملف الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="b7464-158">يتم تضمين كافة الشيكات غير المضمنة في ملف دفع إيجابي بنهاية تاريخ الشيك هذا في الملف.</span><span class="sxs-lookup"><span data-stu-id="b7464-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="b7464-159">عرض نتائج إنشاء ملف الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="b7464-160">بعد إنشاء ملف الدفع الإيجابي، يمكنك عرض النتائج في صفحة **ملخص ملف الدفع الإيجابي**.</span><span class="sxs-lookup"><span data-stu-id="b7464-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="b7464-161">لعرض تفاصيل شيكات فردية، استخدم صفحة **ملف الدفع الإيجابي**.</span><span class="sxs-lookup"><span data-stu-id="b7464-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="b7464-162">تأكيد ملف الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-162">Confirm a positive pay file</span></span>
<span data-ttu-id="b7464-163">بعد اتمام دفع كل الشيكات المدرجة في ملف الدفع الإيجابي، ستتلقى رقم تأكيد من البنك.</span><span class="sxs-lookup"><span data-stu-id="b7464-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="b7464-164">يمكنك عندئذٍ تأكيد ملف الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="b7464-165">في صفحة **ملخص ملف الدفع الإيجابي**، حدد ملف دفع إيجابي بالحالة **تم إنشاؤه**، ثم حدد الإجراء **إدخال التأكيد**.</span><span class="sxs-lookup"><span data-stu-id="b7464-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="b7464-166">عندما تؤكد ملف الدفع الإيجابي، يتم تسجيل رقم التأكيد الذي تلقيته من البنك.</span><span class="sxs-lookup"><span data-stu-id="b7464-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="b7464-167">استدعاء ملف دفع إيجابي</span><span class="sxs-lookup"><span data-stu-id="b7464-167">Recall a positive pay file</span></span>
<span data-ttu-id="b7464-168">إذا لزم تغيير ملف دفع إيجابي، فيمكنك إعادة استدعائه.</span><span class="sxs-lookup"><span data-stu-id="b7464-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="b7464-169">في صفحة **ملخص ملف الدفع الإيجابي**، حدد ملف دفع إيجابي بالحالة **تم إنشاؤه**، ثم حدد الإجراء **استدعاء**.</span><span class="sxs-lookup"><span data-stu-id="b7464-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="b7464-170">لكل شيك في ملف الدفع الإيجابي، يُعاد تعيين الحقل الذي يشير إلى ما إذا تم تضمين الشيك في ملف دفع إيجابي.</span><span class="sxs-lookup"><span data-stu-id="b7464-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="b7464-171">وبعد ذلك، يمكنك إنشاء ملف دفع إيجابي جديد يتضمن الشيك الذي تم استدعاؤه.</span><span class="sxs-lookup"><span data-stu-id="b7464-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



