---
title: وظيفة DATETIMEFORMAT ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETIMEFORMAT‏ (ER).
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
ms.openlocfilehash: e21b676046b6279826a728657fcc0d2a00a38b76
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287357"
---
# <a name="datetimeformat-er-function"></a>وظيفة DATETIMEFORMAT ER

[!include [banner](../includes/banner.md)]

تُرجع الدالة `DATETIMEFORMAT` قيمة *[سلسلة](er-formula-supported-data-types-primitive.md#string)* تمثل قيمة تاريخ/وقت معين كنص في التنسيق المحدد وفي [ثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) محددة بشكل اختياري. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>الوسائط

`datetime`: *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*

قيمة التاريخ/الوقت التي تمثل التاريخ والوقت المراد تنسيقه.

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

إذا لم يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء. على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية. قيمة `culture` الافتراضية هي **EN-US**.

عندما تقوم الوظيفة `DATETIMEFORMAT` بتحويل قيمة تاريخ/وقت مُحدد، فإنها تعتبر إعداد المنطقة الزمنية لمستخدم التطبيق الذي يقوم بتشغيل تنسيق ER الذي تمت استدعاء الوظيفة في سياقه.

## <a name="example-1"></a>مثال1

يُرجع التعبير `DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` قيمة تاريخ/وقت خادم التطبيق الحالي، 24 ديسمبر 2015، كـ **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد.

## <a name="example-2"></a>مثال2

تُرجع وظيفة `DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` قيمة تاريخ/وقت جلسة التطبيق الحالية، 24 ديسمبر 2015، كـ **"24.12.2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. 

## <a name="example-3"></a>المثال الثالث

تُرجع  `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` قيمة السلسلة **2019-11-12T08:00:00.0000000-08:00** عندما يتم استدعاء الدالة أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‏‫(GMT-08:00) توقيت الباسيفيكي (الولايات المتحدة وكند)‬‬** في قسم **تفضيلات البلد/المنطقة واللغة‬**.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
