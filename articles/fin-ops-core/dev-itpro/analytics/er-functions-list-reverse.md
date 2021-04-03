---
title: REVERSE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية REVERSE (ER).
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
ms.openlocfilehash: f76582bc8b752fe0322bee8917d8649ed1c024ba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567356"
---
# <a name="reverse-er-function"></a>REVERSE ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `REVERSE` القائمة المُحددة كقيمة *قائمة التسجيلات* في ترتيب فرز معكوس.

## <a name="syntax"></a>بناء الجملة

```vb
REVERSE (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="example-1"></a>مثال1

إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` القيمة النصية **"C"**.

## <a name="example-2"></a>مثال2

عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` قائمة مورّدين تم فرزها حسب الاسم بترتيب تنازلي.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]