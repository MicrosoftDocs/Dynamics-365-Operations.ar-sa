---
title: CHAR ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CHAR (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915730"
---
# <a name="CHAR">CHAR ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CHAR` قيمة *السلسلة* التي توضح حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.

## <a name="syntax"></a>بناء الجملة

```
CHAR (number)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد صحيح*

رقم يتوافق مع حرف مفرد متوقع.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تتوقف السلسلة التي تُرجعها هذه وظيفة على الترميز المحدد في عنصر تنسيق **FILE** الأصلي. للحصول على قائمة بالرموز المدعومة، راجع [فئة الترميز](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>مثال

تُرجع `CHAR (255)` **"ÿ"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
