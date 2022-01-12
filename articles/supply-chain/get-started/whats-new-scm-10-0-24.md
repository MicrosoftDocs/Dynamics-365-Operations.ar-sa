---
title: معاينة Dynamics 365 Supply Chain Management 10.0.24 (فبراير 2022)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.24 من Microsoft Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f6402d7f9f433ca621c475bd62553529943dbe62
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920538"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10024-february-2022"></a>معاينة Dynamics 365 Supply Chain Management 10.0.24 (فبراير 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في معينة الإصدار 10.0.24 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.1084، وهو يتوفر كما يلي

- **معاينة الإصدار الأولي:** ديسمبر 2021
- **التوفر العام للإصدار (تحديث ذاتي):** يناير 2022
- **التوفر العام للإصدار (تحديث تلقائي):** فبراير 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تم إدراجها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| المخطط المختلط الموزع | [أحمال عمل تنفيذ المستودع المعززة في وحدات القياس](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [أحمال عمل إدارة المستودعات لوحدات نطاق السحابة والحافة](../cloud-edge/cloud-edge-workload-warehousing.md) | ممكن افتراضيا. |
| التخطيط | [دعم تحسين التخطيط ل‏‫إعادة ترتيب هامش الإصدار والموضوع](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [حدود الأمان](../master-planning/planning-optimization/safety-margins.md) | ممكن افتراضيا. |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. وتوفر كل واحدة منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطة الإصدار](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك).

إذا كنت ترغب في تشغيل أي من هذه الميزات أو إيقاف تشغيلها، فإنه يجب عليك القيام بذلك في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | اسم الميزة في إدارة الميزات | معلومات إضافية |
|---|---|---|
| التحكم بالإنتاج | فحص توفر المادة حسب الطلب لأوامر الإنتاج | وتجعل هذه الميزة من الأسرع فتح الصفحة **أوامر الإنتاج للإصدار**، والتي تتوفر من مساحة العمل **إداره طابق الإنتاج**. وبدون هذه الميزة، يقوم النظام تلقائيًا بالتحقق مما إذا كانت المواد متوفرة لكافة أوامر الإنتاج المدرجة بمجرد فتح الصفحة، الأمر الذي قد يستغرق وقتًا طويلاً إذا كان لديك عدد كبير من الطلبات. عند تمكين هذه الميزة، يقوم النظام بدلاً من ذلك بتوفير زر شريط الأدوات، والذي يمكنك استخدامه لبدء المواد التي يتم التحقق منها فقط من أجل الأوامر المحددة وعند الحاجة. |
| التحكم بالإنتاج | (إصدار أولي) تسجيل استهلاك المواد في واجهة تنفيذ طابق الإنتاج (خلاف WMS) | تعمل هذه الميزة على تمكين العاملين من استخدام واجهة تنفيذ صالة الإنتاج لتسجيل استهلاك المواد وأرقام الدُفعات والأرقام التسلسلية. لا تدعم هذه الميزة إلا الأصناف التي لم يتم تمكينها لاستخدام عمليات المستودع المتقدمة (WMS). تتم جدولة دعم الأصناف التي تم تمكينها لاستخدام عمليات المستودع المتقدمة (WMS) لإصدار مستقبلي.<p>تحتاج بعض الشركات المصنعة، وخاصة داخل صناعات العملية، إلى تسجيل مقدار المواد المستهلكة بشكل صريح لكل دفعة أو أمر إنتاج. على سبيل المثال، قد يستخدم العاملون مقياسًا لوزن مقدار المواد المستهلكة عند العمل. لضمان إمكانية التتبع الكاملة للمواد، ، تحتاج هذه المؤسسات أيضًا إلى تسجيل أرقام الدفعات التي تم استهلاكها عند إنتاج كل منتج. |
| التحكم بالإنتاج | الإبلاغ كمنته في حمل عمل لـ warehouse management لوحدة قياس السحابة والحافة | تتيح هذه الميزة للعمال استخدام تطبيق Warehouse Management للأجهزة المحمولة للإبلاغ عن إنتاج أو أمر دفعة كمنته عند تشغيل التطبيق مقابل حمل عمل لـ warehouse management على وحدة مقياس السحابة والحافة. لمزيد من المعلومات، راجع [‏‫الإبلاغ كمنته والتخزين على وحدة المقياس‬](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| التحكم بالإنتاج | بدء أمر إنتاج في حمل عمل لـ warehouse management لوحدة قياس السحابة والحافة | تمكن هذه الميزة العمال من استخدام تطبيق Warehouse Management للأجهزة المحمولة لبدء إنتاج أو أمر دفعة كمنته عند تشغيل التطبيق مقابل حمل عمل لـ warehouse management على وحدة مقياس السحابة والحافة. |
| Warehouse management | صفحات جدول عمل تخطيط الحِمل الجديدة | تمكين صفحتين من صفحات جدول عمل تخطيط التحميل الجديدة: **جدول عمل تخطيط التحميل الداخلي** و **جدول عمل تخطيط الحمل الصادر**. |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا باضافه موضوعات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة أن تكون هذه الموضوعات مرتبطة بالميزات الجديدة التي تمت إضافتها لهذا الإصدار، كما هو موضح في القسم السابق. ومع ذلك، قد تساعدك في الحصول على مزيد من الميزات الموجودة.

| منطقة الميزة | الموضوعات الجديدة أو المحدثة |
|---|---|
| إدارة التكلفة | [تقارير قيمة المخزون](../cost-management/inventory-value-report-storage.md) |
| إدارة التكلفة | [أمثلة تقرير قيمة المخزون والمنطق](../cost-management/inventory-value-report-examples.md) |
| التخطيط الرئيسي | [معلمات التاريخ والوقت المستخدمة في تحسين التخطيط](../master-planning/planning-optimization/date-time-used.md) |
| التخطيط الرئيسي | [إعداد التنبؤ بالطلب](../master-planning/demand-forecasting-setup.md) |
| التخطيط الرئيسي | [استخدام دفتر يومية المخزون الآمن لتحديث الحد الأدنى من التغطية للعناصر](../master-planning/safety-stock-journal.md) |
| التحكم بالإنتاج | [تخصيص واجهة تنفيذ صالة الإنتاج‬ واستخدامها](../production-control/production-floor-execution-customize.md) |
| التحكم بالإنتاج | [واجهة تنفيذ صالة الإنتاج](../production-control/production-floor-execution-styles.md) |
| المبيعات والتسويق | [تحسينات في أداء تنظيف محفوظات المبيعات](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Warehouse management | [حسابات مستخدم الجهاز المحمول](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديث النظام الأساسي لتطبيقات Finance and Operations

يتضمن الإصدار 10.0.24 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.24 من تطبيقات Finance and Operations (نوفمبر 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.24، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2021

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2021](/dynamics365-release-plan/2021wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح الموضوع [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في الموضوع [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
