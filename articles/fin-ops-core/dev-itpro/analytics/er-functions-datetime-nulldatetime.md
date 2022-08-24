---
title: NULLDATETIME ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية NULLDATETIME‏ (ER).
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
ms.openlocfilehash: 49b75a6cc1e2c1eee926ed8a235ae886d781ad3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287267"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم وظيفة `NULLDATETIME` بإرجاع قيمة *DateTime* التي تظهر قيمة التاريخ/الوقت **الفارغة** (1 يناير 1900) بالتوقيت العالمي المتفق عليه (توقيت جرينتش المتوسط \[GMT\]).

## <a name="syntax"></a>بناء الجملة

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="example"></a>مثال

تُرجع وظيفة `DATETIMEFORMAT( NULLDATETIME(), "O")` قيمة السلسلة **1900-01-01T00:00:00.0000000+00:00** عندما يتم استدعاءها أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‫التوقيت العالمي المتفق عليه (GMT)‬** في قسم **‏‫تفضيلات البلد/المنطقة واللغة‬**.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
