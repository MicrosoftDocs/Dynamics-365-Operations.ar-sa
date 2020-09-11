---
title: قائمة وظائف التقارير الإلكترونية في الفئة المنطقية
description: يوفر هذا الموضوع معلومات حول الوظائف المنطقية المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705085"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>قائمة وظائف التقارير الإلكترونية في الفئة المنطقية

[!include [banner](../includes/banner.md)]

يُمكن استخدام الوظائف المنطقية للتقارير الإلكترونية (ER) للعمل باستخدام القيم المنطقية لإجراء أكثر من مقارنة واحدة في تعبير واحد أو اختبار شروط متعددة. يعرض هذا الموضوع ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [و](er-functions-logical-and.md)                       | تُرجع هذه الوظيفة قيمة *منطقية* **TRUE** إذا كانت جميع الشروط المُحددة صحيحة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [الحالة](er-functions-logical-case.md)                     | تٌقيّم هذه الوظيفة قيمة التعبير المُحدد في مقابل الخيارات البديلة المُحددة، وترجع نتيجة الخيار الأول الذي يساوي قيمة التعبير المُحدد. وإلا، فإنه يقوم بإرجاع النتيجة الافتراضية الاختيارية، إذا كانت النتيجة الافتراضية مُحدد كآخر وسيطة للوظيفة التي تم استدعائها والتي لم يسبقها خيار. يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة. |
| [إذا](er-functions-logical-if.md)                         | تُرجع هذه الوظيفة القيمة المُحددة الأولى عند تحقق الشرط المُحدد. وإلا، تُرجع القيمة المحددة الثانية. يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة. |
| [ليس](er-functions-logical-not.md)                       | ترجع هذه الوظيفة القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*. |
| [Or](er-functions-logical-or.md)                         | تُرجع هذه الوظيفة قيمة *منطقية* **FALSE** إذا كانت جميع الشروط المُحددة خطأ. إذا كانت أي من الشروط المُحددة صحيحة، تُرجع هذه الوظيفة قيمة *منطقية* **TRUE**. |
| [ValueIn](er-functions-logical-valuein.md)               | تُحدد هذه الوظيفة ما إذا كان الإدخال المُحدد يطابق أي قيمة عنصر مُحدد في القائمة المُحددة. يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | تُحدد هذه الوظيفة ما إذا كان الإدخال المُحدد من النوع *Int64* أو *عدد صحيح* يطابق أي قيمة عنصر مُحدد في القائمة المُحددة. يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |


## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)
