---
title: FIRST ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية FIRST‏ (ER).
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
ms.openlocfilehash: b06f07c4cfef5c74c22f60dfa37986ee88c544cf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275457"
---
# <a name="first-er-function"></a>FIRST ER وظيفة

[!include [banner](../includes/banner.md)]

تُعيد الوظيفة `FIRST` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم تكن هذه القائمة فارغة. إذا كانت القائمة فارغة، تطرح هذه الوظيفة استثناء.

## <a name="syntax"></a>بناء الجملة

```vb
FIRST (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="example-1"></a>مثال1

يُرجع التعبير `FIRST(SPLIT("ABC",1)).Value` القيمة النصية **"A"**.

## <a name="example-2"></a>مثال2

يطرح التعبير `FIRST(SPLIT("",1)).Value` استثناءًا في وقت التشغيل.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
