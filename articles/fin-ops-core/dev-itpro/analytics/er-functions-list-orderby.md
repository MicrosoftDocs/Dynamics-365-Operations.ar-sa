---
title: ORDERBY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ORDERBY (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: fcacacbf0727fa26350ff23c781c2da54d0ba77262c94dd48d88d01444352947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776136"
---
# <a name="orderby-er-function"></a>ORDERBY ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ORDERBY` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تم فرزها وفقًا للوسيطات المُحددة. يمكن تعريف الوسيطات التالية كعبارات.

## <a name="syntax"></a>بناء الجملة

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`expression 1`: *الحقل*

المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها. يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية. هذه الوسيطة مطلوبة.

`expression N`: *الحقل*

المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها. يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="example-1"></a>مثال1

إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( ORDERBY( DS, DS. Value)).Value` القيمة النصية **"A"**.

## <a name="example-2"></a>مثال2

عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `ORDERBY (Vendors, Vendors.'name()')` قائمة مورّدين تم فرزها حسب الاسم بترتيب تصاعدي.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]