---
title: تحديد إصدار قائمة مكونات الصنف
description: أثناء تحديد إجمالي المكونات المطلوبة للطلب، إذا تم تعيين نوع الأمر الافتراضي لصنف على الإنتاج، فإن محرك التخطيط يقوم بإيجاد إصدار قائمة مكونات صنف صالح يستند إلى الموقع.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 511d69dd1c02771840ef45e9a74aa3444b099dd2
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470347"
---
# <a name="determine-the-bom-version"></a>تحديد إصدار قائمة مكونات الصنف

[!include [banner](../includes/banner.md)]

أثناء تحديد إجمالي المكونات المطلوبة للطلب، إذا تم تعيين نوع الأمر الافتراضي لصنف على الإنتاج، فإن محرك التخطيط يقوم بإيجاد إصدار قائمة مكونات صنف صالح يستند إلى الموقع. 

يكون بُعد الموقع معروفًا دائمًا ويتم تحديده في حركة الطلب. ويتم استخدام العملية التالية تحديد إصدار قائمة مكونات الصنف المراد استخدامه:

-   إذا تم تحديد إصدار قائمة مكونات الصنف للصنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات الصنف الخاصة بالموقع.
-   وإذا لم يتم تحديد أي إصدار لقائمة مكونات الصنف الخاصة بالموقع لأي صنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات صنف عامة. لا تحدد شجرة المواد العامة موقعًا، وهي صالحة للعديد من المواقع. وإذا كانت هناك قائمة مكونات صنف عامة، فإنه يتم استخدامها.
-   في حالة عدم وجود إصدار شجرة مواد عامة لاستخدامها، فإن تحديد إجمالي المكونات المطلوبة للطلب يتوقف عند هذه النقطة.

يجب أن يتوافق إصدار شجرة المواد الصالح مع المعايير المطلوبة للتاريخ والكمية، سواءً كان لموقع بعينه أو عامًا.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]