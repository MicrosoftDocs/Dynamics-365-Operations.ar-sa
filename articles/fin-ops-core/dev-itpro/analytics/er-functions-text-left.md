---
title: وظيفة LEFT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة LEFT ER.
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
ms.openlocfilehash: 8280a05ea180d9de499d87efa53eca8ca912b0e3
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915638"
---
# <a name="LEFT">وظيفة LEFT ER</a>

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `LEFT` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة.

## <a name="syntax"></a>بناء الجملة

```
LEFT (text, number)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة *سلسلة* التي تمثل النص الأصلي.

`number`: *عدد صحيح*

عدد الأحرف التي يجب إرجاعها من بداية النص الأصلي.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

تُرجع `LEFT ("Sample", 3)` **"Sam"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
