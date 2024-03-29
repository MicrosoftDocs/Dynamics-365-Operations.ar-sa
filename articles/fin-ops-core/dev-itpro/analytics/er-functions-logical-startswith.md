---
title: وظيفة التقارير الإلكترونية STARTSWITH
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية STARTSWITH.
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
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287207"
---
# <a name="startswith-er-function"></a>وظيفة التقارير الإلكترونية STARTSWITH

[!include [banner](../includes/banner.md)]

تحدد وظيفة `STARTSWITH` ما إذا كانت الإدخال المحدد يبدأ بالنص المحدد أم لا. تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كانت المدخلات المحددة تبدأ بالنص المحدد. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.

## <a name="syntax"></a>بناء الجملة

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

المسار الصالح لعنصر مصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تبدأ قيمته بالوسيطة الثانية.

`start text`: *السلسلة*

المسار الصالح لمصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تكون قيمته في بداية الوسيطة الأولى.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يمكن استخدام هذه الوظيفة لتحديد تعبير شرط لوظيفة [FILTER](er-functions-list-filter.md) فقط عند تكوين التعيين المرتبط في [ Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)للوصول إلى [Microsoft Dataverse](/power-platform/admin/data-integrator). خلاف ذلك، يتم إلقاء استثناء في وقت التصميم. توصي الرسالة التي تستلمها باستخدام وظيفة التصفية [WHERE](er-functions-list-where.md) بدلا من وظيفة `FILTER`.

## <a name="example-1"></a>مثال1

يقوم التعبير `STARTSWITH ("abc", "d")` بإرجاع **FALSE**، بينما يقوم التعبير `STARTSWITH ("abc", "A")` بإرجاع **TRUE**.

## <a name="example-2"></a>مثال2

يقوم التعبير `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` بإرجاع **TRUE** إذا كانت قيمة حقل **العنوان** في مصدر بيانات **النموذج** تبدأ بالسلسلة **123 شارع القهوة**. وإلا، يتم إرجاع **FALSE**.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)
