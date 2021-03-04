---
title: INT64VALUE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INT64VALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686040"
---
# <a name="int64value-er-function"></a>INT64VALUE ER وظيفة

[!include [banner](../includes/banner.md)]

تُعيد وظيفة `INT64VALUE` قيمة *Int64* التي تمثل السلسلة المُحددة.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية يجب تحويلها إلى رقم *Int64*.

`number`: *عدد حقيقي* أو *صحيح*

قيمة رقمية *حقيقية* أو *عدد صحيح* يجب تحويلها إلى رقم *Int64*.

## <a name="return-values"></a>إرجاع القيم

*Int64*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يتم اقتطاع أيٍّ من المنازل العشرية.

## <a name="example-1"></a>مثال1

يُرجع `INT64VALUE ("22565422744")` قيمة *Int64* **22565422744**.

## <a name="example-2"></a>مثال2

يُرجع `INT64VALUE ( VALUE("22565422744.77"))` قيمة *Int64* **‎22565422744**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تحويل النوع](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]