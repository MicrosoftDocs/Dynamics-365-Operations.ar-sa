---
title: 'وظيفة ROUNDAMOUNT ER '
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDAMOUNT‏ (E).
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
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286018"
---
# <a name="roundamount-er-function"></a>وظيفة ROUNDAMOUNT ER 

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ROUNDAMOUNT` قيمة *حقيقية* كنتيجة لتقريب الرقم المُحدد إلى أقرب مضاعف لرقم آخر وفقًا لقاعدة التقريب المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد صحيح* أو *حقيقي*

قيمة رقمية يجب تقريبها.

`decimals`: *عدد صحيح* أو *حقيقي*

الرقم الذي يجب تقريب قيمة مُعلمة `number` إلى مضاعفه.

`round rule`: *قيمة التعداد*

قيمة التعداد لتعداد **RoundOffType** التي تُعرف قاعدة التقريب. يعرض هذا التعداد القيم التالية:

- عادي (عادي)
- انحداري (انحداري)
- التقريب (التقريب)

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة الرقمية الناتجة هي مضاعف للقيمة المُحدد بواسطة المُعلمة `decimals` وهي الأقرب إلى القيمة المُحددة بواسطة المُعلمة `number`.

## <a name="usage-notes"></a>ملاحظات الاستخدام

عندما تكون المُعلمة `number` صفر، تُرجع هذه الوظيفة دومًا صفر.

عندما تكون المُعلمة `decimals` صفر، تُقرب هذه الوظيفة إلى قيمة التقريب الافتراضية. عندما يتم تعيين مُعلمة `round rule` إلى **RoundOffType.Ordinary** ، تكون قيمة التقريب الافتراضية هي **0.01**.  وبخلاف ذلك، تكون قيمة التقريب الافتراضية هي **1.0**.

عند تعيين المُعلمة `round rule` إلى **RoundOffType.Ordinary** ، تُقرب هذه الوظيفة إلى أقرب مبلغ تقريب. 

عند تعيين المُعلمة `round rule` إلى **RoundOffType.RoundDown** ، تُقرب هذه الوظيفة في اتجاه الصفر إلى أقرب مبلغ تقريب.

عند تعيين المُعلمة `round rule` إلى **RoundOffType.RoundUp** ، تُقرب هذه الوظيفة بعيدًا عن اتجاه الصفر إلى أقرب مبلغ تقريب.

عند تعيين المُعلمة `round rule` إلى **RoundOffType.Ordinary** ، تتصرف هذه الوظيفة مثل وظيفة Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) ووظيفة X++ [ROUND](../dev-ref/xpp-math-run-time-functions.md#round).

## <a name="remarks"></a>ملاحظات

لتقريب قيمة رقمية إلى رقم محدد من المنازل العشرية، استخدم وظيفة [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>مثال

إذا تم تعيين المعلمة **model.RoundOff** إلى **RoundOffType.Ordinary** ، تٌرجع `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7.35.  

إذا تم تعيين المعلمة **model.RoundOff** إلى **RoundOffType.RoundDown** ، تٌرجع `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7.35.  

إذا تم تعيين المعلمة **model.RoundOff** إلى **RoundOffType.RoundUp** ، تٌرجع `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8.4. 

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)

[الدالات الحسابية](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
