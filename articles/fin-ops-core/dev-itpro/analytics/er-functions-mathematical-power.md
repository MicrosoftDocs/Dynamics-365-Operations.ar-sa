---
title: POWER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية POWER (ER).
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
ms.openlocfilehash: 6955d2787b2a9be6d38fe10165a9d5ef8310b108e3a9772709d9d1ff51712424
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767134"
---
# <a name="power-er-function"></a>POWER ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `POWER` قيمة *حقيقية* تمثل نتيجة رفع الرقم الموجب المحدد إلى الأس المحدد.‬ 

## <a name="syntax"></a>بناء الجملة

```vb
POWER (number, power)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد حقيقي* أو *صحيح*

قيمة رقمية يجب رفعها إلى الأس المُحدد.

`power`: *عدد حقيقي* أو *صحيح*

قيمة رقمية تمثل الأس المُحدد.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="example-1"></a>مثال1

يُرجع التعبير `POWER (10, 2)` **100**.

## <a name="example-2"></a>مثال2

يُرجع التعبير `POWER (4, 0.5)` **2**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]