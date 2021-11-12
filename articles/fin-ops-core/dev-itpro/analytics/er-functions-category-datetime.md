---
title: قائمة وظائف التقارير الإلكترونية في فئة التاريخ والوقت
description: يوفر هذا الموضوع معلومات حول وظائف التاريخ والوقت المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: 706331eaadf602aba46463fdcfc0d38f1fc94e08
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647253"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>قائمة وظائف التقارير الإلكترونية في فئة التاريخ والوقت

[!include [banner](../includes/banner.md)]

يمكن استخدام وظائف التاريخ والوقت في التقارير الإلكترونية (ER) لاستخراج المعلومات من قيم التاريخ والوقت، ولتنفيذ العمليات عليها. يعرض هذا الموضوع ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | تُرجع هذه الوظيفة قيمة *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* والتي هي عدد الأيام المُحددة قبل أو بعد تاريخ البدء المُحدد. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة تاريخ/وقت معين إلى قيمةالتاريخ/الوقت في منطقة زمنية أخرى. |
| [DateFormat](er-functions-datetime-dateformat.md) | تقوم هذه الوظيفة بإرجاع قيمة *[السلسلة](er-formula-supported-data-types-primitive.md#string)* التي تمثل قيمة تاريخ مُعين كنص في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | تقوم هذه الوظيفة بإرجاع قيمة *السلسلة* التي تمثل قيمة تاريخ/وقت مُعين كنص في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | تقوم هذه الوظيفة بإرجاع قيمة *DateTime* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة تاريخ معين إلى قيمةالتاريخ/الوقت بالتوقيت  العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | تقوم هذه الوظيفة بإرجاع قيمة *التاريخ* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | تُرجع هذه الوظيفة قيمة *عدد صحيح* تمثل عدد الأيام من 1 يناير إلى التاريخ المُحدد. |
| [الأيام](er-functions-datetime-days.md) | تُرجع هذه الوظيفة قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني. |
| [Now](er-functions-datetime-now.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل تاريخ خادم التطبيق الحالي والتوقيت. |
| [NullDate](er-functions-datetime-nulldate.md) | تُرجع هذه الوظيفة قيمة *تاريخ* والتي تمثل التاريخ **الفارغ** (1 يناير 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل قيمة التاريخ/الوقت **الفارغة** (1 يناير 1900) بالتوقيت العالمي المتفق عليه. |
| [SessionNow](er-functions-datetime-sessionnow.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل تاريخ جلسة التطبيق الحالية والتوقيت. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | تُرجع هذه الوظيفة قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالية. |
| [اليوم](er-functions-datetime-today.md) | تُرجع هذه الوظيفة قيمة *التاريخ* التي تمثل تاريخ خادم التطبيق الحالي. |

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
