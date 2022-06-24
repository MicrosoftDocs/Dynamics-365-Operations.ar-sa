---
title: ORDERBY ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية ORDERBY‏ (ER).
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
ms.openlocfilehash: 1a922405ea23d2b1ff5ac062785e68626edbc8f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883748"
---
# <a name="orderby-er-function"></a>ORDERBY ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `ORDERBY` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تم فرزها وفقًا للوسيطات المُحددة. يمكن تعريف الوسيطات التالية كعبارات.

## <a name="syntax-1"></a><a name="syntax-1"></a>بناء الجملة 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>بناء الجملة 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> بناء الجملة هذا مدعوم في الإصدار 10.0.25 والإصدارات الأحدث من 365‎ Finance Microsoft Dynamics.

## <a name="arguments"></a>الوسائط

`location`: *[السلسلة](er-formula-supported-data-types-primitive.md#string)*

الموقع الذي يجب تشغيل الفرز فيه. الخيارات التالية هي خيارات صالحة:

- "الاستعلام"
- "InMemory"

`list`: *[قائمة السجلات](er-formula-supported-data-types-composite.md#record-list)*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`expression 1`: *الحقل*

المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها. يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية. هذه الوسيطة مطلوبة.

`expression N`: *الحقل*

المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها. يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

### <a name="syntax-1"></a>بناء الجملة 1

يتم دائمًا إجراء فرز البيانات في ذاكرة خادم التطبيق. لمزيد من التفاصيل، راجع [المثال 1](#example-1).

### <a name="syntax-2"></a>بناء الجملة 2

### <a name="sorting-in-memory"></a>الفرز في الذاكرة

عند تحديد الوسيطة `location` باعتبارها **InMemory**، يتم إجراء فرز البيانات في ذاكرة خادم التطبيق. لمزيد من التفاصيل، راجع [المثال 2](#example-2).

### <a name="sorting-in-database"></a>الفرز في قاعدة البيانات

عند تحديد الوسيطة `location` باعتبارها **استعلام**، يتم فرز البيانات على مستوى قاعدة البيانات. وفي هذه الحالة، يجب أن تشير الوسيطة `list` إلى أحد مصادر البيانات التالية [للتقارير الإلكترونية (ER)](general-electronic-reporting.md) الذي يحدد مصدر التطبيق الذي يمكن إنشاء استعلام قاعدة بيانات له:

- مصدر بيانات من النوع *سجلات الجدول*.
- علاقة مصدر البيانات من النوع *سجلات الجدول*
- مصدر بيانات من النوع *حقل الحساب*.

وفي هذه الحالة، يجب أن تشير الوسيطة `expression 1` والوسيطة `expression N` إلى حقول مصدر بيانات التقارير الإلكترونية الذي يحدد الحقول ذات الصلة لمصدر التطبيق الذي يمكن أيضًا إنشاء استعلام قاعدة بيانات له.

في حاله تعذر إنشاء استعلام قاعدة بيانات، يحدث [خطأ](er-components-inspections.md#i18) في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية. توضح الرسالة التي تتلقاها ان تعبير التقارير الإلكترونية الذي يتضمن وظيفة `ORDERBY` لا يمكن تشغيله في وقت التشغيل.

للحصول على أداء أفضل نوصي باستخدام الخيار **استعلام** عندما يتم تكوين الفرز لمصادر بيانات التطبيق التي قد تحتوي على عدد كبير من السجلات (على سبيل المثال، لجداول تطبيق الحركات).

> [!NOTE]
> لا يمكن ترجمة الدالة `ORDEBY` بحد ذاتها إلى استعلام قاعدة بيانات مباشر. وبالتالي فإن مصدر بيانات التقارير الإلكترونية الذي يحتوي علي هذه الدالة هو غير قابل للاستعلام. كما لا يمكن استخدامه في نطاق دالات التقارير الإلكتروني، مثل [FILTER](er-functions-list-filter.md) و[ALLITEMSQUERY](er-functions-list-allitemsquery.md)، حيث يمكن استخدام مصادر البيانات القابلة للاستعلام فقط.

لمزيد من التفاصيل، راجع [المثال 3](#example-3) و[المثال 4](#example-4).

### <a name="comparability"></a>المقارنة

لأن محرك قاعدة بيانات SQL وخادم تطبيق Finance يمكنهما استخدام قيمة تصنيف مختلفة لحرف واحد، فقد نتيجة الفرز لقائمة السجلات نفسها عند استخدام حقل [السلسلة](er-formula-supported-data-types-primitive.md#string) للفرز. لمزيد من التفاصيل، راجع [المثال 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>المثال 1: التنفيذ الافتراضي في الذاكرة

إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( ORDERBY( DS, DS. Value)).Value` القيمة النصية **"A"**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>المثال 2: التنفيذ الصريح في الذاكرة

إذا تم تكوين **المورّد** كمصدر بيانات تقارير إلكترونية من النوع *سجلات الجدول* الذي يشير إلى الجدول **VendTable**، فسيُرجع كل من التعبير `ORDERBY (Vendor, Vendor.'name()')` والتعبير `ORDERBY ("InMemory", Vendor, Vendor.'name()')` قائمة مورّدين تم فرزها حسب الاسم بترتيب تصاعدي.

عندما تقوم بتكوين التعبير `ORDERBY ("Query", Vendor, Vendor.'name()')` في مصمم تعيين نموذج التقارير الإلكترونية، يحدث [خطأ](er-components-inspections.md#i8) التحقق من الصحة في وقت التصميم لأن المسار `Vendor.'name()'` يشير إلى أسلوب تطبيق لديه منطق لا يمكن ترجمته إلى استعلام قاعدة بيانات مباشر.

## <a name="example-3-database-query"></a><a name="example-3"></a>المثال 3: استعلام قاعدة بيانات

إذا تم تكوين **TaxTransaction** كمصدر بيانات تقارير إلكترونية من النوع *سجلات الجدول* الذي يشير إلى الجدول **TaxTrans**، فإن التعبير `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` يفرز السجلات على مستوى قاعدة بيانات التطبيق ويُرجع قائمة بحركات ضريبية تم فرزها حسب كود الضريبة بترتيب تنازلي.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>المثال 4: مصادر بيانات قابلة للاستعلام

إذا تم تكوين **TaxTransaction** كمصدر بيانات تقارير إلكترونية من النوع *سجلات الجدول* الذي يشير إلى الجدول **TaxTrans**، فيمكن تكوين مصدر بيانات التقارير الإلكترونية **TaxTransactionFiltered** بحيث يحتوي على التعبير `FILTER(TaxTransaction, TaxCode="VAT19")` الذي سيقوم بإحضار الحركات لكود ضريبي معين. لأن مصدر بيانات التقارير الإلكتروني المكوّن **TaxTransactionFiltered** هو قابل للاستعلام، فيمكنك تكوين التعبير `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` بحيث يُرجع قائمة تتضمن حركات ضريبية تم تصفيتها وفرزها حسب تاريخ الحركات بترتيب تصاعدي.

إذا قمت بتكوين **TaxTransactionOrdered** كمصدر بيانات تقارير إلكترونية من النوع *حقل محسوب* الذي يحتوي على التعبير `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` ومصدر بيانات تقارير إلكترونية من النوع *حقل محسوب* الذي يحتوي على التعبير `FILTER(TaxTransactionOrdered, TaxCode="VAT19")`، فسيحدث[خطأ](er-components-inspections.md#i18) تحقق من الصحة في وقت التصميم في مصمم تعيين نموذج التقارير الإلكترونية. يحدث هذا الخطأ لان الوسيطة الأولى للدالة [FILTER](er-functions-list-filter.md#usage-notes) يجب أن تشير إلى مصدر بيانات تقارير إلكترونية قابل للاستعلام، ولكن مصدر البيانات **TaxTransactionOrdered** الذي يحتوي على الدالة `ORDERBY` غير قابل للاستعلام.

## <a name="example-5-comparability"></a><a name="example-5"></a>المثال 5: المقارنة

### <a name="prerequisites"></a>المتطلبات الأساسية

1. أدخل مصدر البيانات **‎DS1** من النوع *حقل محسوب* الذي يحتوي على التعبير `SPLIT ("D1|_D2|D3", "|")`.
2. افتح صفحة **[قيم الأبعاد المالية](../../../finance/general-ledger/financial-dimensions.md)**، وحدد البُعد **CostCenter**.
3. أدخل قيم البُعد التالية: **D1** و **\_D2** و **D3**.

### <a name="sorting-in-memory"></a>الفرز في الذاكرة

1. قم بتكوين مصدر البيانات **DS2** من النوع *حقل محسوب* الذي يحتوي على التعبير `ORDERBY("InMemory", DS1, DS1.Value)`.
2. لاحظ أن التعبير `FIRST(DS2).Value` يُرجع القيمة النصية **"D1"**، وأن التعبير `INDEX(DS2, COUNT(DS2)).Value` يُرجع القيمة النصية **"\_D2"**، وأن التعبير `STRINGJOIN(DS2, DS2.Value, "|")` يُرجع القيمة النصية **"D1\|D3\|\_D2"**.

### <a name="sorting-in-database"></a>الفرز في قاعدة البيانات

1. أدخل مصدر البيانات **DS3** من النوع *سجلات الجدول* الذي يشير إلى الكيان **FinancialDimensionValueEntity**.
2. قم بتكوين مصدر البيانات **DS4** من النوع *حقل محسوب* الذي يحتوي على التعبير `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. قم بتكوين مصدر البيانات **DS5** من النوع *حقل محسوب* الذي يحتوي على التعبير `ORDERBY(DS4, DS4.DimensionValue)`.
4. لاحظ أن التعبير `FIRST(DS5).Value` يُرجع القيمة النصية **"\_D2"**، وأن التعبير `INDEX(DS5, COUNT(DS5)).Value` يُرجع القيمة النصية **"D3"** وأن التعبير `STRINGJOIN(DS5, DS5.Value, "|")` يُرجع القيمة النصية **"\_D2\|D1\|D3"**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
