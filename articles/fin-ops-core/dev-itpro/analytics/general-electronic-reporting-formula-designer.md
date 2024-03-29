---
title: مصمم المعادلات في التقارير الإلكترونية
description: توفر هذه المقالة معلومات عن كيفية استخدام مصمم التركيبة في إعداد التقارير الإلكترونية (ER).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 283c882300ece460c18ffebe572238e7629f8dee
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476791"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>مصمم المعادلات في التقارير الإلكترونية

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية استخدام مصمم المعادلة في التقارير الإلكترونية (ER). عندما تصمم تنسيقًا لمستند إلكتروني معين في التقارير الإلكترونية، يمكنك استخدام معادلات لتحويل البيانات لتلبية متطلبات تنفيذ وتنسيق هذا المستند. هذه المعادلات تشبه المعادلات في Microsoft Excel. هناك أنواع مختلفة من الدالات المعتمدة في المعادلات: النص والتاريخ والوقت ومنطق الرياضيات والمعلومات ووظائف تحويل أنواع البيانات وغير ذلك أيضًا من الدالات الخاصة بمجال الأعمال.

## <a name="formula-designer-overview"></a>نظرة عامة على مصمم المعادلة

تدعم التقارير الإلكترونية مصمم المعادلة. لذلك، في وقت التصميم، يمكنك تكوين التعبيرات التي يمكن استخدامها للمهام التالية في وقت التشغيل:

- تحويل البيانات التي يتم استلامها من قاعدة بيانات تطبيق والتي يجب إدخالها في نموذج بيانات تقارير إلكترونية تم تصميمه ليكون مصدر بيانات لتنسيقات التقارير الإلكترونية. (على سبيل المثال، هذه التحويلات قد تتضمن تحويل نوع البيانات والتصفية والتجميع.)
- بيانات التنسيق التي يجب إرسالها إلى مستند إلكتروني أصلي وفقًا لمخطط وشروط تنسيق تقارير إلكترونية محدد. (على سبيل المثال، التنسيق الذي قد يتم وفقًا للغة أو الثقافة المطلوبة أو الترميز).
- التحكم في عملية إنشاء المستندات الإلكترونية. (على سبيل المثال، يمكن للتعبيرات تمكين أو تعطيل إخراج عناصر معينة للتنسيق، استنادًا إلى معالجة البيانات. كما يمكنها إيقاف عملية إنشاء المستند أو طرح رسائل إلى المستخدمين.)

يمكنك فتح صفحة **مصمم المعادلة‬‏‫** عندما تنفذ أي إجراء من الإجراءات التالية:

- ربط عناصر مصدر البيانات بمكونات نموذج البيانات.
- ربط عناصر مصدر البيانات بمكونات التنسيق.
- إكمال صيانة الحقول المحتسبة كجزء من مصادر البيانات.
- تعريف شروط إمكانية الرؤية وقابلية التحرير‬ لمعلمات إدخال المستخدم‬.
- تعريف القيم الافتراضية‬ لمعلمات إدخال المستخدم‬.
- تصميم عمليات تحويل التنسيق.
- تعريف شروط التمكين لمكونات التنسيق.
- تعريف أسماء الملفات لمكونات ملف التنسيق.
- تعريف الشروط لعمليات التحقق من مراقبة العملية.
- تعريف الرسالة النصية لعمليات التحقق من مراقبة العملية.

## <a name="data-binding"></a><a name="Binding"></a>ربط البيانات

يمكن استخدام مصمم معادلة التقارير الإلكترونية لتعريف تعبير يقوم بتحويل البيانات التي يتم تلقيها من مصادر البيانات، بحيث يمكن إدخال البيانات في مستهلك البيانات بالطرق التالية في وقت التشغيل:

- من مصادر بيانات التطبيق ومعلمات وقت التشغيل إلى نموذج بيانات التقارير الإلكترونية
- من نموذج بيانات التقارير الإلكترونية إلى تنسيق التقارير الإلكترونية
- من مصادر بيانات التطبيق ومعلمات وقت التشغيل إلى تنسيق تقارير إلكترونية

