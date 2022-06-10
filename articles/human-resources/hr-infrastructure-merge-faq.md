---
title: أسئلة شائعة حول دمج البنية الأساسية لـ Dynamics 365 Human Resources
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول دمج البنية الأساسية لتطبيق Microsoft Dynamics 365 Human Resources وتطبيقات التمويل والعمليات.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 766ee49c17749841d8acac6637a0262e87e52e92
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809602"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>أسئلة شائعة حول دمج البنية الأساسية لـ Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



يجيب هذا الموضوع عن الأسئلة المتداولة حول دمج البنية الأساسية لتطبيق Microsoft Dynamics 365 Human Resources وتطبيقات التمويل والعمليات.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>ما هو دمج البنية الأساسية لـ Dynamics 365 Human Resources؟

إن Dynamics 365 Human Resources هو تطبيق مستقل يستخدم بنية أساسية مختلفة عن تطبيقات التمويل والعمليات الأخرى، مثل Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Commerce وDynamics 365 Project Operations. سيؤدي دمج البنية الأساسية إلى جلب Dynamics 365 Human Resources إلى نفس البنية الأساسية لتطبيقات التمويل والعمليات الأخرى.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>قيمة وفوائد دمج البنية الأساسية

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>تستخدم المؤسسة Dynamics 365 Human Resources لإدارة عمليات الموارد البشرية الخاصة بها. ما هي الفوائد التي سنراها من هذه التغييرات؟

- تزيل هذه التغييرات الارتباك الناجم عن مجموعات متعددة من قدرات الموارد البشرية في Dynamics 365.
- فهي توفر Microsoft Power Platform كلا من القابلية للتوسعة، وطريقة لتوسيع منطق العمل وخيارات الميزة.
- فهي تحقق الاتساق بين Dynamics 365 Human Resources وتطبيقات التمويل والعمليات الأخرى من حيث إدارة دورة حياة التطبيق (ALM) وMicrosoft Dynamics Lifecycle Services (LCS) والتوافر الجغرافي وقابلية التوسعة وغيرها.
- فهي تتيح لك الاستفادة من الخدمات والأدوات المشتركة، وتساعد على تقليل التكاليف.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>تستخدم مؤسستي وحدة Human Resources في Dynamics 365 Finance، أو Supply Chain Management، أو Commerce، أو Project Operations. ما هي الفوائد التي سنراها من هذه التغييرات؟

وستكون القدرات والاستثمارات التي تم إجراؤها في Dynamics 365 Human Resources متاحة الآن للعملاء الذين يستخدمون وحدة الموارد البشرية في Dynamics 365 Finance. وتشمل بعض هذه القدرات إدارة الإجازات والغياب، وإدارة الاستحقاقات، وإدارة المهام.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>هل سأفقد أي ميزات أو قدرات أستخدمها حاليا؟

سيكون هناك تكافؤ وظيفي بين Dynamics 365 Human Resources وحدة الموارد البشرية في تطبيقات التمويل والعمليات. Dynamics 365 Human Resources سوف تأخذ الأسبقية لميزات مفضلة. لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>هل ستتغير التجربة بالنسبة للمستخدمين؟

ستتم إدارة قدرات الموارد البشرية الجديدة من خلال إدارة الميزات. سيقرر العملاء ما إذا كانوا يرغبون في استيعابها. في بعض الحالات، قد يتم تعديل القدرات. وفي هذه الحالات، ستقدم الوثائق.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>كيف يؤثر هذا التغيير علي إذا كنت عميلاً موجودًا وأستخدم من وحدة الموارد البشرية في البنية الأساسية لتطبيقات التمويل العمليات وDynamics 365 Human Resources عبر عمليات التكامل المخصصة؟

