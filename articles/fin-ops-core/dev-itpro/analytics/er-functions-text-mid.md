---
title: MID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني MID (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744709"
---
# <a name="mid-er-function"></a>MID ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `MID` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من السلسلة المُحددة، بداية من الموضع المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمه *السلسلة* التي تحدد النص الذي سيتم إرجاع الأحرف منه.

`starting position`: *عدد صحيح*

قيمه *عدد صحيح* التي تحدد موضع الحرف الأول الذي يجب إرجاعه من النص المحدد.

`number of characters`: *عدد صحيح*

قيمه *عدد صحيح* التي تحدد عدد الأحرف التي يجب إرجاعها، بدءًا من موضع البداية المحدد.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا كانت قيمة الوسيطة `starting position` أقل من 0 (صفر)، يتم حساب الأحرف التي يتم إرجاعها من الموضع الأول في السلسلة المحددة.

إذا تجاوزت قيمة `starting position` الوسيطة طول السلسلة المحددة، يتم إرجاع سلسله فارغه.

## <a name="example"></a>مثال

تُرجع`MID ("Sample", 2, 3)` القيمة **"amp"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
