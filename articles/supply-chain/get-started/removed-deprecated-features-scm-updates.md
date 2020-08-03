---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597106"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

سيتم تحديث هذا الموضوع عند توثيق الميزات الجديدة أو التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Supply Chain Management

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>استخدام محرك التخطيط الرئيسي لـ Supply Chain Management لسيناريوهات التوزيع

|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | لتحسين الأداء وتصغير حمل قاعده بيانات SQL أثناء تشغيل التخطيط الرئيسي، يتم استبدال محرك التخطيط الرئيسي لـ Supply Chain Management بواسطة تحسين التخطيط. يسمح تحسين التخطيط بتشغيل التخطيط السريع الذي يمكن تنفيذه حتى أثناء ساعات العمل. ويعمل ذلك علي المخططين من التفاعل علي الفور للتغييرات في محددات الطلب أو التخطيط. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، سيحل تحسين التخطيط محل محرك التخطيط الرئيسي الحالي لـ Supply Chain Management المضمن. |
| **مناطق المنتجات المتأثرة**         | Supply Chain Management - التخطيط الرئيسي |
| **خيارات النشر**              | السحابة فقط. تحسين التخطيط غير مدعوم بعمليات النشر المحلية. |
| **الحالة**                         | مهملة. في إبريل 2021، لن يتم دعم سيناريوهات التوزيع بعد ذلك مع محرك التخطيط الرئيسي المضمّن لـ Dynamics 365 Supply Chain Management. بالنسبة لسيناريوهات التوزيع، يجب أن يستخدم العملاء تحسين التخطيط لعمليات حساب التخطيط الرئيسي. لمزيد من المعلومات، راجع [مستندات تحسين التخطيط](https://go.microsoft.com/fwlink/?linkid=2105830). وقد يستمر العملاء الذين لديهم عمليات نشر محلية لـ Dynamics 365 Supply Chain Management في استخدام محرك التخطيط الرئيسي لـ Supply Chain Management بعد أبريل 2021. ومع ذلك، لن يتم توفير المزيد من تحسينات الميزات. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها

لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
