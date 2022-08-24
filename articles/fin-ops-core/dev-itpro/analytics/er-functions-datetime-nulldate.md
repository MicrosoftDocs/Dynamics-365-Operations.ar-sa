---
title: NULLDATE ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية NULLDATE‏ (ER).
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
ms.openlocfilehash: 276ad99303a4e88ecb1c83e9518e06bfd7afaa45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272641"
---
# <a name="nulldate-er-function"></a>NULLDATE ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `NULLDATE` قيمة *تاريخ* يمثل التاريخ **الفارغ** (1 يناير 1900).

## <a name="syntax"></a>بناء الجملة

```vb
NULLDATE () as 
```

## <a name="return-values"></a>إرجاع القيم

*التاريخ*

قيمة التاريخ الناتجة.

## <a name="example-1"></a>مثال1

تُرجع وظيفة `DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` التاريخ **الفارغ**،1 يناير 1900 كـ **"1900-01-01"**، بناءً على التنسيق المخصص المُحدد.

## <a name="example-2"></a>مثال2

يُرجع التعبير `IF( Invoice.DocumentDate = NULLDATE(), true, false)` **True** عندما تكون قيمة الحقل **DocumentDate** تساوي التاريخ **الفارغ**. في هذا المثال، **Invoice** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **سجلات المالية/الجدول** ، ويشير إلى جدول CustInvoiceJour.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
