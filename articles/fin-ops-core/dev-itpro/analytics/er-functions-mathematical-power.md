---
title: POWER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية POWER (ER).
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
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683319"
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