---
title: وظيفة DATETIMEVALUE ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETIMEVALUE‏ (ER).
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
ms.openlocfilehash: 7e3af6a279163183546255908730ba32d790a22b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870424"
---
# <a name="datetimevalue-er-function"></a>وظيفة DATETIMEVALUE ER

[!include [banner](../includes/banner.md)]

تُرجع الدالة `DATETIMEVALUE` قيمة *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* تم تحويلها من قيمة نصية مُعينة في التنسيق المحدد وفي [ثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) محددة بشكل اختياري إلى قيمة تاريخ/وقت. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>الوسائط

`text`: *[سلسلة](er-formula-supported-data-types-primitive.md#string)*

النص الذي يمثل القيمة المراد تنسيقها.

`format`: *السلسلة*

تنسيق النص المُعين. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *السلسلة*

الثقافة المستخدمة لتنسيق النص المُحدد. للحصول علي معلومات حول الثقافات المعتمدة، راجع [الثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>إرجاع القيم

*التاريخ/الوقت*

قيمة التاريخ/الوقت الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء. على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية. قيمة `culture` الافتراضية هي **EN-US**.

## <a name="example-1"></a>مثال1

يُرجع التعبير `DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` **2:55:00 ص في 21 ديسمبر 2016** ، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.

## <a name="example-2"></a>مثال2

يُرجع التعبير `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` **‬‏‫2:55:00 ص في 21 ديسمبر 2016** ، استنادًا إلى التنسيق المخصص والثقافة.

ومع ذلك، ستطرح `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` استثناءً لإعلام المستخدم بأنه لم يتم التعرف على السلسلة المحددة كقيمة تاريخ/وقت صالحة للثقافة المُحددة.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
