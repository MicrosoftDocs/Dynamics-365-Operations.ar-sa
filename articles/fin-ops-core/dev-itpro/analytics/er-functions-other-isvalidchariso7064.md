---
title: ISVALIDCHARACTERISO7064 ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ISVALIDCHARACTERISO7064 (ER).
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
ms.openlocfilehash: 6f6f3326c9ca5cdcb3cef52f243d6d3da34251ce
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915914"
---
# <a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ISVALIDCHARACTERISO7064` قيمة *منطقية* **TRUE** إذا كانت السلسلة المُحددة تمثل رقم حساب مصرفي دولي (IBAN) صالحًا. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.

## <a name="syntax"></a>بناء الجملة

```
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة نصية تمثل رقم الـ IBAN.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` **TRUE**. 

يُرجع التعبير `ISVALIDCHARACTERISO7064 ("AT61")` **FALSE**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
