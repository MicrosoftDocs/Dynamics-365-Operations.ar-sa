---
title: الدالة GETLABELTEXT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام دالة إعداد التقارير الإلكترونية GETLABELTEXT.
author: NickSelin
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ce66c9410abeee16bbd074204262edf79bf6d68
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462400"
---
# <a name="getlabeltext-er-function"></a>الدالة GETLABELTEXT ER

[!include [banner](../includes/banner.md)]

تبحث الدالة `GETLABELTEXT` عن تسمية معينة لإرجاع قيمة *[سلسلة](er-formula-supported-data-types-primitive.md#string)* تمثل ترجمة التسمية المحددة باللغة المحددة.

## <a name="syntax"></a>بناء الجملة

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>الوسائط

### <a name="label-id"></a>معرف التسمية

`label id`: *سلسلة* أو *معرف التسمية*

المعرف الصالح لأحد أنواع التسميات التالية:

- تسمية [التقارير الإلكترونية (ER)](general-electronic-reporting.md)
- تسمية Microsoft Dynamics 365 Finance

#### <a name="usage-notes"></a>ملاحظات الاستخدام

يمكن تعريف هذه الوسيطة كثابتة فقط، باستخدام أحد الأنماط المدعومة التالية:

- لتسميات التقارير الإلكترونية:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- لتسميات Finance:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> في وقت التصميم، تظهر رسالة خطأ التحقق من الصحة في الصفحة **[مصمم المعادلة](er-advanced-formula-editor.md)** إذا لم يتم العثور على تسمية باستخدام معرف التسمية المتوفر.

### <a name="language"></a>اللغة

`language`: *السلسلة*

سلسلة تمثل رمز لغة.

#### <a name="usage-notes"></a>ملاحظات الاستخدام

يمكن تعريف هذه الوسيطة إما كنص ثابت أو كمسار لحقل مصدر بيانات يقوم بإرجاع قيمة *سلسلة*.

> [!NOTE]
> في وقت التصميم، تظهر رسالة خطأ التحقق من الصحة إذا لم يتم العثور على رمز لغة باستخدام وسيطة المتوفرة `language` المتوفرة عند تعريفها على أنها ثابت نصي.
>
> في وقت التشغيل، يتم إرجاع ترجمة للغة النظام `EN-US` لتسمية محددة في حاله عدم العثور على أي رمز لغة وذلك باستخدام وسيطة `language` المتوفرة.

## <a name="return-values"></a>إرجاع القيم

*سلسلة*

القيمة النصية الناتجة.

## <a name="example-1-system-label"></a><a name=example-1></a>مثال 1: تسمية النظام

يقوم التعبيران `GETLABELTEXT (@"SYS70894", "en-us")` و`GETLABELTEXT ("SYS70894", "en-us")` بإرجاع الترجمة الإنجليزية "Nothing to print" لتسمية التطبيق `@SYS70894`.

## <a name="example-2-er-label"></a><a name=example-2></a>مثال 2: تسمية التقارير الإلكترونية

أنت تبدأ بتحرير [تكوين](general-electronic-reporting.md#Configuration) تقارير إلكترونية [يشتق](er-quick-start2-customize-report.md#DeriveProvidedFormat) من تكوين **ISO20022 تحويل الائتمان (DE)** ، أدخل مصدر بيانات جديدًا من النوع *[حقل محسوب](er-calculated-field-ds-performance.md)*، واكتب التعبير `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` لمصدر البيانات هذا. في هذه الحالة، في وقت التشغيل، يُرجع مصدر البيانات الترجمة الألمانية "Kreditorenname" لتسمية التقارير الإلكترونية `@GER_LABEL:VendorName` التي تم تكوينها في بادئ الأمر في تكوين التقارير الإلكترونية **ISO20022 تحويل الائتمان‬ (DE)**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)

[تصميم تقارير متعددة اللغات في التقارير الإلكترونية](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
