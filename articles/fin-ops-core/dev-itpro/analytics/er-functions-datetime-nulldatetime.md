---
title: NULLDATETIME ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NULLDATETIME (ER).
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917478"
---
# <a name="NULLDATETIME">NULLDATETIME ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تقوم وظيفة `NULLDATETIME` بإرجاع قيمة *DateTime* التي تظهر قيمة التاريخ/الوقت **الفارغة** (1 يناير 1900) بالتوقيت العالمي المتفق عليه (توقيت جرينتش المتوسط \[GMT\]).

## <a name="syntax"></a>بناء الجملة

```
NULLDATETIME ()
```

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="example"></a>مثال

تُرجع وظيفة `DATETIMEFORMAT( NULLDATETIME(), "O")` قيمة السلسلة **1900-01-01T00:00:00.0000000+00:00** عندما يتم استدعاءها أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‫التوقيت العالمي المتفق عليه (GMT)‬** في قسم **‏‫تفضيلات البلد/المنطقة واللغة‬**.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