لن تكون هناك حاجة إلى عمليات تكامل مخصصة بين Dynamics 365 Human Resources الوحدة النمطية للموارد البشرية في Dynamics 365 Finance. ستتواجد جميع بيانات الموارد البشرية في نفس قاعدة البيانات حيث تطبيقات التمويل والعمليات الأخرى.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>الترحيل من Dynamics 365 Human Resources إلى تطبيقات التمويل والعمليات

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>تستخدم مؤسستي Dynamics 365 Human Resources لإدارة عمليات الموارد البشرية الخاصة بها. ما الذي يجب أن نخطط له للهجرة إلى التجربة الجديدة؟

إذا كانت مؤسستك تستخدم Dynamics 365 Human Resources ولكنها لا تستخدم أي تطبيقات تمويل وعمليات أخرى، فسيتم ترحيل بيئة الموارد البشرية إلى البنية الأساسية الجديدة. وسيتم أتمتة جزء كبير من عملية الترحيل هذه. ستكون العمليات في مكان لترحيل قاعدة البيانات ومزامنتها مع البنية الأساسية الجديدة.

بالإضافة إلى ذلك، سيتم وضع الأدوات بحيث يمكنك اختبار عملية الترحيل والتحقق من صحة البيانات والخبرة قبل ترحيل بيئة التشغيل الخاصة بك.

إذا كانت مؤسستك تستخدم Dynamics 365 Human Resources وتطبيقات التمويل والعمليات الأخرى، فعليك التخطيط لمزيد من الوقت للتحقق من الصحة لضمان ترحيل بياناتك بشكل صحيح إلى البيئة الجديدة. سيؤدي الترحيل إلى البنية الأساسية الجديدة إلى دمج البيانات من بيئة الموارد البشرية مع بيئة التمويل والعمليات. ستتطلب البيانات المتضاربة إدخال المستخدم لتحديد كيفية حل التعارض. سيتعين على المستخدمين والمسؤولين إدارة تعيينات البيانات حيث توجد تعارضات واختبار الترحيل في بيئات وضع الحماية قبل ترحيل بيئات الإنتاج.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>تستخدم مؤسستي وحدة Human Resources في Dynamics 365 Finance، أو Supply Chain Management، أو Commerce، أو Project Operations. ما الذي يجب أن نخطط له للهجرة إلى التجربة الجديدة؟

