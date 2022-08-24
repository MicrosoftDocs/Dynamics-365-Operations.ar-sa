---
title: وظيفة DATEVALUE ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEVALUE‏ (ER).
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268687"
---
# <a name="datevalue-er-function"></a>وظيفة DATEVALUE ER

[!include [banner](../includes/banner.md)]

تُرجع الدالة `DATEVALUE` قيمة *[تاريخ](er-formula-supported-data-types-primitive.md#date)* تم تحويلها من قيمة نصية معينة في التنسيق المحدد وفي [ثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) مُحددة بشكل اختياري إلى قيمة تاريخ. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>الوسائط

`text`: *[سلسلة](er-formula-supported-data-types-primitive.md#string)*

النص الذي يمثل القيمة المراد تنسيقها.

`format`: *السلسلة*

تنسيق النص المُعين. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *السلسلة*

الثقافة المستخدمة لتنسيق النص المُحدد. للحصول علي معلومات حول الثقافات المعتمدة، راجع [الثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>إرجاع القيم

*التاريخ*

قيمة التاريخ الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء. على سبيل المثال، إذا تم استدعاء الوظيفة `DATEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية. قيمة `culture` الافتراضية هي **EN-US**.

## <a name="example-1"></a>مثال1

يُرجع التعبير `DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` قيمة التاريخ **21 ديسمبر 2016**، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.

## <a name="example-2"></a>مثال2

يُرجع التعبير `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` قيمة التاريخ **21 يناير 2016** ، استنادًا إلى التنسيق المخصص المُحدد والثقافة.

ولكن، سوف يطرح `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` استثناءً لإبلاغ المستخدم أنه لم يتم التعرف على السلسلة المُحددة كقيمة صالحة للثقافة المُحددة.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
