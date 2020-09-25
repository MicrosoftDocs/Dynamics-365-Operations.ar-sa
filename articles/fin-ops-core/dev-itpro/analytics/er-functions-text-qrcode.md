---
title: وظيفة QRCODE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني QRCODE (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: f634976d83fb4066a953b7ab09c963214415e29b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743743"
---
# <a name="qrcode-er-function"></a>وظيفة QRCODE ER

[!include [banner](../includes/banner.md)]

تقوم الوظيفة `QRCODE` بإرجاع قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR)  للسلسلة المُحددة بالتنسيق الثنائي. 

## <a name="syntax"></a>بناء الجملة

```vb
QRCODE (text)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة *سلسلة* التي تمثل النص الأصلي.

## <a name="return-values"></a>إرجاع القيم

*الحاوية*

الدفق الثنائي الناتج.

## <a name="example"></a>مثال

يُمكنك تكوين تنسيق التقارير الإلكترونية (ER) لإنشاء مستند صادر في تنسيق Microsoft Office (مصنفات Excel أو مستندات Word) باستخدام قالب مُعرف مسبقًا. قد يحتوي هذا القالب على كائن **صورة** (مصنف Excel) أو (مستند Word) **عنصر تحكم محتوى صورة** كعنصر نائب لصورة كود QR. تحتاج إلى إضافة تنسيق ER مكون عنصر **خلية** والذي سوف يتم استخدامه لملء نائب العنصر هذا. لتحديد المعلومات التي سوف يتم تخزينها في رمز QR، تحتاج إلى تعريف لربط عنصر **الخلية** هذا. على سبيل المثال، يمكنك تكوين هذا الرابط على أنه يحتوي على التعبير التالي:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

عندما تقوم بتشغيل تنسيق ER المُكون، فسوف يتم استخدام قيمة نص الحقل **LabelText** من مصدر البيانات **model.ListOfShelfLabels** لإنشاء صورة كود QR.  سوف تحل هذه الصورة محل عنصر نائب صورة كود QR في قالب المستند المستخدم لإنشاء مستند صادر. عندما يتم مسح هذه الصورة من المستند الذي تم إنشاؤه ضوئيًا، تقوم بإرجاع النص الذي تم أخذه من حقل **LableText** من مصدر البيانات **model.ListOfShelfLabels**.  للمزيد من المعلومات، راجع [تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
