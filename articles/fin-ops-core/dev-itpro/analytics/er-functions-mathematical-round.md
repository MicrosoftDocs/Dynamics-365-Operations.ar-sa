---
title: ROUND ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUND (ER).
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683246"
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