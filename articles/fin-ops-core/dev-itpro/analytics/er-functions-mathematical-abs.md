---
title: ABS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ABS (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683271"
---
# <a name="abs-er-function"></a>ABS ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ABS` القيمة المُطلقة (للمعاملات) للرقم المُحدد كقيمة *حقيقة*. وبمعني آخر، يقوم بإرجاع الرقم دون إشارته.

## <a name="syntax"></a>بناء الجملة

```vb
ABS (number)
```

## <a name="arguments"></a>الوسائط

`number`: *حقيقي*

القيمة الرقمية التي تُريدها من المعاملات.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `ABS (-1)` **1**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]