---
title: TABLENAME2ID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية TABLENAME2ID (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563260"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]