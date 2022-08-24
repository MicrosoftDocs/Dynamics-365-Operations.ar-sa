---
title: CH_BANK_MOD_10 ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية CH_BANK_MOD_10‏ (ER).
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f658228e0c181bab9e07237adc330dbcb13c95c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288081"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CH_BANK_MOD_10` قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD10، بناءً على أرقام رقم الفاتورة المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>الوسائط

`invoice number digits`: *السلسلة*

قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `CH_BANK_MOD_10 ("VEND-200002")` **3**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
