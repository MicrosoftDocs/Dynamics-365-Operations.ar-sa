---
title: CN_GBT_ADDITIONALDIMENSIONID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CN_GBT_ADDITIONALDIMENSIONID (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744421"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER وظيفة

[!include [banner](../includes/banner.md)]

تقوم الوظيفة `CN_GBT_ADDITIONALDIMENSIONID` بإرجاع قيمة *سلسلة* تمثل مُعرف بعد مالي واحد مأخوذ من السلسلة المُحددة. تعرض السلسلة المُحددة كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.

## <a name="syntax"></a>بناء الجملة

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة *سلسلة*تمثل كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.

`number`: عدد صحيح

قيمة *عدد صحيح* تُحدد كود التسلسل للبعد المُطلوب في السلسلة المُحددة.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

تُرجع `CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` **"CC"**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
