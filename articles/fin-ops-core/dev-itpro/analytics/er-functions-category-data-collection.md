---
title: قائمة وظائف التقارير الإلكترونية في فئة جمع البيانات
description: توفر هذه المقالة معلومات عن وظائف جمع البيانات المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: a8d4f5068bedcf1f15ae5257e29004a4773ef84c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908550"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>قائمة وظائف التقارير الإلكترونية في فئة جمع البيانات

[!include [banner](../includes/banner.md)]

يتم استخدام وظائف جمع بيانات التقارير الإلكترونية (ER) لإجراء العد والجمع بتنسيق التقارير الإلكترونية التي يتم تشغيلها، استنادًا إلى بيانات المخرجات التي تم إنشاؤها بالفعل بتنسيق **نص** أو **Xml** . يستخدم هذا الأسلوب للمساعدة في تحسين أداء تنسيق التقارير الإلكترونية التي يتم تشغيلها، وإدخال قيم تشغيل الإجماليات في المستندات التي تم إنشاؤها، ولأغراض أخرى. توفر هذه المقالة ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | تُرجع هذه الوظيفة قيمة *قائمة السجل* التي تحتوي على قائمة القيم التي تم ارجاعها بواسطة خاصية **قيمة مفتاح البيانات التي تم جمعها** من عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لتكوين تشغيل مستند صادر أثناء التنسيق، والذي يفي بالشروط المحددة. يتكون كل شرط من نطاق المفتاح وقيمة المفتاح. |
| [CountIF](er-functions-datacollection-countif.md) | تقوم هذه الوظيفة بإرجاع قيمه *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشرط المحدد. يتكون الشرط من نطاق المفتاح وقيمة المفتاح. |
| [CountIFs](er-functions-datacollection-countifs.md) | تقوم هذه الوظيفة بإرجاع قيمه *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشروط المحددة. يتكون كل شرط من نطاق المفتاح وقيمة المفتاح. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | تقوم هذه الوظيفة بإرجاع قيمة *سلسلة* التي تمثل اسم عنصر تنسيق التقارير الإلكترونية الحالية. |
| [SumIF](er-functions-datacollection-sumif.md) | تقوم هذه الوظيفة بإرجاع قيمة *حقيقي* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشرط المحدد . يتكون الشرط من نطاق المفتاح وقيمة المفتاح. |
| [SumIFs](er-functions-datacollection-sumifs.md) | تقوم هذه الوظيفة بإرجاع قيمة *حقيقي* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشروط المحددة. يتكون كل شرط من نطاق المفتاح وقيمة المفتاح. |

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]