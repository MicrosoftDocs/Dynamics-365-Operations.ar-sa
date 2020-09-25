---
title: NULLDATE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NULLDATE (ER).
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744277"
---
# <a name="nulldate-er-function"></a>NULLDATE ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `NULLDATE` قيمة *تاريخ* يمثل التاريخ **الفارغ** (1 يناير 1900).

## <a name="syntax"></a>بناء الجملة

```vb
NULLDATE () as 
```

## <a name="return-values"></a>إرجاع القيم

*التاريخ*

قيمة التاريخ الناتجة.

## <a name="example-1"></a>مثال1

تُرجع وظيفة `DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` التاريخ **الفارغ**،1 يناير 1900 كـ **"1900-01-01"**، بناءً على التنسيق المخصص المُحدد.

## <a name="example-2"></a>مثال2

يُرجع التعبير `IF( Invoice.DocumentDate = NULLDATE(), true, false)` **True** عندما تكون قيمة الحقل **DocumentDate** تساوي التاريخ **الفارغ**. في هذا المثال، **Invoice** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **سجلات المالية/الجدول** ، ويشير إلى جدول CustInvoiceJour.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
