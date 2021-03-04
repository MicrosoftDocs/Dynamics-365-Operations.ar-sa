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
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09b24b88ee5f8104aabd11397d5bd2745e846cb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439828"
---
# <a name="bank-statement-file-import-troubleshooting"></a>استكشاف أخطاء استيراد ملفات كشوفات الحسابات البنكية وإصلاحها

[!include [banner](../includes/banner.md)]

من الضروري أن يتطابق ملف كشف الحساب البنكي من البنك مع التخطيط الذي يدعمه Microsoft Dynamics 365 Finance. بسبب المعايير الصارمة الموضوعة على كشوفات الحسابات البنكية، ستعمل معظم عمليات الدمج بشكل صحيح. ومع ذلك، يتعذر أحيانًا استيراد ملف كشف الحساب أو تكون نتائجه غير صحيحة. بشكل عام، تحدث هذه المشاكل بسبب اختلافات طفيفة في ملف كشف الحساب البنكي. توضح هذه المقالة كيفية حل هذه الاختلافات وحل المشكلات.

<a name="what-is-the-error"></a>ما هو الخطأ؟
------------------

بعد أن تحاول استيراد ملف كشف حساب بنكي، انتقل إلى محفوظات مهمة إدارة البيانات وتفاصيل التنفيذ الخاصة بها للعثور على الخطأ. بإمكان الخطأ أن يكون مساعدًا عن طريق التأشير إلى كشف الحساب البنكي أو الرصيد أو بند في الكشف. ومع ذلك، من غير المحتمل توفير ما يكفي من المعلومات لمساعدتك في تحديد الحقل أو العنصر الذي تسبب في حدوث المشكلة.

## <a name="what-are-the-differences"></a>ما هي الاختلافات؟
قارن تعريف تخطيط الملف البنكي بتعريف استيراد Finance، ودوّن أي اختلافات في الحقول والعناصر. ‏قارن ملف كشف الحساب البنكي بملف Finance النموذجي ذي الصلة. في ملفات ISO20022، يجب أن يكون من السهل رؤية الاختلافات.‬

## <a name="time-zone-differences-on-imported-bank-statements"></a>فروق المنطقة الزمنية على كشوف الحسابات البنكية المستوردة
بإمكان قيم التاريخ والوقت في ملف الاستيراد أن تختلف عن قيم التاريخ والوقت التي تظهر في Finance and Operations. لمنع حدوث هذا الاختلاف، ادخل تفضيل المنطقة الزمنية في الصفحة **تكوين مصادر البيانات**. راجع [إعداد عملية استيراد التسوية البنكية المتقدمة](set-up-advanced-bank-reconciliation-import-process.md) لمزيد من المعلومات حول إدخال تفضيل المنطقة الزمنية.

## <a name="transformations"></a>التحويلات
بشكل عام، يجب إجراء التغيير في أحد التحويلات الثلاثة. تتم كتابة كل تحويل لمعيار محدد.

| اسم المورد                                         | اسم الملف                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>تحويلات التصحيح
### <a name="adjust-the-bai2-and-mt940-files"></a>تعديل الملفات BAI2 وMT940

إن الملفات BAI2 وMT940 عبارة عن ملفات نصية وتتطلب تعديلاً لتمكين تصحيح تحويلات لغة صفحات الأنماط الموسعة (XSLT). يقوم البرنامج بإجراء هذا التعديل عند استيراد ملف.

1.  أنشئ ملف XML وانسخ النص التالي فيه.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  انسخ محتويات ملف كشف الحساب البنكي، والصقها في ملف XML لكي تحل محل **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>تصحيح XSLT

لمزيد من المعلومات، راجع <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  ابدأ تشغيل Microsoft Visual Studio.
2.  أنشئ تطبيق وحدة تحكم.
3.  افتح XSLT المناسب.
4.  انقر فوق XLST وصفحة خصائصه.
5.  عيّن الإدخال إلى موقع ملف كشف الحساب البنكي.
6.  حدد موقعًا واسم ملف للإخراج.
7.  عيّن نقاط التوقف المطلوبة.
8.  في القائمة، انقر فوق **XML** &gt; **بدء تصحيح XSLT**.

### <a name="format-the-xslt-output"></a>تنسيق إخراج XSLT

تقوم عملية التحويل عند تشغيلها بإنشاء ملف إخراج يمكنك عرضه في Visual Studio. استخدم Ctrl + A وCtrl + K وCtrl + D لتنسيق ملف الإخراج بسرعة.

### <a name="adjust-the-transformation"></a>ضبط التحويل

اضبط التحويل للحصول على العنصر أو الحقل الملائم في ملف كشف الحساب البنكي. ثم عيّن هذا الحقل أو العنصر إلى عنصر Finance المناسب.

### <a name="debitcredit-indicator"></a>مؤشر الديون/الائتمانات

في بعض الأحيان، قد يتم استيراد الديون كائتمانات، وقد يتم استيراد الائتمانات كديون. لحل هذه المشكلة، يجب تغيير XSLT المناسب. إذا كانت كشوف الحسابات البنكية تأتي من بنوك متعددة، فتأكد من أنها كلها تستخدم منهج الديون/الائتمانات نفسه أو أنشئ تحويلات منفصلة.

-   قالب BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   قالب ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   قالب MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>أمثلة عن تنسيقات كشوف الحسابات البنكية والتخطيطات التقنية
يسرد الجدول التالي أمثلة على تعريفات التخطيط التقني لملفات استيراد التسوية البنكية المتقدمة وثلاثة ملفات أمثلة عن كشوفات الحسابات البنكية ذات الصلة. يمكنك تنزيل أمثلة الملفات والتخطيطات الفنية هنا:https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| تعريف التخطيط التقني                             | ملف مثال عن كشف الحساب البنكي          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]