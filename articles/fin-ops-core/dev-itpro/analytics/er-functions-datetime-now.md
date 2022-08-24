---
title: NOW ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية NOW‏ (ER).
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
ms.openlocfilehash: 5eded43b0c03304bcb03136bffc18b1630242946
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268654"
---
# <a name="now-er-function"></a>NOW ER وظيفة

[!include [banner](../includes/banner.md)]

ُتُرجع وظيفة `NOW` قيمة *DateTime* التي تمثل تاريخ خادم التطبيق الحالي والتوقيت.

## <a name="syntax"></a>بناء الجملة

```vb
NOW ()
```

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` قيمة تاريخ/وقت خادم التطبيق الحالي، 24 ديسمبر 2015، كـ **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
