---
title: وظيفة PADLEFT ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية PADLEFT‏ (ER).
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278877"
---
# <a name="padleft-er-function"></a>وظيفة PADLEFT ER

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `PADLEFT` قيمة *سلسلة* بطول مُحدد، تمت فيه تعبئة بداية السلسلة المُحددة بالأحرف المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة *سلسلة* التي تمثل النص الأصلي.

`length`: *عدد صحيح*

قيمة *عدد صحيح* تمثل الرقم النهائي للأحرف في السلسلة المُحددة.

`padding chars`: *السلسلة*

الأحرف التي سوف يتم استخدامها للتحديد.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

تُرجع `PADLEFT ("1234", 10, "`&nbsp;`")` السلسلة النصية **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
