---
title: CASE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CASE (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916052"
---
# <a name="CASE">CASE ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تٌقيّم الوظيفة `CASE` قيمة التعبير المُحدد في مقابل الخيارات البديلة المُحددة، وترجع نتيجة الخيار الأول الذي يساوي قيمة التعبير المُحدد. وإلا، فإنه يقوم بإرجاع النتيجة الافتراضية الاختيارية، إذا كانت النتيجة الافتراضية مُحدد كآخر وسيطة للوظيفة التي تم استدعائها والتي لم يسبقها خيار. يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.

## <a name="syntax"></a>بناء الجملة

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>الوسائط

`expression`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)

تعبير صالح يقوم بإرجاع قيمة نوع البيانات الأساسية.

`option 1`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)

تعبير صالح يقوم بإرجاع قيمة نفس أنواع البيانات الأساسية مثل وسيطة `expression` للوظيفة التي تم استدعاؤها. هذه الوسيطة مطلوبة.

`result 1`: *أي من أنواع البيانات المعتمدة*

النتيجة التي تم إرجاعها التي تتوافق مع الخيار السابق. هذه الوسيطة مطلوبة.

`option N`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)

تعبير صالح يقوم بإرجاع قيمة نفس أنواع البيانات الأساسية مثل وسيطة `expression` للوظيفة التي تم استدعاؤها. هذه الوسيطة اختيارية.

`result N`: *أي من أنواع البيانات المعتمدة*

النتيجة التي تم إرجاعها التي تتوافق مع الخيار السابق. هذه الوسيطة اختيارية.

`default result`: *أي من أنواع البيانات المعتمدة*

النتيجة التي يجب إرجاعها في حالة عدم وجود تطابق. هذه الوسيطة اختيارية.

## <a name="return-values"></a>إرجاع القيم

*أي من أنواع البيانات المدعومة*

القيمة الناتجة لأي من أنواع البيانات المدعومة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يتم طرح استثناء في وقت التشغيل إذا لم يكن هناك تطابق ولم يتم تعريف نتيجة افتراضية اختيارية.

يجب تحديد كافة النتائج باستخدام نفس نوع البيانات. يتم طرح استثناء في وقت التصميم إذا لم تتطابق أنواع بيانات النتائج المكونة.

إذا كانت قيمة النتيجة الأولى وقيمة النتيجة *N* هي قيم أنواع البيانات *الحاوية (السجل)* أو *قوائم السجلات* ، فإن النتيجة تحتوي فقط على الحقول الموجودة في كلا القيمتين.

## <a name="example"></a>مثال

يُرجع التعبير `CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` السلسلة **"WINTER"** إذا كان تاريخ جلسة عمل التطبيق الحالية بين أكتوبر وديسمبر. وإلا، تقوم بإرجاع سلسلة فارغة.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)
