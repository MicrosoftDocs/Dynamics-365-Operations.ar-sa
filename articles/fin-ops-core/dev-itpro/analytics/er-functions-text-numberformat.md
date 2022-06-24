---
title: NUMBERFORMAT ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERFORMAT‏ (ER).
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 3e6fa4cbdfb2509418a40980aa29894b5e531bbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862179"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم وظيفة `NUMBERFORMAT` بإرجاع قيمة *سلسلة* تمثل الرقم المحدد في التنسيق المُحدد وفي [الثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-numeric-format-strings) و [مخصص](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد صحيح* أو *حقيقي*

قيمة رقمية تُحدد الرقم الذي يجب تنسيقه.

`format`: *السلسلة*

قيمة *سلسلة* تمثل التنسيق.

`culture`: *السلسلة*

قيمة *السلسلة* التي تمثل الثقافة لاستخدامها للتنسيق.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا لم يتم تعريف الثقافة كوسيطه للوظيفة المسماة، فإن السياق الذي يتم فيه تشغيل هذه الوظيفة يحدد الثقافة التي يتم استخدامها لتنسيق الأرقام.

## <a name="example-1"></a>مثال1

للثقافة **EN-US**, ترجع `NUMBERFORMAT (0.45, "p")` القيمة **"45.00 %"**، وترجع `NUMBERFORMAT (10.45, "#")` القيمة **"10"**.

## <a name="example-2"></a>مثال2

تُرجع`NUMBERFORMAT (10/3, "F2", "de")` القيمة **3،33**، بينما تُرجع `NUMBERFORMAT (10/3, "F2", "en-us")` القيمة **3.33**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]