---
title: قائمة وظائف التقارير الإلكترونية في الفئة المنطقية
description: توفر هذه المقالة معلومات عن الوظائف المنطقية المعتمدة في إعداد التقارير الإلكترونية (ER).
author: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291283"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>قائمة وظائف التقارير الإلكترونية في الفئة المنطقية

[!include [banner](../includes/banner.md)]

يُمكن استخدام الوظائف المنطقية للتقارير الإلكترونية (ER) للعمل باستخدام القيم المنطقية لإجراء أكثر من مقارنة واحدة في تعبير واحد أو اختبار شروط متعددة. توفر هذه المقالة ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة | ‏‏الوصف |
|----------|-------------|
| [و](er-functions-logical-and.md)                       | تُرجع هذه الوظيفة قيمة *منطقية* **TRUE** إذا كانت جميع الشروط المُحددة صحيحة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [الحالة](er-functions-logical-case.md)                     | تٌقيّم هذه الوظيفة قيمة التعبير المُحدد في مقابل الخيارات البديلة المُحددة، وترجع نتيجة الخيار الأول الذي يساوي قيمة التعبير المُحدد. وإلا، فإنه يقوم بإرجاع النتيجة الافتراضية الاختيارية، إذا كانت النتيجة الافتراضية مُحدد كآخر وسيطة للوظيفة التي تم استدعائها والتي لم يسبقها خيار. يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة. |
| [يحتوي على](er-functions-logical-contains.md)             | تحدد هذه الوظيفة ما إذا كان الإدخال المحدد يحتوي على النص المحدد أم لا. تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كان الإدخال المحدد يحتوي على النص المحدد. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [EndsWith](er-functions-logical-endswith.md)             | تحدد هذه الوظيفة ما إذا كانت نهايات الإدخال المحددة تنتهي بالنص المحدد أم لا. تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كانت المدخلات المحددة تنتهي بالنص المحدد. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [إذا](er-functions-logical-if.md)                         | تُرجع هذه الوظيفة القيمة المُحددة الأولى عند تحقق الشرط المُحدد. وإلا، تُرجع القيمة المحددة الثانية. يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة. |
| [ليس](er-functions-logical-not.md)                       | ترجع هذه الوظيفة القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*. |
| [Or](er-functions-logical-or.md)                         | تُرجع هذه الوظيفة قيمة *منطقية* **FALSE** إذا كانت جميع الشروط المُحددة خطأ. إذا كانت أي من الشروط المُحددة صحيحة، تُرجع هذه الوظيفة قيمة *منطقية* **TRUE**. |
| [StartsWith](er-functions-logical-startswith.md)         | تحدد هذه الوظيفة ما إذا كانت الإدخال المحدد يبدأ بالنص المحدد أم لا. تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كانت المدخلات المحددة تبدأ بالنص المحدد. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [ValueIn](er-functions-logical-valuein.md)               | تُحدد هذه الوظيفة ما إذا كان الإدخال المُحدد يطابق أي قيمة عنصر مُحدد في القائمة المُحددة. يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | تُحدد هذه الوظيفة ما إذا كان الإدخال المُحدد من النوع *Int64* أو *عدد صحيح* يطابق أي قيمة عنصر مُحدد في القائمة المُحددة. يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |


## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
