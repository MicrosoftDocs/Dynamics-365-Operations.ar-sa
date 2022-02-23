---
title: وظيفة NUMSEQVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMSEQVALUE (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b513d04bfeb3a37aa0b1703d0fdde040885a5159
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680580"
---
# <a name="numseqvalue-er-function"></a>وظيفة NUMSEQVALUE ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `NUMSEQVALUE` قيمة *سلسلة* تمثل القيمة الجديدة التي تم إنشاؤها للتسلسل الرقمي، استنادًا إلى التسلسل الرقمي المُحدد والنطاق ومُعرف النطاق. يساوي مُعرف النطاق كود الشركة الذي يتم توفيره بواسطة السياق الذي يتم تشغيل تنسيق إعداد التقارير الإلكترونية (ER) ضمنه.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>بناء الجملة 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>الوسائط

`number sequence code`: *السلسلة*

قيمة نصية تمثل كود التسلسل الرقمي المطلوب فيه قيمة جديدة.

`number sequence record ID`: *Int64*

قيمة *Int64* تُمثل مُعرف السجل لسجل في جدول NumberSequenceTable يحتوي على تعريف التسلسل الرقمي المطلوب فيه قيمة جديدة. 

`scope type`: *قيمة التعداد*

قيمة تعداد لتعداد **ERExpressionNumberSequenceScopeType** التي تعرف نطاق التسلسل الرقمي المطلوب فيه قيمة جديدة.  أنواع النطاقات المتاحة هي **مشتركة** و **كيان قانوني** و **شركة**.

`scope ID`: *السلسلة*

قيمة *السلسلة* التي تُعرف النطاق، استنادًا إلى نوع النطاق المُحدد.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

بالنسبة إلى نوع النطاق **المشترك**، حدد سلسلة فارغة كمعرف النطاق.

بالنسبة إلى نوعي النطاق **الشركة** و **الكيان القانوني** ، حدد كود الشركة كمعرف النطاق. إذا قمت بتحديد سلسلة فارغة كمُعرف نطاق لأنواع النطاقات هذه، يتم استخدام كود الشركة الحالي.

عند استخدام بناء الجملة 1، يتم طلب التسلسل الرقمي لنوع نطاق **الشركة** ، ويتم توفير رمز الشركة بواسطة السياق الذي يتم تشغيل تنسيق ER ضمنه.

## <a name="example-1"></a>مثال1

في تنسيق ER الخاص بك، يجب عليك تحديد مصدر بيانات **AskNumSeq** من النوع *مُعلمات إدخال المستخدم*. يشير مصدر البيانات هذا إلى نوع البيانات الموسعة (EDT) **الوصف**. بعد ذلك، يُمكن تعريف مصدر البيانات **NumSeq** من النوع *الحقل المحسوب*. يحتوي مصدر البيانات هذا على التعبير `NUMSEQVALUE (AskNumSeq)`. عندما يتم استدعاء مصدر البيانات **NumSeq** ، يُرجع القيمة الجديدة التي تم إنشاؤها من التسلسل الرقمي الذي تم تحديده في وقت التشغيل عن طريق إدخال الكود الخاص به في مربع الحوار. يتم طلب التسلسل الرقمي لنوع نطاق **الشركة**. يتم توفير كود الشركة بواسطة السياق الذي تم تشغيل تنسيق ER ضمنه.

## <a name="example-2"></a>مثال2

يتم تعريف مصادر البيانات التالية في تعيين النموذج الخاص بك:

- مصدر البيانات **LedgerParms** من النوع *الجدول*. يشير مصدر البيانات هذا إلى جدول LedgerParameters. 
- مصدر البيانات **NumSeq** من النوع *الحقل المحسوب*. يحتوي مصدر البيانات هذا على التعبير `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

يُرجع نوع مصدر البيانات **NumSeq**، عند استدعائه، القيمة الجديدة المُنشأة للتسلسل الرقمي الذي تم تكوينه في معلمات دفتر الأستاذ العام للشركة التي توفر السياق الذي يعمل ضمنه تنسيق التقارير الإلكترونية. يحدد هذا التسلسل الرقمي دفاتر اليومية بشكل فريد ويعمل كرقم دُفعة يربط الحركات ببعضها.

## <a name="example-3"></a>المثال الثالث

يتم تعريف مصادر البيانات التالية في تعيين النموذج الخاص بك:

- مصدر بيانات **enumScope** من النوع Dynamics 365 Finance Microsoft *تعداد*. يُشير مصدر البيانات هذا إلى تعداد **‎ERExpressionNumberSequenceScopeType**. 
- مصدر البيانات **NumSeq** من النوع *الحقل المحسوب*. يحتوي مصدر البيانات هذا على التعبير `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

يُرجع نوع مصدر البيانات **NumSeq**، عند استدعائه، القيمة الجديدة المُنشأة للتسلسل الرقمي **Gene\_1** الذي تم تكوينه للشركة التي توفر السياق الذي يعمل ضمنه تنسيق التقارير الإلكترونية.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
