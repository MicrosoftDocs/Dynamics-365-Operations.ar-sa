---
title: وظيفة DATEFORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEFORMAT (ER).
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
ms.openlocfilehash: 4a6c113f5f8147cbeaab103e86a44d4c66272c13
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485482"
---
# <a name="dateformat-er-function"></a>وظيفة DATEFORMAT ER

[!include [banner](../includes/banner.md)]

تُرجع الدالة `DATEFORMAT` قيمة *[سلسلة](er-formula-supported-data-types-primitive.md#string)* تمثل قيمة تاريخ مُعيّن كنص في التنسيق المُحدد وفي [ثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) محددة بشكل اختياري. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>الوسائط

`date`: *[التاريخ](er-formula-supported-data-types-primitive.md#date)*

قيمة التاريخ التي تمثل تاريخ التنسيق.

`format`: *السلسلة*

تنسيق سلسلة الإخراج. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> تكون سلسله التنسيق حساسة لحاله الأحرف عند استخدام اما تنسيق قياسي أو تنسيق مخصص. علي سبيل المثال، يقوم محدد التنسيق [القياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" بإرجاع التاريخ باستخدام نمط التاريخ القصير، بينما يقوم محدد التنسيق القياسي "d" بإرجاع التاريخ باستخدام نمط التاريخ الطويل. بالاضافه إلى ذلك ، يقوم محدد التنسيق [المخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings) "m" بإرجاع الشهر من 1 إلى 12، بينما يقوم محدد التنسيق المخصص "m" بإرجاع الدقيقة من 0 إلى 59.

`culture`: *السلسلة*

الثقافة التي سيتم استخدامها للتنسيق. للحصول علي معلومات حول الثقافات المعتمدة، راجع [الثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>إرجاع القيم

*سلسلة*

قيمة السلسلة الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا لم يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء. على سبيل المثال، إذا تم استدعاء الوظيفة `DATEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية. قيمة `culture` الافتراضية هي **EN-US**.

## <a name="example-1"></a>مثال1

تُرجع وظيفة `DATEFORMAT (TODAY (), "dd-MM-yyyy")` تاريخ خادم التطبيق الحالي، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد. 

## <a name="example-2"></a>مثال2

تُرجع وظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` قيمة تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. 

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
