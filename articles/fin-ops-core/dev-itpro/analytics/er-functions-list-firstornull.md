---
title: FIRSTORNULL ER وظيفة
description: تشرح هذه المقالة كيفية استخدام وظيفة التقارير الإلكترونية FIRSTORNULL‏ (ER)
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: bae2916371cd00810f559ff2006b2b238c8ad918
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900240"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER وظيفة

[!include [banner](../includes/banner.md)]

تُعيد الوظيفة `FIRSTORNULL` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم يكن هذا السجل فارغًا. إذا كان السجل فارغًا، تُرجع هذه الوظيفة قيمة *حاوية (سجل)* فارغة.

## <a name="syntax"></a>بناء الجملة

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `FIRSTORNULL(SPLIT("",1)).Value` سلسلة فارغة (**""**).

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]