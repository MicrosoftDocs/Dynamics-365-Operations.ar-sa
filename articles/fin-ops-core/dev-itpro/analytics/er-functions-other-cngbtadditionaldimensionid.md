---
title: CN_GBT_ADDITIONALDIMENSIONID ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية CN_GBT_ADDITIONALDIMENSIONID‏ (ER).
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281741"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم الوظيفة `CN_GBT_ADDITIONALDIMENSIONID` بإرجاع قيمة *سلسلة* تمثل مُعرف بعد مالي واحد مأخوذ من السلسلة المُحددة. تعرض السلسلة المُحددة كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.

## <a name="syntax"></a>بناء الجملة

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة *سلسلة* تمثل كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.

`number`: عدد صحيح

قيمة *عدد صحيح* تُحدد كود التسلسل للبعد المُطلوب في السلسلة المُحددة.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

تُرجع `CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` **"CC"**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
