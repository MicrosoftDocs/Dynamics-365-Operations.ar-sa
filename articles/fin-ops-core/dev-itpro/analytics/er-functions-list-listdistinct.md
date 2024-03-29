---
title: دالة إعداد التقارير الإلكترونية LISTDISTINCT
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية LISTDISTINCT‏ (ER).
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285264"
---
# <a name="listdistinct-er-function"></a>دالة إعداد التقارير الإلكترونية LISTDISTINCT

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

تقوم الدالة `LISTDISTINCT` بحساب التعبير المحدد كمحدد لكل سجل من القائمة المحددة. وتقوم بإرجاع قيمة *قائمة سجلات* جديدة تحتوي على سجل مفرد لكل قيمة محدد فريدة.

## <a name="syntax"></a>بناء الجملة

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`selector`: *نوع البيانات الأساسي*

تعبير صالح يتم استخدامه لحساب قيمة محدد لكل سجل في القائمة المحددة.

أنواع البيانات التالية مدعومة لهذه المعلمة:

- منطقي
- التاريخ
- التاريخ/الوقت
- Guid
- عدد صحيح
- Int64
- حقيقي
- السلسلة

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

بنية القائمة التي تم إنشاؤها تتطابق مع بنية القائمة المحددة.

قد يتم حساب نفس قيمة المحدد لسجلات متعددة في القائمة المحددة. في هذه الحالة، تكون قيم الحقول الخاصة بالسجل المقابل في القائمة التي تم إنشاؤها مساوية لقيم السجل الأول من القائمة المحددة التي يتم حساب قيمة المحدد لها.

يتم تنفيذ هذه الوظيفة على مصدر بيانات [إعداد التقارير الإلكترونية](general-electronic-reporting.md) لنوع *قائمة السجلات* الموجود في الذاكرة.

يمكن أيضًا استخدام مصدر البيانات **GROUPBY** لإنشاء قائمة بالسجلات التي يتم من خلالها حساب المحدد الذي يتضمن قيمًا مميزة. ومع ذلك، من منظور الأداء واستهلاك الذاكرة، من الأفضل استخدام الدالة `LISTDISTINCT` بدلاً من مصدر البيانات **GROUPBY‎**، لأن تنفيذ الوظيفة يتم في الذاكرة.

## <a name="example"></a>مثال

يوضح المثال التالي كيفية الحصول علي قائمة بأرقام حسابات العملاء الفريدة التي تم إصدار فاتورة مبيعات أو فاتورة مشروع واحدة عل الأقل خلال فترة محددة.

1. أدخل مصدر البيانات **SalesInvoice** للنوع `Record list` الذي يشير إلى جدول التطبيق **CustInvoiceJour** ويصفي فواتير المبيعات لفترات محددة.

    يقوم الحقل `InvoiceAccount` لمصدر البيانات هذا بإرجاع رقم الحساب الخاص بعميل تمت فوترته.

2. أدخل مصدر البيانات **ProjectInvoice** للنوع `Record list` الذي يشير إلى جدول التطبيق **ProjInvoiceJour** ويصفي فواتير المشاريع لفترات محددة.

    يقوم الحقل `InvoiceAccount` لمصدر البيانات هذا بإرجاع رقم الحساب الخاص بعميل تمت فوترته.

3. قم بتكوين مصدر البيانات **AllInvoices** من النوع `Calculated field` الذي يحتوي على التعبير `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    يقوم مصدر البيانات هذا بإرجاع القائمة المرتبطة لفواتير المبيعات وفواتير المشروع.

4. قم بتكوين مصدر البيانات **InvoicedCustomer** من النوع `Record list` الذي يحتوي على التعبير `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    يقوم مصدر البيانات هذا بإرجاع قائمة جديدة تحتوي على سجل مفرد لكل عميل فريد تمت فوترته خلال الفترة المحددة. يحتوي الحقل `InvoiceAccount` الخاص بهذه القائمة على رقم حساب عميل.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