يبين الرسم التوضيحي التالي تصميم تعبير من هذا النوع. في هذا المثال، يقوم التعبير بتقريب قيمة الحقل **Intrastat.AmountMST** في جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬‏‫ إلى منزلتين عشريتين، ثم يقوم بإرجاع القيمة المقربة.

[![تعبير ربط البيانات.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

يبين الرسم التوضيحي التالي كيف يمكن استخدام تعبير من هذا النوع. في هذا المثال، يتم إدخال نتيجة التعبير المُصمم في المكون **Transaction.InvoicedAmount** لنموذج بيانات **نموذج الإبلاغ الضريبي**.

[![تعبير ربط البيانات قيد الاستخدام.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

في وقت التشغيل، تُقرب الصيغة المٌصممة، `ROUND (Intrastat.AmountMST, 2)`، قيمة حقل **AmountMST** لكل سجل في جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي إلى منزلتين عشريتين. ثم تقوم بإدخال القيمة المقربة في مكون **Transaction.InvoicedAmount** لنموذج بيانات **تقارير الضرائب**.

## <a name="data-formatting"></a><a name="Transformation"></a>تنسيق البيانات

يمكن استخدام مصمم معادلة التقارير الإلكترونية لتعريف تعبير يقوم بتنسيق البيانات التي يتم تلقيها من مصادر البيانات، بحيث يمكن إرسال البيانات كجزء من المستند الإلكتروني الناشئ. قد يكون لديك التنسيق الذي يجب تطبيقه كقاعدة نموذجية يجب إعادة استخدامها لتنسيق. في هذه الحالة، يمكنك تقديم هذا التنسيق مرة واحدة في تكوين التنسيق، كتحويل مسمى يحتوي على تعبير تنسيق. عندئذٍ، يمكن ربط هذا التحويل المسمى بالعديد من مكونات التنسيق التي يجب تنسيق إخراجها وفقًا لتعبير التنسيق الذي أنشأته.

يبين الرسم التوضيحي التالي تصميم تحويل من هذا النوع. في هذا المثال، يقتطع تحويل **TrimmedString** البيانات الواردة من نوع بيانات *السلسلة* عن طريق إزالة المسافات البادئة والزائدة. تم تقوم بإرجاع قيمة السلسلة المقتطعة.

[![التحويل.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

يبين الرسم التوضيحي التالي كيف يمكن استخدام عملية تحويل من هذا النوع. في هذا المثال، يقوم العديد من مكونات التنسيق بإرسال نص كإخراج إلى المستند الإلكتروني الناشئ في وقت التشغيل. تشير جميع مكونات التنسيق هذه إلى تحويل **TrimmedString** حسب الاسم.

[![التحويل قيد الاستخدام.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

عندما تشير مكونات التنسيق، مثل مكون **partyName** في الرسم التوضيحي السابق، إلى تحويل **TrimmedString**، يرسل التحويل نصًا كإخراج إلى المستند الإلكتروني الناشئ. لا يتضمن هذا النص مسافات بادئة وزائدة.

إذا كان لديك تنسيق يجب أن يُطبق بشكل فردي، فيمكنك إدخال ذلك التنسيق كتعبير فردي لربط خاص بمكون تنسيق محدد. يبين الرسم التوضيحي التالي تعبيرًا من هذا النوع. في هذا المثال، يرتبط مكون التنسيق **partyType** بمصدر البيانات عبر تعبير يقوم بتحويل البيانات الواردة من الحقل **Model.Company.RegistrationType** في مصدر البيانات إلى نص بأحرف كبيرة. يرسل التعبير بعد ذلك هذا النص كإخراج إلى المستند الإلكتروني.

[![تطبيق التنسيق على مكون واحد.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>التحكم في تدفق العملية

يمكن استخدام مصمم معادلة التقارير الإلكترونية‬ لتحديد التعبيرات التي تتحكم في تدفق العملية للمستندات الإلكترونية الناشئة. يمكنك القيام بالمهام التالية:

- تعريف الظروف التي تحدد متى يجب إيقاف عملية إنشاء المستند.
- تحديد التعبيرات التي تنشئ رسائل للمستخدم فيما يتعلق بالعملية المتوقفة أو تطرح رسائل سجل تنفيذ فيما يتعلق بالعملية المستمرة لإنشاء التقارير.
- تحديد أسماء ملفات للمستندات الإلكترونية الناشئة والتحكم في ظروف إنشائها.

يتم تصميم كل قاعدة للتحكم في تدفق العملية كعملية تحقق من الصحة واحدة. يبين الرسم التوضيحي التالي عملية تحقق من هذا النوع. فيما يلي شرح للتكوين في هذا المثال:

- يتم تقييم عملية التحقق من الصحة عند إنشاء عقدة **INSTAT** أثناء إنشاء ملف XML.
- إذا كانت قائمة الحركات فارغة، فستوقف عملية التحقق من الصحة العملية وترجع **FALSE**.
- ترجع عملية التحقق من الصحة رسالة خطأ تتضمن نص التسمية SYS70894 باللغة المفضلة للمستخدم.

[![التحقق من الصحة.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

يمكن أيضًا استخدام مصمم معادلة التقارير الإلكترونية لإنشاء اسم ملف للمستند الإلكتروني الناشئ وللتحكم في عملية إنشاء الملف. يبين الرسم التوضيحي التالي تصميم التحكم بانسياب العملية‬ من هذا النوع. فيما يلي شرح للتكوين في هذا المثال:

- يتم تقسيم قائمة بسجلات من مصدر بيانات **model.Intrastat** إلى دُفعات. تحتوي كل دُفعة على ما يصل إلى 1000 سجل.
- ينشئ الإخراج ملف zip يحتوي على ملف واحد بتنسيق XML لكل دُفعة تم إنشاؤها.
- يُرجع التعبير اسم ملف للمستندات الإلكترونية الناشئة عن طريق وصل اسم الملف وملحقه. للدُفعة الثانية وكافة الدُفعات اللاحقة، يحتوي اسم الملف على معرف دُفعة كلاحقة.
- يمكّن التعبير (من خلال إرجاع **TRUE**) عملية إنشاء ملف للدُفعات التي تحتوي على سجل واحد على الأقل.

[![التحكم في تدفق العملية.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>التحكم بمحتوى المستند

يمكن استخدام مصمم معادلة التقارير الإلكترونية لتكوين التعبيرات التي تتحكم في البيانات التي سيتم وضعها داخل المستندات الإلكترونية التي تم إنشاؤها في وقت التشغيل. بإمكان هذه للتعبيرات تمكين أو تعطيل إخراج عناصر معينة للتنسيق، وهذا يتوقف على معالجة البيانات والمنطق المكوّن. يمكن إدخال هذه التعبيرات لعنصر تنسيق واحد في الحقل **مُمكّن** على علامة تبويب **التعيين** في صفحة **مصمم العمليات**. يُمكنك إدخال التعبيرات كشرط منطقي يقوم بإرجاع قيمة *منطقية*:

- إذا قام الشرط بإرجاع القيمة **صحيح**، يتم تشغيل عنصر التنسيق الحالي.
- إذا قام الشرط بإرجاع القيمة **خطأ**، يتم تخطي عنصر التنسيق الحالي.

يبين الرسم التوضيحي التالي تعبيرات من هذا النوع. (يتم استخدام الإصدار 11.12.11 من تكوين تنسيق **تحويل ائتمان ISO20022 (النرويج)** الذي توفره Microsoft كمثال). يتم تكوين مكون تنسيق **XMLHeader** لوصف بنية رسالة تحويل الائتمان إلى معايير رسالة ISO 20022 XML. تم تكوين مكون التنسيق **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** لإضافة عنصر XML **Ustrd** إلى الرسالة المنشأة ولوضع معلومات الحوالة في تنسيق غير منظم كنص لعناصر XML التالية:

- يتم استخدام‏‎ المكون **PaymentNotes‎** لإنشاء نص ملاحظات الدفع.
- يقوم المكون **DelimitedSequence‎** بإنشاء أرقام الفاتورة المفصولة بفواصل المستخدمة لتسويه التحويل الائتماني الحالي.

[![مكونات PaymentNotes وDelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> تتم تسمية المكونين **PaymentNotes** و **DelimitedSequence** باستخدام علامة استفهام. تشير علامة الاستفهام إلى أن استخدام أحد المكونات شرطي. في هذه الحالة، يستند استخدام المكونات على المعايير التالية:
>
> - يُمكن تعبير `@.PaymentsNotes <> ""` المُعرف لمكون **PaymentNotes** (من خلال إرجاع **True**) تعبئة عنصر XML **Ustrd** بنص ملاحظات الدفع، عندما لا يكون هذا النص فارغًا للتحويل الائتماني الحالي.
>
>    [![تعبير لمكون PaymentNotes.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - يُمكن التعبير `@.PaymentsNotes = ""` المُعرف لمكون **DelimitedSequence** (عن طريق إرجاع **TRUE**) تعبئة عنصر XML **Ustrd** بقائمة مفصولة بفاصلة من أرقام الفواتير المستخدمة لتسوية التحويل الائتماني الحالي، إذا كان نص ملاحظات الدفع لهذا التحويل الائتماني فارغًا.
>
>    [![تعبير لمكون DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> استنادًا إلى هذا الإعداد، ستتضمن الرسالة المنشأة لكل دفعة دائن، عنصر **Ustrd** XML، إما نص ملاحظات الدفع أو، عندما يكون هذا النص فارغًا، قائمة أرقام فواتير مفصولة بفاصلة يتم استخدامها لتسوية هذه الدفعة.

## <a name="assistance-in-formulas-writing"></a>المساعدة في كتابه الصيغ

### <a name="data-sources-navigator"></a>ملاح مصادر البيانات

يمكنك تحرير صيغه تمثل عنصرا في مصدر بيانات مهيكل. عندما تقوم بتكوين معلمات ER الخاصة بك لتقديم المسار إلى عنصر [من مصادر البيانات المهيكلة كمسار](relative-path-data-bindings-er-models-format.md) نسبي ، يتم [عرض](er-formula-language.md#relative-path) علامة الجمع "at" في الصيغة بدلا من الجزء المتبقي من المسار المطلق لبنيه الشجرة الهرمية المستخدمة. ويتم الاشاره إلى الجزء المتبقي من المسار المطلق مع العنصر الأصل لواحد القابل للتحرير. في إصدار 10.0.30 المالية والإصدارات **اللاحقة** ، في الصفحة "مصمم **الصيغة** " ، في جزء مصادر **البيانات** ، يمكنك تحديد الخيار الانتقال **إلى @** لوضع راس المؤشر علي شجره مصادر البيانات إلى عنصر يكون أصلا لأخر قابل للتحرير. سيتم تلقائيا إنشاء بنيه كافة العناصر التي تم طيها تصاعديا ويتم توسيعها بشكل متكرر عند الطلب. يمكن ان يساعدك هذا التوسع في تمثيل العنصر الأساسي لعنصر قابل للتحرير بسرعة ، ومشاهده الأمور التابعة للعنصر القابل للتحرير في شجره مصادر البيانات ، واستخدام كل منها في الصيغة القابلة للتحرير إذا لزم الأمر.

![استخدم خيار "الانتقال إلى @" لوضع راس المؤشر علي شجره مصادر البيانات إلى عنصر يكون أصلا لواحد القابل للتحرير في الصفحة "مصمم الصيغة".](./media/er_formula-designer-data-sources-navigator.gif)

### <a name="data-sources-picker"></a>منتقي مصادر البيانات

في الصفحة **"مصمم** الصيغة" ، في **جزء مصادر** البيانات علي اليمين ، حدد عنصرا في مصدر البيانات الذي تريد إحضاره إلى الصيغة القابلة للتحرير. حدد **إضافة مصدر البيانات**. لاحظ انه تمت أضافه العنصر المحدد إلى نص الصيغة القابلة للتحرير.

> [!TIP]
> عند استخدام **خيار أضافه مصدر** بيانات في محرر الصيغة الافتراضي ، يتم دائما أضافه العنصر المحدد إلى نهاية نص الصيغة. عند القيام بنفس الاجراء في محرر [الصيغ المتقدم](er-advanced-formula-editor.md) ، يتم ادراج العنصر المحدد إلى نص الصيغة عند الموضع الحالي للمؤشر.

### <a name="built-in-functions-picker"></a>المدمج في منتقي الوظائف

في **مصمم المعادلات** الصفحة في **المهام** في الجزء الأيمن ، حدد وظيفة مضمنة في إعداد التقارير الإلكترونية تريد إحضارها إلى الصيغة القابلة للتحرير. ثم حدد **أضف وظيفة**. لاحظ أن الوظيفة المحددة تضاف إلى نص الصيغة القابلة للتحرير.

> [!TIP]
> أضف وظيفة **أضف وظيفة** بيانات في محرر الصيغة الافتراضي ، يتم دائما أضافه العنصر المحدد إلى نهاية نص الصيغة. عند القيام بنفس الاجراء في محرر [الصيغ المتقدم](er-advanced-formula-editor.md) ، يتم ادراج العنصر المحدد إلى نص الصيغة عند الموضع الحالي للمؤشر.

### <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>التحقق من صحة المعادلات المكونة

في صفحة **مصمم التركيبة** ، حدد **اختبار** للتحقق من كيفية عمل التركيبة المُكونة.

[![تحديد اختبار للتحقق من صحة معادلة.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

عندما تكون قيم وسيطات التركيبة مطلوبة، يُمكنك فتح مربع حوار **تعبير اختبار** من صفحة **مصمم التركيبة**. في معظم الحالات، يجب تعريف هذه الوسيطات يدويًا، لأنه لا يتم تشغيل الروابط المُكونة في وقت التصميم. تظهر علامة التبويب **نتيجة الاختبار** في صفحة **مصمم التركيبة** النتيجة من تنفيذ التركيبة المُكونة.

يوضح المثال التالي كيف يُمكنك اختبار التركيبة المكونة لمجال التجارة الخارجية للتأكد من احتواء ‏‫أكواد سلع نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬ على أرقام فقط.

عند اختبار هذه التركيبة، يُمكنك استخدام مربع الحوار **تعبير نص** لتحديد قيمة ‏‫رمز سلع نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬ للاختبار.

[![تحديد ‏‫أكواد سلع نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬ للاختبار.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

بعد تحديد ‏‫أكواد سلع نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬، ثم تحديد **موافق**، تُظهر علامة التبويب **نتيجة الاختبار** الموجودة في صفحة **مصمم التركيبة** نتيجة تنفيذ التركيبة المكونة. يمكنك بعد ذلك تقييم ما إذا كانت النتيجة مقبولة أم لا. إذا كانت النتيجة غير مقبولة، يُمكنك تحديث التركيبة واختبارها مرة أخرى.

[![نتيجة الاختبار.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

لا يُمكن اختبار بعض التركيبات في وقت التصميم. على سبيل المثال، قد تُرجع تركيبة نتيجة نوع بيانات لا يُمكن إظهارها في علامة التبويب **نتيجة الاختبار**. في هذه الحالة، سوف تتلقي رسالة خطأ تنص على أنه لا يُمكن اختبار التركيبة.

[![رسالة خطأ.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)
- [لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
