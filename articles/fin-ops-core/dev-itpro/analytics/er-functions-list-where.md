---
title: WHERE ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية WHERE‏ (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b3f8b01bffd0c530e5095531fc184c960744e751
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273147"
---
# <a name="where-er-function"></a>WHERE ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `WHERE` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تمت تصفيتها وفقًا للشرط المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`condition`: *منطقي*

تعبير شرطي صالح يُستخدم لتصفية سجلات القائمة المُحددة.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تختلف هذه الوظيفة عن وظيفة [FILTER](er-functions-list-filter.md) ، لأن يتم تطبيق الشرط المُحدد على أي من مصادر بيانات التقارير الإلكترونية (ER) لنوع *قائمة السجلات* الموجودة في الذاكرة.

إذا كانت هذه الوسيطات المكونة لهذه الوظيفة (`list` و`condition`) تسمح بترجمة هذا الطلب للاستدعاء المباشر لـ SQL، يتم طرح رسالة تحذيرية في وقت التصميم. تُعلم هذه الرسالة المستخدم أنه يُمكنه تحسين الأداء إذا تم استخدام الوظيفة [FILTER](er-functions-list-filter.md) بدلًا من `WHERE`.

## <a name="example-1"></a>مثال1

إذا تم تكوين **Vendor** كمصدر بيانات تقارير إلكترونية يشير إلى جدول VendTable، يُرجع التعبير `WHERE (Vendors, Vendors.VendGroup = "40")` قائمة المورّدين التي تنتمي إلى مجموعة الموردين 40.

## <a name="example-2"></a>مثال2

إذا أدخلت مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `WHERE( DS, DS.Value = "B")` قائمة بسجل واحد فقط يحتوي على النص **"B"** في حقل **القيمة**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
