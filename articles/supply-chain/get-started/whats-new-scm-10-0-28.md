---
title: ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.28 (أغسطس 2022)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في 10.0.28. Microsoft Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 184da494b9998e3e1cf6bd1639b452192d7e7857
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427784"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.28 (أغسطس 2022)

[!include [banner](../includes/banner.md)]

يصف هذا المقالا الميزات الجديدة أو المتغيرة في إصدار 10.0.28 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.1264، وهو يتوفر وفق الجدول التالي:

- **معاينة الإصدار:** مايو، 2022
- **التوفر العام للإصدار (تحديث ذاتي):** يوليو 2022
- **التوفر العام للإصدار (تحديث تلقائي):** يوليو 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تمت إضافتها إلى البنية بعد نشر هذا الموضوع.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| المخزون واللوجستيات | [كيانات تكامل التكلفة شاملة التفريغ لوكلاء الشحن التابعين لجهات خارجية](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [نظرة عامة على كيانات التكاليف شاملة التفريغ](../landed-cost/landed-cost-entities-overview.md) | ممكّن بشكل افتراضي |
| التخطيط | [تخطيط متطلبات المواد حسب الطلب (دمرب)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [نظرة عامة على تخطيط متطلبات المواد المدفوعة بالطلب](../master-planning/planning-optimization/ddmrp-overview.md) | إدارة الميزات:<br>*(إصدار أولي) DDMRP لتحسين التخطيط‬* |
| التخطيط | [دعم تحسين التخطيط للوفاء بالوعد (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [حساب تواريخ تسليم أوامر المبيعات باستخدام CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | إدارة الميزات:<br>*(إصدار أولي) CTP لتحسين التخطيط* |
| التخطيط | [دعم تحسين التخطيط لفترة الصلاحية](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [التخطيط الرئيسي للمنتجات التي لها فتره صلاحيه محدوده](../master-planning/planning-optimization/shelf-life.md) | ممكّن بشكل افتراضي |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. وتوفر كل واحدة منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطة الإصدار](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك).

إذا كنت ترغب في تشغيل أي من هذه الميزات أو إيقاف تشغيلها، فيجب عليك القيام بذلك في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | اسم الميزة في إدارة الميزات | معلومات إضافية |
|---|---|---|
| إدارة المخزون والمستودعات | تمكين المتاح بين الشركات الشقيقة لإظهار كمية غير صفرية متاحة فقط | تتيح لك هذه الميزة اختيار ما إذا كان يجب تضمين العناصر التي لا تحتوي على كمية متوفرة في القائمة المتاحة بين الشركات الشقيقة. يمكنك التحكم في هذا الخيار باستخدام إعداد **عدم إظهار العناصر التي لا تحتوي على كمية متوفرة في القائمة المتاحة بين الشركات الشقيقة**، الذي تضيفه هذه الميزة إلى صفحة **معلمات إدارة المستودعات والمخزون**. |
| إدارة المخزون والمستودعات | (الهند) لتحويل قواعد السعر، تجاهل الموقع عند تعيين "من كود المستودع" إلى "الكل" | <p>تنطبق هذه الميزة فقط على ترجمات الهند. يجعل عملية إعداد أسعار التحويل للعناصر الموجودة في عمليات نقل المخزون أكثر سهولة.</p><p>يمكنك إعداد أسعار التحويل من خلال تكوين كل عنصر بقواعد تسعير التحويل. تتمثل إحدى طرق إجراء هذا التكوين في تضمين سطر قاعدة حيث يتم تعيين حقل **من رمز المستودع** إلى *الكل*. يشير هذا الإعداد إلى أنه يجب تطبيق سعر التحويل المحدد بواسطة البند بغض النظر عن المستودع الذي يتم انتقاء الصنف منه. عند تمكين هذه الميزة، قواعد سعر التحويل حيث سيتجاهل حقل **من رمز المستودع** المعين إلى  *الكل* إعداد **المكان**. لذلك، سيتم تطبيق القاعدة بغض النظر عن الموقع المحدد في أمر التحويل. ربما يكون هذا السلوك هو المتوقع، لأن الموقع أسفل المستودع في التدرج الهرمي لأبعاد التخزين.</p><p>بدون هذه الميزة، سيطبق النظام قواعد من هذا النوع فقط عندما يتطابق الموقع الموجود في أمر التحويل تمامًا مع الموقع الذي تم تعيينه للقاعدة. (إذا تم تعيين موقع فارغ للقاعدة، فسيقوم النظام بتطبيق القاعدة فقط على أوامر التحويل التي تحتوي أيضًا على قيمة فارغة للموقع.)</p> |
| إدارة المخزون والمستودعات | تنظيف بيانات تقرير الكمية المتاحة من المخزون | توفر هذه الميزة طريقة لتنظيف البيانات المستخدمة لإنشاء تقارير *تخزين تقارير المخزون المتاح*. |
| التحكم بالإنتاج | تعيين أنشطة المشروع لاتفاقية الخدمة وبنود أمر الخدمة | تضيف هذه الميزة حقلاً يسمى **نشاط المشروع** لاتفاقية الخدمة وبنود أوامر الخدمة، بحيث يمكنك تعيين نشاط المشروع لهم. ستساعد هذه الميزة في منع أخطاء الحظر عند نشر دفاتر يومية مشروع إدارة الخدمة التي تتطلب تعيين نشاط مشروع.  |
| Warehouse management | خدمة انتقاء بند التحويل يدويًا للمسؤول أو مستخدمين موثوقين مماثلين | تتيح هذه الميزة للمسؤولين انتقاء حركات المخزون المرتبطة بخطوط التحويل يدويًا. تتضمن هذه البنود البنود التي تم تحريرها بالفعل إلى المستودع. يجب على المسؤولين القيام بهذا الانتقاء فقط في حالات استثنائية، مثل عندما يكون النظام في حالة تالفة. للحصول على مزيد من المعلومات، راجع [تعامل يدويًا مع استثناءات انتقاء خطوط النقل والمبيعات](../warehousing/manual-order-line-picking-exception-handling.md). |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا بإضافة مقالات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة أن تكون هذه المقالات مرتبطة بالميزات الجديدة التي تمت إضافتها لهذا الإصدار، كما هو موضح في الأقسام السابقة. ومع ذلك، قد تساعدك في الحصول على مزيد من الميزات الموجودة.

| منطقة الميزة | المقالات الجديدة أو المحدثة |
|---|---|
| إدارة التكلفة | [سعر إيصال ثابت](../cost-management/fixed-receipt-price.md) |
| إدارة التكلفة | [الأسئلة المتداولة حول تكاليف المخزون](../cost-management/inventory-costing-faq.md) |
| إدارة التكلفة | [مبدأ المحاسبة ترحيل إلى حساب التكاليف](../cost-management/post-to-charge-account-accounting-principle.md) |
| إدارة المخزون | [تفاصيل حركة المخزون](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.28 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.28 من تطبيقات التمويل والعمليات (أغسطس 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.28، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 1 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 1 لعام 2022](/dynamics365-release-plan/2022wave1/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح المقال [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

