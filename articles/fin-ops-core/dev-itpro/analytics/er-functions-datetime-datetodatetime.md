---
title: وظيفة DATETODATETIME ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETODATETIME‏ (ER).
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
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287297"
---
# <a name="datetodatetime-er-function"></a>وظيفة DATETODATETIME ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `DATETODATETIME` قيمة *DateTime* يتم تحويلها من قيمة تاريخ مُعين إلى قيمة تاريخ/وقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).

## <a name="syntax"></a>بناء الجملة

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>الوسائط

`date`: *التاريخ*

قيمة التاريخ التي تمثل التاريخ المُراد تحويله.

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="example-1"></a>مثال1

يُرجع `DATETODATETIME (CompInfo. 'getCurrentDate()')` تاريخ جلسة 365‎ Finance Microsoft Dynamics الحالية، 24 ديسمبر 2015، على الشكل التالي **12/24/2015 12:00:00 صباحًا**. في هذا المثال، **CompInfo** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **التمويل والعمليات/جدول** ، ويشير إلى جدول CompanyInfo.

## <a name="example-2"></a>مثال2

يُرجع `DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` قيمة التاريخ/الوقت **11/12/2019 12:00:00 AM**. 

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
