---
title: الأبعاد المالية والحسابات الرئيسية بلغات تكتب من اليمين إلى اليسار
description: تصف هذه المقالة بعض القرارات التي ينبغي اتخاذها عند استخدام لغة ذات اتجاه من اليمين إلى اليسار، ويجب إعداد الأبعاد المالية والحسابات الرئيسية.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b1e2c0ef5cd405232332847078c70af42f056e17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866749"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>الأبعاد المالية والحسابات الرئيسية بلغات تكتب من اليمين إلى اليسار

[!include [banner](../includes/banner.md)]

تصف هذه المقالة بعض قرارات التنفيذ التي ينبغي وضعها في الاعتبار عند استخدام لغة ذات اتجاه من اليمين إلى اليسار، ويجب إعداد الأبعاد المالية والحسابات الرئيسية.

تُعد الأبعاد المالية والحسابات الرئيسية مكونات أساسية من مرحلة التخطيط في عملية التنفيذ. يتم استخدام الأبعاد المالية والحسابات الرئيسية، بعد إنشائها في النظام، في الصفحات **تكوين بنيات حساب** و **بُنى قاعدة متقدمة‬** و **تكوين الأبعاد المالية لتكامل التطبيقات‬**. يتم استخدام الترتيب الذي تم تحديده في تلك الصفحات في النظام لإدخال واستهلاك البيانات. في بعض الأماكن في النظام، تظهر الأبعاد المالية والحسابات الرئيسية في حقول منفصلة. في أماكن أخرى ، مثل دفاتر اليومية، تظهر الأبعاد المالية والحسابات الرئيسية كسلسلة واحدة.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>أفضل الممارسات لإعداد الأبعاد المالية والحسابات الرئيسية في نظام من اليمين لليسار

- عندما تعيّن محددًا لمخططات الحسابات، حدد أحد خيارات المحددات المزدوجة: واصلة مزدوجة (`--`) أو شريط مزدوج (`||`) أو نقطة مزدوجة (`..`) أو شرطة سفلية مزدوجة (`\\`).
- عندما تنشئ قيم الحسابات الرئيسية والأبعاد المالية، استخدم فقط الأرقام وأحرف اللغة من اليمين إلى اليسار.
- تجنب استخدام محدد دليل الحسابات المحدد في قيم الأبعاد المالية والحسابات الرئيسية.

يساعدك اتباع هذه الممارسات على ضمان التمثيل المتسق للترتيب المعرّف من قِبل المستخدم عبر النظام.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
