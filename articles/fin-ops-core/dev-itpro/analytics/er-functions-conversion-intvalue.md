---
title: 'وظيفة INTVALUE ER  '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INTVALUE (ER).
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755362"
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

*Int*

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