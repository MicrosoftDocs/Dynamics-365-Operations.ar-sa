---
title: وظيفة WEEKNUM ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكتروني WEEKNUM‏ (ER).
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268135"
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
