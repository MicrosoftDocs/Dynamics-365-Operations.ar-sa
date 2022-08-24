---
title: GETCURRENTCOMPANY ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETCURRENTCOMPANY‏ (ER).
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b5f5f7d7c884000f59b93e10875f78289a879779
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280174"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `GETCURRENTCOMPANY` قيمة *السلسلة* التي تمثل كود الكيان القانوني (الشركة) الذي يقوم مستخدم بتسجيل الدخول فيه حاليًا.

## <a name="syntax"></a>بناء الجملة

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `GETCURRENTCOMPANY ()` **USMF** لمستخدم سجل دخوله إلى شركة **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
