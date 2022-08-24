---
title: TABLENAME2ID ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية TABLENAME2ID‏ (ER).
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: fe7ed336f2264e15e0a8a7305e1bcebb75b2cd07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268045"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `TABLENAME2ID` تمثيل رقمي لمُعرف الجدول لاسم الجدول المُحدد كقيمة *عدد صحيح*.

## <a name="syntax"></a>بناء الجملة

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية تمثل اسم جدول صالح.

## <a name="return-values"></a>إرجاع القيم

*عدد صحيح*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يُمكن أن ينتج عن تنفيذ هذه الوظيفة نتائج مختلفة في مثيلات مختلفة من 365‎ Finance Microsoft Dynamics ، حتى إذا تم استخدام نفس اسم الشركة.

## <a name="example"></a>مثال

يُرجع التعبير `TABLENAME2ID ("Intrastat")` **1510**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
