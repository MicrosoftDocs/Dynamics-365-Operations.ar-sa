---
title: DAYS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DAYS (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682331"
---
# <a name="days-er-function"></a>DAYS ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `DAYS` قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني.

## <a name="syntax"></a>بناء الجملة

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>الوسائط

`date 1`: *التاريخ*

قيمة التاريخ التي تمثل تاريخ البدء لحساب عدد الأيام.

`date 2`: *التاريخ*

قيمة التاريخ التي تمثل تاريخ النهاية لحساب عدد الأيام.

## <a name="return-values"></a>إرجاع القيم

*عدد صحيح*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تُرجع الوظيفة `DAYS` قيمة موجبه عندما يكون التاريخ الأول لاحقًا للتاريخ الثاني ، وتُرجع **0** (صفر) عندما يساوي التاريخ الأول التاريخ الثاني، ويُرجع قيمة سالبة عندما يكون التاريخ الأول سابقًا للتاريخ الثاني.

## <a name="example"></a>مثال

يُرجع التعبير `DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` **-1**.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
