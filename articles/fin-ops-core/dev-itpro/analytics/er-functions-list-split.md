---
title: SPLIT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLIT (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 31caf7c728a92d31428f47320c074fa9fc35bda6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916098"
---
# <a name="SPLIT">SPLIT ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تقسم الوظيفة `SPLIT` سلسلة الإدخال المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة.

## <a name="syntax-1"></a>بناء الجملة 1

```
SPLIT (input, length)
```

يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، لكل منها الطول المحدد.

## <a name="syntax-2"></a>بناء الجملة 2

```
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
