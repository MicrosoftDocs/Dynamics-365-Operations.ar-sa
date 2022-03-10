---
title: FILTER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FILTER (ER).
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: e857306574dda7bad5dd25fc7708514997d8e86f
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922413"
---
# <a name="filter-er-function"></a>FILTER ER وظيفة

[!include [banner](../includes/banner.md)]

تٌرجع وظيفة `FILTER` القائمة المُحددة كقيمة *قائمة سجلات* بعد تغيير الاستعلام بحيث تتم تصفيتها للشرط المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`condition`: *منطقي*

تعبير شرطي صالح يُستخدم لتصفية سجلات القائمة المُحددة.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a><a name="usage-notes"></a>ملاحظات الاستخدام

تختلف هذه وظيفة عن وظيفة [WHERE](er-functions-list-where.md) لأنه يتم تطبيق الشرط المحدد على أي من مصادر بيانات التقارير الإلكترونية (ER) لنوع *سجلات الجداول* على مستوى قاعدة البيانات. يمكن تحديد القائمة والشرط باستخدام الجداول والعلاقات.

إذا لم تسمح أحد الوسيطتين أو كليهما المكونة لهذه الوظيفة (`list` و`condition`) بترجمة هذا الطلب للاستدعاء المباشر لـ SQL، يتم طرح استثناء في وقت التصميم. يُعلم هذا الاستثناء المستخدم أنه إما `list` أو `condition` لا يُمكن استخدامهم للاستعلام عن قاعدة البيانات.

> [!NOTE]
> تعمل وظيفة `FILTER` بشكل مختلف عن وظيفة `WHERE` عند استخدام وظيفة [`VALUEIN`](er-functions-logical-valuein.md) لتحديد معايير التحديد.
> 
> - إذا تم استخدام وظيفة `VALUEIN` في نطاق وظيفة `WHERE`، وتشير الوسيطة الثانية لـ `VALUEIN` إلى مصدر بيانات لا يقوم بإرجاع أي سجلات، وتتم مراعاة القيمة المنطقية *[False](er-formula-supported-data-types-primitive.md#boolean)* التي تُرجعها وظيفة `VALUEIN`. لذلك، يقوم التعبير `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` بإرجاع أي سجلات موردين إذا كان مصدر بيانات **VendGroups** لا يُرجع أي سجلات لمجموعات الموردين.
> - إذا تم استخدام وظيفة `VALUEIN` في نطاق وظيفة `FILTER`، وتشير الوسيطة الثانية لـ `VALUEIN` إلى مصدر بيانات لا يقوم بإرجاع أي سجلات، ويتم تجاهل القيمة المنطقية *[False](er-formula-supported-data-types-primitive.md#boolean)* التي تُرجعها وظيفة `VALUEIN`. لذلك، يقوم التعبير `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` بإرجاع جميع سجلات الموردين لمصدر بيانات **الموردين**، حتى إذا كان مصدر بيانات **VendGroups** لا يُرجع أي سجلات لمجموعات الموردين.

## <a name="example-1"></a>مثال1

إذا تم تكوين **Vendor** كمصدر بيانات تقارير إلكترونية يشير إلى جدول VendTable، يُرجع التعبير `FILTER (Vendors, Vendors.VendGroup = "40")` قائمة المورّدين التي تنتمي إلى مجموعة الموردين 40.

## <a name="example-2"></a>مثال2

إذا تم تكوين **المورّد** كمصدر بيانات التقارير الإلكترونية (ER) يُشير إلى جدول VendTable، وإذا تم تكوين **parmVendorBankGroup** كمصدر بيانات التقارير الإلكترونية (ER) يُرجع قيمة نوع بيانات *السلسلة*، يُرجع التعبير `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` قائمة حسابات المورّدين الذين ينتمون إلى مجموعة بنكية مُحددة.

## <a name="example-3"></a>المثال الثالث

يُمكنك إدخال مصدر بيانات **DS** من النوع *الحقل المحسوب* ، الذي يحتوي على التعبير `SPLIT ("A,B,C", ",")`. ثم قم بإدخال تعبير آخر، `FILTER( DS, DS.Value = "B")`. عندما تحاول حفظ هذا التعبير في مصم تركيبة التقارير الإلكترونية ER، يتم طرح الاستثناء التالي: "خطأ التحقق من الصحة: تعبير القائمة للوظيفة FILTER غير قابل للاستعلام."

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
