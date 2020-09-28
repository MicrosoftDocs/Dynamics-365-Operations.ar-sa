---
title: GETCURRENTCOMPANY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETCURRENTCOMPANY (ER).
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744108"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `GETCURRENTCOMPANY` قيمة *السلسلة* التي تمثل كود الكيان القانوني (الشركة) الذي يقوم مستخدم بتسجيل الدخول فيه حاليًا.

## <a name="syntax"></a>بناء الجملة

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `GETCURRENTCOMPANY ()` **USMF** لمستخدم سجل دخوله إلى شركة **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
