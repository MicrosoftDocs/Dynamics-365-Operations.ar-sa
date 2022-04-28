---
title: ما الجديد أو المتغير في Dynamics 365 Supply Chain Management الإصدار 10.0.19 (يونيو 2021)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.19 من Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f0f1830c9f667d617b8aae28e61a8e541b17c77f
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570314"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>ما الجديد أو المتغير في Dynamics 365 Supply Chain Management الإصدار 10.0.19 (يونيو 2021)

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في إصدار 10.0.19 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.837، وهو يتوفر كما يلي

- **معاينة الإصدار:** أبريل 2021
- **التوفر العام للإصدار (تحديث ذاتي):** يونيو 2021
- **التوفر العام للإصدار (تحديث تلقائي):** يونيو 2021

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. يوفر عمود *الميزة* ارتباطات إلى [خطة الإصدار](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features)، حيث يمكنك الاطلاع على تواريخ الإصدار الرسمية لكل ميزة. يوفر عمود *مزيد من المعلومات* المزيد من التفاصيل و/أو الارتباطات عن المستندات ذات الصلة.

يجب تمكين معظم هذه الميزات باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) قبل التمكن من استخدامها.

| منطقة الميزة | الميزة | معلومات إضافية |
|---|---|---|
| المخزون&nbsp;و&nbsp;اللوجستيات | [الموافقة على التفاصيل المصرفية المقدمة من المورد وحفظها](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [الاحتفاظ بمعلومات الحساب البنكي للمورد](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| المخزون واللوجستيات | [تحسين تصدير كيان بيانات جهة الاتصال‬](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | عند تمكين هذه الميزة، لن تؤدي التغييرات التي تم إجراؤها على البيانات المرجعية إلى تضمين جهات الاتصال ذات الصلة في التصدير المتزايد التالي. عند تعطيل هذه الميزة، لن تؤدي التغييرات التي تم إجراؤها على البيانات المرجعية إلى تضمين جهات الاتصال ذات الصلة في التصدير المتزايد التالي. |
| المخزون واللوجستيات | [تحسينات تدريجية لقدرات تنفيذ المستودعات مع وحدات القياس](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[رسائل معالج الرسالة](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[تسوية مخزون المستودع](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[أحمال عمل إدارة المستودعات لوحدات نطاق السحابة والحافة](../cloud-edge/cloud-edge-workload-warehousing.md) |
| المخزون واللوجستيات | [وظيفة البحث لمقدمة المستند وحقول خاتمة المستند في صفحة عرض أسعار المبيعات](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | تضيف هذه الميزة وظيفة البحث للحقول **مقدمة المستند** و **نتائج المستند** على الصفحة  **عرض أسعار المبيعات**.<br><br>يتم تمكين هذه الميزة افتراضيًا. |
| المخزون واللوجستيات | [‎تنفيذ المستودعات مع وحدات مقياس الحافة على أجهزتك المخصصة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [انشر وحدات مقياس الحافة على أجهزة مخصصة باستخدام LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| التصنيع | [‎تنفيذ التصنيع مع وحدات مقياس الحافة على أجهزتك المخصصة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [انشر وحدات مقياس الحافة على أجهزة مخصصة باستخدام LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| التخطيط | تأكيد الأمر المخطط المستند إلى الاستعلام | [تأكيد أوامر مخططة](../master-planning/planning-optimization/planned-order-firming.md) |
| إدارة معلومات المنتج | [تحسينات صفحة اقتراحات المتغيرات](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [إنشاء متغيرات المنتج المعرفة مسبقًا](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. ويوفر كل منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطه الإصدار](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك). إذا كنت ترغب في استخدام أي من هذه الميزات، يجب عليك تمكينها بشكل صريح في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | الميزة&nbsp;الاسم&nbsp;في إدارة&nbsp;الميزة | معلومات إضافية |
|---|---|---|
| المبيعات والتسويق | تحسينات أداء تنظيف سجل المبيعات | قد يستغرق تنظيف سجل المبيعات وقتًا طويلاً في حالة التشغيل بشكل غير متكرر على بيئات تحتوي على كمية كبيرة من تحديثات المبيعات. لتقليل المدة وتحسين الموثوقية، تقوم هذه الميزة بتقسيم التنظيف إلى مجموعات يتم تشغيلها لمدة محدودة. وكلما أمكن، سيتم جمع قدرات قاعدة البيانات لتقليل التأمين وتجنب ربط جداول المعاملات أثناء التنظيف. لمزيد من المعلومات، راجع [جدولة تنظيف بيانات سجل المبيعات‬](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| المبيعات والتسويق | تحديث تاريخ الإيصال المطلوب بواسطة التاريخ المؤكد للأوامر المشتركة بين الشركات الشقيقة | تتيح لك هذه الميزة التحكم في ما سيحدث لقيم حقول تاريخ المبيعات والشراء عند استخدام التسليم المباشر بين الشركات الشقيقة. يمكنك اختيار ما إذا كان النظام سيقوم بتحديث التواريخ المطلوبة أو تخطي تحديثها. إذا قمت بتخطي التحديث، ستمثل التواريخ المطلوبة ما طلبه العميل. إذا قمت بتمكين التحديث، ستمثل التواريخ المطلوبة في البداية (عند استخدام التحكم في تاريخ التسليم) ما يطلبه العميل فقط. سيعمل التحكم في تاريخ التسليم، عندما يكون مختلفًا عن *بلا*، على إلغاء ما تم طلبه في البداية. يمكنك تعيين هذا الخيار باستخدام الإعداد **تحديث تاريخ إيصال الاستلام المطلوب بالتاريخ المؤكد** في إعدادات العميل أو المورد بين الشركات الشقيقة.<br><br>في حالة تعطيل الميزة، سيقوم النظام بالكتابة فوق تاريخ إيصال الاستلام المطلوب في أوامر المبيعات الأصلية استنادًا إلى قاعدة التحكم في تاريخ التسليم، ولكن سيظل تاريخ الشحن المطلوب كما هو. |
| إدارة المستودعات | تقريب الكميات لأسفل إلى أقرب وحدة مبيعات عند الإصدار إلى المستودع | تضيف هذه الميزة خيارًا يمكن أن يقوم بتقييد كميات الأوامر عند الإصدار لمستودع. عند التمكين، سيتم تقريب كميات أمر الشراء إلى أقرب وحدة مبيعات كاملة، وسيتم رفض الأوامر التي تشتمل على كميات أقل من وحدة مبيعات واحدة للإصدار. |
| إدارة المستودعات | طريقة الموجة "جدولة إنشاء العمل" على مستوى المؤسسة | عند تمكين هذه الميزة، سيتم تكوين أسلوب موجة *جدولة إنشاء العمل* بالتوازي عبر كل الكيانات القانونية. ستتأثر العديد من الإعدادات الإضافية أيضًا. للحصول على التفاصيل الكاملة، راجع [جدولة إنشاء العمل أثناء الموجة](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا باضافه موضوعات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة ان تكون مرتبطة بالميزات الجديدة المضافة لهذا الإصدار ، كما هو موضح في القسم السابق ، ولكن قد يساعدك ذلك علي الحصول علي مزيد من الميزات الموجودة.

| منطقة الميزة | الموضوعات الجديدة أو المحدثة |
|---|---|
| إدارة التغيير الهندسي | [الأسئلة الشائعة حول إدارة التغيير الهندسي](../engineering-change-management/change-management-faq.md) |
| التدبير وتحديد الموارد | [طلبات الفئات من الموردين](../procurement/category-requests-from-vendors.md) |
| إدارة معلومات المنتج | [إدارة وحدة القياس](../pim/tasks/manage-unit-measure.md)<br><br>[حسابات نموذج تكوين المنتج](../pim/config-model-calculations.md) |
| التحكم بالإنتاج | [التسلسل الرقمي الموحد لمعرفات الوظائف](../production-control/unified-job-ids.md) |
| إدارة النقل | [فئات LTL](../transportation/ltl-class.md)<br><br>[أكواد NMFC](../transportation/nmfc-codes.md) |
| إدارة المستودعات، إنشاء الموجة ومعالجتها | [إنشاء الموجة ومعالجتها](../warehousing/wave-processing.md)<br><br>[معلمات المستودع لمعالجة الموجة](../warehousing/wave-warehouse-parameters.md)<br><br>[قوالب الموجة](../warehousing/wave-templates.md)<br><br>[توزيع الموجة](../warehousing/wave-allocation-method.md)<br><br>[جدولة إنشاء العمل أثناء الموجة](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[التعبئة في حاويات](../warehousing/wave-containerization.md)<br><br>[إخطارات تنفيذ الموجة](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.19 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.19 من تطبيقات التمويل والعمليات (يونيو 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.19، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: خطة الموجة 1 لإصدار 2021

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365: خطة الموجة 1 لإصدار 2021](/dynamics365-release-plan/2021wave1/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح الموضوع [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في الموضوع [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
