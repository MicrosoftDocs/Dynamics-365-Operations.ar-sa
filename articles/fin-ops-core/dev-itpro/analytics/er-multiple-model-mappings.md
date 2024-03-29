---
title: أداره تعيينات مشتقه متعددة لجذر نموذج واحد
description: توضح هذه المقالة كيفية إدارة العديد من التعيينات المشتقة التي تم تكوينها لجذر نموذج واحد.
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERModelMappingTable
ms.openlocfilehash: 868d47ccfebb9a9753d93344c72b10ae4353b0e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277497"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>أداره تعيينات مشتقه متعددة لجذر نموذج واحد

[!include [banner](../includes/banner.md)]

يتم استخدام مكون نموذج بيانات [إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md) في كل مكون من مكونات تنسيق التقارير الإلكترونية كمصدر البيانات لإنشاء المستندات الصادرة. لوصف مجال اعمال واحد، قم بتكوين مكون نموذج بيانات يحتوي علي العديد من تعريفات الجذر. 

ويتيح كل تعريف للجذر تمثيل بيانات ذلك المجال بالطريقة الأكثر ملاءمة لأغراض اعداد التقارير المحددة. ولكل تعريف جذر، يمكنك تكوين مكون تعيين نموذج إعداد التقارير الإلكترونية (ER) كتنفيذ خاص بـ 365‎ Finance Microsoft Dynamics لنموذج بياناتك. وبهذه الطريقة ، يمكنك وصف كيفيه ملء نموذج البيانات الخاص بك في وقت التشغيل.

