---
title: AND ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية AND (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687064"
---
# <a name="and-er-function"></a>AND ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `AND` قيمة *منطقية* لـ **TRUE** إذا كانت جميع الشروط المُحددة صحيحة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.

## <a name="syntax"></a>بناء الجملة

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>الوسائط

`condition 1`: *منطقي*

تعبير شرطي صالح يجب اختباره. هذه الوسيطة مطلوبة.

`condition N`: *منطقي*

تعبير شرطي صالح يجب اختباره. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

في وسيطات الوظائف المنطقية، يُمكنك استخدام مراجع مصادر البيانات والقيم الرقمية والنصية والقيم المنطقية وعوامل تشغيل المقارنة ووظائف التقارير الإلكترونية (ER) الأخرى. ولكن، يجب تقييم كافة الوسيطات إلى قيمة *منطقية* **TRUE** أو **FALSE**.

## <a name="example"></a>مثال

يُرجع التعبير `AND (1=1, "a"="a")` **TRUE**.

يُرجع التعبير `AND (1=2, "a"="a")` **FALSE**.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]