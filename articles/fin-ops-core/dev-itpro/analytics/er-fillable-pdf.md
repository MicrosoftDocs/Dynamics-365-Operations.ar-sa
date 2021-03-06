---
title: تصميم تكوينات التقارير الإلكترونية لملء قوالب PDF
description: يوفر هذا الموضوع معلومات حول كيفيه تصميم تنسيق التقارير الكترونيه لتعبئة قالب PDF.
author: NickSelin
manager: AnnBe
ms.date: 04/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: de31469e79addfb82b3b57e647ff82e4d254881a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688115"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>تصميم تكوينات التقارير الإلكترونية لملء قوالب PDF

[!include[banner](../includes/banner.md)]

الإجراءات الواردة في هذا الموضوع هي أمثله تظهر كيفيه قيام مستخدم يؤدي دور **مسؤول النظام** أو دور **مطور التقارير الإلكترونية‬** بتكوين تنسيق التقارير الكترونيه (ER) الذي يقوم بإنشاء التقارير كملفات PDF باستخدام وثائق PDF التي تم تعبئتها كقوالب تقارير. يمكن تنفيذ هذه الخطوات في أي شركة Dynamics 365 Finance أو Regulatory Configuration Services (RCS).

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل البدء، يجب أن يكون لديك أحد أنواع الوصول التالية، استنادًا إلى الخدمة التي تستخدمها لإكمال الإجراءات في هذا الموضوع:

- الوصول إلى Finance لأحد الأدوار التالية:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

- الوصول إلى RCS لأحد الأدوار التالية:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

ويجب عليك أيضًا إكمال الإجراء [إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).

