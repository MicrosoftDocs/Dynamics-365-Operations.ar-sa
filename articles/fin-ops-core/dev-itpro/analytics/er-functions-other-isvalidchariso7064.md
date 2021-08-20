---
title: ISVALIDCHARACTERISO7064 ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ISVALIDCHARACTERISO7064 (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 884fbf7371ea9d9ac931655f8b11ec1e13c83a46aaa831c96f5d558209205e09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763562"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ISVALIDCHARACTERISO7064` قيمة *منطقية* **TRUE** إذا كانت السلسلة المُحددة تمثل رقم حساب مصرفي دولي (IBAN) صالحًا. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.

## <a name="syntax"></a>بناء الجملة

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية تمثل رقم الـ IBAN.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` **TRUE**. 

يُرجع التعبير `ISVALIDCHARACTERISO7064 ("AT61")` **FALSE**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]