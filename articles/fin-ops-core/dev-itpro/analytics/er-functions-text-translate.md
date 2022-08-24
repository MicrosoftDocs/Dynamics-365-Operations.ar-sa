---
title: وظيفة TRANSLATE ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية TRANSLATE‏ (ER).
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278430"
---
# <a name="translate-er-function"></a>وظيفة TRANSLATE ER

[!include [banner](../includes/banner.md)]

تقوم الدالة `TRANSLATE` بإرجاع قيمة *سلسلة* تحتوي على نتيجة استبدال النص المحدد بأحرف بمجموعة أحرف أخرى متوفرة.

## <a name="syntax"></a>بناء الجملة

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

المسار الصالح لمصدر البيانات من نوع *السلسلة*.

`pattern`: *السلسلة*

النص الذي يجب استبداله.

`replacement`: *السلسلة*

النص الذي سيتم استخدامه كبديل.

## <a name="return-values"></a>إرجاع القيم

*سلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تقوم الدالة `TRANSLATE` باستبدال كل حرف على حدة. تقوم الدالة باستبدال الحرف الأول للوسيطة `text` بالحرف الأول من الوسيطة `pattern` ثم الحرف الثاني وتتبع سير العمل نفسه حتى الانتهاء. عندما يتطابق حرف من الوسيطتين `text` و`pattern`، يتم استبداله بحرف من الوسيطة `replacement` الموجودة في الموضع نفسه للحرف من الوسيطة `pattern`. إذا ظهر أحد الأحرف عدة مرات في الوسيطة `pattern`، فسيتم استخدام تعيين الوسيطة `replacement` الذي يتطابق مع الحدوث الأول لهذا الحرف.

## <a name="example-1"></a>مثال1

تقوم الدالة `TRANSLATE ("abcdef", "cd", "GH")` باستبدال الحرف **"c"** للنص **“abcdef”** المحدد بالحرف **"G"** للنص `replacement` للأسباب التالية:
-   تم تقديم الحرف **"c"** في النص `pattern` في الموضع الأول.
-   يحتوي الموضع الأول للنص `replacement` على الحرف **"G"**.

## <a name="example-2"></a>مثال2

تقوم الدالة `TRANSLATE ("abcdef", "ccd", "GH")` بإرجاع **"abGdef"**.

## <a name="example-3"></a>المثال الثالث

يُرجع التعبير `TRANSLATE ("abccba", "abc", "123")` **"123321"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
