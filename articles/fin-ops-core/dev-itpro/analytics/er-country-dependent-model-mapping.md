---
title: تكوين تعيينات نماذج التقارير الإلكترونية (ER) التي تعتمد على سياق البلد
description: تشرح هذه المقالة كيفية إعداد تعيينات نماذج التقارير الإلكترونية لكي تعتمد علي سياق البلد/المنطقة الخاص بالكيان القانوني الذي يتحكم في استخدامه.
author: kfend
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable
ms.openlocfilehash: 5db0936682e0cc052622658ac14046013bc4fd87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277745"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>تكوين تعيينات نماذج التقارير الإلكترونية التابعة لسياقات البلدان

[!include[banner](../includes/banner.md)]

يمكنك تكوين تعيينات نماذج التقارير الإلكترونية (ER) بحيث تقوم بتطبيق نموذج بيانات تقارير إلكترونية عام ولكنه خاص بـ Dynamics 365 Finance. تشرح هذه المقالة كيفية تصميم تعيينات نماذج تقارير إلكترونية متعددة لنموذج بيانات تقارير إلكترونية للتحكم في كيفية استخدامها بواسطة تنسيقات التقارير الإلكترونية المقابلة التي يتم تشغيلها من الشركات التي لها سياقات بلد/منطقة مختلفة.

## <a name="prerequisites"></a>المتطلبات الأساسية

لإكمال الأمثلة في هذا البرنامج التعليمي، يجب أن تتمتع بالوصول التالي:

- الوصول إلى Finance لأحد الأدوار التالية:
    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

- يمكنك الوصول إلى مثيل خدمات التكوين التنظيمية (RCS) التي تم توفيرها لنفس المستأجر مثل التمويل لأحد الأدوار التالية:
    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

