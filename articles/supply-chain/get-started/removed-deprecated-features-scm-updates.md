---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 9c91ffcb03793db2f2ef3a9631ab549ace3f735d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259081"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

سيتم تحديث هذا الموضوع عند توثيق الميزات الجديدة أو التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://docs.microsoft.com/dynamics/s-e/). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.15 من Supply Chain Management

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>تم إهمال دعم Internet Explorer 11 لـ Dynamics 365

|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | اعتبارًا من ديسمبر 2020، تم إهمال دعم Microsoft Internet Explorer 11 لجميع منتجات Dynamics 365، ولن يتم دعم Internet Explorer 11 بعد أغسطس 2021.<br><br>سيؤثر هذا الاجراء علي العملاء الذين يستخدمون منتجات Dynamics 365 التي تم تصميمها ليتم استخدامها من خلال واجهة Internet Explorer 11. بعد أغسطس 2021، لن يتم دعم Internet Explorer 11 لمنتجات Dynamics 365. |
| **هل تم الاستبدال بميزة أخرى؟**   | نوصي العملاء بالانتقال إلى Microsoft Edge.|
| **مناطق المنتجات المتأثرة**         | كافة منتجات Dynamics 365 |
| **خيارات النشر**              | ‏‏الكل|
| **الحالة**                         | مهملة. لن يتم دعم Internet Explorer 11 بعد (أغسطس) 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>استخدام محرك التخطيط الرئيسي لـ Supply Chain Management لسيناريوهات التصنيع

|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | لتحسين الأداء وتصغير حمل قاعده بيانات SQL أثناء تشغيل التخطيط الرئيسي، يتم استبدال محرك التخطيط الرئيسي لـ Supply Chain Management بواسطة تحسين التخطيط. يسمح تحسين التخطيط بتشغيل التخطيط السريع الذي يمكن تنفيذه حتى أثناء ساعات العمل. ويعمل ذلك علي المخططين من التفاعل علي الفور للتغييرات في محددات الطلب أو التخطيط. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، سيحل تحسين التخطيط محل محرك التخطيط الرئيسي الحالي لـ Supply Chain Management المضمن. |
| **مناطق المنتجات المتأثرة**         | Supply Chain Management - التخطيط الرئيسي |
| **خيارات النشر**              | السحابة فقط. تحسين التخطيط غير مدعوم بعمليات النشر المحلية. |
| **الحالة**                         | مهملة. في 1 أكتوبر 2021، لن يتم دعم سيناريوهات التصنيع بعد ذلك مع محرك التخطيط الرئيسي المضمّن لـ Dynamics 365 Supply Chain Management. بالنسبة لسيناريوهات التصنيع، يجب أن يستخدم العملاء تحسين التخطيط لعمليات حساب التخطيط الرئيسي. لمزيد من المعلومات، راجع [مستندات تحسين التخطيط](https://go.microsoft.com/fwlink/?linkid=2105830). وقد يستمر العملاء الذين لديهم عمليات نشر محلية لـ Dynamics 365 Supply Chain Management في استخدام محرك التخطيط الرئيسي لسيناريوهات التصنيع بعد أكتوبر 2021. ومع ذلك، لن يتم توفير المزيد من تحسينات الميزات. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Supply Chain Management

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>استخدام محرك التخطيط الرئيسي لـ Supply Chain Management لسيناريوهات التوزيع

|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | لتحسين الأداء وتصغير حمل قاعده بيانات SQL أثناء تشغيل التخطيط الرئيسي، يتم استبدال محرك التخطيط الرئيسي لـ Supply Chain Management بواسطة تحسين التخطيط. يسمح تحسين التخطيط بتشغيل التخطيط السريع الذي يمكن تنفيذه حتى أثناء ساعات العمل. ويعمل ذلك علي المخططين من التفاعل علي الفور للتغييرات في محددات الطلب أو التخطيط. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، سيحل تحسين التخطيط محل محرك التخطيط الرئيسي الحالي لـ Supply Chain Management المضمن. |
| **مناطق المنتجات المتأثرة**         | Supply Chain Management - التخطيط الرئيسي |
| **خيارات النشر**              | السحابة فقط. تحسين التخطيط غير مدعوم بعمليات النشر المحلية. |
| **الحالة**                         | مهملة. في 1 إبريل 2021، لن يتم دعم سيناريوهات التوزيع بعد ذلك مع محرك التخطيط الرئيسي المضمّن لـ Dynamics 365 Supply Chain Management. بالنسبة لسيناريوهات التوزيع، يجب أن يستخدم العملاء تحسين التخطيط لعمليات حساب التخطيط الرئيسي. لمزيد من المعلومات، راجع [مستندات تحسين التخطيط](https://go.microsoft.com/fwlink/?linkid=2105830). وقد يستمر العملاء الذين لديهم عمليات نشر محلية لـ Dynamics 365 Supply Chain Management في استخدام محرك التخطيط الرئيسي لـ Supply Chain Management بعد أبريل 2021. ومع ذلك، لن يتم توفير المزيد من تحسينات الميزات. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها

لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]