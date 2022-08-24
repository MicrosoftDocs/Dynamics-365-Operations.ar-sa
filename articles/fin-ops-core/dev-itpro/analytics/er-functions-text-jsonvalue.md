---
title: وظيفة JSONVALUE ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة JSONVALUE‏ (ER).
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267952"
---
# <a name="jsonvalue-er-function"></a>وظيفة JSONVALUE ER

[!include [banner](../includes/banner.md)]

تُحلل وظيفة `JSONVALUE` البيانات في تنسيق JavaScript Object Notation (JSON) الذي يتم الوصول إليه في المسار المُحدد، ويستخرج قيمة عددية تعتمد على المعرف المحدد.‬ ثم يقوم بإرجاع القيمة العددية المستخرجة كقيمة *سلسلة* .

## <a name="syntax"></a>بناء الجملة

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

المسار الصالح لمصدر البيانات من نوع *السلسلة* الذي يحتوي على بيانات JSON.

`path`: *السلسلة*

معرف نوع القيمة العددية لبيانات JSON. استخدم الشرطة المائلة للامام (/) لفصل أسماء عقد JSON المرتبطة. استخدم تعليق القوس ( \[\]) لتحديد فهرس قيمه معينه في صفيف JSON. لاحظ انه يتم استخدام الترقيم المستند إلى الصفر لهذا الفهرس.

## <a name="return-values"></a>إرجاع القيم

*سلسلة*

القيمة النصية الناتجة.

## <a name="example-1"></a>مثال1

يحتوي مصدر البيانات **JsonField** على البيانات التالية بتنسيق: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. في هذه الحالة، يقوم التعبير `JSONVALUE (JsonField, "BuildNumber")` بإرجاع القيمة التالية من نوع البيانات *سلسلة* : **"7.3.1234.1"**.

## <a name="example-2"></a>مثال2

يُمكنك إدخال مصدر بيانات **JsonField** من النوع *الحقل المحسوب* ، الذي يحتوي على التعبير `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`.

تم تكوين هذا التعبير لإرجاع قيمه [*سلسله*](er-formula-supported-data-types-primitive.md#string) تمثل البيانات التالية في تنسيق JSON.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

في هذه الحالة، يقوم التعبير `JSONVALUE(json, "workers/[1]/emails/[0]")` بإرجاع القيمة التالية من نوع البيانات *سلسلة*: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
