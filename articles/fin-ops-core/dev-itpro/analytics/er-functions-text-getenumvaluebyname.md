---
title: وظيفة GETENUMVALUEBYNAME ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية GETENUMVALUEBYNAME‏ (ER).
author: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: eb0c4818c8d5020125d198da4ceb0562605da397
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285958"
---
# <a name="getenumvaluebyname-er-function"></a>وظيفة GETENUMVALUEBYNAME ER

[!include [banner](../includes/banner.md)]

تبحث وظيفة `GETENUMVALUEBYNAME` عن قيمة *Enum* مُحددة في مصدر بيانات التعداد المُحدد باستخدام اسم التعداد المُحدد كقيمة *السلسلة* . إذا تم العثور على قيمة *تعداد* ، تقوم الوظيفة بإرجاعها. وإلا، تقوم الوظيفة بإرجاع قيمه التعداد **null**.

## <a name="syntax"></a>بناء الجملة

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>الوسائط

`enumeration data source path`: *تعداد*

مسار مرجع صالح لمصدر بيانات أحد أنواع التعداد التالية:

- تعداد نموذج إعداد التقارير الإلكترونية (ER)
- تعداد تنسيق إعداد التقارير الإلكترونية
- تعداد Microsoft Dynamics 365‏ Finance

`enumeration value text`: *السلسلة*

قيمة سلسلة تمثل اسم قيمة تعداد مُفرد.

## <a name="return-values"></a>إرجاع القيم

‏‫قابل للإبطال *Enum*

قيمة التعداد الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

لا يتم طرح أي استثناء إذا لم يتم العثور على قيمة *Enum* باستخدام اسم قيمة التعداد المحدد كقيمة *سلسلة* .

## <a name="example-1"></a>مثال1

في الرسم التوضيحي التالي، يتم تقديم تعداد **ReportDirection** في نموذج بيانات. لاحظ أنه يتم تحديد التسميات لقيم التعداد.

![القيم المتوفرة لقائمة تعداد نموذج البيانات.](./media/ER-data-model-enumeration-values.PNG)

يبين الرسم التوضيحي التالي هذه التفاصيل:

- يتم تكوين مصدر البيانات **$Direction** في تقرير التقارير الإلكترونية. يتم تكوين مصدر البيانات هذا استنادًا إلى تعداد نموذج **ReportDirection**.
- تم تصميم التعبير `$IsArrivals` ليستخدم مصدر بيانات **$Direction** المستند إلى تعداد النموذج تعداد النموذج كمعلمة لهذه الوظيفة.
- قيمة تعبير المقارنة هذا هي **TRUE**.

![مثال عن تعداد نموذج بيانات.](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>مثال2

تسمح لك الدالتان `GETENUMVALUEBYNAME` و[`LISTOFFIELDS`](er-functions-list-listoffields.md) بإحضار قيم وتسميات التعدادات المعتمدة كقيم نصية. (التعدادات المعتمدة هي تعدادات التطبيق وتعدادات نموذج البيانات وتعدادات التنسيق.)

في الرسم التوضيحي التالي، يتم تقديم مصدر البيانات **TransType** في تعيين نموذج. يُشير مصدر البيانات هذا إلى تعداد تطبيق **LedgerTransType**.

![مصدر بيانات لتعيين النموذج الذي يشير إلى تعداد التطبيق.](./media/er-functions-text-getenumvaluebyname-example2-1.png)

يبين الرسم التوضيحي التالي مصدر البيانات **TransTypeList** المكوّن في تعيين نموذج. يتم تكوين مصدر البيانات هذا استنادًا إلى تعداد تطبيق **TransType**. تُستخدم الدالة `LISTOFFIELDS` لإرجاع كافة قيم التعداد كقائمة سجلات تحتوي على حقول. بهذه الطريقة، يتم عرض تفاصيل كل قيمة من قيم التعداد.

> [!NOTE]
> تم تكوين الحقل **EnumValue** لمصدر البيانات **TransTypeList** باستخدام التعبير `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. يرجع هذا الحقل قيمة التعداد لكل سجل في هذه القائمة.

![مصدر بيانات لتعيين النموذج الذي يرجع كافة قيم التعداد لتعداد محدد كقائمة بالسجلات.](./media/er-functions-text-getenumvaluebyname-example2-2.png)

يبين الرسم التوضيحي التالي مصدر البيانات **VendTrans** المكوّن في تعيين نموذج. يقوم مصدر البيانات هذا بإرجاع سجلات حركات المورّد من جدول تطبيق **VendTrans**. يتم تحديد نوع دفتر الأستاذ لكل حركة بواسطة قيمة الحقل **TransType**.

> [!NOTE]
> تم تكوين الحقل **TransTypeTitle** لمصدر البيانات **VendTrans** باستخدام التعبير `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. يقوم هذا الحقل بإرجاع تسمية قيمة التعداد الخاصة بالحركة الحالية كنص، إذا كانت قيمة التعداد هذه متوفرة. وإلا، فسيقوم بإرجاع قيمة سلسلة فارغة.
>
> يرتبط الحقل **TransTypeTitle** بحقل **LedgerType** لنموذج بيانات يمكّن استخدام هذه المعلومات في كل تنسيقات التقارير الإلكترونية التي تستخدم نموذج البيانات كمصدر بيانات.

![مصدر بيانات لتعيين النموذج الذي يُرجع حركات المورّد.](./media/er-functions-text-getenumvaluebyname-example2-3.png)

يبين الرسم التوضيحي التالي كيف يمكنك استخدام [مصحح أخطاء مصدر البيانات](er-debug-data-sources.md) لاختبار تعيين النموذج المكوّن.

![استخدام مصحح أخطاء مصدر البيانات لاختبار تعيين النموذج المكوّن.](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

يعرض حقل **LedgerType** لنموذج بيانات تسمية أنواع الحركات كما هو متوقع.

إذا كنت تخطط لاستخدام هذه الطريقة كمية كبيره من بيانات الحركات، فيجب مراعاة أداء التنفيذ. لمزيد من المعلومات، راجع [تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)

[تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER وظيفة](er-functions-list-listoffields.md)

[FIRSTORNULL ER وظيفة](er-functions-list-firstornull.md)

[WHERE ER وظيفة](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
