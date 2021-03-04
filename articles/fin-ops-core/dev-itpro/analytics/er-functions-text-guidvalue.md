---
title: وظيفة GUIDVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية GUIDVALUE.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685937"
---
# <a name="guidvalue-er-function"></a>وظيفة GUIDVALUE ER

[!include [banner](../includes/banner.md)]

تقوم وظيفة `GUIDVALUE` بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.

## <a name="syntax"></a>بناء الجملة

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

المسار الصالح لمصدر البيانات من نوع *السلسلة*.

## <a name="return-values"></a>إرجاع القيم

*GUID*

قيمه المعرف الفريد (GUID) الناتجة عالميًا.

## <a name="usage-notes"></a>ملاحظات الاستخدام

لإجراء تحويل في الاتجاه المعاكس (أي لتحويل المدخلات المحددة من نوع بيانات *GUID* إلى عنصر بيانات من نوع البيانات *سلسلة*)، يمكنك استخدام وظيفة [النص](er-functions-text-text.md) .

## <a name="example"></a>مثال

أنت تحدد مصادر البيانات التالية في تعيين نموذج:

- مصدر بيانات **myID** الخاص بنوع *الحقل المحسوب* الذي يحتوي على التعبير `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- مصدر بيانات **المستخدمين** من النوع *سجلات الجدول* الذي يُشير إلى جدول UserInfo.

يمكنك بعد ذلك استخدام تعبير مثل `FILTER (Users, Users.objectId = myID)` لتصفيه جدول معلومات المستخدم بواسطة الحقل **‎objectId‎** من نوع بيانات *GUID*.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]