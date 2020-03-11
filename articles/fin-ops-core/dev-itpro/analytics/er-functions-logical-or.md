---
title: OR ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية OR (ER).
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041666"
---
# <a name="OR">OR ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `OR` قيمة *منطقية* **FALSE** إذا كانت جميع الشروط المُحددة خطأ. إذا كانت أي من الشروط المُحددة صحيحة، تُرجع هذه الوظيفة قيمة *منطقية* **TRUE**.

## <a name="syntax"></a>بناء الجملة

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>الوسائط

`condition 1`: *منطقي*

تعبير شرطي صالح يجب اختباره. هذه الوسيطة مطلوبة.

`condition N`: *منطقي*

تعبير شرطي صالح يجب اختباره. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `OR (1=2, "a"="a")` **TRUE**.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)
