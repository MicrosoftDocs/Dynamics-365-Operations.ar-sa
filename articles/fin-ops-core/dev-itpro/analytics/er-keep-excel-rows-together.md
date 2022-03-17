---
title: تصميم تنسيق ER للاحتفاظ بالصفوف معًا في نفس صفحة Excel
description: يشرح هذا الموضوع كيفية تصميم تنسيق التقارير الإلكترونية (ER) الذي يبقي الصفوف معًا في صفحة Microsoft Excel نفسها.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 711681ab38fb24b57a83f008f86a8261176aa5a5
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388577"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>تصميم تنسيق ER للاحتفاظ بالصفوف معًا في نفس صفحة Excel

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

يوضح هذا الموضوع كيف يمكن لمستخدم لديه دور مسؤول النظام أو المستشار الوظيفي للتقارير الإلكترونية تكوين [تنسيق التقارير الإلكترونية](general-electronic-reporting.md) [(ER)](er-overview-components.md#format-component) الذي يقوم بإنشاء مستندات صادرة في Microsoft Excel وإدارة ترقيم الصفحات بحيث يتم الاحتفاظ بالصفوف التي تم إنشاؤها في نفس الصفحة.

في هذا المثال، ستقوم بتعديل تنسيق ER المتوفر من قبل Microsoft والذي يتم استخدامه لطباعه فواتير النص الحر في Excel. ستتيح لك التعديلات الخاصة بك القيام باداره الخلايا الخاصة بتقرير فاتورة النص الحر الذي تم إنشاؤه حتى يتم الاحتفاظ بكافة صفوف بند الفاتورة الواحد في نفس الصفحة عند الإمكان.

يمكن إكمال الإجراءات الموجودة في هذا الموضوع في شركة **USMF**. الترميز غير مطلوب.

في هذا المثال، ستقوم بإنشاء تكوينات [ER](general-electronic-reporting.md#Configuration) المطلوبة للشركة النموذجية **Litware, Inc.**. تأكد من أن موفر التكوين للشركة النموذجية **Litware, Inc.** (`http://www.litware.com`) تم إدراجه لإطار عمل إعداد التقارير الإلكترونية، وتم تمييزه على أنه **نشط**. في حالة عدم إدراج موفر التكوين، أو عدم وضع علامة عليه كـ **نشط**، اتبع الخطوات الموجودة في [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط.](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>إدخال فاتورة ذات نص حر جديدة

1. اتبع الخطوات الموجودة في [إنشاء فاتورة ذات نص حر](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) لإضافة فاتورة ذات نص حر.

    1. أضف سطرًا واحدًا إلى الفاتورة.
    2. قم باضافه خمسه ملاحظات لبند الفاتورة.

    ![مراجعه ملاحظات بند الفاتورة علي صفحه المرفقات.](./media/er-keep-excel-rows-together-notes.png)

2. اتبع الخطوات الموجودة في [نسخ البنود](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines)لإنشاء خمسه بنود فاتورة اضافيه تقوم بنسخ بند الفاتورة الذي قمت بإضافته في الخطوة السابقة.

    ![مراجعه بنود فاتورة النص الحر في الصفحة فاتورة نص حر.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>تكوين إطار عمل ER

اتبع الخطوات في [تكوين إطار عمل التقارير الإلكترونية](er-quick-start2-customize-report.md#ConfigureFramework) لإعداد الحد الأدنى لمجموعة معلمات التقارير الإلكترونية. يجب إكمال هذا الإعداد قبل بدء استخدام إطار عمل التقارير الإلكترونية لتصميم إصدار مخصص من التنسيق القياسي للتقارير الإلكترونية.

## <a name="import-the-standard-er-format-configuration"></a>استيراد تكوين التنسيق القياسي للتقارير الإلكترونية.

اتبع الخطوات الواردة في [استيراد تكوين التنسيق القياسي للتقارير الإلكترونية](er-quick-start2-customize-report.md#ImportERSolution1) لإضافة التكوينات القياسية للتقارير الإلكترونية إلى مثيل Dynamics 365 Finance الحالي. على سبيل المثال، قم باستيراد **252.116** من تكوين تنسيق **الفاتورة ذات النص الحر (Excel)**. يتم استيراد الإصدار الأساسي **252** من تكوين **نموذج الفاتورة** الأساسي تلقائيًا من المستودع مع تكوين **تعيين نموذج الفاتورة المطلوب**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>إعداد إدارة الطباعة لاستخدام تنسيق ER الأساسي

اتبع الخطوات الموجودة في [إعداد إدارة الطباعة](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) لتكوين إدارة الطباعة لوحدة **الحسابات المدينة** بحيث يتم استخدام تنسيق ER القياسي لطباعة الفواتير ذات النص الحر.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>تكوين وجهة تنسيق لتنسيق ER القياسي

اتبع الخطوات الواردة في [تكوين وجهة تنسيق للمعاينة على الشاشة](er-quick-start1-new-solution.md#ConfigureDestination) لتكوين وجهة ER الخاصة [بالشاشة](er-destination-type-screen.md) لتنسيق ER القياسي بحيث يتم تحويل التقارير التي تم إنشاؤها إلى تنسيق PDF ومعاينتها في علامة تبويب مستعرض جديدة.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>طباعة فاتورة نص حر باستخدام تنسيق ER القياسي

1. اتبع الخطوات الواردة في [طباعه فاتورة ذات حر](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) لاستخدام التنسيق القياسي لـ ER لإنشاء تقرير فاتورة ذات نص حر بتنسيق Excel للفاتورة المضافة.
2. قم بتنزيل مصنف Excel الذي تم إنشاؤه، ثم قم بمراجعته في تطبيق سطح المكتب في Excel.

    لاحظ ان السطر السادس من الفاتورة يبدا في الصفحة الاولي من التقرير ويستمر علي الصفحة الثانية. تظهر الملاحظة الاخيره علي الصفحة الثانية، ولا تكون واضحة لبند الفاتورة السادس. لذلك، تؤدي فاصل الصفحات في منتصف المحتوي لسطر الفاتورة إلى صعوبة قراءه هذا المستند.

    ![مراجعه الفواصل الخاصة بفاتورة النص الحر التي تم إنشاؤها في تطبيق سطح المكتب في Excel.](./media/er-keep-excel-rows-together-invoice1.gif)

تظهر الإجراءات المتبقية في هذا الموضوع كيفيه ضبط التنسيق القياسي لـ ER لتحسين مظهر تقرير الفاتورة وقابليه القراءة له وذلك بالاحتفاظ بكافة محتويات بند فاتورة واحد في نفس الصفحة.

## <a name="create-a-custom-format"></a>إنشاء تنسيق مخصص

اتبع الخطوات الواردة في [إنشاء تنسيق مخصص](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) لاشتقاق تنسيق من تنسيق ER الذي تم استيراده وإنشاء تكوين ER **مخصص للفاتورة ذات النص الحر (Excel)** المتوفر للتحرير والتعديل.

## <a name="edit-the-custom-format"></a>تحرير التنسيق المخصص

1. اتبع الخطوات الواردة في [إنشاء تنسيق مخصص](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) لفتح تنسيق ER المشتق للتحرير في مصمم تنسيق ER.
2. في صفحة **مصمم التنسيق**، في شجرة مكونات التنسيق في الجزء الأيسر، قم بتوسيع **الفاتورة ذات النص الحر \> الورقة \> InvoiceLines**، ثم حدد مكون **InvoiceLines_Values**.
3. من علامات التبويب **تنسيق**، قم بتعيين الخيار **الحفاظ على الصفوف معًا**  إلى **نعم**.

    ![تعيين خيار الاحتفاظ بالصفوف معا لتنسيق ER القابل للتحرير في الصفحة "مصمم التنسيق".](./media/er-keep-excel-rows-together-format.png)

4. حدد **حفظ** ثم أغلق الصفحة.

## <a name="mark-the-custom-format-as-runnable"></a>تعليم التنسيق المخصص على أنه قابل للتشغيل

اتبع الخطوات الواردة في [وضع علامة على التنسيق المخصص كقابل للتشغيل](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) لجعل الإصدار المعدل من تنسيق ER المخصص قابلاً للتشغيل.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>إعداد إدارة الطباعة لاستخدام تنسيق ER المخصص

اتبع الخطوات الموجودة في [إعداد إدارة الطباعة](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) لتكوين إدارة الطباعة لوحدة **الحسابات المدينة** بحيث يتم استخدام تنسيق ER المخصص لطباعة الفواتير ذات النص الحر.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>تكوين وجهة تنسيق لتنسيق ER المخصص

اتبع الخطوات الواردة في [تكوين وجهة تنسيق للمعاينة على الشاشة](er-quick-start1-new-solution.md#ConfigureDestination) لتكوين وجهة ER الخاصة **بالشاشة** لتنسيق ER المخصص بحيث يتم تحويل التقارير التي تم إنشاؤها إلى تنسيق PDF ومعاينتها في علامة تبويب مستعرض جديدة.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>طباعة فاتورة نص حر باستخدام تنسيق ER المخصص

1. اتبع الخطوات الواردة في [طباعه فاتورة ذات حر](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) لاستخدام تنسيق ER المخصص لإنشاء تقرير فاتورة ذات نص حر بتنسيق Excel للفاتورة المضافة.
2. قم بتنزيل مصنف Excel الذي تم إنشاؤه، ثم قم بمراجعته في تطبيق سطح المكتب في Excel.

    لاحظ أن السطر السادس من الفاتورة يبدأ في الصفحة الثانية، وتظهر جميع صفوف Excel التي تمثل سطر الفاتورة هذا معًا في تلك الصفحة.

    ![مراجعة ترقيم الصفحات المحدث لفاتورة النص الحر المُنشأة في تطبيق Excel لسطح المكتب.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>الموارد الإضافية

[تصميم تكوين لإنشاء مستندات بتنسيق Excel](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
