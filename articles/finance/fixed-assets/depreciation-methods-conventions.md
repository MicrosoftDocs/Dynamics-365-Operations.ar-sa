---
title: أساليب الإهلاك والقواعد
description: توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك التي يدعمها Microsoft Dynamics 365 Finance.
author: moaamer
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 066e571485602907d167b2ed1f7530b2285a02b6
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714162"
---
# <a name="depreciation-methods-and-conventions"></a>أساليب الإهلاك والقواعد

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك المعتمدة.

يُمكنك تحديد أساليب وقواعد إهلاك متعددة. تهدف هذه الطرق إلى تخصيص القيمة الممكن إهلاكها للأصل الثابت إلى فترات مالية. والقيمة الممكن إهلاكها للأصل الثابت هي عبارة عن سعر الامتلاك الذي يتم خصم قيمة الخردة منه، إن وُجدت. 

إذا كنت تستخدم قواعد الإهلاك وقمت بتعديل تاريخ تشغيل آخر إهلاك لأحد الأصول، والذي يؤدي إلى تخطي بعض عمليات الإهلاك، فقد يزيد إهلاك العام الأخير أو يقل عما هو مُتوقع. ويتم تعديل الإهلاك بعدد فترات الإهلاك التي تأثرت بتعديل آخر تاريخ لتشغيل الإهلاك.

على سبيل المثال، إذا كنت تستخدم قاعدة الإهلاك نصف السنوية على مدار ثلاث سنوات، فسيقع الإهلاك عادةً على مدار 3 سنوات ونصف. وإذا قمت بتغيير آخر تاريخ لتشغيل الإهلاك خلال مدة 3 سنوات ونصف، فسيخرج العام الأخير للإهلاك عن عدد الفترات المتأثرة. وفي حالة تقديم التاريخ بثلاثة أشهر، فسيشتمل العام الأخير على تسعة أشهر تستحق الإهلاك، في حين أنه يكون هناك عادةً ستة أشهر تستحق الإهلاك.

ويُمكنك الاختيار من بين قواعد الإهلاك التالية.


-   نصف السنة
-   شهر كامل
-   منتصف الربع
-   منتصف الشهر (أول الشهر)
-   منتصف الشهر(الخامس عشر من الشهر)
-   نصف السنة (بداية السنة)
-   نصف سنة (السنة التالية)

يمكنك التحديد من طرق الإهلاك التالية.
-   مدة خدمة القسط الثابت
-   تقليل الرصيد
-   يدوي
-   العامل‬
-   الاستخدام
-   المتبقي من مدة خدمة القسط الثابت
-   تقليل الرصيد بنسبة 200%
-   تقليل الرصيد بنسبة 175%
-   تقليل الرصيد بنسبة 150%
-   تقليل الرصيد بنسبة 125%





## <a name="additional-resources"></a>الموارد الإضافية

[إهلاك الأصل الثابت](fixed-asset-depreciation.md)

[إهلاك مدة خدمة القسط الثابت](Straight-line-service-life-depreciation.md)

[إهلاك القسط المتناقص](reduce-balance-depreciation.md)

[الإهلاك اليدوي](manual-depreciation.md)

[إهلاك العامل](factor-depreciation.md)

[إهلاك الاستهلاك](consumption-depreciation.md)

[إهلاك المتبقي من مدة خدمة القسط الثابت](straight-line-life-remaining-depreciation.md)

[إهلاك القسط المتناقص بنسبة 125 بالمئة](125-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 150 بالمائة](150-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 175 بالمائة](175-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 200 بالمائة](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
