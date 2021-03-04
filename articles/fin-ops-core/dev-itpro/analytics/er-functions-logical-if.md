---
title: IF ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية IF (ER).
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
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686992"
---
# <a name="if-er-function"></a>IF ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `IF` القيمة المُحددة الأولى عند تحقق الشرط المُحدد. وإلا، تُرجع القيمة المحددة الثانية. يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.

## <a name="syntax"></a>بناء الجملة

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>الوسائط

`condition`: *منطقي*

تعبير شرطي صالح يجب اختباره.

`first value`: *أي من أنواع البيانات المعتمدة*

النتيجة التي يتم إرجاعها إذا تحقق الشرط.

`second value`: *أي من أنواع البيانات المعتمدة*

النتيجة التي يتم إرجاعها إذا لم يتحقق الشرط.

## <a name="return-values"></a>إرجاع القيم

*أي من أنواع البيانات المدعومة*

القيمة الناتجة لأي من أنواع البيانات المدعومة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يجب تحديد الوسيطات `first value` و `second value` باستخدام نفس نوع البيانات. يتم طرح استثناء في وقت التصميم إذا لم تتطابق أنواع بيانات القيم المكونة.

إذا كانت قيمة النتيجة الأولى وقيمة النتيجة الثانية هي قيم أنواع البيانات *الحاوية (السجل)* أو *قوائم السجلات* ، فإن النتيجة تحتوي فقط على الحقول الموجودة في كلا القيمتين.

## <a name="example"></a>مثال

يُرجع التعبير `IF (1=2, "condition is met", "condition is not met")` السلسلة **عدم تحقق الشرط**.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]