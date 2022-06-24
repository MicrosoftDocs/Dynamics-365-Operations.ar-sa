---
title: REPLACE ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية REPLACE‏ (ER).
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 6c2b1ba82d61a3c163f1d657035b66ace9f15c77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878360"
---
# <a name="replace-er-function"></a>REPLACE ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم وظيفة `REPLACE` بإرجاع السلسلة النصية المُحددة كقيمة *سلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى.

## <a name="syntax"></a>بناء الجملة

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

المسار الصالح لمصدر البيانات من نوع *السلسلة*.

`pattern`: *السلسلة*

إذا كانت الوسيطة `regular expression flag` **FALSE**، تحتوي هذه الوسيطة على النص الذي يجب استبداله.

إذا كانت الوسيطة `regular expression flag` **TRUE**، تحتوي هذه الوسيطة على تعبير عادي يُعرف كل من نمط البحث ونص الاستبدال.

`replacement`: *السلسلة*

إذا كانت الوسيطة `regular expression flag` **FALSE**، تحتوي هذه الوسيطة على النص لاستخدامه كبديل.

إذا كانت الوسيطة `regular expression flag` **TRUE**، لا يتم استخدام هذه الوسيطة.

`regular expression flag`: *منطقي*

قيمة *منطقية* تشير إلى إذا ما كان يتم استخدام تعبير عادي للقيام بالاستبدال.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا كانت الوسيطة `regular expression flag` **TRUE**، تقوم هذه الوظيفة بإرجاع السلسلة المُحددة بعد أن تم تغييرها عن طريق تطبيق التعبير العادي المُحدد بواسطة الوسيطة `pattern`. يتم استخدام التعبير العادي للبحث عن الأحرف التي يجب استبدالها.

إذا كانت الوسيطة `regular expression flag` بقيمة **FALSE**، ترجع هذه الدالة السلسلة المحددة بعد أن يتم استبدال مجموعة الأحرف التي تم تعريفها في الوسيطة `pattern` بأحرف من الوسيطة `replacement`. 

## <a name="example-1"></a>مثال1

تُطبق `REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` تعبيرًا عاديًا يقوم بإزالة كافة الرموز غير الرقيمة، ويُرجع **"19234564971"**.  

## <a name="example-2"></a>مثال2

يستبدل `REPLACE ("abcdef", "cd", "GH", false)` النمط **"cd"** بالسلسلة **"GH"** وترجع **"abGHef"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]