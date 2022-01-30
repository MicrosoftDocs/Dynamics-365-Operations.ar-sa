---
title: وظيفة WEEKNUM ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني WEEKNUM (ER).
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 37e62b32896e2030b3322a89ac4acdd6c18d5e3c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982167"
---
# <a name="weeknum-er-function"></a>وظيفة WEEKNUM ER

[!include [banner](../includes/banner.md)]

ترجع الوظيفة `WEEKNUM` قيمة *[عدد صحيح](er-formula-supported-data-types-primitive.md#integer)* تمثل أسبوع من السنة التي تتضمن قيمة *[تاريخ](er-formula-supported-data-types-primitive.md#date)* محددة. يعتمد الحساب على القواعد المعتمدة على الثقافة والتي تحدد أسبوع تقويم واليوم الأول من الأسبوع.

## <a name="syntax"></a>بناء الجملة

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">الوسائط</a>

`date`: *التاريخ*

قيمة التاريخ التي تمثل التاريخ المراد لحساب الأسبوع من السنة.

`culture`: *[السلسلة](er-formula-supported-data-types-primitive.md#string)*

الثقافة التي سيتم استخدامها للحساب. يمكنك استخدام أكواد الثقافة التي يتم دعمها وفقًا .NET [standards](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>إرجاع القيم

*عدد صحيح*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يتم حساب الأسبوع في السنه بناءً على المقياس [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)، إذا تم اعتماد هذا المقياس ‏‫حسب البلد أو المنطقة الذي توفره الإعدادات المحلية في وقت التشغيل. وبخلاف ذلك، يعتمد الحساب على المعايير القومية الخاصة بالبلد/المنطقة.

إذا تم توفير كود [ثقافة](#arguments) كوسيطة لوظيفة `WEEKNUM` في وقت التشغيل، فإنه يتم طرح استثناء في وقت التشغيل. إذا تم توفير السلسلة الفارغة ككود ثقافة، فإنه يتم استخدام التقويم المحايد للإنجليزية لحساب رقم الأسبوع.

## <a name="examples"></a>أمثلة

يُرجع التعبير `WEEKNUM (DATEVALUE ("01-01-2020", "de"))` **1**.

يُرجع التعبير `WEEKNUM (DATEVALUE ("01-01-2021", "de"))` **53**.

يُرجع التعبير `WEEKNUM (DATEVALUE ("01-01-2022", "de"))` **52**.

يُرجع التعبير `WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` **21**.

## <a name="additional-resources"></a>الموارد الإضافية

[‏‫دالات التاريخ والوقت‬](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
