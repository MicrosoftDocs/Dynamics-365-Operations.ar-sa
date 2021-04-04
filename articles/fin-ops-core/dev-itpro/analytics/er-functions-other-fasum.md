---
title: FA_SUM ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FA_SUM (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567558"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `FA_SUM` قيمة *حاوية (سجل)* تتكون من بيانات لمبالغ الأصول الثابتة لعنصر الأصل الثابت المُحدد وكود نموذج القيمة والفترات المرتبطة بالتواريخ.

## <a name="syntax"></a>بناء الجملة

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>الوسائط

`fixed asset code`: *السلسلة*

قيمة *السلسلة* التي تمثل كود الأصل الثابت الذي يتم حساب الرصيد له.

`value model code`: *السلسلة*

قيمة *السلسلة* التي تمثل كود نموذج القيمة الذي يتم حساب الرصيد له.

`start date`: *التاريخ*

قيمة *التاريخ* التي تمثل تاريخ بدء الفترة التي تم حساب مبالغ الأصول الثابتة لها.

`end date`: *التاريخ*

قيمة *التاريخ* التي تمثل تاريخ نهاية الفترة التي تم حساب مبالغ الأصول الثابتة لها.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `FA_SUM ("COMP-000001", "Current", Date1, Date2)` حاوية بيانات الأصل الثابت **COMP-000001** التي تم إعدادها لنموذج القيمة **الحالية** ولمدة من **Date1** إلى **Date2**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]