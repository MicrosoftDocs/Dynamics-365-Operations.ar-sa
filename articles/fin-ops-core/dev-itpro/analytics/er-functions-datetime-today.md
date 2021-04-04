---
title: TODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TODAY (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 9288baf4e6123a7c03152f524a852eae9b671dde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567906"
---
# <a name="today-er-function"></a>TODAY ER وظيفة

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]