---
title: SPLIT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLIT (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 806a0995f0c138f4e80396bb993bc6f41bc7c827
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567332"
---
# <a name="split-er-function"></a>SPLIT ER وظيفة

[!include [banner](../includes/banner.md)]

تقسم الوظيفة `SPLIT` سلسلة الإدخال المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
SPLIT (input, length)
```

يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، لكل منها الطول المحدد.

## <a name="syntax-2"></a>بناء الجملة 2

```vb
SPLIT (input, delimiter)
```

يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، استنادًا إلى المحدد المعين.

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

النص المراد تقسيمه.

`length`: *عدد صحيح*

الحد الأقصى لطول سلسلة فرعية واحدة.

`delimiter`: *السلسلة*

مُحدد يستخدم لفصل السلاسل الفرعية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تتكون بنية سجل القائمة التي تم إرجاعها من حقل **القيمة** من نوع *السلسلة*. يحتوي كل سجل من القائمة التي تم إرجاعها على سلاسل فرعية تم إنشاؤها في هذا الحقل.

إذا كانت وسيطة `delimiter` فارغة، تتكون القائمة الجديدة التي تم إرجاعها من سجل واحد يحتوي على الحقل **القيمة** من نوع *السلسلة*. يحتوي هذا الحقل علي نص الإدخال.

إذا كانت الوسيطة `input` فارغة، يتم إرجاع قائمة فارغة جديدة. إذا لم يتم تعيين الوسيطة `input` أو `delimiter` (null)، يتم طرح استثناء تطبيق.

## <a name="example-1"></a>مثال1

يُرجع التعبير `SPLIT ("abcd", 3)` قائمة جديدة تتكون من سجلين لديهما حقل **القيمة** من نوع *السلسلة*. يحتوي حقل **القيمة** في السجل الأول على النص **"abc"** ، ويحتوي حقل **القيمة** في السجل الثاني على النص **"d"**.

## <a name="example-2"></a>مثال2

يُرجع التعبير `SPLIT ("XAb aBy", "aB")` قائمة جديدة تتكون من ثلاث سجلات لديهم حقل **القيمة** من نوع *السلسلة*. يحتوي حقل **القيمة** في السجل الأول على النص **"X"** ، ويحتوي حقل **القيمة** في السجل الثاني على النص **&nbsp;** ، ويحتوي حقل **القيمة** في السجل الثالث على النص **"y"**. 

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]