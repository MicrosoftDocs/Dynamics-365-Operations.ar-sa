---
title: إعداد ملفات الدفع الإيجابي وإنشاؤها
description: توضح هذه المقالة كيفية إعداد الدفع الإيجابي وإنشاء ملفات الدفع الإيجابي.
author: panolte
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6b3cff1029b02aaabef2ea9795ab9912f20f1129
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871409"
---
# <a name="set-up-and-generate-positive-pay-files"></a>إعداد ملفات الدفع الإيجابي وإنشاؤها

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إعداد الدفع الإيجابي وإنشاء ملفات الدفع الإيجابي. 

إعداد الدفع الإيجابي لإنشاء قائمة إلكترونية بالشيكات التي يتم توفيرها للبنك. بعد ذلك، عندما يتم تقديم الشيك إلى البنك، يقارنه البنك بقائمة الشيكات. إذا تطابق الشيك مع شيك آخر في القائمة، فسيقوم البنك بمخالصته. أما إذا لم يتطابق الشيك لم تطابق مع أي شيك آخر في القائمة، فسيحتفظ البنك به لمراجعته.

## <a name="security-for-positive-pay-files"></a>الأمان لملفات الدفع الإيجابي
يمكن أن تحتوي ملفات الدفع الإيجابي على معلومات هامة حول المستفيدين ومبالغ الشيكات. لذلك، تأكد من استخدام تدابير أمنية مناسبة اعتبارًا من وقت إنشاء الملفات وحى استلام البنك لها. يتم تنزيل ملفات الدفع الإيجابي إلى الموقع المحدد بواسطة مستعرض ويب. ونظرًا لإمكانية احتواء ملفات الدفع الإيجابي على معلومات حساسة، من الضروري أن يقتصر حق الوصول لإنشاء وعرض هذه المعلومات في Microsoft Dynamics 365 Finance على المستخدمين المخوّلين فقط. استخدم الجدول التالي للمساعدة في تحديد الامتيازات المطلوبة.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>المهمة</th>
<th>الامتياز</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>إنشاء ملفات الدفع الإيجابي من صفحة قائمة <strong>الحسابات البنكية</strong> أو صفحة <strong>الحسابات البنكية</strong>.</td>
<td><ul>
<li><strong>الاحتفاظ بمعلومات الدفع الإيجابي البنكي</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>إنشاء ملفات دفع إيجابي لعدة كيانات قانونية وحسابات بنكية من صفحة <strong>إنشاء ملف دفع إيجابي‬</strong>.</td>
<td><ul>
<li><strong>الاحتفاظ بمعلومات الدفع الإيجابي البنكي</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>عرض ملفات الدفع الإيجابي في صفحة <strong>ملخص ملف الدفع الإيجابي</strong>.</td>
<td><strong>عرض معلومات الدفع الإيجابي البنكي لكيانات قانونية متعددة</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>تأكيد ملف الدفع الإيجابي في صفحة <strong>ملخص ملف الدفع الإيجابي</strong>.</td>
<td><strong>تأكيد ملف الدفع الإيجابي</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>استدعاء ملف الدفع الإيجابي في صفحة <strong>ملخص ملف الدفع الإيجابي</strong>.</td>
<td><strong>استدعاء ملف دفع إيجابي</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>إعداد تنسيق الدفع الإيجابي
يتم إنشاء ملفات الدفع الإيجابي باستخدام كيانات البيانات. قبل إنشاء ملف الدفع الإيجابي، يجب إعداد تنسيق إدخال التحويل الذي سيتم استخدامه لترجمة معلومات الشيك إلى تنسيق يمكنه التواصل مع البنك. في صفحة **تنسيق الدفع الإيجابي**، يمكنك إنشاء معرف تنسيق الملف ووصف لهذا التنسيق. يجب أن يكون تنسيق إدخال التحويل عبارة عن ملف من نوع XML. يتوقف التنسيق المحدد على ملف التحويل الذي تستخدمه. على سبيل المثال، يستخدم ملف تحويل لغة صفحات الأنماط الموسعة (XSLT) النموذجي الذي تم توفيره تنسيق **XML-Element**. استخدم الإجراء **تحميل الملف المستخدم في التحويل‬** لتحديد موقع ملف التحويل للتنسيق الذي يتطلبه البنك الذي تتعامل معه.

## <a name="example-xslt-file-for-positive-pay-file"></a>على سبيل المثال: ملف XSLT لملف الدفع الإيجابي

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

