---
title: وظيفة PADLEFT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية PADLEFT (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680136"
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