بالنسبة للمؤسسات التي تستخدم وحدة الموارد البشرية في تطبيقات التمويل والعمليات، سيتم تطبيق وظيفة الميزة الجديدة من Dynamics 365 Human Resources على بيئتك من خلال عملية تحديث One Version القياسية. يمكنك توقع رؤية الوظيفة الجديدة في البيئة الخاصة بك كما تصبح متوفرة في كل تحديث. يمكنك استخدام إدارة الميزات لتشغيل ميزات جديدة، ولكن يجب أن تخطط للتحقق من صحة هذه الميزات. اتبع العمليات التي لديك في مكان للتحقق من صحة التحديثات الأخرى إلى البيئة الخاصة بك. لمزيد من المعلومات حول كيفية تطبيق التحديثات على تطبيقات التمويل والعمليات، راجع [نظرة عامة على One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>متى سيتم ترحيل المؤسسة الخاصة بي؟

يعتمد الترحيل لكل مؤسسة على التكوين الحالي والاستعداد للانتقال إلى البنية الأساسية الجديدة. هذه التواريخ عرضة للتغيير.

- ستتلقى المؤسسات التي تستخدم وحدة الموارد البشرية في تطبيقات التمويل والعمليات وظائف الموارد البشرية في Dynamics 365 Human Resources كجزء من عملية تحديث One Version العادية. ومن المقرر أن تصبح الميزات الجديدة متاحة بشكل عام ابتداء من يناير 2022.
- وستتاح للمؤسسات التي تستخدم فقط Dynamics 365 Human Resources إمكانية الوصول إلى أدوات الترحيل حتى تتمكن من بدء اختبار الترحيل وبدءه في منتصف عام 2022. لم يتم بعد تحديد تاريخ إتمام الترحيل إلى البنية الأساسية الجديدة. ومع ذلك، سيكون على الأقل سنة واحدة بعد التاريخ عندما تصبح أدوات الترحيل متوفرة.
- وستتاح للمؤسسات التي تستخدم Dynamics 365 Human Resources وتطبيقات التمويل والعمليات الأخرى إمكانية الوصول إلى أدوات الترحيل حتى تتمكن من اختبار وبدء الترحيل في منتصف عام 2022. لم يتم بعد تحديد تاريخ إتمام الترحيل إلى البنية الأساسية الجديدة. ومع ذلك، سيكون على الأقل سنة واحدة بعد التاريخ عندما تصبح أدوات الترحيل متوفرة.

لمزيد من المعلومات حول الميزات الجديدة لـ Dynamics 365 Human Resources، راجع [ما الجديد أو الذي تم تغييره في الموارد البشرية](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>لم يتم تشغيل مؤسستي بعد على Dynamics 365 Human Resources. هل يجب أن نباشر البدء الفوري مع وحدة الموارد البشرية في تطبيقات التمويل والعمليات أو مع تطبيق Dynamics 365 Human Resources على البنية الأساسية القديمة؟

العناصر الهامة التي يجب مراعاتها هي وظيفة الموارد البشرية المطلوبة ومتى ستكون هذه الوظيفة متاحة على البنية التحتية الجديدة. إذا احتاجت المؤسسة إلى الوظيفة الأساسية لإدارة شؤون الموظفين، فهذه متاحة حاليًا في وحدة الموارد البشرية لتطبيقات التمويل والعمليات في البنية الأساسية الجديدة. ومن المتوقع أن يكون التكافؤ بين وحدة الموارد البشرية لتطبيقات التمويل والعمليات وتطبيق Dynamics 365 Human Resources في الإصدار 10.0.25، والذي من المقرر أن يكون متاحًا بشكل عام في مارس 2022. ستتوفر ميزات التكامل مثل تكاملات تطبيق Teams وكيان Dataverse في الإصدارات اللاحقة.

إذا كان من المتوقع أن تصبح وظائف الموارد البشرية للمؤسسة متاحة على البنية الأساسية الجديدة ضمن الإطار الزمني للبدء الفوري للمؤسسة، فقد يكون من الأسهل بدء تشغيل وحدة الموارد البشرية في تطبيقات التمويل والعمليات. سينتج عن ذلك ترحيل أسهل لأنه سيكون ترقية قياسية لتطبيق Dynamics 365 Human Resources وسيكون العميل موجودًا بالفعل في البنية الأساسية الجديدة. إذا قررت المؤسسة بدء العمل على تطبيق Dynamics 365 Human Resources على البنية التحتية القديمة، فستكون هناك حاجة إلى ترحيل البيئة للانتقال إلى البنية الأساسية الجديدة. ويمكن تجنب ذلك من خلال العيش على البنية التحتية الجديدة.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>أنا أستخدم قدرات جديدة متوفرة فقط في Dynamics 365 Human Resources (مثل **إجازة والغياب** و **إدارة الفوائد**). هل ستتوفر هذه القدرات الآن في وحدة الموارد البشرية على البنية الأساسية للتمويل والعمليات أيضًا؟

نعم، ستعمل جميع الوحدات من Dynamics 365 Human Resources كما هي في تطبيقات التمويل والعمليات، وسيكون هناك تكافؤ في الميزات بنسبة 100 في المائة. كجزء من استراتيجية الترحيل الشاملة للعملاء الذين يستخدمون هذه القدرات حاليًا في الموارد البشرية، سيتم ترحيل بيانات العملاء بحيث تستمر في العمل على البنية الأساسية لتطبيقات التمويل والعمليات.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>يمكنني استخدام قدرات إدارة فوائد Dynamics 365 Human Resources الجديدة. لقد بنيت التكامل المخصص مع وحدة الموارد البشرية على البنية الأساسية لتطبيقات التمويل والعمليات حتى أتمكن من الاستفادة من قدرات الرواتب باستخدام بيانات الفوائد. هل ستكون هذه التكاملات المخصصة مطلوبة للمضي قدما؟

كجزء من دمج البنية الأساسية، يتم إحضار بيانات الموارد البشرية إلى نفس قاعدة بيانات تطبيقات التمويل والعمليات الأخرى. لن يكون التكامل بين الوحدات النمطية في تطبيقات التمويل والعمليات مطلوبًا بعد الآن.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>تستخدم المؤسسة الخاصة بي حل ISV واحد أو أكثر مع Dynamics 365 Human Resources. هل سيتم ترحيل حلول ISV تلقائيا؟

تختلف تجربة الترحيل لكل مورد برامج مستقل (ISV) الحل، اعتمادا على أسلوب التكامل للحل. ستعمل Microsoft بشكل وثيق مع ISVs لضمان الانتقال السلس إلى البنية الأساسية الجديدة.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>تستخدم منظمتي تكامل LinkedIn Talent Hub مع Dynamics 365 Human Resources. هل سيستمر هذا التكامل في العمل بعد اكتمال تغيير البنية الأساسية؟

لا، لن يعمل تكامل LinkedIn Talent Hub بعد الانتقال إلى البنية التحتية الجديدة. سيتم إيقاف خدمة تكامل LinkedIn Talent Hub مع البنية الأساسية القديمة لـ Dynamics 365 Human Resources.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>تستخدم منظمتي تطبيق الموارد البشرية لـ Teams. هل سيستمر هذا التطبيق في العمل بعد اكتمال تغيير البنية الأساسية؟

نعم، سيستمر تطبيق الموارد البشرية في العمل بعد الترحيل إلى البنية الأساسية الجديدة.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>قامت مؤسستي بتكوين أمان مخصص في Dynamics 365 Human Resources. هل سيظل أماننا المخصص مطبقا بعد اكتمال تغيير البنية الأساسية؟

نعم، سيتم تضمين تكوينات الأمان المخصصة في ترحيل البيانات إلى البنية الأساسية الجديدة.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>نحن نستخدم أداة تكامل البيانات لنقل البيانات بين Dynamics 365 Human Resources وتطبيقات التمويل والعمليات. كيف ستتأثر البيانات التي يتم دمجها حاليا؟

تتم مزامنة بيانات الموارد البشرية الموجودة حاليا في Dynamics 365 Human Resources مع Dataverse. يمكن بعد ذلك استخدام أداة تكامل البيانات للتزامن أحادي الاتجاه مع تطبيقات التمويل والعمليات. بعد الترحيل إلى البنية الأساسية الجديدة، ستكون بيانات الموارد البشرية أصلية في لتطبيقات التمويل والعمليات. لن تعود أداة تكامل البيانات مطلوبة لمزامنة البيانات بين تطبيقات التمويل والعمليات والموارد البشرية.

ستستمر جداول البيانات الأصلية Dataverse الحالية للموارد البشرية في مزامنة البيانات من البيئة على البنية الأساسية الجديدة. سيتم تحويل الكيانات لدعم الكتابة المزدوجة. أي تكاملات بيانات أخرى تم تكوينها عبر "تكامل البيانات" مقابل هذه الجداول لتطبيقات Dynamics 365 الأخرى ستستمر في العمل كما تم تكوينها حاليا.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>نحن نستخدم الكتابة المزدوجة لنقل بيانات الموارد البشرية بين Dataverse وتطبيقات التمويل والعمليات الأخرى. كيف ستتأثر البيانات التي يجري دمجها حاليا بالهجرة إلى البنية الأساسية الجديدة؟

ستكون بيانات الموارد البشرية أصلية في تطبيقات التمويل والعمليات في البيئة على البنية الأساسية الجديدة. سيتم استخدام الكتابة المزدوجة لنقل بيانات الموارد البشرية بين البيئة الجديدة وبيئة Dataverse.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>لقد بنينا تكاملات مخصصة من Dynamics 365 Human Resources إلى نظام خارجي واحد أو أكثر. هل سنستمر في تطوير التكامل الجديد بعد اكتمال تغيير البنية الأساسية؟

يعتمد ذلك على نقطة نهاية التكامل. لمزيد من المعلومات حول تقنيات التكامل المتوفرة في تطبيقات التمويل والعمليات، وكيفية اختيار أفضل تقنية تكامل، راجع [نظرة عامة على التكامل](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>لقد مددنا Dataverse لـ Dynamics 365 Human Resources. هل سيتم ترحيل هذه التمديدات تلقائيا؟

إذا كانت بيئات Dynamics 365 Human Resources والتمويل والعمليات التي ستنضم إلى البيئة على البنية الأساسية الجديدة متصلة ببيئة Dataverse نفسها، فسيستمر اتصال التطبيقين ببيئة Dataverse نفسها بعد الترحيل. لن يلزم ترحيل أي ملحقات Dataverse.

لكن، إذا كانت بيئات Dynamics 365 Human Resources والتمويل والعمليات متصلة حاليًا ببيئات Dataverse منفصلة، فيجب أن يتم ضم بيئتي Dataverse بحيث تتصلان ببيئة واحدة على البنية الأساسية. لترحيل Dataverseهذا، يمكن توصيل جداول Dataverse القياسية إلى حلول الموارد البشرية وإعادة مزامنتها مع بيئة Dataverse الجديدة. لن يتم ترحيل أي ملحقات لبيئة Dataverse تلقائيا ولكن يجب إعادة نشرها في البيئة الجديدة. نوصي باستخدام الحلول المدارة لإدارة إضافات Dataverse. لمزيد من المعلومات، راجع [مقدمة للحلول](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-utilized-the-custom-field-functionality-within-dynamics-365-human-resources-will-those-custom-fields-migrate-automatically"></a>لقد استخدمنا وظيفة الحقول المخصصة في Dynamics 365 Human Resources، هل سيتم ترحيل هذه الحقول المخصصة تلقائيًا؟
نعم، سيتم ترحيل الحقول المخصصة التي تمت اضافتها إلى البنية الأساسية الجديدة.

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>لقد قمنا بتكوين تدفقات Microsoft Power Automate و/أو Microsoft Power Apps للعمل مع Dynamics 365 Human Resources. هل سيتم ترحيل مكونات Microsoft Power Platform هذه والعمل تلقائيا بعد اكتمال تغيير البنية الأساسية؟

تدفقات Power Apps، Power Automate، وتخصيصات Microsoft Power Platform الأخرى مشابهة لإضافات Dataverse. يتوقف عملها بعد الترحيل بشكل تلقائي إلى البنية الأساسية الجديدة على ما إذا كان تطبيق الموارد البشرية وتطبيقات التمويل والعمليات متصلة ببيئة Power Apps نفسها قبل الترحيل.

إذا كانت التطبيقات متصلة حاليا بنفس بيئة Power Apps، فسيستمر اتصالها ببيئة Power Apps تلك بعد الترحيل إلى البنية الأساسية الجديدة. في هذه الحالة، سوف تستمر عمليات التدفق Power Apps, Power Automate وتخصيصات Microsoft Power Platform الأخرى في العمل بدون أي تكوين إضافي. نوصي باستخدام الحلول المدارة لإدارة إضافات التطبيقات على Dataverse. لمزيد من المعلومات، راجع [مقدمة للحلول](/powerapps/developer/data-platform/introduction-solutions).

ومع ذلك، إذا كان تطبيق الموارد البشرية وتطبيقات التمويل والعمليات متصلة ببيئات Power Apps منفصلة، فيجب ضمها كجزء من الترحيل. تتطلب هذه المهمة إعادة توزيع Power Apps والتخصيصات الأخرى في البيئة الجديدة.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>لقد قمنا بتمكين جداول Dataverse ظاهرية لـ Dynamics 365 Human Resources. ماذا سيحدث لهذه الجداول أثناء الترحيل؟

بعد الترحيل، إذا ظلت البيئة على البنية التحتية الجديدة متصلة ببيئة Dataverse المتصلة حاليا بـ Dynamics 365 Human Resources، فإن جداول Dataverse الظاهرية التي تم إنشاؤها في تلك البيئة ستستمر في العمل بدون أي تكوين إضافي.

ومع ذلك، إذا كانت البيئة على البنية الأساسية الجديدة متصلة ببيئة Dataverse مختلفة بعد الترحيل، يجب إعادة إنشاء الجداول الظاهرية في بيئة Dataverse الجديدة.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>لقد قمنا بتطوير تكامل باستخدام واجهة برمجة تطبيقات نظام تتبع المتقدمين (ATS) أو واجهة برمجة تطبيقات الرواتب والجداول Dataverse الافتراضية لـ Dynamics 365 Human Resources ، أو كيانات أخرى في واجهة برمجة تطبيقات الويب لـ Dataverse. هل ستستمر هذه التكاملات في العمل بعد اكتمال تغيير البنية الأساسية؟

بعد الترحيل، إذا ظلت البيئة على البنية التحتية الجديدة متصلة ببيئة Dataverse المتصلة حاليا بـ Dynamics 365 Human Resources، فإن أية تكاملات تم تطويرها بناء على واجهة برمجة تطبيقات الويب لـ Dataverse ستستمر في العمل بعد انتهاء التكامل.

لكن، إذا ظلت البيئة على البنية التحتية الجديدة متصلة ببيئة Dataverse مختلفة بعد الترحيل، فإن أية تكاملات تم تطويرها بناء على واجهة برمجة تطبيقات الويب لـ Dataverse ستحتاج إلى إعادة تكوين لتتصل ببيئة Dataverse الجديدة.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>هل هناك تأثير على منطقة Azure عند ترحيل البيئة الخاصة بي؟

من المتوقع أن تبقى بيئة الموارد البشرية الخاصة بك عادة في نفس المنطقة Azure أثناء الترحيل. يحدث الاستثناء الوحيد إذا كان سيتم دمج بيئة الموارد البشرية مع بيئة التمويل والعلميات في منطقة مختلفة. وفي هذه الحالة، سيتم ترحيل بيئة الموارد البشرية إلى منطقة Azure في بيئة التمويل والعمليات.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>تعتمد مؤسستي على مهام سير العمل في Dynamics 365 Human Resources لعملية عمل واحدة أو أكثر. هل سيتم ترحيل عمليات سير العمل هذه تلقائيا؟

نعم، سيتم ترحيل تكوينات سير العمل ومحفوظات سير العمل وسير العمل الحالي قيد التنفيذ.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>ما التدريب والموارد التي ستتوفر للمساعدة في عملية الترحيل؟

سيتم توفير الوثائق الكاملة لوصف كل خطوة من عملية الترحيل بالتفصيل. وقد تتوفر أيضا موارد تدريبية إضافية، مثل أشرطة الفيديو وحلقات العمل، حسب الحاجة.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>أنشأت المؤسسة طرق عرض Dynamics 365 Human Resources محفوظة لتحسين قابلية استخدام الواجهة. هل سيتم ترحيل طرق العرض المحفوظة هذه تلقائيا؟

نعم، سيتم ترحيل طرق العرض المحفوظة إلى البنية الأساسية الجديدة.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>نحن نستخدم Ceridian مع Dynamics 365 Human Resources. هل سيستمر تكامل Ceridian هذا متاحًا بعد اكتمال تغيير البنية الأساسية؟ 

سيتم ترحيل التكامل مع Ceridian إلى التكامل المستندة إلى واجهة برمجة التطبيقات الرواتب. لن يتم ترحيل التكامل المستند إلى الملفات الموجود حاليًا في Dynamics 365 Human Resources إلى البنية الأساسية لتطبيقات التمويل والعمليات. لمزيد من المعلومات، راجع [مقدمة لواجهة برمجة تطبيقات كشف الرواتب](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>كيف ستؤثر عملية الترحيل على عملية تحديث الخدمة؟

بعد الترحيل، سيكون لدى العملاء مرونة أكبر بكثير من حيث ALM وتحديثات الخدمة. لن يتم تطبيق تحديثات الخدمة تلقائيا على بيئات الموارد البشرية. بدلا من ذلك، ستتبع الخدمة عمليات تحديث خدمة الإصدار واحد والوظائف. لذلك، ستكون خيارات التكوين للتحديثات متوفرة من خلال LCS. لمزيد من المعلومات، راجع [نظرة عامة حول One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>كيف ستؤثر الهجرة على مشروع LCS الخاص بي لـ Dynamics 365 Human Resources؟

سيؤدي الترحيل إلى البنية الأساسية إلى نقل إدارة بيئات Dynamics 365 Human Resources إلى مشروع تنفيذ التمويل والعمليات في LCS. إذا كان الترحيل يعمل على دمج Dynamics 365 Human Resources مع بيئة التمويل والعمليات الموجودة، فسيتم دمج مشروع LCS للموارد البشرية في مشروع تطبيق LCS لتطبيق التمويل والعمليات. إذا كنت تستخدم Dynamics 365 Human Resources حاليا فقط، سيتم إنشاء مشروع تنفيذ LCS جديد، وسيتم ترحيل مشروع LCS للموارد البشرية الحالي إلى المشروع الجديد.

سيكون المشروع الجديد هو نفس نوع المشروع الذي تستخدمه تطبيقات التمويل والعمليات. وسوف يكون لها نفس الميزات والوظائف لإدارة البيئة. للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>لقد ربطنا تسجيلات مهامنا بأداة تكوين عمليات الأعمال في الموارد البشرية. كيف سيتم ترحيل "أداة تكوين عمليات الأعمال" ودمجه في LCS؟

سيتم ترحيل مكتبات العمليات التجارية لمشروع LCS إلى مشروع LCS الجديد للموارد البشرية.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>تستخدم المؤسسة حاليا فقط Dynamics 365 Human Resources. ما هي الموارد المتاحة حتى نتمكن من معرفة المزيد عن قدرات التطوير بعد اكتمال تغيير البنية الأساسية؟

وستكون خيارات قابلية التوسعة في Microsoft Power Platform وخيارات قابلية التوسعة في التمويل والعمليات متاحة ويمكن استخدامها لأغراض التطوير. لمزيد من المعلومات، راجع [تطوير الصفحة الرئيسية وتخصيصها](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>لقد قمنا بتمكين الميزات في Dynamics 365 Human Resources. هل سيتم تمكين هذه الميزات تلقائيا أثناء الترحيل؟

سيتم تحديد ما إذا كان يتم تمكين ميزة تلقائيا في البنية الأساسية الجديدة بشكل فردي لكل ميزة. سيتم تضمين هذه المعلومات في وثائق الميزة.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>ماذا يحدث لقاعدة بيانات BYOD الخاصة بي أثناء الترحيل؟

استيراد وتصدير التكوينات لإحضار قاعدة البيانات الخاصة بك (BYOD) سيتم ترحيلها إلى البنية الأساسية الجديدة.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>ماذا يحدث لـ Azure Data Lake الخاص بي أثناء الترحيل؟

ستحافظ أي عملية تصدير يتم تكوينها حاليًا لـ Azure Data Lake Storage في تطبيقات التمويل والعمليات على نفس التكوين بعد الترحيل.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>نحن نستخدم حاليا Dynamics AX 2012. هل سيتم استخدام أدوات الترقية المتوفرة حاليا لترقية وحدة الموارد البشرية في AX 2012 إلى Dynamics 365 Human Resources؟

نعم. سيتم تضمين Dynamics 365 Human Resources في قاعدة التعليمات البرمجية المدمجة والبنية الأساسية لتطبيقات التمويل والعمليات. سوف تستخدم الترقية من Dynamics AX 2012 إلى Dynamics 365 Human Resources نفس مسار الترقية والأدوات المستخدمة للترقية إلى أحدث إصدار من تطبيقات التمويل والعمليات.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>نحن نستخدم معالجة المستندات مع Dynamics 365 Human Resources. ماذا سيحدث للمستندات أثناء الترحيل؟

ستبقى المستندات في مخزن المستندات الموجود. وسيتم إعادة تشكيلها للبيئة في البنية الأساسية الجديدة.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>ماذا يحدث لوظائف الدفعة التي قمنا بتكوينها في Dynamics 365 Human Resources بعد الترحيل؟

سيتم ترحيل مهام الدفعات القابلة للتطبيق تلقائيا إلى البنية الأساسية الجديدة.

## <a name="licensing-impact"></a>تأثير الترخيص

لا تحل هذه الوثائق محل أي من الوثائق القانونية التي تغطي حقوق الاستخدام أو تحل محلها.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>تستخدم المؤسسة Dynamics 365 Human Resources لإدارة عمليات الموارد البشرية الخاصة بها. هل يتغير ترخيصنا أو التكلفة؟

لن يتأثر العملاء الذين اشتروا تراخيص Dynamics 365 Human Resources. لا يوجد ترحيل ترخيص لهؤلاء العملاء. ولن تكون وحدة حفظ المخزون (SKU) الإضافية الخاصة بالموارد البشرية قابلة للتطبيق بعد الآن. بدلاً من ذلك، يمكن للعملاء اختيار شراء بيئة اختبار معزولة من المستوى 2 لتطبيقات التمويل والعمليات بتكلفة أقل بعض الشيء. سيتم ترحيل العملاء الحاليين الذين اشتروا بيئة اختبار معزولة من المستوى 2 للموارد البشرية إلى بيئة اختبار من المستوى 2 لتطبيقات التمويل والعمليات دون أي تكلفة إضافية.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>تستخدم مؤسستي وحدة Human Resources في Dynamics 365 Finance، أو Supply Chain Management، أو Commerce، أو Project Operations. هل يتغير ترخيصي أو التكلفة؟

بإمكان المستخدمين الحاليين لتطبيقات Dynamics 365 ومستخدمي تطبيقات Dynamics 365 Finance وSupply Chain Management وCommerce وProject Operations المستقلة الوصول إلى Human Resources كجزء من هذه التراخيص حتى فبراير 2025 أو حتى انتهاء صلاحية اتفاقية الترخيص الحالية، أيهما أبكر. يمكنك اختيار الانتقال إلى تراخيص الموارد البشرية في وقت سابق إذا كان يساعدك على تحقيق وفورات أفضل في التكاليف. اعتبارًا من فبراير 2025، يجب على جميع عملاء CSP و EA الحاليين إيقاف تشغيل وحدة الموارد البشرية وشراء تراخيص الموارد البشرية للاستفادة من القدرات الجديدة التي يتم إحضارها إلى تطبيقات التمويل والعمليات.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>تستخدم مؤسستي البث المباشر مع Dynamics 365 Finance أو Supply Chain Management أو Commerce أو Project Operations. هل سيطلب منا شراء بيئة إضافية لدعم دمج البنية الأساسية؟

لا يلزم توفير بيئات إضافية لدعم تغيير البنية الأساسية.

