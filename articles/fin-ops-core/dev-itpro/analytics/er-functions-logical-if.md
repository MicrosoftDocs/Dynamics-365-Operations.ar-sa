---
title: IF ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية IF‏ (ER).
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
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
ms.openlocfilehash: 066cffaebc415305a2481e3bf0f0a5f4e108fabc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844547"
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