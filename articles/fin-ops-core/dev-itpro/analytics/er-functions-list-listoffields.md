---
title: LISTOFFIELDS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LISTOFFIELDS (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8d9f41d6ee5256f560c83486c95ecd47f5b081
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686502"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `LISTOFFIELDS` قيمة *قائمة السجل* التي تم إنشاؤها بناءً على بنية الوسيطة المُحددة للنوع *التعداد* أو *الحاوية (السجل)*.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>الوسائط

`path`: مرجع مصدر البيانات

مسار مرجع صالح لمصدر بيانات أحد أنواع البيانات التالية:

- تعداد النموذج
- تعداد التنسيق
- تعدادات التطبيق
- حاوية (سجل)

`language`: *السلسلة*

النص الذي يمثل رمز لغة.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تتكون القائمة التي تم إنشاؤها من السجلات التي تحتوي على الحقول التالية:

- **الاسم** (نوع بيانات *السلسلة* )
- **التسمية** (نوع بيانات *السلسلة* )
- **الوصف** (نوع بيانات *السلسلة* )
- **IsTranslated** (نوع البيانات *منطقي* )

إذا كانت الوسيطة `path` تشير إلى مصدر بيانات من النوع *الحاوية (سجل)* ، لكل حقل من سجل الحاوية المشار إليه، تتم إضافة سجل جديد إلى القائمة التي تم إنشاؤها. بالنسبة لكل سجل يتم إنشاؤه، يُرجع حقل **الاسم** اسم حقل سجل الحاوية المشار إليه الذي تم إنشاء السجل الحالي له.

إذا كانت الوسيطة `path` تشير إلى مصدر بيانات واحد من أنواع  *التعداد*، لكل قيمة تعداد من التعداد المشار إليه، تتم إضافة سجل جديد إلى القائمة التي تم إنشاؤها. بالنسبة لكل سجل تم إنشاؤه، يُرجع حقل **الاسم** قيمة التعداد المشار إليه الذي تم إنشاء السجل الحالي له، ويرجع حقل **الوصف** وصف التعداد، ويُرجع حقل **التسمية** تسمية هذا التعداد.

في وقت التشغيل، عند استخدام بناء الجملة 1، يجب أن تُرجع الحقول **التسمية** و **الوصف** القيم التي تستند إلى إعدادات اللغة الخاصة بتنسيق التقارير الإلكترونية (ER) قيد التشغيل.

- إذا كانت التسميات والأوصاف الخاصة باللغة المطلوبة متوفرة، تُرجع الحقول **التسمية** و **الوصف** القيم التي تستند إلى تلك اللغة، ويُرجع حقل **IsTranslated** **True**.
- إذا لم تكن التسميات والأوصاف للغة المطلوبة متاحة، تُرجع حقول **التسمية** و **الوصف** القيم التي تستند إلى لغة **EN-US** الافتراضية، ويُرجع الحقل **IsTranslated** **False**.

في وقت التشغيل، عند استخدام بناء الجملة 2، يجب أن تُرجع الحقول **التسمية** و **الوصف** القيم التي تستند إلى اللغة المُحددة كوسيطة ثانية للوظيفة التي تم استدعاءها.

- إذا كانت التسميات والأوصاف الخاصة باللغة المطلوبة متوفرة، تُرجع الحقول **التسمية** و **الوصف** القيم التي تستند إلى تلك اللغة، ويُرجع حقل **IsTranslated** **True**.
- إذا لم تكن التسميات والأوصاف للغة المطلوبة متاحة، تُرجع حقول **التسمية** و **الوصف** القيم التي تستند إلى لغة **EN-US** ، ويُرجع الحقل **IsTranslated** **False**.

## <a name="example-1"></a>مثال1

في الرسم التوضيحي التالي، يتم تقديم تعداد في نموذج بيانات التقارير الإلكترونية (ER).

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

يبين الرسم التوضيحي التالي هذه التفاصيل:

- يتم إدراج تعداد النموذج في تقرير كمصدر بيانات.
- يستخدم تعبير التقارير الإلكترونية تعداد النموذج كمعلمة لوظيفة `LISTOFFIELDS`.
- يتم إدراج مصدر بيانات نوع *قائمة السجلات* في تقرير باستخدام تعبير التقارير الإلكترونية الذي تم إنشاؤه.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

يوضح المثال التالي عناصر تنسيق التقارير الإلكترونية المرتبطة بمصدر البيانات من نوع *قائمة السجلات* الذي تم إنشاؤها باستخدام وظيفة `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> تتم تعبئة النص المترجم للتسميات والأوصاف في إخراج تنسيق التقارير الإلكترونية وفقًا لإعدادات اللغة التي تم تكوينها لعناصر تنسيق **الملف** و **المجلد** الأصلي.

## <a name="example-2"></a>مثال2

سوف تستخدم نوع مصدر البيانات *الحقل المحسوب* لتكوين مصادر البيانات **enumType\_de** و **enumType\_ deCH** لتعداد نموذج بيانات **enumType**: 

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

في هذه الحالة، يمكنك استخدام التعبير التالي للحصول على تسمية لقيمة التعداد بالألمانية السويسرية، في حالة توفر الترجمة. إذا لم تتوفر ترجمة اللغة الألمانية (سويسرا)، فستكون التسمية باللغة الألمانية.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
