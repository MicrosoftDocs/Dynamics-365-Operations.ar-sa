---
title: ROUND ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUND‏ (ER).
author: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 57d41ed92a5577fdc5fffeccef2834e9b6fb5197
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286048"
---
# <a name="round-er-function"></a>ROUND ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ROUND` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه إلى عدد المنازل العشرة المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>الوسائط

`number`: *حقيقي*

قيمة رقمية يجب تقريبها.

`decimals`: *عدد صحيح*

قيمة رقمية تمثل عدد المنازل العشرية.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا كانت قيمة وسيطة `decimals` أكبر من 0 (صفر)، فيتم تقريب الرقم المحدد إلى عدد المنازل العشرية العديدة.

إذا كانت قيمة الوسيطة `decimals` المحددة تساوي **0** (صفر) فيتم تقريب الرقم المحدد إلى أقرب عدد صحيح.

إذا كانت قيمة وسيطة `decimals` المحددة أقل من 0 (صفر)، فيتم تقريب الرقم المحدد إلى يسار الفاصلة العشرية.

## <a name="example-1"></a>مثال1

تقرّب `ROUND (1200.767, 2)` إلى منزلتين عشريتين وترجع **1200.77**.

## <a name="example-2"></a>مثال2

تُقربّ `ROUND (1200.767, -3)` إلى أقرب مضاعف من 1,000 وترجع **1000**.

## <a name="example-3"></a>المثال الثالث

يقوم `ROUND (1200.5, 0)` بالتقريب إلى أقرب عدد صحيح وإرجاع **1200**، بينما يقوم `ROUND (1201.5, 0)` بنفس الإعداد وإرجاع **1202**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
