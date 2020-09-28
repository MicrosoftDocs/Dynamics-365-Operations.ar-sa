---
title: 'وظيفة NUMBERVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERVALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743389"
---
# <a name="numbervalue-er-function"></a>وظيفة NUMBERVALUE ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `NUMBERVALUE` قيمة *حقيقية* يتم تحويلها من قيمة *السلسلة* المُحددة. في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية يجب تحويلها إلى رقم *حقيقي*.

`decimal separator`: السلسلة

فاصل عشري. يُستخدم لفصل العدد الصحيح والأجزاء الكسرية لرقم عشري.

`digit grouping separator`: *السلسلة*

فاصل تجميع أرقام. يُستخدم كفاصل آلاف.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `NUMBERVALUE( "1 234,56", ",", " ")` **1234.56**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تحويل النوع](er-functions-category-type-conversion.md)
