---
title: "أساليب الإهلاك والقواعد"
description: "توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك التي يدعمها Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d802933f29b3e08704480035925b2fbf6743e996
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="depreciation-methods-and-conventions"></a>أساليب الإهلاك والقواعد

[!include[banner](../includes/banner.md)]


توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك التي يدعمها Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

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

[إهلاك الأصول الثابتة‬](fixed-asset-depreciation.md)

[إهلاك مدة خدمة القسط الثابت](Straight-line-service-life-depreciation.md)

[إهلاك القسط المتناقص](reduce-balance-depreciation.md)

[الإهلاك اليدوي](manual-depreciation.md)

[إهلاك العامل](factor-depreciation.md)

[إهلاك الاستهلاك](consumption-depreciation.md)

[إهلاك المتبقي من مدة خدمة القسط الثابت](straight-line-life-remaining-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 125 بالمائة](125-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 150 بالمائة](150-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 175 بالمائة](175-percent-reducing-balance-depreciation.md)

[إهلاك الرصيد المتناقص بنسبة 200 بالمائة](200-percent-reducing-balance-depreciation.md)