يمكن ان توجد مكونات تعيين نموذج ER في [تكوينات](general-electronic-reporting.md#Configuration) نموذج بيانات ER وتكوينات تعيين طراز ER. يمكن ان يحتوي تكوين ER واحد علي العديد من مكونات التعيين ، يتم تكوين كل منها لتعريف جذر مفرد. بدلاً من ذلك، يمكن ان يحتوي تكوين ER واحد فقط علي العديد من مكون التعيين، يتم تكوين كل منها لتعريف جذر مفرد.

قد يوفر العديد من موفري التكوين تكوينات تعيين طراز ل ER لنفس نموذج بيانات (ER). قد تحتوي تكوينات تعيين النماذج هذه علي مكونات تعيين لتعريفات الجذر المختلفة. يمكنك استخدام تعيين نموذج لتعريف جذر واحد يتم توفيره بواسطة [موفر](general-electronic-reporting.md#Provider) واحد واستخدام تعيين نموذج لتعريف جذر آخر يتم توفيره من قبل موفر آخر.

توضح الإجراءات الواردة في هذه المقالة كيفية إدارة تكوينات تعيين طراز التقارير الإلكترونية المتعددة لنموذج بيانات ER عند احتوائهما علي مكونات تعيين نموذج مختلفة مكونة لنفس تعريف الجذر. 

لإتمام هذا الإجراء في هذه المقالة، يجب أن يتم تعيينك لدور مسؤول النظام أو مطور التقارير الإلكترونية.

يمكن إجراء كافة الإجراءات التالية في شركة USMF. الترميز غير مطلوب.

## <a name="configure-the-er-framework"></a>تكوين إطار عمل ER

كمستخدم يؤدي دور مطور إعداد التقارير الإلكترونية، يجب عليك [تكوين مجموعة صغيرة](er-quick-start2-customize-report.md#ConfigureFramework) من معلمات التقارير الإلكترونية قبل بدء استخدام إطار عمل إعداد التقارير الإلكترونية لتصميم الحل الجديد لإعداد التقارير الإلكترونية.

## <a name="import-the-standard-er-format-configurations"></a>استيراد تكوينات تنسيق ER القياسية

لإضافة تكوينات التقارير الإلكترونية القياسية إلى مثيل Finance الحالي، فإنه يجب استيرادها من مستودع التقارير الإلكترونية الذي تم تكوينه لذلك المثيل. اتبع الخطوات الموجودة في [تنزيل تكوينات ER من المستودع العمومي لخدمه التكوين](er-download-configurations-global-repo.md) لاستيراد تكوينات تنسيق ER التالية:

- **فانورة بنص حر (Excel)**، الإصدار 220.106
- **فانورة مشروع (Excel)**، الإصدار 226.27

## <a name="review-the-imported-er-configurations"></a>مراجعة تكوينات ER المستوردة

1. انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد تجانب **تكوينات إعداد التقارير** .
3. في صفحة **التكوينات**، في شجرة التكوينات، الجزء الأيسر، وسَّع **نموذج الفاتورة**.

    ![مراجعة التكوينات المستوردة على صفحة التكوينات.](./media/er-multiple-model-mappings-image1.png)

4. مراجعه **تنسيق فاتورة النص الحر (Excel)**:

    1. في شجرة التكوين الموجودة في الجزء الأيسر، حدد **فاتورة النص الحر (Excel)**.
    2. في جزء الإجراءات، حدد **المصمم**.
    3. في صفحة **مصمم التنسيق**، في علامة التبويب **تعيين**، في قائمة مصادر البيانات، حدد **النموذج**.
    4. حدد **عرض**.
    
       تم تكوين تنسيق ER الحالي لاستخدام تعريف جذر **InvoiceCustomer** لـ **نموذج الفاتورة**. عند تشغيل هذا التنسيق، واستدعاء مصدر بيانات **النموذج**، يتم استخدام تعيين النموذج الذي تم تكوينه لتعريف جذر **InvoiceCustomer**  للوصول إلى بيانات التطبيق وتعبئة نموذج البيانات.

        ![مراجعة مصدر بيانات النموذج في صفحة مصمم التنسيق.](./media/er-multiple-model-mappings-image2.png)

    6. أغلق صفحة **مصمم المعادلة**.

5. مراجعه محتوي تكوين **تعيين نموذج الفواتير**:

    1. في شجرة التكوين الموجودة في الجزء الأيسر، حدد **تعيين نموذج الفاتورة**.
    2. في جزء الإجراءات، حدد **المصمم**.
    3. في صفحه **تعيين النموذج إلى مصدر البيانات**، لاحظ ان تكوين تعيين طراز ER الحالي يحتوي علي مكونات تعيين متعددة النماذج:

        + يتم تكوين تعيين نموذج **فاتورة العميل** لتعريف الجذر **InvoiceCustomer** **لنموذج الفاتورة**. لذلك، عند تشغيل تنسيق ER **فاتورة النص الحر (Excel)**، يمكن اختيار تعيين نموذج **فاتورة العميل** لتكوين ER هذا للوصول إلى بيانات التطبيق وتعبئة نموذج البيانات.
        + يتم تكوين تعيين نموذج **فاتورة المشروع** لتعريف الجذر **InvoiceProject** **لنموذج الفاتورة**. لذلك، عند تشغيل تنسيق ER **فاتورة المشروع (Excel)**، يمكن اختيار تعيين نموذج **فاتورة المشروع** لتكوين ER هذا للوصول إلى بيانات التطبيق وتعبئة نموذج البيانات.

        ![تعيين نموذج الفاتورة في النموذج إلى صفحة تعيين مصدر البيانات.](./media/er-multiple-model-mappings-image3.png)

    4. أغلق صفحة **تعيين النموذج إلى مصدر البيانات**.
    5. في علامة التبويب السريعة **الإصدارات**، حدد **حذف** لحذف كافة إصدارات تكوين ER الحالي التي تكون أحدث من الإصدار 240.175.

6. مراجعه محتوي تكوين **تعيين نموذج فاتورة المشروع (RDP)**:

    1. في شجرة التكوين الموجودة في الجزء الأيسر، حدد **تعيين نموذج فاتورة المشروع (RDP)**.
    2. في جزء الإجراءات، حدد **المصمم**.
    3. في صفحه **تعيين النموذج إلى مصدر البيانات**، لاحظ ان تكوين تعيين طراز ER الحالي يحتوي علي تعيين نموذج **InvoiceProject**، وانه قد تم تكوين تعيين النموذج هذا لتعريف الجذر **InvoiceProject** **لنموذج الفاتورة**. عند تشغيل تنسيق ER **فاتورة المشروع (Excel)**، يمكن اختيار تعيين نموذج **InvoiceProject** لتكوين ER هذا للوصول إلى بيانات التطبيق وتعبئة نموذج البيانات.

        ![تعيين نموذج فاتورة المشروع في النموذج إلى صفحة تعيين مصدر البيانات.](./media/er-multiple-model-mappings-image4.png)

    4. أغلق صفحة **تعيين النموذج إلى مصدر البيانات**.
    5. في علامة التبويب السريعة **الإصدارات**، حدد **حذف** لحذف كافة إصدارات تكوين ER الحالي التي تكون أحدث من الإصدار 226.35.

## <a name="customize-the-imported-er-configurations"></a>تخصيص تكوينات ER المستوردة

يوضح هذا القسم كيفيه [تخصيص](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) تعيينات النماذج التي يتم توفيرها بواسطة Microsoft. علي سبيل المثال، قد يتطلب التخصيص لتطبيق منطق مخصص أو أضافه روابط مفقوده.

### <a name="customize-the-invoice-model-mapping-configuration"></a>تخصيص تكوين تعيين نموذج الفاتورة

1. في صفحة **التكوينات**، في شجرة التكوينات الجزء الأيسر، حدد **تعيين نموذج الفاتورة**.
2. في جزء الإجراء، حدد **إنشاء تكوين**.
3. في مربع الحوار المنسدل **إنشاء تكوين**، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: تعييين نموذج الفاتورة، Microsoft**.
4. في الحقل **الاسم**، أدخل **تعيين نموذج الفاتورة Litware**.
5. حدد **إنشاء التكوين**.
6. [قم بوضع علامة علي إصدار ](er-quick-start2-customize-report.md#MarkFormatRunnable)[المسودة](general-electronic-reporting.md) للتعيين المشتق كمتوفر للاستخدام في وقت التشغيل:

    1. في جزء الإجراءات، على علامة تبويب **التكوينات**، في المجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدم**.
    2. في مربع الحوار **معلمات المستخدم**، قم بتعيين خيارات **إعدادات التشغيل** إلى **نعم**، ثم حدد **موافق**.
    3. حدد **تحرير** لتجعل الصفحة قابلة للتحرير، حسب الحاجة.
    4. بالنسبة للتكوين **تعيين نموذج الفاتورة Litware** المحدد حاليا في شجره التكوين، قم بتعيين الخيار **تشغيل مسودة** إلى **نعم**.

7. في جزء الاجراء، حدد **المصمم** لمراجعه تعيينات النموذج الخاصة بهذا التكوين.

    ![مراجعة تعيين نموذج الفاتورة في النموذج إلى صفحة تعيين مصدر البيانات.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > يمكنك الآن فتح اي من مكونات تعيين طراز ER الخاص بتكوين ER هذا في المصمم لتكوين المنطق المخصص الخاص بك. لمزيد من المعلومات ، راجع [تخصيص تكوين تعيين النموذج](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. أغلق صفحة **تعيين النموذج إلى مصدر البيانات**.

لديك الآن **تعيين نموذج الفواتير** والتكوينات **تعيين نموذج الفواتير Litware**، حيث يحتوي كل منها علي تعيين نموذج تم تكوينه لتعريف جذر **InvoiceCustomer**. قم بشكل صريح بتعيين أحد تعيينات النموذج كتعيين النموذج الافتراضي المستخدم بواسطة اي من تنسيقات ER ، مثل **تنسيق فاتورة النص الحر (Excel)** الذي يحتوي علي مصدر بيانات نموذج له تعريف الجذر **InvoiceCustomer**. والا ، عند تشغيل أحد تنسيقات طراز التطبيق ، أو تحريره أو التحقق من صحته ، يتم طرح الاستثناء التالي ليعلمك بعدم تعيين تعيين النموذج الافتراضي بشكل صريح:
 
> يوجد أكثر من تعيين طراز واحد \<model name\>\<root descriptor\>لنموذج البيانات ' () ' في التكوينات\<configuration names separated by commas\>. قم بتعيين أحد التكوينات كاعداد افتراضي.

![فتح التنسيق للتحرير في صفحة التكوينات.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>تخصيص تكوين تعيين نموذج فاتورة المشروع (RDP)

1. في صفحة **التكوينات**، في شجرة التكوينات الجزء الأيسر، حدد **تعيين نموذج فاتورة المشروع (RDP)**.
2. في جزء الإجراء، حدد **إنشاء تكوين**.
3. في مربع الحوار المنسدل **إنشاء تكوين**، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: تعيين نموذج فاتورة المشروع (RDP)**.
4. في الحقل **الاسم**، أدخل **تعيين نموذج فاتورة المشروع Litware**.
5. حدد **إنشاء التكوين**.
6. بالنسبة للتكوين **تعيين نموذج فاتورة المشروع Litware** المحدد حاليا في شجره التكوين، قم بتعيين الخيار **تشغيل مسودة** إلى **نعم**.
7. في جزء الاجراء، حدد **المصمم** لمراجعه تعيينات النموذج الخاصة بهذا التكوين.

    ![مراجعة تعيين نموذج الفاتورة المخصص في النموذج إلى صفحة تعيين مصدر البيانات.](./media/er-multiple-model-mappings-image7.png)

8. أغلق صفحة **تعيين النموذج إلى مصدر البيانات**.

لديك الآن **تعيين نموذج فواتير** و **تعيين نموذج فواتير المشروع (RDP)** وتكوينات **تعيين نموذج فواتير المشروع Litware**. كل من هذه التكوينات له تعيين نموذج تم تكوينه لتعريف جذر **InvoiceProject**. قم بشكل صريح بتعيين أحد تعيينات النموذج كتعيين النموذج الافتراضي المستخدم بواسطة اي من تنسيقات ER. علي سبيل المثال ، استخدم **تنسيق فاتورة المشروع (Excel)** الذي يحتوي علي مصدر بيانات نموذج له تعريف الجذر **InvoiceProject**. والا ، عند تشغيل أحد تنسيقات طراز التطبيق، أو تحريره، يتم طرح استثناء ليعلمك بعدم تعيين تعيين النموذج الافتراضي بشكل صريح.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>تحديد التكوين تعيين نموذج الفواتير المشتقة Litware كتكوين يحتوي علي تعيينات النموذج الافتراضية

1. في صفحة **التكوينات**، في شجرة التكوينات الجزء الأيسر، حدد **تعيين نموذج الفاتورة Litware**.
2. قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**

    ![تعيين تعيين النموذج كتعيين النموذج الافتراضي في صفحة التكوينات.](./media/er-multiple-model-mappings-image8.png)

    وبسبب هذا الاعداد ، يتم استخدام تعيين نموذج **نسخ فاتورة العميل** عند تشغيل **فاتورة النص الحر (Excel)**، أو عند تحريره أو التحقق من صحته. تم تجاهل تعيين نموذج **فاتورة العميل** من التكوين **تعيين نموذج الفاتورة**.

    يمكنك الآن فتح تنسيق **فاتورة النص الحر (Excel)** للمراجعة في مصمم التنسيق.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>تحديد التكوين تعيين نموذج فاتورة المشروع المشتقة Litware كتكوين يحتوي علي تعيينات النموذج الافتراضية

1. في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، حدد **تعيين نموذج فاتورة المشروع Litware**.
2. قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**

    في هذه الحالة، بخلاف الحالة التي تم وصفها لتكوين **تعيين نموذج الفاتورة Litware** في المقطع السابق، لا يمكنك البدء في استخدام تعيين نموذج **نسخ InvoiceProject** من تكوين **تعيين نموذج فاتورة المشروع Litware**. يتم حاليا وضع اثنين من التكوينات التي تحتوي علي تعيين نموذج لتعريف جذر **InvoiceProject** علي انه التكوين الافتراضي. التالي، يكون لهذه المستخدمين اولويه متساوية للاستخدام. لحل هذه المشكلة ، أكمل الخطوات المتبقية من هذا الاجراء.

3. في شجرة التكوين الموجودة في الجزء الأيسر، حدد **تعيين نموذج الفاتورة Litware**.
4. في جزء الإجراءات، حدد **المصمم**.
5. في صفحه **تعيين النموذج إلى مصدر البيانات**، حدد **تحرير** لجعل الصفحة قابله للتحرير، حسب الحاجة.
6. حدد تعيين نموذج **نسخ فاتورة المشروع**، ثم حدد خانه الاختيار **محذوف**.

    ![إعداد تعيين النموذج كمحذوف افتراضيًا في صفحة تعين النموذج إلى مصدر البيانات.](./media/er-multiple-model-mappings-image9.png)

    وبسبب هذا الاعداد، يتم التعامل مع تكوين **تعيين نموذج الفواتير** علي الرغم من انه لا يحتوي علي تعيين نموذج لتعريف جذر **InvoiceProject**. يتم إصدار تعيين نموذج **نسخ InvoiceProject** افتراضيا. تحديد التكوين **تعيين نموذج فاتورة المشروع Litware**، الذي يحتوي على تعيين النموذج هذا، كتكوين افتراضي. نظرا لأنه يتم وضع علامة عليه كافتراضي، فهو له اولويه اعلي من تعيين نموذج **InvoiceProject** من تكوين **تعيين نموذج فاتورة المشروع (RDP)**.

## <a name="other-considerations"></a>اعتبارات أخرى

تم تصميم تعيين نموذج **نسخ InvoiceProject** لتكوين **تعيين نموذج فاتورة المشروع Litware** لاستخدام مصدر بيانات **ReportDataProvider**. يعد مصدر البيانات جزءا من نوع *الكائن* الذي يشير إلى فئة التطبيق **PsaProjInvoiceDP**. يتم تطبيق هذه الفئة كموفر البيانات لتقرير SQL Server Reporting Services (SSRS) الخاص بالمشروع (SSRS) الخاص بإطار عمل أداره الطباعة. حدد مصدر البيانات هذا [كنقطه تكامل](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents)  لـ ER. ياخذ التطبيق الحالي ل ER الخاص بتقارير أداره الطباعة هذا الاعداد في الحساب. لمزيد من التفاصيل، راجع التعليمات البرمجية المصدر لفئة التطبيق **ERPrintMgmtDataProviderReport**. في وقت التشغيل، تفرض تعيين مصدر بيانات **ReportDataProvider** كنقطه تكامل تعيين النموذج المالية للتعامل مع مكون التعيين هذا باولويه اعلي من مكون تعيين **InvoiceProject** من تكوين **نموذج فاتورة المشروع (RDP)**.

## <a name="see-also"></a>راجع أيضًا

- [إدارة تعيين نموذج التقارير الإلكترونية في تكوينات تقارير إلكترونية منفصلة](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [تكوين تعيينات نماذج التقارير الإلكترونية التي تعتمد على سياق البلد](er-country-dependent-model-mapping.md)
- [تغيير API لإطار عمل ‏‫إعداد التقارير الإلكترونية](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
