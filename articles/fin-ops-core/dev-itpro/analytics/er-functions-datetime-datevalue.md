---
title: 'وظيفة DATEVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEVALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ef617ebfcaeb75e0284ea3cb4e889a204120b3d3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042356"
---
# <a name="DATEVALUE">وظيفة DATEVALUE ER</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `DATEVALUE` قيمة *التاريخ* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري إلى قيمة التاريخ. (لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>بناء الجملة 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

النص الذي يمثل القيمة المراد تنسيقها.

`format`: *السلسلة*

تنسيق النص المُعين.

`culture`: *السلسلة*

الثقافة المستخدمة لتنسيق النص المُحدد.

## <a name="return-values"></a>إرجاع القيم

*التاريخ*

قيمة التاريخ الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء. على سبيل المثال، إذا تم استدعاء الوظيفة `DATEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية. قيمة `culture` الافتراضية هي **EN-US**.

## <a name="example-1"></a>مثال1

يُرجع التعبير `DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` قيمة التاريخ **21 ديسمبر 2016**، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.

## <a name="example-2"></a>مثال2

يُرجع التعبير `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` قيمة التاريخ **21 يناير 2016** ، استنادًا إلى التنسيق المخصص المُحدد والثقافة.

ولكن، سوف يطرح `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` استثناءً لإبلاغ المستخدم أنه لم يتم التعرف على السلسلة المُحددة كقيمة صالحة للثقافة المُحددة.

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
