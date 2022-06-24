---
title: CONVERTCURRENCY ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية CONVERTCURRENCY‏ (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: e51086d977652e4be4c19390a824d4f4507b60d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898451"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]