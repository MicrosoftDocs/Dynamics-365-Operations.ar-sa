---
title: MID ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية MID‏ (ER).
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
ms.openlocfilehash: c53963876db92bb07ed5ac49f009ed4f9bc5e8c4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285898"
---
# <a name="mid-er-function"></a>MID ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `MID` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من السلسلة المُحددة، بداية من الموضع المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمه *السلسلة* التي تحدد النص الذي سيتم إرجاع الأحرف منه.

`starting position`: *عدد صحيح*

قيمه *عدد صحيح* التي تحدد موضع الحرف الأول الذي يجب إرجاعه من النص المحدد.

`number of characters`: *عدد صحيح*

قيمه *عدد صحيح* التي تحدد عدد الأحرف التي يجب إرجاعها، بدءًا من موضع البداية المحدد.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا كانت قيمة الوسيطة `starting position` أقل من 0 (صفر)، يتم حساب الأحرف التي يتم إرجاعها من الموضع الأول في السلسلة المحددة.

إذا تجاوزت قيمة `starting position` الوسيطة طول السلسلة المحددة، يتم إرجاع سلسله فارغه.

## <a name="example"></a>مثال

تُرجع`MID ("Sample", 2, 3)` القيمة **"amp"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
