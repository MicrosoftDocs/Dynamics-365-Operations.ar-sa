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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744541"
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

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات الحسابية](er-functions-category-mathematical.md)
