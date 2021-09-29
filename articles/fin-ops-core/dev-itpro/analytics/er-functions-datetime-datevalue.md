---
title: 'وظيفة DATEVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEVALUE (ER).
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 446f1357e54342073e73f86ef36e6467e029ebc4
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485564"
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
