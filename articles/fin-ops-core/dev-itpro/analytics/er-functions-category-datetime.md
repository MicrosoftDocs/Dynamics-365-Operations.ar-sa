---
title: قائمة وظائف التقارير الإلكترونية في فئة التاريخ والوقت
description: توفر هذه المقالة معلومات عن وظائف التاريخ والوقت المعتمدة في التقارير الإلكترونية (ER).
author: kfend
ms.date: 09/09/2021
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
ms.openlocfilehash: d77f41e10d927a9aae06b9ba0fc58ca237c071cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291313"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>قائمة وظائف التقارير الإلكترونية في فئة التاريخ والوقت

[!include [banner](../includes/banner.md)]

يمكن استخدام وظائف التاريخ والوقت في التقارير الإلكترونية (ER) لاستخراج المعلومات من قيم التاريخ والوقت، ولتنفيذ العمليات عليها. توفر هذه المقالة ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | تُرجع هذه الوظيفة قيمة *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* والتي هي عدد الأيام المُحددة قبل أو بعد تاريخ البدء المُحدد. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة تاريخ/وقت معين إلى قيمةالتاريخ/الوقت في منطقة زمنية أخرى. |
| [DateFormat](er-functions-datetime-dateformat.md) | تقوم هذه الوظيفة بإرجاع قيمة *[السلسلة](er-formula-supported-data-types-primitive.md#string)* التي تمثل قيمة تاريخ مُعين كنص في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | تقوم هذه الوظيفة بإرجاع قيمة *السلسلة* التي تمثل قيمة تاريخ/وقت مُعين كنص في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | تقوم هذه الوظيفة بإرجاع قيمة *DateTime* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة تاريخ معين إلى قيمةالتاريخ/الوقت بالتوقيت  العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | تقوم هذه الوظيفة بإرجاع قيمة *[التاريخ](er-formula-supported-data-types-primitive.md#date)* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | ترجع الوظيفة قيمة *[عدد صحيح](er-formula-supported-data-types-primitive.md#integer)* تمثل عدد الأيام بين 1 يناير والتاريخ المُحدد. |
| [الأيام](er-functions-datetime-days.md) | تُرجع هذه الوظيفة قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني. |
| [Now](er-functions-datetime-now.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل تاريخ خادم التطبيق الحالي والتوقيت. |
| [NullDate](er-functions-datetime-nulldate.md) | تُرجع هذه الوظيفة قيمة *تاريخ* والتي تمثل التاريخ **الفارغ** (1 يناير 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل قيمة التاريخ/الوقت **الفارغة** (1 يناير 1900) بالتوقيت العالمي المتفق عليه. |
| [SessionNow](er-functions-datetime-sessionnow.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل تاريخ جلسة التطبيق الحالية والتوقيت. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | تُرجع هذه الوظيفة قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالية. |
| [اليوم](er-functions-datetime-today.md) | تُرجع هذه الوظيفة قيمة *التاريخ* التي تمثل تاريخ خادم التطبيق الحالي. |
| [WeekNum](er-functions-datetime-weeknum.md) | تُرجع هذه الوظيفة قيمة *عدد صحيح* التي تمثل أسبوع من السنة. |

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