تتطلب بعض الخطوات الواردة في هذه المقالة تنفيذ تنسيق تقارير إلكترونية. في بعض الحالات، يتاثر تنفيذ التنسيق الخاص بالتقارير الإلكترونية بسياق البلد/المنطقة للشركة التي تقوم بتسجيل الدخول إليها حاليا. يمكنك تشغيل تنسيق التقارير الإلكترونية في مثيل RCS الحالي إذا كانت الشركة التي لها سياق البلد/المنطقة المطلوب متوفرة في RCS. وبخلاف ذلك، يجب تحميل إصدار مكتمل من تعيين نموذج التقارير الإلكترونية وتكوينات تنسيق التقارير الإلكترونية التي تستخدم نموذج البيانات التقارير الإلكترونية إلى مثيل التمويل الخاص بك، ثم قم بتشغيل تنسيق التقارير الإلكترونية في مثيل التمويل هذا. للحصول علي معلومات حول كيفيه استيراد التكوينات التي توجد في RCS إلى مثيل تمويل، راجع [استيراد التكوينات من RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>حاله تعيين نموذج واحد

اتبع الخطوات الواردة في [ملحق 1](#appendix1) من هذه المقالة لتصميم مكونات التقارير الإلكترونية المطلوبة. لديك الآن تكوين تعيين نموذج **التعيين (عام)** الذي يحتوي على تعيين النموذج لتعريف **نقطة الإدخال 1**.

![صفحه تكوينات ER ، التنسيق للتعرف علي تكوين التعيينات.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>تشغيل التنسيق المكوَّن

1.  في **صفحة التكوينات**، في علامة التبويب السريع **الإصدارات**، حدد **تشغيل**.
2.  حدد **موافق**.

لاحظ أن مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه. بسبب تكوين هذا التنسيق لاستخدام **تعريف نقطه الإدخال 1**، وتعيين نموذج واحد فقط متوفر حاليا للنموذج الأساسي الذي يحتوي علي تعيين لهذا التعريف ، فان تنسيق التقارير الإلكترونية الذي تم تنفيذه استخدم تعيين نموذج **التعيين (عام)** لتكوين **التعيين (عام)** كمصدر بيانات. لذلك ، يحتوي الملف الذي تم تنزيله علي **نص الوظيفة العامة 1**

## <a name="multiple-shared-model-mappings-case"></a>حاله تعيينات متعددة النماذج المشتركة

اتبع الخطوات الواردة في [ملحق 2](#appendix2) من هذه المقالة لتصميم مكونات التقارير الإلكترونية المطلوبة. لديك الآن تكوينات تعيين نموذج **التعيين (عام)** و **التعيين المخصص (عام)**، والتي يحتوي كل منها على تعيين النموذج لتعريف **نقطة الإدخال 1**.

![صفحه تكوينات ER ، تعيين تكوين عام مخصص.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>تشغيل التنسيق المكوَّن

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.
2.  في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.
3.  حدد **موافق**.

لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد غير ناجح. تظهر رسالة خطا لاعلامك بوجود أكثر من تعيين نموذج واحد لنموذج **النموذج للتعرف على التعيينات** وتعريف **نقطة الإخال 1** في **التعيين (عام)** وتكوينات تعيين نموذج **التعيين المخصص (عام)**. وتوصي الرسالة أيضا بتحديد أحد هذه التكوينات كتكوين افتراضي.

![صفحه تكوينات ER مع رسالة الخطا.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>تحديد تكوين افتراضي للتعيين

اتبع الخطوات التالية **لتعريف تكوين تعيين** نموذج مخصص (عام) كتكوين افتراضي ، بحيث يمكن استخدام التعيينات الخاصة بها كمصادر بيانات للتنسيق الذي يمكن من خلاله **التعرف علي تنسيق التعيينات** ل ER.

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين المخصص (عام)**.
2.  حسب الحاجة، حدد **تحرير** لتجعل الصفحة الحالية جاهزه للتحرير.
3.  قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**
4.  حدد **حفظ**.

![صفحه تكوينات ER ، تم تعيين الاعداد الافتراضي لشريط تمرير تعيين النموذج إلى نعم.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>تشغيل التنسيق المكوَّن

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.
2.  في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.
3.  حدد **موافق**.

لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح. مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه. بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين المخصص (عام)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **نسخة التعيين (عام)** لتكوين **التعيين المخصص** كمصدر بيانات. لذلك، يحتوي الملف الذي تم تنزيله على **الوظيفة العامة المخصصة 1**.

> [!NOTE]
> إذا قمت بتغيير الشركة التي قمت بتسجيل الدخول اليها حاليا وتشغيل تنسيق التقارير الإلكترونية هذا مره أخرى ، ستحصل علي نفس المحتوي في الملف الذي تم إنشاؤه ، لان تكوين تعيين نموذج التقارير الإكترونية الافتراضي لا يحتوي علي إيه قيود تعتمد علي الشركة.

## <a name="multiple-mixed-model-mappings-case"></a>حاله تعيينات متعددة النماذج المختلطة

اتبع الخطوات الواردة في [ملحق 3](#appendix3) من هذه المقالة لتصميم مكونات التقارير الإلكترونية المطلوبة. لديك الآن تكوينات **التعيين (عام)**، و **التعيين المخصص (عام)**، و **تعيين نموذج التعيين (FR)** التي تحتوي على تعيين النموذج لتعريف **نقطة الإدخال 1**.

لاحظ ان الإصدار 1 من تكوين تعيين النموذج **التعيين (FR)** تم تكوينه بحيث يتم تطبيقه فقط علي تنسيقات التقارير الإلكترونية لنموذج **النموذج للتعرف على التعيينات** الذي يعمل في شركات Finance التي لها سياق بلد/منطقه فرنسية.

![صفحه تكوينات ER ، تكوين (FR) تعيين نموذج.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>تشغيل التنسيق المكوَّن

1.  قم بتغيير الشركة إلى **FRSI**.
2.  في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.
3.  في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.
4.  حدد **موافق**.

لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح. مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه. بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين المخصص (عام)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **نسخة التعيين (عام)** لتكوين **التعيين المخصص** كمصدر بيانات. لذلك، يحتوي الملف الذي تم تنزيله على **الوظيفة العامة المخصصة 1**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>حدد تكوين التعيين الخاص بفرنسا كتكوين افتراضي

اتبع الخطوات التالية لتحديد تكوين تعيين نموذج **التعيين (FR)** باعتباره التكوين الافتراضي. لاحظ انه نظرا لان هذا التعيين مخصص لفرنسا، فانه سيتم اعتباره التعيين الافتراضي بين كافة تكوينات تعيينات النماذج التي تشتمل على كود البلد **FR** في حقل **أكواد البلد/المنطقة ISO**.

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين (FR)**.
2.  حسب الحاجة، حدد **تحرير** لتجعل الصفحة الحالية جاهزه للتحرير.
3.  قم بتعيين الخيار **الاعداد الافتراضي لتعيين النموذج** إلى **نعم.**
4.  حدد **حفظ**.

![صفحه تكوينات ER ، تكوين (FR) تعيين، تم تعيين الاعداد الافتراضي لشريط تمرير تعيين النموذج إلى نعم.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>تشغيل التنسيق المكوَّن

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.
2.  في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.
3.  حدد **موافق**.

لاحظ ان تنفيذ تنسيق التقارير الإلكترونية المحدد ناجح. مستعرض الويب يعرض تنزيل الملف النصي الذي تم إنشاؤه بواسطة تنسيق التقارير الإلكترونية الذي تم تنفيذه. بسبب تكوين هذا التنسيق لاستخدام تعريف **نقطة الإدخال 1**، تم تحديد تكوين تعيين نموذج **التعيين (FR)** باعتباره التكوين الافتراضي، واستخدم تنسيق التقارير الإلكترونية المنفذ تعيين نموذج **التعيين (FR)** لتكوين **التعيين (FR)** كمصدر بيانات. لذلك ، يحتوي الملف الذي تم تنزيله علي **وظيفة FR 1**

> [!NOTE]
> في حاله تغيير الشركة التي قمت بتسجيل الدخول اليها حاليا وتشغيل تنسيق التقارير الإلكترونية هذا مره أخرى ، سيعتمد الإخراج علي سياق البلد/المنطقة الخاص بالشركة المحددة.

## <a name="other-model-mapping-cases"></a>حاله تعيينات النماذج الأخرى

وكما شاهدت، فان تحديد تعيين النموذج لتنفيذ تنسيق التقارير الإلكترونية يعمل بالطريقة التالية:

- يتم تحديد تعريف تعيين النموذج الذي يستخدمه تنسيق التقارير الإلكترونية (**نقطه الإدخال 1** في الأمثلة الموجودة في هذه المقالة).
- يمكن استخدام كافة تكوينات التعيين التي تحتوي على تعيين لديه التعريف المحدد، والتي تفي بقيود سياق البلد/المنطقة التي تم تكوينها لتشغيل تنسيق التقارير الإلكترونية (**التعيين (عام)**، **والتعيين المخصص (عام)**، و **التعيين (FR)** في الأمثلة الواردة في هذه المقالة).
- ويكون لأي تعيين نموذج افتراضي له قيود علي سياق البلد/المنطقة أعلى أولوية للتحديد (**التعيين (FR)** في الأمثلة الموجودة في هذه المقالة).
- ويكون لأي تعيين نموذج افتراضي لا يشتمل على قيود سياق البلد/المنطقة الأولوية الأعلى التالية (**التعيين المخصص (عام)** في الأمثلة الموجودة في هذا الموضوع).
- ان اي تعيين نموذج له قيود علي سياق البلد/المنطقة له اولويه اعلي للتحديد مقارنةً بتعيين نموذج ليس له قيود علي سياق البلد/المنطقة.

يوفر الجدول التالي معلومات حول نتائج تحديد تعيين النماذج لكافة الحالات المحتملة لإعدادات تعيين النماذج:

- يشير العمود 1 إلى ما إذا كان التعيين الأول للنموذج الذي ليس له قيود على سياق البلد/المنطقة (على سبيل المثال، تعيين **التعيين (عام)**) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.
- يشير العمود 2 إلى ما إذا كان التعيين الثاني للنموذج الذي ليس له قيود على سياق البلد/المنطقة (على سبيل المثال، تعيين **التعيين المخصص (عام)**) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.
- يشير العمود 3 إلى ما إذا كان التعيين الأول للنموذج يشتمل على قيود على سياق البلد/المنطقة A (على سبيل المثال، تعيين **التعيين (FR)** الخاص بفرنسا) موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.
- يشير العمود 4 إلى ما إذا كان التعيين الثاني للنموذج يشتمل على قيود على سياق البلد/المنطقة A موجودًا، وإذا كان الأمر كذلك، وما إذا كان تم تعيين **الإعداد الافتراضي لتعيين النموذج** إلى **نعم** له.
- يقدم العمود رقم 5 النتيجة الخاصة بتحديد تعيين النموذج لتنفيذ أحد تنسيقات التقارير الإلكترونية ضمن التحكم في الشركة التي لها سياق A للمنطقه/البلد.
- يقدم العمود رقم 6 النتيجة الخاصة بتحديد تعيين النموذج لتنفيذ أحد تنسيقات التقارير الإلكترونية ضمن التحكم في الشركة التي لها سياق B للمنطقه/البلد.

وتشير علامة الجمع (+) في الجدول إلى وجود تكوين تعيين النموذج في المثيل الحالي لخدمة Microsoft Azure المستخدمة لتشغيل تنسيق التقارير الإلكترونية (إما Finance أو RCS).

| الحالة | تعيين النموذج 1 دون سياق البلد/المنطقة (MM1) | تعيين النموذج 2 دون سياق البلد/المنطقة (MM2) | تعيين النموذج 1 مع سياق البلد/المنطقة A (MM1A) | تعيين النموذج 2 مع سياق البلد/المنطقة A (MM2A) | تشغيل ضمن عنصر التحكم في شركه لها سياق منطقه/البلد A | تشغيل ضمن عنصر التحكم في شركه لها سياق منطقه/البلد B |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | خطأ (تعيين مفقود)   | خطأ (تعيين مفقود)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | خطأ (تعيينات متعددة) | خطأ (تعيينات متعددة)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | خطأ (تعيينات متعددة) | MM1                        |
|     6   |     +   | افتراضية |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | افتراضية |         | MM1A                      | MM1                        |
|     8   |     +   |         | افتراضية |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | افتراضية | افتراضية | خطأ (تعيينات متعددة) | MM1                        |
|    10   | افتراضية |         |         |         | MM1                       | MM1                        |
|    11   | افتراضية |    +    |         |         | MM1                       | MM1                        |
|    12   | افتراضية |         |    +    |         | MM1                       | MM1                        |
|    13   | افتراضية | افتراضية |         |         | خطأ (تعيينات متعددة) | خطأ (تعيينات متعددة)  |
|    14   | افتراضية |         | افتراضية |         | MM1A                      | MM1                        |
|    15   | افتراضية |         | افتراضية | افتراضية | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | افتراضية | افتراضية | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>التعرف على التعيين الذي تم استخدامه في تنفيذ أحد تنسيقات التقارير الإلكترونية

### <a name="configure-er-user-parameters"></a>تكوين معلمات مستخدم التقارير الإلكترونية

1.  في صفحة **التكوينات**، في جزء الإجراء، في علامة التبويب **التكوينات**، حدد **معلمات المستخدمين**.
2.  قم بتعيين خيار **تشغيل في وضع التصحيح** إلى **نعم**.
4.  حدد **موافق**.

### <a name="run-the-configured-format"></a>تشغيل التنسيق المكوَّن

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد عنصر **التنسيق للتعرف على التعيينات**.
2.  في علامة التبويب السريعة **الإصدارات**، حدد **تشغيل**.
3.  حدد **موافق**.

### <a name="review-the-er-debug-log"></a>مراجعة سجل تصحيح التقارير الإلكترونية

1.  في جزء التنقل، انتقل إلى **الوحدات \> إدارة المؤسسة \> التقارير الإلكترونية \> سجل تصحيح التكوين**.
2.  حدد الزر **إعادة تحميل هذه الصفحة**.

![صفحة سجلات تشغيل التقارير الإلكترونية.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

لاحظ انه تمت أضافه سجل جديد إلى سجل تصحيح التقارير الإلكترونية لتنسيق التقارير الإلكترونية الذي تم تنفيذه. ونظرا لأنه يتم تعيين حقل **المستوى** لهذا السجل إلى **معلومات**، يكون السجل معلوماتيًا. نظرًا لتعيين حقل مكون التنسيق إلى **تكوين التعيين**، يقوم السجل باعلامك عن تعيين النموذج الذي تم استخدامه أثناء تنفيذ تنسيق التقارير الإلكترونية **التنسيق للتعرف على التعيينات** (المحدد في حقل **اسم التكوين**). ويعلمك محتوى حقل **النص الذي تم إنشاؤه** بأن مكون تعيين **التعيين (FR)** الموجود في تكوين **التعيين (FR)** تم استخدامه لتشغيل هذا التقرير.

## <a name="appendix-1"></a><a name="appendix1"></a> الملحق 1

### <a name="configure-a-sample-data-model"></a>تكوين نموذج بيانات النموذج

سجل الدخول إلى مثيل RCS.

في هذا المثال، سوف تنشئ تكوينًا للشركة النموذجية Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً في RCS إكمال الخطوات الموجودة في الإجراء [‏‫إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).

#### <a name="create-an-er-data-model-configuration"></a>إنشاء تكوين نموذج بيانات تقارير إلكترونية

1.  في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.
2.  حدد تجانب **تكوينات التقارير‬**.
3.  في صفحة **التكوينات**، حدد **إنشاء التكوين**.
4.  في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **النموذج للتعرف على التعيينات**.
5.  حدد **إنشاء التكوين**.
6.  حدد علامة التبويب السريعة **مكونات التكوين**.

لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير. يحتوي هذا الإصدار على مكون نموذج البيانات.

#### <a name="design-a-sample-data-model"></a>تصميم نموذج بيانات النموذج

1.  في **صفحة التكوينات**، حدد **المصمم**.
2.  حدد **جديد**.
3.  في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **نقطة الإدخال 1**.
4.  حدد **إضافة**.
5.  حدد **جديد**.
6.  في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **وصف الوظيفة**.
7.  حدد **إضافة**.
8.  حدد **جديد**.
9.  في مربع الحوار المنسدل، في مجموعة حقول **العقدة الجديدة**، حدد **جذر النموذج**.
10. في حقل **الاسم**، أدخل **نقطة الإدخال 2**.
11. حدد **نقطه الإدخال 2**.
12. حدد **إضافة**.
13. حدد **جديد**.
14. في مربع الحوار المنسدل، في حقل **الاسم**، أدخل **وصف الوظيفة**.
15. حدد **إضافة**.

    ![صفحة مصمم نموذج بيانات التقارير الإلكترونية.](./media/RCS-Context-specific-mapping-Model.PNG)

16. حدد **حفظ**.
17. قم بإغلاق الصفحة.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>إكمال الإصدار المعدل من تكوين النموذج

1.  في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.

    > قم بتغيير حالة تكوين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه لتصميم تنسيقات وتعيينات النماذج المطلوبة.

2.  حدد **مكتمل**.
3.  حدد **موافق**.

لاحظ أن التكوين الذي قمت بإنشائه تم حفظه باعتباره الإصدار المكتمل 1.

### <a name="configure-a-sample-model-mapping"></a>تكوين تعيين نموذج عينة

#### <a name="create-an-er-model-mapping-configuration"></a>إنشاء تكوين تعيين نموذج التقارير الإلكترونية

1.  في صفحة **التكوينات**، حدد **إنشاء التكوين**.
2.  في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد **تعيين النموذج استنادًا إلى نموذج نموذج البيانات للتعرف إلى التعيينات**.
3.  في حقل **الاسم**، أدخل **التعيين (عام)**.
4.  في حقل **تعريف نموذج البيانات**، حدد **نقطة الإدخال 1**.
5.  حدد **إنشاء التكوين**.

لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير. يحتوي هذا الإصدار على مكون تعيين النموذج.

#### <a name="design-a-sample-model-mapping"></a>تصميم تعيين نموذج عينة

1.  في صفحة **التكوينات**، حدد **المصمم**.

    لاحظ انه تمت أضافه تعيين النموذج من نوع اتجاه **إلى النموذج** تلقائيًا إلى هذا المكون لتعريف **نقطة الإدخال 1**.
    
2.  حدد **المصمم** للبدء في تحرير تعيين النموذج المضاف.
3.  في قسم **نموذج البيانات**، حدد **تحرير**.
4.  في حقل **المعادلة**، أدخل **"الوظيفة العامة 1"**.
5.  حدد **حفظ**.
6.  أغلق صفحة **مصمم المعادلة**.

    ![صفحه مصمم تعيين نموذج طراز طراز الطراز ل ER ، تعريف نقطه الإدخال 1.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  حدد **حفظ**.
8.  أغلق صفحة **مصمم تعيين النموذج**.
9.  حدد **جديد**.
10. في حقل **التعريف**، حدد **نقطة الإدخال 2**.
11. في حقل **الاسم**، أدخل **التعيين (عام) 2**.
12. حدد **المصمم**.
13. في قسم **نموذج البيانات**، حدد **تحرير**.
14. في حقل **المعادلة**، أدخل **"الوظيفة العامة 2"**.
15. حدد **حفظ**.
16. أغلق صفحة **مصمم المعادلة**.

    ![صفحه مصمم تعيين نموذج طراز طراز الطراز ل ER ، تعريف نقطه الإدخال 2.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. حدد **حفظ**.
18. أغلق صفحة **مصمم تعيين النموذج**.

    ![صفحه تعيينات نموذج ER مع تعريفات نقطه الإدخال.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. أغلق صفحة **تعيينات النماذج**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>إكمال الإصدار المعدل من تكوين تعيين النموذج

1.  في **صفحة التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.

    > قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.

2.  حدد **مكتمل**.
3.  حدد **موافق**.

لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.

### <a name="configure-a-sample-format"></a>تكوين تنسيق نموذج

#### <a name="create-an-er-format-configuration"></a>إنشاء تكوين تنسيق التقارير الإلكترونية

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد **النموذج للتعرف على التعيينات**.
2.  حدد **إنشاء التكوين**.
3.  في مربع الحوار المنسدل، في مجموعة الحقل **جديد**، حدد **التنسيق استنادًا إلى نموذج نموذج البيانات للتعرف على التعيينات**.
4.  في حقل **الاسم**، أدخل **التنسيق للتعرف على التعيينات**.
5.  في حقل **تعريف نموذج البيانات**، حدد **نقطة الإدخال 1**.
6.  حدد **إنشاء التكوين**.

لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير. يحتوي هذا الإصدار على مكون التنسيق.

#### <a name="design-a-sample-format"></a>تصميم تنسيق نموذج

1.  في صفحة **التكوينات**، حدد **المصمم**.
2.  حدد **إضافة جذر**.
3.  في مجموعة **النص**، حدد عنصر **السلسلة**.
4.  حدد **موافق**.

#### <a name="bind-format-elements-to-a-data-source"></a>ربط عناصر التنسيق بمصدر بيانات

1.  في صفحة **مصمم التنسيق**، في علامة التبويب **تعيين**، قم بتوسيع مصدر بيانات النموذج.
2.  حدد حقل **وصف الوظيفة**.
3.  حدد **ربط**.

    ![صفحة مصمم تنسيق‬ التقارير الإلكترونية.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  حدد **حفظ**.
5.  قم بإغلاق الصفحة.

## <a name="appendix-2"></a><a name="appendix2"></a> الملحق 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>تكوين تعيين نموذج عينة للتخصيص العام

قد تحتاج إلى تخصيص تعيين نموذج تم توفيره من قبل موفر التكوين (الشريك)، ثم استخدام الإصدار المخصص كمصدر بيانات لتنسيقات التقارير الإلكترونية. في هذه الحالة، يجب إنشاء تكوين تعيين نموذج تقارير إلكترونية (ER) مخصص لاجراء التغييرات المطلوبة في تعيينات النماذج الموجودة. تستخدم الإجراءات الموجودة في هذا الملحق تعيين نموذج **التعيين (عام)** كمثال.

#### <a name="create-an-er-model-mapping-configuration"></a>إنشاء تكوين تعيين نموذج التقارير الإلكترونية

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين (عام)**.
2.  حدد **إنشاء التكوين**.
3.  في مربع الحوار المنسدل ، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: التعيين (عام)، شركة Litware, Inc.**.
4.  في حقل **الاسم**، أدخل **التعيين المخصص (عام)**.
5.  حدد **إنشاء التكوين**.

لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.

#### <a name="design-a-sample-model-mapping"></a>تصميم تعيين نموذج عينة

1.  في صفحة **التكوينات**، حدد **المصمم**.

    > لاحظ أنه تم نسخ تعيينات النماذج الخاصة بالتكوين الأساسي تلقائيًا إلى هذا التكوين.

2.  حدد تعيين **نسخ التعيين (عام)**.
3.  حدد **المصمم**.
4.  في قسم **نموذج البيانات**، حدد **تحرير**.
5.  في حقل **المعادلة**، أدخل **"الوظيفة العامة المخصصة 1"**.
6.  حدد **حفظ**.
7.  قم بإغلاق الصفحة.

    ![صفحه مصمم تعيين طراز ER ، وهي المعادلة العامة للوظيفة العامة.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  حدد **حفظ**.
9.  قم بإغلاق الصفحة.
10. حدد تعيين **نسخة التعيين (عام) 2**.
11. حدد **المصمم**.
12. في قسم **نموذج البيانات**، حدد **تحرير**.
13. في حقل **المعادلة**، أدخل **"الوظيفة العامة المخصصة 2"**.
14. حدد **حفظ**.
15. قم بإغلاق الصفحة.

    ![صفحه مصمم تعيين طراز ER ، وهي المعادلة العامة للوظيفة العامة.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. حدد **حفظ**.
17. قم بإغلاق الصفحة.

    ![صفحه النموذج ل ER إلى مصدر البيانات صفحه التعيين للتعيين (عام).](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. قم بإغلاق الصفحة.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>إكمال الإصدار المعدل من تكوين تعيين النموذج

1.  في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.

    > قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.

2.  حدد **مكتمل**.
3.  حدد **موافق**.

لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.

## <a name="appendix-3"></a><a name="appendix3"></a> الملحق 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>تكوين تعيين نموذج عينة للتخصيص الخاص بالبلد/المنطقة

بالنسبة لبعض تنسيقات التقارير الإلكترونية، قد تكون هناك متطلبات خاصة بالبلد/المنطقة لإعداد البيانات. في هذه الحالة، يمكنك أداره تكوين تعيين نموذج تقارير إلكترونية وعزل تنفيذ هذه المتطلبات الخاصة بالبلد/المنطقة عن التنفيذ العام. تستخدم الإجراءات الموجودة في هذا الملحق تنسيق التقارير الإلكترونية **التنسيق للتعرف على التعيينات** والمتطلبات الخاصة بالفرنسية كمثال.

#### <a name="create-an-er-model-mapping-configuration"></a>إنشاء تكوين تعيين نموذج التقارير الإلكترونية

أولاً، قم بإنشاء تكوين تعيين نموذج تقارير إلكترونية (ER) جديد لتنفيذ المتطلبات الخاصة بالبلد/المنطقة. استخدم تكوين تعيين نموذج تقارير إلكترونية مخصص كأساس.

1.  في صفحة **التكوينات**، في شجرة التكوينات، حدد **التعيين المخصص (عام)**.
2.  حدد **إنشاء التكوين**.
3.  في مربع الحوار المنسدل، في مجموعه الحقل **جديد**، حدد **الاشتقاق من الاسم: التعيين المخصص (عام)، شركة Litware, Inc**.
4.  في حقل **الاسم**، أدخل **التعيين (FR)**.
5.  حدد **إنشاء التكوين**.

لاحظ أن إصدار المسودة 1 لتكوين التقارير الإلكترونية هذا جاهز للتحرير.

#### <a name="design-a-sample-model-mapping"></a>تصميم تعيين نموذج عينة

1.  في صفحة **التكوينات**، حدد **المصمم**.

    > لاحظ أنه تم نسخ تعيينات النماذج الخاصة بالتكوين الأساسي تلقائيًا إلى هذا التكوين.

2.  حدد تعيين **نسخ نسخة التعيين (عام)**.
3.  أعد تسميتها بـ **التعيين (FR)**.
4.  حدد **المصمم**.
5.  في قسم **نموذج البيانات**، حدد **تحرير**.
6.  في حقل **المعادلة**، أدخل **"وظيفة FR رقم 1"**.
7.  حدد **حفظ**.
8.  قم بإغلاق الصفحة.

    ![صفحه مصمم تعيين طراز ER ، وهي المعادلة 1 لوظيفة FR.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  حدد **حفظ**.
10. قم بإغلاق الصفحة.
11. حدد تعيين **نسخ نسخة التعيين (عام) 2**.
12. أعد تسميتها بـ **التعيين (FR) 2**.
13. حدد **المصمم**.
14. في قسم **نموذج البيانات**، حدد **تحرير**.
15. في حقل **المعادلة**، أدخل **"وظيفة FR رقم 2"**.
16. حدد **حفظ**.
17. قم بإغلاق الصفحة.

    ![صفحه مصمم تعيين طراز ER ، وهي المعادلة 2 لوظيفة FR.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. حدد **حفظ**.
19. قم بإغلاق الصفحة.

    ![صفحة تعيين النموذج ER إلى مصدر البيانات.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. قم بإغلاق الصفحة.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>تحديد قيود سياق البلد/المنطقة للاستخدام

1.  في صفحة **التكوينات**، في علامة التبويب السريع **أكواد البلد/المنطقة ISO**، حدد **جديد**.
2.  في حقل **ISO**، حدد **FR**.
3.  حدد **حفظ**.

لاحظ انه يجب عليك تسجيل الدخول إلى شركه معينه في Finance لتشغيل تنسيق التقارير الإلكترونية. وبالتالي ، يمكن اعتبار هذه الشركة جهة تحكم في تنفيذ تنسيق التقارير الإلكترونية وتحديد تعيين نموذج التقارير الإلكترونية الصحيح لنموذج البيانات الأساسي للتقارير الإلكترونية. عن طريق أضافه كود البلد **FR**، فانك تحدد أن تعيين النموذج هذا متوفر للتحديد بواسطة تنسيق التقارير الإلكترونية الخاص بنموذج البيانات الأساسي فقط عند تشغيل هذا التنسيق ضمن عنصر تحكم شركه لها سياق بلد/منطقه فرنسية.

يمكنك أضافه العديد من أكواد البلد/المنطقة لإصدار واحد من تكوين تعيين نموذج التقارير الإلكترونية (ER). وبهذه الطريقة، يمكن استخدام تعيينات النماذج الموجودة في تكوين تعيين النموذج لتنسيق تقارير إلكترونية يتم تشغيله ضمن التحكم في الشركات التي لها سياق بلد/منطقه مختلف.

لاحظ انه تم تحديد قائمه أكواد البلد/المنطقة لكل إصدار من تكوين تعيين نموذج تقارير إلكترونية ويمكن ان تختلف من إصدار إلى إصدار.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>إكمال الإصدار المعدل من تكوين تعيين النموذج

1.  في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.

    > قم بتغيير حالة تكوين تعيين النموذج المصمم من **مسودة** إلى **مكتمل**، بحيث يمكن استخدامه بواسطة تنسيقات التقارير الإلكترونية.

2.  حدد **مكتمل**.
3.  حدد **موافق**.

لاحظ أن التكوين الذي تم إنشاؤه تم حفظه باعتباره الإصدار المكتمل 1.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[إدارة تعيين نموذج ER (تقارير إلكترونية) في تكوينات ER (تقارير إلكترونية) منفصلة](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[تطبيق سياق البلد/المنطقة](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>لقد قمت بتكوين اثنين من تكوينات تعيين نموذج تقارير إلكترونية مشترك في RCS وتم وضع علامة علي أحدهما كتكوين تعيين للنموذج الافتراضي. لقد قمت بنجاح بتشغيل تنسيق تقارير إلكترونية تم إنشاؤه لنفس التكوين الأساسي لنموذج بيانات التقارير الإلكترونية، لاختبار تعيينات النماذج. ثم قمت بعد ذلك باستيراد حل التقارير الإلكترونية الكامل (نموذج بيانات التقارير الإلكترونية، وتكوينا تعيين نموذج التقارير الإلكترونية، وتكوين تنسيق التقارير الإلكترونية) إلى Finance. لماذا أتلقى رسالة خطا عند محاولة تشغيل نفس تنسيق التقارير الإلكترونية في Finance؟
إعداد تعيين النموذج الافتراضي خاص بالبيئة. تم تكوينه في RCS ولكن لم يتم تصديره إلى Finance. لتشغيل تنسيق التقارير الإلكترونية بنجاح، يجب عليك وضع علامة على أحد تكوينات تعيين نموذج التقارير الإلكترونية كتكوين تعيين النموذج الافتراضي في Finance أيضا.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>لقد قمت بتكوين تعيين نموذج واحد كتعيين نموذج مشترك وأكملت إصدار المسودة له. بعد ذلك قمت باضافه تكوين تعيين نموذج جديد لنفس نموذج البيانات وتكوينه كخاص بالفرنسية. لماذا يتم تحديد تعيين النموذج المشترك عند تشغيل تنسيق التقارير الإلكترونية، حتى إذا كان هذا التنسيق للتقارير الإلكترونية يستخدم تعريف الجذر الصحيح وتم اجراء التنفيذ ضمن التحكم في الشركة التي لها سياق بلد/منطقه فرنسية؟
تأكد من أن تكوين تعيين النموذج المشترك لم يتم وضع علامة عليه علي أنه تكوين تعيين النموذج الافتراضي. والا سيكون له اولويه أعلى أثناء تحديد التعيين. وتأكد أيضا من مراعاه تكوين تعيين النموذج الخاص بالفرنسية عند تحديد تعيين أثناء تنفيذ تنسيق التقارير الإلكترونية. يتوفر تكوين لتعيين نموذج تقارير إلكترونية للتحديد فقط في حاله تحقق أحد الشروط التالية على الأقل:
- إصدار واحد على الأقل من تكوين تعيين نموذج التقارير الإلكترونية بالحالة **مكتمل** أو **مشترك**. في هذه الحالة، سيتم استخدام الإصدار الذي يحتوي على رقم الإصدار الأعلى لتنفيذ تنسيق التقارير الإلكترونية.
- تم تشغيل خيار **تشغيل المسودة** لتكوين تعيين نموذج التقارير الإلكترونية. في هذه الحالة، سيتم استخدام الإصدار الذي له حالة **المسودة** لتنفيذ تنسيق التقارير الإلكترونية.
> يتوفر خيار **تشغيل المسودة** في صفحة **التكوينات** لكل تكوين تعيين نموذج تقارير إلكترونية عند تشغيل معلمة مستخدم التقارير الإلكترونية **تشغيل الإعداد**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
