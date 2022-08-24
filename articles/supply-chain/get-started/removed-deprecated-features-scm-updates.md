---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management
description: يصف هذا المقال الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f70d05f5663d8249b2435ad353421c278692a9ac
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218791"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

سيتم تحديث هذا المقال عند توثيق الميزات الجديدة أو التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات التمويل والعمليات في [التقارير المرجعية التقنية](/dynamics/s-e/). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات التمويل والعمليات.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.29 من Supply Chain Management

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>أوامر تحويل المخزون التي تخضع لضريبة على سعر التحويل

| &nbsp;  | &nbsp;  |
|---|---|
| **سبب الإهلاك/الإزالة** | يتم استبدال أوامر تحويل المخزون [التي تحتوي علي ضريبة في وظيفة سع ](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) التحويل بواسطة أوامر تحويل المخزون [الخاصة بوظيفة الهند](../../finance/localizations/apac-ind-stock-transfer.md). |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم يتم استبدال أوامر تحويل المخزون [التي تحتوي علي ضريبة في وظيفة سع](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) التحويل بواسطة أوامر تحويل المخزون [الخاصة بوظيفة الهند](../../finance/localizations/apac-ind-stock-transfer.md). |
| **مناطق المنتجات المتأثرة** | Supply Chain Management - المخزون |
| **خيارات النشر** | السحابة ومحلي |
| **Status** | <p>يجري مهملة. لن *تتلقي أوامر تحويل المخزون التي تحتوي علي ضريبة في وظيفة سعر* التحويل بعد الآن استقبال الدعم مع إصلاحات الأخطاء وإصلاحات الأمان.</p><p>بعد أبريل 2023، سيطلب من العملاء استخدام الوظائف المحسنة ، وهي *أوامر تحويل المخزون للهند* بشكل افتراضي. بعد 2023 أكتوبر *لن تكون أوامر تحويل المخزون* لن تكون الوظيفة متاحة بعد الآن ، وسيُطلب من العملاء الانتقال إلى الوضع المحسن لوظيفة *أوامر تحويل* المخزون.</p><p>لمزيد من المعلومات ، راجع [أوامر تحويل المخزون للهند](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.19 من Supply Chain Management

### <a name="job-card-device"></a>جهاز بطاقة الوظيفة

| &nbsp;  | &nbsp;  |
|---|---|
| **سبب الإهلاك/الإزالة** | يتم استبدال [جهاز بطاقة الوظيفة](../production-control/config-job-card-device.md) بواسطة [واجهة تنفيذ صالة الإنتاج الجديدة](../production-control/production-floor-execution-configure.md). |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، ينبغي استبدال [جهاز بطاقة الوظيفة](../production-control/config-job-card-device.md) بواسطة [واجهة تنفيذ صالة الإنتاج الجديدة](../production-control/production-floor-execution-configure.md). |
| **مناطق المنتجات المتأثرة** | Supply Chain Management - التحكم في الإنتاج |
| **خيارات النشر** | السحابة ومحلي |
| **الحالة** | مهملة. سيتلقى جهاز بطاقة العمل الدعم من خلال إصلاحات الأخطاء والأمان، ولكن لن يتم توفير تحسينات الميزات. بعد أبريل 2022، لن يتم دعم جهاز بطاقة العمل وسيُطلب من العملاء الانتقال إلى واجهة تنفيذ أرضية الإنتاج الجديدة. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.18 من Supply Chain Management

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>إدارة سلسلة التوريد - التخزين (تطبيق المستودع)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | اعتبارًا من أبريل 2021، *إدارة سلسلة التوريد - التخزين* تم إيقاف (تطبيق المستودع) ولن يتم دعمه بعد نيسان (أبريل) 2022. وقد تم استبداله الآن بواسطة *تطبيق إدارة المستودع للأجهزة المحمولة*، الذي تم إصداره مع إصدار 10.0.17 من Supply Chain Management. التطبيق الجديد هو استبدال كامل ولكن يستخدم نفس اطار العمل الأساسي، الذي يجعل الترحيل سهل. وفي حاله الضرورة، يمكن استخدام التطبيقين جنبا إلى جنب لمساعده المستخدمين علي الضبط بالتدريجي عند التعرف علي استخدام التطبيق الجديد.<br><br>لمزيد من المعلومات حول تطبيق إدارة المستودع للأجهزة المحمولة الجديد، راجع [تطبيق إدارة المستودع للأجهزة المحمولة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) و[تثبيت وتوصيل تطبيق إدارة المستودع للأجهزة المحمولة](../warehousing/install-configure-warehouse-management-app.md). |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، تم استبداله بتطبيق "إدارة المستودعات" الجديد للأجهزة المحمولة. |
| **مناطق المنتجات المتأثرة**         | Supply Chain Management - تطبيق المستودع |
| **خيارات النشر**              | السحابة ومحلي |
| **الحالة**                         | مهملة. سيتلقى تطبيق المستودع الدعم مع الأخطاء وإصلاحات الأمان، ولكن لن يتم توفير تحسينات الميزات بعد الآن. بعد أبريل 2022، لن يتم دعم تطبيق المستودع القديم وسيُطلب من العملاء الانتقال إلى تطبيق إدارة المستودع للأجهزة المحمولة الجديد. ستتم أزاله تطبيق المستودع القديم من متجر Microsoft Store وGoogle Play.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.15 من Supply Chain Management

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>تم إهمال دعم Internet Explorer 11 لـ Dynamics 365

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | اعتبارًا من ديسمبر 2020، تم إهمال دعم Microsoft Internet Explorer 11 لجميع منتجات Dynamics 365، ولن يتم دعم Internet Explorer 11 بعد أغسطس 2021.<br><br>سيؤثر هذا الاجراء علي العملاء الذين يستخدمون منتجات Dynamics 365 التي تم تصميمها ليتم استخدامها من خلال واجهة Internet Explorer 11. بعد أغسطس 2021، لن يتم دعم Internet Explorer 11 لمنتجات Dynamics 365. |
| **هل تم الاستبدال بميزة أخرى؟**   | نوصي العملاء بالانتقال إلى Microsoft Edge.|
| **مناطق المنتجات المتأثرة**         | كافة منتجات Dynamics 365 |
| **خيارات النشر**              | ‏‏الكل|
| **الحالة**                         | مهملة. لن يتم دعم Internet Explorer 11 بعد (أغسطس) 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>استخدام محرك التخطيط الرئيسي لـ Supply Chain Management لسيناريوهات التصنيع

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | لتحسين الأداء وتصغير حمل قاعده بيانات SQL أثناء تشغيل التخطيط الرئيسي، يتم استبدال محرك التخطيط الرئيسي لـ Supply Chain Management بواسطة تحسين التخطيط. يسمح تحسين التخطيط بتشغيل التخطيط السريع الذي يمكن تنفيذه حتى أثناء ساعات العمل. ويعمل ذلك علي المخططين من التفاعل علي الفور للتغييرات في محددات الطلب أو التخطيط. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، سيحل تحسين التخطيط محل محرك التخطيط الرئيسي الحالي لـ Supply Chain Management المضمن. |
| **مناطق المنتجات المتأثرة**         | Supply Chain Management - التخطيط الرئيسي |
| **خيارات النشر**              | السحابة فقط. تحسين التخطيط غير مدعوم بعمليات النشر المحلية. |
| **الحالة**                         | مهملة. بحلول 1 إبريل 2022، لن يتم دعم سيناريوهات التصنيع لمحرك التخطيط الرئيسي المضمّن في Supply Chain Management. اعتبارًا من ذلك التاريخ، ستوقف Microsoft جميع عمليات التطوير النشطة في سيناريوهات التصنيع لمحرك التخطيط الضمّن، ولن تصدر أي ميزات جديدة، وستصدر فقط إصلاحات الأخطاء الهامة. بعد هذا التاريخ، يجب على جميع الشركات التي تتطلب دعمًا لسيناريوهات التصنيع استخدام "تحسين التخطيط" لحسابات التخطيط الرئيسية لديها. من المتوقع أن يدعم تحسين التخطيط سيناريوهات التصنيع بشكل كامل بحلول أكتوبر 2022. لمزيد من المعلومات، راجع [وثائق تحسين التخطيط](../master-planning/planning-optimization/planning-optimization-overview.md).<br><br>قد تواصل الشركات التي لديها عمليات نشر محلية لـ Supply Chain Management استخدام محرك التخطيط الرئيسي المضمّن لسيناريوهات التصنيع بعد أبريل 2022. ومع ذلك، لن يتم توفير المزيد من تحسينات الميزات. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Supply Chain Management

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>استخدام محرك التخطيط الرئيسي لـ Supply Chain Management لسيناريوهات التوزيع

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | لتحسين الأداء وتصغير حمل قاعده بيانات SQL أثناء تشغيل التخطيط الرئيسي، يتم استبدال محرك التخطيط الرئيسي لـ Supply Chain Management بواسطة تحسين التخطيط. يسمح تحسين التخطيط بتشغيل التخطيط السريع الذي يمكن تنفيذه حتى أثناء ساعات العمل. ويعمل ذلك علي المخططين من التفاعل علي الفور للتغييرات في محددات الطلب أو التخطيط. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم، سيحل تحسين التخطيط محل محرك التخطيط الرئيسي الحالي لـ Supply Chain Management المضمن. |
| **مناطق المنتجات المتأثرة**         | Supply Chain Management - التخطيط الرئيسي |
| **خيارات النشر**              | السحابة فقط. تحسين التخطيط غير مدعوم بعمليات النشر المحلية. |
| **الحالة**                         | مهملة. في 1 إبريل 2021، لن يتم دعم سيناريوهات التوزيع بعد ذلك مع محرك التخطيط الرئيسي المضمّن لـ Dynamics 365 Supply Chain Management. بالنسبة لسيناريوهات التوزيع، يجب أن يستخدم العملاء تحسين التخطيط لعمليات حساب التخطيط الرئيسي. لمزيد من المعلومات، راجع [مستندات تحسين التخطيط](../master-planning/planning-optimization/planning-optimization-overview.md). وقد يستمر العملاء الذين لديهم عمليات نشر محلية لـ Dynamics 365 Supply Chain Management في استخدام محرك التخطيط الرئيسي لـ Supply Chain Management بعد أبريل 2021. ومع ذلك، لن يتم توفير المزيد من تحسينات الميزات. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها

لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

