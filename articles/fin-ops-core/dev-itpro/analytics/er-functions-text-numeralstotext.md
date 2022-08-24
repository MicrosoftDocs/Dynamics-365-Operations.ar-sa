---
title: NUMERALSTOTEXT ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMERALSTOTEXT‏ (ER).
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287977"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم وظيفة `NUMERALSTOTEXT` بإرجاع الرقم المحدد كقيمة *سلسلة* بعد كتابته (أي، تحويله إلى سلاسل نصية) باللغة المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد صحيح* أو *حقيقي*

قيمة رقمية تُحدد الرقم الذي يجب كتابته.

`language`: *السلسلة*

قيمة *سلسلة* تمثل كود اللغة.

`currency`: *السلسلة*

قيمة *سلسلة* تمثل كود العملة.

`print currency name flag`: *منطقي*

قيمة *منطقية* تُشير إلى ما إذا كان يجب إضافة اسم عملة إلى النص المكتوب.

`decimal points`: *عدد صحيح*

قيمة *عدد صحيح* تُشير إلى عدد المنازل العشرية التي يجب أن تكون موجود في النص المكتوب.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

كود اللغة اختياري. إذا حُدد كسلسلة فارغة، يتم استخدام كود اللغة الخاص بسياق التشغيل بدلاً من ذلك. كود اللغة الافتراضية هو **EN-US**. يتم تعريف كود اللغة الخاص بسياق التشغيل في عنصر **مجلد** أو **ملف** من تنسيق إعداد التقارير الإلكترونية (ER) قيد التشغيل.

كود العملة اختياري. إذا حُدد كسلسلة فارغة، يتم استخدام عملة الشركة الخاصة للسياق قيد التشغيل.

> [!NOTE] 
> يتم تحليل الوسيطات `print currency name flag` و `decimal points` فقط لأكواد اللغات التالية: **CS** و **ET** و **HU** و **LT** و **LV** و **PL** و **RU**. بالإضافة إلى ذلك، يتم تحليل وسيطة `print currency name flag` فقط للشركات التي يدعم فيها سياق البلد أو المنطقة صرف أسماء العملات.

## <a name="example-1"></a>مثال1

تُرجع `NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` **"‬‏‫ألف ومئتين وأربعة وثلاثون و 56"**. 

## <a name="example-2"></a>مثال2

تُرجع `NUMERALSTOTEXT (120, "PL", "", false, 0)` **"Sto dwadzieścia"**.  

## <a name="example-3"></a>المثال الثالث

تُرجع وظيفة `NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` **"Сто двадцать евро 21 евроцент"**. 

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
