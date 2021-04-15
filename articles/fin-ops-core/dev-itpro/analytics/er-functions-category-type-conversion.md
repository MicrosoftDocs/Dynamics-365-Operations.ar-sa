---
title: قائمة وظائف التقارير الإلكترونية في فئة تحويل النوع
description: يوفر هذا الموضوع معلومات حول وظائف التحويل المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 199d51ae8a4dbdd7d2f3bd290a2b487ceb1174dc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752594"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>قائمة وظائف التقارير الإلكترونية في فئة تحويل النوع

[!include [banner](../includes/banner.md)]

يُمكن استخدام وظائف تحويل نوع التقارير الإلكترونية (ER) لتحويل القيم بين الأنواع. يعرض هذا الموضوع ملخصًا لهذه الوظائف.

## <a name="type-conversion-functions"></a>وظائف تحويل النوع

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | تُرجع هذه الوظيفة قيمة *Int64* التي تمثل السلسلة المُحددة. |
| [IntValue](er-functions-conversion-intvalue.md)       | تُرجع هذه الوظيفة قيمة *Int* التي تمثل السلسلة المُحددة. |
| [NumberValue](er-functions-conversion-numbervalue.md) | تُرجع هذه الوظيفة قيمة *حقيقة* يتم تحويلها من قيمة *السلسلة* المُحددة. في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة. |
| [القيمة](er-functions-conversion-value.md)             | تُرجع هذه الوظيفة قيمة *حقيقة* يتم تحويلها من قيمة *السلسلة* المُحددة. |

## <a name="type-conversion-functions-in-the-container-category"></a>وظائف تحويل النوع في فئة الحاوية

يوضح الجدول التالي وظائف تحويل النوع في فئة [الحاوية](er-functions-category-container.md).

| الوظيفة | الوصف |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | تقوم دالة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *الحاوية*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>وظائف تحويل النوع في فئة التاريخ والوقت

يوضح الجدول التالي وظائف تحويل النوع في [فئة التاريخ والوقت](er-functions-category-datetime.md).

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة *سلسلة* معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة *تاريخ* معين إلى قيمة التاريخ/الوقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | تُرجع هذه الوظيفة قيمة *التاريخ* التي تم تحويلها من قيمة *سلسلة* معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. |

## <a name="type-conversion-functions-in-the-list-category"></a>وظائف تحويل النوع في فئة القائمة

يوضح الجدول التالي وظائف تحويل النوع في [فئة القائمة](er-functions-category-list.md).

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [قائمة](er-functions-list-list.md)                 | تُرجع هذه الوظيفة قيمة *قائمة السجلات* كقائمة جديدة تم إنشاءها من الوسيطات المُحددة من النوع *الحاوية (سجل)*. |
| [ListOfFields](er-functions-list-listoffields.md) | تُرجع هذه الوظيفة قيمة *قائمة السجل* التي تم إنشاؤها بناءً على بنية الوسيطة المُحددة للنوع *التعداد* أو *الحاوية (السجل)*. |
| [تقسيم](er-functions-list-split.md)               | تقسم هذه الوظيفة قيمة *السلسلة* المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة. |
| [StringJoin](er-functions-list-stringjoin.md)     | تُرجع هذه الوظيفة قيمة *السلسلة* التي تتكون من القيم المتصلة من الحقل المُحدد من قيمة *قائمة السجلات* المُحددة. يُمكن فصل القيم بالمحدد المعين. |

## <a name="type-conversion-functions-in-the-text-category"></a>وظائف تحويل النوع في فئة النص

يوضح الجدول التالي وظائف تحويل النوع في [فئة النص](er-functions-category-text.md).

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل حرف واحد مُشار إليه بواسطة رقم Unicode الموحد. |
| [GUIDVALUE](er-functions-text-guidvalue.md)       | تقوم هذه الوظيفة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل الرقم المُحدد بالتنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري. |
| [QrCode](er-functions-text-qrcode.md)             | تُرجع هذه الوظيفة قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR) للسلسلة المُحددة بالتنسيق الثنائي.  |
| [النص](er-functions-text-text.md)                 | تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل الرقم المُحدد بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي. |

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]