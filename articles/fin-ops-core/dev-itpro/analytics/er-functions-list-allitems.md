---
title: ALLITEMS ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكتروني ALLITEMS‏ (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: bb469955c66baf875eea80dde8199986e69e2e71
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274098"
---
# <a name="allitems-er-function"></a>ALLITEMS ER وظيفة

[!include [banner](../includes/banner.md)]

تعمل وظيفة `ALLITEMS` كمجموعة في الذاكرة وتُرجع قيمة *قائمة سجلات* مُدمجة جديدة كقائمة من السجلات التي تمثل كافة العناصر التي تتطابق مع المسار المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>الوسائط

`path`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يجب تحديد المسار كمسار مصدر بيانات صالح لعنصر مصدر بيانات لنوع بيانات *قائمة السجلات*. يجب أن تُظهر عناصر البيانات مثل سلسلة المسار والتاريخ خطأ في وقت التصميم في منشئ تعبير التقارير الإلكترونية (ER).

لا نوصي باستخدام هذه وظيفة لمصادر البيانات التعاملية التي قد تحتوي على مقدار كبير من البيانات. بدلًا من ذلك، ضع في اعتبارك استخدام وظيفة [ALLTEMSQUERY](er-functions-list-allitemsquery.md). 

## <a name="example-1"></a>مثال1

إذا قمت بإدخال `SPLIT("abcdef" , 2)` كمصدر بيانات **DS**، يُرجع التعبير `COUNT( ALLITEMS (DS))` **3**.

## <a name="example-2"></a>مثال2

إذا قمت بإدخال **Vend** كمصدر بيانات لنوع البيانات *قائمة السجلات* التي تشير إلى جدول تطبيق VendTable، يُرجع التعبير `ALLITEMS (Vend.'<Relations'.ContactPerson)` قائمة سجلات مُسطحة تحتوي على بنية جدول **ContactPerson** وتحتوي على كافة جهات الاتصال التي يُمكن الوصول إليها باستخدام العلاقة **ContactPerson.ContactForParty == VendTable.Party**، والمتاحة لجميع الموردين من جدول الموردين المرجعي.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
