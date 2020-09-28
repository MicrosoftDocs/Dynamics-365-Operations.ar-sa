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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744301"
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
