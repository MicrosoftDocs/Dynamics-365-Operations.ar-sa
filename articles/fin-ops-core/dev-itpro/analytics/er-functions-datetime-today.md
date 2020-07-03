---
title: TODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TODAY (ER).
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
ms.openlocfilehash: 94ef15d1971287e8bf13944bc8f693b567950031
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411427"
---
# <a name=""></a><a name="TODAY">TODAY ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `TODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة الخادم الحالي.

## <a name="syntax"></a>بناء الجملة

```xpp
TODAY ()
```

## <a name="return-values"></a>إرجاع القيم

*التاريخ*

قيمة التاريخ الناتجة.

## <a name="example"></a>مثال

تُرجع وظيفة `DATEFORMAT (TODAY (), "dd-MM-yyyy")` تاريخ خادم التطبيق الحالي، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد. 

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
