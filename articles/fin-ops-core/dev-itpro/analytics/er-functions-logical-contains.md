---
title: وظيفة التقرير الإلكترونية CONTAINS
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية CONTAINS‏ (ER).
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273117"
---
# <a name="contains-er-function"></a>وظيفة التقرير الإلكترونية CONTAINS

[!include [banner](../includes/banner.md)]

تحدد وظيفة `CONTAINS` ما إذا كان الإدخال المحدد يحتوي على النص المحدد أم لا. تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كان الإدخال المحدد يحتوي على النص المحدد. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.

## <a name="syntax"></a>بناء الجملة

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

المسار الصالح لعنصر مصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تحتوي قيمته على الوسيطة الثانية.

`search text`: *السلسلة*

المسار الصالح لمصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تكون قيمته متضمنة في الوسيطة الأولى.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يمكن استخدام هذه الوظيفة لتحديد تعبير شرط لوظيفة [FILTER](er-functions-list-filter.md) فقط عند تكوين التعيين المرتبط في [ Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)للوصول إلى [Microsoft Dataverse](/power-platform/admin/data-integrator). خلاف ذلك، يتم إلقاء استثناء في وقت التصميم. توصي الرسالة التي تستلمها باستخدام وظيفة التصفية [WHERE](er-functions-list-where.md) بدلا من وظيفة `FILTER`.

## <a name="example-1"></a>مثال1

يقوم التعبير `CONTAINS ("abc", "d")` بإرجاع **FALSE**، بينما يقوم التعبير `CONTAINS ("abc", "C")` بإرجاع **TRUE**.

## <a name="example-2"></a>مثال2

يقوم التعبير `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` بإرجاع **TRUE** إذا كانت قيمة حقل **العنوان** في مصدر بيانات **النموذج** يحتوي على السلسلة **DEU**. وإلا، يتم إرجاع **FALSE**.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)
