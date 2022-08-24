---
title: ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.20 (أغسطس 2021)
description: تصف هذه المقالة الميزات الجديدة أو المتغيرة في 10.0.20. Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d99a7a7d0261ba0afd19efbb237dff329527723d
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219143"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.20 (أغسطس 2021)

[!include [banner](../includes/banner.md)]

يصف هذا المقالا الميزات الجديدة أو المتغيرة في إصدار 10.0.20 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.886، وهو يتوفر كما يلي

- **معاينة الإصدار:** مايو، 2021
- **التوفر العام للإصدار (تحديث ذاتي):** يوليو 2021
- **التوفر العام للإصدار (تحديث تلقائي):** أغسطس 2021

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. يوفر عمود *الميزة* ارتباطات إلى [خطة الإصدار](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features)، حيث يمكنك الاطلاع على تواريخ الإصدار الرسمية لكل ميزة. يوفر عمود *مزيد من المعلومات* المزيد من التفاصيل و/أو الارتباطات عن المستندات ذات الصلة.

يجب تمكين معظم هذه الميزات باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) قبل التمكن من استخدامها.

| منطقة الميزة | الميزة | معلومات إضافية |
|---|---|---|
| المخزون&nbsp;و&nbsp;اللوجستيات | [تحسين أداء تفاصيل أمر المبيعات](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | وتتيح هذه الميزة إمكانية الاستجابة لواجهة المستخدم بشكل أكبر عند فتح أوامر المبيعات، وخاصة الأوامر التي تتضمن العديد من البنود. |
| التصنيع | [استدعاء تدفقات التنفيذ التلقائي للعمليات لإنشاء أوامر الجودة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [استدعاء تدفقات التنفيذ التلقائي للعمليات لإنشاء أوامر الجودة](../production-control/process-automation-quality-orders.md ) |
| التصنيع | [واجهة تنفيذ صالة الإنتاج للتصنيع](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [تكوين واجهة تنفيذ صالة الإنتاج‬ واستخدامها](../production-control/production-floor-execution-configure.md) |
| التخطيط | [جدولة سعة غير محدودة لتحسين التخطيط](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [جدولة ذات سعة لا نهائية](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| إدارة معلومات المنتج | [إدارة التغييرات في المعادلات والمكونات الخاصة بها](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [إدارة التغييرات في المعادلات والمكونات الخاصة بها](../engineering-change-management/manage-formula-changes.md) |
| إدارة معلومات المنتج | [فحوصات جاهزية المنتج](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [جاهزية المنتج](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. ويوفر كل منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطه الإصدار](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك). إذا كنت ترغب في استخدام أي من هذه الميزات، يجب عليك تمكينها بشكل صريح في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | الميزة&nbsp;الاسم&nbsp;في إدارة&nbsp;الميزة | معلومات إضافية |
|---|---|---|
| التخطيط الرئيسي | التخويل المتوازي للتنبؤ بالطلب المعدّل | تتيح هذه الميزة تخويلاً متوازيًا للتنبؤ بالطلبات المعدلة من الصفحة **التنبؤ بالطلب المعدل**. تهدف هذه الميزة إلى زيادة الأداء عند اعتماد عدد كبير من التنبؤات. عند التخويل، يمكن للمستخدم تحديد **عدد مؤشرات الترابط** في مربع حوار التخويل. |
| التخطيط الرئيسي | تأكيد الأوامر المجمعة وأوامر التعبئة المخططة ودمجها بطريقة دُفعية. | تتيح لك هذه الميزة استخدام الوظائف الدفعية لتأكيد الأوامر المجمعة وأوامر التعبئة المخططة ودمجها. |
| التحكم بالإنتاج | نسخ المسارات العامة | تعمل هذه الميزة على تحسين وظيفة نسخ المسار للسماح للمستخدمين بنسخ المسارات التي لا تخص الصنف. وهي تمكن النظام من تحديث كافة المعلومات ذات الصلة (مثل الموقع ومجموعة المسارات ومتطلبات المصادر والأوقات المختلفة) بعد استخدام وظيفة مسار النسخ للكتابة فوق المسار الذي لم يتم تعيينه إلى أحد الأصناف حتى الآن. |
| التحكم بالإنتاج | تحديث متطلبات الموارد ذات الصلة عند تغيير عملية مسار | تسمح هذه الميزة للنظام بتحديث متطلبات الموارد ذات الصلة بعد قيام المستخدم بتغيير عملية خطوة مسار موجودة. |
| إدارة معلومات المنتج | المعالجة المسبقة لتقرير ‏‫قائمة مكونات الصنف لمنع المهلة | تؤدي هذه الميزة إلى معالجة تقرير قائمة مكونات الصنف بشكل مسبق. سيؤدي ذلك إلى تجنب مشكلات المهلة عند الحصول على حمل عمل بيانات كبير للتقرير. |
| التدبير وتحديد الموارد | تمكين إعادة تعيين عمليات سير العمل ذات الصلة بالتدبير | تتيح ميزة المعاينة هذه إمكانية إعادة تعيين عمليات سير العمل التالية إلى حاله المسودة: أمر الشراء وتغيير المورد وطلبات الشراء. |
| إدارة النقل | تمكين إنشاء دفتر يومية فواتير المورّد عند تجاهل فاتورة الشحن | عند تمكين هذه الميزة، سيتم إنشاء دفتر يومية فاتورة المورد المقابل فقط لأسباب تتعلق بالتسوية عند استخدام خيار الدفع -المورد. وبخلاف ذلك، سيتم دائمًا إنشاء دفتر يومية الفواتير. |
| إدارة المستودعات | تحقق من صحة من القوالب المحددة لمهام التزويد | تساعد هذه الميزة على ضمان قيام المستخدمين بتحديد قوالب تزويد صالحة عند إعداد وظيفة التزويد. ويمنع المستخدمين من إنشاء وظيفة تزويد بدون قالب ومن تحديد القوالب من النوع *طلب الموجة*، والذي لا يمكنه إنشاء أي عمل تزويد وقد يستغرق وقتًا طويلاً للمعالجة. |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا بإضافة مقالات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة ان تكون مرتبطة بالميزات الجديدة المضافة لهذا الإصدار ، كما هو موضح في القسم السابق ، ولكن قد يساعدك ذلك علي الحصول علي مزيد من الميزات الموجودة.

| منطقة الميزة | المقالات الجديدة أو المحدثة |
|---|---|
| إدارة التغيير الهندسي | [حالات دوره حياه المنتج وحركاتها](../engineering-change-management/product-lifecycle-state-transactions.md) |
| إدارة المخزون | [الوظيفة الإضافية لرؤية المخزون](../inventory/inventory-visibility.md)<br><br>[نظرة عامة على إدارة عدم المطابقة والجودة](../inventory/quality-management-processes.md) (بالإضافة إلى كافة مقالات إدارة الجودة ذات الصلة) |
| التدبير وتحديد الموارد | [الاحتفاظ بشهادة المورد](../../finance/public-sector/manage-vendor-certification.md) |
| التحكم بالإنتاج | [واجهة تنفيذ صالة الإنتاج](../production-control/production-floor-execution-styles.md) |
| إدارة المستودعات | [تعيين رموز وعناوين الخطوة لتطبيق الأجهزة المحمولة لـ Warehouse Management](../warehousing/step-icons-titles.md)<br><br>[المعالجة المؤجلة لحركة المخزون اليدوية](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.20 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.20 من تطبيقات التمويل والعمليات (يوليو 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.20، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: خطة الموجة 1 لإصدار 2021

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365: خطة الموجة 1 لإصدار 2021](/dynamics365-release-plan/2021wave1/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح المقال [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

