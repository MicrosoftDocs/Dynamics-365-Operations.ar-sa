---
title: VALUEIN ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية VALUEIN‏ (ER).
author: kfend
ms.date: 12/14/2021
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
ms.openlocfilehash: 14c3d08ee3478b55593a3e473f9eb60f1bba0760
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288127"
---
# <a name="valuein-er-function"></a>VALUEIN ER وظيفة

[!include [banner](../includes/banner.md)]

تُحدد الوظيفة `VALUEIN` ما إذا كان الإدخال المُحدد يطابق أي قيمة عنصر مُحدد في القائمة المُحددة. يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.

## <a name="syntax"></a>بناء الجملة

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>الوسائط

`input`: *الحقل*

مسار صالح لعنصر مصدر بيانات من نوع *قائمة السجلات*. وستتم مطابقة قيمة هذا الصنف.

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`list item expression`: *منطقي*

تعبير شرطي صالح يشير إما إلى أو يحتوي على حقل واحد من القائمة المحددة يجب استخدامه للمطابقة.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

بشكل عام، يتم تحويل الوظيفة `VALUEIN` إلى مجموعة من شروط **OR**. إذا كانت قائمة شروط **OR** كبيرة وقد يتم تجاوز الحد الأقصى لطول عبارة SQL، فعليك استخدام الوظيفة [`VALUEINLARGE`](er-functions-logical-valueinlarge.md).

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

في بعض الحالات، يُمكن تحويله إلى عبارة SQL لقاعدة بيانات باستخدام عامل التشغيل `EXISTS JOIN`.

> [!NOTE]
> القيمة التي تُرجعها وظيفة `VALUEIN` يتم [استخدامها بشكل مختلف](er-functions-list-filter.md#usage-notes)، اعتمادًا على ما إذا كانت هذه الوظيفة تُستخدم لتحديد معايير التحديد لوظيفة [`FILTER`](er-functions-list-filter.md) أو وظيفة [`WHERE`](er-functions-list-where.md).

## <a name="example-1"></a>مثال1

في تعيين النموذج الخاص بك، يجب عليك تحديد مصدر البيانات **القائمة** من النوع *الحقل المحسوب*. يحتوي مصدر البيانات هذا على التعبير `SPLIT ("a,b,c", ",")`.

عندما يتم استدعاء مصدر بيانات، إذا تم تكوينه كتعبير `VALUEIN ("B", List, List.Value)`، يُرجع **TRUE**. في هذه الحالة، يتم تحويل الوظيفة `VALUEIN` إلى مجموعة الشروط التالية: `(("B" = "a") or ("B" = "b") or ("B" = "c"))` ، حيث تساوي `("B" = "b")` **TRUE**.

عندما يتم استدعاء مصدر بيانات، إذا تم تكوينه كتعبير `VALUEIN ("B", List, LEFT(List.Value, 0))`، يُرجع **FALSE**. في هذه الحالة، تتم ترجمة الوظيفة `VALUEIN` إلى الشرط التالي: `("B" = "")`، والذي لا يساوي **TRUE**.

الحد الأقصى لعدد الأحرف في نص شرط هو 32768 حرفًا. لذلك، يجب عدم إنشاء مصادر بيانات قد تتجاوز هذا الحد في وقت التشغيل. إذا تم تجاوز الحد المسموح به، يتوقف تشغيل التطبيق، ويتم طرح استثناء. على سبيل المثال، قد تحدث هذه الحالة إذا تم تكوين مصدر البيانات على الشكل `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ، وتحتوي القائمتين **List1** و **List2** على عدد ضخم من السجلات.

في بعض الحالات، تُترجم الوظيفة `VALUEIN` إلى بيان قاعدة بيانات باستخدام عامل التشغيل `EXISTS JOIN`. يحدث هذا السلوك عند استخدام الدالة [`FILTER`](er-functions-list-filter.md) وتلبية الشروط التالية:

- يكون الخيار **طلب استعلام**‬ متوقفًا عن التشغيل لمصدر بيانات الوظيفة `VALUEIN` التي تشير إلى قائمة السجلات. لم يتم تطبيق أية شروط إضافية لمصدر البيانات هذا في وقت التشغيل.
- لا يتم تكوين تعبيرات متداخلة لمصدر بيانات وظيفة `VALUEIN` التي تشير إلى قائمة السجلات.
- يُشير عنصر قائمة الوظيفة `VALUEIN` إلى حقل مصدر بيانات مُحدد، وليس إلى تعبير أو أسلوب لمصدر البيانات هذا.

يمكنك استخدام هذا الخيار بدلاً من الوظيفة [`WHERE`](er-functions-list-where.md) الموضحة سابقًا في هذا المثال.

## <a name="example-2"></a>مثال2

أنت تحدد مصادر البيانات التالية في تعيين نموذج:

- مصدر البيانات **In** من النوع *سجلات الجدول*. يشير مصدر البيانات هذا إلى جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. 
- مصدر البيانات **المنفذ** من النوع *سجلات الجدول*. يشير مصدر البيانات هذا إلى جدول IntrastatPort. 

عند استدعاء مصدر بيانات تم تكوينه على أنه التعبير `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` ، يتم إنشاء عبارة SQL التالية لإرجاع السجلات التي تمت تصفيتها في جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

بالنسبة إلى حقول **dataAreaId**، يتم إنشاء عبارة SQL النهائية باستخدام عامل التشغيل `IN`.

## <a name="example-3"></a>المثال الثالث

أنت تحدد مصادر البيانات التالية في تعيين نموذج:

- مصدر البيانات **Le** من النوع *الحقل المحسوب*. يحتوي مصدر البيانات هذا على التعبير `SPLIT ("DEMF,GBSI,USMF", ",")`.
- مصدر البيانات **In** من النوع *سجلات الجدول*. يشير مصدر البيانات هذا إلى جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي ، ويتم تشغيل الخيار **عبر الشركة** لذلك.

عند استدعاء مصدر بيانات تم تكوينه على أنه التعبير `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` ، تحتوي عبارة SQL النهائية على الشرط التالي:

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)

[وظائف VALUEINLARGE](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
