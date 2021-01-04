---
title: CONVERTCURRENCY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CONVERTCURRENCY (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686776"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CONVERTCURRENCY` قيمة *حقيقية* تمثيل نتيجة تحويل المبلغ المالي المحدد من العملة المصدر المحددة إلى العملة الهدف المحددة باستخدام إعدادات الشركة المُحددة في التاريخ المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>الوسائط

`amount`: *عدد صحيح* أو *حقيقي*

قيمة رقمية تمثل المبلغ النقدي الذي يجب تحويله.

`source currency`: *السلسلة*

كود عملة المصدر.

`target currency`: *السلسلة*

كود العملة الهدف.

`date`: *التاريخ*

قيمة *التاريخ* التي تمثل التاريخ المستخدم لتحديد سعر الصرف للتحويل.

`company`: *السلسلة*

قيمة *السلسلة* التي تمثل كود الشركة التي توفر الإعدادات المستخدمة للتحويل.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="example"></a>مثال

تُرجع `CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` مكافئ اليورو الواحد بالدولار الأمريكي بتاريخ الجلسة الحالية، استنادًا إلى إعدادات شركة **DEMF**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
