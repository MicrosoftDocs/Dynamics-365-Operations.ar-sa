---
title: STRINGJOIN ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية STRINGJOIN‏ (ER).
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6510c271ac5e01d841722fdf2c5fd8c7deaf8caf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271632"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `STRINGJOIN` قيمة *السلسلة* التي تتكون من القيم المتصلة للحقل المُحدد من القائمة المُحددة. يُمكن فصل القيم بالمحدد المعين.

## <a name="syntax"></a>بناء الجملة

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`field`: *الحقل*

المسار الصالح لحقل من نوع بيانات *السلسلة* في القائمة المُحددة.

`delimiter`: *السلسلة*

مُحدد يستخدم لفصل السلاسل الفرعية.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

إذا قمت بإدخال `SPLIT("abc" , 1)` كمصدر بيانات **DS**، يُرجع التعبير `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
