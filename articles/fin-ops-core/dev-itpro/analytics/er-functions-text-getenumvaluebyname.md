---
title: 'وظيفة GETENUMVALUEBYNAME ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETENUMVALUEBYNAME (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916834"
---
# <a name="GETENUMVALUEBYNAME">وظيفة GETENUMVALUEBYNAME ER</a>

[!include [banner](../includes/banner.md)]

تبحث وظيفة `GETENUMVALUEBYNAME` عن قيمة *Enum* مُحددة في مصدر بيانات التعداد المُحدد باستخدام اسم التعداد المُحدد كقيمة *السلسلة* . إذا تم العثور على قيمة *تعداد* ، تقوم الوظيفة بإرجاعها. وإلا، تقوم الوظيفة بإرجاع قيمه التعداد **null**.

## <a name="syntax"></a>بناء الجملة

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>الوسائط

`enumeration data source path`: *تعداد*

مسار مرجع صالح لمصدر بيانات أحد أنواع التعداد التالية:

- تعداد نموذج إعداد التقارير الإلكترونية (ER)
- تعداد تنسيق إعداد التقارير الإلكترونية
- تعداد Microsoft Dynamics 365 Finance

`enumeration value text`: *السلسلة*

قيمة سلسلة تمثل اسم قيمة تعداد مُفرد.

## <a name="return-values"></a>إرجاع القيم

‏‫قابل للإبطال *Enum*

قيمة التعداد الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

لا يتم طرح أي استثناء إذا لم يتم العثور على قيمة *Enum* باستخدام اسم قيمة التعداد المحدد كقيمة *سلسلة* .

## <a name="example"></a>مثال

في الرسم التوضيحي التالي، يتم تقديم تعداد **ReportDirection** في نموذج بيانات. لاحظ أنه يتم تحديد التسميات لقيم التعداد.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

يبين الرسم التوضيحي التالي هذه التفاصيل:

- يتم تكوين مصدر البيانات **$Direction** في تقرير التقارير الإلكترونية. يتم تكوين مصدر البيانات هذا استنادًا إلى تعداد نموذج **ReportDirection**.
- تم تصميم التعبير `$IsArrivals` ليستخدم مصدر بيانات **$Direction** المستند إلى تعداد النموذج تعداد النموذج كمعلمة لهذه الوظيفة.
- قيمة تعبير المقارنة هذا هي **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
