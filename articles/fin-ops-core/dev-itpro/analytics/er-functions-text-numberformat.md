---
title: NUMBERFORMAT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERFORMAT (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2c3907d1d2c74c852f4f90731e5f4bc23bfbd717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680256"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم وظيفة `NUMBERFORMAT` بإرجاع قيمة *سلسلة* تمثل الرقم المحدد في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري. لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

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