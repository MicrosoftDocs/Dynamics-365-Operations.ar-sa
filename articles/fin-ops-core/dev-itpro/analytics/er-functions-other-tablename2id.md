---
title: TABLENAME2ID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية TABLENAME2ID (ER).
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
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681148"
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

يُمكن أن ينتج عن تنفيذ هذه الوظيفة نتائج مختلفة في مثيلات مختلفة من  Microsoft Dynamics 365 Finance ، حتى إذا تم استخدام نفس اسم الشركة.

## <a name="example"></a>مثال

يُرجع التعبير `TABLENAME2ID ("Intrastat")` **1510**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
