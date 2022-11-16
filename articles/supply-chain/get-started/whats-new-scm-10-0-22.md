---
title: ما الجديد أو المتغير في الإصدار 10.0.22 من Dynamics 365 Supply Chain Management (نوفمبر 2021)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في 10.0.22. Microsoft Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b95f131a45c11748cfd4c66c47e5a51c765ed486
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740400"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>ما الجديد أو المتغير في الإصدار 10.0.22 من Dynamics 365 Supply Chain Management (نوفمبر 2021)

[!include [banner](../includes/banner.md)]

تصف هذا المقالات الميزات الجديدة أو المتغيرة في إصدار 10.0.22 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.995، وهو يتوفر كما يلي

- **معاينة الإصدار:** سبتمبر 2021
- **التوفر العام للإصدار (تحديث ذاتي):** أكتوبر 2020
- **التوفر العام للإصدار (تحديث تلقائي):** نوفمبر 2021

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. يوفر عمود *الميزة* ارتباطات إلى [خطة الإصدار](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)، حيث يمكنك الاطلاع على تواريخ الإصدار الرسمية لكل ميزة. يوفر عمود *مزيد من المعلومات* المزيد من التفاصيل و/أو الارتباطات عن المستندات ذات الصلة. لتحديد كيفية تشغيل إحدى الميزات، راجع عمود *تم التمكين بواسطة*. لمزيد من المعلومات حول كيفية استخدام إدارة الميزات، راجع [نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). قد نقوم بتحديث هذا المقال ليشمل الميزات التي تم إدراجها في البناء بعد أن يتم نشر هذا المقال في البداية.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| التخطيط | [دعم تحسين التخطيط لتخصيص الموارد المستندة إلى القدرات](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [الجدولة باستخدام تحديد المورد بالاستناد إلى القدرة](../master-planning/planning-optimization/capability-based-scheduling.md) | إدارة الميزات (*جدولة سعة غير محدودة لتحسين التخطيط*) |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. وتوفر كل واحدة منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطة الإصدار](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك). إذا كنت ترغب في استخدام أي من هذه الميزات، يجب عليك تمكينها بشكل صريح في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | اسم الميزة في إدارة الميزات | معلومات إضافية |
|---|---|---|
| المخطط المختلط الموزع | *(لا يلزم إدارة الميزات.)* | <p>ويقوم هذا الإصدار بتوسيع إمكانيات تخطيط التحميل الصادرة لحمل عمل إدارة المستودع لوحدات مقياس السحابة والحافة.</p><p>للحصول على مزيد من المعلومات، راجع [أحمال عمل إدارة المستودعات لوحدات قياس السحابة والحافة](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| إدارة التغيير الهندسي | إنشاء متغيرات للمنتجات الهندسية | <p>تتيح لك هذه الميزة إنشاء متغيرات متعددة لمنتج هندسي، استناداً إلى اللون أو الحجم أو النمط أو أبعاد التكوين الخاصة به.</p><p>لمزيد من المعلومات ، راجع [إنشاء متغيرات لمنتجات الهندسة](../engineering-change-management/engineering-variants.md).</p> |
| إدارة المخزون والمستودعات | تكامل رؤية المخزون مع تعويض الحجز | <p>لا يمكن تمكين هذه الميزة إلا بعد تمكين ميزة *تكامل رؤية المخزون*. وهي توفر وظائف لتعويض الحجوزات التي يتم إجراؤها في رؤية المخزون.</p><p>لمزيد من المعلومات، راجع [حجوزات رؤية المخزون](../inventory/inventory-visibility-reservations.md).</p> |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا بإضافة مقالات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة أن تكون هذه المقالات مرتبطة بالميزات الجديدة التي تمت إضافتها لهذا الإصدار، كما هو موضح في القسم السابق. ومع ذلك، قد تساعدك في الحصول على مزيد من الميزات الموجودة.

| منطقة الميزة | المقالات الجديدة أو المحدثة |
|---|---|
| إدارة التغيير الهندسي | [نظرة عامة حول إدارة تغيير الهندسة](../engineering-change-management/product-engineering-overview.md) الآن تسرد كافة الميزات الاختيارية المتوفرة في إدارة الميزات |
| التخطيط الرئيسي | [إعداد التنبؤ بالطلب](../master-planning/demand-forecasting-setup.md) |
| التخطيط الرئيسي | [صافي المتطلبات ومعلومات تثبيت السعر](../master-planning/planning-optimization/net-requirements.md) |
| Warehouse management | [الإصدار إلى المستودع](../warehousing/release-to-warehouse-process.md) يوفر نظرة عامة مفصلة حول عملية الإصدار إلى المستودع الكاملة |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.22 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.22 من تطبيقات التمويل والعمليات (نوفمبر 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.22، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2021

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2021](/dynamics365-release-plan/2021wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح المقال [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

