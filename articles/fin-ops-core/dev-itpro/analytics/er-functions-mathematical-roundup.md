---
title: ROUNDUP ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDUP‏ (ER).
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
ms.openlocfilehash: 5266b0f74f348d936bde8948770e48dbbf9bb4f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268015"
---
# <a name="roundup-er-function"></a>ROUNDUP ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ROUNDUP` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه لأعلى إلى عدد المنازل العشرة المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>الوسائط

`number`: *حقيقي*

قيمة رقمية يجب تقريبها لأعلى.

`decimals`: *عدد صحيح*

قيمة رقمية تمثل عدد المنازل العشرية.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تعمل هذه الدالة مثل الدالة [ROUND](er-functions-mathematical-round.md)، إلا أنها تقرّب دائمًا الرقم المحدد لأعلى (بعيدًا عن الصفر).

## <a name="example-1"></a>مثال1

تقرّب `ROUNDUP (1200.763, 2)` لأعلى إلى منزلتين عشريتين وترجع **1200.77**.

## <a name="example-2"></a>مثال2

تُقربّ `ROUNDUP (1200.767, -3)` لأعلى إلى أقرب مضاعف من 1,000 وترجع **2000**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
