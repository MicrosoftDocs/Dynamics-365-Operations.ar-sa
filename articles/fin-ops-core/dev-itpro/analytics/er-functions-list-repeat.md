---
title: تكرار وظيفة ER
description: توفر هذه المقالة معلومات حول كيفية استخدام وظيفة REPEAT Electronic Report (ER).
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220681"
---
# <a name="repeat-er-function"></a>تكرار وظيفة ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

تقوم الوظيفة `REPEAT` بإنشاء سجل يحتوي علي الحقل الذي يحتوي علي القيمة التي تطابق الإدخال المحدد. ثم تقوم بإرجاع قائمه *سجلات جديده* لسجل يتكرر بعدد محدد من المرات.

## <a name="syntax"></a>بناء الجملة

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>الوسائط

`item`: أي [بدائي مدعوم](er-formula-supported-data-types-primitive.md) أو [نوع](er-formula-supported-data-types-composite.md) بيانات مركب

القيمة التي سيتم تكرارها.

`number`: *عدد صحيح*

عدد التكرارات.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تعرض قائمة السجلات المكررة التي تم إرجاعها الحقول التالية:

- القيمة المحددة (حقل`Item` )
- فهرس السجلات الحالية (الحقل رقم`Number` )

> [!NOTE]
> نظرًا لاستخدام الترقيم المستند إلى واحد لهذه الوظيفة ، فإن حقل `Number` له القيمة **1** للسجل الأول من القائمة الناتجة.

يمكنك استخدام هذه الوظيفة لضرب البيانات الموجودة بحيث يمكنك عمل اختبار الأداء والتخزين لحلول التقارير الكترونية [(ER)](general-electronic-reporting.md) باستخدام [Regression suite automation tool (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>مثال

تريد إنشاء مستند بتنسيق XML يجب ان يحتوي علي العديد من `Party` عناصر XML التي تقوم بتحديدها في حقل إدخال البيانات في مربع الحوار في وقت التشغيل ، قبل ان يبدا تنفيذ تنسيق ER.

يوضح الرسم التوضيحي التالي [تنسيق](er-overview-components.md#format-component). بهذا التنسيق ، يتم أضافه عنصر XML واحد `Party` لكشف الخصائص الخاصة بطرف واحد.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

يبين الرسم التوضيحي التالي مصادر البيانات المكونة التالية:

- مصدر البيانات الذي `Party` يمثل طرفًا واحدًا. يستخدم الحقل `Party.Value` لكشف قيمة نصية مفردة.
- The `NumberOfRepeats` [مصدر بيانات](er-user-input-parameter-data-sources.md) الذي يتم استخدامه لتقديم حقل إدخال بيانات في مربع الحوار في وقت التشغيل ، بحيث يمكنك تحديد عدد الأطراف التي يجب إدخالها في المستند الذي تم إنشاؤه.
- يقوم مصدر البيانات `Party2` الذي يكرر `Party` عدد المرات التي قمت بتحديدها في مصدر البيانات `NumberOfRepeats` .

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

يبين الرسم التوضيحي التالي روابط البيانات لتنسيق ER القابل للتحرير والذي تم إنشاؤه لإنشاء الإخراج في تنسيق XML. يقدم هذا الناتج الأطراف الفردية كعقد تم تعدادها.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

يبين الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق الذي تم تصميمه وتحديد قيمة مصدر البيانات علي `NumberOfRepeats` أنه **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
