---
title: 'وظيفة CONCATENATE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CONCATENATE (ER)
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569595"
---
# <a name="concatenate-er-function"></a>وظيفة CONCATENATE ER 

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CONCATENATE` جميع السلاسل النصية المُحددة كقيمة *سلسلة* بعد انضمامها في سلسلة واحدة.

## <a name="syntax"></a>بناء الجملة

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>الوسائط

`text 1`: *السلسلة*

مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*. هذه الوسيطة مطلوبة.

`text N`: *السلسلة*

مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `CONCATENATE ("abc", "def")` **"abcdef"**.

## <a name="usage-notes"></a>ملاحظات الاستخدام

كما يُرجع التعبير `"abc" & "def"` **"abcdef"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]