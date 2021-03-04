---
title: ROUNDDOWN ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDDOWN (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686872"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ROUNDDOWN` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه لأسفل إلى عدد المنازل العشرة المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>الوسائط

`number`: *حقيقي*

قيمة رقمية يجب تقريبها لأسفل.

`decimals`: *عدد صحيح*

قيمة رقمية تمثل عدد المنازل العشرية.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تعمل هذه الدالة مثل الدالة [ROUND](er-functions-mathematical-round.md)، إلا أنها تقرّب دائمًا الرقم المحدد لأسفل (في اتجاه الصفر).

## <a name="example-1"></a>مثال1

تقرّب `ROUNDDOWN (1200.767, 2)` لأسفل إلى منزلتين عشريتين وترجع **1200.76**. 

## <a name="example-2"></a>مثال2

تُقربّ `ROUNDDOWN (1700.767, -3)` لأسفل إلى أقرب مضاعف من 1,000 وترجع **1000**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]