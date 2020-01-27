---
title: ROUND ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUND (ER).
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917064"
---
# <a name="ROUND">ROUND ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ROUND` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه إلى عدد المنازل العشرة المُحدد.

## <a name="syntax"></a>بناء الجملة

```
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

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)
