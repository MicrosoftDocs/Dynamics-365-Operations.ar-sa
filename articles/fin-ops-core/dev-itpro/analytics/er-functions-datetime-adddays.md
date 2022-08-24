---
title: وظيفة ADDDAYS ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية ADDDAYS‏ (ER).
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274128"
---
# <a name="adddays-er-function"></a>وظيفة ADDDAYS ER

[!include [banner](../includes/banner.md)]

تحسب وظيفة `ADDDAYS` قيمة *DateTime* والتي هي عدد الأيام المُحددة قبل أو بعد تاريخ البدء المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>الوسائط

`datetime`: *DateTime*

قيمة الوقت/التاريخ التي تمثل تاريخ البدء.

`days`: *عدد صحيح*

عدد الأيام قبل أو بعد `datetime`.

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

قيمة موجبة لـ `days` تُعطي تاريخ مستقبلي. قيمة سالبة تعطي تاريخًا سابقًا.

## <a name="example-1"></a>مثال1

يُرجع التعبير `ADDDAYS (NOW(), 7)` التاريخ والوقت سبعة أيام في المستقبل.

## <a name="example-2"></a>مثال2

يُرجع التعبير `ADDDAYS (NOW(), -3)` التاريخ والوقت ثلاثة أيام في الماضي.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
