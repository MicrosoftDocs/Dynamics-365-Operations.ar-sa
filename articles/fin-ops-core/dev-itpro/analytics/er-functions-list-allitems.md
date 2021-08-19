---
title: ALLITEMS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ALLITEMS (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cf1e05e9377ba18ad0269a48b13bd242a8e5356f4a52ea3723e347dcf5e138e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719838"
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