---
title: ISOCREDREF ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ISOCREDREF (ER).
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
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680676"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ISOCREDREF` قيمة *سلسلة* تمثل مرجع دائن المنطقة العالمية للمواصفات (ISO)، استنادًا إلى الخامات الرقمية والرموز الأبجدية في رقم الفاتورة المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>الوسائط

`invoice number digits`: *السلسلة*

قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

> [!NOTE] 
> لإزالة الرموز من الحروف الأبجدية غير المتوافقة مع ISO، يجب ترجمة الوسيطة `invoice number digits` قبل أن يتم تمريرها إلى هذه الوظيفة.

## <a name="example"></a>مثال

يُرجع التعبير `ISOCredRef ("VEND-200002")` **"RF23VEND-200002"**. 

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
