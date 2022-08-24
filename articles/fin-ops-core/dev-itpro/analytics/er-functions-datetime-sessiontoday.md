---
title: SESSIONTODAY ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية SESSIONTODAY‏ (ER).
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 0eeb4fcc449b565774cc79b767a2d157557d5b98
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274878"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `SESSIONTODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالي.

## <a name="syntax"></a>بناء الجملة

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>إرجاع القيم

*التاريخ*

قيمة التاريخ الناتجة.

## <a name="example"></a>مثال

تُرجع وظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` قيمة تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. 

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