> [!NOTE]
> يجب أن تتطابق أسماء XML الموجودة في XSLT مع حاله الأحرف الخاصة بالعقد الموجودة في XML. كل من ملفات XSLT و XML حساسة لحاله الأحرف. 

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>تعيين تنسيق الدفع الإيجابي لحساب بنكي
لكل حساب بنكي تريد إنشاء معلومات دفع إيجابي له، يجب تعيين تنسيق الدفع الإيجابي الذي حددته في القسم السابق. في صفحة **الحسابات البنكية**، حدد تنسيق الدفع الإيجابي الذي يتوافق مع الحساب البنكي. في الحقل **تاريخ بدء الدفع الإيجابي‬**  التاريخ الأول لإنشاء ملفات الدفع الإيجابي. من الضروري إدخال تاريخ في هذا الحقل. خلاف ذلك، سيتضمن ملف الدفع الإيجابي الأول الذي تقوم بإنشائه كل الشيكات التي تم إنشاؤها لهذا الحساب البنكي.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>تعيين تسلسل رقمي لملفات الدفع الإيجابي
يجب أن يكون لكل ملف دفع إيجابي رقم فريد. استخدم علامة التبويب **التسلسلات الرقمية‬** في صفحة **محددات إدارة البنك والنقد‬** لإنشاء تسلسل رقمي لملفات الدفع الإيجابي.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>إنشاء ملف دفع إيجابي لحساب بنكي واحد
يمكنك إنشاء ملف دفع إيجابي لكيان قانوني واحد وحساب بنكي واحد. للحصول على معلومات حول كيفية إنشاء ملفات الدفع الإيجابي لكيانات قانونية وحسابات بنكية متعددة في نفس الوقت، راجع القسم التالي. لإنشاء ملف دفع إيجابي لكيان قانوني واحد وحساب بنكي واحد، افتح مربع الحوار **إنشاء ملف دفع إيجابي** من صفحة **الحسابات البنكية**. في حقل **تاريخ الانقطاع‬**، أدخل تاريخ الشيك الأخير لتضمينه في ملف الدفع الإيجابي. يتم تضمين كافة الشيكات غير المضمنة في ملف دفع إيجابي بنهاية تاريخ الشيك هذا في الملف.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>إنشاء ملف دفع إيجابي لحسابات بنكية متعددة
لإنشاء ملف دفع إيجابي لحسابات بنكية متعددة، استخدم المهمة الدورية **إنشاء ملف دفع إيجابي**. حدد تنسيق ملف الدفع الإيجابي، وحدد إذا كنت تريد إنشاء ملف الدفع الإيجابي لجميع الكيانات القانونية أو لكيان قانوني محدد. يمكنك أيضًا إنشاء ملف الدفع الإيجابي لجميع الحسابات البنكية التي تستخدم تنسيق الدفع الإيجابي المحدد أو لحساب بنكي محدد. في حقل **تاريخ الانقطاع‬**، أدخل تاريخ الشيك الأخير لتضمينه في ملف الدفع الإيجابي. يتم تضمين كافة الشيكات غير المضمنة في ملف دفع إيجابي بنهاية تاريخ الشيك هذا في الملف.

## <a name="view-the-results-of-positive-pay-file-generation"></a>عرض نتائج إنشاء ملف الدفع الإيجابي
بعد إنشاء ملف الدفع الإيجابي، يمكنك عرض النتائج في صفحة **ملخص ملف الدفع الإيجابي**. لعرض تفاصيل شيكات فردية، استخدم صفحة **ملف الدفع الإيجابي**.

## <a name="confirm-a-positive-pay-file"></a>تأكيد ملف الدفع الإيجابي
بعد اتمام دفع كل الشيكات المدرجة في ملف الدفع الإيجابي، ستتلقى رقم تأكيد من البنك. يمكنك عندئذٍ تأكيد ملف الدفع الإيجابي. في صفحة **ملخص ملف الدفع الإيجابي**، حدد ملف دفع إيجابي بالحالة **تم إنشاؤه**، ثم حدد الإجراء **إدخال التأكيد**. عندما تؤكد ملف الدفع الإيجابي، يتم تسجيل رقم التأكيد الذي تلقيته من البنك.

## <a name="recall-a-positive-pay-file"></a>استدعاء ملف دفع إيجابي
إذا لزم تغيير ملف دفع إيجابي، فيمكنك إعادة استدعائه. في صفحة **ملخص ملف الدفع الإيجابي**، حدد ملف دفع إيجابي بالحالة **تم إنشاؤه**، ثم حدد الإجراء **استدعاء**. لكل شيك في ملف الدفع الإيجابي، يُعاد تعيين الحقل الذي يشير إلى ما إذا تم تضمين الشيك في ملف دفع إيجابي. وبعد ذلك، يمكنك إنشاء ملف دفع إيجابي جديد يتضمن الشيك الذي تم استدعاؤه.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