وأخيرًا، يجب تنزيل الملفات التالية من [CustomerSource](https://go.microsoft.com/fwlink/?linkid=874111).

| وصف المحتوى                       | اسم الملف                                     |
|-------------------------------------------|-----------------------------------------------|
| قالب للصفحة الأولى من التقرير | [IntrastatReportTemplate1.pdf](https://mbs.microsoft.com/Files/public/CS)                  |
| قالب للصفحات الأخرى من التقرير    | [IntrastatReportTemplate2.pdf](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatReportTemplate2.pdf)                  |
| تنسيق التقارير الإلكترونية النموذجي - PDF                          | [تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (PDF) الإصدار.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatreportPDFversion11.xml)        |
| تنسيق التقارير الإلكترونية النموذجي - Excel                          | [نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (استيراد من Excel) الإصدار.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatimportfromExcelversion11.xml) |
| مجموعة بيانات نموذجية                            | [Intrastat sample data.xlsx](https://mbs.microsoft.com/Files/public/CS/AX/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>تصميم تكوين التنسيق

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>الوصول إلى قائمة التكوينات التي توفرها Microsoft

1. انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.
2. تأكد من أن الموفر **Litware, Inc.** متوفر وتم وضع علامة نشط عليه.
3. على الإطار المتجانب لموفر **Microsoft**، حدد **المستودعات**.

    > [!NOTE]
    > إذا كان مستودع من النوع **LCS** موجودًا، فيمكنك تخطي الخطوات المتبقية من هذا الاجراء.

4. حدد **إضافة**.
5. في مربع حوار القائمة المنسدلة، في مجموعة حقل **نوع مستودع التكوين**، حدد الخيار **LCS**
6. حدد **إنشاء مستودع**.
7. حدد **موافق**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>الحصول على تكوينات النموذج التي توفرها Microsoft

1. على الجانب الأيمن من الصفحة‏‎ **مستودعات التكوين**، حدد الزر **إظهار عوامل التصفية** (رمز القمع).
2. أضف عامل تصفيه لقيمة **LCS** في حقل **النوع**، واستخدم عامل التشغيل **يبدأ بـ**.
3. حدد **تطبيق**.
4. حدد **فتح**.
5. في الشجرة، حدد **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
6. في علامة التبويب السريعة **الإصدارات**، حدد الإصدار **1**.

    > [!NOTE]
    > إذا لم يتوفر الزر **استيراد‏‎** على علامة التبويب السريعة **الإصدارات**، يمكنك تخطي الخطوات المتبقية لهذا الاجراء.

7. حدد **استيراد**.
8. حدد **نعم** لتأكيد استيراد الإصدار المحدد من تكوين نموذج **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.

### <a name="create-a-new-format-configuration"></a>قم بإنشاء تكوين تنسيق جديد

1. في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.
2. في الشجرة، حدد **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
3. حدد **إنشاء التكوين**.

    > [!NOTE]
    > إذا لم يكن الزر **إنشاء التكوين** متوفرًا، فيجب تشغيل وضع التصميم في الصفحة **معلمات التقارير الإلكترونية‬** التي يمكن فتحها من مساحة عمل **إعداد التقارير الإلكترونية‬**.

4. في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد الخيار **تنسيق استنادًا إلى نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لنموذج البيانات**.
5. في حقل **الاسم**، أدخل **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (PDF)**.
6. في حقل **الوصف**، أدخل **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بتنسيق PDF**.

    > [!NOTE]
    > يتم تلقائيًا إدخال موفر التكوين النشط. سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين. على الرغم من أنه باستطاعة موفرين آخرين استخدام هذا التكوين، إلا أنه سيتعذر عليهم المحافظة عليه.

7. اختياري: في الحقل **نوع التنسيق** ، يمكنك تحديد تنسيق محدد للمستند الإلكتروني. إذا حددت **PDF**، في وقت التصميم، فإن مصمم عمليات التقارير الإلكترونية سيقدم فقط عناصر التنسيق القابلة للتطبيق فقط على المستندات المُنشأة بتنسيق PDF (**PDF\ملف**، **PDF\PDF أداة دمج** وغير ذلك). إذا تركت هذا الحقل فارغًا، سيتم تحديد تنسيق المستند الإلكتروني في وقت التصميم في مصمم عمليات التقارير عند إضافة عنصر التنسيق الأول. على سبيل المثال، إذا أضفت **Excel\File** كعنصر تنسيق أول، سيقدم لك مصمم عمليات التقارير الإلكترونية فقط عناصر التنسيق القابلة للتطبيق على المستندات المُنشأة بتنسيق Excel (**Excel\خلية**، **Excel\نطاق** وغير ذلك). تنسيق.
8. حدد **إنشاء التكوين**.

يتم إنشاء تكوين تنسيق جديد للتقارير الإلكترونية. يمكنك استخدام الإصدار التمهيدي من هذا التكوين لتخزين مكون تنسيق التقارير الإلكترونية الذي تم تصميمه لإنشاء المستندات الإلكترونية بتنسيق PDF.

### <a name="design-the-format-of-an-electronic-document"></a>تصميم تنسيق مستند إلكتروني

بعد ذلك، في تكوين تنسيق التقارير الإلكترونية الذي أنشأته، ستقوم بتصميم تنسيق التقارير الإلكترونية الذي يُنشئ تقرير **عنصر تحكم نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي** بتنسيق PDF. يجب أن تعرض الصفحة الأولى من هذا التقرير ملخصًا للتقرير وتفاصيل الحركات التجارية الخارجية التي تم إدخالها في هذا التقرير. ويجب أن تعرض الصفحات الأخرى تفاصيل الحركات التجارية الخارجية التي تم إدخالها في هذا التقرير. نظرًا لضرورة وجود تخطيطات مختلفة لصفحات التقارير التي تم إنشاؤها، سيتم استخدام قالبين مختلفين بتنسيق PDF في التنسيق الخاص بالتقارير الإلكترونية.

في أي عارض PDF، افتح قوالب PDF التي قمت بتنزيلها. لاحظ أن كل قالب يحتوي على حقول متعددة يجب تعبئتها. في كل قالب، يتم تقديم تفاصيل الحركات التجارية الأجنبية على شكل 42 صفًا، حيث يحتوي كل واحد منها على تسعه حقول. يظهر رقم الصف في نهاية كل اسم حقل (على سبيل المثال، **التاريخ 1**…**التاريخ 42** و **السلعة 1**…**السلعة 42**).

يبين الرسم التوضيحي التالي قالب PDF الخاص بالصفحة الأولى من التقرير.

![القالب 1](media/rcs-ger-filloutpdf-template1.png)

يبين الرسم التوضيحي التالي قالب PDF الخاص بالصفحات الأخرى من التقرير.

![القالب 2](media/rcs-ger-filloutpdf-template2.png)

1. في صفحة **التكوينات**، حدد **المصمم**.
2. حدد **إضافة جذر**.
3. في مربع الحوار المنسدل، في الشجرة، حدد **PDF \> أداة دمج PDF**.

    عندما تحدد **أداة دمج PDF** كعنصر الجذر الخاص بالتنسيق، فسيتم دمج كل وثائق PDF التي تم إنشاؤها في وقت التشغيل في مستند PDF نهائي واحد. إذا احتجت إلى قالب PDF واحد فقط لإنشاء كل المستندات المطلوبة باستخدام التنسيق الخاص بالتقارير الإلكترونية الذي تعمل على تصميمه، فيمكنك تحديد **ملف PDF** كعنصر جذر.

4. في الحقل **الاسم**، أدخل **إخراج**.
5. في الحقل **تفضيلات اللغة**، حدد **تفضيلات المستخدم**. سيتم إنشاء التقرير باللغة المفضلة للمستخدم الذي يقوم بتشغيله.
6. في الحقل **تفضيلات الثقافة**، حدد **تفضيلات المستخدم**. سيتم تنسيق القيم والتواريخ التي يتم تقديمها في صفحات التقرير استنادًا إلى الإعدادات المحلية المفضلة لدى المستخدم الذي يقوم بتشغيل التقرير.
7. حدد **موافق**.
8. في جزء الإجراءات، في علامة التبويب **استيراد** ، حدد **استيراد من**.

    عندما يتم ادراج مستند PDF قابل للتعبئة كقالب لتنسيق التقارير الإلكترونية هذا، يتم بشكل تلقائي إنشاء جميع عناصر تنسيق التقارير الإلكترونية المطلوبة (العناصر **ملف PDF** و **مجموعة حقول** و **الحقل** ) في التنسيق المصمم، استنادًا إلى بنية مستند PDF الذي يتم استيراده.

9. حدد **استعراض**. انتقل إلى الملف **IntrastatReportTemplate1.pdf** الذي قمت بتنزيله سابقًا كمطلب أساسي، ثم حدده.
10. حدد **موافق**.

    يتم تحميل الملف المحدد، وتتم تعبئة حقل **القالب** في مربع الحوار **استيراد من PDF**.

11. عيّن الخيار **حقول المجموعة** إلى **نعم**. إذا تضمن مستند PDF المحدد أي مجموعات حقول، سيتم استخدامها لتجميع عناصر تنسيق التقارير الإلكترونية التي يتم إنشاؤها. سيتم إنشاء عنصر تنسيق **مجموعة حقول** لهذا الغرض.

    في حاله تعيين هذا الخيار إلى **لا**، سيتم إنشاء عناصر تنسيق التقارير الإلكترونية المطلوبة كقائمة كاملة تتضمن العناصر المتداخلة تحت عنصر تنسيق **ملف PDF** الذي تم إنشاؤه.

12. حدد **موافق**.

    ![مربع الحوار "استيراد من PDF"](media/rcs-ger-filloutpdf-importtemplate.png)

13. في الشجرة، قم بتوسيع **الإخراج‬**.

    لاحظ إنشاء مكون **ملف PDF** تلقائيًا لإدارة إنشاء الصفحة الأولى من التقرير الذي يتم إنشاؤه في وقت التشغيل.

14. في الشجرة، قم بتوسيع **الإخراج‬‏‎ \> ملف PDF**.

    لاحظ أن القائمة المهيكلة لعناصر التنسيق قد نشأت تلقائيًا في تنسيق التقارير الإلكترونية هذا استنادًا PDF بنية مستند PDF القابل للتعبئه الذي استوردته في وقت سابق.

15. في الشجرة، حدد **الإخراج‬‏‎ \> ملف PDF**.
16. في الحقل **الاسم**، أدخل **الصفحة 1**.

    سيتم استخدام عنصر التنسيق هذا لإنشاء الصفحة الأولى من تقرير **عنصر تحكم نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. ستعرض هذه الصفحة ملخص التقرير وتفاصيل الحركات التجارية الخارجية.

    إذا تركت الحقل **تفضيلات‏‎ اللغة** فارغًا، فسيحدد إعداد **تفضيلات‏‎ اللغة** للعنصر الأصل **أداة دمج PDF** لغة التقرير الذي تم إنشاؤه باستخدام عنصر التنسيق هذا. يمكنك تحديد قيمة أخرى لتجاوز إعداد العنصر الأصل.

    إذا تركت الحقل **تفضيلات‏‎ الثقافة‬‏** فارغًا، فسيحدد إعداد **تفضيلات‏‎ الثقافة** للعنصر الأصل **أداة دمج PDF** الإعدادات المحلية للتقرير الذي تم إنشاؤه باستخدام عنصر التنسيق هذا. تحدد الإعدادات المحلية تنسيق القيم والتواريخ في صفحات التقرير. يمكنك تحديد قيمة أخرى لتجاوز إعداد العنصر الأصل.

17. في جزء الإجراءات، حدد علامة التبويب **استيراد**. لاحظ أن الزر **تحديث من PDF** أصبح متوفرًا لعنصر التنسيق المحدد **ملف PDF**.

    يمكنك استخدام هذا الزر لاستيراد قالب PDF المحدث إلى التنسيق المحرر. عندما يتم استيراد قالب PDF المحدث، ستتغير قائمة عناصر التنسيق وفقًا لذلك:

    - بالنسبة إلى أي حقول جديدة في قالب PDF المحدث، يتم إنشاء عناصر تنسيق جديدة بتنسيق التقارير الإلكترونية الذي تم تحريره.
    - إذا لم يعد قالب PDF المحدث يتضمن حقولاً تطابق أي عناصر تنسيق موجودة في تنسيق التقارير الإلكترونية الذي تم تحريره، فسيتم حذف عناصر التنسيق هذه من تنسيق التقارير الإلكترونية.

18. ضمن علامة التبويب **تنسيق**، حدد **مرفقات**.

    لاحظ أنه تم إرفاق مستند PDF الذي تم استيراده بتنسيق التقارير الإلكترونية الذي تم تحريره.

    ![معاينة مرفقات PDF](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. تابع تصميم هذا التنسيق عن طريق استيراد قالب PDF الثاني وإضافة لارتباطات الضرورية إلى مصادر البيانات، وما إلى ذلك.
20. حدد **حفظ**.
21. قم بإغلاق الصفحة.
22. حدد **حذف**.
23. حدد **نعم**.

لمعرفة كيفية استخدام عناصر التنسيق **أداة دمج PDF** و **ملف PDF** و **مجموعة الحقول** و **الحقل** لتوليد مستندات بتنسيق PDF، يمكنك إدراج وتحليل تنسيق التقارير الإلكتروني النموذجي

### <a name="import-the-format-configuration"></a>استيراد تكوين التنسيق

بعد ذلك، ستقوم باستيراد تنسيق التقارير الإلكترونية النموذجي الذي قمت بتنزيله في وقت سابق لإنشاء تقرير **عنصر تحكم نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬‏‫** بتنسيق PDF. يجب أن تعرض الصفحة الأولى من التقرير ملخصًا للتقرير وتفاصيل الحركات التجارية الخارجية التي تم إدخالها في هذا التقرير. ويجب أن تعرض الصفحات الأخرى تفاصيل الحركات التجارية الخارجية التي تم إدخالها في هذا التقرير.

1. في صفحة **التكوينات**، حدد **التبادل‬ \> تحميل من ملف XML**.
2. حدد **استعراض**. انتقل إلى الملف **Intrastat report (PDF).version.1.1.xml** الذي قمت بتنزيله سابقًا كمطلب أساسي، ثم حدده.
3. حدد **موافق**.

## <a name="analyze-the-format-configuration"></a>تحليل تكوين التنسيق

### <a name="format-layout"></a>تخطيط التنسيق

1. في صفحة **التكوينات**، في الشجرة، حدد **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (PDF)**.
2. حدد **المصمم**.
3. حدد **إظهار التفاصيل**.
4. في الشجرة، قم بتوسيع **الإخراج‬‏‎: أداة دمج PDF**.

    لاحظ ان تنسيق التقارير الإلكترونية هذا يحتوي على عنصري **ملف PDF**، يستخدم كل واحد منهما قالب PDF مختلفًا. يتم استخدام قالب لإنشاء الصفحة الأولى من التقرير بتنسيق PDF، ويتم استخدام القالب الآخر لإنشاء الصفحات الأخرى.

5. في الشجرة، قم بتوسيع **الإخراج‬‏‎: أداة دمج PDF \> الصفحة 1: ملف PDF (IntrastatReportTemplate1)**.
6. في الشجرة، قم بتوسيع **الإخراج‬‏‎: أداة دمج PDF \> الصفحة N: ملف PDF (IntrastatReportTemplate2)**.

    نظرًا لاختلاف محتويات قالبي PDF، تختلف أيضًا بنية عناصر التنسيق المتداخلة للعناصر في **ملفي PDF**.

### <a name="format-mapping"></a>تعيين تنسيق

1. في الصفحة **مصمم التنسيق**، حدد علامة التبويب **التعيين**.
2. في الشجرة، قم بتوسيع **ترحيل الصفحات \> الصفحات**.

    ![يتم توسيع صفحة مصمم المعادلة‬ حيث شجرة النموذج.](media/rcs-ger-filloutpdf-reviewformat.png)

    لاحظ التفاصيل التالية:

    - لا يرتبط عنصر التنسيق **الإخراج \> الصفحة 1** لنوع **ملف PDF** بأي مصدر بيانات، والتعبير **ممكّن** لعنصر التنسيق هذا فارغ. وبالتالي، في وقت التشغيل، ستتم تعبئة قالب PDF **IntrastatReportTemplate1** في مرة واحدة فقط عند إنشاء مستند PDF فردي.
    - يرتبط عنصر التنسيق **الإخراج \> الصفحة N** لنوع **ملف PDF** بمصدر البيانات **Paging.PageN** من النوع **قائمة سجلات** والتعبير **ممكّن** لعنصر التنسيق هذا فارغ. وبالتالي، في وقت التشغيل، ستتم تعبئة قالب PDF **IntrastatReportTemplate2** لكل سجل من قائمة السجلات المرتبطة عند إنشاء مستند PDF فردي.
    - نظرًا لكون عنصري التنسيق **الصفحة 1: ملف PDF** و **الصفحة N: ملف PDF** من العناصر التابعة لعنصر التنسيق **الإخراج: أداة دمج PDF**،سيتم دمج جميع مستندات PDF التي تتم تعبئها في مستند PDF واحد نهائي.
    - يتم تكوين مصدري البيانات **Paging.Page1** و **Paging.PageN** كعوامل تصفية للسجلات من مصدر البيانات **Paging.Pages**. يتم تكوين مصدر البيانات هذا لتقسيم المجموعة الكاملة للحركات التجارية الأجنبية إلى دُفعات. تحتوي كل دُفعة على ما يصل إلى 42 سجل. يتم استخدام تعبير التقارير الإلكترونية التالي لتقسيم الحركات إلى دُفعات:

        SPLITLIST(Totals.CommodityRecord,42)

    - يحتوي مصدر البيانات **Paging.Pages** على عناصر **Paging.Pages.Enumerated** التي تقوم بإرجاع تفاصيل كل سجل مضمن في المجموعة. تتضمن هذه التفاصيل تسلسل السجل في الدفع الحالية (الحقل **Paging.Pages.Enumerated.Number**). يُستخدم الحقل **Paging.Pages.Enumerated.Number** في التعبير **الاسم** في عناصر تنسيق **حقل PDF** لإنشاء اسم حقل يستند إلى رقم الحركة بشكل ديناميكي في الدُفعة. عندئذ يتم استخدام اسم الحقل الذي يتم إنشاؤه لتعبئة حقل PDF الصحيح في قالب PDF المستخدم.
    - يرتبط عنصر التنسيق **الإخراج \> الصفحة N \> Details 2** لنوع **مجموعة PDF** بمصدر البيانات **Paging.PageN.Enumerated** (أو **\@.Enumerated** عند استخدام وضع طريقة عرض **المسار النسبي**) من النوع **قائمة سجلات**. ولذلك ، في وقت التشغيل ، ستتم تعبئة العناصر المتداخلة لمجموعة PDF هذه لكل سجل من قائمة السجلات المرتبطة. وبهذه الطريقة، يتم إنشاء سطور PDF المنفردة عند تعبئة حقول PDF التالية: التاريخ N، الاتجاه N، السلعة N وغير ذلك لكل Nth من 42 سجلاً من القائمة **Paging.PageN.Enumerated**. وبالتالي، وفي هذا الإطار، يشبه سلوك عنصر تنسيق **مجموعة الحقول** سلوك عناصر التنسيق **XML \> التسلسل** و **النص \> التسلسل**.

3. في الشجرة ، قم بتوسيع **الإخراج \> الصفحة N \> التفاصيل2**.
4. في الشجرة ، حدد **الإخراج \> الصفحة N \> التفاصيل2 \> PageFooter**.

    لاحظ أن سمة **الاسم** لعنصر التنسيق هذا معرّفة كـ **PageFooter‎**. ولاحظ أيضًا أن تعبير **الاسم** لعنصر التنسيق فارغ.

5. في الشجرة ، حدد **الإخراج \> الصفحة N \> التفاصيل2 \> التصحيح 1**.

    لاحظ أن سمة **الاسم** لعنصر التنسيق هذا معرّفة كـ **التصحيح 1‎**. ولاحظ أيضًا أنه تم تعريف تعبير **الاسم** لعنصر التنسيق كـ **Paging.FldName("Correction",\@.Number)**.

![مصمم التنسيق حيث تم تحديد تعيين](media/rcs-ger-filloutpdf-reviewformat2.png)

لاحظ ان عنصر تنسيق‏‎ **الحقل** يُستخدم لتعبئة حقل فردي من مستند PDF قابل للتعبئة تم تعريفه كقالب لعنصر التنسيق الأصل **ملف PDF**. يحدد ارتباط عنصر تنسيق **ملف PDF** أو عناصر المتداخلة، عند وجودها، القيمة التي تم إدخالها في حقول PDF المناظرة. يمكن استخدام خصائص مختلفة لعنصر تنسيق **الحقل** لتحديد أي حقل PDF تتم تعبئته بواسطة عنصر تنسيق فردي:

- ضمن علامة التبويب **تنسيق**، سمة **الاسم** لعنصر التنسيق
- ضمن علامة التبويب **التعيين**، تعبير **الاسم** لعنصر التنسيق

نظرًا لكون الخاصيتين اختياريتين لعنصر تنسيق **الحقل**، يتم تطبيق القواعد التالية لتحديد حقل PDF الهدف:

- إذا كانت سمة **الاسم** فارغة، وقام تعبير **الاسم** بإرجاع سلسلة فارغة في وقت التشغيل، يتم طرح استثناء في وقت التشغيل لإعلام المستخدم بتعذر العثور على حقل PDF في قالب PDF الذي يتم استخدامه لتعبئة مستند PDF.
- إذا تم تعريف سمة **الاسم** وكان تعبير **الاسم‏‎** فارغًا، ستتم تعبئة ملف PDF الذي يحمل الاسم نفسه لسمة **الاسم‏‎** لعنصر التنسيق.
- إذا تم تعريف سمة **الاسم** وكان تعبير **الاسم‏‎** مكوّنًا، ستتم تعبئة ملف PDF الذي يحمل الاسم نفسه للقيمة التي يرجعها تعبير **الاسم‏‎** لعنصر التنسيق.

> [!NOTE]
> يمكن تعبئة خانه اختيار PDF كما هو محدد بالطرق التالية:
>
> - عندما يرتبط عنصر تنسيق‏‎ **الحقل** المناظر بحقل مصدر بيانات من نوع البيانات **منطقي** لديه القيمة **True**
> - عندما يحتوي عنصر تنسيق **الحقل** المناظر على عنصر تنسيق **سلسلة** متداخل يرتبط بحقل مصدر بيانات لديه قيمة نصية من **1** أو **صوات** أو **نعم**

## <a name="run-the-format-configuration"></a>تشغيل تكوين التنسيق

### <a name="import-the-format-configuration"></a>استيراد تكوين التنسيق

بعد ذلك، تقوم بتحميل تنسيق التقارير الإلكترونية النموذجي **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (استيراد من Excel**). وقد تم تصميم هذا التنسيق لتحليل مصنف Microsoft Excel محدد من قبل المستخدم يحاكي الحركات التجارية الأجنبية.

1. في صفحة **التكوينات**، حدد **التبادل‬ \> تحميل من ملف XML**.
2. حدد **استعراض**. انتقل إلى الملف **Intrastat (import from Excel).version.1.1.xml** الذي قمت بتنزيله سابقًا كمطلب أساسي، ثم حدده.
3. حدد **موافق**.
4. في الشجرة، حدد **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (استيراد من Excel)**.
5. حدد **تحرير**.
6. قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**

    > [!NOTE]
    > إذا قمت سابقًا بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم** بالنسبة إلى تكوين **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي** أو تكوين آخر متداخل تحت التكوين **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، فعيّن هذا الخيار إلى **لا**.

    عند تعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم**، يتم تعيين تنسيق التقارير الإلكترونية **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (استيراد من Excel)** المستورد كمصدر بيانات افتراضي لتكوين تنسيق **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (PDF)**. بعد ذلك، عند تشغيل تكوين تنسيق **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (PDF)** ، سيحاكي محتوى مصنف Excel الذي تم تحليله بواسطة **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (استيراد من Excel)** الحركات التجارية الخارجية التي يجب إدخالها في التقرير. يبين الرسم التوضيحي التالي مثالاً لمصنف Excel.

    ![مصنف Excel يحتوي على بيانات نموذجية](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>تشغيل تكوين التنسيق

1. في صفحة **التكوينات**، في الشجرة، حدد **نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (PDF)**.
2. حدد **تشغيل**.
3. حدد **استعراض**. انتقل إلى الملف **Intrastat sample data.xlsx** الذي قمت بتنزيله سابقًا كمطلب أساسي، ثم حدده.
4. حدد **موافق**.
5. في الحقل **اتجاه التقرير**، حدد **كلاهما‬** لتعبئة كافة الحركات من مصنف Excel المستورد في تقرير PDF الذي تم إنشاؤه.
6. حدد **موافق**.
7. راجع مستند PDF الذي يتم إنشاؤه.

يبين الرسم التوضيحي التالي مثالاً للصفحة الأولى من التقرير الذي يتم إنشاؤه.

![الصفحة الأولى من التقرير المُنشأ](media/rcs-ger-filloutpdf-generatedreport.png)

يبين الرسم التوضيحي التالي مثالاً لصفحة أخرى من التقرير الذي يتم إنشاؤه.

![الصفحة الأخرى من التقرير المُنشأ](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a>الموارد الإضافية

- [التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [تصميم تكوينات التقارير الإلكترونية لإنشاء تقارير بتنسيق Word](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]