---
title: ENUMERATE ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكتروني ENUMERATE‏ (ER).
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
ms.openlocfilehash: adaa2582e6dced428cf1f15a235ecbfd036362e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273237"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ENUMERATE` قيمة *قائمة سجلات* جديدة تتكون من السجلات التي تم تعدادها للقائمة المحددة.

## <a name="syntax"></a>بناء الجملة

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تكشف قائمة السجلات التي تم تعدادها المُعادة العناصر الإضافية التالية:

- سجل الحقول (مكون **القيمة** )
- فهرس السجلات الحالية (المكون **Number**)

## <a name="example"></a>مثال

في الرسم التوضيحي التالي، يتم إنشاء مصدر البيانات **Enumerated** كقائمة تم تعدادها لسجلات المورّدين من مصدر البيانات **Vendors** الذي يشير إلى الجدول VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

يوضح الرسم التوضيحي التالي تنسيق التقارير الإلكترونية (ER). في هذا التنسيق، يتم إنشاء عمليات ربط البيانات لإنشاء إخراج بتنسيق XML. يقدم هذا الإخراج موردين فرديين كعقد تم تعدادها.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
