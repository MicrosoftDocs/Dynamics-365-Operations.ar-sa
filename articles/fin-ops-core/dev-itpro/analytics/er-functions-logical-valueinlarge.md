---
title: 'وظيفة VALUEINLARGE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية VALUEINLARGE (ER).
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705133"
---
# <a name="valueinlarge-er-function"></a>وظيفة VALUEINLARGE ER 

[!include [banner](../includes/banner.md)]

تُحدد وظيفة `VALUEINLARGE` ما إذا كان الإدخال المُحدد من النوع *Int64* أو *عدد صحيح* يطابق أي قيمة عنصر مُحدد في القائمة المُحددة. تقوم الوظيفة بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. لفهم المختلف في الوظيفة `VALUEIN` ، راجع قسم [ملاحظة الاستخدام](#usage_note) لاحقًا في هذا الموضوع.

## <a name="syntax"></a>بناء الجملة

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>الوسائط

`input`: *الحقل*

مسار صالح لصنف مصدر بيانات من نوع *قائمة السجلات*. وستتم مطابقة قيمة هذا الصنف.

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`list item expression`: *التعبير*

تعبير شرطي صالح يشير إما إلى أو يحتوي على حقل واحد من القائمة المحددة يجب استخدامه للمطابقة.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name=""></a><a name="usage_note">ملاحظات الاستخدام</a>

عندما يمثل الإدخال المُحدد نوع *Int64* أو *عدد صحيح* لصنف مصدر البيانات، فمن ثم يكون الاستدعاء لها قابلًا للترجمة إلى عبارة SQL مباشرة، يتم تحويل القائمة المُحددة إلى جدول SQL مؤقت ويتم إجراء مطابقة في قاعدة البيانات من خلال تنفيذ استعلام `EXISTS JOIN` واحد. وبخلاف ذلك، تعمل هذه الوظيفة كوظيفة [`VALUEIN`](er-functions-logical-valuein.md).

عندما يمثل الإدخال المُحدد صنف مصدر بيانات تم تصمميه كأحد الأصناف بخلاف النوع *Int64* و *عدد صحيح*، يحدث خطأ في وقت التصميم يُخبرك بأن وظيفة `VALUEINLARGE` غير منطبقة لتعبير ER الذي تم تكوينه.

عندما يتم تنفيذ تعبير الوظيفة `VALUEINLARGE` واستخدام أكثر من جدول مؤقت في نطاق هذا التنفيذ، يحدث خطأ في وقت التشغيل.

## <a name="example"></a>مثال

أنت تحدد مصادر البيانات التالية في تعيين نموذج:

- مصدر البيانات **In** من النوع *سجلات الجدول*.
    - يشير مصدر البيانات هذا إلى جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. 
    - يتم تعيين الخيار **عبر الشركة** إلى **لا**.
- مصدر البيانات **InMemory** من النوع *الحقل المحسوب*.
    - يحتوي مصدر البيانات هذا على التعبير `WHERE (In, In.Port <> "")`.
- مصدر البيانات **InFiltered** من النوع *الحقل المحسوب*.
    - يحتوي مصدر البيانات هذا على التعبير `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

عندما يتم استدعاء مصدر البيانات **InFiltered** ضمن سياق الشركة **DEMF**، يتم إنشاء جدول مؤقت جديد في قاعدة بيانات التطبيق، ويتم إدراج ما تم تجميعه في قائمة ذاكرة رموز تعريف السجل في هذا الجدول، ويتم إنشاء عبارة SQL التالية لإرجاع السجلات التي تمت تصفيتها من جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. 

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)

[وظائف VALUEIN](er-functions-logical-valuein.md)
