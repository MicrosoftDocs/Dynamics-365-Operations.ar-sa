---
title: وظيفة SUMIF ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية SUMIF‏ (ER).
author: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 66f8f60714f403c9e4ce5c798f08d9566a3e334d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285324"
---
# <a name="sumif-er-function"></a>وظيفة SUMIF ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `SUMIF` قيمة *حقيقية* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشرط المحدد. يتكون الشرط من نطاق المفتاح وقيمة المفتاح.

## <a name="syntax"></a>بناء الجملة

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>الوسائط

`key name for summing`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER) الذي يجب استخدام قيمة الربط لأغراض التجميع.

يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.

في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.

في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.

## <a name="example"></a>مثال

لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.

لمزيد من المعلومات والأمثلة حول استخدام هذه الوظيفة، راجع [تأجيل تنفيذ عناصر التسلسل في تنسيقات إعداد التقارير الإلكترونية](er-defer-sequence-element.md#Example) و [‏‫تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية‬](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تجميع البيانات](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
