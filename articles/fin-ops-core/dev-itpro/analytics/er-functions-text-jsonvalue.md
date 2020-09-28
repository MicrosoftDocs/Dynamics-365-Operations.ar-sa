---
title: وظيفة JSONVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة JSONVALUE ER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 985a7e4f46756e595580d77ac904c883c305b04a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743797"
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

معرف نوع القيمة العددية لبيانات JSON.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يحتوي مصدر البيانات **JsonField** على البيانات التالية بتنسيق: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. في هذه الحالة، يقوم التعبير `JSONVALUE (JsonField, "BuildNumber")` بإرجاع القيمة التالية من نوع البيانات *سلسلة* : **"7.3.1234.1"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
