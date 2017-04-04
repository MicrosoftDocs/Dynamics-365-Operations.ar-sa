---
title: "أساليب الإهلاك والقواعد"
description: "توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك معتمدة من قبل Microsoft Dynamics AX."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>أساليب الإهلاك والقواعد

توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك معتمدة من قبل Microsoft Dynamics AX.

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
-   المعامل
-   الاستهلاك
-   المتبقي من مدة خدمة القسط الثابت
-   تقليل الرصيد بنسبة 200%
-   تقليل الرصيد بنسبة 175%
-   تقليل الرصيد بنسبة 150%
-   تقليل الرصيد بنسبة 125%

 



<a name="see-also"></a>راجع أيضًا
--------

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

[125 في المائة إهلاك الرصيد المتناقص](125-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص 150 في المائة](150-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص 175 في المائة](175-percent-reducing-balance-depreciation.md)

[200 في المائة إهلاك الرصيد المتناقص](200-percent-reducing-balance-depreciation.md)


