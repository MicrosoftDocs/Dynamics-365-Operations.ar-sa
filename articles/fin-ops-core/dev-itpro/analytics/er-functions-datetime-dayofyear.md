---
title: وظيفة DAYOFYEAR ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية DAYOFYEAR‏ (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: fc4d1d3293c31b1b89a7390c8ac313e1407d433e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848769"
---
# <a name="dayofyear-er-function"></a>وظيفة DAYOFYEAR ER

[!include [banner](../includes/banner.md)]

ترجع الوظيفة `DAYOFYEAR` قيمة *عدد صحيح* تمثل عدد الأيام بين 1 يناير والتاريخ المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>الوسائط

`date`: *التاريخ*

قيمة التاريخ التي تمثل التاريخ المراد الذي سيتم استخدامه لحساب عدد الأيام.

## <a name="return-values"></a>إرجاع القيم

*عدد صحيح*

القيمة العددية الناتجة.

## <a name="example-1"></a>مثال1

يُرجع التعبير `DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` **61**.

## <a name="example-2"></a>مثال2

يُرجع التعبير `DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` **1**.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]