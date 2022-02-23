---
title: NOW ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NOW (ER).
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
ms.openlocfilehash: 0c3cfefd36db44608f05225746704aa3fbe4fc2c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682355"
---
# <a name="now-er-function"></a>NOW ER وظيفة

[!include [banner](../includes/banner.md)]

ُتُرجع وظيفة `NOW` قيمة *DateTime* التي تمثل تاريخ خادم التطبيق الحالي والتوقيت.

## <a name="syntax"></a>بناء الجملة

```vb
NOW ()
```

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` قيمة تاريخ/وقت خادم التطبيق الحالي، 24 ديسمبر 2015، كـ **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
