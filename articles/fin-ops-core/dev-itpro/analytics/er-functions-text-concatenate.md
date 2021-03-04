---
title: 'وظيفة CONCATENATE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CONCATENATE (ER)
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
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687928"
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