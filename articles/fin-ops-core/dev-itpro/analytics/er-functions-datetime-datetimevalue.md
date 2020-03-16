---
title: وظيفة DATETIMEVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETIMEVALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070680"
---
# <a name="DATETIMEVALUE">وظيفة DATETIMEVALUE ER</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `DATETIMEVALUE` قيمة *DateTime* التي تم تحويلها من قيمة نصية مُعينة في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت. (لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

النص الذي يمثل القيمة المراد تنسيقها.

`format`: *السلسلة*

تنسيق النص المُعين.

`culture`: *السلسلة*

الثقافة المستخدمة لتنسيق النص المُحدد.

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء. على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية. قيمة `culture` الافتراضية هي **EN-US**.

## <a name="example-1"></a>مثال1

يُرجع التعبير `DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` **2:55:00 ص في 21 ديسمبر 2016** ، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.

## <a name="example-2"></a>مثال2

يُرجع التعبير `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` **‬‏‫2:55:00 ص في 21 ديسمبر 2016** ، استنادًا إلى التنسيق المخصص والثقافة.

ومع ذلك، ستطرح `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` استثناءً لإعلام المستخدم بأنه لم يتم التعرف على السلسلة المحددة كقيمة تاريخ/وقت صالحة للثقافة المُحددة.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
