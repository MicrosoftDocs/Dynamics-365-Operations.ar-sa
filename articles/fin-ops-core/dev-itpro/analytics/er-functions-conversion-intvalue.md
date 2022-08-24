---
title: 'وظيفة INTVALUE ER  '
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية INTVALUE‏ (ER).
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282610"
---
# <a name="intvalue-er-function"></a>وظيفة INTVALUE ER  

[!include [banner](../includes/banner.md)]

تُعيد وظيفة `INTVALUE` قيمة *Int* التي تمثل السلسلة المُحددة.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية يجب تحويلها إلى رقم *Int*.

`number`: *عدد حقيقي* أو *صحيح*

قيمة رقمية *حقيقية* أو *عدد صحيح* يجب تحويلها إلى رقم *Int*.

## <a name="return-values"></a>إرجاع القيم

*الفترة*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يتم اقتطاع أيٍّ من المنازل العشرية.

## <a name="example-1"></a>مثال1

يُرجع `INTVALUE ("100.77")` قيمة *Int* **100**.

## <a name="example-2"></a>مثال2

يُرجع `INTVALUE (-100.77)` قيمة *Int* **100**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تحويل النوع](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
