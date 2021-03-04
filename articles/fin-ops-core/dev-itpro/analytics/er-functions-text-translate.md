---
title: وظيفة TRANSLATE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TRANSLATE (ER).
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c5d192b8679d6df2c44a0038fe4ffc181a6a54df
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685293"
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