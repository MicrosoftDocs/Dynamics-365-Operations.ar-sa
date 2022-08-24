---
title: 'وظيفة COUNTIF ER '
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية COUNTIF‏ (ER).
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 61ac05d30845eae7c107c8a1edc66e4ff547c8a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274158"
---
# <a name="countif-er-function"></a>وظيفة COUNTIF ER 

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `COUNTIF` قيمة *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشرط المحدد. يتكون الشرط من نطاق المفتاح وقيمة المفتاح.

## <a name="syntax"></a>بناء الجملة

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>الوسائط

`condition range`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة لتعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER).

`condition value`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.

## <a name="return-values"></a>إرجاع القيم

*عدد صحيح*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يُمكن تكوين خصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.

تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.

في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.

في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.

## <a name="example"></a>مثال

لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تجميع البيانات](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
