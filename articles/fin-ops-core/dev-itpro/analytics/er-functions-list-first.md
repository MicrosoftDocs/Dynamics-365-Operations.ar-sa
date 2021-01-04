---
title: FIRST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FIRST (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679404"
---
# <a name="first-er-function"></a>FIRST ER وظيفة

[!include [banner](../includes/banner.md)]

تُعيد الوظيفة `FIRST` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم تكن هذه القائمة فارغة. إذا كانت القائمة فارغة، تطرح هذه الوظيفة استثناء.

## <a name="syntax"></a>بناء الجملة

```vb
FIRST (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="example-1"></a>مثال1

يُرجع التعبير `FIRST(SPLIT("ABC",1)).Value` القيمة النصية **"A"**.

## <a name="example-2"></a>مثال2

يطرح التعبير `FIRST(SPLIT("",1)).Value` استثناءًا في وقت التشغيل.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
