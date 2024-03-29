---
title: الدالة LISTJOIN ER
description: توفر هذه المقالة معلومات عن كيفية استخدام دالة إعداد التقارير الإلكترونية LISTJOIN.
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ec8a5985277de8036ec8ad51b947a8bab098a1c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291193"
---
# <a name="listjoin-er-function"></a>الدالة LISTJOIN ER

[!include [banner](../includes/banner.md)]

تُرجع الدالة `LISTJOIN` قيمة *قائمة السجلات* التي تمثل قائمة منضمة جديدة تم إنشاءها من الوسيطات المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>الوسائط

`list 1`: *قائمة السجلات*

مرجع إلى مصدر البيانات من نوع بيانات *قائمة سجلات*. هذه الوسيطة إلزامية.

`list N`: *قائمة السجلات*

مرجع إلى مصدر البيانات من نوع بيانات *قائمة سجلات*. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تحتوي بنية القائمة التي تم إنشائها فقط على الحقول الموجودة في بنية كل قائمة سجلات مشار إليها في الوسيطات.

## <a name="example"></a>مثال

أدخل مصدر البيانات **السجل 1** من النوع `Container`. يحتوي مصدر البيانات هذا على الحقول المتداخلة التالية من النوع `Calculated field`:

- **الرمز**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `String`.
- **المبلغ**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Real`.

بعد ذلك، أدخل مصدر البيانات **السجل 2** من النوع `Container`. يحتوي مصدر البيانات هذا على الحقول المتداخلة التالية من النوع `Calculated field`:

- **المبلغ**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Real`.
- **‎IsValid**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Boolean`.

![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية.](./media/er-functions-list-listjoin-image1.gif)

في هذه الحالة، يُرجع التعبير `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` قائمة جديدة تحتوي على سجلين.

![صفحة مصمم تعيين نموذج التقارير الإلكترونية مع سجلين.](./media/er-functions-list-listjoin-image2.gif)

تتكون بنية هذه القائمة من حقل **مبلغ** واحد من النوع `Real`، لأن هذا الحقل هو الحقل الوحيد الذي يتم تقديمه في كل وسطية من الوظيفة المستدعاة.

![حقل المبلغ في صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)

[تصحيح مصادر البيانات لتنسيق ER الذي تم تنفيذه لتحليل تدفق البيانات وتحويلها](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
