---
title: FA_BALANCE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FA_BALANCE (ER).
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041436"
---
# <a name="FA_BALANCE">FA_BALANCE ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `FA_BALANCE` قيمة *حاوية (سجل)* تتكون من بيانات لرصيد الأصل الثابت لعنصر الأصل الثابت المُحدد وكود نموذج القيمة وسنة إعداد التقرير وتاريخ إعداد التقرير.

## <a name="syntax"></a>بناء الجملة

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>الوسائط

`fixed asset code`: *السلسلة*

قيمة *السلسلة* التي تمثل كود الأصل الثابت الذي يتم حساب الرصيد له.

`value model code`: *السلسلة*

قيمة *السلسلة* التي تمثل كود نموذج القيمة الذي يتم حساب الرصيد له.

`reporting year`: *قيمة التعداد*

قيمة التعداد لتعداد تطبيق **AssetYear** التي تُعرف فترة لحساب الرصيد.

`reporting date`: *التاريخ*

قيمة *التاريخ* التي تعرف تاريخ لحساب الرصيد.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` حاوية بيانات الأرصدة المعدة للأصل الثابت **COMP-000001** الذي لديه نموذج القيمة **الحالية** في تاريخ جلسة عمل التطبيق الحالية.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
