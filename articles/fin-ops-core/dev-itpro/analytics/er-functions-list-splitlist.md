---
title: SPLITLIST ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLITLIST‏ (ER).
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292515"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER وظيفة

[!include [banner](../includes/banner.md)]

تقسم الوظيفة `SPLITLIST` القائمة المُحددة إلى قوائم فرعية (أو دفعات)، تحتوي كل واحدة منها على العدد المُحدد من السجلات. ثم يقوم بإرجاع النتيجة كقيمة *قائمة سجلات* جديدة التي تتكون من الدفعات.

## <a name="syntax-1"></a>بناء الجملة 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>بناء الجملة 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`number`: *عدد صحيح*

أقصى عدد للسجلات لكل دفعة.

`on-demand reading flag`: *منطقي*

*قيمة منطقية* القيمة التي تحدد ما إذا كان يجب إنشاء عناصر القوائم الفرعية عند الطلب.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تحتوي قائمة الدفعات التي تم إرجاعها على العناصر التالية:

 - **القيمة:** *القائمة*

    قائمة السجلات التي تخص الدفعة الحالية.

- **BatchNumber:** *عدد صحيح*

    عدد الدفعات الحالية في القائمة المُرتجعة.

عند تعيين علامة القراءة عند الطلب على **True**، يتم إنشاء القوائم الفرعية عند الطلب مما يسمح بتقليل استهلاك الذاكرة ولكن قد يتسبب في تدهور الأداء إذا لم يتم استخدام العناصر بشكل تسلسلي.

## <a name="example"></a>مثال

في الرسم التوضيح التالي، يتم إنشاء مصدر بيانات **الخطوط** كقائمة سجلات تحتوي على ثلاث سجلات. يتم تقسيم هذه القائمة إلى دُفعات، يحتوي كل منها على ما يصل إلى سجلين.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

يبين الرسم التوضيحي التالي تخطيط التنسيق المصمم. في تخطيط التنسيق هذا، يتم إنشاء عمليات الربط إلى مصدر بيانات **الخطوط** لإنشاء إخراج بتنسيق XML. يقدم هذا الإخراج عقدًا فردية لكل دُفعة والسجلات التي فيها.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
