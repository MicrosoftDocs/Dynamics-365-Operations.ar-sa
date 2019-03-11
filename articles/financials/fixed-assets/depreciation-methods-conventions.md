---
title: أساليب الإهلاك والقواعد
description: توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك المعتمدة من قبل Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be8e05a386178b9172a906109e015269dc72b32e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "331105"
---
# <a name="depreciation-methods-and-conventions"></a>طرق الإهلاك والقواعد

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك المعتمدة من قبل Microsoft Dynamics 365 for Finance and Operations.

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





<a name="additional-resources"></a>الموارد الإضافية
--------

[إهلاك الأصل الثابت](fixed-asset-depreciation.md)

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



