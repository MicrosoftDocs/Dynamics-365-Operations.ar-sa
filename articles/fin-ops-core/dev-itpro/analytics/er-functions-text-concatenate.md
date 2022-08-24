---
title: 'وظيفة CONCATENATE ER '
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية CONCATENATE‏ (ER)
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
ms.openlocfilehash: 230bbbac5df7824c3ef7d0550cc45dbf6c374858
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267273"
---
# <a name="concatenate-er-function"></a>وظيفة CONCATENATE ER 

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CONCATENATE` جميع السلاسل النصية المُحددة كقيمة *سلسلة* بعد انضمامها في سلسلة واحدة.

## <a name="syntax"></a>بناء الجملة

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>الوسائط

`text 1`: *السلسلة*

مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*. هذه الوسيطة مطلوبة.

`text N`: *السلسلة*

مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `CONCATENATE ("abc", "def")` **"abcdef"**.

## <a name="usage-notes"></a>ملاحظات الاستخدام

كما يُرجع التعبير `"abc" & "def"` **"abcdef"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
