---
title: 'وظيفة NUMBERVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERVALUE (ER).
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755338"
---
# <a name="numbervalue-er-function"></a>وظيفة NUMBERVALUE ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `NUMBERVALUE` قيمة *حقيقية* يتم تحويلها من قيمة *السلسلة* المُحددة. في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية يجب تحويلها إلى رقم *حقيقي*.

`decimal separator`: السلسلة

فاصل عشري. يُستخدم لفصل العدد الصحيح والأجزاء الكسرية لرقم عشري.

`digit grouping separator`: *السلسلة*

فاصل تجميع أرقام. يُستخدم كفاصل آلاف.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `NUMBERVALUE( "1 234,56", ",", " ")` **1234.56**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تحويل النوع](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]