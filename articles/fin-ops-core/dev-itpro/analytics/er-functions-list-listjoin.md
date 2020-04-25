---
title: الدالة LISTJOIN ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام دالة إعداد التقارير الإلكترونية LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249025"
---
# <a name=""></a><a name="LISTJOIN">الدالة LISTJOIN ER</a>

[!include [banner](../includes/banner.md)]

تُرجع الدالة `LISTJOIN` قيمة *قائمة السجلات* التي تمثل قائمة منضمة جديدة تم إنشاءها من الوسيطات المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
LIST (list 1 [, list 2, …, list N])
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

في هذه الحالة، يُرجع التعبير `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` قائمة جديدة تحتوي على سجلين. تتكون بنية هذه القائمة من حقل **مبلغ** واحد من النوع `Real`، لأن هذا الحقل هو الحقل الوحيد الذي يتم تقديمه في كل وسطية من الوظيفة المستدعاة.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
