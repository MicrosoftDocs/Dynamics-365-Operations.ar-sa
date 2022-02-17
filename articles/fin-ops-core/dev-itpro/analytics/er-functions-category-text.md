---
title: قائمة وظائف التقارير الإلكترونية من فئة النص
description: يوفر هذا الموضوع معلومات حول وظائف النص المعتمدة في التقارير الإلكترونية (ER).
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
ms.openlocfilehash: afe45bf1ff5c641346997aa4f32f3241dce2f0a2
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075490"
---
# <a name="list-of-er-functions-of-the-text-category"></a>قائمة وظائف التقارير الإلكترونية من فئة النص

[!include [banner](../includes/banner.md)]

يُمكن استخدام وظائف النص في التقارير الإلكترونية (ER) لاستخراج المعلومات من وتنفيذ العمليات علي مصادر البيانات من نوع البيانات *السلسلة*. يعرض هذا الموضوع ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [Char](er-functions-text-char.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح حرف واحد مُشار إليه بواسطة رقم Unicode الموحد. |
| [تسلسل](er-functions-text-concatenate.md) | تُرجع هذه الوظيفة جميع السلاسل النصية المُحددة كقيمة *السلسلة* بعد ضمها في سلسلة واحدة. |
| [تنسيق](er-functions-text-format.md) | تُرجع هذه الوظيفة السلسلة المُحددة كقيمة *السلسلة* بعد أن تم تنسيقها باستبدال أي تواجد من **%N** بالوسيطة *N*. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | تبحث هذه الوظيفة عن قيمة *تعداد* مُحددة في مصدر بيانات التعداد المُحدد باستخدام اسم التعداد المُحدد كقيمة *السلسلة*. إذا تم العثور على قيمة *تعداد* ، تقوم الوظيفة بإرجاعها. |
| [GetLabelText](er-functions-text-getlabeltext.md) | تبحث هذه الدالة عن تسمية معينة لإرجاع قيمة *[String](er-formula-supported-data-types-primitive.md#string)* تمثل ترجمة التسمية المحددة باللغة المحددة. |
| [GUIDVALUE](er-functions-text-guidvalue.md) | تقوم هذه الوظيفة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | تُحلل هذه الوظيفة البيانات في تنسيق JavaScript Object Notation (JSON) الذي يتم الوصول إليه في المسار المُحدد، ويستخرج قيمة عددية تعتمد على المعرف المحدد.‬   ثم يقوم بإرجاع القيمة العددية المستخرجة كقيمة *سلسلة* . |
| [إلى اليسار](er-functions-text-left.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة. |
| [Len](er-functions-text-len.md) | تُرجع هذه الوظيفة قيمة *عدد صحيح* توضح عدد الأحرف في السلسلة المُحددة. |
| [Lower](er-functions-text-lower.md) | تُرجع هذه الوظيفة سلسلة النص المُحددة كقيمة *السلسلة* بعد أن تم تحويلها إلى أحرف صغيرة. |
| [Mid](er-functions-text-mid.md) | تُرجع هذه الوظيفة قيمة *[السلسلة](er-formula-supported-data-types-primitive.md#string)* التي توضح العدد المُحدد من الأحرف من السلسلة المُحددة، بداية من المنصب المُحدد. |
| [NewGUID](er-functions-text-newguid.md) | تقوم هذه الدالة بإرجاع قيمه *[GUID](er-formula-supported-data-types-primitive.md#guid)* التي تم إنشاؤها حديثا. |
| [NumberFormat](er-functions-text-numberformat.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح الرقم المُحدد بالتنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | تُرجع هذه الوظيفة الرقم المُحدد كقيمة *السلسلة* بعد كتابته (أي تحويله إلى سلاسل نصية) باللغة المُحددة. |
| [PadLeft](er-functions-text-padleft.md) | تُرجع هذه الوظيفة قيمة *السلسلة* بطول مُحدد، تمت فيه تعبئة بداية السلسلة المُحددة بمثيل واحد أو أكثر من الأحرف المُحددة. |
| [QrCode](er-functions-text-qrcode.md) | تُرجع هذه الوظيفة قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR) للسلسلة المُحددة بالتنسيق الثنائي.  |
| [استبدال](er-functions-text-replace.md) | تُرجع هذه الوظيفة السلسلة النصية المُحددة كقيمة *السلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى. |
| [إلى اليمين](er-functions-text-right.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من نهاية السلسلة المُحددة. |
| [النص](er-functions-text-text.md) | تُرجع هذه الوظيفة الرقم المُحدد كقيمة *سلسلة* بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي. |
| [ترجمة](er-functions-text-translate.md) | تقوم هذه الدالة بإرجاع قيمة *سلسلة* تحتوي على نتيجة استبدال النص المحدد بأحرف بمجموعة أحرف أخرى متوفرة. |
| [Trim](er-functions-text-trim.md) | تُرجع هذه الوظيفة سلسلة النص المُحددة كقيمة *سلسلة* بعد اقتطاع المسافات البادئة والزائدة، وبعد أن تمت إزالة المسافات المتعددة بين الكلمات. |
| [Upper](er-functions-text-upper.md) | تُرجع هذه الوظيفة سلسلة النص المُحددة كقيمة *السلسلة* بعد أن تم تحويلها إلى أحرف كبيرة. |

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
