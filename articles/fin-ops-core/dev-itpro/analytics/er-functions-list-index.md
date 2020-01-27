---
title: INDEX ER الوظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INDEX (ER).
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
ms.openlocfilehash: a7fe2cbb5421da3c6dd1d044316b276836c5e5c1
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917294"
---
# <a name="INDEX">INDEX ER الوظيفة</a>

[!include [banner](../includes/banner.md)]

تقوم الوظيفة `INDEX` بإرجاع قيمة *الحاوية (سجل)* المُحددة باستخدام الفهرس الرقمي المُحدد في القائمة المُحددة. إذا كان هذا الفهرس خارج النطاق للسجلات في القائمة المُحددة، يتم طرح استثناء.

## <a name="syntax"></a>بناء الجملة

```
INDEX (list, index)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`index`: *عدد صحيح*

فهرس رقمي يشير إلى موضع السجل المطلوب في القائمة المُحددة.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="example-1"></a>مثال1

إذا أدخلت مصدر البيانات **DS** من النوع *حقل محتسب* ، يحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `DS.Value` القيمة النصية **"B"** للسجل الثاني من قائمة النص هذه. يُرجع التعبير `INDEX (SPLIT ("A|B|C", "|"), 2).Value` القيمة النصية **"B"** أيضًا.

## <a name="example-2"></a>مثال2

إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يطرح التعبير `INDEX (SPLIT ("A|B|C", "|"), 4).Value` استثناءً في وقت التشغيل.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
