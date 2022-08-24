---
title: CHAR ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية CHAR‏ (ER).
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
ms.openlocfilehash: 61e402718723325fc975d577ab76039e3e59691e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288037"
---
# <a name="char-er-function"></a>CHAR ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CHAR` قيمة *السلسلة* التي توضح حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.

## <a name="syntax"></a>بناء الجملة

```vb
CHAR (number)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد صحيح*

رقم يتوافق مع حرف مفرد متوقع.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تتوقف السلسلة التي تُرجعها هذه وظيفة على الترميز المحدد في عنصر تنسيق **FILE** الأصلي. للحصول على قائمة بالرموز المدعومة، راجع [فئة الترميز](/dotnet/api/system.text.encoding).

## <a name="example"></a>مثال

تُرجع `CHAR (255)` **"ÿ"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
