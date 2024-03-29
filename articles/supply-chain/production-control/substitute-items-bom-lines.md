---
title: استبدال المواد في التصنيع
description: يوضح هذا المقال كيفية استبدال المواد أثناء عملية الإنتاج.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c2e6c9cc8ed85c8c60539b37fb6c51c96bc2872
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855967"
---
# <a name="material-substitution-in-manufacturing"></a>استبدال المواد في التصنيع

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفية استبدال المواد أثناء عملية الإنتاج. 

هناك ثلاث طرق لاستبدال المواد أثناء عملية الإنتاج:

-   حسب التاريخ، عندما يتم استبدال مادة واحدة بأخرى بعد تاريخ معين
-   أثناء التخطيط الرئيسي، عند استبدال مادة في معادلة بمادة أخرى، لأنها نفدت من المخزون
-   أثناء الإنتاج، عند نفاد مادة بشكل غير متوقع من المخزون واستبدالها بمادة أخرى

## <a name="substituting-material-by-date"></a>استبدال المواد حسب التاريخ
‏‫فكر في السيناريو التالي: يحتوي جهاز تقوم بشركة بتصنيعه على مكون ستنتهي صلاحيته في غضون شهرين من كتالوج المورّد. ومن تاريخ انتهاء الصلاحية فصاعدًا، سوف يقدم المورد مكونًا جديدًا يمكن أن يكون بديلاً للمكون القديم.‬ يمكن إعداد تواريخ من وإلى الصلاحية على بنود قائمة مكونات الصنف (BOM). على سبيل المثال، يمكنك إعداد المكون القديم بحيث تنتهي صلاحيته بإدخال تاريخ انتهاء الصلاحية في الحقل **إلى تاريخ**. ثم في قائمة مكونات الصنف، يمكنك إعداد المكون البديل الجديد بحيث يكون صالحاً من اليوم بعد انتهاء صلاحية المكون القديم. وللقيام بذلك، أدخل تاريخ البدء في الحقل **من تاريخ**.

## <a name="substituting-material-by-planning"></a>استبدال المواد حسب التخطيط
يمكنك استبدال المواد أثناء التخطيط فقط عند استخدام المعادلات، وليس عند استخدام قائمة مكونات صنف. النظر في اتباع السيناريو: تقوم شركة تصنيع أغذية بتصنيع صلصة من معادلة تشتمل على 20 مكونًا. ويمكن استبدال مكون واحد في المعادلة بمكون واحد من مكونين آخرين. ومع ذلك، ولأن هذان المكونان أغلى من المكون المفضل، فإنه يتم استخدام الاستبدال فقط في حالة نفاد مخزون المكون المفضل. تُسمى المادة التي يمكن استبدالها أ، بينما تُسمى المادتين التي يمكن أن تحلا محلها ب وج. ويتم التحكم في استبدال المواد حسب التخطيط بواسطة حقلي **مجموعة الخطط** و **الأولوية** في بنود المعادلة. على سبيل المثال، تُنشئ بنود معادلة للمواد الثثة، وتُقرن بنود المعادلة بنفس مجموعة الخطط. وأثناء الإعداد، يكون لبند لمعادلة الخاص بالمادة أ الأولوية الأعلى (الرقم الأدنى)، ويكون لبند المعادلة الخاص بالمادة ج الأولوية الأدنى، ويكون لبند المعادلة الخاص بالمادة ب أولوية بين أولوية البندين الآخرين. وإذا كان لديك طلب خاص بالصنف المنتهي، يحدد التخطيط الرئيسي أولاً ما إذا كان يمكن تغطية طلب المادة أ. إذا كان الطلب لا يمكن تغطيته، يبحث التخطيط الرئيسي في المادتين ب وج، بترتيب الأولويات. إذا كانت المادة ب متوفرة، فسيتم استخدامها بعد تأكيد أمر دُفعة مخطط للمعادلة. في حالة توفر أي مادة من المواد، يُنشئ التخطيط الرئيسي أمرًا مخططًا للمادة أ. **ملاحظة:** عند إعداد بنود المعادلة في مجموعة خطط،، يجب عليك تحديد الكمية فقط فيما يتعلق بالمادة ذات الأولوية الأعلى. وسيتم استخدام هذه الكمية لحساب طلب جميع المواد في الخطة، حتى المواد التي لها أولوية منخفضة. ولا يمكنك تحديد كميات مختلفة فيما يتعلق بالأصناف ذات الأولوية الأدنى في مجموعة الخطط.

## <a name="substituting-material-during-production"></a>استبدال المادة أثناء الإنتاج
أطلع على السيناريو التالي: جزء من اللوح المعدني مطلوب لعملية لحام. أثناء العملية، يُخبر عامل مستودع مشغل الآلة بنفاد اللوح في المخزون. ومع ذلك، تقرر أنه يمكن استبدال اللوح بلوح أكبر سمكًا قليلاً. وبهذه الطريقة، يمكن إنهاء العملية. ويمكن إضافة مادة إلى قائمة مكونات الصنف لأمر إنتاج مفتوح. إذا كان أمر الإنتاج بحالة **تم بدء التشغيل**، فإنه تتم مطالبة المستخدمين بإعادة تقدير الأمر عند إضافة صنف جديد إلى قائمة مكونات صنف الإنتاج. بعد إضافة المادة، يمكنك إنشاء قائمة انتقاء جديدة للصنف الجديد. ولا يلزمك إضافة المادة الجديدة إلى قائمة مكونات صنف الإنتاج. بدلاً من ذلك، يمكنك إضافتها إلى قائمة انتقاء الإنتاج مباشرةً. وفيما بعد عندما يتم ترحيل قائمة الانتقاء، يضيف النظام المادة إلى قائمة مكونات صنف الإنتاج.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]