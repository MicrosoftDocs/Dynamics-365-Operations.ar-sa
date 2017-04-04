---
title: "تحديد إصدار شجرة المواد"
description: "خلال انفجار طلب، إذا كان عنصر نوع افتراضي أمر الإنتاج، يجد مشغل تخطيط إصدار شجرة مواد صالحاً استناداً إلى الموقع."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e4f5f02dfa986669decbc8854148b5eff928c2a
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-bom-version"></a>تحديد إصدار شجرة المواد

خلال انفجار طلب، إذا كان عنصر نوع افتراضي أمر الإنتاج، يجد مشغل تخطيط إصدار شجرة مواد صالحاً استناداً إلى الموقع. 

يكون بُعد الموقع معروفًا دائمًا ويتم تحديده في حركة الطلب. ويتم استخدام العملية التالية تحديد إصدار قائمة مكونات الصنف المراد استخدامه:

-   إذا تم تحديد إصدار قائمة مكونات الصنف للصنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات الصنف الخاصة بالموقع.
-   وإذا لم يتم تحديد أي إصدار لقائمة مكونات الصنف الخاصة بالموقع لأي صنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات صنف عامة. لا تحدد شجرة المواد العامة موقعًا، وهي صالحة للعديد من المواقع. وإذا كانت هناك قائمة مكونات صنف عامة، فإنه يتم استخدامها.
-   في حالة عدم وجود إصدار شجرة مواد عامة لاستخدامها، فإن تحديد إجمالي المكونات المطلوبة للطلب يتوقف عند هذه النقطة.

يجب أن يتوافق إصدار شجرة المواد الصالح مع المعايير المطلوبة للتاريخ والكمية، سواءً كان لموقع بعينه أو عامًا.




