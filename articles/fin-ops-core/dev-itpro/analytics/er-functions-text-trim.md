---
title: TRIM ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية TRIM‏ (ER).
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273087"
---
# <a name="trim-er-function"></a>TRIM ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم وظيفة `TRIM` بإرجاع السلسلة النصية المحددة كقيمة *سلسلة* بعد علامة التبويب، ونقل الإرجاع، وتغذية البنود، وأحرف تغذية النموذج بحرف مسافة واحد، بعد قطع المسافات البادئة واللاحقة، وبعد إزالة المسافات المتعددة بين الكلمات.

## <a name="syntax"></a>بناء الجملة

```vb
TRIM (text)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

المسار الصالح لمصدر البيانات من نوع *السلسلة*.

## <a name="return-values"></a>إرجاع القيم

*سلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

في بعض الحالات، قد ترغب في اقتطاع المسافات البادئة والزائدة ولكنك تفضل الاحتفاظ بالتنسيق للنص المحدد. على سبيل المثال، عندما يمثل هذا النص عنوانًا يمكن إدخاله في مربع نص متعدد الأسطر ويمكن أن يحتوي على تغذية سطر وتنسيق إرجاع أول السطر. في هذه الحالة، استخدم التعبير التالي: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`حيث `text` هي الوسيطة التي تشير إلى سلسلة النص المحددة.

## <a name="example-1"></a>مثال1

تُرجع `TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` **"نصًا نموذجيًا"**.

## <a name="example-2"></a>مثال2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` يقوم بإرجاع **"نموذج نص"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)

[REPLACE ER وظيفة](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
