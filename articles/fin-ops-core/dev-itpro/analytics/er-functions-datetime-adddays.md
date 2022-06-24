---
title: وظيفة ADDDAYS ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية ADDDAYS‏ (ER).
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 7cf2031c042ae93512cc85afe6a1b51558f6c8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858730"
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