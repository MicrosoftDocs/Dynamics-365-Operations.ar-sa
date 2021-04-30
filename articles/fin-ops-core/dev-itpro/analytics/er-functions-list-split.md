---
title: SPLIT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLIT (ER).
author: NickSelin
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853433"
---
# <a name="split-er-function"></a>SPLIT ER وظيفة

[!include [banner](../includes/banner.md)]

تقسم الوظيفة `SPLIT` سلسلة الإدخال المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
SPLIT (input, length)
```

يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، لكل منها الطول المحدد.

## <a name="syntax-2"></a>بناء الجملة 2

```vb
SPLIT (input, delimiter)
```

يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، استنادًا إلى المحدد المعين.

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

النص المراد تقسيمه.

`length`: *عدد صحيح*

الحد الأقصى لطول سلسلة فرعية واحدة.

`delimiter`: *السلسلة*

مُحدد يستخدم لفصل السلاسل الفرعية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تتكون بنية سجل القائمة التي تم إرجاعها من حقل **القيمة** من نوع *السلسلة*. يحتوي كل سجل من القائمة التي تم إرجاعها على سلاسل فرعية تم إنشاؤها في هذا الحقل.

إذا كانت وسيطة `delimiter` فارغة، تتكون القائمة الجديدة التي تم إرجاعها من سجل واحد يحتوي على الحقل **القيمة** من نوع *السلسلة*. يحتوي هذا الحقل علي نص الإدخال.

إذا كانت الوسيطة `input` فارغة، يتم إرجاع قائمة فارغة جديدة. إذا لم يتم تعيين الوسيطة `input` أو `delimiter` (null)، يتم طرح استثناء تطبيق.

## <a name="example-1"></a>مثال1

يُرجع التعبير `SPLIT ("abcd", 3)` قائمة جديدة تتكون من سجلين لديهما حقل **القيمة** من نوع *السلسلة*. يحتوي حقل **القيمة** في السجل الأول على النص **"abc"** ، ويحتوي حقل **القيمة** في السجل الثاني على النص **"d"**.

## <a name="example-2"></a>مثال2

يُرجع التعبير `SPLIT ("XAb aBy", "aB")` قائمة جديدة تتكون من ثلاث سجلات لديهم حقل **القيمة** من نوع *السلسلة*. يحتوي حقل **القيمة** في السجل الأول على النص **"X"** ، ويحتوي حقل **القيمة** في السجل الثاني على النص **&nbsp;** ، ويحتوي حقل **القيمة** في السجل الثالث على النص **"y"**. 

## <a name="example-3"></a>المثال الثالث

يمكنك استخدام الدالة [INDEX](er-functions-list-index.md) للوصول إلى العناصر الفردية لإعداد الإدخال المحدد. إذا قمت بإدخال مصدر البيانات **MyList** من النوع **الحقل المحسوب** وقمت بتكوينه للتعبير `SPLIT("abc", 1)`، يرجع التعبير `INDEX(MyList,2).Value` النص **"b"**.

## <a name="example-4"></a>المثال الرابع

يمكنك استخدام الدالة [ENUMERATE](er-functions-list-enumerate.md) لمساعدتك في الوصول إلى العناصر الفردية لإعداد الإدخال المحدد. إذا قمت أولاً بإدخال مصدر البيانات **MyList** للنوع **الحقل المحسوب** وقمت بتكوينه للتعبير `SPLIT("abc", 1)`، ثم أدخلت مصدر البيانات **EnumeratedList** للنوع **الحقل المحسوب** وقمت بتكوينه للتعبير `ENUMERATE(MyList)`، يرجع التعبير `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` النص **"b"**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
