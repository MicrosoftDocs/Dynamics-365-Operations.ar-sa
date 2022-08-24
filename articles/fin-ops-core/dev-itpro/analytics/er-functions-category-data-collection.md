---
title: قائمة وظائف التقارير الإلكترونية في فئة جمع البيانات
description: توفر هذه المقالة معلومات عن وظائف جمع البيانات المعتمدة في التقارير الإلكترونية (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286138"
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
