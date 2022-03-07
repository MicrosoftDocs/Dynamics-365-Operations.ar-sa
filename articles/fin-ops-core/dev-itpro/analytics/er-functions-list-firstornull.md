---
title: FIRSTORNULL ER وظيفة
description: 'يشرح هذا الموضوع كيفية استخدام وظيفة التقارير الإلكترونية FIRSTORNULL (ER) '
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564615"
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