---
title: 'وظيفة COLLECTEDLIST ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني COLLECTEDLIST (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 85258ae0a8d8a9720133a294f88ad84e1678532a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743653"
---
# <a name="collectedlist-er-function"></a>وظيفة COLLECTEDLIST ER 

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `COLLECTEDLIST` قيمة *قائمة السجل* التي تحتوي على قائمة القيم التي تم ارجاعها بواسطة خاصية **قيمة مفتاح البيانات التي تم جمعها** من عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء تشغيل مستند صادر أثناء التنسيق، والذي يفي بالشروط المحددة. يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.

## <a name="syntax"></a>بناء الجملة

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>الوسائط

`condition 1 range`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة لتعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER). هذه الوسيطة إلزامية.

`condition 1 value`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER. هذه الوسيطة إلزامية.

`condition N range`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق ER. هذه الوسائط الإضافية اختيارية.

`condition N value`: *السلسلة*

القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يُمكن تكوين خصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.

تُرجع هذه الوظيفة قائمة فارغة عندما يكون خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع** متوقف عن التشغيل.

في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.

في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.

## <a name="example"></a>مثال

لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تجميع البيانات](er-functions-category-data-collection.md)
